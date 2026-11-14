# DSAPrivateKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAPrivateKeySpec

```
open class DSAPrivateKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.DSAPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/DSAPrivateKeySpec#) |

This class specifies a DSA private key with its associated parameters.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DSAPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/DSAPrivateKeySpec#DSAPrivateKeySpec(java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger))`(`x:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `p:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `q:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `g:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Creates a new DSAPrivateKeySpec with the specified parameter values. |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getG](https://developer.android.com/reference/kotlin/java/security/spec/DSAPrivateKeySpec#getG())`()` Returns the base`g`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getP](https://developer.android.com/reference/kotlin/java/security/spec/DSAPrivateKeySpec#getP())`()` Returns the prime`p`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getQ](https://developer.android.com/reference/kotlin/java/security/spec/DSAPrivateKeySpec#getQ())`()` Returns the sub-prime`q`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getX](https://developer.android.com/reference/kotlin/java/security/spec/DSAPrivateKeySpec#getX())`()` Returns the private key`x`. |

## Public constructors

### DSAPrivateKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DSAPrivateKeySpec(
    x: BigInteger!, 
    p: BigInteger!, 
    q: BigInteger!, 
    g: BigInteger!)
```

Creates a new DSAPrivateKeySpec with the specified parameter values.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `x` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the private key. |
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

### getX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getX(): BigInteger!
```

Returns the private key`x`.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the private key`x`. |
