# RSAMultiPrimePrivateCrtKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAMultiPrimePrivateCrtKey

```
interface RSAMultiPrimePrivateCrtKey : RSAPrivateKey
```

| [java.security.interfaces.RSAMultiPrimePrivateCrtKey](RSAMultiPrimePrivateCrtKey.md) |

The interface to an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](RSAMultiPrimePrivateCrtKey.md) The type fingerprint that is set to indicate serialization compatibility with a previous version of the type. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](../java.math/BigInteger.md)! | [getCrtCoefficient](RSAMultiPrimePrivateCrtKey.md))`()` Returns the crtCoefficient. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RSAOtherPrimeInfo](../java.security.spec/RSAOtherPrimeInfo.md)!\>! | [getOtherPrimeInfo](RSAMultiPrimePrivateCrtKey.md))`()` Returns the otherPrimeInfo or null if there are only two prime factors (p and q). |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getPrimeExponentP](RSAMultiPrimePrivateCrtKey.md))`()` Returns the primeExponentP. |
| --- | --- |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getPrimeExponentQ](RSAMultiPrimePrivateCrtKey.md))`()` Returns the primeExponentQ. |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getPrimeP](RSAMultiPrimePrivateCrtKey.md))`()` Returns the primeP. |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getPrimeQ](RSAMultiPrimePrivateCrtKey.md))`()` Returns the primeQ. |
| --- | --- |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getPublicExponent](RSAMultiPrimePrivateCrtKey.md))`()` Returns the public exponent. |

| Inherited functions ||
|---|---|
| From class [RSAKey](RSAKey.md) |---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BigInteger](../java.math/BigInteger.md)! | [getModulus](RSAKey.md))`()` <br /> Returns the modulus. <br /> | | [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)! | [getParams](RSAKey.md))`()` <br /> Returns the parameters associated with this key. The parameters are optional and may be either explicitly specified or implicitly created during key pair generation. <br /> | ||
| From class [RSAPrivateKey](RSAPrivateKey.md) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BigInteger](../java.math/BigInteger.md)! | [getPrivateExponent](RSAPrivateKey.md))`()` <br /> Returns the private exponent. <br /> | ||

## Constants

### serialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val serialVersionUID: Long
```

**Deprecated:** *A`serialVersionUID`field in an interface is ineffectual. Do not use; no replacement.*

The type fingerprint that is set to indicate serialization compatibility with a previous version of the type. 

 Value: 618058533534628008L

## Public methods

### getCrtCoefficient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCrtCoefficient(): BigInteger!
```

Returns the crtCoefficient.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](../java.math/BigInteger.md)! | the crtCoefficient. |

### getOtherPrimeInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOtherPrimeInfo(): Array<RSAOtherPrimeInfo!>!
```

Returns the otherPrimeInfo or null if there are only two prime factors (p and q).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [RSAOtherPrimeInfo](../java.security.spec/RSAOtherPrimeInfo.md)!>! | the otherPrimeInfo. |

### getPrimeExponentP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimeExponentP(): BigInteger!
```

Returns the primeExponentP.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeExponentP. |

### getPrimeExponentQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimeExponentQ(): BigInteger!
```

Returns the primeExponentQ.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeExponentQ. |

### getPrimeP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimeP(): BigInteger!
```

Returns the primeP.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeP. |

### getPrimeQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimeQ(): BigInteger!
```

Returns the primeQ.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeQ. |

### getPublicExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPublicExponent(): BigInteger!
```

Returns the public exponent.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](../java.math/BigInteger.md)! | the public exponent. |
