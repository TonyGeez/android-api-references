# EdECPublicKey

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EdECPublicKey

```
interface EdECPublicKey : EdECKey, PublicKey
```

| [java.security.interfaces.EdECPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/EdECPublicKey#) |

An interface for an elliptic curve public key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). These keys are distinct from the keys represented by `ECPublicKey`, and they are intended for use with algorithms based on RFC 8032 such as the EdDSA `Signature` algorithm.

An Edwards-Curve public key is a point on the curve, which is represented using an EdECPoint.

## Summary

| Inherited constants ||
|---|---|
| From class [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#serialVersionUID:kotlin.Long) The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [EdECPoint](https://developer.android.com/reference/kotlin/java/security/spec/EdECPoint.html#)! | [getPoint](https://developer.android.com/reference/kotlin/java/security/interfaces/EdECPublicKey#getPoint())`()` Get the point representing the public key. |

| Inherited functions ||
|---|---|
| From class [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/java/security/Key.html#getAlgorithm())`()` Returns the standard algorithm name for this key. For example, "DSA" would indicate that this key is a DSA key. See the key related sections (KeyFactory, KeyGenerator, KeyPairGenerator, and SecretKeyFactory) in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html) for information about standard key algorithm names. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](https://developer.android.com/reference/kotlin/java/security/Key.html#getEncoded())`()` Returns the key in its primary encoding format, or null if this key does not support encoding. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormat](https://developer.android.com/reference/kotlin/java/security/Key.html#getFormat())`()` Returns the name of the primary encoding format of this key, or null if this key does not support encoding. The primary encoding format is named in terms of the appropriate ASN.1 data format, if an ASN.1 specification for this key exists. For example, the name of the ASN.1 data format for public keys is *SubjectPublicKeyInfo* , as defined by the X.509 standard; in this case, the returned format is `"X.509"`. Similarly, the name of the ASN.1 data format for private keys is *PrivateKeyInfo* , as defined by the PKCS #8 standard; in this case, the returned format is `"PKCS#8"`. <br /> | ||
| From class [EdECKey](https://developer.android.com/reference/kotlin/java/security/interfaces/EdECKey) |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#)! | [getParams](https://developer.android.com/reference/kotlin/java/security/interfaces/EdECKey#getParams())`()` Returns the algorithm parameters associated with the key. <br /> | ||

## Public methods

### getPoint

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPoint(): EdECPoint!
```

Get the point representing the public key.

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------|
| [EdECPoint](https://developer.android.com/reference/kotlin/java/security/spec/EdECPoint.html#)! | the `EdECPoint` representing the public key. |
