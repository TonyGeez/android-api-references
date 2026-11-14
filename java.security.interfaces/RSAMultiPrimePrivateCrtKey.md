# RSAMultiPrimePrivateCrtKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAMultiPrimePrivateCrtKey

```
interface RSAMultiPrimePrivateCrtKey : RSAPrivateKey
```

| [java.security.interfaces.RSAMultiPrimePrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey#) |

The interface to an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey#serialVersionUID:kotlin.Long) The type fingerprint that is set to indicate serialization compatibility with a previous version of the type. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getCrtCoefficient](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey#getCrtCoefficient())`()` Returns the crtCoefficient. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RSAOtherPrimeInfo](https://developer.android.com/reference/kotlin/java/security/spec/RSAOtherPrimeInfo.html#)!\>! | [getOtherPrimeInfo](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey#getOtherPrimeInfo())`()` Returns the otherPrimeInfo or null if there are only two prime factors (p and q). |
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrimeExponentP](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey#getPrimeExponentP())`()` Returns the primeExponentP. |
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrimeExponentQ](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey#getPrimeExponentQ())`()` Returns the primeExponentQ. |
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrimeP](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey#getPrimeP())`()` Returns the primeP. |
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrimeQ](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey#getPrimeQ())`()` Returns the primeQ. |
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPublicExponent](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey#getPublicExponent())`()` Returns the public exponent. |

| Inherited functions ||
|---|---|
| From class [RSAKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAKey) |---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getModulus](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAKey#getModulus())`()` <br /> Returns the modulus. <br /> | | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)! | [getParams](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAKey#getParams())`()` <br /> Returns the parameters associated with this key. The parameters are optional and may be either explicitly specified or implicitly created during key pair generation. <br /> | ||
| From class [RSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateKey) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrivateExponent](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateKey#getPrivateExponent())`()` <br /> Returns the private exponent. <br /> | ||

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
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the crtCoefficient. |

### getOtherPrimeInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOtherPrimeInfo(): Array<RSAOtherPrimeInfo!>!
```

Returns the otherPrimeInfo or null if there are only two prime factors (p and q).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [RSAOtherPrimeInfo](https://developer.android.com/reference/kotlin/java/security/spec/RSAOtherPrimeInfo.html#)!>! | the otherPrimeInfo. |

### getPrimeExponentP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimeExponentP(): BigInteger!
```

Returns the primeExponentP.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the primeExponentP. |

### getPrimeExponentQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimeExponentQ(): BigInteger!
```

Returns the primeExponentQ.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the primeExponentQ. |

### getPrimeP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimeP(): BigInteger!
```

Returns the primeP.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the primeP. |

### getPrimeQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimeQ(): BigInteger!
```

Returns the primeQ.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the primeQ. |

### getPublicExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPublicExponent(): BigInteger!
```

Returns the public exponent.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the public exponent. |
