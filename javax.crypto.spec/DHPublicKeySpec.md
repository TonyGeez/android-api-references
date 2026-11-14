# DHPublicKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DHPublicKeySpec

```
open class DHPublicKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.DHPublicKeySpec](DHPublicKeySpec.md) |

This class specifies a Diffie-Hellman public key with its associated parameters.

Note that this class does not perform any validation on specified parameters. Thus, the specified values are returned directly even if they are null.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DHPublicKeySpec](DHPublicKeySpec.md))`(`y:` ` [BigInteger](../java.math/BigInteger.md)!`, `p:` ` [BigInteger](../java.math/BigInteger.md)!`, `g:` ` [BigInteger](../java.math/BigInteger.md)!`)` Constructor that takes a public value `y`, a prime modulus `p`, and a base generator `g`. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](../java.math/BigInteger.md)! | [getG](DHPublicKeySpec.md))`()` Returns the base generator `g`. |
| open [BigInteger](../java.math/BigInteger.md)! | [getP](DHPublicKeySpec.md))`()` Returns the prime modulus `p`. |
| open [BigInteger](../java.math/BigInteger.md)! | [getY](DHPublicKeySpec.md))`()` Returns the public value `y`. |
| --- | --- |

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
| `y` | [BigInteger](../java.math/BigInteger.md)!: public value y |
| `p` | [BigInteger](../java.math/BigInteger.md)!: prime modulus p |
| `g` | [BigInteger](../java.math/BigInteger.md)!: base generator g |
| --- | --- |

## Public methods

### getG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getG(): BigInteger!
```

Returns the base generator `g`.

| Return ||
|------------------------------------------------------------------------------------------|------------------------|
| [BigInteger](../java.math/BigInteger.md)! | the base generator `g` |

### getP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getP(): BigInteger!
```

Returns the prime modulus `p`.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------|
| [BigInteger](../java.math/BigInteger.md)! | the prime modulus `p` |

### getY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getY(): BigInteger!
```

Returns the public value `y`.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](../java.math/BigInteger.md)! | the public value `y` |
