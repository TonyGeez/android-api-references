# MediaActionSound

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaActionSound

Kotlin| [Java](MediaActionSound.md) 
| --- | --- |

```
open class MediaActionSound
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaActionSound](MediaActionSound.md) |

A class for producing sounds that match those produced by various actions taken by the media and camera APIs. It is recommended to call methods in this class in a background thread since it relies on binder calls.

This class is recommended for use with the [android.hardware.camera2](../android.hardware.camera2/_package.md) API, since the camera2 API does not play any sounds on its own for any capture or video recording actions.

With the older [android.hardware.Camera](../android.hardware/Camera.md) API, use this class to play an appropriate camera operation sound when implementing a custom still or video recording mechanism (through the Camera preview callbacks with [Camera.setPreviewCallback](../android.hardware/Camera.md)), or through GPU processing with [Camera.setPreviewTexture](../android.hardware/Camera.md)), for example), or when implementing some other camera-like function in your application.

There is no need to play sounds when using android.hardware.Camera#takePicture or [android.media.MediaRecorder](MediaRecorder.md) for still images or video, respectively, as the Android framework will play the appropriate sounds when needed for these calls.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FOCUS_COMPLETE](MediaActionSound.md) A sound to indicate that focusing has completed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHUTTER_CLICK](MediaActionSound.md) The sound used by android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [START_VIDEO_RECORDING](MediaActionSound.md) The sound used by [MediaRecorder.start()](MediaRecorder.md))to indicate the start of video recording. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_VIDEO_RECORDING](MediaActionSound.md) The sound used by [MediaRecorder.stop()](MediaRecorder.md))to indicate the end of video recording. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaActionSound](MediaActionSound.md))`()` Construct a new MediaActionSound instance. |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [load](MediaActionSound.md))`(`soundName:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Preload a predefined platform sound to minimize latency when the sound is played later by [play](MediaActionSound.md)). |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [mustPlayShutterSound](MediaActionSound.md))`()` Returns true if the application must play the shutter sound in accordance to certain regional restrictions. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [play](MediaActionSound.md))`(`soundName:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Play one of the predefined platform sounds for media actions. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](MediaActionSound.md))`()` Free up all audio resources used by this MediaActionSound instance. |

## Constants

### FOCUS_COMPLETE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FOCUS_COMPLETE: Int
```

A sound to indicate that focusing has completed. Because deciding when this occurs is application-dependent, this sound is not used by any methods in the media or camera APIs. 

 Value: 1

**See Also**

- [#play](MediaActionSound.md)) 

### SHUTTER_CLICK

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHUTTER_CLICK: Int
```

The sound used by android.hardware.Camera#takePicture to indicate still image capture. 

 Value: 0

**See Also**

- [#play](MediaActionSound.md)) 

### START_VIDEO_RECORDING

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val START_VIDEO_RECORDING: Int
```

The sound used by [MediaRecorder.start()](MediaRecorder.md))to indicate the start of video recording. 

 Value: 2

**See Also**

- [#play](MediaActionSound.md)) 

### STOP_VIDEO_RECORDING

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_VIDEO_RECORDING: Int
```

The sound used by [MediaRecorder.stop()](MediaRecorder.md))to indicate the end of video recording. 

 Value: 3

**See Also**

- [#play](MediaActionSound.md))

## Public constructors

### MediaActionSound

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaActionSound()
```

Construct a new MediaActionSound instance. Only a single instance is needed for playing any platform media action sound; you do not need a separate instance for each sound type.

## Public methods

### load

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun load(soundName: Int): Unit
```

Preload a predefined platform sound to minimize latency when the sound is played later by [play](MediaActionSound.md)).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `soundName` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of sound to preload, selected from SHUTTER_CLICK, FOCUS_COMPLETE, START_VIDEO_RECORDING, or STOP_VIDEO_RECORDING. |

**See Also**

- [#play](MediaActionSound.md))
- [#SHUTTER_CLICK](MediaActionSound.md)
- [#FOCUS_COMPLETE](MediaActionSound.md)
- [#START_VIDEO_RECORDING](MediaActionSound.md)
- [#STOP_VIDEO_RECORDING](MediaActionSound.md) 

### mustPlayShutterSound

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun mustPlayShutterSound(): Boolean
```

Returns true if the application must play the shutter sound in accordance to certain regional restrictions.

If this method returns true, applications are strongly recommended to use MediaActionSound.play(SHUTTER_CLICK) or START_VIDEO_RECORDING whenever it captures images or video to storage or sends them over the network. 

### play

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun play(soundName: Int): Unit
```

Play one of the predefined platform sounds for media actions.

Use this method to play a platform-specific sound for various media actions. The sound playback is done asynchronously, with the same behavior and content as the sounds played by android.hardware.Camera#takePicture, [MediaRecorder.start](MediaRecorder.md)), and [MediaRecorder.stop](MediaRecorder.md)).

With the [camera2](../android.hardware.camera2/_package.md) API, this method can be used to play standard camera operation sounds with the appropriate system behavior for such sounds.

With the older [android.hardware.Camera](../android.hardware/Camera.md) API, using this method makes it easy to match the default device sounds when recording or capturing data through the preview callbacks, or when implementing custom camera-like features in your application.

If the sound has not been loaded by [load](MediaActionSound.md))before calling play, play will load the sound at the cost of some additional latency before sound playback begins.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `soundName` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of sound to play, selected from SHUTTER_CLICK, FOCUS_COMPLETE, START_VIDEO_RECORDING, or STOP_VIDEO_RECORDING. |

**See Also**

- [android.media.MediaRecorder](MediaRecorder.md)
- [#SHUTTER_CLICK](MediaActionSound.md)
- [#FOCUS_COMPLETE](MediaActionSound.md)
- [#START_VIDEO_RECORDING](MediaActionSound.md)
- [#STOP_VIDEO_RECORDING](MediaActionSound.md) 

### release

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Free up all audio resources used by this MediaActionSound instance. Do not call any other methods on a MediaActionSound instance after calling release().
