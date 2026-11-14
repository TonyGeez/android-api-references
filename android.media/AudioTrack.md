Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioTrack

```
open class AudioTrack : AudioRouting, VolumeAutomation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioTrack](AudioTrack.md) |

The AudioTrack class manages and plays a single audio resource for Java applications. It allows streaming of PCM audio buffers to the audio sink for playback. This is achieved by "pushing" the data to the AudioTrack object using one of the write, write, and write methods.

An AudioTrack instance can operate under two modes: static or streaming. 
In Streaming mode, the application writes a continuous stream of data to the AudioTrack, using one of the `write()` methods. These are blocking and return when the data has been transferred from the Java layer to the native layer and queued for playback. The streaming mode is most useful when playing blocks of audio data that for instance are:

- too big to fit in memory because of the duration of the sound to play,
- too big to fit in memory because of the characteristics of the audio data (high sampling rate, bits per sample ...)
- received or generated while previously queued audio is playing.

The static mode should be chosen when dealing with short sounds that fit in memory and that need to be played with the smallest latency possible. The static mode will therefore be preferred for UI and game sounds that are played often, and with the smallest overhead possible.

Upon creation, an AudioTrack object initializes its associated audio buffer. The size of this buffer, specified during the construction, determines how long an AudioTrack can play before running out of data. 
For an AudioTrack using the static mode, this size is the maximum size of the sound that can be played from it. 
For the streaming mode, data will be written to the audio sink in chunks of sizes less than or equal to the total buffer size. AudioTrack is not final and thus permits subclasses, but such use is not recommended.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/media/AudioTrack.Builder` Builder class for AudioTrack objects. |
| | `https://developer.android.com/reference/kotlin/android/media/AudioTrack.MetricsConstants` <br /> |
| abstract | `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnCodecFormatChangedListener` Interface definition for a listener for codec format changes. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnPlaybackPositionUpdateListener` Interface definition for a callback to be invoked when the playback head position of an AudioTrack has reached a notification marker or has increased by a certain period. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnRoutingChangedListener` Defines the interface by which applications can receive notifications of routing changes for the associated AudioTrack. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/AudioTrack.StreamEventCallback` Abstract class to receive event notifications about the stream playback in offloaded mode. |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_LL:kotlin.Int` This mode indicates that a stereo stream should be presented with the left audio channel replicated into the right audio channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_LR:kotlin.Int` This mode indicates that a stereo stream should be presented with the left and right audio channels blended together and delivered to both channels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_OFF:kotlin.Int` This mode disables any Dual Mono presentation effect. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_RR:kotlin.Int` This mode indicates that a stereo stream should be presented with the right audio channel replicated into the left audio channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_METADATA_TYPE_DVB_AD_DESCRIPTOR:kotlin.Int` Encapsulation metadata type for DVB AD descriptor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_METADATA_TYPE_FRAMEWORK_TUNER:kotlin.Int` Encapsulation metadata type for framework tuner information. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_METADATA_TYPE_SUPPLEMENTARY_AUDIO_PLACEMENT:kotlin.Int` Encapsulation metadata type for placement of supplementary audio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_MODE_ELEMENTARY_STREAM:kotlin.Int` This mode indicates metadata encapsulation with an elementary stream payload. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_MODE_NONE:kotlin.Int` This mode indicates no metadata encapsulation, which is the default mode for sending audio data through `AudioTrack`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR:kotlin.Int` Denotes a generic operation failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` Denotes a failure due to the use of an invalid value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_DEAD_OBJECT:kotlin.Int` An error code indicating that the object reporting it is no longer valid and needs to be recreated. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` Denotes a failure due to the improper use of a method. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#FLUSH_FROM_ACCURACY_BEST_EFFORT:kotlin.Int` Accuracy mode for flushWrittenFramesFromPosition to indicate the framework will flush the data as close as possible, but not below, to the requested position. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#FLUSH_FROM_ACCURACY_EXACT:kotlin.Int` Accuracy mode for flushWrittenFramesFromPosition to indicate the AudioTrack must be flushed from the requested position. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#FLUSH_WRITTEN_FRAMES_SUPPORTED:kotlin.Int` Constant flag value to indicate flushWrittenFramesFromPosition is supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int` Creation mode where audio data is transferred from Java to the native layer only once before the audio starts playing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int` Creation mode where audio data is streamed from Java to the native layer as the audio is playing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PERFORMANCE_MODE_LOW_LATENCY:kotlin.Int` Low latency performance mode for an AudioTrack. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PERFORMANCE_MODE_NONE:kotlin.Int` Default performance mode for an AudioTrack. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PERFORMANCE_MODE_POWER_SAVING:kotlin.Int` Power saving performance mode for an AudioTrack. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PLAYSTATE_PAUSED:kotlin.Int` indicates AudioTrack state is paused |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PLAYSTATE_PLAYING:kotlin.Int` indicates AudioTrack state is playing |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PLAYSTATE_STOPPED:kotlin.Int` indicates AudioTrack state is stopped |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#STATE_INITIALIZED:kotlin.Int` State of an AudioTrack that is ready to be used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#STATE_NO_STATIC_DATA:kotlin.Int` State of a successfully initialized AudioTrack that uses static data, but that hasn't received that data yet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#STATE_UNINITIALIZED:kotlin.Int` State of an AudioTrack that was not successfully initialized upon creation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUCCESS:kotlin.Int` Denotes a successful operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUPPLEMENTARY_AUDIO_PLACEMENT_LEFT:kotlin.Int` Supplementary audio placement left. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUPPLEMENTARY_AUDIO_PLACEMENT_NORMAL:kotlin.Int` Supplementary audio placement normal. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUPPLEMENTARY_AUDIO_PLACEMENT_RIGHT:kotlin.Int` Supplementary audio placement right. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int` The write mode indicating the write operation will block until all data has been written, to be used as the actual value of the writeMode parameter in write, write, write, write, and write. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int` The write mode indicating the write operation will return immediately after queuing as much audio data for playback as possible without blocking, to be used as the actual value of the writeMode parameter in write, write, write, write, and write. |
| --- | --- |

| Public constructors ||
|---|---|
| AudioTrack Class constructor with AudioAttributes and AudioFormat. |
| AudioTrack Class constructor. |
| AudioTrack Class constructor with audio session. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnCodecFormatChangedListener Adds an `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnCodecFormatChangedListener` to receive notifications of codec format change events on this `AudioTrack`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnRoutingChangedListener Adds an `https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener` to receive notifications of routing changes on this AudioTrack. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnRoutingChangedListener Adds an `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnRoutingChangedListener` to receive notifications of routing changes on this AudioTrack. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | attachAuxEffect Attaches an auxiliary effect to the audio track. |
| open [VolumeShaper](VolumeShaper.md) | createVolumeShaper Returns a VolumeShaper object that can be used modify the volume envelope of the player or track. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | flush Flushes the audio data currently queued for playback. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | flushWrittenFramesFromPosition Flush all data from the given position. |
| open [AudioAttributes](AudioAttributes.md) | getAudioAttributes Returns the AudioAttributes used in configuration. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getAudioDescriptionMixLeveldB Returns the Audio Description mix level in dB. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAudioFormat Returns the configured audio data encoding. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAudioSessionId Returns the audio session ID. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getBufferCapacityInFrames Returns the maximum size of the `AudioTrack` buffer in frames. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getBufferSizeInFrames Returns the effective size of the `AudioTrack` buffer that the application writes to. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getChannelConfiguration Returns the configured channel position mask. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getChannelCount Returns the configured number of channels. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getCodecProvenance Returns the codec provenance of the `AudioTrack` specified at the time of configuration. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDualMonoMode Returns the Dual Mono mode presentation setting. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getFlushWrittenFramesFromPositionSupport Returns a bit mask representing the current feature support for flushWrittenFramesFromPosition for the AudioTrack in offload mode that is created with the given AudioFormat and AudioAttributes. |
| --- | --- |
| open [AudioFormat](AudioFormat.md) | getFormat Returns the configured `AudioTrack` format. |
| open [LogSessionId](../android.media.metrics/LogSessionId.md) | getLogSessionId Returns the LogSessionId. |
| open static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getMaxVolume Returns the maximum gain value, which is greater than or equal to 1. |
| --- | --- |
| open [PersistableBundle](../android.os/PersistableBundle.md)! | getMetrics Return Metrics data about the current AudioTrack instance. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMinBufferSize Returns the estimated minimum buffer size required for an AudioTrack object to be created in the `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int` mode. |
| open static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getMinVolume Returns the minimum gain value, which is the constant 0. |
| --- | --- |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNativeOutputSampleRate Returns the output sample rate in Hz for the specified stream type. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNotificationMarkerPosition Returns marker position expressed in frames. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getOffloadDelay Return the decoder delay of an offloaded track, expressed in frames, previously set with setOffloadDelayPadding, or 0 if it was never modified. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getOffloadPadding Return the decoder padding of an offloaded track, expressed in frames, previously set with setOffloadDelayPadding, or 0 if it was never modified. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPerformanceMode Returns the current performance mode of the AudioTrack. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPlayState Returns the playback state of the AudioTrack instance. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPlaybackHeadPosition Returns the playback head position expressed in frames. |
| open [PlaybackParams](PlaybackParams.md) | getPlaybackParams Returns the current playback parameters. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPlaybackRate Returns the current playback sample rate rate in Hz. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPositionNotificationPeriod Returns the notification update period expressed in frames. |
| open [AudioDeviceInfo](AudioDeviceInfo.md)! | getPreferredDevice Returns the selected output specified by setPreferredDevice. |
| open [AudioDeviceInfo](AudioDeviceInfo.md)! | getRoutedDevice Returns an AudioDeviceInfo identifying the current routing of this AudioTrack. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioDeviceInfo](AudioDeviceInfo.md)!\> | getRoutedDevices Returns a List of AudioDeviceInfo identifying the current routing of this AudioTrack. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSampleRate Returns the configured audio source sample rate in Hz. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getStartThresholdInFrames Returns the streaming start threshold of the `AudioTrack`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getState Returns the state of the AudioTrack instance. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getStreamType Returns the volume stream type of this AudioTrack. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getTimestamp Poll for a timestamp on demand. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getUnderrunCount Returns the number of underrun occurrences in the application-level write buffer since the AudioTrack was created. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getWrittenFramesCount Returns the number of audio frames written to a `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int` AudioTrack. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDirectPlaybackSupported Returns whether direct playback of an audio format with the provided attributes is currently supported on the system. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isOffloadedPlayback Returns whether the track was built with setOffloadedPlayback set to `true`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | pause Pauses the playback of the audio data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | play Starts playing an AudioTrack. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerStreamEventCallback Registers a callback for the notification of stream events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | release Releases the native AudioTrack resources. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | reloadStaticData Sets the playback head position within the static buffer to zero, that is it rewinds to start of static buffer. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnCodecFormatChangedListener Removes an `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnCodecFormatChangedListener` which has been previously added to receive codec format change events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnRoutingChangedListener Removes an `https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener` which has been previously added to receive rerouting notifications. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnRoutingChangedListener Removes an `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnRoutingChangedListener` which has been previously added to receive rerouting notifications. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setAudioDescriptionMixLeveldB Sets the Audio Description mix level in dB. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | setAuxEffectSendLevel Sets the send level of the audio track to the attached auxiliary effect attachAuxEffect. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | setBufferSizeInFrames Limits the effective size of the `AudioTrack` buffer that the application writes to. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setDualMonoMode Sets the Dual Mono mode presentation on the output device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLogSessionId Sets a LogSessionId instance to this AudioTrack for metrics collection. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | setLoopPoints Sets the loop points and the loop count. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | setNotificationMarkerPosition Sets the position of the notification marker. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOffloadDelayPadding Configures the delay and padding values for the current compressed stream playing in offload mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOffloadEndOfStream Declares that the last write() operation on this track provided the last buffer of this stream. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | setPlaybackHeadPosition Sets the playback head position within the static buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPlaybackParams Sets the playback parameters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPlaybackPositionUpdateListener Sets the listener the AudioTrack notifies when a previously set marker is reached or for each periodic playback head position update. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPlaybackPositionUpdateListener Sets the listener the AudioTrack notifies when a previously set marker is reached or for each periodic playback head position update. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | setPlaybackRate Sets the playback sample rate for this track. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | setPositionNotificationPeriod Sets the period for the periodic notification event. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setPreferredDevice Specifies an audio device (via an AudioDeviceInfo object) to route the output from this AudioTrack. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | setPresentation Sets the audio presentation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | setStartThresholdInFrames Sets the streaming start threshold for an `AudioTrack`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | setStereoVolume Sets the specified left and right output gain values on the AudioTrack. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | setVolume Sets the specified output gain value on all channels of this track. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | stop Stops playing the audio data. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterStreamEventCallback Unregisters the callback for notification of stream events, previously registered with registerStreamEventCallback. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | write Writes the audio data to the audio sink for playback (streaming mode), or copies audio data for later playback (static buffer mode). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | write Writes the audio data to the audio sink for playback (streaming mode), or copies audio data for later playback (static buffer mode). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | write Writes the audio data to the audio sink for playback (streaming mode), or copies audio data for later playback (static buffer mode). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | write Writes the audio data to the audio sink for playback (streaming mode), or copies audio data for later playback (static buffer mode). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | write Writes the audio data to the audio sink for playback in streaming mode on a HW_AV_SYNC track. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | write Writes the audio data to the audio sink for playback (streaming mode), or copies audio data for later playback (static buffer mode). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | write Writes the audio data to the audio sink for playback (streaming mode), or copies audio data for later playback (static buffer mode). |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNativeFrameCount Returns the frame count of the native `AudioTrack` buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setState Sets the initialization state of the instance. |
| --- | --- |

## Constants

### DUAL_MONO_MODE_LL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DUAL_MONO_MODE_LL: Int
```

This mode indicates that a stereo stream should be presented with the left audio channel replicated into the right audio channel. Behavior for non-stereo streams is implementation defined. A suggested guideline is that all channels with left-right stereo symmetry will have the left channel position replicated into the right channel position. The center channels (with no left/right symmetry) or unbalanced channels are left alone. The Dual Mono effect occurs before volume scaling.

 Value: 2

### DUAL_MONO_MODE_LR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DUAL_MONO_MODE_LR: Int
```

This mode indicates that a stereo stream should be presented with the left and right audio channels blended together and delivered to both channels. Behavior for non-stereo streams is implementation defined. A suggested guideline is that the left-right stereo symmetric channels are pairwise blended; the other channels such as center are left alone. The Dual Mono effect occurs before volume scaling.

 Value: 1

### DUAL_MONO_MODE_OFF

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DUAL_MONO_MODE_OFF: Int
```

This mode disables any Dual Mono presentation effect.

 Value: 0

### DUAL_MONO_MODE_RR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DUAL_MONO_MODE_RR: Int
```

This mode indicates that a stereo stream should be presented with the right audio channel replicated into the left audio channel. Behavior for non-stereo streams is implementation defined. A suggested guideline is that all channels with left-right stereo symmetry will have the right channel position replicated into the left channel position. The center channels (with no left/right symmetry) or unbalanced channels are left alone. The Dual Mono effect occurs before volume scaling.

 Value: 3

### ENCAPSULATION_METADATA_TYPE_DVB_AD_DESCRIPTOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCAPSULATION_METADATA_TYPE_DVB_AD_DESCRIPTOR: Int
```

Encapsulation metadata type for DVB AD descriptor. This metadata is formatted per ETSI TS 101 154 Table E.1: AD_descriptor.

 Value: 2

### ENCAPSULATION_METADATA_TYPE_FRAMEWORK_TUNER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCAPSULATION_METADATA_TYPE_FRAMEWORK_TUNER: Int
```

Encapsulation metadata type for framework tuner information. Refer to the Android Media TV Tuner API for details.

 Value: 1

### ENCAPSULATION_METADATA_TYPE_SUPPLEMENTARY_AUDIO_PLACEMENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCAPSULATION_METADATA_TYPE_SUPPLEMENTARY_AUDIO_PLACEMENT: Int
```

Encapsulation metadata type for placement of supplementary audio. A 32 bit integer constant, one of `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUPPLEMENTARY_AUDIO_PLACEMENT_NORMAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUPPLEMENTARY_AUDIO_PLACEMENT_LEFT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUPPLEMENTARY_AUDIO_PLACEMENT_RIGHT:kotlin.Int`.

 Value: 3

### ENCAPSULATION_MODE_ELEMENTARY_STREAM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCAPSULATION_MODE_ELEMENTARY_STREAM: Int
```

This mode indicates metadata encapsulation with an elementary stream payload. Both compressed and PCM format is allowed.

 Value: 1

### ENCAPSULATION_MODE_NONE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCAPSULATION_MODE_NONE: Int
```

This mode indicates no metadata encapsulation, which is the default mode for sending audio data through `AudioTrack`.

 Value: 0

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

### FLUSH_FROM_ACCURACY_BEST_EFFORT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLUSH_FROM_ACCURACY_BEST_EFFORT: Int
```

Accuracy mode for flushWrittenFramesFromPosition to indicate the framework will flush the data as close as possible, but not below, to the requested position.

 Value: 0

**See Also**

- flushWrittenFramesFromPosition

### FLUSH_FROM_ACCURACY_EXACT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLUSH_FROM_ACCURACY_EXACT: Int
```

Accuracy mode for flushWrittenFramesFromPosition to indicate the AudioTrack must be flushed from the requested position. If it is not possible to flush from the requested position, the AudioTrack must not be flushed.

 Value: 1

**See Also**

- flushWrittenFramesFromPosition

### FLUSH_WRITTEN_FRAMES_SUPPORTED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLUSH_WRITTEN_FRAMES_SUPPORTED: Int
```

Constant flag value to indicate flushWrittenFramesFromPosition is supported.

 Value: 1

**See Also**

- flushWrittenFramesFromPosition
- getFlushWrittenFramesFromPositionSupport

### MODE_STATIC

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_STATIC: Int
```

Creation mode where audio data is transferred from Java to the native layer only once before the audio starts playing.

 Value: 0

### MODE_STREAM

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_STREAM: Int
```

Creation mode where audio data is streamed from Java to the native layer as the audio is playing.

 Value: 1

### PERFORMANCE_MODE_LOW_LATENCY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERFORMANCE_MODE_LOW_LATENCY: Int
```

Low latency performance mode for an AudioTrack. If the device supports it, this mode enables a lower latency path through to the audio output sink. Effects may no longer work with such an `AudioTrack` and the sample rate must match that of the output sink.

Applications should be aware that low latency requires careful buffer management, with smaller chunks of audio data written by each `write()` call.

If this flag is used without specifying a `bufferSizeInBytes` then the `AudioTrack`'s actual buffer size may be too small. It is recommended that a fairly large buffer should be specified when the `AudioTrack` is created. Then the actual size can be reduced by calling setBufferSizeInFrames. The buffer size can be optimized by lowering it after each `write()` call until the audio glitches, which is detected by calling getUnderrunCount. Then the buffer size can be increased until there are no glitches. This tuning step should be done while playing silence. This technique provides a compromise between latency and glitch rate.

 Value: 1

### PERFORMANCE_MODE_NONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERFORMANCE_MODE_NONE: Int
```

Default performance mode for an AudioTrack.

 Value: 0

### PERFORMANCE_MODE_POWER_SAVING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERFORMANCE_MODE_POWER_SAVING: Int
```

Power saving performance mode for an AudioTrack. If the device supports it, this mode will enable a lower power path to the audio output sink. In addition, this lower power path typically will have deeper internal buffers and better underrun resistance, with a tradeoff of higher latency.

In this mode, applications should attempt to use a larger buffer size and deliver larger chunks of audio data per `write()` call. Use getBufferSizeInFrames to determine the actual buffer size of the `AudioTrack` as it may have increased to accommodate a deeper buffer.

 Value: 2

### PLAYSTATE_PAUSED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PLAYSTATE_PAUSED: Int
```

indicates AudioTrack state is paused

 Value: 2

### PLAYSTATE_PLAYING

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PLAYSTATE_PLAYING: Int
```

indicates AudioTrack state is playing

 Value: 3

### PLAYSTATE_STOPPED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PLAYSTATE_STOPPED: Int
```

indicates AudioTrack state is stopped

 Value: 1

### STATE_INITIALIZED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_INITIALIZED: Int
```

State of an AudioTrack that is ready to be used.

 Value: 1

### STATE_NO_STATIC_DATA

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_NO_STATIC_DATA: Int
```

State of a successfully initialized AudioTrack that uses static data, but that hasn't received that data yet.

 Value: 2

### STATE_UNINITIALIZED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_UNINITIALIZED: Int
```

State of an AudioTrack that was not successfully initialized upon creation.

 Value: 0

### SUCCESS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUCCESS: Int
```

Denotes a successful operation.

 Value: 0

### SUPPLEMENTARY_AUDIO_PLACEMENT_LEFT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUPPLEMENTARY_AUDIO_PLACEMENT_LEFT: Int
```

Supplementary audio placement left.

 Value: 1

### SUPPLEMENTARY_AUDIO_PLACEMENT_NORMAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUPPLEMENTARY_AUDIO_PLACEMENT_NORMAL: Int
```

Supplementary audio placement normal.

 Value: 0

### SUPPLEMENTARY_AUDIO_PLACEMENT_RIGHT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUPPLEMENTARY_AUDIO_PLACEMENT_RIGHT: Int
```

Supplementary audio placement right.

 Value: 2

### WRITE_BLOCKING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WRITE_BLOCKING: Int
```

The write mode indicating the write operation will block until all data has been written, to be used as the actual value of the writeMode parameter in write, write, write, write, and write.

 Value: 0

### WRITE_NON_BLOCKING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WRITE_NON_BLOCKING: Int
```

The write mode indicating the write operation will return immediately after queuing as much audio data for playback as possible without blocking, to be used as the actual value of the writeMode parameter in write, write, write, write, and write.

 Value: 1

## Public constructors

### AudioTrack

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AudioTrack(
    attributes: AudioAttributes!, 
    format: AudioFormat!, 
    bufferSizeInBytes: Int, 
    mode: Int, 
    sessionId: Int)
```

Class constructor with AudioAttributes and AudioFormat.

| Parameters ||
|---|---|
| `attributes` | [AudioAttributes](AudioAttributes.md)!: a non-null AudioAttributes instance. |
| `format` | [AudioFormat](AudioFormat.md)!: a non-null AudioFormat instance describing the format of the data that will be played through this AudioTrack. See `https://developer.android.com/reference/kotlin/android/media/AudioFormat.Builder` for configuring the audio format parameters such as encoding, channel mask and sample rate. |
| `bufferSizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the total size (in bytes) of the internal buffer where audio data is read from for playback. This should be a nonzero multiple of the frame size in bytes. If the track's creation mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int`, this is the maximum length sample, or audio clip, that can be played by this instance. If the track's creation mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int`, this should be the desired buffer size for the `AudioTrack` to satisfy the application's latency requirements. If `bufferSizeInBytes` is less than the minimum buffer size for the output sink, it is increased to the minimum buffer size. The method getBufferSizeInFrames returns the actual size in frames of the buffer created, which determines the minimum frequency to write to the streaming `AudioTrack` to avoid underrun. See getMinBufferSize to determine the estimated minimum buffer size for an AudioTrack instance in streaming mode. |
| --- | --- |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): streaming or static buffer. See `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int`. |
| `sessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): ID of audio session the AudioTrack must be attached to, or `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIO_SESSION_ID_GENERATE:kotlin.Int` if the session isn't known at construction time. See also generateAudioSessionId to obtain a session ID before construction. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |

### AudioTrack

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AudioTrack(
    streamType: Int, 
    sampleRateInHz: Int, 
    channelConfig: Int, 
    audioFormat: Int, 
    bufferSizeInBytes: Int, 
    mode: Int)
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/media/AudioTrack.Builder` or AudioTrack to specify the AudioAttributes instead of the stream type which is only for volume control.*

Class constructor.

| Parameters ||
|---|---|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the type of the audio stream. See `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_VOICE_CALL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_SYSTEM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_RING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_MUSIC:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ALARM:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_NOTIFICATION:kotlin.Int`. |
| `sampleRateInHz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial source sample rate expressed in Hz. `https://developer.android.com/reference/kotlin/android/media/AudioFormat#SAMPLE_RATE_UNSPECIFIED:kotlin.Int` means to use a route-dependent value which is usually the sample rate of the sink. getSampleRate can be used to retrieve the actual sample rate chosen. |
| `channelConfig` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): describes the configuration of the audio channels. See `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_MONO:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_STEREO:kotlin.Int` |
| --- | --- |
| `audioFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the format in which the audio data is represented. See `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int`. |
| `bufferSizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the total size (in bytes) of the internal buffer where audio data is read from for playback. This should be a nonzero multiple of the frame size in bytes. If the track's creation mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int`, this is the maximum length sample, or audio clip, that can be played by this instance. If the track's creation mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int`, this should be the desired buffer size for the `AudioTrack` to satisfy the application's latency requirements. If `bufferSizeInBytes` is less than the minimum buffer size for the output sink, it is increased to the minimum buffer size. The method getBufferSizeInFrames returns the actual size in frames of the buffer created, which determines the minimum frequency to write to the streaming `AudioTrack` to avoid underrun. See getMinBufferSize to determine the estimated minimum buffer size for an AudioTrack instance in streaming mode. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): streaming or static buffer. See `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int` |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |

### AudioTrack

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AudioTrack(
    streamType: Int, 
    sampleRateInHz: Int, 
    channelConfig: Int, 
    audioFormat: Int, 
    bufferSizeInBytes: Int, 
    mode: Int, 
    sessionId: Int)
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/media/AudioTrack.Builder` or AudioTrack to specify the AudioAttributes instead of the stream type which is only for volume control.*

Class constructor with audio session. Use this constructor when the AudioTrack must be attached to a particular audio session. The primary use of the audio session ID is to associate audio effects to a particular instance of AudioTrack: if an audio session ID is provided when creating an AudioEffect, this effect will be applied only to audio tracks and media players in the same session and not to the output mix. When an AudioTrack is created without specifying a session, it will create its own session which can be retrieved by calling the getAudioSessionId method. If a non-zero session ID is provided, this AudioTrack will share effects attached to this session with all other media players or audio tracks in the same session, otherwise a new session will be created for this track if none is supplied.

| Parameters ||
|---|---|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the type of the audio stream. See `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_VOICE_CALL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_SYSTEM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_RING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_MUSIC:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ALARM:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_NOTIFICATION:kotlin.Int`. |
| `sampleRateInHz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial source sample rate expressed in Hz. `https://developer.android.com/reference/kotlin/android/media/AudioFormat#SAMPLE_RATE_UNSPECIFIED:kotlin.Int` means to use a route-dependent value which is usually the sample rate of the sink. |
| `channelConfig` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): describes the configuration of the audio channels. See `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_MONO:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_STEREO:kotlin.Int` |
| --- | --- |
| `audioFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the format in which the audio data is represented. See `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int`. |
| `bufferSizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the total size (in bytes) of the internal buffer where audio data is read from for playback. This should be a nonzero multiple of the frame size in bytes. If the track's creation mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int`, this is the maximum length sample, or audio clip, that can be played by this instance. If the track's creation mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int`, this should be the desired buffer size for the `AudioTrack` to satisfy the application's latency requirements. If `bufferSizeInBytes` is less than the minimum buffer size for the output sink, it is increased to the minimum buffer size. The method getBufferSizeInFrames returns the actual size in frames of the buffer created, which determines the minimum frequency to write to the streaming `AudioTrack` to avoid underrun. You can write data into this buffer in smaller chunks than this size. See getMinBufferSize to determine the estimated minimum buffer size for an AudioTrack instance in streaming mode. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): streaming or static buffer. See `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int` |
| --- | --- |
| `sessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Id of audio session the AudioTrack must be attached to |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |

## Public methods

### addOnCodecFormatChangedListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnCodecFormatChangedListener(
    executor: Executor, 
    listener: AudioTrack.OnCodecFormatChangedListener
): Unit
```

Adds an `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnCodecFormatChangedListener` to receive notifications of codec format change events on this `AudioTrack`.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): Specifies the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` object to control execution. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [AudioTrack.OnCodecFormatChangedListener](../android/media/AudioTrack.OnCodecFormatChangedListener.md): The `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnCodecFormatChangedListener` interface to receive notifications of codec events. This value cannot be `null`. |

### addOnRoutingChangedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnRoutingChangedListener(
    listener: AudioRouting.OnRoutingChangedListener!, 
    handler: Handler!
): Unit
```

Adds an `https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener` to receive notifications of routing changes on this AudioTrack.

| Parameters ||
|---|---|
| `listener` | [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!: The `https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener` interface to receive notifications of rerouting events. |
| `handler` | [Handler](../android.os/Handler.md)!: Specifies the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` object for the thread on which to execute the callback. If `null`, the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` associated with the main `https://developer.android.com/reference/kotlin/android/os/Looper.html#` will be used. |

### addOnRoutingChangedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnRoutingChangedListener(
    listener: AudioTrack.OnRoutingChangedListener!, 
    handler: Handler!
): Unit
```

**Deprecated:** *users should switch to the general purpose `https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener` class instead.*

Adds an `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnRoutingChangedListener` to receive notifications of routing changes on this AudioTrack.

| Parameters ||
|---|---|
| `listener` | [AudioTrack.OnRoutingChangedListener](../android/media/AudioTrack.OnRoutingChangedListener.md)!: The `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnRoutingChangedListener` interface to receive notifications of rerouting events. |
| `handler` | [Handler](../android.os/Handler.md)!: Specifies the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` object for the thread on which to execute the callback. If `null`, the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` associated with the main `https://developer.android.com/reference/kotlin/android/os/Looper.html#` will be used. |

### attachAuxEffect

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun attachAuxEffect(effectId: Int): Int
```

Attaches an auxiliary effect to the audio track. A typical auxiliary effect is a reverberation effect which can be applied on any sound source that directs a certain amount of its energy to this effect. This amount is defined by setAuxEffectSendLevel.

After creating an auxiliary effect (e.g. EnvironmentalReverb), retrieve its ID with getId and use it when calling this method to attach the audio track to the effect.

To detach the effect from the audio track, call this method with a null effect id.

| Parameters ||
|---|---|
| `effectId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): system wide unique id of the effect to attach |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | error code or success, see `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` |

### createVolumeShaper

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createVolumeShaper(configuration: VolumeShaper.Configuration): VolumeShaper
```

Returns a VolumeShaper object that can be used modify the volume envelope of the player or track.

| Parameters ||
|---|---|
| `configuration` | [VolumeShaper.Configuration](../android/media/VolumeShaper.Configuration.md): This value cannot be `null`. |

| Return ||
|---|---|
| VolumeShaper | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `configuration` is not allowed by the player. |
| `java.lang.IllegalStateException` | if too many `VolumeShaper`s are requested or the state of the player does not permit its creation (e.g. player is released). |

### flush

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun flush(): Unit
```

Flushes the audio data currently queued for playback. Any data that has been written but not yet presented will be discarded. No-op if not stopped or paused, or if the track's creation mode is not `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int`. 
Note that although data written but not yet presented is discarded, there is no guarantee that all of the buffer space formerly used by that data is available for a subsequent write. For example, a call to write with `sizeInBytes` less than or equal to the total buffer size may return a short actual transfer count.

### flushWrittenFramesFromPosition

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun flushWrittenFramesFromPosition(
    positionInFrames: Long, 
    accuracy: Int
): Long
```

Flush all data from the given position.

If this operation returns successfully, #write after a call to this method will be written from frame position returned by this method. The method getWrittenFramesCount may be used to find the current frame position.

This method is only allowed in offload mode ((i.e. tracks created with setOffloadedPlayback set to `true`)). Applications can call this function to flush data while it is actively playing.

Supporting this method relies on the device's capabilities. Call getFlushWrittenFramesFromPositionSupport to query how this method is supported with the AudioFormat and AudioAttributes before creating the AudioTrack. If getFlushWrittenFramesFromPositionSupport returns `0`, UnsupportedOperationException will be thrown.

When clients request to flush from a certain position, the audio system will return the actual flushed position based on the requested position, the requested flush accuracy, and how much it was able to discard. All data from the actual flushed position will be discarded. When the stream is flushed, the stream end (if set by setOffloadEndOfStream) will be reset.

The client must not write any data before this function returns. Otherwise, the data may be corrupted. When the method returns successfully and the stream is active, the client must write data immediately if little audio data remains, otherwise the playback may underrun.

| Parameters ||
|---|---|
| `positionInFrames` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the start point in frames to flush. The value must be between 0 and total written frames. |
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the accuracy requirement when flushing. Use `https://developer.android.com/reference/kotlin/android/media/AudioTrack#FLUSH_FROM_ACCURACY_BEST_EFFORT:kotlin.Int` to indicate flush as close as possible to the requested position. Use `https://developer.android.com/reference/kotlin/android/media/AudioTrack#FLUSH_FROM_ACCURACY_EXACT:kotlin.Int` to indicate must flush from the requested position. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#FLUSH_FROM_ACCURACY_BEST_EFFORT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#FLUSH_FROM_ACCURACY_EXACT:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the actual flushed position. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `accuracy` is not valid, or `positionInFrames` is negative. |
| `java.lang.IllegalStateException` | when accuracy is specified as `https://developer.android.com/reference/kotlin/android/media/AudioTrack#FLUSH_FROM_ACCURACY_EXACT:kotlin.Int` but the requested position is not between the rendered position and the written position. Call getTimestamp to query the rendered position and getWrittenFramesCount for the written position. |
| `java.lang.UnsupportedOperationException` | if this method is not supported. |
| --- | --- |

**See Also**

- getFlushWrittenFramesFromPositionSupport

### getAudioAttributes

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAudioAttributes(): AudioAttributes
```

Returns the AudioAttributes used in configuration. If a `streamType` is used instead of an `AudioAttributes` to configure the AudioTrack (the use of `streamType` for configuration is deprecated), then the `AudioAttributes` equivalent to the `streamType` is returned.

| Return ||
|---|---|
| AudioAttributes | The `AudioAttributes` used to configure the AudioTrack. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If the track is not initialized. |

### getAudioDescriptionMixLeveldB

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAudioDescriptionMixLeveldB(): Float
```

Returns the Audio Description mix level in dB. If Audio Description mixing is unavailable from the hardware device, a value of `Float.NEGATIVE_INFINITY` is returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the current Audio Description Mix Level in dB. A value of `Float.NEGATIVE_INFINITY` means that the audio description is not mixed or the hardware is not available. This should reflect the **true** internal device mix level; hence the application might receive any floating value except `Float.NaN`. |

### getAudioFormat

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAudioFormat(): Int
```

Returns the configured audio data encoding. See `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int`.

### getAudioSessionId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAudioSessionId(): Int
```

Returns the audio session ID.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the ID of the audio session this AudioTrack belongs to. |

### getBufferCapacityInFrames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBufferCapacityInFrames(): Int
```

Returns the maximum size of the `AudioTrack` buffer in frames.

If the track's creation mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int`, it is equal to the specified bufferSizeInBytes on construction, converted to frame units. A static track's frame count will not change.

If the track's creation mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int`, it is greater than or equal to the specified bufferSizeInBytes converted to frame units. For streaming tracks, this value may be rounded up to a larger value if needed by the target output sink, and if the track is subsequently routed to a different output sink, the frame count may enlarge to accommodate.

If the `AudioTrack` encoding indicates compressed data, e.g. `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC3:kotlin.Int`, then the frame count returned is the size of the `AudioTrack` buffer in bytes.

See also getProperty for key `https://developer.android.com/reference/kotlin/android/media/AudioManager#PROPERTY_OUTPUT_FRAMES_PER_BUFFER:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | maximum size in frames of the `AudioTrack` buffer. Value is 0 or greater |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if track is not initialized. |

### getBufferSizeInFrames

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBufferSizeInFrames(): Int
```

Returns the effective size of the `AudioTrack` buffer that the application writes to.

This will be less than or equal to the result of getBufferCapacityInFrames. It will be equal if setBufferSizeInFrames has never been called.

If the track is subsequently routed to a different output sink, the buffer size and capacity may enlarge to accommodate.

If the `AudioTrack` encoding indicates compressed data, e.g. `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC3:kotlin.Int`, then the frame count returned is the size of the `AudioTrack` buffer in bytes.

See also getProperty for key `https://developer.android.com/reference/kotlin/android/media/AudioManager#PROPERTY_OUTPUT_FRAMES_PER_BUFFER:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | current size in frames of the `AudioTrack` buffer. Value is 0 or greater |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if track is not initialized. |

### getChannelConfiguration

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChannelConfiguration(): Int
```

Returns the configured channel position mask.

For example, refer to `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_MONO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_STEREO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_5POINT1:kotlin.Int`. This method may return `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_INVALID:kotlin.Int` if a channel index mask was used. Consider getFormat instead, to obtain an AudioFormat, which contains both the channel position mask and the channel index mask.

### getChannelCount

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChannelCount(): Int
```

Returns the configured number of channels.

### getCodecProvenance

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCodecProvenance(): String
```

Returns the codec provenance of the `AudioTrack` specified at the time of configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a media type of the audio codec or an empty string if the codec provenance is not set. This value cannot be `null`. |

### getDualMonoMode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDualMonoMode(): Int
```

Returns the Dual Mono mode presentation setting. If no Dual Mono presentation is available for the output device, then `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_OFF:kotlin.Int` is returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | one of `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_OFF:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_LR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_LL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_RR:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_LR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_LL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_RR:kotlin.Int` |

### getFlushWrittenFramesFromPositionSupport

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getFlushWrittenFramesFromPositionSupport(
    format: AudioFormat, 
    attributes: AudioAttributes
): Int
```

Returns a bit mask representing the current feature support for flushWrittenFramesFromPosition for the AudioTrack in offload mode that is created with the given AudioFormat and AudioAttributes.

| Parameters ||
|---|---|
| `format` | [AudioFormat](AudioFormat.md): the AudioFormat to create AudioTrack. This value cannot be `null`. |
| `attributes` | [AudioAttributes](AudioAttributes.md): the AudioAttributes to create AudioTrack. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask representing the flushWrittenFramesFromPosition support level. If flushWrittenFramesFromPosition is not supported, `0` is returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#FLUSH_WRITTEN_FRAMES_SUPPORTED:kotlin.Int` |

**See Also**

- flushWrittenFramesFromPosition

### getFormat

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFormat(): AudioFormat
```

Returns the configured `AudioTrack` format.

| Return ||
|---|---|
| AudioFormat | an AudioFormat containing the `AudioTrack` parameters at the time of configuration. This value cannot be `null`. |

### getLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLogSessionId(): LogSessionId
```

Returns the LogSessionId.

| Return ||
|---|---|
| LogSessionId | This value cannot be `null`. |

### getMaxVolume

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getMaxVolume(): Float
```

Returns the maximum gain value, which is greater than or equal to 1.0. Gain values greater than the maximum will be clamped to the maximum.

The word "volume" in the API name is historical; this is actually a gain. expressed as a linear multiplier on sample values, where a maximum value of 1.0 corresponds to a gain of 0 dB (sample values left unmodified).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the maximum value, which is greater than or equal to 1.0. |

### getMetrics

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMetrics(): PersistableBundle!
```

Return Metrics data about the current AudioTrack instance.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#!` | a `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` containing the set of attributes and values available for the media being handled by this instance of AudioTrack The attributes are descibed in `https://developer.android.com/reference/kotlin/android/media/AudioTrack.MetricsConstants`. Additional vendor-specific fields may also be present in the return value. |

### getMinBufferSize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getMinBufferSize(
    sampleRateInHz: Int, 
    channelConfig: Int, 
    audioFormat: Int
): Int
```

Returns the estimated minimum buffer size required for an AudioTrack object to be created in the `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int` mode. The size is an estimate because it does not consider either the route or the sink, since neither is known yet. Note that this size doesn't guarantee a smooth playback under load, and higher values should be chosen according to the expected frequency at which the buffer will be refilled with additional data to play. For example, if you intend to dynamically set the source sample rate of an AudioTrack to a higher value than the initial source sample rate, be sure to configure the buffer size based on the highest planned sample rate.

| Parameters ||
|---|---|
| `sampleRateInHz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the source sample rate expressed in Hz. `https://developer.android.com/reference/kotlin/android/media/AudioFormat#SAMPLE_RATE_UNSPECIFIED:kotlin.Int` is not permitted. |
| `channelConfig` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): describes the configuration of the audio channels. See `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_MONO:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_STEREO:kotlin.Int` |
| `audioFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the format in which the audio data is represented. See `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` if an invalid parameter was passed, or `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR:kotlin.Int` if unable to query for output properties, or the minimum buffer size expressed in bytes. |

### getMinVolume

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getMinVolume(): Float
```

Returns the minimum gain value, which is the constant 0.0. Gain values less than 0.0 will be clamped to 0.0.

The word "volume" in the API name is historical; this is actually a linear gain.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the minimum value, which is the constant 0.0. |

### getNativeOutputSampleRate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getNativeOutputSampleRate(streamType: Int): Int
```

Returns the output sample rate in Hz for the specified stream type.

### getNotificationMarkerPosition

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNotificationMarkerPosition(): Int
```

Returns marker position expressed in frames.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | marker position in wrapping frame units similar to getPlaybackHeadPosition, or zero if marker is disabled. |

### getOffloadDelay

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOffloadDelay(): Int
```

Return the decoder delay of an offloaded track, expressed in frames, previously set with setOffloadDelayPadding, or 0 if it was never modified.

This delay indicates the number of frames to be ignored at the beginning of the stream. This value can only be queried on a track successfully initialized with setOffloadedPlayback.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | decoder delay expressed in frames. Value is 0 or greater |

### getOffloadPadding

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOffloadPadding(): Int
```

Return the decoder padding of an offloaded track, expressed in frames, previously set with setOffloadDelayPadding, or 0 if it was never modified.

This padding indicates the number of frames to be ignored at the end of the stream. This value can only be queried on a track successfully initialized with setOffloadedPlayback.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | decoder padding expressed in frames. Value is 0 or greater |

### getPerformanceMode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPerformanceMode(): Int
```

Returns the current performance mode of the AudioTrack.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | one of `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PERFORMANCE_MODE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PERFORMANCE_MODE_LOW_LATENCY:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PERFORMANCE_MODE_POWER_SAVING:kotlin.Int`. Use setPerformanceMode in the `https://developer.android.com/reference/kotlin/android/media/AudioTrack.Builder` to enable a performance mode. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PERFORMANCE_MODE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PERFORMANCE_MODE_LOW_LATENCY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PERFORMANCE_MODE_POWER_SAVING:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if track is not initialized. |

### getPlayState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPlayState(): Int
```

Returns the playback state of the AudioTrack instance.
**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PLAYSTATE_STOPPED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PLAYSTATE_PAUSED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PLAYSTATE_PLAYING:kotlin.Int`

### getPlaybackHeadPosition

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPlaybackHeadPosition(): Int
```

Returns the playback head position expressed in frames. Though the "int" type is signed 32-bits, the value should be reinterpreted as if it is unsigned 32-bits. That is, the next position after 0x7FFFFFFF is (int) 0x80000000. This is a continuously advancing counter. It will wrap (overflow) periodically, for example approximately once every 27:03:11 hours:minutes:seconds at 44.1 kHz. It is reset to zero by flush, reloadStaticData, and stop. If the track's creation mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int`, the return value indicates the total number of frames played since reset, *not* the current offset within the buffer.

### getPlaybackParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPlaybackParams(): PlaybackParams
```

Returns the current playback parameters. See setPlaybackParams to set playback parameters

| Return ||
|---|---|
| PlaybackParams | current PlaybackParams. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if track is not initialized. |

### getPlaybackRate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPlaybackRate(): Int
```

Returns the current playback sample rate rate in Hz.

### getPositionNotificationPeriod

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPositionNotificationPeriod(): Int
```

Returns the notification update period expressed in frames. Zero means that no position update notifications are being delivered.

### getPreferredDevice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPreferredDevice(): AudioDeviceInfo!
```

Returns the selected output specified by setPreferredDevice. Note that this is not guaranteed to correspond to the actual device being used for playback.

### getRoutedDevice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRoutedDevice(): AudioDeviceInfo!
```

Returns an AudioDeviceInfo identifying the current routing of this AudioTrack. Note: The query is only valid if the AudioTrack is currently playing. If it is not, `getRoutedDevice()` will return null. Audio may play on multiple devices simultaneously (e.g. an alarm playing on headphones and speaker on a phone), so prefer using getRoutedDevices.

### getRoutedDevices

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRoutedDevices(): MutableList<AudioDeviceInfo!>
```

Returns a List of AudioDeviceInfo identifying the current routing of this AudioTrack. Note: The query is only valid if the AudioTrack is currently playing. If it is not, `getRoutedDevices()` will return an empty list.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo!>` | This value cannot be `null`. |

### getSampleRate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSampleRate(): Int
```

Returns the configured audio source sample rate in Hz. The initial source sample rate depends on the constructor parameters, but the source sample rate may change if setPlaybackRate is called. If the constructor had a specific sample rate, then the initial sink sample rate is that value. If the constructor had `https://developer.android.com/reference/kotlin/android/media/AudioFormat#SAMPLE_RATE_UNSPECIFIED:kotlin.Int`, then the initial sink sample rate is a route-dependent default value based on the source \[sic\].

### getStartThresholdInFrames

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStartThresholdInFrames(): Int
```

Returns the streaming start threshold of the `AudioTrack`.

The streaming start threshold is the buffer level that the written audio data must reach for audio streaming to start after play is called. When an `AudioTrack` is created, the streaming start threshold is the buffer capacity in frames. If the buffer size in frames is reduced by setBufferSizeInFrames to a value smaller than the start threshold then that value will be used instead for the streaming start threshold.

For compressed streams, the size of a frame is considered to be exactly one byte.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current start threshold in frames value. This is an integer between 1 to the buffer capacity (see getBufferCapacityInFrames), and might change if the output sink changes after track creation. Value is 1 or greater |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the track is not initialized or the track is not `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int`. |

**See Also**

- setStartThresholdInFrames

### getState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getState(): Int
```

Returns the state of the AudioTrack instance. This is useful after the AudioTrack instance has been created to check if it was initialized properly. This ensures that the appropriate resources have been acquired.
**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioTrack#STATE_UNINITIALIZED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioTrack#STATE_INITIALIZED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioTrack#STATE_NO_STATIC_DATA:kotlin.Int`

### getStreamType

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStreamType(): Int
```

Returns the volume stream type of this AudioTrack. Compare the result against `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_VOICE_CALL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_SYSTEM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_RING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_MUSIC:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ALARM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_NOTIFICATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_DTMF:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ACCESSIBILITY:kotlin.Int`.

### getTimestamp

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimestamp(timestamp: AudioTimestamp!): Boolean
```

Poll for a timestamp on demand.

If you need to track timestamps during initial warmup or after a routing or mode change, you should request a new timestamp periodically until the reported timestamps show that the frame position is advancing, or until it becomes clear that timestamps are unavailable for this route.

After the clock is advancing at a stable rate, query for a new timestamp approximately once every 10 seconds to once per minute. Calling this method more often is inefficient. It is also counter-productive to call this method more often than recommended, because the short-term differences between successive timestamp reports are not meaningful. If you need a high-resolution mapping between frame position and presentation time, consider implementing that at application level, based on low-resolution timestamps.

The audio data at the returned position may either already have been presented, or may have not yet been presented but is committed to be presented. It is not possible to request the time corresponding to a particular position, or to request the (fractional) position corresponding to a particular time. If you need such features, consider implementing them at application level.

| Parameters ||
|---|---|
| `timestamp` | [AudioTimestamp](AudioTimestamp.md)!: a reference to a non-null AudioTimestamp instance allocated and owned by caller. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a timestamp is available, or false if no timestamp is available. If a timestamp is available, the AudioTimestamp instance is filled in with a position in frame units, together with the estimated time when that frame was presented or is committed to be presented. In the case that no timestamp is available, any supplied instance is left unaltered. A timestamp may be temporarily unavailable while the audio clock is stabilizing, or during and immediately after a route change. A timestamp is permanently unavailable for a given route if the route does not support timestamps. In this case, the approximate frame position can be obtained using getPlaybackHeadPosition. However, it may be useful to continue to query for timestamps occasionally, to recover after a route change. |

### getUnderrunCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUnderrunCount(): Int
```

Returns the number of underrun occurrences in the application-level write buffer since the AudioTrack was created. An underrun occurs if the application does not write audio data quickly enough, causing the buffer to underflow and a potential audio glitch or pop.

Underruns are less likely when buffer sizes are large. It may be possible to eliminate underruns by recreating the AudioTrack with a larger buffer. Or by using setBufferSizeInFrames to dynamically increase the effective size of the buffer.

### getWrittenFramesCount

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWrittenFramesCount(): Long
```

Returns the number of audio frames written to a `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int` AudioTrack.

The counter starts from zero and is incremented for every successful #write call to a `MODE_STREAM` `AudioTrack`, and is set to the return value of a successful flushWrittenFramesFromPosition call. This counter is not reset when the track is flushed by flush, stopped by stop, or paused by pause. The frames returned by this method represents the current frame position for flushWrittenFramesFromPosition. It does not represent the actual frames rendered.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of frames written. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the track is not initialized or called on a `MODE_STATIC` `AudioTrack`. |

**See Also**

- flushWrittenFramesFromPosition

### isDirectPlaybackSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isDirectPlaybackSupported(
    format: AudioFormat, 
    attributes: AudioAttributes
): Boolean
```

**Deprecated:** *Use getDirectPlaybackSupport instead.*

Returns whether direct playback of an audio format with the provided attributes is currently supported on the system.

Direct playback means that the audio stream is not resampled or downmixed by the framework. Checking for direct support can help the app select the representation of audio content that most closely matches the capabilities of the device and peripherials (e.g. A/V receiver) connected to it. Note that the provided stream can still be re-encoded or mixed with other streams, if needed.

Also note that this query only provides information about the support of an audio format. It does not indicate whether the resources necessary for the playback are available at that instant.

| Parameters ||
|---|---|
| `format` | [AudioFormat](AudioFormat.md): a non-null AudioFormat instance describing the format of the audio data. |
| `attributes` | [AudioAttributes](AudioAttributes.md): a non-null AudioAttributes instance. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the given audio format can be played directly. |

### isOffloadedPlayback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isOffloadedPlayback(): Boolean
```

Returns whether the track was built with setOffloadedPlayback set to `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the track is using offloaded playback. |

### pause

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pause(): Unit
```

Pauses the playback of the audio data. Data that has not been played back will not be discarded. Subsequent calls to play will play this data back. See flush to discard this data.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | |

### play

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun play(): Unit
```

Starts playing an AudioTrack.

If track's creation mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int`, you must have called one of the write methods (write, write, write, write, write, or write) prior to play().

If the mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int`, you can optionally prime the data path prior to calling play(), by writing up to `bufferSizeInBytes` (from constructor). If you don't call write() first, or if you call write() but with an insufficient amount of data, then the track will be in underrun state at play(). In this case, playback will not actually start playing until the data path is filled to a device-specific minimum level. This requirement for the path to be filled to a minimum level is also true when resuming audio playback after calling stop(). Similarly the buffer will need to be filled up again after the track underruns due to failure to call write() in a timely manner with sufficient data. For portability, an application should prime the data path to the maximum allowed by writing data until the write() method returns a short transfer count. This allows play() to start immediately, and reduces the chance of underrun.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` the minimum level to start playing can be obtained using getStartThresholdInFrames and set with setStartThresholdInFrames.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the track isn't properly initialized |

### registerStreamEventCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerStreamEventCallback(
    executor: Executor, 
    eventCallback: AudioTrack.StreamEventCallback
): Unit
```

Registers a callback for the notification of stream events. This callback can only be registered for instances operating in offloaded mode (see setOffloadedPlayback and isOffloadedPlaybackSupported for more details).

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` to handle the callbacks. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `eventCallback` | [AudioTrack.StreamEventCallback](../android/media/AudioTrack.StreamEventCallback.md): the callback to receive the stream event notifications. This value cannot be `null`. |

### release

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun release(): Unit
```

Releases the native AudioTrack resources.

### reloadStaticData

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reloadStaticData(): Int
```

Sets the playback head position within the static buffer to zero, that is it rewinds to start of static buffer. The track must be stopped or paused, and the track's creation mode must be `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int`.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, also resets the value returned by getPlaybackHeadPosition to zero. For earlier API levels, the reset behavior is unspecified.

Use setPlaybackHeadPosition with a zero position if the reset of `getPlaybackHeadPosition()` is not needed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | error code or success, see `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` |

### removeOnCodecFormatChangedListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnCodecFormatChangedListener(listener: AudioTrack.OnCodecFormatChangedListener): Unit
```

Removes an `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnCodecFormatChangedListener` which has been previously added to receive codec format change events.

| Parameters ||
|---|---|
| `listener` | [AudioTrack.OnCodecFormatChangedListener](../android/media/AudioTrack.OnCodecFormatChangedListener.md): The previously added `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnCodecFormatChangedListener` interface to remove. This value cannot be `null`. |

### removeOnRoutingChangedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnRoutingChangedListener(listener: AudioRouting.OnRoutingChangedListener!): Unit
```

Removes an `https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener` which has been previously added to receive rerouting notifications.

| Parameters ||
|---|---|
| `listener` | [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!: The previously added `https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener` interface to remove. |

### removeOnRoutingChangedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnRoutingChangedListener(listener: AudioTrack.OnRoutingChangedListener!): Unit
```

**Deprecated:** *users should switch to the general purpose `https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener` class instead.*

Removes an `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnRoutingChangedListener` which has been previously added to receive rerouting notifications.

| Parameters ||
|---|---|
| `listener` | [AudioTrack.OnRoutingChangedListener](../android/media/AudioTrack.OnRoutingChangedListener.md)!: The previously added `https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnRoutingChangedListener` interface to remove. |

### setAudioDescriptionMixLeveldB

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAudioDescriptionMixLeveldB(level: Float): Boolean
```

Sets the Audio Description mix level in dB. For AudioTracks incorporating a secondary Audio Description stream (where such contents may be sent through an Encapsulation Mode other than `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_MODE_NONE:kotlin.Int`). or internally by a HW channel), the level of mixing of the Audio Description to the Main Audio stream is controlled by this method. Such mixing occurs **prior** to overall volume scaling.

| Parameters ||
|---|---|
| `level` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a floating point value between `Float.NEGATIVE_INFINITY` to `+48.f`, where `Float.NEGATIVE_INFINITY` means the Audio Description is not mixed and a level of `0.f` means the Audio Description is mixed without scaling. Value is 48.0f or less |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false on failure. |

### setAuxEffectSendLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAuxEffectSendLevel(level: Float): Int
```

Sets the send level of the audio track to the attached auxiliary effect attachAuxEffect. Effect levels are clamped to the closed interval \[0.0, max\] where max is the value of getMaxVolume. A value of 0.0 results in no effect, and a value of 1.0 is full send.

By default the send level is 0.0f, so even if an effect is attached to the player this method must be called for the effect to be applied.

Note that the passed level value is a linear scalar. UI controls should be scaled logarithmically: the gain applied by audio framework ranges from -72dB to at least 0dB, so an appropriate conversion from linear UI input x to level is: x == 0 -\> level = 0 0 \< x \<= R -\> level = 10\^(72\*(x-R)/20/R)

| Parameters ||
|---|---|
| `level` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): linear send level. Value is 0.0f or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | error code or success, see `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR:kotlin.Int` |

### setBufferSizeInFrames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBufferSizeInFrames(bufferSizeInFrames: Int): Int
```

Limits the effective size of the `AudioTrack` buffer that the application writes to.

A write to this AudioTrack will not fill the buffer beyond this limit. If a blocking write is used then the write will block until the data can fit within this limit.

Changing this limit modifies the latency associated with the buffer for this track. A smaller size will give lower latency but there may be more glitches due to buffer underruns.

The actual size used may not be equal to this requested size. It will be limited to a valid range with a maximum of getBufferCapacityInFrames. It may also be adjusted slightly for internal reasons. If bufferSizeInFrames is less than zero then `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` will be returned.

This method is supported for PCM audio at all API levels. Compressed audio is supported in API levels 33 and above. For compressed streams the size of a frame is considered to be exactly one byte.

| Parameters ||
|---|---|
| `bufferSizeInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): requested buffer size in frames. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the actual buffer size in frames or an error code, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if track is not initialized. |

### setDualMonoMode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDualMonoMode(dualMonoMode: Int): Boolean
```

Sets the Dual Mono mode presentation on the output device. The Dual Mono mode is generally applied to stereo audio streams where the left and right channels come from separate sources. For compressed audio, where the decoding is done in hardware, Dual Mono presentation needs to be performed by the hardware output device as the PCM audio is not available to the framework.

| Parameters ||
|---|---|
| `dualMonoMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_OFF:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_LR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_LL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_RR:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_LR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_LL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#DUAL_MONO_MODE_RR:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false on failure if the output device does not support Dual Mono mode. |

### setLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLogSessionId(logSessionId: LogSessionId): Unit
```

Sets a LogSessionId instance to this AudioTrack for metrics collection.

| Parameters ||
|---|---|
| `logSessionId` | [LogSessionId](../android.media.metrics/LogSessionId.md): a LogSessionId instance which is used to identify this object to the metrics service. Proper generated Ids must be obtained from the Java metrics service and should be considered opaque. Use `https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId#LOG_SESSION_ID_NONE:android.media.metrics.LogSessionId` to remove the logSessionId association. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if AudioTrack not initialized. |

### setLoopPoints

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLoopPoints(
    startInFrames: Int, 
    endInFrames: Int, 
    loopCount: Int
): Int
```

Sets the loop points and the loop count. The loop can be infinite. Similarly to setPlaybackHeadPosition, the track must be stopped or paused for the loop points to be changed, and must use the `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int` mode.

| Parameters ||
|---|---|
| `startInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): loop start marker expressed in frames. Zero corresponds to start of buffer. The start marker must not be greater than or equal to the buffer size in frames, or negative. Value is 0 or greater |
| `endInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): loop end marker expressed in frames. The total buffer size in frames corresponds to end of buffer. The end marker must not be greater than the buffer size in frames. For looping, the end marker must not be less than or equal to the start marker, but to disable looping it is permitted for start marker, end marker, and loop count to all be 0. If any input parameters are out of range, this method returns `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int`. If the loop period (endInFrames - startInFrames) is too small for the implementation to support, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` is returned. The loop range is the interval \[startInFrames, endInFrames). As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, the position is left unchanged, unless it is greater than or equal to the loop end marker, in which case it is forced to the loop start marker. For earlier API levels, the effect on position is unspecified. Value is 0 or greater |
| `loopCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of times the loop is looped; must be greater than or equal to -1. A value of -1 means infinite looping, and 0 disables looping. A value of positive N means to "loop" (go back) N times. For example, a value of one means to play the region two times in total. Value is -1 or greater |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | error code or success, see `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` |

### setNotificationMarkerPosition

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNotificationMarkerPosition(markerInFrames: Int): Int
```

Sets the position of the notification marker. At most one marker can be active.

| Parameters ||
|---|---|
| `markerInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): marker position in wrapping frame units similar to getPlaybackHeadPosition, or zero to disable the marker. To set a marker at a position which would appear as zero due to wraparound, a workaround is to use a non-zero position near zero, such as -1 or 1. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | error code or success, see `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` |

### setOffloadDelayPadding

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOffloadDelayPadding(
    delayInFrames: Int, 
    paddingInFrames: Int
): Unit
```

Configures the delay and padding values for the current compressed stream playing in offload mode. This can only be used on a track successfully initialized with setOffloadedPlayback. The unit is frames, where a frame indicates the number of samples per channel, e.g. 100 frames for a stereo compressed stream corresponds to 200 decoded interleaved PCM samples.

| Parameters ||
|---|---|
| `delayInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of frames to be ignored at the beginning of the stream. A value of 0 indicates no delay is to be applied. Value is 0 or greater |
| `paddingInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of frames to be ignored at the end of the stream. A value of 0 of 0 indicates no padding is to be applied. Value is 0 or greater |

### setOffloadEndOfStream

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOffloadEndOfStream(): Unit
```

Declares that the last write() operation on this track provided the last buffer of this stream. After the end of stream, previously set padding and delay values are ignored. Can only be called only if the AudioTrack is opened in offload mode see setOffloadedPlayback. Can only be called only if the AudioTrack is in state `https://developer.android.com/reference/kotlin/android/media/AudioTrack#PLAYSTATE_PLAYING:kotlin.Int`; see getPlayState. Use this method in the same thread as any write() operation.

### setPlaybackHeadPosition

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPlaybackHeadPosition(positionInFrames: Int): Int
```

Sets the playback head position within the static buffer. The track must be stopped or paused for the position to be changed, and must use the `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STATIC:kotlin.Int` mode.

| Parameters ||
|---|---|
| `positionInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): playback head position within buffer, expressed in frames. Zero corresponds to start of buffer. The position must not be greater than the buffer size in frames, or negative. Though this method and getPlaybackHeadPosition have similar names, the position values have different meanings. If looping is currently enabled and the new position is greater than or equal to the loop end marker, the behavior varies by API level: as of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, the looping is first disabled and then the position is set. For earlier API levels, the behavior is unspecified. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | error code or success, see `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` |

### setPlaybackParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPlaybackParams(params: PlaybackParams): Unit
```

Sets the playback parameters. This method returns failure if it cannot apply the playback parameters. One possible cause is that the parameters for speed or pitch are out of range. Another possible cause is that the `AudioTrack` is streaming (see `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int`) and the buffer size is too small. For speeds greater than 1.0f, the `AudioTrack` buffer on configuration must be larger than the speed multiplied by the minimum size getMinBufferSize) to allow proper playback.

| Parameters ||
|---|---|
| `params` | [PlaybackParams](PlaybackParams.md): see PlaybackParams. In particular, speed, pitch, and audio mode should be set. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the parameters are invalid or not accepted. |
| `java.lang.IllegalStateException` | if track is not initialized. |

### setPlaybackPositionUpdateListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPlaybackPositionUpdateListener(listener: AudioTrack.OnPlaybackPositionUpdateListener!): Unit
```

Sets the listener the AudioTrack notifies when a previously set marker is reached or for each periodic playback head position update. Notifications will be received in the same thread as the one in which the AudioTrack instance was created.

| Parameters ||
|---|---|
| `listener` | [AudioTrack.OnPlaybackPositionUpdateListener](../android/media/AudioTrack.OnPlaybackPositionUpdateListener.md)!: |

### setPlaybackPositionUpdateListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPlaybackPositionUpdateListener(
    listener: AudioTrack.OnPlaybackPositionUpdateListener!, 
    handler: Handler!
): Unit
```

Sets the listener the AudioTrack notifies when a previously set marker is reached or for each periodic playback head position update. Use this method to receive AudioTrack events in the Handler associated with another thread than the one in which you created the AudioTrack instance.

| Parameters ||
|---|---|
| `listener` | [AudioTrack.OnPlaybackPositionUpdateListener](../android/media/AudioTrack.OnPlaybackPositionUpdateListener.md)!: |
| `handler` | [Handler](../android.os/Handler.md)!: the Handler that will receive the event notification messages. |

### setPlaybackRate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPlaybackRate(sampleRateInHz: Int): Int
```

Sets the playback sample rate for this track. This sets the sampling rate at which the audio data will be consumed and played back (as set by the sampleRateInHz parameter in the AudioTrack constructor), not the original sampling rate of the content. For example, setting it to half the sample rate of the content will cause the playback to last twice as long, but will also result in a pitch shift down by one octave. The valid sample rate range is from 1 Hz to twice the value returned by getNativeOutputSampleRate. Use setPlaybackParams for speed control.

This method may also be used to repurpose an existing `AudioTrack` for playback of content of differing sample rate, but with identical encoding and channel mask.

| Parameters ||
|---|---|
| `sampleRateInHz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the sample rate expressed in Hz |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | error code or success, see `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` |

### setPositionNotificationPeriod

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPositionNotificationPeriod(periodInFrames: Int): Int
```

Sets the period for the periodic notification event.

| Parameters ||
|---|---|
| `periodInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): update period expressed in frames. Zero period means no position updates. A negative period is not allowed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | error code or success, see `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` |

### setPreferredDevice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPreferredDevice(deviceInfo: AudioDeviceInfo!): Boolean
```

Specifies an audio device (via an AudioDeviceInfo object) to route the output from this AudioTrack.

| Parameters ||
|---|---|
| `deviceInfo` | [AudioDeviceInfo](AudioDeviceInfo.md)!: The AudioDeviceInfo specifying the audio sink. If deviceInfo is null, default routing is restored. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if succesful, false if the specified AudioDeviceInfo is non-null and does not correspond to a valid audio output device. |

### setPresentation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPresentation(presentation: AudioPresentation): Int
```

Sets the audio presentation. If the audio presentation is invalid then `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` will be returned. If a multi-stream decoder (MSD) is not present, or the format does not support multiple presentations, then `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` will be returned. `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR:kotlin.Int` is returned in case of any other error.

| Parameters ||
|---|---|
| `presentation` | [AudioPresentation](AudioPresentation.md): see AudioPresentation. In particular, id should be set. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | error code or success, see `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the audio presentation is null. |
| `java.lang.IllegalStateException` | if track is not initialized. |

### setStartThresholdInFrames

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStartThresholdInFrames(startThresholdInFrames: Int): Int
```

Sets the streaming start threshold for an `AudioTrack`.

The streaming start threshold is the buffer level that the written audio data must reach for audio streaming to start after play is called.

For compressed streams, the size of a frame is considered to be exactly one byte.

| Parameters ||
|---|---|
| `startThresholdInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the desired start threshold. Value is 1 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the actual start threshold in frames value. This is an integer between 1 to the buffer capacity (see getBufferCapacityInFrames), and might change if the output sink changes after track creation. Value is 1 or greater |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if startThresholdInFrames is not positive. |
| `java.lang.IllegalStateException` | if the track is not initialized or the track transfer mode is not `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int`. |

**See Also**

- getStartThresholdInFrames

### setStereoVolume

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStereoVolume(
    leftGain: Float, 
    rightGain: Float
): Int
```

**Deprecated:** *Applications should use setVolume instead, as it more gracefully scales down to mono, and up to multi-channel content beyond stereo.*

Sets the specified left and right output gain values on the AudioTrack.

Gain values are clamped to the closed interval \[0.0, max\] where max is the value of getMaxVolume. A value of 0.0 results in zero gain (silence), and a value of 1.0 means unity gain (signal unchanged). The default value is 1.0 meaning unity gain.

The word "volume" in the API name is historical; this is actually a linear gain.

| Parameters ||
|---|---|
| `leftGain` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): output gain for the left channel. |
| `rightGain` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): output gain for the right channel |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | error code or success, see `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` |

### setVolume

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVolume(gain: Float): Int
```

Sets the specified output gain value on all channels of this track.

Gain values are clamped to the closed interval \[0.0, max\] where max is the value of getMaxVolume. A value of 0.0 results in zero gain (silence), and a value of 1.0 means unity gain (signal unchanged). The default value is 1.0 meaning unity gain.

This API is preferred over setStereoVolume, as it more gracefully scales down to mono, and up to multi-channel content beyond stereo.

The word "volume" in the API name is historical; this is actually a linear gain.

| Parameters ||
|---|---|
| `gain` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): output gain for all channels. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | error code or success, see `https://developer.android.com/reference/kotlin/android/media/AudioTrack#SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` |

### stop

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stop(): Unit
```

Stops playing the audio data. When used on an instance created in `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int` mode, audio will stop playing after the last buffer that was written has been played. For an immediate stop, use pause, followed by flush to discard audio data that hasn't been played back yet.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | |

### unregisterStreamEventCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterStreamEventCallback(eventCallback: AudioTrack.StreamEventCallback): Unit
```

Unregisters the callback for notification of stream events, previously registered with registerStreamEventCallback.

| Parameters ||
|---|---|
| `eventCallback` | [AudioTrack.StreamEventCallback](../android/media/AudioTrack.StreamEventCallback.md): the callback to unregister. This value cannot be `null`. |

### write

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(
    audioData: ByteArray, 
    offsetInBytes: Int, 
    sizeInBytes: Int
): Int
```

Writes the audio data to the audio sink for playback (streaming mode), or copies audio data for later playback (static buffer mode). The format specified in the AudioTrack constructor should be `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int` to correspond to the data in the array. The format can be `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int`, but this is deprecated.

In streaming mode, the write will normally block until all the data has been enqueued for playback, and will return a full transfer count. However, if the track is stopped or paused on entry, or another thread interrupts the write by calling stop or pause, or an I/O error occurs during the write, then the write may return a short transfer count.

In static buffer mode, copies the data to the buffer starting at offset 0. Note that the actual playback of this data might occur after this function returns.

| Parameters ||
|---|---|
| `audioData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the array that holds the data to play. This value cannot be `null`. |
| `offsetInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset expressed in bytes in audioData where the data to write starts. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes to write in audioData after the offset. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | zero or the positive number of bytes that were written, or one of the following error codes. The number of bytes will be a multiple of the frame size in bytes not to exceed sizeInBytes. - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` if the track isn't properly initialized - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` if the parameters don't resolve to valid data and indexes - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_DEAD_OBJECT:kotlin.Int` if the AudioTrack is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next write() - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR:kotlin.Int` in case of other error This is equivalent to write with `writeMode` set to `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`. |

### write

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(
    audioData: ByteArray, 
    offsetInBytes: Int, 
    sizeInBytes: Int, 
    writeMode: Int
): Int
```

Writes the audio data to the audio sink for playback (streaming mode), or copies audio data for later playback (static buffer mode). The format specified in the AudioTrack constructor should be `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int` to correspond to the data in the array. The format can be `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int`, but this is deprecated.

In streaming mode, the blocking behavior depends on the write mode. If the write mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, the write will normally block until all the data has been enqueued for playback, and will return a full transfer count. However, if the write mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`, or the track is stopped or paused on entry, or another thread interrupts the write by calling stop or pause, or an I/O error occurs during the write, then the write may return a short transfer count.

In static buffer mode, copies the data to the buffer starting at offset 0, and the write mode is ignored. Note that the actual playback of this data might occur after this function returns.

| Parameters ||
|---|---|
| `audioData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the array that holds the data to play. This value cannot be `null`. |
| `offsetInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset expressed in bytes in audioData where the data to write starts. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes to write in audioData after the offset. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |
| `writeMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`. It has no effect in static mode. With `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, the write will block until all data has been written to the audio sink. With `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`, the write will return immediately after queuing as much audio data for playback as possible without blocking. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | zero or the positive number of bytes that were written, or one of the following error codes. The number of bytes will be a multiple of the frame size in bytes not to exceed sizeInBytes. - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` if the track isn't properly initialized - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` if the parameters don't resolve to valid data and indexes - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_DEAD_OBJECT:kotlin.Int` if the AudioTrack is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next write() - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR:kotlin.Int` in case of other error |

### write

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(
    audioData: FloatArray, 
    offsetInFloats: Int, 
    sizeInFloats: Int, 
    writeMode: Int
): Int
```

Writes the audio data to the audio sink for playback (streaming mode), or copies audio data for later playback (static buffer mode). The format specified in the AudioTrack constructor should be `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int` to correspond to the data in the array.

In streaming mode, the blocking behavior depends on the write mode. If the write mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, the write will normally block until all the data has been enqueued for playback, and will return a full transfer count. However, if the write mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`, or the track is stopped or paused on entry, or another thread interrupts the write by calling stop or pause, or an I/O error occurs during the write, then the write may return a short transfer count.

In static buffer mode, copies the data to the buffer starting at offset 0, and the write mode is ignored. Note that the actual playback of this data might occur after this function returns.

| Parameters ||
|---|---|
| `audioData` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the array that holds the data to write. The implementation does not clip for sample values within the nominal range \[-1.0f, 1.0f\], provided that all gains in the audio pipeline are less than or equal to unity (1.0f), and in the absence of post-processing effects that could add energy, such as reverb. For the convenience of applications that compute samples using filters with non-unity gain, sample values +3 dB beyond the nominal range are permitted. However such values may eventually be limited or clipped, depending on various gains and later processing in the audio path. Therefore applications are encouraged to provide samples values within the nominal range. This value cannot be `null`. |
| `offsetInFloats` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset, expressed as a number of floats, in audioData where the data to write starts. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInFloats` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of floats to write in audioData after the offset. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |
| `writeMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`. It has no effect in static mode. With `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, the write will block until all data has been written to the audio sink. With `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`, the write will return immediately after queuing as much audio data for playback as possible without blocking. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | zero or the positive number of floats that were written, or one of the following error codes. The number of floats will be a multiple of the channel count not to exceed sizeInFloats. - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` if the track isn't properly initialized - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` if the parameters don't resolve to valid data and indexes - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_DEAD_OBJECT:kotlin.Int` if the AudioTrack is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next write() - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR:kotlin.Int` in case of other error |

### write

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(
    audioData: ByteBuffer, 
    sizeInBytes: Int, 
    writeMode: Int
): Int
```

Writes the audio data to the audio sink for playback (streaming mode), or copies audio data for later playback (static buffer mode). The audioData in ByteBuffer should match the format specified in the AudioTrack constructor.

In streaming mode, the blocking behavior depends on the write mode. If the write mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, the write will normally block until all the data has been enqueued for playback, and will return a full transfer count. However, if the write mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`, or the track is stopped or paused on entry, or another thread interrupts the write by calling stop or pause, or an I/O error occurs during the write, then the write may return a short transfer count.

In static buffer mode, copies the data to the buffer starting at offset 0, and the write mode is ignored. Note that the actual playback of this data might occur after this function returns.

| Parameters ||
|---|---|
| `audioData` | [ByteBuffer](../java.nio/ByteBuffer.md): the buffer that holds the data to write, starting at the position reported by `audioData.position()`. Note that upon return, the buffer position (`audioData.position()`) will have been advanced to reflect the amount of data that was successfully written to the AudioTrack. This value cannot be `null`. |
| `sizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of bytes to write. It is recommended but not enforced that the number of bytes requested be a multiple of the frame size (sample size in bytes multiplied by the channel count). Note this may differ from `audioData.remaining()`, but cannot exceed it. |
| `writeMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`. It has no effect in static mode. With `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, the write will block until all data has been written to the audio sink. With `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`, the write will return immediately after queuing as much audio data for playback as possible without blocking. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | zero or the positive number of bytes that were written, or one of the following error codes. - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` if the track isn't properly initialized - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` if the parameters don't resolve to valid data and indexes - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_DEAD_OBJECT:kotlin.Int` if the AudioTrack is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next write() - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR:kotlin.Int` in case of other error |

### write

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(
    audioData: ByteBuffer, 
    sizeInBytes: Int, 
    writeMode: Int, 
    timestamp: Long
): Int
```

Writes the audio data to the audio sink for playback in streaming mode on a HW_AV_SYNC track. The blocking behavior will depend on the write mode.

| Parameters ||
|---|---|
| `audioData` | [ByteBuffer](../java.nio/ByteBuffer.md): the buffer that holds the data to write, starting at the position reported by `audioData.position()`. Note that upon return, the buffer position (`audioData.position()`) will have been advanced to reflect the amount of data that was successfully written to the AudioTrack. This value cannot be `null`. |
| `sizeInBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of bytes to write. It is recommended but not enforced that the number of bytes requested be a multiple of the frame size (sample size in bytes multiplied by the channel count). Note this may differ from `audioData.remaining()`, but cannot exceed it. |
| `writeMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`. With `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, the write will block until all data has been written to the audio sink. With `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`, the write will return immediately after queuing as much audio data for playback as possible without blocking. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int` |
| --- | --- |
| `timestamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The timestamp, in nanoseconds, of the first decodable audio frame in the provided audioData. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | zero or the positive number of bytes that were written, or one of the following error codes. - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` if the track isn't properly initialized - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` if the parameters don't resolve to valid data and indexes - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_DEAD_OBJECT:kotlin.Int` if the AudioTrack is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next write() - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR:kotlin.Int` in case of other error |

### write

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(
    audioData: ShortArray, 
    offsetInShorts: Int, 
    sizeInShorts: Int
): Int
```

Writes the audio data to the audio sink for playback (streaming mode), or copies audio data for later playback (static buffer mode). The format specified in the AudioTrack constructor should be `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int` to correspond to the data in the array.

In streaming mode, the write will normally block until all the data has been enqueued for playback, and will return a full transfer count. However, if the track is stopped or paused on entry, or another thread interrupts the write by calling stop or pause, or an I/O error occurs during the write, then the write may return a short transfer count.

In static buffer mode, copies the data to the buffer starting at offset 0. Note that the actual playback of this data might occur after this function returns.

| Parameters ||
|---|---|
| `audioData` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the array that holds the data to play. This value cannot be `null`. |
| `offsetInShorts` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset expressed in shorts in audioData where the data to play starts. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInShorts` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of shorts to read in audioData after the offset. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | zero or the positive number of shorts that were written, or one of the following error codes. The number of shorts will be a multiple of the channel count not to exceed sizeInShorts. - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` if the track isn't properly initialized - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` if the parameters don't resolve to valid data and indexes - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_DEAD_OBJECT:kotlin.Int` if the AudioTrack is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next write() - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR:kotlin.Int` in case of other error This is equivalent to write with `writeMode` set to `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`. |

### write

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(
    audioData: ShortArray, 
    offsetInShorts: Int, 
    sizeInShorts: Int, 
    writeMode: Int
): Int
```

Writes the audio data to the audio sink for playback (streaming mode), or copies audio data for later playback (static buffer mode). The format specified in the AudioTrack constructor should be `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int` to correspond to the data in the array.

In streaming mode, the blocking behavior depends on the write mode. If the write mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, the write will normally block until all the data has been enqueued for playback, and will return a full transfer count. However, if the write mode is `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`, or the track is stopped or paused on entry, or another thread interrupts the write by calling stop or pause, or an I/O error occurs during the write, then the write may return a short transfer count.

In static buffer mode, copies the data to the buffer starting at offset 0. Note that the actual playback of this data might occur after this function returns.

| Parameters ||
|---|---|
| `audioData` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the array that holds the data to write. This value cannot be `null`. |
| `offsetInShorts` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset expressed in shorts in audioData where the data to write starts. Must not be negative, or cause the data access to go out of bounds of the array. |
| `sizeInShorts` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of shorts to read in audioData after the offset. Must not be negative, or cause the data access to go out of bounds of the array. |
| --- | --- |
| `writeMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`. It has no effect in static mode. With `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int`, the write will block until all data has been written to the audio sink. With `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int`, the write will return immediately after queuing as much audio data for playback as possible without blocking. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_BLOCKING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#WRITE_NON_BLOCKING:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | zero or the positive number of shorts that were written, or one of the following error codes. The number of shorts will be a multiple of the channel count not to exceed sizeInShorts. - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_INVALID_OPERATION:kotlin.Int` if the track isn't properly initialized - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_BAD_VALUE:kotlin.Int` if the parameters don't resolve to valid data and indexes - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR_DEAD_OBJECT:kotlin.Int` if the AudioTrack is not valid anymore and needs to be recreated. The dead object error code is not returned if some data was successfully transferred. In this case, the error is returned at the next write() - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ERROR:kotlin.Int` in case of other error |

## Protected methods

### finalize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |

### getNativeFrameCount

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getNativeFrameCount(): Int
```

**Deprecated:** *Use the identical public method getBufferSizeInFrames instead.*

Returns the frame count of the native `AudioTrack` buffer.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | current size in frames of the `AudioTrack` buffer. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | |

### setState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setState(state: Int): Unit
```

**Deprecated:** *Only accessible by subclasses, which are not recommended for AudioTrack.*

Sets the initialization state of the instance. This method was originally intended to be used in an AudioTrack subclass constructor to set a subclass-specific post-initialization state. However, subclasses of AudioTrack are no longer recommended, so this method is obsolete.

| Parameters ||
|---|---|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the state of the AudioTrack instance |
