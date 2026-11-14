# SQLiteClosable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteClosable

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteClosable "View this page in Java") 

```
abstract class SQLiteClosable : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.database.sqlite.SQLiteClosable](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#) |

| Known Direct Subclasses [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow.html#), [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase), [SQLiteProgram](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram) |---------------------------------------------------------------------------------------------------------|----------------------------------------------| | [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow.html#) | A buffer containing multiple cursor rows. | | [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase) | Exposes methods to manage a SQLite database. | | [SQLiteProgram](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram) | A base class for compiled SQLite programs. | |

| Known Indirect Subclasses [SQLiteQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery), [SQLiteStatement](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement) |-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------| | [SQLiteQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery) | Represents a query that reads the resulting rows into a [SQLiteQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery). | | [SQLiteStatement](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement) | Represents a statement that can be executed against a database. | |

An object created from a SQLiteDatabase that can be closed. This class implements a primitive reference counting scheme for database objects.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteClosable](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#SQLiteClosable())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireReference](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#acquireReference())`()` Acquires a reference to the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#close())`()` Releases a reference to the object, closing the object if the last reference was released. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReference](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference())`()` Releases a reference to the object, closing the object if the last reference was released. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReferenceFromContainer](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReferenceFromContainer())`()` Releases a reference to the object that was owned by the container of the object, closing the object if the last reference was released. |

| Protected methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleased](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#onAllReferencesReleased())`()` Called when the last reference to the object was released by a call to [releaseReference()](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference())or #close(). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleasedFromContainer](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#onAllReferencesReleasedFromContainer())`()` Called when the last reference to the object was released by a call to [releaseReferenceFromContainer()](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReferenceFromContainer()). |

## Public constructors

### SQLiteClosable

```
SQLiteClosable()
```

## Public methods

### acquireReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun acquireReference(): Unit
```

Acquires a reference to the object.

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the last reference to the object has already been released. |

### close

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Releases a reference to the object, closing the object if the last reference was released. Calling this method is equivalent to calling [releaseReference](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference()).

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

**See Also**

- <https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference()>
- <https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#onAllReferencesReleased()> 

### releaseReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun releaseReference(): Unit
```

Releases a reference to the object, closing the object if the last reference was released. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#onAllReferencesReleased()> 

### releaseReferenceFromContainer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun releaseReferenceFromContainer(): Unit
```

**Deprecated:** *Do not use.*

Releases a reference to the object that was owned by the container of the object, closing the object if the last reference was released. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#onAllReferencesReleasedFromContainer()>

## Protected methods

### onAllReferencesReleased

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun onAllReferencesReleased(): Unit
```

Called when the last reference to the object was released by a call to [releaseReference()](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference())or #close(). 

### onAllReferencesReleasedFromContainer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onAllReferencesReleasedFromContainer(): Unit
```

**Deprecated:** *Do not use.*

Called when the last reference to the object was released by a call to [releaseReferenceFromContainer()](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReferenceFromContainer()).
