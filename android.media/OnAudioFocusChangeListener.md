# AudioManager.OnAudioFocusChangeListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnAudioFocusChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioManager.OnAudioFocusChangeListener "View this page in Java") 

```
interface OnAudioFocusChangeListener
```

| [android.media.AudioManager.OnAudioFocusChangeListener](https://developer.android.com/reference/kotlin/android/media/AudioManager.OnAudioFocusChangeListener#) |

Interface definition for a callback to be invoked when the audio focus of the system is updated.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAudioFocusChange](https://developer.android.com/reference/kotlin/android/media/AudioManager.OnAudioFocusChangeListener#onAudioFocusChange(kotlin.Int))`(`focusChange:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called on the listener to notify it the audio focus for this listener has been changed. |

## Public methods

### onAudioFocusChange

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAudioFocusChange(focusChange: Int): Unit
```

Called on the listener to notify it the audio focus for this listener has been changed. The focusChange value indicates whether the focus was gained, whether the focus was lost, and whether that loss is transient, or whether the new focus holder will hold it for an unknown amount of time. When losing focus, listeners can use the focus change information to decide what behavior to adopt when losing focus. A music player could for instance elect to lower the volume of its music stream (duck) for transient focus losses, and pause otherwise.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `focusChange` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type of focus change, one of [AudioManager.AUDIOFOCUS_GAIN](https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_GAIN:kotlin.Int), [AudioManager.AUDIOFOCUS_LOSS](https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_LOSS:kotlin.Int), [AudioManager.AUDIOFOCUS_LOSS_TRANSIENT](https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_LOSS_TRANSIENT:kotlin.Int) and [AudioManager.AUDIOFOCUS_LOSS_TRANSIENT_CAN_DUCK](https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_LOSS_TRANSIENT_CAN_DUCK:kotlin.Int). |
