# View.OnFocusChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnFocusChangeListener

Kotlin| [Java](../android/view/View.OnFocusChangeListener.md) 
| --- | --- |

```
interface OnFocusChangeListener
```

| [android.view.View.OnFocusChangeListener](../android/view/View.OnFocusChangeListener.md) |

| Known Direct Subclasses [TabWidget](../android/widget/TabWidget.md) |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------| | [TabWidget](../android/widget/TabWidget.md) | Displays a list of tab labels representing each page in the parent's tab collection. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when the focus state of a view changed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFocusChange](../android/view/View.OnFocusChangeListener.md))`(`v:` ` [View](../android/view/View.md)!`, `hasFocus:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the focus state of a view has changed. |

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
| `v` | [View](../android/view/View.md)!:The view whose state has changed. |
| `hasFocus` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The new focus state of v. |
