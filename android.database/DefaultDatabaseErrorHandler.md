# DefaultDatabaseErrorHandler

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DefaultDatabaseErrorHandler

Kotlin| [Java](https://developer.android.com/reference/android/database/DefaultDatabaseErrorHandler "View this page in Java") 

```
class DefaultDatabaseErrorHandler : DatabaseErrorHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.database.DefaultDatabaseErrorHandler](https://developer.android.com/reference/kotlin/android/database/DefaultDatabaseErrorHandler#) |

Default class used to define the action to take when database corruption is reported by sqlite.

An application can specify an implementation of [DatabaseErrorHandler](https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler) on the following:

- [SQLiteDatabase.openOrCreateDatabase(String,](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#openOrCreateDatabase(kotlin.String,%20android.database.sqlite.SQLiteDatabase.CursorFactory,%20android.database.DatabaseErrorHandler))
- [SQLiteDatabase.openDatabase(String,](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase#openDatabase(kotlin.String,%20android.database.sqlite.SQLiteDatabase.CursorFactory,%20kotlin.Int,%20android.database.DatabaseErrorHandler))

The specified [DatabaseErrorHandler](https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler) is used to handle database corruption errors, if they occur.

If null is specified for the DatabaseErrorHandler param in the above calls, this class is used as the default [DatabaseErrorHandler](https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DefaultDatabaseErrorHandler](https://developer.android.com/reference/kotlin/android/database/DefaultDatabaseErrorHandler#DefaultDatabaseErrorHandler())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCorruption](https://developer.android.com/reference/kotlin/android/database/DefaultDatabaseErrorHandler#onCorruption(android.database.sqlite.SQLiteDatabase))`(`dbObj:` ` [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)!`)` defines the default method to be invoked when database corruption is detected. |

## Public constructors

### DefaultDatabaseErrorHandler

```
DefaultDatabaseErrorHandler()
```

## Public methods

### onCorruption

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onCorruption(dbObj: SQLiteDatabase!): Unit
```

defines the default method to be invoked when database corruption is detected.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dbObj` | [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)!:the [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase) object representing the database on which corruption is detected. |
