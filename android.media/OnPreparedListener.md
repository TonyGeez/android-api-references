# MediaPlayer.OnPreparedListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPreparedListener

Kotlin| [Java](../android/media/MediaPlayer.OnPreparedListener.md) 
| --- | --- |

```
interface OnPreparedListener
```

| [android.media.MediaPlayer.OnPreparedListener](../android/media/MediaPlayer.OnPreparedListener.md) |

Interface definition for a callback to be invoked when the media source is ready for playback.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepared](../android/media/MediaPlayer.OnPreparedListener.md))`(`mp:` ` [MediaPlayer](../android/media/MediaPlayer.md)!`)` Called when the media file is ready for playback. |

## Public methods

### onPrepared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPrepared(mp: MediaPlayer!): Unit
```

Called when the media file is ready for playback.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](../android/media/MediaPlayer.md)!:the MediaPlayer that is ready for playback |
