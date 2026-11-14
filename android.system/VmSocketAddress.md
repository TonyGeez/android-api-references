# VmSocketAddress

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VmSocketAddress

Kotlin| [Java](../android/system/VmSocketAddress.md) 
| --- | --- |

```
class VmSocketAddress : SocketAddress
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.net.SocketAddress](../java/net/SocketAddress.md) ||
| | ↳ | [android.system.VmSocketAddress](../android/system/VmSocketAddress.md) |

A virtio-vsock address [VmSocketAddress](../android/system/VmSocketAddress.md).

virtio-vsock socket address, linux specific.

[VmSocketAddress](../android/system/VmSocketAddress.md) corresponds to`struct sockaddr_vm`in bionic/libc/kernel/uapi/linux/vm_sockets.h.

Currently virtio-vsock is used as a generic purpose pipe in emulators to talk to the host. Most I/O operations using this address via [Os](../android/system/Os.md) class will require additional permissions to talk to the host.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [VmSocketAddress](../android/system/VmSocketAddress.md))`(`svmPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `svmCid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new instance of VmSocketAddress. |

| Public methods ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSvmCid](../android/system/VmSocketAddress.md))`()` Returns the value of the svmCid field |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSvmPort](../android/system/VmSocketAddress.md))`()` Returns the value of the svmPort field |

## Public constructors

### VmSocketAddress

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VmSocketAddress(
    svmPort: Int, 
    svmCid: Int)
```

Creates a new instance of VmSocketAddress.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `svmPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The svmPort field value, see [OsConstants.VMADDR_PORT_ANY](../android/system/OsConstants.md). |
| `svmCid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The svmCid field value, see OsConstants.VMADDR_CID_\* for VMADDR_CID_\* values. |

## Public methods

### getSvmCid

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSvmCid(): Int
```

Returns the value of the svmCid field 

### getSvmPort

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSvmPort(): Int
```

Returns the value of the svmPort field
