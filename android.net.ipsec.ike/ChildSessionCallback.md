# ChildSessionCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChildSessionCallback

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/ChildSessionCallback "View this page in Java") 

```
interface ChildSessionCallback
```

| [android.net.ipsec.ike.ChildSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#) |

Callback interface for receiving state changes of a Child Session.

[ChildSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#) MUST be unique to each Child Session. It is registered when callers are requesting a new Child Session. It is automatically unregistered when a Child Session or the parent IKE Session is closed.

[ChildSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#) s are also used for identifying Child Sessions. It is required when a caller wants to delete a specific Child Session.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClosed](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onClosed())`()` Called when the Child Session is closed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClosedWithException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onClosedWithException(android.net.ipsec.ike.exceptions.IkeException))`(`exception:` ` [IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException)`)` Called if the Child Session setup failed or Child Session is closed because of a fatal error. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onIpSecTransformCreated](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onIpSecTransformCreated(android.net.IpSecTransform,%20kotlin.Int))`(`ipSecTransform:` ` [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#)`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#) is created by this Child Session. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onIpSecTransformDeleted](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onIpSecTransformDeleted(android.net.IpSecTransform,%20kotlin.Int))`(`ipSecTransform:` ` [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#)`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#) is deleted by this Child Session. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOpened](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onOpened(android.net.ipsec.ike.ChildSessionConfiguration))`(`sessionConfiguration:` ` [ChildSessionConfiguration](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionConfiguration)`)` Called when the Child Session setup succeeds. |

## Public methods

### onClosed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClosed(): Unit
```

Called when the Child Session is closed.

This method will be called immediately after [onIpSecTransformDeleted(android.net.IpSecTransform,int)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onIpSecTransformDeleted(android.net.IpSecTransform,%20kotlin.Int))for the deleted IPsec SA pair is fired.

When the closure is caused by a local, fatal error, [onClosedWithException(android.net.ipsec.ike.exceptions.IkeException)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onClosedWithException(android.net.ipsec.ike.exceptions.IkeException))will be fired instead of this method. 

### onClosedWithException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onClosedWithException(exception: IkeException): Unit
```

Called if the Child Session setup failed or Child Session is closed because of a fatal error.

This method will be called immediately after [onIpSecTransformDeleted(android.net.IpSecTransform,int)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onIpSecTransformDeleted(android.net.IpSecTransform,%20kotlin.Int))for the deleted IPsec SA pair is fired.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException):the detailed error information. This value cannot be`null`. |

### onIpSecTransformCreated

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onIpSecTransformCreated(
    ipSecTransform: IpSecTransform, 
    direction: Int
): Unit
```

Called when an [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#) is created by this Child Session.

This method is fired when a Child Session is created or rekeyed.

The [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#) must be applied to relevant sockets or interfaces when this method is called; traffic may otherwise flow over the socket or interface unprotected.

As this method is fired on an executor, there is an inherent race condition during rekeys where traffic may be routed through the old transforms while the remote has switched to using the new set of transforms.

To avoid the initial startup race condition where the transforms have not yet been applied, the [onOpened(android.net.ipsec.ike.ChildSessionConfiguration)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onOpened(android.net.ipsec.ike.ChildSessionConfiguration))callback should be used as the authoritative signal that the socket or tunnel is ready, as it is fired after both transforms have had a chance to be applied.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ipSecTransform` | [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#):the created [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#). This value cannot be`null`. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the direction of this [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#). Value is [android.net.IpSecManager#DIRECTION_IN](https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#DIRECTION_IN:kotlin.Int), or [android.net.IpSecManager#DIRECTION_OUT](https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#DIRECTION_OUT:kotlin.Int) |

### onIpSecTransformDeleted

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onIpSecTransformDeleted(
    ipSecTransform: IpSecTransform, 
    direction: Int
): Unit
```

Called when an [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#) is deleted by this Child Session.

This method is fired when a Child Session is closed or a Child Session has deleted old IPsec SA during rekey. When this method is fired due to Child Session closure, it will be followed by [onClosed()](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onClosed())or [onClosedWithException(android.net.ipsec.ike.exceptions.IkeException)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onClosedWithException(android.net.ipsec.ike.exceptions.IkeException)).

Users SHOULD remove the [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#) from the socket or interface when this method is called. Otherwise the IPsec traffic protected by this [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#) will be discarded.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ipSecTransform` | [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#):the deleted [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#). This value cannot be`null`. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the direction of this [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#). Value is [android.net.IpSecManager#DIRECTION_IN](https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#DIRECTION_IN:kotlin.Int), or [android.net.IpSecManager#DIRECTION_OUT](https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#DIRECTION_OUT:kotlin.Int) |

### onOpened

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onOpened(sessionConfiguration: ChildSessionConfiguration): Unit
```

Called when the Child Session setup succeeds.

This method will be called immediately after [onIpSecTransformCreated(android.net.IpSecTransform,int)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onIpSecTransformCreated(android.net.IpSecTransform,%20kotlin.Int))for the created IPsec SA pair is fired.

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionConfiguration` | [ChildSessionConfiguration](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionConfiguration):the [ChildSessionConfiguration](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionConfiguration) of Child Session negotiated during Child creation. This value cannot be`null`. |
