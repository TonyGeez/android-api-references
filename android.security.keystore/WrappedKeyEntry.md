# WrappedKeyEntry

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WrappedKeyEntry

Kotlin| [Java](https://developer.android.com/reference/android/security/keystore/WrappedKeyEntry "View this page in Java") 

```
open class WrappedKeyEntry : KeyStore.Entry
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.security.keystore.WrappedKeyEntry](https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry#) |

An [Entry](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry.html#) that holds a wrapped key. Wrapped keys contain encrypted key data and description information that can be used to securely import key material into a hardware-backed Keystore.

The wrapped key is in DER-encoded ASN.1 format, specified by the following schema: 

```kotlin
KeyDescription ::= SEQUENCE(
          keyFormat INTEGER,                   # Values from KeyFormat enum.
          keyParams AuthorizationList,
      )
 
      SecureKeyWrapper ::= SEQUENCE(
          version INTEGER,                     # Contains value 0
          encryptedTransportKey OCTET_STRING,
          initializationVector OCTET_STRING,
          keyDescription KeyDescription,
          encryptedKey OCTET_STRING,
          tag OCTET_STRING
      )
  
```

- keyFormat is an integer from the KeyFormat enum, defining the format of the plaintext key material.
- keyParams is the characteristics of the key to be imported (as with generateKey or importKey). If the secure import is successful, these characteristics must be associated with the key exactly as if the key material had been insecurely imported with importKey. See [Key Attestation](https://developer.android.com/training/articles/security-key-attestation.html#certificate_schema) for the AuthorizationList format.
- encryptedTransportKey is a 256-bit AES key, XORed with a masking key and then encrypted in RSA-OAEP mode (SHA-256 digest, SHA-1 MGF1 digest) with the wrapping key specified by wrappingKeyBlob.
- keyDescription is a KeyDescription, above.
- encryptedKey is the key material of the key to be imported, in format keyFormat, and encrypted with encryptedEphemeralKey in AES-GCM mode, with the DER-encoded representation of keyDescription provided as additional authenticated data.
- tag is the tag produced by the AES-GCM encryption of encryptedKey.

Imported wrapped keys will have KeymasterDefs.KM_ORIGIN_SECURELY_IMPORTED

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WrappedKeyEntry](https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry#WrappedKeyEntry(kotlin.ByteArray,%20kotlin.String,%20kotlin.String,%20java.security.spec.AlgorithmParameterSpec))`(`wrappedKeyBytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `wrappingKeyAlias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `transformation:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `algorithmParameterSpec:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!`)` Constructs a [WrappedKeyEntry](https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry#) with a binary wrapped key. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)! | [getAlgorithmParameterSpec](https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry#getAlgorithmParameterSpec())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTransformation](https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry#getTransformation())`()` <br /> |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getWrappedKeyBytes](https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry#getWrappedKeyBytes())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getWrappingKeyAlias](https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry#getWrappingKeyAlias())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [Entry](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry.html#) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [KeyStore.Entry.Attribute](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry.Attribute.html#)!>! | [getAttributes](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry.html#getAttributes())`()` <br /> Retrieves the attributes associated with an entry. <br /> | ||

## Public constructors

### WrappedKeyEntry

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WrappedKeyEntry(
    wrappedKeyBytes: ByteArray!, 
    wrappingKeyAlias: String!, 
    transformation: String!, 
    algorithmParameterSpec: AlgorithmParameterSpec!)
```

Constructs a [WrappedKeyEntry](https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry#) with a binary wrapped key.

| Parameters ||
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `wrappedKeyBytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:ASN.1 DER encoded wrapped key |
| `wrappingKeyAlias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:identifies the private key that can unwrap the wrapped key |
| `transformation` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:used to unwrap the key. ex: "RSA/ECB/OAEPPadding" |
| `algorithmParameterSpec` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!:spec for the private key used to unwrap the wrapped key |

## Public methods

### getAlgorithmParameterSpec

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlgorithmParameterSpec(): AlgorithmParameterSpec!
```  

### getTransformation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransformation(): String!
```  

### getWrappedKeyBytes

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWrappedKeyBytes(): ByteArray!
```  

### getWrappingKeyAlias

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWrappingKeyAlias(): String!
```
