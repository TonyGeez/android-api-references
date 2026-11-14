# SQLiteException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteException

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteException "View this page in Java") 
| --- | --- |

```
open class SQLiteException : SQLException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](https://developer.android.com/reference/kotlin/android/database/SQLException.html#) ||
| | | | | ↳ | [android.database.sqlite.SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException#) |

| Known Direct Subclasses [SQLiteAbortException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAbortException), [SQLiteAccessPermException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAccessPermException), [SQLiteBindOrColumnIndexOutOfRangeException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteBindOrColumnIndexOutOfRangeException), [SQLiteBlobTooBigException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteBlobTooBigException), [SQLiteCantOpenDatabaseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCantOpenDatabaseException), [SQLiteConstraintException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteConstraintException), [SQLiteDatabaseCorruptException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabaseCorruptException), [SQLiteDatabaseLockedException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabaseLockedException), [SQLiteDatatypeMismatchException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatatypeMismatchException), [SQLiteDiskIOException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDiskIOException), [SQLiteDoneException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDoneException), [SQLiteFullException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteFullException), and 4 others. |-----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------| | [SQLiteAbortException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAbortException) | An exception that indicates that the SQLite program was aborted. | | [SQLiteAccessPermException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAccessPermException) | This exception class is used when sqlite can't access the database file due to lack of permissions on the file. | | [SQLiteBindOrColumnIndexOutOfRangeException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteBindOrColumnIndexOutOfRangeException) | Thrown if the bind or column parameter index is out of range. | | [SQLiteBlobTooBigException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteBlobTooBigException) | <br /> | | [SQLiteCantOpenDatabaseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCantOpenDatabaseException) | <br /> | | [SQLiteConstraintException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteConstraintException) | An exception that indicates that an integrity constraint was violated. | | [SQLiteDatabaseCorruptException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabaseCorruptException) | An exception that indicates that the SQLite database file is corrupt. | | [SQLiteDatabaseLockedException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabaseLockedException) | Thrown if the database engine was unable to acquire the database locks it needs to do its job. | | [SQLiteDatatypeMismatchException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatatypeMismatchException) | <br /> | | [SQLiteDiskIOException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDiskIOException) | Indicates that an IO error occurred while accessing the SQLite database file. | | [SQLiteDoneException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDoneException) | An exception that indicates that the SQLite program is done. | | [SQLiteFullException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteFullException) | An exception that indicates that the SQLite database is full. | | [SQLiteMisuseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteMisuseException) | This error can occur if the application creates a SQLiteStatement object and allows multiple threads in the application use it at the same time. | | [SQLiteOutOfMemoryException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOutOfMemoryException) | <br /> | | [SQLiteReadOnlyDatabaseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteReadOnlyDatabaseException) | <br /> | | [SQLiteTableLockedException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTableLockedException) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A SQLite exception that indicates there was an error with SQL parsing or execution.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException#SQLiteException())`()` <br /> |
| [SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException#SQLiteException(kotlin.String))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException#SQLiteException(kotlin.String,%20kotlin.Throwable))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

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
