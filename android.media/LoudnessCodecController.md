# LoudnessCodecController

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LoudnessCodecController

Kotlin | [Java](LoudnessCodecController.md) 
| --- | --- |

```
open class LoudnessCodecController : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.LoudnessCodecController](LoudnessCodecController.md) |

Class for getting recommended loudness parameter updates for audio decoders as they are used to play back media content according to the encoded format and current audio routing. These audio decoder updates leverage loudness metadata present in compressed audio streams. They ensure the loudness and dynamic range of the content is optimized to the physical characteristics of the audio output device (e.g. phone microspeakers vs headphones vs TV speakers).Those updates can be automatically applied to the [MediaCodec](MediaCodec.md) instance(s), or be provided to the user. The codec loudness management parameter updates are computed in accordance to the CTA-2075 standard.

A new object should be instantiated for each audio session (see [AudioManager.generateAudioSessionId()](AudioManager.md))) using creator methods [create(int)](LoudnessCodecController.md)) or [create(int,java.util.concurrent.Executor,android.media.LoudnessCodecController.OnLoudnessCodecUpdateListener)](LoudnessCodecController.md)).

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnLoudnessCodecUpdateListener](../android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener.md) Listener used for receiving asynchronous loudness metadata updates. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addMediaCodec](LoudnessCodecController.md))`(`mediaCodec:` ` [MediaCodec](MediaCodec.md)`)` Adds a new [MediaCodec](MediaCodec.md) that will stream data to a player which uses #mSessionId. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](LoudnessCodecController.md))`()` Stops any loudness updates and frees up the resources. |
| open static [LoudnessCodecController](LoudnessCodecController.md) | [create](LoudnessCodecController.md))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new instance of [LoudnessCodecController](LoudnessCodecController.md) |
| --- | --- |
| open static [LoudnessCodecController](LoudnessCodecController.md) | [create](LoudnessCodecController.md))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `listener:` ` [LoudnessCodecController.OnLoudnessCodecUpdateListener](../android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener.md)`)` Creates a new instance of [LoudnessCodecController](LoudnessCodecController.md) |
| open [Bundle](../android.os/Bundle.md) | [getLoudnessCodecParams](LoudnessCodecController.md))`(`mediaCodec:` ` [MediaCodec](MediaCodec.md)`)` Returns the loudness parameters of the registered audio decoders |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeMediaCodec](LoudnessCodecController.md))`(`mediaCodec:` ` [MediaCodec](MediaCodec.md)`)` Removes the [MediaCodec](MediaCodec.md) from receiving loudness updates. |
| --- | --- |

## Public methods

### addMediaCodec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addMediaCodec(mediaCodec: MediaCodec): Boolean
```

Adds a new [MediaCodec](MediaCodec.md) that will stream data to a player which uses #mSessionId.

No new element will be added if the passed `mediaCodec` was previously added.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCodec` | [MediaCodec](MediaCodec.md): the codec to start receiving asynchronous loudness updates. The codec has to be in a configured or started state in order to add it for loudness updates. |

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

Creates a new instance of [LoudnessCodecController](LoudnessCodecController.md)

This method should be used when the client does not need to alter the codec loudness parameters before they are applied to the audio decoders. Otherwise, use [create(int,java.util.concurrent.Executor,android.media.LoudnessCodecController.OnLoudnessCodecUpdateListener)](LoudnessCodecController.md)).

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the session ID of the track that will receive data from the added [MediaCodec](MediaCodec.md)'s |

| Return ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [LoudnessCodecController](LoudnessCodecController.md) | the [LoudnessCodecController](LoudnessCodecController.md) instance |

### create

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    sessionId: Int, 
    executor: Executor, 
    listener: LoudnessCodecController.OnLoudnessCodecUpdateListener
): LoudnessCodecController
```

Creates a new instance of [LoudnessCodecController](LoudnessCodecController.md)

This method should be used when the client wants to alter the codec loudness parameters before they are applied to the audio decoders. Otherwise, use [create(int)](LoudnessCodecController.md)).

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the session ID of the track that will receive data from the added [MediaCodec](MediaCodec.md)'s |
| `executor` | [Executor](../java.util.concurrent/Executor.md): [Executor](../java.util.concurrent/Executor.md) to handle the callbacks Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `listener` | [LoudnessCodecController.OnLoudnessCodecUpdateListener](../android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener.md): used for receiving updates |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [LoudnessCodecController](LoudnessCodecController.md) | the [LoudnessCodecController](LoudnessCodecController.md) instance |

### getLoudnessCodecParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLoudnessCodecParams(mediaCodec: MediaCodec): Bundle
```

Returns the loudness parameters of the registered audio decoders

Those parameters may have been automatically applied if the `LoudnessCodecController` was created with [create(int)](LoudnessCodecController.md)), or they are the parameters that have been sent to the [OnLoudnessCodecUpdateListener](../android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener.md) if using a codec update listener.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCodec` | [MediaCodec](MediaCodec.md): codec that decodes loudness annotated data. Has to be added with [addMediaCodec(android.media.MediaCodec)](LoudnessCodecController.md)) before calling this method |

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](../android.os/Bundle.md) | the [Bundle](../android.os/Bundle.md) containing the current loudness parameters. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the passed [MediaCodec](MediaCodec.md) was not added before calling this method |

### removeMediaCodec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeMediaCodec(mediaCodec: MediaCodec): Unit
```

Removes the [MediaCodec](MediaCodec.md) from receiving loudness updates.

This method can be called while asynchronous updates are live.

No elements will be removed if the passed mediaCodec was not added before.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCodec` | [MediaCodec](MediaCodec.md): the element to remove for receiving asynchronous updates |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the `mediaCodec` was not configured, does not contain loudness metadata or if it was not added before |
