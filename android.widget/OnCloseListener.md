# SearchView.OnCloseListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCloseListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/SearchView.OnCloseListener "View this page in Java") 

```
interface OnCloseListener
```

| [android.widget.SearchView.OnCloseListener](https://developer.android.com/reference/kotlin/android/widget/SearchView.OnCloseListener#) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onClose](https://developer.android.com/reference/kotlin/android/widget/SearchView.OnCloseListener#onClose())`()` The user is attempting to close the SearchView. |

## Public methods

### onClose

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClose(): Boolean
```

The user is attempting to close the SearchView.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the listener wants to override the default behavior of clearing the text field and dismissing it, false otherwise. |
