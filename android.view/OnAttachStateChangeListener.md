# View.OnAttachStateChangeListener

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnAttachStateChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/view/View.OnAttachStateChangeListener "View this page in Java") 

```
interface OnAttachStateChangeListener
```

| [android.view.View.OnAttachStateChangeListener](https://developer.android.com/reference/kotlin/android/view/View.OnAttachStateChangeListener#) |

Interface definition for a callback to be invoked when this view is attached or detached from its window.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onViewAttachedToWindow](https://developer.android.com/reference/kotlin/android/view/View.OnAttachStateChangeListener#onViewAttachedToWindow(android.view.View))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`)` Called when the view is attached to a window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onViewDetachedFromWindow](https://developer.android.com/reference/kotlin/android/view/View.OnAttachStateChangeListener#onViewDetachedFromWindow(android.view.View))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`)` Called when the view is detached from a window. |

## Public methods

### onViewAttachedToWindow

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onViewAttachedToWindow(v: View): Unit
```

Called when the view is attached to a window.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View):The view that was attached This value cannot be`null`. |

### onViewDetachedFromWindow

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onViewDetachedFromWindow(v: View): Unit
```

Called when the view is detached from a window.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View):The view that was detached This value cannot be`null`. |
