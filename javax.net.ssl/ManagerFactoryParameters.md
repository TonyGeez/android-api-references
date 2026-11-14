# ManagerFactoryParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ManagerFactoryParameters

```
interface ManagerFactoryParameters
```

| [javax.net.ssl.ManagerFactoryParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/ManagerFactoryParameters#) |

| Known Direct Subclasses [CertPathTrustManagerParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/CertPathTrustManagerParameters), [KeyStoreBuilderParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyStoreBuilderParameters) |-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------| | [CertPathTrustManagerParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/CertPathTrustManagerParameters) | A wrapper for CertPathParameters. | | [KeyStoreBuilderParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyStoreBuilderParameters) | A parameters object for X509KeyManagers that encapsulates a List of KeyStore. | |

This class is the base interface for providing algorithm-specific information to a KeyManagerFactory or TrustManagerFactory.

In some cases, initialization parameters other than keystores may be needed by a provider. Users of that particular provider are expected to pass an implementation of the appropriate sub-interface of this class as defined by the provider. The provider can then call the specified methods in the`ManagerFactoryParameters`implementation to obtain the needed information.

## Summary
