# SearchView.OnSuggestionListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSuggestionListener

Kotlin| [Java](../android/widget/SearchView.OnSuggestionListener.md) 
| --- | --- |

```
interface OnSuggestionListener
```

| [android.widget.SearchView.OnSuggestionListener](../android/widget/SearchView.OnSuggestionListener.md) |

Callback interface for selection events on suggestions. These callbacks are only relevant when a SearchableInfo has been specified by [setSearchableInfo](SearchView.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSuggestionClick](../android/widget/SearchView.OnSuggestionListener.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a suggestion was clicked. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSuggestionSelect](../android/widget/SearchView.OnSuggestionListener.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a suggestion was selected by navigating to it. |

## Public methods

### onSuggestionClick

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuggestionClick(position: Int): Boolean
```

Called when a suggestion was clicked.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the absolute position of the clicked item in the list of suggestions. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the listener handles the event and wants to override the default behavior of launching any intent or submitting a search query specified on that item. Return false otherwise. |

### onSuggestionSelect

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuggestionSelect(position: Int): Boolean
```

Called when a suggestion was selected by navigating to it.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the absolute position in the list of suggestions. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the listener handles the event and wants to override the default behavior of possibly rewriting the query based on the selected item, false otherwise. |
