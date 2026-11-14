# AccessibilityManager.AudioDescriptionRequestedChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioDescriptionRequestedChangeListener

Kotlin| [Java](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md) 
| --- | --- |

```
interface AudioDescriptionRequestedChangeListener
```

| [android.view.accessibility.AccessibilityManager.AudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md) |

Listener for the audio description by default state. To listen for changes to the audio description by default state on the device, implement this interface and register it with the system by calling [addAudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAudioDescriptionRequestedChanged](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the audio description enabled state changes. |

## Public methods

### onAudioDescriptionRequestedChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAudioDescriptionRequestedChanged(enabled: Boolean): Unit
```

Called when the audio description enabled state changes.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether audio description by default is enabled. |
