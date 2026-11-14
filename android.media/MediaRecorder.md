# MediaRecorder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaRecorder

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaRecorder "View this page in Java") 

```
open class MediaRecorder : AudioRecordingMonitor, AudioRouting, MicrophoneDirection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#) |

Used to record audio and video. The recording control is based on a simple state machine (see below).

<br />

A common case of using MediaRecorder to record audio works as follows: 

```kotlin
MediaRecorder recorder = new MediaRecorder(context);
  recorder.setAudioSource(MediaRecorder.AudioSource.MIC);
  recorder.setOutputFormat(MediaRecorder.OutputFormat.THREE_GPP);
  recorder.setAudioEncoder(MediaRecorder.AudioEncoder.AMR_NB);
  recorder.setOutputFile(PATH_NAME);
  recorder.prepare();
  recorder.start();   // Recording is now started
  ...
  recorder.stop();
  recorder.reset();   // You can reuse the object by going back to setAudioSource() step
  recorder.release(); // Now the object cannot be reused
  
```

Applications may want to register for informational and error events in order to be informed of some internal update and possible runtime errors during recording. Registration for such events is done by setting the appropriate listeners (via calls (to [setOnInfoListener(android.media.MediaRecorder.OnInfoListener)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOnInfoListener(android.media.MediaRecorder.OnInfoListener))setOnInfoListener and/or [setOnErrorListener(android.media.MediaRecorder.OnErrorListener)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOnErrorListener(android.media.MediaRecorder.OnErrorListener))setOnErrorListener). In order to receive the respective callback associated with these listeners, applications are required to create MediaRecorder objects on threads with a Looper running (the main UI thread by default already has a Looper running).

**Note:**Currently, MediaRecorder does not work on the emulator.
|
| ### Developer Guides
|
| For more information about how to use MediaRecorder for recording video, read the [Camera](https://developer.android.com/guide/topics/media/camera.html#capture-video) developer guide. For more information about how to use MediaRecorder for recording sound, read the [Audio Capture](https://developer.android.com/guide/topics/media/audio-capture.html) developer guide.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [AudioEncoder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioEncoder) Defines the audio encoding. |
| | [AudioSource](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource) Defines the audio source. |
| | [MetricsConstants](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.MetricsConstants) <br /> |
| abstract | [OnErrorListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnErrorListener) Interface definition for a callback to be invoked when an error occurs while recording. |
| abstract | [OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnInfoListener) Interface definition of a callback to be invoked to communicate some info and/or warning about the recording. |
| | [OutputFormat](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat) Defines the output format. |
| | [VideoEncoder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder) Defines the video encoding. |
| | [VideoSource](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoSource) Defines the video source. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_ERROR_SERVER_DIED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_ERROR_SERVER_DIED:kotlin.Int) Media server died. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_RECORDER_ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_ERROR_UNKNOWN:kotlin.Int) Unspecified media recorder error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_RECORDER_INFO_MAX_DURATION_REACHED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_MAX_DURATION_REACHED:kotlin.Int) A maximum duration had been setup and has now been reached. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_RECORDER_INFO_MAX_FILESIZE_APPROACHING](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_MAX_FILESIZE_APPROACHING:kotlin.Int) A maximum filesize had been setup and current recorded file size has reached 90% of the limit. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_RECORDER_INFO_MAX_FILESIZE_REACHED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_MAX_FILESIZE_REACHED:kotlin.Int) A maximum filesize had been setup and has now been reached. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_RECORDER_INFO_NEXT_OUTPUT_FILE_STARTED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_NEXT_OUTPUT_FILE_STARTED:kotlin.Int) A maximum filesize had been reached and MediaRecorder has switched output to a new file set by application #setNextOutputFile. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_RECORDER_INFO_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_UNKNOWN:kotlin.Int) Unspecified media recorder info. |

| Inherited constants ||
|---|---|
| From class [MicrophoneDirection](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_AWAY_FROM_USER](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_AWAY_FROM_USER:kotlin.Int) <br /> Optimize capture for audio coming from the side of the device pointing away from the user. In the typical case, a device with a single screen, screen-side camera/microphone and non-screen-side camera/microphone, this will be the non-screen side. For a different device geometry, it is the side for which the expectation is to be facing away from the user. This is the "taking a video of something else" case. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_EXTERNAL](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_EXTERNAL:kotlin.Int) <br /> Optimize capture for audio coming from an off-device microphone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_TOWARDS_USER](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_TOWARDS_USER:kotlin.Int) <br /> Optimize capture for audio coming from the side of the device facing the user. In the typical case, a device with a single screen, screen-side camera/microphone and non-screen-side camera/microphone, this will be the screen side (as in a "selfie"). For a different device geometry, it is the side for which the expectation is to be facing the user. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIC_DIRECTION_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_UNSPECIFIED:kotlin.Int) <br /> Don't do any directionality processing of the activated microphone(s). <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MediaRecorder())`()` Default constructor. |
| [MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MediaRecorder(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`)` Default constructor. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#addOnRoutingChangedListener(android.media.AudioRouting.OnRoutingChangedListener,%20android.os.Handler))`(`listener:` ` [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Adds an [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) to receive notifications of routing changes on this MediaRecorder. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MicrophoneInfo](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo)!\>! | [getActiveMicrophones](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#getActiveMicrophones())`()` Return A lists of [MicrophoneInfo](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo) representing the active microphones. |
| open [AudioRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration)? | [getActiveRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#getActiveRecordingConfiguration())`()` Returns the current active audio recording for this audio recorder. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSourceMax](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#getAudioSourceMax())`()` Gets the maximum value for audio sources. |
| open [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) | [getLogSessionId](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#getLogSessionId())`()` Returns the [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) for MediaRecorder. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxAmplitude](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#getMaxAmplitude())`()` Returns the maximum absolute amplitude that was sampled since the last call to this method. |
| open [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)! | [getMetrics](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#getMetrics())`()` Return Metrics data about the current Mediarecorder instance. |
| open [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)! | [getPreferredDevice](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#getPreferredDevice())`()` Returns the selected input device specified by [setPreferredDevice](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setPreferredDevice(android.media.AudioDeviceInfo)). |
| open [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)! | [getRoutedDevice](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#getRoutedDevice())`()` Returns an [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) identifying the current routing of this MediaRecorder Note: The query is only valid if the MediaRecorder is currently recording. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!\> | [getRoutedDevices](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#getRoutedDevices())`()` Returns a List of [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) identifying the current routing of this MediaRecorder. |
| open [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)! | [getSurface](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#getSurface())`()` Gets the surface to record from when using SURFACE video source. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrivacySensitive](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#isPrivacySensitive())`()` Returns whether this MediaRecorder is marked as privacy sensitive or not with regard to audio capture. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pause](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#pause())`()` Pauses recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [prepare](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#prepare())`()` Prepares the recorder to begin capturing and encoding data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#registerAudioRecordingCallback(java.util.concurrent.Executor,%20android.media.AudioManager.AudioRecordingCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `cb:` ` [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback)`)` Register a callback to be notified of audio capture changes via a [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#release())`()` Releases resources associated with this MediaRecorder object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#removeOnRoutingChangedListener(android.media.AudioRouting.OnRoutingChangedListener))`(`listener:` ` [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener)!`)` Removes an [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) which has been previously added to receive rerouting notifications. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#reset())`()` Restarts the MediaRecorder to its idle state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resume](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#resume())`()` Resumes recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAudioChannels](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setAudioChannels(kotlin.Int))`(`numChannels:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the number of audio channels for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAudioEncoder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setAudioEncoder(kotlin.Int))`(`audio_encoder:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the audio encoder to be used for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAudioEncodingBitRate](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setAudioEncodingBitRate(kotlin.Int))`(`bitRate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the audio encoding bit rate for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAudioProfile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setAudioProfile(android.media.EncoderProfiles.AudioProfile))`(`profile:` ` [EncoderProfiles.AudioProfile](https://developer.android.com/reference/kotlin/android/media/EncoderProfiles.AudioProfile)`)` Uses the settings from an AudioProfile for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAudioSamplingRate](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setAudioSamplingRate(kotlin.Int))`(`samplingRate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the audio sampling rate for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAudioSource](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setAudioSource(kotlin.Int))`(`audioSource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the audio source to be used for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCamera](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setCamera(android.hardware.Camera))`(`c:` ` [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera.html#)!`)` Sets a [android.hardware.Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera.html#) to use for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCaptureRate](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setCaptureRate(kotlin.Double))`(`fps:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Set video frame capture rate. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputSurface](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setInputSurface(android.view.Surface))`(`surface:` ` [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)`)` Configures the recorder to use a persistent surface when using SURFACE video source. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocation](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setLocation(kotlin.Float,%20kotlin.Float))`(`latitude:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `longitude:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set and store the geodata (latitude and longitude) in the output file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLogSessionId](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setLogSessionId(android.media.metrics.LogSessionId))`(`id:` ` [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId)`)` Sets the [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) for MediaRecorder. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxDuration](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setMaxDuration(kotlin.Int))`(`max_duration_ms:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum duration (in ms) of the recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxFileSize](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setMaxFileSize(kotlin.Long))`(`max_filesize_bytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the maximum filesize (in bytes) of the recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNextOutputFile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setNextOutputFile(java.io.File))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Sets the next output file to be used when the maximum filesize is reached on the prior output #setOutputFile or #setNextOutputFile). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNextOutputFile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setNextOutputFile(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`)` Sets the next output file descriptor to be used when the maximum filesize is reached on the prior output #setOutputFile or #setNextOutputFile). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnErrorListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOnErrorListener(android.media.MediaRecorder.OnErrorListener))`(`l:` ` [MediaRecorder.OnErrorListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnErrorListener)!`)` Register a callback to be invoked when an error occurs while recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOnInfoListener(android.media.MediaRecorder.OnInfoListener))`(`listener:` ` [MediaRecorder.OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnInfoListener)!`)` Register a callback to be invoked when an informational event occurs while recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrientationHint](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOrientationHint(kotlin.Int))`(`degrees:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the orientation hint for output video playback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutputFile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOutputFile(java.io.File))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Pass in the file object to be written. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutputFile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOutputFile(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`)` Pass in the file descriptor of the file to be written. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutputFile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOutputFile(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the path of the output file to be produced. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutputFormat](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOutputFormat(kotlin.Int))`(`output_format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the format of the output file produced during recording. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredDevice](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setPreferredDevice(android.media.AudioDeviceInfo))`(`deviceInfo:` ` [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!`)` Specifies an audio device (via an [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) object) to route the input from this MediaRecorder. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredMicrophoneDirection](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setPreferredMicrophoneDirection(kotlin.Int))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specifies the logical microphone (for processing). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredMicrophoneFieldDimension](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setPreferredMicrophoneFieldDimension(kotlin.Float))`(`zoom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Specifies the zoom factor (i.e. the field dimension) for the selected microphone (for processing). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreviewDisplay](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setPreviewDisplay(android.view.Surface))`(`sv:` ` [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)!`)` Sets a Surface to show a preview of recorded media (video). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPrivacySensitive](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setPrivacySensitive(kotlin.Boolean))`(`privacySensitive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Indicates that this capture request is privacy sensitive and that any concurrent capture is not permitted. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProfile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setProfile(android.media.CamcorderProfile))`(`profile:` ` [CamcorderProfile](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile)!`)` Uses the settings from a CamcorderProfile object for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVideoEncoder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoEncoder(kotlin.Int))`(`video_encoder:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the video encoder to be used for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVideoEncodingBitRate](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoEncodingBitRate(kotlin.Int))`(`bitRate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the video encoding bit rate for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVideoEncodingProfileLevel](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoEncodingProfileLevel(kotlin.Int,%20kotlin.Int))`(`profile:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the desired video encoding profile and level for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVideoFrameRate](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoFrameRate(kotlin.Int))`(`rate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the frame rate of the video to be captured. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVideoProfile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoProfile(android.media.EncoderProfiles.VideoProfile))`(`profile:` ` [EncoderProfiles.VideoProfile](https://developer.android.com/reference/kotlin/android/media/EncoderProfiles.VideoProfile)`)` Uses the settings from a VideoProfile object for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVideoSize](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoSize(kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the width and height of the video to be captured. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVideoSource](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoSource(kotlin.Int))`(`video_source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the video source to be used for recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#start())`()` Begins capturing and encoding data to the file specified with setOutputFile(). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#stop())`()` Stops recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#unregisterAudioRecordingCallback(android.media.AudioManager.AudioRecordingCallback))`(`cb:` ` [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback)`)` Unregister an audio recording callback previously registered with [registerAudioRecordingCallback(java.util.concurrent.Executor,android.media.AudioManager.AudioRecordingCallback)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#registerAudioRecordingCallback(java.util.concurrent.Executor,%20android.media.AudioManager.AudioRecordingCallback)). |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#finalize())`()` <br /> |

## Constants

### MEDIA_ERROR_SERVER_DIED

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_ERROR_SERVER_DIED: Int
```

Media server died. In this case, the application must release the MediaRecorder object and instantiate a new one. 

 Value: 100

**See Also**

- [android.media.MediaRecorder.OnErrorListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnErrorListener) 

### MEDIA_RECORDER_ERROR_UNKNOWN

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_RECORDER_ERROR_UNKNOWN: Int
```

Unspecified media recorder error. 

 Value: 1

**See Also**

- [android.media.MediaRecorder.OnErrorListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnErrorListener) 

### MEDIA_RECORDER_INFO_MAX_DURATION_REACHED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_RECORDER_INFO_MAX_DURATION_REACHED: Int
```

A maximum duration had been setup and has now been reached. 

 Value: 800

**See Also**

- [android.media.MediaRecorder.OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnInfoListener) 

### MEDIA_RECORDER_INFO_MAX_FILESIZE_APPROACHING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_RECORDER_INFO_MAX_FILESIZE_APPROACHING: Int
```

A maximum filesize had been setup and current recorded file size has reached 90% of the limit. This is sent once per file upon reaching/passing the 90% limit. To continue the recording, applicaiton should use #setNextOutputFile to set the next output file. Otherwise, recording will stop when reaching maximum file size. 

 Value: 802

**See Also**

- [android.media.MediaRecorder.OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnInfoListener) 

### MEDIA_RECORDER_INFO_MAX_FILESIZE_REACHED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_RECORDER_INFO_MAX_FILESIZE_REACHED: Int
```

A maximum filesize had been setup and has now been reached. Note: This event will not be sent if application already set next output file through #setNextOutputFile. 

 Value: 801

**See Also**

- [android.media.MediaRecorder.OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnInfoListener) 

### MEDIA_RECORDER_INFO_NEXT_OUTPUT_FILE_STARTED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_RECORDER_INFO_NEXT_OUTPUT_FILE_STARTED: Int
```

A maximum filesize had been reached and MediaRecorder has switched output to a new file set by application #setNextOutputFile. For best practice, application should use this event to keep track of whether the file previously set has been used or not. 

 Value: 803

**See Also**

- [android.media.MediaRecorder.OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnInfoListener) 

### MEDIA_RECORDER_INFO_UNKNOWN

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_RECORDER_INFO_UNKNOWN: Int
```

Unspecified media recorder info. 

 Value: 1

**See Also**

- [android.media.MediaRecorder.OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnInfoListener)

## Public constructors

### MediaRecorder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaRecorder()
```

**Deprecated:** *Use [MediaRecorder(android.content.Context)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MediaRecorder(android.content.Context))instead*

Default constructor. 

### MediaRecorder

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaRecorder(context: Context)
```

Default constructor.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):Context the recorder belongs to This value cannot be`null`. |

## Public methods

### addOnRoutingChangedListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addOnRoutingChangedListener(
    listener: AudioRouting.OnRoutingChangedListener!, 
    handler: Handler!
): Unit
```

Adds an [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) to receive notifications of routing changes on this MediaRecorder.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener)!:The [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) interface to receive notifications of rerouting events. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:Specifies the [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) object for the thread on which to execute the callback. If`null`, the handler on the main looper will be used. |

### getActiveMicrophones

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActiveMicrophones(): MutableList<MicrophoneInfo!>!
```

Return A lists of [MicrophoneInfo](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo) representing the active microphones. By querying channel mapping for each active microphone, developer can know how the microphone is used by each channels or a capture stream.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MicrophoneInfo](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo)!>! | a lists of [MicrophoneInfo](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo) representing the active microphones |

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

### getAudioSourceMax

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAudioSourceMax(): Int
```

Gets the maximum value for audio sources. 
**See Also**

- [android.media.MediaRecorder.AudioSource](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource) 

### getLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLogSessionId(): LogSessionId
```

Returns the [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) for MediaRecorder.

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) | the global ID for monitoring the MediaRecorder performance This value cannot be`null`. |

### getMaxAmplitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxAmplitude(): Int
```

Returns the maximum absolute amplitude that was sampled since the last call to this method. Call this only after the setAudioSource().

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum absolute amplitude measured since the last call, or 0 when called for the first time |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called before the audio source has been set. |

### getMetrics

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMetrics(): PersistableBundle!
```

Return Metrics data about the current Mediarecorder instance.

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)! | a [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) containing the set of attributes and values available for the media being generated by this instance of MediaRecorder. The attributes are descibed in [MetricsConstants](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.MetricsConstants). Additional vendor-specific fields may also be present in the return value. |

### getPreferredDevice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreferredDevice(): AudioDeviceInfo!
```

Returns the selected input device specified by [setPreferredDevice](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setPreferredDevice(android.media.AudioDeviceInfo)). Note that this is not guaranteed to correspond to the actual device being used for recording. 

### getRoutedDevice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoutedDevice(): AudioDeviceInfo!
```

Returns an [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) identifying the current routing of this MediaRecorder Note: The query is only valid if the MediaRecorder is currently recording. If the recorder is not recording, the returned device can be null or correspond to previously selected device when the recorder was last active. 

### getRoutedDevices

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoutedDevices(): MutableList<AudioDeviceInfo!>
```

Returns a List of [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) identifying the current routing of this MediaRecorder. Note: The query is only valid if the MediaRecorder is currently recording. If the recorder is not recording, the returned devices can be empty or correspond to previously selected devices when the recorder was last active.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!> | This value cannot be`null`. |

### getSurface

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSurface(): Surface!
```

Gets the surface to record from when using SURFACE video source.

May only be called after [prepare](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#prepare()). Frames rendered to the Surface before [start](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#start())will be discarded.

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called before [prepare](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#prepare()), after [stop](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#stop()), or is called when VideoSource is not set to SURFACE. |

**See Also**

- [android.media.MediaRecorder.VideoSource](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoSource) 

### isPrivacySensitive

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPrivacySensitive(): Boolean
```

Returns whether this MediaRecorder is marked as privacy sensitive or not with regard to audio capture.

See [setPrivacySensitive(boolean)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setPrivacySensitive(kotlin.Boolean))

<br />

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if privacy sensitive, false otherwise |

### pause

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pause(): Unit
```

Pauses recording. Call this after start(). You may resume recording with resume() without reconfiguration, as opposed to stop(). It does nothing if the recording is already paused. When the recording is paused and resumed, the resulting output would be as if nothing happend during paused period, immediately switching to the resumed scene.

| Exceptions ||
|-----------------------------------|------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called before start() or after stop() |

### prepare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun prepare(): Unit
```

Prepares the recorder to begin capturing and encoding data. This method must be called after setting up the desired audio and video sources, encoders, file format, etc., but before start().

| Exceptions ||
|-----------------------------------|------------------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called after start() or before setOutputFormat(). |
| `java.io.IOException` | if prepare fails otherwise. |

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

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Releases resources associated with this MediaRecorder object. It is good practice to call this method when you're done using the MediaRecorder. In particular, whenever an Activity of an application is paused (its onPause() method is called), or stopped (its onStop() method is called), this method should be invoked to release the MediaRecorder object, unless the application has a special need to keep the object around. In addition to unnecessary resources (such as memory and instances of codecs) being held, failure to call this method immediately if a MediaRecorder object is no longer needed may also lead to continuous battery consumption for mobile devices, and recording failure for other applications if no multiple instances of the same codec are supported on a device. Even if multiple instances of the same codec are supported, some performance degradation may be expected when unnecessary multiple instances are used at the same time. 

### removeOnRoutingChangedListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeOnRoutingChangedListener(listener: AudioRouting.OnRoutingChangedListener!): Unit
```

Removes an [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) which has been previously added to receive rerouting notifications.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener)!:The previously added [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) interface to remove. |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Restarts the MediaRecorder to its idle state. After calling this method, you will have to configure it again as if it had just been constructed. 

### resume

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resume(): Unit
```

Resumes recording. Call this after start(). It does nothing if the recording is not paused.

| Exceptions ||
|-----------------------------------|------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called before start() or after stop() |

**See Also**

- [android.media.MediaRecorder#pause](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#pause()) 

### setAudioChannels

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAudioChannels(numChannels: Int): Unit
```

Sets the number of audio channels for recording. Call this method before prepare(). Prepare() may perform additional checks on the parameter to make sure whether the specified number of audio channels are applicable.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numChannels` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of audio channels. Usually it is either 1 (mono) or 2 (stereo). |

### setAudioEncoder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAudioEncoder(audio_encoder: Int): Unit
```

Sets the audio encoder to be used for recording. If this method is not called, the output file will not contain an audio track. Call this after setOutputFormat() but before prepare().

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audio_encoder` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the audio encoder to use. Value is [android.media.MediaRecorder.AudioEncoder#DEFAULT](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioEncoder#DEFAULT:kotlin.Int), [android.media.MediaRecorder.AudioEncoder#AMR_NB](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioEncoder#AMR_NB:kotlin.Int), [android.media.MediaRecorder.AudioEncoder#AMR_WB](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioEncoder#AMR_WB:kotlin.Int), [android.media.MediaRecorder.AudioEncoder#AAC](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioEncoder#AAC:kotlin.Int), [android.media.MediaRecorder.AudioEncoder#HE_AAC](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioEncoder#HE_AAC:kotlin.Int), [android.media.MediaRecorder.AudioEncoder#AAC_ELD](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioEncoder#AAC_ELD:kotlin.Int), [android.media.MediaRecorder.AudioEncoder#VORBIS](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioEncoder#VORBIS:kotlin.Int), or [android.media.MediaRecorder.AudioEncoder#OPUS](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioEncoder#OPUS:kotlin.Int) |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called before setOutputFormat() or after prepare(). |

**See Also**

- [android.media.MediaRecorder.AudioEncoder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioEncoder) 

### setAudioEncodingBitRate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAudioEncodingBitRate(bitRate: Int): Unit
```

Sets the audio encoding bit rate for recording. Call this method before prepare(). Prepare() may perform additional checks on the parameter to make sure whether the specified bit rate is applicable, and sometimes the passed bitRate will be clipped internally to ensure the audio recording can proceed smoothly based on the capabilities of the platform.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `bitRate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the audio encoding bit rate in bits per second. |

### setAudioProfile

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAudioProfile(profile: EncoderProfiles.AudioProfile): Unit
```

Uses the settings from an AudioProfile for recording.

This method should be called after the video AND audio sources are set, and before setOutputFile().

This method can be used instead of [setProfile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setProfile(android.media.CamcorderProfile))when using EncoderProfiles.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `profile` | [EncoderProfiles.AudioProfile](https://developer.android.com/reference/kotlin/android/media/EncoderProfiles.AudioProfile):the AudioProfile to use This value cannot be`null`. |

**See Also**

- [android.media.EncoderProfiles](https://developer.android.com/reference/kotlin/android/media/EncoderProfiles)
- [android.media.CamcorderProfile#getAll](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#getAll(kotlin.String,%20kotlin.Int)) 

### setAudioSamplingRate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAudioSamplingRate(samplingRate: Int): Unit
```

Sets the audio sampling rate for recording. Call this method before prepare(). Prepare() may perform additional checks on the parameter to make sure whether the specified audio sampling rate is applicable. The sampling rate really depends on the format for the audio recording, as well as the capabilities of the platform. For instance, the sampling rate supported by AAC audio coding standard ranges from 8 to 96 kHz, the sampling rate supported by AMRNB is 8kHz, and the sampling rate supported by AMRWB is 16kHz. Please consult with the related audio coding standard for the supported audio sampling rate.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `samplingRate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the sampling rate for audio in samples per second. |

### setAudioSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAudioSource(audioSource: Int): Unit
```

Sets the audio source to be used for recording. If this method is not called, the output file will not contain an audio track. The source needs to be specified before setting recording-parameters or encoders. Call this only before setOutputFormat().

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioSource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the audio source to use Value is [android.media.MediaRecorder.AudioSource#DEFAULT](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#DEFAULT:kotlin.Int), [android.media.MediaRecorder.AudioSource#MIC](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#MIC:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_UPLINK](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_UPLINK:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_DOWNLINK](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_DOWNLINK:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_CALL](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_CALL:kotlin.Int), [android.media.MediaRecorder.AudioSource#CAMCORDER](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#CAMCORDER:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_RECOGNITION](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_RECOGNITION:kotlin.Int), [android.media.MediaRecorder.AudioSource#VOICE_COMMUNICATION](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_COMMUNICATION:kotlin.Int), [android.media.MediaRecorder.AudioSource#UNPROCESSED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#UNPROCESSED:kotlin.Int), or [android.media.MediaRecorder.AudioSource#VOICE_PERFORMANCE](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_PERFORMANCE:kotlin.Int) |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | if it is called after setOutputFormat() |

**See Also**

- [android.media.MediaRecorder.AudioSource](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource) 

### setCamera

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCamera(c: Camera!): Unit
```

**Deprecated:** *Use [getSurface](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#getSurface())and the [android.hardware.camera2](https://developer.android.com/reference/kotlin/android/hardware/camera2/package-summary.html) API instead.*

Sets a [android.hardware.Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera.html#) to use for recording.

Use this function to switch quickly between preview and capture mode without a teardown of the camera object. [android.hardware.Camera#unlock()](https://developer.android.com/reference/kotlin/android/hardware/Camera.html#unlock())should be called before this. Must call before [prepare](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#prepare()).

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------|
| `c` | [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera.html#)!:the Camera to use for recording |

### setCaptureRate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCaptureRate(fps: Double): Unit
```

Set video frame capture rate. This can be used to set a different video frame capture rate than the recorded video's playback rate. This method also sets the recording mode to time lapse. In time lapse video recording, only video is recorded. Audio related parameters are ignored when a time lapse recording session starts, if an application sets them.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fps` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):Rate at which frames should be captured in frames per second. The fps can go as low as desired. However the fastest fps will be limited by the hardware. For resolutions that can be captured by the video camera, the fastest fps can be computed using[android.hardware.Camera.Parameters#getPreviewFpsRange(int[])](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters.html#getPreviewFpsRange(kotlin.IntArray)). For higher resolutions the fastest fps may be more restrictive. Note that the recorder cannot guarantee that frames will be captured at the given rate due to camera/encoder limitations. However it tries to be as close as possible. |

### setInputSurface

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInputSurface(surface: Surface): Unit
```

Configures the recorder to use a persistent surface when using SURFACE video source.

May only be called before [prepare](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#prepare()). If called, [getSurface](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#getSurface())should not be used and will throw IllegalStateException. Frames rendered to the Surface before [start](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#start())will be discarded.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#):a persistent input surface created by [MediaCodec.createPersistentInputSurface](https://developer.android.com/reference/kotlin/android/media/MediaCodec#createPersistentInputSurface())This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called after [prepare](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#prepare())and before [stop](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#stop()). |
| `java.lang.IllegalArgumentException` | if the surface was not created by [MediaCodec.createPersistentInputSurface](https://developer.android.com/reference/kotlin/android/media/MediaCodec#createPersistentInputSurface()). |

**See Also**

- [android.media.MediaCodec#createPersistentInputSurface](https://developer.android.com/reference/kotlin/android/media/MediaCodec#createPersistentInputSurface())
- [android.media.MediaRecorder.VideoSource](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoSource) 

### setLocation

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLocation(
    latitude: Float, 
    longitude: Float
): Unit
```

Set and store the geodata (latitude and longitude) in the output file. This method should be called before prepare(). The geodata is stored in udta box if the output format is OutputFormat.THREE_GPP or OutputFormat.MPEG_4, and is ignored for other output formats. The geodata is stored according to ISO-6709 standard.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `latitude` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):latitude in degrees. Its value must be in the range \[-90, 90\]. |
| `longitude` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):longitude in degrees. Its value must be in the range \[-180, 180\]. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the given latitude or longitude is out of range. |

### setLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLogSessionId(id: LogSessionId): Unit
```

Sets the [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) for MediaRecorder.

The log session ID is a random 32-byte hexadecimal string that is used for monitoring the MediaRecorder performance.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId):the global ID for monitoring the MediaRecorder performance This value cannot be`null`. |

### setMaxDuration

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaxDuration(max_duration_ms: Int): Unit
```

Sets the maximum duration (in ms) of the recording session. Call this after setOutputFormat() but before prepare(). After recording reaches the specified duration, a notification will be sent to the [android.media.MediaRecorder.OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnInfoListener) with a "what" code of [MEDIA_RECORDER_INFO_MAX_DURATION_REACHED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_MAX_DURATION_REACHED:kotlin.Int) and recording will be stopped. Stopping happens asynchronously, there is no guarantee that the recorder will have stopped by the time the listener is notified.

When using MPEG-4 container ([setOutputFormat(int)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOutputFormat(kotlin.Int))with [OutputFormat.MPEG_4](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#MPEG_4:kotlin.Int)), it is recommended to set maximum duration that fits the use case. Setting a larger than required duration may result in a larger than needed output file because of space reserved for MOOV box expecting large movie data in this recording session. Unused space of MOOV box is turned into FREE box in the output file.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `max_duration_ms` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum duration in ms (if zero or negative, disables the duration limit) |

### setMaxFileSize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaxFileSize(max_filesize_bytes: Long): Unit
```

Sets the maximum filesize (in bytes) of the recording session. Call this after setOutputFormat() but before prepare(). After recording reaches the specified filesize, a notification will be sent to the [android.media.MediaRecorder.OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnInfoListener) with a "what" code of [MEDIA_RECORDER_INFO_MAX_FILESIZE_REACHED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_MAX_FILESIZE_REACHED:kotlin.Int) and recording will be stopped. Stopping happens asynchronously, there is no guarantee that the recorder will have stopped by the time the listener is notified.

When using MPEG-4 container ([setOutputFormat(int)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOutputFormat(kotlin.Int))with [OutputFormat.MPEG_4](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#MPEG_4:kotlin.Int)), it is recommended to set maximum filesize that fits the use case. Setting a larger than required filesize may result in a larger than needed output file because of space reserved for MOOV box expecting large movie data in this recording session. Unused space of MOOV box is turned into FREE box in the output file.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `max_filesize_bytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum filesize in bytes (if zero or negative, disables the limit) |

### setNextOutputFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNextOutputFile(file: File!): Unit
```

Sets the next output file to be used when the maximum filesize is reached on the prior output #setOutputFile or #setNextOutputFile). File should be seekable. After setting the next output file, application should not use the file until [stop](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#stop()). Application must call this after receiving on the [android.media.MediaRecorder.OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnInfoListener) a "what" code of [MEDIA_RECORDER_INFO_MAX_FILESIZE_APPROACHING](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_MAX_FILESIZE_APPROACHING:kotlin.Int) and before receiving a "what" code of [MEDIA_RECORDER_INFO_MAX_FILESIZE_REACHED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_MAX_FILESIZE_REACHED:kotlin.Int). The file is not used until switching to that output. Application will receive [MEDIA_RECORDER_INFO_NEXT_OUTPUT_FILE_STARTED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_NEXT_OUTPUT_FILE_STARTED:kotlin.Int) when the next output file is used. Application will not be able to set a new output file if the previous one has not been used. Application is responsible for cleaning up unused files after [stop](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#stop())is called.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:The file to use. |

| Exceptions ||
|-----------------------------------|---------------------------------------|
| `java.lang.IllegalStateException` | if it is called before prepare(). |
| `java.io.IOException` | if setNextOutputFile fails otherwise. |

### setNextOutputFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNextOutputFile(fd: FileDescriptor!): Unit
```

Sets the next output file descriptor to be used when the maximum filesize is reached on the prior output #setOutputFile or #setNextOutputFile). File descriptor must be seekable and writable. After setting the next output file, application should not use the file referenced by this file descriptor until [stop](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#stop()). It is the application's responsibility to close the file descriptor. It is safe to do so as soon as this call returns. Application must call this after receiving on the [android.media.MediaRecorder.OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnInfoListener) a "what" code of [MEDIA_RECORDER_INFO_MAX_FILESIZE_APPROACHING](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_MAX_FILESIZE_APPROACHING:kotlin.Int) and before receiving a "what" code of [MEDIA_RECORDER_INFO_MAX_FILESIZE_REACHED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_MAX_FILESIZE_REACHED:kotlin.Int). The file is not used until switching to that output. Application will receive [MEDIA_RECORDER_INFO_NEXT_OUTPUT_FILE_STARTED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#MEDIA_RECORDER_INFO_NEXT_OUTPUT_FILE_STARTED:kotlin.Int) when the next output file is used. Application will not be able to set a new output file if the previous one has not been used. Application is responsible for cleaning up unused files after [stop](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#stop())is called.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!:an open file descriptor to be written into. |

| Exceptions ||
|-----------------------------------|---------------------------------------|
| `java.lang.IllegalStateException` | if it is called before prepare(). |
| `java.io.IOException` | if setNextOutputFile fails otherwise. |

### setOnErrorListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnErrorListener(l: MediaRecorder.OnErrorListener!): Unit
```

Register a callback to be invoked when an error occurs while recording.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `l` | [MediaRecorder.OnErrorListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnErrorListener)!:the callback that will be run |

### setOnInfoListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnInfoListener(listener: MediaRecorder.OnInfoListener!): Unit
```

Register a callback to be invoked when an informational event occurs while recording.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaRecorder.OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OnInfoListener)!:the callback that will be run |

### setOrientationHint

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOrientationHint(degrees: Int): Unit
```

Sets the orientation hint for output video playback. This method should be called before prepare(). This method will not trigger the source video frame to rotate during video recording, but to add a composition matrix containing the rotation angle in the output video if the output format is OutputFormat.THREE_GPP or OutputFormat.MPEG_4 so that a video player can choose the proper orientation for playback. Note that some video players may choose to ignore the compostion matrix in a video during playback.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `degrees` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the angle to be rotated clockwise in degrees. The supported angles are 0, 90, 180, and 270 degrees. |

| Exceptions ||
|--------------------------------------|--------------------------------|
| `java.lang.IllegalArgumentException` | if the angle is not supported. |

### setOutputFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOutputFile(file: File!): Unit
```

Pass in the file object to be written. Call this after setOutputFormat() but before prepare(). File should be seekable. After setting the next output file, application should not use the file until [stop](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#stop()). Application is responsible for cleaning up unused files after [stop](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#stop())is called.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:the file object to be written into. |

### setOutputFile

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOutputFile(fd: FileDescriptor!): Unit
```

Pass in the file descriptor of the file to be written. Call this after setOutputFormat() but before prepare().

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!:an open file descriptor to be written into. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called before setOutputFormat() or after prepare() |

### setOutputFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOutputFile(path: String!): Unit
```

Sets the path of the output file to be produced. Call this after setOutputFormat() but before prepare().

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The pathname to use. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called before setOutputFormat() or after prepare() |

### setOutputFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOutputFormat(output_format: Int): Unit
```

Sets the format of the output file produced during recording. Call this after setAudioSource()/setVideoSource() but before prepare().

It is recommended to always use 3GP format when using the H.263 video encoder and AMR audio encoder. Using an MPEG-4 container format may confuse some desktop players.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `output_format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the output format to use. The output format needs to be specified before setting recording-parameters or encoders. Value is [android.media.MediaRecorder.OutputFormat#DEFAULT](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#DEFAULT:kotlin.Int), [android.media.MediaRecorder.OutputFormat#THREE_GPP](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#THREE_GPP:kotlin.Int), [android.media.MediaRecorder.OutputFormat#MPEG_4](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#MPEG_4:kotlin.Int), [android.media.MediaRecorder.OutputFormat#AMR_NB](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#AMR_NB:kotlin.Int), [android.media.MediaRecorder.OutputFormat#AMR_WB](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#AMR_WB:kotlin.Int), android.media.MediaRecorder.OutputFormat.AAC_ADIF, [android.media.MediaRecorder.OutputFormat#AAC_ADTS](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#AAC_ADTS:kotlin.Int), [android.media.MediaRecorder.OutputFormat#MPEG_2_TS](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#MPEG_2_TS:kotlin.Int), [android.media.MediaRecorder.OutputFormat#WEBM](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#WEBM:kotlin.Int), android.media.MediaRecorder.OutputFormat.HEIF, or [android.media.MediaRecorder.OutputFormat#OGG](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#OGG:kotlin.Int) |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called after prepare() or before setAudioSource()/setVideoSource(). |

**See Also**

- [android.media.MediaRecorder.OutputFormat](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat) 

### setPreferredDevice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferredDevice(deviceInfo: AudioDeviceInfo!): Boolean
```

Specifies an audio device (via an [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) object) to route the input from this MediaRecorder.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceInfo` | [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!:The [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) specifying the audio source. If deviceInfo is null, default routing is restored. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if succesful, false if the specified [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) is non-null and does not correspond to a valid audio input device. |

### setPreferredMicrophoneDirection

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferredMicrophoneDirection(direction: Int): Boolean
```

Specifies the logical microphone (for processing).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Direction constant. Value is [android.media.MicrophoneDirection#MIC_DIRECTION_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_UNSPECIFIED:kotlin.Int), [android.media.MicrophoneDirection#MIC_DIRECTION_TOWARDS_USER](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_TOWARDS_USER:kotlin.Int), [android.media.MicrophoneDirection#MIC_DIRECTION_AWAY_FROM_USER](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_AWAY_FROM_USER:kotlin.Int), or [android.media.MicrophoneDirection#MIC_DIRECTION_EXTERNAL](https://developer.android.com/reference/kotlin/android/media/MicrophoneDirection#MIC_DIRECTION_EXTERNAL:kotlin.Int) |

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

### setPreviewDisplay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreviewDisplay(sv: Surface!): Unit
```

Sets a Surface to show a preview of recorded media (video). Calls this before prepare() to make sure that the desirable preview display is set. If [setCamera(android.hardware.Camera)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setCamera(android.hardware.Camera))is used and the surface has been already set to the camera, application do not need to call this. If this is called with non-null surface, the preview surface of the camera will be replaced by the new surface. If this method is called with null surface or not called at all, media recorder will not change the preview surface of the camera.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------|
| `sv` | [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)!:the Surface to use for the preview |

**See Also**

- [android.hardware.Camera#setPreviewDisplay(android.view.SurfaceHolder)](https://developer.android.com/reference/kotlin/android/hardware/Camera.html#setPreviewDisplay(android.view.SurfaceHolder)) 

### setPrivacySensitive

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPrivacySensitive(privacySensitive: Boolean): Unit
```

Indicates that this capture request is privacy sensitive and that any concurrent capture is not permitted.

The default is not privacy sensitive except when the audio source set with [setAudioSource(int)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setAudioSource(kotlin.Int))is [AudioSource.VOICE_COMMUNICATION](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_COMMUNICATION:kotlin.Int) or [AudioSource.CAMCORDER](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#CAMCORDER:kotlin.Int).

Always takes precedence over default from audio source when set explicitly.

Using this API is only permitted when the audio source is one of:

- [AudioSource.MIC](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#MIC:kotlin.Int)
- [AudioSource.CAMCORDER](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#CAMCORDER:kotlin.Int)
- [AudioSource.VOICE_RECOGNITION](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_RECOGNITION:kotlin.Int)
- [AudioSource.VOICE_COMMUNICATION](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_COMMUNICATION:kotlin.Int)
- [AudioSource.UNPROCESSED](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#UNPROCESSED:kotlin.Int)
- [AudioSource.VOICE_PERFORMANCE](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioSource#VOICE_PERFORMANCE:kotlin.Int)

Invoking [prepare()](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#prepare())will throw an IOException if this condition is not met.

Must be called after [setAudioSource(int)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setAudioSource(kotlin.Int))and before [setOutputFormat(int)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOutputFormat(kotlin.Int)).

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `privacySensitive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if capture from this MediaRecorder must be marked as privacy sensitive, false otherwise. |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if called before [setAudioSource(int)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setAudioSource(kotlin.Int))or after [setOutputFormat(int)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setOutputFormat(kotlin.Int)) |

### setProfile

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProfile(profile: CamcorderProfile!): Unit
```

Uses the settings from a CamcorderProfile object for recording. This method should be called after the video AND audio sources are set, and before setOutputFile(). If a time lapse CamcorderProfile is used, audio related source or recording parameters are ignored.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------|
| `profile` | [CamcorderProfile](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile)!:the CamcorderProfile to use |

**See Also**

- [android.media.CamcorderProfile](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile) 

### setVideoEncoder

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVideoEncoder(video_encoder: Int): Unit
```

Sets the video encoder to be used for recording. If this method is not called, the output file will not contain an video track. Call this after setOutputFormat() and before prepare().

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `video_encoder` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the video encoder to use. Value is [android.media.MediaRecorder.VideoEncoder#DEFAULT](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder#DEFAULT:kotlin.Int), [android.media.MediaRecorder.VideoEncoder#H263](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder#H263:kotlin.Int), [android.media.MediaRecorder.VideoEncoder#H264](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder#H264:kotlin.Int), [android.media.MediaRecorder.VideoEncoder#MPEG_4_SP](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder#MPEG_4_SP:kotlin.Int), [android.media.MediaRecorder.VideoEncoder#VP8](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder#VP8:kotlin.Int), [android.media.MediaRecorder.VideoEncoder#HEVC](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder#HEVC:kotlin.Int), [android.media.MediaRecorder.VideoEncoder#VP9](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder#VP9:kotlin.Int), [android.media.MediaRecorder.VideoEncoder#DOLBY_VISION](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder#DOLBY_VISION:kotlin.Int), [android.media.MediaRecorder.VideoEncoder#AV1](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder#AV1:kotlin.Int), or [android.media.MediaRecorder.VideoEncoder#APV](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder#APV:kotlin.Int) |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called before setOutputFormat() or after prepare() |

**See Also**

- [android.media.MediaRecorder.VideoEncoder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder) 

### setVideoEncodingBitRate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVideoEncodingBitRate(bitRate: Int): Unit
```

Sets the video encoding bit rate for recording. Call this method before prepare(). Prepare() may perform additional checks on the parameter to make sure whether the specified bit rate is applicable, and sometimes the passed bitRate will be clipped internally to ensure the video recording can proceed smoothly based on the capabilities of the platform.

NB: the actual bitrate and other encoding characteristics may be affected by the minimum quality floor behavior introduced in [android.os.Build.VERSION_CODES#S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int). More detail on how and where this impacts video encoding can be found in the [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) page and looking for "quality floor" (near the top of the page).

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `bitRate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the video encoding bit rate in bits per second. |

### setVideoEncodingProfileLevel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVideoEncodingProfileLevel(
    profile: Int, 
    level: Int
): Unit
```

Sets the desired video encoding profile and level for recording. The profile and level must be valid for the video encoder set by [setVideoEncoder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoEncoder(kotlin.Int)). This method can called before or after [setVideoEncoder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoEncoder(kotlin.Int))but it must be called before [prepare](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#prepare()).`prepare()`may perform additional checks on the parameter to make sure that the specified profile and level are applicable, and sometimes the passed profile or level will be discarded due to codec capablity or to ensure the video recording can proceed smoothly based on the capabilities of the platform. 
Application can also use the [MediaCodecInfo.CodecCapabilities.profileLevels](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#profileLevels:kotlin.Array) to query applicable combination of profile and level for the corresponding format. Note that the requested profile/level may not be supported by the codec that is actually being used by this MediaRecorder instance.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `profile` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):declared in [MediaCodecInfo.CodecProfileLevel](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecProfileLevel). |
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):declared in [MediaCodecInfo.CodecProfileLevel](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecProfileLevel). |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.lang.IllegalArgumentException` | when an invalid profile or level value is used. |

### setVideoFrameRate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVideoFrameRate(rate: Int): Unit
```

Sets the frame rate of the video to be captured. Must be called after setVideoSource(). Call this after setOutputFormat() but before prepare().

NOTE: On some devices that have auto-frame rate, this sets the maximum frame rate, not a constant frame rate. Actual frame rate will vary according to lighting conditions.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------|
| `rate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of frames per second of video to capture |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called after prepare() or before setOutputFormat(). |

### setVideoProfile

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVideoProfile(profile: EncoderProfiles.VideoProfile): Unit
```

Uses the settings from a VideoProfile object for recording.

This method should be called after the video AND audio sources are set, and before setOutputFile().

This method can be used instead of [setProfile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setProfile(android.media.CamcorderProfile))when using EncoderProfiles.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `profile` | [EncoderProfiles.VideoProfile](https://developer.android.com/reference/kotlin/android/media/EncoderProfiles.VideoProfile):the VideoProfile to use This value cannot be`null`. |

**See Also**

- [android.media.EncoderProfiles](https://developer.android.com/reference/kotlin/android/media/EncoderProfiles)
- [android.media.CamcorderProfile#getAll](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#getAll(kotlin.String,%20kotlin.Int)) 

### setVideoSize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVideoSize(
    width: Int, 
    height: Int
): Unit
```

Sets the width and height of the video to be captured. Must be called after setVideoSource(). Call this after setOutputFormat() but before prepare().

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the width of the video to be captured |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the height of the video to be captured |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called after prepare() or before setOutputFormat() |

### setVideoSource

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVideoSource(video_source: Int): Unit
```

Sets the video source to be used for recording. If this method is not called, the output file will not contain an video track. The source needs to be specified before setting recording-parameters or encoders. Call this only before setOutputFormat().

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------|
| `video_source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the video source to use |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | if it is called after setOutputFormat() |

**See Also**

- [android.media.MediaRecorder.VideoSource](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoSource) 

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun start(): Unit
```

Begins capturing and encoding data to the file specified with setOutputFile(). Call this after prepare().

Since API level 13, if applications set a camera via [setCamera(android.hardware.Camera)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setCamera(android.hardware.Camera)), the apps can use the camera after this method call. The apps do not need to lock the camera again. However, if this method fails, the apps should still lock the camera back. The apps should not start another recording session during recording.

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if it is called before prepare() or when the camera is already in use by another app. |

### stop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stop(): Unit
```

Stops recording. Call this after start(). Once recording is stopped, you will have to configure it again as if it has just been constructed. Note that a RuntimeException is intentionally thrown to the application, if no valid audio/video data has been received when stop() is called. This happens if stop() is called immediately after start(). The failure lets the application take action accordingly to clean up the output file (delete the output file, for instance), since the output file is not properly constructed when this happens.

| Exceptions ||
|-----------------------------------|--------------------------------|
| `java.lang.IllegalStateException` | if it is called before start() |

### unregisterAudioRecordingCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterAudioRecordingCallback(cb: AudioManager.AudioRecordingCallback): Unit
```

Unregister an audio recording callback previously registered with [registerAudioRecordingCallback(java.util.concurrent.Executor,android.media.AudioManager.AudioRecordingCallback)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#registerAudioRecordingCallback(java.util.concurrent.Executor,%20android.media.AudioManager.AudioRecordingCallback)).

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback):non-null callback to unregister |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
