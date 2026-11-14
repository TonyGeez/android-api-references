# ECParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECParameterSpec

```
open class ECParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec#) |

This immutable class specifies the set of domain parameters used with elliptic curve cryptography (ECC).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec#ECParameterSpec(java.security.spec.EllipticCurve,%20java.security.spec.ECPoint,%20java.math.BigInteger,%20kotlin.Int))`(`curve:` ` [EllipticCurve](https://developer.android.com/reference/kotlin/java/security/spec/EllipticCurve)!`, `g:` ` [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint)!`, `n:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `h:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates elliptic curve domain parameters based on the specified values. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCofactor](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec#getCofactor())`()` Returns the cofactor. |
| open [EllipticCurve](https://developer.android.com/reference/kotlin/java/security/spec/EllipticCurve)! | [getCurve](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec#getCurve())`()` Returns the elliptic curve that this parameter defines. |
| open [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint)! | [getGenerator](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec#getGenerator())`()` Returns the generator which is also known as the base point. |
| --- | --- |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getOrder](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec#getOrder())`()` Returns the order of the generator. |

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
| `curve` | [EllipticCurve](https://developer.android.com/reference/kotlin/java/security/spec/EllipticCurve)!:the elliptic curve which this parameter defines. |
| `g` | [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint)!:the generator which is also known as the base point. |
| `n` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the order of the generator`g`. |
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
| [EllipticCurve](https://developer.android.com/reference/kotlin/java/security/spec/EllipticCurve)! | the elliptic curve that this parameter defines. |

### getGenerator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGenerator(): ECPoint!
```

Returns the generator which is also known as the base point.

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------------------|
| [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint)! | the generator which is also known as the base point. |

### getOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOrder(): BigInteger!
```

Returns the order of the generator.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the order of the generator. |
