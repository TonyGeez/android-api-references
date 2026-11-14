# RSAPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAPublicKey

```
interface RSAPublicKey : PublicKey, RSAKey
```

| [java.security.interfaces.RSAPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPublicKey#) |

The interface to an RSA public key.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPublicKey#serialVersionUID:kotlin.Long) The type fingerprint that is set to indicate serialization compatibility with a previous version of the type. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPublicExponent](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPublicKey#getPublicExponent())`()` Returns the public exponent. |

| Inherited functions ||
|---|---|
| From class [RSAKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAKey) |---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getModulus](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAKey#getModulus())`()` <br /> Returns the modulus. <br /> | | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)! | [getParams](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAKey#getParams())`()` <br /> Returns the parameters associated with this key. The parameters are optional and may be either explicitly specified or implicitly created during key pair generation. <br /> | ||

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
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the public exponent |
