# AsyncPlayer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsyncPlayer

Kotlin| [Java](https://developer.android.com/reference/android/media/AsyncPlayer "View this page in Java") 

```
open class AsyncPlayer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.AsyncPlayer](https://developer.android.com/reference/kotlin/android/media/AsyncPlayer#) |

Plays a series of audio URIs, but does all the hard work on another thread so that any slowness with preparing or loading doesn't block the calling thread.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AsyncPlayer](https://developer.android.com/reference/kotlin/android/media/AsyncPlayer#AsyncPlayer(kotlin.String))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct an AsyncPlayer object. |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [play](https://developer.android.com/reference/kotlin/android/media/AsyncPlayer#play(android.content.Context,%20android.net.Uri,%20kotlin.Boolean,%20android.media.AudioAttributes))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `looping:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `attributes:` ` [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes)`)` Start playing the sound. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [play](https://developer.android.com/reference/kotlin/android/media/AsyncPlayer#play(android.content.Context,%20android.net.Uri,%20kotlin.Boolean,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `looping:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `stream:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start playing the sound. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](https://developer.android.com/reference/kotlin/android/media/AsyncPlayer#stop())`()` Stop a previously played sound. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):the non-null application's context. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):the non-null URI to play. (see [MediaPlayer.setDataSource(Context, Uri)](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#setDataSource(android.content.Context,%20android.net.Uri))) |
| `looping` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the audio should loop forever. (see [MediaPlayer.setLooping(boolean)](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#setLooping(kotlin.Boolean))) |
| `attributes` | [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes):the non-null [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes) to use. (see [MediaPlayer.setAudioAttributes(AudioAttributes)](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#setAudioAttributes(android.media.AudioAttributes))) |

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

**Deprecated:** *use [play(android.content.Context,android.net.Uri,boolean,android.media.AudioAttributes)](https://developer.android.com/reference/kotlin/android/media/AsyncPlayer#play(android.content.Context,%20android.net.Uri,%20kotlin.Boolean,%20android.media.AudioAttributes))instead*

Start playing the sound. It will actually start playing at some point in the future. There are no guarantees about latency here. Calling this before another audio file is done playing will stop that one and start the new one.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Your application's context. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:The URI to play. (see [MediaPlayer.setDataSource(Context, Uri)](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#setDataSource(android.content.Context,%20android.net.Uri))) |
| `looping` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the audio should loop forever. (see [MediaPlayer.setLooping(boolean)](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#setLooping(kotlin.Boolean))) |
| `stream` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the AudioStream to use. (see [MediaPlayer.setAudioStreamType(int)](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#setAudioStreamType(kotlin.Int))) |

### stop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stop(): Unit
```

Stop a previously played sound. It can't be played again or unpaused at this point. Calling this multiple times has no ill effects.
