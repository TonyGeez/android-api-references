# EllipticCurve

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EllipticCurve

```
open class EllipticCurve
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.EllipticCurve](EllipticCurve.md) |

This immutable class holds the necessary values needed to represent an elliptic curve.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EllipticCurve](EllipticCurve.md))`(`field:` ` [ECField](ECField.md)!`, `a:` ` [BigInteger](../java.math/BigInteger.md)!`, `b:` ` [BigInteger](../java.math/BigInteger.md)!`)` Creates an elliptic curve with the specified elliptic field`field`and the coefficients`a`and`b`. |
| [EllipticCurve](EllipticCurve.md))`(`field:` ` [ECField](ECField.md)!`, `a:` ` [BigInteger](../java.math/BigInteger.md)!`, `b:` ` [BigInteger](../java.math/BigInteger.md)!`, `seed:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates an elliptic curve with the specified elliptic field`field`, the coefficients`a`and`b`, and the`seed`used for curve generation. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](EllipticCurve.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this elliptic curve for equality with the specified object. |
| open [BigInteger](../java.math/BigInteger.md)! | [getA](EllipticCurve.md))`()` Returns the first coefficient`a`of the elliptic curve. |
| open [BigInteger](../java.math/BigInteger.md)! | [getB](EllipticCurve.md))`()` Returns the second coefficient`b`of the elliptic curve. |
| --- | --- |
| open [ECField](ECField.md)! | [getField](EllipticCurve.md))`()` Returns the finite field`field`that this elliptic curve is over. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getSeed](EllipticCurve.md))`()` Returns the seeding bytes`seed`used during curve generation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](EllipticCurve.md))`()` Returns a hash code value for this elliptic curve. |
| --- | --- |

## Public constructors

### EllipticCurve

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EllipticCurve(
    field: ECField!, 
    a: BigInteger!, 
    b: BigInteger!)
```

Creates an elliptic curve with the specified elliptic field`field`and the coefficients`a`and`b`.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [ECField](ECField.md)!:the finite field that this elliptic curve is over. |
| `a` | [BigInteger](../java.math/BigInteger.md)!:the first coefficient of this elliptic curve. |
| `b` | [BigInteger](../java.math/BigInteger.md)!:the second coefficient of this elliptic curve. |
| --- | --- |

| Exceptions ||
|--------------------------------------|------------------------------------------|
| `java.lang.NullPointerException` | if`field`,`a`, or`b`is null. |
| `java.lang.IllegalArgumentException` | if`a`or`b`is not null and not in`field`. |

### EllipticCurve

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EllipticCurve(
    field: ECField!, 
    a: BigInteger!, 
    b: BigInteger!, 
    seed: ByteArray!)
```

Creates an elliptic curve with the specified elliptic field`field`, the coefficients`a`and`b`, and the`seed`used for curve generation.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [ECField](ECField.md)!:the finite field that this elliptic curve is over. |
| `a` | [BigInteger](../java.math/BigInteger.md)!:the first coefficient of this elliptic curve. |
| `b` | [BigInteger](../java.math/BigInteger.md)!:the second coefficient of this elliptic curve. |
| --- | --- |
| `seed` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the bytes used during curve generation for later validation. Contents of this array are copied to protect against subsequent modification. |

| Exceptions ||
|--------------------------------------|------------------------------------------|
| `java.lang.NullPointerException` | if`field`,`a`, or`b`is null. |
| `java.lang.IllegalArgumentException` | if`a`or`b`is not null and not in`field`. |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this elliptic curve for equality with the specified object.

| Parameters ||
|-------|----------------------------|
| `obj` | the object to be compared. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if`obj`is an instance of EllipticCurve and the field, A, and B match, false otherwise. |

### getA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getA(): BigInteger!
```

Returns the first coefficient`a`of the elliptic curve.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------|
| [BigInteger](../java.math/BigInteger.md)! | the first coefficient`a`. |

### getB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getB(): BigInteger!
```

Returns the second coefficient`b`of the elliptic curve.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------|
| [BigInteger](../java.math/BigInteger.md)! | the second coefficient`b`. |

### getField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getField(): ECField!
```

Returns the finite field`field`that this elliptic curve is over.

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------|
| [ECField](ECField.md)! | the field`field`that this curve is over. |

### getSeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSeed(): ByteArray!
```

Returns the seeding bytes`seed`used during curve generation. May be null if not specified.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the seeding bytes`seed`. A new array is returned each time this method is called. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for this elliptic curve.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value computed from the hash codes of the field, A, and B, as follows: ```kotlin <code>(field.hashCode() &lt;&lt; 6) + (a.hashCode() &lt;&lt; 4) + (b.hashCode() &lt;&lt; 2) </code> ``` |
