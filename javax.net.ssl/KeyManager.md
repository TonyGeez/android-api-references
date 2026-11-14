# KeyManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyManager

```
interface KeyManager
```

| [javax.net.ssl.KeyManager](KeyManager.md) |

| Known Direct Subclasses [X509KeyManager](X509KeyManager.md) |-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------| | [X509KeyManager](X509KeyManager.md) | Instances of this interface manage which X509 certificate-based key pairs are used to authenticate the local side of a secure socket. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [X509ExtendedKeyManager](X509ExtendedKeyManager.md) |---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [X509ExtendedKeyManager](X509ExtendedKeyManager.md) | Abstract class that provides for extension of the X509KeyManager interface. | |
| --- | --- | --- | --- | --- | --- | --- |

This is the base interface for JSSE key managers.

`KeyManager`s are responsible for managing the key material which is used to authenticate the local SSLSocket to its peer. If no key material is available, the socket will be unable to present authentication credentials.

`KeyManager`s are created by either using a`KeyManagerFactory`, or by implementing one of the`KeyManager`subclasses.

## Summary
