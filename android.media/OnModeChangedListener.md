# AudioManager.OnModeChangedListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnModeChangedListener

Kotlin| [Java](../android/media/AudioManager.OnModeChangedListener.md) 
| --- | --- |

```
interface OnModeChangedListener
```

| [android.media.AudioManager.OnModeChangedListener](../android/media/AudioManager.OnModeChangedListener.md) |

Interface definition of a callback that is notified when the audio mode changes

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onModeChanged](../android/media/AudioManager.OnModeChangedListener.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called on the listener to indicate that the audio mode has changed |

## Public methods

### onModeChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onModeChanged(mode: Int): Unit
```

Called on the listener to indicate that the audio mode has changed

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current audio mode Value is [android.media.AudioManager#MODE_NORMAL](AudioManager.md), [android.media.AudioManager#MODE_RINGTONE](AudioManager.md), [android.media.AudioManager#MODE_IN_CALL](AudioManager.md), [android.media.AudioManager#MODE_IN_COMMUNICATION](AudioManager.md), [android.media.AudioManager#MODE_CALL_SCREENING](AudioManager.md), [android.media.AudioManager#MODE_CALL_REDIRECT](AudioManager.md), [android.media.AudioManager#MODE_COMMUNICATION_REDIRECT](AudioManager.md), or [android.media.AudioManager#MODE_ASSISTANT_CONVERSATION](AudioManager.md) |
