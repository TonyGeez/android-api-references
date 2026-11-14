Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangingSession

```
class RangingSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.ranging.RangingSession](https://developer.android.com/reference/kotlin/android/ranging/RangingSession#) |

Represents a session for performing ranging operations. A `https://developer.android.com/reference/kotlin/android/ranging/RangingSession#` manages the lifecycle of a ranging operation, including start, stop, and event callbacks.

All methods are asynchronous and rely on the provided `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` to invoke callbacks on appropriate threads.

This class implements `https://developer.android.com/reference/kotlin/java/lang/AutoCloseable.html#`, ensuring that resources can be automatically released when the session is closed.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/ranging/RangingSession.Callback` Callback interface for receiving ranging session events. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingSession#addDeviceToRangingSession(android.ranging.RangingConfig)(deviceRangingParams: https://developer.android.com/reference/kotlin/android/ranging/RangingConfig)` Adds a new device to an ongoing ranging session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingSession#close()()` Closes this resource, relinquishing any underlying resources. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingSession#reconfigureRangingInterval(kotlin.Int)(intervalSkipCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reconfigures the ranging interval for the current session by setting the interval skip count. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingSession#removeDeviceFromRangingSession(android.ranging.RangingDevice)(rangingDevice: https://developer.android.com/reference/kotlin/android/ranging/RangingDevice)` Removes a specific device from an ongoing ranging session. |
| [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#) | `https://developer.android.com/reference/kotlin/android/ranging/RangingSession#start(android.ranging.RangingPreference)(rangingPreference: https://developer.android.com/reference/kotlin/android/ranging/RangingPreference)` Starts the ranging session with the provided ranging preferences. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingSession#stop()()` Stops the ranging session. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingSession#toString()()` Returns a string representation of the object. |

## Public methods

### addDeviceToRangingSession

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addDeviceToRangingSession(deviceRangingParams: RangingConfig): Unit
```

Adds a new device to an ongoing ranging session.

This method allows for adding a new device to an active ranging session using raw ranging parameters. Only devices represented by `https://developer.android.com/reference/kotlin/android/ranging/raw/RawResponderRangingConfig` is supported. If the provided `https://developer.android.com/reference/kotlin/android/ranging/RangingConfig` does not match one of these types, the addition fails and invokes `https://developer.android.com/reference/kotlin/android/ranging/RangingSession.Callback#onOpenFailed(kotlin.Int)` with a reason of `https://developer.android.com/reference/kotlin/android/ranging/RangingSession.Callback#REASON_UNSUPPORTED:kotlin.Int`.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RANGING:kotlin.String`

| Parameters ||
|---|---|
| `deviceRangingParams` | [RangingConfig](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig): the ranging parameters for the device to be added, which must be an instance of `https://developer.android.com/reference/kotlin/android/ranging/raw/RawResponderRangingConfig` This value cannot be `null`. |

### close

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Closes this resource, relinquishing any underlying resources. This method is invoked automatically on objects managed by the `try`-with-resources statement. Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RANGING:kotlin.String`

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### reconfigureRangingInterval

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reconfigureRangingInterval(intervalSkipCount: Int): Unit
```

Reconfigures the ranging interval for the current session by setting the interval skip count. The `intervalSkipCount` defines how many intervals should be skipped between successive ranging rounds. Valid values range from 0 to 255. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RANGING:kotlin.String`

| Parameters ||
|---|---|
| `intervalSkipCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of intervals to skip, ranging from 0 to 255. Value is between 0 and 255 inclusive |

### removeDeviceFromRangingSession

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeDeviceFromRangingSession(rangingDevice: RangingDevice): Unit
```

Removes a specific device from an ongoing ranging session.

This method removes a specified device from the active ranging session, stopping further ranging operations for that device. The operation is handled by the system server and may throw a `https://developer.android.com/reference/kotlin/android/os/RemoteException.html#` in case of server-side communication issues.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RANGING:kotlin.String`

| Parameters ||
|---|---|
| `rangingDevice` | [RangingDevice](https://developer.android.com/reference/kotlin/android/ranging/RangingDevice): the device to be removed from the session. This value cannot be `null`. |

### start

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun start(rangingPreference: RangingPreference): CancellationSignal
```

Starts the ranging session with the provided ranging preferences.

The `https://developer.android.com/reference/kotlin/android/ranging/RangingSession.Callback#onOpened()` will be called when the session finishes starting.

The provided `https://developer.android.com/reference/kotlin/android/ranging/RangingPreference` determines the configuration for the session. A `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` is returned to allow the caller to cancel the session if needed. If the session is canceled, the `https://developer.android.com/reference/kotlin/android/ranging/RangingSession#close()` method will be invoked automatically to release resources.

This method conditionally requires one or more permissions depending on the technologies configured in the `rangingPreference`:

- `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RANGING:kotlin.String` is required for UWB, BLE, or RTT ranging sessions.
- `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` is required for Location-based or UWB DL-TDoA ranging sessions.
- `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_BACKGROUND_LOCATION:kotlin.String` is additionally required if Location-based or UWB DL-TDoA ranging is initiated or continues while the application is in the background.

| Parameters ||
|---|---|
| `rangingPreference` | [RangingPreference](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference): `https://developer.android.com/reference/kotlin/android/ranging/RangingPreference` the preferences for configuring the ranging session. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` | a `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` to close the session. This value cannot be `null`. |

### stop

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stop(): Unit
```

Stops the ranging session.

This method releases any ongoing ranging operations. If the operation fails, it will propagate a `https://developer.android.com/reference/kotlin/android/os/RemoteException.html#` from the system server. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RANGING:kotlin.String`

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
