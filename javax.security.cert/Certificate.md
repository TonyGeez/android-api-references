# Certificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Certificate

```
abstract class Certificate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.security.cert.Certificate](../javax/security/cert/Certificate.md) |

| Known Direct Subclasses [X509Certificate](../javax/security/cert/X509Certificate.md) |-------------------------------------------------------------------------------------------------------|-----------------------| | [X509Certificate](../javax/security/cert/X509Certificate.md) | Abstract class for X. | |
| --- | --- | --- | --- | --- | --- | --- |

Abstract class for managing a variety of identity certificates. An identity certificate is a guarantee by a principal that a public key is that of another principal. (A principal represents an entity such as an individual user, a group, or a corporation.)

This class is an abstraction for certificates that have different formats but important common uses. For example, different types of certificates, such as X.509 and PGP, share general certificate functionality (like encoding and verifying) and some types of information (like a public key).

X.509, PGP, and SDSI certificates can all be implemented by subclassing the Certificate class, even though they contain different sets of information, and they store and retrieve the information in different ways.

*Note: The classes in the package`javax.security.cert`exist for compatibility with earlier versions of the Java Secure Sockets Extension (JSSE). New applications should instead use the standard Java SE certificate classes located in`java.security.cert`.*

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------|---|
| [Certificate](../javax/security/cert/Certificate.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../javax/security/cert/Certificate.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this certificate for equality with the specified object. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](../javax/security/cert/Certificate.md))`()` Returns the encoded form of this certificate. |
| abstract [PublicKey](../java/security/PublicKey.md)! | [getPublicKey](../javax/security/cert/Certificate.md))`()` Gets the public key from this certificate. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../javax/security/cert/Certificate.md))`()` Returns a hashcode value for this certificate from its encoded form. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../javax/security/cert/Certificate.md))`()` Returns a string representation of this certificate. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](../javax/security/cert/Certificate.md))`(`key:` ` [PublicKey](../java/security/PublicKey.md)!`)` Verifies that this certificate was signed using the private key that corresponds to the specified public key. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](../javax/security/cert/Certificate.md))`(`key:` ` [PublicKey](../java/security/PublicKey.md)!`, `sigProvider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Verifies that this certificate was signed using the private key that corresponds to the specified public key. |

## Public constructors

### Certificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Certificate()
```

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
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the encoded forms of the two certificates match, false otherwise. |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncoded(): ByteArray!
```

Returns the encoded form of this certificate. It is assumed that each certificate type would have only a single form of encoding; for example, X.509 certificates would be encoded as ASN.1 DER.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | encoded form of this certificate |

| Exceptions ||
|----------------------------------------------------|------------------------------------------|
| `javax.security.cert.CertificateEncodingException` | on internal certificate encoding failure |

### getPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPublicKey(): PublicKey!
```

Gets the public key from this certificate.

| Return ||
|--------------------------------------------------------------------------------------------|-----------------|
| [PublicKey](../java/security/PublicKey.md)! | the public key. |

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
| `key` | [PublicKey](../java/security/PublicKey.md)!:the PublicKey used to carry out the verification. |

| Exceptions ||
|--------------------------------------------|--------------------------------------|
| `java.security.NoSuchAlgorithmException` | on unsupported signature algorithms. |
| `java.security.InvalidKeyException` | on incorrect key. |
| `java.security.NoSuchProviderException` | if there's no default provider. |
| --- | --- |
| `java.security.SignatureException` | on signature errors. |
| `javax.security.cert.CertificateException` | on encoding errors. |

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
| `key` | [PublicKey](../java/security/PublicKey.md)!:the PublicKey used to carry out the verification. |
| `sigProvider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the signature provider. |

| Exceptions ||
|--------------------------------------------|--------------------------------------|
| `java.security.NoSuchAlgorithmException` | on unsupported signature algorithms. |
| `java.security.InvalidKeyException` | on incorrect key. |
| `java.security.NoSuchProviderException` | on incorrect provider. |
| --- | --- |
| `java.security.SignatureException` | on signature errors. |
| `javax.security.cert.CertificateException` | on encoding errors. |
