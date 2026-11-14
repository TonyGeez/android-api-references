# DSAParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAParameterSpec

```
open class DSAParameterSpec : AlgorithmParameterSpec, DSAParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.DSAParameterSpec](DSAParameterSpec.md) |

This class specifies the set of parameters used with the DSA algorithm.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DSAParameterSpec](DSAParameterSpec.md))`(`p:` ` [BigInteger](../java.math/BigInteger.md)!`, `q:` ` [BigInteger](../java.math/BigInteger.md)!`, `g:` ` [BigInteger](../java.math/BigInteger.md)!`)` Creates a new DSAParameterSpec with the specified parameter values. |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](../java.math/BigInteger.md)! | [getG](DSAParameterSpec.md))`()` Returns the base`g`. |
| open [BigInteger](../java.math/BigInteger.md)! | [getP](DSAParameterSpec.md))`()` Returns the prime`p`. |
| open [BigInteger](../java.math/BigInteger.md)! | [getQ](DSAParameterSpec.md))`()` Returns the sub-prime`q`. |
| --- | --- |

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
| `p` | [BigInteger](../java.math/BigInteger.md)!:the prime. |
| `q` | [BigInteger](../java.math/BigInteger.md)!:the sub-prime. |
| `g` | [BigInteger](../java.math/BigInteger.md)!:the base. |
| --- | --- |

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
