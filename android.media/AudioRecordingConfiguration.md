# AudioRecordingConfiguration

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioRecordingConfiguration

Kotlin| [Java](../android/media/AudioRecordingConfiguration.md) 
| --- | --- |

```
class AudioRecordingConfiguration : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioRecordingConfiguration](../android/media/AudioRecordingConfiguration.md) |

The AudioRecordingConfiguration class collects the information describing an audio recording session.

Direct polling (see [AudioManager.getActiveRecordingConfigurations()](../android/media/AudioManager.md))) or callback (see [AudioManager.registerAudioRecordingCallback(android.media.AudioManager.AudioRecordingCallback, android.os.Handler)](../android/media/AudioManager.md))methods are ways to receive information about the current recording configuration of the device.

An audio recording configuration contains information about the recording format as used by the application ([getClientFormat()](../android/media/AudioRecordingConfiguration.md)), as well as the recording format actually used by the device ([getFormat()](../android/media/AudioRecordingConfiguration.md))). The two recording formats may, for instance, be at different sampling rates due to hardware limitations (e.g. application recording at 44.1kHz whereas the device always records at 48kHz, and the Android framework resamples for the application).

The configuration also contains the use case for which audio is recorded ([getClientAudioSource()](../android/media/AudioRecordingConfiguration.md))), enabling the ability to distinguish between different activities such as ongoing voice recognition or camcorder recording.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/media/AudioRecordingConfiguration.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/media/AudioRecordingConfiguration.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)! | [getAudioDevice](../android/media/AudioRecordingConfiguration.md))`()` Returns information about the audio input device used for this recording. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSource](../android/media/AudioRecordingConfiguration.md))`()` Returns the audio source currently used to configure the capture path. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getClientAudioSessionId](../android/media/AudioRecordingConfiguration.md))`()` Returns the session number of the recording, see [AudioRecord.getAudioSessionId()](../android/media/AudioRecord.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getClientAudioSource](../android/media/AudioRecordingConfiguration.md))`()` Returns the audio source selected by the client. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)!\> | [getClientEffects](../android/media/AudioRecordingConfiguration.md))`()` Returns the list of [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) for all effects currently enabled on the audio capture client (e.g. |
| [AudioFormat](../android/media/AudioFormat.md)! | [getClientFormat](../android/media/AudioRecordingConfiguration.md))`()` Returns the audio format at which the client application is recording audio. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)!\> | [getEffects](../android/media/AudioRecordingConfiguration.md))`()` Returns the list of [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) for all effects currently enabled on the capture stream. |
| --- | --- |
| [AudioFormat](../android/media/AudioFormat.md)! | [getFormat](../android/media/AudioRecordingConfiguration.md))`()` Returns the audio format at which audio is recorded on this Android device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/media/AudioRecordingConfiguration.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClientSilenced](../android/media/AudioRecordingConfiguration.md))`()` Returns true if the audio returned to the client is currently being silenced by the audio framework due to concurrent capture policy (e.g the capturing application does not have an active foreground process or service anymore). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/media/AudioRecordingConfiguration.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AudioRecordingConfiguration](../android/media/AudioRecordingConfiguration.md)!\> | [CREATOR](../android/media/AudioRecordingConfiguration.md) <br /> |

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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
| [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)! | the audio recording device or null if this information cannot be retrieved |

### getAudioSource

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioSource(): Int
```

Returns the audio source currently used to configure the capture path. It can be different from the source returned by [getClientAudioSource()](../android/media/AudioRecordingConfiguration.md))if another capture is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the audio source active on the capture path. Value is [android.media.MediaRecorder.AudioSource#DEFAULT](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#MIC](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#VOICE_UPLINK](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#VOICE_DOWNLINK](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#VOICE_CALL](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#CAMCORDER](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#VOICE_RECOGNITION](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#VOICE_COMMUNICATION](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#UNPROCESSED](../android/media/MediaRecorder.AudioSource.md), or [android.media.MediaRecorder.AudioSource#VOICE_PERFORMANCE](../android/media/MediaRecorder.AudioSource.md) |

### getClientAudioSessionId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientAudioSessionId(): Int
```

Returns the session number of the recording, see [AudioRecord.getAudioSessionId()](../android/media/AudioRecord.md)).

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the audio source selected by the client. Value is [android.media.MediaRecorder.AudioSource#DEFAULT](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#MIC](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#VOICE_UPLINK](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#VOICE_DOWNLINK](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#VOICE_CALL](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#CAMCORDER](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#VOICE_RECOGNITION](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#VOICE_COMMUNICATION](../android/media/MediaRecorder.AudioSource.md), [android.media.MediaRecorder.AudioSource#UNPROCESSED](../android/media/MediaRecorder.AudioSource.md), or [android.media.MediaRecorder.AudioSource#VOICE_PERFORMANCE](../android/media/MediaRecorder.AudioSource.md) |

### getClientEffects

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientEffects(): MutableList<AudioEffect.Descriptor!>
```

Returns the list of [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) for all effects currently enabled on the audio capture client (e.g. [AudioRecord](../android/media/AudioRecord.md) or [MediaRecorder](../android/media/MediaRecorder.md)).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)!> | List of [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) containing all effects enabled for the client. This value cannot be`null`. |

### getClientFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientFormat(): AudioFormat!
```

Returns the audio format at which the client application is recording audio. Note that it may differ from the actual recording format (see [getFormat()](../android/media/AudioRecordingConfiguration.md))).

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [AudioFormat](../android/media/AudioFormat.md)! | the recording format |

### getEffects

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEffects(): MutableList<AudioEffect.Descriptor!>
```

Returns the list of [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) for all effects currently enabled on the capture stream.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)!> | List of [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) containing all effects enabled on the capture stream. This can be different from the list returned by [getClientEffects()](../android/media/AudioRecordingConfiguration.md))if another capture is active. This value cannot be`null`. |

### getFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormat(): AudioFormat!
```

Returns the audio format at which audio is recorded on this Android device. Note that it may differ from the client application recording format (see [getClientFormat()](../android/media/AudioRecordingConfiguration.md))).

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [AudioFormat](../android/media/AudioFormat.md)! | the device recording format |

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
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AudioRecordingConfiguration!>
```
