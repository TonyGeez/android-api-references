# DHKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DHKey

```
interface DHKey
```

| [javax.crypto.interfaces.DHKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHKey#) |

| Known Direct Subclasses [DHPrivateKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPrivateKey), [DHPublicKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPublicKey) |-----------------------------------------------------------------------------------------------------|------------------------------------------------| | [DHPrivateKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPrivateKey) | The interface to a Diffie-Hellman private key. | | [DHPublicKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPublicKey) | The interface to a Diffie-Hellman public key. | |

The interface to a Diffie-Hellman key.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DHParameterSpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHParameterSpec.html#)! | [getParams](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHKey#getParams())`()` Returns the key parameters. |

## Public methods

### getParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParams(): DHParameterSpec!
```

Returns the key parameters.

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------|
| [DHParameterSpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/DHParameterSpec.html#)! | the key parameters |
