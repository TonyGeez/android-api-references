# SQLiteException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteException

Kotlin| [Java](SQLiteException.md) 
| --- | --- |

```
open class SQLiteException : SQLException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](../android.database/SQLException.md) ||
| | | | | ↳ | [android.database.sqlite.SQLiteException](SQLiteException.md) |

| Known Direct Subclasses [SQLiteAbortException](SQLiteAbortException.md), [SQLiteAccessPermException](SQLiteAccessPermException.md), [SQLiteBindOrColumnIndexOutOfRangeException](SQLiteBindOrColumnIndexOutOfRangeException.md), [SQLiteBlobTooBigException](SQLiteBlobTooBigException.md), [SQLiteCantOpenDatabaseException](SQLiteCantOpenDatabaseException.md), [SQLiteConstraintException](SQLiteConstraintException.md), [SQLiteDatabaseCorruptException](SQLiteDatabaseCorruptException.md), [SQLiteDatabaseLockedException](SQLiteDatabaseLockedException.md), [SQLiteDatatypeMismatchException](SQLiteDatatypeMismatchException.md), [SQLiteDiskIOException](SQLiteDiskIOException.md), [SQLiteDoneException](SQLiteDoneException.md), [SQLiteFullException](SQLiteFullException.md), and 4 others. |-----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------| | [SQLiteAbortException](SQLiteAbortException.md) | An exception that indicates that the SQLite program was aborted. | | [SQLiteAccessPermException](SQLiteAccessPermException.md) | This exception class is used when sqlite can't access the database file due to lack of permissions on the file. | | [SQLiteBindOrColumnIndexOutOfRangeException](SQLiteBindOrColumnIndexOutOfRangeException.md) | Thrown if the bind or column parameter index is out of range. | | [SQLiteBlobTooBigException](SQLiteBlobTooBigException.md) | <br /> | | [SQLiteCantOpenDatabaseException](SQLiteCantOpenDatabaseException.md) | <br /> | | [SQLiteConstraintException](SQLiteConstraintException.md) | An exception that indicates that an integrity constraint was violated. | | [SQLiteDatabaseCorruptException](SQLiteDatabaseCorruptException.md) | An exception that indicates that the SQLite database file is corrupt. | | [SQLiteDatabaseLockedException](SQLiteDatabaseLockedException.md) | Thrown if the database engine was unable to acquire the database locks it needs to do its job. | | [SQLiteDatatypeMismatchException](SQLiteDatatypeMismatchException.md) | <br /> | | [SQLiteDiskIOException](SQLiteDiskIOException.md) | Indicates that an IO error occurred while accessing the SQLite database file. | | [SQLiteDoneException](SQLiteDoneException.md) | An exception that indicates that the SQLite program is done. | | [SQLiteFullException](SQLiteFullException.md) | An exception that indicates that the SQLite database is full. | | [SQLiteMisuseException](SQLiteMisuseException.md) | This error can occur if the application creates a SQLiteStatement object and allows multiple threads in the application use it at the same time. | | [SQLiteOutOfMemoryException](SQLiteOutOfMemoryException.md) | <br /> | | [SQLiteReadOnlyDatabaseException](SQLiteReadOnlyDatabaseException.md) | <br /> | | [SQLiteTableLockedException](SQLiteTableLockedException.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A SQLite exception that indicates there was an error with SQL parsing or execution.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteException](SQLiteException.md))`()` <br /> |
| [SQLiteException](SQLiteException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [SQLiteException](SQLiteException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

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
