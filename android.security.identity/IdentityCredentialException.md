Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IdentityCredentialException

```
open class IdentityCredentialException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.security.identity.IdentityCredentialException](IdentityCredentialException.md) |
| --- | --- | --- | --- |

Known Direct Subclasses [AlreadyPersonalizedException](AlreadyPersonalizedException.md), [CipherSuiteNotSupportedException](CipherSuiteNotSupportedException.md), [DocTypeNotSupportedException](DocTypeNotSupportedException.md), [EphemeralPublicKeyNotFoundException](EphemeralPublicKeyNotFoundException.md), [InvalidReaderSignatureException](InvalidReaderSignatureException.md), [InvalidRequestMessageException](InvalidRequestMessageException.md), [MessageDecryptionException](MessageDecryptionException.md), [NoAuthenticationKeyAvailableException](NoAuthenticationKeyAvailableException.md), [SessionTranscriptMismatchException](SessionTranscriptMismatchException.md), [UnknownAuthenticationKeyException](UnknownAuthenticationKeyException.md) [AlreadyPersonalizedException](AlreadyPersonalizedException.md) Thrown if trying to create a credential which already exists.
[CipherSuiteNotSupportedException](CipherSuiteNotSupportedException.md) Thrown if trying to use a cipher suite which isn't supported.
[DocTypeNotSupportedException](DocTypeNotSupportedException.md) Thrown if trying to create a credential with an unsupported document type.
[EphemeralPublicKeyNotFoundException](EphemeralPublicKeyNotFoundException.md) Thrown if the ephemeral public key was not found in the session transcript passed to getEntries.
[InvalidReaderSignatureException](InvalidReaderSignatureException.md) Thrown if the reader signature is invalid, or it doesn't contain a certificate chain, or if the signature failed to validate.
[InvalidRequestMessageException](InvalidRequestMessageException.md) Thrown if message with the request doesn't satisfy the requirements documented in getEntries.
[MessageDecryptionException](MessageDecryptionException.md) Thrown when failing to decrypt a message from the reader device.
[NoAuthenticationKeyAvailableException](NoAuthenticationKeyAvailableException.md) Thrown if no dynamic authentication keys are available.
[SessionTranscriptMismatchException](SessionTranscriptMismatchException.md) Thrown when trying use multiple different session transcripts in the same presentation session.
[UnknownAuthenticationKeyException](UnknownAuthenticationKeyException.md) Thrown if trying to certify an unknown dynamic authentication key.

> [!CAUTION]
> **This exception was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

Base class for all Identity Credential exceptions.

## Summary

| Public constructors ||
|---|---|
| IdentityCredentialException Constructs a new IdentityCredentialException exception. |
| IdentityCredentialException Constructs a new IdentityCredentialException exception. |

## Public constructors

### IdentityCredentialException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IdentityCredentialException(message: String)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new IdentityCredentialException exception.

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

Constructs a new IdentityCredentialException exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html): the cause. This value cannot be `null`. |
