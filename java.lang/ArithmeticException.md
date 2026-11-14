Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArithmeticException

```
open class ArithmeticException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) ||
| | | | ↳ | [java.lang.ArithmeticException](https://developer.android.com/reference/kotlin/java/lang/ArithmeticException#) |

Thrown when an exceptional arithmetic condition has occurred. For example, an integer "divide by zero" throws an instance of this class. `ArithmeticException` objects may be constructed by the virtual machine as if [suppression were disabled and/or the](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.String,%20kotlin.Throwable,%20kotlin.Boolean,%20kotlin.Boolean)).

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/ArithmeticException#ArithmeticException()()` Constructs an `ArithmeticException` with no detail message. |
| `https://developer.android.com/reference/kotlin/java/lang/ArithmeticException#ArithmeticException(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructs an `ArithmeticException` with the specified detail message. |

## Public constructors

### ArithmeticException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ArithmeticException()
```

Constructs an `ArithmeticException` with no detail message.

### ArithmeticException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ArithmeticException(s: String!)
```

Constructs an `ArithmeticException` with the specified detail message.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |
