Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HidManager

```
class HidManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.hid.HidManager](https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager#) |

Provides access to Human Interface Device (HID) nodes.

This manager allows applications to enumerate connected HID devices and query their information (such as vendor/product IDs and report descriptors).

HID devices include peripherals such as keyboards, mice, game controllers, and other interactive devices that follow the HID specification.

Access to HID devices requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HID:kotlin.String` permission. Apps are typically granted access to specific devices via a system-provided chooser or permission dialog.

Device access may be restricted when the application is in the background or in a cached state to ensure system security and resource efficiency.

## Summary

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager#canEnumerateDevices()()` Checks if the calling app has the necessary permissions to enumerate connected HID devices. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [HidDevice](https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice)!\> | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager#getDevices()()` Returns a list of all currently connected HID devices. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager#registerListener(android.hardware.hid.HidDeviceListener,%20java.util.concurrent.Executor)(listener: https://developer.android.com/reference/kotlin/android/hardware/hid/HidDeviceListener, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)` Registers a listener to receive notifications about HID device lifecycle events. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager#unregisterListener(android.hardware.hid.HidDeviceListener)(listener: https://developer.android.com/reference/kotlin/android/hardware/hid/HidDeviceListener)` Unregisters a previously registered listener for HID device lifecycle events. |

## Public methods

### canEnumerateDevices

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun canEnumerateDevices(): Boolean
```

Checks if the calling app has the necessary permissions to enumerate connected HID devices.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the calling app can enumerate HIDs, `false` otherwise. |

### getDevices

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDevices(): MutableList<HidDevice!>
```

Returns a list of all currently connected HID devices.

The returned list contains `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice` objects representing each connected HID node that the system has detected and made available.

It is recommended to call `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager#canEnumerateDevices()` before calling this method. 
This method may take several seconds to complete, so it should only be called from a worker thread. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HID:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice!>` | a list of connected HID devices, or an empty list if no devices are connected. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if called on the main thread. |
| `java.lang.SecurityException` | if the caller does not have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HID:kotlin.String` permission or if `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager#canEnumerateDevices()` returns `false`. |

### registerListener

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerListener(
    listener: HidDeviceListener, 
    executor: Executor
): Unit
```

Registers a listener to receive notifications about HID device lifecycle events.

When a HID device is physically connected to or disconnected from the system, the provided `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDeviceListener` will be notified. If the listener is already registered, this call does nothing.

All callback methods on the listener will be invoked using the provided `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`.

Upon registration, `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDeviceListener#onHidDeviceAdded(android.hardware.hid.HidDevice)` will be immediately invoked for all HID devices currently connected to the system. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HID:kotlin.String`

| Parameters ||
|---|---|
| `listener` | [HidDeviceListener](https://developer.android.com/reference/kotlin/android/hardware/hid/HidDeviceListener): The listener to receive device addition and removal events. Must not be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which the listener methods will be invoked. Must not be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager#unregisterListener(android.hardware.hid.HidDeviceListener)`

### unregisterListener

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterListener(listener: HidDeviceListener): Unit
```

Unregisters a previously registered listener for HID device lifecycle events.

Once unregistered, the listener will no longer receive notifications when HID devices are added to or removed from the system. If the provided listener was not previously registered via `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager#registerListener(android.hardware.hid.HidDeviceListener,%20java.util.concurrent.Executor)`, this call does nothing.

After this method returns, no further callbacks will be dispatched to the executor associated with this listener. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HID:kotlin.String`

| Parameters ||
|---|---|
| `listener` | [HidDeviceListener](https://developer.android.com/reference/kotlin/android/hardware/hid/HidDeviceListener): The listener to unregister. Must not be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager#registerListener(android.hardware.hid.HidDeviceListener,%20java.util.concurrent.Executor)`
