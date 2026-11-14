# RestoreObserver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RestoreObserver

Kotlin| [Java](https://developer.android.com/reference/android/app/backup/RestoreObserver "View this page in Java") 
| --- | --- |

```
abstract class RestoreObserver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.backup.RestoreObserver](https://developer.android.com/reference/kotlin/android/app/backup/RestoreObserver#) |

Callback class for receiving progress reports during a restore operation. These methods will all be called on your application's main thread.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------|---|
| [RestoreObserver](https://developer.android.com/reference/kotlin/android/app/backup/RestoreObserver#RestoreObserver())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUpdate](https://developer.android.com/reference/kotlin/android/app/backup/RestoreObserver#onUpdate(kotlin.Int,%20kotlin.String))`(`nowBeingRestored:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `currentPackage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` An indication of which package is being restored currently, out of the total number provided in the [restoreStarting(int)](https://developer.android.com/reference/kotlin/android/app/backup/RestoreObserver#restoreStarting(kotlin.Int))callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreFinished](https://developer.android.com/reference/kotlin/android/app/backup/RestoreObserver#restoreFinished(kotlin.Int))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The restore process has completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreStarting](https://developer.android.com/reference/kotlin/android/app/backup/RestoreObserver#restoreStarting(kotlin.Int))`(`numPackages:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The restore operation has begun. |
| --- | --- |

## Public constructors

### RestoreObserver

```
RestoreObserver()
```

## Public methods

### onUpdate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onUpdate(
    nowBeingRestored: Int, 
    currentPackage: String!
): Unit
```

An indication of which package is being restored currently, out of the total number provided in the [restoreStarting(int)](https://developer.android.com/reference/kotlin/android/app/backup/RestoreObserver#restoreStarting(kotlin.Int))callback. This method is not guaranteed to be called: if the transport is unable to obtain data for one or more of the requested packages, no onUpdate() call will occur for those packages.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `nowBeingRestored` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index, between 1 and the numPackages parameter to the [restoreStarting(int)](https://developer.android.com/reference/kotlin/android/app/backup/RestoreObserver#restoreStarting(kotlin.Int))callback, of the package now being restored. This may be non-monotonic; it is intended purely as a rough indication of the backup manager's progress through the overall restore process. |
| `currentPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the package now being restored. |

### restoreFinished

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreFinished(error: Int): Unit
```

The restore process has completed. This method will always be called, even if no individual package restore operations were attempted.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Zero on success; a nonzero error code if the restore operation as a whole failed. |

### restoreStarting

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreStarting(numPackages: Int): Unit
```

The restore operation has begun.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `numPackages` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The total number of packages being processed in this restore operation. |
