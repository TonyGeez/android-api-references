# SoundPool

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SoundPool

Kotlin| [Java](../android/media/SoundPool.md) 
| --- | --- |

```
open class SoundPool
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.SoundPool](../android/media/SoundPool.md) |

The SoundPool class manages and plays audio resources for applications.

A SoundPool is a collection of sound samples that can be loaded into memory from a resource inside the APK or from a file in the file system. The SoundPool library uses the MediaCodec service to decode the audio into raw 16-bit PCM. This allows applications to ship with compressed streams without having to suffer the CPU load and latency of decompressing during playback.

Soundpool sounds are expected to be short as they are predecoded into memory. Each decoded sound is internally limited to one megabyte storage, which represents approximately 5.6 seconds at 44.1kHz stereo (the duration is proportionally longer at lower sample rates or a channel mask of mono). A decoded audio sound will be truncated if it would exceed the per-sound one megabyte storage space.

In addition to low-latency playback, SoundPool can also manage the number of audio streams being rendered at once. When the SoundPool object is constructed, the maxStreams parameter sets the maximum number of streams that can be played at a time from this single SoundPool. SoundPool tracks the number of active streams. If the maximum number of streams is exceeded, SoundPool will automatically stop a previously playing stream based first on priority and then by age within that priority. Limiting the maximum number of streams helps to cap CPU loading and reducing the likelihood that audio mixing will impact visuals or UI performance.

Sounds can be looped by setting a non-zero loop value. A value of -1 causes the sound to loop forever. In this case, the application must explicitly call the stop() function to stop the sound. Any other non-zero value will cause the sound to repeat the specified number of times, e.g. a value of 3 causes the sound to play a total of 4 times.

The playback rate can also be changed. A playback rate of 1.0 causes the sound to play at its original frequency (resampled, if necessary, to the hardware output frequency). A playback rate of 2.0 causes the sound to play at twice its original frequency, and a playback rate of 0.5 causes it to play at half its original frequency. The playback rate range is 0.5 to 2.0.

Priority runs low to high, i.e. higher numbers are higher priority. Priority is used when a call to play() would cause the number of active streams to exceed the value established by the maxStreams parameter when the SoundPool was created. In this case, the stream allocator will stop the lowest priority stream. If there are multiple streams with the same low priority, it will choose the oldest stream to stop. In the case where the priority of the new stream is lower than all the active streams, the new sound will not play and the play() function will return a streamID of zero.

Let's examine a typical use case: A game consists of several levels of play. For each level, there is a set of unique sounds that are used only by that level. In this case, the game logic should create a new SoundPool object when the first level is loaded. The level data itself might contain the list of sounds to be used by this level. The loading logic iterates through the list of sounds calling the appropriate SoundPool.load() function. This should typically be done early in the process to allow time for decompressing the audio to raw PCM format before they are needed for playback.

Once the sounds are loaded and play has started, the application can trigger sounds by calling SoundPool.play(). Playing streams can be paused or resumed, and the application can also alter the pitch by adjusting the playback rate in real-time for doppler or synthesis effects.

Note that since streams can be stopped due to resource constraints, the streamID is a reference to a particular instance of a stream. If the stream is stopped to allow a higher priority stream to play, the stream is no longer valid. However, the application is allowed to call methods on the streamID without error. This may help simplify program logic since the application need not concern itself with the stream lifecycle.

In our example, when the player has completed the level, the game logic should call SoundPool.release() to release all the native resources in use and then set the SoundPool reference to null. If the player starts another level, a new SoundPool is created, sounds are loaded, and play resumes.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](../android/media/SoundPool.Builder.md) Builder class for [SoundPool](../android/media/SoundPool.md) objects. |
| abstract | [OnLoadCompleteListener](../android/media/SoundPool.OnLoadCompleteListener.md) <br /> |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SoundPool](../android/media/SoundPool.md))`(`maxStreams:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `streamType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `srcQuality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor. |

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [autoPause](../android/media/SoundPool.md))`()` Pause all active streams. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [autoResume](../android/media/SoundPool.md))`()` Resume all previously active streams. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [load](../android/media/SoundPool.md))`(`context:` ` [Context](../android/content/Context.md)!`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Load the sound from the specified APK resource. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [load](../android/media/SoundPool.md))`(`afd:` ` [AssetFileDescriptor](../android/content/res/AssetFileDescriptor.md)!`, `priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Load the sound from an asset file descriptor. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [load](../android/media/SoundPool.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`, `offset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Load the sound from a FileDescriptor. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [load](../android/media/SoundPool.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Load the sound from the specified path. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pause](../android/media/SoundPool.md))`(`streamID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Pause a playback stream. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [play](../android/media/SoundPool.md))`(`soundID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `leftVolume:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `rightVolume:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `loop:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rate:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Play a sound from a sound ID. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](../android/media/SoundPool.md))`()` Release the SoundPool resources. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resume](../android/media/SoundPool.md))`(`streamID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Resume a playback stream. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLoop](../android/media/SoundPool.md))`(`streamID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `loop:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set loop mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnLoadCompleteListener](../android/media/SoundPool.md))`(`listener:` ` [SoundPool.OnLoadCompleteListener](../android/media/SoundPool.OnLoadCompleteListener.md)!`)` Sets the callback hook for the OnLoadCompleteListener. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPriority](../android/media/SoundPool.md))`(`streamID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change stream priority. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRate](../android/media/SoundPool.md))`(`streamID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rate:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Change playback rate. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVolume](../android/media/SoundPool.md))`(`streamID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `leftVolume:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `rightVolume:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set stream volume. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](../android/media/SoundPool.md))`(`streamID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Stop a playback stream. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unload](../android/media/SoundPool.md))`(`soundID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Unload a sound from a sound ID. |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/media/SoundPool.md))`()` <br /> |

## Public constructors

### SoundPool

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SoundPool(
    maxStreams: Int, 
    streamType: Int, 
    srcQuality: Int)
```

**Deprecated:** *use [SoundPool.Builder](../android/media/SoundPool.Builder.md) instead to create and configure a SoundPool instance*

Constructor. Constructs a SoundPool object with the following characteristics:

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `maxStreams` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of simultaneous streams for this SoundPool object |
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the audio stream type as described in AudioManager For example, game applications will normally use [AudioManager.STREAM_MUSIC](../android/media/AudioManager.md). |
| `srcQuality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the sample-rate converter quality. Currently has no effect. Use 0 for the default. |
| --- | --- |

| Return ||
|---|------------------------------------------------|
| | a SoundPool object, or null if creation failed |

## Public methods

### autoPause

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun autoPause(): Unit
```

Pause all active streams. Pause all streams that are currently playing. This function iterates through all the active streams and pauses any that are playing. It also sets a flag so that any streams that are playing can be resumed by calling autoResume(). 

### autoResume

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun autoResume(): Unit
```

Resume all previously active streams. Automatically resumes all streams that were paused in previous calls to autoPause(). 

### load

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun load(
    context: Context!, 
    resId: Int, 
    priority: Int
): Int
```

Load the sound from the specified APK resource. Note that the extension is dropped. For example, if you want to load a sound from the raw resource file "explosion.mp3", you would specify "R.raw.explosion" as the resource ID. Note that this means you cannot have both an "explosion.wav" and an "explosion.mp3" in the res/raw directory.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the application context |
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the resource ID |
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the priority of the sound. Currently has no effect. Use a value of 1 for future compatibility. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a sound ID. This value can be used to play or unload the sound. |

### load

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun load(
    afd: AssetFileDescriptor!, 
    priority: Int
): Int
```

Load the sound from an asset file descriptor.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `afd` | [AssetFileDescriptor](../android/content/res/AssetFileDescriptor.md)!:an asset file descriptor |
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the priority of the sound. Currently has no effect. Use a value of 1 for future compatibility. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a sound ID. This value can be used to play or unload the sound. |

### load

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun load(
    fd: FileDescriptor!, 
    offset: Long, 
    length: Long, 
    priority: Int
): Int
```

Load the sound from a FileDescriptor. This version is useful if you store multiple sounds in a single binary. The offset specifies the offset from the start of the file and the length specifies the length of the sound within the file.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md)!:a FileDescriptor object |
| `offset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):offset to the start of the sound |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):length of the sound |
| --- | --- |
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the priority of the sound. Currently has no effect. Use a value of 1 for future compatibility. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a sound ID. This value can be used to play or unload the sound. |

### load

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun load(
    path: String!, 
    priority: Int
): Int
```

Load the sound from the specified path.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path to the audio file |
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the priority of the sound. Currently has no effect. Use a value of 1 for future compatibility. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a sound ID. This value can be used to play or unload the sound. |

### pause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun pause(streamID: Int): Unit
```

Pause a playback stream. Pause the stream specified by the streamID. This is the value returned by the play() function. If the stream is playing, it will be paused. If the stream is not playing (e.g. is stopped or was previously paused), calling this function will have no effect.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------|
| `streamID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a streamID returned by the play() function |

### play

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun play(
    soundID: Int, 
    leftVolume: Float, 
    rightVolume: Float, 
    priority: Int, 
    loop: Int, 
    rate: Float
): Int
```

Play a sound from a sound ID. Play the sound specified by the soundID. This is the value returned by the load() function. Returns a non-zero streamID if successful, zero if it fails. The streamID can be used to further control playback. Note that calling play() may cause another sound to stop playing if the maximum number of active streams is exceeded. A loop value of -1 means loop forever, a value of 0 means don't loop, other values indicate the number of repeats, e.g. a value of 1 plays the audio twice. The playback rate allows the application to vary the playback rate (pitch) of the sound. A value of 1.0 means play back at the original frequency. A value of 2.0 means play back twice as fast, and a value of 0.5 means playback at half speed.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `soundID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a soundID returned by the load() function |
| `leftVolume` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):left volume value (range = 0.0 to 1.0) |
| `rightVolume` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):right volume value (range = 0.0 to 1.0) |
| --- | --- |
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):stream priority (0 = lowest priority) |
| `loop` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):loop mode (0 = no loop, -1 = loop forever) |
| `rate` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):playback rate (1.0 = normal playback, range 0.5 to 2.0) |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | non-zero streamID if successful, zero if failed |

### release

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun release(): Unit
```

Release the SoundPool resources. Release all memory and native resources used by the SoundPool object. The SoundPool can no longer be used and the reference should be set to null. 

### resume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun resume(streamID: Int): Unit
```

Resume a playback stream. Resume the stream specified by the streamID. This is the value returned by the play() function. If the stream is paused, this will resume playback. If the stream was not previously paused, calling this function will have no effect.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------|
| `streamID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a streamID returned by the play() function |

### setLoop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLoop(
    streamID: Int, 
    loop: Int
): Unit
```

Set loop mode. Change the loop mode. A loop value of -1 means loop forever, a value of 0 means don't loop, other values indicate the number of repeats, e.g. a value of 1 plays the audio twice. If the stream does not exist, it will have no effect.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------|
| `streamID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a streamID returned by the play() function |
| `loop` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):loop mode (0 = no loop, -1 = loop forever) |

### setOnLoadCompleteListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnLoadCompleteListener(listener: SoundPool.OnLoadCompleteListener!): Unit
```

Sets the callback hook for the OnLoadCompleteListener. 

### setPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPriority(
    streamID: Int, 
    priority: Int
): Unit
```

Change stream priority. Change the priority of the stream specified by the streamID. This is the value returned by the play() function. Affects the order in which streams are re-used to play new sounds. If the stream does not exist, it will have no effect.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------|
| `streamID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a streamID returned by the play() function |

### setRate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRate(
    streamID: Int, 
    rate: Float
): Unit
```

Change playback rate. The playback rate allows the application to vary the playback rate (pitch) of the sound. A value of 1.0 means playback at the original frequency. A value of 2.0 means playback twice as fast, and a value of 0.5 means playback at half speed. If the stream does not exist, it will have no effect.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `streamID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a streamID returned by the play() function |
| `rate` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):playback rate (1.0 = normal playback, range 0.5 to 2.0) |

### setVolume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setVolume(
    streamID: Int, 
    leftVolume: Float, 
    rightVolume: Float
): Unit
```

Set stream volume. Sets the volume on the stream specified by the streamID. This is the value returned by the play() function. The value must be in the range of 0.0 to 1.0. If the stream does not exist, it will have no effect.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------|
| `streamID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a streamID returned by the play() function |
| `leftVolume` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):left volume value (range = 0.0 to 1.0) |
| `rightVolume` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):right volume value (range = 0.0 to 1.0) |
| --- | --- |

### stop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stop(streamID: Int): Unit
```

Stop a playback stream. Stop the stream specified by the streamID. This is the value returned by the play() function. If the stream is playing, it will be stopped. It also releases any native resources associated with this stream. If the stream is not playing, it will have no effect.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------|
| `streamID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a streamID returned by the play() function |

### unload

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unload(soundID: Int): Boolean
```

Unload a sound from a sound ID. Unloads the sound specified by the soundID. This is the value returned by the load() function. Returns true if the sound is successfully unloaded, false if the sound was already unloaded.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------|
| `soundID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a soundID returned by the load() function |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if just unloaded, false if previously unloaded |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
