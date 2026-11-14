# StaleDataException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StaleDataException

Kotlin| [Java](https://developer.android.com/reference/android/database/StaleDataException "View this page in Java") 
| --- | --- |

```
open class StaleDataException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.StaleDataException](https://developer.android.com/reference/kotlin/android/database/StaleDataException#) |

This exception is thrown when a Cursor contains stale data and must be requeried before being used again.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StaleDataException](https://developer.android.com/reference/kotlin/android/database/StaleDataException#StaleDataException())`()` <br /> |
| [StaleDataException](https://developer.android.com/reference/kotlin/android/database/StaleDataException#StaleDataException(kotlin.String))`(`description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### StaleDataException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StaleDataException()
```  

### StaleDataException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StaleDataException(description: String!)
```
