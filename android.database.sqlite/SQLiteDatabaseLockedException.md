# SQLiteDatabaseLockedException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteDatabaseLockedException

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteDatabaseLockedException "View this page in Java") 

```
open class SQLiteDatabaseLockedException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| | | | ↳ | [android.database.SQLException](https://developer.android.com/reference/kotlin/android/database/SQLException.html#) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteDatabaseLockedException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabaseLockedException#) |

Thrown if the database engine was unable to acquire the database locks it needs to do its job. If the statement is a \[COMMIT\] or occurs outside of an explicit transaction, then you can retry the statement. If the statement is not a \[COMMIT\] and occurs within a explicit transaction then you should rollback the transaction before continuing.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteDatabaseLockedException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabaseLockedException#SQLiteDatabaseLockedException())`()` <br /> |
| [SQLiteDatabaseLockedException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabaseLockedException#SQLiteDatabaseLockedException(kotlin.String))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

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
