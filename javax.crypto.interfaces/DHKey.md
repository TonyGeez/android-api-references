# DHKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DHKey

```
interface DHKey
```

| [javax.crypto.interfaces.DHKey](../javax/crypto/interfaces/DHKey.md) |

| Known Direct Subclasses [DHPrivateKey](../javax/crypto/interfaces/DHPrivateKey.md), [DHPublicKey](../javax/crypto/interfaces/DHPublicKey.md) |-----------------------------------------------------------------------------------------------------|------------------------------------------------| | [DHPrivateKey](../javax/crypto/interfaces/DHPrivateKey.md) | The interface to a Diffie-Hellman private key. | | [DHPublicKey](../javax/crypto/interfaces/DHPublicKey.md) | The interface to a Diffie-Hellman public key. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The interface to a Diffie-Hellman key.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DHParameterSpec](../javax/crypto/spec/DHParameterSpec.md)! | [getParams](../javax/crypto/interfaces/DHKey.md))`()` Returns the key parameters. |

## Public methods

### getParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParams(): DHParameterSpec!
```

Returns the key parameters.

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------|
| [DHParameterSpec](../javax/crypto/spec/DHParameterSpec.md)! | the key parameters |
