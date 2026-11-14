# SQLiteDatabaseLockedException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteDatabaseLockedException

Kotlin| [Java](SQLiteDatabaseLockedException.md) 
| --- | --- |

```
open class SQLiteDatabaseLockedException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](../android.database/SQLException.md) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](SQLiteException.md) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteDatabaseLockedException](SQLiteDatabaseLockedException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Thrown if the database engine was unable to acquire the database locks it needs to do its job. If the statement is a \[COMMIT\] or occurs outside of an explicit transaction, then you can retry the statement. If the statement is not a \[COMMIT\] and occurs within a explicit transaction then you should rollback the transaction before continuing.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteDatabaseLockedException](SQLiteDatabaseLockedException.md))`()` <br /> |
| [SQLiteDatabaseLockedException](SQLiteDatabaseLockedException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### SQLiteDatabaseLockedException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteDatabaseLockedException()
```  

### SQLiteDatabaseLockedException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteDatabaseLockedException(error: String!)
```
