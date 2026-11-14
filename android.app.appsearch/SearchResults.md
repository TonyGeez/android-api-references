# SearchResults

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SearchResults

Kotlin| [Java](../android/app/appsearch/SearchResults.md) 
| --- | --- |

```
open class SearchResults : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.SearchResults](../android/app/appsearch/SearchResults.md) |

Encapsulates results of a search operation.

Each [AppSearchSession.search](../android/app/appsearch/AppSearchSession.md))operation returns a list of [SearchResult](../android/app/appsearch/SearchResult.md) objects, referred to as a "page", limited by the size configured by [android.app.appsearch.SearchSpec.Builder#setResultCountPerPage](../android/app/appsearch/SearchSpec.Builder.md)).

To fetch a page of results, call [getNextPage](../android/app/appsearch/SearchResults.md)).

All instances of [SearchResults](../android/app/appsearch/SearchResults.md) must call android.app.appsearch.SearchResults#close() after the results are fetched.

This class is not thread safe.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/app/appsearch/SearchResults.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getNextPage](../android/app/appsearch/SearchResults.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [Consumer](../java/util/function/Consumer.md)< [AppSearchResult](../android/app/appsearch/AppSearchResult.md)< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [SearchResult](../android/app/appsearch/SearchResult.md)!>!>!>`)` Retrieves the next page of [SearchResult](../android/app/appsearch/SearchResult.md) objects. |

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

Retrieves the next page of [SearchResult](../android/app/appsearch/SearchResult.md) objects.

The page size is configured by [SearchSpec.Builder.setResultCountPerPage](../android/app/appsearch/SearchSpec.Builder.md)).

Continue calling this method to access results until it returns an empty list, signifying there are no more results.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java/util/function/Consumer.md)\< [AppSearchResult](../android/app/appsearch/AppSearchResult.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SearchResult](../android/app/appsearch/SearchResult.md)!\>!\>!\>:Callback to receive the pending result of performing this operation. This value cannot be`null`. |
