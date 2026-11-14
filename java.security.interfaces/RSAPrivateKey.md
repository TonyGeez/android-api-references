# RSAPrivateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAPrivateKey

```
interface RSAPrivateKey : PrivateKey, RSAKey
```

| [java.security.interfaces.RSAPrivateKey](../java/security/interfaces/RSAPrivateKey.md) |

| Known Direct Subclasses [RSAMultiPrimePrivateCrtKey](../java/security/interfaces/RSAMultiPrimePrivateCrtKey.md), [RSAPrivateCrtKey](../java/security/interfaces/RSAPrivateCrtKey.md) |----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RSAMultiPrimePrivateCrtKey](../java/security/interfaces/RSAMultiPrimePrivateCrtKey.md) | The interface to an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateCrtKey](../java/security/interfaces/RSAPrivateCrtKey.md) | The interface to an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The interface to an RSA private key.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](../java/security/interfaces/RSAPrivateKey.md) The type fingerprint that is set to indicate serialization compatibility with a previous version of the type. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](../java/math/BigInteger.md)! | [getPrivateExponent](../java/security/interfaces/RSAPrivateKey.md))`()` Returns the private exponent. |

| Inherited functions ||
|---|---|
| From class [RSAKey](../java/security/interfaces/RSAKey.md) |---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BigInteger](../java/math/BigInteger.md)! | [getModulus](../java/security/interfaces/RSAKey.md))`()` <br /> Returns the modulus. <br /> | | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | [getParams](../java/security/interfaces/RSAKey.md))`()` <br /> Returns the parameters associated with this key. The parameters are optional and may be either explicitly specified or implicitly created during key pair generation. <br /> | ||

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
| [BigInteger](../java/math/BigInteger.md)! | the private exponent |
