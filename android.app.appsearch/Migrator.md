# Migrator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Migrator

Kotlin| [Java](Migrator.md) 
| --- | --- |

```
abstract class Migrator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.Migrator](Migrator.md) |

A migrator class to translate [GenericDocument](GenericDocument.md) from different version of [AppSearchSchema](AppSearchSchema.md)

Make non-backwards-compatible changes will delete all stored documents in old schema. You can save your documents by setting [Migrator](Migrator.md) via the [android.app.appsearch.SetSchemaRequest.Builder#setMigrator](../android/app/appsearch/SetSchemaRequest.Builder.md))for each type and target version you want to save.

[onDowngrade](Migrator.md))or [onUpgrade](Migrator.md))will be triggered if the version number of the schema stored in AppSearch is different with the version in the request.

If any error or Exception occurred in the [onDowngrade](Migrator.md))or [onUpgrade](Migrator.md)), all the setSchema request will be rejected unless the schema changes are backwards-compatible, and stored documents won't have any observable changes.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------|---|
| [Migrator](Migrator.md))`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [GenericDocument](GenericDocument.md) | [onDowngrade](Migrator.md))`(`currentVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `finalVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `document:` ` [GenericDocument](GenericDocument.md)`)` Migrates [GenericDocument](GenericDocument.md) to an older version of [AppSearchSchema](AppSearchSchema.md). |
| abstract [GenericDocument](GenericDocument.md) | [onUpgrade](Migrator.md))`(`currentVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `finalVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `document:` ` [GenericDocument](GenericDocument.md)`)` Migrates [GenericDocument](GenericDocument.md) to a newer version of [AppSearchSchema](AppSearchSchema.md). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldMigrate](Migrator.md))`(`currentVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `finalVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns`true`if this migrator's source type needs to be migrated to update from currentVersion to finalVersion. |
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

Migrates [GenericDocument](GenericDocument.md) to an older version of [AppSearchSchema](AppSearchSchema.md).

This method will be invoked only if the [SetSchemaRequest](SetSchemaRequest.md) is setting a lower version number than the current [AppSearchSchema](AppSearchSchema.md) saved in AppSearch.

If this [Migrator](Migrator.md) is provided to cover a compatible schema change via [android.app.appsearch.AppSearchSession#setSchema](AppSearchSession.md)), documents under the old version won't be removed unless you use the same document ID.

This method will be invoked on the background worker thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `currentVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current version of the document's schema. |
| `finalVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The final version that documents need to be migrated to. |
| `document` | [GenericDocument](GenericDocument.md):The [GenericDocument](GenericDocument.md) need to be translated to new version. This value cannot be`null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [GenericDocument](GenericDocument.md) | A [GenericDocument](GenericDocument.md) in new version. This value cannot be`null`. |

### onUpgrade

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUpgrade(
    currentVersion: Int, 
    finalVersion: Int, 
    document: GenericDocument
): GenericDocument
```

Migrates [GenericDocument](GenericDocument.md) to a newer version of [AppSearchSchema](AppSearchSchema.md).

This method will be invoked only if the [SetSchemaRequest](SetSchemaRequest.md) is setting a higher version number than the current [AppSearchSchema](AppSearchSchema.md) saved in AppSearch.

If this [Migrator](Migrator.md) is provided to cover a compatible schema change via [android.app.appsearch.AppSearchSession#setSchema](AppSearchSession.md)), documents under the old version won't be removed unless you use the same document ID.

This method will be invoked on the background worker thread provided via [android.app.appsearch.AppSearchSession#setSchema](AppSearchSession.md)). 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `currentVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current version of the document's schema. |
| `finalVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The final version that documents need to be migrated to. |
| `document` | [GenericDocument](GenericDocument.md):The [GenericDocument](GenericDocument.md) need to be translated to new version. This value cannot be`null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [GenericDocument](GenericDocument.md) | A [GenericDocument](GenericDocument.md) in new version. This value cannot be`null`. |

### shouldMigrate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun shouldMigrate(
    currentVersion: Int, 
    finalVersion: Int
): Boolean
```

Returns`true`if this migrator's source type needs to be migrated to update from currentVersion to finalVersion.

Migration won't be triggered if currentVersion is equal to finalVersion even if [shouldMigrate](Migrator.md))return true;
