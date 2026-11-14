# AudioEffect.OnEnableStatusChangeListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnEnableStatusChangeListener

Kotlin| [Java](../android/media/audiofx/AudioEffect.OnEnableStatusChangeListener.md) 
| --- | --- |

```
interface OnEnableStatusChangeListener
```

| [android.media.audiofx.AudioEffect.OnEnableStatusChangeListener](../android/media/audiofx/AudioEffect.OnEnableStatusChangeListener.md) |

The OnEnableStatusChangeListener interface defines a method called by the AudioEffect when the enabled state of the effect engine was changed by the controlling application.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEnableStatusChange](../android/media/audiofx/AudioEffect.OnEnableStatusChangeListener.md))`(`effect:` ` [AudioEffect](AudioEffect.md)!`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called on the listener to notify it that the effect engine has been enabled or disabled. |

## Public methods

### onEnableStatusChange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onEnableStatusChange(
    effect: AudioEffect!, 
    enabled: Boolean
): Unit
```

Called on the listener to notify it that the effect engine has been enabled or disabled.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [AudioEffect](AudioEffect.md)!:the effect on which the interface is registered. |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):new effect state. |
