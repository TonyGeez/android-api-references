# DatabaseErrorHandler

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatabaseErrorHandler

Kotlin| [Java](../android/database/DatabaseErrorHandler.md) 
| --- | --- |

```
interface DatabaseErrorHandler
```

| [android.database.DatabaseErrorHandler](../android/database/DatabaseErrorHandler.md) |

| Known Direct Subclasses [DefaultDatabaseErrorHandler](../android/database/DefaultDatabaseErrorHandler.md) |----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [DefaultDatabaseErrorHandler](../android/database/DefaultDatabaseErrorHandler.md) | Default class used to define the action to take when database corruption is reported by sqlite. | |
| --- | --- | --- | --- | --- | --- | --- |

An interface to let apps define an action to take when database corruption is detected.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCorruption](../android/database/DatabaseErrorHandler.md))`(`dbObj:` ` [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md)!`)` The method invoked when database corruption is detected. |

## Public methods

### onCorruption

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCorruption(dbObj: SQLiteDatabase!): Unit
```

The method invoked when database corruption is detected.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dbObj` | [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md)!:the [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md) object representing the database on which corruption is detected. |
