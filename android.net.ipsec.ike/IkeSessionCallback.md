# IkeSessionCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeSessionCallback

Kotlin| [Java](../android/net/ipsec/ike/IkeSessionCallback.md) 
| --- | --- |

```
interface IkeSessionCallback
```

| [android.net.ipsec.ike.IkeSessionCallback](../android/net/ipsec/ike/IkeSessionCallback.md) |

Callback interface for receiving state changes of an [IkeSession](../android/net/ipsec/ike/IkeSession.md).

[IkeSessionCallback](../android/net/ipsec/ike/IkeSessionCallback.md) MUST be unique to each [IkeSession](../android/net/ipsec/ike/IkeSession.md). It is registered when callers are requesting a new [IkeSession](../android/net/ipsec/ike/IkeSession.md). It is automatically unregistered when an [IkeSession](../android/net/ipsec/ike/IkeSession.md) is closed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClosed](../android/net/ipsec/ike/IkeSessionCallback.md))`()` Called when the [IkeSession](../android/net/ipsec/ike/IkeSession.md) is closed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClosedWithException](../android/net/ipsec/ike/IkeSessionCallback.md))`(`exception:` ` [IkeException](../android/net/ipsec/ike/exceptions/IkeException.md)`)` Called if [IkeSession](../android/net/ipsec/ike/IkeSession.md) setup failed or [IkeSession](../android/net/ipsec/ike/IkeSession.md) is closed because of a fatal error. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](../android/net/ipsec/ike/IkeSessionCallback.md))`(`exception:` ` [IkeException](../android/net/ipsec/ike/exceptions/IkeException.md)`)` Called if a recoverable error is encountered in an established [IkeSession](../android/net/ipsec/ike/IkeSession.md). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOpened](../android/net/ipsec/ike/IkeSessionCallback.md))`(`sessionConfiguration:` ` [IkeSessionConfiguration](../android/net/ipsec/ike/IkeSessionConfiguration.md)`)` Called when the [IkeSession](../android/net/ipsec/ike/IkeSession.md) setup succeeds. |

## Public methods

### onClosed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClosed(): Unit
```

Called when the [IkeSession](../android/net/ipsec/ike/IkeSession.md) is closed.

When the closure is caused by a local, fatal error, [onClosedWithException(android.net.ipsec.ike.exceptions.IkeException)](../android/net/ipsec/ike/IkeSessionCallback.md))will be fired instead of this method. 

### onClosedWithException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onClosedWithException(exception: IkeException): Unit
```

Called if [IkeSession](../android/net/ipsec/ike/IkeSession.md) setup failed or [IkeSession](../android/net/ipsec/ike/IkeSession.md) is closed because of a fatal error.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [IkeException](../android/net/ipsec/ike/exceptions/IkeException.md):the detailed error information. This value cannot be`null`. |

### onError

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onError(exception: IkeException): Unit
```

Called if a recoverable error is encountered in an established [IkeSession](../android/net/ipsec/ike/IkeSession.md).

This method may be triggered by protocol errors such as an INVALID_IKE_SPI, or by non-protocol errors such as the underlying [android.net.Network](../android/net/Network.md) dying.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [IkeException](../android/net/ipsec/ike/exceptions/IkeException.md):the detailed error information. This value cannot be`null`. |

### onOpened

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onOpened(sessionConfiguration: IkeSessionConfiguration): Unit
```

Called when the [IkeSession](../android/net/ipsec/ike/IkeSession.md) setup succeeds.

This method does not indicate the first Child Session has been setup. Caller MUST refer to the corresponding [ChildSessionCallback](../android/net/ipsec/ike/ChildSessionCallback.md) for the Child Session setup result.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionConfiguration` | [IkeSessionConfiguration](../android/net/ipsec/ike/IkeSessionConfiguration.md):the configuration information of [IkeSession](../android/net/ipsec/ike/IkeSession.md) negotiated during IKE setup. This value cannot be`null`. |
