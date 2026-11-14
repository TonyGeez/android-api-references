# SyncParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncParams

Kotlin| [Java](../android/media/SyncParams.md) 
| --- | --- |

```
class SyncParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.SyncParams](../android/media/SyncParams.md) |

Structure for common A/V sync params. Used by [MediaSync](../android/media/MediaSync.md){link MediaSync#getSyncParams()} and {link MediaSync#setSyncParams(SyncParams)} to control A/V sync behavior.

**audio adjust mode:**select handling of audio track when changing playback speed due to sync.

- [SyncParams.AUDIO_ADJUST_MODE_DEFAULT](../android/media/SyncParams.md): System will determine best handling.
- [SyncParams.AUDIO_ADJUST_MODE_STRETCH](../android/media/SyncParams.md): Change the speed of audio playback without altering its pitch.
- [SyncParams.AUDIO_ADJUST_MODE_RESAMPLE](../android/media/SyncParams.md): Change the speed of audio playback by resampling the audio.

**sync source:**select clock source for sync.

- [SyncParams.SYNC_SOURCE_DEFAULT](../android/media/SyncParams.md): System will determine best selection.
- [SyncParams.SYNC_SOURCE_SYSTEM_CLOCK](../android/media/SyncParams.md): Use system clock for sync source.
- [SyncParams.SYNC_SOURCE_AUDIO](../android/media/SyncParams.md): Use audio track for sync source.
- [SyncParams.SYNC_SOURCE_VSYNC](../android/media/SyncParams.md): Syncronize media to vsync.

**tolerance:**specifies the amount of allowed playback rate change to keep media in sync with the sync source. The handling of this depends on the sync source, but must not be negative, and must be less than one.

**frameRate:**initial hint for video frame rate. Used when sync source is vsync. Negative values can be used to clear a previous hint.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUDIO_ADJUST_MODE_DEFAULT](../android/media/SyncParams.md) System will determine best handling of audio for playback rate adjustments. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUDIO_ADJUST_MODE_RESAMPLE](../android/media/SyncParams.md) Resample audio when playback rate must be adjusted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUDIO_ADJUST_MODE_STRETCH](../android/media/SyncParams.md) Time stretch audio when playback rate must be adjusted. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_SOURCE_AUDIO](../android/media/SyncParams.md) Use audio track for sync source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_SOURCE_DEFAULT](../android/media/SyncParams.md) Use the default sync source (default). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_SOURCE_SYSTEM_CLOCK](../android/media/SyncParams.md) Use system monotonic clock for sync source. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_SOURCE_VSYNC](../android/media/SyncParams.md) Use vsync as the sync source. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------|---|
| [SyncParams](../android/media/SyncParams.md))`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SyncParams](../android/media/SyncParams.md)! | [allowDefaults](../android/media/SyncParams.md))`()` Allows defaults to be returned for properties not set. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioAdjustMode](../android/media/SyncParams.md))`()` Retrieves the audio adjust mode. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFrameRate](../android/media/SyncParams.md))`()` Retrieves the video frame rate hint. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSyncSource](../android/media/SyncParams.md))`()` Retrieves the sync source. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getTolerance](../android/media/SyncParams.md))`()` Retrieves the tolerance factor. |
| [SyncParams](../android/media/SyncParams.md)! | [setAudioAdjustMode](../android/media/SyncParams.md))`(`audioAdjustMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the audio adjust mode. |
| --- | --- |
| [SyncParams](../android/media/SyncParams.md)! | [setFrameRate](../android/media/SyncParams.md))`(`frameRate:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the video frame rate hint to be used. |
| [SyncParams](../android/media/SyncParams.md)! | [setSyncSource](../android/media/SyncParams.md))`(`syncSource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the sync source. |
| [SyncParams](../android/media/SyncParams.md)! | [setTolerance](../android/media/SyncParams.md))`(`tolerance:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the tolerance. |
| --- | --- |

## Constants

### AUDIO_ADJUST_MODE_DEFAULT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUDIO_ADJUST_MODE_DEFAULT: Int
```

System will determine best handling of audio for playback rate adjustments.

Used by default. This will make audio play faster or slower as required by the sync source without changing its pitch; however, system may fall back to some other method (e.g. change the pitch, or mute the audio) if time stretching is no longer supported for the playback rate. 

 Value: 0

### AUDIO_ADJUST_MODE_RESAMPLE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUDIO_ADJUST_MODE_RESAMPLE: Int
```

Resample audio when playback rate must be adjusted.

This will make audio play faster or slower as required by the sync source by changing its pitch (making it lower to play slower, and higher to play faster.) 

 Value: 2

### AUDIO_ADJUST_MODE_STRETCH

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUDIO_ADJUST_MODE_STRETCH: Int
```

Time stretch audio when playback rate must be adjusted.

This will make audio play faster or slower as required by the sync source without changing its pitch, as long as it is supported for the playback rate. 

 Value: 1

### SYNC_SOURCE_AUDIO

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_SOURCE_AUDIO: Int
```

Use audio track for sync source. This requires audio data and an audio track. 

 Value: 2

**See Also**

- [android.media.AudioTrack#getTimestamp(android.media.AudioTimestamp)](../android/media/AudioTrack.md)) 

### SYNC_SOURCE_DEFAULT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_SOURCE_DEFAULT: Int
```

Use the default sync source (default). If media has video, the sync renders to a surface that directly renders to a display, and tolerance is non zero (e.g. not less than 0.001) vsync source is used for clock source. Otherwise, if media has audio, audio track is used. Finally, if media has no audio, system clock is used. 

 Value: 0

### SYNC_SOURCE_SYSTEM_CLOCK

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_SOURCE_SYSTEM_CLOCK: Int
```

Use system monotonic clock for sync source. 

 Value: 1

**See Also**

- [java.lang.System#nanoTime](../java/lang/System.md)) 

### SYNC_SOURCE_VSYNC

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_SOURCE_VSYNC: Int
```

Use vsync as the sync source. This requires video data and an output surface that directly renders to the display, e.g. [android.view.SurfaceView](../android/view/SurfaceView.md)

This mode allows smoother playback experience by adjusting the playback speed to match the vsync rate, e.g. playing 30fps content on a 59.94Hz display. When using this mode, the tolerance should be set to greater than 0 (e.g. at least 1/1000), so that the playback speed can actually be adjusted.

This mode can also be used to play 25fps content on a 60Hz display using a 2:3 pulldown (basically playing the content at 24fps), which results on better playback experience on most devices. In this case the tolerance should be at least (1/24). 

 Value: 3

**See Also**

- [android.view.Choreographer.FrameCallback#doFrame](../android/view/Choreographer.FrameCallback.md))
- [android.view.Display#getAppVsyncOffsetNanos](../android/view/Display.md))

## Public constructors

### SyncParams

```
SyncParams()
```

## Public methods

### allowDefaults

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun allowDefaults(): SyncParams!
```

Allows defaults to be returned for properties not set. Otherwise a [java.lang.IllegalArgumentException](../java/lang/IllegalArgumentException.md) exception is raised when getting those properties which have defaults but have never been set.

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------|
| [SyncParams](../android/media/SyncParams.md)! | this`SyncParams`instance. |

### getAudioAdjustMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioAdjustMode(): Int
```

Retrieves the audio adjust mode.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | audio adjust mode Value is [android.media.SyncParams#AUDIO_ADJUST_MODE_DEFAULT](../android/media/SyncParams.md), [android.media.SyncParams#AUDIO_ADJUST_MODE_STRETCH](../android/media/SyncParams.md), or [android.media.SyncParams#AUDIO_ADJUST_MODE_RESAMPLE](../android/media/SyncParams.md) |

| Exceptions ||
|-----------------------------------|--------------------------------------|
| `java.lang.IllegalStateException` | if the audio adjust mode is not set. |

### getFrameRate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrameRate(): Float
```

Retrieves the video frame rate hint.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | frame rate factor. A non-negative number representing the maximum deviation of the playback rate from the playback rate set. (`abs(actual_rate - set_rate) / set_rate`), or a negative number representing the desire to clear a previous hint using these params. |

| Exceptions ||
|-----------------------------------|---------------------------|
| `java.lang.IllegalStateException` | if frame rate is not set. |

### getSyncSource

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSyncSource(): Int
```

Retrieves the sync source.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | sync source Value is [android.media.SyncParams#SYNC_SOURCE_DEFAULT](../android/media/SyncParams.md), [android.media.SyncParams#SYNC_SOURCE_SYSTEM_CLOCK](../android/media/SyncParams.md), [android.media.SyncParams#SYNC_SOURCE_AUDIO](../android/media/SyncParams.md), or [android.media.SyncParams#SYNC_SOURCE_VSYNC](../android/media/SyncParams.md) |

| Exceptions ||
|-----------------------------------|--------------------------------|
| `java.lang.IllegalStateException` | if the sync source is not set. |

### getTolerance

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTolerance(): Float
```

Retrieves the tolerance factor.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | tolerance factor. A non-negative number representing the maximum deviation of the playback rate from the playback rate set. (`abs(actual_rate - set_rate) / set_rate`) |

| Exceptions ||
|-----------------------------------|--------------------------|
| `java.lang.IllegalStateException` | if tolerance is not set. |

### setAudioAdjustMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAudioAdjustMode(audioAdjustMode: Int): SyncParams!
```

Sets the audio adjust mode.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioAdjustMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.SyncParams#AUDIO_ADJUST_MODE_DEFAULT](../android/media/SyncParams.md), [android.media.SyncParams#AUDIO_ADJUST_MODE_STRETCH](../android/media/SyncParams.md), or [android.media.SyncParams#AUDIO_ADJUST_MODE_RESAMPLE](../android/media/SyncParams.md) |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------|
| [SyncParams](../android/media/SyncParams.md)! | this`SyncParams`instance. |

### setFrameRate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFrameRate(frameRate: Float): SyncParams!
```

Sets the video frame rate hint to be used. By default the frame rate is unspecified.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameRate` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A non-negative number used as an initial hint on the video frame rate to be used when using vsync as the sync source. A negative number is used to clear a previous hint. |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------|
| [SyncParams](../android/media/SyncParams.md)! | this`SyncParams`instance. |

### setSyncSource

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSyncSource(syncSource: Int): SyncParams!
```

Sets the sync source.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `syncSource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.SyncParams#SYNC_SOURCE_DEFAULT](../android/media/SyncParams.md), [android.media.SyncParams#SYNC_SOURCE_SYSTEM_CLOCK](../android/media/SyncParams.md), [android.media.SyncParams#SYNC_SOURCE_AUDIO](../android/media/SyncParams.md), or [android.media.SyncParams#SYNC_SOURCE_VSYNC](../android/media/SyncParams.md) |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------|
| [SyncParams](../android/media/SyncParams.md)! | this`SyncParams`instance. |

### setTolerance

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTolerance(tolerance: Float): SyncParams!
```

Sets the tolerance. The default tolerance is platform specific, but is never more than 1/24.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tolerance` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A non-negative number representing the maximum deviation of the playback rate from the playback rate set. (`abs(actual_rate - set_rate) / set_rate`) |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------|
| [SyncParams](../android/media/SyncParams.md)! | this`SyncParams`instance. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the tolerance is negative, or not less than one. |
