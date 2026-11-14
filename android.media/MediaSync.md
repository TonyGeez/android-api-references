Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaSync

```
class MediaSync
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaSync](MediaSync.md) |

MediaSync class can be used to synchronously play audio and video streams. It can be used to play audio-only or video-only stream, too.

MediaSync is generally used like this:

```kotlin
MediaSync sync = new MediaSync();
  sync.setSurface(surface);
  Surface inputSurface = sync.createInputSurface();
  ...
  // MediaCodec videoDecoder = ...;
  videoDecoder.configure(format, inputSurface, ...);
  ...
  sync.setAudioTrack(audioTrack);
  sync.setCallback(new MediaSync.Callback() {
      @Override
      public void onAudioBufferConsumed(MediaSync sync, ByteBuffer audioBuffer, int bufferId) {
          ...
      }
  }, null);
  // This needs to be done since sync is paused on creation.
  sync.setPlaybackParams(new PlaybackParams().setSpeed(1.f));
 
  for (;;) {
    ...
    // send video frames to surface for rendering, e.g., call
    // videoDecoder.releaseOutputBuffer(videoOutputBufferIx, videoPresentationTimeNs);
    // More details are available as below.
    ...
    sync.queueAudio(audioByteBuffer, bufferId, audioPresentationTimeUs); // non-blocking.
    // The audioByteBuffer and bufferId will be returned via callback.
    // More details are available as below.
    ...
      ...
  }
  sync.setPlaybackParams(new PlaybackParams().setSpeed(0.f));
  sync.release();
  sync = null;
 
  // The following code snippet illustrates how video/audio raw frames are created by
  // MediaCodec's, how they are fed to MediaSync and how they are returned by MediaSync.
  // This is the callback from MediaCodec.
  onOutputBufferAvailable(MediaCodec codec, int bufferId, BufferInfo info) {
      // ...
      if (codec == videoDecoder) {
          // surface timestamp must contain media presentation time in nanoseconds.
          codec.releaseOutputBuffer(bufferId, 1000 * info.presentationTime);
      } else {
          ByteBuffer audioByteBuffer = codec.getOutputBuffer(bufferId);
          sync.queueAudio(audioByteBuffer, bufferId, info.presentationTime);
      }
      // ...
  }
 
  // This is the callback from MediaSync.
  onAudioBufferConsumed(MediaSync sync, ByteBuffer buffer, int bufferId) {
      // ...
      audioDecoder.releaseBuffer(bufferId, false);
      // ...
  }
 
  
```
The client needs to configure corresponding sink by setting the Surface and/or AudioTrack based on the stream type it will play.

For video, the client needs to call `https://developer.android.com/reference/kotlin/android/media/MediaSync#createInputSurface()` to obtain a surface on which it will render video frames.

For audio, the client needs to set up audio track correctly, e.g., using `https://developer.android.com/reference/kotlin/android/media/AudioTrack#MODE_STREAM:kotlin.Int`. The audio buffers are sent to MediaSync directly via `https://developer.android.com/reference/kotlin/android/media/MediaSync#queueAudio(java.nio.ByteBuffer,%20kotlin.Int,%20kotlin.Long)`, and are returned to the client via `https://developer.android.com/reference/kotlin/android/media/MediaSync.Callback#onAudioBufferConsumed(android.media.MediaSync,%20java.nio.ByteBuffer,%20kotlin.Int)` asynchronously. The client should not modify an audio buffer till it's returned.

The client can optionally pre-fill audio/video buffers by setting playback rate to 0.0, and then feed audio/video buffers to corresponding components. This can reduce possible initial underrun.

<br />

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaSync.Callback` MediaSync callback interface. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaSync.OnErrorListener` Interface definition of a callback to be invoked when there has been an error during an asynchronous operation (other errors will throw exceptions at method call time). |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#MEDIASYNC_ERROR_AUDIOTRACK_FAIL:kotlin.Int` Audio track failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#MEDIASYNC_ERROR_SURFACE_FAIL:kotlin.Int` The surface failed to handle video buffers. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaSync#MediaSync()()` Class constructor. |

| Public methods ||
|---|---|
| [Surface](../android.view/Surface.md) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#createInputSurface()()` Requests a Surface to use as the input. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#flush()()` Flushes all buffers from the sync object. |
| [PlaybackParams](PlaybackParams.md) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#getPlaybackParams()()` Gets the playback rate using `https://developer.android.com/reference/kotlin/android/media/PlaybackParams`. |
| --- | --- |
| [SyncParams](SyncParams.md) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#getSyncParams()()` Gets the A/V sync mode. |
| [MediaTimestamp](MediaTimestamp.md)? | `https://developer.android.com/reference/kotlin/android/media/MediaSync#getTimestamp()()` Get current playback position. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#queueAudio(java.nio.ByteBuffer,%20kotlin.Int,%20kotlin.Long)(audioData: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#, bufferId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, presentationTimeUs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Queues the audio data asynchronously for playback (AudioTrack must be in streaming mode). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#release()()` Make sure you call this when you're done to free up any opened component instance instead of relying on the garbage collector to do this for you at some point in the future. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#setAudioTrack(android.media.AudioTrack)(audioTrack: https://developer.android.com/reference/kotlin/android/media/AudioTrack?)` Sets the audio track for MediaSync. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#setCallback(android.media.MediaSync.Callback,%20android.os.Handler)(cb: https://developer.android.com/reference/kotlin/android/media/MediaSync.Callback?, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Sets an asynchronous callback for actionable MediaSync events. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#setOnErrorListener(android.media.MediaSync.OnErrorListener,%20android.os.Handler)(listener: https://developer.android.com/reference/kotlin/android/media/MediaSync.OnErrorListener?, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Sets an asynchronous callback for error events. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#setPlaybackParams(android.media.PlaybackParams)(params: https://developer.android.com/reference/kotlin/android/media/PlaybackParams)` Sets playback rate using `https://developer.android.com/reference/kotlin/android/media/PlaybackParams`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#setSurface(android.view.Surface)(surface: https://developer.android.com/reference/kotlin/android/view/Surface.html#?)` Sets the output surface for MediaSync. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#setSyncParams(android.media.SyncParams)(params: https://developer.android.com/reference/kotlin/android/media/SyncParams)` Sets A/V sync mode. |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaSync#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Constants

### MEDIASYNC_ERROR_AUDIOTRACK_FAIL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEDIASYNC_ERROR_AUDIOTRACK_FAIL: Int
```

Audio track failed.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaSync.OnErrorListener`

### MEDIASYNC_ERROR_SURFACE_FAIL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEDIASYNC_ERROR_SURFACE_FAIL: Int
```

The surface failed to handle video buffers.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaSync.OnErrorListener`

## Public constructors

### MediaSync

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MediaSync()
```

Class constructor. On creation, MediaSync is paused, i.e., playback rate is 0.0f.

## Public methods

### createInputSurface

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createInputSurface(): Surface
```

Requests a Surface to use as the input. This may only be called after `https://developer.android.com/reference/kotlin/android/media/MediaSync#setSurface(android.view.Surface)`.

The application is responsible for calling release() on the Surface when done.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Surface.html#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if not set, or another input surface has already been created. |

### flush

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun flush(): Unit
```

Flushes all buffers from the sync object.

All pending unprocessed audio and video buffers are discarded. If an audio track was configured, it is flushed and stopped. If a video output surface was configured, the last frame queued to it is left on the frame. Queue a blank video frame to clear the surface,

No callbacks are received for the flushed buffers.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized. |

### getPlaybackParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPlaybackParams(): PlaybackParams
```

Gets the playback rate using `https://developer.android.com/reference/kotlin/android/media/PlaybackParams`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/PlaybackParams` | the playback rate being used. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the internal sync engine or the audio track has not been initialized. |

### getSyncParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSyncParams(): SyncParams
```

Gets the A/V sync mode.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/SyncParams` | the A/V sync params. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized. |

### getTimestamp

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTimestamp(): MediaTimestamp?
```

Get current playback position.

The MediaTimestamp represents how the media time correlates to the system time in a linear fashion using an anchor and a clock rate. During regular playback, the media time moves fairly constantly (though the anchor frame may be rebased to a current system time, the linear correlation stays steady). Therefore, this method does not need to be called often.

To help users get current playback position, this method always anchors the timestamp to the current `https://developer.android.com/reference/kotlin/java/lang/System.html#nanoTime()`, so `https://developer.android.com/reference/kotlin/android/media/MediaTimestamp#getAnchorMediaTimeUs()` can be used as current playback position.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaTimestamp?` | a MediaTimestamp object if a timestamp is available, or `null` if no timestamp is available, e.g. because the media player has not been initialized. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaTimestamp`

### queueAudio

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queueAudio(
    audioData: ByteBuffer, 
    bufferId: Int, 
    presentationTimeUs: Long
): Unit
```

Queues the audio data asynchronously for playback (AudioTrack must be in streaming mode). If the audio track was flushed as a result of `https://developer.android.com/reference/kotlin/android/media/MediaSync#flush()`, it will be restarted.

| Parameters ||
|---|---|
| `audioData` | [ByteBuffer](../java.nio/ByteBuffer.md): the buffer that holds the data to play. This buffer will be returned to the client via registered callback. This value cannot be `null`. |
| `bufferId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an integer used to identify audioData. It will be returned to the client along with audioData. This helps applications to keep track of audioData, e.g., it can be used to store the output buffer index used by the audio codec. |
| `presentationTimeUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the presentation timestamp in microseconds for the first frame in the buffer. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if audio track is not set or internal configureation has not been done correctly. |

### release

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun release(): Unit
```

Make sure you call this when you're done to free up any opened component instance instead of relying on the garbage collector to do this for you at some point in the future.

### setAudioTrack

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAudioTrack(audioTrack: AudioTrack?): Unit
```

Sets the audio track for MediaSync.

Currently, this is only supported in the Initialized state.

| Parameters ||
|---|---|
| `audioTrack` | [AudioTrack](AudioTrack.md)?: Specify an AudioTrack through which to render the audio data. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the audioTrack has been released, or is invalid. |
| `java.lang.IllegalStateException` | if setting the audio track is not supported, e.g. not in the Initialized state, or another audio track has already been set. |

### setCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCallback(
    cb: MediaSync.Callback?, 
    handler: Handler?
): Unit
```

Sets an asynchronous callback for actionable MediaSync events.

This method can be called multiple times to update a previously set callback. If the handler is changed, undelivered notifications scheduled for the old handler may be dropped.

**Do not call this inside callback.**

| Parameters ||
|---|---|
| `cb` | [MediaSync.Callback](../android/media/MediaSync.Callback.md)?: The callback that will run. Use `null` to stop receiving callbacks. |
| `handler` | [Handler](../android.os/Handler.md)?: The Handler that will run the callback. Use `null` to use MediaSync's internal handler if it exists. |

### setOnErrorListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOnErrorListener(
    listener: MediaSync.OnErrorListener?, 
    handler: Handler?
): Unit
```

Sets an asynchronous callback for error events.

This method can be called multiple times to update a previously set listener. If the handler is changed, undelivered notifications scheduled for the old handler may be dropped.

**Do not call this inside callback.**

| Parameters ||
|---|---|
| `listener` | [MediaSync.OnErrorListener](../android/media/MediaSync.OnErrorListener.md)?: The callback that will run. Use `null` to stop receiving callbacks. |
| `handler` | [Handler](../android.os/Handler.md)?: The Handler that will run the callback. Use `null` to use MediaSync's internal handler if it exists. |

### setPlaybackParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPlaybackParams(params: PlaybackParams): Unit
```

Sets playback rate using `https://developer.android.com/reference/kotlin/android/media/PlaybackParams`.

When using MediaSync with `https://developer.android.com/reference/kotlin/android/media/AudioTrack`, set playback params using this call instead of calling it directly on the track, so that the sync is aware of the params change.

This call also works if there is no audio track.

| Parameters ||
|---|---|
| `params` | [PlaybackParams](PlaybackParams.md): the playback params to use. `https://developer.android.com/reference/kotlin/android/media/PlaybackParams#getSpeed()` is the ratio between desired playback rate and normal one. 1.0 means normal playback speed. 0.0 means pause. Value larger than 1.0 means faster playback, while value between 0.0 and 1.0 for slower playback. **Note:** the normal rate does not change as a result of this call. To restore the original rate at any time, use speed of 1.0. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the params are not supported. |
| `java.lang.IllegalStateException` | if the internal sync engine or the audio track has not been initialized. |

### setSurface

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setSurface(surface: Surface?): Unit
```

Sets the output surface for MediaSync.

Currently, this is only supported in the Initialized state.

| Parameters ||
|---|---|
| `surface` | [Surface](../android.view/Surface.md)?: Specify a surface on which to render the video data. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the surface has been released, is invalid, or can not be connected. |
| `java.lang.IllegalStateException` | if setting the surface is not supported, e.g. not in the Initialized state, or another surface has already been set. |

### setSyncParams

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setSyncParams(params: SyncParams): Unit
```

Sets A/V sync mode.

| Parameters ||
|---|---|
| `params` | [SyncParams](SyncParams.md): the A/V sync params to apply. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if params are not supported. |
| `java.lang.IllegalStateException` | if the internal player engine has not been initialized. |

## Protected methods

### finalize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun finalize(): Unit
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
