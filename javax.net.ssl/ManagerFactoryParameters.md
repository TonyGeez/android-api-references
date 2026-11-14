# ManagerFactoryParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ManagerFactoryParameters

```
interface ManagerFactoryParameters
```

| [javax.net.ssl.ManagerFactoryParameters](../javax/net/ssl/ManagerFactoryParameters.md) |

| Known Direct Subclasses [CertPathTrustManagerParameters](../javax/net/ssl/CertPathTrustManagerParameters.md), [KeyStoreBuilderParameters](../javax/net/ssl/KeyStoreBuilderParameters.md) |-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------| | [CertPathTrustManagerParameters](../javax/net/ssl/CertPathTrustManagerParameters.md) | A wrapper for CertPathParameters. | | [KeyStoreBuilderParameters](../javax/net/ssl/KeyStoreBuilderParameters.md) | A parameters object for X509KeyManagers that encapsulates a List of KeyStore. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class is the base interface for providing algorithm-specific information to a KeyManagerFactory or TrustManagerFactory.

In some cases, initialization parameters other than keystores may be needed by a provider. Users of that particular provider are expected to pass an implementation of the appropriate sub-interface of this class as defined by the provider. The provider can then call the specified methods in the`ManagerFactoryParameters`implementation to obtain the needed information.

## Summary
