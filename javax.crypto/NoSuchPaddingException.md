# NoSuchPaddingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoSuchPaddingException

```
open class NoSuchPaddingException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.security.GeneralSecurityException](../java.security/GeneralSecurityException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [javax.crypto.NoSuchPaddingException](NoSuchPaddingException.md) |

This exception is thrown when a particular padding mechanism is requested but is not available in the environment.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NoSuchPaddingException](NoSuchPaddingException.md))`()` Constructs a NoSuchPaddingException with no detail message. |
| [NoSuchPaddingException](NoSuchPaddingException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a NoSuchPaddingException with the specified detail message. |

## Public constructors

### NoSuchPaddingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchPaddingException()
```

Constructs a NoSuchPaddingException with no detail message. A detail message is a String that describes this particular exception. 

### NoSuchPaddingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchPaddingException(msg: String!)
```

Constructs a NoSuchPaddingException with the specified detail message.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
