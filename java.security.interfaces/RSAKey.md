# RSAKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAKey

```
interface RSAKey
```

| [java.security.interfaces.RSAKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAKey#) |

| Known Direct Subclasses [RSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateKey), [RSAPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPublicKey) |--------------------------------------------------------------------------------------------------------|--------------------------------------| | [RSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateKey) | The interface to an RSA private key. | | [RSAPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPublicKey) | The interface to an RSA public key. | |

| Known Indirect Subclasses [RSAMultiPrimePrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey), [RSAPrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateCrtKey) |----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RSAMultiPrimePrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey) | The interface to an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateCrtKey) | The interface to an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | |

The interface to a public or private key in [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, such as those for RSA, or RSASSA-PSS algorithms.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getModulus](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAKey#getModulus())`()` Returns the modulus. |
| open [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)! | [getParams](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAKey#getParams())`()` Returns the parameters associated with this key. |

## Public methods

### getModulus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getModulus(): BigInteger!
```

Returns the modulus.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the modulus |

### getParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParams(): AlgorithmParameterSpec!
```

Returns the parameters associated with this key. The parameters are optional and may be either explicitly specified or implicitly created during key pair generation.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)! | the associated parameters, may be null |
