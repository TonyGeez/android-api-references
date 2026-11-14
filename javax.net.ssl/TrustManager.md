# TrustManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrustManager

```
interface TrustManager
```

| [javax.net.ssl.TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManager#) |

| Known Direct Subclasses [X509TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager) |---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [X509TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager) | Instance of this interface manage which X509 certificates may be used to authenticate the remote side of a secure socket. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [X509ExtendedTrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager) |-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------| | [X509ExtendedTrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager) | Extensions to the`X509TrustManager`interface to support SSL/TLS connection sensitive trust management. | |
| --- | --- | --- | --- | --- | --- | --- |

This is the base interface for JSSE trust managers.

`TrustManager`s are responsible for managing the trust material that is used when making trust decisions, and for deciding whether credentials presented by a peer should be accepted.

`TrustManager`s are created by either using a`TrustManagerFactory`, or by implementing one of the`TrustManager`subclasses.

## Summary
