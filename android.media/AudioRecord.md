# AudioRecord

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioRecord

Kotlin| [Java](AudioRecord.md) 
| --- | --- |

```
open class AudioRecord : AudioRecordingMonitor, AudioRouting, MicrophoneDirection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioRecord](AudioRecord.md) |

The AudioRecord class manages the audio resources for Java applications to record audio from the audio input hardware of the platform. This is achieved by "pulling" (reading) the data from the AudioRecord object. The application is responsible for polling the AudioRecord object in time using one of the following three methods:[read(byte[],int,int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)),[read(short[],int,int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#read(kotlin.ShortArray,%20kotlin.Int,%20kotlin.Int))or [read(java.nio.ByteBuffer,int)](AudioRecord.md)). The choice of which method to use will be based on the audio data storage format that is the most convenient for the user of AudioRecord.

Upon creation, an AudioRecord object initializes its associated audio buffer that it will fill with the new audio data. The size of this buffer, specified during the construction, determines how long an AudioRecord can record before "over-running" data that has not been read yet. Data should be read from the audio hardware in chunks of sizes inferior to the total recording buffer size.

Applications creating an AudioRecord instance need [android.Manifest.permission#RECORD_AUDIO](../android/Manifest.permission.md) or the Builder will throw [java.lang.UnsupportedOperationException](../java.lang/UnsupportedOperationException.md) on [build()](../android/media/AudioRecord.Builder.md)), and the constructor will return an instance in state [STATE_UNINITIALIZED](AudioRecord.md).

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](../android/media/AudioRecord.Builder.md) Builder class for [AudioRecord](AudioRecord.md) objects. |
| | [MetricsConstants](../android/media/AudioRecord.MetricsConstants.md) <br /> |
| abstract | [OnRecordPositionUpdateListener](../android/media/AudioRecord.OnRecordPositionUpdateListener.md) Interface definition for a callback to be invoked when an AudioRecord has reached a notification marker set by [AudioRecord.setNotificationMarkerPosition(int)](AudioRecord.md))or for periodic updates on the progress of the record head, as set by [AudioRecord.setPositionNotificationPeriod(int)](AudioRecord.md)). |
| --- | --- |
| abstract | [OnRoutingChangedListener](../android/media/AudioRecord.OnRoutingChangedListener.md) Defines the interface by which applications can receive notifications of routing changes for the associated [AudioRecord](AudioRecord.md). |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](AudioRecord.md) Denotes a generic operation failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](AudioRecord.md) Denotes a failure due to the use of an invalid value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEAD_OBJECT](AudioRecord.md) An error code indicating that the object reporting it is no longer valid and needs to be recreated. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_OPERATION](AudioRecord.md) Denotes a failure due to the improper use of a method. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [READ_BLOCKING](AudioRecord.md) The read mode indicating the read operation will block until all data requested has been read. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [READ_NON_BLOCKING](AudioRecord.md) The read mode indicating the read operation will return immediately after reading as much audio data as possible without blocking. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDSTATE_RECORDING](AudioRecord.md) indicates AudioRecord recording state is recording |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDSTATE_STOPPED](AudioRecord.md) indicates AudioRecord recording state is not recording |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_INITIALIZED](AudioRecord.md) indicates AudioRecord state is ready to be used |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNINITIALIZED](AudioRecord.md) indicates AudioRecord state is not successfully initialized. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](AudioRecord.md) Denotes a successful operation. |

| Inherited constants ||
|---|---|
| From class [MicrophoneDirection](MicrophoneDirection.md) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_AWAY_FROM_USER](MicrophoneDirection.md) <br /> Optimize capture for audio coming from the side of the device pointing away from the user. In the typical case, a device with a single screen, screen-side camera/microphone and non-screen-side camera/microphone, this will be the non-screen side. For a different device geometry, it is the side for which the expectation is to be facing away from the user. This is the "taking a video of something else" case. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_EXTERNAL](MicrophoneDirection.md) <br /> Optimize capture for audio coming from an off-device microphone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_TOWARDS_USER](MicrophoneDirection.md) <br /> Optimize capture for audio coming from the side of the device facing the user. In the typical case, a device with a single screen, screen-side camera/microphone and non-screen-side camera/microphone, this will be the screen side (as in a "selfie"). For a different device geometry, it is the side for which the expectation is to be facing the user. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_UNSPECIFIED](MicrophoneDirection.md) <br /> Don't do any directionality processing of the activated microphone(s). <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AudioRecord](AudioRecord.md))`(`audioSource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sampleRateInHz:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `channelConfig:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bufferSizeInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Class constructor. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnRoutingChangedListener](AudioRecord.md))`(`listener:` ` [AudioRecord.OnRoutingChangedListener](../android/media/AudioRecord.OnRoutingChangedListener.md)!`, `handler:` ` [Handler](../android.os/Handler.md)!`)` Adds an [OnRoutingChangedListener](../android/media/AudioRecord.OnRoutingChangedListener.md) to receive notifications of routing changes on this AudioRecord. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnRoutingChangedListener](AudioRecord.md))`(`listener:` ` [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!`, `handler:` ` [Handler](../android.os/Handler.md)!`)` Adds an [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) to receive notifications of routing changes on this AudioRecord. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MicrophoneInfo](MicrophoneInfo.md)!\>! | [getActiveMicrophones](AudioRecord.md))`()` Returns a lists of [MicrophoneInfo](MicrophoneInfo.md) representing the active microphones. |
| --- | --- |
| open [AudioRecordingConfiguration](AudioRecordingConfiguration.md)? | [getActiveRecordingConfiguration](AudioRecord.md))`()` Returns the current active audio recording for this audio recorder. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioFormat](AudioRecord.md))`()` Returns the configured audio data encoding. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSessionId](AudioRecord.md))`()` Returns the audio session ID. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSource](AudioRecord.md))`()` Returns the audio recording source. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBufferSizeInFrames](AudioRecord.md))`()` Returns the frame count of the native`AudioRecord`buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChannelConfiguration](AudioRecord.md))`()` Returns the configured channel position mask. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChannelCount](AudioRecord.md))`()` Returns the configured number of channels. |
| open [AudioFormat](AudioFormat.md) | [getFormat](AudioRecord.md))`()` Returns the configured`AudioRecord`format. |
| open [LogSessionId](../android.media.metrics/LogSessionId.md) | [getLogSessionId](AudioRecord.md))`()` Returns the [LogSessionId](../android.media.metrics/LogSessionId.md). |
| --- | --- |
| open [PersistableBundle](../android.os/PersistableBundle.md)! | [getMetrics](AudioRecord.md))`()` Return Metrics data about the current AudioTrack instance. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinBufferSize](AudioRecord.md))`(`sampleRateInHz:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `channelConfig:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the minimum buffer size required for the successful creation of an AudioRecord object, in byte units. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNotificationMarkerPosition](AudioRecord.md))`()` Returns the notification marker position expressed in frames. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPositionNotificationPeriod](AudioRecord.md))`()` Returns the notification update period expressed in frames. |
| open [AudioDeviceInfo](AudioDeviceInfo.md)! | [getPreferredDevice](AudioRecord.md))`()` Returns the selected input specified by [setPreferredDevice](AudioRecord.md)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRecordingState](AudioRecord.md))`()` Returns the recording state of the AudioRecord instance. |
| --- | --- |
| open [AudioDeviceInfo](AudioDeviceInfo.md)! | [getRoutedDevice](AudioRecord.md))`()` Returns an [AudioDeviceInfo](AudioDeviceInfo.md) identifying the current routing of this AudioRecord. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioDeviceInfo](AudioDeviceInfo.md)!\> | [getRoutedDevices](AudioRecord.md))`()` Returns a List of [AudioDeviceInfo](AudioDeviceInfo.md) identifying the current routing of this AudioRecord. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSampleRate](AudioRecord.md))`()` Returns the configured audio sink sample rate in Hz. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](AudioRecord.md))`()` Returns the state of the AudioRecord instance. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimestamp](AudioRecord.md))`(`outTimestamp:` ` [AudioTimestamp](AudioTimestamp.md)`, `timebase:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Poll for an [AudioTimestamp](AudioTimestamp.md) on demand. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrivacySensitive](AudioRecord.md))`()` Returns whether this AudioRecord is marked as privacy sensitive or not. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](AudioRecord.md))`(`audioData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offsetInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sizeInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a byte array. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](AudioRecord.md))`(`audioData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offsetInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sizeInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a byte array. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](AudioRecord.md))`(`audioData:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `offsetInFloats:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sizeInFloats:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a float array. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](AudioRecord.md))`(`audioBuffer:` ` [ByteBuffer](../java.nio/ByteBuffer.md)`, `sizeInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a direct buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](AudioRecord.md))`(`audioBuffer:` ` [ByteBuffer](../java.nio/ByteBuffer.md)`, `sizeInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a direct buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](AudioRecord.md))`(`audioData:` ` [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)`, `offsetInShorts:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sizeInShorts:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a short array. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](AudioRecord.md))`(`audioData:` ` [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)`, `offsetInShorts:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sizeInShorts:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a short array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAudioRecordingCallback](AudioRecord.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `cb:` ` [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md)`)` Register a callback to be notified of audio capture changes via a [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](AudioRecord.md))`()` Releases the native AudioRecord resources. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnRoutingChangedListener](AudioRecord.md))`(`listener:` ` [AudioRecord.OnRoutingChangedListener](../android/media/AudioRecord.OnRoutingChangedListener.md)!`)` Removes an [OnRoutingChangedListener](../android/media/AudioRecord.OnRoutingChangedListener.md) which has been previously added to receive rerouting notifications. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnRoutingChangedListener](AudioRecord.md))`(`listener:` ` [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!`)` Removes an [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) which has been previously added to receive rerouting notifications. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLogSessionId](AudioRecord.md))`(`logSessionId:` ` [LogSessionId](../android.media.metrics/LogSessionId.md)`)` Sets a [LogSessionId](../android.media.metrics/LogSessionId.md) instance to this AudioRecord for metrics collection. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setNotificationMarkerPosition](AudioRecord.md))`(`markerInFrames:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the marker position at which the listener is called, if set with [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener)](AudioRecord.md))or [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,android.os.Handler)](AudioRecord.md)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setPositionNotificationPeriod](AudioRecord.md))`(`periodInFrames:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the period at which the listener is called, if set with [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener)](AudioRecord.md))or [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,android.os.Handler)](AudioRecord.md)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredDevice](AudioRecord.md))`(`deviceInfo:` ` [AudioDeviceInfo](AudioDeviceInfo.md)!`)` Specifies an audio device (via an [AudioDeviceInfo](AudioDeviceInfo.md) object) to route the input to this AudioRecord. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredMicrophoneDirection](AudioRecord.md))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specifies the logical microphone (for processing). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredMicrophoneFieldDimension](AudioRecord.md))`(`zoom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Specifies the zoom factor (i.e. the field dimension) for the selected microphone (for processing). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRecordPositionUpdateListener](AudioRecord.md))`(`listener:` ` [AudioRecord.OnRecordPositionUpdateListener](../android/media/AudioRecord.OnRecordPositionUpdateListener.md)!`)` Sets the listener the AudioRecord notifies when a previously set marker is reached or for each periodic record head position update. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRecordPositionUpdateListener](AudioRecord.md))`(`listener:` ` [AudioRecord.OnRecordPositionUpdateListener](../android/media/AudioRecord.OnRecordPositionUpdateListener.md)!`, `handler:` ` [Handler](../android.os/Handler.md)!`)` Sets the listener the AudioRecord notifies when a previously set marker is reached or for each periodic record head position update. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startRecording](AudioRecord.md))`()` Starts recording from the AudioRecord instance. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startRecording](AudioRecord.md))`(`syncEvent:` ` [MediaSyncEvent](MediaSyncEvent.md)!`)` Starts recording from the AudioRecord instance when the specified synchronization event occurs on the specified audio session. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](AudioRecord.md))`()` Stops recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAudioRecordingCallback](AudioRecord.md))`(`cb:` ` [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md)`)` Unregister an audio recording callback previously registered with [registerAudioRecordingCallback(java.util.concurrent.Executor,android.media.AudioManager.AudioRecordingCallback)](AudioRecord.md)). |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](AudioRecord.md))`()` <br /> |

## Constants

### ERROR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR: Int
```

Denotes a generic operation failure. 

 Value: -1

### ERROR_BAD_VALUE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_BAD_VALUE: Int
```

Denotes a failure due to the use of an invalid value. 

 Value: -2

### ERROR_DEAD_OBJECT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DEAD_OBJECT: Int
```

An error code indicating that the object reporting it is no longer valid and needs to be recreated. 

 Value: -6

### ERROR_INVALID_OPERATION

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_OPERATION: Int
```

Denotes a failure due to the improper use of a method. 

 Value: -3

### READ_BLOCKING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val READ_BLOCKING: Int
```

The read mode indicating the read operation will block until all data requested has been read. 

 Value: 0

### READ_NON_BLOCKING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val READ_NON_BLOCKING: Int
```

The read mode indicating the read operation will return immediately after reading as much audio data as possible without blocking. 

 Value: 1

### RECORDSTATE_RECORDING

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORDSTATE_RECORDING: Int
```

indicates AudioRecord recording state is recording 

 Value: 3

### RECORDSTATE_STOPPED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORDSTATE_STOPPED: Int
```

indicates AudioRecord recording state is not recording 

 Value: 1

### STATE_INITIALIZED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_INITIALIZED: Int
```

indicates AudioRecord state is ready to be used 

 Value: 1

### STATE_UNINITIALIZED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_UNINITIALIZED: Int
```

indicates AudioRecord state is not successfully initialized. 

 Value: 0

### SUCCESS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUCCESS: Int
```

Denotes a successful operation. 

 Value: 0

## Public constructors

### AudioRecord

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AudioRecord(
    audioSource: Int, 
    sampleRateInHz: Int, 
    channelConfig: Int, 
    audioFormat: Int, 
    bufferSizeInBytes: Int)
```

Class constructor. Though some invalid parameters will result in an [IllegalArgumentException](../java.lang/IllegalArgumentException.md) exception, other errors do not. Thus you should call [getState()](AudioRecord.md))immediately after construction to confirm that the object is usable. 
Requires [android.Manifest.permission#RECORD_AUDIO](../android/Manifest.permission.md)

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioSource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the recording source. See [MediaRecorder.AudioSource](../android/media/MediaRecorder.AudioSource.md) for the recording source definitions. |
| `sampleRateInHz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the sample rate expressed in Hertz. 44100Hz is currently the only rate that is guaranteed to work on all devices, but other rates such as 22050, 16000, and 11025 may work on some devices. [AudioFormat.SAMPLE_RATE_UNSPECIFIED](AudioFormat.md) means to use a route-dependent value which is usually the sample rate of the source. [getSampleRate()](AudioRecord.md))can be used to retrieve the actual sample rate chosen. |
| `channelConfig` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):describes the configuration of the audio channels. See [AudioFormat.CHANNEL_IN_MONO](AudioFormat.md) and [AudioFormat.CHANNEL_IN_STEREO](AudioFormat.md). [AudioFormat.CHANNEL_IN_MONO](AudioFormat.md) is guaranteed to work on all devices. |
| --- | --- |
| `audioFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the format in which the audio data is to be returned. See [AudioFormat.ENCODING_PCM_8BIT](AudioFormat.md), [AudioFormat.ENCODING_PCM_16BIT](AudioFormat.md), and [AudioFormat.ENCODING_PCM_FLOAT](AudioFormat.md). |
| `bufferSizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the total size (in bytes) of the buffer where audio data is written to during the recording. New audio data can be read from this buffer in smaller chunks than this size. See [getMinBufferSize(int,int,int)](AudioRecord.md))to determine the minimum required buffer size for the successful creation of an AudioRecord instance. Using values smaller than getMinBufferSize() will result in an initialization failure. |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalArgumentException` | |

## Public methods

### addOnRoutingChangedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addOnRoutingChangedListener(
    listener: AudioRecord.OnRoutingChangedListener!, 
    handler: Handler!
): Unit
```

**Deprecated:** *users should switch to the general purpose [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) class instead.*

Adds an [OnRoutingChangedListener](../android/media/AudioRecord.OnRoutingChangedListener.md) to receive notifications of routing changes on this AudioRecord.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRecord.OnRoutingChangedListener](../android/media/AudioRecord.OnRoutingChangedListener.md)!:The [OnRoutingChangedListener](../android/media/AudioRecord.OnRoutingChangedListener.md) interface to receive notifications of rerouting events. |
| `handler` | [Handler](../android.os/Handler.md)!:Specifies the [Handler](../android.os/Handler.md) object for the thread on which to execute the callback. If`null`, the [Handler](../android.os/Handler.md) associated with the main [Looper](../android.os/Looper.md) will be used. |

### addOnRoutingChangedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addOnRoutingChangedListener(
    listener: AudioRouting.OnRoutingChangedListener!, 
    handler: Handler!
): Unit
```

Adds an [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) to receive notifications of routing changes on this AudioRecord.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!:The [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) interface to receive notifications of rerouting events. |
| `handler` | [Handler](../android.os/Handler.md)!:Specifies the [Handler](../android.os/Handler.md) object for the thread on which to execute the callback. If`null`, the [Handler](../android.os/Handler.md) associated with the main [Looper](../android.os/Looper.md) will be used. |

### getActiveMicrophones

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActiveMicrophones(): MutableList<MicrophoneInfo!>!
```

Returns a lists of [MicrophoneInfo](MicrophoneInfo.md) representing the active microphones. By querying channel mapping for each active microphone, developer can know how the microphone is used by each channels or a capture stream. Note that the information about the active microphones may change during a recording. See [AudioManager.registerAudioDeviceCallback](AudioManager.md))to be notified of changes in the audio devices, querying the active microphones then will return the latest information.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MicrophoneInfo](MicrophoneInfo.md)!>! | a lists of [MicrophoneInfo](MicrophoneInfo.md) representing the active microphones. |

| Exceptions ||
|-----------------------|--------------------|
| `java.io.IOException` | if an error occurs |

### getActiveRecordingConfiguration

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActiveRecordingConfiguration(): AudioRecordingConfiguration?
```

Returns the current active audio recording for this audio recorder.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AudioRecordingConfiguration](AudioRecordingConfiguration.md)? | a valid [AudioRecordingConfiguration](AudioRecordingConfiguration.md) if this recorder is active or null otherwise. |

**See Also**

- [android.media.AudioRecordingConfiguration](AudioRecordingConfiguration.md) 

### getAudioFormat

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAudioFormat(): Int
```

Returns the configured audio data encoding. See [AudioFormat.ENCODING_PCM_8BIT](AudioFormat.md), [AudioFormat.ENCODING_PCM_16BIT](AudioFormat.md), and [AudioFormat.ENCODING_PCM_FLOAT](AudioFormat.md). 

### getAudioSessionId

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAudioSessionId(): Int
```

Returns the audio session ID.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the ID of the audio session this AudioRecord belongs to. |

### getAudioSource

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAudioSource(): Int
```

Returns the audio recording source. 
**See Also**

- [android.media.MediaRecorder.AudioSource](../android/media/MediaRecorder.AudioSource.md) 

### getBufferSizeInFrames

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBufferSizeInFrames(): Int
```

Returns the frame count of the native`AudioRecord`buffer. This is greater than or equal to the bufferSizeInBytes converted to frame units specified in the`AudioRecord`constructor or Builder. The native frame count may be enlarged to accommodate the requirements of the source on creation or if the`AudioRecord`is subsequently rerouted.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | current size in frames of the`AudioRecord`buffer. |

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

### getChannelConfiguration

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChannelConfiguration(): Int
```

Returns the configured channel position mask.

See [AudioFormat.CHANNEL_IN_MONO](AudioFormat.md) and [AudioFormat.CHANNEL_IN_STEREO](AudioFormat.md). This method may return [AudioFormat.CHANNEL_INVALID](AudioFormat.md) if a channel index mask is used. Consider [getFormat()](AudioRecord.md))instead, to obtain an [AudioFormat](AudioFormat.md), which contains both the channel position mask and the channel index mask. 

### getChannelCount

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChannelCount(): Int
```

Returns the configured number of channels. 

### getFormat

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFormat(): AudioFormat
```

Returns the configured`AudioRecord`format.

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AudioFormat](AudioFormat.md) | an [AudioFormat](AudioFormat.md) containing the`AudioRecord`parameters at the time of configuration. This value cannot be`null`. |

### getLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLogSessionId(): LogSessionId
```

Returns the [LogSessionId](../android.media.metrics/LogSessionId.md).

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------|
| [LogSessionId](../android.media.metrics/LogSessionId.md) | This value cannot be`null`. |

### getMetrics

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMetrics(): PersistableBundle!
```

Return Metrics data about the current AudioTrack instance.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PersistableBundle](../android.os/PersistableBundle.md)! | a [PersistableBundle](../android.os/PersistableBundle.md) containing the set of attributes and values available for the media being handled by this instance of AudioRecord The attributes are descibed in [MetricsConstants](../android/media/AudioRecord.MetricsConstants.md). Additional vendor-specific fields may also be present in the return value. |

### getMinBufferSize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMinBufferSize(
    sampleRateInHz: Int, 
    channelConfig: Int, 
    audioFormat: Int
): Int
```

Returns the minimum buffer size required for the successful creation of an AudioRecord object, in byte units. Note that this size doesn't guarantee a smooth recording under load, and higher values should be chosen according to the expected frequency at which the AudioRecord instance will be polled for new data. See [AudioRecord(int,int,int,int,int)](AudioRecord.md))for more information on valid configuration values.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sampleRateInHz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the sample rate expressed in Hertz. [AudioFormat.SAMPLE_RATE_UNSPECIFIED](AudioFormat.md) is not permitted. |
| `channelConfig` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):describes the configuration of the audio channels. See [AudioFormat.CHANNEL_IN_MONO](AudioFormat.md) and [AudioFormat.CHANNEL_IN_STEREO](AudioFormat.md) |
| `audioFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the format in which the audio data is represented. See [AudioFormat.ENCODING_PCM_16BIT](AudioFormat.md). |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](AudioRecord.md) if the recording parameters are not supported by the hardware, or an invalid parameter was passed, or [ERROR](AudioRecord.md) if the implementation was unable to query the hardware for its input properties, or the minimum buffer size expressed in bytes. |

**See Also**

- [#AudioRecord(int, int, int, int, int)](AudioRecord.md)) 

### getNotificationMarkerPosition

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNotificationMarkerPosition(): Int
```

Returns the notification marker position expressed in frames. 

### getPositionNotificationPeriod

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPositionNotificationPeriod(): Int
```

Returns the notification update period expressed in frames. 

### getPreferredDevice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreferredDevice(): AudioDeviceInfo!
```

Returns the selected input specified by [setPreferredDevice](AudioRecord.md)). Note that this is not guarenteed to correspond to the actual device being used for recording. 

### getRecordingState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRecordingState(): Int
```

Returns the recording state of the AudioRecord instance. 
**See Also**

- [android.media.AudioRecord#RECORDSTATE_STOPPED](AudioRecord.md)
- [android.media.AudioRecord#RECORDSTATE_RECORDING](AudioRecord.md) 

### getRoutedDevice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoutedDevice(): AudioDeviceInfo!
```

Returns an [AudioDeviceInfo](AudioDeviceInfo.md) identifying the current routing of this AudioRecord. Note: The query is only valid if the AudioRecord is currently recording. If it is not,`getRoutedDevice()`will return null. 

### getRoutedDevices

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoutedDevices(): MutableList<AudioDeviceInfo!>
```

Returns a List of [AudioDeviceInfo](AudioDeviceInfo.md) identifying the current routing of this AudioRecord. Note: The query is only valid if the AudioRecord is currently playing. If it is not,`getRoutedDevices()`will return an empty list.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AudioDeviceInfo](AudioDeviceInfo.md)!> | This value cannot be`null`. |

### getSampleRate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSampleRate(): Int
```

Returns the configured audio sink sample rate in Hz. The sink sample rate never changes after construction. If the constructor had a specific sample rate, then the sink sample rate is that value. If the constructor had [AudioFormat.SAMPLE_RATE_UNSPECIFIED](AudioFormat.md), then the sink sample rate is a route-dependent default value based on the source \[sic\]. 

### getState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getState(): Int
```

Returns the state of the AudioRecord instance. This is useful after the AudioRecord instance has been created to check if it was initialized properly. This ensures that the appropriate hardware resources have been acquired. 
**See Also**

- [android.media.AudioRecord#STATE_INITIALIZED](AudioRecord.md)
- [android.media.AudioRecord#STATE_UNINITIALIZED](AudioRecord.md) 

### getTimestamp

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimestamp(
    outTimestamp: AudioTimestamp, 
    timebase: Int
): Int
```

Poll for an [AudioTimestamp](AudioTimestamp.md) on demand.

The AudioTimestamp reflects the frame delivery information at the earliest point available in the capture pipeline.

Calling [startRecording()](AudioRecord.md))following a [stop()](AudioRecord.md))will reset the frame count to 0.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outTimestamp` | [AudioTimestamp](AudioTimestamp.md):a caller provided non-null AudioTimestamp instance, which is updated with the AudioRecord frame delivery information upon success. |
| `timebase` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [AudioTimestamp.TIMEBASE_BOOTTIME](AudioTimestamp.md) or [AudioTimestamp.TIMEBASE_MONOTONIC](AudioTimestamp.md), used to select the clock for the AudioTimestamp time. Value is [android.media.AudioTimestamp#TIMEBASE_MONOTONIC](AudioTimestamp.md), or [android.media.AudioTimestamp#TIMEBASE_BOOTTIME](AudioTimestamp.md) |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](AudioRecord.md) if a timestamp is available, or [ERROR_INVALID_OPERATION](AudioRecord.md) if a timestamp not available. |

### isPrivacySensitive

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPrivacySensitive(): Boolean
```

Returns whether this AudioRecord is marked as privacy sensitive or not.

See [Builder.setPrivacySensitive(boolean)](../android/media/AudioRecord.Builder.md))

<br />

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if privacy sensitive, false otherwise |

### read

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    audioData: ByteArray, 
    offsetInBytes: Int, 
    sizeInBytes: Int
): Int
```

Reads audio data from the audio hardware for recording into a byte array. The format specified in the AudioRecord constructor should be [AudioFormat.ENCODING_PCM_8BIT](AudioFormat.md) to correspond to the data in the array.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the array to which the recorded audio data is written. This value cannot be`null`. |
| `offsetInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index in audioData from which the data is written expressed in bytes. |
| `sizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested bytes. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of bytes that were read, or one of the following error codes. The number of bytes will not exceed sizeInBytes. - [ERROR_INVALID_OPERATION](AudioRecord.md) if the object isn't properly initialized - [ERROR_BAD_VALUE](AudioRecord.md) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](AudioRecord.md) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](AudioRecord.md) in case of other error |

### read

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    audioData: ByteArray, 
    offsetInBytes: Int, 
    sizeInBytes: Int, 
    readMode: Int
): Int
```

Reads audio data from the audio hardware for recording into a byte array. The format specified in the AudioRecord constructor should be [AudioFormat.ENCODING_PCM_8BIT](AudioFormat.md) to correspond to the data in the array. The format can be [AudioFormat.ENCODING_PCM_16BIT](AudioFormat.md), but this is deprecated.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the array to which the recorded audio data is written. This value cannot be`null`. |
| `offsetInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index in audioData to which the data is written expressed in bytes. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested bytes. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |
| `readMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [READ_BLOCKING](AudioRecord.md), [READ_NON_BLOCKING](AudioRecord.md). With [READ_BLOCKING](AudioRecord.md), the read will block until all the requested data is read. With [READ_NON_BLOCKING](AudioRecord.md), the read will return immediately after reading as much audio data as possible without blocking. Value is [android.media.AudioRecord#READ_BLOCKING](AudioRecord.md), or [android.media.AudioRecord#READ_NON_BLOCKING](AudioRecord.md) |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of bytes that were read, or one of the following error codes. The number of bytes will be a multiple of the frame size in bytes not to exceed sizeInBytes. - [ERROR_INVALID_OPERATION](AudioRecord.md) if the object isn't properly initialized - [ERROR_BAD_VALUE](AudioRecord.md) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](AudioRecord.md) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](AudioRecord.md) in case of other error |

### read

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    audioData: FloatArray, 
    offsetInFloats: Int, 
    sizeInFloats: Int, 
    readMode: Int
): Int
```

Reads audio data from the audio hardware for recording into a float array. The format specified in the AudioRecord constructor should be [AudioFormat.ENCODING_PCM_FLOAT](AudioFormat.md) to correspond to the data in the array.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioData` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):the array to which the recorded audio data is written. This value cannot be`null`. |
| `offsetInFloats` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index in audioData from which the data is written. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInFloats` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested floats. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |
| `readMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [READ_BLOCKING](AudioRecord.md), [READ_NON_BLOCKING](AudioRecord.md). With [READ_BLOCKING](AudioRecord.md), the read will block until all the requested data is read. With [READ_NON_BLOCKING](AudioRecord.md), the read will return immediately after reading as much audio data as possible without blocking. Value is [android.media.AudioRecord#READ_BLOCKING](AudioRecord.md), or [android.media.AudioRecord#READ_NON_BLOCKING](AudioRecord.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of floats that were read, or one of the following error codes. The number of floats will be a multiple of the channel count not to exceed sizeInFloats. - [ERROR_INVALID_OPERATION](AudioRecord.md) if the object isn't properly initialized - [ERROR_BAD_VALUE](AudioRecord.md) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](AudioRecord.md) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](AudioRecord.md) in case of other error |

### read

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    audioBuffer: ByteBuffer, 
    sizeInBytes: Int
): Int
```

Reads audio data from the audio hardware for recording into a direct buffer. If this buffer is not a direct buffer, this method will always return 0. Note that the value returned by [java.nio.Buffer#position()](../java.nio/Buffer.md))on this buffer is unchanged after a call to this method. The representation of the data in the buffer will depend on the format specified in the AudioRecord constructor, and will be native endian.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioBuffer` | [ByteBuffer](../java.nio/ByteBuffer.md):the direct buffer to which the recorded audio data is written. Data is written to the beginning of the byte buffer. Importantly, this method ignores the [java.nio.Buffer#position()](../java.nio/Buffer.md))and [java.nio.Buffer#limit()](../java.nio/Buffer.md))properties. This value cannot be`null`. |
| `sizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested bytes. It is recommended but not enforced that the number of bytes requested be a multiple of the frame size (sample size in bytes multiplied by the channel count). |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of bytes that were read, or one of the following error codes. The number of bytes will not exceed sizeInBytes and will be truncated to be a multiple of the frame size. - [ERROR_INVALID_OPERATION](AudioRecord.md) if the object isn't properly initialized - [ERROR_BAD_VALUE](AudioRecord.md) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](AudioRecord.md) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](AudioRecord.md) in case of other error |

### read

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    audioBuffer: ByteBuffer, 
    sizeInBytes: Int, 
    readMode: Int
): Int
```

Reads audio data from the audio hardware for recording into a direct buffer. If this buffer is not a direct buffer, this method will always return 0. Note that the value returned by [java.nio.Buffer#position()](../java.nio/Buffer.md))on this buffer is unchanged after a call to this method. The representation of the data in the buffer will depend on the format specified in the AudioRecord constructor, and will be native endian.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioBuffer` | [ByteBuffer](../java.nio/ByteBuffer.md):the direct buffer to which the recorded audio data is written. Data is written to the beginning of the byte buffer. Importantly, this method ignores the [java.nio.Buffer#position()](../java.nio/Buffer.md))and [java.nio.Buffer#limit()](../java.nio/Buffer.md))properties. This value cannot be`null`. |
| `sizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested bytes. It is recommended but not enforced that the number of bytes requested be a multiple of the frame size (sample size in bytes multiplied by the channel count). |
| `readMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [READ_BLOCKING](AudioRecord.md), [READ_NON_BLOCKING](AudioRecord.md). With [READ_BLOCKING](AudioRecord.md), the read will block until all the requested data is read. With [READ_NON_BLOCKING](AudioRecord.md), the read will return immediately after reading as much audio data as possible without blocking. Value is [android.media.AudioRecord#READ_BLOCKING](AudioRecord.md), or [android.media.AudioRecord#READ_NON_BLOCKING](AudioRecord.md) |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of bytes that were read, or one of the following error codes. The number of bytes will not exceed sizeInBytes and will be truncated to be a multiple of the frame size. - [ERROR_INVALID_OPERATION](AudioRecord.md) if the object isn't properly initialized - [ERROR_BAD_VALUE](AudioRecord.md) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](AudioRecord.md) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](AudioRecord.md) in case of other error |

### read

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    audioData: ShortArray, 
    offsetInShorts: Int, 
    sizeInShorts: Int
): Int
```

Reads audio data from the audio hardware for recording into a short array. The format specified in the AudioRecord constructor should be [AudioFormat.ENCODING_PCM_16BIT](AudioFormat.md) to correspond to the data in the array.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioData` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html):the array to which the recorded audio data is written. This value cannot be`null`. |
| `offsetInShorts` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index in audioData to which the data is written expressed in shorts. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInShorts` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested shorts. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of shorts that were read, or one of the following error codes. The number of shorts will be a multiple of the channel count not to exceed sizeInShorts. - [ERROR_INVALID_OPERATION](AudioRecord.md) if the object isn't properly initialized - [ERROR_BAD_VALUE](AudioRecord.md) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](AudioRecord.md) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](AudioRecord.md) in case of other error |

### read

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    audioData: ShortArray, 
    offsetInShorts: Int, 
    sizeInShorts: Int, 
    readMode: Int
): Int
```

Reads audio data from the audio hardware for recording into a short array. The format specified in the AudioRecord constructor should be [AudioFormat.ENCODING_PCM_16BIT](AudioFormat.md) to correspond to the data in the array.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioData` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html):the array to which the recorded audio data is written. This value cannot be`null`. |
| `offsetInShorts` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index in audioData from which the data is written expressed in shorts. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInShorts` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested shorts. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |
| `readMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [READ_BLOCKING](AudioRecord.md), [READ_NON_BLOCKING](AudioRecord.md). With [READ_BLOCKING](AudioRecord.md), the read will block until all the requested data is read. With [READ_NON_BLOCKING](AudioRecord.md), the read will return immediately after reading as much audio data as possible without blocking. Value is [android.media.AudioRecord#READ_BLOCKING](AudioRecord.md), or [android.media.AudioRecord#READ_NON_BLOCKING](AudioRecord.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of shorts that were read, or one of the following error codes. The number of shorts will be a multiple of the channel count not to exceed sizeInShorts. - [ERROR_INVALID_OPERATION](AudioRecord.md) if the object isn't properly initialized - [ERROR_BAD_VALUE](AudioRecord.md) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](AudioRecord.md) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](AudioRecord.md) in case of other error |

### registerAudioRecordingCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerAudioRecordingCallback(
    executor: Executor, 
    cb: AudioManager.AudioRecordingCallback
): Unit
```

Register a callback to be notified of audio capture changes via a [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md). A callback is received when the capture path configuration changes (pre-processing, format, sampling rate...) or capture is silenced/unsilenced by the system.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md): [Executor](../java.util.concurrent/Executor.md) to handle the callbacks. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `cb` | [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md):non-null callback to register |

### release

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Releases the native AudioRecord resources. The object can no longer be used and the reference should be set to null after a call to release() 

### removeOnRoutingChangedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeOnRoutingChangedListener(listener: AudioRecord.OnRoutingChangedListener!): Unit
```

**Deprecated:** *users should switch to the general purpose [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) class instead.*

Removes an [OnRoutingChangedListener](../android/media/AudioRecord.OnRoutingChangedListener.md) which has been previously added to receive rerouting notifications.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRecord.OnRoutingChangedListener](../android/media/AudioRecord.OnRoutingChangedListener.md)!:The previously added [OnRoutingChangedListener](../android/media/AudioRecord.OnRoutingChangedListener.md) interface to remove. |

### removeOnRoutingChangedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeOnRoutingChangedListener(listener: AudioRouting.OnRoutingChangedListener!): Unit
```

Removes an [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) which has been previously added to receive rerouting notifications.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!:The previously added [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) interface to remove. |

### setLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLogSessionId(logSessionId: LogSessionId): Unit
```

Sets a [LogSessionId](../android.media.metrics/LogSessionId.md) instance to this AudioRecord for metrics collection.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `logSessionId` | [LogSessionId](../android.media.metrics/LogSessionId.md):a [LogSessionId](../android.media.metrics/LogSessionId.md) instance which is used to identify this object to the metrics service. Proper generated Ids must be obtained from the Java metrics service and should be considered opaque. Use [LogSessionId.LOG_SESSION_ID_NONE](../android.media.metrics/LogSessionId.md) to remove the logSessionId association. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------|
| `java.lang.IllegalStateException` | if AudioRecord not initialized. |

### setNotificationMarkerPosition

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNotificationMarkerPosition(markerInFrames: Int): Int
```

Sets the marker position at which the listener is called, if set with [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener)](AudioRecord.md))or [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,android.os.Handler)](AudioRecord.md)).

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------|
| `markerInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):marker position expressed in frames |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | error code or success, see [SUCCESS](AudioRecord.md), [ERROR_BAD_VALUE](AudioRecord.md), [ERROR_INVALID_OPERATION](AudioRecord.md) |

### setPositionNotificationPeriod

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPositionNotificationPeriod(periodInFrames: Int): Int
```

Sets the period at which the listener is called, if set with [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener)](AudioRecord.md))or [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,android.os.Handler)](AudioRecord.md)). It is possible for notifications to be lost if the period is too small.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------|
| `periodInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):update period expressed in frames |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | error code or success, see [SUCCESS](AudioRecord.md), [ERROR_INVALID_OPERATION](AudioRecord.md) |

### setPreferredDevice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferredDevice(deviceInfo: AudioDeviceInfo!): Boolean
```

Specifies an audio device (via an [AudioDeviceInfo](AudioDeviceInfo.md) object) to route the input to this AudioRecord.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceInfo` | [AudioDeviceInfo](AudioDeviceInfo.md)!:The [AudioDeviceInfo](AudioDeviceInfo.md) specifying the audio source. If deviceInfo is null, default routing is restored. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if successful, false if the specified [AudioDeviceInfo](AudioDeviceInfo.md) is non-null and does not correspond to a valid audio input device. |

### setPreferredMicrophoneDirection

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferredMicrophoneDirection(direction: Int): Boolean
```

Specifies the logical microphone (for processing). Applications can use this to specify which side of the device to optimize capture from. Typically used in conjunction with the camera capturing video.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.MicrophoneDirection#MIC_DIRECTION_UNSPECIFIED](MicrophoneDirection.md), [android.media.MicrophoneDirection#MIC_DIRECTION_TOWARDS_USER](MicrophoneDirection.md), [android.media.MicrophoneDirection#MIC_DIRECTION_AWAY_FROM_USER](MicrophoneDirection.md), or [android.media.MicrophoneDirection#MIC_DIRECTION_EXTERNAL](MicrophoneDirection.md) |

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if sucessful. |

### setPreferredMicrophoneFieldDimension

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferredMicrophoneFieldDimension(zoom: Float): Boolean
```

Specifies the zoom factor (i.e. the field dimension) for the selected microphone (for processing). The selected microphone is determined by the use-case for the stream.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `zoom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the desired field dimension of microphone capture. Range is from -1 (wide angle), though 0 (no zoom) to 1 (maximum zoom). Value is between -1.0f and 1.0f inclusive |

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if sucessful. |

### setRecordPositionUpdateListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRecordPositionUpdateListener(listener: AudioRecord.OnRecordPositionUpdateListener!): Unit
```

Sets the listener the AudioRecord notifies when a previously set marker is reached or for each periodic record head position update.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRecord.OnRecordPositionUpdateListener](../android/media/AudioRecord.OnRecordPositionUpdateListener.md)!: |

### setRecordPositionUpdateListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRecordPositionUpdateListener(
    listener: AudioRecord.OnRecordPositionUpdateListener!, 
    handler: Handler!
): Unit
```

Sets the listener the AudioRecord notifies when a previously set marker is reached or for each periodic record head position update. Use this method to receive AudioRecord events in the Handler associated with another thread than the one in which you created the AudioRecord instance.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRecord.OnRecordPositionUpdateListener](../android/media/AudioRecord.OnRecordPositionUpdateListener.md)!: |
| `handler` | [Handler](../android.os/Handler.md)!:the Handler that will receive the event notification messages. |

### startRecording

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startRecording(): Unit
```

Starts recording from the AudioRecord instance.

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

### startRecording

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startRecording(syncEvent: MediaSyncEvent!): Unit
```

Starts recording from the AudioRecord instance when the specified synchronization event occurs on the specified audio session.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------|
| `syncEvent` | [MediaSyncEvent](MediaSyncEvent.md)!:event that triggers the capture. |

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

**See Also**

- [android.media.MediaSyncEvent](MediaSyncEvent.md) 

### stop

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stop(): Unit
```

Stops recording.

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

### unregisterAudioRecordingCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterAudioRecordingCallback(cb: AudioManager.AudioRecordingCallback): Unit
```

Unregister an audio recording callback previously registered with [registerAudioRecordingCallback(java.util.concurrent.Executor,android.media.AudioManager.AudioRecordingCallback)](AudioRecord.md)).

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md):non-null callback to unregister |

## Protected methods

### finalize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
