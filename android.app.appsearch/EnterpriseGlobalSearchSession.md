# EnterpriseGlobalSearchSession

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

# EnterpriseGlobalSearchSession

Kotlin| [Java](EnterpriseGlobalSearchSession.md) 
| --- | --- |

```
open class EnterpriseGlobalSearchSession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.EnterpriseGlobalSearchSession](EnterpriseGlobalSearchSession.md) |

Provides a connection to all enterprise (work profile) AppSearch databases the querying application has been granted access to.

This session can be created from any user profile but will only properly return results when created from the main profile. If the user is not the main profile or an associated work profile does not exist, queries will still successfully complete but with empty results.

Schemas must be explicitly tagged enterprise and may require additional permissions to be visible from an enterprise session. Retrieved documents may also have certain fields restricted or modified unlike if they were retrieved directly from [GlobalSearchSession](GlobalSearchSession.md) on the work profile.

This class is thread safe.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getByDocumentId](EnterpriseGlobalSearchSession.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `request:` ` [GetByDocumentIdRequest](GetByDocumentIdRequest.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [BatchResultCallback](BatchResultCallback.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [GenericDocument](GenericDocument.md)!>`)` Retrieves [GenericDocument](GenericDocument.md) documents, belonging to the specified package name and database name and identified by the namespace and ids in the request, from the [GlobalSearchSession](GlobalSearchSession.md) database. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getSchema](EnterpriseGlobalSearchSession.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [Consumer](../java.util.function/Consumer.md)< [AppSearchResult](AppSearchResult.md)< [GetSchemaResponse](GetSchemaResponse.md)!>!>`)` Retrieves the collection of schemas most recently successfully provided to [android.app.appsearch.AppSearchSession#setSchema](AppSearchSession.md))for any types belonging to the requested package and database that the caller has been granted access to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openBlobForRead](EnterpriseGlobalSearchSession.md))`(`handles:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [AppSearchBlobHandle](AppSearchBlobHandle.md)!>`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [Consumer](../java.util.function/Consumer.md)< [AppSearchResult](AppSearchResult.md)< [OpenBlobForReadResponse](OpenBlobForReadResponse.md)!>!>`)` Opens a batch of AppSearch Blobs for reading. |
| --- | --- |
| open [SearchResults](SearchResults.md) | [search](EnterpriseGlobalSearchSession.md))`(`queryExpression:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `searchSpec:` ` [SearchSpec](SearchSpec.md)`)` Retrieves documents from all AppSearch databases that the querying application has access to. |

## Public methods

### getByDocumentId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions) 

```
open fun getByDocumentId(
    packageName: String, 
    databaseName: String, 
    request: GetByDocumentIdRequest, 
    executor: Executor, 
    callback: BatchResultCallback<String!, GenericDocument!>
): Unit
```

Retrieves [GenericDocument](GenericDocument.md) documents, belonging to the specified package name and database name and identified by the namespace and ids in the request, from the [GlobalSearchSession](GlobalSearchSession.md) database.

If the package or database doesn't exist or if the calling package doesn't have access, the gets will be handled as failures in an [AppSearchBatchResult](AppSearchBatchResult.md) object in the callback.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the package to get from This value cannot be`null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the database to get from This value cannot be`null`. |
| `request` | [GetByDocumentIdRequest](GetByDocumentIdRequest.md):a request containing a namespace and IDs to get documents for. This value cannot be`null`. |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [BatchResultCallback](BatchResultCallback.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [GenericDocument](GenericDocument.md)!\>:Callback to receive the pending result of performing this operation. The keys of the returned [AppSearchBatchResult](AppSearchBatchResult.md) are the input IDs. The values are the returned [GenericDocument](GenericDocument.md) s on success, or a failed [AppSearchResult](AppSearchResult.md) otherwise. IDs that are not found will return a failed [AppSearchResult](AppSearchResult.md) with a result code of [AppSearchResult.RESULT_NOT_FOUND](AppSearchResult.md). If an unexpected internal error occurs in the AppSearch service, [BatchResultCallback.onSystemError](BatchResultCallback.md))will be invoked with a [Throwable](../java.lang/Throwable.md). This value cannot be`null`. |

### getSchema

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions) 

```
open fun getSchema(
    packageName: String, 
    databaseName: String, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<GetSchemaResponse!>!>
): Unit
```

Retrieves the collection of schemas most recently successfully provided to [android.app.appsearch.AppSearchSession#setSchema](AppSearchSession.md))for any types belonging to the requested package and database that the caller has been granted access to.

If the requested package/database combination does not exist or the caller has not been granted access to it, then an empty GetSchemaResponse will be returned.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the package that owns the requested [AppSearchSchema](AppSearchSchema.md) instances. This value cannot be`null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the database that owns the requested [AppSearchSchema](AppSearchSchema.md) instances. This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [GetSchemaResponse](GetSchemaResponse.md)!\>!\>:The pending [GetSchemaResponse](GetSchemaResponse.md) containing the schemas that the caller has access to or an empty GetSchemaResponse if the request package and database does not exist, has not set a schema or contains no schemas that are accessible to the caller. This value cannot be`null`. |

### openBlobForRead

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions) 

```
open fun openBlobForRead(
    handles: MutableSet<AppSearchBlobHandle!>, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<OpenBlobForReadResponse!>!>
): Unit
```

Opens a batch of AppSearch Blobs for reading.

See [AppSearchSession.openBlobForRead](AppSearchSession.md))for a general description when a blob is for read.

The returned [OpenBlobForReadResponse](OpenBlobForReadResponse.md) must be closed after use to avoid resource leaks. Failing to close it will result in system file descriptor exhaustion.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handles` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchBlobHandle](AppSearchBlobHandle.md)!\>:The [AppSearchBlobHandle](AppSearchBlobHandle.md) s that identifies the blobs. This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [OpenBlobForReadResponse](OpenBlobForReadResponse.md)!\>!\>:Callback to receive the [OpenBlobForReadResponse](OpenBlobForReadResponse.md). This value cannot be`null`. |
| --- | --- |

**See Also**

- [android.app.appsearch.GenericDocument.Builder#setPropertyBlobHandle](../android/app/appsearch/GenericDocument.Builder.md)) 

### search

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions) 

```
open fun search(
    queryExpression: String, 
    searchSpec: SearchSpec
): SearchResults
```

Retrieves documents from all AppSearch databases that the querying application has access to.

Applications can be granted access to documents by specifying [android.app.appsearch.SetSchemaRequest.Builder#setSchemaTypeVisibilityForPackage](../android/app/appsearch/SetSchemaRequest.Builder.md))when building a schema.

Document access can also be granted to system UIs by specifying [android.app.appsearch.SetSchemaRequest.Builder#setSchemaTypeDisplayedBySystem](../android/app/appsearch/SetSchemaRequest.Builder.md))when building a schema.

See [AppSearchSession.search](AppSearchSession.md))for a detailed explanation on forming a query string.

This method is lightweight. The heavy work will be done in [android.app.appsearch.SearchResults#getNextPage](SearchResults.md)).

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `queryExpression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):query string to search. This value cannot be`null`. |
| `searchSpec` | [SearchSpec](SearchSpec.md):spec for setting document filters, adding projection, setting term match type, etc. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SearchResults](SearchResults.md) | a [SearchResults](SearchResults.md) object for retrieved matched documents. This value cannot be`null`. |
