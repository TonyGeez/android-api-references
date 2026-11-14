# UnsatisfiedLinkError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsatisfiedLinkError

```
open class UnsatisfiedLinkError : LinkageError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) |||
| | | ↳ | [java.lang.LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError) ||
| | | | ↳ | [java.lang.UnsatisfiedLinkError](https://developer.android.com/reference/kotlin/java/lang/UnsatisfiedLinkError#) |

Thrown if the Java Virtual Machine cannot find an appropriate native-language definition of a method declared`native`.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnsatisfiedLinkError](https://developer.android.com/reference/kotlin/java/lang/UnsatisfiedLinkError#UnsatisfiedLinkError())`()` Constructs an`UnsatisfiedLinkError`with no detail message. |
| [UnsatisfiedLinkError](https://developer.android.com/reference/kotlin/java/lang/UnsatisfiedLinkError#UnsatisfiedLinkError(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`UnsatisfiedLinkError`with the specified detail message. |

## Public constructors

### UnsatisfiedLinkError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnsatisfiedLinkError()
```

Constructs an`UnsatisfiedLinkError`with no detail message. 

### UnsatisfiedLinkError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnsatisfiedLinkError(s: String!)
```

Constructs an`UnsatisfiedLinkError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
