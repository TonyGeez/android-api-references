Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Vibrator

```
abstract class Vibrator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Vibrator](Vibrator.md) |

Class that operates the vibrator on the device.

If your process exits, any vibration you started will stop.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_NO:kotlin.Int` Vibration effect support: unsupported |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_UNKNOWN:kotlin.Int` Vibration effect support: unknown |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_YES:kotlin.Int` Vibration effect support: supported |
| --- | --- |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | areAllEffectsSupported Query whether the vibrator supports all the given effects. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | areAllPrimitivesSupported Query whether the vibrator supports all of the given primitives. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | areEffectsSupported Query whether the vibrator natively supports the given effects. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | areEnvelopeEffectsSupported Checks whether the vibrator supports the creation of envelope effects. |
| open [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html) | arePrimitivesSupported Query whether the vibrator supports the given primitives. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancel Turn the vibrator off. |
| --- | --- |
| open [VibratorEnvelopeEffectInfo](../android.os.vibrator/VibratorEnvelopeEffectInfo.md) | getEnvelopeEffectInfo Retrieves the vibrator's capabilities and limitations for envelope effects. |
| open [VibratorFrequencyProfile](../android.os.vibrator/VibratorFrequencyProfile.md)? | getFrequencyProfile Gets the profile that describes the vibrator output across the supported frequency range. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getId Return the ID of this vibrator. |
| --- | --- |
| open [Duration](../java.time/Duration.md) | getPresetDuration Query the estimated duration of the given preset. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | getPrimitiveDurations Query the estimated durations of the given primitives. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getQFactor Gets the [Q factor](https://en.wikipedia.org/wiki/Q_factor) of the vibrator. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getResonantFrequency Gets the resonant frequency of the vibrator, if applicable. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasAmplitudeControl Check whether the vibrator has amplitude control. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasVibrator Check whether the hardware has a vibrator. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPresetSupported Query whether the vibrator supports the given preset. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | vibrate Vibrate with a given effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | vibrate Vibrate with a given effect. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | vibrate Vibrate with a given effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | vibrate Vibrate constantly for the specified period of time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | vibrate Vibrate constantly for the specified period of time. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | vibrate Vibrate with a given pattern. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | vibrate Vibrate with a given pattern. |

## Constants

### VIBRATION_EFFECT_SUPPORT_NO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIBRATION_EFFECT_SUPPORT_NO: Int
```

Vibration effect support: unsupported

This effect is **not** natively supported by the underlying hardware, although the system may still play a fallback vibration.

 Value: 2

### VIBRATION_EFFECT_SUPPORT_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIBRATION_EFFECT_SUPPORT_UNKNOWN: Int
```

Vibration effect support: unknown

The hardware doesn't report its supported effects, so we can't determine whether the effect is supported or not.

 Value: 0

### VIBRATION_EFFECT_SUPPORT_YES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIBRATION_EFFECT_SUPPORT_YES: Int
```

Vibration effect support: supported

This effect is supported by the underlying hardware.

 Value: 1

## Public methods

### areAllEffectsSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun areAllEffectsSupported(vararg effectIds: Int): Int
```

Query whether the vibrator supports all the given effects. If no argument is provided this method will always return `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_YES:kotlin.Int`.

If an effect is not supported, the system may still automatically fall back to a simpler vibration instead, which is not optimised for the specific device, however vibration isn't guaranteed in this case.

If the result is `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_YES:kotlin.Int`, all effects in the query are supported by the hardware.

If the result is `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_NO:kotlin.Int`, at least one of the effects in the query is not supported, and using them may fall back to an un-optimized vibration or no vibration.

If the result is `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_UNKNOWN:kotlin.Int`, the system doesn't know whether all the effects are supported. It may support any or all of the queried effects, but there's no way to programmatically know whether a #vibrate call will successfully cause a vibration. It's guaranteed, however, that none of the queried effects are definitively unsupported by the hardware.

Use areEffectsSupported to get individual results for each effect.

| Parameters ||
|---|---|
| `effectIds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which effects to query for. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_TICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_HEAVY_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_DOUBLE_CLICK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Whether all specified effects are natively supported by the device. Empty query defaults to `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_YES:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_YES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_NO:kotlin.Int` |

### areAllPrimitivesSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun areAllPrimitivesSupported(vararg primitiveIds: Int): Boolean
```

Query whether the vibrator supports all of the given primitives. If no argument is provided this method will always return `true`.

If a primitive is not supported by the device, then *no vibration* will occur if it is played.

Use arePrimitivesSupported to get individual results for each primitive.

| Parameters ||
|---|---|
| `primitiveIds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which primitives to query for. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_THUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_SPIN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_QUICK_RISE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_SLOW_RISE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_QUICK_FALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_TICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_LOW_TICK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether all specified primitives are supported. Empty query defaults to `true`. |

### areEffectsSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun areEffectsSupported(vararg effectIds: Int): IntArray
```

Query whether the vibrator natively supports the given effects.

If an effect is not supported, the system may still automatically fall back to playing a simpler vibration instead, which is not optimised for the specific device. This includes the unknown case, which can't be determined in advance, that will dynamically attempt to fall back if the optimised effect fails to play.

The returned array will be the same length as the query array and the value at a given index will contain `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_YES:kotlin.Int` if the effect at that same index in the querying array is supported, `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_NO:kotlin.Int` if it isn't supported, or `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_UNKNOWN:kotlin.Int` if the system can't determine whether it's supported or not, as some hardware doesn't report its effect capabilities.

Use areAllEffectsSupported to get a single combined result, or for convenience when querying exactly one effect.

| Parameters ||
|---|---|
| `effectIds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which effects to query for. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_TICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_HEAVY_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_DOUBLE_CLICK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | An array containing the systems current knowledge about whether the given effects are natively supported by the device, or not. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_YES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/Vibrator#VIBRATION_EFFECT_SUPPORT_NO:kotlin.Int` |

### areEnvelopeEffectsSupported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun areEnvelopeEffectsSupported(): Boolean
```

Checks whether the vibrator supports the creation of envelope effects. Envelope effects are defined by a series of frequency-amplitude pairs with specified transition times, allowing the creation of more complex vibration patterns.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the hardware supports creating envelope effects, false otherwise. |

### arePrimitivesSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun arePrimitivesSupported(vararg primitiveIds: Int): BooleanArray
```

Query whether the vibrator supports the given primitives. The returned array will be the same length as the query array and the value at a given index will contain whether the effect at that same index in the querying array is supported or not.

If a primitive is not supported by the device, then *no vibration* will occur if it is played.

Use areAllPrimitivesSupported to get a single combined result, or for convenience when querying exactly one primitive.

| Parameters ||
|---|---|
| `primitiveIds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which primitives to query for. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_THUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_SPIN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_QUICK_RISE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_SLOW_RISE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_QUICK_FALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_TICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_LOW_TICK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html` | Whether the primitives are supported. This value cannot be `null`. |

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun cancel(): Unit
```

Turn the vibrator off. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#VIBRATE:kotlin.String`

### getEnvelopeEffectInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEnvelopeEffectInfo(): VibratorEnvelopeEffectInfo
```

Retrieves the vibrator's capabilities and limitations for envelope effects.

These parameters can be used with `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.WaveformEnvelopeBuilder` to create custom envelope effects.

| Return ||
|---|---|
| VibratorEnvelopeEffectInfo | The vibrator's envelope effect information, or null if not supported. If this vibrator is a composite of multiple physical devices then this will return a profile supported in all devices, or null if the intersection is empty or not available. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.WaveformEnvelopeBuilder`

### getFrequencyProfile

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFrequencyProfile(): VibratorFrequencyProfile?
```

Gets the profile that describes the vibrator output across the supported frequency range.

The profile describes the output acceleration that the device can reach when it vibrates at different frequencies.

| Return ||
|---|---|
| VibratorFrequencyProfile | The frequency profile for this vibrator, or null if the vibrator does not have frequency control. If this vibrator is a composite of multiple physical devices then this will return a profile supported in all devices, or null if the intersection is empty or not available. |

### getId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getId(): Int
```

Return the ID of this vibrator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A non-negative integer representing the id of the vibrator controlled by this service, or -1 this service is not attached to any physical vibrator. |

### getPresetDuration

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPresetDuration(presetId: Int): Duration
```

Query the estimated duration of the given preset.

| Parameters ||
|---|---|
| `presetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which preset to query for. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Preset#PRESET_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Preset#PRESET_TICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Preset#PRESET_LOW_TICK:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#` | The duration of the preset as a `https://developer.android.com/reference/kotlin/java/time/Duration.html#`. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the preset is not supported. |

### getPrimitiveDurations

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPrimitiveDurations(vararg primitiveIds: Int): IntArray
```

Query the estimated durations of the given primitives.

The returned array will be the same length as the query array and the value at a given index will contain the duration in milliseconds of the effect at the same index in the querying array.

The duration will be positive for primitives that are supported and zero for the unsupported ones, in correspondence with arePrimitivesSupported.

| Parameters ||
|---|---|
| `primitiveIds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which primitives to query for. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_THUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_SPIN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_QUICK_RISE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_SLOW_RISE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_QUICK_FALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_TICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_LOW_TICK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | The duration of each primitive, with zeroes for primitives that are not supported. This value cannot be `null`. |

### getQFactor

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getQFactor(): Float
```

Gets the [Q factor](https://en.wikipedia.org/wiki/Q_factor) of the vibrator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the Q factor of the vibrator, or `https://developer.android.com/reference/kotlin/java/lang/Float.html#NaN:kotlin.Float` if it's unknown, not applicable, or if this vibrator is a composite of multiple physical devices with different Q factors. |

### getResonantFrequency

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResonantFrequency(): Float
```

Gets the resonant frequency of the vibrator, if applicable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the resonant frequency of the vibrator, or `https://developer.android.com/reference/kotlin/java/lang/Float.html#NaN:kotlin.Float` if it's unknown, not applicable, or if this vibrator is a composite of multiple physical devices with different frequencies. |

### hasAmplitudeControl

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun hasAmplitudeControl(): Boolean
```

Check whether the vibrator has amplitude control.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the hardware can control the amplitude of the vibrations, otherwise false. |

### hasVibrator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun hasVibrator(): Boolean
```

Check whether the hardware has a vibrator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the hardware has a vibrator, else false. |

### isPresetSupported

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPresetSupported(presetId: Int): Boolean
```

Query whether the vibrator supports the given preset.

| Parameters ||
|---|---|
| `presetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which preset to query for. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Preset#PRESET_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Preset#PRESET_TICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Preset#PRESET_LOW_TICK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the preset is supported. |

### vibrate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun vibrate(vibe: VibrationEffect!): Unit
```

Vibrate with a given effect.

The app should be in the foreground for the vibration to happen.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#VIBRATE:kotlin.String`

| Parameters ||
|---|---|
| `vibe` | [VibrationEffect](VibrationEffect.md)!: VibrationEffect describing the vibration to be performed. |

### vibrate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun vibrate(
    vibe: VibrationEffect!, 
    attributes: AudioAttributes!
): Unit
```

**Deprecated:** *Use vibrate instead.*

Vibrate with a given effect.

The app should be in the foreground for the vibration to happen. Background apps should specify a ringtone, notification or alarm usage in order to vibrate.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#VIBRATE:kotlin.String`

| Parameters ||
|---|---|
| `vibe` | [VibrationEffect](VibrationEffect.md)!: VibrationEffect describing the vibration to be performed. |
| `attributes` | [AudioAttributes](../android.media/AudioAttributes.md)!: `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#` corresponding to the vibration. For example, specify `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#USAGE_ALARM:kotlin.Int` for alarm vibrations or `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#USAGE_NOTIFICATION_RINGTONE:kotlin.Int` for vibrations associated with incoming calls. |

### vibrate

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun vibrate(
    vibe: VibrationEffect, 
    attributes: VibrationAttributes
): Unit
```

Vibrate with a given effect.

The app should be in the foreground for the vibration to happen. Background apps should specify a ringtone, notification or alarm usage in order to vibrate.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#VIBRATE:kotlin.String`

| Parameters ||
|---|---|
| `vibe` | [VibrationEffect](VibrationEffect.md): VibrationEffect describing the vibration to be performed. This value cannot be `null`. |
| `attributes` | [VibrationAttributes](VibrationAttributes.md): VibrationAttributes corresponding to the vibration. For example, specify `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_ALARM:kotlin.Int` for alarm vibrations or `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_RINGTONE:kotlin.Int` for vibrations associated with incoming calls. This value cannot be `null`. |

### vibrate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun vibrate(milliseconds: Long): Unit
```

**Deprecated:** *Use vibrate instead.*

Vibrate constantly for the specified period of time.

The app should be in the foreground for the vibration to happen.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#VIBRATE:kotlin.String`

| Parameters ||
|---|---|
| `milliseconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The number of milliseconds to vibrate. |

### vibrate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun vibrate(
    milliseconds: Long, 
    attributes: AudioAttributes!
): Unit
```

**Deprecated:** *Use vibrate instead.*

Vibrate constantly for the specified period of time.

The app should be in the foreground for the vibration to happen. Background apps should specify a ringtone, notification or alarm usage in order to vibrate.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#VIBRATE:kotlin.String`

| Parameters ||
|---|---|
| `milliseconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The number of milliseconds to vibrate. |
| `attributes` | [AudioAttributes](../android.media/AudioAttributes.md)!: `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#` corresponding to the vibration. For example, specify `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#USAGE_ALARM:kotlin.Int` for alarm vibrations or `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#USAGE_NOTIFICATION_RINGTONE:kotlin.Int` for vibrations associated with incoming calls. |

### vibrate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun vibrate(
    pattern: LongArray!, 
    repeat: Int
): Unit
```

**Deprecated:** *Use vibrate instead.*

Vibrate with a given pattern.

Pass in an array of ints that are the durations for which to turn on or off the vibrator in milliseconds. The first value indicates the number of milliseconds to wait before turning the vibrator on. The next value indicates the number of milliseconds for which to keep the vibrator on before turning it off. Subsequent values alternate between durations in milliseconds to turn the vibrator off or to turn the vibrator on.

To cause the pattern to repeat, pass the index into the pattern array at which to start the repeat, or -1 to disable repeating.

The app should be in the foreground for the vibration to happen.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#VIBRATE:kotlin.String`

| Parameters ||
|---|---|
| `pattern` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!: an array of longs of times for which to turn the vibrator on or off. |
| `repeat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index into pattern at which to repeat, or -1 if you don't want to repeat. |

### vibrate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun vibrate(
    pattern: LongArray!, 
    repeat: Int, 
    attributes: AudioAttributes!
): Unit
```

**Deprecated:** *Use vibrate instead.*

Vibrate with a given pattern.

Pass in an array of ints that are the durations for which to turn on or off the vibrator in milliseconds. The first value indicates the number of milliseconds to wait before turning the vibrator on. The next value indicates the number of milliseconds for which to keep the vibrator on before turning it off. Subsequent values alternate between durations in milliseconds to turn the vibrator off or to turn the vibrator on.

To cause the pattern to repeat, pass the index into the pattern array at which to start the repeat, or -1 to disable repeating.

The app should be in the foreground for the vibration to happen. Background apps should specify a ringtone, notification or alarm usage in order to vibrate.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#VIBRATE:kotlin.String`

| Parameters ||
|---|---|
| `pattern` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!: an array of longs of times for which to turn the vibrator on or off. |
| `repeat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index into pattern at which to repeat, or -1 if you don't want to repeat. |
| `attributes` | [AudioAttributes](../android.media/AudioAttributes.md)!: `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#` corresponding to the vibration. For example, specify `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#USAGE_ALARM:kotlin.Int` for alarm vibrations or `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#USAGE_NOTIFICATION_RINGTONE:kotlin.Int` for vibrations associated with incoming calls. |
| --- | --- |
