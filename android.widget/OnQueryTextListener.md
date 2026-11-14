# SearchView.OnQueryTextListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnQueryTextListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/SearchView.OnQueryTextListener "View this page in Java") 
| --- | --- |

```
interface OnQueryTextListener
```

| [android.widget.SearchView.OnQueryTextListener](https://developer.android.com/reference/kotlin/android/widget/SearchView.OnQueryTextListener#) |

Callbacks for changes to the query text.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onQueryTextChange](https://developer.android.com/reference/kotlin/android/widget/SearchView.OnQueryTextListener#onQueryTextChange(kotlin.String))`(`newText:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called when the query text is changed by the user. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onQueryTextSubmit](https://developer.android.com/reference/kotlin/android/widget/SearchView.OnQueryTextListener#onQueryTextSubmit(kotlin.String))`(`query:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called when the user submits the query. |

## Public methods

### onQueryTextChange

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onQueryTextChange(newText: String!): Boolean
```

Called when the query text is changed by the user.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `newText` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new content of the query text field. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | false if the SearchView should perform the default action of showing any suggestions if available, true if the action was handled by the listener. |

### onQueryTextSubmit

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onQueryTextSubmit(query: String!): Boolean
```

Called when the user submits the query. This could be due to a key press on the keyboard or due to pressing a submit button. The listener can override the standard behavior by returning true to indicate that it has handled the submit request. Otherwise return false to let the SearchView handle the submission by launching any associated intent.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------|
| `query` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the query text that is to be submitted |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the query has been handled by the listener, false to let the SearchView perform the default action. |
