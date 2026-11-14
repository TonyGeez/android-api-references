# IkeNetworkLostException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeNetworkLostException

Kotlin| [Java](IkeNetworkLostException.md) 
| --- | --- |

```
class IkeNetworkLostException : IkeNonProtocolException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](IkeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeNonProtocolException](IkeNonProtocolException.md) ||
| | | | | ↳ | [android.net.ipsec.ike.exceptions.IkeNetworkLostException](IkeNetworkLostException.md) |

IkeNetworkLostException is returned to the caller via [android.net.ipsec.ike.IkeSessionCallback#onError(android.net.ipsec.ike.exceptions.IkeException)](../android.net.ipsec.ike/IkeSessionCallback.md))if the underlying Network for the was lost with no alternatives.

This Exception corresponds to [android.net.ConnectivityManager.NetworkCallback#onLost(android.net.Network)](../android/net/ConnectivityManager.NetworkCallback.md))being invoked for the specified underlying Network.

When the caller receives this Exception, they must either:

- set a new underlying Network for the corresponding IkeSession (MOBIKE must be enabled and the IKE Session must have started with a caller-configured Network), or
- wait for a new underlying Network to become available (MOBIKE must be enabled and the IKE Session must be tracking the System default Network), or
 - Note: if the maximum retransmission time is encountered while waiting, the IKE Session will close. If this occurs, the caller will be notified via [android.net.ipsec.ike.IkeSessionCallback#onClosedWithException(android.net.ipsec.ike.exceptions.IkeException)](../android.net.ipsec.ike/IkeSessionCallback.md)).
- close the corresponding IkeSession.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IkeNetworkLostException](IkeNetworkLostException.md))`(`network:` ` [Network](../android.net/Network.md)`)` Constructs an IkeNetworkLostException to indicate the specified Network was lost. |

| Public methods ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Network](../android.net/Network.md) | [getNetwork](IkeNetworkLostException.md))`()` Returns the IkeSession's underlying Network that was lost. |

## Public constructors

### IkeNetworkLostException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IkeNetworkLostException(network: Network)
```

Constructs an IkeNetworkLostException to indicate the specified Network was lost.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `network` | [Network](../android.net/Network.md):This value cannot be`null`. |

## Public methods

### getNetwork

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetwork(): Network
```

Returns the IkeSession's underlying Network that was lost.

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------|
| [Network](../android.net/Network.md) | This value cannot be`null`. |
