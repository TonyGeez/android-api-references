Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HidDeviceListener

```
interface HidDeviceListener
```

| [android.hardware.hid.HidDeviceListener](HidDeviceListener.md) |

Interface for receiving HID device connectivity updates.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onHidDeviceAdded Called when a HID device is added. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onHidDeviceRemoved Called when a HID device is removed. |

## Public methods

### onHidDeviceAdded

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onHidDeviceAdded(device: HidDevice): Unit
```

Called when a HID device is added.

| Parameters ||
|---|---|
| `device` | [HidDevice](HidDevice.md): The HID device that was added. This value cannot be `null`. |

### onHidDeviceRemoved

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onHidDeviceRemoved(device: HidDevice): Unit
```

Called when a HID device is removed.

| Parameters ||
|---|---|
| `device` | [HidDevice](HidDevice.md): The HID device that was removed. This value cannot be `null`. |
