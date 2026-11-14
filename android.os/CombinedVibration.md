# CombinedVibration

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CombinedVibration

Kotlin| [Java](https://developer.android.com/reference/android/os/CombinedVibration "View this page in Java") 

```
abstract class CombinedVibration : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.CombinedVibration](https://developer.android.com/reference/kotlin/android/os/CombinedVibration#) |

A CombinedVibration describes a combination of haptic effects to be performed by one or more [Vibrators](https://developer.android.com/reference/kotlin/android/os/Vibrator). These effects may be any number of things, from single shot vibrations to complex waveforms.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ParallelCombination](https://developer.android.com/reference/kotlin/android/os/CombinedVibration.ParallelCombination) A combination of haptic effects that should be played in multiple vibrators in parallel. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [CombinedVibration](https://developer.android.com/reference/kotlin/android/os/CombinedVibration#) | [createParallel](https://developer.android.com/reference/kotlin/android/os/CombinedVibration#createParallel(android.os.VibrationEffect))`(`effect:` ` [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect)`)` Create a vibration that plays a single effect in parallel on all vibrators. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/os/CombinedVibration#describeContents())`()` <br /> |
| openstatic [CombinedVibration.ParallelCombination](https://developer.android.com/reference/kotlin/android/os/CombinedVibration.ParallelCombination) | [startParallel](https://developer.android.com/reference/kotlin/android/os/CombinedVibration#startParallel())`()` Start creating a vibration that plays effects in parallel on one or more vibrators. |

| Inherited functions ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Flatten this object in to a Parcel. <br /> | ||

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator)\< [CombinedVibration](https://developer.android.com/reference/kotlin/android/os/CombinedVibration#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/os/CombinedVibration#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### createParallel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createParallel(effect: VibrationEffect): CombinedVibration
```

Create a vibration that plays a single effect in parallel on all vibrators. A parallel vibration that takes a single [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect) to be performed by multiple vibrators at the same time.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect):The [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect) to perform. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [CombinedVibration](https://developer.android.com/reference/kotlin/android/os/CombinedVibration#) | The combined vibration representing the single effect to be played in all vibrators. This value cannot be`null`. |

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### startParallel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun startParallel(): CombinedVibration.ParallelCombination
```

Start creating a vibration that plays effects in parallel on one or more vibrators. A parallel vibration takes one or more [VibrationEffects](https://developer.android.com/reference/kotlin/android/os/VibrationEffect) associated to individual vibrators to be performed at the same time.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [CombinedVibration.ParallelCombination](https://developer.android.com/reference/kotlin/android/os/CombinedVibration.ParallelCombination) | This value cannot be`null`. |

**See Also**

- [android.os.CombinedVibration.ParallelCombination](https://developer.android.com/reference/kotlin/android/os/CombinedVibration.ParallelCombination)

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CombinedVibration!>
```
