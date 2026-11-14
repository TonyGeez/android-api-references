# PlaybackParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PlaybackParams

Kotlin| [Java](../android/media/PlaybackParams.md) 
| --- | --- |

```
class PlaybackParams : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.PlaybackParams](../android/media/PlaybackParams.md) |

Structure for common playback params. Used by [AudioTrack](../android/media/AudioTrack.md) [AudioTrack.getPlaybackParams()](../android/media/AudioTrack.md))and [AudioTrack.setPlaybackParams(PlaybackParams)](../android/media/AudioTrack.md))to control playback behavior.

**audio fallback mode:**select out-of-range parameter handling.

- [PlaybackParams.AUDIO_FALLBACK_MODE_DEFAULT](../android/media/PlaybackParams.md): System will determine best handling.
- [PlaybackParams.AUDIO_FALLBACK_MODE_MUTE](../android/media/PlaybackParams.md): Play silence for params normally out of range.
- [PlaybackParams.AUDIO_FALLBACK_MODE_FAIL](../android/media/PlaybackParams.md): Return [java.lang.IllegalArgumentException](../java/lang/IllegalArgumentException.md) from`AudioTrack.setPlaybackParams(PlaybackParams)`.

**pitch:**increases or decreases the tonal frequency of the audio content. It is expressed as a multiplicative factor, where normal pitch is 1.0f.

**speed:**increases or decreases the time to play back a set of audio or video frames. It is expressed as a multiplicative factor, where normal speed is 1.0f.

Different combinations of speed and pitch may be used for audio playback; some common ones:

- *Pitch equals 1.0f.* Speed change will be done with pitch preserved, often called*timestretching*.
- *Pitch equals speed.* Speed change will be done by*resampling* , similar to [AudioTrack.setPlaybackRate(int)](../android/media/AudioTrack.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUDIO_FALLBACK_MODE_DEFAULT](../android/media/PlaybackParams.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUDIO_FALLBACK_MODE_FAIL](../android/media/PlaybackParams.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUDIO_FALLBACK_MODE_MUTE](../android/media/PlaybackParams.md) <br /> |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------|---|
| [PlaybackParams](../android/media/PlaybackParams.md))`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PlaybackParams](../android/media/PlaybackParams.md)! | [allowDefaults](../android/media/PlaybackParams.md))`()` Allows defaults to be returned for properties not set. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/media/PlaybackParams.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioFallbackMode](../android/media/PlaybackParams.md))`()` Retrieves the audio fallback mode. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPitch](../android/media/PlaybackParams.md))`()` Retrieves the pitch factor. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSpeed](../android/media/PlaybackParams.md))`()` Retrieves the speed factor. |
| [PlaybackParams](../android/media/PlaybackParams.md)! | [setAudioFallbackMode](../android/media/PlaybackParams.md))`(`audioFallbackMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the audio fallback mode. |
| --- | --- |
| [PlaybackParams](../android/media/PlaybackParams.md)! | [setPitch](../android/media/PlaybackParams.md))`(`pitch:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the pitch factor. |
| [PlaybackParams](../android/media/PlaybackParams.md)! | [setSpeed](../android/media/PlaybackParams.md))`(`speed:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the speed factor. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/media/PlaybackParams.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PlaybackParams](../android/media/PlaybackParams.md)!\> | [CREATOR](../android/media/PlaybackParams.md) <br /> |

## Constants

### AUDIO_FALLBACK_MODE_DEFAULT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUDIO_FALLBACK_MODE_DEFAULT: Int
```  

 Value: 0

### AUDIO_FALLBACK_MODE_FAIL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUDIO_FALLBACK_MODE_FAIL: Int
```  

 Value: 2

### AUDIO_FALLBACK_MODE_MUTE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUDIO_FALLBACK_MODE_MUTE: Int
```  

 Value: 1

## Public constructors

### PlaybackParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PlaybackParams()
```

## Public methods

### allowDefaults

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun allowDefaults(): PlaybackParams!
```

Allows defaults to be returned for properties not set. Otherwise a [java.lang.IllegalArgumentException](../java/lang/IllegalArgumentException.md) exception is raised when getting those properties which have defaults but have never been set.

| Return ||
|-------------------------------------------------------------------------------------------------|-------------------------------|
| [PlaybackParams](../android/media/PlaybackParams.md)! | this`PlaybackParams`instance. |

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getAudioFallbackMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioFallbackMode(): Int
```

Retrieves the audio fallback mode.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | audio fallback mode Value is [android.media.PlaybackParams#AUDIO_FALLBACK_MODE_DEFAULT](../android/media/PlaybackParams.md), [android.media.PlaybackParams#AUDIO_FALLBACK_MODE_MUTE](../android/media/PlaybackParams.md), or [android.media.PlaybackParams#AUDIO_FALLBACK_MODE_FAIL](../android/media/PlaybackParams.md) |

| Exceptions ||
|-----------------------------------|----------------------------------------|
| `java.lang.IllegalStateException` | if the audio fallback mode is not set. |

### getPitch

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPitch(): Float
```

Retrieves the pitch factor.

| Return ||
|--------------------------------------------------------------------------------|-------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | pitch |

| Exceptions ||
|-----------------------------------|----------------------|
| `java.lang.IllegalStateException` | if pitch is not set. |

### getSpeed

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSpeed(): Float
```

Retrieves the speed factor.

| Return ||
|--------------------------------------------------------------------------------|-------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | speed |

| Exceptions ||
|-----------------------------------|----------------------|
| `java.lang.IllegalStateException` | if speed is not set. |

### setAudioFallbackMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAudioFallbackMode(audioFallbackMode: Int): PlaybackParams!
```

Sets the audio fallback mode.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioFallbackMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.PlaybackParams#AUDIO_FALLBACK_MODE_DEFAULT](../android/media/PlaybackParams.md), [android.media.PlaybackParams#AUDIO_FALLBACK_MODE_MUTE](../android/media/PlaybackParams.md), or [android.media.PlaybackParams#AUDIO_FALLBACK_MODE_FAIL](../android/media/PlaybackParams.md) |

| Return ||
|-------------------------------------------------------------------------------------------------|-------------------------------|
| [PlaybackParams](../android/media/PlaybackParams.md)! | this`PlaybackParams`instance. |

### setPitch

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPitch(pitch: Float): PlaybackParams!
```

Sets the pitch factor.

| Parameters ||
|---------|---------------------------------------------------------------------------------|
| `pitch` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |

| Return ||
|-------------------------------------------------------------------------------------------------|-------------------------------|
| [PlaybackParams](../android/media/PlaybackParams.md)! | this`PlaybackParams`instance. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if the pitch is negative. |

### setSpeed

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSpeed(speed: Float): PlaybackParams!
```

Sets the speed factor.

| Parameters ||
|---------|---------------------------------------------------------------------------------|
| `speed` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |

| Return ||
|-------------------------------------------------------------------------------------------------|-------------------------------|
| [PlaybackParams](../android/media/PlaybackParams.md)! | this`PlaybackParams`instance. |

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PlaybackParams!>
```
