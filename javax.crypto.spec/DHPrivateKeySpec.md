# DHPrivateKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DHPrivateKeySpec

```
open class DHPrivateKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.DHPrivateKeySpec](DHPrivateKeySpec.md) |

This class specifies a Diffie-Hellman private key with its associated parameters.

Note that this class does not perform any validation on specified parameters. Thus, the specified values are returned directly even if they are null.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DHPrivateKeySpec](DHPrivateKeySpec.md))`(`x:` ` [BigInteger](../java.math/BigInteger.md)!`, `p:` ` [BigInteger](../java.math/BigInteger.md)!`, `g:` ` [BigInteger](../java.math/BigInteger.md)!`)` Constructor that takes a private value`x`, a prime modulus`p`, and a base generator`g`. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](../java.math/BigInteger.md)! | [getG](DHPrivateKeySpec.md))`()` Returns the base generator`g`. |
| open [BigInteger](../java.math/BigInteger.md)! | [getP](DHPrivateKeySpec.md))`()` Returns the prime modulus`p`. |
| open [BigInteger](../java.math/BigInteger.md)! | [getX](DHPrivateKeySpec.md))`()` Returns the private value`x`. |
| --- | --- |

## Public constructors

### DHPrivateKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DHPrivateKeySpec(
    x: BigInteger!, 
    p: BigInteger!, 
    g: BigInteger!)
```

Constructor that takes a private value`x`, a prime modulus`p`, and a base generator`g`.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `x` | [BigInteger](../java.math/BigInteger.md)!:private value x |
| `p` | [BigInteger](../java.math/BigInteger.md)!:prime modulus p |
| `g` | [BigInteger](../java.math/BigInteger.md)!:base generator g |
| --- | --- |

## Public methods

### getG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getG(): BigInteger!
```

Returns the base generator`g`.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------|
| [BigInteger](../java.math/BigInteger.md)! | the base generator`g` |

### getP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getP(): BigInteger!
```

Returns the prime modulus`p`.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](../java.math/BigInteger.md)! | the prime modulus`p` |

### getX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getX(): BigInteger!
```

Returns the private value`x`.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](../java.math/BigInteger.md)! | the private value`x` |
