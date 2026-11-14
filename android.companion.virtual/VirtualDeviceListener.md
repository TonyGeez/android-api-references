# VirtualDeviceManager.VirtualDeviceListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VirtualDeviceListener

Kotlin| [Java](https://developer.android.com/reference/android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener "View this page in Java") 
| --- | --- |

```
interface VirtualDeviceListener
```

| [android.companion.virtual.VirtualDeviceManager.VirtualDeviceListener](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener#) |

Listener for changes in the available virtual devices.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onVirtualDeviceClosed](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener#onVirtualDeviceClosed(kotlin.Int))`(`deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever a virtual device has been removed from the system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onVirtualDeviceCreated](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener#onVirtualDeviceCreated(kotlin.Int))`(`deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever a new virtual device has been added to the system. |

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

Called whenever a new virtual device has been added to the system. Use [VirtualDeviceManager.getVirtualDevice(int)](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager#getVirtualDevice(kotlin.Int))to get more information about the device.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the virtual device that was added. |
