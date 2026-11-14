# MediaPlayer.OnPreparedListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPreparedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaPlayer.OnPreparedListener "View this page in Java") 
| --- | --- |

```
interface OnPreparedListener
```

| [android.media.MediaPlayer.OnPreparedListener](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnPreparedListener#) |

Interface definition for a callback to be invoked when the media source is ready for playback.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepared](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnPreparedListener#onPrepared(android.media.MediaPlayer))`(`mp:` ` [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!`)` Called when the media file is ready for playback. |

## Public methods

### onPrepared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPrepared(mp: MediaPlayer!): Unit
```

Called when the media file is ready for playback.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!:the MediaPlayer that is ready for playback |
