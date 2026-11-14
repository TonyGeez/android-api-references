# MediaPlayer.OnCompletionListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCompletionListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaPlayer.OnCompletionListener "View this page in Java") 

```
interface OnCompletionListener
```

| [android.media.MediaPlayer.OnCompletionListener](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnCompletionListener#) |

Interface definition for a callback to be invoked when playback of a media source has completed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCompletion](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnCompletionListener#onCompletion(android.media.MediaPlayer))`(`mp:` ` [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!`)` Called when the end of a media source is reached during playback. |

## Public methods

### onCompletion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCompletion(mp: MediaPlayer!): Unit
```

Called when the end of a media source is reached during playback.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!:the MediaPlayer that reached the end of the file |
