# View.OnAttachStateChangeListener

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnAttachStateChangeListener

Kotlin| [Java](../android/view/View.OnAttachStateChangeListener.md) 
| --- | --- |

```
interface OnAttachStateChangeListener
```

| [android.view.View.OnAttachStateChangeListener](../android/view/View.OnAttachStateChangeListener.md) |

Interface definition for a callback to be invoked when this view is attached or detached from its window.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onViewAttachedToWindow](../android/view/View.OnAttachStateChangeListener.md))`(`v:` ` [View](View.md)`)` Called when the view is attached to a window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onViewDetachedFromWindow](../android/view/View.OnAttachStateChangeListener.md))`(`v:` ` [View](View.md)`)` Called when the view is detached from a window. |

## Public methods

### onViewAttachedToWindow

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onViewAttachedToWindow(v: View): Unit
```

Called when the view is attached to a window.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](View.md):The view that was attached This value cannot be`null`. |

### onViewDetachedFromWindow

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onViewDetachedFromWindow(v: View): Unit
```

Called when the view is detached from a window.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](View.md):The view that was detached This value cannot be`null`. |
