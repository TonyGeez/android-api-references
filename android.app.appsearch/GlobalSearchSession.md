# GlobalSearchSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GlobalSearchSession

Kotlin | [Java](GlobalSearchSession.md) 
| --- | --- |

```
open class GlobalSearchSession : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.GlobalSearchSession](GlobalSearchSession.md) |

Provides a connection to all AppSearch databases the querying application has been granted access to.

This class is thread safe.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](GlobalSearchSession.md))`()` Closes the [GlobalSearchSession](GlobalSearchSession.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getByDocumentId](GlobalSearchSession.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `request:` ` [GetByDocumentIdRequest](GetByDocumentIdRequest.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [BatchResultCallback](BatchResultCallback.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [GenericDocument](GenericDocument.md)!>`)` Retrieves [GenericDocument](GenericDocument.md) documents, belonging to the specified package name and database name and identified by the namespace and ids in the request, from the [GlobalSearchSession](GlobalSearchSession.md) database. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getSchema](GlobalSearchSession.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [Consumer](../java.util.function/Consumer.md)< [AppSearchResult](AppSearchResult.md)< [GetSchemaResponse](GetSchemaResponse.md)!>!>`)` Retrieves the collection of schemas most recently successfully provided to [android.app.appsearch.AppSearchSession#setSchema](AppSearchSession.md)) for any types belonging to the requested package and database that the caller has been granted access to. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openBlobForRead](GlobalSearchSession.md))`(`handles:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [AppSearchBlobHandle](AppSearchBlobHandle.md)!>`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [Consumer](../java.util.function/Consumer.md)< [AppSearchResult](AppSearchResult.md)< [OpenBlobForReadResponse](OpenBlobForReadResponse.md)!>!>`)` Opens a batch of AppSearch Blobs for reading. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerObserverCallback](GlobalSearchSession.md))`(`targetPackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `spec:` ` [ObserverSpec](../android.app.appsearch.observer/ObserverSpec.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `observer:` ` [ObserverCallback](../android.app.appsearch.observer/ObserverCallback.md)`)` Adds an [ObserverCallback](../android.app.appsearch.observer/ObserverCallback.md) to monitor changes within the databases owned by `targetPackageName` if they match the given . |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportSystemUsage](GlobalSearchSession.md))`(`request:` ` [ReportSystemUsageRequest](ReportSystemUsageRequest.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [Consumer](../java.util.function/Consumer.md)< [AppSearchResult](AppSearchResult.md)< [Void](../java.lang/Void.md)!>!>`)` Reports that a particular document has been used from a system surface. |
| --- | --- |
| open [SearchResults](SearchResults.md) | [search](GlobalSearchSession.md))`(`queryExpression:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `searchSpec:` ` [SearchSpec](SearchSpec.md)`)` Retrieves documents from all AppSearch databases that the querying application has access to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterObserverCallback](GlobalSearchSession.md))`(`targetPackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `observer:` ` [ObserverCallback](../android.app.appsearch.observer/ObserverCallback.md)`)` Removes previously registered [ObserverCallback](../android.app.appsearch.observer/ObserverCallback.md) instances from the system. |

## Public methods

### close

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes the [GlobalSearchSession](GlobalSearchSession.md).

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

Retrieves [GenericDocument](GenericDocument.md) documents, belonging to the specified package name and database name and identified by the namespace and ids in the request, from the [GlobalSearchSession](GlobalSearchSession.md) database. When a call is successful, the result will be returned in the successes section of the [AppSearchBatchResult](AppSearchBatchResult.md) object in the callback. If the package doesn't exist, database doesn't exist, or if the calling package doesn't have access, these failures will be reflected as [AppSearchResult](AppSearchResult.md) objects with a RESULT_NOT_FOUND status code in the failures section of the [AppSearchBatchResult](AppSearchBatchResult.md) object.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the package to get from This value cannot be `null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the database to get from This value cannot be `null`. |
| `request` | [GetByDocumentIdRequest](GetByDocumentIdRequest.md): a request containing a namespace and IDs to get documents for. This value cannot be `null`. |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [BatchResultCallback](BatchResultCallback.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [GenericDocument](GenericDocument.md)!\>: Callback to receive the pending result of performing this operation. The keys of the returned [AppSearchBatchResult](AppSearchBatchResult.md) are the input IDs. The values are the returned [GenericDocument](GenericDocument.md) s on success, or a failed [AppSearchResult](AppSearchResult.md) otherwise. IDs that are not found will return a failed [AppSearchResult](AppSearchResult.md) with a result code of [AppSearchResult.RESULT_NOT_FOUND](AppSearchResult.md). If an unexpected internal error occurs in the AppSearch service, [BatchResultCallback.onSystemError](BatchResultCallback.md)) will be invoked with a [Throwable](../java.lang/Throwable.md). This value cannot be `null`. |

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

Retrieves the collection of schemas most recently successfully provided to [android.app.appsearch.AppSearchSession#setSchema](AppSearchSession.md)) for any types belonging to the requested package and database that the caller has been granted access to.

If the requested package/database combination does not exist or the caller has not been granted access to it, then an empty GetSchemaResponse will be returned.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the package that owns the requested [AppSearchSchema](AppSearchSchema.md) instances. This value cannot be `null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the database that owns the requested [AppSearchSchema](AppSearchSchema.md) instances. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [GetSchemaResponse](GetSchemaResponse.md)!\>!\>: Callback to receive the pending [GetSchemaResponse](GetSchemaResponse.md) containing the schemas that the caller has access to or an empty GetSchemaResponse if the request package and database does not exist, has not set a schema or contains no schemas that are accessible to the caller. This value cannot be `null`. |

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

See [AppSearchSession.openBlobForRead](AppSearchSession.md)) for a general description when a blob is for read.

The returned [OpenBlobForReadResponse](OpenBlobForReadResponse.md) must be closed after use to avoid resource leaks. Failing to close it will result in system file descriptor exhaustion.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handles` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchBlobHandle](AppSearchBlobHandle.md)!\>: The [AppSearchBlobHandle](AppSearchBlobHandle.md) s that identifies the blobs. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [OpenBlobForReadResponse](OpenBlobForReadResponse.md)!\>!\>: Callback to receive the [OpenBlobForReadResponse](OpenBlobForReadResponse.md). This value cannot be `null`. |
| --- | --- |

**See Also**

- [android.app.appsearch.GenericDocument.Builder#setPropertyBlobHandle](../android/app/appsearch/GenericDocument.Builder.md)) 

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

Adds an [ObserverCallback](../android.app.appsearch.observer/ObserverCallback.md) to monitor changes within the databases owned by `targetPackageName` if they match the given .

The observer callback is only triggered for data that changes after it is registered. No notification about existing data is sent as a result of registering an observer. To find out about existing data, you must use the [GlobalSearchSession.search](GlobalSearchSession.md)) API.

If the data owned by `targetPackageName` is not visible to you, the registration call will succeed but no notifications will be dispatched. Notifications could start flowing later if `targetPackageName` changes its schema visibility settings.

If no package matching `targetPackageName` exists on the system, the registration call will succeed but no notifications will be dispatched. Notifications could start flowing later if `targetPackageName` is installed and starts indexing data.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `targetPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Package whose changes to monitor This value cannot be `null`. |
| `spec` | [ObserverSpec](../android.app.appsearch.observer/ObserverSpec.md): Specification of what types of changes to listen for This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to call the `observer` callback methods. This value cannot be `null`. |
| --- | --- |
| `observer` | [ObserverCallback](../android.app.appsearch.observer/ObserverCallback.md): Callback to trigger when a schema or document changes This value cannot be `null`. |

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

See [AppSearchSession.reportUsage](AppSearchSession.md)) for a general description of document usage, as well as an API that can be used by the app itself.

Usage reported via this method is accounted separately from usage reported via [android.app.appsearch.AppSearchSession#reportUsage](AppSearchSession.md)) and may be accessed using the constants [android.app.appsearch.SearchSpec#RANKING_STRATEGY_SYSTEM_USAGE_COUNT](SearchSpec.md) and [android.app.appsearch.SearchSpec#RANKING_STRATEGY_SYSTEM_USAGE_LAST_USED_TIMESTAMP](SearchSpec.md).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [ReportSystemUsageRequest](ReportSystemUsageRequest.md): The usage reporting request. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [Void](../java.lang/Void.md)!\>!\>: Callback to receive errors. If the operation succeeds, the callback will be invoked with an [AppSearchResult](AppSearchResult.md) whose value is `null`. The callback will be invoked with an [AppSearchResult](AppSearchResult.md) of [AppSearchResult.RESULT_SECURITY_ERROR](AppSearchResult.md) if this API is invoked by an app which is not part of the system. |
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

Applications can be granted access to documents by specifying [android.app.appsearch.SetSchemaRequest.Builder#setSchemaTypeVisibilityForPackage](../android/app/appsearch/SetSchemaRequest.Builder.md)), or android.app.appsearch.SetSchemaRequest.Builder#setDocumentClassVisibilityForPackage when building a schema.

Document access can also be granted to system UIs by specifying [android.app.appsearch.SetSchemaRequest.Builder#setSchemaTypeDisplayedBySystem](../android/app/appsearch/SetSchemaRequest.Builder.md)), or android.app.appsearch.SetSchemaRequest.Builder#setDocumentClassDisplayedBySystem when building a schema.

See [AppSearchSession.search](AppSearchSession.md)) for a detailed explanation on forming a query string.

This method is lightweight. The heavy work will be done in [android.app.appsearch.SearchResults#getNextPage](SearchResults.md)).

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `queryExpression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): query string to search. This value cannot be `null`. |
| `searchSpec` | [SearchSpec](SearchSpec.md): spec for setting document filters, adding projection, setting term match type, etc. This value cannot be `null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SearchResults](SearchResults.md) | a [SearchResults](SearchResults.md) object for retrieved matched documents. This value cannot be `null`. |

### unregisterObserverCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
open fun unregisterObserverCallback(
    targetPackageName: String, 
    observer: ObserverCallback
): Unit
```

Removes previously registered [ObserverCallback](../android.app.appsearch.observer/ObserverCallback.md) instances from the system.

All instances of [ObserverCallback](../android.app.appsearch.observer/ObserverCallback.md) which are registered to observe `targetPackageName` and compare equal to the provided callback using the provided argument's `ObserverCallback#equals` will be removed.

If no matching observers have been registered, this method has no effect. If multiple matching observers have been registered, all will be removed.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `targetPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Package which the observers to be removed are listening to. This value cannot be `null`. |
| `observer` | [ObserverCallback](../android.app.appsearch.observer/ObserverCallback.md): Callback to unregister. This value cannot be `null`. |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.app.appsearch.exceptions.AppSearchException` | if an error occurs trying to remove the observer, such as a failure to communicate with the system service. Note that no error will be thrown if the provided observer doesn't match any registered observer. |
