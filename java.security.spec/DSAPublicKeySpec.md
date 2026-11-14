# DSAPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAPublicKeySpec

```
open class DSAPublicKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.DSAPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/DSAPublicKeySpec#) |

This class specifies a DSA public key with its associated parameters.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DSAPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/DSAPublicKeySpec#DSAPublicKeySpec(java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger))`(`y:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `p:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `q:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `g:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Creates a new DSAPublicKeySpec with the specified parameter values. |

| Public methods ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getG](https://developer.android.com/reference/kotlin/java/security/spec/DSAPublicKeySpec#getG())`()` Returns the base`g`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getP](https://developer.android.com/reference/kotlin/java/security/spec/DSAPublicKeySpec#getP())`()` Returns the prime`p`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getQ](https://developer.android.com/reference/kotlin/java/security/spec/DSAPublicKeySpec#getQ())`()` Returns the sub-prime`q`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getY](https://developer.android.com/reference/kotlin/java/security/spec/DSAPublicKeySpec#getY())`()` Returns the public key`y`. |

## Public constructors

### DSAPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DSAPublicKeySpec(
    y: BigInteger!, 
    p: BigInteger!, 
    q: BigInteger!, 
    g: BigInteger!)
```

Creates a new DSAPublicKeySpec with the specified parameter values.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `y` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the public key. |
| `p` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the prime. |
| `q` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the sub-prime. |
| `g` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the base. |

## Public methods

### getG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getG(): BigInteger!
```

Returns the base`g`.

| Return ||
|------------------------------------------------------------------------------------------|--------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the base`g`. |

### getP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getP(): BigInteger!
```

Returns the prime`p`.

| Return ||
|------------------------------------------------------------------------------------------|---------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the prime`p`. |

### getQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQ(): BigInteger!
```

Returns the sub-prime`q`.

| Return ||
|------------------------------------------------------------------------------------------|-------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the sub-prime`q`. |

### getY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getY(): BigInteger!
```

Returns the public key`y`.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the public key`y`. |
