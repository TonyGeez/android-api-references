# android.database.sqlite

# android.database.sqlite

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [SQLiteCursorDriver](SQLiteCursorDriver.md) | A driver for SQLiteCursors that is used to create them and gets notified by the cursors it creates on significant events in their lifetimes. |
| --- | --- |
| [CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md) | Used to allow returning sub-classes of [Cursor](../android.database/Cursor.md) when calling query. |
| [SQLiteTransactionListener](SQLiteTransactionListener.md) | A listener for transaction events. |

## Classes

| [SQLiteClosable](SQLiteClosable.md) | An object created from a SQLiteDatabase that can be closed. |
| --- | --- |
| [SQLiteCursor](SQLiteCursor.md) | A Cursor implementation that exposes results from a query on a [SQLiteDatabase](SQLiteDatabase.md). |
| [SQLiteDatabase](SQLiteDatabase.md) | Exposes methods to manage a SQLite database. |
| [SQLiteOpenHelper](SQLiteOpenHelper.md) | A helper class to manage database creation and version management. |
| --- | --- |
| [SQLiteProgram](SQLiteProgram.md) | A base class for compiled SQLite programs. |
| [SQLiteQuery](SQLiteQuery.md) | Represents a query that reads the resulting rows into a [SQLiteQuery](SQLiteQuery.md). |
| [SQLiteQueryBuilder](SQLiteQueryBuilder.md) | This is a convenience class that helps build SQL queries to be sent to [SQLiteDatabase](SQLiteDatabase.md) objects. |
| --- | --- |
| [SQLiteRawStatement](SQLiteRawStatement.md) | A represents a SQLite prepared statement. |
| [SQLiteStatement](SQLiteStatement.md) | Represents a statement that can be executed against a database. |

## Exceptions

| [SQLiteAbortException](SQLiteAbortException.md) | An exception that indicates that the SQLite program was aborted. |
| --- | --- |
| [SQLiteAccessPermException](SQLiteAccessPermException.md) | This exception class is used when sqlite can't access the database file due to lack of permissions on the file. |
| [SQLiteBindOrColumnIndexOutOfRangeException](SQLiteBindOrColumnIndexOutOfRangeException.md) | Thrown if the bind or column parameter index is out of range. |
| [SQLiteBlobTooBigException](SQLiteBlobTooBigException.md) | <br /> |
| --- | --- |
| [SQLiteCantOpenDatabaseException](SQLiteCantOpenDatabaseException.md) | <br /> |
| [SQLiteConstraintException](SQLiteConstraintException.md) | An exception that indicates that an integrity constraint was violated. |
| [SQLiteDatabaseCorruptException](SQLiteDatabaseCorruptException.md) | An exception that indicates that the SQLite database file is corrupt. |
| --- | --- |
| [SQLiteDatabaseLockedException](SQLiteDatabaseLockedException.md) | Thrown if the database engine was unable to acquire the database locks it needs to do its job. |
| [SQLiteDatatypeMismatchException](SQLiteDatatypeMismatchException.md) | <br /> |
| [SQLiteDiskIOException](SQLiteDiskIOException.md) | Indicates that an IO error occurred while accessing the SQLite database file. |
| --- | --- |
| [SQLiteDoneException](SQLiteDoneException.md) | An exception that indicates that the SQLite program is done. |
| [SQLiteException](SQLiteException.md) | A SQLite exception that indicates there was an error with SQL parsing or execution. |
| [SQLiteFullException](SQLiteFullException.md) | An exception that indicates that the SQLite database is full. |
| --- | --- |
| [SQLiteMisuseException](SQLiteMisuseException.md) | This error can occur if the application creates a SQLiteStatement object and allows multiple threads in the application use it at the same time. |
| [SQLiteOutOfMemoryException](SQLiteOutOfMemoryException.md) | <br /> |
| [SQLiteReadOnlyDatabaseException](SQLiteReadOnlyDatabaseException.md) | <br /> |
| --- | --- |
| [SQLiteTableLockedException](SQLiteTableLockedException.md) | <br /> |
