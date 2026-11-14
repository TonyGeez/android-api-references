# SearchView.OnCloseListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCloseListener

Kotlin| [Java](../android/widget/SearchView.OnCloseListener.md) 
| --- | --- |

```
interface OnCloseListener
```

| [android.widget.SearchView.OnCloseListener](../android/widget/SearchView.OnCloseListener.md) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onClose](../android/widget/SearchView.OnCloseListener.md))`()` The user is attempting to close the SearchView. |

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
