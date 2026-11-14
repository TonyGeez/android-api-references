# RestoreObserver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RestoreObserver

Kotlin| [Java](RestoreObserver.md) 
| --- | --- |

```
abstract class RestoreObserver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.backup.RestoreObserver](RestoreObserver.md) |

Callback class for receiving progress reports during a restore operation. These methods will all be called on your application's main thread.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------|---|
| [RestoreObserver](RestoreObserver.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUpdate](RestoreObserver.md))`(`nowBeingRestored:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `currentPackage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` An indication of which package is being restored currently, out of the total number provided in the [restoreStarting(int)](RestoreObserver.md))callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreFinished](RestoreObserver.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The restore process has completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreStarting](RestoreObserver.md))`(`numPackages:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The restore operation has begun. |
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

An indication of which package is being restored currently, out of the total number provided in the [restoreStarting(int)](RestoreObserver.md))callback. This method is not guaranteed to be called: if the transport is unable to obtain data for one or more of the requested packages, no onUpdate() call will occur for those packages.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `nowBeingRestored` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index, between 1 and the numPackages parameter to the [restoreStarting(int)](RestoreObserver.md))callback, of the package now being restored. This may be non-monotonic; it is intended purely as a rough indication of the backup manager's progress through the overall restore process. |
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
