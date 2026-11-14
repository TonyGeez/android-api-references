# SearchResults

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SearchResults

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/SearchResults "View this page in Java") 

```
open class SearchResults : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.appsearch.SearchResults](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults#) |

Encapsulates results of a search operation.

Each [AppSearchSession.search](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec))operation returns a list of [SearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult) objects, referred to as a "page", limited by the size configured by [android.app.appsearch.SearchSpec.Builder#setResultCountPerPage](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec.Builder#setResultCountPerPage(kotlin.Int)).

To fetch a page of results, call [getNextPage](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults#getNextPage(java.util.concurrent.Executor,%20java.util.function.Consumer)).

All instances of [SearchResults](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults#) must call android.app.appsearch.SearchResults#close() after the results are fetched.

This class is not thread safe.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults#close())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getNextPage](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults#getNextPage(java.util.concurrent.Executor,%20java.util.function.Consumer))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [SearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult)!>!>!>`)` Retrieves the next page of [SearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult) objects. |

## Public methods

### close

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### getNextPage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNextPage(
    executor: Executor, 
    callback: Consumer<AppSearchResult<MutableList<SearchResult!>!>!>
): Unit
```

Retrieves the next page of [SearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult) objects.

The page size is configured by [SearchSpec.Builder.setResultCountPerPage](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec.Builder#setResultCountPerPage(kotlin.Int)).

Continue calling this method to access results until it returns an empty list, signifying there are no more results.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult)!\>!\>!\>:Callback to receive the pending result of performing this operation. This value cannot be`null`. |
