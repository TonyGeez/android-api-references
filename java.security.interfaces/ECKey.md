# ECKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECKey

```
interface ECKey
```

| [java.security.interfaces.ECKey](ECKey.md) |

| Known Direct Subclasses [ECPrivateKey](ECPrivateKey.md), [ECPublicKey](ECPublicKey.md) |------------------------------------------------------------------------------------------------------|------------------------------------------------------| | [ECPrivateKey](ECPrivateKey.md) | The interface to an elliptic curve (EC) private key. | | [ECPublicKey](ECPublicKey.md) | The interface to an elliptic curve (EC) public key. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The interface to an elliptic curve (EC) key.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ECParameterSpec](../java.security.spec/ECParameterSpec.md)! | [getParams](ECKey.md))`()` Returns the domain parameters associated with this key. |

## Public methods

### getParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParams(): ECParameterSpec!
```

Returns the domain parameters associated with this key. The domain parameters are either explicitly specified or implicitly created during key generation.

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [ECParameterSpec](../java.security.spec/ECParameterSpec.md)! | the associated domain parameters. |
