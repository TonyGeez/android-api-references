# VirtualDeviceManager.VirtualDeviceListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VirtualDeviceListener

Kotlin| [Java](../android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener.md) 
| --- | --- |

```
interface VirtualDeviceListener
```

| [android.companion.virtual.VirtualDeviceManager.VirtualDeviceListener](../android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener.md) |

Listener for changes in the available virtual devices.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onVirtualDeviceClosed](../android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener.md))`(`deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever a virtual device has been removed from the system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onVirtualDeviceCreated](../android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener.md))`(`deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever a new virtual device has been added to the system. |

## Public methods

### onVirtualDeviceClosed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onVirtualDeviceClosed(deviceId: Int): Unit
```

Called whenever a virtual device has been removed from the system.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------|
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the virtual device that was removed. |

### onVirtualDeviceCreated

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onVirtualDeviceCreated(deviceId: Int): Unit
```

Called whenever a new virtual device has been added to the system. Use [VirtualDeviceManager.getVirtualDevice(int)](../android/companion/virtual/VirtualDeviceManager.md))to get more information about the device.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the virtual device that was added. |
