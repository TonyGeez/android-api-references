Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CipherSuiteNotSupportedException

```
open class CipherSuiteNotSupportedException : IdentityCredentialException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [android.security.identity.IdentityCredentialException](IdentityCredentialException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.security.identity.CipherSuiteNotSupportedException](CipherSuiteNotSupportedException.md) |

> [!CAUTION]
> **This exception was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

Thrown if trying to use a cipher suite which isn't supported.

## Summary

| Public constructors ||
|---|---|
| CipherSuiteNotSupportedException Constructs a new CipherSuiteNotSupportedException exception. |
| CipherSuiteNotSupportedException Constructs a new CipherSuiteNotSupportedException exception. |

## Public constructors

### CipherSuiteNotSupportedException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CipherSuiteNotSupportedException(message: String)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new CipherSuiteNotSupportedException exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |

### CipherSuiteNotSupportedException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CipherSuiteNotSupportedException(
    message: String, 
    cause: Throwable)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new CipherSuiteNotSupportedException exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html): the cause. This value cannot be `null`. |
