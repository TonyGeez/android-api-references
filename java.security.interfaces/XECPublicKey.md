# XECPublicKey

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XECPublicKey

```
interface XECPublicKey : PublicKey, XECKey
```

| [java.security.interfaces.XECPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/XECPublicKey#) |

An interface for an elliptic curve public key as defined by RFC 7748. These keys are distinct from the keys represented by`ECPublicKey`, and they are intended for use with algorithms based on RFC 7748 such as the XDH`KeyAgreement`algorithm. An XEC public key is a particular point on the curve, which is represented using only its u-coordinate as described in RFC 7748. A u-coordinate is an element of the field of integers modulo some value that is determined by the algorithm parameters. This field element is represented by a BigInteger which may hold any value. That is, the BigInteger is not restricted to the range of canonical field elements.

## Summary

| Inherited constants ||
|---|---|
| From class [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#serialVersionUID:kotlin.Long) <br /> The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getU](https://developer.android.com/reference/kotlin/java/security/interfaces/XECPublicKey#getU())`()` Get the u coordinate of the point. |

| Inherited functions ||
|---|---|
| From class [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#) |------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/java/security/Key.html#getAlgorithm())`()` <br /> Returns the standard algorithm name for this key. For example, "DSA" would indicate that this key is a DSA key. See the key related sections (KeyFactory, KeyGenerator, KeyPairGenerator, and SecretKeyFactory) in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html) for information about standard key algorithm names. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](https://developer.android.com/reference/kotlin/java/security/Key.html#getEncoded())`()` <br /> Returns the key in its primary encoding format, or null if this key does not support encoding. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormat](https://developer.android.com/reference/kotlin/java/security/Key.html#getFormat())`()` <br /> Returns the name of the primary encoding format of this key, or null if this key does not support encoding. The primary encoding format is named in terms of the appropriate ASN.1 data format, if an ASN.1 specification for this key exists. For example, the name of the ASN.1 data format for public keys is*SubjectPublicKeyInfo* , as defined by the X.509 standard; in this case, the returned format is`"X.509"`. Similarly, the name of the ASN.1 data format for private keys is*PrivateKeyInfo* , as defined by the PKCS #8 standard; in this case, the returned format is`"PKCS#8"`. <br /> | ||
| From class [XECKey](https://developer.android.com/reference/kotlin/java/security/interfaces/XECKey) |---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)! | [getParams](https://developer.android.com/reference/kotlin/java/security/interfaces/XECKey#getParams())`()` <br /> Returns the algorithm parameters associated with the key. <br /> | ||

## Public methods

### getU

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getU(): BigInteger!
```

Get the u coordinate of the point.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the u-coordinate, represented using a BigInteger which may hold any value |
