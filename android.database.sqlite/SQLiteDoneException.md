# SQLiteDoneException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteDoneException

Kotlin | [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteDoneException "View this page in Java") 
| --- | --- |

```
open class SQLiteDoneException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](https://developer.android.com/reference/kotlin/android/database/SQLException.html#) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteDoneException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDoneException#) |
| --- | --- | --- | --- | --- | --- | --- |

An exception that indicates that the SQLite program is done. Thrown when an operation that expects a row (such as [android.database.sqlite.SQLiteStatement#simpleQueryForString](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement#simpleQueryForString()) or [android.database.sqlite.SQLiteStatement#simpleQueryForLong](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement#simpleQueryForLong())) does not get one.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteDoneException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDoneException#SQLiteDoneException())`()` <br /> |
| [SQLiteDoneException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDoneException#SQLiteDoneException(kotlin.String))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### SQLiteDoneException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteDoneException()
```  

### SQLiteDoneException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteDoneException(error: String!)
```
