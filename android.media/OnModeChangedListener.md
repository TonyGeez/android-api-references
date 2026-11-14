# AudioManager.OnModeChangedListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnModeChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioManager.OnModeChangedListener "View this page in Java") 

```
interface OnModeChangedListener
```

| [android.media.AudioManager.OnModeChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioManager.OnModeChangedListener#) |

Interface definition of a callback that is notified when the audio mode changes

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onModeChanged](https://developer.android.com/reference/kotlin/android/media/AudioManager.OnModeChangedListener#onModeChanged(kotlin.Int))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called on the listener to indicate that the audio mode has changed |

## Public methods

### onModeChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onModeChanged(mode: Int): Unit
```

Called on the listener to indicate that the audio mode has changed

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current audio mode Value is [android.media.AudioManager#MODE_NORMAL](https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_NORMAL:kotlin.Int), [android.media.AudioManager#MODE_RINGTONE](https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_RINGTONE:kotlin.Int), [android.media.AudioManager#MODE_IN_CALL](https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_IN_CALL:kotlin.Int), [android.media.AudioManager#MODE_IN_COMMUNICATION](https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_IN_COMMUNICATION:kotlin.Int), [android.media.AudioManager#MODE_CALL_SCREENING](https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_CALL_SCREENING:kotlin.Int), [android.media.AudioManager#MODE_CALL_REDIRECT](https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_CALL_REDIRECT:kotlin.Int), [android.media.AudioManager#MODE_COMMUNICATION_REDIRECT](https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_COMMUNICATION_REDIRECT:kotlin.Int), or [android.media.AudioManager#MODE_ASSISTANT_CONVERSATION](https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_ASSISTANT_CONVERSATION:kotlin.Int) |
