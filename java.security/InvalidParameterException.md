# InvalidParameterException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidParameterException

```
open class InvalidParameterException : IllegalArgumentException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java.lang/IllegalArgumentException.md) ||
| | | | | ↳ | [java.security.InvalidParameterException](InvalidParameterException.md) |

This exception, designed for use by the JCA/JCE engine classes, is thrown when an invalid parameter is passed to a method.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvalidParameterException](InvalidParameterException.md))`()` Constructs an InvalidParameterException with no detail message. |
| [InvalidParameterException](InvalidParameterException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an InvalidParameterException with the specified detail message. |

## Public constructors

### InvalidParameterException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidParameterException()
```

Constructs an InvalidParameterException with no detail message. A detail message is a String that describes this particular exception. 

### InvalidParameterException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidParameterException(msg: String!)
```

Constructs an InvalidParameterException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
