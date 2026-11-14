# SQLiteAbortException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteAbortException

Kotlin | [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteAbortException "View this page in Java") 

```
open class SQLiteAbortException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| | | | ↳ | [android.database.SQLException](https://developer.android.com/reference/kotlin/android/database/SQLException.html#) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteAbortException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAbortException#) |

An exception that indicates that the SQLite program was aborted. This can happen either through a call to ABORT in a trigger, or as the result of using the ABORT conflict clause.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteAbortException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAbortException#SQLiteAbortException())`()` <br /> |
| [SQLiteAbortException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAbortException#SQLiteAbortException(kotlin.String))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### SQLiteAbortException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteAbortException()
```  

### SQLiteAbortException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteAbortException(error: String!)
```
