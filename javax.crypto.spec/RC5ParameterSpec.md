# RC5ParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RC5ParameterSpec

```
open class RC5ParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.RC5ParameterSpec](../javax/crypto/spec/RC5ParameterSpec.md) |

This class specifies the parameters used with the [*RC5*](http://www.ietf.org/rfc/rfc2040.txt) algorithm.

The parameters consist of a version number, a rounds count, a word size, and optionally an initialization vector (IV) (only in feedback mode).

This class can be used to initialize a`Cipher`object that implements the*RC5* algorithm as supplied by [RSA Security Inc.](http://www.rsasecurity.com), or any parties authorized by RSA Security.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RC5ParameterSpec](../javax/crypto/spec/RC5ParameterSpec.md))`(`version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rounds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `wordSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a parameter set for RC5 from the given version, number of rounds and word size (in bits). |
| [RC5ParameterSpec](../javax/crypto/spec/RC5ParameterSpec.md))`(`version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rounds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `wordSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `iv:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Constructs a parameter set for RC5 from the given version, number of rounds, word size (in bits), and IV. |
| [RC5ParameterSpec](../javax/crypto/spec/RC5ParameterSpec.md))`(`version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rounds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `wordSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `iv:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a parameter set for RC5 from the given version, number of rounds, word size (in bits), and IV. |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../javax/crypto/spec/RC5ParameterSpec.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Tests for equality between the specified object and this object. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getIV](../javax/crypto/spec/RC5ParameterSpec.md))`()` Returns the IV or null if this parameter set does not contain an IV. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRounds](../javax/crypto/spec/RC5ParameterSpec.md))`()` Returns the number of rounds. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](../javax/crypto/spec/RC5ParameterSpec.md))`()` Returns the version. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWordSize](../javax/crypto/spec/RC5ParameterSpec.md))`()` Returns the word size in bits. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../javax/crypto/spec/RC5ParameterSpec.md))`()` Calculates a hash code value for the object. |
| --- | --- |

## Public constructors

### RC5ParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RC5ParameterSpec(
    version: Int, 
    rounds: Int, 
    wordSize: Int)
```

Constructs a parameter set for RC5 from the given version, number of rounds and word size (in bits).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------|
| `version` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the version. |
| `rounds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of rounds. |
| `wordSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the word size in bits. |
| --- | --- |

### RC5ParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RC5ParameterSpec(
    version: Int, 
    rounds: Int, 
    wordSize: Int, 
    iv: ByteArray!)
```

Constructs a parameter set for RC5 from the given version, number of rounds, word size (in bits), and IV.

Note that the size of the IV (block size) must be twice the word size. The bytes that constitute the IV are those between`iv[0]`and`iv[2*(wordSize/8)-1]`inclusive.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `version` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the version. |
| `rounds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of rounds. |
| `wordSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the word size in bits. |
| --- | --- |
| `iv` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer with the IV. The first`2*(wordSize/8) `bytes of the buffer are copied to protect against subsequent modification. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`iv`is`null`or`(iv.length < 2 * (wordSize / 8))` |

### RC5ParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RC5ParameterSpec(
    version: Int, 
    rounds: Int, 
    wordSize: Int, 
    iv: ByteArray!, 
    offset: Int)
```

Constructs a parameter set for RC5 from the given version, number of rounds, word size (in bits), and IV.

The IV is taken from`iv`, starting at`offset`inclusive. Note that the size of the IV (block size), starting at`offset`inclusive, must be twice the word size. The bytes that constitute the IV are those between`iv[offset]`and`iv[offset+2*(wordSize/8)-1]`inclusive.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `version` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the version. |
| `rounds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of rounds. |
| `wordSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the word size in bits. |
| --- | --- |
| `iv` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer with the IV. The first`2*(wordSize/8) `bytes of the buffer beginning at`offset`inclusive are copied to protect against subsequent modification. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`iv`where the IV starts. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`iv`is`null`or`(iv.length - offset < 2 * (wordSize / 8))` |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Tests for equality between the specified object and this object. Two RC5ParameterSpec objects are considered equal if their version numbers, number of rounds, word sizes, and IVs are equal. (Two IV references are considered equal if both are null.)

| Parameters ||
|-------|---------------------------------------------------|
| `obj` | the object to test for equality with this object. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the objects are considered equal, false if`obj`is null or otherwise. |

### getIV

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIV(): ByteArray!
```

Returns the IV or null if this parameter set does not contain an IV.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the IV or null if this parameter set does not contain an IV. Returns a new array each time this method is called. |

### getRounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRounds(): Int
```

Returns the number of rounds.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rounds. |

### getVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVersion(): Int
```

Returns the version.

| Return ||
|----------------------------------------------------------------------------|--------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the version. |

### getWordSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWordSize(): Int
```

Returns the word size in bits.

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the word size in bits. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Calculates a hash code value for the object. Objects that are equal will also have the same hashcode.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
