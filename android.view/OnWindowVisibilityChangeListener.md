# ViewTreeObserver.OnWindowVisibilityChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnWindowVisibilityChangeListener

Kotlin | [Java](../android/view/ViewTreeObserver.OnWindowVisibilityChangeListener.md) 
| --- | --- |

```
interface OnWindowVisibilityChangeListener
```

| [android.view.ViewTreeObserver.OnWindowVisibilityChangeListener](../android/view/ViewTreeObserver.OnWindowVisibilityChangeListener.md) |

Interface definition for a callback to be invoked when the view hierarchy's window visibility changes.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowVisibilityChanged](../android/view/ViewTreeObserver.OnWindowVisibilityChangeListener.md))`(`visibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback method to be invoked when the window visibility changes in the view tree. |

## Public methods

### onWindowVisibilityChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onWindowVisibilityChanged(visibility: Int): Unit
```

Callback method to be invoked when the window visibility changes in the view tree.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new visibility of the window. Value is [android.view.View#VISIBLE](../android/view/View.md), [android.view.View#INVISIBLE](../android/view/View.md), or [android.view.View#GONE](../android/view/View.md) |
