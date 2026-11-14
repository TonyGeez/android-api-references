Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IdentityCredentialStore

```
abstract class IdentityCredentialStore
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.security.identity.IdentityCredentialStore](https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#) |

> [!CAUTION]
> **This class was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

An interface to a secure store for user identity documents.

This interface is deliberately fairly general and abstract. To the extent possible, specification of the message formats and semantics of communication with credential verification devices and issuing authorities (IAs) is out of scope. It provides the interface with secure storage but a credential-specific Android application will be required to implement the presentation and verification protocols and processes appropriate for the specific credential type.

Multiple credentials can be created. Each credential comprises:

- A document type, which is a string.
- A set of namespaces, which serve to disambiguate value names. It is recommended that namespaces be structured as reverse domain names so that IANA effectively serves as the namespace registrar.
- For each namespace, a set of name/value pairs, each with an associated set of access control profile IDs. Names are strings and values are typed and can be any value supported by [CBOR](http://cbor.io/).
- A set of access control profiles (up to 32), each with a profile ID and a specification of the conditions which satisfy the profile's requirements.
- An asymmetric key pair which is used to authenticate the credential to the Issuing Authority, called the *CredentialKey*.
- A set of zero or more named reader authentication public keys, which are used to authenticate an authorized reader to the credential.
- A set of named signing keys, which are used to sign collections of values and session transcripts.

Implementing support for user identity documents in secure storage requires dedicated hardware-backed support and may not always be available.

Two different credential stores exist - the *default* store and the *direct access* store. Most often credentials will be accessed through the default store but that requires that the Android device be powered up and fully functional. It is desirable to allow identity credential usage when the Android device's battery is too low to boot the Android operating system, so direct access to the secure hardware via NFC may allow data retrieval, if the secure hardware chooses to implement it.

Credentials provisioned to the direct access store should **always** use reader authentication to protect data elements. The reason for this is user authentication or user approval of data release is not possible when the device is off.

The Identity Credential API is designed to be able to evolve and change over time but still provide 100% backwards compatibility. This is complicated by the fact that there may be a version skew between the API used by the application and the version implemented in secure hardware. To solve this problem, the API provides for a way for the application to query which feature version the hardware implements (if any at all) using android.content.pm#FEATURE_IDENTITY_CREDENTIAL_HARDWARE and android.content.pm#FEATURE_IDENTITY_CREDENTIAL_HARDWARE_DIRECT_ACCESS. Methods which only work on certain feature versions are clearly documented as such.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#CIPHERSUITE_ECDHE_HKDF_ECDSA_WITH_AES_256_GCM_SHA256:kotlin.Int` Specifies that the cipher suite that will be used to secure communications between the reader and the prover is using the following primitives - ECKA-DH (Elliptic Curve Key Agreement Algorithm - Diffie-Hellman, see BSI TR-03111). - HKDF-SHA-256 (see RFC 5869). - AES-256-GCM (see NIST SP 800-38D). - HMAC-SHA-256 (see RFC 2104). <br /> |

| Public methods ||
|---|---|
| abstract [WritableIdentityCredential](https://developer.android.com/reference/kotlin/android/security/identity/WritableIdentityCredential) | `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#createCredential(kotlin.String,%20kotlin.String)(credentialName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, docType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Creates a new credential. |
| open [PresentationSession](https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession) | `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#createPresentationSession(kotlin.Int)(cipherSuite: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new presentation session. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#deleteCredentialByName(kotlin.String)(credentialName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Delete a named credential. |
| abstract [IdentityCredential](https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential)? | `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#getCredentialByName(kotlin.String,%20kotlin.Int)(credentialName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, cipherSuite: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve a named credential. |
| open static [IdentityCredentialStore](https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#)? | `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#getDirectAccessInstance(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Gets the `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#` for direct access. |
| open static [IdentityCredentialStore](https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#)? | `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#getInstance(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Gets the default `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#`. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#getSupportedDocTypes()()` Gets a list of supported document types. |

## Constants

### CIPHERSUITE_ECDHE_HKDF_ECDSA_WITH_AES_256_GCM_SHA256

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CIPHERSUITE_ECDHE_HKDF_ECDSA_WITH_AES_256_GCM_SHA256: Int
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Specifies that the cipher suite that will be used to secure communications between the reader and the prover is using the following primitives

- ECKA-DH (Elliptic Curve Key Agreement Algorithm - Diffie-Hellman, see BSI TR-03111).
- HKDF-SHA-256 (see RFC 5869).
- AES-256-GCM (see NIST SP 800-38D).
- HMAC-SHA-256 (see RFC 2104).

<br />

The exact way these primitives are combined to derive the session key is specified in section 9.2.1.4 of ISO/IEC 18013-5 (see description of cipher suite '1').

At present this is the only supported cipher suite.

 Value: 1

## Public methods

### createCredential

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createCredential(
    credentialName: String, 
    docType: String
): WritableIdentityCredential
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Creates a new credential.

When a credential is created, a cryptographic key-pair - CredentialKey - is created which is used to authenticate the store to the Issuing Authority. The private part of this key-pair never leaves secure hardware and the public part can be obtained using `https://developer.android.com/reference/kotlin/android/security/identity/WritableIdentityCredential#getCredentialKeyCertificateChain(kotlin.ByteArray)` on the returned object.

In addition, all of the Credential data content is imported and a certificate for the CredentialKey and a signature produced with the CredentialKey are created. These latter values may be checked by an issuing authority to verify that the data was imported into secure hardware and that it was imported unmodified.

| Parameters ||
|---|---|
| `credentialName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name used to identify the credential. This value cannot be `null`. |
| `docType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The document type for the credential. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/WritableIdentityCredential` | A `https://developer.android.com/reference/kotlin/android/security/identity/WritableIdentityCredential` that can be used to create a new credential. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.security.identity.AlreadyPersonalizedException` | if a credential with the given name already exists. |
| `android.security.identity.DocTypeNotSupportedException` | if the given document type isn't supported by the store. |

### createPresentationSession

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createPresentationSession(cipherSuite: Int): PresentationSession
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Creates a new presentation session.

This method gets an object to be used for interaction with a remote verifier for presentation of one or more credentials.

This is only implemented in feature version 202201 or later. If not implemented, the call fails with `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IDENTITY_CREDENTIAL_HARDWARE:kotlin.String` for known feature versions.

| Parameters ||
|---|---|
| `cipherSuite` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the cipher suite to use for communicating with the verifier. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#CIPHERSUITE_ECDHE_HKDF_ECDSA_WITH_AES_256_GCM_SHA256:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession` | The presentation session. This value cannot be `null`. |

### deleteCredentialByName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun deleteCredentialByName(credentialName: String): ByteArray?
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#delete(kotlin.ByteArray)` instead.*

Delete a named credential.

This method returns a COSE_Sign1 data structure signed by the CredentialKey with payload set to `ProofOfDeletion` as defined below:

```kotlin
ProofOfDeletion = [
           "ProofOfDeletion",            ; tstr
           tstr,                         ; DocType
           bool                          ; true if this is a test credential, should
                                         ; always be false.
       ]
  
```

| Parameters ||
|---|---|
| `credentialName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the credential to delete. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | `null` if the credential was not found, the COSE_Sign1 data structure above if the credential was found and deleted. |

### getCredentialByName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCredentialByName(
    credentialName: String, 
    cipherSuite: Int
): IdentityCredential?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Retrieve a named credential.

The cipher suite used to communicate with the remote verifier must also be specified. Currently only a single cipher-suite is supported. Support for other cipher suites may be added in a future version of this API.

| Parameters ||
|---|---|
| `credentialName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the credential to retrieve. This value cannot be `null`. |
| `cipherSuite` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the cipher suite to use for communicating with the verifier. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#CIPHERSUITE_ECDHE_HKDF_ECDSA_WITH_AES_256_GCM_SHA256:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential?` | The named credential, or null if not found. |

### getDirectAccessInstance

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDirectAccessInstance(context: Context): IdentityCredentialStore?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#` for direct access.

Direct access requires specialized NFC hardware and may not be supported on all devices even if default store is available. Credentials provisioned to the direct access store should **always** use reader authentication to protect data elements.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): the application context. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#?` | the `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#` or `null` if direct access is not supported on this device. |

### getInstance

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(context: Context): IdentityCredentialStore?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the default `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#`.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): the application context. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#?` | the `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#` or `null` if the device doesn't have hardware-backed support for secure storage of user identity documents. |

### getSupportedDocTypes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSupportedDocTypes(): Array<String!>
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets a list of supported document types.

Only the direct-access store may restrict the kind of document types that can be used for credentials. The default store always supports any document type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | The supported document types or the empty array if any document type is supported. This value cannot be `null`. |
