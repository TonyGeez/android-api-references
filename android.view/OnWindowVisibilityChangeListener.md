# ViewTreeObserver.OnWindowVisibilityChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnWindowVisibilityChangeListener

Kotlin | [Java](https://developer.android.com/reference/android/view/ViewTreeObserver.OnWindowVisibilityChangeListener "View this page in Java") 
| --- | --- |

```
interface OnWindowVisibilityChangeListener
```

| [android.view.ViewTreeObserver.OnWindowVisibilityChangeListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnWindowVisibilityChangeListener#) |

Interface definition for a callback to be invoked when the view hierarchy's window visibility changes.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowVisibilityChanged](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnWindowVisibilityChangeListener#onWindowVisibilityChanged(kotlin.Int))`(`visibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback method to be invoked when the window visibility changes in the view tree. |

## Public methods

### onWindowVisibilityChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onWindowVisibilityChanged(visibility: Int): Unit
```

Callback method to be invoked when the window visibility changes in the view tree.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new visibility of the window. Value is [android.view.View#VISIBLE](https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int), [android.view.View#INVISIBLE](https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int), or [android.view.View#GONE](https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int) |
