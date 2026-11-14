# SQLiteClosable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteClosable

Kotlin| [Java](../android/database/sqlite/SQLiteClosable.md) 
| --- | --- |

```
abstract class SQLiteClosable : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.database.sqlite.SQLiteClosable](../android/database/sqlite/SQLiteClosable.md) |

| Known Direct Subclasses [CursorWindow](../android/database/CursorWindow.md), [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md), [SQLiteProgram](../android/database/sqlite/SQLiteProgram.md) |---------------------------------------------------------------------------------------------------------|----------------------------------------------| | [CursorWindow](../android/database/CursorWindow.md) | A buffer containing multiple cursor rows. | | [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md) | Exposes methods to manage a SQLite database. | | [SQLiteProgram](../android/database/sqlite/SQLiteProgram.md) | A base class for compiled SQLite programs. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [SQLiteQuery](../android/database/sqlite/SQLiteQuery.md), [SQLiteStatement](../android/database/sqlite/SQLiteStatement.md) |-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------| | [SQLiteQuery](../android/database/sqlite/SQLiteQuery.md) | Represents a query that reads the resulting rows into a [SQLiteQuery](../android/database/sqlite/SQLiteQuery.md). | | [SQLiteStatement](../android/database/sqlite/SQLiteStatement.md) | Represents a statement that can be executed against a database. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An object created from a SQLiteDatabase that can be closed. This class implements a primitive reference counting scheme for database objects.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteClosable](../android/database/sqlite/SQLiteClosable.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireReference](../android/database/sqlite/SQLiteClosable.md))`()` Acquires a reference to the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/database/sqlite/SQLiteClosable.md))`()` Releases a reference to the object, closing the object if the last reference was released. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReference](../android/database/sqlite/SQLiteClosable.md))`()` Releases a reference to the object, closing the object if the last reference was released. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReferenceFromContainer](../android/database/sqlite/SQLiteClosable.md))`()` Releases a reference to the object that was owned by the container of the object, closing the object if the last reference was released. |

| Protected methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleased](../android/database/sqlite/SQLiteClosable.md))`()` Called when the last reference to the object was released by a call to [releaseReference()](../android/database/sqlite/SQLiteClosable.md))or #close(). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleasedFromContainer](../android/database/sqlite/SQLiteClosable.md))`()` Called when the last reference to the object was released by a call to [releaseReferenceFromContainer()](../android/database/sqlite/SQLiteClosable.md)). |

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

Releases a reference to the object, closing the object if the last reference was released. Calling this method is equivalent to calling [releaseReference](../android/database/sqlite/SQLiteClosable.md)).

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

Called when the last reference to the object was released by a call to [releaseReference()](../android/database/sqlite/SQLiteClosable.md))or #close(). 

### onAllReferencesReleasedFromContainer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onAllReferencesReleasedFromContainer(): Unit
```

**Deprecated:** *Do not use.*

Called when the last reference to the object was released by a call to [releaseReferenceFromContainer()](../android/database/sqlite/SQLiteClosable.md)).
