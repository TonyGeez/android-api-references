# SQLiteConstraintException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteConstraintException

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteConstraintException "View this page in Java") 
| --- | --- |

```
open class SQLiteConstraintException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](https://developer.android.com/reference/kotlin/android/database/SQLException.html#) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteConstraintException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteConstraintException#) |
| --- | --- | --- | --- | --- | --- | --- |

An exception that indicates that an integrity constraint was violated.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteConstraintException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteConstraintException#SQLiteConstraintException())`()` <br /> |
| [SQLiteConstraintException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteConstraintException#SQLiteConstraintException(kotlin.String))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### SQLiteConstraintException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteConstraintException()
```  

### SQLiteConstraintException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteConstraintException(error: String!)
```
