Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HidDeviceListener

```
interface HidDeviceListener
```

| [android.hardware.hid.HidDeviceListener](https://developer.android.com/reference/kotlin/android/hardware/hid/HidDeviceListener#) |

Interface for receiving HID device connectivity updates.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDeviceListener#onHidDeviceAdded(android.hardware.hid.HidDevice)(device: https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice)` Called when a HID device is added. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDeviceListener#onHidDeviceRemoved(android.hardware.hid.HidDevice)(device: https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice)` Called when a HID device is removed. |

## Public methods

### onHidDeviceAdded

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onHidDeviceAdded(device: HidDevice): Unit
```

Called when a HID device is added.

| Parameters ||
|---|---|
| `device` | [HidDevice](https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice): The HID device that was added. This value cannot be `null`. |

### onHidDeviceRemoved

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onHidDeviceRemoved(device: HidDevice): Unit
```

Called when a HID device is removed.

| Parameters ||
|---|---|
| `device` | [HidDevice](https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice): The HID device that was removed. This value cannot be `null`. |
