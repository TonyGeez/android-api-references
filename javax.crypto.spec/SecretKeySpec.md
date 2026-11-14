Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecretKeySpec

```
open class SecretKeySpec : KeySpec, SecretKey
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.SecretKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec#) |

This class specifies a secret key in a provider-independent fashion.

It can be used to construct a `SecretKey` from a byte array, without having to go through a (provider-based) `SecretKeyFactory`.

This class is only useful for raw secret keys that can be represented as a byte array and have no key parameters associated with them, e.g., DES or Triple DES keys.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/javax/crypto/SecretKey.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/javax/crypto/SecretKey.html#serialVersionUID:kotlin.Long` The class fingerprint that is set to indicate serialization compatibility since J2SE 1.4. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec#SecretKeySpec(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, algorithm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructs a secret key from the given byte array, using the first `len` bytes of `key`, starting at `offset` inclusive. |
| `https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec#SecretKeySpec(kotlin.ByteArray,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, algorithm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructs a secret key from the given byte array. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Tests for equality between the specified object and this object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec#getAlgorithm()()` Returns the name of the algorithm associated with this secret key. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec#getEncoded()()` Returns the key material of this secret key. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec#getFormat()()` Returns the name of the encoding format for this secret key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec#hashCode()()` Calculates a hash code value for the object. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/javax/security/auth/Destroyable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/javax/security/auth/Destroyable.html#destroy()()` Destroy this `Object`. Sensitive information associated with this `Object` is destroyed or cleared. Subsequent calls to certain methods on this `Object` will result in an `IllegalStateException` being thrown. The default implementation throws `DestroyFailedException`. Android note: Up to and including API 25 this method did not have a default implementation. Implementations of this interface must provide a concrete implementation of this method in order to work on older versions of Android. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/javax/security/auth/Destroyable.html#isDestroyed()()` Determine if this `Object` has been destroyed. The default implementation returns false. Android note: Up to and including API 25 this method did not have a default implementation. Implementations of this interface must provide a concrete implementation of this method in order to work on older versions of Android. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/security/Key.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/security/Key.html#getAlgorithm()()` Returns the standard algorithm name for this key. For example, "DSA" would indicate that this key is a DSA key. See the key related sections (KeyFactory, KeyGenerator, KeyPairGenerator, and SecretKeyFactory) in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html) for information about standard key algorithm names. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/security/Key.html#getEncoded()()` Returns the key in its primary encoding format, or null if this key does not support encoding. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/security/Key.html#getFormat()()` Returns the name of the primary encoding format of this key, or null if this key does not support encoding. The primary encoding format is named in terms of the appropriate ASN.1 data format, if an ASN.1 specification for this key exists. For example, the name of the ASN.1 data format for public keys is *SubjectPublicKeyInfo* , as defined by the X.509 standard; in this case, the returned format is `"X.509"`. Similarly, the name of the ASN.1 data format for private keys is *PrivateKeyInfo* , as defined by the PKCS #8 standard; in this case, the returned format is `"PKCS#8"`. <br /> | ||

## Public constructors

### SecretKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SecretKeySpec(
    key: ByteArray!, 
    offset: Int, 
    len: Int, 
    algorithm: String!)
```

Constructs a secret key from the given byte array, using the first `len` bytes of `key`, starting at `offset` inclusive.

The bytes that constitute the secret key are those between `key[offset]` and `key[offset+len-1]` inclusive.

This constructor does not check if the given bytes indeed specify a secret key of the specified algorithm. For example, if the algorithm is DES, this constructor does not check if `key` is 8 bytes long, and also does not check for weak or semi-weak keys. In order for those checks to be performed, an algorithm-specific key specification class (in this case: `https://developer.android.com/reference/kotlin/javax/crypto/spec/DESKeySpec`) must be used.

| Parameters ||
|---|---|
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the key material of the secret key. The first `len` bytes of the array beginning at `offset` inclusive are copied to protect against subsequent modification. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset in `key` where the key material starts. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the key material. |
| --- | --- |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the secret-key algorithm to be associated with the given key material. See Appendix A in the [Java Cryptography Architecture Reference Guide](https://docs.oracle.com/javase/8/docs/technotes/guides/security/crypto/CryptoSpec.html#AppA) for information about standard algorithm names. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | is thrown if `offset` or `len` index bytes outside the `key`. |
| `java.lang.IllegalArgumentException` | if `algorithm` is null or `key` is null, empty, or too short, i.e. `key.length-offset<len`. |

### SecretKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SecretKeySpec(
    key: ByteArray!, 
    algorithm: String!)
```

Constructs a secret key from the given byte array.

This constructor does not check if the given bytes indeed specify a secret key of the specified algorithm. For example, if the algorithm is DES, this constructor does not check if `key` is 8 bytes long, and also does not check for weak or semi-weak keys. In order for those checks to be performed, an algorithm-specific *key specification* class (in this case: `https://developer.android.com/reference/kotlin/javax/crypto/spec/DESKeySpec`) should be used.

| Parameters ||
|---|---|
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the key material of the secret key. The contents of the array are copied to protect against subsequent modification. |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the secret-key algorithm to be associated with the given key material. See Appendix A in the [Java Cryptography Architecture Reference Guide](https://docs.oracle.com/javase/8/docs/technotes/guides/security/crypto/CryptoSpec.html#AppA) for information about standard algorithm names. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `algorithm` is null or `key` is null or empty. |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Tests for equality between the specified object and this object. Two SecretKeySpec objects are considered equal if they are both SecretKey instances which have the same case-insensitive algorithm name and key encoding.

| Parameters ||
|---|---|
| `obj` | the object to test for equality with this object. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the objects are considered equal, false if `obj` is null or otherwise. |

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAlgorithm(): String!
```

Returns the name of the algorithm associated with this secret key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the secret key algorithm. |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEncoded(): ByteArray!
```

Returns the key material of this secret key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the key material. Returns a new array each time this method is called. |

### getFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFormat(): String!
```

Returns the name of the encoding format for this secret key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the string "RAW". |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Calculates a hash code value for the object. Objects that are equal will also have the same hashcode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
