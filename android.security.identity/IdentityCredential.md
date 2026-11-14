Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IdentityCredential

```
abstract class IdentityCredential
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.identity.IdentityCredential](IdentityCredential.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

Class used to read data from a previously provisioned credential.

## Summary

| Public methods ||
|---|---|
| abstract [KeyPair](../java.security/KeyPair.md) | createEphemeralKeyPair Create an ephemeral key pair to use to establish a secure channel with a reader. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | decryptMessageFromReader Decrypt a message received from the reader. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | delete Deletes a credential. |
| --- | --- |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | encryptMessageToReader Encrypt a message for transmission to the reader. |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [X509Certificate](../java.security.cert/X509Certificate.md)!\> | getAuthKeysNeedingCertification Gets a collection of dynamic authentication keys that need certification. |
| abstract [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | getAuthenticationDataUsageCount Get the number of times the dynamic authentication keys have been used. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AuthenticationKeyMetadata](AuthenticationKeyMetadata.md)!\> | getAuthenticationKeyMetadata Get information about dynamic authentication keys. |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [X509Certificate](../java.security.cert/X509Certificate.md)!\> | getCredentialKeyCertificateChain Gets the X. |
| abstract [ResultData](ResultData.md) | getEntries Retrieve data entries and associated data from this `IdentityCredential`. |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | proveOwnership Proves ownership of a credential. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAllowUsingExhaustedKeys Sets whether to allow using an authentication key which use count has been exceeded if no other key is available. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAllowUsingExpiredKeys Sets whether to allow using an authentication key which has been expired if no other key is available. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAvailableAuthenticationKeys Sets the number of dynamic authentication keys the `IdentityCredential` will maintain, and the number of times each should be used. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAvailableAuthenticationKeys Sets the number of dynamic authentication keys the `IdentityCredential` will maintain, the number of times each should be used, and the minimum amount of time it's valid for. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setReaderEphemeralPublicKey Set the ephemeral public key provided by the reader. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | storeStaticAuthenticationData Store authentication data associated with a dynamic authentication key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | storeStaticAuthenticationData Store authentication data associated with a dynamic authentication key. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | update Updates the credential with new access control profiles and data items. |
| --- | --- |

## Public methods

### createEphemeralKeyPair

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createEphemeralKeyPair(): KeyPair
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Create an ephemeral key pair to use to establish a secure channel with a reader.

Applications should use this key-pair for the communications channel with the reader using a protocol / cipher-suite appropriate for the application. One example of such a protocol is the one used for Mobile Driving Licenses, see ISO 18013-5 section 9.2.1 "Session encryption".

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/KeyPair.html#` | ephemeral key pair to use to establish a secure channel with a reader. This value cannot be `null`. |

### decryptMessageFromReader

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun decryptMessageFromReader(messageCiphertext: ByteArray): ByteArray
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Decrypt a message received from the reader.

Do not use. In this version of the API, this method produces an incorrect result. Instead, applications should implement message encryption/decryption themselves as detailed in the createEphemeralKeyPair method. In a future API-level, this method will be deprecated.

| Parameters ||
|---|---|
| `messageCiphertext` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): encrypted message to decrypt. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | decrypted message. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.security.identity.MessageDecryptionException` | if the ciphertext couldn't be decrypted. |

### delete

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun delete(challenge: ByteArray): ByteArray
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Deletes a credential.

This method returns a COSE_Sign1 data structure signed by the CredentialKey with payload set to `ProofOfDeletion` as defined below.

```kotlin
ProofOfDeletion = [
           "ProofOfDeletion",            ; tstr
           tstr,                         ; DocType
           bstr,                         ; Challenge
           bool                          ; true if this is a test credential, should
                                         ; always be false.
       ]
  
```

This is only implemented in feature version 202101 or later. If not implemented, the call fails with `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IDENTITY_CREDENTIAL_HARDWARE:kotlin.String` for known feature versions.

| Parameters ||
|---|---|
| `challenge` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): is a non-empty byte array whose contents should be unique, fresh and provided by the issuing authority. The value provided is embedded in the generated CBOR and enables the issuing authority to verify that the returned proof is fresh. Implementations are required to support challenges at least 32 bytes of length. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | the COSE_Sign1 data structure above. This value cannot be `null`. |

### encryptMessageToReader

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun encryptMessageToReader(messagePlaintext: ByteArray): ByteArray
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Encrypt a message for transmission to the reader.

Do not use. In this version of the API, this method produces an incorrect result. Instead, applications should implement message encryption/decryption themselves as detailed in the createEphemeralKeyPair method. In a future API-level, this method will be deprecated.

| Parameters ||
|---|---|
| `messagePlaintext` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): unencrypted message to encrypt. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | encrypted message. This value cannot be `null`. |

### getAuthKeysNeedingCertification

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getAuthKeysNeedingCertification(): MutableCollection<X509Certificate!>
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets a collection of dynamic authentication keys that need certification.

When there aren't enough certified dynamic authentication keys, either because the key count has been increased or because one or more keys have reached their usage count or it if a key is too close to its expiration date, this method will generate replacement keys and certificates and return them for issuer certification. The issuer certificates and associated static authentication data must then be provided back to the Identity Credential using storeStaticAuthenticationData. The private part of each authentication key never leaves secure hardware.

Each X.509 certificate is signed by CredentialKey. The certificate chain for CredentialKey can be obtained using the getCredentialKeyCertificateChain method.

If the implementation is feature version 202101 or later, each X.509 certificate contains an X.509 extension at OID 1.3.6.1.4.1.11129.2.1.26 which contains a DER encoded OCTET STRING with the bytes of the CBOR with the following CDDL:

```kotlin
ProofOfBinding = [
      "ProofOfBinding",
      bstr,              // Contains SHA-256(ProofOfProvisioning)
    ]
  
```

This CBOR enables an issuer to determine the exact state of the credential it returns issuer-signed data for.

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IDENTITY_CREDENTIAL_HARDWARE:kotlin.String` for known feature versions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!>` | A collection of X.509 certificates for dynamic authentication keys that need issuer certification. This value cannot be `null`. |

### getAuthenticationDataUsageCount

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getAuthenticationDataUsageCount(): IntArray
```

**Deprecated:** *Use getAuthenticationKeyMetadata instead.*

Get the number of times the dynamic authentication keys have been used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | int array of dynamic authentication key usage counts. This value cannot be `null`. |

### getAuthenticationKeyMetadata

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAuthenticationKeyMetadata(): MutableList<AuthenticationKeyMetadata!>
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Get information about dynamic authentication keys.

The returned list may have `null` values if certification for the dynamic authentication key is pending.

The list is always `keyCount` elements long.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/security/identity/AuthenticationKeyMetadata!>` | list of authentication key metadata objects. |

### getCredentialKeyCertificateChain

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCredentialKeyCertificateChain(): MutableCollection<X509Certificate!>
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the X.509 certificate chain for the CredentialKey which identifies this credential to the issuing authority. This is the same certificate chain that was returned by getCredentialKeyCertificateChain when the credential was first created and its Android Keystore extension will contain the `challenge` data set at that time. See the documentation for that method for important information about this certificate chain.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!>` | the certificate chain for this credential's CredentialKey. This value cannot be `null`. |

### getEntries

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEntries(
    requestMessage: ByteArray?, 
    entriesToRequest: MutableMap<String!, MutableCollection<String!>!>, 
    sessionTranscript: ByteArray?, 
    readerSignature: ByteArray?
): ResultData
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Retrieve data entries and associated data from this `IdentityCredential`.

If an access control check fails for one of the requested entries or if the entry doesn't exist, the entry is simply not returned. The application can detect this by using the getStatus method on each of the requested entries.

It is permissible to call this method multiple times using the same instance but if this is done, the `sessionTranscript` parameter must be identical for each call. If this is not the case, the SessionTranscriptMismatchException exception is thrown. Additionally, if this is done the same auth-key will be used.

The application should not make any assumptions on whether user authentication is needed. Instead, the application should request the data elements values first and then examine the returned ResultData. If `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_USER_AUTHENTICATION_FAILED:kotlin.Int` is returned the application should get a `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.CryptoObject.html#` which references this object and use it with a `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.html#`. Upon successful authentication the application may call getEntries again.

If not `null` the `requestMessage` parameter must contain data for the request from the verifier. The content can be defined in the way appropriate for the credential, but there are three requirements that must be met to work with this API:

- The content must be a CBOR-encoded structure.
- The CBOR structure must be a map.
- The map must contain a tstr key "nameSpaces" whose value contains a map, as described in the example below.

If these requirements are not met the InvalidRequestMessageException exception is thrown.

Here's an example of CBOR which conforms to this requirement:

```kotlin
ItemsRequest = {
      ? "docType" : DocType,
      "nameSpaces" : NameSpaces,
      ? "RequestInfo" : {* tstr => any} ; Additional info the reader wants to provide
    }
 
    DocType = tstr
 
    NameSpaces = {
      + NameSpace => DataElements    ; Requested data elements for each NameSpace
    }
 
    NameSpace = tstr
 
    DataElements = {
      + DataElement => IntentToRetain
    }
 
    DataElement = tstr
    IntentToRetain = bool
  
```

If mdoc session encryption is used (e.g. if createEphemeralKeyPair has been called) and if the `sessionTranscript` parameter is not `null`, the X and Y coordinates of the public part of the key-pair previously generated by createEphemeralKeyPair must appear somewhere in the bytes of the CBOR. Each of these coordinates must appear encoded with the most significant bits first and use the exact amount of bits indicated by the key size of the ephemeral keys. For example, if the ephemeral key is using the P-256 curve then the 32 bytes for the X coordinate encoded with the most significant bits first must appear somewhere in `sessionTranscript` and ditto for the 32 bytes for the Y coordinate.

If `readerSignature` is not `null` it must be the bytes of a `COSE_Sign1` structure as defined in RFC 8152. For the payload nil shall be used and the detached payload is the ReaderAuthenticationBytes CBOR described below.

```kotlin
ReaderAuthentication = [
        "ReaderAuthentication",
        SessionTranscript,
        ItemsRequestBytes
      ]
 
      ItemsRequestBytes = #6.24(bstr .cbor ItemsRequest)
 
      ReaderAuthenticationBytes = #6.24(bstr .cbor ReaderAuthentication)
  
```

where `ItemsRequestBytes` are the bytes in the `requestMessage` parameter.

The public key corresponding to the key used to make the signature, can be found in the `x5chain` unprotected header element of the `COSE_Sign1` structure (as as described in [draft-ietf-cose-x509-04](https://tools.ietf.org/html/draft-ietf-cose-x509-04)). There will be at least one certificate in said element and there may be more (and if so, each certificate must be signed by its successor).

Data elements protected by reader authentication are returned if, and only if, they are mentioned in `requestMessage`, `requestMessage` is signed by the top-most certificate in the reader's certificate chain, and the data element is configured with an AccessControlProfile configured with an X.509 certificate which appears in the certificate chain.

Note that only items referenced in `entriesToRequest` are returned - the `requestMessage` parameter is used only for enforcing reader authentication.

The reason for having `requestMessage` and `entriesToRequest` as separate parameters is that the former represents a request from the remote verifier device (optionally signed) and this allows the application to filter the request to not include data elements which the user has not consented to sharing.

| Parameters ||
|---|---|
| `requestMessage` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: If not `null`, must contain CBOR data conforming to the schema mentioned above. |
| `entriesToRequest` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>: The entries to request, organized as a map of namespace names with each value being a collection of data elements in the given namespace. This value cannot be `null`. |
| `sessionTranscript` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: This value may be `null`. |
| --- | --- |
| `readerSignature` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: A `COSE_Sign1` structure as described above or `null` if reader authentication is not being used. |

| Return ||
|---|---|
| ResultData | A ResultData object containing entry data organized by namespace and a cryptographically authenticated representation of the same data. |

| Exceptions ||
|---|---|
| `android.security.identity.EphemeralPublicKeyNotFoundException` | if the ephemeral public key was not found in the session transcript. |
| `android.security.identity.InvalidReaderSignatureException` | if the reader signature is invalid, or it doesn't contain a certificate chain, or if the signature failed to validate. |
| `android.security.identity.InvalidRequestMessageException` | if the requestMessage is malformed. |
| --- | --- |
| `android.security.identity.NoAuthenticationKeyAvailableException` | if authentication keys were never provisioned, the method setAvailableAuthenticationKeys was called with `keyCount` set to 0, the method setAllowUsingExhaustedKeys was called with `false` and all available authentication keys have been exhausted. |
| `android.security.identity.SessionTranscriptMismatchException` | Thrown when trying use multiple different session transcripts. |

### proveOwnership

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun proveOwnership(challenge: ByteArray): ByteArray
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Proves ownership of a credential.

This method returns a COSE_Sign1 data structure signed by the CredentialKey with payload set to `ProofOfDeletion` as defined below.

The returned CBOR is the following:

```kotlin
ProofOfOwnership = [
           "ProofOfOwnership",           ; tstr
           tstr,                         ; DocType
           bstr,                         ; Challenge
           bool                          ; true if this is a test credential, should
                                         ; always be false.
       ]
  
```

This is only implemented in feature version 202101 or later. If not implemented, the call fails with `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IDENTITY_CREDENTIAL_HARDWARE:kotlin.String` for known feature versions.

| Parameters ||
|---|---|
| `challenge` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): is a non-empty byte array whose contents should be unique, fresh and provided by the issuing authority. The value provided is embedded in the generated CBOR and enables the issuing authority to verify that the returned proof is fresh. Implementations are required to support challenges at least 32 bytes of length. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | the COSE_Sign1 data structure above. This value cannot be `null`. |

### setAllowUsingExhaustedKeys

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setAllowUsingExhaustedKeys(allowUsingExhaustedKeys: Boolean): Unit
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Sets whether to allow using an authentication key which use count has been exceeded if no other key is available. This must be called prior to calling getEntries. By default this is set to true.

| Parameters ||
|---|---|
| `allowUsingExhaustedKeys` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether to allow using an authentication key which use count has been exceeded if no other key is available. |

### setAllowUsingExpiredKeys

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAllowUsingExpiredKeys(allowUsingExpiredKeys: Boolean): Unit
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Sets whether to allow using an authentication key which has been expired if no other key is available. This must be called prior to calling getEntries.

By default this is set to false.

This is only implemented in feature version 202101 or later. If not implemented, the call fails with `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IDENTITY_CREDENTIAL_HARDWARE:kotlin.String` for known feature versions.

| Parameters ||
|---|---|
| `allowUsingExpiredKeys` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether to allow using an authentication key which use count has been exceeded if no other key is available. |

### setAvailableAuthenticationKeys

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setAvailableAuthenticationKeys(
    keyCount: Int, 
    maxUsesPerKey: Int
): Unit
```

**Deprecated:** *Use setAvailableAuthenticationKeys instead.*

Sets the number of dynamic authentication keys the `IdentityCredential` will maintain, and the number of times each should be used.

The Identity Credential system will select the least-used dynamic authentication key each time getEntries is called. Identity Credentials for which this method has not been called behave as though it had been called wit `keyCount` 0 and `maxUsesPerKey` 1.

The effect of this method is like calling setAvailableAuthenticationKeys with the last parameter is set to 0.

| Parameters ||
|---|---|
| `keyCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of active, certified dynamic authentication keys the `IdentityCredential` will try to keep available. This value must be non-negative. |
| `maxUsesPerKey` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of times each of the keys will be used before it's eligible for replacement. This value must be greater than zero. |

### setAvailableAuthenticationKeys

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAvailableAuthenticationKeys(
    keyCount: Int, 
    maxUsesPerKey: Int, 
    minValidTimeMillis: Long
): Unit
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Sets the number of dynamic authentication keys the `IdentityCredential` will maintain, the number of times each should be used, and the minimum amount of time it's valid for.

The Identity Credential system will select the least-used dynamic authentication key each time getEntries is called. Identity Credentials for which this method has not been called behave as though it had been called wit `keyCount` 0, `maxUsesPerKey` 1, and `minValidTimeMillis` 0.

Applications can use getAuthenticationKeyMetadata to get a picture of the usage andtime left of each configured authentication key. This can be used to determine how urgent it is recertify new authentication keys via the getAuthKeysNeedingCertification method.

| Parameters ||
|---|---|
| `keyCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of active, certified dynamic authentication keys the `IdentityCredential` will try to keep available. This value must be non-negative. Value is 0 or greater |
| `maxUsesPerKey` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of times each of the keys will be used before it's eligible for replacement. This value must be greater than zero. Value is 1 or greater |
| `minValidTimeMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): If a key has less time left than this value it will be eliglible for replacement. This value must be non-negative. Value is 0 or greater |
| --- | --- |

### setReaderEphemeralPublicKey

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setReaderEphemeralPublicKey(readerEphemeralPublicKey: PublicKey): Unit
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Set the ephemeral public key provided by the reader. If called, this must be called before getEntries is called.

| Parameters ||
|---|---|
| `readerEphemeralPublicKey` | [PublicKey](../java.security/PublicKey.md): The ephemeral public key provided by the reader to establish a secure session. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.security.InvalidKeyException` | if the given key is invalid. |

### storeStaticAuthenticationData

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun storeStaticAuthenticationData(
    authenticationKey: X509Certificate, 
    staticAuthData: ByteArray
): Unit
```

**Deprecated:** *Use storeStaticAuthenticationData instead.*

Store authentication data associated with a dynamic authentication key. This should only be called for an authenticated key returned by getAuthKeysNeedingCertification.

| Parameters ||
|---|---|
| `authenticationKey` | [X509Certificate](../java.security.cert/X509Certificate.md): The dynamic authentication key for which certification and associated static authentication data is being provided. This value cannot be `null`. |
| `staticAuthData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): Static authentication data provided by the issuer that validates the authenticity and integrity of the credential data fields. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.security.identity.UnknownAuthenticationKeyException` | If the given authentication key is not recognized. |

### storeStaticAuthenticationData

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun storeStaticAuthenticationData(
    authenticationKey: X509Certificate, 
    expirationDate: Instant, 
    staticAuthData: ByteArray
): Unit
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Store authentication data associated with a dynamic authentication key. This should only be called for an authenticated key returned by getAuthKeysNeedingCertification.

| Parameters ||
|---|---|
| `authenticationKey` | [X509Certificate](../java.security.cert/X509Certificate.md): The dynamic authentication key for which certification and associated static authentication data is being provided. This value cannot be `null`. |
| `expirationDate` | [Instant](../java.time/Instant.md): The expiration date of the static authentication data. This value cannot be `null`. |
| `staticAuthData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): Static authentication data provided by the issuer that validates the authenticity and integrity of the credential data fields. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.security.identity.UnknownAuthenticationKeyException` | If the given authentication key is not recognized. |

### update

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun update(personalizationData: PersonalizationData): ByteArray
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Updates the credential with new access control profiles and data items.

This method is similar to personalize except that it operates on an existing credential, see the documentation for that method for the format of the returned data.

If this call succeeds an side-effect is that all dynamic authentication keys for the credential are deleted. The application will need to use getAuthKeysNeedingCertification to generate replacement keys and return them for issuer certification.

This is only implemented in feature version 202101 or later. If not implemented, the call fails with `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IDENTITY_CREDENTIAL_HARDWARE:kotlin.String` for known feature versions.

| Parameters ||
|---|---|
| `personalizationData` | [PersonalizationData](PersonalizationData.md): The data to update, including access control profiles and data elements and their values, grouped into namespaces. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | A COSE_Sign1 data structure, see above. This value cannot be `null`. |
