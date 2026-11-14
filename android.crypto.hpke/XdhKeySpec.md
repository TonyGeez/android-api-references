# XdhKeySpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XdhKeySpec

Kotlin| [Java](XdhKeySpec.md) 
| --- | --- |

```
class XdhKeySpec : EncodedKeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.spec.EncodedKeySpec](../java.security.spec/EncodedKeySpec.md) ||
| | ↳ | [android.crypto.hpke.XdhKeySpec](XdhKeySpec.md) |

External Diffie--Hellman (XDH) key spec holding either a public or private key.

Subclasses`EncodedKeySpec`using the non-Standard "raw" format. The XdhKeyFactory class utilises this in order to create XDH keys from raw bytes and to return them as an XdhKeySpec allowing the raw key material to be extracted from an XDH key.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XdhKeySpec](XdhKeySpec.md))`(`encoded:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Creates an instance of [XdhKeySpec](XdhKeySpec.md) by passing a public or private key in its raw format. |

| Public methods ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](XdhKeySpec.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getFormat](XdhKeySpec.md))`()` Returns the name of the encoding format associated with this key specification. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getKey](XdhKeySpec.md))`()` Returns the public or private key in its raw format. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](XdhKeySpec.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [EncodedKeySpec](../java.security.spec/EncodedKeySpec.md) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](../java.security.spec/EncodedKeySpec.md))`()` <br /> Returns the name of the algorithm of the encoded key. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](../java.security.spec/EncodedKeySpec.md))`()` <br /> Returns the encoded key. <br /> | ||

## Public constructors

### XdhKeySpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XdhKeySpec(encoded: ByteArray)
```

Creates an instance of [XdhKeySpec](XdhKeySpec.md) by passing a public or private key in its raw format.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------|
| `encoded` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):This value cannot be`null`. |

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getFormat

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormat(): String
```

Returns the name of the encoding format associated with this key specification.

If the opaque representation of a key (see [Key](../java.security/Key.md)) can be transformed (see [KeyFactory](../java.security/KeyFactory.md)) into this key specification (or a subclass of it),`getFormat`called on the opaque key returns the same value as the`getFormat`method of this key specification.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getKey

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKey(): ByteArray
```

Returns the public or private key in its raw format.

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | key in its raw format. This value cannot be`null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
