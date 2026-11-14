# InputManager.InputDeviceListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputDeviceListener

Kotlin| [Java](../android/hardware/input/InputManager.InputDeviceListener.md) 
| --- | --- |

```
interface InputDeviceListener
```

| [android.hardware.input.InputManager.InputDeviceListener](../android/hardware/input/InputManager.InputDeviceListener.md) |

Listens for changes in input devices.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInputDeviceAdded](../android/hardware/input/InputManager.InputDeviceListener.md))`(`deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever an input device has been added to the system. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInputDeviceChanged](../android/hardware/input/InputManager.InputDeviceListener.md))`(`deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever the properties of an input device have changed since they were last queried. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInputDeviceRemoved](../android/hardware/input/InputManager.InputDeviceListener.md))`(`deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever an input device has been removed from the system. |
| --- | --- |

## Public methods

### onInputDeviceAdded

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onInputDeviceAdded(deviceId: Int): Unit
```

Called whenever an input device has been added to the system. Use [getInputDevice(int)](../android/hardware/input/InputManager.md))to get more information about the device.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------|
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the input device that was added. |

### onInputDeviceChanged

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onInputDeviceChanged(deviceId: Int): Unit
```

Called whenever the properties of an input device have changed since they were last queried. Use [InputManager.getInputDevice](../android/hardware/input/InputManager.md))to get a fresh [InputDevice](../android/view/InputDevice.md) object with the new properties.

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
