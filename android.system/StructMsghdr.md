# StructMsghdr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StructMsghdr

Kotlin | [Java](https://developer.android.com/reference/android/system/StructMsghdr "View this page in Java") 

```
class StructMsghdr
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.system.StructMsghdr](https://developer.android.com/reference/kotlin/android/system/StructMsghdr#) |

Corresponds to C's `struct msghdr`

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StructMsghdr](https://developer.android.com/reference/kotlin/android/system/StructMsghdr#StructMsghdr(java.net.SocketAddress,%20kotlin.Array,%20kotlin.Array,%20kotlin.Int))`(`msg_name:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)?`, `msg_iov:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>`, `msg_control:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StructCmsghdr](https://developer.android.com/reference/kotlin/android/system/StructCmsghdr)!>?`, `msg_flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an instance with the given field values |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [StructCmsghdr](https://developer.android.com/reference/kotlin/android/system/StructCmsghdr)!\>? | [msg_control](https://developer.android.com/reference/kotlin/android/system/StructMsghdr#msg_control:kotlin.Array) Ancillary data |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [msg_flags](https://developer.android.com/reference/kotlin/android/system/StructMsghdr#msg_flags:kotlin.Int) Flags on received message. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\> | [msg_iov](https://developer.android.com/reference/kotlin/android/system/StructMsghdr#msg_iov:kotlin.Array) Scatter/gather array |
| [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)? | [msg_name](https://developer.android.com/reference/kotlin/android/system/StructMsghdr#msg_name:java.net.SocketAddress) Optional address. |

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
| `msg_name` | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)?: This value may be `null`. |
| `msg_iov` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>: This value cannot be `null`. |
| `msg_control` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [StructCmsghdr](https://developer.android.com/reference/kotlin/android/system/StructCmsghdr)!\>?: This value may be `null`. |

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
