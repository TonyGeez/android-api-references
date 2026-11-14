Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidRequestMessageException

```
open class InvalidRequestMessageException : IdentityCredentialException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [android.security.identity.IdentityCredentialException](IdentityCredentialException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.security.identity.InvalidRequestMessageException](InvalidRequestMessageException.md) |

> [!CAUTION]
> **This exception was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

Thrown if message with the request doesn't satisfy the requirements documented in `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/InvalidRequestMessageException#InvalidRequestMessageException(kotlin.String)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/InvalidRequestMessageException#` exception. |
| `https://developer.android.com/reference/kotlin/android/security/identity/InvalidRequestMessageException#InvalidRequestMessageException(kotlin.String,%20kotlin.Throwable)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)` Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/InvalidRequestMessageException#` exception. |

## Public constructors

### InvalidRequestMessageException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InvalidRequestMessageException(message: String)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/InvalidRequestMessageException#` exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |

### InvalidRequestMessageException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InvalidRequestMessageException(
    message: String, 
    cause: Throwable)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/InvalidRequestMessageException#` exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html): the cause. This value cannot be `null`. |
