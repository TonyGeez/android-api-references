# SQLiteMisuseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteMisuseException

Kotlin| [Java](../android/database/sqlite/SQLiteMisuseException.md) 
| --- | --- |

```
open class SQLiteMisuseException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](../android/database/SQLException.md) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](../android/database/sqlite/SQLiteException.md) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteMisuseException](../android/database/sqlite/SQLiteMisuseException.md) |
| --- | --- | --- | --- | --- | --- | --- |

This error can occur if the application creates a SQLiteStatement object and allows multiple threads in the application use it at the same time. Sqlite returns this error if bind and execute methods on this object occur at the same time from multiple threads, like so: thread # 1: in execute() method of the SQLiteStatement object while thread # 2: is in bind..() on the same object.

<br />

FIX this by NEVER sharing the same SQLiteStatement object between threads. Create a local instance of the SQLiteStatement whenever it is needed, use it and close it ASAP. NEVER make it globally available.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteMisuseException](../android/database/sqlite/SQLiteMisuseException.md))`()` <br /> |
| [SQLiteMisuseException](../android/database/sqlite/SQLiteMisuseException.md))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### SQLiteMisuseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteMisuseException()
```  

### SQLiteMisuseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteMisuseException(error: String!)
```
