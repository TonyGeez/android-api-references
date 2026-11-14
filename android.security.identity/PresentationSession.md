Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PresentationSession

```
abstract class PresentationSession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.identity.PresentationSession](../android/security/identity/PresentationSession.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

Class for presenting multiple documents to a remote verifier.

This should be used for all interactions with a remote verifier instead of the now deprecated `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)` method. Use `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#createPresentationSession(kotlin.Int)` to create a `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#` instance.

## Summary

| Public methods ||
|---|---|
| abstract [CredentialDataResult](../android/security/identity/CredentialDataResult.md)? | `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#getCredentialData(kotlin.String,%20android.security.identity.CredentialDataRequest)(credentialName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, request: https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest)` Retrieves data from a named credential in the current presentation session. |
| abstract [KeyPair](../java/security/KeyPair.md) | `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#getEphemeralKeyPair()()` Gets the ephemeral key pair to use to establish a secure channel with the verifier. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#setReaderEphemeralPublicKey(java.security.PublicKey)(readerEphemeralPublicKey: https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)` Set the ephemeral public key provided by the verifier. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#setSessionTranscript(kotlin.ByteArray)(sessionTranscript: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Set the session transcript. |

## Public methods

### getCredentialData

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCredentialData(
    credentialName: String, 
    request: CredentialDataRequest
): CredentialDataResult?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Retrieves data from a named credential in the current presentation session.

If an access control check fails for one of the requested entries or if the entry doesn't exist, the entry is simply not returned. The application can detect this by using the `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#getStatus(kotlin.String,%20kotlin.String)` method on each of the requested entries.

The application should not make any assumptions on whether user authentication is needed. Instead, the application should request the data elements values first and then examine the returned `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries`. If `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_USER_AUTHENTICATION_FAILED:kotlin.Int` is returned the application should get a `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.CryptoObject.html#` which references this object and use it with a `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.html#`. Upon successful authentication the application may call `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#getCredentialData(kotlin.String,%20android.security.identity.CredentialDataRequest)` again.

It is permissible to call this method multiple times using the same credential name. If this is done the same auth-key will be used.

If the reader signature is set in the request parameter (via the `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest.Builder#setReaderSignature(kotlin.ByteArray)` method) it must contain the bytes of a `COSE_Sign1` structure as defined in RFC 8152. For the payload `nil` shall be used and the detached payload is the `ReaderAuthenticationBytes` CBOR described below.

```kotlin
ReaderAuthentication = [
        "ReaderAuthentication",
        SessionTranscript,
        ItemsRequestBytes
      ]
 
      ItemsRequestBytes = #6.24(bstr .cbor ItemsRequest)
 
      ReaderAuthenticationBytes = #6.24(bstr .cbor ReaderAuthentication)
  
```

where `ItemsRequestBytes` are the bytes of the request message set in the request parameter (via the `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest.Builder#setRequestMessage(kotlin.ByteArray)` method).

The public key corresponding to the key used to make the signature, can be found in the `x5chain` unprotected header element of the `COSE_Sign1` structure (as as described in [draft-ietf-cose-x509-08](https://tools.ietf.org/html/draft-ietf-cose-x509-08)). There will be at least one certificate in said element and there may be more (and if so, each certificate must be signed by its successor).

Data elements protected by reader authentication are returned if, and only if, `requestMessage` is signed by the top-most certificate in the reader's certificate chain, and the data element is configured with an `https://developer.android.com/reference/kotlin/android/security/identity/AccessControlProfile` configured with an X.509 certificate for a key which appear in the certificate chain.

Note that the request message CBOR is used only for enforcing reader authentication, it's not used for determining which entries this API will return. The application is expected to have parsed the request message and filtered it according to user preference and/or consent.

| Parameters ||
|---|---|
| `credentialName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the credential to retrieve. This value cannot be `null`. |
| `request` | [CredentialDataRequest](../android/security/identity/CredentialDataRequest.md): the data to retrieve from the credential. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult?` | If the credential wasn't found, returns null. Otherwise a `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult` object containing entry data organized by namespace and a cryptographically authenticated representation of the same data, bound to the current session. |

| Exceptions ||
|---|---|
| `android.security.identity.EphemeralPublicKeyNotFoundException` | if the ephemeral public key was not found in the session transcript. |
| `android.security.identity.InvalidReaderSignatureException` | if the reader signature is invalid, or it doesn't contain a certificate chain, or if the signature failed to validate. |
| `android.security.identity.InvalidRequestMessageException` | if the requestMessage is malformed. |
| --- | --- |
| `android.security.identity.NoAuthenticationKeyAvailableException` | if authentication keys were never provisioned for the credential or if they are expired or exhausted their use-count. |

### getEphemeralKeyPair

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEphemeralKeyPair(): KeyPair
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the ephemeral key pair to use to establish a secure channel with the verifier.

Applications should use this key-pair for the communications channel with the verifier using a protocol / cipher-suite appropriate for the application. One example of such a protocol is the one used for Mobile Driving Licenses, see ISO 18013-5.

The ephemeral key pair is tied to the `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#` instance so subsequent calls to this method will return the same key-pair.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/KeyPair.html#` | ephemeral key pair to use to establish a secure channel with a reader. This value cannot be `null`. |

### setReaderEphemeralPublicKey

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setReaderEphemeralPublicKey(readerEphemeralPublicKey: PublicKey): Unit
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Set the ephemeral public key provided by the verifier.

If called, this must be called before any calls to `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#getCredentialData(kotlin.String,%20android.security.identity.CredentialDataRequest)`.

This method can only be called once per `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#` instance.

| Parameters ||
|---|---|
| `readerEphemeralPublicKey` | [PublicKey](../java/security/PublicKey.md): The ephemeral public key provided by the reader to establish a secure session. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.security.InvalidKeyException` | if the given key is invalid. |

### setSessionTranscript

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setSessionTranscript(sessionTranscript: ByteArray): Unit
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Set the session transcript.

If called, this must be called before any calls to `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#getCredentialData(kotlin.String,%20android.security.identity.CredentialDataRequest)`.

If mdoc session encryption is used (e.g. if `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#getEphemeralKeyPair()` has been called) then the X and Y coordinates of the public part of the key-pair returned by `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#getEphemeralKeyPair()` must appear somewhere in the bytes of the passed in CBOR. Each of these coordinates must appear encoded with the most significant bits first and use the exact amount of bits indicated by the key size of the ephemeral keys. For example, if the ephemeral key is using the P-256 curve then the 32 bytes for the X coordinate encoded with the most significant bits first must appear somewhere and ditto for the 32 bytes for the Y coordinate.

This method can only be called once per `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#` instance.

| Parameters ||
|---|---|
| `sessionTranscript` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the session transcript. This value cannot be `null`. |
