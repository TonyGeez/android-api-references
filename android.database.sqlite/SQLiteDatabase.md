Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteDatabase

```
class SQLiteDatabase : SQLiteClosable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.database.sqlite.SQLiteClosable](SQLiteClosable.md) ||
| | ↳ | [android.database.sqlite.SQLiteDatabase](SQLiteDatabase.md) |

Exposes methods to manage a SQLite database.

SQLiteDatabase has methods to create, delete, execute SQL commands, and perform other common database management tasks.

See the Notepad sample application in the SDK for an example of creating and managing a database.

Database names must be unique within an application, not across all applications.

### Localized Collation - ORDER BY

In addition to SQLite's default `BINARY` collator, Android supplies two more, `LOCALIZED`, which changes with the system's current locale, and `UNICODE`, which is the Unicode Collation Algorithm and not tailored to the current locale.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory` Used to allow returning sub-classes of `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` when calling query. |
| | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.OpenParams` Wrapper for configuration parameters that are used for opening `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#` |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CONFLICT_ABORT:kotlin.Int` When a constraint violation occurs,no ROLLBACK is executed so changes from prior commands within the same transaction are preserved. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CONFLICT_FAIL:kotlin.Int` When a constraint violation occurs, the command aborts with a return code SQLITE_CONSTRAINT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CONFLICT_IGNORE:kotlin.Int` When a constraint violation occurs, the one row that contains the constraint violation is not inserted or changed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CONFLICT_NONE:kotlin.Int` Use the following when no conflict action is specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CONFLICT_REPLACE:kotlin.Int` When a UNIQUE constraint violation occurs, the pre-existing rows that are causing the constraint violation are removed prior to inserting or updating the current row. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CONFLICT_ROLLBACK:kotlin.Int` When a constraint violation occurs, an immediate ROLLBACK occurs, thus ending the current transaction, and the command aborts with a return code of SQLITE_CONSTRAINT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CREATE_IF_NECESSARY:kotlin.Int` Open flag: Flag for #openDatabase to create the database file if it does not already exist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int` Open flag: Flag for #openDatabase to open the database file with write-ahead logging enabled by default. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#JOURNAL_MODE_DELETE:kotlin.String` The `DELETE` journaling mode is the normal behavior. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#JOURNAL_MODE_MEMORY:kotlin.String` The `MEMORY` journaling mode stores the rollback journal in volatile RAM. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#JOURNAL_MODE_OFF:kotlin.String` The `OFF` journaling mode disables the rollback journal completely. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#JOURNAL_MODE_PERSIST:kotlin.String` The `PERSIST` journaling mode prevents the rollback journal from being deleted at the end of each transaction. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#JOURNAL_MODE_TRUNCATE:kotlin.String` The `TRUNCATE` journaling mode commits transactions by truncating the rollback journal to zero-length instead of deleting it. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#JOURNAL_MODE_WAL:kotlin.String` The `WAL` journaling mode uses a write-ahead log instead of a rollback journal to implement transactions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#MAX_SQL_CACHE_SIZE:kotlin.Int` Absolute max value that can be set by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setMaxSqlCacheSize(kotlin.Int)`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#NO_LOCALIZED_COLLATORS:kotlin.Int` Open flag: Flag for #openDatabase to open the database without support for localized collators. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READONLY:kotlin.Int` Open flag: Flag for #openDatabase to open the database for reading only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READWRITE:kotlin.Int` Open flag: Flag for #openDatabase to open the database for reading and writing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#SQLITE_MAX_LIKE_PATTERN_LENGTH:kotlin.Int` Maximum Length Of A LIKE Or GLOB Pattern The pattern matching algorithm used in the default LIKE and GLOB implementation of SQLite can exhibit O(N\^2) performance (where N is the number of characters in the pattern) for certain pathological cases. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#SYNC_MODE_EXTRA:kotlin.String` The `EXTRA` sync mode is like `FULL` sync mode with the addition that the directory containing a rollback journal is synced after that journal is unlinked to commit a transaction in `DELETE` journal mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#SYNC_MODE_FULL:kotlin.String` In `FULL` sync mode the SQLite database engine will use the xSync method of the VFS to ensure that all content is safely written to the disk surface prior to continuing. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#SYNC_MODE_NORMAL:kotlin.String` The `NORMAL` sync mode, the SQLite database engine will still sync at the most critical moments, but less often than in `FULL` mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#SYNC_MODE_OFF:kotlin.String` In `OFF` sync mode SQLite continues without syncing as soon as it has handed data off to the operating system. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#beginTransaction()()` Begins a transaction in EXCLUSIVE mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#beginTransactionNonExclusive()()` Begins a transaction in IMMEDIATE mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#beginTransactionReadOnly()()` Begins a transaction in DEFERRED mode, with the android-specific constraint that the transaction is read-only. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#beginTransactionWithListener(android.database.sqlite.SQLiteTransactionListener)(transactionListener: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTransactionListener?)` Begins a transaction in EXCLUSIVE mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#beginTransactionWithListenerNonExclusive(android.database.sqlite.SQLiteTransactionListener)(transactionListener: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTransactionListener?)` Begins a transaction in IMMEDIATE mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#beginTransactionWithListenerReadOnly(android.database.sqlite.SQLiteTransactionListener)(transactionListener: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTransactionListener?)` Begins a transaction in read-only mode with a `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTransactionListener` listener. |
| --- | --- |
| [SQLiteStatement](SQLiteStatement.md)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#compileStatement(kotlin.String)(sql: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Compiles an SQL statement into a reusable pre-compiled statement object. |
| static [SQLiteDatabase](SQLiteDatabase.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#create(android.database.sqlite.SQLiteDatabase.CursorFactory)(factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory?)` Create a memory backed SQLite database. |
| static [SQLiteDatabase](SQLiteDatabase.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#createInMemory(android.database.sqlite.SQLiteDatabase.OpenParams)(openParams: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.OpenParams)` Create a memory backed SQLite database. |
| --- | --- |
| [SQLiteRawStatement](SQLiteRawStatement.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#createRawStatement(kotlin.String)(sql: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Return a `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement` connected to the database. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#delete(kotlin.String,%20kotlin.String,%20kotlin.Array)(table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, whereClause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, whereArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Convenience method for deleting rows in the database. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#deleteDatabase(java.io.File)(file: https://developer.android.com/reference/kotlin/java/io/File.html#)` Deletes a database including its journal file and other auxiliary files that may have been created by the database engine. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#disableWriteAheadLogging()()` This method disables the features enabled by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()()` Write-ahead logging enables parallel execution of queries from multiple threads on the same database, and reduces the likelihood of stalling on filesystem syncs. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#endTransaction()()` End a transaction. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#execPerConnectionSQL(kotlin.String,%20kotlin.Array)(sql: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, bindArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>?)` Execute the given SQL statement on all connections to this database. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#execSQL(kotlin.String)(sql: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Execute a single SQL statement that is NOT a SELECT or any other SQL statement that returns data. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#execSQL(kotlin.String,%20kotlin.Array)(sql: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, bindArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>)` Execute a single SQL statement that is NOT a SELECT/INSERT/UPDATE/DELETE. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#findEditTable(kotlin.String)(tables: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Finds the name of the first table, which is editable. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Pair](../android.util/Pair.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#getAttachedDbs()()` Returns list of full pathnames of all attached databases including the main database by executing 'pragma database_list' on the database. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#getLastChangedRowCount()()` Return the number of database rows that were inserted, updated, or deleted by the most recent SQL statement within the current transaction. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#getLastInsertRowId()()` Return the "rowid" of the last row to be inserted on the current connection. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#getMaximumSize()()` Returns the maximum size the database may grow to. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#getPageSize()()` Returns the current database page size, in bytes. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#getPath()()` Gets the path to the database file. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#getSyncedTables()()` Deprecated. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#getTotalChangedRowCount()()` Return the total number of database rows that have been inserted, updated, or deleted on the current connection since it was created. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#getVersion()()` Gets the database version. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#inTransaction()()` Returns true if the current thread has a transaction pending. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#insert(kotlin.String,%20kotlin.String,%20android.content.ContentValues)(table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, nullColumnHack: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?)` Convenience method for inserting a row into the database. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#insertOrThrow(kotlin.String,%20kotlin.String,%20android.content.ContentValues)(table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, nullColumnHack: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?)` Convenience method for inserting a row into the database. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#insertWithOnConflict(kotlin.String,%20kotlin.String,%20android.content.ContentValues,%20kotlin.Int)(table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, nullColumnHack: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialValues: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?, conflictAlgorithm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` General method for inserting a row into the database. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#isDatabaseIntegrityOk()()` Runs 'pragma integrity_check' on the given database (and all the attached databases) and returns true if the given database (and all its attached databases) pass integrity_check, false otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#isDbLockedByCurrentThread()()` Returns true if the current thread is holding an active connection to the database. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#isDbLockedByOtherThreads()()` Always returns false. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#isOpen()()` Returns true if the database is currently open. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#isReadOnly()()` Returns true if the database is opened as read only. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#isWriteAheadLoggingEnabled()()` Returns true if write-ahead logging has been enabled for this database. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#markTableSyncable(kotlin.String,%20kotlin.String)(table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, deletedTable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Mark this table as syncable. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#markTableSyncable(kotlin.String,%20kotlin.String,%20kotlin.String)(table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, foreignKey: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, updateTable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Mark this table as syncable, with the _sync_dirty residing in another table. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#needUpgrade(kotlin.Int)(newVersion: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if the new version code is greater than the current database version. |
| static [SQLiteDatabase](SQLiteDatabase.md)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#openDatabase(java.io.File,%20android.database.sqlite.SQLiteDatabase.OpenParams)(path: https://developer.android.com/reference/kotlin/java/io/File.html#, openParams: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.OpenParams)` Open the database according to the specified `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.OpenParams` |
| --- | --- |
| static [SQLiteDatabase](SQLiteDatabase.md)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#openDatabase(kotlin.String,%20android.database.sqlite.SQLiteDatabase.CursorFactory,%20kotlin.Int)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory?, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Open the database according to the flags `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READWRITE:kotlin.Int` `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READONLY:kotlin.Int` `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CREATE_IF_NECESSARY:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#NO_LOCALIZED_COLLATORS:kotlin.Int`. |
| static [SQLiteDatabase](SQLiteDatabase.md)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#openDatabase(kotlin.String,%20android.database.sqlite.SQLiteDatabase.CursorFactory,%20kotlin.Int,%20android.database.DatabaseErrorHandler)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory?, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, errorHandler: https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#?)` Open the database according to the flags `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READWRITE:kotlin.Int``https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READONLY:kotlin.Int``https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CREATE_IF_NECESSARY:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#NO_LOCALIZED_COLLATORS:kotlin.Int`. |
| static [SQLiteDatabase](SQLiteDatabase.md)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#openOrCreateDatabase(java.io.File,%20android.database.sqlite.SQLiteDatabase.CursorFactory)(file: https://developer.android.com/reference/kotlin/java/io/File.html#, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory?)` Equivalent to openDatabase(file.getPath(), factory, CREATE_IF_NECESSARY). |
| --- | --- |
| static [SQLiteDatabase](SQLiteDatabase.md)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#openOrCreateDatabase(kotlin.String,%20android.database.sqlite.SQLiteDatabase.CursorFactory)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory?)` Equivalent to openDatabase(path, factory, CREATE_IF_NECESSARY). |
| static [SQLiteDatabase](SQLiteDatabase.md)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#openOrCreateDatabase(kotlin.String,%20android.database.sqlite.SQLiteDatabase.CursorFactory,%20android.database.DatabaseErrorHandler)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory?, errorHandler: https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#?)` Equivalent to openDatabase(path, factory, CREATE_IF_NECESSARY, errorHandler). |
| [Cursor](../android.database/Cursor.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#query(kotlin.Boolean,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String)(distinct: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, columns: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, groupBy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, having: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, orderBy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, limit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Query the given URL, returning a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set. |
| --- | --- |
| [Cursor](../android.database/Cursor.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#query(kotlin.Boolean,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.CancellationSignal)(distinct: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, columns: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, groupBy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, having: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, orderBy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, limit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Query the given URL, returning a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set. |
| [Cursor](../android.database/Cursor.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#query(kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String)(table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, columns: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, groupBy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, having: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, orderBy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Query the given table, returning a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set. |
| [Cursor](../android.database/Cursor.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#query(kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String)(table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, columns: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, groupBy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, having: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, orderBy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, limit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Query the given table, returning a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set. |
| --- | --- |
| [Cursor](../android.database/Cursor.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#queryWithFactory(android.database.sqlite.SQLiteDatabase.CursorFactory,%20kotlin.Boolean,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String)(cursorFactory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory?, distinct: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, columns: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, groupBy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, having: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, orderBy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, limit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Query the given URL, returning a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set. |
| [Cursor](../android.database/Cursor.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#queryWithFactory(android.database.sqlite.SQLiteDatabase.CursorFactory,%20kotlin.Boolean,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.CancellationSignal)(cursorFactory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory?, distinct: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, columns: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, groupBy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, having: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, orderBy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, limit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Query the given URL, returning a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set. |
| [Cursor](../android.database/Cursor.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#rawQuery(kotlin.String,%20kotlin.Array)(sql: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Runs the provided SQL and returns a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set. |
| --- | --- |
| [Cursor](../android.database/Cursor.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#rawQuery(kotlin.String,%20kotlin.Array,%20android.os.CancellationSignal)(sql: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Runs the provided SQL and returns a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set. |
| [Cursor](../android.database/Cursor.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#rawQueryWithFactory(android.database.sqlite.SQLiteDatabase.CursorFactory,%20kotlin.String,%20kotlin.Array,%20kotlin.String)(cursorFactory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory?, sql: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, editTable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Runs the provided SQL and returns a cursor over the result set. |
| [Cursor](../android.database/Cursor.md) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#rawQueryWithFactory(android.database.sqlite.SQLiteDatabase.CursorFactory,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20android.os.CancellationSignal)(cursorFactory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory?, sql: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, editTable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Runs the provided SQL and returns a cursor over the result set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#releaseMemory()()` Attempts to release memory that SQLite holds but does not require to operate properly. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#replace(kotlin.String,%20kotlin.String,%20android.content.ContentValues)(table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, nullColumnHack: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialValues: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?)` Convenience method for replacing a row in the database. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#replaceOrThrow(kotlin.String,%20kotlin.String,%20android.content.ContentValues)(table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, nullColumnHack: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialValues: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?)` Convenience method for replacing a row in the database. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setCustomAggregateFunction(kotlin.String,%20java.util.function.BinaryOperator)(functionName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, aggregateFunction: https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Register a custom aggregate function that can be called from SQL expressions. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setCustomScalarFunction(kotlin.String,%20java.util.function.UnaryOperator)(functionName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, scalarFunction: https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Register a custom scalar function that can be called from SQL expressions. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setForeignKeyConstraintsEnabled(kotlin.Boolean)(enable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether foreign key constraints are enabled for the database. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setLocale(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Sets the locale for this database. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setLockingEnabled(kotlin.Boolean)(lockingEnabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Control whether or not the SQLiteDatabase is made thread-safe by using locks around critical sections. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setMaxSqlCacheSize(kotlin.Int)(cacheSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the maximum size of the prepared-statement cache for this database. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setMaximumSize(kotlin.Long)(numBytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the maximum size the database will grow to. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setPageSize(kotlin.Long)(numBytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the database page size. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setTransactionSuccessful()()` Marks the current transaction as successful. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setVersion(kotlin.Int)(version: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the database version. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#toString()()` Returns a string representation of the object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#update(kotlin.String,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array)(table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?, whereClause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, whereArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Convenience method for updating rows in the database. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#updateWithOnConflict(kotlin.String,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array,%20kotlin.Int)(table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?, whereClause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, whereArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, conflictAlgorithm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Convenience method for updating rows in the database. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#validateSql(kotlin.String,%20android.os.CancellationSignal)(sql: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Verifies that a SQL SELECT statement is valid by compiling it. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#yieldIfContended()()` Temporarily end the transaction to let other threads run. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#yieldIfContendedSafely()()` Temporarily end the transaction to let other threads run. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#yieldIfContendedSafely(kotlin.Long)(sleepAfterYieldDelay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Temporarily end the transaction to let other threads run. |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#onAllReferencesReleased()()` Called when the last reference to the object was released by a call to `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference()` or #close(). |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#acquireReference()()`

Acquires a reference to the object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#close()()`

Releases a reference to the object, closing the object if the last reference was released. Calling this method is equivalent to calling `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#onAllReferencesReleasedFromContainer()()`

Called when the last reference to the object was released by a call to `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReferenceFromContainer()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference()()`

Releases a reference to the object, closing the object if the last reference was released.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReferenceFromContainer()()`

Releases a reference to the object that was owned by the container of the object, closing the object if the last reference was released.

<br />

## Constants

### CONFLICT_ABORT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFLICT_ABORT: Int
```

When a constraint violation occurs,no ROLLBACK is executed so changes from prior commands within the same transaction are preserved. This is the default behavior.

 Value: 2

### CONFLICT_FAIL

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFLICT_FAIL: Int
```

When a constraint violation occurs, the command aborts with a return code SQLITE_CONSTRAINT. But any changes to the database that the command made prior to encountering the constraint violation are preserved and are not backed out.

 Value: 3

### CONFLICT_IGNORE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFLICT_IGNORE: Int
```

When a constraint violation occurs, the one row that contains the constraint violation is not inserted or changed. But the command continues executing normally. Other rows before and after the row that contained the constraint violation continue to be inserted or updated normally. No error is returned.

 Value: 4

### CONFLICT_NONE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFLICT_NONE: Int
```

Use the following when no conflict action is specified.

 Value: 0

### CONFLICT_REPLACE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFLICT_REPLACE: Int
```

When a UNIQUE constraint violation occurs, the pre-existing rows that are causing the constraint violation are removed prior to inserting or updating the current row. Thus the insert or update always occurs. The command continues executing normally. No error is returned. If a NOT NULL constraint violation occurs, the NULL value is replaced by the default value for that column. If the column has no default value, then the ABORT algorithm is used. If a CHECK constraint violation occurs then the IGNORE algorithm is used. When this conflict resolution strategy deletes rows in order to satisfy a constraint, it does not invoke delete triggers on those rows. This behavior might change in a future release.

 Value: 5

### CONFLICT_ROLLBACK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFLICT_ROLLBACK: Int
```

When a constraint violation occurs, an immediate ROLLBACK occurs, thus ending the current transaction, and the command aborts with a return code of SQLITE_CONSTRAINT. If no transaction is active (other than the implied transaction that is created on every command) then this algorithm works the same as ABORT.

 Value: 1

### CREATE_IF_NECESSARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATE_IF_NECESSARY: Int
```

Open flag: Flag for #openDatabase to create the database file if it does not already exist.

 Value: 268435456

### ENABLE_WRITE_AHEAD_LOGGING

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENABLE_WRITE_AHEAD_LOGGING: Int
```

Open flag: Flag for #openDatabase to open the database file with write-ahead logging enabled by default. Using this flag is more efficient than calling `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()`. Write-ahead logging cannot be used with read-only databases so the value of this flag is ignored if the database is opened read-only.

 Value: 536870912

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()`

### JOURNAL_MODE_DELETE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JOURNAL_MODE_DELETE: String
```

The `DELETE` journaling mode is the normal behavior. In the DELETE mode, the rollback journal is deleted at the conclusion of each transaction.

See [here](https://www.sqlite.org/pragma.html#pragma_journal_mode) for more details.

 Value: "DELETE"

### JOURNAL_MODE_MEMORY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JOURNAL_MODE_MEMORY: String
```

The `MEMORY` journaling mode stores the rollback journal in volatile RAM. This saves disk I/O but at the expense of database safety and integrity. If the application using SQLite crashes in the middle of a transaction when the MEMORY journaling mode is set, then the database file will very likely go corrupt.

See [here](https://www.sqlite.org/pragma.html#pragma_journal_mode) for more details.

 Value: "MEMORY"

### JOURNAL_MODE_OFF

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JOURNAL_MODE_OFF: String
```

The `OFF` journaling mode disables the rollback journal completely. No rollback journal is ever created and hence there is never a rollback journal to delete. The OFF journaling mode disables the atomic commit and rollback capabilities of SQLite. The ROLLBACK command behaves in an undefined way thus applications must avoid using the ROLLBACK command. If the application crashes in the middle of a transaction, then the database file will very likely go corrupt.

See [here](https://www.sqlite.org/pragma.html#pragma_journal_mode) for more details.

 Value: "OFF"

### JOURNAL_MODE_PERSIST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JOURNAL_MODE_PERSIST: String
```

The `PERSIST` journaling mode prevents the rollback journal from being deleted at the end of each transaction. Instead, the header of the journal is overwritten with zeros. This will prevent other database connections from rolling the journal back. This mode is useful as an optimization on platforms where deleting or truncating a file is much more expensive than overwriting the first block of a file with zeros.

See [here](https://www.sqlite.org/pragma.html#pragma_journal_mode) for more details.

 Value: "PERSIST"

### JOURNAL_MODE_TRUNCATE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JOURNAL_MODE_TRUNCATE: String
```

The `TRUNCATE` journaling mode commits transactions by truncating the rollback journal to zero-length instead of deleting it. On many systems, truncating a file is much faster than deleting the file since the containing directory does not need to be changed.

See [here](https://www.sqlite.org/pragma.html#pragma_journal_mode) for more details.

 Value: "TRUNCATE"

### JOURNAL_MODE_WAL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JOURNAL_MODE_WAL: String
```

The `WAL` journaling mode uses a write-ahead log instead of a rollback journal to implement transactions. The WAL journaling mode is persistent; after being set it stays in effect across multiple database connections and after closing and reopening the database. Performance Considerations: This mode is recommended when the goal is to improve write performance or parallel read/write performance. However, it is important to note that WAL introduces checkpoints which commit all transactions that have not been synced to the database thus to maximize read performance and lower checkpointing cost a small journal size is recommended. However, other modes such as `DELETE` will not perform checkpoints, so it is a trade off that needs to be considered as part of the decision of which journal mode to use.

See [here](https://www.sqlite.org/pragma.html#pragma_journal_mode) for more details.

 Value: "WAL"

### MAX_SQL_CACHE_SIZE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_SQL_CACHE_SIZE: Int
```

Absolute max value that can be set by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setMaxSqlCacheSize(kotlin.Int)`. Each prepared-statement is between 1K - 6K, depending on the complexity of the SQL statement \& schema. A large SQL cache may use a significant amount of memory.

 Value: 100

### NO_LOCALIZED_COLLATORS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_LOCALIZED_COLLATORS: Int
```

Open flag: Flag for #openDatabase to open the database without support for localized collators. {@more} This causes the collator `LOCALIZED` not to be created. You must be consistent when using this flag to use the setting the database was created with. If this is set, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setLocale(java.util.Locale)` will do nothing.

 Value: 16

### OPEN_READONLY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPEN_READONLY: Int
```

Open flag: Flag for #openDatabase to open the database for reading only. This is the only reliable way to open a database if the disk may be full.

 Value: 1

### OPEN_READWRITE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPEN_READWRITE: Int
```

Open flag: Flag for #openDatabase to open the database for reading and writing. If the disk is full, this may fail even before you actually write anything. {@more} Note that the value of this flag is 0, so it is the default.

 Value: 0

### SQLITE_MAX_LIKE_PATTERN_LENGTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SQLITE_MAX_LIKE_PATTERN_LENGTH: Int
```

Maximum Length Of A LIKE Or GLOB Pattern The pattern matching algorithm used in the default LIKE and GLOB implementation of SQLite can exhibit O(N\^2) performance (where N is the number of characters in the pattern) for certain pathological cases. To avoid denial-of-service attacks the length of the LIKE or GLOB pattern is limited to SQLITE_MAX_LIKE_PATTERN_LENGTH bytes. The default value of this limit is 50000. A modern workstation can evaluate even a pathological LIKE or GLOB pattern of 50000 bytes relatively quickly. The denial of service problem only comes into play when the pattern length gets into millions of bytes. Nevertheless, since most useful LIKE or GLOB patterns are at most a few dozen bytes in length, cautious application developers may want to reduce this parameter to something in the range of a few hundred if they know that external users are able to generate arbitrary patterns.

 Value: 50000

### SYNC_MODE_EXTRA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYNC_MODE_EXTRA: String
```

The `EXTRA` sync mode is like `FULL` sync mode with the addition that the directory containing a rollback journal is synced after that journal is unlinked to commit a transaction in `DELETE` journal mode. `EXTRA` provides additional durability if the commit is followed closely by a power loss.

See [here](https://www.sqlite.org/pragma.html#pragma_synchronous) for more details.

 Value: "EXTRA"

### SYNC_MODE_FULL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYNC_MODE_FULL: String
```

In `FULL` sync mode the SQLite database engine will use the xSync method of the VFS to ensure that all content is safely written to the disk surface prior to continuing. This ensures that an operating system crash or power failure will not corrupt the database. `FULL` is very safe, but it is also slower. `FULL` is the most commonly used synchronous setting when not in WAL mode.

See [here](https://www.sqlite.org/pragma.html#pragma_synchronous) for more details.

 Value: "FULL"

### SYNC_MODE_NORMAL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYNC_MODE_NORMAL: String
```

The `NORMAL` sync mode, the SQLite database engine will still sync at the most critical moments, but less often than in `FULL` mode. There is a very small chance that a power failure at the wrong time could corrupt the database in `DELETE` journal mode on an older filesystem. `WAL` journal mode is safe from corruption with `NORMAL` sync mode, and probably `DELETE` sync mode is safe too on modern filesystems. WAL mode is always consistent with `NORMAL` sync mode, but WAL mode does lose durability. A transaction committed in WAL mode with `NORMAL` might roll back following a power loss or system crash. Transactions are durable across application crashes regardless of the synchronous setting or journal mode. The `NORMAL` sync mode is a good choice for most applications running in WAL mode.

Caveat: Even though this sync mode is safe Be careful when using `NORMAL` sync mode when dealing with data dependencies between multiple databases, unless those databases use the same durability or are somehow synced, there could be corruption.

See [here](https://www.sqlite.org/pragma.html#pragma_synchronous) for more details.

 Value: "NORMAL"

### SYNC_MODE_OFF

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYNC_MODE_OFF: String
```

In `OFF` sync mode SQLite continues without syncing as soon as it has handed data off to the operating system. If the application running SQLite crashes, the data will be safe, but the database might become corrupted if the operating system crashes or the computer loses power before that data has been written to the disk surface. On the other hand, commits can be orders of magnitude faster with synchronous `OFF`.

See [here](https://www.sqlite.org/pragma.html#pragma_synchronous) for more details.

 Value: "OFF"

## Public methods

### beginTransaction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun beginTransaction(): Unit
```

Begins a transaction in EXCLUSIVE mode.

Transactions can be nested. When the outer transaction is ended all of the work done in that transaction and all of the nested transactions will be committed or rolled back. The changes will be rolled back if any transaction is ended without being marked as clean (by calling setTransactionSuccessful). Otherwise they will be committed.

Here is the standard idiom for transactions:

```kotlin
db.beginTransaction();
    try {
      ...
      db.setTransactionSuccessful();
    } finally {
      db.endTransaction();
    }
  
```

### beginTransactionNonExclusive

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun beginTransactionNonExclusive(): Unit
```

Begins a transaction in IMMEDIATE mode. Transactions can be nested. When the outer transaction is ended all of the work done in that transaction and all of the nested transactions will be committed or rolled back. The changes will be rolled back if any transaction is ended without being marked as clean (by calling setTransactionSuccessful). Otherwise they will be committed.

Here is the standard idiom for transactions:

```kotlin
db.beginTransactionNonExclusive();
    try {
      ...
      db.setTransactionSuccessful();
    } finally {
      db.endTransaction();
    }
  
```

### beginTransactionReadOnly

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun beginTransactionReadOnly(): Unit
```

Begins a transaction in DEFERRED mode, with the android-specific constraint that the transaction is read-only. The database may not be modified inside a read-only transaction.

Read-only transactions may run concurrently with other read-only transactions, and if the database is in WAL mode, they may also run concurrently with IMMEDIATE or EXCLUSIVE transactions. The `temp` schema may be modified during a read-only transaction; if the transaction is `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setTransactionSuccessful()`, modifications to temp tables may be visible to some subsequent transactions.

Transactions can be nested. However, the behavior of the transaction is not altered by nested transactions. A nested transaction may be any of the three transaction types but if the outermost type is read-only then nested transactions remain read-only, regardless of how they are started.

Here is the standard idiom for read-only transactions:

```kotlin
db.beginTransactionReadOnly();
    try {
      ...
    } finally {
      db.endTransaction();
    }
  
```

### beginTransactionWithListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun beginTransactionWithListener(transactionListener: SQLiteTransactionListener?): Unit
```

Begins a transaction in EXCLUSIVE mode.

Transactions can be nested. When the outer transaction is ended all of the work done in that transaction and all of the nested transactions will be committed or rolled back. The changes will be rolled back if any transaction is ended without being marked as clean (by calling setTransactionSuccessful). Otherwise they will be committed.

Here is the standard idiom for transactions:

```kotlin
db.beginTransactionWithListener(listener);
    try {
      ...
      db.setTransactionSuccessful();
    } finally {
      db.endTransaction();
    }
  
```

| Parameters ||
|---|---|
| `transactionListener` | [SQLiteTransactionListener](SQLiteTransactionListener.md)?: listener that should be notified when the transaction begins, commits, or is rolled back, either explicitly or by a call to #yieldIfContendedSafely. This value may be `null`. |

### beginTransactionWithListenerNonExclusive

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun beginTransactionWithListenerNonExclusive(transactionListener: SQLiteTransactionListener?): Unit
```

Begins a transaction in IMMEDIATE mode. Transactions can be nested. When the outer transaction is ended all of the work done in that transaction and all of the nested transactions will be committed or rolled back. The changes will be rolled back if any transaction is ended without being marked as clean (by calling setTransactionSuccessful). Otherwise they will be committed.

Here is the standard idiom for transactions:

```kotlin
db.beginTransactionWithListenerNonExclusive(listener);
    try {
      ...
      db.setTransactionSuccessful();
    } finally {
      db.endTransaction();
    }
  
```

| Parameters ||
|---|---|
| `transactionListener` | [SQLiteTransactionListener](SQLiteTransactionListener.md)?: listener that should be notified when the transaction begins, commits, or is rolled back, either explicitly or by a call to #yieldIfContendedSafely. This value may be `null`. |

### beginTransactionWithListenerReadOnly

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun beginTransactionWithListenerReadOnly(transactionListener: SQLiteTransactionListener?): Unit
```

Begins a transaction in read-only mode with a `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTransactionListener` listener. The database may not be updated inside a read-only transaction.

Transactions can be nested. However, the behavior of the transaction is not altered by nested transactions. A nested transaction may be any of the three transaction types but if the outermost type is read-only then nested transactions remain read-only, regardless of how they are started.

Here is the standard idiom for read-only transactions:

```kotlin
db.beginTransactionWightListenerReadOnly(listener);
    try {
      ...
    } finally {
      db.endTransaction();
    }
  
```

| Parameters ||
|---|---|
| `transactionListener` | [SQLiteTransactionListener](SQLiteTransactionListener.md)?: This value may be `null`. |

### compileStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compileStatement(sql: String!): SQLiteStatement!
```

Compiles an SQL statement into a reusable pre-compiled statement object. The parameters are identical to `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#execSQL(kotlin.String)`. You may put ?s in the statement and fill in those values with `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindString(kotlin.Int,%20kotlin.String)` and `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindLong(kotlin.Int,%20kotlin.Long)` each time you want to run the statement. Statements may not return result sets larger than 1x1.

No two threads should be using the same `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement` at the same time.

| Parameters ||
|---|---|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The raw SQL statement, may contain ? for unknown values to be bound later. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement!` | A pre-compiled `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement` object. Note that `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement`s are not synchronized, see the documentation for more details. |

### create

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun create(factory: SQLiteDatabase.CursorFactory?): SQLiteDatabase
```

Create a memory backed SQLite database. Its contents will be destroyed when the database is closed.

Sets the locale of the database to the system's current locale. Call `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setLocale(java.util.Locale)` if you would like something else.

| Parameters ||
|---|---|
| `factory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)?: an optional factory class that is called to instantiate a cursor when query is called. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#` | a SQLiteDatabase instance. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if the database cannot be created |

### createInMemory

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createInMemory(openParams: SQLiteDatabase.OpenParams): SQLiteDatabase
```

Create a memory backed SQLite database. Its contents will be destroyed when the database is closed.

Sets the locale of the database to the system's current locale. Call `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setLocale(java.util.Locale)` if you would like something else.

| Parameters ||
|---|---|
| `openParams` | [SQLiteDatabase.OpenParams](../android/database/sqlite/SQLiteDatabase.OpenParams.md): configuration parameters that are used for opening SQLiteDatabase. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#` | a SQLiteDatabase instance. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.database.SQLException` | if the database cannot be created |

### createRawStatement

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createRawStatement(sql: String): SQLiteRawStatement
```

Return a `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement` connected to the database. A transaction must be in progress or an exception will be thrown. The resulting object will be closed automatically when the current transaction closes.

| Parameters ||
|---|---|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The SQL string to be compiled into a prepared statement. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement` | A `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement` holding the compiled SQL. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if the SQL cannot be compiled. |
| `java.lang.IllegalStateException` | if a transaction is not in progress. |

### delete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun delete(
    table: String, 
    whereClause: String?, 
    whereArgs: Array<String!>?
): Int
```

Convenience method for deleting rows in the database.

| Parameters ||
|---|---|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the table to delete from. This value cannot be `null`. |
| `whereClause` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the optional WHERE clause to apply when deleting. Passing null will delete all rows. |
| `whereArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in the where clause, which will be replaced by the values from whereArgs. The values will be bound as Strings. If whereClause is null or does not contain ?s then whereArgs may be null. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of rows affected if a whereClause is passed in, 0 otherwise. To remove all rows and get a count pass "1" as the whereClause. |

### deleteDatabase

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun deleteDatabase(file: File): Boolean
```

Deletes a database including its journal file and other auxiliary files that may have been created by the database engine.

| Parameters ||
|---|---|
| `file` | [File](../java.io/File.md): The database file path. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the database was successfully deleted. |

### disableWriteAheadLogging

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disableWriteAheadLogging(): Unit
```

This method disables the features enabled by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()`.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if there are transactions in progress at the time this method is called. WAL mode can only be changed when there are no transactions in progress. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()`

### enableWriteAheadLogging

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun enableWriteAheadLogging(): Boolean
```

Write-ahead logging enables parallel execution of queries from multiple threads on the same database, and reduces the likelihood of stalling on filesystem syncs. Write-ahead logging is significantly faster in most scenarios.

### Benefits and Best Practices

<br />

Write-ahead logging is not enabled by default. However it is generally recommended for apps to enable write-ahead logging, unless the app uses SQLite features that are not compatible with write-ahead logging.

When write-ahead logging is enabled, write operations occur in a separate log file, which allows reads in other threads to proceed concurrently. While a write is in progress, readers on other threads will perceive the state of the database as it was before the write began. When the write completes, readers on other threads will then perceive the new state of the database.

Another benefit of write-ahead logging is that it reduces the number of `fsync` calls to the underlying file system. Calling `fsync` may block on system locks and has poor tail latency on devices with slow filesystems.

The most efficient way to enable write-ahead logging is to pass the `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int` flag to #openDatabase. This is more efficient than calling `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()`.

```kotlin
<code>
      SQLiteDatabase db = SQLiteDatabase.openDatabase("db_filename", cursorFactory,
              SQLiteDatabase.CREATE_IF_NECESSARY | SQLiteDatabase.ENABLE_WRITE_AHEAD_LOGGING,
              myDatabaseErrorHandler);
  </code>
```

### Disabling Write-ahead Logging

If the database has any attached databases, then execution of queries in parallel is NOT possible. Likewise, write-ahead logging is not supported for read-only databases or memory databases. In such cases, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()` returns false.

When write-ahead logging is not enabled (the default, or after calling `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#disableWriteAheadLogging()`), it is not possible for reads and writes to occur on the database at the same time. Before modifying the database, the writer implicitly acquires an exclusive lock on the database which prevents readers from accessing the database until the write is completed.

Write-ahead logging slightly increases the memory usage by SQLite. You can measure the impact on memory using tools like [meminfo](https://developer.android.com/tools/dumpsys#meminfo).

### Usage

After opening a database with the `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int` flag or by calling this method, execution of queries in parallel is enabled as long as the database remains open. To disable execution of queries in parallel, either call `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#disableWriteAheadLogging()` or close the database and reopen it.

Parallel execution of queries is performed by opening multiple connections to the database and using a different database connection for each query. The database journal mode is also changed to enable writes to proceed concurrently with reads. The maximum number of connections used to execute queries in parallel is dependent upon the device memory and possibly other properties.

If a query is part of a transaction, then it is executed on the same database handle the transaction was begun.

Writers should use `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#beginTransactionNonExclusive()` or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#beginTransactionWithListenerNonExclusive(android.database.sqlite.SQLiteTransactionListener)` to start a transaction. Non-exclusive mode allows database file to be in readable by other threads executing queries.

If the database has any attached databases, then execution of queries in parallel is NOT possible. Likewise, write-ahead logging is not supported for read-only databases or memory databases. In such cases, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()` returns false.

See also [SQLite Write-Ahead Logging](http://sqlite.org/wal.html) for more details about how write-ahead logging works.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if write-ahead logging is enabled. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if there are transactions in progress at the time this method is called. WAL mode can only be changed when there are no transactions in progress. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#disableWriteAheadLogging()`

### endTransaction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun endTransaction(): Unit
```

End a transaction. See beginTransaction for notes about how to use this and when transactions are committed and rolled back.

### execPerConnectionSQL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun execPerConnectionSQL(
    sql: String, 
    bindArgs: Array<Any!>?
): Unit
```

Execute the given SQL statement on all connections to this database.

This statement will be immediately executed on all existing connections, and will be automatically executed on all future connections.

Some example usages are changes like `PRAGMA trusted_schema=OFF` or functions like `SELECT icu_load_collation()`. If you execute these statements using #execSQL then they will only apply to a single database connection; using this method will ensure that they are uniformly applied to all current and future connections.

| Parameters ||
|---|---|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The SQL statement to be executed. Multiple statements separated by semicolons are not supported. This value cannot be `null`. |
| `bindArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?: The arguments that should be bound to the SQL statement. This value may be `null`. |

### execSQL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun execSQL(sql: String!): Unit
```

Execute a single SQL statement that is NOT a SELECT or any other SQL statement that returns data.

It has no means to return any data (such as the number of affected rows). Instead, you're encouraged to use `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#insert(kotlin.String,%20kotlin.String,%20android.content.ContentValues)`, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#update(kotlin.String,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array)`, et al, when possible.

When using `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()`, journal_mode is automatically managed by this class. So, do not set journal_mode using "PRAGMA journal_mode'" statement if your app is using `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()`

Note that `PRAGMA` values which apply on a per-connection basis should *not* be configured using this method; you should instead use `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#execPerConnectionSQL(kotlin.String,%20kotlin.Array)` to ensure that they are uniformly applied to all current and future connections.

| Parameters ||
|---|---|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the SQL statement to be executed. Multiple statements separated by semicolons are not supported. |

| Exceptions ||
|---|---|
| `android.database.SQLException` | if the SQL string is invalid |

### execSQL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun execSQL(
    sql: String, 
    bindArgs: Array<Any!>
): Unit
```

Execute a single SQL statement that is NOT a SELECT/INSERT/UPDATE/DELETE.

For INSERT statements, use any of the following instead.

- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#insert(kotlin.String,%20kotlin.String,%20android.content.ContentValues)`
- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#insertOrThrow(kotlin.String,%20kotlin.String,%20android.content.ContentValues)`
- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#insertWithOnConflict(kotlin.String,%20kotlin.String,%20android.content.ContentValues,%20kotlin.Int)`

For UPDATE statements, use any of the following instead.

- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#update(kotlin.String,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array)`
- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#updateWithOnConflict(kotlin.String,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array,%20kotlin.Int)`

For DELETE statements, use any of the following instead.

- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#delete(kotlin.String,%20kotlin.String,%20kotlin.Array)`

For example, the following are good candidates for using this method:

- ALTER TABLE
- CREATE or DROP table / trigger / view / index / virtual table
- REINDEX
- RELEASE
- SAVEPOINT
- PRAGMA that returns no data

<br />

When using `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()`, journal_mode is automatically managed by this class. So, do not set journal_mode using "PRAGMA journal_mode'" statement if your app is using `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()`

Note that `PRAGMA` values which apply on a per-connection basis should *not* be configured using this method; you should instead use `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#execPerConnectionSQL(kotlin.String,%20kotlin.Array)` to ensure that they are uniformly applied to all current and future connections.

| Parameters ||
|---|---|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the SQL statement to be executed. Multiple statements separated by semicolons are not supported. This value cannot be `null`. |
| `bindArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: only byte\[\], String, Long and Double are supported in bindArgs. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.database.SQLException` | if the SQL string is invalid |

### findEditTable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun findEditTable(tables: String!): String!
```

Finds the name of the first table, which is editable.

| Parameters ||
|---|---|
| `tables` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a list of tables |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the first table listed |

### getAttachedDbs

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAttachedDbs(): MutableList<Pair<String!, String!>!>!
```

Returns list of full pathnames of all attached databases including the main database by executing 'pragma database_list' on the database.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/util/Pair.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>!` | ArrayList of pairs of (database name, database file path) or null if the database is not open. |

### getLastChangedRowCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLastChangedRowCount(): Long
```

Return the number of database rows that were inserted, updated, or deleted by the most recent SQL statement within the current transaction.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The number of rows changed by the most recent sql statement |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if there is no current transaction. |

**See Also**

### getLastInsertRowId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLastInsertRowId(): Long
```

Return the "rowid" of the last row to be inserted on the current connection. This method must only be called when inside a transaction. `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` is thrown if the method is called outside a transaction. If the function is called before any inserts in the current transaction, the value returned will be from a previous transaction, which may be from a different thread. If no inserts have occurred on the current connection, the function returns 0. See the SQLite documentation for the specific details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The ROWID of the last row to be inserted under this connection. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if there is no current transaction. |

**See Also**

### getMaximumSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaximumSize(): Long
```

Returns the maximum size the database may grow to.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the new maximum database size |

### getPageSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPageSize(): Long
```

Returns the current database page size, in bytes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the database page size, in bytes |

### getPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPath(): String!
```

Gets the path to the database file.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The path to the database file. |

### getSyncedTables

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSyncedTables(): MutableMap<String!, String!>!
```

**Deprecated:** *This method no longer serves any useful purpose and has been deprecated.*

Deprecated.

### getTotalChangedRowCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTotalChangedRowCount(): Long
```

Return the total number of database rows that have been inserted, updated, or deleted on the current connection since it was created. Due to Android's internal management of SQLite connections, the value may, or may not, include changes made in earlier transactions. Best practice is to compare values returned within a single transaction. `
`

 database.beginTransaction();
 try {
 long initialValue = database.getTotalChangedRowCount();
 // Execute SQL statements
 long changedRows = database.getTotalChangedRowCount() - initialValue;
 // changedRows counts the total number of rows updated in the transaction.
 } finally {
 database.endTransaction();
 }
 
`
`

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The number of rows changed on the current connection. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if there is no current transaction. |

**See Also**

### getVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVersion(): Int
```

Gets the database version.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the database version |

### inTransaction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun inTransaction(): Boolean
```

Returns true if the current thread has a transaction pending.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the current thread is in a transaction. |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    table: String, 
    nullColumnHack: String?, 
    values: ContentValues?
): Long
```

Convenience method for inserting a row into the database.

| Parameters ||
|---|---|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the table to insert the row into. This value cannot be `null`. |
| `nullColumnHack` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: optional; may be `null`. SQL doesn't allow inserting a completely empty row without naming at least one column name. If your provided `values` is empty, no column names are known and an empty row can't be inserted. If not set to null, the `nullColumnHack` parameter provides the name of nullable column name to explicitly insert a NULL into in the case where your `values` is empty. |
| `values` | [ContentValues](../android.content/ContentValues.md)?: this map contains the initial column values for the row. The keys should be the column names and the values the column values. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the row ID of the newly inserted row, or -1 if an error occurred |

### insertOrThrow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insertOrThrow(
    table: String, 
    nullColumnHack: String?, 
    values: ContentValues?
): Long
```

Convenience method for inserting a row into the database.

| Parameters ||
|---|---|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the table to insert the row into. This value cannot be `null`. |
| `nullColumnHack` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: optional; may be `null`. SQL doesn't allow inserting a completely empty row without naming at least one column name. If your provided `values` is empty, no column names are known and an empty row can't be inserted. If not set to null, the `nullColumnHack` parameter provides the name of nullable column name to explicitly insert a NULL into in the case where your `values` is empty. |
| `values` | [ContentValues](../android.content/ContentValues.md)?: this map contains the initial column values for the row. The keys should be the column names and the values the column values. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the row ID of the newly inserted row, or -1 if an error occurred |

| Exceptions ||
|---|---|
| `android.database.SQLException` | |

### insertWithOnConflict

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insertWithOnConflict(
    table: String, 
    nullColumnHack: String?, 
    initialValues: ContentValues?, 
    conflictAlgorithm: Int
): Long
```

General method for inserting a row into the database.

| Parameters ||
|---|---|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the table to insert the row into. This value cannot be `null`. |
| `nullColumnHack` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: optional; may be `null`. SQL doesn't allow inserting a completely empty row without naming at least one column name. If your provided `initialValues` is empty, no column names are known and an empty row can't be inserted. If not set to null, the `nullColumnHack` parameter provides the name of nullable column name to explicitly insert a NULL into in the case where your `initialValues` is empty. |
| `initialValues` | [ContentValues](../android.content/ContentValues.md)?: this map contains the initial column values for the row. The keys should be the column names and the values the column values. This value may be `null`. |
| --- | --- |
| `conflictAlgorithm` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): for insert conflict resolver |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the row ID of the newly inserted row OR `-1` if either the input parameter `conflictAlgorithm` = `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CONFLICT_IGNORE:kotlin.Int` or an error occurred. |

### isDatabaseIntegrityOk

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDatabaseIntegrityOk(): Boolean
```

Runs 'pragma integrity_check' on the given database (and all the attached databases) and returns true if the given database (and all its attached databases) pass integrity_check, false otherwise.

If the result is false, then this method logs the errors reported by the integrity_check command execution.

Note that 'pragma integrity_check' on a database can take a long time.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the given database (and all its attached databases) pass integrity_check, false otherwise. |

### isDbLockedByCurrentThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDbLockedByCurrentThread(): Boolean
```

Returns true if the current thread is holding an active connection to the database.

The name of this method comes from a time when having an active connection to the database meant that the thread was holding an actual lock on the database. Nowadays, there is no longer a true "database lock" although threads may block if they cannot acquire a database connection to perform a particular operation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the current thread is holding an active connection to the database. |

### isDbLockedByOtherThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDbLockedByOtherThreads(): Boolean
```

**Deprecated:** *Always returns false. Do not use this method.*

Always returns false.

There is no longer the concept of a database lock, so this method always returns false.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | False. |

### isOpen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOpen(): Boolean
```

Returns true if the database is currently open.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the database is currently open (has not been closed). |

### isReadOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isReadOnly(): Boolean
```

Returns true if the database is opened as read only.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if database is opened as read only. |

### isWriteAheadLoggingEnabled

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isWriteAheadLoggingEnabled(): Boolean
```

Returns true if write-ahead logging has been enabled for this database.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if write-ahead logging has been enabled for this database. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()`
- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int`

### markTableSyncable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun markTableSyncable(
    table: String!, 
    deletedTable: String!
): Unit
```

**Deprecated:** *This method no longer serves any useful purpose and has been deprecated.*

Mark this table as syncable. When an update occurs in this table the _sync_dirty field will be set to ensure proper syncing operation.

| Parameters ||
|---|---|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the table to mark as syncable |
| `deletedTable` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The deleted table that corresponds to the syncable table |

### markTableSyncable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun markTableSyncable(
    table: String!, 
    foreignKey: String!, 
    updateTable: String!
): Unit
```

**Deprecated:** *This method no longer serves any useful purpose and has been deprecated.*

Mark this table as syncable, with the _sync_dirty residing in another table. When an update occurs in this table the _sync_dirty field of the row in updateTable with the _id in foreignKey will be set to ensure proper syncing operation.

| Parameters ||
|---|---|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: an update on this table will trigger a sync time removal |
| `foreignKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: this is the column in table whose value is an _id in updateTable |
| `updateTable` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: this is the table that will have its _sync_dirty |
| --- | --- |

### needUpgrade

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun needUpgrade(newVersion: Int): Boolean
```

Returns true if the new version code is greater than the current database version.

| Parameters ||
|---|---|
| `newVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new version code. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the new version code is greater than the current database version. |

### openDatabase

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun openDatabase(
    path: File, 
    openParams: SQLiteDatabase.OpenParams
): SQLiteDatabase!
```

Open the database according to the specified `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.OpenParams`

| Parameters ||
|---|---|
| `path` | [File](../java.io/File.md): path to database file to open and/or create. **Important:** The file should be constructed either from an absolute path or by using `https://developer.android.com/reference/kotlin/android/content/Context.html#getDatabasePath(kotlin.String)`. This value cannot be `null`. |
| `openParams` | [SQLiteDatabase.OpenParams](../android/database/sqlite/SQLiteDatabase.OpenParams.md): configuration parameters that are used for opening `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#` This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#!` | the newly opened database |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if the database cannot be opened |

### openDatabase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun openDatabase(
    path: String, 
    factory: SQLiteDatabase.CursorFactory?, 
    flags: Int
): SQLiteDatabase!
```

Open the database according to the flags `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READWRITE:kotlin.Int` `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READONLY:kotlin.Int` `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CREATE_IF_NECESSARY:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#NO_LOCALIZED_COLLATORS:kotlin.Int`.

Sets the locale of the database to the system's current locale. Call `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setLocale(java.util.Locale)` if you would like something else.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): to database file to open and/or create. This value cannot be `null`. |
| `factory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)?: an optional factory class that is called to instantiate a cursor when query is called, or null for default |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): to control database access mode. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READWRITE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CREATE_IF_NECESSARY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#NO_LOCALIZED_COLLATORS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#!` | the newly opened database |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if the database cannot be opened |

### openDatabase

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun openDatabase(
    path: String, 
    factory: SQLiteDatabase.CursorFactory?, 
    flags: Int, 
    errorHandler: DatabaseErrorHandler?
): SQLiteDatabase!
```

Open the database according to the flags `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READWRITE:kotlin.Int``https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READONLY:kotlin.Int``https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CREATE_IF_NECESSARY:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#NO_LOCALIZED_COLLATORS:kotlin.Int`.

Sets the locale of the database to the system's current locale. Call `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setLocale(java.util.Locale)` if you would like something else.

Accepts input param: a concrete instance of `https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#` to be used to handle corruption when sqlite reports database corruption.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): to database file to open and/or create. This value cannot be `null`. |
| `factory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)?: an optional factory class that is called to instantiate a cursor when query is called, or null for default |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): to control database access mode. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READWRITE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#OPEN_READONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CREATE_IF_NECESSARY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#NO_LOCALIZED_COLLATORS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int` |
| --- | --- |
| `errorHandler` | [DatabaseErrorHandler](../android.database/DatabaseErrorHandler.md)?: the `https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#` obj to be used to handle corruption when sqlite reports database corruption. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#!` | the newly opened database |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if the database cannot be opened |

### openOrCreateDatabase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun openOrCreateDatabase(
    file: File, 
    factory: SQLiteDatabase.CursorFactory?
): SQLiteDatabase!
```

Equivalent to openDatabase(file.getPath(), factory, CREATE_IF_NECESSARY).

| Parameters ||
|---|---|
| `file` | [File](../java.io/File.md): This value cannot be `null`. |
| `factory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)?: This value may be `null`. |

### openOrCreateDatabase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun openOrCreateDatabase(
    path: String, 
    factory: SQLiteDatabase.CursorFactory?
): SQLiteDatabase!
```

Equivalent to openDatabase(path, factory, CREATE_IF_NECESSARY).

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `factory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)?: This value may be `null`. |

### openOrCreateDatabase

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun openOrCreateDatabase(
    path: String, 
    factory: SQLiteDatabase.CursorFactory?, 
    errorHandler: DatabaseErrorHandler?
): SQLiteDatabase!
```

Equivalent to openDatabase(path, factory, CREATE_IF_NECESSARY, errorHandler).

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `factory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)?: This value may be `null`. |
| `errorHandler` | [DatabaseErrorHandler](../android.database/DatabaseErrorHandler.md)?: This value may be `null`. |
| --- | --- |

### query

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun query(
    distinct: Boolean, 
    table: String, 
    columns: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    groupBy: String?, 
    having: String?, 
    orderBy: String?, 
    limit: String?
): Cursor
```

Query the given URL, returning a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set.

| Parameters ||
|---|---|
| `distinct` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if you want each row to be unique, false otherwise. |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The table name to compile the query against. This value cannot be `null`. |
| `columns` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| --- | --- |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declaring which rows to return, formatted as an SQL WHERE clause (excluding the WHERE itself). Passing null will return all rows for the given table. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in selection, which will be replaced by the values from selectionArgs, in the order that they appear in the selection. The values will be bound as Strings. If selection is null or does not contain ?s then selectionArgs may be null. |
| `groupBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declaring how to group rows, formatted as an SQL GROUP BY clause (excluding the GROUP BY itself). Passing null will cause the rows to not be grouped. |
| --- | --- |
| `having` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declare which row groups to include in the cursor, if row grouping is being used, formatted as an SQL HAVING clause (excluding the HAVING itself). Passing null will cause all row groups to be included, and is required when row grouping is not being used. |
| `orderBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: How to order the rows, formatted as an SQL ORDER BY clause (excluding the ORDER BY itself). Passing null will use the default sort order, which may be unordered. |
| `limit` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Limits the number of rows returned by the query, formatted as LIMIT clause. Passing null denotes no LIMIT clause. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | A `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object, which is positioned before the first entry. Note that `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`s are not synchronized, see the documentation for more details. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`

### query

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun query(
    distinct: Boolean, 
    table: String, 
    columns: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    groupBy: String?, 
    having: String?, 
    orderBy: String?, 
    limit: String?, 
    cancellationSignal: CancellationSignal?
): Cursor
```

Query the given URL, returning a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set.

| Parameters ||
|---|---|
| `distinct` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if you want each row to be unique, false otherwise. |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The table name to compile the query against. This value cannot be `null`. |
| `columns` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| --- | --- |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declaring which rows to return, formatted as an SQL WHERE clause (excluding the WHERE itself). Passing null will return all rows for the given table. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in selection, which will be replaced by the values from selectionArgs, in the order that they appear in the selection. The values will be bound as Strings. If selection is null or does not contain ?s then selectionArgs may be null. |
| `groupBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declaring how to group rows, formatted as an SQL GROUP BY clause (excluding the GROUP BY itself). Passing null will cause the rows to not be grouped. |
| --- | --- |
| `having` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declare which row groups to include in the cursor, if row grouping is being used, formatted as an SQL HAVING clause (excluding the HAVING itself). Passing null will cause all row groups to be included, and is required when row grouping is not being used. |
| `orderBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: How to order the rows, formatted as an SQL ORDER BY clause (excluding the ORDER BY itself). Passing null will use the default sort order, which may be unordered. |
| `limit` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Limits the number of rows returned by the query, formatted as LIMIT clause. Passing null denotes no LIMIT clause. |
| --- | --- |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: A signal to cancel the operation in progress, or null if none. If the operation is canceled, then `https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#` will be thrown when the query is executed. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | A `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object, which is positioned before the first entry. Note that `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`s are not synchronized, see the documentation for more details. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`

### query

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun query(
    table: String, 
    columns: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    groupBy: String?, 
    having: String?, 
    orderBy: String?
): Cursor
```

Query the given table, returning a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set.

| Parameters ||
|---|---|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The table name to compile the query against. This value cannot be `null`. |
| `columns` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declaring which rows to return, formatted as an SQL WHERE clause (excluding the WHERE itself). Passing null will return all rows for the given table. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in selection, which will be replaced by the values from selectionArgs, in the order that they appear in the selection. The values will be bound as Strings. If selection is null or does not contain ?s then selectionArgs may be null. |
| `groupBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declaring how to group rows, formatted as an SQL GROUP BY clause (excluding the GROUP BY itself). Passing null will cause the rows to not be grouped. |
| `having` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declare which row groups to include in the cursor, if row grouping is being used, formatted as an SQL HAVING clause (excluding the HAVING itself). Passing null will cause all row groups to be included, and is required when row grouping is not being used. |
| --- | --- |
| `orderBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: How to order the rows, formatted as an SQL ORDER BY clause (excluding the ORDER BY itself). Passing null will use the default sort order, which may be unordered. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | A `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object, which is positioned before the first entry. Note that `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`s are not synchronized, see the documentation for more details. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`

### query

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun query(
    table: String, 
    columns: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    groupBy: String?, 
    having: String?, 
    orderBy: String?, 
    limit: String?
): Cursor
```

Query the given table, returning a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set.

| Parameters ||
|---|---|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The table name to compile the query against. This value cannot be `null`. |
| `columns` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declaring which rows to return, formatted as an SQL WHERE clause (excluding the WHERE itself). Passing null will return all rows for the given table. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in selection, which will be replaced by the values from selectionArgs, in the order that they appear in the selection. The values will be bound as Strings. If selection is null or does not contain ?s then selectionArgs may be null. |
| `groupBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declaring how to group rows, formatted as an SQL GROUP BY clause (excluding the GROUP BY itself). Passing null will cause the rows to not be grouped. |
| `having` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declare which row groups to include in the cursor, if row grouping is being used, formatted as an SQL HAVING clause (excluding the HAVING itself). Passing null will cause all row groups to be included, and is required when row grouping is not being used. |
| --- | --- |
| `orderBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: How to order the rows, formatted as an SQL ORDER BY clause (excluding the ORDER BY itself). Passing null will use the default sort order, which may be unordered. |
| `limit` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Limits the number of rows returned by the query, formatted as LIMIT clause. Passing null denotes no LIMIT clause. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | A `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object, which is positioned before the first entry. Note that `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`s are not synchronized, see the documentation for more details. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`

### queryWithFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queryWithFactory(
    cursorFactory: SQLiteDatabase.CursorFactory?, 
    distinct: Boolean, 
    table: String, 
    columns: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    groupBy: String?, 
    having: String?, 
    orderBy: String?, 
    limit: String?
): Cursor
```

Query the given URL, returning a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set.

| Parameters ||
|---|---|
| `cursorFactory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)?: the cursor factory to use, or null for the default factory |
| `distinct` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if you want each row to be unique, false otherwise. |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The table name to compile the query against. This value cannot be `null`. |
| --- | --- |
| `columns` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declaring which rows to return, formatted as an SQL WHERE clause (excluding the WHERE itself). Passing null will return all rows for the given table. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in selection, which will be replaced by the values from selectionArgs, in the order that they appear in the selection. The values will be bound as Strings. If selection is null or does not contain ?s then selectionArgs may be null. |
| --- | --- |
| `groupBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declaring how to group rows, formatted as an SQL GROUP BY clause (excluding the GROUP BY itself). Passing null will cause the rows to not be grouped. |
| `having` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declare which row groups to include in the cursor, if row grouping is being used, formatted as an SQL HAVING clause (excluding the HAVING itself). Passing null will cause all row groups to be included, and is required when row grouping is not being used. |
| `orderBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: How to order the rows, formatted as an SQL ORDER BY clause (excluding the ORDER BY itself). Passing null will use the default sort order, which may be unordered. |
| --- | --- |
| `limit` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Limits the number of rows returned by the query, formatted as LIMIT clause. Passing null denotes no LIMIT clause. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | A `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object, which is positioned before the first entry. Note that `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`s are not synchronized, see the documentation for more details. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`

### queryWithFactory

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queryWithFactory(
    cursorFactory: SQLiteDatabase.CursorFactory?, 
    distinct: Boolean, 
    table: String, 
    columns: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    groupBy: String?, 
    having: String?, 
    orderBy: String?, 
    limit: String?, 
    cancellationSignal: CancellationSignal?
): Cursor
```

Query the given URL, returning a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set.

| Parameters ||
|---|---|
| `cursorFactory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)?: the cursor factory to use, or null for the default factory |
| `distinct` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if you want each row to be unique, false otherwise. |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The table name to compile the query against. This value cannot be `null`. |
| --- | --- |
| `columns` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declaring which rows to return, formatted as an SQL WHERE clause (excluding the WHERE itself). Passing null will return all rows for the given table. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in selection, which will be replaced by the values from selectionArgs, in the order that they appear in the selection. The values will be bound as Strings. If selection is null or does not contain ?s then selectionArgs may be null. |
| --- | --- |
| `groupBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declaring how to group rows, formatted as an SQL GROUP BY clause (excluding the GROUP BY itself). Passing null will cause the rows to not be grouped. |
| `having` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A filter declare which row groups to include in the cursor, if row grouping is being used, formatted as an SQL HAVING clause (excluding the HAVING itself). Passing null will cause all row groups to be included, and is required when row grouping is not being used. |
| `orderBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: How to order the rows, formatted as an SQL ORDER BY clause (excluding the ORDER BY itself). Passing null will use the default sort order, which may be unordered. |
| --- | --- |
| `limit` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Limits the number of rows returned by the query, formatted as LIMIT clause. Passing null denotes no LIMIT clause. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: A signal to cancel the operation in progress, or null if none. If the operation is canceled, then `https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#` will be thrown when the query is executed. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | A `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object, which is positioned before the first entry. Note that `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`s are not synchronized, see the documentation for more details. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`

### rawQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun rawQuery(
    sql: String, 
    selectionArgs: Array<String!>?
): Cursor
```

Runs the provided SQL and returns a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set.

| Parameters ||
|---|---|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the SQL query. The SQL string must not be ; terminated. This value cannot be `null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in where clause in the query, which will be replaced by the values from selectionArgs. The values will be bound as Strings. If selection is null or does not contain ?s then selectionArgs may be null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | A `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object, which is positioned before the first entry. Note that `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`s are not synchronized, see the documentation for more details. This value cannot be `null`. |

### rawQuery

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun rawQuery(
    sql: String, 
    selectionArgs: Array<String!>?, 
    cancellationSignal: CancellationSignal?
): Cursor
```

Runs the provided SQL and returns a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` over the result set.

| Parameters ||
|---|---|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the SQL query. The SQL string must not be ; terminated. This value cannot be `null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in where clause in the query, which will be replaced by the values from selectionArgs. The values will be bound as Strings. If selection is null or does not contain ?s then selectionArgs may be null. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: A signal to cancel the operation in progress, or null if none. If the operation is canceled, then `https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#` will be thrown when the query is executed. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | A `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object, which is positioned before the first entry. Note that `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`s are not synchronized, see the documentation for more details. This value cannot be `null`. |

### rawQueryWithFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun rawQueryWithFactory(
    cursorFactory: SQLiteDatabase.CursorFactory?, 
    sql: String, 
    selectionArgs: Array<String!>?, 
    editTable: String
): Cursor
```

Runs the provided SQL and returns a cursor over the result set.

| Parameters ||
|---|---|
| `cursorFactory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)?: the cursor factory to use, or null for the default factory |
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the SQL query. The SQL string must not be ; terminated. This value cannot be `null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in where clause in the query, which will be replaced by the values from selectionArgs. The values will be bound as Strings. If selection is null or does not contain ?s then selectionArgs may be null. |
| --- | --- |
| `editTable` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the first table, which is editable. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | A `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object, which is positioned before the first entry. Note that `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`s are not synchronized, see the documentation for more details. This value cannot be `null`. |

### rawQueryWithFactory

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun rawQueryWithFactory(
    cursorFactory: SQLiteDatabase.CursorFactory?, 
    sql: String, 
    selectionArgs: Array<String!>?, 
    editTable: String, 
    cancellationSignal: CancellationSignal?
): Cursor
```

Runs the provided SQL and returns a cursor over the result set.

| Parameters ||
|---|---|
| `cursorFactory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)?: the cursor factory to use, or null for the default factory |
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the SQL query. The SQL string must not be ; terminated. This value cannot be `null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in where clause in the query, which will be replaced by the values from selectionArgs. The values will be bound as Strings. If selection is null or does not contain ?s then selectionArgs may be null. |
| --- | --- |
| `editTable` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the first table, which is editable. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: A signal to cancel the operation in progress, or null if none. If the operation is canceled, then `https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#` will be thrown when the query is executed. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | A `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object, which is positioned before the first entry. Note that `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`s are not synchronized, see the documentation for more details. This value cannot be `null`. |

### releaseMemory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun releaseMemory(): Int
```

Attempts to release memory that SQLite holds but does not require to operate properly. Typically this memory will come from the page cache.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of bytes actually released |

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun replace(
    table: String, 
    nullColumnHack: String?, 
    initialValues: ContentValues?
): Long
```

Convenience method for replacing a row in the database. Inserts a new row if a row does not already exist.

| Parameters ||
|---|---|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the table in which to replace the row. This value cannot be `null`. |
| `nullColumnHack` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: optional; may be `null`. SQL doesn't allow inserting a completely empty row without naming at least one column name. If your provided `initialValues` is empty, no column names are known and an empty row can't be inserted. If not set to null, the `nullColumnHack` parameter provides the name of nullable column name to explicitly insert a NULL into in the case where your `initialValues` is empty. |
| `initialValues` | [ContentValues](../android.content/ContentValues.md)?: this map contains the initial column values for the row. The keys should be the column names and the values the column values. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the row ID of the newly inserted row, or -1 if an error occurred |

### replaceOrThrow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun replaceOrThrow(
    table: String, 
    nullColumnHack: String?, 
    initialValues: ContentValues?
): Long
```

Convenience method for replacing a row in the database. Inserts a new row if a row does not already exist.

| Parameters ||
|---|---|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the table in which to replace the row. This value cannot be `null`. |
| `nullColumnHack` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: optional; may be `null`. SQL doesn't allow inserting a completely empty row without naming at least one column name. If your provided `initialValues` is empty, no column names are known and an empty row can't be inserted. If not set to null, the `nullColumnHack` parameter provides the name of nullable column name to explicitly insert a NULL into in the case where your `initialValues` is empty. |
| `initialValues` | [ContentValues](../android.content/ContentValues.md)?: this map contains the initial column values for the row. The keys should be the column names and the values the column values. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the row ID of the newly inserted row, or -1 if an error occurred |

| Exceptions ||
|---|---|
| `android.database.SQLException` | |

### setCustomAggregateFunction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCustomAggregateFunction(
    functionName: String, 
    aggregateFunction: BinaryOperator<String!>
): Unit
```

Register a custom aggregate function that can be called from SQL expressions.

For example, registering a custom aggregation function named `LONGEST` could be used in a query like `SELECT LONGEST(name) FROM employees`.

The implementation of this method follows the reduction flow outlined in `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#reduce(java.util.function.BinaryOperator)`, and the custom aggregation function is expected to be an associative accumulation function, as defined by that class.

When attempting to register multiple functions with the same function name, SQLite will replace any previously defined functions with the latest definition, regardless of what function type they are. SQLite does not support unregistering functions.

| Parameters ||
|---|---|
| `functionName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Case-insensitive name to register this function under, limited to 255 UTF-8 bytes in length. This value cannot be `null`. |
| `aggregateFunction` | [BinaryOperator](../java.util.function/BinaryOperator.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: Functional interface that will be invoked when the function name is used by a SQL statement. The argument values from the SQL statement are passed to the functional interface, and the return values from the functional interface are returned back into the SQL statement. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if the custom function could not be registered. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setCustomScalarFunction(kotlin.String,%20java.util.function.UnaryOperator)`

### setCustomScalarFunction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCustomScalarFunction(
    functionName: String, 
    scalarFunction: UnaryOperator<String!>
): Unit
```

Register a custom scalar function that can be called from SQL expressions.

For example, registering a custom scalar function named `REVERSE` could be used in a query like `SELECT REVERSE(name) FROM employees`.

When attempting to register multiple functions with the same function name, SQLite will replace any previously defined functions with the latest definition, regardless of what function type they are. SQLite does not support unregistering functions.

| Parameters ||
|---|---|
| `functionName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Case-insensitive name to register this function under, limited to 255 UTF-8 bytes in length. This value cannot be `null`. |
| `scalarFunction` | [UnaryOperator](../java.util.function/UnaryOperator.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: Functional interface that will be invoked when the function name is used by a SQL statement. The argument values from the SQL statement are passed to the functional interface, and the return values from the functional interface are returned back into the SQL statement. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if the custom function could not be registered. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setCustomAggregateFunction(kotlin.String,%20java.util.function.BinaryOperator)`

### setForeignKeyConstraintsEnabled

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setForeignKeyConstraintsEnabled(enable: Boolean): Unit
```

Sets whether foreign key constraints are enabled for the database.

By default, foreign key constraints are not enforced by the database. This method allows an application to enable foreign key constraints. It must be called each time the database is opened to ensure that foreign key constraints are enabled for the session.

A good time to call this method is right after calling #openOrCreateDatabase or in the `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onConfigure(android.database.sqlite.SQLiteDatabase)` callback.

When foreign key constraints are disabled, the database does not check whether changes to the database will violate foreign key constraints. Likewise, when foreign key constraints are disabled, the database will not execute cascade delete or update triggers. As a result, it is possible for the database state to become inconsistent. To perform a database integrity check, call `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#isDatabaseIntegrityOk()`.

This method must not be called while a transaction is in progress.

See also [SQLite Foreign Key Constraints](http://sqlite.org/foreignkeys.html) for more details about foreign key constraint support.

| Parameters ||
|---|---|
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True to enable foreign key constraints, false to disable them. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the are transactions is in progress when this method is called. |

### setLocale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setLocale(locale: Locale!): Unit
```

Sets the locale for this database. Does nothing if this database has the `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#NO_LOCALIZED_COLLATORS:kotlin.Int` flag set or was opened read only.

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md)!: The new locale. |

| Exceptions ||
|---|---|
| `android.database.SQLException` | if the locale could not be set. The most common reason for this is that there is no collator available for the locale you requested. In this case the database remains unchanged. |

### setLockingEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setLockingEnabled(lockingEnabled: Boolean): Unit
```

**Deprecated:** *This method now does nothing. Do not use.*

Control whether or not the SQLiteDatabase is made thread-safe by using locks around critical sections. This is pretty expensive, so if you know that your DB will only be used by a single thread then you should set this to false. The default is true.

| Parameters ||
|---|---|
| `lockingEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set to true to enable locks, false otherwise |

### setMaxSqlCacheSize

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setMaxSqlCacheSize(cacheSize: Int): Unit
```

Sets the maximum size of the prepared-statement cache for this database. (size of the cache = number of compiled-sql-statements stored in the cache).

Maximum cache size can ONLY be increased from its current size (default = 10). If this method is called with smaller size than the current maximum value, then IllegalStateException is thrown.

This method is thread-safe.

| Parameters ||
|---|---|
| `cacheSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the size of the cache. can be (0 to `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#MAX_SQL_CACHE_SIZE:kotlin.Int`) |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if input cacheSize \> `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#MAX_SQL_CACHE_SIZE:kotlin.Int`. |

### setMaximumSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setMaximumSize(numBytes: Long): Long
```

Sets the maximum size the database will grow to. The maximum size cannot be set below the current size.

| Parameters ||
|---|---|
| `numBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum database size, in bytes |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the new maximum database size |

### setPageSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPageSize(numBytes: Long): Unit
```

Sets the database page size. The page size must be a power of two. This method does not work if any data has been written to the database file, and must be called right after the database has been created.

| Parameters ||
|---|---|
| `numBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the database page size, in bytes |

### setTransactionSuccessful

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTransactionSuccessful(): Unit
```

Marks the current transaction as successful. Do not do any more database work between calling this and calling endTransaction. Do as little non-database work as possible in that situation too. If any errors are encountered between this and endTransaction the transaction will still be committed.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the current thread is not in a transaction or the transaction is already marked as successful. |

### setVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setVersion(version: Int): Unit
```

Sets the database version.

| Parameters ||
|---|---|
| `version` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new database version |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun update(
    table: String, 
    values: ContentValues?, 
    whereClause: String?, 
    whereArgs: Array<String!>?
): Int
```

Convenience method for updating rows in the database.

| Parameters ||
|---|---|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the table to update in. This value cannot be `null`. |
| `values` | [ContentValues](../android.content/ContentValues.md)?: a map from column names to new column values. null is a valid value that will be translated to NULL. |
| `whereClause` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the optional WHERE clause to apply when updating. Passing null will update all rows. |
| --- | --- |
| `whereArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in the where clause, which will be replaced by the values from whereArgs. The values will be bound as Strings. If whereClause is null or does not contain ?s then whereArgs may be null. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of rows affected |

### updateWithOnConflict

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun updateWithOnConflict(
    table: String, 
    values: ContentValues?, 
    whereClause: String?, 
    whereArgs: Array<String!>?, 
    conflictAlgorithm: Int
): Int
```

Convenience method for updating rows in the database.

| Parameters ||
|---|---|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the table to update in. This value cannot be `null`. |
| `values` | [ContentValues](../android.content/ContentValues.md)?: a map from column names to new column values. null is a valid value that will be translated to NULL. |
| `whereClause` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the optional WHERE clause to apply when updating. Passing null will update all rows. |
| --- | --- |
| `whereArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in the where clause, which will be replaced by the values from whereArgs. The values will be bound as Strings. If whereClause is null or does not contain ?s then whereArgs may be null. |
| `conflictAlgorithm` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): for update conflict resolver |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of rows affected |

### validateSql

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun validateSql(
    sql: String, 
    cancellationSignal: CancellationSignal?
): Unit
```

Verifies that a SQL SELECT statement is valid by compiling it. If the SQL statement is not valid, this method will throw a `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException`.

| Parameters ||
|---|---|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): SQL to be validated. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: A signal to cancel the operation in progress, or null if none. If the operation is canceled, then `https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#` will be thrown when the query is executed. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if `sql` is invalid |

### yieldIfContended

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun yieldIfContended(): Boolean
```

**Deprecated:** *if the db is locked more than once (because of nested transactions) then the lock will not be yielded. Use yieldIfContendedSafely instead.*

Temporarily end the transaction to let other threads run. The transaction is assumed to be successful so far. Do not call setTransactionSuccessful before calling this. When this returns a new transaction will have been created but not marked as successful.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the transaction was yielded |

### yieldIfContendedSafely

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun yieldIfContendedSafely(): Boolean
```

Temporarily end the transaction to let other threads run. The transaction is assumed to be successful so far. Do not call setTransactionSuccessful before calling this. When this returns a new transaction will have been created but not marked as successful. This assumes that there are no nested transactions (beginTransaction has only been called once) and will throw an exception if that is not the case.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the transaction was yielded |

### yieldIfContendedSafely

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun yieldIfContendedSafely(sleepAfterYieldDelay: Long): Boolean
```

Temporarily end the transaction to let other threads run. The transaction is assumed to be successful so far. Do not call setTransactionSuccessful before calling this. When this returns a new transaction will have been created but not marked as successful. This assumes that there are no nested transactions (beginTransaction has only been called once) and will throw an exception if that is not the case.

| Parameters ||
|---|---|
| `sleepAfterYieldDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): if \> 0, sleep this long before starting a new transaction if the lock was actually yielded. This will allow other background threads to make some more progress than they would if we started the transaction immediately. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the transaction was yielded |

## Protected methods

### onAllReferencesReleased

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun onAllReferencesReleased(): Unit
```

Called when the last reference to the object was released by a call to `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference()` or #close().
