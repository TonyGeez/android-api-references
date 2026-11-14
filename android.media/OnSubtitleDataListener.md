# MediaPlayer.OnSubtitleDataListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSubtitleDataListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaPlayer.OnSubtitleDataListener "View this page in Java") 

```
interface OnSubtitleDataListener
```

| [android.media.MediaPlayer.OnSubtitleDataListener](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnSubtitleDataListener#) |

Interface definition of a callback to be invoked when a player subtitle track has new subtitle data available. See the [MediaPlayer.setOnSubtitleDataListener(OnSubtitleDataListener, Handler)](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#setOnSubtitleDataListener(android.media.MediaPlayer.OnSubtitleDataListener,%20android.os.Handler))method for the description of which track will report data through this listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSubtitleData](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnSubtitleDataListener#onSubtitleData(android.media.MediaPlayer,%20android.media.SubtitleData))`(`mp:` ` [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)`, `data:` ` [SubtitleData](https://developer.android.com/reference/kotlin/android/media/SubtitleData)`)` Method called when new subtitle data is available |

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
| `mp` | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer):the player that reports the new subtitle data This value cannot be`null`. |
| `data` | [SubtitleData](https://developer.android.com/reference/kotlin/android/media/SubtitleData):the subtitle data This value cannot be`null`. |
