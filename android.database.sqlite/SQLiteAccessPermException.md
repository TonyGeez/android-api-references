# SQLiteAccessPermException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteAccessPermException

Kotlin| [Java](SQLiteAccessPermException.md) 
| --- | --- |

```
open class SQLiteAccessPermException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](../android.database/SQLException.md) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](SQLiteException.md) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteAccessPermException](SQLiteAccessPermException.md) |
| --- | --- | --- | --- | --- | --- | --- |

This exception class is used when sqlite can't access the database file due to lack of permissions on the file.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteAccessPermException](SQLiteAccessPermException.md))`()` <br /> |
| [SQLiteAccessPermException](SQLiteAccessPermException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

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
