# DefaultDatabaseErrorHandler

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DefaultDatabaseErrorHandler

Kotlin| [Java](../android/database/DefaultDatabaseErrorHandler.md) 
| --- | --- |

```
class DefaultDatabaseErrorHandler : DatabaseErrorHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.database.DefaultDatabaseErrorHandler](../android/database/DefaultDatabaseErrorHandler.md) |

Default class used to define the action to take when database corruption is reported by sqlite.

An application can specify an implementation of [DatabaseErrorHandler](../android/database/DatabaseErrorHandler.md) on the following:

- [SQLiteDatabase.openOrCreateDatabase(String,](../android/database/sqlite/SQLiteDatabase.md))
- [SQLiteDatabase.openDatabase(String,](../android/database/sqlite/SQLiteDatabase.md))

The specified [DatabaseErrorHandler](../android/database/DatabaseErrorHandler.md) is used to handle database corruption errors, if they occur.

If null is specified for the DatabaseErrorHandler param in the above calls, this class is used as the default [DatabaseErrorHandler](../android/database/DatabaseErrorHandler.md).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DefaultDatabaseErrorHandler](../android/database/DefaultDatabaseErrorHandler.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCorruption](../android/database/DefaultDatabaseErrorHandler.md))`(`dbObj:` ` [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md)!`)` defines the default method to be invoked when database corruption is detected. |

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
| `dbObj` | [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md)!:the [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md) object representing the database on which corruption is detected. |
