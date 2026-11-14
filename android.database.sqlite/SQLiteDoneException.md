# SQLiteDoneException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteDoneException

Kotlin | [Java](../android/database/sqlite/SQLiteDoneException.md) 
| --- | --- |

```
open class SQLiteDoneException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](../android/database/SQLException.md) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](../android/database/sqlite/SQLiteException.md) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteDoneException](../android/database/sqlite/SQLiteDoneException.md) |
| --- | --- | --- | --- | --- | --- | --- |

An exception that indicates that the SQLite program is done. Thrown when an operation that expects a row (such as [android.database.sqlite.SQLiteStatement#simpleQueryForString](../android/database/sqlite/SQLiteStatement.md)) or [android.database.sqlite.SQLiteStatement#simpleQueryForLong](../android/database/sqlite/SQLiteStatement.md))) does not get one.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteDoneException](../android/database/sqlite/SQLiteDoneException.md))`()` <br /> |
| [SQLiteDoneException](../android/database/sqlite/SQLiteDoneException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

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
