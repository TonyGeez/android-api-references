# CursorWindowAllocationException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorWindowAllocationException

Kotlin| [Java](https://developer.android.com/reference/android/database/CursorWindowAllocationException "View this page in Java") 

```
open class CursorWindowAllocationException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| | | | ↳ | [android.database.CursorWindowAllocationException](https://developer.android.com/reference/kotlin/android/database/CursorWindowAllocationException#) |

This exception is thrown when a CursorWindow couldn't be allocated, most probably due to memory not being available.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CursorWindowAllocationException](https://developer.android.com/reference/kotlin/android/database/CursorWindowAllocationException#CursorWindowAllocationException(kotlin.String))`(`description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> |

## Public constructors

### CursorWindowAllocationException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorWindowAllocationException(description: String)
```

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------|
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
