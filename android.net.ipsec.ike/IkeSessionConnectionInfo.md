# IkeSessionConnectionInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeSessionConnectionInfo

Kotlin | [Java](../android/net/ipsec/ike/IkeSessionConnectionInfo.md) 
| --- | --- |

```
class IkeSessionConnectionInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ipsec.ike.IkeSessionConnectionInfo](../android/net/ipsec/ike/IkeSessionConnectionInfo.md) |

IkeSessionConnectionInfo represents the connection information of an [IkeSession](../android/net/ipsec/ike/IkeSession.md).

Connection information includes IP addresses of both the IKE client and server and the network being used.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IkeSessionConnectionInfo](../android/net/ipsec/ike/IkeSessionConnectionInfo.md))`(`localAddress:` ` [InetAddress](../java/net/InetAddress.md)`, `remoteAddress:` ` [InetAddress](../java/net/InetAddress.md)`, `network:` ` [Network](../android/net/Network.md)`)` Construct an instance of [IkeSessionConnectionInfo](../android/net/ipsec/ike/IkeSessionConnectionInfo.md). |

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [InetAddress](../java/net/InetAddress.md) | [getLocalAddress](../android/net/ipsec/ike/IkeSessionConnectionInfo.md))`()` Returns the local IP address for the underlying [Network](../android/net/Network.md) being used. |
| [Network](../android/net/Network.md) | [getNetwork](../android/net/ipsec/ike/IkeSessionConnectionInfo.md))`()` Returns the underlying [Network](../android/net/Network.md) being used. |
| [InetAddress](../java/net/InetAddress.md) | [getRemoteAddress](../android/net/ipsec/ike/IkeSessionConnectionInfo.md))`()` Returns the remote IP address for the underlying [Network](../android/net/Network.md) being used. |
| --- | --- |

## Public constructors

### IkeSessionConnectionInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IkeSessionConnectionInfo(
    localAddress: InetAddress, 
    remoteAddress: InetAddress, 
    network: Network)
```

Construct an instance of [IkeSessionConnectionInfo](../android/net/ipsec/ike/IkeSessionConnectionInfo.md).

Except for testing, IKE library users normally do not instantiate [IkeSessionConnectionInfo](../android/net/ipsec/ike/IkeSessionConnectionInfo.md) themselves but instead get a reference via [IkeSessionConfiguration](../android/net/ipsec/ike/IkeSessionConfiguration.md) or [IkeSessionCallback](../android/net/ipsec/ike/IkeSessionCallback.md)

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------|
| `localAddress` | [InetAddress](../java/net/InetAddress.md): This value cannot be `null`. |
| `remoteAddress` | [InetAddress](../java/net/InetAddress.md): This value cannot be `null`. |
| `network` | [Network](../android/net/Network.md): This value cannot be `null`. |
| --- | --- |

## Public methods

### getLocalAddress

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocalAddress(): InetAddress
```

Returns the local IP address for the underlying [Network](../android/net/Network.md) being used.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------|
| [InetAddress](../java/net/InetAddress.md) | the local IP address. This value cannot be `null`. |

### getNetwork

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetwork(): Network
```

Returns the underlying [Network](../android/net/Network.md) being used.

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Network](../android/net/Network.md) | the underlying [Network](../android/net/Network.md) that carries all IKE traffic. This value cannot be `null`. |

### getRemoteAddress

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRemoteAddress(): InetAddress
```

Returns the remote IP address for the underlying [Network](../android/net/Network.md) being used.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [InetAddress](../java/net/InetAddress.md) | the remote IP address. This value cannot be `null`. |
