# DHPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DHPublicKeySpec

```
open class DHPublicKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.crypto.spec.DHPublicKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHPublicKeySpec#) |

This class specifies a Diffie-Hellman public key with its associated parameters.

Note that this class does not perform any validation on specified parameters. Thus, the specified values are returned directly even if they are null.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DHPublicKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHPublicKeySpec#DHPublicKeySpec(java.math.BigInteger,%20java.math.BigInteger,%20java.math.BigInteger))`(`y:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `p:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `g:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Constructor that takes a public value `y`, a prime modulus `p`, and a base generator `g`. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getG](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHPublicKeySpec#getG())`()` Returns the base generator `g`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getP](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHPublicKeySpec#getP())`()` Returns the prime modulus `p`. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getY](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHPublicKeySpec#getY())`()` Returns the public value `y`. |

## Public constructors

### DHPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DHPublicKeySpec(
    y: BigInteger!, 
    p: BigInteger!, 
    g: BigInteger!)
```

Constructor that takes a public value `y`, a prime modulus `p`, and a base generator `g`.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `y` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!: public value y |
| `p` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!: prime modulus p |
| `g` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!: base generator g |

## Public methods

### getG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getG(): BigInteger!
```

Returns the base generator `g`.

| Return ||
|------------------------------------------------------------------------------------------|------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the base generator `g` |

### getP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getP(): BigInteger!
```

Returns the prime modulus `p`.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the prime modulus `p` |

### getY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getY(): BigInteger!
```

Returns the public value `y`.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the public value `y` |
