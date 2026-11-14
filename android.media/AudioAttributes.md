# AudioAttributes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioAttributes

Kotlin| [Java](../android/media/AudioAttributes.md) 
| --- | --- |

```
class AudioAttributes : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioAttributes](../android/media/AudioAttributes.md) |

A class to encapsulate a collection of attributes describing information about an audio stream.

`AudioAttributes`supersede the notion of stream types (see for instance [AudioManager.STREAM_MUSIC](../android/media/AudioManager.md) or [AudioManager.STREAM_ALARM](../android/media/AudioManager.md)) for defining the behavior of audio playback. Attributes allow an application to specify more information than is conveyed in a stream type by allowing the application to define:

- usage: "why" you are playing a sound, what is this sound used for. This is achieved with the "usage" information. Examples of usage are [USAGE_MEDIA](../android/media/AudioAttributes.md) and [USAGE_ALARM](../android/media/AudioAttributes.md). These two examples are the closest to stream types, but more detailed use cases are available. Usage information is more expressive than a stream type, and allows certain platforms or routing policies to use this information for more refined volume or routing decisions. Usage is the most important information to supply in`AudioAttributes`and it is recommended to build any instance with this information supplied, see [AudioAttributes.Builder](../android/media/AudioAttributes.Builder.md) for exceptions.
- content type: "what" you are playing. The content type expresses the general category of the content. This information is optional. But in case it is known (for instance [CONTENT_TYPE_MOVIE](../android/media/AudioAttributes.md) for a movie streaming service or [CONTENT_TYPE_MUSIC](../android/media/AudioAttributes.md) for a music playback application) this information might be used by the audio framework to selectively configure some audio post-processing blocks.
- flags: "how" is playback to be affected, see the flag definitions for the specific playback behaviors they control.

`AudioAttributes`are used for example in one of the [AudioTrack](../android/media/AudioTrack.md) constructors (see [AudioTrack.AudioTrack(AudioAttributes, AudioFormat, int, int, int)](../android/media/AudioTrack.md))), to configure a [MediaPlayer](../android/media/MediaPlayer.md)(see [MediaPlayer.setAudioAttributes(AudioAttributes)](../android/media/MediaPlayer.md))or a [android.app.Notification](../android/app/Notification.md)(see [android.app.Notification#audioAttributes](../android/app/Notification.md)). An`AudioAttributes`instance is built through its builder, [AudioAttributes.Builder](../android/media/AudioAttributes.Builder.md).

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/media/AudioAttributes.Builder.md) Builder class for [AudioAttributes](../android/media/AudioAttributes.md) objects. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALLOW_CAPTURE_BY_ALL](../android/media/AudioAttributes.md) Indicates that the audio may be captured by any app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALLOW_CAPTURE_BY_NONE](../android/media/AudioAttributes.md) Indicates that the audio is not to be recorded by any app, even if it is a system app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALLOW_CAPTURE_BY_SYSTEM](../android/media/AudioAttributes.md) Indicates that the audio may only be captured by system apps. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MOVIE](../android/media/AudioAttributes.md) Content type value to use when the content type is the audio typically accompanying a movie or TV program, containing a mix of dialogue, music and sound effects. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MUSIC](../android/media/AudioAttributes.md) Content type value to use when the content type is music. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_SONIFICATION](../android/media/AudioAttributes.md) Content type value to use when the content type is a sound used to accompany a user action, such as a beep or sound effect expressing a key click, or event, such as the type of a sound for a bonus being received in a game. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_SPEECH](../android/media/AudioAttributes.md) Content type value to use when the content type is speech. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_UNKNOWN](../android/media/AudioAttributes.md) Content type value to use when the content type is unknown, or other than the ones defined. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_AUDIBILITY_ENFORCED](../android/media/AudioAttributes.md) Flag defining a behavior where the audibility of the sound will be ensured by the system. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_HW_AV_SYNC](../android/media/AudioAttributes.md) Flag requesting the use of an output stream supporting hardware A/V synchronization. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_LOW_LATENCY](../android/media/AudioAttributes.md) Flag requesting a low latency path when creating an AudioTrack. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPATIALIZATION_BEHAVIOR_AUTO](../android/media/AudioAttributes.md) Constant indicating the audio content associated with these attributes will follow the default platform behavior with regards to which content will be spatialized or not. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPATIALIZATION_BEHAVIOR_NEVER](../android/media/AudioAttributes.md) Constant indicating the audio content associated with these attributes should never be virtualized. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_ALARM](../android/media/AudioAttributes.md) Usage value to use when the usage is an alarm (e.g. wake-up alarm). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_ASSISTANCE_ACCESSIBILITY](../android/media/AudioAttributes.md) Usage value to use when the usage is for accessibility, such as with a screen reader. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_ASSISTANCE_NAVIGATION_GUIDANCE](../android/media/AudioAttributes.md) Usage value to use when the usage is driving or navigation directions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_ASSISTANCE_SONIFICATION](../android/media/AudioAttributes.md) Usage value to use when the usage is sonification, such as with user interface sounds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_ASSISTANT](../android/media/AudioAttributes.md) Usage value to use for audio responses to user queries, audio instructions or help utterances. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_GAME](../android/media/AudioAttributes.md) Usage value to use when the usage is for game audio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_MEDIA](../android/media/AudioAttributes.md) Usage value to use when the usage is media, such as music, or movie soundtracks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_NOTIFICATION](../android/media/AudioAttributes.md) Usage value to use when the usage is notification. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_NOTIFICATION_COMMUNICATION_DELAYED](../android/media/AudioAttributes.md) Usage value to use when the usage is notification for a non-immediate type of communication such as e-mail. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_NOTIFICATION_COMMUNICATION_INSTANT](../android/media/AudioAttributes.md) Usage value to use when the usage is notification for an "instant" communication such as a chat, or SMS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_NOTIFICATION_COMMUNICATION_REQUEST](../android/media/AudioAttributes.md) Usage value to use when the usage is a request to enter/end a communication, such as a VoIP communication or video-conference. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_NOTIFICATION_EVENT](../android/media/AudioAttributes.md) Usage value to use when the usage is to attract the user's attention, such as a reminder or low battery warning. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_NOTIFICATION_RINGTONE](../android/media/AudioAttributes.md) Usage value to use when the usage is telephony ringtone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_UNKNOWN](../android/media/AudioAttributes.md) Usage value to use when the usage is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_VOICE_COMMUNICATION](../android/media/AudioAttributes.md) Usage value to use when the usage is voice communications, such as telephony or VoIP. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USAGE_VOICE_COMMUNICATION_SIGNALLING](../android/media/AudioAttributes.md) Usage value to use when the usage is in-call signalling, such as with a "busy" beep, or DTMF tones. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areHapticChannelsMuted](../android/media/AudioAttributes.md))`()` Return if haptic channels are muted. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/media/AudioAttributes.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/media/AudioAttributes.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAllowedCapturePolicy](../android/media/AudioAttributes.md))`()` Return the capture policy. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getContentType](../android/media/AudioAttributes.md))`()` Return the content type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFlags](../android/media/AudioAttributes.md))`()` Return the flags. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpatializationBehavior](../android/media/AudioAttributes.md))`()` Return the behavior affecting whether spatialization will be used. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUsage](../android/media/AudioAttributes.md))`()` Return the usage. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolumeControlStream](../android/media/AudioAttributes.md))`()` Returns the stream type matching this`AudioAttributes`instance for volume control. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/media/AudioAttributes.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isContentSpatialized](../android/media/AudioAttributes.md))`()` Return true if the audio content associated with these attributes has already been spatialized, that is it has already been processed to offer a binaural or transaural immersive audio experience. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/media/AudioAttributes.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/media/AudioAttributes.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AudioAttributes](../android/media/AudioAttributes.md)!\> | [CREATOR](../android/media/AudioAttributes.md) <br /> |

## Constants

### ALLOW_CAPTURE_BY_ALL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALLOW_CAPTURE_BY_ALL: Int
```

Indicates that the audio may be captured by any app. For privacy, the following usages cannot be recorded: VOICE_COMMUNICATION\*, USAGE_NOTIFICATION\*, USAGE_ASSISTANCE\* and USAGE_ASSISTANT. On [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md), this means only [USAGE_UNKNOWN](../android/media/AudioAttributes.md), [USAGE_MEDIA](../android/media/AudioAttributes.md) and [USAGE_GAME](../android/media/AudioAttributes.md) may be captured. See [android.media.projection.MediaProjection](../android/media/projection/MediaProjection.md) and [Builder.setAllowedCapturePolicy](../android/media/AudioAttributes.Builder.md)). 

 Value: 1

### ALLOW_CAPTURE_BY_NONE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALLOW_CAPTURE_BY_NONE: Int
```

Indicates that the audio is not to be recorded by any app, even if it is a system app. It is encouraged to use [ALLOW_CAPTURE_BY_SYSTEM](../android/media/AudioAttributes.md) instead of this value as system apps provide significant and useful features for the user (such as live captioning and accessibility). See [Builder.setAllowedCapturePolicy](../android/media/AudioAttributes.Builder.md)). 

 Value: 3

### ALLOW_CAPTURE_BY_SYSTEM

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALLOW_CAPTURE_BY_SYSTEM: Int
```

Indicates that the audio may only be captured by system apps. System apps can capture for many purposes like accessibility, live captions, user guidance... but abide to the following restrictions: - the audio cannot leave the device - the audio cannot be passed to a third party app - the audio cannot be recorded at a higher quality than 16kHz 16bit mono See [Builder.setAllowedCapturePolicy](../android/media/AudioAttributes.Builder.md)). 

 Value: 2

### CONTENT_TYPE_MOVIE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_MOVIE: Int
```

Content type value to use when the content type is the audio typically accompanying a movie or TV program, containing a mix of dialogue, music and sound effects. 

 Value: 3

### CONTENT_TYPE_MUSIC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_MUSIC: Int
```

Content type value to use when the content type is music. 

 Value: 2

### CONTENT_TYPE_SONIFICATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_SONIFICATION: Int
```

Content type value to use when the content type is a sound used to accompany a user action, such as a beep or sound effect expressing a key click, or event, such as the type of a sound for a bonus being received in a game. These sounds are mostly synthesized or short Foley sounds. 

 Value: 4

### CONTENT_TYPE_SPEECH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_SPEECH: Int
```

Content type value to use when the content type is speech. 

 Value: 1

### CONTENT_TYPE_UNKNOWN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_UNKNOWN: Int
```

Content type value to use when the content type is unknown, or other than the ones defined. 

 Value: 0

### FLAG_AUDIBILITY_ENFORCED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_AUDIBILITY_ENFORCED: Int
```

Flag defining a behavior where the audibility of the sound will be ensured by the system. To ensure sound audibility, the system only uses built-in speakers or wired headphones and specifically excludes wireless audio devices.

Note this flag should only be used for sounds subject to regulatory behaviors in some countries, such as for camera shutter sound, and not for routing behaviors. 

 Value: 1

### FLAG_HW_AV_SYNC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_HW_AV_SYNC: Int
```

Flag requesting the use of an output stream supporting hardware A/V synchronization. 

 Value: 16

### FLAG_LOW_LATENCY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_LOW_LATENCY: Int
```

**Deprecated:** *Use [AudioTrack.Builder.setPerformanceMode(int)](../android/media/AudioTrack.Builder.md))with [AudioTrack.PERFORMANCE_MODE_LOW_LATENCY](../android/media/AudioTrack.md) to control performance.*

Flag requesting a low latency path when creating an AudioTrack. When using this flag, the sample rate must match the native sample rate of the device. Effects processing is also unavailable. Note that if this flag is used without specifying a bufferSizeInBytes then the AudioTrack's actual buffer size may be too small. It is recommended that a fairly large buffer should be specified when the AudioTrack is created. Then the actual size can be reduced by calling [AudioTrack.setBufferSizeInFrames(int)](../android/media/AudioTrack.md)). The buffer size can be optimized by lowering it after each write() call until the audio glitches, which is detected by calling [AudioTrack.getUnderrunCount()](../android/media/AudioTrack.md)). Then the buffer size can be increased until there are no glitches. This tuning step should be done while playing silence. This technique provides a compromise between latency and glitch rate. 

 Value: 256

### SPATIALIZATION_BEHAVIOR_AUTO

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPATIALIZATION_BEHAVIOR_AUTO: Int
```

Constant indicating the audio content associated with these attributes will follow the default platform behavior with regards to which content will be spatialized or not. 

 Value: 0

**See Also**

- <https://developer.android.com/reference/kotlin/android/media/AudioAttributes#getSpatializationBehavior()>
- [android.media.Spatializer](../android/media/Spatializer.md) 

### SPATIALIZATION_BEHAVIOR_NEVER

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPATIALIZATION_BEHAVIOR_NEVER: Int
```

Constant indicating the audio content associated with these attributes should never be virtualized. 

 Value: 1

**See Also**

- <https://developer.android.com/reference/kotlin/android/media/AudioAttributes#getSpatializationBehavior()>
- [android.media.Spatializer](../android/media/Spatializer.md) 

### USAGE_ALARM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_ALARM: Int
```

Usage value to use when the usage is an alarm (e.g. wake-up alarm). 

 Value: 4

### USAGE_ASSISTANCE_ACCESSIBILITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_ASSISTANCE_ACCESSIBILITY: Int
```

Usage value to use when the usage is for accessibility, such as with a screen reader. 

 Value: 11

### USAGE_ASSISTANCE_NAVIGATION_GUIDANCE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_ASSISTANCE_NAVIGATION_GUIDANCE: Int
```

Usage value to use when the usage is driving or navigation directions. 

 Value: 12

### USAGE_ASSISTANCE_SONIFICATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_ASSISTANCE_SONIFICATION: Int
```

Usage value to use when the usage is sonification, such as with user interface sounds. 

 Value: 13

### USAGE_ASSISTANT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_ASSISTANT: Int
```

Usage value to use for audio responses to user queries, audio instructions or help utterances. 

 Value: 16

### USAGE_GAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_GAME: Int
```

Usage value to use when the usage is for game audio. 

 Value: 14

### USAGE_MEDIA

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_MEDIA: Int
```

Usage value to use when the usage is media, such as music, or movie soundtracks. 

 Value: 1

### USAGE_NOTIFICATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_NOTIFICATION: Int
```

Usage value to use when the usage is notification. See other notification usages for more specialized uses. 

 Value: 5

### USAGE_NOTIFICATION_COMMUNICATION_DELAYED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_NOTIFICATION_COMMUNICATION_DELAYED: Int
```

**Deprecated:** *Use [USAGE_NOTIFICATION](../android/media/AudioAttributes.md) which is handled the same way as this usage by the audio framework*

Usage value to use when the usage is notification for a non-immediate type of communication such as e-mail. 

 Value: 9

### USAGE_NOTIFICATION_COMMUNICATION_INSTANT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_NOTIFICATION_COMMUNICATION_INSTANT: Int
```

**Deprecated:** *Use [USAGE_NOTIFICATION](../android/media/AudioAttributes.md) which is handled the same way as this usage by the audio framework*

Usage value to use when the usage is notification for an "instant" communication such as a chat, or SMS. 

 Value: 8

### USAGE_NOTIFICATION_COMMUNICATION_REQUEST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_NOTIFICATION_COMMUNICATION_REQUEST: Int
```

**Deprecated:** *Use [USAGE_NOTIFICATION](../android/media/AudioAttributes.md) which is handled the same way as this usage by the audio framework*

Usage value to use when the usage is a request to enter/end a communication, such as a VoIP communication or video-conference. 

 Value: 7

### USAGE_NOTIFICATION_EVENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_NOTIFICATION_EVENT: Int
```

Usage value to use when the usage is to attract the user's attention, such as a reminder or low battery warning. 

 Value: 10

### USAGE_NOTIFICATION_RINGTONE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_NOTIFICATION_RINGTONE: Int
```

Usage value to use when the usage is telephony ringtone. 

 Value: 6

### USAGE_UNKNOWN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_UNKNOWN: Int
```

Usage value to use when the usage is unknown. 

 Value: 0

### USAGE_VOICE_COMMUNICATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_VOICE_COMMUNICATION: Int
```

Usage value to use when the usage is voice communications, such as telephony or VoIP. 

 Value: 2

### USAGE_VOICE_COMMUNICATION_SIGNALLING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_VOICE_COMMUNICATION_SIGNALLING: Int
```

Usage value to use when the usage is in-call signalling, such as with a "busy" beep, or DTMF tones. 

 Value: 3

## Public methods

### areHapticChannelsMuted

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun areHapticChannelsMuted(): Boolean
```

Return if haptic channels are muted.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if haptic channels are muted,`false`otherwise. |

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAllowedCapturePolicy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAllowedCapturePolicy(): Int
```

Return the capture policy.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the capture policy set by [Builder.setAllowedCapturePolicy(int)](../android/media/AudioAttributes.Builder.md))or the default if it was not called. Value is [android.media.AudioAttributes#ALLOW_CAPTURE_BY_ALL](../android/media/AudioAttributes.md), [android.media.AudioAttributes#ALLOW_CAPTURE_BY_SYSTEM](../android/media/AudioAttributes.md), or [android.media.AudioAttributes#ALLOW_CAPTURE_BY_NONE](../android/media/AudioAttributes.md) |

### getContentType

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentType(): Int
```

Return the content type.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | one of the values that can be set in [Builder.setContentType(int)](../android/media/AudioAttributes.Builder.md)) |

### getFlags

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Int
```

Return the flags.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a combined mask of all flags |

### getSpatializationBehavior

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSpatializationBehavior(): Int
```

Return the behavior affecting whether spatialization will be used.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the spatialization behavior Value is [android.media.AudioAttributes#SPATIALIZATION_BEHAVIOR_AUTO](../android/media/AudioAttributes.md), or [android.media.AudioAttributes#SPATIALIZATION_BEHAVIOR_NEVER](../android/media/AudioAttributes.md) |

### getUsage

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUsage(): Int
```

Return the usage.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | one of the values that can be set in [Builder.setUsage(int)](../android/media/AudioAttributes.Builder.md)) |

### getVolumeControlStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolumeControlStream(): Int
```

Returns the stream type matching this`AudioAttributes`instance for volume control. Use this method to derive the stream type needed to configure the volume control slider in an [android.app.Activity](../android/app/Activity.md) with [android.app.Activity#setVolumeControlStream(int)](../android/app/Activity.md))for playback conducted with these attributes. 
Do not use this method to set the stream type on an audio player object (e.g. [AudioTrack](../android/media/AudioTrack.md), [MediaPlayer](../android/media/MediaPlayer.md)) as this is deprecated, use`AudioAttributes`instead.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a valid stream type for`Activity`or stream volume control that matches the attributes, or [AudioManager.USE_DEFAULT_STREAM_TYPE](../android/media/AudioManager.md) if there isn't a direct match. Note that`USE_DEFAULT_STREAM_TYPE`is not a valid value for [AudioManager.setStreamVolume(int, int, int)](../android/media/AudioManager.md)). |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isContentSpatialized

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isContentSpatialized(): Boolean
```

Return true if the audio content associated with these attributes has already been spatialized, that is it has already been processed to offer a binaural or transaural immersive audio experience.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the content has been processed |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AudioAttributes!>
```
