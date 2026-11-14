# MicrophoneDirection

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MicrophoneDirection

Kotlin| [Java](MicrophoneDirection.md) 
| --- | --- |

```
interface MicrophoneDirection
```

| [android.media.MicrophoneDirection](MicrophoneDirection.md) |

| Known Direct Subclasses [AudioRecord](AudioRecord.md), [MediaRecorder](MediaRecorder.md) |---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------| | [AudioRecord](AudioRecord.md) | The AudioRecord class manages the audio resources for Java applications to record audio from the audio input hardware of the platform. | | [MediaRecorder](MediaRecorder.md) | Used to record audio and video. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface defining mechanism for controlling the directionality and field width of audio capture.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_AWAY_FROM_USER](MicrophoneDirection.md) Optimize capture for audio coming from the side of the device pointing away from the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_EXTERNAL](MicrophoneDirection.md) Optimize capture for audio coming from an off-device microphone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_TOWARDS_USER](MicrophoneDirection.md) Optimize capture for audio coming from the side of the device facing the user. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_UNSPECIFIED](MicrophoneDirection.md) Don't do any directionality processing of the activated microphone(s). |

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredMicrophoneDirection](MicrophoneDirection.md))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specifies the logical microphone (for processing). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredMicrophoneFieldDimension](MicrophoneDirection.md))`(`zoom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Specifies the zoom factor (i.e. the field dimension) for the selected microphone (for processing). |

## Constants

### MIC_DIRECTION_AWAY_FROM_USER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIC_DIRECTION_AWAY_FROM_USER: Int
```

Optimize capture for audio coming from the side of the device pointing away from the user. In the typical case, a device with a single screen, screen-side camera/microphone and non-screen-side camera/microphone, this will be the non-screen side. For a different device geometry, it is the side for which the expectation is to be facing away from the user. This is the "taking a video of something else" case. 

 Value: 2

### MIC_DIRECTION_EXTERNAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIC_DIRECTION_EXTERNAL: Int
```

Optimize capture for audio coming from an off-device microphone. 

 Value: 3

### MIC_DIRECTION_TOWARDS_USER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIC_DIRECTION_TOWARDS_USER: Int
```

Optimize capture for audio coming from the side of the device facing the user. In the typical case, a device with a single screen, screen-side camera/microphone and non-screen-side camera/microphone, this will be the screen side (as in a "selfie"). For a different device geometry, it is the side for which the expectation is to be facing the user. 

 Value: 1

### MIC_DIRECTION_UNSPECIFIED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIC_DIRECTION_UNSPECIFIED: Int
```

Don't do any directionality processing of the activated microphone(s). 

 Value: 0

## Public methods

### setPreferredMicrophoneDirection

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPreferredMicrophoneDirection(direction: Int): Boolean
```

Specifies the logical microphone (for processing). Applications can use this to specify which side of the device to optimize capture from. Typically used in conjunction with the camera capturing video. Usage would include specifying the audio capture to follow camera being used to capture video.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Direction constant. Value is [android.media.MicrophoneDirection#MIC_DIRECTION_UNSPECIFIED](MicrophoneDirection.md), [android.media.MicrophoneDirection#MIC_DIRECTION_TOWARDS_USER](MicrophoneDirection.md), [android.media.MicrophoneDirection#MIC_DIRECTION_AWAY_FROM_USER](MicrophoneDirection.md), or [android.media.MicrophoneDirection#MIC_DIRECTION_EXTERNAL](MicrophoneDirection.md) |

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if sucessful. |

### setPreferredMicrophoneFieldDimension

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPreferredMicrophoneFieldDimension(zoom: Float): Boolean
```

Specifies the zoom factor (i.e. the field dimension) for the selected microphone (for processing). The selected microphone is determined by the use-case for the stream. Usage would include specifying the audio focus to follow the zoom specified for the camera being used to capture video.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `zoom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the desired field dimension of microphone capture. Range is from -1 (wide angle), though 0 (no zoom) to 1 (maximum zoom). Value is between -1.0f and 1.0f inclusive |

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if sucessful. |
