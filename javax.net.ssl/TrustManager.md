# TrustManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrustManager

```
interface TrustManager
```

| [javax.net.ssl.TrustManager](../javax/net/ssl/TrustManager.md) |

| Known Direct Subclasses [X509TrustManager](../javax/net/ssl/X509TrustManager.md) |---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [X509TrustManager](../javax/net/ssl/X509TrustManager.md) | Instance of this interface manage which X509 certificates may be used to authenticate the remote side of a secure socket. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [X509ExtendedTrustManager](../javax/net/ssl/X509ExtendedTrustManager.md) |-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------| | [X509ExtendedTrustManager](../javax/net/ssl/X509ExtendedTrustManager.md) | Extensions to the`X509TrustManager`interface to support SSL/TLS connection sensitive trust management. | |
| --- | --- | --- | --- | --- | --- | --- |

This is the base interface for JSSE trust managers.

`TrustManager`s are responsible for managing the trust material that is used when making trust decisions, and for deciding whether credentials presented by a peer should be accepted.

`TrustManager`s are created by either using a`TrustManagerFactory`, or by implementing one of the`TrustManager`subclasses.

## Summary
