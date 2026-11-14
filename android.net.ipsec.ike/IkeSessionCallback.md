# IkeSessionCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeSessionCallback

Kotlin| [Java](IkeSessionCallback.md) 
| --- | --- |

```
interface IkeSessionCallback
```

| [android.net.ipsec.ike.IkeSessionCallback](IkeSessionCallback.md) |

Callback interface for receiving state changes of an [IkeSession](IkeSession.md).

[IkeSessionCallback](IkeSessionCallback.md) MUST be unique to each [IkeSession](IkeSession.md). It is registered when callers are requesting a new [IkeSession](IkeSession.md). It is automatically unregistered when an [IkeSession](IkeSession.md) is closed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClosed](IkeSessionCallback.md))`()` Called when the [IkeSession](IkeSession.md) is closed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClosedWithException](IkeSessionCallback.md))`(`exception:` ` [IkeException](../android.net.ipsec.ike.exceptions/IkeException.md)`)` Called if [IkeSession](IkeSession.md) setup failed or [IkeSession](IkeSession.md) is closed because of a fatal error. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](IkeSessionCallback.md))`(`exception:` ` [IkeException](../android.net.ipsec.ike.exceptions/IkeException.md)`)` Called if a recoverable error is encountered in an established [IkeSession](IkeSession.md). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOpened](IkeSessionCallback.md))`(`sessionConfiguration:` ` [IkeSessionConfiguration](IkeSessionConfiguration.md)`)` Called when the [IkeSession](IkeSession.md) setup succeeds. |

## Public methods

### onClosed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClosed(): Unit
```

Called when the [IkeSession](IkeSession.md) is closed.

When the closure is caused by a local, fatal error, [onClosedWithException(android.net.ipsec.ike.exceptions.IkeException)](IkeSessionCallback.md))will be fired instead of this method. 

### onClosedWithException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onClosedWithException(exception: IkeException): Unit
```

Called if [IkeSession](IkeSession.md) setup failed or [IkeSession](IkeSession.md) is closed because of a fatal error.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [IkeException](../android.net.ipsec.ike.exceptions/IkeException.md):the detailed error information. This value cannot be`null`. |

### onError

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onError(exception: IkeException): Unit
```

Called if a recoverable error is encountered in an established [IkeSession](IkeSession.md).

This method may be triggered by protocol errors such as an INVALID_IKE_SPI, or by non-protocol errors such as the underlying [android.net.Network](../android.net/Network.md) dying.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [IkeException](../android.net.ipsec.ike.exceptions/IkeException.md):the detailed error information. This value cannot be`null`. |

### onOpened

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onOpened(sessionConfiguration: IkeSessionConfiguration): Unit
```

Called when the [IkeSession](IkeSession.md) setup succeeds.

This method does not indicate the first Child Session has been setup. Caller MUST refer to the corresponding [ChildSessionCallback](ChildSessionCallback.md) for the Child Session setup result.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionConfiguration` | [IkeSessionConfiguration](IkeSessionConfiguration.md):the configuration information of [IkeSession](IkeSession.md) negotiated during IKE setup. This value cannot be`null`. |
