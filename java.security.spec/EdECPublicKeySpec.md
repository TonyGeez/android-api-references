# EdECPublicKeySpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EdECPublicKeySpec

```
class EdECPublicKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.EdECPublicKeySpec](../java/security/spec/EdECPublicKeySpec.md) |

A class representing elliptic curve public keys as defined in [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032), including the curve and other algorithm parameters. The public key is a point on the curve, which is represented using an`EdECPoint`.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EdECPublicKeySpec](../java/security/spec/EdECPublicKeySpec.md))`(`params:` ` [NamedParameterSpec](../java/security/spec/NamedParameterSpec.md)`, `point:` ` [EdECPoint](../java/security/spec/EdECPoint.md)`)` Construct a public key spec using the supplied parameters and point. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NamedParameterSpec](../java/security/spec/NamedParameterSpec.md) | [getParams](../java/security/spec/EdECPublicKeySpec.md))`()` Get the algorithm parameters that define the curve and other settings. |
| [EdECPoint](../java/security/spec/EdECPoint.md) | [getPoint](../java/security/spec/EdECPublicKeySpec.md))`()` Get the point representing the public key. |

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
| `params` | [NamedParameterSpec](../java/security/spec/NamedParameterSpec.md):the algorithm parameters. |
| `point` | [EdECPoint](../java/security/spec/EdECPoint.md):the point representing the public key. |

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
| [NamedParameterSpec](../java/security/spec/NamedParameterSpec.md) | the parameters. |

### getPoint

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPoint(): EdECPoint
```

Get the point representing the public key.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------|
| [EdECPoint](../java/security/spec/EdECPoint.md) | the`EdECPoint`representing the public key. |
