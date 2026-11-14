# ChooserSession.StateListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StateListener

Kotlin| [Java](../android/service/chooser/ChooserSession.StateListener.md) 
| --- | --- |

```
interface StateListener
```

| [android.service.chooser.ChooserSession.StateListener](../android/service/chooser/ChooserSession.StateListener.md) |

A callback interface for Chooser session state updates.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChanged](../android/service/chooser/ChooserSession.StateListener.md))`(`bounds:` ` [Rect](../android/graphics/Rect.md)`)` Gets invoked when the Chooser bounds are changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStateChanged](../android/service/chooser/ChooserSession.StateListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets invoked when ChooserManager lifecycle state has changed. |

## Public methods

### onBoundsChanged

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBoundsChanged(bounds: Rect): Unit
```

Gets invoked when the Chooser bounds are changed. The rect parameter represents Chooser window bounds in pixels.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](../android/graphics/Rect.md):This value cannot be`null`. |

### onStateChanged

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStateChanged(state: Int): Unit
```

Gets invoked when ChooserManager lifecycle state has changed.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.service.chooser.ChooserSession#STATE_INITIALIZED](../android/service/chooser/ChooserSession.md), [android.service.chooser.ChooserSession#STATE_STARTED](../android/service/chooser/ChooserSession.md), or [android.service.chooser.ChooserSession#STATE_CLOSED](../android/service/chooser/ChooserSession.md) |
