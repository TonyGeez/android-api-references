# SQLiteFullException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteFullException

Kotlin| [Java](../android/database/sqlite/SQLiteFullException.md) 
| --- | --- |

```
open class SQLiteFullException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](../android/database/SQLException.md) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](../android/database/sqlite/SQLiteException.md) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteFullException](../android/database/sqlite/SQLiteFullException.md) |
| --- | --- | --- | --- | --- | --- | --- |

An exception that indicates that the SQLite database is full.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteFullException](../android/database/sqlite/SQLiteFullException.md))`()` <br /> |
| [SQLiteFullException](../android/database/sqlite/SQLiteFullException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### SQLiteFullException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteFullException()
```  

### SQLiteFullException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteFullException(error: String!)
```
