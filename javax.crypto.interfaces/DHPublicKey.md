# DHPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DHPublicKey

```
interface DHPublicKey : DHKey, PublicKey
```

| [javax.crypto.interfaces.DHPublicKey](DHPublicKey.md) |

The interface to a Diffie-Hellman public key.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](DHPublicKey.md) The class fingerprint that is set to indicate serialization compatibility since J2SE 1. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](../java.math/BigInteger.md)! | [getY](DHPublicKey.md))`()` Returns the public value,`y`. |

| Inherited functions ||
|---|---|
| From class [DHKey](DHKey.md) |------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------| | [DHParameterSpec](../javax.crypto.spec/DHParameterSpec.md)! | [getParams](DHKey.md))`()` <br /> Returns the key parameters. <br /> | ||

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
| [BigInteger](../java.math/BigInteger.md)! | the public value,`y` |
