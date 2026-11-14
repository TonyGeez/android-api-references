# IkeSessionConnectionInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeSessionConnectionInfo

Kotlin | [Java](https://developer.android.com/reference/android/net/ipsec/ike/IkeSessionConnectionInfo "View this page in Java") 
| --- | --- |

```
class IkeSessionConnectionInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ipsec.ike.IkeSessionConnectionInfo](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConnectionInfo#) |

IkeSessionConnectionInfo represents the connection information of an [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession).

Connection information includes IP addresses of both the IKE client and server and the network being used.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IkeSessionConnectionInfo](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConnectionInfo#IkeSessionConnectionInfo(java.net.InetAddress,%20java.net.InetAddress,%20android.net.Network))`(`localAddress:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)`, `remoteAddress:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)`, `network:` ` [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#)`)` Construct an instance of [IkeSessionConnectionInfo](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConnectionInfo#). |

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) | [getLocalAddress](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConnectionInfo#getLocalAddress())`()` Returns the local IP address for the underlying [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) being used. |
| [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) | [getNetwork](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConnectionInfo#getNetwork())`()` Returns the underlying [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) being used. |
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) | [getRemoteAddress](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConnectionInfo#getRemoteAddress())`()` Returns the remote IP address for the underlying [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) being used. |
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

Construct an instance of [IkeSessionConnectionInfo](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConnectionInfo#).

Except for testing, IKE library users normally do not instantiate [IkeSessionConnectionInfo](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConnectionInfo#) themselves but instead get a reference via [IkeSessionConfiguration](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration) or [IkeSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback)

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------|
| `localAddress` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#): This value cannot be `null`. |
| `remoteAddress` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#): This value cannot be `null`. |
| `network` | [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#): This value cannot be `null`. |
| --- | --- |

## Public methods

### getLocalAddress

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocalAddress(): InetAddress
```

Returns the local IP address for the underlying [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) being used.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) | the local IP address. This value cannot be `null`. |

### getNetwork

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetwork(): Network
```

Returns the underlying [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) being used.

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) | the underlying [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) that carries all IKE traffic. This value cannot be `null`. |

### getRemoteAddress

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRemoteAddress(): InetAddress
```

Returns the remote IP address for the underlying [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) being used.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) | the remote IP address. This value cannot be `null`. |
