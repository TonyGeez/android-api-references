# ECPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECPublicKeySpec

```
open class ECPublicKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.ECPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/ECPublicKeySpec#) |

This immutable class specifies an elliptic curve public key with its associated parameters.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ECPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/ECPublicKeySpec#ECPublicKeySpec(java.security.spec.ECPoint,%20java.security.spec.ECParameterSpec))`(`w:` ` [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint)!`, `params:` ` [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec)!`)` Creates a new ECPublicKeySpec with the specified parameter values. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec)! | [getParams](https://developer.android.com/reference/kotlin/java/security/spec/ECPublicKeySpec#getParams())`()` Returns the associated elliptic curve domain parameters. |
| open [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint)! | [getW](https://developer.android.com/reference/kotlin/java/security/spec/ECPublicKeySpec#getW())`()` Returns the public point W. |

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
| `w` | [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint)!:the public point. |
| `params` | [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec)!:the associated elliptic curve domain parameters. |

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
| [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec)! | the EC domain parameters. |

### getW

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getW(): ECPoint!
```

Returns the public point W.

| Return ||
|---------------------------------------------------------------------------------------|---------------------|
| [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint)! | the public point W. |
