Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TetheringManager

```
open class TetheringManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.TetheringManager](https://developer.android.com/reference/kotlin/android/net/TetheringManager#) |

This class provides the APIs to control the tethering service.

The primary responsibilities of this class are to provide the APIs for applications to start tethering, stop tethering, query configuration and query status.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/net/TetheringManager.StartTetheringCallback` Callback for use with `https://developer.android.com/reference/kotlin/android/net/TetheringManager#startTethering(android.net.TetheringManager.TetheringRequest,%20java.util.concurrent.Executor,%20android.net.TetheringManager.StartTetheringCallback)` to find out whether tethering succeeded. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/TetheringManager.StopTetheringCallback` Callback for use with `https://developer.android.com/reference/kotlin/android/net/TetheringManager#stopTethering(android.net.TetheringManager.TetheringRequest,%20java.util.concurrent.Executor,%20android.net.TetheringManager.StopTetheringCallback)` to find out whether stop tethering succeeded. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringEventCallback` Callback for use with registerTetheringEventCallback to find out tethering upstream status. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringRequest` Use with `https://developer.android.com/reference/kotlin/android/net/TetheringManager#startTethering(android.net.TetheringManager.TetheringRequest,%20java.util.concurrent.Executor,%20android.net.TetheringManager.StartTetheringCallback)` to specify additional parameters when starting tethering. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#CONNECTIVITY_SCOPE_GLOBAL:kotlin.Int` Indicates that this tethering connection will provide connectivity beyond this device (e.g., global Internet access). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHERING_WIFI:kotlin.Int` Wifi tethering type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_DHCPSERVER_ERROR:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_DISABLE_FORWARDING_ERROR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_DUPLICATE_REQUEST:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_ENABLE_FORWARDING_ERROR:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_ENTITLEMENT_UNKNOWN:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_IFACE_CFG_ERROR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_INTERNAL_ERROR:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_NO_ACCESS_TETHERING_PERMISSION:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_NO_CHANGE_TETHERING_PERMISSION:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_NO_ERROR:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_PROVISIONING_FAILED:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_SERVICE_UNAVAIL:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_TETHER_IFACE_ERROR:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_UNAVAIL_IFACE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_UNKNOWN_IFACE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_UNKNOWN_REQUEST:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_UNKNOWN_TYPE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_UNSUPPORTED:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_UNTETHER_IFACE_ERROR:kotlin.Int` <br /> |
| --- | --- |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#registerTetheringEventCallback(java.util.concurrent.Executor,%20android.net.TetheringManager.TetheringEventCallback)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringEventCallback)` Start listening to tethering change events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#startTethering(android.net.TetheringManager.TetheringRequest,%20java.util.concurrent.Executor,%20android.net.TetheringManager.StartTetheringCallback)(request: https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/net/TetheringManager.StartTetheringCallback)` Starts tethering and runs tether provisioning for the given type if needed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#stopTethering(android.net.TetheringManager.TetheringRequest,%20java.util.concurrent.Executor,%20android.net.TetheringManager.StopTetheringCallback)(request: https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/net/TetheringManager.StopTetheringCallback)` Stops tethering for the given request. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#unregisterTetheringEventCallback(android.net.TetheringManager.TetheringEventCallback)(callback: https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringEventCallback)` Remove tethering event callback previously registered with `https://developer.android.com/reference/kotlin/android/net/TetheringManager#registerTetheringEventCallback(java.util.concurrent.Executor,%20android.net.TetheringManager.TetheringEventCallback)`. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/TetheringManager#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Constants

### CONNECTIVITY_SCOPE_GLOBAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTIVITY_SCOPE_GLOBAL: Int
```

Indicates that this tethering connection will provide connectivity beyond this device (e.g., global Internet access).

 Value: 1

### TETHERING_WIFI

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHERING_WIFI: Int
```

Wifi tethering type.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/TetheringManager#startTethering(android.net.TetheringManager.TetheringRequest,%20java.util.concurrent.Executor,%20android.net.TetheringManager.StartTetheringCallback)`

### TETHER_ERROR_DHCPSERVER_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_DHCPSERVER_ERROR: Int
```

 Value: 12

### TETHER_ERROR_DISABLE_FORWARDING_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_DISABLE_FORWARDING_ERROR: Int
```

 Value: 9

### TETHER_ERROR_DUPLICATE_REQUEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_DUPLICATE_REQUEST: Int
```

 Value: 18

### TETHER_ERROR_ENABLE_FORWARDING_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_ENABLE_FORWARDING_ERROR: Int
```

 Value: 8

### TETHER_ERROR_ENTITLEMENT_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_ENTITLEMENT_UNKNOWN: Int
```

 Value: 13

### TETHER_ERROR_IFACE_CFG_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_IFACE_CFG_ERROR: Int
```

 Value: 10

### TETHER_ERROR_INTERNAL_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_INTERNAL_ERROR: Int
```

 Value: 5

### TETHER_ERROR_NO_ACCESS_TETHERING_PERMISSION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_NO_ACCESS_TETHERING_PERMISSION: Int
```

 Value: 15

### TETHER_ERROR_NO_CHANGE_TETHERING_PERMISSION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_NO_CHANGE_TETHERING_PERMISSION: Int
```

 Value: 14

### TETHER_ERROR_NO_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_NO_ERROR: Int
```

 Value: 0

### TETHER_ERROR_PROVISIONING_FAILED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_PROVISIONING_FAILED: Int
```

 Value: 11

### TETHER_ERROR_SERVICE_UNAVAIL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_SERVICE_UNAVAIL: Int
```

 Value: 2

### TETHER_ERROR_TETHER_IFACE_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_TETHER_IFACE_ERROR: Int
```

 Value: 6

### TETHER_ERROR_UNAVAIL_IFACE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_UNAVAIL_IFACE: Int
```

 Value: 4

### TETHER_ERROR_UNKNOWN_IFACE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_UNKNOWN_IFACE: Int
```

 Value: 1

### TETHER_ERROR_UNKNOWN_REQUEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_UNKNOWN_REQUEST: Int
```

 Value: 17

### TETHER_ERROR_UNKNOWN_TYPE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_UNKNOWN_TYPE: Int
```

 Value: 16

### TETHER_ERROR_UNSUPPORTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_UNSUPPORTED: Int
```

 Value: 3

### TETHER_ERROR_UNTETHER_IFACE_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TETHER_ERROR_UNTETHER_IFACE_ERROR: Int
```

 Value: 7

## Public methods

### registerTetheringEventCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerTetheringEventCallback(
    executor: Executor, 
    callback: TetheringManager.TetheringEventCallback
): Unit
```

Start listening to tethering change events. Any new added callback will receive the last tethering status right away. If callback is registered, android.net.TetheringManager.TetheringEventCallback#onUpstreamChanged will immediately be called. If tethering has no upstream or disabled, the argument of callback will be null. The same callback object cannot be registered twice. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor on which callback will be invoked. This value cannot be `null`. |
| `callback` | [TetheringManager.TetheringEventCallback](https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringEventCallback): the callback to be called when tethering has change events. This value cannot be `null`. |

### startTethering

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startTethering(
    request: TetheringManager.TetheringRequest, 
    executor: Executor, 
    callback: TetheringManager.StartTetheringCallback
): Unit
```

Starts tethering and runs tether provisioning for the given type if needed. If provisioning fails, stopTethering will be called automatically.

| Parameters ||
|---|---|
| `request` | [TetheringManager.TetheringRequest](https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringRequest): a `https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringRequest` which can specify the preferred configuration. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` to specify the thread upon which the callback of TetheringRequest will be invoked. This value cannot be `null`. |
| `callback` | [TetheringManager.StartTetheringCallback](https://developer.android.com/reference/kotlin/android/net/TetheringManager.StartTetheringCallback): A callback that will be called to indicate the success status of the tethering start request. This value cannot be `null`. |
| --- | --- |

### stopTethering

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stopTethering(
    request: TetheringManager.TetheringRequest, 
    executor: Executor, 
    callback: TetheringManager.StopTetheringCallback
): Unit
```

Stops tethering for the given request. Operation will fail with `https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_UNKNOWN_REQUEST:kotlin.Int` if there is no request that matches it.

| Parameters ||
|---|---|
| `request` | [TetheringManager.TetheringRequest](https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringRequest): This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): This value cannot be `null`. |
| `callback` | [TetheringManager.StopTetheringCallback](https://developer.android.com/reference/kotlin/android/net/TetheringManager.StopTetheringCallback): This value cannot be `null`. |
| --- | --- |

### unregisterTetheringEventCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterTetheringEventCallback(callback: TetheringManager.TetheringEventCallback): Unit
```

Remove tethering event callback previously registered with `https://developer.android.com/reference/kotlin/android/net/TetheringManager#registerTetheringEventCallback(java.util.concurrent.Executor,%20android.net.TetheringManager.TetheringEventCallback)`. 
Requires android.Manifest.permission#TETHER_PRIVILEGED or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `callback` | [TetheringManager.TetheringEventCallback](https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringEventCallback): previously registered callback. This value cannot be `null`. |

## Protected methods

### finalize

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
