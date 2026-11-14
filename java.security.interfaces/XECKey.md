# XECKey

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XECKey

```
interface XECKey
```

| [java.security.interfaces.XECKey](https://developer.android.com/reference/kotlin/java/security/interfaces/XECKey#) |

| Known Direct Subclasses [XECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/XECPrivateKey), [XECPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/XECPublicKey) |--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------| | [XECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/XECPrivateKey) | An interface for an elliptic curve private key as defined by RFC 7748. | | [XECPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/XECPublicKey) | An interface for an elliptic curve public key as defined by RFC 7748. | |

An interface for an elliptic curve public/private key as defined by RFC 7748. These keys are distinct from the keys represented by`ECKey`, and they are intended for use with algorithms based on RFC 7748 such as the XDH`KeyAgreement`algorithm. This interface allows access to the algorithm parameters associated with the key.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)! | [getParams](https://developer.android.com/reference/kotlin/java/security/interfaces/XECKey#getParams())`()` Returns the algorithm parameters associated with the key. |

## Public methods

### getParams

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParams(): AlgorithmParameterSpec!
```

Returns the algorithm parameters associated with the key.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)! | the associated algorithm parameters |
