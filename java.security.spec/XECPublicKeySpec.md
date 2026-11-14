# XECPublicKeySpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XECPublicKeySpec

```
open class XECPublicKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.XECPublicKeySpec](../java/security/spec/XECPublicKeySpec.md) |

A class representing elliptic curve public keys as defined in RFC 7748, including the curve and other algorithm parameters. The public key is a particular point on the curve, which is represented using only its u-coordinate. A u-coordinate is an element of the field of integers modulo some value that is determined by the algorithm parameters. This field element is represented by a BigInteger which may hold any value. That is, the BigInteger is not restricted to the range of canonical field elements.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XECPublicKeySpec](../java/security/spec/XECPublicKeySpec.md))`(`params:` ` [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!`, `u:` ` [BigInteger](../java/math/BigInteger.md)!`)` Construct a public key spec using the supplied parameters and u coordinate. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | [getParams](../java/security/spec/XECPublicKeySpec.md))`()` Get the algorithm parameters that define the curve and other settings. |
| open [BigInteger](../java/math/BigInteger.md)! | [getU](../java/security/spec/XECPublicKeySpec.md))`()` Get the u coordinate of the point. |

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
| `params` | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!:the algorithm parameters |
| `u` | [BigInteger](../java/math/BigInteger.md)!:the u-coordinate of the point, represented using a BigInteger which may hold any value |

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
| [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | the parameters |

### getU

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getU(): BigInteger!
```

Get the u coordinate of the point.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [BigInteger](../java/math/BigInteger.md)! | the u-coordinate, represented using a BigInteger which may hold any value |
