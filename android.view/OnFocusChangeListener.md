# View.OnFocusChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnFocusChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/view/View.OnFocusChangeListener "View this page in Java") 

```
interface OnFocusChangeListener
```

| [android.view.View.OnFocusChangeListener](https://developer.android.com/reference/kotlin/android/view/View.OnFocusChangeListener#) |

| Known Direct Subclasses [TabWidget](https://developer.android.com/reference/kotlin/android/widget/TabWidget.html#) |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------| | [TabWidget](https://developer.android.com/reference/kotlin/android/widget/TabWidget.html#) | Displays a list of tab labels representing each page in the parent's tab collection. | |

Interface definition for a callback to be invoked when the focus state of a view changed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFocusChange](https://developer.android.com/reference/kotlin/android/view/View.OnFocusChangeListener#onFocusChange(android.view.View,%20kotlin.Boolean))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `hasFocus:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the focus state of a view has changed. |

## Public methods

### onFocusChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFocusChange(
    v: View!, 
    hasFocus: Boolean
): Unit
```

Called when the focus state of a view has changed.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view whose state has changed. |
| `hasFocus` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The new focus state of v. |
