# CombinedVibration

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CombinedVibration

Kotlin| [Java](../android/os/CombinedVibration.md) 
| --- | --- |

```
abstract class CombinedVibration : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.CombinedVibration](../android/os/CombinedVibration.md) |

A CombinedVibration describes a combination of haptic effects to be performed by one or more [Vibrators](../android/os/Vibrator.md). These effects may be any number of things, from single shot vibrations to complex waveforms.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ParallelCombination](../android/os/CombinedVibration.ParallelCombination.md) A combination of haptic effects that should be played in multiple vibrators in parallel. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [CombinedVibration](../android/os/CombinedVibration.md) | [createParallel](../android/os/CombinedVibration.md))`(`effect:` ` [VibrationEffect](../android/os/VibrationEffect.md)`)` Create a vibration that plays a single effect in parallel on all vibrators. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/os/CombinedVibration.md))`()` <br /> |
| openstatic [CombinedVibration.ParallelCombination](../android/os/CombinedVibration.ParallelCombination.md) | [startParallel](../android/os/CombinedVibration.md))`()` Start creating a vibration that plays effects in parallel on one or more vibrators. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/os/Parcelable.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Flatten this object in to a Parcel. <br /> | ||

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CombinedVibration](../android/os/CombinedVibration.md)!\> | [CREATOR](../android/os/CombinedVibration.md) <br /> |

## Public methods

### createParallel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createParallel(effect: VibrationEffect): CombinedVibration
```

Create a vibration that plays a single effect in parallel on all vibrators. A parallel vibration that takes a single [VibrationEffect](../android/os/VibrationEffect.md) to be performed by multiple vibrators at the same time.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [VibrationEffect](../android/os/VibrationEffect.md):The [VibrationEffect](../android/os/VibrationEffect.md) to perform. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [CombinedVibration](../android/os/CombinedVibration.md) | The combined vibration representing the single effect to be played in all vibrators. This value cannot be`null`. |

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### startParallel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun startParallel(): CombinedVibration.ParallelCombination
```

Start creating a vibration that plays effects in parallel on one or more vibrators. A parallel vibration takes one or more [VibrationEffects](../android/os/VibrationEffect.md) associated to individual vibrators to be performed at the same time.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [CombinedVibration.ParallelCombination](../android/os/CombinedVibration.ParallelCombination.md) | This value cannot be`null`. |

**See Also**

- [android.os.CombinedVibration.ParallelCombination](../android/os/CombinedVibration.ParallelCombination.md)

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CombinedVibration!>
```
