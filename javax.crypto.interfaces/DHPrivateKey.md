# DHPrivateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DHPrivateKey

```
interface DHPrivateKey : DHKey, PrivateKey
```

| [javax.crypto.interfaces.DHPrivateKey](DHPrivateKey.md) |

The interface to a Diffie-Hellman private key.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](DHPrivateKey.md) The class fingerprint that is set to indicate serialization compatibility since J2SE 1. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](../java.math/BigInteger.md)! | [getX](DHPrivateKey.md))`()` Returns the private value,`x`. |

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
| [BigInteger](../java.math/BigInteger.md)! | the private value,`x` |
