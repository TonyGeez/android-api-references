# RSAPrivateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAPrivateKey

```
interface RSAPrivateKey : PrivateKey, RSAKey
```

| [java.security.interfaces.RSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateKey#) |

| Known Direct Subclasses [RSAMultiPrimePrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey), [RSAPrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateCrtKey) |----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RSAMultiPrimePrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey) | The interface to an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateCrtKey) | The interface to an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | |

The interface to an RSA private key.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateKey#serialVersionUID:kotlin.Long) The type fingerprint that is set to indicate serialization compatibility with a previous version of the type. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrivateExponent](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateKey#getPrivateExponent())`()` Returns the private exponent. |

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

 Value: 5187144804936595022L

## Public methods

### getPrivateExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrivateExponent(): BigInteger!
```

Returns the private exponent.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the private exponent |
