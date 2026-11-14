# WrongMethodTypeException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WrongMethodTypeException

```
open class WrongMethodTypeException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| | | | ↳ | [java.lang.invoke.WrongMethodTypeException](https://developer.android.com/reference/kotlin/java/lang/invoke/WrongMethodTypeException#) |

Thrown to indicate that code has attempted to call a method handle via the wrong method type. As with the bytecode representation of normal Java method calls, method handle calls are strongly typed to a specific type descriptor associated with a call site.

This exception may also be thrown when two method handles are composed, and the system detects that their types cannot be matched up correctly. This amounts to an early evaluation of the type mismatch, at method handle construction time, instead of when the mismatched method handle is called.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WrongMethodTypeException](https://developer.android.com/reference/kotlin/java/lang/invoke/WrongMethodTypeException#WrongMethodTypeException())`()` Constructs a`WrongMethodTypeException`with no detail message. |
| [WrongMethodTypeException](https://developer.android.com/reference/kotlin/java/lang/invoke/WrongMethodTypeException#WrongMethodTypeException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`WrongMethodTypeException`with the specified detail message. |

## Public constructors

### WrongMethodTypeException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WrongMethodTypeException()
```

Constructs a`WrongMethodTypeException`with no detail message. 

### WrongMethodTypeException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WrongMethodTypeException(s: String!)
```

Constructs a`WrongMethodTypeException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
