# ECKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECKey

```
interface ECKey
```

| [java.security.interfaces.ECKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECKey#) |

| Known Direct Subclasses [ECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPrivateKey), [ECPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPublicKey) |------------------------------------------------------------------------------------------------------|------------------------------------------------------| | [ECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPrivateKey) | The interface to an elliptic curve (EC) private key. | | [ECPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPublicKey) | The interface to an elliptic curve (EC) public key. | |

The interface to an elliptic curve (EC) key.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec.html#)! | [getParams](https://developer.android.com/reference/kotlin/java/security/interfaces/ECKey#getParams())`()` Returns the domain parameters associated with this key. |

## Public methods

### getParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParams(): ECParameterSpec!
```

Returns the domain parameters associated with this key. The domain parameters are either explicitly specified or implicitly created during key generation.

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec.html#)! | the associated domain parameters. |
