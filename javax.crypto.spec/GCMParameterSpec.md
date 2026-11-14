# GCMParameterSpec

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GCMParameterSpec

```
open class GCMParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.GCMParameterSpec](../javax/crypto/spec/GCMParameterSpec.md) |

Specifies the set of parameters required by a using the Galois/Counter Mode (GCM) mode.

Simple block cipher modes (such as CBC) generally require only an initialization vector (such as`IvParameterSpec`), but GCM needs these parameters:

- `IV`: Initialization Vector (IV)
- `tLen`: length (in bits) of authentication tag T

In addition to the parameters described here, other GCM inputs/output (Additional Authenticated Data (AAD), Keys, block ciphers, plain/ciphertext and authentication tags) are handled in the`Cipher`class.

Please see [RFC 5116](http://www.ietf.org/rfc/rfc5116.txt) for more information on the Authenticated Encryption with Associated Data (AEAD) algorithm, and [NIST Special Publication 800-38D](http://csrc.nist.gov/publications/nistpubs/800-38D/SP-800-38D.pdf), "NIST Recommendation for Block Cipher Modes of Operation: Galois/Counter Mode (GCM) and GMAC."

The GCM specification states that`tLen`may only have the values {128, 120, 112, 104, 96}, or {64, 32} for certain applications. Other values can be specified for this class, but not all CSP implementations will support them.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GCMParameterSpec](../javax/crypto/spec/GCMParameterSpec.md))`(`tLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Constructs a GCMParameterSpec using the specified authentication tag bit-length and IV buffer. |
| [GCMParameterSpec](../javax/crypto/spec/GCMParameterSpec.md))`(`tLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a GCMParameterSpec object using the specified authentication tag bit-length and a subset of the specified buffer as the IV. |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getIV](../javax/crypto/spec/GCMParameterSpec.md))`()` Returns the Initialization Vector (IV). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTLen](../javax/crypto/spec/GCMParameterSpec.md))`()` Returns the authentication tag length. |

## Public constructors

### GCMParameterSpec

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GCMParameterSpec(
    tLen: Int, 
    src: ByteArray!)
```

Constructs a GCMParameterSpec using the specified authentication tag bit-length and IV buffer.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the authentication tag length (in bits) |
| `src` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the IV source buffer. The contents of the buffer are copied to protect against subsequent modification. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if`tLen`is negative, or`src`is null. |

### GCMParameterSpec

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GCMParameterSpec(
    tLen: Int, 
    src: ByteArray!, 
    offset: Int, 
    len: Int)
```

Constructs a GCMParameterSpec object using the specified authentication tag bit-length and a subset of the specified buffer as the IV.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the authentication tag length (in bits) |
| `src` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the IV source buffer. The contents of the buffer are copied to protect against subsequent modification. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`src`where the IV starts |
| --- | --- |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of IV bytes |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`tLen`is negative,`src`is null,`len`or`offset`is negative, or the sum of`offset`and`len`is greater than the length of the`src`byte array. |

## Public methods

### getIV

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIV(): ByteArray!
```

Returns the Initialization Vector (IV).

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the IV. Creates a new array each time this method is called. |

### getTLen

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTLen(): Int
```

Returns the authentication tag length.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the authentication tag length (in bits) |
