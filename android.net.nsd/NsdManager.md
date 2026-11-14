Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NsdManager

```
class NsdManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.nsd.NsdManager](NsdManager.md) |

Provides APIs for discovering and advertising network services on the local network.

Network Service Discovery (NSD) allows applications to find other devices on a local network that support the services the application is interested in. For example, a game can find other players on the same local network, or a document viewer can find printers.

The implementation is based on DNS Service Discovery (DNS-SD) as described in [RFC 6763](http://www.ietf.org/rfc/rfc6763.txt), and operates over Multicast DNS (mDNS).

### SDK Extensions

The `NsdManager` API is updated via [SDK extensions](https://developer.android.com/guide/sdk-extensions). This allows newer features and APIs to be available on devices running older versions of Android. Applications should generally use SDK extension version checks instead of SDK version (`https://developer.android.com/reference/kotlin/android/os/Build.VERSION.html#`) checks when interacting with `NsdManager`.

### Usage Patterns

The API is asynchronous. Requests are made to the system, and results are returned through listener or callback interfaces.

#### Discovering and Tracking Services

The easiest way to find and maintain an up-to-date list of services is to use registerServiceInfoCallback. This API, available starting from "T extensions 22" (which covers all Android 14+ devices), combines discovery and resolution into a single operation. It automatically notifies the app when a service is found, when its properties (like IP addresses or TXT records) change, and when it becomes unavailable.

On older devices, or if an app needs fine-grained control over which services to resolve, use overloads of #discoverServices with a `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.DiscoveryListener`, then call registerServiceInfoCallback or #resolveService for the specific services of interest.

#### Advertising Services

To make a service on the current device discoverable by others, use #registerService. The app provides an NsdServiceInfo containing the service name, type, and port.

### Wi-Fi Multicast Lock

Performing mDNS operations on Wi-Fi requires the device to receive multicast packets.

- **Before T extensions 7** (Android 12 and below devices, and Android 13 devices that have not received the T extensions 7 update): Apps must manually acquire a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.MulticastLock.html#` to receive mDNS packets, even when the app is in the foreground.
- **Starting from T extensions 7**: The system automatically manages multicast reception for apps in the foreground. Background apps should still avoid taking the lock unless absolutely necessary to minimize battery impact.

### Local network permission (Android 17+)

Starting with API 37, access to the local network is restricted.

Applications targeting API 37 or higher generally require the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_LOCAL_NETWORK:kotlin.String` permission to communicate with local devices. However, `NsdManager` provides a way to gain access to specific services without this broad permission:

1. An app calls #discoverServices or #registerServiceInfoCallback with the `https://developer.android.com/reference/kotlin/android/net/nsd/DiscoveryRequest#FLAG_SHOW_PICKER:kotlin.Long` flag. This triggers a system-provided UI allowing the user to choose a specific service.
2. Once the user selects a service, the app is granted permission to communicate with that specific device through getHostAddresses on getNetwork. The app can also receive updates for that service without requiring the `ACCESS_LOCAL_NETWORK` permission by calling registerServiceInfoCallback. This grant persists across reboots.
3. If the `https://developer.android.com/reference/kotlin/android/net/Network.html#` reconnects or the service changes addresses, apps must use registerServiceInfoCallback to obtain up-to-date IP addresses with the grant applied. Apps should avoid storing service IP addresses as they can change over time.
4. Apps can use checkPermissionForService to verify if they still have access to a previously selected service.
5. To rediscover previously approved services without showing the UI again, apps can use `https://developer.android.com/reference/kotlin/android/net/nsd/DiscoveryRequest#FLAG_USER_APPROVED_ONLY:kotlin.Long`.

### Example finding and resolving a single service

```kotlin
<code>// Discover a service for a given service type, with an optional name filter. Consider
  // calling in a withTimeout block.
  suspend fun findService(serviceType: String, nameFilter: PatternMatcher?): NsdServiceInfo? {
      if (SdkExtensions.getExtensionVersion(Build.VERSION_CODES.TIRAMISU) &lt; 22) {
          return findServiceLegacy(serviceType, nameFilter)
      }
      // Note the Wi-Fi multicast lock is not necessary for foreground discovery in recent SDKs
      // Using kotlinx-coroutines-core
      return suspendCancellableCoroutine { cont -&gt;
          val request = DiscoveryRequest.Builder(serviceType)
              .setServiceNameFilter(nameFilter)
              .setFlags(DiscoveryRequest.FLAG_SHOW_PICKER)
              .build()
 
          val listener = object : NsdManager.ServiceInfoCallback {
              override fun onServiceUpdated(serviceInfo: NsdServiceInfo) {
                  if (cont.isActive) cont.resume(serviceInfo)
                  // With FLAG_SHOW_PICKER only the selected service is returned, the
                  // listener is then unregistered automatically
              }
 
              override fun onServiceInfoCallbackRegistrationFailed(errorCode: Int) {
                  cont.resumeWithException(DiscoveryException(errorCode))
              }
 
              override fun onServiceInfoCallbackUnregistered() {
                  // This will be called if the user dismisses the picker without selecting
                  if (cont.isActive) cont.resume(null)
              }
          }
 
          nsdManager.registerServiceInfoCallback(request, Runnable::run, listener)
          cont.invokeOnCancellation {
              // unregistration is safe to call multiple times on SDK Ext 22+
              nsdManager.unregisterServiceInfoCallback(listener)
          }
      }
  }
 
  private suspend fun findServiceLegacy(
      serviceType: String, nameFilter: PatternMatcher?): NsdServiceInfo? {
      val tiramisuExt = SdkExtensions.getExtensionVersion(Build.VERSION_CODES.TIRAMISU)
      val lock = if (tiramisuExt &lt; 7) {
          getSystemService(WifiManager::class.java)
              .createMulticastLock("MyAppTag").apply { acquire() }
      } else {
          null
      }
 
      try {
          val discoveredService = suspendCancellableCoroutine { cont -&gt;
              val discoveryListener = object : NsdManager.DiscoveryListener {
                  override fun onServiceFound(info: NsdServiceInfo) {
                      // onServiceFound may be called multiple times
                      if (!cont.isActive) return
                      // Apps implement their own logic to select which discovered service
                      // to use. They may show a UI selector to the user, or have some
                      // custom name filtering to identify the service as assumed here.
                      if (nameFilter?.match(info.serviceName) == false) return
                      try {
                          // This may throw IllegalArgumentException on older SDKs if
                          // discovery was stopped already
                          nsdManager.stopServiceDiscovery(this)
                      } catch (_: IllegalArgumentException) {}
                      cont.resume(info)
                  }
                  override fun onStartDiscoveryFailed(type: String, err: Int) {
                      cont.resumeWithException(DiscoveryException(err))
                  }
                  override fun onDiscoveryStarted(type: String) {}
                  override fun onDiscoveryStopped(type: String) {}
                  override fun onServiceLost(info: NsdServiceInfo) {}
                  override fun onStopDiscoveryFailed(type: String, err: Int) {}
              }
              nsdManager.discoverServices(
                  serviceType, NsdManager.PROTOCOL_DNS_SD, discoveryListener)
              cont.invokeOnCancellation {
                  try {
                      nsdManager.stopServiceDiscovery(discoveryListener)
                  } catch (_: IllegalArgumentException) {}
              }
          }
 
          return suspendCancellableCoroutine { cont -&gt;
              val resolveListener = object : NsdManager.ResolveListener {
                  override fun onServiceResolved(info: NsdServiceInfo) {
                      cont.resume(info)
                  }
                  override fun onResolveFailed(info: NsdServiceInfo, err: Int) {
                      cont.resumeWithException(DiscoveryException(err))
                  }
              }
              nsdManager.resolveService(discoveredService, resolveListener)
              cont.invokeOnCancellation {
                  if (tiramisuExt &gt;= 7) {
                      try {
                          nsdManager.stopServiceResolution(resolveListener)
                      } catch (_: IllegalArgumentException) {}
                  }
              }
          }
      } finally {
          lock?.release()
      }
  }
  </code>
```

### Example re-finding a previously discovered service

```kotlin
<code>// Fetch the latest service information (such as IP addresses) for a service that was
  // previously discovered and saved in the app. This should typically be used before
  // each connection to the service to fetch up-to-date NsdServiceInfo#getHostAddresses()
  // and NsdServiceInfo#getNetwork(). Consider calling in a withTimeout block.
  suspend fun findKnownService(serviceType: String, serviceName: String): NsdServiceInfo? {
      if (SdkExtensions.getExtensionVersion(Build.VERSION_CODES.TIRAMISU) &lt; 22) {
          return findKnownServiceLegacy(serviceType, serviceName)
      }
      val hasPermission = if (Build.VERSION.SDK_INT &lt; Build.VERSION_CODES.CINNAMON_BUN) {
          true
      } else suspendCancellableCoroutine { cont -&gt;
          nsdManager.checkPermissionForService(serviceName, serviceType, Runnable::run) {
              cont.resume(it == NsdManager.SERVICE_PERMISSION_GRANTED)
          }
      }
      if (!hasPermission) {
          // Trigger FLAG_SHOW_PICKER flow for the user to reselect the service
          return findService(serviceType,
              PatternMatcher(serviceName, PatternMatcher.PATTERN_LITERAL))
      }
 
      return suspendCancellableCoroutine { cont -&gt;
          val listener = object : NsdManager.ServiceInfoCallback {
              override fun onServiceUpdated(serviceInfo: NsdServiceInfo) {
                  if (!cont.isActive) return // onServiceUpdated may be called multiple times
                  cont.resume(serviceInfo)
                  nsdManager.unregisterServiceInfoCallback(this)
              }
 
              override fun onServiceInfoCallbackRegistrationFailed(errorCode: Int) {
                  cont.resumeWithException(DiscoveryException(errorCode))
              }
 
              override fun onServiceInfoCallbackUnregistered() {}
          }
 
          val serviceToFind = NsdServiceInfo().apply {
              this.serviceName = serviceName
              this.serviceType = serviceType
              // Set to find on specific Networks, see ConnectivityManager#requestNetwork
              // this.network = network
          }
          nsdManager.registerServiceInfoCallback(
              serviceToFind, Runnable::run, listener)
          cont.invokeOnCancellation {
              nsdManager.unregisterServiceInfoCallback(listener)
          }
      }
  }
 
  private suspend fun findKnownServiceLegacy(
      serviceType: String, serviceName: String): NsdServiceInfo? {
      val tiramisuExt = SdkExtensions.getExtensionVersion(Build.VERSION_CODES.TIRAMISU)
      return suspendCancellableCoroutine { cont -&gt;
          val lock = if (tiramisuExt &lt; 7) {
              getSystemService(WifiManager::class.java)
                  .createMulticastLock("MyAppTag").apply { acquire() }
          } else {
              null
          }
          try {
              val listener = object : NsdManager.ResolveListener {
                  override fun onResolveFailed(serviceInfo: NsdServiceInfo, errorCode: Int) {
                      cont.resumeWithException(DiscoveryException(errorCode))
                  }
 
                  override fun onServiceResolved(serviceInfo: NsdServiceInfo) {
                      if (cont.isActive) cont.resume(serviceInfo)
                  }
              }
              val serviceToFind = NsdServiceInfo().apply {
                  this.serviceName = serviceName
                  this.serviceType = serviceType
              }
              nsdManager.resolveService(serviceToFind, listener)
              cont.invokeOnCancellation {
                  if (SdkExtensions.getExtensionVersion(Build.VERSION_CODES.TIRAMISU) &gt;= 7) {
                      try {
                          nsdManager.stopServiceResolution(listener)
                      } catch (_: IllegalArgumentException) {
                      }
                  }
              }
          } finally {
              lock?.release()
          }
      }
  }
  </code>
```

### Example advertising a service

```kotlin
<code>// Advertise a service for other devices to connect to the current device. This should be called
  // after opening a listening socket to handle connections from other devices, on a dynamic port
  // to avoid conflicts. Note this always requires the ACCESS_LOCAL_NETWORK permission.
  fun advertiseService(portNumber: Int): Pair&lt;NsdManager.RegistrationListener, MulticastLock?&gt; {
      // The Wi-Fi multicast lock is not necessary for advertising on Wi-Fi while in the
      // foreground since SDK extension 7
      val lock = if (SdkExtensions.getExtensionVersion(Build.VERSION_CODES.TIRAMISU) &lt; 7) {
          getSystemService(WifiManager::class.java).createMulticastLock("MyAppTag").apply {
              acquire()
          }
      } else null
 
      val service = NsdServiceInfo().apply {
          serviceName = "My service name"
          serviceType = "_servicetype._tcp"
          port = portNumber
      }
      val listener = object : NsdManager.RegistrationListener {
          override fun onRegistrationFailed(serviceType: NsdServiceInfo, errorCode: Int) {}
          override fun onServiceRegistered(serviceInfo: NsdServiceInfo) {}
          override fun onUnregistrationFailed(serviceType: NsdServiceInfo, errorCode: Int) {}
          override fun onServiceUnregistered(serviceType: NsdServiceInfo) {}
      }
      nsdManager.registerService(service, NsdManager.PROTOCOL_DNS_SD, listener)
      return Pair(listener, lock)
  }
 
  fun stopAdvertisingService(listener: NsdManager.RegistrationListener, lock: MulticastLock?) {
      lock?.release()
      // unregisterService may throw IllegalArgumentException on T SDK extension &lt; 22 if the
      // listener was already unregistered or failed to register
      try {
          nsdManager.unregisterService(listener)
      } catch (_: IllegalArgumentException) {}
  }
  </code>
```

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.DiscoveryListener` Interface for callback invocation for service discovery |
| abstract | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.RegistrationListener` Interface for callback invocation for service registration |
| abstract | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ResolveListener` Callback for use with android. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ServiceInfoCallback` Callback to listen to service info updates. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#ACTION_NSD_STATE_CHANGED:kotlin.String` Broadcast intent action to indicate whether network service discovery is enabled or disabled. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#EXTRA_NSD_STATE:kotlin.String` The lookup key for an int that indicates whether network service discovery is enabled or disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#FAILURE_ALREADY_ACTIVE:kotlin.Int` Indicates that the operation failed because it is already active. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#FAILURE_BAD_PARAMETERS:kotlin.Int` Indicates that the service has failed to resolve because of bad parameters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#FAILURE_INTERNAL_ERROR:kotlin.Int` Failures are passed with onRegistrationFailed, onUnregistrationFailed, onStartDiscoveryFailed, onStopDiscoveryFailed or onResolveFailed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#FAILURE_MAX_LIMIT:kotlin.Int` Indicates that the operation failed because the maximum outstanding requests from the applications have reached. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#FAILURE_OPERATION_NOT_RUNNING:kotlin.Int` Indicates that the stop operation failed because it is not running. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#FAILURE_PERMISSION_DENIED:kotlin.Int` Indicates that the operation failed because the caller did not have the required permissions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#NSD_STATE_DISABLED:kotlin.Int` Network service discovery is disabled |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#NSD_STATE_ENABLED:kotlin.Int` Network service discovery is enabled |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#PROTOCOL_DNS_SD:kotlin.Int` Dns based service discovery protocol |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#SERVICE_PERMISSION_DENIED:kotlin.Int` Indicates the caller is not allowed to register service info callbacks or resolve a service. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#SERVICE_PERMISSION_GRANTED:kotlin.Int` Indicates the caller can register service info callbacks or resolve a service. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | checkPermissionForService Check whether the caller can register service info callbacks or resolve a service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | discoverServices Initiates service discovery to browse for instances of a service type. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | discoverServices Initiate service discovery to browse for instances of a service type. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | discoverServices Initiate service discovery to browse for instances of a service type. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | discoverServices Initiate service discovery to browse for instances of a service type. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerService Register a service to be discovered by other services. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerService Register a service to be discovered by other services. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerService Register a service to be discovered by other services. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerServiceInfoCallback Register a callback to discover and track updates of services. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerServiceInfoCallback Register a callback to listen for updates to a service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | resolveService Resolve a discovered service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | resolveService Resolve a discovered service. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | stopServiceDiscovery Stop service discovery initiated with #discoverServices. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | stopServiceResolution Stop service resolution initiated with #resolveService. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterService Unregister a service registered through #registerService. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterServiceInfoCallback Unregister a callback registered with #registerServiceInfoCallback. |

## Constants

### ACTION_NSD_STATE_CHANGED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NSD_STATE_CHANGED: String
```

Broadcast intent action to indicate whether network service discovery is enabled or disabled. An extra `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#EXTRA_NSD_STATE:kotlin.String` provides the state information as int.

 Value: "android.net.nsd.STATE_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#EXTRA_NSD_STATE:kotlin.String`

### EXTRA_NSD_STATE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NSD_STATE: String
```

The lookup key for an int that indicates whether network service discovery is enabled or disabled. Retrieve it with getIntExtra.

 Value: "nsd_state"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#NSD_STATE_DISABLED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#NSD_STATE_ENABLED:kotlin.Int`

### FAILURE_ALREADY_ACTIVE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FAILURE_ALREADY_ACTIVE: Int
```

Indicates that the operation failed because it is already active.

 Value: 3

### FAILURE_BAD_PARAMETERS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val FAILURE_BAD_PARAMETERS: Int
```

Indicates that the service has failed to resolve because of bad parameters. This failure is passed with onServiceInfoCallbackRegistrationFailed.

 Value: 6

### FAILURE_INTERNAL_ERROR

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FAILURE_INTERNAL_ERROR: Int
```

Failures are passed with onRegistrationFailed, onUnregistrationFailed, onStartDiscoveryFailed, onStopDiscoveryFailed or onResolveFailed. Indicates that the operation failed due to an internal error.

 Value: 0

### FAILURE_MAX_LIMIT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FAILURE_MAX_LIMIT: Int
```

Indicates that the operation failed because the maximum outstanding requests from the applications have reached.

 Value: 4

### FAILURE_OPERATION_NOT_RUNNING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val FAILURE_OPERATION_NOT_RUNNING: Int
```

Indicates that the stop operation failed because it is not running. This failure is passed with onStopResolutionFailed.

 Value: 5

### FAILURE_PERMISSION_DENIED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 22](https://developer.android.com/sdkExtensions)

```
static val FAILURE_PERMISSION_DENIED: Int
```

Indicates that the operation failed because the caller did not have the required permissions. This can happen when trying to perform resolution, discovery, or callback registration without the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_LOCAL_NETWORK:kotlin.String` permission. This failure is passed with onResolveFailed, onStartDiscoveryFailed, or onServiceInfoCallbackRegistrationFailed.

 Value: 7

### NSD_STATE_DISABLED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NSD_STATE_DISABLED: Int
```

Network service discovery is disabled

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#ACTION_NSD_STATE_CHANGED:kotlin.String`

### NSD_STATE_ENABLED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NSD_STATE_ENABLED: Int
```

Network service discovery is enabled

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#ACTION_NSD_STATE_CHANGED:kotlin.String`

### PROTOCOL_DNS_SD

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_DNS_SD: Int
```

Dns based service discovery protocol

 Value: 1

### SERVICE_PERMISSION_DENIED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 22](https://developer.android.com/sdkExtensions)

```
static val SERVICE_PERMISSION_DENIED: Int
```

Indicates the caller is not allowed to register service info callbacks or resolve a service.

This is a result code for checkPermissionForService.

 Value: 2

### SERVICE_PERMISSION_GRANTED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 22](https://developer.android.com/sdkExtensions)

```
static val SERVICE_PERMISSION_GRANTED: Int
```

Indicates the caller can register service info callbacks or resolve a service.

This is a result code for checkPermissionForService.

 Value: 1

## Public methods

### checkPermissionForService

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 22](https://developer.android.com/sdkExtensions)

```
fun checkPermissionForService(
    serviceName: String, 
    serviceType: String, 
    executor: Executor, 
    resultReceiver: IntConsumer
): Unit
```

Check whether the caller can register service info callbacks or resolve a service.

Starting from target SDK `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, unless apps have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_LOCAL_NETWORK:kotlin.String` permission, they can only register service info callbacks or resolve services that were selected in a UI picker, as per `https://developer.android.com/reference/kotlin/android/net/nsd/DiscoveryRequest#FLAG_SHOW_PICKER:kotlin.Long`.

The system will remember whether a user has selected a service in the past, but access may be revoked for storage reasons or by the user. This method allows checking whether access to the service was granted in the picker and not revoked.

The `resultReceiver` will be called using the provided `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` with either `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#SERVICE_PERMISSION_GRANTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#SERVICE_PERMISSION_DENIED:kotlin.Int`.

| Parameters ||
|---|---|
| `serviceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Instance name of the service. This value cannot be `null`. |
| `serviceType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Type of the service, e.g. _ipp._tcp. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to invoke the receiver. This value cannot be `null`. |
| --- | --- |
| `resultReceiver` | [IntConsumer](../java.util.function/IntConsumer.md): The `https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#` to receive the permission check result code; will be either `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#SERVICE_PERMISSION_GRANTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#SERVICE_PERMISSION_DENIED:kotlin.Int`. This value cannot be `null`. |

### discoverServices

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

```
fun discoverServices(
    discoveryRequest: DiscoveryRequest, 
    executor: Executor, 
    listener: NsdManager.DiscoveryListener
): Unit
```

Initiates service discovery to browse for instances of a service type. Service discovery consumes network bandwidth and will continue until the application calls stopServiceDiscovery.

The function call immediately returns after sending a request to start service discovery to the framework. The application is notified of a success to initiate discovery through the callback onDiscoveryStarted or a failure through onStartDiscoveryFailed.

Upon successful start, application is notified when a service is found with onServiceFound or when a service is lost with onServiceLost.

Upon failure to start, service discovery is not active and application does not need to invoke stopServiceDiscovery

The application should call stopServiceDiscovery when discovery of this service type is no longer required, and/or whenever the application is paused or stopped.

| Parameters ||
|---|---|
| `discoveryRequest` | [DiscoveryRequest](DiscoveryRequest.md): the DiscoveryRequest object which specifies the discovery parameters such as service type, subtype and network. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor to run listener callbacks with. This value cannot be `null`. |
| `listener` | [NsdManager.DiscoveryListener](../android/net/nsd/NsdManager.DiscoveryListener.md): The listener notifies of a successful discovery and is used to stop discovery on this serviceType through a call on stopServiceDiscovery. This value cannot be `null`. |
| --- | --- |

### discoverServices

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

```
fun discoverServices(
    serviceType: String, 
    protocolType: Int, 
    network: Network?, 
    executor: Executor, 
    listener: NsdManager.DiscoveryListener
): Unit
```

Initiate service discovery to browse for instances of a service type. Service discovery consumes network bandwidth and will continue until the application calls stopServiceDiscovery.

The function call immediately returns after sending a request to start service discovery to the framework. The application is notified of a success to initiate discovery through the callback onDiscoveryStarted or a failure through onStartDiscoveryFailed.

Upon successful start, application is notified when a service is found with onServiceFound or when a service is lost with onServiceLost.

Upon failure to start, service discovery is not active and application does not need to invoke stopServiceDiscovery

The application should call stopServiceDiscovery when discovery of this service type is no longer required, and/or whenever the application is paused or stopped.

| Parameters ||
|---|---|
| `serviceType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The service type being discovered. Examples include "_http._tcp" for http services or "_ipp._tcp" for printers. This value cannot be `null`. |
| `protocolType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The service discovery protocol |
| `network` | [Network](../android.net/Network.md)?: Network to discover services on, or null to discover on all available networks |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor to run listener callbacks with. This value cannot be `null`. |
| `listener` | [NsdManager.DiscoveryListener](../android/net/nsd/NsdManager.DiscoveryListener.md): The listener notifies of a successful discovery and is used to stop discovery on this serviceType through a call on stopServiceDiscovery. This value cannot be `null`. |

### discoverServices

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

```
fun discoverServices(
    serviceType: String, 
    protocolType: Int, 
    networkRequest: NetworkRequest, 
    executor: Executor, 
    listener: NsdManager.DiscoveryListener
): Unit
```

Initiate service discovery to browse for instances of a service type. Service discovery consumes network bandwidth and will continue until the application calls stopServiceDiscovery.

The function call immediately returns after sending a request to start service discovery to the framework. The application is notified of a success to initiate discovery through the callback onDiscoveryStarted or a failure through onStartDiscoveryFailed.

Upon successful start, application is notified when a service is found with onServiceFound or when a service is lost with onServiceLost.

Upon failure to start, service discovery is not active and application does not need to invoke stopServiceDiscovery

The application should call stopServiceDiscovery when discovery of this service type is no longer required, and/or whenever the application is paused or stopped.

During discovery, new networks may connect or existing networks may disconnect - for example if wifi is reconnected. When a service was found on a network that disconnects, onServiceLost will be called. If a new network connects that matches the `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.html#`, onServiceFound will be called for services found on that network. Applications that do not want to track networks themselves are encouraged to use this method instead of other overloads of `discoverServices`, as they will receive proper notifications when a service becomes available or unavailable due to network changes. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `serviceType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The service type being discovered. Examples include "_http._tcp" for http services or "_ipp._tcp" for printers. This value cannot be `null`. |
| `protocolType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The service discovery protocol |
| `networkRequest` | [NetworkRequest](../android.net/NetworkRequest.md): Request specifying networks that should be considered when discovering. This value cannot be `null`. |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor to run listener callbacks with. This value cannot be `null`. |
| `listener` | [NsdManager.DiscoveryListener](../android/net/nsd/NsdManager.DiscoveryListener.md): The listener notifies of a successful discovery and is used to stop discovery on this serviceType through a call on stopServiceDiscovery. This value cannot be `null`. |

### discoverServices

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

```
fun discoverServices(
    serviceType: String!, 
    protocolType: Int, 
    listener: NsdManager.DiscoveryListener!
): Unit
```

Initiate service discovery to browse for instances of a service type. Service discovery consumes network bandwidth and will continue until the application calls stopServiceDiscovery.

The function call immediately returns after sending a request to start service discovery to the framework. The application is notified of a success to initiate discovery through the callback onDiscoveryStarted or a failure through onStartDiscoveryFailed.

Upon successful start, application is notified when a service is found with onServiceFound or when a service is lost with onServiceLost.

Upon failure to start, service discovery is not active and application does not need to invoke stopServiceDiscovery

The application should call stopServiceDiscovery when discovery of this service type is no longer required, and/or whenever the application is paused or stopped.

| Parameters ||
|---|---|
| `serviceType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The service type being discovered. Examples include "_http._tcp" for http services or "_ipp._tcp" for printers |
| `protocolType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The service discovery protocol |
| `listener` | [NsdManager.DiscoveryListener](../android/net/nsd/NsdManager.DiscoveryListener.md)!: The listener notifies of a successful discovery and is used to stop discovery on this serviceType through a call on stopServiceDiscovery. Cannot be null. Cannot be in use for an active service discovery. |
| --- | --- |

### registerService

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

```
fun registerService(
    advertisingRequest: AdvertisingRequest, 
    executor: Executor, 
    listener: NsdManager.RegistrationListener
): Unit
```

Register a service to be discovered by other services.

The function call immediately returns after sending a request to register service to the framework. The application is notified of a successful registration through the callback onServiceRegistered or a failure through onRegistrationFailed.

The application should call unregisterService when the service registration is no longer required, and/or whenever the application is stopped.

| Parameters ||
|---|---|
| `advertisingRequest` | [AdvertisingRequest](AdvertisingRequest.md): service being registered. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor to run listener callbacks with. This value cannot be `null`. |
| `listener` | [NsdManager.RegistrationListener](../android/net/nsd/NsdManager.RegistrationListener.md): The listener notifies of a successful registration and is used to unregister this service through a call on unregisterService. Cannot be null. |
| --- | --- |

### registerService

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

```
fun registerService(
    serviceInfo: NsdServiceInfo!, 
    protocolType: Int, 
    listener: NsdManager.RegistrationListener!
): Unit
```

Register a service to be discovered by other services.

The function call immediately returns after sending a request to register service to the framework. The application is notified of a successful registration through the callback onServiceRegistered or a failure through onRegistrationFailed.

The application should call unregisterService when the service registration is no longer required, and/or whenever the application is stopped.

| Parameters ||
|---|---|
| `serviceInfo` | [NsdServiceInfo](NsdServiceInfo.md)!: The service being registered |
| `protocolType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The service discovery protocol |
| `listener` | [NsdManager.RegistrationListener](../android/net/nsd/NsdManager.RegistrationListener.md)!: The listener notifies of a successful registration and is used to unregister this service through a call on unregisterService. Cannot be null. Cannot be in use for an active service registration. |
| --- | --- |

### registerService

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

```
fun registerService(
    serviceInfo: NsdServiceInfo, 
    protocolType: Int, 
    executor: Executor, 
    listener: NsdManager.RegistrationListener
): Unit
```

Register a service to be discovered by other services.

The function call immediately returns after sending a request to register service to the framework. The application is notified of a successful registration through the callback onServiceRegistered or a failure through onRegistrationFailed.

The application should call unregisterService when the service registration is no longer required, and/or whenever the application is stopped.

| Parameters ||
|---|---|
| `serviceInfo` | [NsdServiceInfo](NsdServiceInfo.md): The service being registered. This value cannot be `null`. |
| `protocolType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The service discovery protocol |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor to run listener callbacks with. This value cannot be `null`. |
| --- | --- |
| `listener` | [NsdManager.RegistrationListener](../android/net/nsd/NsdManager.RegistrationListener.md): The listener notifies of a successful registration and is used to unregister this service through a call on unregisterService. Cannot be null. |

### registerServiceInfoCallback

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun registerServiceInfoCallback(
    discoveryRequest: DiscoveryRequest, 
    executor: Executor, 
    listener: NsdManager.ServiceInfoCallback
): Unit
```

Register a callback to discover and track updates of services.

This method combines discoverServices and registerServiceInfoCallback by finding services as per the provided DiscoveryRequest, and continuously monitoring availability and properties of the discovered services.

This API may cause more network traffic than using discoverServices and only calling registerServiceInfoCallback for select services, because it automatically queries all service information for all discovered services. However most mDNS advertisers reply with their full service information in one discovery reply, in which case there is no additional traffic, and this API saves the cost of registering multiple listeners for discovering and resolving services.

Applications need to cancel the registration before registering the same callback instance again. Upon failure to register a callback, the application is notified through onServiceInfoCallbackRegistrationFailed.

| Parameters ||
|---|---|
| `discoveryRequest` | [DiscoveryRequest](DiscoveryRequest.md): the DiscoveryRequest object which specifies the discovery parameters such as service type, subtype and network. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor to run listener callbacks with. This value cannot be `null`. |
| `listener` | [NsdManager.ServiceInfoCallback](../android/net/nsd/NsdManager.ServiceInfoCallback.md): The listener to be notified of found, updated or lost services. This value cannot be `null`. |
| --- | --- |

### registerServiceInfoCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun registerServiceInfoCallback(
    serviceInfo: NsdServiceInfo, 
    executor: Executor, 
    listener: NsdManager.ServiceInfoCallback
): Unit
```

Register a callback to listen for updates to a service. An application can listen to a service to continuously monitor availability of given service. The callback methods will be called on the passed executor. And service updates are sent with continuous calls to onServiceUpdated. This is different from #resolveService which provides one shot service information.

This API listens to updates for one service at a time. Applications need to cancel the registration before registering the same callback instance again. Upon failure to register a callback for example if it's a duplicated registration, the application is notified through onServiceInfoCallbackRegistrationFailed with `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#FAILURE_BAD_PARAMETERS:kotlin.Int`.

| Parameters ||
|---|---|
| `serviceInfo` | [NsdServiceInfo](NsdServiceInfo.md): the service to receive updates for. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor to run callbacks with. This value cannot be `null`. |
| `listener` | [NsdManager.ServiceInfoCallback](../android/net/nsd/NsdManager.ServiceInfoCallback.md): to receive callback upon service update. This value cannot be `null`. |
| --- | --- |

### resolveService

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun resolveService(
    serviceInfo: NsdServiceInfo!, 
    listener: NsdManager.ResolveListener!
): Unit
```

**Deprecated:** *the returned ServiceInfo may get stale at any time after resolution, including immediately after the callback is called, and may not contain some service information that could be delivered later, like additional host addresses. Prefer using #registerServiceInfoCallback, which will keep the application up-to-date with the state of the service.*

Resolve a discovered service. An application can resolve a service right before establishing a connection to fetch the IP and port details on which to setup the connection.

| Parameters ||
|---|---|
| `serviceInfo` | [NsdServiceInfo](NsdServiceInfo.md)!: service to be resolved |
| `listener` | [NsdManager.ResolveListener](../android/net/nsd/NsdManager.ResolveListener.md)!: to receive callback upon success or failure. Cannot be null. Cannot be in use for an active service resolution. |

### resolveService

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun resolveService(
    serviceInfo: NsdServiceInfo, 
    executor: Executor, 
    listener: NsdManager.ResolveListener
): Unit
```

**Deprecated:** *the returned ServiceInfo may get stale at any time after resolution, including immediately after the callback is called, and may not contain some service information that could be delivered later, like additional host addresses. Prefer using #registerServiceInfoCallback, which will keep the application up-to-date with the state of the service.*

Resolve a discovered service. An application can resolve a service right before establishing a connection to fetch the IP and port details on which to setup the connection.

| Parameters ||
|---|---|
| `serviceInfo` | [NsdServiceInfo](NsdServiceInfo.md): service to be resolved. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor to run listener callbacks with. This value cannot be `null`. |
| `listener` | [NsdManager.ResolveListener](../android/net/nsd/NsdManager.ResolveListener.md): to receive callback upon success or failure. This value cannot be `null`. |
| --- | --- |

### stopServiceDiscovery

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stopServiceDiscovery(listener: NsdManager.DiscoveryListener!): Unit
```

Stop service discovery initiated with #discoverServices. An active service discovery is notified to the application with onDiscoveryStarted and it stays active until the application invokes a stop service discovery. A successful stop is notified to with a call to onDiscoveryStopped.

Upon failure to stop service discovery, application is notified through onStopDiscoveryFailed.

If the listener is not already registered, for apps running on devices with T SDK extension \< 22, this will throw with `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

| Parameters ||
|---|---|
| `listener` | [NsdManager.DiscoveryListener](../android/net/nsd/NsdManager.DiscoveryListener.md)!: This should be the listener object that was passed to #discoverServices. It identifies the discovery that should be stopped and notifies of a successful or unsuccessful stop. In API versions 20 and above, the listener object may be used for another service discovery once the callback has been called. In API versions \<= 19, there is no entirely reliable way to know when a listener may be re-used, and a new listener should be created for each service discovery request. |

### stopServiceResolution

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun stopServiceResolution(listener: NsdManager.ResolveListener): Unit
```

Stop service resolution initiated with #resolveService. A successful stop is notified with a call to onResolutionStopped.

Upon failure to stop service resolution for example if resolution is done or the requester stops resolution repeatedly, the application is notified onStopResolutionFailed with `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#FAILURE_OPERATION_NOT_RUNNING:kotlin.Int`

If the listener is not already registered, for apps running on devices with T SDK extension \< 22, this will throw with `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

| Parameters ||
|---|---|
| `listener` | [NsdManager.ResolveListener](../android/net/nsd/NsdManager.ResolveListener.md): This should be a listener object that was passed to #resolveService. It identifies the resolution that should be stopped and notifies of a successful or unsuccessful stop. This value cannot be `null`. |

### unregisterService

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterService(listener: NsdManager.RegistrationListener!): Unit
```

Unregister a service registered through #registerService. A successful unregister is notified to the application with a call to onServiceUnregistered.

| Parameters ||
|---|---|
| `listener` | [NsdManager.RegistrationListener](../android/net/nsd/NsdManager.RegistrationListener.md)!: This should be the listener object that was passed to #registerService. It identifies the service that should be unregistered and notifies of a successful or unsuccessful unregistration via the listener callbacks. In API versions 20 and above, the listener object may be used for another service registration once the callback has been called. In API versions \<= 19, there is no entirely reliable way to know when a listener may be re-used, and a new listener should be created for each service registration request. If the listener is not already registered, for apps running on devices with T SDK extension \< 22, this will throw with `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`. |

### unregisterServiceInfoCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun unregisterServiceInfoCallback(listener: NsdManager.ServiceInfoCallback): Unit
```

Unregister a callback registered with #registerServiceInfoCallback. A successful unregistration is notified with a call to onServiceInfoCallbackUnregistered. The same callback can only be reused after this is called.

If the listener is not already registered, for apps running on devices with T SDK extension \< 22, this will throw with `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

| Parameters ||
|---|---|
| `listener` | [NsdManager.ServiceInfoCallback](../android/net/nsd/NsdManager.ServiceInfoCallback.md): This should be a listener object that was passed to #registerServiceInfoCallback. It identifies the registration that should be unregistered and notifies of a successful or unsuccessful stop. This value cannot be `null`. |
