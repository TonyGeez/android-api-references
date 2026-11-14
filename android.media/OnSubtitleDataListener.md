# MediaPlayer.OnSubtitleDataListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSubtitleDataListener

Kotlin| [Java](../android/media/MediaPlayer.OnSubtitleDataListener.md) 
| --- | --- |

```
interface OnSubtitleDataListener
```

| [android.media.MediaPlayer.OnSubtitleDataListener](../android/media/MediaPlayer.OnSubtitleDataListener.md) |

Interface definition of a callback to be invoked when a player subtitle track has new subtitle data available. See the [MediaPlayer.setOnSubtitleDataListener(OnSubtitleDataListener, Handler)](MediaPlayer.md))method for the description of which track will report data through this listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSubtitleData](../android/media/MediaPlayer.OnSubtitleDataListener.md))`(`mp:` ` [MediaPlayer](MediaPlayer.md)`, `data:` ` [SubtitleData](SubtitleData.md)`)` Method called when new subtitle data is available |

## Public methods

### onSubtitleData

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSubtitleData(
    mp: MediaPlayer, 
    data: SubtitleData
): Unit
```

Method called when new subtitle data is available

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](MediaPlayer.md):the player that reports the new subtitle data This value cannot be`null`. |
| `data` | [SubtitleData](SubtitleData.md):the subtitle data This value cannot be`null`. |
