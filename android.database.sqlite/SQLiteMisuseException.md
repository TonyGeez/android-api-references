# SQLiteMisuseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteMisuseException

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteMisuseException "View this page in Java") 
| --- | --- |

```
open class SQLiteMisuseException : SQLiteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.SQLException](https://developer.android.com/reference/kotlin/android/database/SQLException.html#) |||
| | | | | ↳ | [android.database.sqlite.SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) ||
| | | | | | ↳ | [android.database.sqlite.SQLiteMisuseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteMisuseException#) |
| --- | --- | --- | --- | --- | --- | --- |

This error can occur if the application creates a SQLiteStatement object and allows multiple threads in the application use it at the same time. Sqlite returns this error if bind and execute methods on this object occur at the same time from multiple threads, like so: thread # 1: in execute() method of the SQLiteStatement object while thread # 2: is in bind..() on the same object.

<br />

FIX this by NEVER sharing the same SQLiteStatement object between threads. Create a local instance of the SQLiteStatement whenever it is needed, use it and close it ASAP. NEVER make it globally available.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteMisuseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteMisuseException#SQLiteMisuseException())`()` <br /> |
| [SQLiteMisuseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteMisuseException#SQLiteMisuseException(kotlin.String))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

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
