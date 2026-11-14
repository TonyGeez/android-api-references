# AEADBadTagException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AEADBadTagException

```
open class AEADBadTagException : BadPaddingException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.security.GeneralSecurityException](../java/security/GeneralSecurityException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [javax.crypto.BadPaddingException](../javax/crypto/BadPaddingException.md) ||
| | | | | ↳ | [javax.crypto.AEADBadTagException](../javax/crypto/AEADBadTagException.md) |

This exception is thrown when a [Cipher](../javax/crypto/Cipher.md) operating in an AEAD mode (such as GCM/CCM) is unable to verify the supplied authentication tag.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AEADBadTagException](../javax/crypto/AEADBadTagException.md))`()` Constructs a AEADBadTagException with no detail message. |
| [AEADBadTagException](../javax/crypto/AEADBadTagException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a AEADBadTagException with the specified detail message. |

## Public constructors

### AEADBadTagException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AEADBadTagException()
```

Constructs a AEADBadTagException with no detail message. 

### AEADBadTagException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AEADBadTagException(msg: String!)
```

Constructs a AEADBadTagException with the specified detail message.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
