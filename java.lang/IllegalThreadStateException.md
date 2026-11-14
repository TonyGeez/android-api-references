# IllegalThreadStateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalThreadStateException

```
open class IllegalThreadStateException : IllegalArgumentException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java/lang/IllegalArgumentException.md) ||
| | | | | ↳ | [java.lang.IllegalThreadStateException](../java/lang/IllegalThreadStateException.md) |

Thrown to indicate that a thread is not in an appropriate state for the requested operation. See, for example, the`suspend`and`resume`methods in class`Thread`.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalThreadStateException](../java/lang/IllegalThreadStateException.md))`()` Constructs an`IllegalThreadStateException`with no detail message. |
| [IllegalThreadStateException](../java/lang/IllegalThreadStateException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`IllegalThreadStateException`with the specified detail message. |

## Public constructors

### IllegalThreadStateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalThreadStateException()
```

Constructs an`IllegalThreadStateException`with no detail message. 

### IllegalThreadStateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalThreadStateException(s: String!)
```

Constructs an`IllegalThreadStateException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
