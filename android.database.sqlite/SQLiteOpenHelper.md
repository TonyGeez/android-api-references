Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteOpenHelper

Kotlin | [Java](SQLiteOpenHelper.md)
| --- | --- |

```
abstract class SQLiteOpenHelper : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.database.sqlite.SQLiteOpenHelper](SQLiteOpenHelper.md) |

A helper class to manage database creation and version management.

You create a subclass implementing `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onCreate(android.database.sqlite.SQLiteDatabase)`, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onUpgrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)` and optionally `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onOpen(android.database.sqlite.SQLiteDatabase)`, and this class takes care of opening the database if it exists, creating it if it does not, and upgrading it as necessary. Transactions are used to make sure the database is always in a sensible state.

This class makes it easy for `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` implementations to defer opening and upgrading the database until first use, to avoid blocking application startup with long-running database upgrades.

For an example, see the NotePadProvider class in the NotePad sample application, in the *samples/* directory of the SDK.

**Note:** this class assumes monotonically increasing version numbers for upgrades.

**Note:** the `https://developer.android.com/reference/kotlin/java/lang/AutoCloseable.html#` interface was first added in the `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` release.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#SQLiteOpenHelper(android.content.Context,%20kotlin.String,%20android.database.sqlite.SQLiteDatabase.CursorFactory,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#?, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory?, version: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a helper object to create, open, and/or manage a database. |
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#SQLiteOpenHelper(android.content.Context,%20kotlin.String,%20android.database.sqlite.SQLiteDatabase.CursorFactory,%20kotlin.Int,%20android.database.DatabaseErrorHandler)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#?, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory?, version: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, errorHandler: https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#?)` Create a helper object to create, open, and/or manage a database. |
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#SQLiteOpenHelper(android.content.Context,%20kotlin.String,%20kotlin.Int,%20android.database.sqlite.SQLiteDatabase.OpenParams)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#?, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, version: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, openParams: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.OpenParams)` Create a helper object to create, open, and/or manage a database. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#close()()` Close any open database object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getDatabaseName()()` Return the name of the SQLite database being opened, as given to the constructor. |
| open [SQLiteDatabase](SQLiteDatabase.md)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getReadableDatabase()()` Create and/or open a database. |
| --- | --- |
| open [SQLiteDatabase](SQLiteDatabase.md)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getWritableDatabase()()` Create and/or open a database that will be used for reading and writing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onConfigure(android.database.sqlite.SQLiteDatabase)(db: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!)` Called when the database connection is being configured, to enable features such as write-ahead logging or foreign key support. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onCreate(android.database.sqlite.SQLiteDatabase)(db: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!)` Called when the database is created for the first time. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onDowngrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)(db: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!, oldVersion: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newVersion: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when the database needs to be downgraded. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onOpen(android.database.sqlite.SQLiteDatabase)(db: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!)` Called when the database has been opened. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onUpgrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)(db: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!, oldVersion: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newVersion: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when the database needs to be upgraded. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#setIdleConnectionTimeout(kotlin.Long)(idleConnectionTimeoutMs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the maximum number of milliseconds that SQLite connection is allowed to be idle before it is closed and removed from the pool. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#setLookasideConfig(kotlin.Int,%20kotlin.Int)(slotSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, slotCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Configures [lookaside memory allocator](https://sqlite.org/malloc.html#lookaside) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#setOpenParams(android.database.sqlite.SQLiteDatabase.OpenParams)(openParams: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.OpenParams)` Sets configuration parameters that are used for opening `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#setWriteAheadLoggingEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enables or disables the use of write-ahead logging for the database. |

## Public constructors

### SQLiteOpenHelper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SQLiteOpenHelper(
    context: Context?, 
    name: String?, 
    factory: SQLiteDatabase.CursorFactory?, 
    version: Int)
```

Create a helper object to create, open, and/or manage a database. This method always returns very quickly. The database is not actually created or opened until one of `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getWritableDatabase()` or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getReadableDatabase()` is called.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)?: to use for locating paths to the the database. This value may be `null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: of the database file, or null for an in-memory database |
| `factory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)?: to use for creating cursor objects, or null for the default |
| --- | --- |
| `version` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of the database (starting at 1); if the database is older, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onUpgrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)` will be used to upgrade the database; if the database is newer, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onDowngrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)` will be used to downgrade the database |

### SQLiteOpenHelper

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SQLiteOpenHelper(
    context: Context?, 
    name: String?, 
    factory: SQLiteDatabase.CursorFactory?, 
    version: Int, 
    errorHandler: DatabaseErrorHandler?)
```

Create a helper object to create, open, and/or manage a database. The database is not actually created or opened until one of `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getWritableDatabase()` or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getReadableDatabase()` is called.

Accepts input param: a concrete instance of `https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#` to be used to handle corruption when sqlite reports database corruption.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)?: to use for locating paths to the the database. This value may be `null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: of the database file, or null for an in-memory database |
| `factory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)?: to use for creating cursor objects, or null for the default |
| --- | --- |
| `version` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of the database (starting at 1); if the database is older, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onUpgrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)` will be used to upgrade the database; if the database is newer, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onDowngrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)` will be used to downgrade the database |
| `errorHandler` | [DatabaseErrorHandler](../android.database/DatabaseErrorHandler.md)?: the `https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#` to be used when sqlite reports database corruption, or null to use the default error handler. |

### SQLiteOpenHelper

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SQLiteOpenHelper(
    context: Context?, 
    name: String?, 
    version: Int, 
    openParams: SQLiteDatabase.OpenParams)
```

Create a helper object to create, open, and/or manage a database. This method always returns very quickly. The database is not actually created or opened until one of `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getWritableDatabase()` or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getReadableDatabase()` is called.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)?: to use for locating paths to the the database. This value may be `null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: of the database file, or null for an in-memory database |
| `version` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of the database (starting at 1); if the database is older, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onUpgrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)` will be used to upgrade the database; if the database is newer, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onDowngrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)` will be used to downgrade the database |
| --- | --- |
| `openParams` | [SQLiteDatabase.OpenParams](../android/database/sqlite/SQLiteDatabase.OpenParams.md): configuration parameters that are used for opening `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase`. Please note that `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CREATE_IF_NECESSARY:kotlin.Int` flag will always be set when the helper opens the database. This value cannot be `null`. |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Close any open database object.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### getDatabaseName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDatabaseName(): String!
```

Return the name of the SQLite database being opened, as given to the constructor.

### getReadableDatabase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReadableDatabase(): SQLiteDatabase!
```

Create and/or open a database. This will be the same object returned by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getWritableDatabase()` unless some problem, such as a full disk, requires the database to be opened read-only. In that case, a read-only database object will be returned. If the problem is fixed, a future call to `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getWritableDatabase()` may succeed, in which case the read-only database object will be closed and the read/write object will be returned in the future.

Like `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getWritableDatabase()`, this method may take a long time to return, so you should not call it from the application main thread, including from `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!` | a database object valid until `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#getWritableDatabase()` or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#close()` is called. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if the database cannot be opened |

### getWritableDatabase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWritableDatabase(): SQLiteDatabase!
```

Create and/or open a database that will be used for reading and writing. The first time this is called, the database will be opened and `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onCreate(android.database.sqlite.SQLiteDatabase)`, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onUpgrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)` and/or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onOpen(android.database.sqlite.SQLiteDatabase)` will be called.

Once opened successfully, the database is cached, so you can call this method every time you need to write to the database. (Make sure to call `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#close()` when you no longer need the database.) Errors such as bad permissions or a full disk may cause this method to fail, but future attempts may succeed if the problem is fixed.

Database upgrade may take a long time, you should not call this method from the application main thread, including from `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!` | a read/write database object valid until `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#close()` is called |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if the database cannot be opened for writing |

### onConfigure

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConfigure(db: SQLiteDatabase!): Unit
```

Called when the database connection is being configured, to enable features such as write-ahead logging or foreign key support.

This method is called before `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onCreate(android.database.sqlite.SQLiteDatabase)`, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onUpgrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onDowngrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)`, or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onOpen(android.database.sqlite.SQLiteDatabase)` are called. It should not modify the database except to configure the database connection as required.

This method should only call methods that configure the parameters of the database connection, such as `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()` `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setForeignKeyConstraintsEnabled(kotlin.Boolean)`, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setLocale(java.util.Locale)`, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#setMaximumSize(kotlin.Long)`, or executing PRAGMA statements.

| Parameters ||
|---|---|
| `db` | [SQLiteDatabase](SQLiteDatabase.md)!: The database. |

### onCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onCreate(db: SQLiteDatabase!): Unit
```

Called when the database is created for the first time. This is where the creation of tables and the initial population of the tables should happen.

| Parameters ||
|---|---|
| `db` | [SQLiteDatabase](SQLiteDatabase.md)!: The database. |

### onDowngrade

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDowngrade(
    db: SQLiteDatabase!, 
    oldVersion: Int, 
    newVersion: Int
): Unit
```

Called when the database needs to be downgraded. This is strictly similar to `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onUpgrade(android.database.sqlite.SQLiteDatabase,%20kotlin.Int,%20kotlin.Int)` method, but is called whenever current version is newer than requested one. However, this method is not abstract, so it is not mandatory for a customer to implement it. If not overridden, default implementation will reject downgrade and throws SQLiteException

This method executes within a transaction. If an exception is thrown, all changes will automatically be rolled back.

| Parameters ||
|---|---|
| `db` | [SQLiteDatabase](SQLiteDatabase.md)!: The database. |
| `oldVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The old database version. |
| `newVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new database version. |
| --- | --- |

### onOpen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onOpen(db: SQLiteDatabase!): Unit
```

Called when the database has been opened. The implementation should check `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#isReadOnly()` before updating the database.

This method is called after the database connection has been configured and after the database schema has been created, upgraded or downgraded as necessary. If the database connection must be configured in some way before the schema is created, upgraded, or downgraded, do it in `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper#onConfigure(android.database.sqlite.SQLiteDatabase)` instead.

| Parameters ||
|---|---|
| `db` | [SQLiteDatabase](SQLiteDatabase.md)!: The database. |

### onUpgrade

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onUpgrade(
    db: SQLiteDatabase!, 
    oldVersion: Int, 
    newVersion: Int
): Unit
```

Called when the database needs to be upgraded. The implementation should use this method to drop tables, add tables, or do anything else it needs to upgrade to the new schema version.

The SQLite ALTER TABLE documentation can be found [here](http://sqlite.org/lang_altertable.html). If you add new columns you can use ALTER TABLE to insert them into a live table. If you rename or remove columns you can use ALTER TABLE to rename the old table, then create the new table and then populate the new table with the contents of the old table.

This method executes within a transaction. If an exception is thrown, all changes will automatically be rolled back.

*Important:* You should NOT modify an existing migration step from version X to X+1 once a build has been released containing that migration step. If a migration step has an error and it runs on a device, the step will NOT re-run itself in the future if a fix is made to the migration step.

For example, suppose a migration step renames a database column from `foo` to `bar` when the name should have been `baz`. If that migration step is released in a build and runs on a user's device, the column will be renamed to `bar`. If the developer subsequently edits this same migration step to change the name to `baz` as intended, the user devices which have already run this step will still have the name `bar`. Instead, a NEW migration step should be created to correct the error and rename `bar` to `baz`, ensuring the error is corrected on devices which have already run the migration step with the error.

| Parameters ||
|---|---|
| `db` | [SQLiteDatabase](SQLiteDatabase.md)!: The database. |
| `oldVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The old database version. |
| `newVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new database version. |
| --- | --- |

### setIdleConnectionTimeout

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIdleConnectionTimeout(idleConnectionTimeoutMs: Long): Unit
```

**Deprecated:** *DO NOT USE this method. See the javadoc of `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.OpenParams.Builder#setIdleConnectionTimeout(kotlin.Long)` for the details.*

Sets the maximum number of milliseconds that SQLite connection is allowed to be idle before it is closed and removed from the pool.

This method should be called from the constructor of the subclass, before opening the database

**DO NOT USE** this method. This feature has negative side effects that are very hard to foresee. See the javadoc of `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.OpenParams.Builder#setIdleConnectionTimeout(kotlin.Long)` for the details.

| Parameters ||
|---|---|
| `idleConnectionTimeoutMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): timeout in milliseconds. Use `https://developer.android.com/reference/kotlin/java/lang/Long.html#MAX_VALUE:kotlin.Long` value to allow unlimited idle connections. Value is 0 or greater |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.OpenParams.Builder#setIdleConnectionTimeout(kotlin.Long)`

### setLookasideConfig

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLookasideConfig(
    slotSize: Int, 
    slotCount: Int
): Unit
```

Configures [lookaside memory allocator](https://sqlite.org/malloc.html#lookaside)

This method should be called from the constructor of the subclass, before opening the database, since lookaside memory configuration can only be changed when no connection is using it

SQLite default settings will be used, if this method isn't called. Use `setLookasideConfig(0,0)` to disable lookaside

**Note:** Provided slotSize/slotCount configuration is just a recommendation. The system may choose different values depending on a device, e.g. lookaside allocations can be disabled on low-RAM devices

| Parameters ||
|---|---|
| `slotSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The size in bytes of each lookaside slot. Value is 0 or greater |
| `slotCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The total number of lookaside memory slots per database connection. Value is 0 or greater |

### setOpenParams

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOpenParams(openParams: SQLiteDatabase.OpenParams): Unit
```

Sets configuration parameters that are used for opening `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase`.

Please note that `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#CREATE_IF_NECESSARY:kotlin.Int` flag will always be set when opening the database

| Parameters ||
|---|---|
| `openParams` | [SQLiteDatabase.OpenParams](../android/database/sqlite/SQLiteDatabase.OpenParams.md): configuration parameters that are used for opening `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase`. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the database is already open |

### setWriteAheadLoggingEnabled

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWriteAheadLoggingEnabled(enabled: Boolean): Unit
```

Enables or disables the use of write-ahead logging for the database. Write-ahead logging cannot be used with read-only databases so the value of this flag is ignored if the database is opened read-only.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if write-ahead logging should be enabled, false if it should be disabled. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#enableWriteAheadLogging()`
