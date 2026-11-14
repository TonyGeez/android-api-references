# SQLiteAbortException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteAbortException

Kotlin | [Java](SQLiteAbortException.md) 
| --- | --- |

```
open class SQLiteAbortException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](../android.database/SQLException.md) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](SQLiteException.md) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteAbortException](SQLiteAbortException.md) |
| --- | --- | --- | --- | --- | --- | --- |

An exception that indicates that the SQLite program was aborted. This can happen either through a call to ABORT in a trigger, or as the result of using the ABORT conflict clause.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteAbortException](SQLiteAbortException.md))`()` <br /> |
| [SQLiteAbortException](SQLiteAbortException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

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
