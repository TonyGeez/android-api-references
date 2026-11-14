# Key

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Key

```
interface Key : Serializable
```

| [java.security.Key](../java/security/Key.md) |

| Known Direct Subclasses [PrivateKey](../java/security/PrivateKey.md), [PublicKey](../java/security/PublicKey.md), [SecretKey](../javax/crypto/SecretKey.md) |------------------------------------------------------------------------------------------|---------------------------| | [PrivateKey](../java/security/PrivateKey.md) | A private key. | | [PublicKey](../java/security/PublicKey.md) | A public key. | | [SecretKey](../javax/crypto/SecretKey.md) | A secret (symmetric) key. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DHPrivateKey](../javax/crypto/interfaces/DHPrivateKey.md), [DHPublicKey](../javax/crypto/interfaces/DHPublicKey.md), [DSAPrivateKey](../java/security/interfaces/DSAPrivateKey.md), [DSAPublicKey](../java/security/interfaces/DSAPublicKey.md), [ECPrivateKey](../java/security/interfaces/ECPrivateKey.md), [ECPublicKey](../java/security/interfaces/ECPublicKey.md), [EdECPrivateKey](../java/security/interfaces/EdECPrivateKey.md), [EdECPublicKey](../java/security/interfaces/EdECPublicKey.md), [PBEKey](../javax/crypto/interfaces/PBEKey.md), [RSAMultiPrimePrivateCrtKey](../java/security/interfaces/RSAMultiPrimePrivateCrtKey.md), [RSAPrivateCrtKey](../java/security/interfaces/RSAPrivateCrtKey.md), [RSAPrivateKey](../java/security/interfaces/RSAPrivateKey.md), and 4 others. |----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DHPrivateKey](../javax/crypto/interfaces/DHPrivateKey.md) | The interface to a Diffie-Hellman private key. | | [DHPublicKey](../javax/crypto/interfaces/DHPublicKey.md) | The interface to a Diffie-Hellman public key. | | [DSAPrivateKey](../java/security/interfaces/DSAPrivateKey.md) | The standard interface to a DSA private key. | | [DSAPublicKey](../java/security/interfaces/DSAPublicKey.md) | The interface to a DSA public key. | | [ECPrivateKey](../java/security/interfaces/ECPrivateKey.md) | The interface to an elliptic curve (EC) private key. | | [ECPublicKey](../java/security/interfaces/ECPublicKey.md) | The interface to an elliptic curve (EC) public key. | | [EdECPrivateKey](../java/security/interfaces/EdECPrivateKey.md) | An interface for an elliptic curve private key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). | | [EdECPublicKey](../java/security/interfaces/EdECPublicKey.md) | An interface for an elliptic curve public key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). | | [PBEKey](../javax/crypto/interfaces/PBEKey.md) | The interface to a PBE key. | | [RSAMultiPrimePrivateCrtKey](../java/security/interfaces/RSAMultiPrimePrivateCrtKey.md) | The interface to an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateCrtKey](../java/security/interfaces/RSAPrivateCrtKey.md) | The interface to an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateKey](../java/security/interfaces/RSAPrivateKey.md) | The interface to an RSA private key. | | [RSAPublicKey](../java/security/interfaces/RSAPublicKey.md) | The interface to an RSA public key. | | [SecretKeySpec](../javax/crypto/spec/SecretKeySpec.md) | This class specifies a secret key in a provider-independent fashion. | | [XECPrivateKey](../java/security/interfaces/XECPrivateKey.md) | An interface for an elliptic curve private key as defined by RFC 7748. | | [XECPublicKey](../java/security/interfaces/XECPublicKey.md) | An interface for an elliptic curve public key as defined by RFC 7748. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The Key interface is the top-level interface for all keys. It defines the functionality shared by all key objects. All keys have three characteristics:

- An AlgorithmThis is the key algorithm for that key. The key algorithm is usually an encryption or asymmetric operation algorithm (such as DSA or RSA), which will work with those algorithms and with related algorithms (such as MD5 with RSA, SHA-1 with RSA, Raw DSA, etc.) The name of the algorithm of a key is obtained using the [getAlgorithm](../java/security/Key.md))method.

- An Encoded FormThis is an external encoded form for the key used when a standard representation of the key is needed outside the Java Virtual Machine, as when transmitting the key to some other party. The key is encoded according to a standard format (such as X.509`SubjectPublicKeyInfo`or PKCS#8), and is returned using the [getEncoded](../java/security/Key.md))method. Note: The syntax of the ASN.1 type`SubjectPublicKeyInfo`is defined as follows:

  ```kotlin
  SubjectPublicKeyInfo ::= SEQUENCE {
      algorithm AlgorithmIdentifier,
      subjectPublicKey BIT STRING }
   
    AlgorithmIdentifier ::= SEQUENCE {
      algorithm OBJECT IDENTIFIER,
      parameters ANY DEFINED BY algorithm OPTIONAL }
    
  ```
 For more information, see [RFC 5280: Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://tools.ietf.org/html/rfc5280).
- A FormatThis is the name of the format of the encoded key. It is returned by the [getFormat](../java/security/Key.md))method.

Keys are generally obtained through key generators, certificates, key stores or other classes used to manage keys. Keys may also be obtained from key specifications (transparent representations of the underlying key material) through the use of a key factory (see [KeyFactory](../java/security/KeyFactory.md)).

<br />

A Key should use KeyRep as its serialized representation. Note that a serialized Key may contain sensitive information which should not be exposed in untrusted environments. See the [Security Appendix](https://docs.oracle.com/en/java/javase/17/docs/specs/serialization/security.html) of the Serialization Specification for more information.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](../java/security/Key.md) The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](../java/security/Key.md))`()` Returns the standard algorithm name for this key. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](../java/security/Key.md))`()` Returns the key in its primary encoding format, or null if this key does not support encoding. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormat](../java/security/Key.md))`()` Returns the name of the primary encoding format of this key, or null if this key does not support encoding. |
| --- | --- |

## Constants

### serialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val serialVersionUID: Long
```

**Deprecated:** *A`serialVersionUID`field in an interface is ineffectual. Do not use; no replacement.*

The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. 

 Value: 6603384152749567654L

## Public methods

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAlgorithm(): String!
```

Returns the standard algorithm name for this key. For example, "DSA" would indicate that this key is a DSA key. See the key related sections (KeyFactory, KeyGenerator, KeyPairGenerator, and SecretKeyFactory) in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html) for information about standard key algorithm names.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the algorithm associated with this key. |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncoded(): ByteArray!
```

Returns the key in its primary encoding format, or null if this key does not support encoding.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the encoded key, or null if the key does not support encoding. |

### getFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFormat(): String!
```

Returns the name of the primary encoding format of this key, or null if this key does not support encoding. The primary encoding format is named in terms of the appropriate ASN.1 data format, if an ASN.1 specification for this key exists. For example, the name of the ASN.1 data format for public keys is*SubjectPublicKeyInfo* , as defined by the X.509 standard; in this case, the returned format is`"X.509"`. Similarly, the name of the ASN.1 data format for private keys is*PrivateKeyInfo* , as defined by the PKCS #8 standard; in this case, the returned format is`"PKCS#8"`.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the primary encoding format of the key. |
