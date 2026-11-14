# StructMsghdr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StructMsghdr

Kotlin | [Java](StructMsghdr.md) 
| --- | --- |

```
class StructMsghdr
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.system.StructMsghdr](StructMsghdr.md) |

Corresponds to C's `struct msghdr`

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StructMsghdr](StructMsghdr.md))`(`msg_name:` ` [SocketAddress](../java.net/SocketAddress.md)?`, `msg_iov:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](../java.nio/ByteBuffer.md)!>`, `msg_control:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StructCmsghdr](StructCmsghdr.md)!>?`, `msg_flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an instance with the given field values |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [StructCmsghdr](StructCmsghdr.md)!\>? | [msg_control](StructMsghdr.md) Ancillary data |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [msg_flags](StructMsghdr.md) Flags on received message. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](../java.nio/ByteBuffer.md)!\> | [msg_iov](StructMsghdr.md) Scatter/gather array |
| --- | --- |
| [SocketAddress](../java.net/SocketAddress.md)? | [msg_name](StructMsghdr.md) Optional address. |

## Public constructors

### StructMsghdr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StructMsghdr(
    msg_name: SocketAddress?, 
    msg_iov: Array<ByteBuffer!>, 
    msg_control: Array<StructCmsghdr!>?, 
    msg_flags: Int)
```

Constructs an instance with the given field values

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msg_name` | [SocketAddress](../java.net/SocketAddress.md)?: This value may be `null`. |
| `msg_iov` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](../java.nio/ByteBuffer.md)!\>: This value cannot be `null`. |
| `msg_control` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [StructCmsghdr](StructCmsghdr.md)!\>?: This value may be `null`. |
| --- | --- |

## Properties

### msg_control

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var msg_control: Array<StructCmsghdr!>?
```

Ancillary data 

### msg_flags

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var msg_flags: Int
```

Flags on received message. 

### msg_iov

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val msg_iov: Array<ByteBuffer!>
```

Scatter/gather array 

### msg_name

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var msg_name: SocketAddress?
```

Optional address.

Sendmsg: Caller must populate to specify the target address for a datagram, or pass `null` to send to the destination of an already-connected socket. Recvmsg: Populated by the system to specify the source address.
