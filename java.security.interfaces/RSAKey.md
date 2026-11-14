# RSAKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAKey

```
interface RSAKey
```

| [java.security.interfaces.RSAKey](../java/security/interfaces/RSAKey.md) |

| Known Direct Subclasses [RSAPrivateKey](../java/security/interfaces/RSAPrivateKey.md), [RSAPublicKey](../java/security/interfaces/RSAPublicKey.md) |--------------------------------------------------------------------------------------------------------|--------------------------------------| | [RSAPrivateKey](../java/security/interfaces/RSAPrivateKey.md) | The interface to an RSA private key. | | [RSAPublicKey](../java/security/interfaces/RSAPublicKey.md) | The interface to an RSA public key. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [RSAMultiPrimePrivateCrtKey](../java/security/interfaces/RSAMultiPrimePrivateCrtKey.md), [RSAPrivateCrtKey](../java/security/interfaces/RSAPrivateCrtKey.md) |----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RSAMultiPrimePrivateCrtKey](../java/security/interfaces/RSAMultiPrimePrivateCrtKey.md) | The interface to an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateCrtKey](../java/security/interfaces/RSAPrivateCrtKey.md) | The interface to an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The interface to a public or private key in [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, such as those for RSA, or RSASSA-PSS algorithms.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](../java/math/BigInteger.md)! | [getModulus](../java/security/interfaces/RSAKey.md))`()` Returns the modulus. |
| open [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | [getParams](../java/security/interfaces/RSAKey.md))`()` Returns the parameters associated with this key. |

## Public methods

### getModulus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getModulus(): BigInteger!
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

Returns the parameters associated with this key. The parameters are optional and may be either explicitly specified or implicitly created during key pair generation.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | the associated parameters, may be null |
