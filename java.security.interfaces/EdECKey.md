# EdECKey

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EdECKey

```
interface EdECKey
```

| [java.security.interfaces.EdECKey](../java/security/interfaces/EdECKey.md) |

| Known Direct Subclasses [EdECPrivateKey](../java/security/interfaces/EdECPrivateKey.md), [EdECPublicKey](../java/security/interfaces/EdECPublicKey.md) |----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [EdECPrivateKey](../java/security/interfaces/EdECPrivateKey.md) | An interface for an elliptic curve private key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). | | [EdECPublicKey](../java/security/interfaces/EdECPublicKey.md) | An interface for an elliptic curve public key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An interface for an elliptic curve public/private key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). These keys are distinct from the keys represented by`ECKey`, and they are intended for use with algorithms based on RFC 8032 such as the EdDSA`Signature`algorithm. This interface allows access to the algorithm parameters associated with the key.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [NamedParameterSpec](../java/security/spec/NamedParameterSpec.md)! | [getParams](../java/security/interfaces/EdECKey.md))`()` Returns the algorithm parameters associated with the key. |

## Public methods

### getParams

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParams(): NamedParameterSpec!
```

Returns the algorithm parameters associated with the key.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [NamedParameterSpec](../java/security/spec/NamedParameterSpec.md)! | the associated algorithm parameters. |
