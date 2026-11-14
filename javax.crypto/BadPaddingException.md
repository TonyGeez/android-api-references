# BadPaddingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BadPaddingException

```
open class BadPaddingException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||
| | | | ↳ | [javax.crypto.BadPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/BadPaddingException#) |

| Known Direct Subclasses [AEADBadTagException](https://developer.android.com/reference/kotlin/javax/crypto/AEADBadTagException) |--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AEADBadTagException](https://developer.android.com/reference/kotlin/javax/crypto/AEADBadTagException) | This exception is thrown when a [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher) operating in an AEAD mode (such as GCM/CCM) is unable to verify the supplied authentication tag. | |

This exception is thrown when a particular padding mechanism is expected for the input data but the data is not padded properly.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BadPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/BadPaddingException#BadPaddingException())`()` Constructs a BadPaddingException with no detail message. |
| [BadPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/BadPaddingException#BadPaddingException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a BadPaddingException with the specified detail message. |

## Public constructors

### BadPaddingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BadPaddingException()
```

Constructs a BadPaddingException with no detail message. A detail message is a String that describes this particular exception. 

### BadPaddingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BadPaddingException(msg: String!)
```

Constructs a BadPaddingException with the specified detail message.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
