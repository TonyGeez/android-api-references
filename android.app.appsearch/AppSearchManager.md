# AppSearchManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppSearchManager

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/AppSearchManager "View this page in Java") 
| --- | --- |

```
open class AppSearchManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.AppSearchManager](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager#) |

Provides access to the centralized AppSearch index maintained by the system.

AppSearch is an offline, on-device search library for managing structured data featuring:

- APIs to index and retrieve data via full-text search.
- An API for applications to explicitly grant read-access permission of their data to other applications.**See: [android.app.appsearch.SetSchemaRequest.Builder#setSchemaTypeVisibilityForPackage](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#setSchemaTypeVisibilityForPackage(kotlin.String,%20kotlin.Boolean,%20android.app.appsearch.PackageIdentifier))**
- An API for applications to opt into or out of having their data displayed on System UI surfaces by the System-designated global querier.**See: [android.app.appsearch.SetSchemaRequest.Builder#setSchemaTypeDisplayedBySystem](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#setSchemaTypeDisplayedBySystem(kotlin.String,%20kotlin.Boolean))**

Applications create a database by opening an [AppSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession).

Example: 

```kotlin
AppSearchManager appSearchManager = context.getSystemService(AppSearchManager.class);
 
  AppSearchManager.SearchContext searchContext = new AppSearchManager.SearchContext.Builder().
     setDatabaseName(dbName).build());
  appSearchManager.createSearchSession(searchContext, mExecutor, appSearchSessionResult -> {
       mAppSearchSession = appSearchSessionResult.getResultValue();
  });
```

After opening the session, a schema must be set in order to define the organizational structure of data. The schema is set by calling [AppSearchSession.setSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)). The schema is composed of a collection of [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) objects, each of which defines a unique type of data.

Example: 

```kotlin
AppSearchSchema emailSchemaType = new AppSearchSchema.Builder("Email")
      .addProperty(new StringPropertyConfig.Builder("subject")
         .setCardinality(PropertyConfig.CARDINALITY_OPTIONAL)
         .setIndexingType(PropertyConfig.INDEXING_TYPE_PREFIXES)
         .setTokenizerType(PropertyConfig.TOKENIZER_TYPE_PLAIN)
     .build()
  ).build();
 
  SetSchemaRequest request = new SetSchemaRequest.Builder().addSchema(emailSchemaType).build();
  mAppSearchSession.set(request, mExecutor, appSearchResult -> {
       if (appSearchResult.isSuccess()) {
            // Schema has been successfully set.
       }
  });
```

The basic unit of data in AppSearch is represented as a [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) object, containing an ID, namespace, time-to-live, score, and properties. A namespace organizes a logical group of documents. For example, a namespace can be created to group documents on a per-account basis. An ID identifies a single document within a namespace. The combination of namespace and ID uniquely identifies a [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) in the database.

Once the schema has been set, [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) objects can be put into the database and indexed by calling [AppSearchSession.put](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#put(android.app.appsearch.PutDocumentsRequest,%20java.util.concurrent.Executor,%20android.app.appsearch.BatchResultCallback)).

Example: 

```kotlin
// Although for this example we use GenericDocument directly, we recommend extending
  // GenericDocument to create specific types (i.e. Email) with specific setters/getters.
  GenericDocument email = new GenericDocument.Builder<>(NAMESPACE, ID, EMAIL_SCHEMA_TYPE)
      .setPropertyString("subject", EMAIL_SUBJECT)
      .setScore(EMAIL_SCORE)
      .build();
 
  PutDocumentsRequest request = new PutDocumentsRequest.Builder().addGenericDocuments(email)
      .build();
  mAppSearchSession.put(request, mExecutor, appSearchBatchResult -> {
       if (appSearchBatchResult.isSuccess()) {
            // All documents have been successfully indexed.
       }
  });
```

Searching within the database is done by calling [AppSearchSession.search](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec))and providing the query string to search for, as well as a [SearchSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec).

Alternatively, [AppSearchSession.getByDocumentId](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#getByDocumentId(android.app.appsearch.GetByDocumentIdRequest,%20java.util.concurrent.Executor,%20android.app.appsearch.BatchResultCallback))can be called to retrieve documents by namespace and ID.

Document removal is done either by time-to-live expiration, or explicitly calling a remove operation. Remove operations can be done by namespace and ID via [android.app.appsearch.AppSearchSession#remove(android.app.appsearch.RemoveByDocumentIdRequest,java.util.concurrent.Executor,android.app.appsearch.BatchResultCallback)](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#remove(android.app.appsearch.RemoveByDocumentIdRequest,%20java.util.concurrent.Executor,%20android.app.appsearch.BatchResultCallback)), or by query via [AppSearchSession.remove(String, SearchSpec, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#remove(kotlin.String,%20android.app.appsearch.SearchSpec,%20java.util.concurrent.Executor,%20java.util.function.Consumer)).

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [SearchContext](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.SearchContext) Contains information about how to create the search session. |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createEnterpriseGlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager#createEnterpriseGlobalSearchSession(java.util.concurrent.Executor,%20java.util.function.Consumer))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)< [EnterpriseGlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/EnterpriseGlobalSearchSession)!>!>`)` Creates a new [EnterpriseGlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/EnterpriseGlobalSearchSession) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createGlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager#createGlobalSearchSession(java.util.concurrent.Executor,%20java.util.function.Consumer))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)< [GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession)!>!>`)` Creates a new [GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager#createSearchSession(android.app.appsearch.AppSearchManager.SearchContext,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`searchContext:` ` [AppSearchManager.SearchContext](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.SearchContext)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)< [AppSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession)!>!>`)` Creates a new [AppSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession). |
| --- | --- |

## Public methods

### createEnterpriseGlobalSearchSession

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions) 

```
open fun createEnterpriseGlobalSearchSession(
    executor: Executor, 
    callback: Consumer<AppSearchResult<EnterpriseGlobalSearchSession!>!>
): Unit
```

Creates a new [EnterpriseGlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/EnterpriseGlobalSearchSession)

EnterpriseGlobalSearchSession queries data from the user's work profile, allowing apps running on the personal profile to access a limited subset of work profile data. Enterprise access must be explicitly enabled on schemas, and schemas may also specify additional permissions required for enterprise access.

This process requires an AppSearch native indexing file system. If it's not created, the initialization process will create one under the user's credential encrypted directory.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [EnterpriseGlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/EnterpriseGlobalSearchSession)!\>!\>:The [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [EnterpriseGlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/EnterpriseGlobalSearchSession)\> of performing this operation. Or a [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) with failure reason code and error information. This value cannot be`null`. |

### createGlobalSearchSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createGlobalSearchSession(
    executor: Executor, 
    callback: Consumer<AppSearchResult<GlobalSearchSession!>!>
): Unit
```

Creates a new [GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession).

This process requires an AppSearch native indexing file system. If it's not created, the initialization process will create one under the user's credential encrypted directory.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession)!\>!\>:The [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [GlobalSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession)\> of performing this operation. Or a [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) with failure reason code and error information. This value cannot be`null`. |

### createSearchSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSearchSession(
    searchContext: AppSearchManager.SearchContext, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<AppSearchSession!>!>
): Unit
```

Creates a new [AppSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession).

This process requires an AppSearch native indexing file system. If it's not created, the initialization process will create one under the user's credential encrypted directory.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `searchContext` | [AppSearchManager.SearchContext](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.SearchContext):The [SearchContext](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.SearchContext) contains all information to create a new [AppSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession) This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [AppSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession)!\>!\>:The [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\< [AppSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession)\> of performing this operation. Or a [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) with failure reason code and error information. This value cannot be`null`. |
| --- | --- |
