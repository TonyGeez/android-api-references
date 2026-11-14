# ECPrivateKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECPrivateKeySpec

```
open class ECPrivateKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.ECPrivateKeySpec](../java/security/spec/ECPrivateKeySpec.md) |

This immutable class specifies an elliptic curve private key with its associated parameters.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ECPrivateKeySpec](../java/security/spec/ECPrivateKeySpec.md))`(`s:` ` [BigInteger](../java/math/BigInteger.md)!`, `params:` ` [ECParameterSpec](../java/security/spec/ECParameterSpec.md)!`)` Creates a new ECPrivateKeySpec with the specified parameter values. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ECParameterSpec](../java/security/spec/ECParameterSpec.md)! | [getParams](../java/security/spec/ECPrivateKeySpec.md))`()` Returns the associated elliptic curve domain parameters. |
| open [BigInteger](../java/math/BigInteger.md)! | [getS](../java/security/spec/ECPrivateKeySpec.md))`()` Returns the private value S. |

## Public constructors

### ECPrivateKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ECPrivateKeySpec(
    s: BigInteger!, 
    params: ECParameterSpec!)
```

Creates a new ECPrivateKeySpec with the specified parameter values.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [BigInteger](../java/math/BigInteger.md)!:the private value. |
| `params` | [ECParameterSpec](../java/security/spec/ECParameterSpec.md)!:the associated elliptic curve domain parameters. |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if`s`or`params`is null. |

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

### getS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getS(): BigInteger!
```

Returns the private value S.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](../java/math/BigInteger.md)! | the private value S. |
