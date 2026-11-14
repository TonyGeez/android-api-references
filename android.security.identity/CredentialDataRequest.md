Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CredentialDataRequest

```
open class CredentialDataRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.identity.CredentialDataRequest](CredentialDataRequest.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

An object representing a request for credential data.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest.Builder` A builder for `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest#`. |

| Public methods ||
|---|---|
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest#getDeviceSignedEntriesToRequest()()` Gets the device-signed entries to request. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest#getIssuerSignedEntriesToRequest()()` Gets the issuer-signed entries to request. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest#getReaderSignature()()` Gets the reader signature. |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest#getRequestMessage()()` Gets the request message CBOR. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest#isAllowUsingExhaustedKeys()()` Gets whether to allow using an authentication key which use count has been exceeded. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest#isAllowUsingExpiredKeys()()` Gets whether to allow using an authentication key which is expired. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest#isIncrementUseCount()()` Gets whether to increment the use-count for the authentication key used. |

## Public methods

### getDeviceSignedEntriesToRequest

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeviceSignedEntriesToRequest(): MutableMap<String!, MutableCollection<String!>!>
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the device-signed entries to request.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>` | the device-signed entries to request. This value cannot be `null`. |

### getIssuerSignedEntriesToRequest

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIssuerSignedEntriesToRequest(): MutableMap<String!, MutableCollection<String!>!>
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the issuer-signed entries to request.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>` | the issuer-signed entries to request. This value cannot be `null`. |

### getReaderSignature

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReaderSignature(): ByteArray?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the reader signature.

This data structure is described in the documentation for the `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#getCredentialData(kotlin.String,%20android.security.identity.CredentialDataRequest)` method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | a `COSE_Sign1` structure as described above. This value may be `null`. |

### getRequestMessage

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRequestMessage(): ByteArray?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the request message CBOR.

This data structure is described in the documentation for the `https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession#getCredentialData(kotlin.String,%20android.security.identity.CredentialDataRequest)` method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | the request message CBOR as described above. This value may be `null`. |

### isAllowUsingExhaustedKeys

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAllowUsingExhaustedKeys(): Boolean
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets whether to allow using an authentication key which use count has been exceeded.

By default this is set to true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether to allow using an authentication key which use count has been exceeded if no other key is available. |

### isAllowUsingExpiredKeys

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAllowUsingExpiredKeys(): Boolean
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets whether to allow using an authentication key which is expired.

By default this is set to false.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether to allow using an authentication key which is expired if no other key is available. |

### isIncrementUseCount

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isIncrementUseCount(): Boolean
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets whether to increment the use-count for the authentication key used.

By default this is set to true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether to increment the use count of the authentication key used. |
