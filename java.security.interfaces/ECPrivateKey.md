# ECPrivateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECPrivateKey

```
interface ECPrivateKey : ECKey, PrivateKey
```

| [java.security.interfaces.ECPrivateKey](ECPrivateKey.md) |

The interface to an elliptic curve (EC) private key.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](ECPrivateKey.md) The class fingerprint that is set to indicate serialization compatibility. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](../java.math/BigInteger.md)! | [getS](ECPrivateKey.md))`()` Returns the private value S. |

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

 Value: -7896394956925609184L

## Public methods

### getS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getS(): BigInteger!
```

Returns the private value S.

| Return ||
|------------------------------------------------------------------------------------------|----------------------|
| [BigInteger](../java.math/BigInteger.md)! | the private value S. |
