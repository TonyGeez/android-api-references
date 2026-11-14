# SocketOption

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketOption

```
interface SocketOption<T : Any!>
```

| [java.net.SocketOption](SocketOption.md) |

A socket option associated with a socket.

In the [channels](../java.nio.channels/_package.md) package, the interface defines the [setOption](../java.nio.channels/NetworkChannel.md))and [getOption](../java.nio.channels/NetworkChannel.md))methods to set and query the channel's socket options.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](SocketOption.md))`()` Returns the name of the socket option. |
| abstract [Class](../java.lang/Class.md)\<T\>! | [type](SocketOption.md))`()` Returns the type of the socket option value. |

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
| [Class](../java.lang/Class.md)<T>! | the type of the socket option value |
