# DSAKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAKey

```
interface DSAKey
```

| [java.security.interfaces.DSAKey](DSAKey.md) |

| Known Direct Subclasses [DSAPrivateKey](DSAPrivateKey.md), [DSAPublicKey](DSAPublicKey.md) |--------------------------------------------------------------------------------------------------------|----------------------------------------------| | [DSAPrivateKey](DSAPrivateKey.md) | The standard interface to a DSA private key. | | [DSAPublicKey](DSAPublicKey.md) | The interface to a DSA public key. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The interface to a DSA public or private key. DSA (Digital Signature Algorithm) is defined in NIST's FIPS-186.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DSAParams](DSAParams.md)! | [getParams](DSAKey.md))`()` Returns the DSA-specific key parameters. |

## Public methods

### getParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParams(): DSAParams!
```

Returns the DSA-specific key parameters. These parameters are never secret.

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------|
| [DSAParams](DSAParams.md)! | the DSA-specific key parameters. |

**See Also**

- [java.security.interfaces.DSAParams](DSAParams.md)
