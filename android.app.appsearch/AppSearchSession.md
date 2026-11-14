Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppSearchSession

Kotlin | [Java](https://developer.android.com/reference/android/app/appsearch/AppSearchSession "View this page in Java")

```
class AppSearchSession : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.appsearch.AppSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#) |

Provides a connection to a single AppSearch database.

An `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` instance provides access to database operations such as setting a schema, adding documents, and searching.

This class is thread safe.

## Summary

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#close()()` Closes the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` to persist all schema and document updates, additions, and deletes to disk. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#commitBlob(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(handles: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult<https://developer.android.com/reference/kotlin/android/app/appsearch/CommitBlobResponse!>!>)` Commits the blobs to make it retrievable and immutable. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#getByDocumentId(android.app.appsearch.GetByDocumentIdRequest,%20java.util.concurrent.Executor,%20android.app.appsearch.BatchResultCallback)(request: https://developer.android.com/reference/kotlin/android/app/appsearch/GetByDocumentIdRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument!>)` Gets `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` objects by document IDs in a namespace from the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` database. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#getNamespaces(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>!>)` Retrieves the set of all namespaces in the current database with at least one document. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#getSchema(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult<https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse!>!>)` Retrieves the schema most recently successfully provided to `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#getStorageInfo(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult<https://developer.android.com/reference/kotlin/android/app/appsearch/StorageInfo!>!>)` Gets the storage info for this `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` database. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#openBlobForRead(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(handles: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult<https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse!>!>)` Opens a batch of AppSearch Blobs for reading. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#openBlobForWrite(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(handles: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult<https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForWriteResponse!>!>)` Opens a batch of AppSearch Blobs for writing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#put(android.app.appsearch.PutDocumentsRequest,%20java.util.concurrent.Executor,%20android.app.appsearch.BatchResultCallback)(request: https://developer.android.com/reference/kotlin/android/app/appsearch/PutDocumentsRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://developer.android.com/reference/kotlin/java/lang/Void.html#!>)` Indexes documents into the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` database. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#remove(android.app.appsearch.RemoveByDocumentIdRequest,%20java.util.concurrent.Executor,%20android.app.appsearch.BatchResultCallback)(request: https://developer.android.com/reference/kotlin/android/app/appsearch/RemoveByDocumentIdRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://developer.android.com/reference/kotlin/java/lang/Void.html#!>)` Removes `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` objects by document IDs in a namespace from the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` database. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#remove(kotlin.String,%20android.app.appsearch.SearchSpec,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(queryExpression: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, searchSpec: https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!>)` Removes `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`s from the index by Query. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#removeBlob(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(handles: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult<https://developer.android.com/reference/kotlin/android/app/appsearch/RemoveBlobResponse!>!>)` Removes the blob data from AppSearch. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#reportUsage(android.app.appsearch.ReportUsageRequest,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(request: https://developer.android.com/reference/kotlin/android/app/appsearch/ReportUsageRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!>)` Reports usage of a particular document by namespace and ID. |
| [SearchResults](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)(queryExpression: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, searchSpec: https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec)` Retrieves documents from the open `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` that match a given query string and type of search provided. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#searchSuggestion(kotlin.String,%20android.app.appsearch.SearchSuggestionSpec,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(suggestionQueryExpression: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, searchSuggestionSpec: https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionResult!>!>!>)` Retrieves suggested Strings that could be used as `queryExpression` in `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)` API. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setBlobVisibility(android.app.appsearch.SetBlobVisibilityRequest,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(request: https://developer.android.com/reference/kotlin/android/app/appsearch/SetBlobVisibilityRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!>)` Sets the visibility configuration for all blob namespaces within an appsearch database. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(request: https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest, workExecutor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callbackExecutor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult<https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse!>!>)` Sets the schema that represents the organizational structure of data within the AppSearch database. |

## Public methods

### close

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Closes the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` to persist all schema and document updates, additions, and deletes to disk.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### commitBlob

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
fun commitBlob(
    handles: MutableSet<AppSearchBlobHandle!>, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<CommitBlobResponse!>!>
): Unit
```

Commits the blobs to make it retrievable and immutable.

After this call, the blob is readable via `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#openBlobForRead(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`. Any change to the content or rewrite via `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#openBlobForWrite(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` of this blob won't be allowed.

If the blob is already stored in AppSearch and committed. A failed `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult` with error code `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_ALREADY_EXISTS:kotlin.Int` will be associated with the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`.

If the blob content doesn't match the digest in `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`, a failed `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult` with error code `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_INVALID_ARGUMENT:kotlin.Int` will be associated with the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`. The pending Blob file will be removed from AppSearch.

Pending blobs won't be lost or auto-commit if `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` closed. Pending blobs will store in disk rather than memory. You can re-open `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` and re-write the pending blobs.

The default time to recycle pending and orphan blobs is 1 week. A blob will be considered as an orphan if no `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` references it.

| Parameters ||
|---|---|
| `handles` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchBlobHandle](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle)!\>: The `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`s that identifies the blobs. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [CommitBlobResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/CommitBlobResponse)!\>!\>: Callback to receive the `https://developer.android.com/reference/kotlin/android/app/appsearch/CommitBlobResponse`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyBlobHandle(kotlin.String,%20android.app.appsearch.AppSearchBlobHandle)`

### getByDocumentId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getByDocumentId(
    request: GetByDocumentIdRequest, 
    executor: Executor, 
    callback: BatchResultCallback<String!, GenericDocument!>
): Unit
```

Gets `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` objects by document IDs in a namespace from the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` database.

| Parameters ||
|---|---|
| `request` | [GetByDocumentIdRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/GetByDocumentIdRequest): a request containing a namespace and IDs to get documents for. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [BatchResultCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument)!\>: Callback to receive the pending result of performing this operation. The keys of the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult` represent the input document IDs from the `https://developer.android.com/reference/kotlin/android/app/appsearch/GetByDocumentIdRequest` object. The values are either the corresponding `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` object for the ID on success, or an `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult` object on failure. For example, if an ID is not found, the value for that ID will be set to an `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult` object with result code: `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_NOT_FOUND:kotlin.Int`. If an unexpected internal error occurs in the AppSearch service, `https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback#onSystemError(kotlin.Throwable)` will be invoked with a `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#`. This value cannot be `null`. |

### getNamespaces

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNamespaces(
    executor: Executor, 
    callback: Consumer<AppSearchResult<MutableSet<String!>!>!>
): Unit
```

Retrieves the set of all namespaces in the current database with at least one document.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>!\>: Callback to receive the namespaces. This value cannot be `null`. |

### getSchema

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSchema(
    executor: Executor, 
    callback: Consumer<AppSearchResult<GetSchemaResponse!>!>
): Unit
```

Retrieves the schema most recently successfully provided to `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [GetSchemaResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse)!\>!\>: Callback to receive the pending results of schema. This value cannot be `null`. |

### getStorageInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStorageInfo(
    executor: Executor, 
    callback: Consumer<AppSearchResult<StorageInfo!>!>
): Unit
```

Gets the storage info for this `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` database.

This may take time proportional to the number of documents and may be inefficient to call repeatedly.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [StorageInfo](https://developer.android.com/reference/kotlin/android/app/appsearch/StorageInfo)!\>!\>: Callback to receive the storage info. This value cannot be `null`. |

### openBlobForRead

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
fun openBlobForRead(
    handles: MutableSet<AppSearchBlobHandle!>, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<OpenBlobForReadResponse!>!>
): Unit
```

Opens a batch of AppSearch Blobs for reading.

Only blobs committed via `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#commitBlob(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` are available for reading.

The returned `https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse` must be closed after use to avoid resource leaks. Failing to close it will result in system file descriptor exhaustion.

| Parameters ||
|---|---|
| `handles` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchBlobHandle](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle)!\>: The `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`s that identifies the blobs. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [OpenBlobForReadResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse)!\>!\>: Callback to receive the `https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyBlobHandle(kotlin.String,%20android.app.appsearch.AppSearchBlobHandle)`

### openBlobForWrite

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
fun openBlobForWrite(
    handles: MutableSet<AppSearchBlobHandle!>, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<OpenBlobForWriteResponse!>!>
): Unit
```

Opens a batch of AppSearch Blobs for writing.

A "blob" is a large binary object. It is used to store a significant amount of data that is not searchable, such as images, videos, audio files, or other binary data. Unlike other fields in AppSearch, blobs are stored as blob files on disk rather than in memory, and use `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` to read and write. This allows for efficient handling of large, non-searchable content.

Once done writing, call `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#commitBlob(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` to commit blob files.

This call will create a empty blob file for each given `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`, and a `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` of that blob file will be returned in the `https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForWriteResponse`.

If the blob file is already stored in AppSearch and committed. A failed `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult` with error code `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_ALREADY_EXISTS:kotlin.Int` will be associated with the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`.

If the blob file is already stored in AppSearch but not committed. A `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` of that blob file will be returned for continue writing.

For given duplicate `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`, the same `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` pointing to the same blob file will be returned.

Pending blob files won't be lost or auto-commit if `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` closed. Pending blob files will be stored in disk rather than memory. You can re-open `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` and re-write the pending blob files.

A committed blob file will be considered as an orphan if no `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` references it. Uncommitted pending blob files and orphan blobs files will be cleaned up if they has been created for an extended period (default is 1 week).

The returned `https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForWriteResponse` must be closed after use to avoid resource leaks. Failing to close it will result in system file descriptor exhaustion.

| Parameters ||
|---|---|
| `handles` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchBlobHandle](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle)!\>: The `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`s that identifies the blobs. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [OpenBlobForWriteResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForWriteResponse)!\>!\>: Callback to receive the `https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForWriteResponse`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyBlobHandle(kotlin.String,%20android.app.appsearch.AppSearchBlobHandle)`

### put

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun put(
    request: PutDocumentsRequest, 
    executor: Executor, 
    callback: BatchResultCallback<String!, Void!>
): Unit
```

Indexes documents into the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` database.

Each `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` object must have a `schemaType` field set to an `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema` type that has been previously registered by calling the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` method.

| Parameters ||
|---|---|
| `request` | [PutDocumentsRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/PutDocumentsRequest): containing documents to be indexed. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [BatchResultCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!\>: Callback to receive pending result of performing this operation. The keys of the returned `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult` are the IDs of the input documents. The values are either `null` if the corresponding document was successfully indexed, or a failed `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult` otherwise. If an unexpected internal error occurs in the AppSearch service, `https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback#onSystemError(kotlin.Throwable)` will be invoked with a `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#`. |

### remove

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun remove(
    request: RemoveByDocumentIdRequest, 
    executor: Executor, 
    callback: BatchResultCallback<String!, Void!>
): Unit
```

Removes `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` objects by document IDs in a namespace from the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` database.

Removed documents will no longer be surfaced by `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)` or `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#getByDocumentId(android.app.appsearch.GetByDocumentIdRequest,%20java.util.concurrent.Executor,%20android.app.appsearch.BatchResultCallback)` calls.

Once the database crosses the document count or byte usage threshold, removed documents will be deleted from disk.

| Parameters ||
|---|---|
| `request` | [RemoveByDocumentIdRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/RemoveByDocumentIdRequest): `https://developer.android.com/reference/kotlin/android/app/appsearch/RemoveByDocumentIdRequest` with IDs in a namespace to remove from the index. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [BatchResultCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!\>: Callback to receive the pending result of performing this operation. The keys of the returned `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult` represent the input IDs from the `https://developer.android.com/reference/kotlin/android/app/appsearch/RemoveByDocumentIdRequest` object. The values are either `null` on success, or a failed `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult` otherwise. IDs that are not found will return a failed `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult` with a result code of `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_NOT_FOUND:kotlin.Int`. If an unexpected internal error occurs in the AppSearch service, `https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback#onSystemError(kotlin.Throwable)` will be invoked with a `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#`.. |

### remove

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun remove(
    queryExpression: String, 
    searchSpec: SearchSpec, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<Void!>!>
): Unit
```

Removes `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`s from the index by Query. Documents will be removed if they match the `queryExpression` in given namespaces and schemaTypes which is set via android.app.appsearch.SearchSpec.Builder#addFilterNamespaces and android.app.appsearch.SearchSpec.Builder#addFilterSchemas.

An empty `queryExpression` matches all documents.

An empty set of namespaces or schemaTypes matches all namespaces or schemaTypes in the current database.

| Parameters ||
|---|---|
| `queryExpression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Query String to search. This value cannot be `null`. |
| `searchSpec` | [SearchSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec): Spec containing schemaTypes, namespaces and query expression indicates how document will be removed. All specific about how to scoring, ordering, snippeting and resulting will be ignored. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!\>!\>: Callback to receive errors resulting from removing the documents. If the operation succeeds, the callback will be invoked with `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec` contains a `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec`. `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec` lets you join docs that are not owned by the caller, so the semantics of failures from this method would be complex. |

### removeBlob

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
fun removeBlob(
    handles: MutableSet<AppSearchBlobHandle!>, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<RemoveBlobResponse!>!>
): Unit
```

Removes the blob data from AppSearch.

After this call, the blob data is removed immediately and cannot be recovered. It will not accessible via `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#openBlobForRead(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`. `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#openBlobForWrite(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` could reopen and rewrite it.

This API can be used to remove pending blob data and committed blob data.

Removing a committed blob data that is still referenced by documents will leave those documents with no readable blob content. It is highly recommended to let AppSearch control the blob data's life cycle. AppSearch automatically recycles orphaned and pending blob data. The default time to recycle pending and orphan blob file is 1 week. A blob file will be considered as an orphan if no `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` references it. If you want to remove a committed blob data, you should remove the reference documents first.

| Parameters ||
|---|---|
| `handles` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchBlobHandle](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle)!\>: The `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`s that identifies the blobs. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [RemoveBlobResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/RemoveBlobResponse)!\>!\>: Callback to receive the `https://developer.android.com/reference/kotlin/android/app/appsearch/CommitBlobResponse`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyBlobHandle(kotlin.String,%20android.app.appsearch.AppSearchBlobHandle)`

### reportUsage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reportUsage(
    request: ReportUsageRequest, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<Void!>!>
): Unit
```

Reports usage of a particular document by namespace and ID.

A usage report represents an event in which a user interacted with or viewed a document.

For each call to `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#reportUsage(android.app.appsearch.ReportUsageRequest,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`, AppSearch updates usage count and usage recency metrics for that particular document. These metrics are used for ordering `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)` results by the `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_USAGE_COUNT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_USAGE_LAST_USED_TIMESTAMP:kotlin.Int` ranking strategies.

Reporting usage of a document is optional.

| Parameters ||
|---|---|
| `request` | [ReportUsageRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/ReportUsageRequest): The usage reporting request. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!\>!\>: Callback to receive errors. If the operation succeeds, the callback will be invoked with `null`. |

### search

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun search(
    queryExpression: String, 
    searchSpec: SearchSpec
): SearchResults
```

Retrieves documents from the open `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#` that match a given query string and type of search provided.

Query strings can be empty, contain one term with no operators, or contain multiple terms and operators.

For query strings that are empty, all documents that match the `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec` will be returned.

For query strings with a single term and no operators, documents that match the provided query string and `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec` will be returned.

The following operators are supported:

- AND (implicit) AND is an operator that matches documents that contain *all* provided terms.

 **NOTE:** A space between terms is treated as an "AND" operator. Explicitly including "AND" in a query string will treat "AND" as a term, returning documents that also contain "AND".

 Example: "apple AND banana" matches documents that contain the terms "apple", "and", "banana".

 Example: "apple banana" matches documents that contain both "apple" and "banana".

 Example: "apple banana cherry" matches documents that contain "apple", "banana", and "cherry".
- OR OR is an operator that matches documents that contain *any* provided term.

 Example: "apple OR banana" matches documents that contain either "apple" or "banana".

 Example: "apple OR banana OR cherry" matches documents that contain any of "apple", "banana", or "cherry".
- Exclusion (-) Exclusion (-) is an operator that matches documents that *do not* contain the provided term.

 Example: "-apple" matches documents that do not contain "apple".
- Grouped Terms For queries that require multiple operators and terms, terms can be grouped into subqueries. Subqueries are contained within an open "(" and close ")" parenthesis.

 Example: "(donut OR bagel) (coffee OR tea)" matches documents that contain either "donut" or "bagel" and either "coffee" or "tea".
- Property Restricts For queries that require a term to match a specific `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema` property of a document, a ":" must be included between the property name and the term.

 Example: "subject:important" matches documents that contain the term "important" in the "subject" property.

The above description covers the query operators that are supported on all versions of AppSearch. Additional operators and their required features are described below.

LIST_FILTER_QUERY_LANGUAGE: This feature covers the expansion of the query language to conform to the definition of the list filters language (https://aip.dev/160). This includes:

- addition of explicit 'AND' and 'NOT' operators
- property restricts are allowed with groupings (ex. "prop:(a OR b)")
- addition of custom functions to control matching

The newly added custom functions covered by this feature are:

- createList(String...)
- search(String, `List<String>`)
- propertyDefined(String)

createList takes a variable number of strings and returns a list of strings. It is for use with search.

search takes a query string that will be parsed according to the supported query language and an optional list of strings that specify the properties to be restricted to. This exists as a convenience for multiple property restricts. So, for example, the query \`(subject:foo OR body:foo) (subject:bar OR body:bar)\` could be rewritten as \`search("foo bar", createList("subject", "body"))\`.

propertyDefined takes a string specifying the property of interest and matches all documents of any type that defines the specified property (ex. \`propertyDefined("sender.name")\`). Note that propertyDefined will match so long as the document's type defines the specified property. Unlike the "hasProperty" function below, this function does NOT require that the document actually hold any values for this property.

NUMERIC_SEARCH: This feature covers numeric search expressions. In the query language, the values of properties that have `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema.LongPropertyConfig#INDEXING_TYPE_RANGE:kotlin.Int` set can be matched with a numeric search expression (the property, a supported comparator and an integer value). Supported comparators are \<, \<=, ==, \>= and \>.

Ex. \`price \< 10\` will match all documents that has a numeric value in its price property that is less than 10.

VERBATIM_SEARCH: This feature covers the verbatim string operator (quotation marks).

Ex. \`"foo/bar" OR baz\` will ensure that 'foo/bar' is treated as a single 'verbatim' token.

LIST_FILTER_HAS_PROPERTY_FUNCTION: This feature covers the "hasProperty" function in query expressions, which takes a string specifying the property of interest and matches all documents that hold values for this property. Not to be confused with the "propertyDefined" function, which checks whether a document's schema has defined the property, instead of whether a document itself has this property.

Ex. \`foo hasProperty("sender.name")\` will return all documents that have the term "foo" AND have values in the property "sender.name". Consider two documents, documentA and documentB, of the same schema with an optional property "sender.name". If documentA sets "foo" in this property but documentB does not, then \`hasProperty("sender.name")\` will only match documentA. However, \`propertyDefined("sender.name")\` will match both documentA and documentB, regardless of whether a value is actually set.

LIST_FILTER_MATCH_SCORE_EXPRESSION_FUNCTION: This feature covers the "matchScoreExpression" function in query expressions.

Usage: matchScoreExpression({score_expression}, {low}, {high})

- matchScoreExpression matches all documents with scores falling within the specified range. These scores are calculated using the provided score expression, which adheres to the syntax defined in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec.Builder#setRankingStrategy(kotlin.String)`.
- "score_expression" is a string value that specifies the score expression.
- "low" and "high" are floating point numbers that specify the score range. The "high" parameter is optional; if not provided, it defaults to positive infinity.

Ex. \`matchScoreExpression("this.documentScore()", 3, 4)\` will return all documents that have document scores from 3 to 4.

SCHEMA_EMBEDDING_PROPERTY_CONFIG: This feature covers the "semanticSearch" and "getEmbeddingParameter" functions in query expressions, which are used for semantic search.

Usage: semanticSearch(getEmbeddingParameter({embedding_index}), {low}, {high}, {metric})

- semanticSearch matches all documents that have at least one embedding vector with a matching model signature (see `https://developer.android.com/reference/kotlin/android/app/appsearch/EmbeddingVector#getModelSignature()`) and a similarity score within the range specified based on the provided metric.
- getEmbeddingParameter({embedding_index}) retrieves the embedding search passed in android.app.appsearch.SearchSpec.Builder#addEmbeddingParameters based on the index specified, which starts from 0.
- "low" and "high" are floating point numbers that specify the similarity score range. If omitted, they default to negative and positive infinity, respectively.
- "metric" is a string value that specifies how embedding similarities should be calculated. If omitted, it defaults to the metric specified in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec.Builder#setDefaultEmbeddingSearchMetricType(kotlin.Int)`. Possible values:
 - "COSINE"
 - "DOT_PRODUCT"
 - "EUCLIDEAN"

Examples:

- Basic: semanticSearch(getEmbeddingParameter(0), 0.5, 1, "COSINE")
- With a property restriction: property1:semanticSearch(getEmbeddingParameter(0), 0.5, 1)
- Hybrid: foo OR semanticSearch(getEmbeddingParameter(0), 0.5, 1)
- Complex: (foo OR semanticSearch(getEmbeddingParameter(0), 0.5, 1)) AND bar

SEARCH_SPEC_SEARCH_STRING_PARAMETERS: This feature covers the "getSearchStringParameter" function in query expressions, which substitutes the string provided at the same index in android.app.appsearch.SearchSpec.Builder#addSearchStringParameters into the query as plain text. This string is then segmented, normalized and stripped of punctuation-only segments. The remaining tokens are then AND'd together. This function is useful for callers who wish to provide user input, but want to ensure that that user input does not invoke any query operators.

Usage: getSearchStringParameter({search_parameter_strings_index})

Ex. \`foo OR getSearchStringParameter(0)\` with `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#getSearchStringParameters()` returning {"bar OR baz."}. The string "bar OR baz." will be segmented into "bar", "OR", "baz", ".". Punctuation is removed and the segments are normalized to "bar", "or", "baz". This query will be equivalent to \`foo OR (bar AND or AND baz)\`.

Additional search specifications, such as filtering by `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema` type or adding projection, can be set by calling the corresponding `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec.Builder` setter.

This method is lightweight. The heavy work will be done in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults#getNextPage(java.util.concurrent.Executor,%20java.util.function.Consumer)`.

| Parameters ||
|---|---|
| `queryExpression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): query string to search. This value cannot be `null`. |
| `searchSpec` | [SearchSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec): spec for setting document filters, adding projection, setting term match type, etc. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults` | a `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults` object for retrieved matched documents. This value cannot be `null`. |

### searchSuggestion

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun searchSuggestion(
    suggestionQueryExpression: String, 
    searchSuggestionSpec: SearchSuggestionSpec, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<MutableList<SearchSuggestionResult!>!>!>
): Unit
```

Retrieves suggested Strings that could be used as `queryExpression` in `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)` API.

The `suggestionQueryExpression` can contain one term with no operators, or contain multiple terms and operators. Operators will be considered as a normal term. Please see the operator examples below. The `suggestionQueryExpression` must end with a valid term, the suggestions are generated based on the last term. If the input `suggestionQueryExpression` doesn't have a valid token, AppSearch will return an empty result list. Please see the invalid examples below.

Example: if there are following documents with content stored in AppSearch.

- document1: "term1"
- document2: "term1 term2"
- document3: "term1 term2 term3"
- document4: "org"

Search suggestions with the single term `suggestionQueryExpression` "t", the suggested results are:

- "term1" - Use it to be queryExpression in `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)` could get 3 `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult`s, which contains document 1, 2 and 3.
- "term2" - Use it to be queryExpression in `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)` could get 2 `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult`s, which contains document 2 and 3.
- "term3" - Use it to be queryExpression in `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)` could get 1 `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult`, which contains document 3.

Search suggestions with the multiple term `suggestionQueryExpression` "org t", the suggested result will be "org term1" - The last token is completed by the suggested String.

Operators in `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)` are supported.

**NOTE:** Exclusion and Grouped Terms in the last term is not supported.

example: "apple -f": This Api will throw an `https://developer.android.com/reference/kotlin/android/app/appsearch/exceptions/AppSearchException` with `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_INVALID_ARGUMENT:kotlin.Int`.

example: "apple (f)": This Api will return an empty results.

Invalid example: All these input `suggestionQueryExpression` don't have a valid last token, AppSearch will return an empty result list.

- "" - Empty `suggestionQueryExpression`.
- "(f)" - Ending in a closed brackets.
- "f:" - Ending in an operator.
- "f " - Ending in trailing space.

| Parameters ||
|---|---|
| `suggestionQueryExpression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the non empty query string to search suggestions. This value cannot be `null`. |
| `searchSuggestionSpec` | [SearchSuggestionSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec): spec for setting document filters. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SearchSuggestionResult](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionResult)!\>!\>!\>: Callback to receive the pending result of performing this operation, which is a List of `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionResult` on success. The returned suggestion Strings are ordered by the number of `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult` you could get by using that suggestion in `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)`

### setBlobVisibility

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
fun setBlobVisibility(
    request: SetBlobVisibilityRequest, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<Void!>!>
): Unit
```

Sets the visibility configuration for all blob namespaces within an appsearch database.

Blobs under the same namespace will share same visibility settings.

The default setting is blobs will be only visible to the owner package and System. To configure other kinds of sharing, set `https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig` via `https://developer.android.com/reference/kotlin/android/app/appsearch/SetBlobVisibilityRequest`.

| Parameters ||
|---|---|
| `request` | [SetBlobVisibilityRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/SetBlobVisibilityRequest): The request holds visibility settings for all blob namespaces. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!\>!\>: Callback to receive the pending result of performing this operation which resolves to `null` on success. |

### setSchema

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setSchema(
    request: SetSchemaRequest, 
    workExecutor: Executor, 
    callbackExecutor: Executor, 
    callback: Consumer<AppSearchResult<SetSchemaResponse!>!>
): Unit
```

Sets the schema that represents the organizational structure of data within the AppSearch database.

Upon creating an `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#`, `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` should be called. If the schema needs to be updated, or it has not been previously set, then the provided schema will be saved and persisted to disk. Otherwise, `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` is handled efficiently as a no-op call.

| Parameters ||
|---|---|
| `request` | [SetSchemaRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest): the schema to set or update the AppSearch database to. This value cannot be `null`. |
| `workExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to schedule heavy client-side background work such as transforming documents. This value cannot be `null`. |
| `callbackExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [SetSchemaResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse)!\>!\>: Callback to receive the result of setting the schema. This value cannot be `null`. |
