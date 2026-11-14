# DatabaseErrorHandler

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatabaseErrorHandler

Kotlin| [Java](https://developer.android.com/reference/android/database/DatabaseErrorHandler "View this page in Java") 

```
interface DatabaseErrorHandler
```

| [android.database.DatabaseErrorHandler](https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler#) |

| Known Direct Subclasses [DefaultDatabaseErrorHandler](https://developer.android.com/reference/kotlin/android/database/DefaultDatabaseErrorHandler) |----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [DefaultDatabaseErrorHandler](https://developer.android.com/reference/kotlin/android/database/DefaultDatabaseErrorHandler) | Default class used to define the action to take when database corruption is reported by sqlite. | |

An interface to let apps define an action to take when database corruption is detected.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCorruption](https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler#onCorruption(android.database.sqlite.SQLiteDatabase))`(`dbObj:` ` [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)!`)` The method invoked when database corruption is detected. |

## Public methods

### onCorruption

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCorruption(dbObj: SQLiteDatabase!): Unit
```

The method invoked when database corruption is detected.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dbObj` | [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)!:the [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase) object representing the database on which corruption is detected. |
