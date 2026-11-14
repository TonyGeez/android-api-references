# ECKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECKey

```
interface ECKey
```

| [java.security.interfaces.ECKey](../java/security/interfaces/ECKey.md) |

| Known Direct Subclasses [ECPrivateKey](../java/security/interfaces/ECPrivateKey.md), [ECPublicKey](../java/security/interfaces/ECPublicKey.md) |------------------------------------------------------------------------------------------------------|------------------------------------------------------| | [ECPrivateKey](../java/security/interfaces/ECPrivateKey.md) | The interface to an elliptic curve (EC) private key. | | [ECPublicKey](../java/security/interfaces/ECPublicKey.md) | The interface to an elliptic curve (EC) public key. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The interface to an elliptic curve (EC) key.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ECParameterSpec](../java/security/spec/ECParameterSpec.md)! | [getParams](../java/security/interfaces/ECKey.md))`()` Returns the domain parameters associated with this key. |

## Public methods

### getParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParams(): ECParameterSpec!
```

Returns the domain parameters associated with this key. The domain parameters are either explicitly specified or implicitly created during key generation.

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [ECParameterSpec](../java/security/spec/ECParameterSpec.md)! | the associated domain parameters. |
