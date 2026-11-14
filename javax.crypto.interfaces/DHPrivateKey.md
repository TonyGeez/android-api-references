# DHPrivateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DHPrivateKey

```
interface DHPrivateKey : DHKey, PrivateKey
```

| [javax.crypto.interfaces.DHPrivateKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPrivateKey#) |

The interface to a Diffie-Hellman private key.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPrivateKey#serialVersionUID:kotlin.Long) The class fingerprint that is set to indicate serialization compatibility since J2SE 1. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getX](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPrivateKey#getX())`()` Returns the private value,`x`. |

| Inherited functions ||
|---|---|
| From class [DHKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHKey) |------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------| | [DHParameterSpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHParameterSpec.html#)! | [getParams](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHKey#getParams())`()` <br /> Returns the key parameters. <br /> | ||

## Constants

### serialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val serialVersionUID: Long
```

The class fingerprint that is set to indicate serialization compatibility since J2SE 1.4. 

 Value: 2211791113380396553L

## Public methods

### getX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getX(): BigInteger!
```

Returns the private value,`x`.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the private value,`x` |
