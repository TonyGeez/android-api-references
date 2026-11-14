# SocketOption

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketOption

```
interface SocketOption<T : Any!>
```

| [java.net.SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption#) |

A socket option associated with a socket.

In the [channels](https://developer.android.com/reference/kotlin/java/nio/channels/package-summary.html) package, the interface defines the [setOption](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel.html#setOption(java.net.SocketOption,%20java.nio.channels.NetworkChannel.setOption.T))and [getOption](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel.html#getOption(java.net.SocketOption))methods to set and query the channel's socket options.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](https://developer.android.com/reference/kotlin/java/net/SocketOption#name())`()` Returns the name of the socket option. |
| abstract [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>! | [type](https://developer.android.com/reference/kotlin/java/net/SocketOption#type())`()` Returns the type of the socket option value. |

## Public methods

### name

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun name(): String!
```

Returns the name of the socket option.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the socket option |

### type

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun type(): Class<T>!
```

Returns the type of the socket option value.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>! | the type of the socket option value |
