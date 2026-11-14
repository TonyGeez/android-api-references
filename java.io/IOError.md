# IOError

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IOError

```
open class IOError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error.html#) ||
| | | ↳ | [java.io.IOError](https://developer.android.com/reference/kotlin/java/io/IOError#) |

Thrown when a serious I/O error has occurred.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IOError](https://developer.android.com/reference/kotlin/java/io/IOError#IOError(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new instance of IOError with the specified cause. |

## Public constructors

### IOError

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IOError(cause: Throwable!)
```

Constructs a new instance of IOError with the specified cause. The IOError is created with the detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of cause).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The cause of this error, or`null`if the cause is not known |
