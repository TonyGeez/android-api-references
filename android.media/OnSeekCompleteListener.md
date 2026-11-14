# MediaPlayer.OnSeekCompleteListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSeekCompleteListener

Kotlin| [Java](../android/media/MediaPlayer.OnSeekCompleteListener.md) 
| --- | --- |

```
interface OnSeekCompleteListener
```

| [android.media.MediaPlayer.OnSeekCompleteListener](../android/media/MediaPlayer.OnSeekCompleteListener.md) |

Interface definition of a callback to be invoked indicating the completion of a seek operation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSeekComplete](../android/media/MediaPlayer.OnSeekCompleteListener.md))`(`mp:` ` [MediaPlayer](../android/media/MediaPlayer.md)!`)` Called to indicate the completion of a seek operation. |

## Public methods

### onSeekComplete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSeekComplete(mp: MediaPlayer!): Unit
```

Called to indicate the completion of a seek operation.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](../android/media/MediaPlayer.md)!:the MediaPlayer that issued the seek operation |
