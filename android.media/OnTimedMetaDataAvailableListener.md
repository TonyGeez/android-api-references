# MediaPlayer.OnTimedMetaDataAvailableListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnTimedMetaDataAvailableListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaPlayer.OnTimedMetaDataAvailableListener "View this page in Java") 
| --- | --- |

```
interface OnTimedMetaDataAvailableListener
```

| [android.media.MediaPlayer.OnTimedMetaDataAvailableListener](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnTimedMetaDataAvailableListener#) |

Interface definition of a callback to be invoked when a track has timed metadata available.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTimedMetaDataAvailable](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnTimedMetaDataAvailableListener#onTimedMetaDataAvailable(android.media.MediaPlayer,%20android.media.TimedMetaData))`(`mp:` ` [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!`, `data:` ` [TimedMetaData](https://developer.android.com/reference/kotlin/android/media/TimedMetaData)!`)` Called to indicate avaliable timed metadata |

## Public methods

### onTimedMetaDataAvailable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTimedMetaDataAvailable(
    mp: MediaPlayer!, 
    data: TimedMetaData!
): Unit
```

Called to indicate avaliable timed metadata

This method will be called as timed metadata is extracted from the media, in the same order as it occurs in the media. The timing of this event is not controlled by the associated timestamp.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!:the MediaPlayer associated with this callback |
| `data` | [TimedMetaData](https://developer.android.com/reference/kotlin/android/media/TimedMetaData)!:the timed metadata sample associated with this event |
