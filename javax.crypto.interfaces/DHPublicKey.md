# DHPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DHPublicKey

```
interface DHPublicKey : DHKey, PublicKey
```

| [javax.crypto.interfaces.DHPublicKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPublicKey#) |

The interface to a Diffie-Hellman public key.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPublicKey#serialVersionUID:kotlin.Long) The class fingerprint that is set to indicate serialization compatibility since J2SE 1. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getY](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPublicKey#getY())`()` Returns the public value,`y`. |

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

 Value: -6628103563352519193L

## Public methods

### getY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getY(): BigInteger!
```

Returns the public value,`y`.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the public value,`y` |
