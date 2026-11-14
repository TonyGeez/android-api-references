# VibratorFrequencyProfile

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VibratorFrequencyProfile

Kotlin| [Java](../android/os/vibrator/VibratorFrequencyProfile.md) 
| --- | --- |

```
class VibratorFrequencyProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.vibrator.VibratorFrequencyProfile](../android/os/vibrator/VibratorFrequencyProfile.md) |

Describes the output of a [android.os.Vibrator](../android/os/Vibrator.md) for different vibration frequencies.

The profile contains the vibrator's frequency range (minimum/maximum) and maximum acceleration, enabling retrieval of supported acceleration levels for specific frequencies, if the device supports independent frequency control.

It also describes the max output acceleration (Gs), of a vibration at different supported frequencies (Hz).

Vibrators without independent frequency control do not have a frequency profile.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SparseArray](../android/util/SparseArray.md)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | [getFrequenciesOutputAcceleration](../android/os/vibrator/VibratorFrequencyProfile.md))`()` Returns a [SparseArray](../android/util/SparseArray.md) representing the vibrator's output acceleration capabilities across different frequencies. |
| [Range](../android/util/Range.md)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>? | [getFrequencyRange](../android/os/vibrator/VibratorFrequencyProfile.md))`(`minOutputAccelerationGs:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Returns the frequency range (in Hz) where the vibrator can sustain at least the given minimum output acceleration (Gs). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMaxFrequencyHz](../android/os/vibrator/VibratorFrequencyProfile.md))`()` Gets the maximum frequency supported by the vibrator. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMaxOutputAccelerationGs](../android/os/vibrator/VibratorFrequencyProfile.md))`()` Returns the maximum output acceleration (in Gs) supported by the vibrator. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMinFrequencyHz](../android/os/vibrator/VibratorFrequencyProfile.md))`()` Gets the minimum frequency supported by the vibrator. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getOutputAccelerationGs](../android/os/vibrator/VibratorFrequencyProfile.md))`(`frequencyHz:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Returns the output acceleration (in Gs) for the given frequency (Hz). |
| --- | --- |

## Public methods

### getFrequenciesOutputAcceleration

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrequenciesOutputAcceleration(): SparseArray<Float!>
```

Returns a [SparseArray](../android/util/SparseArray.md) representing the vibrator's output acceleration capabilities across different frequencies. This map defines the maximum acceleration the vibrator can achieve at each supported frequency.

The map's keys are frequencies in Hz, and the corresponding values are the maximum achievable output accelerations in Gs.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [SparseArray](../android/util/SparseArray.md)< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!> | A map of frequencies (Hz) to maximum accelerations (Gs). This value cannot be`null`. |

### getFrequencyRange

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrequencyRange(minOutputAccelerationGs: Float): Range<Float!>?
```

Returns the frequency range (in Hz) where the vibrator can sustain at least the given minimum output acceleration (Gs).

| Parameters ||
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `minOutputAccelerationGs` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The minimum desired output acceleration in Gs. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Range](../android/util/Range.md)< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!>? | A [Range](../android/util/Range.md) object representing the frequency range where the vibrator can sustain at least the given minimum acceleration, or null if the minimum output acceleration cannot be achieved. |

### getMaxFrequencyHz

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxFrequencyHz(): Float
```

Gets the maximum frequency supported by the vibrator.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the maximum frequency supported by the vibrator, in hertz. |

### getMaxOutputAccelerationGs

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxOutputAccelerationGs(): Float
```

Returns the maximum output acceleration (in Gs) supported by the vibrator. This value represents the highest acceleration the vibrator can achieve across its entire frequency range.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The maximum output acceleration in Gs. |

### getMinFrequencyHz

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMinFrequencyHz(): Float
```

Gets the minimum frequency supported by the vibrator.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the minimum frequency supported by the vibrator, in hertz. |

### getOutputAccelerationGs

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutputAccelerationGs(frequencyHz: Float): Float
```

Returns the output acceleration (in Gs) for the given frequency (Hz). This method provides the actual acceleration the vibrator will produce when operating at the specified frequency, using linear interpolation over the [getFrequenciesOutputAcceleration()](../android/os/vibrator/VibratorFrequencyProfile.md)).

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------|
| `frequencyHz` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The frequency in Hz. |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The output acceleration in Gs for the given frequency. |
