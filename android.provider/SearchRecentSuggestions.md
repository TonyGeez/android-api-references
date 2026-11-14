# SearchRecentSuggestions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SearchRecentSuggestions

Kotlin| [Java](../android/provider/SearchRecentSuggestions.md) 
| --- | --- |

```
open class SearchRecentSuggestions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.SearchRecentSuggestions](../android/provider/SearchRecentSuggestions.md) |

This is a utility class providing access to [android.content.SearchRecentSuggestionsProvider](../android/content/SearchRecentSuggestionsProvider.md).

Unlike some utility classes, this one must be instantiated and properly initialized, so that it can be configured to operate with the search suggestions provider that you have created.

Typically, you will do this in your searchable activity, each time you receive an incoming [ACTION_SEARCH](../android/content/Intent.md) Intent. The code to record each incoming query is as follows: 

```kotlin
SearchSuggestions suggestions = new SearchSuggestions(this,
               MySuggestionsProvider.AUTHORITY, MySuggestionsProvider.MODE);
       suggestions.saveRecentQuery(queryString, null);
  
```

For a working example, see SearchSuggestionSampleProvider and SearchQueryResults in samples/ApiDemos/app.
|
| ### Developer Guides
|
| For information about using search suggestions in your application, read the [Adding Recent Query Suggestions](https://developer.android.com/guide/topics/search/adding-recent-query-suggestions.html) developer guide.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUERIES_PROJECTION_DATE_INDEX](../android/provider/SearchRecentSuggestions.md) Index into the provided query projections. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUERIES_PROJECTION_DISPLAY1_INDEX](../android/provider/SearchRecentSuggestions.md) Index into the provided query projections. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUERIES_PROJECTION_DISPLAY2_INDEX](../android/provider/SearchRecentSuggestions.md) Index into the provided query projections. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUERIES_PROJECTION_QUERY_INDEX](../android/provider/SearchRecentSuggestions.md) Index into the provided query projections. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SearchRecentSuggestions](../android/provider/SearchRecentSuggestions.md))`(`context:` ` [Context](../android/content/Context.md)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Although provider utility classes are typically static, this one must be constructed because it needs to be initialized using the same values that you provided in your [android.content.SearchRecentSuggestionsProvider](../android/content/SearchRecentSuggestionsProvider.md). |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearHistory](../android/provider/SearchRecentSuggestions.md))`()` Completely delete the history. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [saveRecentQuery](../android/provider/SearchRecentSuggestions.md))`(`queryString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `line2:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Add a query to the recent queries list. |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [truncateHistory](../android/provider/SearchRecentSuggestions.md))`(`cr:` ` [ContentResolver](../android/content/ContentResolver.md)!`, `maxEntries:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reduces the length of the history table, to prevent it from growing too large. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [QUERIES_PROJECTION_1LINE](../android/provider/SearchRecentSuggestions.md) This is the database projection that can be used to view saved queries, when configured for one-line operation. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [QUERIES_PROJECTION_2LINE](../android/provider/SearchRecentSuggestions.md) This is the database projection that can be used to view saved queries, when configured for two-line operation. |

## Constants

### QUERIES_PROJECTION_DATE_INDEX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERIES_PROJECTION_DATE_INDEX: Int
```

Index into the provided query projections. For use with Cursor.update methods. 

 Value: 1

### QUERIES_PROJECTION_DISPLAY1_INDEX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERIES_PROJECTION_DISPLAY1_INDEX: Int
```

Index into the provided query projections. For use with Cursor.update methods. 

 Value: 3

### QUERIES_PROJECTION_DISPLAY2_INDEX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERIES_PROJECTION_DISPLAY2_INDEX: Int
```

Index into the provided query projections. For use with Cursor.update methods. 

 Value: 4

### QUERIES_PROJECTION_QUERY_INDEX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERIES_PROJECTION_QUERY_INDEX: Int
```

Index into the provided query projections. For use with Cursor.update methods. 

 Value: 2

## Public constructors

### SearchRecentSuggestions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SearchRecentSuggestions(
    context: Context!, 
    authority: String!, 
    mode: Int)
```

Although provider utility classes are typically static, this one must be constructed because it needs to be initialized using the same values that you provided in your [android.content.SearchRecentSuggestionsProvider](../android/content/SearchRecentSuggestionsProvider.md).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:This must match the authority that you've declared in your manifest. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):You can use mode flags here to determine certain functional aspects of your database. Note, this value should not change from run to run, because when it does change, your suggestions database may be wiped. |

**See Also**

- [android.content.SearchRecentSuggestionsProvider](../android/content/SearchRecentSuggestionsProvider.md)
- [android.content.SearchRecentSuggestionsProvider#setupSuggestions](../android/content/SearchRecentSuggestionsProvider.md))

## Public methods

### clearHistory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearHistory(): Unit
```

Completely delete the history. Use this call to implement a "clear history" UI. Any application that implements search suggestions based on previous actions (such as recent queries, page/items viewed, etc.) should provide a way for the user to clear the history. This gives the user a measure of privacy, if they do not wish for their recent searches to be replayed by other users of the device (via suggestions). 

### saveRecentQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveRecentQuery(
    queryString: String!, 
    line2: String!
): Unit
```

Add a query to the recent queries list. Returns immediately, performing the save in the background.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `queryString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The string as typed by the user. This string will be displayed as the suggestion, and if the user clicks on the suggestion, this string will be sent to your searchable activity (as a new search query). |
| `line2` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:If you have configured your recent suggestions provider with [android.content.SearchRecentSuggestionsProvider#DATABASE_MODE_2LINES](../android/content/SearchRecentSuggestionsProvider.md), you can pass a second line of text here. It will be shown in a smaller font, below the primary suggestion. When typing, matches in either line of text will be displayed in the list. If you did not configure two-line mode, or if a given suggestion does not have any additional text to display, you can pass null here. |

## Protected methods

### truncateHistory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun truncateHistory(
    cr: ContentResolver!, 
    maxEntries: Int
): Unit
```

Reduces the length of the history table, to prevent it from growing too large.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `cr` | [ContentResolver](../android/content/ContentResolver.md)!:Convenience copy of the content resolver. |
| `maxEntries` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Max entries to leave in the table. 0 means remove all entries. |

## Properties

### QUERIES_PROJECTION_1LINE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERIES_PROJECTION_1LINE: Array<String!>!
```

This is the database projection that can be used to view saved queries, when configured for one-line operation. 

### QUERIES_PROJECTION_2LINE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERIES_PROJECTION_2LINE: Array<String!>!
```

This is the database projection that can be used to view saved queries, when configured for two-line operation.
