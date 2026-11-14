# ECParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECParameterSpec

```
open class ECParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.ECParameterSpec](ECParameterSpec.md) |

This immutable class specifies the set of domain parameters used with elliptic curve cryptography (ECC).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ECParameterSpec](ECParameterSpec.md))`(`curve:` ` [EllipticCurve](EllipticCurve.md)!`, `g:` ` [ECPoint](ECPoint.md)!`, `n:` ` [BigInteger](../java.math/BigInteger.md)!`, `h:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates elliptic curve domain parameters based on the specified values. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCofactor](ECParameterSpec.md))`()` Returns the cofactor. |
| open [EllipticCurve](EllipticCurve.md)! | [getCurve](ECParameterSpec.md))`()` Returns the elliptic curve that this parameter defines. |
| open [ECPoint](ECPoint.md)! | [getGenerator](ECParameterSpec.md))`()` Returns the generator which is also known as the base point. |
| --- | --- |
| open [BigInteger](../java.math/BigInteger.md)! | [getOrder](ECParameterSpec.md))`()` Returns the order of the generator. |

## Public constructors

### ECParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ECParameterSpec(
    curve: EllipticCurve!, 
    g: ECPoint!, 
    n: BigInteger!, 
    h: Int)
```

Creates elliptic curve domain parameters based on the specified values.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `curve` | [EllipticCurve](EllipticCurve.md)!:the elliptic curve which this parameter defines. |
| `g` | [ECPoint](ECPoint.md)!:the generator which is also known as the base point. |
| `n` | [BigInteger](../java.math/BigInteger.md)!:the order of the generator`g`. |
| --- | --- |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the cofactor. |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.lang.NullPointerException` | if`curve`,`g`, or`n`is null. |
| `java.lang.IllegalArgumentException` | if`n`or`h`is not positive. |

## Public methods

### getCofactor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCofactor(): Int
```

Returns the cofactor.

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the cofactor. |

### getCurve

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurve(): EllipticCurve!
```

Returns the elliptic curve that this parameter defines.

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [EllipticCurve](EllipticCurve.md)! | the elliptic curve that this parameter defines. |

### getGenerator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGenerator(): ECPoint!
```

Returns the generator which is also known as the base point.

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------------------|
| [ECPoint](ECPoint.md)! | the generator which is also known as the base point. |

### getOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOrder(): BigInteger!
```

Returns the order of the generator.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [BigInteger](../java.math/BigInteger.md)! | the order of the generator. |
