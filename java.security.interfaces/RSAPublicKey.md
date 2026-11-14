# RSAPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAPublicKey

```
interface RSAPublicKey : PublicKey, RSAKey
```

| [java.security.interfaces.RSAPublicKey](RSAPublicKey.md) |

The interface to an RSA public key.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](RSAPublicKey.md) The type fingerprint that is set to indicate serialization compatibility with a previous version of the type. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](../java.math/BigInteger.md)! | [getPublicExponent](RSAPublicKey.md))`()` Returns the public exponent. |

| Inherited functions ||
|---|---|
| From class [RSAKey](RSAKey.md) |---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BigInteger](../java.math/BigInteger.md)! | [getModulus](RSAKey.md))`()` <br /> Returns the modulus. <br /> | | [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)! | [getParams](RSAKey.md))`()` <br /> Returns the parameters associated with this key. The parameters are optional and may be either explicitly specified or implicitly created during key pair generation. <br /> | ||

## Constants

### serialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val serialVersionUID: Long
```

**Deprecated:** *A`serialVersionUID`field in an interface is ineffectual. Do not use; no replacement.*

The type fingerprint that is set to indicate serialization compatibility with a previous version of the type. 

 Value: -8727434096241101194L

## Public methods

### getPublicExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPublicExponent(): BigInteger!
```

Returns the public exponent.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](../java.math/BigInteger.md)! | the public exponent |
