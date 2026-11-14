# LightsManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LightsManager

Kotlin| [Java](https://developer.android.com/reference/android/hardware/lights/LightsManager "View this page in Java") 

```
abstract class LightsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.lights.LightsManager](https://developer.android.com/reference/kotlin/android/hardware/lights/LightsManager#) |

The LightsManager class allows control over device lights.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [LightsSession](https://developer.android.com/reference/kotlin/android/hardware/lights/LightsManager.LightsSession) Encapsulates a session that can be used to control device lights and represents the lifetime of the requests. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [LightState](https://developer.android.com/reference/kotlin/android/hardware/lights/LightState) | [getLightState](https://developer.android.com/reference/kotlin/android/hardware/lights/LightsManager#getLightState(android.hardware.lights.Light))`(`light:` ` [Light](https://developer.android.com/reference/kotlin/android/hardware/lights/Light)`)` Returns the state of a specified light. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Light](https://developer.android.com/reference/kotlin/android/hardware/lights/Light)!\> | [getLights](https://developer.android.com/reference/kotlin/android/hardware/lights/LightsManager#getLights())`()` Returns the lights available on the device. |
| abstract [LightsManager.LightsSession](https://developer.android.com/reference/kotlin/android/hardware/lights/LightsManager.LightsSession) | [openSession](https://developer.android.com/reference/kotlin/android/hardware/lights/LightsManager#openSession())`()` Creates a new LightsSession that can be used to control the device lights. |

## Public methods

### getLightState

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLightState(light: Light): LightState
```

Returns the state of a specified light.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `light` | [Light](https://developer.android.com/reference/kotlin/android/hardware/lights/Light):This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------|
| [LightState](https://developer.android.com/reference/kotlin/android/hardware/lights/LightState) | This value cannot be`null`. |

### getLights

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLights(): MutableList<Light!>
```

Returns the lights available on the device.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Light](https://developer.android.com/reference/kotlin/android/hardware/lights/Light)!> | A list of available lights This value cannot be`null`. |

### openSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun openSession(): LightsManager.LightsSession
```

Creates a new LightsSession that can be used to control the device lights.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [LightsManager.LightsSession](https://developer.android.com/reference/kotlin/android/hardware/lights/LightsManager.LightsSession) | This value cannot be`null`. |
