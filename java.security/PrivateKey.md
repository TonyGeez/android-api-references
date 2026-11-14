# PrivateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrivateKey

```
interface PrivateKey : Destroyable, Key
```

| [java.security.PrivateKey](../java/security/PrivateKey.md) |

| Known Direct Subclasses [DHPrivateKey](../javax/crypto/interfaces/DHPrivateKey.md), [DSAPrivateKey](../java/security/interfaces/DSAPrivateKey.md), [ECPrivateKey](../java/security/interfaces/ECPrivateKey.md), [EdECPrivateKey](../java/security/interfaces/EdECPrivateKey.md), [RSAPrivateKey](../java/security/interfaces/RSAPrivateKey.md), [XECPrivateKey](../java/security/interfaces/XECPrivateKey.md) |-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DHPrivateKey](../javax/crypto/interfaces/DHPrivateKey.md) | The interface to a Diffie-Hellman private key. | | [DSAPrivateKey](../java/security/interfaces/DSAPrivateKey.md) | The standard interface to a DSA private key. | | [ECPrivateKey](../java/security/interfaces/ECPrivateKey.md) | The interface to an elliptic curve (EC) private key. | | [EdECPrivateKey](../java/security/interfaces/EdECPrivateKey.md) | An interface for an elliptic curve private key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). | | [RSAPrivateKey](../java/security/interfaces/RSAPrivateKey.md) | The interface to an RSA private key. | | [XECPrivateKey](../java/security/interfaces/XECPrivateKey.md) | An interface for an elliptic curve private key as defined by RFC 7748. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [RSAMultiPrimePrivateCrtKey](../java/security/interfaces/RSAMultiPrimePrivateCrtKey.md), [RSAPrivateCrtKey](../java/security/interfaces/RSAPrivateCrtKey.md) |----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RSAMultiPrimePrivateCrtKey](../java/security/interfaces/RSAMultiPrimePrivateCrtKey.md) | The interface to an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateCrtKey](../java/security/interfaces/RSAPrivateCrtKey.md) | The interface to an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A private key. The purpose of this interface is to group (and provide type safety for) all private key interfaces.

Note: The specialized private key interfaces extend this interface. See, for example, the`DSAPrivateKey`interface in [java.security.interfaces](../java/security/interfaces/_package.md).

Implementations should override the default`destroy`and`isDestroyed`methods from the [javax.security.auth.Destroyable](../javax/security/auth/Destroyable.md) interface to enable sensitive key information to be destroyed, cleared, or in the case where such information is immutable, unreferenced. Finally, since`PrivateKey`is`Serializable`, implementations should also override [java.io.ObjectOutputStream#writeObject(java.lang.Object)](../java/io/ObjectOutputStream.md))to prevent keys that have been destroyed from being serialized.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](../java/security/PrivateKey.md) The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. |

| Inherited functions ||
|---|---|
| From class [Destroyable](../javax/security/auth/Destroyable.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](../javax/security/auth/Destroyable.md))`()` <br /> Destroy this`Object`. Sensitive information associated with this`Object`is destroyed or cleared. Subsequent calls to certain methods on this`Object`will result in an`IllegalStateException`being thrown. The default implementation throws`DestroyFailedException`. Android note: Up to and including API 25 this method did not have a default implementation. Implementations of this interface must provide a concrete implementation of this method in order to work on older versions of Android. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDestroyed](../javax/security/auth/Destroyable.md))`()` <br /> Determine if this`Object`has been destroyed. The default implementation returns false. Android note: Up to and including API 25 this method did not have a default implementation. Implementations of this interface must provide a concrete implementation of this method in order to work on older versions of Android. <br /> | ||
| From class [Key](../java/security/Key.md) |------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](../java/security/Key.md))`()` <br /> Returns the standard algorithm name for this key. For example, "DSA" would indicate that this key is a DSA key. See the key related sections (KeyFactory, KeyGenerator, KeyPairGenerator, and SecretKeyFactory) in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html) for information about standard key algorithm names. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](../java/security/Key.md))`()` <br /> Returns the key in its primary encoding format, or null if this key does not support encoding. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormat](../java/security/Key.md))`()` <br /> Returns the name of the primary encoding format of this key, or null if this key does not support encoding. The primary encoding format is named in terms of the appropriate ASN.1 data format, if an ASN.1 specification for this key exists. For example, the name of the ASN.1 data format for public keys is*SubjectPublicKeyInfo* , as defined by the X.509 standard; in this case, the returned format is`"X.509"`. Similarly, the name of the ASN.1 data format for private keys is*PrivateKeyInfo* , as defined by the PKCS #8 standard; in this case, the returned format is`"PKCS#8"`. <br /> | ||

## Constants

### serialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val serialVersionUID: Long
```

**Deprecated:** *A`serialVersionUID`field in an interface is ineffectual. Do not use; no replacement.*

The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. 

 Value: 6034044314589513430L
