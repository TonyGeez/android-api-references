# Migrator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Migrator

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/Migrator "View this page in Java") 
| --- | --- |

```
abstract class Migrator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.Migrator](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#) |

A migrator class to translate [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) from different version of [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema)

Make non-backwards-compatible changes will delete all stored documents in old schema. You can save your documents by setting [Migrator](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#) via the [android.app.appsearch.SetSchemaRequest.Builder#setMigrator](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#setMigrator(kotlin.String,%20android.app.appsearch.Migrator))for each type and target version you want to save.

[onDowngrade](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#onDowngrade(kotlin.Int,%20kotlin.Int,%20android.app.appsearch.GenericDocument))or [onUpgrade](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#onUpgrade(kotlin.Int,%20kotlin.Int,%20android.app.appsearch.GenericDocument))will be triggered if the version number of the schema stored in AppSearch is different with the version in the request.

If any error or Exception occurred in the [onDowngrade](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#onDowngrade(kotlin.Int,%20kotlin.Int,%20android.app.appsearch.GenericDocument))or [onUpgrade](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#onUpgrade(kotlin.Int,%20kotlin.Int,%20android.app.appsearch.GenericDocument)), all the setSchema request will be rejected unless the schema changes are backwards-compatible, and stored documents won't have any observable changes.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------|---|
| [Migrator](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#Migrator())`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) | [onDowngrade](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#onDowngrade(kotlin.Int,%20kotlin.Int,%20android.app.appsearch.GenericDocument))`(`currentVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `finalVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `document:` ` [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument)`)` Migrates [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) to an older version of [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema). |
| abstract [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) | [onUpgrade](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#onUpgrade(kotlin.Int,%20kotlin.Int,%20android.app.appsearch.GenericDocument))`(`currentVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `finalVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `document:` ` [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument)`)` Migrates [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) to a newer version of [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldMigrate](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#shouldMigrate(kotlin.Int,%20kotlin.Int))`(`currentVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `finalVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns`true`if this migrator's source type needs to be migrated to update from currentVersion to finalVersion. |
| --- | --- |

## Public constructors

### Migrator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Migrator()
```

## Public methods

### onDowngrade

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDowngrade(
    currentVersion: Int, 
    finalVersion: Int, 
    document: GenericDocument
): GenericDocument
```

Migrates [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) to an older version of [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema).

This method will be invoked only if the [SetSchemaRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest) is setting a lower version number than the current [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) saved in AppSearch.

If this [Migrator](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#) is provided to cover a compatible schema change via [android.app.appsearch.AppSearchSession#setSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)), documents under the old version won't be removed unless you use the same document ID.

This method will be invoked on the background worker thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `currentVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current version of the document's schema. |
| `finalVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The final version that documents need to be migrated to. |
| `document` | [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument):The [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) need to be translated to new version. This value cannot be`null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) | A [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) in new version. This value cannot be`null`. |

### onUpgrade

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUpgrade(
    currentVersion: Int, 
    finalVersion: Int, 
    document: GenericDocument
): GenericDocument
```

Migrates [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) to a newer version of [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema).

This method will be invoked only if the [SetSchemaRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest) is setting a higher version number than the current [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) saved in AppSearch.

If this [Migrator](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#) is provided to cover a compatible schema change via [android.app.appsearch.AppSearchSession#setSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)), documents under the old version won't be removed unless you use the same document ID.

This method will be invoked on the background worker thread provided via [android.app.appsearch.AppSearchSession#setSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)). 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `currentVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current version of the document's schema. |
| `finalVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The final version that documents need to be migrated to. |
| `document` | [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument):The [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) need to be translated to new version. This value cannot be`null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) | A [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) in new version. This value cannot be`null`. |

### shouldMigrate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun shouldMigrate(
    currentVersion: Int, 
    finalVersion: Int
): Boolean
```

Returns`true`if this migrator's source type needs to be migrated to update from currentVersion to finalVersion.

Migration won't be triggered if currentVersion is equal to finalVersion even if [shouldMigrate](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator#shouldMigrate(kotlin.Int,%20kotlin.Int))return true;
