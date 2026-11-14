# MediaPlayer.OnVideoSizeChangedListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnVideoSizeChangedListener

Kotlin| [Java](../android/media/MediaPlayer.OnVideoSizeChangedListener.md) 
| --- | --- |

```
interface OnVideoSizeChangedListener
```

| [android.media.MediaPlayer.OnVideoSizeChangedListener](../android/media/MediaPlayer.OnVideoSizeChangedListener.md) |

Interface definition of a callback to be invoked when the video size is first known or updated

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onVideoSizeChanged](../android/media/MediaPlayer.OnVideoSizeChangedListener.md))`(`mp:` ` [MediaPlayer](../android/media/MediaPlayer.md)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to indicate the video size The video size (width and height) could be 0 if there was no video, no display surface was set, or the value was not determined yet. |

## Public methods

### onVideoSizeChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onVideoSizeChanged(
    mp: MediaPlayer!, 
    width: Int, 
    height: Int
): Unit
```

Called to indicate the video size The video size (width and height) could be 0 if there was no video, no display surface was set, or the value was not determined yet.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](../android/media/MediaPlayer.md)!:the MediaPlayer associated with this callback |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the width of the video |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the height of the video |
| --- | --- |
