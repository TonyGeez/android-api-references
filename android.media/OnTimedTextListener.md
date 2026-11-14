# MediaPlayer.OnTimedTextListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnTimedTextListener

Kotlin| [Java](../android/media/MediaPlayer.OnTimedTextListener.md) 
| --- | --- |

```
interface OnTimedTextListener
```

| [android.media.MediaPlayer.OnTimedTextListener](../android/media/MediaPlayer.OnTimedTextListener.md) |

Interface definition of a callback to be invoked when a timed text is available for display.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTimedText](../android/media/MediaPlayer.OnTimedTextListener.md))`(`mp:` ` [MediaPlayer](MediaPlayer.md)!`, `text:` ` [TimedText](TimedText.md)!`)` Called to indicate an avaliable timed text |

## Public methods

### onTimedText

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTimedText(
    mp: MediaPlayer!, 
    text: TimedText!
): Unit
```

Called to indicate an avaliable timed text

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](MediaPlayer.md)!:the MediaPlayer associated with this callback |
| `text` | [TimedText](TimedText.md)!:the timed text sample which contains the text needed to be displayed and the display format. |
