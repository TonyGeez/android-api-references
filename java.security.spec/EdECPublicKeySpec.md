# EdECPublicKeySpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EdECPublicKeySpec

```
class EdECPublicKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.EdECPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/EdECPublicKeySpec#) |

A class representing elliptic curve public keys as defined in [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032), including the curve and other algorithm parameters. The public key is a point on the curve, which is represented using an`EdECPoint`.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EdECPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/EdECPublicKeySpec#EdECPublicKeySpec(java.security.spec.NamedParameterSpec,%20java.security.spec.EdECPoint))`(`params:` ` [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec)`, `point:` ` [EdECPoint](https://developer.android.com/reference/kotlin/java/security/spec/EdECPoint)`)` Construct a public key spec using the supplied parameters and point. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec) | [getParams](https://developer.android.com/reference/kotlin/java/security/spec/EdECPublicKeySpec#getParams())`()` Get the algorithm parameters that define the curve and other settings. |
| [EdECPoint](https://developer.android.com/reference/kotlin/java/security/spec/EdECPoint) | [getPoint](https://developer.android.com/reference/kotlin/java/security/spec/EdECPublicKeySpec#getPoint())`()` Get the point representing the public key. |

## Public constructors

### EdECPublicKeySpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EdECPublicKeySpec(
    params: NamedParameterSpec, 
    point: EdECPoint)
```

Construct a public key spec using the supplied parameters and point.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec):the algorithm parameters. |
| `point` | [EdECPoint](https://developer.android.com/reference/kotlin/java/security/spec/EdECPoint):the point representing the public key. |

| Exceptions ||
|----------------------------------|-----------------------------|
| `java.lang.NullPointerException` | if`params`or`point`is null. |

## Public methods

### getParams

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParams(): NamedParameterSpec
```

Get the algorithm parameters that define the curve and other settings.

| Return ||
|------------------------------------------------------------------------------------------------------------|-----------------|
| [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec) | the parameters. |

### getPoint

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPoint(): EdECPoint
```

Get the point representing the public key.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------|
| [EdECPoint](https://developer.android.com/reference/kotlin/java/security/spec/EdECPoint) | the`EdECPoint`representing the public key. |
