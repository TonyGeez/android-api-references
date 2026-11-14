# ECPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECPublicKey

```
interface ECPublicKey : ECKey, PublicKey
```

| [java.security.interfaces.ECPublicKey](ECPublicKey.md) |

The interface to an elliptic curve (EC) public key.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](ECPublicKey.md) The class fingerprint that is set to indicate serialization compatibility. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ECPoint](../java.security.spec/ECPoint.md)! | [getW](ECPublicKey.md))`()` Returns the public point W. |

| Inherited functions ||
|---|---|
| From class [ECKey](ECKey.md) |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ECParameterSpec](../java.security.spec/ECParameterSpec.md)! | [getParams](ECKey.md))`()` <br /> Returns the domain parameters associated with this key. The domain parameters are either explicitly specified or implicitly created during key generation. <br /> | ||

## Constants

### serialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val serialVersionUID: Long
```

**Deprecated:** *A`serialVersionUID`field in an interface is ineffectual. Do not use; no replacement.*

The class fingerprint that is set to indicate serialization compatibility. 

 Value: -3314988629879632826L

## Public methods

### getW

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getW(): ECPoint!
```

Returns the public point W.

| Return ||
|---------------------------------------------------------------------------------------------|---------------------|
| [ECPoint](../java.security.spec/ECPoint.md)! | the public point W. |
