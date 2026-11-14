Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MessageDecryptionException

```
open class MessageDecryptionException : IdentityCredentialException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [android.security.identity.IdentityCredentialException](IdentityCredentialException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.security.identity.MessageDecryptionException](MessageDecryptionException.md) |

> [!CAUTION]
> **This exception was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

Thrown when failing to decrypt a message from the reader device.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/MessageDecryptionException#MessageDecryptionException(kotlin.String)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/MessageDecryptionException#` exception. |
| `https://developer.android.com/reference/kotlin/android/security/identity/MessageDecryptionException#MessageDecryptionException(kotlin.String,%20kotlin.Throwable)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)` Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/MessageDecryptionException#` exception. |

## Public constructors

### MessageDecryptionException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MessageDecryptionException(message: String)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/MessageDecryptionException#` exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |

### MessageDecryptionException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MessageDecryptionException(
    message: String, 
    cause: Throwable)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/MessageDecryptionException#` exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html): the cause. This value cannot be `null`. |
