# DSAParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAParameterSpec

```
open class DSAParameterSpec : AlgorithmParameterSpec, DSAParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.DSAParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/DSAParameterSpec#) |

This class specifies the set of parameters used with the DSA algorithm.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DSAParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/DSAParameterSpec#DSAParameterSpec(java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger))`(`p:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `q:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `g:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Creates a new DSAParameterSpec with the specified parameter values. |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getG](https://developer.android.com/reference/kotlin/java/security/spec/DSAParameterSpec#getG())`()` Returns the base`g`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getP](https://developer.android.com/reference/kotlin/java/security/spec/DSAParameterSpec#getP())`()` Returns the prime`p`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getQ](https://developer.android.com/reference/kotlin/java/security/spec/DSAParameterSpec#getQ())`()` Returns the sub-prime`q`. |

## Public constructors

### DSAParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DSAParameterSpec(
    p: BigInteger!, 
    q: BigInteger!, 
    g: BigInteger!)
```

Creates a new DSAParameterSpec with the specified parameter values.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
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
