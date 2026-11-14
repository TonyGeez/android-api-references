# InputManager.InputDeviceListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputDeviceListener

Kotlin| [Java](https://developer.android.com/reference/android/hardware/input/InputManager.InputDeviceListener "View this page in Java") 
| --- | --- |

```
interface InputDeviceListener
```

| [android.hardware.input.InputManager.InputDeviceListener](https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.InputDeviceListener#) |

Listens for changes in input devices.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInputDeviceAdded](https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.InputDeviceListener#onInputDeviceAdded(kotlin.Int))`(`deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever an input device has been added to the system. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInputDeviceChanged](https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.InputDeviceListener#onInputDeviceChanged(kotlin.Int))`(`deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever the properties of an input device have changed since they were last queried. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInputDeviceRemoved](https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.InputDeviceListener#onInputDeviceRemoved(kotlin.Int))`(`deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever an input device has been removed from the system. |
| --- | --- |

## Public methods

### onInputDeviceAdded

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onInputDeviceAdded(deviceId: Int): Unit
```

Called whenever an input device has been added to the system. Use [getInputDevice(int)](https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#getInputDevice(kotlin.Int))to get more information about the device.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------|
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the input device that was added. |

### onInputDeviceChanged

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onInputDeviceChanged(deviceId: Int): Unit
```

Called whenever the properties of an input device have changed since they were last queried. Use [InputManager.getInputDevice](https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#getInputDevice(kotlin.Int))to get a fresh [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice.html#) object with the new properties.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------|
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the input device that changed. |

### onInputDeviceRemoved

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onInputDeviceRemoved(deviceId: Int): Unit
```

Called whenever an input device has been removed from the system.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the input device that was removed. |
