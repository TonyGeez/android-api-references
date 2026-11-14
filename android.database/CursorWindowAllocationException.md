# CursorWindowAllocationException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorWindowAllocationException

Kotlin| [Java](../android/database/CursorWindowAllocationException.md) 
| --- | --- |

```
open class CursorWindowAllocationException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.database.CursorWindowAllocationException](../android/database/CursorWindowAllocationException.md) |

This exception is thrown when a CursorWindow couldn't be allocated, most probably due to memory not being available.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CursorWindowAllocationException](../android/database/CursorWindowAllocationException.md))`(`description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> |

## Public constructors

### CursorWindowAllocationException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorWindowAllocationException(description: String)
```

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------|
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
