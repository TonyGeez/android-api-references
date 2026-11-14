# SQLiteDatabaseCorruptException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteDatabaseCorruptException

Kotlin| [Java](SQLiteDatabaseCorruptException.md) 
| --- | --- |

```
open class SQLiteDatabaseCorruptException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](../android.database/SQLException.md) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](SQLiteException.md) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteDatabaseCorruptException](SQLiteDatabaseCorruptException.md) |
| --- | --- | --- | --- | --- | --- | --- |

An exception that indicates that the SQLite database file is corrupt.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteDatabaseCorruptException](SQLiteDatabaseCorruptException.md))`()` <br /> |
| [SQLiteDatabaseCorruptException](SQLiteDatabaseCorruptException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### SQLiteDatabaseCorruptException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteDatabaseCorruptException()
```  

### SQLiteDatabaseCorruptException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteDatabaseCorruptException(error: String!)
```
