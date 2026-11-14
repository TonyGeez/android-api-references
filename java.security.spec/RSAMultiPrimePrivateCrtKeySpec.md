# RSAMultiPrimePrivateCrtKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAMultiPrimePrivateCrtKeySpec

```
open class RSAMultiPrimePrivateCrtKeySpec : RSAPrivateKeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.spec.RSAPrivateKeySpec](RSAPrivateKeySpec.md) ||
| | ↳ | [java.security.spec.RSAMultiPrimePrivateCrtKeySpec](RSAMultiPrimePrivateCrtKeySpec.md) |

This class specifies an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard using the Chinese Remainder Theorem (CRT) information values for efficiency.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RSAMultiPrimePrivateCrtKeySpec](RSAMultiPrimePrivateCrtKeySpec.md))`(`modulus:` ` [BigInteger](../java.math/BigInteger.md)!`, `publicExponent:` ` [BigInteger](../java.math/BigInteger.md)!`, `privateExponent:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeP:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeQ:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeExponentP:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeExponentQ:` ` [BigInteger](../java.math/BigInteger.md)!`, `crtCoefficient:` ` [BigInteger](../java.math/BigInteger.md)!`, `otherPrimeInfo:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [RSAOtherPrimeInfo](RSAOtherPrimeInfo.md)!>!`)` Creates a new`RSAMultiPrimePrivateCrtKeySpec`. |
| [RSAMultiPrimePrivateCrtKeySpec](RSAMultiPrimePrivateCrtKeySpec.md))`(`modulus:` ` [BigInteger](../java.math/BigInteger.md)!`, `publicExponent:` ` [BigInteger](../java.math/BigInteger.md)!`, `privateExponent:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeP:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeQ:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeExponentP:` ` [BigInteger](../java.math/BigInteger.md)!`, `primeExponentQ:` ` [BigInteger](../java.math/BigInteger.md)!`, `crtCoefficient:` ` [BigInteger](../java.math/BigInteger.md)!`, `otherPrimeInfo:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [RSAOtherPrimeInfo](RSAOtherPrimeInfo.md)!>!`, `keyParams:` ` [AlgorithmParameterSpec](AlgorithmParameterSpec.md)!`)` Creates a new`RSAMultiPrimePrivateCrtKeySpec`with additional key parameters. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](../java.math/BigInteger.md)! | [getCrtCoefficient](RSAMultiPrimePrivateCrtKeySpec.md))`()` Returns the crtCoefficient. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RSAOtherPrimeInfo](RSAOtherPrimeInfo.md)!\>! | [getOtherPrimeInfo](RSAMultiPrimePrivateCrtKeySpec.md))`()` Returns a copy of the otherPrimeInfo or null if there are only two prime factors (p and q). |
| open [BigInteger](../java.math/BigInteger.md)! | [getPrimeExponentP](RSAMultiPrimePrivateCrtKeySpec.md))`()` Returns the primeExponentP. |
| --- | --- |
| open [BigInteger](../java.math/BigInteger.md)! | [getPrimeExponentQ](RSAMultiPrimePrivateCrtKeySpec.md))`()` Returns the primeExponentQ. |
| open [BigInteger](../java.math/BigInteger.md)! | [getPrimeP](RSAMultiPrimePrivateCrtKeySpec.md))`()` Returns the primeP. |
| open [BigInteger](../java.math/BigInteger.md)! | [getPrimeQ](RSAMultiPrimePrivateCrtKeySpec.md))`()` Returns the primeQ. |
| --- | --- |
| open [BigInteger](../java.math/BigInteger.md)! | [getPublicExponent](RSAMultiPrimePrivateCrtKeySpec.md))`()` Returns the public exponent. |

| Inherited functions ||
|---|---|
| From class [RSAPrivateKeySpec](RSAPrivateKeySpec.md) |---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BigInteger](../java.math/BigInteger.md)! | [getModulus](RSAPrivateKeySpec.md))`()` <br /> Returns the modulus. <br /> | | [AlgorithmParameterSpec](AlgorithmParameterSpec.md)! | [getParams](RSAPrivateKeySpec.md))`()` <br /> Returns the parameters associated with this key, may be null if not present. <br /> | | [BigInteger](../java.math/BigInteger.md)! | [getPrivateExponent](RSAPrivateKeySpec.md))`()` <br /> Returns the private exponent. <br /> | ||

## Public constructors

### RSAMultiPrimePrivateCrtKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAMultiPrimePrivateCrtKeySpec(
    modulus: BigInteger!, 
    publicExponent: BigInteger!, 
    privateExponent: BigInteger!, 
    primeP: BigInteger!, 
    primeQ: BigInteger!, 
    primeExponentP: BigInteger!, 
    primeExponentQ: BigInteger!, 
    crtCoefficient: BigInteger!, 
    otherPrimeInfo: Array<RSAOtherPrimeInfo!>!)
```

Creates a new`RSAMultiPrimePrivateCrtKeySpec`.

Note that the contents of`otherPrimeInfo`are copied to protect against subsequent modification when constructing this object.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `modulus` | [BigInteger](../java.math/BigInteger.md)!:the modulus n |
| `publicExponent` | [BigInteger](../java.math/BigInteger.md)!:the public exponent e |
| `privateExponent` | [BigInteger](../java.math/BigInteger.md)!:the private exponent d |
| --- | --- |
| `primeP` | [BigInteger](../java.math/BigInteger.md)!:the prime factor p of n |
| `primeQ` | [BigInteger](../java.math/BigInteger.md)!:the prime factor q of n |
| `primeExponentP` | [BigInteger](../java.math/BigInteger.md)!:this is d mod (p-1) |
| --- | --- |
| `primeExponentQ` | [BigInteger](../java.math/BigInteger.md)!:this is d mod (q-1) |
| `crtCoefficient` | [BigInteger](../java.math/BigInteger.md)!:the Chinese Remainder Theorem coefficient q-1 mod p |
| `otherPrimeInfo` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RSAOtherPrimeInfo](RSAOtherPrimeInfo.md)!\>!:triplets of the rest of primes, null can be specified if there are only two prime factors (p and q) |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if any of the specified parameters with the exception of`otherPrimeInfo`is null |
| `java.lang.IllegalArgumentException` | if an empty, i.e. 0-length,`otherPrimeInfo`is specified |

### RSAMultiPrimePrivateCrtKeySpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAMultiPrimePrivateCrtKeySpec(
    modulus: BigInteger!, 
    publicExponent: BigInteger!, 
    privateExponent: BigInteger!, 
    primeP: BigInteger!, 
    primeQ: BigInteger!, 
    primeExponentP: BigInteger!, 
    primeExponentQ: BigInteger!, 
    crtCoefficient: BigInteger!, 
    otherPrimeInfo: Array<RSAOtherPrimeInfo!>!, 
    keyParams: AlgorithmParameterSpec!)
```

Creates a new`RSAMultiPrimePrivateCrtKeySpec`with additional key parameters.

Note that the contents of`otherPrimeInfo`are copied to protect against subsequent modification when constructing this object.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `modulus` | [BigInteger](../java.math/BigInteger.md)!:the modulus n |
| `publicExponent` | [BigInteger](../java.math/BigInteger.md)!:the public exponent e |
| `privateExponent` | [BigInteger](../java.math/BigInteger.md)!:the private exponent d |
| --- | --- |
| `primeP` | [BigInteger](../java.math/BigInteger.md)!:the prime factor p of n |
| `primeQ` | [BigInteger](../java.math/BigInteger.md)!:the prime factor q of n |
| `primeExponentP` | [BigInteger](../java.math/BigInteger.md)!:this is d mod (p-1) |
| --- | --- |
| `primeExponentQ` | [BigInteger](../java.math/BigInteger.md)!:this is d mod (q-1) |
| `crtCoefficient` | [BigInteger](../java.math/BigInteger.md)!:the Chinese Remainder Theorem coefficient q-1 mod p |
| `otherPrimeInfo` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RSAOtherPrimeInfo](RSAOtherPrimeInfo.md)!\>!:triplets of the rest of primes, null can be specified if there are only two prime factors (p and q) |
| --- | --- |
| `keyParams` | [AlgorithmParameterSpec](AlgorithmParameterSpec.md)!:the parameters associated with key |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if any of the specified parameters with the exception of`otherPrimeInfo`and`keyParams`is null |
| `java.lang.IllegalArgumentException` | if an empty, i.e. 0-length,`otherPrimeInfo`is specified |

## Public methods

### getCrtCoefficient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCrtCoefficient(): BigInteger!
```

Returns the crtCoefficient.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](../java.math/BigInteger.md)! | the crtCoefficient. |

### getOtherPrimeInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOtherPrimeInfo(): Array<RSAOtherPrimeInfo!>!
```

Returns a copy of the otherPrimeInfo or null if there are only two prime factors (p and q).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [RSAOtherPrimeInfo](RSAOtherPrimeInfo.md)!>! | the otherPrimeInfo. Returns a new array each time this method is called. |

### getPrimeExponentP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeExponentP(): BigInteger!
```

Returns the primeExponentP.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeExponentP. |

### getPrimeExponentQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeExponentQ(): BigInteger!
```

Returns the primeExponentQ.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeExponentQ. |

### getPrimeP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeP(): BigInteger!
```

Returns the primeP.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeP. |

### getPrimeQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimeQ(): BigInteger!
```

Returns the primeQ.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeQ. |

### getPublicExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicExponent(): BigInteger!
```

Returns the public exponent.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](../java.math/BigInteger.md)! | the public exponent. |
