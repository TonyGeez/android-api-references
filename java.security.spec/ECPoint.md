# ECPoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECPoint

```
open class ECPoint
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint#) |

This immutable class represents a point on an elliptic curve (EC) in affine coordinates. Other coordinate systems can extend this class to represent this point in other coordinates.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint#ECPoint(java.math.BigInteger,%20java.math.BigInteger))`(`x:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `y:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Creates an ECPoint from the specified affine x-coordinate`x`and affine y-coordinate`y`. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this elliptic curve point for equality with the specified object. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getAffineX](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint#getAffineX())`()` Returns the affine x-coordinate`x`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getAffineY](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint#getAffineY())`()` Returns the affine y-coordinate`y`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint#hashCode())`()` Returns a hash code value for this elliptic curve point. |

| Properties ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint#)! | [POINT_INFINITY](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint#POINT_INFINITY:java.security.spec.ECPoint) This defines the point at infinity. |

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
| `x` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the affine x-coordinate. |
| `y` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the affine y-coordinate. |

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
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the affine x-coordinate. |

### getAffineY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAffineY(): BigInteger!
```

Returns the affine y-coordinate`y`. Note: POINT_INFINITY has a null affine y-coordinate.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the affine y-coordinate. |

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
