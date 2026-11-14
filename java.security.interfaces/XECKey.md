# XECKey

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XECKey

```
interface XECKey
```

| [java.security.interfaces.XECKey](../java/security/interfaces/XECKey.md) |

| Known Direct Subclasses [XECPrivateKey](../java/security/interfaces/XECPrivateKey.md), [XECPublicKey](../java/security/interfaces/XECPublicKey.md) |--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------| | [XECPrivateKey](../java/security/interfaces/XECPrivateKey.md) | An interface for an elliptic curve private key as defined by RFC 7748. | | [XECPublicKey](../java/security/interfaces/XECPublicKey.md) | An interface for an elliptic curve public key as defined by RFC 7748. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An interface for an elliptic curve public/private key as defined by RFC 7748. These keys are distinct from the keys represented by`ECKey`, and they are intended for use with algorithms based on RFC 7748 such as the XDH`KeyAgreement`algorithm. This interface allows access to the algorithm parameters associated with the key.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | [getParams](../java/security/interfaces/XECKey.md))`()` Returns the algorithm parameters associated with the key. |

## Public methods

### getParams

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParams(): AlgorithmParameterSpec!
```

Returns the algorithm parameters associated with the key.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | the associated algorithm parameters |
