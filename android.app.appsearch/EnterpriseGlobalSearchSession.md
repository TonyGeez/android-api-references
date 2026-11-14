# EnterpriseGlobalSearchSession

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

# EnterpriseGlobalSearchSession

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/EnterpriseGlobalSearchSession "View this page in Java") 
| --- | --- |

```
open class EnterpriseGlobalSearchSession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.EnterpriseGlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/EnterpriseGlobalSearchSession#) |

Provides a connection to all enterprise (work profile) AppSearch databases the querying application has been granted access to.

This session can be created from any user profile but will only properly return results when created from the main profile. If the user is not the main profile or an associated work profile does not exist, queries will still successfully complete but with empty results.

Schemas must be explicitly tagged enterprise and may require additional permissions to be visible from an enterprise session. Retrieved documents may also have certain fields restricted or modified unlike if they were retrieved directly from [GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession) on the work profile.

This class is thread safe.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getByDocumentId](https://developer.android.com/reference/kotlin/android/app/appsearch/EnterpriseGlobalSearchSession#getByDocumentId(kotlin.String,%20kotlin.String,%20android.app.appsearch.GetByDocumentIdRequest,%20java.util.concurrent.Executor,%20android.app.appsearch.BatchResultCallback))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `request:` ` [GetByDocumentIdRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/GetByDocumentIdRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [BatchResultCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument)!>`)` Retrieves [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) documents, belonging to the specified package name and database name and identified by the namespace and ids in the request, from the [GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession) database. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/EnterpriseGlobalSearchSession#getSchema(kotlin.String,%20kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)< [GetSchemaResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse)!>!>`)` Retrieves the collection of schemas most recently successfully provided to [android.app.appsearch.AppSearchSession#setSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer))for any types belonging to the requested package and database that the caller has been granted access to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openBlobForRead](https://developer.android.com/reference/kotlin/android/app/appsearch/EnterpriseGlobalSearchSession#openBlobForRead(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`handles:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [AppSearchBlobHandle](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle)!>`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)< [OpenBlobForReadResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse)!>!>`)` Opens a batch of AppSearch Blobs for reading. |
| --- | --- |
| open [SearchResults](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults) | [search](https://developer.android.com/reference/kotlin/android/app/appsearch/EnterpriseGlobalSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec))`(`queryExpression:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `searchSpec:` ` [SearchSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec)`)` Retrieves documents from all AppSearch databases that the querying application has access to. |

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

Retrieves [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) documents, belonging to the specified package name and database name and identified by the namespace and ids in the request, from the [GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession) database.

If the package or database doesn't exist or if the calling package doesn't have access, the gets will be handled as failures in an [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult) object in the callback.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the package to get from This value cannot be`null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the database to get from This value cannot be`null`. |
| `request` | [GetByDocumentIdRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/GetByDocumentIdRequest):a request containing a namespace and IDs to get documents for. This value cannot be`null`. |
| --- | --- |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [BatchResultCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument)!\>:Callback to receive the pending result of performing this operation. The keys of the returned [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult) are the input IDs. The values are the returned [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) s on success, or a failed [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) otherwise. IDs that are not found will return a failed [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) with a result code of [AppSearchResult.RESULT_NOT_FOUND](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_NOT_FOUND:kotlin.Int). If an unexpected internal error occurs in the AppSearch service, [BatchResultCallback.onSystemError](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback#onSystemError(kotlin.Throwable))will be invoked with a [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#). This value cannot be`null`. |

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

Retrieves the collection of schemas most recently successfully provided to [android.app.appsearch.AppSearchSession#setSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer))for any types belonging to the requested package and database that the caller has been granted access to.

If the requested package/database combination does not exist or the caller has not been granted access to it, then an empty GetSchemaResponse will be returned.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the package that owns the requested [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) instances. This value cannot be`null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the database that owns the requested [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) instances. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [GetSchemaResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse)!\>!\>:The pending [GetSchemaResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse) containing the schemas that the caller has access to or an empty GetSchemaResponse if the request package and database does not exist, has not set a schema or contains no schemas that are accessible to the caller. This value cannot be`null`. |

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

See [AppSearchSession.openBlobForRead](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#openBlobForRead(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer))for a general description when a blob is for read.

The returned [OpenBlobForReadResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse) must be closed after use to avoid resource leaks. Failing to close it will result in system file descriptor exhaustion.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handles` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchBlobHandle](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle)!\>:The [AppSearchBlobHandle](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle) s that identifies the blobs. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [OpenBlobForReadResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse)!\>!\>:Callback to receive the [OpenBlobForReadResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse). This value cannot be`null`. |
| --- | --- |

**See Also**

- [android.app.appsearch.GenericDocument.Builder#setPropertyBlobHandle](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyBlobHandle(kotlin.String,%20android.app.appsearch.AppSearchBlobHandle)) 

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

Applications can be granted access to documents by specifying [android.app.appsearch.SetSchemaRequest.Builder#setSchemaTypeVisibilityForPackage](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#setSchemaTypeVisibilityForPackage(kotlin.String,%20kotlin.Boolean,%20android.app.appsearch.PackageIdentifier))when building a schema.

Document access can also be granted to system UIs by specifying [android.app.appsearch.SetSchemaRequest.Builder#setSchemaTypeDisplayedBySystem](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#setSchemaTypeDisplayedBySystem(kotlin.String,%20kotlin.Boolean))when building a schema.

See [AppSearchSession.search](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec))for a detailed explanation on forming a query string.

This method is lightweight. The heavy work will be done in [android.app.appsearch.SearchResults#getNextPage](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults#getNextPage(java.util.concurrent.Executor,%20java.util.function.Consumer)).

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `queryExpression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):query string to search. This value cannot be`null`. |
| `searchSpec` | [SearchSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec):spec for setting document filters, adding projection, setting term match type, etc. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SearchResults](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults) | a [SearchResults](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults) object for retrieved matched documents. This value cannot be`null`. |
