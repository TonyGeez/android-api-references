# LoudnessCodecController

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LoudnessCodecController

Kotlin | [Java](https://developer.android.com/reference/android/media/LoudnessCodecController "View this page in Java") 
| --- | --- |

```
open class LoudnessCodecController : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.LoudnessCodecController](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#) |

Class for getting recommended loudness parameter updates for audio decoders as they are used to play back media content according to the encoded format and current audio routing. These audio decoder updates leverage loudness metadata present in compressed audio streams. They ensure the loudness and dynamic range of the content is optimized to the physical characteristics of the audio output device (e.g. phone microspeakers vs headphones vs TV speakers).Those updates can be automatically applied to the [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) instance(s), or be provided to the user. The codec loudness management parameter updates are computed in accordance to the CTA-2075 standard.

A new object should be instantiated for each audio session (see [AudioManager.generateAudioSessionId()](https://developer.android.com/reference/kotlin/android/media/AudioManager#generateAudioSessionId())) using creator methods [create(int)](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#create(kotlin.Int)) or [create(int,java.util.concurrent.Executor,android.media.LoudnessCodecController.OnLoudnessCodecUpdateListener)](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#create(kotlin.Int,%20java.util.concurrent.Executor,%20android.media.LoudnessCodecController.OnLoudnessCodecUpdateListener)).

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnLoudnessCodecUpdateListener](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener) Listener used for receiving asynchronous loudness metadata updates. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addMediaCodec](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#addMediaCodec(android.media.MediaCodec))`(`mediaCodec:` ` [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)`)` Adds a new [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) that will stream data to a player which uses #mSessionId. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#close())`()` Stops any loudness updates and frees up the resources. |
| open static [LoudnessCodecController](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#) | [create](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#create(kotlin.Int))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new instance of [LoudnessCodecController](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#) |
| --- | --- |
| open static [LoudnessCodecController](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#) | [create](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#create(kotlin.Int,%20java.util.concurrent.Executor,%20android.media.LoudnessCodecController.OnLoudnessCodecUpdateListener))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [LoudnessCodecController.OnLoudnessCodecUpdateListener](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener)`)` Creates a new instance of [LoudnessCodecController](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#) |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getLoudnessCodecParams](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#getLoudnessCodecParams(android.media.MediaCodec))`(`mediaCodec:` ` [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)`)` Returns the loudness parameters of the registered audio decoders |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeMediaCodec](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#removeMediaCodec(android.media.MediaCodec))`(`mediaCodec:` ` [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)`)` Removes the [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) from receiving loudness updates. |
| --- | --- |

## Public methods

### addMediaCodec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addMediaCodec(mediaCodec: MediaCodec): Boolean
```

Adds a new [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) that will stream data to a player which uses #mSessionId.

No new element will be added if the passed `mediaCodec` was previously added.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCodec` | [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec): the codec to start receiving asynchronous loudness updates. The codec has to be in a configured or started state in order to add it for loudness updates. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false` if the `mediaCodec` was not configured or does not contain loudness metadata, `true` otherwise. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the same `mediaCodec` was already added before. |

### close

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Stops any loudness updates and frees up the resources.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### create

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(sessionId: Int): LoudnessCodecController
```

Creates a new instance of [LoudnessCodecController](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#)

This method should be used when the client does not need to alter the codec loudness parameters before they are applied to the audio decoders. Otherwise, use [create(int,java.util.concurrent.Executor,android.media.LoudnessCodecController.OnLoudnessCodecUpdateListener)](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#create(kotlin.Int,%20java.util.concurrent.Executor,%20android.media.LoudnessCodecController.OnLoudnessCodecUpdateListener)).

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the session ID of the track that will receive data from the added [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)'s |

| Return ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [LoudnessCodecController](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#) | the [LoudnessCodecController](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#) instance |

### create

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    sessionId: Int, 
    executor: Executor, 
    listener: LoudnessCodecController.OnLoudnessCodecUpdateListener
): LoudnessCodecController
```

Creates a new instance of [LoudnessCodecController](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#)

This method should be used when the client wants to alter the codec loudness parameters before they are applied to the audio decoders. Otherwise, use [create(int)](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#create(kotlin.Int)).

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the session ID of the track that will receive data from the added [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)'s |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) to handle the callbacks Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `listener` | [LoudnessCodecController.OnLoudnessCodecUpdateListener](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener): used for receiving updates |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [LoudnessCodecController](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#) | the [LoudnessCodecController](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#) instance |

### getLoudnessCodecParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLoudnessCodecParams(mediaCodec: MediaCodec): Bundle
```

Returns the loudness parameters of the registered audio decoders

Those parameters may have been automatically applied if the `LoudnessCodecController` was created with [create(int)](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#create(kotlin.Int)), or they are the parameters that have been sent to the [OnLoudnessCodecUpdateListener](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener) if using a codec update listener.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCodec` | [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec): codec that decodes loudness annotated data. Has to be added with [addMediaCodec(android.media.MediaCodec)](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController#addMediaCodec(android.media.MediaCodec)) before calling this method |

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | the [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) containing the current loudness parameters. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the passed [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) was not added before calling this method |

### removeMediaCodec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeMediaCodec(mediaCodec: MediaCodec): Unit
```

Removes the [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) from receiving loudness updates.

This method can be called while asynchronous updates are live.

No elements will be removed if the passed mediaCodec was not added before.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCodec` | [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec): the element to remove for receiving asynchronous updates |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the `mediaCodec` was not configured, does not contain loudness metadata or if it was not added before |
