# ChildSessionCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChildSessionCallback

Kotlin| [Java](../android/net/ipsec/ike/ChildSessionCallback.md) 
| --- | --- |

```
interface ChildSessionCallback
```

| [android.net.ipsec.ike.ChildSessionCallback](../android/net/ipsec/ike/ChildSessionCallback.md) |

Callback interface for receiving state changes of a Child Session.

[ChildSessionCallback](../android/net/ipsec/ike/ChildSessionCallback.md) MUST be unique to each Child Session. It is registered when callers are requesting a new Child Session. It is automatically unregistered when a Child Session or the parent IKE Session is closed.

[ChildSessionCallback](../android/net/ipsec/ike/ChildSessionCallback.md) s are also used for identifying Child Sessions. It is required when a caller wants to delete a specific Child Session.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClosed](../android/net/ipsec/ike/ChildSessionCallback.md))`()` Called when the Child Session is closed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClosedWithException](../android/net/ipsec/ike/ChildSessionCallback.md))`(`exception:` ` [IkeException](../android/net/ipsec/ike/exceptions/IkeException.md)`)` Called if the Child Session setup failed or Child Session is closed because of a fatal error. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onIpSecTransformCreated](../android/net/ipsec/ike/ChildSessionCallback.md))`(`ipSecTransform:` ` [IpSecTransform](../android/net/IpSecTransform.md)`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an [IpSecTransform](../android/net/IpSecTransform.md) is created by this Child Session. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onIpSecTransformDeleted](../android/net/ipsec/ike/ChildSessionCallback.md))`(`ipSecTransform:` ` [IpSecTransform](../android/net/IpSecTransform.md)`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an [IpSecTransform](../android/net/IpSecTransform.md) is deleted by this Child Session. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOpened](../android/net/ipsec/ike/ChildSessionCallback.md))`(`sessionConfiguration:` ` [ChildSessionConfiguration](../android/net/ipsec/ike/ChildSessionConfiguration.md)`)` Called when the Child Session setup succeeds. |

## Public methods

### onClosed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClosed(): Unit
```

Called when the Child Session is closed.

This method will be called immediately after [onIpSecTransformDeleted(android.net.IpSecTransform,int)](../android/net/ipsec/ike/ChildSessionCallback.md))for the deleted IPsec SA pair is fired.

When the closure is caused by a local, fatal error, [onClosedWithException(android.net.ipsec.ike.exceptions.IkeException)](../android/net/ipsec/ike/ChildSessionCallback.md))will be fired instead of this method. 

### onClosedWithException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onClosedWithException(exception: IkeException): Unit
```

Called if the Child Session setup failed or Child Session is closed because of a fatal error.

This method will be called immediately after [onIpSecTransformDeleted(android.net.IpSecTransform,int)](../android/net/ipsec/ike/ChildSessionCallback.md))for the deleted IPsec SA pair is fired.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [IkeException](../android/net/ipsec/ike/exceptions/IkeException.md):the detailed error information. This value cannot be`null`. |

### onIpSecTransformCreated

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onIpSecTransformCreated(
    ipSecTransform: IpSecTransform, 
    direction: Int
): Unit
```

Called when an [IpSecTransform](../android/net/IpSecTransform.md) is created by this Child Session.

This method is fired when a Child Session is created or rekeyed.

The [IpSecTransform](../android/net/IpSecTransform.md) must be applied to relevant sockets or interfaces when this method is called; traffic may otherwise flow over the socket or interface unprotected.

As this method is fired on an executor, there is an inherent race condition during rekeys where traffic may be routed through the old transforms while the remote has switched to using the new set of transforms.

To avoid the initial startup race condition where the transforms have not yet been applied, the [onOpened(android.net.ipsec.ike.ChildSessionConfiguration)](../android/net/ipsec/ike/ChildSessionCallback.md))callback should be used as the authoritative signal that the socket or tunnel is ready, as it is fired after both transforms have had a chance to be applied.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ipSecTransform` | [IpSecTransform](../android/net/IpSecTransform.md):the created [IpSecTransform](../android/net/IpSecTransform.md). This value cannot be`null`. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the direction of this [IpSecTransform](../android/net/IpSecTransform.md). Value is [android.net.IpSecManager#DIRECTION_IN](../android/net/IpSecManager.md), or [android.net.IpSecManager#DIRECTION_OUT](../android/net/IpSecManager.md) |

### onIpSecTransformDeleted

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onIpSecTransformDeleted(
    ipSecTransform: IpSecTransform, 
    direction: Int
): Unit
```

Called when an [IpSecTransform](../android/net/IpSecTransform.md) is deleted by this Child Session.

This method is fired when a Child Session is closed or a Child Session has deleted old IPsec SA during rekey. When this method is fired due to Child Session closure, it will be followed by [onClosed()](../android/net/ipsec/ike/ChildSessionCallback.md))or [onClosedWithException(android.net.ipsec.ike.exceptions.IkeException)](../android/net/ipsec/ike/ChildSessionCallback.md)).

Users SHOULD remove the [IpSecTransform](../android/net/IpSecTransform.md) from the socket or interface when this method is called. Otherwise the IPsec traffic protected by this [IpSecTransform](../android/net/IpSecTransform.md) will be discarded.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ipSecTransform` | [IpSecTransform](../android/net/IpSecTransform.md):the deleted [IpSecTransform](../android/net/IpSecTransform.md). This value cannot be`null`. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the direction of this [IpSecTransform](../android/net/IpSecTransform.md). Value is [android.net.IpSecManager#DIRECTION_IN](../android/net/IpSecManager.md), or [android.net.IpSecManager#DIRECTION_OUT](../android/net/IpSecManager.md) |

### onOpened

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onOpened(sessionConfiguration: ChildSessionConfiguration): Unit
```

Called when the Child Session setup succeeds.

This method will be called immediately after [onIpSecTransformCreated(android.net.IpSecTransform,int)](../android/net/ipsec/ike/ChildSessionCallback.md))for the created IPsec SA pair is fired.

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionConfiguration` | [ChildSessionConfiguration](../android/net/ipsec/ike/ChildSessionConfiguration.md):the [ChildSessionConfiguration](../android/net/ipsec/ike/ChildSessionConfiguration.md) of Child Session negotiated during Child creation. This value cannot be`null`. |
