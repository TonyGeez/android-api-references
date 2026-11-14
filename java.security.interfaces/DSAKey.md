# DSAKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAKey

```
interface DSAKey
```

| [java.security.interfaces.DSAKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAKey#) |

| Known Direct Subclasses [DSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPrivateKey), [DSAPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPublicKey) |--------------------------------------------------------------------------------------------------------|----------------------------------------------| | [DSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPrivateKey) | The standard interface to a DSA private key. | | [DSAPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPublicKey) | The interface to a DSA public key. | |

The interface to a DSA public or private key. DSA (Digital Signature Algorithm) is defined in NIST's FIPS-186.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DSAParams](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAParams)! | [getParams](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAKey#getParams())`()` Returns the DSA-specific key parameters. |

## Public methods

### getParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParams(): DSAParams!
```

Returns the DSA-specific key parameters. These parameters are never secret.

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------|
| [DSAParams](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAParams)! | the DSA-specific key parameters. |

**See Also**

- [java.security.interfaces.DSAParams](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAParams)
