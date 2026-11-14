# MediaPlayer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaPlayer

Kotlin| [Java](../android/media/MediaPlayer.md) 
| --- | --- |

```
open class MediaPlayer : AudioRouting, VolumeAutomation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaPlayer](../android/media/MediaPlayer.md) |

MediaPlayer class can be used to control playback of audio/video files and streams.

MediaPlayer is not thread-safe. Creation of and all access to player instances should be on the same thread. If registering [callbacks](../android/media/MediaPlayer.md), the thread must have a Looper.

Topics covered here are:

1. [State Diagram](../android/media/MediaPlayer.md)
2. [Valid and Invalid States](../android/media/MediaPlayer.md)
3. [Permissions](../android/media/MediaPlayer.md)
4. [Register informational and error callbacks](../android/media/MediaPlayer.md)

| ### Developer Guides
|
| For more information about how to use MediaPlayer, read the [Media Playback](https://developer.android.com/guide/topics/media/mediaplayer.html) developer guide.

### State Diagram

Playback control of audio/video files and streams is managed as a state machine. The following diagram shows the life cycle and the states of a MediaPlayer object driven by the supported playback control operations. The ovals represent the states a MediaPlayer object may reside in. The arcs represent the playback control operations that drive the object state transition. There are two types of arcs. The arcs with a single arrow head represent synchronous method calls, while those with a double arrow head represent asynchronous method calls.

<br />

From this state diagram, one can see that a MediaPlayer object has the following states:

- When a MediaPlayer object is just created using`new`or after [reset()](../android/media/MediaPlayer.md))is called, it is in the*Idle* state; and after [release()](../android/media/MediaPlayer.md))is called, it is in the*End* state. Between these two states is the life cycle of the MediaPlayer object.
 - There is a subtle but important difference between a newly constructed MediaPlayer object and the MediaPlayer object after [reset()](../android/media/MediaPlayer.md))is called. It is a programming error to invoke methods such as [getCurrentPosition()](../android/media/MediaPlayer.md)), [getDuration()](../android/media/MediaPlayer.md)), [getVideoHeight()](../android/media/MediaPlayer.md)), [getVideoWidth()](../android/media/MediaPlayer.md)), [setAudioAttributes(android.media.AudioAttributes)](../android/media/MediaPlayer.md)), [setLooping(boolean)](../android/media/MediaPlayer.md)), [setVolume(float,float)](../android/media/MediaPlayer.md)), [pause()](../android/media/MediaPlayer.md)), [start()](../android/media/MediaPlayer.md)), [stop()](../android/media/MediaPlayer.md)), [seekTo(long,int)](../android/media/MediaPlayer.md)), [prepare()](../android/media/MediaPlayer.md))or [prepareAsync()](../android/media/MediaPlayer.md))in the*Idle* state for both cases. If any of these methods is called right after a MediaPlayer object is constructed, the user supplied callback method OnErrorListener.onError() won't be called by the internal player engine and the object state remains unchanged; but if these methods are called right after [reset()](../android/media/MediaPlayer.md)), the user supplied callback method OnErrorListener.onError() will be invoked by the internal player engine and the object will be transfered to the*Error*state.
 - You must keep a reference to a MediaPlayer instance to prevent it from being garbage collected. If a MediaPlayer instance is garbage collected, [release](../android/media/MediaPlayer.md))will be called, causing any ongoing playback to stop.
 - You must call [release()](../android/media/MediaPlayer.md))once you have finished using an instance to release acquired resources, such as memory and codecs. Once you have called [release](../android/media/MediaPlayer.md)), you must no longer interact with the released instance.
 - MediaPlayer objects created using`new`is in the*Idle* state, while those created with one of the overloaded convenient`create`methods are*NOT* in the*Idle* state. In fact, the objects are in the*Prepared* state if the creation using`create`method is successful.
- In general, some playback control operation may fail due to various reasons, such as unsupported audio/video format, poorly interleaved audio/video, resolution too high, streaming timeout, and the like. Thus, error reporting and recovery is an important concern under these circumstances. Sometimes, due to programming errors, invoking a playback control operation in an invalid state may also occur. Under all these error conditions, the internal player engine invokes a user supplied OnErrorListener.onError() method if an OnErrorListener has been registered beforehand via [setOnErrorListener(android.media.MediaPlayer.OnErrorListener)](../android/media/MediaPlayer.md)).
 - It is important to note that once an error occurs, the MediaPlayer object enters the*Error*state (except as noted above), even if an error listener has not been registered by the application.
 - In order to reuse a MediaPlayer object that is in the*Error* state and recover from the error, [reset()](../android/media/MediaPlayer.md))can be called to restore the object to its*Idle*state.
 - It is good programming practice to have your application register a OnErrorListener to look out for error notifications from the internal player engine.
 - IllegalStateException is thrown to prevent programming errors such as calling [prepare()](../android/media/MediaPlayer.md)), [prepareAsync()](../android/media/MediaPlayer.md)), or one of the overloaded`setDataSource `methods in an invalid state.
- Calling [setDataSource(java.io.FileDescriptor)](../android/media/MediaPlayer.md)), or [setDataSource(java.lang.String)](../android/media/MediaPlayer.md)), or [setDataSource(android.content.Context,android.net.Uri)](../android/media/MediaPlayer.md)), or [setDataSource(java.io.FileDescriptor,long,long)](../android/media/MediaPlayer.md)), or [setDataSource(android.media.MediaDataSource)](../android/media/MediaPlayer.md))transfers a MediaPlayer object in the*Idle* state to the*Initialized* state.
 - An IllegalStateException is thrown if setDataSource() is called in any other state.
 - It is good programming practice to always look out for`IllegalArgumentException`and`IOException`that may be thrown from the overloaded`setDataSource`methods.
- A MediaPlayer object must first enter the*Prepared* state before playback can be started.
 - There are two ways (synchronous vs. asynchronous) that the*Prepared* state can be reached: either a call to [prepare()](../android/media/MediaPlayer.md))(synchronous) which transfers the object to the*Prepared* state once the method call returns, or a call to [prepareAsync()](../android/media/MediaPlayer.md))(asynchronous) which first transfers the object to the*Preparing* state after the call returns (which occurs almost right away) while the internal player engine continues working on the rest of preparation work until the preparation work completes. When the preparation completes or when [prepare()](../android/media/MediaPlayer.md))call returns, the internal player engine then calls a user supplied callback method, onPrepared() of the OnPreparedListener interface, if an OnPreparedListener is registered beforehand via [setOnPreparedListener(android.media.MediaPlayer.OnPreparedListener)](../android/media/MediaPlayer.md)).
 - It is important to note that the*Preparing* state is a transient state, and the behavior of calling any method with side effect while a MediaPlayer object is in the*Preparing*state is undefined.
 - An IllegalStateException is thrown if [prepare()](../android/media/MediaPlayer.md))or [prepareAsync()](../android/media/MediaPlayer.md))is called in any other state.
 - While in the*Prepared*state, properties such as audio/sound volume, screenOnWhilePlaying, looping can be adjusted by invoking the corresponding set methods.
- To start the playback, [start()](../android/media/MediaPlayer.md))must be called. After [start()](../android/media/MediaPlayer.md))returns successfully, the MediaPlayer object is in the*Started* state. [isPlaying()](../android/media/MediaPlayer.md))can be called to test whether the MediaPlayer object is in the*Started* state.
 - While in the*Started* state, the internal player engine calls a user supplied OnBufferingUpdateListener.onBufferingUpdate() callback method if a OnBufferingUpdateListener has been registered beforehand via [setOnBufferingUpdateListener(android.media.MediaPlayer.OnBufferingUpdateListener)](../android/media/MediaPlayer.md)). This callback allows applications to keep track of the buffering status while streaming audio/video.
 - Calling [start()](../android/media/MediaPlayer.md))has no effect on a MediaPlayer object that is already in the*Started*state.
- Playback can be paused and stopped, and the current playback position can be adjusted. Playback can be paused via [pause()](../android/media/MediaPlayer.md)). When the call to [pause()](../android/media/MediaPlayer.md))returns, the MediaPlayer object enters the*Paused* state. Note that the transition from the*Started* state to the*Paused* state and vice versa happens asynchronously in the player engine. It may take some time before the state is updated in calls to [isPlaying()](../android/media/MediaPlayer.md)), and it can be a number of seconds in the case of streamed content.
 - Calling [start()](../android/media/MediaPlayer.md))to resume playback for a paused MediaPlayer object, and the resumed playback position is the same as where it was paused. When the call to [start()](../android/media/MediaPlayer.md))returns, the paused MediaPlayer object goes back to the*Started*state.
 - Calling [pause()](../android/media/MediaPlayer.md))has no effect on a MediaPlayer object that is already in the*Paused*state.
- Calling [stop()](../android/media/MediaPlayer.md))stops playback and causes a MediaPlayer in the*Started* ,*Paused* ,*Prepared* or*PlaybackCompleted* state to enter the*Stopped* state.
 - Once in the*Stopped* state, playback cannot be started until [prepare()](../android/media/MediaPlayer.md))or [prepareAsync()](../android/media/MediaPlayer.md))are called to set the MediaPlayer object to the*Prepared*state again.
 - Calling [stop()](../android/media/MediaPlayer.md))has no effect on a MediaPlayer object that is already in the*Stopped*state.
- The playback position can be adjusted with a call to [seekTo(long,int)](../android/media/MediaPlayer.md)).
 - Although the asynchronuous [seekTo(long,int)](../android/media/MediaPlayer.md))call returns right away, the actual seek operation may take a while to finish, especially for audio/video being streamed. When the actual seek operation completes, the internal player engine calls a user supplied OnSeekComplete.onSeekComplete() if an OnSeekCompleteListener has been registered beforehand via [setOnSeekCompleteListener(android.media.MediaPlayer.OnSeekCompleteListener)](../android/media/MediaPlayer.md)).
 - Please note that [seekTo(long,int)](../android/media/MediaPlayer.md))can also be called in the other states, such as*Prepared* ,*Paused* and*PlaybackCompleted* state. When [seekTo(long,int)](../android/media/MediaPlayer.md))is called in those states, one video frame will be displayed if the stream has video and the requested position is valid.
 - Furthermore, the actual current playback position can be retrieved with a call to [getCurrentPosition()](../android/media/MediaPlayer.md)), which is helpful for applications such as a Music player that need to keep track of the playback progress.
- When the playback reaches the end of stream, the playback completes.
 - If the looping mode was being set to true with [setLooping(boolean)](../android/media/MediaPlayer.md)), the MediaPlayer object shall remain in the*Started*state.
 - If the looping mode was set to false , the player engine calls a user supplied callback method, OnCompletion.onCompletion(), if a OnCompletionListener is registered beforehand via [setOnCompletionListener(android.media.MediaPlayer.OnCompletionListener)](../android/media/MediaPlayer.md)). The invoke of the callback signals that the object is now in the*PlaybackCompleted*state.
 - While in the*PlaybackCompleted* state, calling [start()](../android/media/MediaPlayer.md))can restart the playback from the beginning of the audio/video source.

 ### Valid and invalid states

 | Method Name <br /> | Valid States <br /> | Invalid States <br /> | Comments <br /> |
| --- | --- | --- | --- |
 | attachAuxEffect <br /> | {Initialized, Prepared, Started, Paused, Stopped, PlaybackCompleted} <br /> | {Idle, Error} <br /> | This method must be called after setDataSource. Calling it does not change the object state. <br /> |
 | getAudioSessionId <br /> | any <br /> | {} <br /> | This method can be called in any state and calling it does not change the object state. <br /> |
 | getCurrentPosition <br /> | {Idle, Initialized, Prepared, Started, Paused, Stopped, PlaybackCompleted} <br /> | {Error} <br /> | Successful invoke of this method in a valid state does not change the state. Calling this method in an invalid state transfers the object to the*Error* state. <br /> |
| --- | --- | --- | --- |
 | getDuration <br /> | {Prepared, Started, Paused, Stopped, PlaybackCompleted} <br /> | {Idle, Initialized, Error} <br /> | Successful invoke of this method in a valid state does not change the state. Calling this method in an invalid state transfers the object to the*Error* state. <br /> |
 | getVideoHeight <br /> | {Idle, Initialized, Prepared, Started, Paused, Stopped, PlaybackCompleted} <br /> | {Error} <br /> | Successful invoke of this method in a valid state does not change the state. Calling this method in an invalid state transfers the object to the*Error* state. <br /> |
 | getVideoWidth <br /> | {Idle, Initialized, Prepared, Started, Paused, Stopped, PlaybackCompleted} <br /> | {Error} <br /> | Successful invoke of this method in a valid state does not change the state. Calling this method in an invalid state transfers the object to the*Error* state. <br /> |
| --- | --- | --- | --- |
 | isPlaying <br /> | {Idle, Initialized, Prepared, Started, Paused, Stopped, PlaybackCompleted} <br /> | {Error} <br /> | Successful invoke of this method in a valid state does not change the state. Calling this method in an invalid state transfers the object to the*Error* state. <br /> |
 | pause <br /> | {Started, Paused, PlaybackCompleted} <br /> | {Idle, Initialized, Prepared, Stopped, Error} <br /> | Successful invoke of this method in a valid state transfers the object to the*Paused* state. Calling this method in an invalid state transfers the object to the*Error* state. <br /> |
 | prepare <br /> | {Initialized, Stopped} <br /> | {Idle, Prepared, Started, Paused, PlaybackCompleted, Error} <br /> | Successful invoke of this method in a valid state transfers the object to the*Prepared* state. Calling this method in an invalid state throws an IllegalStateException. <br /> |
| --- | --- | --- | --- |
 | prepareAsync <br /> | {Initialized, Stopped} <br /> | {Idle, Prepared, Started, Paused, PlaybackCompleted, Error} <br /> | Successful invoke of this method in a valid state transfers the object to the*Preparing* state. Calling this method in an invalid state throws an IllegalStateException. <br /> |
 | release <br /> | any <br /> | {} <br /> | After [release()](../android/media/MediaPlayer.md)), you must not interact with the object. <br /> |
 | reset <br /> | {Idle, Initialized, Prepared, Started, Paused, Stopped, PlaybackCompleted, Error} <br /> | {} <br /> | After [reset()](../android/media/MediaPlayer.md)), the object is like being just created. <br /> |
| --- | --- | --- | --- |
 | seekTo <br /> | {Prepared, Started, Paused, PlaybackCompleted} <br /> | {Idle, Initialized, Stopped, Error} <br /> | Successful invoke of this method in a valid state does not change the state. Calling this method in an invalid state transfers the object to the*Error* state. <br /> |
 | setAudioAttributes <br /> | {Idle, Initialized, Stopped, Prepared, Started, Paused, PlaybackCompleted} <br /> | {Error} <br /> | Successful invoke of this method does not change the state. In order for the target audio attributes type to become effective, this method must be called before prepare() or prepareAsync(). <br /> |
 | setAudioSessionId <br /> | {Idle} <br /> | {Initialized, Prepared, Started, Paused, Stopped, PlaybackCompleted, Error} <br /> | This method must be called in idle state as the audio session ID must be known before calling setDataSource. Calling it does not change the object state. <br /> |
| --- | --- | --- | --- |
 | setAudioStreamType (deprecated) <br /> | {Idle, Initialized, Stopped, Prepared, Started, Paused, PlaybackCompleted} <br /> | {Error} <br /> | Successful invoke of this method does not change the state. In order for the target audio stream type to become effective, this method must be called before prepare() or prepareAsync(). <br /> |
 | setAuxEffectSendLevel <br /> | any <br /> | {} <br /> | Calling this method does not change the object state. <br /> |
 | setDataSource <br /> | {Idle} <br /> | {Initialized, Prepared, Started, Paused, Stopped, PlaybackCompleted, Error} <br /> | Successful invoke of this method in a valid state transfers the object to the*Initialized* state. Calling this method in an invalid state throws an IllegalStateException. <br /> |
| --- | --- | --- | --- |
 | setDisplay <br /> | any <br /> | {} <br /> | This method can be called in any state and calling it does not change the object state. <br /> |
 | setSurface <br /> | any <br /> | {} <br /> | This method can be called in any state and calling it does not change the object state. <br /> |
 | setVideoScalingMode <br /> | {Initialized, Prepared, Started, Paused, Stopped, PlaybackCompleted} <br /> | {Idle, Error} <br /> | Successful invoke of this method does not change the state. <br /> |
| --- | --- | --- | --- |
 | setLooping <br /> | {Idle, Initialized, Stopped, Prepared, Started, Paused, PlaybackCompleted} <br /> | {Error} <br /> | Successful invoke of this method in a valid state does not change the state. Calling this method in an invalid state transfers the object to the*Error* state. <br /> |
 | isLooping <br /> | any <br /> | {} <br /> | This method can be called in any state and calling it does not change the object state. <br /> |
 | setOnBufferingUpdateListener <br /> | any <br /> | {} <br /> | This method can be called in any state and calling it does not change the object state. <br /> |
| --- | --- | --- | --- |
 | setOnCompletionListener <br /> | any <br /> | {} <br /> | This method can be called in any state and calling it does not change the object state. <br /> |
 | setOnErrorListener <br /> | any <br /> | {} <br /> | This method can be called in any state and calling it does not change the object state. <br /> |
 | setOnPreparedListener <br /> | any <br /> | {} <br /> | This method can be called in any state and calling it does not change the object state. <br /> |
| --- | --- | --- | --- |
 | setOnSeekCompleteListener <br /> | any <br /> | {} <br /> | This method can be called in any state and calling it does not change the object state. <br /> |
 | setPlaybackParams <br /> | {Initialized, Prepared, Started, Paused, PlaybackCompleted, Error} <br /> | {Idle, Stopped} <br /> | This method will change state in some cases, depending on when it's called. <br /> |
 | setScreenOnWhilePlaying | any <br /> | {} <br /> | This method can be called in any state and calling it does not change the object state. <br /> |
| --- | --- | --- | --- |
 | setVolume <br /> | {Idle, Initialized, Stopped, Prepared, Started, Paused, PlaybackCompleted} <br /> | {Error} <br /> | Successful invoke of this method does not change the state. |
 | setWakeMode <br /> | any <br /> | {} <br /> | This method can be called in any state and calling it does not change the object state. <br /> |
 | start <br /> | {Prepared, Started, Paused, PlaybackCompleted} <br /> | {Idle, Initialized, Stopped, Error} <br /> | Successful invoke of this method in a valid state transfers the object to the*Started* state. Calling this method in an invalid state transfers the object to the*Error* state. <br /> |
| --- | --- | --- | --- |
 | stop <br /> | {Prepared, Started, Stopped, Paused, PlaybackCompleted} <br /> | {Idle, Initialized, Error} <br /> | Successful invoke of this method in a valid state transfers the object to the*Stopped* state. Calling this method in an invalid state transfers the object to the*Error* state. <br /> |
 | getTrackInfo <br /> | {Prepared, Started, Stopped, Paused, PlaybackCompleted} <br /> | {Idle, Initialized, Error} <br /> | Successful invoke of this method does not change the state. <br /> |
 | addTimedTextSource <br /> | {Prepared, Started, Stopped, Paused, PlaybackCompleted} <br /> | {Idle, Initialized, Error} <br /> | Successful invoke of this method does not change the state. <br /> |
| --- | --- | --- | --- |
 | selectTrack <br /> | {Prepared, Started, Stopped, Paused, PlaybackCompleted} <br /> | {Idle, Initialized, Error} <br /> | Successful invoke of this method does not change the state. <br /> |
 | deselectTrack <br /> | {Prepared, Started, Stopped, Paused, PlaybackCompleted} <br /> | {Idle, Initialized, Error} <br /> | Successful invoke of this method does not change the state. <br /> |

 ### Permissions

 One may need to declare a corresponding WAKE_LOCK permission [<uses-permission>](../android/R.styleable.md) element.

 This class requires the [android.Manifest.permission#INTERNET](../android/Manifest.permission.md) permission when used with network-based content.

 ### Callbacks

 Applications may want to register for informational and error events in order to be informed of some internal state update and possible runtime errors during playback or streaming. Registration for these events is done by properly setting the appropriate listeners (via calls to [setOnPreparedListener](../android/media/MediaPlayer.md)), [setOnVideoSizeChangedListener](../android/media/MediaPlayer.md)), [setOnSeekCompleteListener](../android/media/MediaPlayer.md)), [setOnCompletionListener](../android/media/MediaPlayer.md)), [setOnBufferingUpdateListener](../android/media/MediaPlayer.md)), [setOnInfoListener](../android/media/MediaPlayer.md)), [setOnErrorListener](../android/media/MediaPlayer.md)), etc). In order to receive the respective callback associated with these listeners, applications are required to create MediaPlayer objects on a thread with its own Looper running (main UI thread by default has a Looper running).

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [DrmInfo](../android/media/MediaPlayer.DrmInfo.md) Encapsulates the DRM properties of the source. |
| | [MetricsConstants](../android/media/MediaPlayer.MetricsConstants.md) <br /> |
| | [NoDrmSchemeException](../android/media/MediaPlayer.NoDrmSchemeException.md) Thrown when a DRM method is called before preparing a DRM scheme through prepareDrm(). |
| --- | --- |
| abstract | [OnBufferingUpdateListener](../android/media/MediaPlayer.OnBufferingUpdateListener.md) Interface definition of a callback to be invoked indicating buffering status of a media resource being streamed over the network. |
| abstract | [OnCompletionListener](../android/media/MediaPlayer.OnCompletionListener.md) Interface definition for a callback to be invoked when playback of a media source has completed. |
| abstract | [OnDrmConfigHelper](../android/media/MediaPlayer.OnDrmConfigHelper.md) Interface definition of a callback to be invoked when the app can do DRM configuration (get/set properties) before the session is opened. |
| --- | --- |
| abstract | [OnDrmInfoListener](../android/media/MediaPlayer.OnDrmInfoListener.md) Interface definition of a callback to be invoked when the DRM info becomes available |
| abstract | [OnDrmPreparedListener](../android/media/MediaPlayer.OnDrmPreparedListener.md) Interface definition of a callback to notify the app when the DRM is ready for key request/response |
| abstract | [OnErrorListener](../android/media/MediaPlayer.OnErrorListener.md) Interface definition of a callback to be invoked when there has been an error during an asynchronous operation (other errors will throw exceptions at method call time). |
| --- | --- |
| abstract | [OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) Interface definition of a callback to be invoked to communicate some info and/or warning about the media or its playback. |
| abstract | [OnMediaTimeDiscontinuityListener](../android/media/MediaPlayer.OnMediaTimeDiscontinuityListener.md) Interface definition of a callback to be invoked when discontinuity in the normal progression of the media time is detected. |
| abstract | [OnPreparedListener](../android/media/MediaPlayer.OnPreparedListener.md) Interface definition for a callback to be invoked when the media source is ready for playback. |
| --- | --- |
| abstract | [OnSeekCompleteListener](../android/media/MediaPlayer.OnSeekCompleteListener.md) Interface definition of a callback to be invoked indicating the completion of a seek operation. |
| abstract | [OnSubtitleDataListener](../android/media/MediaPlayer.OnSubtitleDataListener.md) Interface definition of a callback to be invoked when a player subtitle track has new subtitle data available. |
| abstract | [OnTimedMetaDataAvailableListener](../android/media/MediaPlayer.OnTimedMetaDataAvailableListener.md) Interface definition of a callback to be invoked when a track has timed metadata available. |
| --- | --- |
| abstract | [OnTimedTextListener](../android/media/MediaPlayer.OnTimedTextListener.md) Interface definition of a callback to be invoked when a timed text is available for display. |
| abstract | [OnVideoSizeChangedListener](../android/media/MediaPlayer.OnVideoSizeChangedListener.md) Interface definition of a callback to be invoked when the video size is first known or updated |
| | [ProvisioningNetworkErrorException](../android/media/MediaPlayer.ProvisioningNetworkErrorException.md) Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to a network error (Internet reachability, timeout, etc.). |
| --- | --- |
| | [ProvisioningServerErrorException](../android/media/MediaPlayer.ProvisioningServerErrorException.md) Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to the provisioning server denying the request. |
| open | [TrackInfo](../android/media/MediaPlayer.TrackInfo.md) Class for MediaPlayer to return each audio/video/subtitle track's metadata. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_ERROR_IO](../android/media/MediaPlayer.md) File or network related operation errors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_ERROR_MALFORMED](../android/media/MediaPlayer.md) Bitstream is not conforming to the related coding standard or file spec. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_ERROR_NOT_VALID_FOR_PROGRESSIVE_PLAYBACK](../android/media/MediaPlayer.md) The video is streamed and its container is not valid for progressive playback i. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_ERROR_SERVER_DIED](../android/media/MediaPlayer.md) Media server died. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_ERROR_TIMED_OUT](../android/media/MediaPlayer.md) Some operation takes too long to complete, usually more than 3-5 seconds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_ERROR_UNKNOWN](../android/media/MediaPlayer.md) Unspecified media player error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_ERROR_UNSUPPORTED](../android/media/MediaPlayer.md) Bitstream is conforming to the related coding standard or file spec, but the media framework does not support the feature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_AUDIO_NOT_PLAYING](../android/media/MediaPlayer.md) Informs that audio is not playing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_BAD_INTERLEAVING](../android/media/MediaPlayer.md) Bad interleaving means that a media has been improperly interleaved or not interleaved at all, e. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_BUFFERING_END](../android/media/MediaPlayer.md) MediaPlayer is resuming playback after filling buffers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_BUFFERING_START](../android/media/MediaPlayer.md) MediaPlayer is temporarily pausing playback internally in order to buffer more data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_METADATA_UPDATE](../android/media/MediaPlayer.md) A new set of metadata is available. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_NOT_SEEKABLE](../android/media/MediaPlayer.md) The media cannot be seeked (e.g live stream) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_STARTED_AS_NEXT](../android/media/MediaPlayer.md) The player was started because it was used as the next player for another player, which just completed playback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_SUBTITLE_TIMED_OUT](../android/media/MediaPlayer.md) Reading the subtitle track takes too long. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_UNKNOWN](../android/media/MediaPlayer.md) Unspecified media player info. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_UNSUPPORTED_SUBTITLE](../android/media/MediaPlayer.md) Subtitle track was not supported by the media framework. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_VIDEO_NOT_PLAYING](../android/media/MediaPlayer.md) Informs that video is not playing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_VIDEO_RENDERING_START](../android/media/MediaPlayer.md) The player just pushed the very first video frame for rendering. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIA_INFO_VIDEO_TRACK_LAGGING](../android/media/MediaPlayer.md) The video is too complex for the decoder: it can't decode frames fast enough. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_MIMETYPE_TEXT_SUBRIP](../android/media/MediaPlayer.md) MIME type for SubRip (SRT) container. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREPARE_DRM_STATUS_PREPARATION_ERROR](../android/media/MediaPlayer.md) The DRM preparation has failed . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREPARE_DRM_STATUS_PROVISIONING_NETWORK_ERROR](../android/media/MediaPlayer.md) The device required DRM provisioning but couldn't reach the provisioning server. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREPARE_DRM_STATUS_PROVISIONING_SERVER_ERROR](../android/media/MediaPlayer.md) The device required DRM provisioning but the provisioning server denied the request. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREPARE_DRM_STATUS_SUCCESS](../android/media/MediaPlayer.md) The status codes for [OnDrmPreparedListener.onDrmPrepared](../android/media/MediaPlayer.OnDrmPreparedListener.md))listener. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEEK_CLOSEST](../android/media/MediaPlayer.md) This mode is used with [seekTo(long,int)](../android/media/MediaPlayer.md))to move media position to a frame (not necessarily a key frame) associated with a data source that is located closest to or at the given time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEEK_CLOSEST_SYNC](../android/media/MediaPlayer.md) This mode is used with [seekTo(long,int)](../android/media/MediaPlayer.md))to move media position to a sync (or key) frame associated with a data source that is located closest to (in time) or at the given time. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEEK_NEXT_SYNC](../android/media/MediaPlayer.md) This mode is used with [seekTo(long,int)](../android/media/MediaPlayer.md))to move media position to a sync (or key) frame associated with a data source that is located right after or at the given time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEEK_PREVIOUS_SYNC](../android/media/MediaPlayer.md) This mode is used with [seekTo(long,int)](../android/media/MediaPlayer.md))to move media position to a sync (or key) frame associated with a data source that is located right before or at the given time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_SCALING_MODE_SCALE_TO_FIT](../android/media/MediaPlayer.md) Specifies a video scaling mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_SCALING_MODE_SCALE_TO_FIT_WITH_CROPPING](../android/media/MediaPlayer.md) Specifies a video scaling mode. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaPlayer](../android/media/MediaPlayer.md))`()` Default constructor. |
| [MediaPlayer](../android/media/MediaPlayer.md))`(`context:` ` [Context](../android/content/Context.md)`)` Default constructor with context. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnRoutingChangedListener](../android/media/MediaPlayer.md))`(`listener:` ` [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!`, `handler:` ` [Handler](../android/os/Handler.md)!`)` Adds an [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) to receive notifications of routing changes on this MediaPlayer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTimedTextSource](../android/media/MediaPlayer.md))`(`context:` ` [Context](../android/content/Context.md)!`, `uri:` ` [Uri](../android/net/Uri.md)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adds an external timed text source file (Uri). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTimedTextSource](../android/media/MediaPlayer.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adds an external timed text source file (FileDescriptor). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTimedTextSource](../android/media/MediaPlayer.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`, `offset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `mime:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adds an external timed text file (FileDescriptor). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTimedTextSource](../android/media/MediaPlayer.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adds an external timed text source file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachAuxEffect](../android/media/MediaPlayer.md))`(`effectId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attaches an auxiliary effect to the player. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearOnMediaTimeDiscontinuityListener](../android/media/MediaPlayer.md))`()` Clears the listener previously set with [setOnMediaTimeDiscontinuityListener(android.media.MediaPlayer.OnMediaTimeDiscontinuityListener)](../android/media/MediaPlayer.md))or [setOnMediaTimeDiscontinuityListener(android.media.MediaPlayer.OnMediaTimeDiscontinuityListener,android.os.Handler)](../android/media/MediaPlayer.md)) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearOnSubtitleDataListener](../android/media/MediaPlayer.md))`()` Clears the listener previously set with [setOnSubtitleDataListener(android.media.MediaPlayer.OnSubtitleDataListener)](../android/media/MediaPlayer.md))or [setOnSubtitleDataListener(android.media.MediaPlayer.OnSubtitleDataListener,android.os.Handler)](../android/media/MediaPlayer.md)). |
| openstatic [MediaPlayer](../android/media/MediaPlayer.md)! | [create](../android/media/MediaPlayer.md))`(`context:` ` [Context](../android/content/Context.md)!`, `uri:` ` [Uri](../android/net/Uri.md)!`)` Convenience method to create a MediaPlayer for a given Uri. |
| --- | --- |
| openstatic [MediaPlayer](../android/media/MediaPlayer.md)! | [create](../android/media/MediaPlayer.md))`(`context:` ` [Context](../android/content/Context.md)!`, `uri:` ` [Uri](../android/net/Uri.md)!`, `holder:` ` [SurfaceHolder](../android/view/SurfaceHolder.md)!`)` Convenience method to create a MediaPlayer for a given Uri. |
| openstatic [MediaPlayer](../android/media/MediaPlayer.md)! | [create](../android/media/MediaPlayer.md))`(`context:` ` [Context](../android/content/Context.md)!`, `uri:` ` [Uri](../android/net/Uri.md)!`, `holder:` ` [SurfaceHolder](../android/view/SurfaceHolder.md)!`, `audioAttributes:` ` [AudioAttributes](../android/media/AudioAttributes.md)!`, `audioSessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same factory method as [create(android.content.Context,android.net.Uri,android.view.SurfaceHolder)](../android/media/MediaPlayer.md))but that lets you specify the audio attributes and session ID to be used by the new MediaPlayer instance. |
| openstatic [MediaPlayer](../android/media/MediaPlayer.md)! | [create](../android/media/MediaPlayer.md))`(`context:` ` [Context](../android/content/Context.md)!`, `resid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convenience method to create a MediaPlayer for a given resource id. |
| --- | --- |
| openstatic [MediaPlayer](../android/media/MediaPlayer.md)! | [create](../android/media/MediaPlayer.md))`(`context:` ` [Context](../android/content/Context.md)!`, `resid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioAttributes:` ` [AudioAttributes](../android/media/AudioAttributes.md)!`, `audioSessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same factory method as [create(android.content.Context,int)](../android/media/MediaPlayer.md))but that lets you specify the audio attributes and session ID to be used by the new MediaPlayer instance. |
| open [VolumeShaper](../android/media/VolumeShaper.md) | [createVolumeShaper](../android/media/MediaPlayer.md))`(`configuration:` ` [VolumeShaper.Configuration](../android/media/VolumeShaper.Configuration.md)`)` Returns a [VolumeShaper](../android/media/VolumeShaper.md) object that can be used modify the volume envelope of the player or track. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deselectTrack](../android/media/MediaPlayer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Deselect a track. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSessionId](../android/media/MediaPlayer.md))`()` Returns the audio session ID. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentPosition](../android/media/MediaPlayer.md))`()` Gets the current playback position. |
| open [MediaPlayer.DrmInfo](../android/media/MediaPlayer.DrmInfo.md)! | [getDrmInfo](../android/media/MediaPlayer.md))`()` Retrieves the DRM Info associated with the current source |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDrmPropertyString](../android/media/MediaPlayer.md))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Read a DRM engine plugin String property value, given the property name string. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDuration](../android/media/MediaPlayer.md))`()` Gets the duration of the file. |
| open [MediaDrm.KeyRequest](../android/media/MediaDrm.KeyRequest.md) | [getKeyRequest](../android/media/MediaPlayer.md))`(`keySetId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `initData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `keyType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `optionalParameters:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` A key request/response exchange occurs between the app and a license server to obtain or release keys used to decrypt encrypted content. |
| --- | --- |
| open [PersistableBundle](../android/os/PersistableBundle.md)! | [getMetrics](../android/media/MediaPlayer.md))`()` Return Metrics data about the current player. |
| open [PlaybackParams](../android/media/PlaybackParams.md) | [getPlaybackParams](../android/media/MediaPlayer.md))`()` Gets the playback params, containing the current playback rate. |
| open [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)! | [getPreferredDevice](../android/media/MediaPlayer.md))`()` Returns the selected output specified by [setPreferredDevice](../android/media/MediaPlayer.md)). |
| --- | --- |
| open [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)! | [getRoutedDevice](../android/media/MediaPlayer.md))`()` Returns an [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) identifying the current routing of this MediaPlayer Note: The query is only valid if the MediaPlayer is currently playing. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)!\> | [getRoutedDevices](../android/media/MediaPlayer.md))`()` Returns a List of [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) identifying the current routing of this MediaPlayer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSelectedTrack](../android/media/MediaPlayer.md))`(`trackType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the index of the audio, video, or subtitle track currently selected for playback, The return value is an index into the array returned by [getTrackInfo()](../android/media/MediaPlayer.md)), and can be used in calls to [selectTrack(int)](../android/media/MediaPlayer.md))or [deselectTrack(int)](../android/media/MediaPlayer.md)). |
| --- | --- |
| open [SyncParams](../android/media/SyncParams.md) | [getSyncParams](../android/media/MediaPlayer.md))`()` Gets the A/V sync mode. |
| open [MediaTimestamp](../android/media/MediaTimestamp.md)? | [getTimestamp](../android/media/MediaPlayer.md))`()` Get current playback position as a [MediaTimestamp](../android/media/MediaTimestamp.md). |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MediaPlayer.TrackInfo](../android/media/MediaPlayer.TrackInfo.md)!\>! | [getTrackInfo](../android/media/MediaPlayer.md))`()` Returns an array of track information. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVideoHeight](../android/media/MediaPlayer.md))`()` Returns the height of the video. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVideoWidth](../android/media/MediaPlayer.md))`()` Returns the width of the video. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLooping](../android/media/MediaPlayer.md))`()` Checks whether the MediaPlayer is looping or non-looping. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPlaying](../android/media/MediaPlayer.md))`()` Checks whether the MediaPlayer is playing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pause](../android/media/MediaPlayer.md))`()` Pauses playback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [prepare](../android/media/MediaPlayer.md))`()` Prepares the player for playback, synchronously. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [prepareAsync](../android/media/MediaPlayer.md))`()` Prepares the player for playback, asynchronously. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [prepareDrm](../android/media/MediaPlayer.md))`(`uuid:` ` [UUID](../java/util/UUID.md)`)` Prepares the DRM for the current source |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [provideKeyResponse](../android/media/MediaPlayer.md))`(`keySetId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `response:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` A key response is received from the license server by the app, then it is provided to the DRM engine plugin using provideKeyResponse. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](../android/media/MediaPlayer.md))`()` Releases resources associated with this MediaPlayer object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseDrm](../android/media/MediaPlayer.md))`()` Releases the DRM session |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnRoutingChangedListener](../android/media/MediaPlayer.md))`(`listener:` ` [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!`)` Removes an [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) which has been previously added to receive rerouting notifications. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../android/media/MediaPlayer.md))`()` Resets the MediaPlayer to its uninitialized state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreKeys](../android/media/MediaPlayer.md))`(`keySetId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Restore persisted offline keys into a new session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [seekTo](../android/media/MediaPlayer.md))`(`msec:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Seeks to specified time position. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [seekTo](../android/media/MediaPlayer.md))`(`msec:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Moves the media to specified time position by considering the given mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [selectTrack](../android/media/MediaPlayer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Selects a track. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAudioAttributes](../android/media/MediaPlayer.md))`(`attributes:` ` [AudioAttributes](../android/media/AudioAttributes.md)!`)` Sets the audio attributes for this MediaPlayer. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAudioSessionId](../android/media/MediaPlayer.md))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the audio session ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAudioStreamType](../android/media/MediaPlayer.md))`(`streamtype:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the audio stream type for this MediaPlayer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAuxEffectSendLevel](../android/media/MediaPlayer.md))`(`level:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the send level of the player to the attached auxiliary effect. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaPlayer.md))`(`context:` ` [Context](../android/content/Context.md)`, `uri:` ` [Uri](../android/net/Uri.md)`)` Sets the data source as a content Uri. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaPlayer.md))`(`context:` ` [Context](../android/content/Context.md)`, `uri:` ` [Uri](../android/net/Uri.md)`, `headers:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Sets the data source as a content Uri. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaPlayer.md))`(`context:` ` [Context](../android/content/Context.md)`, `uri:` ` [Uri](../android/net/Uri.md)`, `headers:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `cookies:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [HttpCookie](../java/net/HttpCookie.md)!>?`)` Sets the data source as a content Uri. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaPlayer.md))`(`afd:` ` [AssetFileDescriptor](../android/content/res/AssetFileDescriptor.md)`)` Sets the data source (AssetFileDescriptor) to use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaPlayer.md))`(`dataSource:` ` [MediaDataSource](../android/media/MediaDataSource.md)!`)` Sets the data source (MediaDataSource) to use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaPlayer.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`)` Sets the data source (FileDescriptor) to use. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaPlayer.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`, `offset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the data source (FileDescriptor) to use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaPlayer.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the data source (file-path or http/rtsp URL) to use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDisplay](../android/media/MediaPlayer.md))`(`sh:` ` [SurfaceHolder](../android/view/SurfaceHolder.md)!`)` Sets the [SurfaceHolder](../android/view/SurfaceHolder.md) to use for displaying the video portion of the media. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDrmPropertyString](../android/media/MediaPlayer.md))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Set a DRM engine plugin String property value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLooping](../android/media/MediaPlayer.md))`(`looping:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the player to be looping or non-looping. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNextMediaPlayer](../android/media/MediaPlayer.md))`(`next:` ` [MediaPlayer](../android/media/MediaPlayer.md)!`)` Set the MediaPlayer to start when this MediaPlayer finishes playback (i.e. reaches the end of the stream). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnBufferingUpdateListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnBufferingUpdateListener](../android/media/MediaPlayer.OnBufferingUpdateListener.md)!`)` Register a callback to be invoked when the status of a network stream's buffer has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnCompletionListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnCompletionListener](../android/media/MediaPlayer.OnCompletionListener.md)!`)` Register a callback to be invoked when the end of a media source has been reached during playback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDrmConfigHelper](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnDrmConfigHelper](../android/media/MediaPlayer.OnDrmConfigHelper.md)!`)` Register a callback to be invoked for configuration of the DRM object before the session is created. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDrmInfoListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnDrmInfoListener](../android/media/MediaPlayer.OnDrmInfoListener.md)!`)` Register a callback to be invoked when the DRM info is known. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDrmInfoListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnDrmInfoListener](../android/media/MediaPlayer.OnDrmInfoListener.md)!`, `handler:` ` [Handler](../android/os/Handler.md)!`)` Register a callback to be invoked when the DRM info is known. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDrmPreparedListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnDrmPreparedListener](../android/media/MediaPlayer.OnDrmPreparedListener.md)!`)` Register a callback to be invoked when the DRM object is prepared. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDrmPreparedListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnDrmPreparedListener](../android/media/MediaPlayer.OnDrmPreparedListener.md)!`, `handler:` ` [Handler](../android/os/Handler.md)!`)` Register a callback to be invoked when the DRM object is prepared. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnErrorListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnErrorListener](../android/media/MediaPlayer.OnErrorListener.md)!`)` Register a callback to be invoked when an error has happened during an asynchronous operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnInfoListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md)!`)` Register a callback to be invoked when an info/warning is available. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnMediaTimeDiscontinuityListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnMediaTimeDiscontinuityListener](../android/media/MediaPlayer.OnMediaTimeDiscontinuityListener.md)`)` Sets the listener to be invoked when a media time discontinuity is encountered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnMediaTimeDiscontinuityListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnMediaTimeDiscontinuityListener](../android/media/MediaPlayer.OnMediaTimeDiscontinuityListener.md)`, `handler:` ` [Handler](../android/os/Handler.md)`)` Sets the listener to be invoked when a media time discontinuity is encountered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreparedListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnPreparedListener](../android/media/MediaPlayer.OnPreparedListener.md)!`)` Register a callback to be invoked when the media source is ready for playback. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnSeekCompleteListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnSeekCompleteListener](../android/media/MediaPlayer.OnSeekCompleteListener.md)!`)` Register a callback to be invoked when a seek operation has been completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnSubtitleDataListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnSubtitleDataListener](../android/media/MediaPlayer.OnSubtitleDataListener.md)`)` Sets the listener to be invoked when a subtitle track has new data available. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnSubtitleDataListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnSubtitleDataListener](../android/media/MediaPlayer.OnSubtitleDataListener.md)`, `handler:` ` [Handler](../android/os/Handler.md)`)` Sets the listener to be invoked when a subtitle track has new data available. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnTimedMetaDataAvailableListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnTimedMetaDataAvailableListener](../android/media/MediaPlayer.OnTimedMetaDataAvailableListener.md)!`)` Register a callback to be invoked when a selected track has timed metadata available. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnTimedTextListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnTimedTextListener](../android/media/MediaPlayer.OnTimedTextListener.md)!`)` Register a callback to be invoked when a timed text is available for display. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnVideoSizeChangedListener](../android/media/MediaPlayer.md))`(`listener:` ` [MediaPlayer.OnVideoSizeChangedListener](../android/media/MediaPlayer.OnVideoSizeChangedListener.md)!`)` Register a callback to be invoked when the video size is known or updated. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlaybackParams](../android/media/MediaPlayer.md))`(`params:` ` [PlaybackParams](../android/media/PlaybackParams.md)`)` Sets playback rate using [PlaybackParams](../android/media/PlaybackParams.md). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredDevice](../android/media/MediaPlayer.md))`(`deviceInfo:` ` [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)!`)` Specifies an audio device (via an [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) object) to route the output from this MediaPlayer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScreenOnWhilePlaying](../android/media/MediaPlayer.md))`(`screenOn:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether we should use the attached SurfaceHolder to keep the screen on while video playback is occurring. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSurface](../android/media/MediaPlayer.md))`(`surface:` ` [Surface](../android/view/Surface.md)!`)` Sets the [Surface](../android/view/Surface.md) to be used as the sink for the video portion of the media. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSyncParams](../android/media/MediaPlayer.md))`(`params:` ` [SyncParams](../android/media/SyncParams.md)`)` Sets A/V sync mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVideoScalingMode](../android/media/MediaPlayer.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets video scaling mode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVolume](../android/media/MediaPlayer.md))`(`leftVolume:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `rightVolume:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the volume on this player. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWakeMode](../android/media/MediaPlayer.md))`(`context:` ` [Context](../android/content/Context.md)!`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the low-level power management behavior for this MediaPlayer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/media/MediaPlayer.md))`()` Starts or resumes playback. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](../android/media/MediaPlayer.md))`()` Stops playback after playback has been started or paused. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/media/MediaPlayer.md))`()` <br /> |

## Constants

### MEDIA_ERROR_IO

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_ERROR_IO: Int
```

File or network related operation errors. 

 Value: -1004

### MEDIA_ERROR_MALFORMED

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_ERROR_MALFORMED: Int
```

Bitstream is not conforming to the related coding standard or file spec. 

 Value: -1007

### MEDIA_ERROR_NOT_VALID_FOR_PROGRESSIVE_PLAYBACK

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_ERROR_NOT_VALID_FOR_PROGRESSIVE_PLAYBACK: Int
```

The video is streamed and its container is not valid for progressive playback i.e the video's index (e.g moov atom) is not at the start of the file. 

 Value: 200

**See Also**

- [android.media.MediaPlayer.OnErrorListener](../android/media/MediaPlayer.OnErrorListener.md) 

### MEDIA_ERROR_SERVER_DIED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_ERROR_SERVER_DIED: Int
```

Media server died. In this case, the application must release the MediaPlayer object and instantiate a new one. 

 Value: 100

**See Also**

- [android.media.MediaPlayer.OnErrorListener](../android/media/MediaPlayer.OnErrorListener.md) 

### MEDIA_ERROR_TIMED_OUT

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_ERROR_TIMED_OUT: Int
```

Some operation takes too long to complete, usually more than 3-5 seconds. 

 Value: -110

### MEDIA_ERROR_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_ERROR_UNKNOWN: Int
```

Unspecified media player error. 

 Value: 1

**See Also**

- [android.media.MediaPlayer.OnErrorListener](../android/media/MediaPlayer.OnErrorListener.md) 

### MEDIA_ERROR_UNSUPPORTED

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_ERROR_UNSUPPORTED: Int
```

Bitstream is conforming to the related coding standard or file spec, but the media framework does not support the feature. 

 Value: -1010

### MEDIA_INFO_AUDIO_NOT_PLAYING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_AUDIO_NOT_PLAYING: Int
```

Informs that audio is not playing. Note that playback of the video is not interrupted. 

 Value: 804

**See Also**

- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_INFO_BAD_INTERLEAVING

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_BAD_INTERLEAVING: Int
```

Bad interleaving means that a media has been improperly interleaved or not interleaved at all, e.g has all the video samples first then all the audio ones. Video is playing but a lot of disk seeks may be happening. 

 Value: 800

**See Also**

- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_INFO_BUFFERING_END

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_BUFFERING_END: Int
```

MediaPlayer is resuming playback after filling buffers. 

 Value: 702

**See Also**

- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_INFO_BUFFERING_START

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_BUFFERING_START: Int
```

MediaPlayer is temporarily pausing playback internally in order to buffer more data. 

 Value: 701

**See Also**

- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_INFO_METADATA_UPDATE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_METADATA_UPDATE: Int
```

A new set of metadata is available. 

 Value: 802

**See Also**

- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_INFO_NOT_SEEKABLE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_NOT_SEEKABLE: Int
```

The media cannot be seeked (e.g live stream) 

 Value: 801

**See Also**

- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_INFO_STARTED_AS_NEXT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_STARTED_AS_NEXT: Int
```

The player was started because it was used as the next player for another player, which just completed playback. 

 Value: 2

**See Also**

- [android.media.MediaPlayer#setNextMediaPlayer(MediaPlayer)](../android/media/MediaPlayer.md))
- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_INFO_SUBTITLE_TIMED_OUT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_SUBTITLE_TIMED_OUT: Int
```

Reading the subtitle track takes too long. 

 Value: 902

**See Also**

- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_INFO_UNKNOWN

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_UNKNOWN: Int
```

Unspecified media player info. 

 Value: 1

**See Also**

- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_INFO_UNSUPPORTED_SUBTITLE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_UNSUPPORTED_SUBTITLE: Int
```

Subtitle track was not supported by the media framework. 

 Value: 901

**See Also**

- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_INFO_VIDEO_NOT_PLAYING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_VIDEO_NOT_PLAYING: Int
```

Informs that video is not playing. Note that playback of the audio is not interrupted. 

 Value: 805

**See Also**

- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_INFO_VIDEO_RENDERING_START

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_VIDEO_RENDERING_START: Int
```

The player just pushed the very first video frame for rendering. 

 Value: 3

**See Also**

- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_INFO_VIDEO_TRACK_LAGGING

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_INFO_VIDEO_TRACK_LAGGING: Int
```

The video is too complex for the decoder: it can't decode frames fast enough. Possibly only the audio plays fine at this stage. 

 Value: 700

**See Also**

- [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) 

### MEDIA_MIMETYPE_TEXT_SUBRIP

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_MIMETYPE_TEXT_SUBRIP: String
```

**Deprecated:** *use [MediaFormat.MIMETYPE_TEXT_SUBRIP](../android/media/MediaFormat.md)*

MIME type for SubRip (SRT) container. Used in addTimedTextSource APIs. 

 Value: "application/x-subrip"

### PREPARE_DRM_STATUS_PREPARATION_ERROR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREPARE_DRM_STATUS_PREPARATION_ERROR: Int
```

The DRM preparation has failed . 

 Value: 3

### PREPARE_DRM_STATUS_PROVISIONING_NETWORK_ERROR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREPARE_DRM_STATUS_PROVISIONING_NETWORK_ERROR: Int
```

The device required DRM provisioning but couldn't reach the provisioning server. 

 Value: 1

### PREPARE_DRM_STATUS_PROVISIONING_SERVER_ERROR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREPARE_DRM_STATUS_PROVISIONING_SERVER_ERROR: Int
```

The device required DRM provisioning but the provisioning server denied the request. 

 Value: 2

### PREPARE_DRM_STATUS_SUCCESS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREPARE_DRM_STATUS_SUCCESS: Int
```

The status codes for [OnDrmPreparedListener.onDrmPrepared](../android/media/MediaPlayer.OnDrmPreparedListener.md))listener.

DRM preparation has succeeded. 

 Value: 0

### SEEK_CLOSEST

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEEK_CLOSEST: Int
```

This mode is used with [seekTo(long,int)](../android/media/MediaPlayer.md))to move media position to a frame (not necessarily a key frame) associated with a data source that is located closest to or at the given time. 

 Value: 3

**See Also**

- [#seekTo(long, int)](../android/media/MediaPlayer.md)) 

### SEEK_CLOSEST_SYNC

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEEK_CLOSEST_SYNC: Int
```

This mode is used with [seekTo(long,int)](../android/media/MediaPlayer.md))to move media position to a sync (or key) frame associated with a data source that is located closest to (in time) or at the given time. 

 Value: 2

**See Also**

- [#seekTo(long, int)](../android/media/MediaPlayer.md)) 

### SEEK_NEXT_SYNC

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEEK_NEXT_SYNC: Int
```

This mode is used with [seekTo(long,int)](../android/media/MediaPlayer.md))to move media position to a sync (or key) frame associated with a data source that is located right after or at the given time. 

 Value: 1

**See Also**

- [#seekTo(long, int)](../android/media/MediaPlayer.md)) 

### SEEK_PREVIOUS_SYNC

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEEK_PREVIOUS_SYNC: Int
```

This mode is used with [seekTo(long,int)](../android/media/MediaPlayer.md))to move media position to a sync (or key) frame associated with a data source that is located right before or at the given time. 

 Value: 0

**See Also**

- [#seekTo(long, int)](../android/media/MediaPlayer.md)) 

### VIDEO_SCALING_MODE_SCALE_TO_FIT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_SCALING_MODE_SCALE_TO_FIT: Int
```

Specifies a video scaling mode. The content is stretched to the surface rendering area. When the surface has the same aspect ratio as the content, the aspect ratio of the content is maintained; otherwise, the aspect ratio of the content is not maintained when video is being rendered. Unlike [VIDEO_SCALING_MODE_SCALE_TO_FIT_WITH_CROPPING](../android/media/MediaPlayer.md), there is no content cropping with this video scaling mode. 

 Value: 1

### VIDEO_SCALING_MODE_SCALE_TO_FIT_WITH_CROPPING

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_SCALING_MODE_SCALE_TO_FIT_WITH_CROPPING: Int
```

Specifies a video scaling mode. The content is scaled, maintaining its aspect ratio. The whole surface area is always used. When the aspect ratio of the content is the same as the surface, no content is cropped; otherwise, content is cropped to fit the surface. 

 Value: 2

## Public constructors

### MediaPlayer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaPlayer()
```

Default constructor.

Consider using one of the create() methods for synchronously instantiating a MediaPlayer from a Uri or resource.

You must call [release()](../android/media/MediaPlayer.md))when you are finished using the instantiated instance. Doing so frees any resources you have previously acquired. 

### MediaPlayer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaPlayer(context: Context)
```

Default constructor with context.

Consider using one of the create() methods for synchronously instantiating a MediaPlayer from a Uri or resource.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):non-null context. This context will be used to pull information, such as [android.content.AttributionSource](../android/content/AttributionSource.md) and device specific session ids, which will be associated with the [MediaPlayer](../android/media/MediaPlayer.md). However, the context itself will not be retained by the MediaPlayer. |

## Public methods

### addOnRoutingChangedListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addOnRoutingChangedListener(
    listener: AudioRouting.OnRoutingChangedListener!, 
    handler: Handler!
): Unit
```

Adds an [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) to receive notifications of routing changes on this MediaPlayer.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!:The [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) interface to receive notifications of rerouting events. |
| `handler` | [Handler](../android/os/Handler.md)!:Specifies the [Handler](../android/os/Handler.md) object for the thread on which to execute the callback. If`null`, the handler on the main looper will be used. |

### addTimedTextSource

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addTimedTextSource(
    context: Context!, 
    uri: Uri!, 
    mimeType: String!
): Unit
```

Adds an external timed text source file (Uri). Currently supported format is SubRip with the file extension .srt, case insensitive. Note that a single external timed text source may contain multiple tracks in it. One can find the total number of available tracks using [getTrackInfo()](../android/media/MediaPlayer.md))to see what additional tracks become available after this method call.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the Context to use when resolving the Uri |
| `uri` | [Uri](../android/net/Uri.md)!:the Content URI of the data you want to play |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The mime type of the file. Must be one of the mime types listed above. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.io.IOException` | if the file cannot be accessed or is corrupted. |
| `java.lang.IllegalArgumentException` | if the mimeType is not supported. |
| `java.lang.IllegalStateException` | if called in an invalid state. |
| --- | --- |

### addTimedTextSource

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addTimedTextSource(
    fd: FileDescriptor!, 
    mimeType: String!
): Unit
```

Adds an external timed text source file (FileDescriptor). It is the caller's responsibility to close the file descriptor. It is safe to do so as soon as this call returns. Currently supported format is SubRip. Note that a single external timed text source may contain multiple tracks in it. One can find the total number of available tracks using [getTrackInfo()](../android/media/MediaPlayer.md))to see what additional tracks become available after this method call.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md)!:the FileDescriptor for the file you want to play |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The mime type of the file. Must be one of the mime types listed above. |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.IllegalArgumentException` | if the mimeType is not supported. |
| `java.lang.IllegalStateException` | if called in an invalid state. |

### addTimedTextSource

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addTimedTextSource(
    fd: FileDescriptor!, 
    offset: Long, 
    length: Long, 
    mime: String!
): Unit
```

Adds an external timed text file (FileDescriptor). It is the caller's responsibility to close the file descriptor. It is safe to do so as soon as this call returns. Currently supported format is SubRip. Note that a single external timed text source may contain multiple tracks in it. One can find the total number of available tracks using [getTrackInfo()](../android/media/MediaPlayer.md))to see what additional tracks become available after this method call.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md)!:the FileDescriptor for the file you want to play |
| `offset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the offset into the file where the data to be played starts, in bytes |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the length in bytes of the data to be played |
| --- | --- |
| `mime` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The mime type of the file. Must be one of the mime types listed above. |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.IllegalArgumentException` | if the mimeType is not supported. |
| `java.lang.IllegalStateException` | if called in an invalid state. |

### addTimedTextSource

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addTimedTextSource(
    path: String!, 
    mimeType: String!
): Unit
```

Adds an external timed text source file. Currently supported format is SubRip with the file extension .srt, case insensitive. Note that a single external timed text source may contain multiple tracks in it. One can find the total number of available tracks using [getTrackInfo()](../android/media/MediaPlayer.md))to see what additional tracks become available after this method call.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The file path of external timed text source file. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The mime type of the file. Must be one of the mime types listed above. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.io.IOException` | if the file cannot be accessed or is corrupted. |
| `java.lang.IllegalArgumentException` | if the mimeType is not supported. |
| `java.lang.IllegalStateException` | if called in an invalid state. |
| --- | --- |

### attachAuxEffect

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun attachAuxEffect(effectId: Int): Unit
```

Attaches an auxiliary effect to the player. A typical auxiliary effect is a reverberation effect which can be applied on any sound source that directs a certain amount of its energy to this effect. This amount is defined by setAuxEffectSendLevel(). See [setAuxEffectSendLevel(float)](../android/media/MediaPlayer.md)).

After creating an auxiliary effect (e.g. [android.media.audiofx.EnvironmentalReverb](../android/media/audiofx/EnvironmentalReverb.md)), retrieve its ID with [android.media.audiofx.AudioEffect#getId()](../android/media/audiofx/AudioEffect.md))and use it when calling this method to attach the player to the effect.

To detach the effect from the player, call this method with a null effect id.

This method must be called after one of the overloaded` setDataSource `methods.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `effectId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):system wide unique id of the effect to attach |

### clearOnMediaTimeDiscontinuityListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearOnMediaTimeDiscontinuityListener(): Unit
```

Clears the listener previously set with [setOnMediaTimeDiscontinuityListener(android.media.MediaPlayer.OnMediaTimeDiscontinuityListener)](../android/media/MediaPlayer.md))or [setOnMediaTimeDiscontinuityListener(android.media.MediaPlayer.OnMediaTimeDiscontinuityListener,android.os.Handler)](../android/media/MediaPlayer.md)) 

### clearOnSubtitleDataListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearOnSubtitleDataListener(): Unit
```

Clears the listener previously set with [setOnSubtitleDataListener(android.media.MediaPlayer.OnSubtitleDataListener)](../android/media/MediaPlayer.md))or [setOnSubtitleDataListener(android.media.MediaPlayer.OnSubtitleDataListener,android.os.Handler)](../android/media/MediaPlayer.md)). 

### create

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    context: Context!, 
    uri: Uri!
): MediaPlayer!
```

Convenience method to create a MediaPlayer for a given Uri. On success, [prepare()](../android/media/MediaPlayer.md))will already have been called and must not be called again.

You must call [release()](../android/media/MediaPlayer.md))when you are finished using the created instance. Doing so frees any resources you have previously acquired.

Note that since [prepare()](../android/media/MediaPlayer.md))is called automatically in this method, you cannot change the audio session ID (see [setAudioSessionId(int)](../android/media/MediaPlayer.md))) or audio attributes (see [setAudioAttributes(android.media.AudioAttributes)](../android/media/MediaPlayer.md))of the new MediaPlayer.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the Context to use |
| `uri` | [Uri](../android/net/Uri.md)!:the Uri from which to get the datasource |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MediaPlayer](../android/media/MediaPlayer.md)! | a MediaPlayer object, or null if creation failed |

### create

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    context: Context!, 
    uri: Uri!, 
    holder: SurfaceHolder!
): MediaPlayer!
```

Convenience method to create a MediaPlayer for a given Uri. On success, [prepare()](../android/media/MediaPlayer.md))will already have been called and must not be called again.

You must call [release()](../android/media/MediaPlayer.md))when you are finished using the created instance. Doing so frees any resources you have previously acquired.

Note that since [prepare()](../android/media/MediaPlayer.md))is called automatically in this method, you cannot change the audio session ID (see [setAudioSessionId(int)](../android/media/MediaPlayer.md))) or audio attributes (see [setAudioAttributes(android.media.AudioAttributes)](../android/media/MediaPlayer.md))of the new MediaPlayer.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the Context to use |
| `uri` | [Uri](../android/net/Uri.md)!:the Uri from which to get the datasource |
| `holder` | [SurfaceHolder](../android/view/SurfaceHolder.md)!:the SurfaceHolder to use for displaying the video |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MediaPlayer](../android/media/MediaPlayer.md)! | a MediaPlayer object, or null if creation failed |

### create

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    context: Context!, 
    uri: Uri!, 
    holder: SurfaceHolder!, 
    audioAttributes: AudioAttributes!, 
    audioSessionId: Int
): MediaPlayer!
```

Same factory method as [create(android.content.Context,android.net.Uri,android.view.SurfaceHolder)](../android/media/MediaPlayer.md))but that lets you specify the audio attributes and session ID to be used by the new MediaPlayer instance.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the Context to use |
| `uri` | [Uri](../android/net/Uri.md)!:the Uri from which to get the datasource |
| `holder` | [SurfaceHolder](../android/view/SurfaceHolder.md)!:the SurfaceHolder to use for displaying the video, may be null. |
| --- | --- |
| `audioAttributes` | [AudioAttributes](../android/media/AudioAttributes.md)!:the [AudioAttributes](../android/media/AudioAttributes.md) to be used by the media player. |
| `audioSessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the audio session ID to be used by the media player, see [AudioManager.generateAudioSessionId()](../android/media/AudioManager.md))to obtain a new session. |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MediaPlayer](../android/media/MediaPlayer.md)! | a MediaPlayer object, or null if creation failed |

### create

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    context: Context!, 
    resid: Int
): MediaPlayer!
```

Convenience method to create a MediaPlayer for a given resource id. On success, [prepare()](../android/media/MediaPlayer.md))will already have been called and must not be called again.

You must call [release()](../android/media/MediaPlayer.md))when you are finished using the created instance. Doing so frees any resources you have previously acquired.

Note that since [prepare()](../android/media/MediaPlayer.md))is called automatically in this method, you cannot change the audio session ID (see [setAudioSessionId(int)](../android/media/MediaPlayer.md))) or audio attributes (see [setAudioAttributes(android.media.AudioAttributes)](../android/media/MediaPlayer.md))of the new MediaPlayer.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the Context to use |
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the raw resource id (R.raw.\<something\>) for the resource to use as the datasource |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MediaPlayer](../android/media/MediaPlayer.md)! | a MediaPlayer object, or null if creation failed |

### create

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    context: Context!, 
    resid: Int, 
    audioAttributes: AudioAttributes!, 
    audioSessionId: Int
): MediaPlayer!
```

Same factory method as [create(android.content.Context,int)](../android/media/MediaPlayer.md))but that lets you specify the audio attributes and session ID to be used by the new MediaPlayer instance.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the Context to use |
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the raw resource id (R.raw.\<something\>) for the resource to use as the datasource |
| `audioAttributes` | [AudioAttributes](../android/media/AudioAttributes.md)!:the [AudioAttributes](../android/media/AudioAttributes.md) to be used by the media player. |
| --- | --- |
| `audioSessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the audio session ID to be used by the media player, see [AudioManager.generateAudioSessionId()](../android/media/AudioManager.md))to obtain a new session. |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MediaPlayer](../android/media/MediaPlayer.md)! | a MediaPlayer object, or null if creation failed |

### createVolumeShaper

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createVolumeShaper(configuration: VolumeShaper.Configuration): VolumeShaper
```

Returns a [VolumeShaper](../android/media/VolumeShaper.md) object that can be used modify the volume envelope of the player or track.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `configuration` | [VolumeShaper.Configuration](../android/media/VolumeShaper.Configuration.md):This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------|
| [VolumeShaper](../android/media/VolumeShaper.md) | This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`configuration`is not allowed by the player. |
| `java.lang.IllegalStateException` | if too many`VolumeShaper`s are requested or the state of the player does not permit its creation (e.g. player is released). |

### deselectTrack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deselectTrack(index: Int): Unit
```

Deselect a track.

Currently, the track must be a timed text track and no audio or video tracks can be deselected. If the timed text track identified by index has not been selected before, it throws an exception.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the track to be deselected. The valid range of the index is 0..total number of tracks - 1. The total number of tracks as well as the type of each individual track can be found by calling [getTrackInfo()](../android/media/MediaPlayer.md))method. |

| Exceptions ||
|-----------------------------------|--------------------------------|
| `java.lang.IllegalStateException` | if called in an invalid state. |

**See Also**

- [android.media.MediaPlayer#getTrackInfo](../android/media/MediaPlayer.md)) 

### getAudioSessionId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAudioSessionId(): Int
```

Returns the audio session ID.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the audio session ID. {@see #setAudioSessionId(int)} Note that the audio session ID is 0 only if a problem occured when the MediaPlayer was contructed. |

### getCurrentPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrentPosition(): Int
```

Gets the current playback position.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current position in milliseconds |

### getDrmInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDrmInfo(): MediaPlayer.DrmInfo!
```

Retrieves the DRM Info associated with the current source

| Exceptions ||
|-----------------------------------|----------------------------|
| `java.lang.IllegalStateException` | if called before prepare() |

### getDrmPropertyString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDrmPropertyString(propertyName: String): String
```

Read a DRM engine plugin String property value, given the property name string.

<br />

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the property name Standard fields names are: [MediaDrm.PROPERTY_VENDOR](../android/media/MediaDrm.md), [MediaDrm.PROPERTY_VERSION](../android/media/MediaDrm.md), [MediaDrm.PROPERTY_DESCRIPTION](../android/media/MediaDrm.md), [MediaDrm.PROPERTY_ALGORITHMS](../android/media/MediaDrm.md) This value cannot be`null`. Value is [android.media.MediaDrm#PROPERTY_VENDOR](../android/media/MediaDrm.md), [android.media.MediaDrm#PROPERTY_VERSION](../android/media/MediaDrm.md), [android.media.MediaDrm#PROPERTY_DESCRIPTION](../android/media/MediaDrm.md), or [android.media.MediaDrm#PROPERTY_ALGORITHMS](../android/media/MediaDrm.md) |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDuration(): Int
```

Gets the duration of the file.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the duration in milliseconds, if no duration is available (for example, if streaming live content), -1 is returned. |

### getKeyRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeyRequest(
    keySetId: ByteArray?, 
    initData: ByteArray?, 
    mimeType: String?, 
    keyType: Int, 
    optionalParameters: MutableMap<String!, String!>?
): MediaDrm.KeyRequest
```

A key request/response exchange occurs between the app and a license server to obtain or release keys used to decrypt encrypted content.

getKeyRequest() is used to obtain an opaque key request byte array that is delivered to the license server. The opaque key request byte array is returned in KeyRequest.data. The recommended URL to deliver the key request to is returned in KeyRequest.defaultUrl.

After the app has received the key request response from the server, it should deliver to the response to the DRM engine plugin using the method [provideKeyResponse](../android/media/MediaPlayer.md)).

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keySetId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:is the key-set identifier of the offline keys being released when keyType is [MediaDrm.KEY_TYPE_RELEASE](../android/media/MediaDrm.md). It should be set to null for other key requests, when keyType is [MediaDrm.KEY_TYPE_STREAMING](../android/media/MediaDrm.md) or [MediaDrm.KEY_TYPE_OFFLINE](../android/media/MediaDrm.md). |
| `initData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:is the container-specific initialization data when the keyType is [MediaDrm.KEY_TYPE_STREAMING](../android/media/MediaDrm.md) or [MediaDrm.KEY_TYPE_OFFLINE](../android/media/MediaDrm.md). Its meaning is interpreted based on the mime type provided in the mimeType parameter. It could contain, for example, the content ID, key ID or other data obtained from the content metadata that is required in generating the key request. When the keyType is [MediaDrm.KEY_TYPE_RELEASE](../android/media/MediaDrm.md), it should be set to null. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:identifies the mime type of the content This value may be`null`. |
| --- | --- |
| `keyType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):specifies the type of the request. The request may be to acquire keys for streaming, [MediaDrm.KEY_TYPE_STREAMING](../android/media/MediaDrm.md), or for offline content [MediaDrm.KEY_TYPE_OFFLINE](../android/media/MediaDrm.md), or to release previously acquired keys ([MediaDrm.KEY_TYPE_RELEASE](../android/media/MediaDrm.md)), which are identified by a keySetId. Value is [android.media.MediaDrm#KEY_TYPE_STREAMING](../android/media/MediaDrm.md), [android.media.MediaDrm#KEY_TYPE_OFFLINE](../android/media/MediaDrm.md), or [android.media.MediaDrm#KEY_TYPE_RELEASE](../android/media/MediaDrm.md) |
| `optionalParameters` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:are included in the key request message to allow a client application to provide additional message parameters to the server. This may be`null`if no additional parameters are to be sent. |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------|
| [MediaDrm.KeyRequest](../android/media/MediaDrm.KeyRequest.md) | This value cannot be`null`. |

| Exceptions ||
|--------------------------------------------------|-----------------------------------|
| `android.media.MediaPlayer.NoDrmSchemeException` | if there is no active DRM session |

### getMetrics

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMetrics(): PersistableBundle!
```

Return Metrics data about the current player.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PersistableBundle](../android/os/PersistableBundle.md)! | a [PersistableBundle](../android/os/PersistableBundle.md) containing the set of attributes and values available for the media being handled by this instance of MediaPlayer The attributes are descibed in [MetricsConstants](../android/media/MediaPlayer.MetricsConstants.md). Additional vendor-specific fields may also be present in the return value. |

### getPlaybackParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPlaybackParams(): PlaybackParams
```

Gets the playback params, containing the current playback rate.

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| [PlaybackParams](../android/media/PlaybackParams.md) | the playback params. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized. |

### getPreferredDevice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreferredDevice(): AudioDeviceInfo!
```

Returns the selected output specified by [setPreferredDevice](../android/media/MediaPlayer.md)). Note that this is not guaranteed to correspond to the actual device being used for playback. 

### getRoutedDevice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoutedDevice(): AudioDeviceInfo!
```

Returns an [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) identifying the current routing of this MediaPlayer Note: The query is only valid if the MediaPlayer is currently playing. If the player is not playing, the returned device can be null or correspond to previously selected device when the player was last active. Audio may play on multiple devices simultaneously (e.g. an alarm playing on headphones and speaker on a phone), so prefer using [getRoutedDevices](../android/media/MediaPlayer.md)). 

### getRoutedDevices

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoutedDevices(): MutableList<AudioDeviceInfo!>
```

Returns a List of [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) identifying the current routing of this MediaPlayer. Note: The query is only valid if the MediaPlayer is currently playing. If the player is not playing, the returned devices can be empty or correspond to previously selected devices when the player was last active.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)!> | This value cannot be`null`. |

### getSelectedTrack

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSelectedTrack(trackType: Int): Int
```

Returns the index of the audio, video, or subtitle track currently selected for playback, The return value is an index into the array returned by [getTrackInfo()](../android/media/MediaPlayer.md)), and can be used in calls to [selectTrack(int)](../android/media/MediaPlayer.md))or [deselectTrack(int)](../android/media/MediaPlayer.md)).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trackType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):should be one of [TrackInfo.MEDIA_TRACK_TYPE_VIDEO](../android/media/MediaPlayer.TrackInfo.md), [TrackInfo.MEDIA_TRACK_TYPE_AUDIO](../android/media/MediaPlayer.TrackInfo.md), or [TrackInfo.MEDIA_TRACK_TYPE_SUBTITLE](../android/media/MediaPlayer.TrackInfo.md) |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | index of the audio, video, or subtitle track currently selected for playback; a negative integer is returned when there is no selected track for`trackType`or when`trackType`is not one of audio, video, or subtitle. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if called after [release()](../android/media/MediaPlayer.md)) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/media/MediaPlayer#getTrackInfo()>
- [#selectTrack(int)](../android/media/MediaPlayer.md))
- [#deselectTrack(int)](../android/media/MediaPlayer.md)) 

### getSyncParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSyncParams(): SyncParams
```

Gets the A/V sync mode.

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------|
| [SyncParams](../android/media/SyncParams.md) | the A/V sync params This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized. |

### getTimestamp

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimestamp(): MediaTimestamp?
```

Get current playback position as a [MediaTimestamp](../android/media/MediaTimestamp.md).

The MediaTimestamp represents how the media time correlates to the system time in a linear fashion using an anchor and a clock rate. During regular playback, the media time moves fairly constantly (though the anchor frame may be rebased to a current system time, the linear correlation stays steady). Therefore, this method does not need to be called often.

To help users get current playback position, this method always anchors the timestamp to the current [system time](../java/lang/System.md)), so [MediaTimestamp.getAnchorMediaTimeUs](../android/media/MediaTimestamp.md))can be used as current playback position.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [MediaTimestamp](../android/media/MediaTimestamp.md)? | a MediaTimestamp object if a timestamp is available, or`null`if no timestamp is available, e.g. because the media player has not been initialized. |

**See Also**

- [android.media.MediaTimestamp](../android/media/MediaTimestamp.md) 

### getTrackInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTrackInfo(): Array<MediaPlayer.TrackInfo!>!
```

Returns an array of track information.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MediaPlayer.TrackInfo](../android/media/MediaPlayer.TrackInfo.md)!>! | Array of track info. The total number of tracks is the array length. Must be called again if an external timed text source has been added after any of the addTimedTextSource methods are called. |

| Exceptions ||
|-----------------------------------|--------------------------------------|
| `java.lang.IllegalStateException` | if it is called in an invalid state. |

### getVideoHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVideoHeight(): Int
```

Returns the height of the video.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the height of the video, or 0 if there is no video, no display surface was set, or the height has not been determined yet. The OnVideoSizeChangedListener can be registered via [setOnVideoSizeChangedListener(android.media.MediaPlayer.OnVideoSizeChangedListener)](../android/media/MediaPlayer.md))to provide a notification when the height is available. |

### getVideoWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVideoWidth(): Int
```

Returns the width of the video.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the width of the video, or 0 if there is no video, no display surface was set, or the width has not been determined yet. The OnVideoSizeChangedListener can be registered via [setOnVideoSizeChangedListener(android.media.MediaPlayer.OnVideoSizeChangedListener)](../android/media/MediaPlayer.md))to provide a notification when the width is available. |

### isLooping

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLooping(): Boolean
```

Checks whether the MediaPlayer is looping or non-looping.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the MediaPlayer is currently looping, false otherwise |

### isPlaying

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPlaying(): Boolean
```

Checks whether the MediaPlayer is playing.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if currently playing, false otherwise |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized or has been released. |

### pause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pause(): Unit
```

Pauses playback. Call start() to resume.

| Exceptions ||
|-----------------------------------|---------------------------------------------------------|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized. |

### prepare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun prepare(): Unit
```

Prepares the player for playback, synchronously. After setting the datasource and the display surface, you need to either call prepare() or prepareAsync(). For files, it is OK to call prepare(), which blocks until MediaPlayer is ready for playback.

| Exceptions ||
|-----------------------------------|-------------------------------------|
| `java.lang.IllegalStateException` | if it is called in an invalid state |

### prepareAsync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun prepareAsync(): Unit
```

Prepares the player for playback, asynchronously. After setting the datasource and the display surface, you need to either call prepare() or prepareAsync(). For streams, you should call prepareAsync(), which returns immediately, rather than blocking until enough data has been buffered.

| Exceptions ||
|-----------------------------------|-------------------------------------|
| `java.lang.IllegalStateException` | if it is called in an invalid state |

### prepareDrm

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun prepareDrm(uuid: UUID): Unit
```

Prepares the DRM for the current source

If`OnDrmConfigHelper`is registered, it will be called during preparation to allow configuration of the DRM properties before opening the DRM session. Note that the callback is called synchronously in the thread that called`prepareDrm`. It should be used only for a series of`getDrmPropertyString`and`setDrmPropertyString`calls and refrain from any lengthy operation.

If the device has not been provisioned before, this call also provisions the device which involves accessing the provisioning server and can take a variable time to complete depending on the network connectivity. If`OnDrmPreparedListener`is registered, prepareDrm() runs in non-blocking mode by launching the provisioning in the background and returning. The listener will be called when provisioning and preparation has finished. If a`OnDrmPreparedListener`is not registered, prepareDrm() waits till provisioning and preparation has finished, i.e., runs in blocking mode.

If`OnDrmPreparedListener`is registered, it is called to indicate the DRM session being ready. The application should not make any assumption about its call sequence (e.g., before or after prepareDrm returns), or the thread context that will execute the listener (unless the listener is registered with a handler thread).

<br />

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uuid` | [UUID](../java/util/UUID.md):The UUID of the crypto scheme. If not known beforehand, it can be retrieved from the source through`getDrmInfo`or registering a`onDrmInfoListener`. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if called before prepare(), or the DRM was prepared already |
| `android.media.UnsupportedSchemeException` | if the crypto scheme is not supported |
| `android.media.ResourceBusyException` | if required DRM resources are in use |
| --- | --- |
| `android.media.MediaPlayer.ProvisioningNetworkErrorException` | if provisioning is required but failed due to a network error |
| `android.media.MediaPlayer.ProvisioningServerErrorException` | if provisioning is required but failed due to the request denied by the provisioning server |

### provideKeyResponse

```
open fun provideKeyResponse(
    keySetId: ByteArray?, 
    response: ByteArray
): ByteArray!
```

A key response is received from the license server by the app, then it is provided to the DRM engine plugin using provideKeyResponse. When the response is for an offline key request, a key-set identifier is returned that can be used to later restore the keys to a new session with the method {@ link # restoreKeys}. \* When the response is for a streaming or release request, null is returned. \* \* @param keySetId When the response is for a release request, keySetId identifies \* the saved key associated with the release request (i.e., the same keySetId \* passed to the earlier {@ link # getKeyRequest} call. It MUST be null when the \* response is for either streaming or offline key requests. \* \* @param response the byte array response from the server \* \* @throws NoDrmSchemeException if there is no active DRM session \* @throws DeniedByServerException if the response indicates that the \* server rejected the request \* @param keySetId This value may be {@code null}. \* @param response This value cannot be {@code null}. \* @apiSince 26 

### release

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Releases resources associated with this MediaPlayer object.

You must call this method once the instance is no longer required. 

### releaseDrm

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun releaseDrm(): Unit
```

Releases the DRM session

The player has to have an active DRM session and be in stopped, or prepared state before this call is made. A`reset()`call will release the DRM session implicitly.

| Exceptions ||
|--------------------------------------------------|----------------------------------------------|
| `android.media.MediaPlayer.NoDrmSchemeException` | if there is no active DRM session to release |

### removeOnRoutingChangedListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeOnRoutingChangedListener(listener: AudioRouting.OnRoutingChangedListener!): Unit
```

Removes an [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) which has been previously added to receive rerouting notifications.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!:The previously added [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) interface to remove. |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets the MediaPlayer to its uninitialized state. After calling this method, you will have to initialize it again by setting the data source and calling prepare(). 

### restoreKeys

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreKeys(keySetId: ByteArray): Unit
```

Restore persisted offline keys into a new session. keySetId identifies the keys to load, obtained from a prior call to [provideKeyResponse](../android/media/MediaPlayer.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keySetId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):identifies the saved key set to restore This value cannot be`null`. |

### seekTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun seekTo(msec: Int): Unit
```

Seeks to specified time position. Same as [seekTo(long,int)](../android/media/MediaPlayer.md))with`mode = SEEK_PREVIOUS_SYNC`.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------|
| `msec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in milliseconds from the start to seek to |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized |

### seekTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun seekTo(
    msec: Long, 
    mode: Int
): Unit
```

Moves the media to specified time position by considering the given mode.

When seekTo is finished, the user will be notified via OnSeekComplete supplied by the user. There is at most one active seekTo processed at any time. If there is a to-be-completed seekTo, new seekTo requests will be queued in such a way that only the last request is kept. When current seekTo is completed, the queued request will be processed if that request is different from just-finished seekTo operation, i.e., the requested position or mode is different.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msec` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the offset in milliseconds from the start to seek to. When seeking to the given time position, there is no guarantee that the data source has a frame located at the position. When this happens, a frame nearby will be rendered. If msec is negative, time position zero will be used. If msec is larger than duration, duration will be used. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the mode indicating where exactly to seek to. Use [SEEK_PREVIOUS_SYNC](../android/media/MediaPlayer.md) if one wants to seek to a sync frame that has a timestamp earlier than or the same as msec. Use [SEEK_NEXT_SYNC](../android/media/MediaPlayer.md) if one wants to seek to a sync frame that has a timestamp later than or the same as msec. Use [SEEK_CLOSEST_SYNC](../android/media/MediaPlayer.md) if one wants to seek to a sync frame that has a timestamp closest to or the same as msec. Use [SEEK_CLOSEST](../android/media/MediaPlayer.md) if one wants to seek to a frame that may or may not be a sync frame but is closest to or the same as msec. [SEEK_CLOSEST](../android/media/MediaPlayer.md) often has larger performance overhead compared to the other options if there is no sync frame located at msec. Value is [android.media.MediaPlayer#SEEK_PREVIOUS_SYNC](../android/media/MediaPlayer.md), [android.media.MediaPlayer#SEEK_NEXT_SYNC](../android/media/MediaPlayer.md), [android.media.MediaPlayer#SEEK_CLOSEST_SYNC](../android/media/MediaPlayer.md), or [android.media.MediaPlayer#SEEK_CLOSEST](../android/media/MediaPlayer.md) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized |
| `java.lang.IllegalArgumentException` | if the mode is invalid. |

### selectTrack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun selectTrack(index: Int): Unit
```

Selects a track.

If a MediaPlayer is in invalid state, it throws an IllegalStateException exception. If a MediaPlayer is in*Started*state, the selected track is presented immediately. If a MediaPlayer is not in Started state, it just marks the track to be played.

In any valid state, if it is called multiple times on the same type of track (ie. Video, Audio, Timed Text), the most recent one will be chosen.

The first audio and video tracks are selected by default if available, even though this method is not called. However, no timed text track will be selected until this function is called.

Currently, only timed text, subtitle or audio tracks can be selected via this method. In addition, the support for selecting an audio track at runtime is pretty limited in that an audio track can only be selected in the*Prepared*state.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the track to be selected. The valid range of the index is 0..total number of track - 1. The total number of tracks as well as the type of each individual track can be found by calling [getTrackInfo()](../android/media/MediaPlayer.md))method. |

| Exceptions ||
|-----------------------------------|--------------------------------|
| `java.lang.IllegalStateException` | if called in an invalid state. |

**See Also**

- [android.media.MediaPlayer#getTrackInfo](../android/media/MediaPlayer.md)) 

### setAudioAttributes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAudioAttributes(attributes: AudioAttributes!): Unit
```

Sets the audio attributes for this MediaPlayer. See [AudioAttributes](../android/media/AudioAttributes.md) for how to build and configure an instance of this class. You must call this method before [prepare()](../android/media/MediaPlayer.md))or [prepareAsync()](../android/media/MediaPlayer.md))in order for the audio attributes to become effective thereafter.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [AudioAttributes](../android/media/AudioAttributes.md)!:a non-null set of audio attributes |

### setAudioSessionId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAudioSessionId(sessionId: Int): Unit
```

Sets the audio session ID.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the audio session ID. The audio session ID is a system wide unique identifier for the audio stream played by this MediaPlayer instance. The primary use of the audio session ID is to associate audio effects to a particular instance of MediaPlayer: if an audio session ID is provided when creating an audio effect, this effect will be applied only to the audio content of media players within the same audio session and not to the output mix. When created, a MediaPlayer instance automatically generates its own audio session ID. However, it is possible to force this player to be part of an already existing audio session by calling this method. This method must be called before one of the overloaded` setDataSource `methods. Note that session id set using this method will override device-specific audio session id, if the [MediaPlayer](../android/media/MediaPlayer.md) was instantiated using device-specific [Context](../android/content/Context.md)- see [MediaPlayer.MediaPlayer(Context)](../android/media/MediaPlayer.md)). |

| Exceptions ||
|-----------------------------------|-------------------------------------|
| `java.lang.IllegalStateException` | if it is called in an invalid state |

### setAudioStreamType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAudioStreamType(streamtype: Int): Unit
```

**Deprecated:** *use [setAudioAttributes(android.media.AudioAttributes)](../android/media/MediaPlayer.md))*

Sets the audio stream type for this MediaPlayer. See [AudioManager](../android/media/AudioManager.md) for a list of stream types. Must call this method before prepare() or prepareAsync() in order for the target stream type to become effective thereafter.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------|
| `streamtype` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the audio stream type |

**See Also**

- [android.media.AudioManager](../android/media/AudioManager.md) 

### setAuxEffectSendLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAuxEffectSendLevel(level: Float): Unit
```

Sets the send level of the player to the attached auxiliary effect. See [attachAuxEffect(int)](../android/media/MediaPlayer.md)). The level value range is 0 to 1.0.

By default the send level is 0, so even if an effect is attached to the player this method must be called for the effect to be applied.

Note that the passed level value is a raw scalar. UI controls should be scaled logarithmically: the gain applied by audio framework ranges from -72dB to 0dB, so an appropriate conversion from linear UI input x to level is: x == 0 -\> level = 0 0 \< x \<= R -\> level = 10\^(72\*(x-R)/20/R)

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `level` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):send level scalar |

### setDataSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(
    context: Context, 
    uri: Uri
): Unit
```

Sets the data source as a content Uri.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):the Context to use when resolving the Uri This value cannot be`null`. |
| `uri` | [Uri](../android/net/Uri.md):the Content URI of the data you want to play This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------|
| `java.lang.IllegalStateException` | if it is called in an invalid state |

### setDataSource

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(
    context: Context, 
    uri: Uri, 
    headers: MutableMap<String!, String!>?
): Unit
```

Sets the data source as a content Uri.

**Note**that the cross domain redirection is allowed by default, but that can be changed with key/value pairs through the headers parameter with "android-allow-cross-domain-redirect" as the key and "0" or "1" as the value to disallow or allow cross domain redirection.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):the Context to use when resolving the Uri This value cannot be`null`. |
| `uri` | [Uri](../android/net/Uri.md):the Content URI of the data you want to play This value cannot be`null`. |
| `headers` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:the headers to be sent together with the request for the data This value may be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------------------|
| `java.lang.IllegalStateException` | if it is called in an invalid state |

### setDataSource

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(
    context: Context, 
    uri: Uri, 
    headers: MutableMap<String!, String!>?, 
    cookies: MutableList<HttpCookie!>?
): Unit
```

Sets the data source as a content Uri. To provide cookies for the subsequent HTTP requests, you can install your own default cookie handler and use other variants of setDataSource APIs instead. Alternatively, you can use this API to pass the cookies as a list of HttpCookie. If the app has not installed a CookieHandler already, this API creates a CookieManager and populates its CookieStore with the provided cookies. If the app has installed its own handler already, this API requires the handler to be of CookieManager type such that the API can update the manager's CookieStore.

**Note**that the cross domain redirection is allowed by default, but that can be changed with key/value pairs through the headers parameter with "android-allow-cross-domain-redirect" as the key and "0" or "1" as the value to disallow or allow cross domain redirection.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):the Context to use when resolving the Uri This value cannot be`null`. |
| `uri` | [Uri](../android/net/Uri.md):the Content URI of the data you want to play This value cannot be`null`. |
| `headers` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:the headers to be sent together with the request for the data The headers must not include cookies. Instead, use the cookies param. This value may be`null`. |
| --- | --- |
| `cookies` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [HttpCookie](../java/net/HttpCookie.md)!\>?:the cookies to be sent together with the request This value may be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if cookies are provided and the installed handler is not a CookieManager |
| `java.lang.IllegalStateException` | if it is called in an invalid state |
| `java.lang.NullPointerException` | if context or uri is null |
| --- | --- |
| `java.io.IOException` | if uri has a file scheme and an I/O error occurs |

### setDataSource

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(afd: AssetFileDescriptor): Unit
```

Sets the data source (AssetFileDescriptor) to use. It is the caller's responsibility to close the file descriptor. It is safe to do so as soon as this call returns.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `afd` | [AssetFileDescriptor](../android/content/res/AssetFileDescriptor.md):the AssetFileDescriptor for the file you want to play This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------|
| `java.lang.IllegalStateException` | if it is called in an invalid state |
| `java.lang.IllegalArgumentException` | if afd is not a valid AssetFileDescriptor |
| `java.io.IOException` | if afd can not be read |
| --- | --- |

### setDataSource

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(dataSource: MediaDataSource!): Unit
```

Sets the data source (MediaDataSource) to use.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataSource` | [MediaDataSource](../android/media/MediaDataSource.md)!:the MediaDataSource for the media you want to play |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.IllegalStateException` | if it is called in an invalid state |
| `java.lang.IllegalArgumentException` | if dataSource is not a valid MediaDataSource |

### setDataSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(fd: FileDescriptor!): Unit
```

Sets the data source (FileDescriptor) to use. It is the caller's responsibility to close the file descriptor. It is safe to do so as soon as this call returns.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md)!:the FileDescriptor for the file you want to play |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalStateException` | if it is called in an invalid state |
| `java.lang.IllegalArgumentException` | if fd is not a valid FileDescriptor |
| `java.io.IOException` | if fd can not be read |
| --- | --- |

### setDataSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(
    fd: FileDescriptor!, 
    offset: Long, 
    length: Long
): Unit
```

Sets the data source (FileDescriptor) to use. The FileDescriptor must be seekable (N.B. a LocalSocket is not seekable). It is the caller's responsibility to close the file descriptor. It is safe to do so as soon as this call returns.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md)!:the FileDescriptor for the file you want to play |
| `offset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the offset into the file where the data to be played starts, in bytes |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the length in bytes of the data to be played |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalStateException` | if it is called in an invalid state |
| `java.lang.IllegalArgumentException` | if fd is not a valid FileDescriptor |
| `java.io.IOException` | if fd can not be read |
| --- | --- |

### setDataSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(path: String!): Unit
```

Sets the data source (file-path or http/rtsp URL) to use.

When`path`refers to a local file, the file may actually be opened by a process other than the calling application. This implies that the pathname should be an absolute path (as any other process runs with unspecified current working directory), and that the pathname should reference a world-readable file. As an alternative, the application could first open the file for reading, and then use the file descriptor form [setDataSource(java.io.FileDescriptor)](../android/media/MediaPlayer.md)).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path of the file, or the http/rtsp URL of the stream you want to play |

| Exceptions ||
|-----------------------------------|-------------------------------------|
| `java.lang.IllegalStateException` | if it is called in an invalid state |

### setDisplay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDisplay(sh: SurfaceHolder!): Unit
```

Sets the [SurfaceHolder](../android/view/SurfaceHolder.md) to use for displaying the video portion of the media. Either a surface holder or surface must be set if a display or video sink is needed. Not calling this method or [setSurface(android.view.Surface)](../android/media/MediaPlayer.md))when playing back a video will result in only the audio track being played. A null surface holder or surface will result in only the audio track being played.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `sh` | [SurfaceHolder](../android/view/SurfaceHolder.md)!:the SurfaceHolder to use for video display |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized or has been released. |

### setDrmPropertyString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDrmPropertyString(
    propertyName: String, 
    value: String
): Unit
```

Set a DRM engine plugin String property value.

<br />

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the property name This value cannot be`null`. Value is [android.media.MediaDrm#PROPERTY_VENDOR](../android/media/MediaDrm.md), [android.media.MediaDrm#PROPERTY_VERSION](../android/media/MediaDrm.md), [android.media.MediaDrm#PROPERTY_DESCRIPTION](../android/media/MediaDrm.md), or [android.media.MediaDrm#PROPERTY_ALGORITHMS](../android/media/MediaDrm.md) |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the property value Standard fields names are: [MediaDrm.PROPERTY_VENDOR](../android/media/MediaDrm.md), [MediaDrm.PROPERTY_VERSION](../android/media/MediaDrm.md), [MediaDrm.PROPERTY_DESCRIPTION](../android/media/MediaDrm.md), [MediaDrm.PROPERTY_ALGORITHMS](../android/media/MediaDrm.md) This value cannot be`null`. |

### setLooping

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLooping(looping: Boolean): Unit
```

Sets the player to be looping or non-looping.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------|
| `looping` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to loop or not |

### setNextMediaPlayer

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNextMediaPlayer(next: MediaPlayer!): Unit
```

Set the MediaPlayer to start when this MediaPlayer finishes playback (i.e. reaches the end of the stream). The media framework will attempt to transition from this player to the next as seamlessly as possible. The next player can be set at any time before completion, but shall be after setDataSource has been called successfully. The next player must be prepared by the app, and the application should not call start() on it. The next MediaPlayer must be different from 'this'. An exception will be thrown if next == this. The application may call setNextMediaPlayer(null) to indicate no next player should be started at the end of playback. If the current player is looping, it will keep looping and the next player will not be started.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `next` | [MediaPlayer](../android/media/MediaPlayer.md)!:the player to start after this one completes playback. |

### setOnBufferingUpdateListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnBufferingUpdateListener(listener: MediaPlayer.OnBufferingUpdateListener!): Unit
```

Register a callback to be invoked when the status of a network stream's buffer has changed.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnBufferingUpdateListener](../android/media/MediaPlayer.OnBufferingUpdateListener.md)!:the callback that will be run. |

### setOnCompletionListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnCompletionListener(listener: MediaPlayer.OnCompletionListener!): Unit
```

Register a callback to be invoked when the end of a media source has been reached during playback.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnCompletionListener](../android/media/MediaPlayer.OnCompletionListener.md)!:the callback that will be run |

### setOnDrmConfigHelper

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnDrmConfigHelper(listener: MediaPlayer.OnDrmConfigHelper!): Unit
```

Register a callback to be invoked for configuration of the DRM object before the session is created. The callback will be invoked synchronously during the execution of [prepareDrm(java.util.UUID)](../android/media/MediaPlayer.md)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnDrmConfigHelper](../android/media/MediaPlayer.OnDrmConfigHelper.md)!:the callback that will be run |

### setOnDrmInfoListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnDrmInfoListener(listener: MediaPlayer.OnDrmInfoListener!): Unit
```

Register a callback to be invoked when the DRM info is known.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnDrmInfoListener](../android/media/MediaPlayer.OnDrmInfoListener.md)!:the callback that will be run |

### setOnDrmInfoListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnDrmInfoListener(
    listener: MediaPlayer.OnDrmInfoListener!, 
    handler: Handler!
): Unit
```

Register a callback to be invoked when the DRM info is known.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnDrmInfoListener](../android/media/MediaPlayer.OnDrmInfoListener.md)!:the callback that will be run |

### setOnDrmPreparedListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnDrmPreparedListener(listener: MediaPlayer.OnDrmPreparedListener!): Unit
```

Register a callback to be invoked when the DRM object is prepared.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnDrmPreparedListener](../android/media/MediaPlayer.OnDrmPreparedListener.md)!:the callback that will be run |

### setOnDrmPreparedListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnDrmPreparedListener(
    listener: MediaPlayer.OnDrmPreparedListener!, 
    handler: Handler!
): Unit
```

Register a callback to be invoked when the DRM object is prepared.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnDrmPreparedListener](../android/media/MediaPlayer.OnDrmPreparedListener.md)!:the callback that will be run |
| `handler` | [Handler](../android/os/Handler.md)!:the Handler that will receive the callback |

### setOnErrorListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnErrorListener(listener: MediaPlayer.OnErrorListener!): Unit
```

Register a callback to be invoked when an error has happened during an asynchronous operation.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnErrorListener](../android/media/MediaPlayer.OnErrorListener.md)!:the callback that will be run |

### setOnInfoListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnInfoListener(listener: MediaPlayer.OnInfoListener!): Unit
```

Register a callback to be invoked when an info/warning is available.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md)!:the callback that will be run |

### setOnMediaTimeDiscontinuityListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnMediaTimeDiscontinuityListener(listener: MediaPlayer.OnMediaTimeDiscontinuityListener): Unit
```

Sets the listener to be invoked when a media time discontinuity is encountered. The listener will be called on the same thread as the one in which the MediaPlayer was created.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnMediaTimeDiscontinuityListener](../android/media/MediaPlayer.OnMediaTimeDiscontinuityListener.md):the listener called after a discontinuity This value cannot be`null`. |

### setOnMediaTimeDiscontinuityListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnMediaTimeDiscontinuityListener(
    listener: MediaPlayer.OnMediaTimeDiscontinuityListener, 
    handler: Handler
): Unit
```

Sets the listener to be invoked when a media time discontinuity is encountered.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnMediaTimeDiscontinuityListener](../android/media/MediaPlayer.OnMediaTimeDiscontinuityListener.md):the listener called after a discontinuity This value cannot be`null`. |
| `handler` | [Handler](../android/os/Handler.md):the [Handler](../android/os/Handler.md) that receives the listener events This value cannot be`null`. |

### setOnPreparedListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnPreparedListener(listener: MediaPlayer.OnPreparedListener!): Unit
```

Register a callback to be invoked when the media source is ready for playback.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnPreparedListener](../android/media/MediaPlayer.OnPreparedListener.md)!:the callback that will be run |

### setOnSeekCompleteListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnSeekCompleteListener(listener: MediaPlayer.OnSeekCompleteListener!): Unit
```

Register a callback to be invoked when a seek operation has been completed.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnSeekCompleteListener](../android/media/MediaPlayer.OnSeekCompleteListener.md)!:the callback that will be run |

### setOnSubtitleDataListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnSubtitleDataListener(listener: MediaPlayer.OnSubtitleDataListener): Unit
```

Sets the listener to be invoked when a subtitle track has new data available. The subtitle data comes from a subtitle track previously selected with [selectTrack(int)](../android/media/MediaPlayer.md)). Use [getTrackInfo()](../android/media/MediaPlayer.md))to determine which tracks are subtitles (of type [TrackInfo.MEDIA_TRACK_TYPE_SUBTITLE](../android/media/MediaPlayer.TrackInfo.md)), Subtitle track encodings can be determined by [TrackInfo.getFormat()](../android/media/MediaPlayer.TrackInfo.md))). 
See [SubtitleData](../android/media/SubtitleData.md) for an example of querying subtitle encoding. 
The listener will be called on the same thread as the one in which the MediaPlayer was created.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnSubtitleDataListener](../android/media/MediaPlayer.OnSubtitleDataListener.md):the listener called when new data is available This value cannot be`null`. |

### setOnSubtitleDataListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnSubtitleDataListener(
    listener: MediaPlayer.OnSubtitleDataListener, 
    handler: Handler
): Unit
```

Sets the listener to be invoked when a subtitle track has new data available. The subtitle data comes from a subtitle track previously selected with [selectTrack(int)](../android/media/MediaPlayer.md)). Use [getTrackInfo()](../android/media/MediaPlayer.md))to determine which tracks are subtitles (of type [TrackInfo.MEDIA_TRACK_TYPE_SUBTITLE](../android/media/MediaPlayer.TrackInfo.md)), Subtitle track encodings can be determined by [TrackInfo.getFormat()](../android/media/MediaPlayer.TrackInfo.md))). 
See [SubtitleData](../android/media/SubtitleData.md) for an example of querying subtitle encoding.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnSubtitleDataListener](../android/media/MediaPlayer.OnSubtitleDataListener.md):the listener called when new data is available This value cannot be`null`. |
| `handler` | [Handler](../android/os/Handler.md):the [Handler](../android/os/Handler.md) that receives the listener events This value cannot be`null`. |

### setOnTimedMetaDataAvailableListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnTimedMetaDataAvailableListener(listener: MediaPlayer.OnTimedMetaDataAvailableListener!): Unit
```

Register a callback to be invoked when a selected track has timed metadata available.

Currently only HTTP live streaming data URI's embedded with timed ID3 tags generates [TimedMetaData](../android/media/TimedMetaData.md).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnTimedMetaDataAvailableListener](../android/media/MediaPlayer.OnTimedMetaDataAvailableListener.md)!:the callback that will be run |

**See Also**

- [android.media.MediaPlayer#selectTrack(int)](../android/media/MediaPlayer.md))
- [android.media.MediaPlayer.OnTimedMetaDataAvailableListener](../android/media/MediaPlayer.OnTimedMetaDataAvailableListener.md)
- [android.media.TimedMetaData](../android/media/TimedMetaData.md) 

### setOnTimedTextListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnTimedTextListener(listener: MediaPlayer.OnTimedTextListener!): Unit
```

Register a callback to be invoked when a timed text is available for display.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnTimedTextListener](../android/media/MediaPlayer.OnTimedTextListener.md)!:the callback that will be run |

### setOnVideoSizeChangedListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnVideoSizeChangedListener(listener: MediaPlayer.OnVideoSizeChangedListener!): Unit
```

Register a callback to be invoked when the video size is known or updated.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaPlayer.OnVideoSizeChangedListener](../android/media/MediaPlayer.OnVideoSizeChangedListener.md)!:the callback that will be run |

### setPlaybackParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPlaybackParams(params: PlaybackParams): Unit
```

Sets playback rate using [PlaybackParams](../android/media/PlaybackParams.md). The object sets its internal PlaybackParams to the input, except that the object remembers previous speed when input speed is zero. This allows the object to resume at previous speed when start() is called. Calling it before the object is prepared does not change the object state. After the object is prepared, calling it with zero speed is equivalent to calling pause(). After the object is prepared, calling it with non-zero speed is equivalent to calling start().

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [PlaybackParams](../android/media/PlaybackParams.md):the playback params. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized or has been released. |
| `java.lang.IllegalArgumentException` | if params is not supported. |

### setPreferredDevice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferredDevice(deviceInfo: AudioDeviceInfo!): Boolean
```

Specifies an audio device (via an [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) object) to route the output from this MediaPlayer.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceInfo` | [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)!:The [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) specifying the audio sink or source. If deviceInfo is null, default routing is restored. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if succesful, false if the specified [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) is non-null and does not correspond to a valid audio device. |

### setScreenOnWhilePlaying

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScreenOnWhilePlaying(screenOn: Boolean): Unit
```

Control whether we should use the attached SurfaceHolder to keep the screen on while video playback is occurring. This is the preferred method over [setWakeMode](../android/media/MediaPlayer.md))where possible, since it doesn't require that the application have permission for low-level wake lock access.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `screenOn` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Supply true to keep the screen on, false to allow it to turn off. |

### setSurface

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSurface(surface: Surface!): Unit
```

Sets the [Surface](../android/view/Surface.md) to be used as the sink for the video portion of the media. This is similar to [setDisplay(android.view.SurfaceHolder)](../android/media/MediaPlayer.md)), but does not support [setScreenOnWhilePlaying(boolean)](../android/media/MediaPlayer.md)). Setting a Surface will un-set any Surface or SurfaceHolder that was previously set. A null surface will result in only the audio track being played. If the Surface sends frames to a [SurfaceTexture](../android/graphics/SurfaceTexture.md), the timestamps returned from [SurfaceTexture.getTimestamp()](../android/graphics/SurfaceTexture.md))will have an unspecified zero point. These timestamps cannot be directly compared between different media sources, different instances of the same media source, or multiple runs of the same program. The timestamp is normally monotonically increasing and is unaffected by time-of-day adjustments, but it is reset when the position is set.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [Surface](../android/view/Surface.md)!:The [Surface](../android/view/Surface.md) to be used for the video portion of the media. |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized or has been released. |

### setSyncParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSyncParams(params: SyncParams): Unit
```

Sets A/V sync mode.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [SyncParams](../android/media/SyncParams.md):the A/V sync params to apply This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized. |
| `java.lang.IllegalArgumentException` | if params are not supported. |

### setVideoScalingMode

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVideoScalingMode(mode: Int): Unit
```

Sets video scaling mode. To make the target video scaling mode effective during playback, this method must be called after data source is set. If not called, the default video scaling mode is [VIDEO_SCALING_MODE_SCALE_TO_FIT](../android/media/MediaPlayer.md).

The supported video scaling modes are:

- [VIDEO_SCALING_MODE_SCALE_TO_FIT](../android/media/MediaPlayer.md)
- [VIDEO_SCALING_MODE_SCALE_TO_FIT_WITH_CROPPING](../android/media/MediaPlayer.md)

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):target video scaling mode. Must be one of the supported video scaling modes; otherwise, IllegalArgumentException will be thrown. |

**See Also**

- [android.media.MediaPlayer#VIDEO_SCALING_MODE_SCALE_TO_FIT](../android/media/MediaPlayer.md)
- [android.media.MediaPlayer#VIDEO_SCALING_MODE_SCALE_TO_FIT_WITH_CROPPING](../android/media/MediaPlayer.md) 

### setVolume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVolume(
    leftVolume: Float, 
    rightVolume: Float
): Unit
```

Sets the volume on this player. This API is recommended for balancing the output of audio streams within an application. Unless you are writing an application to control user settings, this API should be used in preference to [AudioManager.setStreamVolume(int, int, int)](../android/media/AudioManager.md))which sets the volume of ALL streams of a particular type. Note that the passed volume values are raw scalars in range 0.0 to 1.0. UI controls should be scaled logarithmically.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------|
| `leftVolume` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):left volume scalar |
| `rightVolume` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):right volume scalar |

### setWakeMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWakeMode(
    context: Context!, 
    mode: Int
): Unit
```

Set the low-level power management behavior for this MediaPlayer. This can be used when the MediaPlayer is not playing through a SurfaceHolder set with [setDisplay(android.view.SurfaceHolder)](../android/media/MediaPlayer.md))and thus can use the high-level [setScreenOnWhilePlaying(boolean)](../android/media/MediaPlayer.md))feature.

This function has the MediaPlayer access the low-level power manager service to control the device's power usage while playing is occurring. The parameter is a combination of [android.os.PowerManager](../android/os/PowerManager.md) wake flags. Use of this method requires [android.Manifest.permission#WAKE_LOCK](../android/Manifest.permission.md) permission. By default, no attempt is made to keep the device awake during playback.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the Context to use |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the power/wake mode to set |

**See Also**

- [android.os.PowerManager](../android/os/PowerManager.md) 

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun start(): Unit
```

Starts or resumes playback. If playback had previously been paused, playback will continue from where it was paused. If playback had been stopped, or never started before, playback will start at the beginning.

| Exceptions ||
|-----------------------------------|-------------------------------------|
| `java.lang.IllegalStateException` | if it is called in an invalid state |

### stop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stop(): Unit
```

Stops playback after playback has been started or paused.

| Exceptions ||
|-----------------------------------|---------------------------------------------------------|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized. |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
