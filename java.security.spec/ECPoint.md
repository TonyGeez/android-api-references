# ECPoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECPoint

```
open class ECPoint
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.ECPoint](ECPoint.md) |

This immutable class represents a point on an elliptic curve (EC) in affine coordinates. Other coordinate systems can extend this class to represent this point in other coordinates.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ECPoint](ECPoint.md))`(`x:` ` [BigInteger](../java.math/BigInteger.md)!`, `y:` ` [BigInteger](../java.math/BigInteger.md)!`)` Creates an ECPoint from the specified affine x-coordinate`x`and affine y-coordinate`y`. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](ECPoint.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this elliptic curve point for equality with the specified object. |
| open [BigInteger](../java.math/BigInteger.md)! | [getAffineX](ECPoint.md))`()` Returns the affine x-coordinate`x`. |
| open [BigInteger](../java.math/BigInteger.md)! | [getAffineY](ECPoint.md))`()` Returns the affine y-coordinate`y`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](ECPoint.md))`()` Returns a hash code value for this elliptic curve point. |

| Properties ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ECPoint](ECPoint.md)! | [POINT_INFINITY](ECPoint.md) This defines the point at infinity. |

## Public constructors

### ECPoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ECPoint(
    x: BigInteger!, 
    y: BigInteger!)
```

Creates an ECPoint from the specified affine x-coordinate`x`and affine y-coordinate`y`.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------|
| `x` | [BigInteger](../java.math/BigInteger.md)!:the affine x-coordinate. |
| `y` | [BigInteger](../java.math/BigInteger.md)!:the affine y-coordinate. |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`x`or`y`is null. |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this elliptic curve point for equality with the specified object.

| Parameters ||
|-------|----------------------------|
| `obj` | the object to be compared. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if`obj`is an instance of ECPoint and the affine coordinates match, false otherwise. |

### getAffineX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAffineX(): BigInteger!
```

Returns the affine x-coordinate`x`. Note: POINT_INFINITY has a null affine x-coordinate.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [BigInteger](../java.math/BigInteger.md)! | the affine x-coordinate. |

### getAffineY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAffineY(): BigInteger!
```

Returns the affine y-coordinate`y`. Note: POINT_INFINITY has a null affine y-coordinate.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [BigInteger](../java.math/BigInteger.md)! | the affine y-coordinate. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for this elliptic curve point.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value. |

## Properties

### POINT_INFINITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POINT_INFINITY: ECPoint!
```

This defines the point at infinity.
