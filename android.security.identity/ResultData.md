Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResultData

```
abstract class ResultData
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.identity.ResultData](https://developer.android.com/reference/kotlin/android/security/identity/ResultData#) |

> [!CAUTION]
> **This class was deprecated in API level 33.**
>
> Use `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession` instead.

An object that contains the result of retrieving data from a credential. This is used to return data requested from a `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential`.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_NOT_IN_REQUEST_MESSAGE:kotlin.Int` The entry wasn't in the request message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_NOT_REQUESTED:kotlin.Int` The entry was not requested. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_NO_ACCESS_CONTROL_PROFILES:kotlin.Int` The entry was not retrieved because it was configured without any access control profile. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_NO_SUCH_ENTRY:kotlin.Int` The entry does not exist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_OK:kotlin.Int` Value was successfully retrieved. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_READER_AUTHENTICATION_FAILED:kotlin.Int` The entry was not retrieved because reader authentication failed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_USER_AUTHENTICATION_FAILED:kotlin.Int` The entry was not retrieved because user authentication failed. |

| Public methods ||
|---|---|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getAuthenticatedData()()` Returns a CBOR structure containing the retrieved data. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getEntry(kotlin.String,%20kotlin.String)(namespaceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Gets the raw CBOR data for the value of an entry. |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getEntryNames(kotlin.String)(namespaceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Get the names of all entries. |
| --- | --- |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getMessageAuthenticationCode()()` Returns a message authentication code over the `DeviceAuthenticationBytes` CBOR specified in `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getAuthenticatedData()`, to prove to the reader that the data is from a trusted credential. |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getNamespaces()()` Gets the names of namespaces with retrieved entries. |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getRetrievedEntryNames(kotlin.String)(namespaceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Get the names of all entries that was successfully retrieved. |
| --- | --- |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getStaticAuthenticationData()()` Returns the static authentication data associated with the dynamic authentication key used to sign or MAC the data returned by `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getAuthenticatedData()`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getStatus(kotlin.String,%20kotlin.String)(namespaceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Gets the status of an entry. |

## Constants

### STATUS_NOT_IN_REQUEST_MESSAGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NOT_IN_REQUEST_MESSAGE: Int
```

**Deprecated:** *Deprecated in Java.*

The entry wasn't in the request message.

 Value: 3

### STATUS_NOT_REQUESTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NOT_REQUESTED: Int
```

**Deprecated:** *Deprecated in Java.*

The entry was not requested.

 Value: 2

### STATUS_NO_ACCESS_CONTROL_PROFILES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NO_ACCESS_CONTROL_PROFILES: Int
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

The entry was not retrieved because it was configured without any access control profile.

 Value: 6

### STATUS_NO_SUCH_ENTRY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NO_SUCH_ENTRY: Int
```

**Deprecated:** *Deprecated in Java.*

The entry does not exist.

 Value: 1

### STATUS_OK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_OK: Int
```

**Deprecated:** *Deprecated in Java.*

Value was successfully retrieved.

 Value: 0

### STATUS_READER_AUTHENTICATION_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_READER_AUTHENTICATION_FAILED: Int
```

**Deprecated:** *Deprecated in Java.*

The entry was not retrieved because reader authentication failed.

 Value: 5

### STATUS_USER_AUTHENTICATION_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_USER_AUTHENTICATION_FAILED: Int
```

**Deprecated:** *Deprecated in Java.*

The entry was not retrieved because user authentication failed.

 Value: 4

## Public methods

### getAuthenticatedData

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getAuthenticatedData(): ByteArray
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Returns a CBOR structure containing the retrieved data.

This structure - along with the session transcript - may be cryptographically authenticated to prove to the reader that the data is from a trusted credential and `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getMessageAuthenticationCode()` can be used to get a MAC.

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

### getEntry

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEntry(
    namespaceName: String, 
    name: String
): ByteArray?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the raw CBOR data for the value of an entry.

This should only be called on an entry for which the `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getStatus(kotlin.String,%20kotlin.String)` method returns `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_OK:kotlin.Int`.

| Parameters ||
|---|---|
| `namespaceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the namespace name of the entry. This value cannot be `null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the entry to get the value for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | the raw CBOR data or `null` if no entry with the given name exists. |

### getEntryNames

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEntryNames(namespaceName: String): MutableCollection<String!>?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Get the names of all entries.

This includes the name of entries that wasn't successfully retrieved.

| Parameters ||
|---|---|
| `namespaceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the namespace name to get entries for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | A collection of names or `null` if there are no entries for the given namespace. |

### getMessageAuthenticationCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getMessageAuthenticationCode(): ByteArray?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Returns a message authentication code over the `DeviceAuthenticationBytes` CBOR specified in `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getAuthenticatedData()`, to prove to the reader that the data is from a trusted credential.

The MAC proves to the reader that the data is from a trusted credential. This code is produced by using the key agreement and key derivation function from the ciphersuite with the authentication private key and the reader ephemeral public key to compute a shared message authentication code (MAC) key, then using the MAC function from the ciphersuite to compute a MAC of the authenticated data. See section 9.2.3.5 of ISO/IEC 18013-5 for details of this operation.

If the `sessionTranscript` parameter passed to `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)` was `null` or the reader ephmeral public key was never set using `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#setReaderEphemeralPublicKey(java.security.PublicKey)`, no message authencation code will be produced and this method will return `null`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | A COSE_Mac0 structure with the message authentication code as described above or `null` if the conditions specified above are not met. |

### getNamespaces

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getNamespaces(): MutableCollection<String!>
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the names of namespaces with retrieved entries.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | collection of name of namespaces containing retrieved entries. May be empty if no data was retrieved. This value cannot be `null`. |

### getRetrievedEntryNames

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getRetrievedEntryNames(namespaceName: String): MutableCollection<String!>?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Get the names of all entries that was successfully retrieved.

This only return entries for which `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getStatus(kotlin.String,%20kotlin.String)` will return `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_OK:kotlin.Int`.

| Parameters ||
|---|---|
| `namespaceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the namespace name to get entries for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | A collection of names or `null` if there are no entries for the given namespace. |

### getStaticAuthenticationData

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getStaticAuthenticationData(): ByteArray
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Returns the static authentication data associated with the dynamic authentication key used to sign or MAC the data returned by `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#getAuthenticatedData()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | The static authentication data associated with dynamic authentication key used to MAC the data. This value cannot be `null`. |

### getStatus

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getStatus(
    namespaceName: String, 
    name: String
): Int
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the status of an entry.

This returns `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_OK:kotlin.Int` if the value was retrieved, `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_NO_SUCH_ENTRY:kotlin.Int` if the given entry wasn't retrieved, `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_NOT_REQUESTED:kotlin.Int` if it wasn't requested, `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_NOT_IN_REQUEST_MESSAGE:kotlin.Int` if the request message was set but the entry wasn't present in the request message, `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_USER_AUTHENTICATION_FAILED:kotlin.Int` if the value wasn't retrieved because the necessary user authentication wasn't performed, `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_READER_AUTHENTICATION_FAILED:kotlin.Int` if the supplied reader certificate chain didn't match the set of certificates the entry was provisioned with, or `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_NO_ACCESS_CONTROL_PROFILES:kotlin.Int` if the entry was configured without any access control profiles.

| Parameters ||
|---|---|
| `namespaceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the namespace name of the entry. This value cannot be `null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the entry to get the value for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the status indicating whether the value was retrieved and if not, why. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_OK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_NO_SUCH_ENTRY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_NOT_REQUESTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_NOT_IN_REQUEST_MESSAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_USER_AUTHENTICATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_READER_AUTHENTICATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/identity/ResultData#STATUS_NO_ACCESS_CONTROL_PROFILES:kotlin.Int` |
