# SQLiteAccessPermException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteAccessPermException

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteAccessPermException "View this page in Java") 
| --- | --- |

```
open class SQLiteAccessPermException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](https://developer.android.com/reference/kotlin/android/database/SQLException.html#) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteAccessPermException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAccessPermException#) |
| --- | --- | --- | --- | --- | --- | --- |

This exception class is used when sqlite can't access the database file due to lack of permissions on the file.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteAccessPermException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAccessPermException#SQLiteAccessPermException())`()` <br /> |
| [SQLiteAccessPermException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAccessPermException#SQLiteAccessPermException(kotlin.String))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### SQLiteAccessPermException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteAccessPermException()
```  

### SQLiteAccessPermException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteAccessPermException(error: String!)
```
