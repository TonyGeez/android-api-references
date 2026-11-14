# SQLiteDiskIOException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteDiskIOException

Kotlin| [Java](../android/database/sqlite/SQLiteDiskIOException.md) 
| --- | --- |

```
open class SQLiteDiskIOException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](../android/database/SQLException.md) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](../android/database/sqlite/SQLiteException.md) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteDiskIOException](../android/database/sqlite/SQLiteDiskIOException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Indicates that an IO error occurred while accessing the SQLite database file.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteDiskIOException](../android/database/sqlite/SQLiteDiskIOException.md))`()` <br /> |
| [SQLiteDiskIOException](../android/database/sqlite/SQLiteDiskIOException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### SQLiteDiskIOException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteDiskIOException()
```  

### SQLiteDiskIOException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteDiskIOException(error: String!)
```
