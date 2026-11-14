# VpnManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VpnManager

Kotlin | [Java](https://developer.android.com/reference/android/net/VpnManager "View this page in Java") 

```
open class VpnManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.VpnManager](https://developer.android.com/reference/kotlin/android/net/VpnManager#) |

This class provides an interface for apps to manage platform VPN profiles

Apps can use this API to provide profiles with which the platform can set up a VPN without further app intermediation. When a VPN profile is present and the app is selected as an always-on VPN, the platform will directly trigger the negotiation of the VPN without starting or waking the app (unlike VpnService).

VPN apps using supported protocols should preferentially use this API over the [VpnService](https://developer.android.com/reference/kotlin/android/net/VpnService) API for ease-of-development and reduced maintenance burden. This also give the user the guarantee that VPN network traffic is not subjected to on-device packet interception. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_VPN_MANAGER_EVENT](https://developer.android.com/reference/kotlin/android/net/VpnManager#ACTION_VPN_MANAGER_EVENT:kotlin.String) Action sent in [android.content.Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) s to VpnManager clients when an event occurred. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CATEGORY_EVENT_ALWAYS_ON_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_ALWAYS_ON_STATE_CHANGED:kotlin.String) The always-on state of this VPN was changed |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CATEGORY_EVENT_DEACTIVATED_BY_USER](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_DEACTIVATED_BY_USER:kotlin.String) The user deactivated the VPN. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CATEGORY_EVENT_IKE_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_IKE_ERROR:kotlin.String) An IKE protocol error occurred. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CATEGORY_EVENT_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_NETWORK_ERROR:kotlin.String) A network error occurred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CLASS_NOT_RECOVERABLE](https://developer.android.com/reference/kotlin/android/net/VpnManager#ERROR_CLASS_NOT_RECOVERABLE:kotlin.Int) [EXTRA_ERROR_CLASS](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CLASS:kotlin.String) coding for a non-recoverable error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CLASS_RECOVERABLE](https://developer.android.com/reference/kotlin/android/net/VpnManager#ERROR_CLASS_RECOVERABLE:kotlin.Int) [EXTRA_ERROR_CLASS](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CLASS:kotlin.String) coding for a recoverable error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_NETWORK_IO](https://developer.android.com/reference/kotlin/android/net/VpnManager#ERROR_CODE_NETWORK_IO:kotlin.Int) An [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String) for [CATEGORY_EVENT_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_NETWORK_ERROR:kotlin.String) indicating an input/output error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_NETWORK_LOST](https://developer.android.com/reference/kotlin/android/net/VpnManager#ERROR_CODE_NETWORK_LOST:kotlin.Int) An [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String) for [CATEGORY_EVENT_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_NETWORK_ERROR:kotlin.String) indicating that network connectivity was lost. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_NETWORK_PROTOCOL_TIMEOUT](https://developer.android.com/reference/kotlin/android/net/VpnManager#ERROR_CODE_NETWORK_PROTOCOL_TIMEOUT:kotlin.Int) An [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String) for [CATEGORY_EVENT_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_NETWORK_ERROR:kotlin.String) indicating a timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_NETWORK_UNKNOWN_HOST](https://developer.android.com/reference/kotlin/android/net/VpnManager#ERROR_CODE_NETWORK_UNKNOWN_HOST:kotlin.Int) An [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String) for [CATEGORY_EVENT_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_NETWORK_ERROR:kotlin.String) to indicate that the network host isn't known. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ERROR_CLASS](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CLASS:kotlin.String) Extra for the error class, as an `int`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String) Extra for an error code, as an `int`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SESSION_KEY](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_SESSION_KEY:kotlin.String) The key of the session that experienced this event, as a `String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_TIMESTAMP_MILLIS](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_TIMESTAMP_MILLIS:kotlin.String) A `long` timestamp containing the time at which the event occurred. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UNDERLYING_LINK_PROPERTIES](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_UNDERLYING_LINK_PROPERTIES:kotlin.String) The [LinkProperties](https://developer.android.com/reference/kotlin/android/net/LinkProperties) of the underlying network when the event occurred. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UNDERLYING_NETWORK](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_UNDERLYING_NETWORK:kotlin.String) The network that was underlying the VPN when the event occurred, as a [Network](https://developer.android.com/reference/kotlin/android/net/Network). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UNDERLYING_NETWORK_CAPABILITIES](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_UNDERLYING_NETWORK_CAPABILITIES:kotlin.String) The [NetworkCapabilities](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities) of the underlying network when the event occurred. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_VPN_PROFILE_STATE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_VPN_PROFILE_STATE:kotlin.String) The VpnProfileState at the time that this event occurred. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteProvisionedVpnProfile](https://developer.android.com/reference/kotlin/android/net/VpnManager#deleteProvisionedVpnProfile())`()` Delete the VPN profile configuration that was provisioned by the calling app |
| open [VpnProfileState](https://developer.android.com/reference/kotlin/android/net/VpnProfileState)? | [getProvisionedVpnProfileState](https://developer.android.com/reference/kotlin/android/net/VpnManager#getProvisionedVpnProfileState())`()` Retrieve the VpnProfileState for the profile provisioned by the calling package. |
| open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)? | [provisionVpnProfile](https://developer.android.com/reference/kotlin/android/net/VpnManager#provisionVpnProfile(android.net.PlatformVpnProfile))`(`profile:` ` [PlatformVpnProfile](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile)`)` Install a VpnProfile configuration keyed on the calling app's package name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startProvisionedVpnProfile](https://developer.android.com/reference/kotlin/android/net/VpnManager#startProvisionedVpnProfile())`()` Request the startup of a previously provisioned VPN. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [startProvisionedVpnProfileSession](https://developer.android.com/reference/kotlin/android/net/VpnManager#startProvisionedVpnProfileSession())`()` Request the startup of a previously provisioned VPN. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopProvisionedVpnProfile](https://developer.android.com/reference/kotlin/android/net/VpnManager#stopProvisionedVpnProfile())`()` Tear down the VPN provided by the calling app (if any) |

## Constants

### ACTION_VPN_MANAGER_EVENT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_VPN_MANAGER_EVENT: String
```

Action sent in [android.content.Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) s to VpnManager clients when an event occurred.

If the provisioning application declares a service handling this intent action, but is not already running, it will be started. Upon starting, the application is granted a short grace period to run in the background even while the device is idle to handle any potential failures. Applications requiring long-running actions triggered by one of these events should declare a foreground service to prevent being killed once the grace period expires. This action will have a category of either [CATEGORY_EVENT_IKE_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_IKE_ERROR:kotlin.String), [CATEGORY_EVENT_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_NETWORK_ERROR:kotlin.String), or [CATEGORY_EVENT_DEACTIVATED_BY_USER](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_DEACTIVATED_BY_USER:kotlin.String), that the app can use to filter events it's interested in reacting to. It will also contain the following extras :

- [EXTRA_SESSION_KEY](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_SESSION_KEY:kotlin.String), a `String` for the session key, as returned by [startProvisionedVpnProfileSession](https://developer.android.com/reference/kotlin/android/net/VpnManager#startProvisionedVpnProfileSession()).
- [EXTRA_TIMESTAMP_MILLIS](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_TIMESTAMP_MILLIS:kotlin.String), a long for the timestamp at which the error occurred, in milliseconds since the epoch, as returned by [java.lang.System#currentTimeMillis](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()).
- [EXTRA_UNDERLYING_NETWORK](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_UNDERLYING_NETWORK:kotlin.String), a [Network](https://developer.android.com/reference/kotlin/android/net/Network) containing the underlying network at the time the error occurred, or null if none. Note that this network may have disconnected already.
- [EXTRA_UNDERLYING_NETWORK_CAPABILITIES](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_UNDERLYING_NETWORK_CAPABILITIES:kotlin.String), a [NetworkCapabilities](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities) for the underlying network at the time the error occurred.
- [EXTRA_UNDERLYING_LINK_PROPERTIES](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_UNDERLYING_LINK_PROPERTIES:kotlin.String), a [LinkProperties](https://developer.android.com/reference/kotlin/android/net/LinkProperties) for the underlying network at the time the error occurred.

When this event is an error, either [CATEGORY_EVENT_IKE_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_IKE_ERROR:kotlin.String) or [CATEGORY_EVENT_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_NETWORK_ERROR:kotlin.String), the following extras will be populated :

- [EXTRA_ERROR_CLASS](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CLASS:kotlin.String), an `int` for the class of error, either [ERROR_CLASS_RECOVERABLE](https://developer.android.com/reference/kotlin/android/net/VpnManager#ERROR_CLASS_RECOVERABLE:kotlin.Int) or [ERROR_CLASS_NOT_RECOVERABLE](https://developer.android.com/reference/kotlin/android/net/VpnManager#ERROR_CLASS_NOT_RECOVERABLE:kotlin.Int).
- [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String), an `int` error code specific to the error. See [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String) for details.

 Value: "android.net.action.VPN_MANAGER_EVENT"

### CATEGORY_EVENT_ALWAYS_ON_STATE_CHANGED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_EVENT_ALWAYS_ON_STATE_CHANGED: String
```

The always-on state of this VPN was changed

This may be the result of a user changing VPN settings, or a Device Policy Manager app having changed the VPN policy. 

 Value: "android.net.category.EVENT_ALWAYS_ON_STATE_CHANGED"

### CATEGORY_EVENT_DEACTIVATED_BY_USER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_EVENT_DEACTIVATED_BY_USER: String
```

The user deactivated the VPN. This can happen either when the user turns the VPN off explicitly, or when they select a different VPN provider. 

 Value: "android.net.category.EVENT_DEACTIVATED_BY_USER"

### CATEGORY_EVENT_IKE_ERROR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_EVENT_IKE_ERROR: String
```

An IKE protocol error occurred. Codes (in [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String)) are the codes from [android.net.ipsec.ike.exceptions.IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException), as defined by IANA in "IKEv2 Notify Message Types - Error Types". 

 Value: "android.net.category.EVENT_IKE_ERROR"

### CATEGORY_EVENT_NETWORK_ERROR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_EVENT_NETWORK_ERROR: String
```

A network error occurred. Error codes (in [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String)) are ERROR_CODE_NETWORK_\*. 

 Value: "android.net.category.EVENT_NETWORK_ERROR"

### ERROR_CLASS_NOT_RECOVERABLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CLASS_NOT_RECOVERABLE: Int
```

[EXTRA_ERROR_CLASS](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CLASS:kotlin.String) coding for a non-recoverable error. This error is fatal, e.g. configuration error. The stack will not retry connection. 

 Value: 1

### ERROR_CLASS_RECOVERABLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CLASS_RECOVERABLE: Int
```

[EXTRA_ERROR_CLASS](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CLASS:kotlin.String) coding for a recoverable error. The stack experienced an error but will retry with exponential backoff, e.g. network timeout. 

 Value: 2

### ERROR_CODE_NETWORK_IO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_NETWORK_IO: Int
```

An [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String) for [CATEGORY_EVENT_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_NETWORK_ERROR:kotlin.String) indicating an input/output error. This code happens when reading or writing to sockets on the underlying networks was terminated by an I/O error. {@see IOException}. 

 Value: 3

### ERROR_CODE_NETWORK_LOST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_NETWORK_LOST: Int
```

An [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String) for [CATEGORY_EVENT_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_NETWORK_ERROR:kotlin.String) indicating that network connectivity was lost. The most common reason for this error is that the underlying network was disconnected, {@see android.net.ipsec.ike.exceptions.IkeNetworkLostException}. 

 Value: 2

### ERROR_CODE_NETWORK_PROTOCOL_TIMEOUT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_NETWORK_PROTOCOL_TIMEOUT: Int
```

An [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String) for [CATEGORY_EVENT_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_NETWORK_ERROR:kotlin.String) indicating a timeout. For Ikev2 VPNs, this happens typically after a retransmission failure. {@see android.net.ipsec.ike.exceptions.IkeTimeoutException} 

 Value: 1

### ERROR_CODE_NETWORK_UNKNOWN_HOST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_NETWORK_UNKNOWN_HOST: Int
```

An [EXTRA_ERROR_CODE](https://developer.android.com/reference/kotlin/android/net/VpnManager#EXTRA_ERROR_CODE:kotlin.String) for [CATEGORY_EVENT_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_NETWORK_ERROR:kotlin.String) to indicate that the network host isn't known. This happens when domain name resolution could not resolve an IP address for the specified host. {@see java.net.UnknownHostException} 

 Value: 0

### EXTRA_ERROR_CLASS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ERROR_CLASS: String
```

Extra for the error class, as an `int`. This is always either [ERROR_CLASS_NOT_RECOVERABLE](https://developer.android.com/reference/kotlin/android/net/VpnManager#ERROR_CLASS_NOT_RECOVERABLE:kotlin.Int) or [ERROR_CLASS_RECOVERABLE](https://developer.android.com/reference/kotlin/android/net/VpnManager#ERROR_CLASS_RECOVERABLE:kotlin.Int). This extra is only populated for error categories. 

 Value: "android.net.extra.ERROR_CLASS"

### EXTRA_ERROR_CODE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ERROR_CODE: String
```

Extra for an error code, as an `int`.

- For [CATEGORY_EVENT_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_NETWORK_ERROR:kotlin.String), this is one of the `ERROR_CODE_NETWORK_*` constants.
- For [CATEGORY_EVENT_IKE_ERROR](https://developer.android.com/reference/kotlin/android/net/VpnManager#CATEGORY_EVENT_IKE_ERROR:kotlin.String), this is one of values defined in [android.net.ipsec.ike.exceptions.IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException).ERROR_TYPE_\*.

For non-error categories, this extra is not populated.

<br />

 Value: "android.net.extra.ERROR_CODE"

### EXTRA_SESSION_KEY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SESSION_KEY: String
```

The key of the session that experienced this event, as a `String`. This is the same key that was returned by [startProvisionedVpnProfileSession](https://developer.android.com/reference/kotlin/android/net/VpnManager#startProvisionedVpnProfileSession()). 

 Value: "android.net.extra.SESSION_KEY"

### EXTRA_TIMESTAMP_MILLIS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_TIMESTAMP_MILLIS: String
```

A `long` timestamp containing the time at which the event occurred. This is a number of milliseconds since the epoch, suitable to be compared with [java.lang.System#currentTimeMillis](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()). 

 Value: "android.net.extra.TIMESTAMP_MILLIS"

### EXTRA_UNDERLYING_LINK_PROPERTIES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UNDERLYING_LINK_PROPERTIES: String
```

The [LinkProperties](https://developer.android.com/reference/kotlin/android/net/LinkProperties) of the underlying network when the event occurred.

This extra will be null if there was no underlying network at the time of the event, or the underlying network has no bearing on the event, as in the case of:

- CATEGORY_EVENT_DEACTIVATED_BY_USER
- CATEGORY_EVENT_ALWAYS_ON_STATE_CHANGED

 Value: "android.net.extra.UNDERLYING_LINK_PROPERTIES"

### EXTRA_UNDERLYING_NETWORK

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UNDERLYING_NETWORK: String
```

The network that was underlying the VPN when the event occurred, as a [Network](https://developer.android.com/reference/kotlin/android/net/Network).

This extra will be null if there was no underlying network at the time of the event, or the underlying network has no bearing on the event, as in the case of:

- CATEGORY_EVENT_DEACTIVATED_BY_USER
- CATEGORY_EVENT_ALWAYS_ON_STATE_CHANGED

 Value: "android.net.extra.UNDERLYING_NETWORK"

### EXTRA_UNDERLYING_NETWORK_CAPABILITIES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UNDERLYING_NETWORK_CAPABILITIES: String
```

The [NetworkCapabilities](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities) of the underlying network when the event occurred.

This extra will be null if there was no underlying network at the time of the event, or the underlying network has no bearing on the event, as in the case of:

- CATEGORY_EVENT_DEACTIVATED_BY_USER
- CATEGORY_EVENT_ALWAYS_ON_STATE_CHANGED

 Value: "android.net.extra.UNDERLYING_NETWORK_CAPABILITIES"

### EXTRA_VPN_PROFILE_STATE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_VPN_PROFILE_STATE: String
```

The VpnProfileState at the time that this event occurred.

This extra may be null if the VPN was revoked by the user, or the profile was deleted. 

 Value: "android.net.extra.VPN_PROFILE_STATE"

## Public methods

### deleteProvisionedVpnProfile

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deleteProvisionedVpnProfile(): Unit
```

Delete the VPN profile configuration that was provisioned by the calling app

| Exceptions ||
|-------------------------------|-------------------------------------|
| `java.lang.SecurityException` | if this would violate user settings |

### getProvisionedVpnProfileState

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProvisionedVpnProfileState(): VpnProfileState?
```

Retrieve the VpnProfileState for the profile provisioned by the calling package.

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [VpnProfileState](https://developer.android.com/reference/kotlin/android/net/VpnProfileState)? | the VpnProfileState with current information, or null if there was no profile provisioned and started by the calling package. |

### provisionVpnProfile

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun provisionVpnProfile(profile: PlatformVpnProfile): Intent?
```

Install a VpnProfile configuration keyed on the calling app's package name.

This method returns `null` if user consent has already been granted, or an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) to a system activity. If an intent is returned, the application should launch the activity using android.app.Activity#startActivityForResult to request user consent. The activity may pop up a dialog to require user action, and the result will come back via its android.app.Activity#onActivityResult. If the result is [Activity.RESULT_OK](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int), the user has consented, and the VPN profile can be started.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `profile` | [PlatformVpnProfile](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile): the VpnProfile provided by this package. Will override any previous VpnProfile stored for this package. This value cannot be `null`. |

| Return ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)? | an Intent requesting user consent to start the VPN, or null if consent is not required based on privileges or previous user consent. |

### startProvisionedVpnProfile

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startProvisionedVpnProfile(): Unit
```

**Deprecated:** *This method is replaced by startProvisionedVpnProfileSession which returns a session key for the caller to diagnose the errors.*

Request the startup of a previously provisioned VPN.

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | exception if user or device settings prevent this VPN from being setup, or if user consent has not been granted |

### startProvisionedVpnProfileSession

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startProvisionedVpnProfileSession(): String
```

Request the startup of a previously provisioned VPN.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A unique key corresponding to this session. This value cannot be `null`. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | exception if user or device settings prevent this VPN from being setup, or if user consent has not been granted |

### stopProvisionedVpnProfile

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stopProvisionedVpnProfile(): Unit
```

Tear down the VPN provided by the calling app (if any)
