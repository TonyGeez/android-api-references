# AppSearchManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppSearchManager

Kotlin| [Java](../android/app/appsearch/AppSearchManager.md) 
| --- | --- |

```
open class AppSearchManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.AppSearchManager](../android/app/appsearch/AppSearchManager.md) |

Provides access to the centralized AppSearch index maintained by the system.

AppSearch is an offline, on-device search library for managing structured data featuring:

- APIs to index and retrieve data via full-text search.
- An API for applications to explicitly grant read-access permission of their data to other applications.**See: [android.app.appsearch.SetSchemaRequest.Builder#setSchemaTypeVisibilityForPackage](../android/app/appsearch/SetSchemaRequest.Builder.md))**
- An API for applications to opt into or out of having their data displayed on System UI surfaces by the System-designated global querier.**See: [android.app.appsearch.SetSchemaRequest.Builder#setSchemaTypeDisplayedBySystem](../android/app/appsearch/SetSchemaRequest.Builder.md))**

Applications create a database by opening an [AppSearchSession](../android/app/appsearch/AppSearchSession.md).

Example: 

```kotlin
AppSearchManager appSearchManager = context.getSystemService(AppSearchManager.class);
 
  AppSearchManager.SearchContext searchContext = new AppSearchManager.SearchContext.Builder().
     setDatabaseName(dbName).build());
  appSearchManager.createSearchSession(searchContext, mExecutor, appSearchSessionResult -> {
       mAppSearchSession = appSearchSessionResult.getResultValue();
  });
```

After opening the session, a schema must be set in order to define the organizational structure of data. The schema is set by calling [AppSearchSession.setSchema](../android/app/appsearch/AppSearchSession.md)). The schema is composed of a collection of [AppSearchSchema](../android/app/appsearch/AppSearchSchema.md) objects, each of which defines a unique type of data.

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

The basic unit of data in AppSearch is represented as a [GenericDocument](../android/app/appsearch/GenericDocument.md) object, containing an ID, namespace, time-to-live, score, and properties. A namespace organizes a logical group of documents. For example, a namespace can be created to group documents on a per-account basis. An ID identifies a single document within a namespace. The combination of namespace and ID uniquely identifies a [GenericDocument](../android/app/appsearch/GenericDocument.md) in the database.

Once the schema has been set, [GenericDocument](../android/app/appsearch/GenericDocument.md) objects can be put into the database and indexed by calling [AppSearchSession.put](../android/app/appsearch/AppSearchSession.md)).

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

Searching within the database is done by calling [AppSearchSession.search](../android/app/appsearch/AppSearchSession.md))and providing the query string to search for, as well as a [SearchSpec](../android/app/appsearch/SearchSpec.md).

Alternatively, [AppSearchSession.getByDocumentId](../android/app/appsearch/AppSearchSession.md))can be called to retrieve documents by namespace and ID.

Document removal is done either by time-to-live expiration, or explicitly calling a remove operation. Remove operations can be done by namespace and ID via [android.app.appsearch.AppSearchSession#remove(android.app.appsearch.RemoveByDocumentIdRequest,java.util.concurrent.Executor,android.app.appsearch.BatchResultCallback)](../android/app/appsearch/AppSearchSession.md)), or by query via [AppSearchSession.remove(String, SearchSpec, Executor, Consumer)](../android/app/appsearch/AppSearchSession.md)).

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [SearchContext](../android/app/appsearch/AppSearchManager.SearchContext.md) Contains information about how to create the search session. |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createEnterpriseGlobalSearchSession](../android/app/appsearch/AppSearchManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [Consumer](../java/util/function/Consumer.md)< [AppSearchResult](../android/app/appsearch/AppSearchResult.md)< [EnterpriseGlobalSearchSession](../android/app/appsearch/EnterpriseGlobalSearchSession.md)!>!>`)` Creates a new [EnterpriseGlobalSearchSession](../android/app/appsearch/EnterpriseGlobalSearchSession.md) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createGlobalSearchSession](../android/app/appsearch/AppSearchManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [Consumer](../java/util/function/Consumer.md)< [AppSearchResult](../android/app/appsearch/AppSearchResult.md)< [GlobalSearchSession](../android/app/appsearch/GlobalSearchSession.md)!>!>`)` Creates a new [GlobalSearchSession](../android/app/appsearch/GlobalSearchSession.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createSearchSession](../android/app/appsearch/AppSearchManager.md))`(`searchContext:` ` [AppSearchManager.SearchContext](../android/app/appsearch/AppSearchManager.SearchContext.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [Consumer](../java/util/function/Consumer.md)< [AppSearchResult](../android/app/appsearch/AppSearchResult.md)< [AppSearchSession](../android/app/appsearch/AppSearchSession.md)!>!>`)` Creates a new [AppSearchSession](../android/app/appsearch/AppSearchSession.md). |
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

Creates a new [EnterpriseGlobalSearchSession](../android/app/appsearch/EnterpriseGlobalSearchSession.md)

EnterpriseGlobalSearchSession queries data from the user's work profile, allowing apps running on the personal profile to access a limited subset of work profile data. Enterprise access must be explicitly enabled on schemas, and schemas may also specify additional permissions required for enterprise access.

This process requires an AppSearch native indexing file system. If it's not created, the initialization process will create one under the user's credential encrypted directory.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java/util/function/Consumer.md)\< [AppSearchResult](../android/app/appsearch/AppSearchResult.md)\< [EnterpriseGlobalSearchSession](../android/app/appsearch/EnterpriseGlobalSearchSession.md)!\>!\>:The [AppSearchResult](../android/app/appsearch/AppSearchResult.md)\< [EnterpriseGlobalSearchSession](../android/app/appsearch/EnterpriseGlobalSearchSession.md)\> of performing this operation. Or a [AppSearchResult](../android/app/appsearch/AppSearchResult.md) with failure reason code and error information. This value cannot be`null`. |

### createGlobalSearchSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createGlobalSearchSession(
    executor: Executor, 
    callback: Consumer<AppSearchResult<GlobalSearchSession!>!>
): Unit
```

Creates a new [GlobalSearchSession](../android/app/appsearch/GlobalSearchSession.md).

This process requires an AppSearch native indexing file system. If it's not created, the initialization process will create one under the user's credential encrypted directory.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java/util/function/Consumer.md)\< [AppSearchResult](../android/app/appsearch/AppSearchResult.md)\< [GlobalSearchSession](../android/app/appsearch/GlobalSearchSession.md)!\>!\>:The [AppSearchResult](../android/app/appsearch/AppSearchResult.md)\< [GlobalSearchSession](../android/app/appsearch/GlobalSearchSession.md)\> of performing this operation. Or a [AppSearchResult](../android/app/appsearch/AppSearchResult.md) with failure reason code and error information. This value cannot be`null`. |

### createSearchSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSearchSession(
    searchContext: AppSearchManager.SearchContext, 
    executor: Executor, 
    callback: Consumer<AppSearchResult<AppSearchSession!>!>
): Unit
```

Creates a new [AppSearchSession](../android/app/appsearch/AppSearchSession.md).

This process requires an AppSearch native indexing file system. If it's not created, the initialization process will create one under the user's credential encrypted directory.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `searchContext` | [AppSearchManager.SearchContext](../android/app/appsearch/AppSearchManager.SearchContext.md):The [SearchContext](../android/app/appsearch/AppSearchManager.SearchContext.md) contains all information to create a new [AppSearchSession](../android/app/appsearch/AppSearchSession.md) This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):Executor on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java/util/function/Consumer.md)\< [AppSearchResult](../android/app/appsearch/AppSearchResult.md)\< [AppSearchSession](../android/app/appsearch/AppSearchSession.md)!\>!\>:The [AppSearchResult](../android/app/appsearch/AppSearchResult.md)\< [AppSearchSession](../android/app/appsearch/AppSearchSession.md)\> of performing this operation. Or a [AppSearchResult](../android/app/appsearch/AppSearchResult.md) with failure reason code and error information. This value cannot be`null`. |
| --- | --- |
