# Key

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Key

```
interface Key : Serializable
```

| [java.security.Key](https://developer.android.com/reference/kotlin/java/security/Key#) |

| Known Direct Subclasses [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey), [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey), [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey.html#) |------------------------------------------------------------------------------------------|---------------------------| | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey) | A private key. | | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey) | A public key. | | [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey.html#) | A secret (symmetric) key. | |

| Known Indirect Subclasses [DHPrivateKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPrivateKey.html#), [DHPublicKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPublicKey.html#), [DSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPrivateKey), [DSAPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPublicKey), [ECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPrivateKey), [ECPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPublicKey), [EdECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/EdECPrivateKey), [EdECPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/EdECPublicKey), [PBEKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/PBEKey.html#), [RSAMultiPrimePrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey), [RSAPrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateCrtKey), [RSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateKey), and 4 others. |----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DHPrivateKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPrivateKey.html#) | The interface to a Diffie-Hellman private key. | | [DHPublicKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPublicKey.html#) | The interface to a Diffie-Hellman public key. | | [DSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPrivateKey) | The standard interface to a DSA private key. | | [DSAPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPublicKey) | The interface to a DSA public key. | | [ECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPrivateKey) | The interface to an elliptic curve (EC) private key. | | [ECPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPublicKey) | The interface to an elliptic curve (EC) public key. | | [EdECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/EdECPrivateKey) | An interface for an elliptic curve private key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). | | [EdECPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/EdECPublicKey) | An interface for an elliptic curve public key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). | | [PBEKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/PBEKey.html#) | The interface to a PBE key. | | [RSAMultiPrimePrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey) | The interface to an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateCrtKey) | The interface to an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateKey) | The interface to an RSA private key. | | [RSAPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPublicKey) | The interface to an RSA public key. | | [SecretKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec.html#) | This class specifies a secret key in a provider-independent fashion. | | [XECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/XECPrivateKey) | An interface for an elliptic curve private key as defined by RFC 7748. | | [XECPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/XECPublicKey) | An interface for an elliptic curve public key as defined by RFC 7748. | |

The Key interface is the top-level interface for all keys. It defines the functionality shared by all key objects. All keys have three characteristics:

- An AlgorithmThis is the key algorithm for that key. The key algorithm is usually an encryption or asymmetric operation algorithm (such as DSA or RSA), which will work with those algorithms and with related algorithms (such as MD5 with RSA, SHA-1 with RSA, Raw DSA, etc.) The name of the algorithm of a key is obtained using the [getAlgorithm](https://developer.android.com/reference/kotlin/java/security/Key#getAlgorithm())method.

- An Encoded FormThis is an external encoded form for the key used when a standard representation of the key is needed outside the Java Virtual Machine, as when transmitting the key to some other party. The key is encoded according to a standard format (such as X.509`SubjectPublicKeyInfo`or PKCS#8), and is returned using the [getEncoded](https://developer.android.com/reference/kotlin/java/security/Key#getEncoded())method. Note: The syntax of the ASN.1 type`SubjectPublicKeyInfo`is defined as follows:

  ```kotlin
  SubjectPublicKeyInfo ::= SEQUENCE {
      algorithm AlgorithmIdentifier,
      subjectPublicKey BIT STRING }
   
    AlgorithmIdentifier ::= SEQUENCE {
      algorithm OBJECT IDENTIFIER,
      parameters ANY DEFINED BY algorithm OPTIONAL }
    
  ```
 For more information, see [RFC 5280: Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://tools.ietf.org/html/rfc5280).
- A FormatThis is the name of the format of the encoded key. It is returned by the [getFormat](https://developer.android.com/reference/kotlin/java/security/Key#getFormat())method.

Keys are generally obtained through key generators, certificates, key stores or other classes used to manage keys. Keys may also be obtained from key specifications (transparent representations of the underlying key material) through the use of a key factory (see [KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory)).

<br />

A Key should use KeyRep as its serialized representation. Note that a serialized Key may contain sensitive information which should not be exposed in untrusted environments. See the [Security Appendix](https://docs.oracle.com/en/java/javase/17/docs/specs/serialization/security.html) of the Serialization Specification for more information.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](https://developer.android.com/reference/kotlin/java/security/Key#serialVersionUID:kotlin.Long) The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/java/security/Key#getAlgorithm())`()` Returns the standard algorithm name for this key. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](https://developer.android.com/reference/kotlin/java/security/Key#getEncoded())`()` Returns the key in its primary encoding format, or null if this key does not support encoding. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormat](https://developer.android.com/reference/kotlin/java/security/Key#getFormat())`()` Returns the name of the primary encoding format of this key, or null if this key does not support encoding. |

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
