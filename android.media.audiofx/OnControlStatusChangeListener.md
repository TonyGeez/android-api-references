# AudioEffect.OnControlStatusChangeListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnControlStatusChangeListener

Kotlin| [Java](../android/media/audiofx/AudioEffect.OnControlStatusChangeListener.md) 
| --- | --- |

```
interface OnControlStatusChangeListener
```

| [android.media.audiofx.AudioEffect.OnControlStatusChangeListener](../android/media/audiofx/AudioEffect.OnControlStatusChangeListener.md) |

The OnControlStatusChangeListener interface defines a method called by the AudioEffect when control of the effect engine is gained or lost by the application

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onControlStatusChange](../android/media/audiofx/AudioEffect.OnControlStatusChangeListener.md))`(`effect:` ` [AudioEffect](../android/media/audiofx/AudioEffect.md)!`, `controlGranted:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called on the listener to notify it that the effect engine control has been taken or returned. |

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
| `effect` | [AudioEffect](../android/media/audiofx/AudioEffect.md)!:the effect on which the interface is registered. |
| `controlGranted` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the application has been granted control of the effect engine, false otherwise. |
