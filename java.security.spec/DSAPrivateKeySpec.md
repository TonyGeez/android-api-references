# DSAPrivateKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAPrivateKeySpec

```
open class DSAPrivateKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.DSAPrivateKeySpec](DSAPrivateKeySpec.md) |

This class specifies a DSA private key with its associated parameters.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DSAPrivateKeySpec](DSAPrivateKeySpec.md))`(`x:` ` [BigInteger](../java.math/BigInteger.md)!`, `p:` ` [BigInteger](../java.math/BigInteger.md)!`, `q:` ` [BigInteger](../java.math/BigInteger.md)!`, `g:` ` [BigInteger](../java.math/BigInteger.md)!`)` Creates a new DSAPrivateKeySpec with the specified parameter values. |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](../java.math/BigInteger.md)! | [getG](DSAPrivateKeySpec.md))`()` Returns the base`g`. |
| open [BigInteger](../java.math/BigInteger.md)! | [getP](DSAPrivateKeySpec.md))`()` Returns the prime`p`. |
| open [BigInteger](../java.math/BigInteger.md)! | [getQ](DSAPrivateKeySpec.md))`()` Returns the sub-prime`q`. |
| --- | --- |
| open [BigInteger](../java.math/BigInteger.md)! | [getX](DSAPrivateKeySpec.md))`()` Returns the private key`x`. |

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
| `x` | [BigInteger](../java.math/BigInteger.md)!:the private key. |
| `p` | [BigInteger](../java.math/BigInteger.md)!:the prime. |
| `q` | [BigInteger](../java.math/BigInteger.md)!:the sub-prime. |
| --- | --- |
| `g` | [BigInteger](../java.math/BigInteger.md)!:the base. |

## Public methods

### getG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getG(): BigInteger!
```

Returns the base`g`.

| Return ||
|------------------------------------------------------------------------------------------|--------------|
| [BigInteger](../java.math/BigInteger.md)! | the base`g`. |

### getP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getP(): BigInteger!
```

Returns the prime`p`.

| Return ||
|------------------------------------------------------------------------------------------|---------------|
| [BigInteger](../java.math/BigInteger.md)! | the prime`p`. |

### getQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQ(): BigInteger!
```

Returns the sub-prime`q`.

| Return ||
|------------------------------------------------------------------------------------------|-------------------|
| [BigInteger](../java.math/BigInteger.md)! | the sub-prime`q`. |

### getX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getX(): BigInteger!
```

Returns the private key`x`.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](../java.math/BigInteger.md)! | the private key`x`. |
