Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WritableIdentityCredential

```
abstract class WritableIdentityCredential
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.identity.WritableIdentityCredential](../android/security/identity/WritableIdentityCredential.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

Class used to personalize a new identity credential.

Credentials cannot be updated or modified after creation; any changes require deletion and re-creation. Use `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore#createCredential(kotlin.String,%20kotlin.String)` to create a new credential.

## Summary

| Public methods ||
|---|---|
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [X509Certificate](../java/security/cert/X509Certificate.md)!\> | `https://developer.android.com/reference/kotlin/android/security/identity/WritableIdentityCredential#getCredentialKeyCertificateChain(kotlin.ByteArray)(challenge: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Generates and returns an X. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/WritableIdentityCredential#personalize(android.security.identity.PersonalizationData)(personalizationData: https://developer.android.com/reference/kotlin/android/security/identity/PersonalizationData)` Stores all of the data in the credential, with the specified access control profiles. |

## Public methods

### getCredentialKeyCertificateChain

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCredentialKeyCertificateChain(challenge: ByteArray): MutableCollection<X509Certificate!>
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Generates and returns an X.509 certificate chain for the CredentialKey which identifies this credential to the issuing authority. The certificate contains an [Android Keystore](https://source.android.com/security/keystore/attestation) attestation extension which describes the key and the security hardware in which it lives.

Additionally, the attestation extension will contain the tag Tag::IDENTITY_CREDENTIAL_KEY which indicates it is an Identity Credential key (which can only sign/MAC very specific messages) and not an Android Keystore key (which can be used to sign/MAC anything).

The issuer **MUST** carefully examine this certificate chain including (but not limited to) checking that the root certificate is well-known, the tag Tag::IDENTITY_CREDENTIAL_KEY present, the passed in challenge is present, the tag Tag::ATTESTATION_APPLICATION_ID is set to the expected Android application, the device has verified boot enabled, each certificate in the chain is signed by its successor, none of the certificates have been revoked, and so on.

It is not strictly necessary to use this method to provision a credential if the issuing authority doesn't care about the nature of the security hardware. If called, however, this method must be called before `https://developer.android.com/reference/kotlin/android/security/identity/WritableIdentityCredential#personalize(android.security.identity.PersonalizationData)`.

| Parameters ||
|---|---|
| `challenge` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): is a non-empty byte array whose contents should be unique, fresh and provided by the issuing authority. The value provided is embedded in the attestation extension and enables the issuing authority to verify that the attestation certificate is fresh. Implementations are required to support challenges at least 32 bytes of length. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!>` | the X.509 certificate for this credential's CredentialKey. This value cannot be `null`. |

### personalize

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun personalize(personalizationData: PersonalizationData): ByteArray
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Stores all of the data in the credential, with the specified access control profiles.

This method returns a COSE_Sign1 data structure signed by the CredentialKey with payload set to `ProofOfProvisioning` as defined below.

```kotlin
ProofOfProvisioning = [
           "ProofOfProvisioning",        ; tstr
           tstr,                         ; DocType
           [ * AccessControlProfile ],
           ProvisionedData,
           bool                          ; true if this is a test credential, should
                                         ; always be false.
       ]
 
       AccessControlProfile = {
           "id": uint,
           ? "readerCertificate" : bstr,
           ? (
                "userAuthenticationRequired" : bool,
                "timeoutMillis" : uint,
           )
       }
 
       ProvisionedData = {
           * Namespace => [ + Entry ]
       },
 
       Namespace = tstr
 
       Entry = {
           "name" : tstr,
           "value" : any,
           "accessControlProfiles" : [ * uint ],
       }
  
```

This data structure provides a guarantee to the issuer about the data which may be returned in the CBOR returned by `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getAuthenticatedData()` during a credential presentation.

| Parameters ||
|---|---|
| `personalizationData` | [PersonalizationData](../android/security/identity/PersonalizationData.md): The data to provision, including access control profiles and data elements and their values, grouped into namespaces. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | A COSE_Sign1 data structure, see above. This value cannot be `null`. |
