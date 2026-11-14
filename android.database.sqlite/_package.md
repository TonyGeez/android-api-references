# android.database.sqlite

# android.database.sqlite

Kotlin| [Java](../android/database/sqlite/_package.md)
| --- | --- |

## Interfaces

| [SQLiteCursorDriver](../android/database/sqlite/SQLiteCursorDriver.md) | A driver for SQLiteCursors that is used to create them and gets notified by the cursors it creates on significant events in their lifetimes. |
| --- | --- |
| [CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md) | Used to allow returning sub-classes of [Cursor](../android/database/Cursor.md) when calling query. |
| [SQLiteTransactionListener](../android/database/sqlite/SQLiteTransactionListener.md) | A listener for transaction events. |

## Classes

| [SQLiteClosable](../android/database/sqlite/SQLiteClosable.md) | An object created from a SQLiteDatabase that can be closed. |
| --- | --- |
| [SQLiteCursor](../android/database/sqlite/SQLiteCursor.md) | A Cursor implementation that exposes results from a query on a [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md). |
| [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md) | Exposes methods to manage a SQLite database. |
| [SQLiteOpenHelper](../android/database/sqlite/SQLiteOpenHelper.md) | A helper class to manage database creation and version management. |
| --- | --- |
| [SQLiteProgram](../android/database/sqlite/SQLiteProgram.md) | A base class for compiled SQLite programs. |
| [SQLiteQuery](../android/database/sqlite/SQLiteQuery.md) | Represents a query that reads the resulting rows into a [SQLiteQuery](../android/database/sqlite/SQLiteQuery.md). |
| [SQLiteQueryBuilder](../android/database/sqlite/SQLiteQueryBuilder.md) | This is a convenience class that helps build SQL queries to be sent to [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md) objects. |
| --- | --- |
| [SQLiteRawStatement](../android/database/sqlite/SQLiteRawStatement.md) | A represents a SQLite prepared statement. |
| [SQLiteStatement](../android/database/sqlite/SQLiteStatement.md) | Represents a statement that can be executed against a database. |

## Exceptions

| [SQLiteAbortException](../android/database/sqlite/SQLiteAbortException.md) | An exception that indicates that the SQLite program was aborted. |
| --- | --- |
| [SQLiteAccessPermException](../android/database/sqlite/SQLiteAccessPermException.md) | This exception class is used when sqlite can't access the database file due to lack of permissions on the file. |
| [SQLiteBindOrColumnIndexOutOfRangeException](../android/database/sqlite/SQLiteBindOrColumnIndexOutOfRangeException.md) | Thrown if the bind or column parameter index is out of range. |
| [SQLiteBlobTooBigException](../android/database/sqlite/SQLiteBlobTooBigException.md) | <br /> |
| --- | --- |
| [SQLiteCantOpenDatabaseException](../android/database/sqlite/SQLiteCantOpenDatabaseException.md) | <br /> |
| [SQLiteConstraintException](../android/database/sqlite/SQLiteConstraintException.md) | An exception that indicates that an integrity constraint was violated. |
| [SQLiteDatabaseCorruptException](../android/database/sqlite/SQLiteDatabaseCorruptException.md) | An exception that indicates that the SQLite database file is corrupt. |
| --- | --- |
| [SQLiteDatabaseLockedException](../android/database/sqlite/SQLiteDatabaseLockedException.md) | Thrown if the database engine was unable to acquire the database locks it needs to do its job. |
| [SQLiteDatatypeMismatchException](../android/database/sqlite/SQLiteDatatypeMismatchException.md) | <br /> |
| [SQLiteDiskIOException](../android/database/sqlite/SQLiteDiskIOException.md) | Indicates that an IO error occurred while accessing the SQLite database file. |
| --- | --- |
| [SQLiteDoneException](../android/database/sqlite/SQLiteDoneException.md) | An exception that indicates that the SQLite program is done. |
| [SQLiteException](../android/database/sqlite/SQLiteException.md) | A SQLite exception that indicates there was an error with SQL parsing or execution. |
| [SQLiteFullException](../android/database/sqlite/SQLiteFullException.md) | An exception that indicates that the SQLite database is full. |
| --- | --- |
| [SQLiteMisuseException](../android/database/sqlite/SQLiteMisuseException.md) | This error can occur if the application creates a SQLiteStatement object and allows multiple threads in the application use it at the same time. |
| [SQLiteOutOfMemoryException](../android/database/sqlite/SQLiteOutOfMemoryException.md) | <br /> |
| [SQLiteReadOnlyDatabaseException](../android/database/sqlite/SQLiteReadOnlyDatabaseException.md) | <br /> |
| --- | --- |
| [SQLiteTableLockedException](../android/database/sqlite/SQLiteTableLockedException.md) | <br /> |
