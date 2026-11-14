Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CredentialDataResult

```
abstract class CredentialDataResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.identity.CredentialDataResult](CredentialDataResult.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

An object that contains the result of retrieving data from a credential. This is used to return data requested in a `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession`.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries` A class for representing data elements returned. |

| Public methods ||
|---|---|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getDeviceMac()()` Returns a message authentication code over the `DeviceAuthenticationBytes` CBOR specified in `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getDeviceNameSpaces()`, to prove to the reader that the data is from a trusted credential. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getDeviceNameSpaces()()` Returns a CBOR structure containing the retrieved device-signed data. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getDeviceSignature()()` Returns a signature over the `DeviceAuthenticationBytes` CBOR specified in `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getDeviceNameSpaces()`, to prove to the reader that the data is from a trusted credential. |
| --- | --- |
| abstract [CredentialDataResult.Entries](../android/security/identity/CredentialDataResult.Entries.md) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getDeviceSignedEntries()()` Gets the device-signed entries that was returned. |
| abstract [CredentialDataResult.Entries](../android/security/identity/CredentialDataResult.Entries.md) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getIssuerSignedEntries()()` Gets the issuer-signed entries that was returned. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getStaticAuthenticationData()()` Returns the static authentication data associated with the dynamic authentication key used to MAC the data returned by `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getDeviceNameSpaces()`. |
| --- | --- |

## Public methods

### getDeviceMac

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDeviceMac(): ByteArray?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Returns a message authentication code over the `DeviceAuthenticationBytes` CBOR specified in `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getDeviceNameSpaces()`, to prove to the reader that the data is from a trusted credential.

The MAC proves to the reader that the data is from a trusted credential. This code is produced by using the key agreement and key derivation function from the ciphersuite with the authentication private key and the reader ephemeral public key to compute a shared message authentication code (MAC) key, then using the MAC function from the ciphersuite to compute a MAC of the authenticated data. See section 9.2.3.5 of ISO/IEC 18013-5 for details of this operation.

If the session transcript or reader ephemeral key wasn't set on the `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession` used to obtain this data no message authencation code will be produced and this method will return `null`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | A COSE_Mac0 structure with the message authentication code as described above or `null` if the conditions specified above are not met. |

### getDeviceNameSpaces

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDeviceNameSpaces(): ByteArray
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Returns a CBOR structure containing the retrieved device-signed data.

This structure - along with the session transcript - may be cryptographically authenticated to prove to the reader that the data is from a trusted credential and `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getDeviceMac()` can be used to get a MAC.

The CBOR structure which is cryptographically authenticated is the `DeviceAuthenticationBytes` structure according to the following [CDDL](https://tools.ietf.org/html/rfc8610) schema:

```kotlin
DeviceAuthentication = [
      "DeviceAuthentication",
      SessionTranscript,
      DocType,
      DeviceNameSpacesBytes
    ]
 
    DocType = tstr
    SessionTranscript = any
    DeviceNameSpacesBytes = #6.24(bstr .cbor DeviceNameSpaces)
    DeviceAuthenticationBytes = #6.24(bstr .cbor DeviceAuthentication)
  
```

where

```kotlin
DeviceNameSpaces = {
      * NameSpace => DeviceSignedItems
    }
 
    DeviceSignedItems = {
      + DataItemName => DataItemValue
    }
 
    NameSpace = tstr
    DataItemName = tstr
    DataItemValue = any
  
```

The returned data is the binary encoding of the `DeviceNameSpaces` structure as defined above.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | The bytes of the `DeviceNameSpaces` CBOR structure. This value cannot be `null`. |

### getDeviceSignature

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeviceSignature(): ByteArray?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Returns a signature over the `DeviceAuthenticationBytes` CBOR specified in `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getDeviceNameSpaces()`, to prove to the reader that the data is from a trusted credential.

The signature is made using the authentication private key. See section 9.1.3.4 of ISO/IEC 18013-5:2021 for details of this operation.

If the session transcript or reader ephemeral key wasn't set on the `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession` used to obtain this data no signature will be produced and this method will return `null`.

This is only implemented in feature version 202301 or later. If not implemented, the call fails with `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IDENTITY_CREDENTIAL_HARDWARE:kotlin.String` for known feature versions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | A COSE_Sign1 structure as described above or `null` if the conditions specified above are not met. |

### getDeviceSignedEntries

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDeviceSignedEntries(): CredentialDataResult.Entries
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the device-signed entries that was returned.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries` | an object to examine the entries returned. This value cannot be `null`. |

### getIssuerSignedEntries

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getIssuerSignedEntries(): CredentialDataResult.Entries
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the issuer-signed entries that was returned.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries` | an object to examine the entries returned. This value cannot be `null`. |

### getStaticAuthenticationData

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getStaticAuthenticationData(): ByteArray
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Returns the static authentication data associated with the dynamic authentication key used to MAC the data returned by `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult#getDeviceNameSpaces()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | The static authentication data associated with dynamic authentication key used to MAC the data. This value cannot be `null`. |
