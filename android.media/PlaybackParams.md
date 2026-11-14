# PlaybackParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PlaybackParams

Kotlin| [Java](https://developer.android.com/reference/android/media/PlaybackParams "View this page in Java") 

```
class PlaybackParams : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.PlaybackParams](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#) |

Structure for common playback params. Used by [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack) [AudioTrack.getPlaybackParams()](https://developer.android.com/reference/kotlin/android/media/AudioTrack#getPlaybackParams())and [AudioTrack.setPlaybackParams(PlaybackParams)](https://developer.android.com/reference/kotlin/android/media/AudioTrack#setPlaybackParams(android.media.PlaybackParams))to control playback behavior.

**audio fallback mode:**select out-of-range parameter handling.

- [PlaybackParams.AUDIO_FALLBACK_MODE_DEFAULT](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#AUDIO_FALLBACK_MODE_DEFAULT:kotlin.Int): System will determine best handling.
- [PlaybackParams.AUDIO_FALLBACK_MODE_MUTE](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#AUDIO_FALLBACK_MODE_MUTE:kotlin.Int): Play silence for params normally out of range.
- [PlaybackParams.AUDIO_FALLBACK_MODE_FAIL](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#AUDIO_FALLBACK_MODE_FAIL:kotlin.Int): Return [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) from`AudioTrack.setPlaybackParams(PlaybackParams)`.

**pitch:**increases or decreases the tonal frequency of the audio content. It is expressed as a multiplicative factor, where normal pitch is 1.0f.

**speed:**increases or decreases the time to play back a set of audio or video frames. It is expressed as a multiplicative factor, where normal speed is 1.0f.

Different combinations of speed and pitch may be used for audio playback; some common ones:

- *Pitch equals 1.0f.* Speed change will be done with pitch preserved, often called*timestretching*.
- *Pitch equals speed.* Speed change will be done by*resampling* , similar to [AudioTrack.setPlaybackRate(int)](https://developer.android.com/reference/kotlin/android/media/AudioTrack#setPlaybackRate(kotlin.Int)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUDIO_FALLBACK_MODE_DEFAULT](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#AUDIO_FALLBACK_MODE_DEFAULT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUDIO_FALLBACK_MODE_FAIL](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#AUDIO_FALLBACK_MODE_FAIL:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUDIO_FALLBACK_MODE_MUTE](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#AUDIO_FALLBACK_MODE_MUTE:kotlin.Int) <br /> |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------|---|
| [PlaybackParams](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#PlaybackParams())`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PlaybackParams](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#)! | [allowDefaults](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#allowDefaults())`()` Allows defaults to be returned for properties not set. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioFallbackMode](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#getAudioFallbackMode())`()` Retrieves the audio fallback mode. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPitch](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#getPitch())`()` Retrieves the pitch factor. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSpeed](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#getSpeed())`()` Retrieves the speed factor. |
| [PlaybackParams](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#)! | [setAudioFallbackMode](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#setAudioFallbackMode(kotlin.Int))`(`audioFallbackMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the audio fallback mode. |
| [PlaybackParams](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#)! | [setPitch](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#setPitch(kotlin.Float))`(`pitch:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the pitch factor. |
| [PlaybackParams](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#)! | [setSpeed](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#setSpeed(kotlin.Float))`(`speed:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the speed factor. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PlaybackParams](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#CREATOR:android.os.Parcelable.Creator) <br /> |

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

Allows defaults to be returned for properties not set. Otherwise a [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) exception is raised when getting those properties which have defaults but have never been set.

| Return ||
|-------------------------------------------------------------------------------------------------|-------------------------------|
| [PlaybackParams](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#)! | this`PlaybackParams`instance. |

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAudioFallbackMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioFallbackMode(): Int
```

Retrieves the audio fallback mode.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | audio fallback mode Value is [android.media.PlaybackParams#AUDIO_FALLBACK_MODE_DEFAULT](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#AUDIO_FALLBACK_MODE_DEFAULT:kotlin.Int), [android.media.PlaybackParams#AUDIO_FALLBACK_MODE_MUTE](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#AUDIO_FALLBACK_MODE_MUTE:kotlin.Int), or [android.media.PlaybackParams#AUDIO_FALLBACK_MODE_FAIL](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#AUDIO_FALLBACK_MODE_FAIL:kotlin.Int) |

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
| `audioFallbackMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.PlaybackParams#AUDIO_FALLBACK_MODE_DEFAULT](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#AUDIO_FALLBACK_MODE_DEFAULT:kotlin.Int), [android.media.PlaybackParams#AUDIO_FALLBACK_MODE_MUTE](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#AUDIO_FALLBACK_MODE_MUTE:kotlin.Int), or [android.media.PlaybackParams#AUDIO_FALLBACK_MODE_FAIL](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#AUDIO_FALLBACK_MODE_FAIL:kotlin.Int) |

| Return ||
|-------------------------------------------------------------------------------------------------|-------------------------------|
| [PlaybackParams](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#)! | this`PlaybackParams`instance. |

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
| [PlaybackParams](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#)! | this`PlaybackParams`instance. |

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
| [PlaybackParams](https://developer.android.com/reference/kotlin/android/media/PlaybackParams#)! | this`PlaybackParams`instance. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PlaybackParams!>
```
