# ECFieldFp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECFieldFp

```
open class ECFieldFp : ECField
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.ECFieldFp](ECFieldFp.md) |

This immutable class defines an elliptic curve (EC) prime finite field.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ECFieldFp](ECFieldFp.md))`(`p:` ` [BigInteger](../java.math/BigInteger.md)!`)` Creates an elliptic curve prime finite field with the specified prime`p`. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](ECFieldFp.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this prime finite field for equality with the specified object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFieldSize](ECFieldFp.md))`()` Returns the field size in bits which is size of prime p for this prime finite field. |
| open [BigInteger](../java.math/BigInteger.md)! | [getP](ECFieldFp.md))`()` Returns the prime`p`of this prime finite field. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](ECFieldFp.md))`()` Returns a hash code value for this prime finite field. |

## Public constructors

### ECFieldFp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ECFieldFp(p: BigInteger!)
```

Creates an elliptic curve prime finite field with the specified prime`p`.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `p` | [BigInteger](../java.math/BigInteger.md)!:the prime. |

| Exceptions ||
|--------------------------------------|-----------------------|
| `java.lang.NullPointerException` | if`p`is null. |
| `java.lang.IllegalArgumentException` | if`p`is not positive. |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this prime finite field for equality with the specified object.

| Parameters ||
|-------|----------------------------|
| `obj` | the object to be compared. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if`obj`is an instance of ECFieldFp and the prime value match, false otherwise. |

### getFieldSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFieldSize(): Int
```

Returns the field size in bits which is size of prime p for this prime finite field.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the field size in bits. |

### getP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getP(): BigInteger!
```

Returns the prime`p`of this prime finite field.

| Return ||
|------------------------------------------------------------------------------------------|------------|
| [BigInteger](../java.math/BigInteger.md)! | the prime. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for this prime finite field.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value. |
