# AsyncPlayer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsyncPlayer

Kotlin| [Java](../android/media/AsyncPlayer.md) 
| --- | --- |

```
open class AsyncPlayer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AsyncPlayer](../android/media/AsyncPlayer.md) |

Plays a series of audio URIs, but does all the hard work on another thread so that any slowness with preparing or loading doesn't block the calling thread.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AsyncPlayer](../android/media/AsyncPlayer.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct an AsyncPlayer object. |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [play](../android/media/AsyncPlayer.md))`(`context:` ` [Context](../android/content/Context.md)`, `uri:` ` [Uri](../android/net/Uri.md)`, `looping:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `attributes:` ` [AudioAttributes](../android/media/AudioAttributes.md)`)` Start playing the sound. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [play](../android/media/AsyncPlayer.md))`(`context:` ` [Context](../android/content/Context.md)!`, `uri:` ` [Uri](../android/net/Uri.md)!`, `looping:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `stream:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start playing the sound. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](../android/media/AsyncPlayer.md))`()` Stop a previously played sound. |
| --- | --- |

## Public constructors

### AsyncPlayer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AsyncPlayer(tag: String!)
```

Construct an AsyncPlayer object.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string to use for debugging |

## Public methods

### play

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun play(
    context: Context, 
    uri: Uri, 
    looping: Boolean, 
    attributes: AudioAttributes
): Unit
```

Start playing the sound. It will actually start playing at some point in the future. There are no guarantees about latency here. Calling this before another audio file is done playing will stop that one and start the new one.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):the non-null application's context. |
| `uri` | [Uri](../android/net/Uri.md):the non-null URI to play. (see [MediaPlayer.setDataSource(Context, Uri)](../android/media/MediaPlayer.md))) |
| `looping` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the audio should loop forever. (see [MediaPlayer.setLooping(boolean)](../android/media/MediaPlayer.md))) |
| --- | --- |
| `attributes` | [AudioAttributes](../android/media/AudioAttributes.md):the non-null [AudioAttributes](../android/media/AudioAttributes.md) to use. (see [MediaPlayer.setAudioAttributes(AudioAttributes)](../android/media/MediaPlayer.md))) |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalArgumentException` | |

### play

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun play(
    context: Context!, 
    uri: Uri!, 
    looping: Boolean, 
    stream: Int
): Unit
```

**Deprecated:** *use [play(android.content.Context,android.net.Uri,boolean,android.media.AudioAttributes)](../android/media/AsyncPlayer.md))instead*

Start playing the sound. It will actually start playing at some point in the future. There are no guarantees about latency here. Calling this before another audio file is done playing will stop that one and start the new one.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:Your application's context. |
| `uri` | [Uri](../android/net/Uri.md)!:The URI to play. (see [MediaPlayer.setDataSource(Context, Uri)](../android/media/MediaPlayer.md))) |
| `looping` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the audio should loop forever. (see [MediaPlayer.setLooping(boolean)](../android/media/MediaPlayer.md))) |
| --- | --- |
| `stream` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the AudioStream to use. (see [MediaPlayer.setAudioStreamType(int)](../android/media/MediaPlayer.md))) |

### stop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stop(): Unit
```

Stop a previously played sound. It can't be played again or unpaused at this point. Calling this multiple times has no ill effects.
