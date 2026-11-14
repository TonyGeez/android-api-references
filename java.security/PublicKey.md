# PublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PublicKey

```
interface PublicKey : Key
```

| [java.security.PublicKey](../java/security/PublicKey.md) |

| Known Direct Subclasses [DHPublicKey](../javax/crypto/interfaces/DHPublicKey.md), [DSAPublicKey](../java/security/interfaces/DSAPublicKey.md), [ECPublicKey](../java/security/interfaces/ECPublicKey.md), [EdECPublicKey](../java/security/interfaces/EdECPublicKey.md), [RSAPublicKey](../java/security/interfaces/RSAPublicKey.md), [XECPublicKey](../java/security/interfaces/XECPublicKey.md) |---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DHPublicKey](../javax/crypto/interfaces/DHPublicKey.md) | The interface to a Diffie-Hellman public key. | | [DSAPublicKey](../java/security/interfaces/DSAPublicKey.md) | The interface to a DSA public key. | | [ECPublicKey](../java/security/interfaces/ECPublicKey.md) | The interface to an elliptic curve (EC) public key. | | [EdECPublicKey](../java/security/interfaces/EdECPublicKey.md) | An interface for an elliptic curve public key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). | | [RSAPublicKey](../java/security/interfaces/RSAPublicKey.md) | The interface to an RSA public key. | | [XECPublicKey](../java/security/interfaces/XECPublicKey.md) | An interface for an elliptic curve public key as defined by RFC 7748. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A public key. This interface contains no methods or constants. It merely serves to group (and provide type safety for) all public key interfaces. Note: The specialized public key interfaces extend this interface. See, for example, the DSAPublicKey interface in `java.security.interfaces`.

## Summary

| Constants ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](../java/security/PublicKey.md) The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. |

| Inherited functions ||
|---|---|
| From class [Key](../java/security/Key.md) |------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](../java/security/Key.md))`()` Returns the standard algorithm name for this key. For example, "DSA" would indicate that this key is a DSA key. See the key related sections (KeyFactory, KeyGenerator, KeyPairGenerator, and SecretKeyFactory) in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html) for information about standard key algorithm names. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](../java/security/Key.md))`()` Returns the key in its primary encoding format, or null if this key does not support encoding. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormat](../java/security/Key.md))`()` Returns the name of the primary encoding format of this key, or null if this key does not support encoding. The primary encoding format is named in terms of the appropriate ASN.1 data format, if an ASN.1 specification for this key exists. For example, the name of the ASN.1 data format for public keys is *SubjectPublicKeyInfo* , as defined by the X.509 standard; in this case, the returned format is `"X.509"`. Similarly, the name of the ASN.1 data format for private keys is *PrivateKeyInfo* , as defined by the PKCS #8 standard; in this case, the returned format is `"PKCS#8"`. <br /> | ||

## Constants

### serialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val serialVersionUID: Long
```

**Deprecated:** *A `serialVersionUID` field in an interface is ineffectual. Do not use; no replacement.*

The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. 

 Value: 7187392471159151072L
