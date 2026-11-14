# RSAPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAPublicKeySpec

```
open class RSAPublicKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.RSAPublicKeySpec](../java/security/spec/RSAPublicKeySpec.md) |

This class specifies an RSA public key.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RSAPublicKeySpec](../java/security/spec/RSAPublicKeySpec.md))`(`modulus:` ` [BigInteger](../java/math/BigInteger.md)!`, `publicExponent:` ` [BigInteger](../java/math/BigInteger.md)!`)` Creates a new RSAPublicKeySpec. |
| [RSAPublicKeySpec](../java/security/spec/RSAPublicKeySpec.md))`(`modulus:` ` [BigInteger](../java/math/BigInteger.md)!`, `publicExponent:` ` [BigInteger](../java/math/BigInteger.md)!`, `params:` ` [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!`)` Creates a new RSAPublicKeySpec with additional key parameters. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](../java/math/BigInteger.md)! | [getModulus](../java/security/spec/RSAPublicKeySpec.md))`()` Returns the modulus. |
| open [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | [getParams](../java/security/spec/RSAPublicKeySpec.md))`()` Returns the parameters associated with this key, may be null if not present. |
| open [BigInteger](../java/math/BigInteger.md)! | [getPublicExponent](../java/security/spec/RSAPublicKeySpec.md))`()` Returns the public exponent. |
| --- | --- |

## Public constructors

### RSAPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAPublicKeySpec(
    modulus: BigInteger!, 
    publicExponent: BigInteger!)
```

Creates a new RSAPublicKeySpec.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------|
| `modulus` | [BigInteger](../java/math/BigInteger.md)!:the modulus |
| `publicExponent` | [BigInteger](../java/math/BigInteger.md)!:the public exponent |

### RSAPublicKeySpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAPublicKeySpec(
    modulus: BigInteger!, 
    publicExponent: BigInteger!, 
    params: AlgorithmParameterSpec!)
```

Creates a new RSAPublicKeySpec with additional key parameters.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `modulus` | [BigInteger](../java/math/BigInteger.md)!:the modulus |
| `publicExponent` | [BigInteger](../java/math/BigInteger.md)!:the public exponent |
| `params` | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!:the parameters associated with this key, may be null |
| --- | --- |

## Public methods

### getModulus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getModulus(): BigInteger!
```

Returns the modulus.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [BigInteger](../java/math/BigInteger.md)! | the modulus |

### getParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParams(): AlgorithmParameterSpec!
```

Returns the parameters associated with this key, may be null if not present.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | the parameters associated with this key |

### getPublicExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicExponent(): BigInteger!
```

Returns the public exponent.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](../java/math/BigInteger.md)! | the public exponent |
