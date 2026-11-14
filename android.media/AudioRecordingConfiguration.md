# AudioRecordingConfiguration

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioRecordingConfiguration

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioRecordingConfiguration "View this page in Java") 

```
class AudioRecordingConfiguration : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.AudioRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#) |

The AudioRecordingConfiguration class collects the information describing an audio recording session.

Direct polling (see [AudioManager.getActiveRecordingConfigurations()](https://developer.android.com/reference/kotlin/android/media/AudioManager#getActiveRecordingConfigurations())) or callback (see [AudioManager.registerAudioRecordingCallback(android.media.AudioManager.AudioRecordingCallback, android.os.Handler)](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerAudioRecordingCallback(android.media.AudioManager.AudioRecordingCallback,%20android.os.Handler))methods are ways to receive information about the current recording configuration of the device.

An audio recording configuration contains information about the recording format as used by the application ([getClientFormat()](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getClientFormat()), as well as the recording format actually used by the device ([getFormat()](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getFormat())). The two recording formats may, for instance, be at different sampling rates due to hardware limitations (e.g. application recording at 44.1kHz whereas the device always records at 48kHz, and the Android framework resamples for the application).

The configuration also contains the use case for which audio is recorded ([getClientAudioSource()](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getClientAudioSource())), enabling the ability to distinguish between different activities such as ongoing voice recognition or camcorder recording.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)! | [getAudioDevice](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getAudioDevice())`()` Returns information about the audio input device used for this recording. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSource](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getAudioSource())`()` Returns the audio source currently used to configure the capture path. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getClientAudioSessionId](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getClientAudioSessionId())`()` Returns the session number of the recording, see [AudioRecord.getAudioSessionId()](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getAudioSessionId()). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getClientAudioSource](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getClientAudioSource())`()` Returns the audio source selected by the client. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor)!\> | [getClientEffects](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getClientEffects())`()` Returns the list of [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor) for all effects currently enabled on the audio capture client (e.g. |
| [AudioFormat](https://developer.android.com/reference/kotlin/android/media/AudioFormat)! | [getClientFormat](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getClientFormat())`()` Returns the audio format at which the client application is recording audio. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor)!\> | [getEffects](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getEffects())`()` Returns the list of [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor) for all effects currently enabled on the capture stream. |
| [AudioFormat](https://developer.android.com/reference/kotlin/android/media/AudioFormat)! | [getFormat](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getFormat())`()` Returns the audio format at which audio is recorded on this Android device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClientSilenced](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#isClientSilenced())`()` Returns true if the audio returned to the client is currently being silenced by the audio framework due to concurrent capture policy (e.g the capturing application does not have an active foreground process or service anymore). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AudioRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAudioDevice

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioDevice(): AudioDeviceInfo!
```

Returns information about the audio input device used for this recording.

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)! | the audio recording device or null if this information cannot be retrieved |

### getAudioSource

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioSource(): Int
```

Returns the audio source currently used to configure the capture path. It can be different from the source returned by [getClientAudioSource()](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getClientAudioSource())if another capture is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the audio source active on the capture path. Value is [android.media.MediaRecorder.AudioSource#DEFAULT](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#DEFAULT:kotlin.Int), [android.media.MediaRecorder.AudioSource#MIC](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#MIC:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_UPLINK](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_UPLINK:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_DOWNLINK](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_DOWNLINK:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_CALL](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_CALL:kotlin.Int), [android.media.MediaRecorder.AudioSource#CAMCORDER](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#CAMCORDER:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_RECOGNITION](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_RECOGNITION:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_COMMUNICATION](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_COMMUNICATION:kotlin.Int), [android.media.MediaRecorder.AudioSource#UNPROCESSED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#UNPROCESSED:kotlin.Int), or [android.media.MediaRecorder.AudioSource#VOICE_PERFORMANCE](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_PERFORMANCE:kotlin.Int) |

### getClientAudioSessionId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientAudioSessionId(): Int
```

Returns the session number of the recording, see [AudioRecord.getAudioSessionId()](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getAudioSessionId()).

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the session number. |

### getClientAudioSource

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientAudioSource(): Int
```

Returns the audio source selected by the client.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the audio source selected by the client. Value is [android.media.MediaRecorder.AudioSource#DEFAULT](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#DEFAULT:kotlin.Int), [android.media.MediaRecorder.AudioSource#MIC](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#MIC:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_UPLINK](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_UPLINK:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_DOWNLINK](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_DOWNLINK:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_CALL](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_CALL:kotlin.Int), [android.media.MediaRecorder.AudioSource#CAMCORDER](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#CAMCORDER:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_RECOGNITION](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_RECOGNITION:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_COMMUNICATION](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_COMMUNICATION:kotlin.Int), [android.media.MediaRecorder.AudioSource#UNPROCESSED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#UNPROCESSED:kotlin.Int), or [android.media.MediaRecorder.AudioSource#VOICE_PERFORMANCE](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_PERFORMANCE:kotlin.Int) |

### getClientEffects

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientEffects(): MutableList<AudioEffect.Descriptor!>
```

Returns the list of [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor) for all effects currently enabled on the audio capture client (e.g. [AudioRecord](https://developer.android.com/reference/kotlin/android/media/AudioRecord) or [MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder)).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor)!> | List of [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor) containing all effects enabled for the client. This value cannot be`null`. |

### getClientFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientFormat(): AudioFormat!
```

Returns the audio format at which the client application is recording audio. Note that it may differ from the actual recording format (see [getFormat()](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getFormat())).

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [AudioFormat](https://developer.android.com/reference/kotlin/android/media/AudioFormat)! | the recording format |

### getEffects

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEffects(): MutableList<AudioEffect.Descriptor!>
```

Returns the list of [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor) for all effects currently enabled on the capture stream.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor)!> | List of [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor) containing all effects enabled on the capture stream. This can be different from the list returned by [getClientEffects()](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getClientEffects())if another capture is active. This value cannot be`null`. |

### getFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormat(): AudioFormat!
```

Returns the audio format at which audio is recorded on this Android device. Note that it may differ from the client application recording format (see [getClientFormat()](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration#getClientFormat())).

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [AudioFormat](https://developer.android.com/reference/kotlin/android/media/AudioFormat)! | the device recording format |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isClientSilenced

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isClientSilenced(): Boolean
```

Returns true if the audio returned to the client is currently being silenced by the audio framework due to concurrent capture policy (e.g the capturing application does not have an active foreground process or service anymore).

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if captured audio is silenced, false otherwise . |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AudioRecordingConfiguration!>
```
