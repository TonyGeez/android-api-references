# Certificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Certificate

```
abstract class Certificate : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.Certificate](Certificate.md) |

| Known Direct Subclasses [X509Certificate](X509Certificate.md) |------------------------------------------------------------------------------------------------------|-----------------------| | [X509Certificate](X509Certificate.md) | Abstract class for X. | |
| --- | --- | --- | --- | --- | --- | --- |

Abstract class for managing a variety of identity certificates. An identity certificate is a binding of a principal to a public key which is vouched for by another principal. (A principal represents an entity such as an individual user, a group, or a corporation.)

This class is an abstraction for certificates that have different formats but important common uses. For example, different types of certificates, such as X.509 and PGP, share general certificate functionality (like encoding and verifying) and some types of information (like a public key).

X.509, PGP, and SDSI certificates can all be implemented by subclassing the Certificate class, even though they contain different sets of information, and they store and retrieve the information in different ways.

## Summary

| Nested classes ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [CertificateRep](../java/security/cert/Certificate.CertificateRep.md) Alternate Certificate class for serialization. |

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Certificate](Certificate.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a certificate of the specified type. |

| Public methods ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Certificate.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this certificate for equality with the specified object. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](Certificate.md))`()` Returns the encoded form of this certificate. |
| abstract [PublicKey](../java.security/PublicKey.md)! | [getPublicKey](Certificate.md))`()` Gets the public key from this certificate. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](Certificate.md))`()` Returns the type of this certificate. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Certificate.md))`()` Returns a hashcode value for this certificate from its encoded form. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Certificate.md))`()` Returns a string representation of this certificate. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](Certificate.md))`(`key:` ` [PublicKey](../java.security/PublicKey.md)!`)` Verifies that this certificate was signed using the private key that corresponds to the specified public key. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](Certificate.md))`(`key:` ` [PublicKey](../java.security/PublicKey.md)!`, `sigProvider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Verifies that this certificate was signed using the private key that corresponds to the specified public key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](Certificate.md))`(`key:` ` [PublicKey](../java.security/PublicKey.md)!`, `sigProvider:` ` [Provider](../java.security/Provider.md)!`)` Verifies that this certificate was signed using the private key that corresponds to the specified public key. |
| --- | --- |

| Protected methods ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [writeReplace](Certificate.md))`()` Replace the Certificate to be serialized. |

## Protected constructors

### Certificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Certificate(type: String!)
```

Creates a certificate of the specified type.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the certificate type. See the CertificateFactory section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certificatefactory-types) for information about standard certificate types. |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this certificate for equality with the specified object. If the`other`object is an`instanceof``Certificate`, then its encoded form is retrieved and compared with the encoded form of this certificate.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object to test for equality with this certificate. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the encoded forms of the two certificates match, false otherwise. |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncoded(): ByteArray!
```

Returns the encoded form of this certificate. It is assumed that each certificate type would have only a single form of encoding; for example, X.509 certificates would be encoded as ASN.1 DER.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the encoded form of this certificate |

| Exceptions ||
|---------------------------------------------------|------------------------------|
| `java.security.cert.CertificateEncodingException` | if an encoding error occurs. |

### getPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPublicKey(): PublicKey!
```

Gets the public key from this certificate.

| Return ||
|--------------------------------------------------------------------------------------------|-----------------|
| [PublicKey](../java.security/PublicKey.md)! | the public key. |

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): String!
```

Returns the type of this certificate.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the type of this certificate. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hashcode value for this certificate from its encoded form.

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hashcode value. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toString(): String
```

Returns a string representation of this certificate.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this certificate. |

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun verify(key: PublicKey!): Unit
```

Verifies that this certificate was signed using the private key that corresponds to the specified public key.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [PublicKey](../java.security/PublicKey.md)!:the PublicKey used to carry out the verification. |

| Exceptions ||
|-------------------------------------------|--------------------------------------|
| `java.security.NoSuchAlgorithmException` | on unsupported signature algorithms. |
| `java.security.InvalidKeyException` | on incorrect key. |
| `java.security.NoSuchProviderException` | if there's no default provider. |
| --- | --- |
| `java.security.SignatureException` | on signature errors. |
| `java.security.cert.CertificateException` | on encoding errors. |

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun verify(
    key: PublicKey!, 
    sigProvider: String!
): Unit
```

Verifies that this certificate was signed using the private key that corresponds to the specified public key. This method uses the signature verification engine supplied by the specified provider.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [PublicKey](../java.security/PublicKey.md)!:the PublicKey used to carry out the verification. |
| `sigProvider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the signature provider. |

| Exceptions ||
|-------------------------------------------|--------------------------------------|
| `java.security.NoSuchAlgorithmException` | on unsupported signature algorithms. |
| `java.security.InvalidKeyException` | on incorrect key. |
| `java.security.NoSuchProviderException` | on incorrect provider. |
| --- | --- |
| `java.security.SignatureException` | on signature errors. |
| `java.security.cert.CertificateException` | on encoding errors. |

### verify

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun verify(
    key: PublicKey!, 
    sigProvider: Provider!
): Unit
```

Verifies that this certificate was signed using the private key that corresponds to the specified public key. This method uses the signature verification engine supplied by the specified provider. Note that the specified Provider object does not have to be registered in the provider list.

This method was added to version 1.8 of the Java Platform Standard Edition. In order to maintain backwards compatibility with existing service providers, this method cannot be`abstract`and by default throws an`UnsupportedOperationException`.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [PublicKey](../java.security/PublicKey.md)!:the PublicKey used to carry out the verification. |
| `sigProvider` | [Provider](../java.security/Provider.md)!:the signature provider. |

| Exceptions ||
|-------------------------------------------|--------------------------------------|
| `java.security.NoSuchAlgorithmException` | on unsupported signature algorithms. |
| `java.security.InvalidKeyException` | on incorrect key. |
| `java.security.SignatureException` | on signature errors. |
| --- | --- |
| `java.security.cert.CertificateException` | on encoding errors. |
| `java.lang.UnsupportedOperationException` | if the method is not supported |

## Protected methods

### writeReplace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun writeReplace(): Any!
```

Replace the Certificate to be serialized.

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the alternate Certificate object to be serialized |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------|
| `java.io.ObjectStreamException` | if a new object representing this Certificate could not be created |
