# ECPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECPublicKey

```
interface ECPublicKey : ECKey, PublicKey
```

| [java.security.interfaces.ECPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPublicKey#) |

The interface to an elliptic curve (EC) public key.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPublicKey#serialVersionUID:kotlin.Long) The class fingerprint that is set to indicate serialization compatibility. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint.html#)! | [getW](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPublicKey#getW())`()` Returns the public point W. |

| Inherited functions ||
|---|---|
| From class [ECKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECKey) |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec.html#)! | [getParams](https://developer.android.com/reference/kotlin/java/security/interfaces/ECKey#getParams())`()` <br /> Returns the domain parameters associated with this key. The domain parameters are either explicitly specified or implicitly created during key generation. <br /> | ||

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
| [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint.html#)! | the public point W. |
