# MediaPlayer.OnCompletionListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCompletionListener

Kotlin| [Java](../android/media/MediaPlayer.OnCompletionListener.md) 
| --- | --- |

```
interface OnCompletionListener
```

| [android.media.MediaPlayer.OnCompletionListener](../android/media/MediaPlayer.OnCompletionListener.md) |

Interface definition for a callback to be invoked when playback of a media source has completed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCompletion](../android/media/MediaPlayer.OnCompletionListener.md))`(`mp:` ` [MediaPlayer](../android/media/MediaPlayer.md)!`)` Called when the end of a media source is reached during playback. |

## Public methods

### onCompletion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCompletion(mp: MediaPlayer!): Unit
```

Called when the end of a media source is reached during playback.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](../android/media/MediaPlayer.md)!:the MediaPlayer that reached the end of the file |
