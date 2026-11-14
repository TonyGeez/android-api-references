# SQLiteException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteException

Kotlin| [Java](../android/database/sqlite/SQLiteException.md) 
| --- | --- |

```
open class SQLiteException : SQLException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](../android/database/SQLException.md) ||
| | | | | ↳ | [android.database.sqlite.SQLiteException](../android/database/sqlite/SQLiteException.md) |

| Known Direct Subclasses [SQLiteAbortException](../android/database/sqlite/SQLiteAbortException.md), [SQLiteAccessPermException](../android/database/sqlite/SQLiteAccessPermException.md), [SQLiteBindOrColumnIndexOutOfRangeException](../android/database/sqlite/SQLiteBindOrColumnIndexOutOfRangeException.md), [SQLiteBlobTooBigException](../android/database/sqlite/SQLiteBlobTooBigException.md), [SQLiteCantOpenDatabaseException](../android/database/sqlite/SQLiteCantOpenDatabaseException.md), [SQLiteConstraintException](../android/database/sqlite/SQLiteConstraintException.md), [SQLiteDatabaseCorruptException](../android/database/sqlite/SQLiteDatabaseCorruptException.md), [SQLiteDatabaseLockedException](../android/database/sqlite/SQLiteDatabaseLockedException.md), [SQLiteDatatypeMismatchException](../android/database/sqlite/SQLiteDatatypeMismatchException.md), [SQLiteDiskIOException](../android/database/sqlite/SQLiteDiskIOException.md), [SQLiteDoneException](../android/database/sqlite/SQLiteDoneException.md), [SQLiteFullException](../android/database/sqlite/SQLiteFullException.md), and 4 others. |-----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------| | [SQLiteAbortException](../android/database/sqlite/SQLiteAbortException.md) | An exception that indicates that the SQLite program was aborted. | | [SQLiteAccessPermException](../android/database/sqlite/SQLiteAccessPermException.md) | This exception class is used when sqlite can't access the database file due to lack of permissions on the file. | | [SQLiteBindOrColumnIndexOutOfRangeException](../android/database/sqlite/SQLiteBindOrColumnIndexOutOfRangeException.md) | Thrown if the bind or column parameter index is out of range. | | [SQLiteBlobTooBigException](../android/database/sqlite/SQLiteBlobTooBigException.md) | <br /> | | [SQLiteCantOpenDatabaseException](../android/database/sqlite/SQLiteCantOpenDatabaseException.md) | <br /> | | [SQLiteConstraintException](../android/database/sqlite/SQLiteConstraintException.md) | An exception that indicates that an integrity constraint was violated. | | [SQLiteDatabaseCorruptException](../android/database/sqlite/SQLiteDatabaseCorruptException.md) | An exception that indicates that the SQLite database file is corrupt. | | [SQLiteDatabaseLockedException](../android/database/sqlite/SQLiteDatabaseLockedException.md) | Thrown if the database engine was unable to acquire the database locks it needs to do its job. | | [SQLiteDatatypeMismatchException](../android/database/sqlite/SQLiteDatatypeMismatchException.md) | <br /> | | [SQLiteDiskIOException](../android/database/sqlite/SQLiteDiskIOException.md) | Indicates that an IO error occurred while accessing the SQLite database file. | | [SQLiteDoneException](../android/database/sqlite/SQLiteDoneException.md) | An exception that indicates that the SQLite program is done. | | [SQLiteFullException](../android/database/sqlite/SQLiteFullException.md) | An exception that indicates that the SQLite database is full. | | [SQLiteMisuseException](../android/database/sqlite/SQLiteMisuseException.md) | This error can occur if the application creates a SQLiteStatement object and allows multiple threads in the application use it at the same time. | | [SQLiteOutOfMemoryException](../android/database/sqlite/SQLiteOutOfMemoryException.md) | <br /> | | [SQLiteReadOnlyDatabaseException](../android/database/sqlite/SQLiteReadOnlyDatabaseException.md) | <br /> | | [SQLiteTableLockedException](../android/database/sqlite/SQLiteTableLockedException.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A SQLite exception that indicates there was an error with SQL parsing or execution.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteException](../android/database/sqlite/SQLiteException.md))`()` <br /> |
| [SQLiteException](../android/database/sqlite/SQLiteException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [SQLiteException](../android/database/sqlite/SQLiteException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

## Public constructors

### SQLiteException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteException()
```  

### SQLiteException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteException(error: String!)
```  

### SQLiteException

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteException(
    error: String!, 
    cause: Throwable!)
```
