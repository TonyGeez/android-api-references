# RC2ParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RC2ParameterSpec

```
open class RC2ParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.RC2ParameterSpec](RC2ParameterSpec.md) |

This class specifies the parameters used with the [*RC2*](http://www.ietf.org/rfc/rfc2268.txt) algorithm.

The parameters consist of an effective key size and optionally an 8-byte initialization vector (IV) (only in feedback mode).

This class can be used to initialize a`Cipher`object that implements the*RC2*algorithm.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RC2ParameterSpec](RC2ParameterSpec.md))`(`effectiveKeyBits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a parameter set for RC2 from the given effective key size (in bits). |
| [RC2ParameterSpec](RC2ParameterSpec.md))`(`effectiveKeyBits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `iv:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Constructs a parameter set for RC2 from the given effective key size (in bits) and an 8-byte IV. |
| [RC2ParameterSpec](RC2ParameterSpec.md))`(`effectiveKeyBits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `iv:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a parameter set for RC2 from the given effective key size (in bits) and IV. |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](RC2ParameterSpec.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Tests for equality between the specified object and this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEffectiveKeyBits](RC2ParameterSpec.md))`()` Returns the effective key size in bits. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getIV](RC2ParameterSpec.md))`()` Returns the IV or null if this parameter set does not contain an IV. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](RC2ParameterSpec.md))`()` Calculates a hash code value for the object. |

## Public constructors

### RC2ParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RC2ParameterSpec(effectiveKeyBits: Int)
```

Constructs a parameter set for RC2 from the given effective key size (in bits).

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------|
| `effectiveKeyBits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the effective key size in bits. |

### RC2ParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RC2ParameterSpec(
    effectiveKeyBits: Int, 
    iv: ByteArray!)
```

Constructs a parameter set for RC2 from the given effective key size (in bits) and an 8-byte IV.

The bytes that constitute the IV are those between`iv[0]`and`iv[7]`inclusive.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effectiveKeyBits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the effective key size in bits. |
| `iv` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer with the 8-byte IV. The first 8 bytes of the buffer are copied to protect against subsequent modification. |

| Exceptions ||
|--------------------------------------|----------------|
| `java.lang.IllegalArgumentException` | if`iv`is null. |

### RC2ParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RC2ParameterSpec(
    effectiveKeyBits: Int, 
    iv: ByteArray!, 
    offset: Int)
```

Constructs a parameter set for RC2 from the given effective key size (in bits) and IV.

The IV is taken from`iv`, starting at`offset`inclusive. The bytes that constitute the IV are those between`iv[offset]`and`iv[offset+7]`inclusive.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effectiveKeyBits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the effective key size in bits. |
| `iv` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer with the IV. The first 8 bytes of the buffer beginning at`offset`inclusive are copied to protect against subsequent modification. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`iv`where the 8-byte IV starts. |
| --- | --- |

| Exceptions ||
|--------------------------------------|----------------|
| `java.lang.IllegalArgumentException` | if`iv`is null. |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Tests for equality between the specified object and this object. Two RC2ParameterSpec objects are considered equal if their effective key sizes and IVs are equal. (Two IV references are considered equal if both are null.)

| Parameters ||
|-------|---------------------------------------------------|
| `obj` | the object to test for equality with this object. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the objects are considered equal, false if`obj`is null or otherwise. |

### getEffectiveKeyBits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEffectiveKeyBits(): Int
```

Returns the effective key size in bits.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the effective key size in bits. |

### getIV

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIV(): ByteArray!
```

Returns the IV or null if this parameter set does not contain an IV.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the IV or null if this parameter set does not contain an IV. Returns a new array each time this method is called. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Calculates a hash code value for the object. Objects that are equal will also have the same hashcode.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
