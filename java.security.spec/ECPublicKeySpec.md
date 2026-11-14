# ECPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECPublicKeySpec

```
open class ECPublicKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.ECPublicKeySpec](../java/security/spec/ECPublicKeySpec.md) |

This immutable class specifies an elliptic curve public key with its associated parameters.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ECPublicKeySpec](../java/security/spec/ECPublicKeySpec.md))`(`w:` ` [ECPoint](../java/security/spec/ECPoint.md)!`, `params:` ` [ECParameterSpec](../java/security/spec/ECParameterSpec.md)!`)` Creates a new ECPublicKeySpec with the specified parameter values. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ECParameterSpec](../java/security/spec/ECParameterSpec.md)! | [getParams](../java/security/spec/ECPublicKeySpec.md))`()` Returns the associated elliptic curve domain parameters. |
| open [ECPoint](../java/security/spec/ECPoint.md)! | [getW](../java/security/spec/ECPublicKeySpec.md))`()` Returns the public point W. |

## Public constructors

### ECPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ECPublicKeySpec(
    w: ECPoint!, 
    params: ECParameterSpec!)
```

Creates a new ECPublicKeySpec with the specified parameter values.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `w` | [ECPoint](../java/security/spec/ECPoint.md)!:the public point. |
| `params` | [ECParameterSpec](../java/security/spec/ECParameterSpec.md)!:the associated elliptic curve domain parameters. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------|
| `java.lang.NullPointerException` | if`w`or`params`is null. |
| `java.lang.IllegalArgumentException` | if`w`is point at infinity, i.e. ECPoint.POINT_INFINITY |

## Public methods

### getParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParams(): ECParameterSpec!
```

Returns the associated elliptic curve domain parameters.

| Return ||
|-------------------------------------------------------------------------------------------------------|---------------------------|
| [ECParameterSpec](../java/security/spec/ECParameterSpec.md)! | the EC domain parameters. |

### getW

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getW(): ECPoint!
```

Returns the public point W.

| Return ||
|---------------------------------------------------------------------------------------|---------------------|
| [ECPoint](../java/security/spec/ECPoint.md)! | the public point W. |
