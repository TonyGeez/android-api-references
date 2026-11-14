Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IdentityCredentialException

```
open class IdentityCredentialException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [android.security.identity.IdentityCredentialException](../android/security/identity/IdentityCredentialException.md) |
| --- | --- | --- | --- |

Known Direct Subclasses [AlreadyPersonalizedException](../android/security/identity/AlreadyPersonalizedException.md), [CipherSuiteNotSupportedException](../android/security/identity/CipherSuiteNotSupportedException.md), [DocTypeNotSupportedException](../android/security/identity/DocTypeNotSupportedException.md), [EphemeralPublicKeyNotFoundException](../android/security/identity/EphemeralPublicKeyNotFoundException.md), [InvalidReaderSignatureException](../android/security/identity/InvalidReaderSignatureException.md), [InvalidRequestMessageException](../android/security/identity/InvalidRequestMessageException.md), [MessageDecryptionException](../android/security/identity/MessageDecryptionException.md), [NoAuthenticationKeyAvailableException](../android/security/identity/NoAuthenticationKeyAvailableException.md), [SessionTranscriptMismatchException](../android/security/identity/SessionTranscriptMismatchException.md), [UnknownAuthenticationKeyException](../android/security/identity/UnknownAuthenticationKeyException.md) [AlreadyPersonalizedException](../android/security/identity/AlreadyPersonalizedException.md) Thrown if trying to create a credential which already exists.
[CipherSuiteNotSupportedException](../android/security/identity/CipherSuiteNotSupportedException.md) Thrown if trying to use a cipher suite which isn't supported.
[DocTypeNotSupportedException](../android/security/identity/DocTypeNotSupportedException.md) Thrown if trying to create a credential with an unsupported document type.
[EphemeralPublicKeyNotFoundException](../android/security/identity/EphemeralPublicKeyNotFoundException.md) Thrown if the ephemeral public key was not found in the session transcript passed to `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`.
[InvalidReaderSignatureException](../android/security/identity/InvalidReaderSignatureException.md) Thrown if the reader signature is invalid, or it doesn't contain a certificate chain, or if the signature failed to validate.
[InvalidRequestMessageException](../android/security/identity/InvalidRequestMessageException.md) Thrown if message with the request doesn't satisfy the requirements documented in `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`.
[MessageDecryptionException](../android/security/identity/MessageDecryptionException.md) Thrown when failing to decrypt a message from the reader device.
[NoAuthenticationKeyAvailableException](../android/security/identity/NoAuthenticationKeyAvailableException.md) Thrown if no dynamic authentication keys are available.
[SessionTranscriptMismatchException](../android/security/identity/SessionTranscriptMismatchException.md) Thrown when trying use multiple different session transcripts in the same presentation session.
[UnknownAuthenticationKeyException](../android/security/identity/UnknownAuthenticationKeyException.md) Thrown if trying to certify an unknown dynamic authentication key.

> [!CAUTION]
> **This exception was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

Base class for all Identity Credential exceptions.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialException#IdentityCredentialException(kotlin.String)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialException#` exception. |
| `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialException#IdentityCredentialException(kotlin.String,%20kotlin.Throwable)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)` Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialException#` exception. |

## Public constructors

### IdentityCredentialException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IdentityCredentialException(message: String)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialException#` exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |

### IdentityCredentialException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IdentityCredentialException(
    message: String, 
    cause: Throwable)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialException#` exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html): the cause. This value cannot be `null`. |
