# DHPrivateKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DHPrivateKeySpec

```
open class DHPrivateKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.DHPrivateKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHPrivateKeySpec#) |

This class specifies a Diffie-Hellman private key with its associated parameters.

Note that this class does not perform any validation on specified parameters. Thus, the specified values are returned directly even if they are null.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DHPrivateKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHPrivateKeySpec#DHPrivateKeySpec(java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger))`(`x:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `p:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `g:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Constructor that takes a private value`x`, a prime modulus`p`, and a base generator`g`. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getG](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHPrivateKeySpec#getG())`()` Returns the base generator`g`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getP](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHPrivateKeySpec#getP())`()` Returns the prime modulus`p`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getX](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHPrivateKeySpec#getX())`()` Returns the private value`x`. |
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
| `x` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:private value x |
| `p` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:prime modulus p |
| `g` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:base generator g |
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
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the base generator`g` |

### getP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getP(): BigInteger!
```

Returns the prime modulus`p`.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the prime modulus`p` |

### getX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getX(): BigInteger!
```

Returns the private value`x`.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the private value`x` |
