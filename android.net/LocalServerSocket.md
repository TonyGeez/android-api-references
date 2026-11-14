# LocalServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalServerSocket

Kotlin| [Java](../android/net/LocalServerSocket.md) 
| --- | --- |

```
open class LocalServerSocket : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.LocalServerSocket](../android/net/LocalServerSocket.md) |

Non-standard class for creating an inbound UNIX-domain socket in the Linux abstract namespace.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LocalServerSocket](../android/net/LocalServerSocket.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`)` Create a LocalServerSocket from a file descriptor that's already been created and bound. |
| [LocalServerSocket](../android/net/LocalServerSocket.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new server socket listening at specified name. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [LocalSocket](../android/net/LocalSocket.md)! | [accept](../android/net/LocalServerSocket.md))`()` Accepts a new connection to the socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/net/LocalServerSocket.md))`()` Closes server socket. |
| open [FileDescriptor](../java/io/FileDescriptor.md)! | [getFileDescriptor](../android/net/LocalServerSocket.md))`()` Returns file descriptor or null if not yet open/already closed |
| --- | --- |
| open [LocalSocketAddress](../android/net/LocalSocketAddress.md)! | [getLocalSocketAddress](../android/net/LocalServerSocket.md))`()` Obtains the socket's local address |

## Public constructors

### LocalServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocalServerSocket(fd: FileDescriptor!)
```

Create a LocalServerSocket from a file descriptor that's already been created and bound. listen() will be called immediately on it. Used for cases where file descriptors are passed in via environment variables. The passed-in FileDescriptor is not managed by this class and must be closed by the caller. Calling #close() on a socket created by this method has no effect.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md)!:bound file descriptor |

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### LocalServerSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocalServerSocket(name: String!)
```

Creates a new server socket listening at specified name. On the Android platform, the name is created in the Linux abstract namespace (instead of on the filesystem).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:address for socket |

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

## Public methods

### accept

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun accept(): LocalSocket!
```

Accepts a new connection to the socket. Blocks until a new connection arrives.

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------|
| [LocalSocket](../android/net/LocalSocket.md)! | a socket representing the new connection. |

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes server socket.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | |

### getFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFileDescriptor(): FileDescriptor!
```

Returns file descriptor or null if not yet open/already closed

| Return ||
|------------------------------------------------------------------------------------------------|------------|
| [FileDescriptor](../java/io/FileDescriptor.md)! | fd or null |

### getLocalSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalSocketAddress(): LocalSocketAddress!
```

Obtains the socket's local address

| Return ||
|------------------------------------------------------------------------------------------------------|---------------|
| [LocalSocketAddress](../android/net/LocalSocketAddress.md)! | local address |
