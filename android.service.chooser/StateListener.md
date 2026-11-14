# ChooserSession.StateListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StateListener

Kotlin| [Java](https://developer.android.com/reference/android/service/chooser/ChooserSession.StateListener "View this page in Java") 

```
interface StateListener
```

| [android.service.chooser.ChooserSession.StateListener](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession.StateListener#) |

A callback interface for Chooser session state updates.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChanged](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession.StateListener#onBoundsChanged(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` Gets invoked when the Chooser bounds are changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStateChanged](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession.StateListener#onStateChanged(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets invoked when ChooserManager lifecycle state has changed. |

## Public methods

### onBoundsChanged

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBoundsChanged(bounds: Rect): Unit
```

Gets invoked when the Chooser bounds are changed. The rect parameter represents Chooser window bounds in pixels.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#):This value cannot be`null`. |

### onStateChanged

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStateChanged(state: Int): Unit
```

Gets invoked when ChooserManager lifecycle state has changed.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.service.chooser.ChooserSession#STATE_INITIALIZED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_INITIALIZED:kotlin.Int), [android.service.chooser.ChooserSession#STATE_STARTED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_STARTED:kotlin.Int), or [android.service.chooser.ChooserSession#STATE_CLOSED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_CLOSED:kotlin.Int) |
