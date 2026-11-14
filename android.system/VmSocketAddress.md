# VmSocketAddress

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VmSocketAddress

Kotlin| [Java](https://developer.android.com/reference/android/system/VmSocketAddress "View this page in Java") 
| --- | --- |

```
class VmSocketAddress : SocketAddress
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.net.SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#) ||
| | ↳ | [android.system.VmSocketAddress](https://developer.android.com/reference/kotlin/android/system/VmSocketAddress#) |

A virtio-vsock address [VmSocketAddress](https://developer.android.com/reference/kotlin/android/system/VmSocketAddress#).

virtio-vsock socket address, linux specific.

[VmSocketAddress](https://developer.android.com/reference/kotlin/android/system/VmSocketAddress#) corresponds to`struct sockaddr_vm`in bionic/libc/kernel/uapi/linux/vm_sockets.h.

Currently virtio-vsock is used as a generic purpose pipe in emulators to talk to the host. Most I/O operations using this address via [Os](https://developer.android.com/reference/kotlin/android/system/Os) class will require additional permissions to talk to the host.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [VmSocketAddress](https://developer.android.com/reference/kotlin/android/system/VmSocketAddress#VmSocketAddress(kotlin.Int,%20kotlin.Int))`(`svmPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `svmCid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new instance of VmSocketAddress. |

| Public methods ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSvmCid](https://developer.android.com/reference/kotlin/android/system/VmSocketAddress#getSvmCid())`()` Returns the value of the svmCid field |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSvmPort](https://developer.android.com/reference/kotlin/android/system/VmSocketAddress#getSvmPort())`()` Returns the value of the svmPort field |

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
| `svmPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The svmPort field value, see [OsConstants.VMADDR_PORT_ANY](https://developer.android.com/reference/kotlin/android/system/OsConstants#VMADDR_PORT_ANY:kotlin.Int). |
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
