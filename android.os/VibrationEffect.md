Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VibrationEffect

```
abstract class VibrationEffect : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect#) |

A VibrationEffect describes a haptic effect to be performed by a `https://developer.android.com/reference/kotlin/android/os/Vibrator`.

These effects may be any number of things, from single shot vibrations to complex waveforms.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.BasicEnvelopeBuilder` A builder for waveform effects defined by their envelope, designed to provide a consistent haptic perception across devices with varying capabilities. |
| | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Builder` A builder for composing haptic effects by sequencing various haptic elements. |
| | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition` A composition of haptic elements that are combined to be playable as a single `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#`. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Envelope` Represents a haptic effect defined by an envelope, to be used within a `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Builder`. |
| | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Event` Represents a single event in a vibration composition with a start time relative to the start of the composition. |
| | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Preset` Represents a predefined haptics pattern, corresponding to android. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.VibrationParseException` Exception thrown when parsing a vibration XML fails due to invalid format or values. |
| | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.WaveformEnvelopeBuilder` A builder for waveform effects described by its envelope. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#DEFAULT_AMPLITUDE:kotlin.Int` The default vibration strength of the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_CLICK:kotlin.Int` A click effect. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_DOUBLE_CLICK:kotlin.Int` A double click effect. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_HEAVY_CLICK:kotlin.Int` A heavy click effect. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_TICK:kotlin.Int` A tick effect. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| open static [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect#)! | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#createOneShot(kotlin.Long,%20kotlin.Int)(milliseconds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, amplitude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a one shot vibration. |
| open static [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect#) | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#createPredefined(kotlin.Int)(effectId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a predefined vibration effect. |
| open static [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect#) | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#createRepeatingEffect(android.os.VibrationEffect)(effect: https://developer.android.com/reference/kotlin/android/os/VibrationEffect#)` Creates a new `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` that repeats the given effect indefinitely. |
| --- | --- |
| open static [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect#) | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#createRepeatingEffect(android.os.VibrationEffect,%20android.os.VibrationEffect)(preamble: https://developer.android.com/reference/kotlin/android/os/VibrationEffect#, repeatingEffect: https://developer.android.com/reference/kotlin/android/os/VibrationEffect#)` Creates a new `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` by merging the preamble and repeating vibration effect. |
| open static [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect#)! | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#createWaveform(kotlin.LongArray,%20kotlin.Int)(timings: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html!, repeat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a waveform vibration, using only off/on transitions at the provided time intervals, and potentially repeating. |
| open static [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect#)! | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#createWaveform(kotlin.LongArray,%20kotlin.IntArray,%20kotlin.Int)(timings: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html!, amplitudes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!, repeat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a waveform vibration. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [VibrationEffect.Event](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Event)!\> | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#getEvents()()` Returns a list of `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Event`s that make up this effect. |
| open static [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect#) | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#parseFromXml(java.io.InputStream)(inputStream: https://developer.android.com/reference/kotlin/java/io/InputStream.html#)` Parses a `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` from an XML input stream. |
| --- | --- |
| open static [VibrationEffect.Composition](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition) | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#startComposition()()` Start composing a haptic effect. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/os/Parcelable` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Flatten this object in to a Parcel.

<br />

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator)\< [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect#)!\> | `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### DEFAULT_AMPLITUDE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT_AMPLITUDE: Int
```

The default vibration strength of the device.

 Value: -1

### EFFECT_CLICK

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EFFECT_CLICK: Int
```

A click effect. Use this effect as a baseline, as it's the most common type of click effect.

 Value: 0

### EFFECT_DOUBLE_CLICK

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EFFECT_DOUBLE_CLICK: Int
```

A double click effect.

 Value: 1

### EFFECT_HEAVY_CLICK

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EFFECT_HEAVY_CLICK: Int
```

A heavy click effect. This effect is stronger than `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_CLICK:kotlin.Int`.

 Value: 5

### EFFECT_TICK

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EFFECT_TICK: Int
```

A tick effect. This effect is less strong compared to `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_CLICK:kotlin.Int`.

 Value: 2

## Public methods

### createOneShot

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createOneShot(
    milliseconds: Long, 
    amplitude: Int
): VibrationEffect!
```

Create a one shot vibration.

One shot vibrations will vibrate constantly for the specified period of time at the specified amplitude, and then stop.

| Parameters ||
|---|---|
| `milliseconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The number of milliseconds to vibrate. This must be a positive number. |
| `amplitude` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The strength of the vibration. This must be a value between 1 and 255, or `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#DEFAULT_AMPLITUDE:kotlin.Int`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#!` | The desired effect. |

### createPredefined

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createPredefined(effectId: Int): VibrationEffect
```

Create a predefined vibration effect.

Predefined effects are a set of common vibration effects that should be identical, regardless of the app they come from, in order to provide a cohesive experience for users across the entire device. They also may be custom tailored to the device hardware in order to provide a better experience than you could otherwise build using the generic building blocks.

This will fallback to a generic pattern if one exists and there does not exist a hardware-specific implementation of the effect.

| Parameters ||
|---|---|
| `effectId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The ID of the effect to perform: `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_CLICK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_DOUBLE_CLICK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_TICK:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_TICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_HEAVY_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#EFFECT_DOUBLE_CLICK:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` | The desired effect. This value cannot be `null`. |

### createRepeatingEffect

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createRepeatingEffect(effect: VibrationEffect): VibrationEffect
```

Creates a new `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` that repeats the given effect indefinitely.

The input vibration must not be a repeating vibration. If it is, an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown.

| Parameters ||
|---|---|
| `effect` | [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect#): The `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` that will be repeated. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` | A `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` that repeats the effect indefinitely. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the effect is already a repeating vibration. |

### createRepeatingEffect

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createRepeatingEffect(
    preamble: VibrationEffect, 
    repeatingEffect: VibrationEffect
): VibrationEffect
```

Creates a new `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` by merging the preamble and repeating vibration effect.

Neither input vibration may already be repeating. An `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown if either input vibration is set to repeat indefinitely.

If this method is invoked with mixed effects (one timelined and one legacy), the legacy effect will be converted into a timelined effect. When converting, the effect's duration is estimated, but this estimation is best-effort and may lead to hardware-dependent timing variations. In such cases, the `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Builder#setRepeatingEffect(kotlin.Long,%20android.os.VibrationEffect,%20kotlin.Long)` method is preferred as it allows for explicit control over the timing of the repeating part.

| Parameters ||
|---|---|
| `preamble` | [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect#): The starting vibration effect, which must be finite. This value cannot be `null`. |
| `repeatingEffect` | [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect#): The vibration effect to be repeated indefinitely after the preamble. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` | A `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` that plays the preamble once followed by the \`repeatingEffect\` indefinitely. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if either preamble or repeatingEffect is already a repeating vibration. |

### createWaveform

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createWaveform(
    timings: LongArray!, 
    repeat: Int
): VibrationEffect!
```

Create a waveform vibration, using only off/on transitions at the provided time intervals, and potentially repeating.

In effect, the timings array represents the number of milliseconds *before* turning the vibrator on, followed by the number of milliseconds to keep the vibrator on, then the number of milliseconds turned off, and so on. Consequently, the first timing value will often be 0, so that the effect will start vibrating immediately.

This method is equivalent to calling `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#createWaveform(kotlin.LongArray,%20kotlin.IntArray,%20kotlin.Int)` with corresponding amplitude values alternating between 0 and `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#DEFAULT_AMPLITUDE:kotlin.Int`, beginning with 0.

To cause the pattern to repeat, pass the index into the timings array at which to start the repetition, or -1 to disable repeating. Repeating effects will be played indefinitely and should be cancelled via `https://developer.android.com/reference/kotlin/android/os/Vibrator#cancel()`.

| Parameters ||
|---|---|
| `timings` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!: The pattern of alternating on-off timings, starting with an 'off' timing, and representing the length of time to sustain the individual item (not cumulative). |
| `repeat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index into the timings array at which to repeat, or -1 if you don't want to repeat indefinitely. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#!` | The desired effect. |

### createWaveform

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createWaveform(
    timings: LongArray!, 
    amplitudes: IntArray!, 
    repeat: Int
): VibrationEffect!
```

Create a waveform vibration.

Waveform vibrations are a potentially repeating series of timing and amplitude pairs, provided in separate arrays. For each pair, the value in the amplitude array determines the strength of the vibration and the value in the timing array determines how long it vibrates for, in milliseconds.

To cause the pattern to repeat, pass the index into the timings array at which to start the repetition, or -1 to disable repeating. Repeating effects will be played indefinitely and should be cancelled via `https://developer.android.com/reference/kotlin/android/os/Vibrator#cancel()`.

| Parameters ||
|---|---|
| `timings` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!: The timing values, in milliseconds, of the timing / amplitude pairs. Timing values of 0 will cause the pair to be ignored. |
| `amplitudes` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The amplitude values of the timing / amplitude pairs. Amplitude values must be between 0 and 255, or equal to `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#DEFAULT_AMPLITUDE:kotlin.Int`. An amplitude value of 0 implies the motor is off. |
| `repeat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index into the timings array at which to repeat, or -1 if you don't want to repeat indefinitely. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#!` | The desired effect. |

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getEvents

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEvents(): MutableList<VibrationEffect.Event!>
```

Returns a list of `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Event`s that make up this effect. This effect must NOT be a repeating effect.

This method is used to retrieve the constituent events from a `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#`, primarily for use with `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Builder`.

If this effect was created via the `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition` API, then each primitive will be converted into an event. The start time for each event is calculated using the primitive delay and an estimated duration for all preceding primitives. These estimates are based on the recommended primitive duration targets from [Android Haptics Constants](https://source.android.com/docs/core/interaction/haptics/haptics-constants-primitives). The estimates used are: - 12ms for `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_CLICK:kotlin.Int`, - 5ms for `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_TICK:kotlin.Int`, - 12ms for `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_LOW_TICK:kotlin.Int`, - 500ms for `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_SLOW_RISE:kotlin.Int`, - 150ms for `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_QUICK_RISE:kotlin.Int`, - 100ms for `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_QUICK_FALL:kotlin.Int`, - 300ms for `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_THUD:kotlin.Int`, - 150ms for `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition#PRIMITIVE_SPIN:kotlin.Int`.

Actual primitive durations may differ between devices.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Event!>` | A list of events. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the effect is a repeating effect. |
| `java.lang.UnsupportedOperationException` | if this effect type cannot be represented as a list of events. |

### parseFromXml

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun parseFromXml(inputStream: InputStream): VibrationEffect
```

Parses a `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` from an XML input stream.

This method is suitable for dynamic or real-time use cases, such as loading vibration patterns from a network download, external storage, or strings generated on the fly in memory.

For static vibration patterns bundled inside the application package, see `https://developer.android.com/reference/kotlin/android/view/VibrationEffectInflater.html#from(android.content.Context)`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `inputStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#): The input stream containing the XML. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#` | Parsed `https://developer.android.com/reference/kotlin/android/os/VibrationEffect#`. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.os.VibrationEffect.VibrationParseException` | If there's a parsing error. |

### startComposition

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun startComposition(): VibrationEffect.Composition
```

Start composing a haptic effect.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition`

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<VibrationEffect!>
```
