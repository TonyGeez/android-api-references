# DESedeKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DESedeKeySpec

```
open class DESedeKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.crypto.spec.DESedeKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESedeKeySpec#) |

This class specifies a DES-EDE ("triple-DES") key.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DES_EDE_KEY_LEN](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESedeKeySpec#DES_EDE_KEY_LEN:kotlin.Int) The constant which defines the length of a DESede key in bytes. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DESedeKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESedeKeySpec#DESedeKeySpec(kotlin.ByteArray))`(`key:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates a DESedeKeySpec object using the first 24 bytes in`key`as the key material for the DES-EDE key. |
| [DESedeKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESedeKeySpec#DESedeKeySpec(kotlin.ByteArray,%20kotlin.Int))`(`key:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a DESedeKeySpec object using the first 24 bytes in`key`, beginning at`offset`inclusive, as the key material for the DES-EDE key. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getKey](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESedeKeySpec#getKey())`()` Returns the DES-EDE key. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParityAdjusted](https://developer.android.com/reference/kotlin/javax/crypto/spec/DESedeKeySpec#isParityAdjusted(kotlin.ByteArray,%20kotlin.Int))`(`key:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if the given DES-EDE key, starting at`offset`inclusive, is parity-adjusted. |

## Constants

### DES_EDE_KEY_LEN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DES_EDE_KEY_LEN: Int
```

The constant which defines the length of a DESede key in bytes. 

 Value: 24

## Public constructors

### DESedeKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DESedeKeySpec(key: ByteArray!)
```

Creates a DESedeKeySpec object using the first 24 bytes in`key`as the key material for the DES-EDE key.

The bytes that constitute the DES-EDE key are those between`key[0]`and`key[23]`inclusive

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer with the DES-EDE key material. The first 24 bytes of the buffer are copied to protect against subsequent modification. |

| Exceptions ||
|-------------------------------------|-----------------------------------------------------|
| `java.lang.NullPointerException` | if`key`is null. |
| `java.security.InvalidKeyException` | if the given key material is shorter than 24 bytes. |

### DESedeKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DESedeKeySpec(
    key: ByteArray!, 
    offset: Int)
```

Creates a DESedeKeySpec object using the first 24 bytes in`key`, beginning at`offset`inclusive, as the key material for the DES-EDE key.

The bytes that constitute the DES-EDE key are those between`key[offset]`and`key[offset+23]`inclusive.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer with the DES-EDE key material. The first 24 bytes of the buffer beginning at`offset`inclusive are copied to protect against subsequent modification. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`key`, where the DES-EDE key material starts. |

| Exceptions ||
|-------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`key`is null. |
| `java.security.InvalidKeyException` | if the given key material, starting at`offset`inclusive, is shorter than 24 bytes |

## Public methods

### getKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKey(): ByteArray!
```

Returns the DES-EDE key.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the DES-EDE key. Returns a new array each time this method is called. |

### isParityAdjusted

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isParityAdjusted(
    key: ByteArray!, 
    offset: Int
): Boolean
```

Checks if the given DES-EDE key, starting at`offset`inclusive, is parity-adjusted.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array which holds the key value |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into the byte array |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the given DES-EDE key is parity-adjusted, false otherwise |

| Exceptions ||
|-------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`key`is null. |
| `java.security.InvalidKeyException` | if the given key material, starting at`offset`inclusive, is shorter than 24 bytes |
