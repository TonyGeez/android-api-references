# MediaPlayer.OnBufferingUpdateListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBufferingUpdateListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaPlayer.OnBufferingUpdateListener "View this page in Java") 
| --- | --- |

```
interface OnBufferingUpdateListener
```

| [android.media.MediaPlayer.OnBufferingUpdateListener](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnBufferingUpdateListener#) |

Interface definition of a callback to be invoked indicating buffering status of a media resource being streamed over the network.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBufferingUpdate](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnBufferingUpdateListener#onBufferingUpdate(android.media.MediaPlayer,%20kotlin.Int))`(`mp:` ` [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!`, `percent:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to update status in buffering a media stream received through progressive HTTP download. |

## Public methods

### onBufferingUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBufferingUpdate(
    mp: MediaPlayer!, 
    percent: Int
): Unit
```

Called to update status in buffering a media stream received through progressive HTTP download. The received buffering percentage indicates how much of the content has been buffered or played. For example a buffering update of 80 percent when half the content has already been played indicates that the next 30 percent of the content to play has been buffered.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!:the MediaPlayer the update pertains to |
| `percent` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the percentage (0-100) of the content that has been buffered or played thus far |
