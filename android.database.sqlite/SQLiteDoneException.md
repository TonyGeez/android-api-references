# SQLiteDoneException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteDoneException

Kotlin | [Java](SQLiteDoneException.md) 
| --- | --- |

```
open class SQLiteDoneException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](../android.database/SQLException.md) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](SQLiteException.md) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteDoneException](SQLiteDoneException.md) |
| --- | --- | --- | --- | --- | --- | --- |

An exception that indicates that the SQLite program is done. Thrown when an operation that expects a row (such as [android.database.sqlite.SQLiteStatement#simpleQueryForString](SQLiteStatement.md)) or [android.database.sqlite.SQLiteStatement#simpleQueryForLong](SQLiteStatement.md))) does not get one.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteDoneException](SQLiteDoneException.md))`()` <br /> |
| [SQLiteDoneException](SQLiteDoneException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

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
