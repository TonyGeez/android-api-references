# XECPublicKeySpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XECPublicKeySpec

```
open class XECPublicKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.XECPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/XECPublicKeySpec#) |

A class representing elliptic curve public keys as defined in RFC 7748, including the curve and other algorithm parameters. The public key is a particular point on the curve, which is represented using only its u-coordinate. A u-coordinate is an element of the field of integers modulo some value that is determined by the algorithm parameters. This field element is represented by a BigInteger which may hold any value. That is, the BigInteger is not restricted to the range of canonical field elements.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XECPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/XECPublicKeySpec#XECPublicKeySpec(java.security.spec.AlgorithmParameterSpec,%20java.math.BigInteger))`(`params:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!`, `u:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Construct a public key spec using the supplied parameters and u coordinate. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)! | [getParams](https://developer.android.com/reference/kotlin/java/security/spec/XECPublicKeySpec#getParams())`()` Get the algorithm parameters that define the curve and other settings. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getU](https://developer.android.com/reference/kotlin/java/security/spec/XECPublicKeySpec#getU())`()` Get the u coordinate of the point. |

## Public constructors

### XECPublicKeySpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XECPublicKeySpec(
    params: AlgorithmParameterSpec!, 
    u: BigInteger!)
```

Construct a public key spec using the supplied parameters and u coordinate.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!:the algorithm parameters |
| `u` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the u-coordinate of the point, represented using a BigInteger which may hold any value |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if`params`or`u`is null. |

## Public methods

### getParams

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParams(): AlgorithmParameterSpec!
```

Get the algorithm parameters that define the curve and other settings.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|----------------|
| [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)! | the parameters |

### getU

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getU(): BigInteger!
```

Get the u coordinate of the point.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the u-coordinate, represented using a BigInteger which may hold any value |
