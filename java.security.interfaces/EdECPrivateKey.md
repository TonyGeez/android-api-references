# EdECPrivateKey

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EdECPrivateKey

```
interface EdECPrivateKey : EdECKey, PrivateKey
```

| [java.security.interfaces.EdECPrivateKey](EdECPrivateKey.md) |

An interface for an elliptic curve private key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). These keys are distinct from the keys represented by `ECPrivateKey`, and they are intended for use with algorithms based on RFC 8032 such as the EdDSA `Signature` algorithm.

An Edwards-Curve private key is a bit string. This interface only supports bit string lengths that are a multiple of 8, and the key is represented using a byte array.

## Summary

| Inherited constants ||
|---|---|
| From class [PrivateKey](../java.security/PrivateKey.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](../java.security/PrivateKey.md) The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Optional](../java.util/Optional.md)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>! | [getBytes](EdECPrivateKey.md))`()` Get a copy of the byte array representing the private key. |

| Inherited functions ||
|---|---|
| From class [Destroyable](../javax.security.auth/Destroyable.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](../javax.security.auth/Destroyable.md))`()` Destroy this `Object`. Sensitive information associated with this `Object` is destroyed or cleared. Subsequent calls to certain methods on this `Object` will result in an `IllegalStateException` being thrown. The default implementation throws `DestroyFailedException`. Android note: Up to and including API 25 this method did not have a default implementation. Implementations of this interface must provide a concrete implementation of this method in order to work on older versions of Android. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDestroyed](../javax.security.auth/Destroyable.md))`()` Determine if this `Object` has been destroyed. The default implementation returns false. Android note: Up to and including API 25 this method did not have a default implementation. Implementations of this interface must provide a concrete implementation of this method in order to work on older versions of Android. <br /> | ||
| From class [Key](../java.security/Key.md) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](../java.security/Key.md))`()` Returns the standard algorithm name for this key. For example, "DSA" would indicate that this key is a DSA key. See the key related sections (KeyFactory, KeyGenerator, KeyPairGenerator, and SecretKeyFactory) in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html) for information about standard key algorithm names. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](../java.security/Key.md))`()` Returns the key in its primary encoding format, or null if this key does not support encoding. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormat](../java.security/Key.md))`()` Returns the name of the primary encoding format of this key, or null if this key does not support encoding. The primary encoding format is named in terms of the appropriate ASN.1 data format, if an ASN.1 specification for this key exists. For example, the name of the ASN.1 data format for public keys is *SubjectPublicKeyInfo* , as defined by the X.509 standard; in this case, the returned format is `"X.509"`. Similarly, the name of the ASN.1 data format for private keys is *PrivateKeyInfo* , as defined by the PKCS #8 standard; in this case, the returned format is `"PKCS#8"`. <br /> | ||
| From class [EdECKey](EdECKey.md) |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [NamedParameterSpec](../java.security.spec/NamedParameterSpec.md)! | [getParams](EdECKey.md))`()` Returns the algorithm parameters associated with the key. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |

## Public methods

### getBytes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBytes(): Optional<ByteArray!>!
```

Get a copy of the byte array representing the private key. This method may return an empty `Optional` if the implementation is not willing to produce the private key value.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Optional](../java.util/Optional.md)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>! | an `Optional` containing the private key byte array. If the key is not available, then an empty `Optional`. |
