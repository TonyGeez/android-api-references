# IvParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IvParameterSpec

```
open class IvParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.IvParameterSpec](../javax/crypto/spec/IvParameterSpec.md) |

This class specifies an*initialization vector*(IV). Examples which use IVs are ciphers in feedback mode, e.g., DES in CBC mode and RSA ciphers with OAEP encoding operation.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IvParameterSpec](../javax/crypto/spec/IvParameterSpec.md))`(`iv:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates an IvParameterSpec object using the bytes in`iv`as the IV. |
| [IvParameterSpec](../javax/crypto/spec/IvParameterSpec.md))`(`iv:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an IvParameterSpec object using the first`len`bytes in`iv`, beginning at`offset`inclusive, as the IV. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getIV](../javax/crypto/spec/IvParameterSpec.md))`()` Returns the initialization vector (IV). |

## Public constructors

### IvParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IvParameterSpec(iv: ByteArray!)
```

Creates an IvParameterSpec object using the bytes in`iv`as the IV.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iv` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer with the IV. The contents of the buffer are copied to protect against subsequent modification. |

| Exceptions ||
|----------------------------------|----------------|
| `java.lang.NullPointerException` | if`iv`is`null` |

### IvParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IvParameterSpec(
    iv: ByteArray!, 
    offset: Int, 
    len: Int)
```

Creates an IvParameterSpec object using the first`len`bytes in`iv`, beginning at`offset`inclusive, as the IV.

The bytes that constitute the IV are those between`iv[offset]`and`iv[offset+len-1]`inclusive.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iv` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer with the IV. The first`len`bytes of the buffer beginning at`offset`inclusive are copied to protect against subsequent modification. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`iv`where the IV starts. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of IV bytes. |
| --- | --- |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`iv`is`null`or`(iv.length - offset < len)` |
| `java.lang.ArrayIndexOutOfBoundsException` | is thrown if`offset`or`len`index bytes outside the`iv`. |

## Public methods

### getIV

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIV(): ByteArray!
```

Returns the initialization vector (IV).

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the initialization vector (IV). Returns a new array each time this method is called. |
