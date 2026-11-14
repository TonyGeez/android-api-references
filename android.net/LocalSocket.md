# LocalSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalSocket

Kotlin| [Java](../android/net/LocalSocket.md) 
| --- | --- |

```
open class LocalSocket : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.LocalSocket](../android/net/LocalSocket.md) |

Creates a (non-server) socket in the UNIX-domain namespace. The interface here is not entirely unlike that of java.net.Socket. This class and the streams returned from it may be used from multiple threads.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_DGRAM](../android/net/LocalSocket.md) Datagram socket type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_SEQPACKET](../android/net/LocalSocket.md) Sequential packet socket type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_STREAM](../android/net/LocalSocket.md) Stream socket type |
| --- | --- |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LocalSocket](../android/net/LocalSocket.md))`()` Creates a AF_LOCAL/UNIX domain stream socket. |
| [LocalSocket](../android/net/LocalSocket.md))`(`sockType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a AF_LOCAL/UNIX domain socket with the given socket type. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bind](../android/net/LocalSocket.md))`(`bindpoint:` ` [LocalSocketAddress](../android/net/LocalSocketAddress.md)!`)` Binds this socket to an endpoint name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/net/LocalSocket.md))`()` Closes the socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/net/LocalSocket.md))`(`endpoint:` ` [LocalSocketAddress](../android/net/LocalSocketAddress.md)!`)` Connects this socket to an endpoint. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/net/LocalSocket.md))`(`endpoint:` ` [LocalSocketAddress](../android/net/LocalSocketAddress.md)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FileDescriptor](../java/io/FileDescriptor.md)!\>! | [getAncillaryFileDescriptors](../android/net/LocalSocket.md))`()` Retrieves a set of file descriptors that a peer has sent through an ancillary message. |
| open [FileDescriptor](../java/io/FileDescriptor.md)! | [getFileDescriptor](../android/net/LocalSocket.md))`()` Returns file descriptor or null if not yet open/already closed |
| --- | --- |
| open [InputStream](../java/io/InputStream.md)! | [getInputStream](../android/net/LocalSocket.md))`()` Retrieves the input stream for this instance. |
| open [LocalSocketAddress](../android/net/LocalSocketAddress.md)! | [getLocalSocketAddress](../android/net/LocalSocket.md))`()` Retrieves the name that this socket is bound to, if any. |
| open [OutputStream](../java/io/OutputStream.md)! | [getOutputStream](../android/net/LocalSocket.md))`()` Retrieves the output stream for this instance. |
| --- | --- |
| open [Credentials](../android/net/Credentials.md)! | [getPeerCredentials](../android/net/LocalSocket.md))`()` Retrieves the credentials of this socket's peer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReceiveBufferSize](../android/net/LocalSocket.md))`()` <br /> |
| open [LocalSocketAddress](../android/net/LocalSocketAddress.md)! | [getRemoteSocketAddress](../android/net/LocalSocket.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSendBufferSize](../android/net/LocalSocket.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoTimeout](../android/net/LocalSocket.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBound](../android/net/LocalSocket.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](../android/net/LocalSocket.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](../android/net/LocalSocket.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInputShutdown](../android/net/LocalSocket.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOutputShutdown](../android/net/LocalSocket.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFileDescriptorsForSend](../android/net/LocalSocket.md))`(`fds:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FileDescriptor](../java/io/FileDescriptor.md)!>!`)` Enqueues a set of file descriptors to send to the peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReceiveBufferSize](../android/net/LocalSocket.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSendBufferSize](../android/net/LocalSocket.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSoTimeout](../android/net/LocalSocket.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdownInput](../android/net/LocalSocket.md))`()` Shuts down the input side of the socket. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdownOutput](../android/net/LocalSocket.md))`()` Shuts down the output side of the socket. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/LocalSocket.md))`()` Returns a string representation of the object. |

## Constants

### SOCKET_DGRAM

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOCKET_DGRAM: Int
```

Datagram socket type 

 Value: 1

### SOCKET_SEQPACKET

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOCKET_SEQPACKET: Int
```

Sequential packet socket type 

 Value: 3

### SOCKET_STREAM

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOCKET_STREAM: Int
```

Stream socket type 

 Value: 2

## Public constructors

### LocalSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocalSocket()
```

Creates a AF_LOCAL/UNIX domain stream socket. 

### LocalSocket

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocalSocket(sockType: Int)
```

Creates a AF_LOCAL/UNIX domain socket with the given socket type.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sockType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):either [SOCKET_DGRAM](../android/net/LocalSocket.md), [SOCKET_STREAM](../android/net/LocalSocket.md) or [SOCKET_SEQPACKET](../android/net/LocalSocket.md) |

## Public methods

### bind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bind(bindpoint: LocalSocketAddress!): Unit
```

Binds this socket to an endpoint name. May only be called on an instance that has not yet been bound.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------|
| `bindpoint` | [LocalSocketAddress](../android/net/LocalSocketAddress.md)!:endpoint address |

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes the socket.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun connect(endpoint: LocalSocketAddress!): Unit
```

Connects this socket to an endpoint. May only be called on an instance that has not yet been connected.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------|
| `endpoint` | [LocalSocketAddress](../android/net/LocalSocketAddress.md)!:endpoint address |

| Exceptions ||
|-----------------------|--------------------------------------------------------------|
| `java.io.IOException` | if socket is in invalid state or the address does not exist. |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun connect(
    endpoint: LocalSocketAddress!, 
    timeout: Int
): Unit
```  

### getAncillaryFileDescriptors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAncillaryFileDescriptors(): Array<FileDescriptor!>!
```

Retrieves a set of file descriptors that a peer has sent through an ancillary message. This method retrieves the most recent set sent, and then returns null until a new set arrives. File descriptors may only be passed along with regular data, so this method can only return a non-null after a read operation.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FileDescriptor](../java/io/FileDescriptor.md)!>! | null or file descriptor array |

| Exceptions ||
|-----------------------|---|
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

### getInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputStream(): InputStream!
```

Retrieves the input stream for this instance. Closing this stream is equivalent to closing the entire socket and its associated streams using #close().

| Return ||
|------------------------------------------------------------------------------------------|--------------|
| [InputStream](../java/io/InputStream.md)! | input stream |

| Exceptions ||
|-----------------------|-------------------------------------------------|
| `java.io.IOException` | if socket has been closed or cannot be created. |

### getLocalSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalSocketAddress(): LocalSocketAddress!
```

Retrieves the name that this socket is bound to, if any.

| Return ||
|------------------------------------------------------------------------------------------------------|------------------------------------|
| [LocalSocketAddress](../android/net/LocalSocketAddress.md)! | Local address or null if anonymous |

### getOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutputStream(): OutputStream!
```

Retrieves the output stream for this instance. Closing this stream is equivalent to closing the entire socket and its associated streams using #close().

| Return ||
|--------------------------------------------------------------------------------------------|---------------|
| [OutputStream](../java/io/OutputStream.md)! | output stream |

| Exceptions ||
|-----------------------|-------------------------------------------------|
| `java.io.IOException` | if socket has been closed or cannot be created. |

### getPeerCredentials

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPeerCredentials(): Credentials!
```

Retrieves the credentials of this socket's peer. Only valid on connected sockets.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------|
| [Credentials](../android/net/Credentials.md)! | non-null; peer credentials |

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### getReceiveBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReceiveBufferSize(): Int
```  

### getRemoteSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRemoteSocketAddress(): LocalSocketAddress!
```  

### getSendBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSendBufferSize(): Int
```  

### getSoTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSoTimeout(): Int
```  

### isBound

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBound(): Boolean
```  

### isClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isClosed(): Boolean
```  

### isConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isConnected(): Boolean
```  

### isInputShutdown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isInputShutdown(): Boolean
```  

### isOutputShutdown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOutputShutdown(): Boolean
```  

### setFileDescriptorsForSend

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFileDescriptorsForSend(fds: Array<FileDescriptor!>!): Unit
```

Enqueues a set of file descriptors to send to the peer. The queue is one deep. The file descriptors will be sent with the next write of normal data, and will be delivered in a single ancillary message. See "man 7 unix" SCM_RIGHTS on a desktop Linux machine.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fds` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FileDescriptor](../java/io/FileDescriptor.md)!\>!:non-null; file descriptors to send. |

### setReceiveBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReceiveBufferSize(size: Int): Unit
```  

### setSendBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSendBufferSize(n: Int): Unit
```  

### setSoTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSoTimeout(n: Int): Unit
```  

### shutdownInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shutdownInput(): Unit
```

Shuts down the input side of the socket.

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### shutdownOutput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shutdownOutput(): Unit
```

Shuts down the output side of the socket.

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
