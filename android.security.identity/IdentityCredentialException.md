Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IdentityCredentialException

```
open class IdentityCredentialException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.security.identity.IdentityCredentialException](https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialException#) |

Known Direct Subclasses [AlreadyPersonalizedException](https://developer.android.com/reference/kotlin/android/security/identity/AlreadyPersonalizedException), [CipherSuiteNotSupportedException](https://developer.android.com/reference/kotlin/android/security/identity/CipherSuiteNotSupportedException), [DocTypeNotSupportedException](https://developer.android.com/reference/kotlin/android/security/identity/DocTypeNotSupportedException), [EphemeralPublicKeyNotFoundException](https://developer.android.com/reference/kotlin/android/security/identity/EphemeralPublicKeyNotFoundException), [InvalidReaderSignatureException](https://developer.android.com/reference/kotlin/android/security/identity/InvalidReaderSignatureException), [InvalidRequestMessageException](https://developer.android.com/reference/kotlin/android/security/identity/InvalidRequestMessageException), [MessageDecryptionException](https://developer.android.com/reference/kotlin/android/security/identity/MessageDecryptionException), [NoAuthenticationKeyAvailableException](https://developer.android.com/reference/kotlin/android/security/identity/NoAuthenticationKeyAvailableException), [SessionTranscriptMismatchException](https://developer.android.com/reference/kotlin/android/security/identity/SessionTranscriptMismatchException), [UnknownAuthenticationKeyException](https://developer.android.com/reference/kotlin/android/security/identity/UnknownAuthenticationKeyException) [AlreadyPersonalizedException](https://developer.android.com/reference/kotlin/android/security/identity/AlreadyPersonalizedException) Thrown if trying to create a credential which already exists.
[CipherSuiteNotSupportedException](https://developer.android.com/reference/kotlin/android/security/identity/CipherSuiteNotSupportedException) Thrown if trying to use a cipher suite which isn't supported.
[DocTypeNotSupportedException](https://developer.android.com/reference/kotlin/android/security/identity/DocTypeNotSupportedException) Thrown if trying to create a credential with an unsupported document type.
[EphemeralPublicKeyNotFoundException](https://developer.android.com/reference/kotlin/android/security/identity/EphemeralPublicKeyNotFoundException) Thrown if the ephemeral public key was not found in the session transcript passed to `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`.
[InvalidReaderSignatureException](https://developer.android.com/reference/kotlin/android/security/identity/InvalidReaderSignatureException) Thrown if the reader signature is invalid, or it doesn't contain a certificate chain, or if the signature failed to validate.
[InvalidRequestMessageException](https://developer.android.com/reference/kotlin/android/security/identity/InvalidRequestMessageException) Thrown if message with the request doesn't satisfy the requirements documented in `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`.
[MessageDecryptionException](https://developer.android.com/reference/kotlin/android/security/identity/MessageDecryptionException) Thrown when failing to decrypt a message from the reader device.
[NoAuthenticationKeyAvailableException](https://developer.android.com/reference/kotlin/android/security/identity/NoAuthenticationKeyAvailableException) Thrown if no dynamic authentication keys are available.
[SessionTranscriptMismatchException](https://developer.android.com/reference/kotlin/android/security/identity/SessionTranscriptMismatchException) Thrown when trying use multiple different session transcripts in the same presentation session.
[UnknownAuthenticationKeyException](https://developer.android.com/reference/kotlin/android/security/identity/UnknownAuthenticationKeyException) Thrown if trying to certify an unknown dynamic authentication key.

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
