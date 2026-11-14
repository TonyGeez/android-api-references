# ShortBufferException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ShortBufferException

```
open class ShortBufferException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||
| | | | ↳ | [javax.crypto.ShortBufferException](https://developer.android.com/reference/kotlin/javax/crypto/ShortBufferException#) |

This exception is thrown when an output buffer provided by the user is too short to hold the operation result.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ShortBufferException](https://developer.android.com/reference/kotlin/javax/crypto/ShortBufferException#ShortBufferException())`()` Constructs a ShortBufferException with no detail message. |
| [ShortBufferException](https://developer.android.com/reference/kotlin/javax/crypto/ShortBufferException#ShortBufferException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a ShortBufferException with the specified detail message. |

## Public constructors

### ShortBufferException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ShortBufferException()
```

Constructs a ShortBufferException with no detail message. A detail message is a String that describes this particular exception. 

### ShortBufferException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ShortBufferException(msg: String!)
```

Constructs a ShortBufferException with the specified detail message.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
