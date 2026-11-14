# NoSuchPaddingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoSuchPaddingException

```
open class NoSuchPaddingException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [javax.crypto.NoSuchPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/NoSuchPaddingException#) |

This exception is thrown when a particular padding mechanism is requested but is not available in the environment.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NoSuchPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/NoSuchPaddingException#NoSuchPaddingException())`()` Constructs a NoSuchPaddingException with no detail message. |
| [NoSuchPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/NoSuchPaddingException#NoSuchPaddingException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a NoSuchPaddingException with the specified detail message. |

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
