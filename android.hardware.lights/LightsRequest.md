Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LightsRequest

Kotlin | [Java](../android/hardware/lights/LightsRequest.md)
| --- | --- |

```
class LightsRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.lights.LightsRequest](../android/hardware/lights/LightsRequest.md) |

Encapsulates a request to modify the state of multiple lights.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/hardware/lights/LightsRequest.Builder` Builder for creating device light change requests. |

| Public methods ||
|---|---|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [LightState](../android/hardware/lights/LightState.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/lights/LightsRequest#getLightStates()()` Get a list of LightState. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/lights/LightsRequest#getLights()()` Get a list of Light as ids. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Light](../android/hardware/lights/Light.md)!, [LightState](../android/hardware/lights/LightState.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/lights/LightsRequest#getLightsAndStates()()` Get a map of lights and states. |
| --- | --- |

## Public methods

### getLightStates

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLightStates(): MutableList<LightState!>
```

Get a list of LightState. The states will be returned in same order as the light ids returned by `https://developer.android.com/reference/kotlin/android/hardware/lights/LightsRequest#getLights()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/lights/LightState!>` | List of light states. This value cannot be `null`. |

### getLights

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLights(): MutableList<Int!>
```

Get a list of Light as ids.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | List of light ids in the request. This value cannot be `null`. |

### getLightsAndStates

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLightsAndStates(): MutableMap<Light!, LightState!>
```

Get a map of lights and states. The map will contain all the lights as keys and the corresponding LightState requested as values.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://developer.android.com/reference/kotlin/android/hardware/lights/Light!, https://developer.android.com/reference/kotlin/android/hardware/lights/LightState!>` | This value cannot be `null`. |
