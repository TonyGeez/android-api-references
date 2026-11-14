# GlobalSearchSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GlobalSearchSession

Kotlin | [Java](https://developer.android.com/reference/android/app/appsearch/GlobalSearchSession "View this page in Java") 
| --- | --- |

```
open class GlobalSearchSession : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#) |

Provides a connection to all AppSearch databases the querying application has been granted access to.

This class is thread safe.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#close())`()` Closes the [GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getByDocumentId](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#getByDocumentId(kotlin.String,%20kotlin.String,%20android.app.appsearch.GetByDocumentIdRequest,%20java.util.concurrent.Executor,%20android.app.appsearch.BatchResultCallback))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `request:` ` [GetByDocumentIdRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/GetByDocumentIdRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [BatchResultCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument)!>`)` Retrieves [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) documents, belonging to the specified package name and database name and identified by the namespace and ids in the request, from the [GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#) database. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#getSchema(kotlin.String,%20kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)< [GetSchemaResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse)!>!>`)` Retrieves the collection of schemas most recently successfully provided to [android.app.appsearch.AppSearchSession#setSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)) for any types belonging to the requested package and database that the caller has been granted access to. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openBlobForRead](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#openBlobForRead(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`handles:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [AppSearchBlobHandle](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle)!>`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)< [OpenBlobForReadResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse)!>!>`)` Opens a batch of AppSearch Blobs for reading. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#registerObserverCallback(kotlin.String,%20android.app.appsearch.observer.ObserverSpec,%20java.util.concurrent.Executor,%20android.app.appsearch.observer.ObserverCallback))`(`targetPackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `spec:` ` [ObserverSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverSpec)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `observer:` ` [ObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback)`)` Adds an [ObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback) to monitor changes within the databases owned by `targetPackageName` if they match the given . |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportSystemUsage](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#reportSystemUsage(android.app.appsearch.ReportSystemUsageRequest,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`request:` ` [ReportSystemUsageRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/ReportSystemUsageRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!>!>`)` Reports that a particular document has been used from a system surface. |
| --- | --- |
| open [SearchResults](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults) | [search](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec))`(`queryExpression:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `searchSpec:` ` [SearchSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec)`)` Retrieves documents from all AppSearch databases that the querying application has access to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#unregisterObserverCallback(kotlin.String,%20android.app.appsearch.observer.ObserverCallback))`(`targetPackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `observer:` ` [ObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback)`)` Removes previously registered [ObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback) instances from the system. |

## Public methods

### close

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes the [GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#).

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### getByDocumentId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
open fun getByDocumentId(
    packageName: String, 
    databaseName: String, 
    request: GetByDocumentIdRequest, 
    executor: Executor, 
    callback: BatchResultCallback<String!, GenericDocument!>
): Unit
```

Retrieves [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) documents, belonging to the specified package name and database name and identified by the namespace and ids in the request, from the [GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#) database. When a call is successful, the result will be returned in the successes section of the [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult) object in the callback. If the package doesn't exist, database doesn't exist, or if the calling package doesn't have access, these failures will be reflected as [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) objects with a RESULT_NOT_FOUND status code in the failures section of the [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult) object.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the package to get from This value cannot be `null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the database to get from This value cannot be `null`. |
| `request` | [GetByDocumentIdRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/GetByDocumentIdRequest): a request containing a namespace and IDs to get documents for. This value cannot be `null`. |
| --- | --- |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [BatchResultCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument)!\>: Callback to receive the pending result of performing this operation. The keys of the returned [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult) are the input IDs. The values are the returned [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) s on success, or a failed [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) otherwise. IDs that are not found will return a failed [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) with a result code of [AppSearchResult.RESULT_NOT_FOUND](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_NOT_FOUND:kotlin.Int). If an unexpected internal error occurs in the AppSearch service, [BatchResultCallback.onSystemError](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback#onSystemError(kotlin.Throwable)) will be invoked with a [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#). This value cannot be `null`. |

### getSchema

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
open fun getSchema(
    packageName: String, 
    databaseName: String, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<GetSchemaResponse!>!>
): Unit
```

Retrieves the collection of schemas most recently successfully provided to [android.app.appsearch.AppSearchSession#setSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)) for any types belonging to the requested package and database that the caller has been granted access to.

If the requested package/database combination does not exist or the caller has not been granted access to it, then an empty GetSchemaResponse will be returned.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the package that owns the requested [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) instances. This value cannot be `null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the database that owns the requested [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) instances. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [GetSchemaResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse)!\>!\>: Callback to receive the pending [GetSchemaResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse) containing the schemas that the caller has access to or an empty GetSchemaResponse if the request package and database does not exist, has not set a schema or contains no schemas that are accessible to the caller. This value cannot be `null`. |

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

See [AppSearchSession.openBlobForRead](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#openBlobForRead(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)) for a general description when a blob is for read.

The returned [OpenBlobForReadResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse) must be closed after use to avoid resource leaks. Failing to close it will result in system file descriptor exhaustion.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handles` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchBlobHandle](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle)!\>: The [AppSearchBlobHandle](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle) s that identifies the blobs. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [OpenBlobForReadResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse)!\>!\>: Callback to receive the [OpenBlobForReadResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse). This value cannot be `null`. |
| --- | --- |

**See Also**

- [android.app.appsearch.GenericDocument.Builder#setPropertyBlobHandle](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyBlobHandle(kotlin.String,%20android.app.appsearch.AppSearchBlobHandle)) 

### registerObserverCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
open fun registerObserverCallback(
    targetPackageName: String, 
    spec: ObserverSpec, 
    executor: Executor, 
    observer: ObserverCallback
): Unit
```

Adds an [ObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback) to monitor changes within the databases owned by `targetPackageName` if they match the given .

The observer callback is only triggered for data that changes after it is registered. No notification about existing data is sent as a result of registering an observer. To find out about existing data, you must use the [GlobalSearchSession.search](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)) API.

If the data owned by `targetPackageName` is not visible to you, the registration call will succeed but no notifications will be dispatched. Notifications could start flowing later if `targetPackageName` changes its schema visibility settings.

If no package matching `targetPackageName` exists on the system, the registration call will succeed but no notifications will be dispatched. Notifications could start flowing later if `targetPackageName` is installed and starts indexing data.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `targetPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Package whose changes to monitor This value cannot be `null`. |
| `spec` | [ObserverSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverSpec): Specification of what types of changes to listen for This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to call the `observer` callback methods. This value cannot be `null`. |
| --- | --- |
| `observer` | [ObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback): Callback to trigger when a schema or document changes This value cannot be `null`. |

| Exceptions ||
|-------------------------------------------------------|----------------------------------------------------|
| `android.app.appsearch.exceptions.AppSearchException` | if an error occurs trying to register the observer |

### reportSystemUsage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reportSystemUsage(
    request: ReportSystemUsageRequest, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<Void!>!>
): Unit
```

Reports that a particular document has been used from a system surface.

See [AppSearchSession.reportUsage](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#reportUsage(android.app.appsearch.ReportUsageRequest,%20java.util.concurrent.Executor,%20java.util.function.Consumer)) for a general description of document usage, as well as an API that can be used by the app itself.

Usage reported via this method is accounted separately from usage reported via [android.app.appsearch.AppSearchSession#reportUsage](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#reportUsage(android.app.appsearch.ReportUsageRequest,%20java.util.concurrent.Executor,%20java.util.function.Consumer)) and may be accessed using the constants [android.app.appsearch.SearchSpec#RANKING_STRATEGY_SYSTEM_USAGE_COUNT](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_SYSTEM_USAGE_COUNT:kotlin.Int) and [android.app.appsearch.SearchSpec#RANKING_STRATEGY_SYSTEM_USAGE_LAST_USED_TIMESTAMP](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_SYSTEM_USAGE_LAST_USED_TIMESTAMP:kotlin.Int).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [ReportSystemUsageRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/ReportSystemUsageRequest): The usage reporting request. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!\>!\>: Callback to receive errors. If the operation succeeds, the callback will be invoked with an [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) whose value is `null`. The callback will be invoked with an [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) of [AppSearchResult.RESULT_SECURITY_ERROR](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_SECURITY_ERROR:kotlin.Int) if this API is invoked by an app which is not part of the system. |
| --- | --- |

### search

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun search(
    queryExpression: String, 
    searchSpec: SearchSpec
): SearchResults
```

Retrieves documents from all AppSearch databases that the querying application has access to.

Applications can be granted access to documents by specifying [android.app.appsearch.SetSchemaRequest.Builder#setSchemaTypeVisibilityForPackage](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#setSchemaTypeVisibilityForPackage(kotlin.String,%20kotlin.Boolean,%20android.app.appsearch.PackageIdentifier)), or android.app.appsearch.SetSchemaRequest.Builder#setDocumentClassVisibilityForPackage when building a schema.

Document access can also be granted to system UIs by specifying [android.app.appsearch.SetSchemaRequest.Builder#setSchemaTypeDisplayedBySystem](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#setSchemaTypeDisplayedBySystem(kotlin.String,%20kotlin.Boolean)), or android.app.appsearch.SetSchemaRequest.Builder#setDocumentClassDisplayedBySystem when building a schema.

See [AppSearchSession.search](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)) for a detailed explanation on forming a query string.

This method is lightweight. The heavy work will be done in [android.app.appsearch.SearchResults#getNextPage](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults#getNextPage(java.util.concurrent.Executor,%20java.util.function.Consumer)).

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `queryExpression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): query string to search. This value cannot be `null`. |
| `searchSpec` | [SearchSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec): spec for setting document filters, adding projection, setting term match type, etc. This value cannot be `null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SearchResults](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults) | a [SearchResults](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults) object for retrieved matched documents. This value cannot be `null`. |

### unregisterObserverCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
open fun unregisterObserverCallback(
    targetPackageName: String, 
    observer: ObserverCallback
): Unit
```

Removes previously registered [ObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback) instances from the system.

All instances of [ObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback) which are registered to observe `targetPackageName` and compare equal to the provided callback using the provided argument's `ObserverCallback#equals` will be removed.

If no matching observers have been registered, this method has no effect. If multiple matching observers have been registered, all will be removed.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `targetPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Package which the observers to be removed are listening to. This value cannot be `null`. |
| `observer` | [ObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback): Callback to unregister. This value cannot be `null`. |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.app.appsearch.exceptions.AppSearchException` | if an error occurs trying to remove the observer, such as a failure to communicate with the system service. Note that no error will be thrown if the provided observer doesn't match any registered observer. |
