# MediaPlayer.OnSeekCompleteListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSeekCompleteListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaPlayer.OnSeekCompleteListener "View this page in Java") 
| --- | --- |

```
interface OnSeekCompleteListener
```

| [android.media.MediaPlayer.OnSeekCompleteListener](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnSeekCompleteListener#) |

Interface definition of a callback to be invoked indicating the completion of a seek operation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSeekComplete](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnSeekCompleteListener#onSeekComplete(android.media.MediaPlayer))`(`mp:` ` [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!`)` Called to indicate the completion of a seek operation. |

## Public methods

### onSeekComplete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSeekComplete(mp: MediaPlayer!): Unit
```

Called to indicate the completion of a seek operation.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!:the MediaPlayer that issued the seek operation |
