# DSAPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAPublicKeySpec

```
open class DSAPublicKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.DSAPublicKeySpec](../java/security/spec/DSAPublicKeySpec.md) |

This class specifies a DSA public key with its associated parameters.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DSAPublicKeySpec](../java/security/spec/DSAPublicKeySpec.md))`(`y:` ` [BigInteger](../java/math/BigInteger.md)!`, `p:` ` [BigInteger](../java/math/BigInteger.md)!`, `q:` ` [BigInteger](../java/math/BigInteger.md)!`, `g:` ` [BigInteger](../java/math/BigInteger.md)!`)` Creates a new DSAPublicKeySpec with the specified parameter values. |

| Public methods ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](../java/math/BigInteger.md)! | [getG](../java/security/spec/DSAPublicKeySpec.md))`()` Returns the base`g`. |
| open [BigInteger](../java/math/BigInteger.md)! | [getP](../java/security/spec/DSAPublicKeySpec.md))`()` Returns the prime`p`. |
| open [BigInteger](../java/math/BigInteger.md)! | [getQ](../java/security/spec/DSAPublicKeySpec.md))`()` Returns the sub-prime`q`. |
| --- | --- |
| open [BigInteger](../java/math/BigInteger.md)! | [getY](../java/security/spec/DSAPublicKeySpec.md))`()` Returns the public key`y`. |

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
| `y` | [BigInteger](../java/math/BigInteger.md)!:the public key. |
| `p` | [BigInteger](../java/math/BigInteger.md)!:the prime. |
| `q` | [BigInteger](../java/math/BigInteger.md)!:the sub-prime. |
| --- | --- |
| `g` | [BigInteger](../java/math/BigInteger.md)!:the base. |

## Public methods

### getG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getG(): BigInteger!
```

Returns the base`g`.

| Return ||
|------------------------------------------------------------------------------------------|--------------|
| [BigInteger](../java/math/BigInteger.md)! | the base`g`. |

### getP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getP(): BigInteger!
```

Returns the prime`p`.

| Return ||
|------------------------------------------------------------------------------------------|---------------|
| [BigInteger](../java/math/BigInteger.md)! | the prime`p`. |

### getQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQ(): BigInteger!
```

Returns the sub-prime`q`.

| Return ||
|------------------------------------------------------------------------------------------|-------------------|
| [BigInteger](../java/math/BigInteger.md)! | the sub-prime`q`. |

### getY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getY(): BigInteger!
```

Returns the public key`y`.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](../java/math/BigInteger.md)! | the public key`y`. |
