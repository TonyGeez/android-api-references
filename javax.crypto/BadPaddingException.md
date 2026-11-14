# BadPaddingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BadPaddingException

```
open class BadPaddingException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.security.GeneralSecurityException](../java.security/GeneralSecurityException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [javax.crypto.BadPaddingException](BadPaddingException.md) |

| Known Direct Subclasses [AEADBadTagException](AEADBadTagException.md) |--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AEADBadTagException](AEADBadTagException.md) | This exception is thrown when a [Cipher](Cipher.md) operating in an AEAD mode (such as GCM/CCM) is unable to verify the supplied authentication tag. | |
| --- | --- | --- | --- | --- | --- | --- |

This exception is thrown when a particular padding mechanism is expected for the input data but the data is not padded properly.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BadPaddingException](BadPaddingException.md))`()` Constructs a BadPaddingException with no detail message. |
| [BadPaddingException](BadPaddingException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a BadPaddingException with the specified detail message. |

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
