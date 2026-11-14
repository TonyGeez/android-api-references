# ViewTreeObserver.OnDrawListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDrawListener

Kotlin| [Java](../android/view/ViewTreeObserver.OnDrawListener.md) 
| --- | --- |

```
interface OnDrawListener
```

| [android.view.ViewTreeObserver.OnDrawListener](../android/view/ViewTreeObserver.OnDrawListener.md) |

Interface definition for a callback to be invoked when the view tree is about to be drawn.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDraw](../android/view/ViewTreeObserver.OnDrawListener.md))`()` Callback method to be invoked when the view tree is about to be drawn. |

## Public methods

### onDraw

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDraw(): Unit
```

Callback method to be invoked when the view tree is about to be drawn. At this point, views cannot be modified in any way.

Unlike with [OnPreDrawListener](../android/view/ViewTreeObserver.OnPreDrawListener.md), this method cannot be used to cancel the current drawing pass.

An [OnDrawListener](../android/view/ViewTreeObserver.OnDrawListener.md) listener**cannot be added or removed**from this method. 
**See Also**

- [android.view.View#onMeasure](View.md))
- [android.view.View#onLayout](View.md))
- [android.view.View#onDraw](View.md))
