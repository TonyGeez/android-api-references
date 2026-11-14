# MediaPlayer.OnTimedMetaDataAvailableListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnTimedMetaDataAvailableListener

Kotlin| [Java](../android/media/MediaPlayer.OnTimedMetaDataAvailableListener.md) 
| --- | --- |

```
interface OnTimedMetaDataAvailableListener
```

| [android.media.MediaPlayer.OnTimedMetaDataAvailableListener](../android/media/MediaPlayer.OnTimedMetaDataAvailableListener.md) |

Interface definition of a callback to be invoked when a track has timed metadata available.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTimedMetaDataAvailable](../android/media/MediaPlayer.OnTimedMetaDataAvailableListener.md))`(`mp:` ` [MediaPlayer](../android/media/MediaPlayer.md)!`, `data:` ` [TimedMetaData](../android/media/TimedMetaData.md)!`)` Called to indicate avaliable timed metadata |

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
| `mp` | [MediaPlayer](../android/media/MediaPlayer.md)!:the MediaPlayer associated with this callback |
| `data` | [TimedMetaData](../android/media/TimedMetaData.md)!:the timed metadata sample associated with this event |
