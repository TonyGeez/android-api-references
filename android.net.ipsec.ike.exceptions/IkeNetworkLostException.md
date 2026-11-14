# IkeNetworkLostException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeNetworkLostException

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/exceptions/IkeNetworkLostException "View this page in Java") 

```
class IkeNetworkLostException : IkeNonProtocolException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException) |||
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeNonProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNonProtocolException) ||
| | | | | ↳ | [android.net.ipsec.ike.exceptions.IkeNetworkLostException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNetworkLostException#) |

IkeNetworkLostException is returned to the caller via [android.net.ipsec.ike.IkeSessionCallback#onError(android.net.ipsec.ike.exceptions.IkeException)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#onError(android.net.ipsec.ike.exceptions.IkeException))if the underlying Network for the was lost with no alternatives.

This Exception corresponds to [android.net.ConnectivityManager.NetworkCallback#onLost(android.net.Network)](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback.html#onLost(android.net.Network))being invoked for the specified underlying Network.

When the caller receives this Exception, they must either:

- set a new underlying Network for the corresponding IkeSession (MOBIKE must be enabled and the IKE Session must have started with a caller-configured Network), or
- wait for a new underlying Network to become available (MOBIKE must be enabled and the IKE Session must be tracking the System default Network), or
 - Note: if the maximum retransmission time is encountered while waiting, the IKE Session will close. If this occurs, the caller will be notified via [android.net.ipsec.ike.IkeSessionCallback#onClosedWithException(android.net.ipsec.ike.exceptions.IkeException)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#onClosedWithException(android.net.ipsec.ike.exceptions.IkeException)).
- close the corresponding IkeSession.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IkeNetworkLostException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNetworkLostException#IkeNetworkLostException(android.net.Network))`(`network:` ` [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#)`)` Constructs an IkeNetworkLostException to indicate the specified Network was lost. |

| Public methods ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) | [getNetwork](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNetworkLostException#getNetwork())`()` Returns the IkeSession's underlying Network that was lost. |

## Public constructors

### IkeNetworkLostException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IkeNetworkLostException(network: Network)
```

Constructs an IkeNetworkLostException to indicate the specified Network was lost.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `network` | [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#):This value cannot be`null`. |

## Public methods

### getNetwork

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetwork(): Network
```

Returns the IkeSession's underlying Network that was lost.

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------|
| [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) | This value cannot be`null`. |
