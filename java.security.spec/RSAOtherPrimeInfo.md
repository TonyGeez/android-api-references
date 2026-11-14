# RSAOtherPrimeInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAOtherPrimeInfo

```
open class RSAOtherPrimeInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.RSAOtherPrimeInfo](https://developer.android.com/reference/kotlin/java/security/spec/RSAOtherPrimeInfo#) |

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
| [RSAOtherPrimeInfo](https://developer.android.com/reference/kotlin/java/security/spec/RSAOtherPrimeInfo#RSAOtherPrimeInfo(java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger))`(`prime:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `primeExponent:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `crtCoefficient:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Creates a new`RSAOtherPrimeInfo`given the prime, primeExponent, and crtCoefficient as defined in PKCS#1. |

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getCrtCoefficient](https://developer.android.com/reference/kotlin/java/security/spec/RSAOtherPrimeInfo#getCrtCoefficient())`()` Returns the prime's crtCoefficient. |
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getExponent](https://developer.android.com/reference/kotlin/java/security/spec/RSAOtherPrimeInfo#getExponent())`()` Returns the prime's exponent. |
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getPrime](https://developer.android.com/reference/kotlin/java/security/spec/RSAOtherPrimeInfo#getPrime())`()` Returns the prime. |

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
| `prime` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the prime factor of n. |
| `primeExponent` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the exponent. |
| `crtCoefficient` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the Chinese Remainder Theorem coefficient. |

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
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the crtCoefficient. |

### getExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExponent(): BigInteger!
```

Returns the prime's exponent.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the primeExponent. |

### getPrime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrime(): BigInteger!
```

Returns the prime.

| Return ||
|------------------------------------------------------------------------------------------|------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the prime. |
