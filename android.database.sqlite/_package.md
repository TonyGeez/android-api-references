# android.database.sqlite

# android.database.sqlite

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [SQLiteCursorDriver](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursorDriver) | A driver for SQLiteCursors that is used to create them and gets notified by the cursors it creates on significant events in their lifetimes. |
| --- | --- |
| [CursorFactory](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory) | Used to allow returning sub-classes of [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) when calling query. |
| [SQLiteTransactionListener](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTransactionListener) | A listener for transaction events. |

## Classes

| [SQLiteClosable](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable) | An object created from a SQLiteDatabase that can be closed. |
| --- | --- |
| [SQLiteCursor](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor) | A Cursor implementation that exposes results from a query on a [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase). |
| [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase) | Exposes methods to manage a SQLite database. |
| [SQLiteOpenHelper](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper) | A helper class to manage database creation and version management. |
| --- | --- |
| [SQLiteProgram](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram) | A base class for compiled SQLite programs. |
| [SQLiteQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery) | Represents a query that reads the resulting rows into a [SQLiteQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery). |
| [SQLiteQueryBuilder](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder) | This is a convenience class that helps build SQL queries to be sent to [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase) objects. |
| --- | --- |
| [SQLiteRawStatement](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement) | A represents a SQLite prepared statement. |
| [SQLiteStatement](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement) | Represents a statement that can be executed against a database. |

## Exceptions

| [SQLiteAbortException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAbortException) | An exception that indicates that the SQLite program was aborted. |
| --- | --- |
| [SQLiteAccessPermException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAccessPermException) | This exception class is used when sqlite can't access the database file due to lack of permissions on the file. |
| [SQLiteBindOrColumnIndexOutOfRangeException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteBindOrColumnIndexOutOfRangeException) | Thrown if the bind or column parameter index is out of range. |
| [SQLiteBlobTooBigException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteBlobTooBigException) | <br /> |
| --- | --- |
| [SQLiteCantOpenDatabaseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCantOpenDatabaseException) | <br /> |
| [SQLiteConstraintException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteConstraintException) | An exception that indicates that an integrity constraint was violated. |
| [SQLiteDatabaseCorruptException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabaseCorruptException) | An exception that indicates that the SQLite database file is corrupt. |
| --- | --- |
| [SQLiteDatabaseLockedException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabaseLockedException) | Thrown if the database engine was unable to acquire the database locks it needs to do its job. |
| [SQLiteDatatypeMismatchException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatatypeMismatchException) | <br /> |
| [SQLiteDiskIOException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDiskIOException) | Indicates that an IO error occurred while accessing the SQLite database file. |
| --- | --- |
| [SQLiteDoneException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDoneException) | An exception that indicates that the SQLite program is done. |
| [SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) | A SQLite exception that indicates there was an error with SQL parsing or execution. |
| [SQLiteFullException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteFullException) | An exception that indicates that the SQLite database is full. |
| --- | --- |
| [SQLiteMisuseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteMisuseException) | This error can occur if the application creates a SQLiteStatement object and allows multiple threads in the application use it at the same time. |
| [SQLiteOutOfMemoryException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOutOfMemoryException) | <br /> |
| [SQLiteReadOnlyDatabaseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteReadOnlyDatabaseException) | <br /> |
| --- | --- |
| [SQLiteTableLockedException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTableLockedException) | <br /> |
