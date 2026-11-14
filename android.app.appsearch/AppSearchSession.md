Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppSearchSession

Kotlin | [Java](AppSearchSession.md)
| --- | --- |

```
class AppSearchSession : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.AppSearchSession](AppSearchSession.md) |

Provides a connection to a single AppSearch database.

An AppSearchSession instance provides access to database operations such as setting a schema, adding documents, and searching.

This class is thread safe.

## Summary

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | close Closes the AppSearchSession to persist all schema and document updates, additions, and deletes to disk. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | commitBlob Commits the blobs to make it retrievable and immutable. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getByDocumentId Gets GenericDocument objects by document IDs in a namespace from the AppSearchSession database. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getNamespaces Retrieves the set of all namespaces in the current database with at least one document. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getSchema Retrieves the schema most recently successfully provided to setSchema. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getStorageInfo Gets the storage info for this AppSearchSession database. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | openBlobForRead Opens a batch of AppSearch Blobs for reading. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | openBlobForWrite Opens a batch of AppSearch Blobs for writing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | put Indexes documents into the AppSearchSession database. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | remove Removes GenericDocument objects by document IDs in a namespace from the AppSearchSession database. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | remove Removes GenericDocuments from the index by Query. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeBlob Removes the blob data from AppSearch. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | reportUsage Reports usage of a particular document by namespace and ID. |
| [SearchResults](SearchResults.md) | search Retrieves documents from the open AppSearchSession that match a given query string and type of search provided. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | searchSuggestion Retrieves suggested Strings that could be used as `queryExpression` in search API. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBlobVisibility Sets the visibility configuration for all blob namespaces within an appsearch database. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSchema Sets the schema that represents the organizational structure of data within the AppSearch database. |

## Public methods

### close

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Closes the AppSearchSession to persist all schema and document updates, additions, and deletes to disk.

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

After this call, the blob is readable via openBlobForRead. Any change to the content or rewrite via openBlobForWrite of this blob won't be allowed.

If the blob is already stored in AppSearch and committed. A failed AppSearchResult with error code `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_ALREADY_EXISTS:kotlin.Int` will be associated with the AppSearchBlobHandle.

If the blob content doesn't match the digest in AppSearchBlobHandle, a failed AppSearchResult with error code `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_INVALID_ARGUMENT:kotlin.Int` will be associated with the AppSearchBlobHandle. The pending Blob file will be removed from AppSearch.

Pending blobs won't be lost or auto-commit if AppSearchSession closed. Pending blobs will store in disk rather than memory. You can re-open AppSearchSession and re-write the pending blobs.

The default time to recycle pending and orphan blobs is 1 week. A blob will be considered as an orphan if no GenericDocument references it.

| Parameters ||
|---|---|
| `handles` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchBlobHandle](AppSearchBlobHandle.md)!\>: The AppSearchBlobHandles that identifies the blobs. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [CommitBlobResponse](CommitBlobResponse.md)!\>!\>: Callback to receive the CommitBlobResponse. This value cannot be `null`. |
| --- | --- |

**See Also**

- setPropertyBlobHandle

### getByDocumentId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getByDocumentId(
    request: GetByDocumentIdRequest, 
    executor: Executor, 
    callback: BatchResultCallback<String!, GenericDocument!>
): Unit
```

Gets GenericDocument objects by document IDs in a namespace from the AppSearchSession database.

| Parameters ||
|---|---|
| `request` | [GetByDocumentIdRequest](GetByDocumentIdRequest.md): a request containing a namespace and IDs to get documents for. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [BatchResultCallback](BatchResultCallback.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [GenericDocument](GenericDocument.md)!\>: Callback to receive the pending result of performing this operation. The keys of the AppSearchBatchResult represent the input document IDs from the GetByDocumentIdRequest object. The values are either the corresponding GenericDocument object for the ID on success, or an AppSearchResult object on failure. For example, if an ID is not found, the value for that ID will be set to an AppSearchResult object with result code: `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_NOT_FOUND:kotlin.Int`. If an unexpected internal error occurs in the AppSearch service, onSystemError will be invoked with a `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#`. This value cannot be `null`. |
| --- | --- |

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
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>!\>: Callback to receive the namespaces. This value cannot be `null`. |

### getSchema

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSchema(
    executor: Executor, 
    callback: Consumer<AppSearchResult<GetSchemaResponse!>!>
): Unit
```

Retrieves the schema most recently successfully provided to setSchema.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [GetSchemaResponse](GetSchemaResponse.md)!\>!\>: Callback to receive the pending results of schema. This value cannot be `null`. |

### getStorageInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStorageInfo(
    executor: Executor, 
    callback: Consumer<AppSearchResult<StorageInfo!>!>
): Unit
```

Gets the storage info for this AppSearchSession database.

This may take time proportional to the number of documents and may be inefficient to call repeatedly.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [StorageInfo](StorageInfo.md)!\>!\>: Callback to receive the storage info. This value cannot be `null`. |

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

Only blobs committed via commitBlob are available for reading.

The returned OpenBlobForReadResponse must be closed after use to avoid resource leaks. Failing to close it will result in system file descriptor exhaustion.

| Parameters ||
|---|---|
| `handles` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchBlobHandle](AppSearchBlobHandle.md)!\>: The AppSearchBlobHandles that identifies the blobs. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [OpenBlobForReadResponse](OpenBlobForReadResponse.md)!\>!\>: Callback to receive the OpenBlobForReadResponse. This value cannot be `null`. |
| --- | --- |

**See Also**

- setPropertyBlobHandle

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

Once done writing, call commitBlob to commit blob files.

This call will create a empty blob file for each given AppSearchBlobHandle, and a `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` of that blob file will be returned in the OpenBlobForWriteResponse.

If the blob file is already stored in AppSearch and committed. A failed AppSearchResult with error code `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_ALREADY_EXISTS:kotlin.Int` will be associated with the AppSearchBlobHandle.

If the blob file is already stored in AppSearch but not committed. A `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` of that blob file will be returned for continue writing.

For given duplicate AppSearchBlobHandle, the same `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` pointing to the same blob file will be returned.

Pending blob files won't be lost or auto-commit if AppSearchSession closed. Pending blob files will be stored in disk rather than memory. You can re-open AppSearchSession and re-write the pending blob files.

A committed blob file will be considered as an orphan if no GenericDocument references it. Uncommitted pending blob files and orphan blobs files will be cleaned up if they has been created for an extended period (default is 1 week).

The returned OpenBlobForWriteResponse must be closed after use to avoid resource leaks. Failing to close it will result in system file descriptor exhaustion.

| Parameters ||
|---|---|
| `handles` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchBlobHandle](AppSearchBlobHandle.md)!\>: The AppSearchBlobHandles that identifies the blobs. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [OpenBlobForWriteResponse](OpenBlobForWriteResponse.md)!\>!\>: Callback to receive the OpenBlobForWriteResponse. This value cannot be `null`. |
| --- | --- |

**See Also**

- setPropertyBlobHandle

### put

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun put(
    request: PutDocumentsRequest, 
    executor: Executor, 
    callback: BatchResultCallback<String!, Void!>
): Unit
```

Indexes documents into the AppSearchSession database.

Each GenericDocument object must have a `schemaType` field set to an AppSearchSchema type that has been previously registered by calling the setSchema method.

| Parameters ||
|---|---|
| `request` | [PutDocumentsRequest](PutDocumentsRequest.md): containing documents to be indexed. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [BatchResultCallback](BatchResultCallback.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Void](../java.lang/Void.md)!\>: Callback to receive pending result of performing this operation. The keys of the returned AppSearchBatchResult are the IDs of the input documents. The values are either `null` if the corresponding document was successfully indexed, or a failed AppSearchResult otherwise. If an unexpected internal error occurs in the AppSearch service, onSystemError will be invoked with a `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#`. |
| --- | --- |

### remove

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun remove(
    request: RemoveByDocumentIdRequest, 
    executor: Executor, 
    callback: BatchResultCallback<String!, Void!>
): Unit
```

Removes GenericDocument objects by document IDs in a namespace from the AppSearchSession database.

Removed documents will no longer be surfaced by search or getByDocumentId calls.

Once the database crosses the document count or byte usage threshold, removed documents will be deleted from disk.

| Parameters ||
|---|---|
| `request` | [RemoveByDocumentIdRequest](RemoveByDocumentIdRequest.md): RemoveByDocumentIdRequest with IDs in a namespace to remove from the index. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [BatchResultCallback](BatchResultCallback.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Void](../java.lang/Void.md)!\>: Callback to receive the pending result of performing this operation. The keys of the returned AppSearchBatchResult represent the input IDs from the RemoveByDocumentIdRequest object. The values are either `null` on success, or a failed AppSearchResult otherwise. IDs that are not found will return a failed AppSearchResult with a result code of `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_NOT_FOUND:kotlin.Int`. If an unexpected internal error occurs in the AppSearch service, onSystemError will be invoked with a `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#`.. |
| --- | --- |

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

Removes GenericDocuments from the index by Query. Documents will be removed if they match the `queryExpression` in given namespaces and schemaTypes which is set via android.app.appsearch.SearchSpec.Builder#addFilterNamespaces and android.app.appsearch.SearchSpec.Builder#addFilterSchemas.

An empty `queryExpression` matches all documents.

An empty set of namespaces or schemaTypes matches all namespaces or schemaTypes in the current database.

| Parameters ||
|---|---|
| `queryExpression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Query String to search. This value cannot be `null`. |
| `searchSpec` | [SearchSpec](SearchSpec.md): Spec containing schemaTypes, namespaces and query expression indicates how document will be removed. All specific about how to scoring, ordering, snippeting and resulting will be ignored. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [Void](../java.lang/Void.md)!\>!\>: Callback to receive errors resulting from removing the documents. If the operation succeeds, the callback will be invoked with `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the SearchSpec contains a JoinSpec. JoinSpec lets you join docs that are not owned by the caller, so the semantics of failures from this method would be complex. |

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

After this call, the blob data is removed immediately and cannot be recovered. It will not accessible via openBlobForRead. openBlobForWrite could reopen and rewrite it.

This API can be used to remove pending blob data and committed blob data.

Removing a committed blob data that is still referenced by documents will leave those documents with no readable blob content. It is highly recommended to let AppSearch control the blob data's life cycle. AppSearch automatically recycles orphaned and pending blob data. The default time to recycle pending and orphan blob file is 1 week. A blob file will be considered as an orphan if no GenericDocument references it. If you want to remove a committed blob data, you should remove the reference documents first.

| Parameters ||
|---|---|
| `handles` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchBlobHandle](AppSearchBlobHandle.md)!\>: The AppSearchBlobHandles that identifies the blobs. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [RemoveBlobResponse](RemoveBlobResponse.md)!\>!\>: Callback to receive the CommitBlobResponse. This value cannot be `null`. |
| --- | --- |

**See Also**

- setPropertyBlobHandle

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

For each call to reportUsage, AppSearch updates usage count and usage recency metrics for that particular document. These metrics are used for ordering search results by the `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_USAGE_COUNT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_USAGE_LAST_USED_TIMESTAMP:kotlin.Int` ranking strategies.

Reporting usage of a document is optional.

| Parameters ||
|---|---|
| `request` | [ReportUsageRequest](ReportUsageRequest.md): The usage reporting request. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [Void](../java.lang/Void.md)!\>!\>: Callback to receive errors. If the operation succeeds, the callback will be invoked with `null`. |
| --- | --- |

### search

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun search(
    queryExpression: String, 
    searchSpec: SearchSpec
): SearchResults
```

Retrieves documents from the open AppSearchSession that match a given query string and type of search provided.

Query strings can be empty, contain one term with no operators, or contain multiple terms and operators.

For query strings that are empty, all documents that match the SearchSpec will be returned.

For query strings with a single term and no operators, documents that match the provided query string and SearchSpec will be returned.

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
- Property Restricts For queries that require a term to match a specific AppSearchSchema property of a document, a ":" must be included between the property name and the term.

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

- matchScoreExpression matches all documents with scores falling within the specified range. These scores are calculated using the provided score expression, which adheres to the syntax defined in setRankingStrategy.
- "score_expression" is a string value that specifies the score expression.
- "low" and "high" are floating point numbers that specify the score range. The "high" parameter is optional; if not provided, it defaults to positive infinity.

Ex. \`matchScoreExpression("this.documentScore()", 3, 4)\` will return all documents that have document scores from 3 to 4.

SCHEMA_EMBEDDING_PROPERTY_CONFIG: This feature covers the "semanticSearch" and "getEmbeddingParameter" functions in query expressions, which are used for semantic search.

Usage: semanticSearch(getEmbeddingParameter({embedding_index}), {low}, {high}, {metric})

- semanticSearch matches all documents that have at least one embedding vector with a matching model signature (see getModelSignature) and a similarity score within the range specified based on the provided metric.
- getEmbeddingParameter({embedding_index}) retrieves the embedding search passed in android.app.appsearch.SearchSpec.Builder#addEmbeddingParameters based on the index specified, which starts from 0.
- "low" and "high" are floating point numbers that specify the similarity score range. If omitted, they default to negative and positive infinity, respectively.
- "metric" is a string value that specifies how embedding similarities should be calculated. If omitted, it defaults to the metric specified in setDefaultEmbeddingSearchMetricType. Possible values:
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

Ex. \`foo OR getSearchStringParameter(0)\` with getSearchStringParameters returning {"bar OR baz."}. The string "bar OR baz." will be segmented into "bar", "OR", "baz", ".". Punctuation is removed and the segments are normalized to "bar", "or", "baz". This query will be equivalent to \`foo OR (bar AND or AND baz)\`.

Additional search specifications, such as filtering by AppSearchSchema type or adding projection, can be set by calling the corresponding `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec.Builder` setter.

This method is lightweight. The heavy work will be done in getNextPage.

| Parameters ||
|---|---|
| `queryExpression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): query string to search. This value cannot be `null`. |
| `searchSpec` | [SearchSpec](SearchSpec.md): spec for setting document filters, adding projection, setting term match type, etc. This value cannot be `null`. |

| Return ||
|---|---|
| SearchResults | a SearchResults object for retrieved matched documents. This value cannot be `null`. |

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

Retrieves suggested Strings that could be used as `queryExpression` in search API.

The `suggestionQueryExpression` can contain one term with no operators, or contain multiple terms and operators. Operators will be considered as a normal term. Please see the operator examples below. The `suggestionQueryExpression` must end with a valid term, the suggestions are generated based on the last term. If the input `suggestionQueryExpression` doesn't have a valid token, AppSearch will return an empty result list. Please see the invalid examples below.

Example: if there are following documents with content stored in AppSearch.

- document1: "term1"
- document2: "term1 term2"
- document3: "term1 term2 term3"
- document4: "org"

Search suggestions with the single term `suggestionQueryExpression` "t", the suggested results are:

- "term1" - Use it to be queryExpression in search could get 3 SearchResults, which contains document 1, 2 and 3.
- "term2" - Use it to be queryExpression in search could get 2 SearchResults, which contains document 2 and 3.
- "term3" - Use it to be queryExpression in search could get 1 SearchResult, which contains document 3.

Search suggestions with the multiple term `suggestionQueryExpression` "org t", the suggested result will be "org term1" - The last token is completed by the suggested String.

Operators in search are supported.

**NOTE:** Exclusion and Grouped Terms in the last term is not supported.

example: "apple -f": This Api will throw an AppSearchException with `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult#RESULT_INVALID_ARGUMENT:kotlin.Int`.

example: "apple (f)": This Api will return an empty results.

Invalid example: All these input `suggestionQueryExpression` don't have a valid last token, AppSearch will return an empty result list.

- "" - Empty `suggestionQueryExpression`.
- "(f)" - Ending in a closed brackets.
- "f:" - Ending in an operator.
- "f " - Ending in trailing space.

| Parameters ||
|---|---|
| `suggestionQueryExpression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the non empty query string to search suggestions. This value cannot be `null`. |
| `searchSuggestionSpec` | [SearchSuggestionSpec](SearchSuggestionSpec.md): spec for setting document filters. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SearchSuggestionResult](SearchSuggestionResult.md)!\>!\>!\>: Callback to receive the pending result of performing this operation, which is a List of SearchSuggestionResult on success. The returned suggestion Strings are ordered by the number of SearchResult you could get by using that suggestion in search. This value cannot be `null`. |

**See Also**

- search

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

The default setting is blobs will be only visible to the owner package and System. To configure other kinds of sharing, set SchemaVisibilityConfig via SetBlobVisibilityRequest.

| Parameters ||
|---|---|
| `request` | [SetBlobVisibilityRequest](SetBlobVisibilityRequest.md): The request holds visibility settings for all blob namespaces. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [Void](../java.lang/Void.md)!\>!\>: Callback to receive the pending result of performing this operation which resolves to `null` on success. |
| --- | --- |

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

Upon creating an AppSearchSession, setSchema should be called. If the schema needs to be updated, or it has not been previously set, then the provided schema will be saved and persisted to disk. Otherwise, setSchema is handled efficiently as a no-op call.

| Parameters ||
|---|---|
| `request` | [SetSchemaRequest](SetSchemaRequest.md): the schema to set or update the AppSearch database to. This value cannot be `null`. |
| `workExecutor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to schedule heavy client-side background work such as transforming documents. This value cannot be `null`. |
| `callbackExecutor` | [Executor](../java.util.concurrent/Executor.md): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [AppSearchResult](AppSearchResult.md)\< [SetSchemaResponse](SetSchemaResponse.md)!\>!\>: Callback to receive the result of setting the schema. This value cannot be `null`. |
