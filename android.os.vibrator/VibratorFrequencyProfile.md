# VibratorFrequencyProfile

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VibratorFrequencyProfile

Kotlin| [Java](https://developer.android.com/reference/android/os/vibrator/VibratorFrequencyProfile "View this page in Java") 
| --- | --- |

```
class VibratorFrequencyProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.vibrator.VibratorFrequencyProfile](https://developer.android.com/reference/kotlin/android/os/vibrator/VibratorFrequencyProfile#) |

Describes the output of a [android.os.Vibrator](https://developer.android.com/reference/kotlin/android/os/Vibrator.html#) for different vibration frequencies.

The profile contains the vibrator's frequency range (minimum/maximum) and maximum acceleration, enabling retrieval of supported acceleration levels for specific frequencies, if the device supports independent frequency control.

It also describes the max output acceleration (Gs), of a vibration at different supported frequencies (Hz).

Vibrators without independent frequency control do not have a frequency profile.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | [getFrequenciesOutputAcceleration](https://developer.android.com/reference/kotlin/android/os/vibrator/VibratorFrequencyProfile#getFrequenciesOutputAcceleration())`()` Returns a [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#) representing the vibrator's output acceleration capabilities across different frequencies. |
| [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>? | [getFrequencyRange](https://developer.android.com/reference/kotlin/android/os/vibrator/VibratorFrequencyProfile#getFrequencyRange(kotlin.Float))`(`minOutputAccelerationGs:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Returns the frequency range (in Hz) where the vibrator can sustain at least the given minimum output acceleration (Gs). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMaxFrequencyHz](https://developer.android.com/reference/kotlin/android/os/vibrator/VibratorFrequencyProfile#getMaxFrequencyHz())`()` Gets the maximum frequency supported by the vibrator. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMaxOutputAccelerationGs](https://developer.android.com/reference/kotlin/android/os/vibrator/VibratorFrequencyProfile#getMaxOutputAccelerationGs())`()` Returns the maximum output acceleration (in Gs) supported by the vibrator. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMinFrequencyHz](https://developer.android.com/reference/kotlin/android/os/vibrator/VibratorFrequencyProfile#getMinFrequencyHz())`()` Gets the minimum frequency supported by the vibrator. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getOutputAccelerationGs](https://developer.android.com/reference/kotlin/android/os/vibrator/VibratorFrequencyProfile#getOutputAccelerationGs(kotlin.Float))`(`frequencyHz:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Returns the output acceleration (in Gs) for the given frequency (Hz). |
| --- | --- |

## Public methods

### getFrequenciesOutputAcceleration

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrequenciesOutputAcceleration(): SparseArray<Float!>
```

Returns a [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#) representing the vibrator's output acceleration capabilities across different frequencies. This map defines the maximum acceleration the vibrator can achieve at each supported frequency.

The map's keys are frequencies in Hz, and the corresponding values are the maximum achievable output accelerations in Gs.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!> | A map of frequencies (Hz) to maximum accelerations (Gs). This value cannot be`null`. |

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
| [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!>? | A [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#) object representing the frequency range where the vibrator can sustain at least the given minimum acceleration, or null if the minimum output acceleration cannot be achieved. |

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

Returns the output acceleration (in Gs) for the given frequency (Hz). This method provides the actual acceleration the vibrator will produce when operating at the specified frequency, using linear interpolation over the [getFrequenciesOutputAcceleration()](https://developer.android.com/reference/kotlin/android/os/vibrator/VibratorFrequencyProfile#getFrequenciesOutputAcceleration()).

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------|
| `frequencyHz` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The frequency in Hz. |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The output acceleration in Gs for the given frequency. |
