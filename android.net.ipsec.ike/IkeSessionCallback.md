# IkeSessionCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeSessionCallback

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/IkeSessionCallback "View this page in Java") 
| --- | --- |

```
interface IkeSessionCallback
```

| [android.net.ipsec.ike.IkeSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback#) |

Callback interface for receiving state changes of an [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession).

[IkeSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback#) MUST be unique to each [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession). It is registered when callers are requesting a new [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession). It is automatically unregistered when an [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession) is closed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClosed](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback#onClosed())`()` Called when the [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession) is closed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClosedWithException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback#onClosedWithException(android.net.ipsec.ike.exceptions.IkeException))`(`exception:` ` [IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException)`)` Called if [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession) setup failed or [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession) is closed because of a fatal error. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback#onError(android.net.ipsec.ike.exceptions.IkeException))`(`exception:` ` [IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException)`)` Called if a recoverable error is encountered in an established [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOpened](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback#onOpened(android.net.ipsec.ike.IkeSessionConfiguration))`(`sessionConfiguration:` ` [IkeSessionConfiguration](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration)`)` Called when the [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession) setup succeeds. |

## Public methods

### onClosed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClosed(): Unit
```

Called when the [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession) is closed.

When the closure is caused by a local, fatal error, [onClosedWithException(android.net.ipsec.ike.exceptions.IkeException)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback#onClosedWithException(android.net.ipsec.ike.exceptions.IkeException))will be fired instead of this method. 

### onClosedWithException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onClosedWithException(exception: IkeException): Unit
```

Called if [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession) setup failed or [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession) is closed because of a fatal error.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException):the detailed error information. This value cannot be`null`. |

### onError

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onError(exception: IkeException): Unit
```

Called if a recoverable error is encountered in an established [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession).

This method may be triggered by protocol errors such as an INVALID_IKE_SPI, or by non-protocol errors such as the underlying [android.net.Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) dying.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException):the detailed error information. This value cannot be`null`. |

### onOpened

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onOpened(sessionConfiguration: IkeSessionConfiguration): Unit
```

Called when the [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession) setup succeeds.

This method does not indicate the first Child Session has been setup. Caller MUST refer to the corresponding [ChildSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback) for the Child Session setup result.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionConfiguration` | [IkeSessionConfiguration](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration):the configuration information of [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession) negotiated during IKE setup. This value cannot be`null`. |
