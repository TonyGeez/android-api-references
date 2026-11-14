# ViewTreeObserver.OnDrawListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDrawListener

Kotlin| [Java](https://developer.android.com/reference/android/view/ViewTreeObserver.OnDrawListener "View this page in Java") 
| --- | --- |

```
interface OnDrawListener
```

| [android.view.ViewTreeObserver.OnDrawListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnDrawListener#) |

Interface definition for a callback to be invoked when the view tree is about to be drawn.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDraw](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnDrawListener#onDraw())`()` Callback method to be invoked when the view tree is about to be drawn. |

## Public methods

### onDraw

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDraw(): Unit
```

Callback method to be invoked when the view tree is about to be drawn. At this point, views cannot be modified in any way.

Unlike with [OnPreDrawListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnPreDrawListener), this method cannot be used to cancel the current drawing pass.

An [OnDrawListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnDrawListener#) listener**cannot be added or removed**from this method. 
**See Also**

- [android.view.View#onMeasure](https://developer.android.com/reference/kotlin/android/view/View#onMeasure(kotlin.Int,%20kotlin.Int))
- [android.view.View#onLayout](https://developer.android.com/reference/kotlin/android/view/View#onLayout(kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.View#onDraw](https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas))
