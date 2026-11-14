# MediaPlayer.OnTimedTextListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnTimedTextListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaPlayer.OnTimedTextListener "View this page in Java") 

```
interface OnTimedTextListener
```

| [android.media.MediaPlayer.OnTimedTextListener](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnTimedTextListener#) |

Interface definition of a callback to be invoked when a timed text is available for display.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTimedText](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnTimedTextListener#onTimedText(android.media.MediaPlayer,%20android.media.TimedText))`(`mp:` ` [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!`, `text:` ` [TimedText](https://developer.android.com/reference/kotlin/android/media/TimedText)!`)` Called to indicate an avaliable timed text |

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
| `mp` | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!:the MediaPlayer associated with this callback |
| `text` | [TimedText](https://developer.android.com/reference/kotlin/android/media/TimedText)!:the timed text sample which contains the text needed to be displayed and the display format. |
