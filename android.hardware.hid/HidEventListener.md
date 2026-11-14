Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HidEventListener

```
interface HidEventListener
```

| [android.hardware.hid.HidEventListener](HidEventListener.md) |

Listener for receiving events from a `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice`.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidEventListener#onDisconnected()()` Called when the HID device has been closed or disconnected. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidEventListener#onError(java.lang.Exception)(cause: https://developer.android.com/reference/kotlin/java/lang/Exception.html#)` Called when an error occurs during HID input report processing. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidEventListener#onInputReport(android.hardware.hid.Report)(report: https://developer.android.com/reference/kotlin/android/hardware/hid/Report)` Called when an input report is received from the HID device. |
| --- | --- |

## Public methods

### onDisconnected

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onDisconnected(): Unit
```

Called when the HID device has been closed or disconnected.

This is the definitive signal that the device session has ended. All registered listeners (including this instance) are automatically unregistered, and the device is no longer usable.

### onError

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onError(cause: Exception): Unit
```

Called when an error occurs during HID input report processing.

This callback is purely informative and **never** unregisters listeners. On non-fatal errors, report processing continues. On fatal errors, this callback is immediately followed by an explicit `https://developer.android.com/reference/kotlin/android/hardware/hid/HidEventListener#onDisconnected()` invocation.

| Parameters ||
|---|---|
| `cause` | [Exception](../java.lang/Exception.md): The exception describing the error. This value cannot be `null`. |

### onInputReport

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onInputReport(report: Report): Unit
```

Called when an input report is received from the HID device.

| Parameters ||
|---|---|
| `report` | [Report](Report.md): This value cannot be `null`. |
