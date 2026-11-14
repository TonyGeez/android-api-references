# LightsManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LightsManager

Kotlin| [Java](../android/hardware/lights/LightsManager.md) 
| --- | --- |

```
abstract class LightsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.lights.LightsManager](../android/hardware/lights/LightsManager.md) |

The LightsManager class allows control over device lights.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [LightsSession](../android/hardware/lights/LightsManager.LightsSession.md) Encapsulates a session that can be used to control device lights and represents the lifetime of the requests. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [LightState](../android/hardware/lights/LightState.md) | [getLightState](../android/hardware/lights/LightsManager.md))`(`light:` ` [Light](../android/hardware/lights/Light.md)`)` Returns the state of a specified light. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Light](../android/hardware/lights/Light.md)!\> | [getLights](../android/hardware/lights/LightsManager.md))`()` Returns the lights available on the device. |
| abstract [LightsManager.LightsSession](../android/hardware/lights/LightsManager.LightsSession.md) | [openSession](../android/hardware/lights/LightsManager.md))`()` Creates a new LightsSession that can be used to control the device lights. |
| --- | --- |

## Public methods

### getLightState

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLightState(light: Light): LightState
```

Returns the state of a specified light.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `light` | [Light](../android/hardware/lights/Light.md):This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------|
| [LightState](../android/hardware/lights/LightState.md) | This value cannot be`null`. |

### getLights

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLights(): MutableList<Light!>
```

Returns the lights available on the device.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Light](../android/hardware/lights/Light.md)!> | A list of available lights This value cannot be`null`. |

### openSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun openSession(): LightsManager.LightsSession
```

Creates a new LightsSession that can be used to control the device lights.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [LightsManager.LightsSession](../android/hardware/lights/LightsManager.LightsSession.md) | This value cannot be`null`. |
