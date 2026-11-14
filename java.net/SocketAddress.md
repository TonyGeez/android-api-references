# SocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketAddress

```
abstract class SocketAddress : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.SocketAddress](SocketAddress.md) |

| Known Direct Subclasses [InetSocketAddress](InetSocketAddress.md), [VmSocketAddress](../android.system/VmSocketAddress.md) |--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InetSocketAddress](InetSocketAddress.md) | This class implements an IP Socket Address (IP address + port number) It can also be a pair (hostname + port number), in which case an attempt will be made to resolve the hostname. | | [VmSocketAddress](../android.system/VmSocketAddress.md) | A virtio-vsock address [VmSocketAddress](../android.system/VmSocketAddress.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class represents a Socket Address with no protocol attachment. As an abstract class, it is meant to be subclassed with a specific, protocol dependent, implementation.

It provides an immutable object used by sockets for binding, connecting, or as returned values.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SocketAddress](SocketAddress.md))`()` Constructor for subclasses to call. |

## Public constructors

### SocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SocketAddress()
```

Constructor for subclasses to call.
