# SQLiteDiskIOException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteDiskIOException

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteDiskIOException "View this page in Java") 
| --- | --- |

```
open class SQLiteDiskIOException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](https://developer.android.com/reference/kotlin/android/database/SQLException.html#) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteDiskIOException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDiskIOException#) |
| --- | --- | --- | --- | --- | --- | --- |

Indicates that an IO error occurred while accessing the SQLite database file.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteDiskIOException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDiskIOException#SQLiteDiskIOException())`()` <br /> |
| [SQLiteDiskIOException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDiskIOException#SQLiteDiskIOException(kotlin.String))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

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
