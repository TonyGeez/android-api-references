# EdECPoint

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EdECPoint

```
class EdECPoint
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.EdECPoint](https://developer.android.com/reference/kotlin/java/security/spec/EdECPoint#) |

An elliptic curve point used to specify keys as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). These points are distinct from the points represented by`ECPoint`, and they are intended for use with algorithms based on RFC 8032 such as the EdDSA`Signature`algorithm.

An EdEC point is specified by its y-coordinate value and a boolean that indicates whether the x-coordinate is odd. The y-coordinate is an element of the field of integers modulo some value p that is determined by the algorithm parameters. This field element is represented by a`BigInteger`, and implementations that consume objects of this class may reject integer values which are not in the range \[0, p).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EdECPoint](https://developer.android.com/reference/kotlin/java/security/spec/EdECPoint#EdECPoint(kotlin.Boolean,%20java.math.BigInteger))`(`xOdd:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `y:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)`)` Construct an EdECPoint. |

| Public methods ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#) | [getY](https://developer.android.com/reference/kotlin/java/security/spec/EdECPoint#getY())`()` Get the y-coordinate of the point. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isXOdd](https://developer.android.com/reference/kotlin/java/security/spec/EdECPoint#isXOdd())`()` Get whether the x-coordinate of the point is odd. |

## Public constructors

### EdECPoint

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EdECPoint(
    xOdd: Boolean, 
    y: BigInteger)
```

Construct an EdECPoint.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `xOdd` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the x-coordinate is odd. |
| `y` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#):the y-coordinate, represented using a`BigInteger`. |

| Exceptions ||
|----------------------------------|---------------|
| `java.lang.NullPointerException` | if`y`is null. |

## Public methods

### getY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getY(): BigInteger
```

Get the y-coordinate of the point.

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#) | the y-coordinate, represented using a`BigInteger`. |

### isXOdd

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isXOdd(): Boolean
```

Get whether the x-coordinate of the point is odd.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a boolean indicating whether the x-coordinate is odd. |
