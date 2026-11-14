Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnknownAuthenticationKeyException

```
open class UnknownAuthenticationKeyException : IdentityCredentialException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [android.security.identity.IdentityCredentialException](https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.security.identity.UnknownAuthenticationKeyException](https://developer.android.com/reference/kotlin/android/security/identity/UnknownAuthenticationKeyException#) |

> [!CAUTION]
> **This exception was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

Thrown if trying to certify an unknown dynamic authentication key.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/UnknownAuthenticationKeyException#UnknownAuthenticationKeyException(kotlin.String)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/UnknownAuthenticationKeyException#` exception. |
| `https://developer.android.com/reference/kotlin/android/security/identity/UnknownAuthenticationKeyException#UnknownAuthenticationKeyException(kotlin.String,%20kotlin.Throwable)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)` Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/UnknownAuthenticationKeyException#` exception. |

## Public constructors

### UnknownAuthenticationKeyException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnknownAuthenticationKeyException(message: String)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/UnknownAuthenticationKeyException#` exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |

### UnknownAuthenticationKeyException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnknownAuthenticationKeyException(
    message: String, 
    cause: Throwable)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/UnknownAuthenticationKeyException#` exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html): the cause. This value cannot be `null`. |
