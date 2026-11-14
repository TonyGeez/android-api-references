# ECPrivateKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECPrivateKeySpec

```
open class ECPrivateKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.ECPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/ECPrivateKeySpec#) |

This immutable class specifies an elliptic curve private key with its associated parameters.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ECPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/ECPrivateKeySpec#ECPrivateKeySpec(java.math.BigInteger,%20java.security.spec.ECParameterSpec))`(`s:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `params:` ` [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec)!`)` Creates a new ECPrivateKeySpec with the specified parameter values. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec)! | [getParams](https://developer.android.com/reference/kotlin/java/security/spec/ECPrivateKeySpec#getParams())`()` Returns the associated elliptic curve domain parameters. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getS](https://developer.android.com/reference/kotlin/java/security/spec/ECPrivateKeySpec#getS())`()` Returns the private value S. |

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
| `s` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the private value. |
| `params` | [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec)!:the associated elliptic curve domain parameters. |

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
| [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec)! | the EC domain parameters. |

### getS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getS(): BigInteger!
```

Returns the private value S.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the private value S. |
