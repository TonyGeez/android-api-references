# NegativeArraySizeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NegativeArraySizeException

```
open class NegativeArraySizeException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.NegativeArraySizeException](../java/lang/NegativeArraySizeException.md) |

Thrown if an application tries to create an array with negative size.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NegativeArraySizeException](../java/lang/NegativeArraySizeException.md))`()` Constructs a`NegativeArraySizeException`with no detail message. |
| [NegativeArraySizeException](../java/lang/NegativeArraySizeException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`NegativeArraySizeException`with the specified detail message. |

## Public constructors

### NegativeArraySizeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NegativeArraySizeException()
```

Constructs a`NegativeArraySizeException`with no detail message. 

### NegativeArraySizeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NegativeArraySizeException(s: String!)
```

Constructs a`NegativeArraySizeException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
