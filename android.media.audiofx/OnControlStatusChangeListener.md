# AudioEffect.OnControlStatusChangeListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnControlStatusChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/media/audiofx/AudioEffect.OnControlStatusChangeListener "View this page in Java") 
| --- | --- |

```
interface OnControlStatusChangeListener
```

| [android.media.audiofx.AudioEffect.OnControlStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnControlStatusChangeListener#) |

The OnControlStatusChangeListener interface defines a method called by the AudioEffect when control of the effect engine is gained or lost by the application

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onControlStatusChange](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnControlStatusChangeListener#onControlStatusChange(android.media.audiofx.AudioEffect,%20kotlin.Boolean))`(`effect:` ` [AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect)!`, `controlGranted:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called on the listener to notify it that the effect engine control has been taken or returned. |

## Public methods

### onControlStatusChange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onControlStatusChange(
    effect: AudioEffect!, 
    controlGranted: Boolean
): Unit
```

Called on the listener to notify it that the effect engine control has been taken or returned.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect)!:the effect on which the interface is registered. |
| `controlGranted` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the application has been granted control of the effect engine, false otherwise. |
