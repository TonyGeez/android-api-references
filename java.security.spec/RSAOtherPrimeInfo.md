# RSAOtherPrimeInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAOtherPrimeInfo

```
open class RSAOtherPrimeInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.RSAOtherPrimeInfo](../java/security/spec/RSAOtherPrimeInfo.md) |

This class represents the triplet (prime, exponent, and coefficient) inside RSA's OtherPrimeInfo structure, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard. The ASN.1 syntax of RSA's OtherPrimeInfo is as follows: 

```kotlin
OtherPrimeInfo ::= SEQUENCE {
    prime        INTEGER,
    exponent     INTEGER,
    coefficient  INTEGER
  }
 
  
```

<br />

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RSAOtherPrimeInfo](../java/security/spec/RSAOtherPrimeInfo.md))`(`prime:` ` [BigInteger](../java/math/BigInteger.md)!`, `primeExponent:` ` [BigInteger](../java/math/BigInteger.md)!`, `crtCoefficient:` ` [BigInteger](../java/math/BigInteger.md)!`)` Creates a new`RSAOtherPrimeInfo`given the prime, primeExponent, and crtCoefficient as defined in PKCS#1. |

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BigInteger](../java/math/BigInteger.md)! | [getCrtCoefficient](../java/security/spec/RSAOtherPrimeInfo.md))`()` Returns the prime's crtCoefficient. |
| [BigInteger](../java/math/BigInteger.md)! | [getExponent](../java/security/spec/RSAOtherPrimeInfo.md))`()` Returns the prime's exponent. |
| [BigInteger](../java/math/BigInteger.md)! | [getPrime](../java/security/spec/RSAOtherPrimeInfo.md))`()` Returns the prime. |
| --- | --- |

## Public constructors

### RSAOtherPrimeInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RSAOtherPrimeInfo(
    prime: BigInteger!, 
    primeExponent: BigInteger!, 
    crtCoefficient: BigInteger!)
```

Creates a new`RSAOtherPrimeInfo`given the prime, primeExponent, and crtCoefficient as defined in PKCS#1.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `prime` | [BigInteger](../java/math/BigInteger.md)!:the prime factor of n. |
| `primeExponent` | [BigInteger](../java/math/BigInteger.md)!:the exponent. |
| `crtCoefficient` | [BigInteger](../java/math/BigInteger.md)!:the Chinese Remainder Theorem coefficient. |
| --- | --- |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if any of the parameters, i.e.`prime`,`primeExponent`,`crtCoefficient`, is null. |

## Public methods

### getCrtCoefficient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCrtCoefficient(): BigInteger!
```

Returns the prime's crtCoefficient.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](../java/math/BigInteger.md)! | the crtCoefficient. |

### getExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExponent(): BigInteger!
```

Returns the prime's exponent.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](../java/math/BigInteger.md)! | the primeExponent. |

### getPrime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrime(): BigInteger!
```

Returns the prime.

| Return ||
|------------------------------------------------------------------------------------------|------------|
| [BigInteger](../java/math/BigInteger.md)! | the prime. |
