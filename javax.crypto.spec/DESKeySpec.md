# DESKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DESKeySpec

```
open class DESKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.crypto.spec.DESKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESKeySpec#) |

This class specifies a DES key.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DES_KEY_LEN](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESKeySpec#DES_KEY_LEN:kotlin.Int) The constant which defines the length of a DES key in bytes. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DESKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESKeySpec#DESKeySpec(kotlin.ByteArray))`(`key:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates a DESKeySpec object using the first 8 bytes in`key`as the key material for the DES key. |
| [DESKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESKeySpec#DESKeySpec(kotlin.ByteArray,%20kotlin.Int))`(`key:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a DESKeySpec object using the first 8 bytes in`key`, beginning at`offset`inclusive, as the key material for the DES key. |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getKey](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESKeySpec#getKey())`()` Returns the DES key material. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParityAdjusted](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESKeySpec#isParityAdjusted(kotlin.ByteArray,%20kotlin.Int))`(`key:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if the given DES key material, starting at`offset`inclusive, is parity-adjusted. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWeak](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESKeySpec#isWeak(kotlin.ByteArray,%20kotlin.Int))`(`key:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if the given DES key material is weak or semi-weak. |

## Constants

### DES_KEY_LEN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DES_KEY_LEN: Int
```

The constant which defines the length of a DES key in bytes. 

 Value: 8

## Public constructors

### DESKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DESKeySpec(key: ByteArray!)
```

Creates a DESKeySpec object using the first 8 bytes in`key`as the key material for the DES key.

The bytes that constitute the DES key are those between`key[0]`and`key[7]`inclusive.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer with the DES key material. The first 8 bytes of the buffer are copied to protect against subsequent modification. |

| Exceptions ||
|-------------------------------------|----------------------------------------------------|
| `java.lang.NullPointerException` | if the given key material is`null` |
| `java.security.InvalidKeyException` | if the given key material is shorter than 8 bytes. |

### DESKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DESKeySpec(
    key: ByteArray!, 
    offset: Int)
```

Creates a DESKeySpec object using the first 8 bytes in`key`, beginning at`offset`inclusive, as the key material for the DES key.

The bytes that constitute the DES key are those between`key[offset]`and`key[offset+7]`inclusive.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer with the DES key material. The first 8 bytes of the buffer beginning at`offset`inclusive are copied to protect against subsequent modification. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`key`, where the DES key material starts. |

| Exceptions ||
|-------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the given key material is`null` |
| `java.security.InvalidKeyException` | if the given key material, starting at`offset`inclusive, is shorter than 8 bytes. |

## Public methods

### getKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKey(): ByteArray!
```

Returns the DES key material.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the DES key material. Returns a new array each time this method is called. |

### isParityAdjusted

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isParityAdjusted(
    key: ByteArray!, 
    offset: Int
): Boolean
```

Checks if the given DES key material, starting at`offset`inclusive, is parity-adjusted.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer with the DES key material. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`key`, where the DES key material starts. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the given DES key material is parity-adjusted, false otherwise. |

| Exceptions ||
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key material is`null`, or starting at`offset`inclusive, is shorter than 8 bytes. |

### isWeak

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isWeak(
    key: ByteArray!, 
    offset: Int
): Boolean
```

Checks if the given DES key material is weak or semi-weak.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer with the DES key material. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`key`, where the DES key material starts. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the given DES key material is weak or semi-weak, false otherwise. |

| Exceptions ||
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key material is`null`, or starting at`offset`inclusive, is shorter than 8 bytes. |
