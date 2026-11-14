Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EncodedKeySpec

```
abstract class EncodedKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.EncodedKeySpec](EncodedKeySpec.md) |

| Known Direct Subclasses [PKCS8EncodedKeySpec](PKCS8EncodedKeySpec.md), [X509EncodedKeySpec](X509EncodedKeySpec.md), [XdhKeySpec](../android.crypto.hpke/XdhKeySpec.md) |---|---| | [PKCS8EncodedKeySpec](PKCS8EncodedKeySpec.md) | This class represents the ASN. | | [X509EncodedKeySpec](X509EncodedKeySpec.md) | This class represents the ASN. | | [XdhKeySpec](../android.crypto.hpke/XdhKeySpec.md) | External Diffie--Hellman (XDH) key spec holding either a public or private key. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class represents a public or private key in encoded format.

## Summary

| Public constructors ||
|---|---|
| EncodedKeySpec Creates a new `EncodedKeySpec` with the given encoded key. |

| Protected constructors ||
|---|---|
| EncodedKeySpec Creates a new `EncodedKeySpec` with the given encoded key. |

| Public methods ||
|---|---|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getAlgorithm Returns the name of the algorithm of the encoded key. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | getEncoded Returns the encoded key. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getFormat Returns the name of the encoding format associated with this key specification. |
| --- | --- |

## Public constructors

### EncodedKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
EncodedKeySpec(encodedKey: ByteArray!)
```

Creates a new `EncodedKeySpec` with the given encoded key.

| Parameters ||
|---|---|
| `encodedKey` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the encoded key. The contents of the array are copied to protect against subsequent modification. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `encodedKey` is null. |

## Protected constructors

### EncodedKeySpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected EncodedKeySpec(
    encodedKey: ByteArray!, 
    algorithm: String!)
```

Creates a new `EncodedKeySpec` with the given encoded key. This constructor is useful when subsequent callers of the `EncodedKeySpec` object might not know the algorithm of the key.

| Parameters ||
|---|---|
| `encodedKey` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the encoded key. The contents of the array are copied to protect against subsequent modification. |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the algorithm name of the encoded key See the KeyFactory section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keyfactory-algorithms) for information about standard algorithm names. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `algorithm` is the empty string `""` |
| `java.lang.NullPointerException` | if `encodedKey` or `algorithm` is null. |

## Public methods

### getAlgorithm

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAlgorithm(): String!
```

Returns the name of the algorithm of the encoded key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the name of the algorithm, or null if not specified |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEncoded(): ByteArray!
```

Returns the encoded key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the encoded key. Returns a new array each time this method is called. |

### getFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFormat(): String!
```

Returns the name of the encoding format associated with this key specification.

If the opaque representation of a key (see `https://developer.android.com/reference/kotlin/java/security/Key.html#`) can be transformed (see `https://developer.android.com/reference/kotlin/java/security/KeyFactory.html#`) into this key specification (or a subclass of it), `getFormat` called on the opaque key returns the same value as the `getFormat` method of this key specification.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a string representation of the encoding format. |
