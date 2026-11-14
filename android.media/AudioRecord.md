# AudioRecord

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioRecord

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioRecord "View this page in Java") 
| --- | --- |

```
open class AudioRecord : AudioRecordingMonitor, AudioRouting, MicrophoneDirection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioRecord](https://developer.android.com/reference/kotlin/android/media/AudioRecord#) |

The AudioRecord class manages the audio resources for Java applications to record audio from the audio input hardware of the platform. This is achieved by "pulling" (reading) the data from the AudioRecord object. The application is responsible for polling the AudioRecord object in time using one of the following three methods:[read(byte[],int,int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)),[read(short[],int,int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#read(kotlin.ShortArray,%20kotlin.Int,%20kotlin.Int))or [read(java.nio.ByteBuffer,int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#read(java.nio.ByteBuffer,%20kotlin.Int)). The choice of which method to use will be based on the audio data storage format that is the most convenient for the user of AudioRecord.

Upon creation, an AudioRecord object initializes its associated audio buffer that it will fill with the new audio data. The size of this buffer, specified during the construction, determines how long an AudioRecord can record before "over-running" data that has not been read yet. Data should be read from the audio hardware in chunks of sizes inferior to the total recording buffer size.

Applications creating an AudioRecord instance need [android.Manifest.permission#RECORD_AUDIO](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RECORD_AUDIO:kotlin.String) or the Builder will throw [java.lang.UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#) on [build()](https://developer.android.com/reference/kotlin/android/media/AudioRecord.Builder#build()), and the constructor will return an instance in state [STATE_UNINITIALIZED](https://developer.android.com/reference/kotlin/android/media/AudioRecord#STATE_UNINITIALIZED:kotlin.Int).

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](https://developer.android.com/reference/kotlin/android/media/AudioRecord.Builder) Builder class for [AudioRecord](https://developer.android.com/reference/kotlin/android/media/AudioRecord#) objects. |
| | [MetricsConstants](https://developer.android.com/reference/kotlin/android/media/AudioRecord.MetricsConstants) <br /> |
| abstract | [OnRecordPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRecordPositionUpdateListener) Interface definition for a callback to be invoked when an AudioRecord has reached a notification marker set by [AudioRecord.setNotificationMarkerPosition(int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setNotificationMarkerPosition(kotlin.Int))or for periodic updates on the progress of the record head, as set by [AudioRecord.setPositionNotificationPeriod(int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setPositionNotificationPeriod(kotlin.Int)). |
| --- | --- |
| abstract | [OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRoutingChangedListener) Defines the interface by which applications can receive notifications of routing changes for the associated [AudioRecord](https://developer.android.com/reference/kotlin/android/media/AudioRecord#). |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR:kotlin.Int) Denotes a generic operation failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_BAD_VALUE:kotlin.Int) Denotes a failure due to the use of an invalid value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEAD_OBJECT](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_DEAD_OBJECT:kotlin.Int) An error code indicating that the object reporting it is no longer valid and needs to be recreated. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_INVALID_OPERATION:kotlin.Int) Denotes a failure due to the improper use of a method. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int) The read mode indicating the read operation will block until all data requested has been read. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int) The read mode indicating the read operation will return immediately after reading as much audio data as possible without blocking. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDSTATE_RECORDING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#RECORDSTATE_RECORDING:kotlin.Int) indicates AudioRecord recording state is recording |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDSTATE_STOPPED](https://developer.android.com/reference/kotlin/android/media/AudioRecord#RECORDSTATE_STOPPED:kotlin.Int) indicates AudioRecord recording state is not recording |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_INITIALIZED](https://developer.android.com/reference/kotlin/android/media/AudioRecord#STATE_INITIALIZED:kotlin.Int) indicates AudioRecord state is ready to be used |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNINITIALIZED](https://developer.android.com/reference/kotlin/android/media/AudioRecord#STATE_UNINITIALIZED:kotlin.Int) indicates AudioRecord state is not successfully initialized. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](https://developer.android.com/reference/kotlin/android/media/AudioRecord#SUCCESS:kotlin.Int) Denotes a successful operation. |

| Inherited constants ||
|---|---|
| From class [MicrophoneDirection](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_AWAY_FROM_USER](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_AWAY_FROM_USER:kotlin.Int) <br /> Optimize capture for audio coming from the side of the device pointing away from the user. In the typical case, a device with a single screen, screen-side camera/microphone and non-screen-side camera/microphone, this will be the non-screen side. For a different device geometry, it is the side for which the expectation is to be facing away from the user. This is the "taking a video of something else" case. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_EXTERNAL](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_EXTERNAL:kotlin.Int) <br /> Optimize capture for audio coming from an off-device microphone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_TOWARDS_USER](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_TOWARDS_USER:kotlin.Int) <br /> Optimize capture for audio coming from the side of the device facing the user. In the typical case, a device with a single screen, screen-side camera/microphone and non-screen-side camera/microphone, this will be the screen side (as in a "selfie"). For a different device geometry, it is the side for which the expectation is to be facing the user. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_UNSPECIFIED:kotlin.Int) <br /> Don't do any directionality processing of the activated microphone(s). <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AudioRecord](https://developer.android.com/reference/kotlin/android/media/AudioRecord#AudioRecord(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`audioSource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sampleRateInHz:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `channelConfig:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bufferSizeInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Class constructor. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord#addOnRoutingChangedListener(android.media.AudioRecord.OnRoutingChangedListener,%20android.os.Handler))`(`listener:` ` [AudioRecord.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRoutingChangedListener)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Adds an [OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRoutingChangedListener) to receive notifications of routing changes on this AudioRecord. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord#addOnRoutingChangedListener(android.media.AudioRouting.OnRoutingChangedListener,%20android.os.Handler))`(`listener:` ` [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Adds an [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) to receive notifications of routing changes on this AudioRecord. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MicrophoneInfo](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo)!\>! | [getActiveMicrophones](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getActiveMicrophones())`()` Returns a lists of [MicrophoneInfo](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo) representing the active microphones. |
| --- | --- |
| open [AudioRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration)? | [getActiveRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getActiveRecordingConfiguration())`()` Returns the current active audio recording for this audio recorder. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioFormat](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getAudioFormat())`()` Returns the configured audio data encoding. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSessionId](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getAudioSessionId())`()` Returns the audio session ID. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSource](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getAudioSource())`()` Returns the audio recording source. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBufferSizeInFrames](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getBufferSizeInFrames())`()` Returns the frame count of the native`AudioRecord`buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChannelConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getChannelConfiguration())`()` Returns the configured channel position mask. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChannelCount](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getChannelCount())`()` Returns the configured number of channels. |
| open [AudioFormat](https://developer.android.com/reference/kotlin/android/media/AudioFormat) | [getFormat](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getFormat())`()` Returns the configured`AudioRecord`format. |
| open [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) | [getLogSessionId](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getLogSessionId())`()` Returns the [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId). |
| --- | --- |
| open [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)! | [getMetrics](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getMetrics())`()` Return Metrics data about the current AudioTrack instance. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinBufferSize](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getMinBufferSize(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`sampleRateInHz:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `channelConfig:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the minimum buffer size required for the successful creation of an AudioRecord object, in byte units. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNotificationMarkerPosition](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getNotificationMarkerPosition())`()` Returns the notification marker position expressed in frames. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPositionNotificationPeriod](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getPositionNotificationPeriod())`()` Returns the notification update period expressed in frames. |
| open [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)! | [getPreferredDevice](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getPreferredDevice())`()` Returns the selected input specified by [setPreferredDevice](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setPreferredDevice(android.media.AudioDeviceInfo)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRecordingState](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getRecordingState())`()` Returns the recording state of the AudioRecord instance. |
| --- | --- |
| open [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)! | [getRoutedDevice](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getRoutedDevice())`()` Returns an [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) identifying the current routing of this AudioRecord. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!\> | [getRoutedDevices](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getRoutedDevices())`()` Returns a List of [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) identifying the current routing of this AudioRecord. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSampleRate](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getSampleRate())`()` Returns the configured audio sink sample rate in Hz. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getState())`()` Returns the state of the AudioRecord instance. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimestamp](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getTimestamp(android.media.AudioTimestamp,%20kotlin.Int))`(`outTimestamp:` ` [AudioTimestamp](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp)`, `timebase:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Poll for an [AudioTimestamp](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp) on demand. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrivacySensitive](https://developer.android.com/reference/kotlin/android/media/AudioRecord#isPrivacySensitive())`()` Returns whether this AudioRecord is marked as privacy sensitive or not. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/android/media/AudioRecord#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`audioData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offsetInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sizeInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a byte array. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/android/media/AudioRecord#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`audioData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offsetInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sizeInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a byte array. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/android/media/AudioRecord#read(kotlin.FloatArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`audioData:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `offsetInFloats:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sizeInFloats:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a float array. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/android/media/AudioRecord#read(java.nio.ByteBuffer,%20kotlin.Int))`(`audioBuffer:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)`, `sizeInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a direct buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/android/media/AudioRecord#read(java.nio.ByteBuffer,%20kotlin.Int,%20kotlin.Int))`(`audioBuffer:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)`, `sizeInBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a direct buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/android/media/AudioRecord#read(kotlin.ShortArray,%20kotlin.Int,%20kotlin.Int))`(`audioData:` ` [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)`, `offsetInShorts:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sizeInShorts:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a short array. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/android/media/AudioRecord#read(kotlin.ShortArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`audioData:` ` [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)`, `offsetInShorts:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sizeInShorts:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads audio data from the audio hardware for recording into a short array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioRecord#registerAudioRecordingCallback(java.util.concurrent.Executor,%20android.media.AudioManager.AudioRecordingCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `cb:` ` [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback)`)` Register a callback to be notified of audio capture changes via a [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/media/AudioRecord#release())`()` Releases the native AudioRecord resources. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord#removeOnRoutingChangedListener(android.media.AudioRecord.OnRoutingChangedListener))`(`listener:` ` [AudioRecord.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRoutingChangedListener)!`)` Removes an [OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRoutingChangedListener) which has been previously added to receive rerouting notifications. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord#removeOnRoutingChangedListener(android.media.AudioRouting.OnRoutingChangedListener))`(`listener:` ` [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener)!`)` Removes an [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) which has been previously added to receive rerouting notifications. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLogSessionId](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setLogSessionId(android.media.metrics.LogSessionId))`(`logSessionId:` ` [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId)`)` Sets a [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) instance to this AudioRecord for metrics collection. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setNotificationMarkerPosition](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setNotificationMarkerPosition(kotlin.Int))`(`markerInFrames:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the marker position at which the listener is called, if set with [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener))or [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,%20android.os.Handler)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setPositionNotificationPeriod](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setPositionNotificationPeriod(kotlin.Int))`(`periodInFrames:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the period at which the listener is called, if set with [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener))or [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,%20android.os.Handler)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredDevice](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setPreferredDevice(android.media.AudioDeviceInfo))`(`deviceInfo:` ` [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!`)` Specifies an audio device (via an [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) object) to route the input to this AudioRecord. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredMicrophoneDirection](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setPreferredMicrophoneDirection(kotlin.Int))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specifies the logical microphone (for processing). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredMicrophoneFieldDimension](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setPreferredMicrophoneFieldDimension(kotlin.Float))`(`zoom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Specifies the zoom factor (i.e. the field dimension) for the selected microphone (for processing). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRecordPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener))`(`listener:` ` [AudioRecord.OnRecordPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRecordPositionUpdateListener)!`)` Sets the listener the AudioRecord notifies when a previously set marker is reached or for each periodic record head position update. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRecordPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,%20android.os.Handler))`(`listener:` ` [AudioRecord.OnRecordPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRecordPositionUpdateListener)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Sets the listener the AudioRecord notifies when a previously set marker is reached or for each periodic record head position update. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startRecording](https://developer.android.com/reference/kotlin/android/media/AudioRecord#startRecording())`()` Starts recording from the AudioRecord instance. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startRecording](https://developer.android.com/reference/kotlin/android/media/AudioRecord#startRecording(android.media.MediaSyncEvent))`(`syncEvent:` ` [MediaSyncEvent](https://developer.android.com/reference/kotlin/android/media/MediaSyncEvent)!`)` Starts recording from the AudioRecord instance when the specified synchronization event occurs on the specified audio session. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](https://developer.android.com/reference/kotlin/android/media/AudioRecord#stop())`()` Stops recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioRecord#unregisterAudioRecordingCallback(android.media.AudioManager.AudioRecordingCallback))`(`cb:` ` [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback)`)` Unregister an audio recording callback previously registered with [registerAudioRecordingCallback(java.util.concurrent.Executor,android.media.AudioManager.AudioRecordingCallback)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#registerAudioRecordingCallback(java.util.concurrent.Executor,%20android.media.AudioManager.AudioRecordingCallback)). |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/AudioRecord#finalize())`()` <br /> |

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

Class constructor. Though some invalid parameters will result in an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) exception, other errors do not. Thus you should call [getState()](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getState())immediately after construction to confirm that the object is usable. 
Requires [android.Manifest.permission#RECORD_AUDIO](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RECORD_AUDIO:kotlin.String)

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioSource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the recording source. See [MediaRecorder.AudioSource](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource) for the recording source definitions. |
| `sampleRateInHz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the sample rate expressed in Hertz. 44100Hz is currently the only rate that is guaranteed to work on all devices, but other rates such as 22050, 16000, and 11025 may work on some devices. [AudioFormat.SAMPLE_RATE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/AudioFormat#SAMPLE_RATE_UNSPECIFIED:kotlin.Int) means to use a route-dependent value which is usually the sample rate of the source. [getSampleRate()](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getSampleRate())can be used to retrieve the actual sample rate chosen. |
| `channelConfig` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):describes the configuration of the audio channels. See [AudioFormat.CHANNEL_IN_MONO](https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_MONO:kotlin.Int) and [AudioFormat.CHANNEL_IN_STEREO](https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_STEREO:kotlin.Int). [AudioFormat.CHANNEL_IN_MONO](https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_MONO:kotlin.Int) is guaranteed to work on all devices. |
| --- | --- |
| `audioFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the format in which the audio data is to be returned. See [AudioFormat.ENCODING_PCM_8BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int), [AudioFormat.ENCODING_PCM_16BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int), and [AudioFormat.ENCODING_PCM_FLOAT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int). |
| `bufferSizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the total size (in bytes) of the buffer where audio data is written to during the recording. New audio data can be read from this buffer in smaller chunks than this size. See [getMinBufferSize(int,int,int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getMinBufferSize(kotlin.Int,%20kotlin.Int,%20kotlin.Int))to determine the minimum required buffer size for the successful creation of an AudioRecord instance. Using values smaller than getMinBufferSize() will result in an initialization failure. |

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

**Deprecated:** *users should switch to the general purpose [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) class instead.*

Adds an [OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRoutingChangedListener) to receive notifications of routing changes on this AudioRecord.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRecord.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRoutingChangedListener)!:The [OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRoutingChangedListener) interface to receive notifications of rerouting events. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:Specifies the [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) object for the thread on which to execute the callback. If`null`, the [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) associated with the main [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#) will be used. |

### addOnRoutingChangedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addOnRoutingChangedListener(
    listener: AudioRouting.OnRoutingChangedListener!, 
    handler: Handler!
): Unit
```

Adds an [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) to receive notifications of routing changes on this AudioRecord.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener)!:The [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) interface to receive notifications of rerouting events. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:Specifies the [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) object for the thread on which to execute the callback. If`null`, the [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) associated with the main [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#) will be used. |

### getActiveMicrophones

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActiveMicrophones(): MutableList<MicrophoneInfo!>!
```

Returns a lists of [MicrophoneInfo](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo) representing the active microphones. By querying channel mapping for each active microphone, developer can know how the microphone is used by each channels or a capture stream. Note that the information about the active microphones may change during a recording. See [AudioManager.registerAudioDeviceCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerAudioDeviceCallback(android.media.AudioDeviceCallback,%20android.os.Handler))to be notified of changes in the audio devices, querying the active microphones then will return the latest information.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MicrophoneInfo](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo)!>! | a lists of [MicrophoneInfo](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo) representing the active microphones. |

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
| [AudioRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration)? | a valid [AudioRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration) if this recorder is active or null otherwise. |

**See Also**

- [android.media.AudioRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration) 

### getAudioFormat

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAudioFormat(): Int
```

Returns the configured audio data encoding. See [AudioFormat.ENCODING_PCM_8BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int), [AudioFormat.ENCODING_PCM_16BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int), and [AudioFormat.ENCODING_PCM_FLOAT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int). 

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

- [android.media.MediaRecorder.AudioSource](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource) 

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

See [AudioFormat.CHANNEL_IN_MONO](https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_MONO:kotlin.Int) and [AudioFormat.CHANNEL_IN_STEREO](https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_STEREO:kotlin.Int). This method may return [AudioFormat.CHANNEL_INVALID](https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_INVALID:kotlin.Int) if a channel index mask is used. Consider [getFormat()](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getFormat())instead, to obtain an [AudioFormat](https://developer.android.com/reference/kotlin/android/media/AudioFormat), which contains both the channel position mask and the channel index mask. 

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
| [AudioFormat](https://developer.android.com/reference/kotlin/android/media/AudioFormat) | an [AudioFormat](https://developer.android.com/reference/kotlin/android/media/AudioFormat) containing the`AudioRecord`parameters at the time of configuration. This value cannot be`null`. |

### getLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLogSessionId(): LogSessionId
```

Returns the [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId).

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------|
| [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) | This value cannot be`null`. |

### getMetrics

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMetrics(): PersistableBundle!
```

Return Metrics data about the current AudioTrack instance.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)! | a [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) containing the set of attributes and values available for the media being handled by this instance of AudioRecord The attributes are descibed in [MetricsConstants](https://developer.android.com/reference/kotlin/android/media/AudioRecord.MetricsConstants). Additional vendor-specific fields may also be present in the return value. |

### getMinBufferSize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMinBufferSize(
    sampleRateInHz: Int, 
    channelConfig: Int, 
    audioFormat: Int
): Int
```

Returns the minimum buffer size required for the successful creation of an AudioRecord object, in byte units. Note that this size doesn't guarantee a smooth recording under load, and higher values should be chosen according to the expected frequency at which the AudioRecord instance will be polled for new data. See [AudioRecord(int,int,int,int,int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#AudioRecord(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))for more information on valid configuration values.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sampleRateInHz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the sample rate expressed in Hertz. [AudioFormat.SAMPLE_RATE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/AudioFormat#SAMPLE_RATE_UNSPECIFIED:kotlin.Int) is not permitted. |
| `channelConfig` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):describes the configuration of the audio channels. See [AudioFormat.CHANNEL_IN_MONO](https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_MONO:kotlin.Int) and [AudioFormat.CHANNEL_IN_STEREO](https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_STEREO:kotlin.Int) |
| `audioFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the format in which the audio data is represented. See [AudioFormat.ENCODING_PCM_16BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int). |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_BAD_VALUE:kotlin.Int) if the recording parameters are not supported by the hardware, or an invalid parameter was passed, or [ERROR](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR:kotlin.Int) if the implementation was unable to query the hardware for its input properties, or the minimum buffer size expressed in bytes. |

**See Also**

- [#AudioRecord(int, int, int, int, int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#AudioRecord(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)) 

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

Returns the selected input specified by [setPreferredDevice](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setPreferredDevice(android.media.AudioDeviceInfo)). Note that this is not guarenteed to correspond to the actual device being used for recording. 

### getRecordingState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRecordingState(): Int
```

Returns the recording state of the AudioRecord instance. 
**See Also**

- [android.media.AudioRecord#RECORDSTATE_STOPPED](https://developer.android.com/reference/kotlin/android/media/AudioRecord#RECORDSTATE_STOPPED:kotlin.Int)
- [android.media.AudioRecord#RECORDSTATE_RECORDING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#RECORDSTATE_RECORDING:kotlin.Int) 

### getRoutedDevice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoutedDevice(): AudioDeviceInfo!
```

Returns an [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) identifying the current routing of this AudioRecord. Note: The query is only valid if the AudioRecord is currently recording. If it is not,`getRoutedDevice()`will return null. 

### getRoutedDevices

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoutedDevices(): MutableList<AudioDeviceInfo!>
```

Returns a List of [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) identifying the current routing of this AudioRecord. Note: The query is only valid if the AudioRecord is currently playing. If it is not,`getRoutedDevices()`will return an empty list.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!> | This value cannot be`null`. |

### getSampleRate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSampleRate(): Int
```

Returns the configured audio sink sample rate in Hz. The sink sample rate never changes after construction. If the constructor had a specific sample rate, then the sink sample rate is that value. If the constructor had [AudioFormat.SAMPLE_RATE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/AudioFormat#SAMPLE_RATE_UNSPECIFIED:kotlin.Int), then the sink sample rate is a route-dependent default value based on the source \[sic\]. 

### getState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getState(): Int
```

Returns the state of the AudioRecord instance. This is useful after the AudioRecord instance has been created to check if it was initialized properly. This ensures that the appropriate hardware resources have been acquired. 
**See Also**

- [android.media.AudioRecord#STATE_INITIALIZED](https://developer.android.com/reference/kotlin/android/media/AudioRecord#STATE_INITIALIZED:kotlin.Int)
- [android.media.AudioRecord#STATE_UNINITIALIZED](https://developer.android.com/reference/kotlin/android/media/AudioRecord#STATE_UNINITIALIZED:kotlin.Int) 

### getTimestamp

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimestamp(
    outTimestamp: AudioTimestamp, 
    timebase: Int
): Int
```

Poll for an [AudioTimestamp](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp) on demand.

The AudioTimestamp reflects the frame delivery information at the earliest point available in the capture pipeline.

Calling [startRecording()](https://developer.android.com/reference/kotlin/android/media/AudioRecord#startRecording())following a [stop()](https://developer.android.com/reference/kotlin/android/media/AudioRecord#stop())will reset the frame count to 0.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outTimestamp` | [AudioTimestamp](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp):a caller provided non-null AudioTimestamp instance, which is updated with the AudioRecord frame delivery information upon success. |
| `timebase` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [AudioTimestamp.TIMEBASE_BOOTTIME](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#TIMEBASE_BOOTTIME:kotlin.Int) or [AudioTimestamp.TIMEBASE_MONOTONIC](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#TIMEBASE_MONOTONIC:kotlin.Int), used to select the clock for the AudioTimestamp time. Value is [android.media.AudioTimestamp#TIMEBASE_MONOTONIC](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#TIMEBASE_MONOTONIC:kotlin.Int), or [android.media.AudioTimestamp#TIMEBASE_BOOTTIME](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#TIMEBASE_BOOTTIME:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](https://developer.android.com/reference/kotlin/android/media/AudioRecord#SUCCESS:kotlin.Int) if a timestamp is available, or [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_INVALID_OPERATION:kotlin.Int) if a timestamp not available. |

### isPrivacySensitive

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPrivacySensitive(): Boolean
```

Returns whether this AudioRecord is marked as privacy sensitive or not.

See [Builder.setPrivacySensitive(boolean)](https://developer.android.com/reference/kotlin/android/media/AudioRecord.Builder#setPrivacySensitive(kotlin.Boolean))

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

Reads audio data from the audio hardware for recording into a byte array. The format specified in the AudioRecord constructor should be [AudioFormat.ENCODING_PCM_8BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int) to correspond to the data in the array.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the array to which the recorded audio data is written. This value cannot be`null`. |
| `offsetInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index in audioData from which the data is written expressed in bytes. |
| `sizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested bytes. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of bytes that were read, or one of the following error codes. The number of bytes will not exceed sizeInBytes. - [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_INVALID_OPERATION:kotlin.Int) if the object isn't properly initialized - [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_BAD_VALUE:kotlin.Int) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_DEAD_OBJECT:kotlin.Int) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR:kotlin.Int) in case of other error |

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

Reads audio data from the audio hardware for recording into a byte array. The format specified in the AudioRecord constructor should be [AudioFormat.ENCODING_PCM_8BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int) to correspond to the data in the array. The format can be [AudioFormat.ENCODING_PCM_16BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int), but this is deprecated.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the array to which the recorded audio data is written. This value cannot be`null`. |
| `offsetInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index in audioData to which the data is written expressed in bytes. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested bytes. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |
| `readMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int), [READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int). With [READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int), the read will block until all the requested data is read. With [READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int), the read will return immediately after reading as much audio data as possible without blocking. Value is [android.media.AudioRecord#READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int), or [android.media.AudioRecord#READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of bytes that were read, or one of the following error codes. The number of bytes will be a multiple of the frame size in bytes not to exceed sizeInBytes. - [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_INVALID_OPERATION:kotlin.Int) if the object isn't properly initialized - [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_BAD_VALUE:kotlin.Int) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_DEAD_OBJECT:kotlin.Int) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR:kotlin.Int) in case of other error |

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

Reads audio data from the audio hardware for recording into a float array. The format specified in the AudioRecord constructor should be [AudioFormat.ENCODING_PCM_FLOAT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int) to correspond to the data in the array.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioData` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):the array to which the recorded audio data is written. This value cannot be`null`. |
| `offsetInFloats` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index in audioData from which the data is written. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInFloats` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested floats. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |
| `readMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int), [READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int). With [READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int), the read will block until all the requested data is read. With [READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int), the read will return immediately after reading as much audio data as possible without blocking. Value is [android.media.AudioRecord#READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int), or [android.media.AudioRecord#READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of floats that were read, or one of the following error codes. The number of floats will be a multiple of the channel count not to exceed sizeInFloats. - [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_INVALID_OPERATION:kotlin.Int) if the object isn't properly initialized - [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_BAD_VALUE:kotlin.Int) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_DEAD_OBJECT:kotlin.Int) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR:kotlin.Int) in case of other error |

### read

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    audioBuffer: ByteBuffer, 
    sizeInBytes: Int
): Int
```

Reads audio data from the audio hardware for recording into a direct buffer. If this buffer is not a direct buffer, this method will always return 0. Note that the value returned by [java.nio.Buffer#position()](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#position())on this buffer is unchanged after a call to this method. The representation of the data in the buffer will depend on the format specified in the AudioRecord constructor, and will be native endian.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioBuffer` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#):the direct buffer to which the recorded audio data is written. Data is written to the beginning of the byte buffer. Importantly, this method ignores the [java.nio.Buffer#position()](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#position())and [java.nio.Buffer#limit()](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#limit())properties. This value cannot be`null`. |
| `sizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested bytes. It is recommended but not enforced that the number of bytes requested be a multiple of the frame size (sample size in bytes multiplied by the channel count). |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of bytes that were read, or one of the following error codes. The number of bytes will not exceed sizeInBytes and will be truncated to be a multiple of the frame size. - [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_INVALID_OPERATION:kotlin.Int) if the object isn't properly initialized - [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_BAD_VALUE:kotlin.Int) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_DEAD_OBJECT:kotlin.Int) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR:kotlin.Int) in case of other error |

### read

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    audioBuffer: ByteBuffer, 
    sizeInBytes: Int, 
    readMode: Int
): Int
```

Reads audio data from the audio hardware for recording into a direct buffer. If this buffer is not a direct buffer, this method will always return 0. Note that the value returned by [java.nio.Buffer#position()](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#position())on this buffer is unchanged after a call to this method. The representation of the data in the buffer will depend on the format specified in the AudioRecord constructor, and will be native endian.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioBuffer` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#):the direct buffer to which the recorded audio data is written. Data is written to the beginning of the byte buffer. Importantly, this method ignores the [java.nio.Buffer#position()](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#position())and [java.nio.Buffer#limit()](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#limit())properties. This value cannot be`null`. |
| `sizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested bytes. It is recommended but not enforced that the number of bytes requested be a multiple of the frame size (sample size in bytes multiplied by the channel count). |
| `readMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int), [READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int). With [READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int), the read will block until all the requested data is read. With [READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int), the read will return immediately after reading as much audio data as possible without blocking. Value is [android.media.AudioRecord#READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int), or [android.media.AudioRecord#READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int) |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of bytes that were read, or one of the following error codes. The number of bytes will not exceed sizeInBytes and will be truncated to be a multiple of the frame size. - [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_INVALID_OPERATION:kotlin.Int) if the object isn't properly initialized - [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_BAD_VALUE:kotlin.Int) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_DEAD_OBJECT:kotlin.Int) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR:kotlin.Int) in case of other error |

### read

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    audioData: ShortArray, 
    offsetInShorts: Int, 
    sizeInShorts: Int
): Int
```

Reads audio data from the audio hardware for recording into a short array. The format specified in the AudioRecord constructor should be [AudioFormat.ENCODING_PCM_16BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int) to correspond to the data in the array.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioData` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html):the array to which the recorded audio data is written. This value cannot be`null`. |
| `offsetInShorts` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index in audioData to which the data is written expressed in shorts. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInShorts` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested shorts. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of shorts that were read, or one of the following error codes. The number of shorts will be a multiple of the channel count not to exceed sizeInShorts. - [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_INVALID_OPERATION:kotlin.Int) if the object isn't properly initialized - [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_BAD_VALUE:kotlin.Int) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_DEAD_OBJECT:kotlin.Int) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR:kotlin.Int) in case of other error |

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

Reads audio data from the audio hardware for recording into a short array. The format specified in the AudioRecord constructor should be [AudioFormat.ENCODING_PCM_16BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int) to correspond to the data in the array.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioData` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html):the array to which the recorded audio data is written. This value cannot be`null`. |
| `offsetInShorts` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index in audioData from which the data is written expressed in shorts. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInShorts` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of requested shorts. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |
| `readMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int), [READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int). With [READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int), the read will block until all the requested data is read. With [READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int), the read will return immediately after reading as much audio data as possible without blocking. Value is [android.media.AudioRecord#READ_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_BLOCKING:kotlin.Int), or [android.media.AudioRecord#READ_NON_BLOCKING](https://developer.android.com/reference/kotlin/android/media/AudioRecord#READ_NON_BLOCKING:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero or the positive number of shorts that were read, or one of the following error codes. The number of shorts will be a multiple of the channel count not to exceed sizeInShorts. - [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_INVALID_OPERATION:kotlin.Int) if the object isn't properly initialized - [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_BAD_VALUE:kotlin.Int) if the parameters don't resolve to valid data and indexes - [ERROR_DEAD_OBJECT](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_DEAD_OBJECT:kotlin.Int) if the object is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next read() - [ERROR](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR:kotlin.Int) in case of other error |

### registerAudioRecordingCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerAudioRecordingCallback(
    executor: Executor, 
    cb: AudioManager.AudioRecordingCallback
): Unit
```

Register a callback to be notified of audio capture changes via a [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback). A callback is received when the capture path configuration changes (pre-processing, format, sampling rate...) or capture is silenced/unsilenced by the system.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) to handle the callbacks. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `cb` | [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback):non-null callback to register |

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

**Deprecated:** *users should switch to the general purpose [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) class instead.*

Removes an [OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRoutingChangedListener) which has been previously added to receive rerouting notifications.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRecord.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRoutingChangedListener)!:The previously added [OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRoutingChangedListener) interface to remove. |

### removeOnRoutingChangedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeOnRoutingChangedListener(listener: AudioRouting.OnRoutingChangedListener!): Unit
```

Removes an [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) which has been previously added to receive rerouting notifications.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener)!:The previously added [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) interface to remove. |

### setLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLogSessionId(logSessionId: LogSessionId): Unit
```

Sets a [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) instance to this AudioRecord for metrics collection.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `logSessionId` | [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId):a [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) instance which is used to identify this object to the metrics service. Proper generated Ids must be obtained from the Java metrics service and should be considered opaque. Use [LogSessionId.LOG_SESSION_ID_NONE](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId#LOG_SESSION_ID_NONE:android.media.metrics.LogSessionId) to remove the logSessionId association. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------|
| `java.lang.IllegalStateException` | if AudioRecord not initialized. |

### setNotificationMarkerPosition

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNotificationMarkerPosition(markerInFrames: Int): Int
```

Sets the marker position at which the listener is called, if set with [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener))or [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,%20android.os.Handler)).

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------|
| `markerInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):marker position expressed in frames |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | error code or success, see [SUCCESS](https://developer.android.com/reference/kotlin/android/media/AudioRecord#SUCCESS:kotlin.Int), [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_BAD_VALUE:kotlin.Int), [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_INVALID_OPERATION:kotlin.Int) |

### setPositionNotificationPeriod

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPositionNotificationPeriod(periodInFrames: Int): Int
```

Sets the period at which the listener is called, if set with [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener))or [setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setRecordPositionUpdateListener(android.media.AudioRecord.OnRecordPositionUpdateListener,%20android.os.Handler)). It is possible for notifications to be lost if the period is too small.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------|
| `periodInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):update period expressed in frames |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | error code or success, see [SUCCESS](https://developer.android.com/reference/kotlin/android/media/AudioRecord#SUCCESS:kotlin.Int), [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/AudioRecord#ERROR_INVALID_OPERATION:kotlin.Int) |

### setPreferredDevice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferredDevice(deviceInfo: AudioDeviceInfo!): Boolean
```

Specifies an audio device (via an [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) object) to route the input to this AudioRecord.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceInfo` | [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!:The [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) specifying the audio source. If deviceInfo is null, default routing is restored. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if successful, false if the specified [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) is non-null and does not correspond to a valid audio input device. |

### setPreferredMicrophoneDirection

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferredMicrophoneDirection(direction: Int): Boolean
```

Specifies the logical microphone (for processing). Applications can use this to specify which side of the device to optimize capture from. Typically used in conjunction with the camera capturing video.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.MicrophoneDirection#MIC_DIRECTION_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_UNSPECIFIED:kotlin.Int), [android.media.MicrophoneDirection#MIC_DIRECTION_TOWARDS_USER](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_TOWARDS_USER:kotlin.Int), [android.media.MicrophoneDirection#MIC_DIRECTION_AWAY_FROM_USER](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_AWAY_FROM_USER:kotlin.Int), or [android.media.MicrophoneDirection#MIC_DIRECTION_EXTERNAL](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_EXTERNAL:kotlin.Int) |

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
| `listener` | [AudioRecord.OnRecordPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRecordPositionUpdateListener)!: |

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
| `listener` | [AudioRecord.OnRecordPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRecordPositionUpdateListener)!: |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:the Handler that will receive the event notification messages. |

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
| `syncEvent` | [MediaSyncEvent](https://developer.android.com/reference/kotlin/android/media/MediaSyncEvent)!:event that triggers the capture. |

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

**See Also**

- [android.media.MediaSyncEvent](https://developer.android.com/reference/kotlin/android/media/MediaSyncEvent) 

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

Unregister an audio recording callback previously registered with [registerAudioRecordingCallback(java.util.concurrent.Executor,android.media.AudioManager.AudioRecordingCallback)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#registerAudioRecordingCallback(java.util.concurrent.Executor,%20android.media.AudioManager.AudioRecordingCallback)).

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback):non-null callback to unregister |

## Protected methods

### finalize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
