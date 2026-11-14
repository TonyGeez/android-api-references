# LocalSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalSocket

Kotlin| [Java](LocalSocket.md) 
| --- | --- |

```
open class LocalSocket : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.LocalSocket](LocalSocket.md) |

Creates a (non-server) socket in the UNIX-domain namespace. The interface here is not entirely unlike that of java.net.Socket. This class and the streams returned from it may be used from multiple threads.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_DGRAM](LocalSocket.md) Datagram socket type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_SEQPACKET](LocalSocket.md) Sequential packet socket type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_STREAM](LocalSocket.md) Stream socket type |
| --- | --- |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LocalSocket](LocalSocket.md))`()` Creates a AF_LOCAL/UNIX domain stream socket. |
| [LocalSocket](LocalSocket.md))`(`sockType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a AF_LOCAL/UNIX domain socket with the given socket type. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bind](LocalSocket.md))`(`bindpoint:` ` [LocalSocketAddress](LocalSocketAddress.md)!`)` Binds this socket to an endpoint name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](LocalSocket.md))`()` Closes the socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](LocalSocket.md))`(`endpoint:` ` [LocalSocketAddress](LocalSocketAddress.md)!`)` Connects this socket to an endpoint. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](LocalSocket.md))`(`endpoint:` ` [LocalSocketAddress](LocalSocketAddress.md)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FileDescriptor](../java.io/FileDescriptor.md)!\>! | [getAncillaryFileDescriptors](LocalSocket.md))`()` Retrieves a set of file descriptors that a peer has sent through an ancillary message. |
| open [FileDescriptor](../java.io/FileDescriptor.md)! | [getFileDescriptor](LocalSocket.md))`()` Returns file descriptor or null if not yet open/already closed |
| --- | --- |
| open [InputStream](../java.io/InputStream.md)! | [getInputStream](LocalSocket.md))`()` Retrieves the input stream for this instance. |
| open [LocalSocketAddress](LocalSocketAddress.md)! | [getLocalSocketAddress](LocalSocket.md))`()` Retrieves the name that this socket is bound to, if any. |
| open [OutputStream](../java.io/OutputStream.md)! | [getOutputStream](LocalSocket.md))`()` Retrieves the output stream for this instance. |
| --- | --- |
| open [Credentials](Credentials.md)! | [getPeerCredentials](LocalSocket.md))`()` Retrieves the credentials of this socket's peer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReceiveBufferSize](LocalSocket.md))`()` <br /> |
| open [LocalSocketAddress](LocalSocketAddress.md)! | [getRemoteSocketAddress](LocalSocket.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSendBufferSize](LocalSocket.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoTimeout](LocalSocket.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBound](LocalSocket.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](LocalSocket.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](LocalSocket.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInputShutdown](LocalSocket.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOutputShutdown](LocalSocket.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFileDescriptorsForSend](LocalSocket.md))`(`fds:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FileDescriptor](../java.io/FileDescriptor.md)!>!`)` Enqueues a set of file descriptors to send to the peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReceiveBufferSize](LocalSocket.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSendBufferSize](LocalSocket.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSoTimeout](LocalSocket.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdownInput](LocalSocket.md))`()` Shuts down the input side of the socket. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdownOutput](LocalSocket.md))`()` Shuts down the output side of the socket. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](LocalSocket.md))`()` Returns a string representation of the object. |

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
| `sockType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):either [SOCKET_DGRAM](LocalSocket.md), [SOCKET_STREAM](LocalSocket.md) or [SOCKET_SEQPACKET](LocalSocket.md) |

## Public methods

### bind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bind(bindpoint: LocalSocketAddress!): Unit
```

Binds this socket to an endpoint name. May only be called on an instance that has not yet been bound.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------|
| `bindpoint` | [LocalSocketAddress](LocalSocketAddress.md)!:endpoint address |

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
| `endpoint` | [LocalSocketAddress](LocalSocketAddress.md)!:endpoint address |

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
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FileDescriptor](../java.io/FileDescriptor.md)!>! | null or file descriptor array |

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
| [FileDescriptor](../java.io/FileDescriptor.md)! | fd or null |

### getInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputStream(): InputStream!
```

Retrieves the input stream for this instance. Closing this stream is equivalent to closing the entire socket and its associated streams using #close().

| Return ||
|------------------------------------------------------------------------------------------|--------------|
| [InputStream](../java.io/InputStream.md)! | input stream |

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
| [LocalSocketAddress](LocalSocketAddress.md)! | Local address or null if anonymous |

### getOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutputStream(): OutputStream!
```

Retrieves the output stream for this instance. Closing this stream is equivalent to closing the entire socket and its associated streams using #close().

| Return ||
|--------------------------------------------------------------------------------------------|---------------|
| [OutputStream](../java.io/OutputStream.md)! | output stream |

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
| [Credentials](Credentials.md)! | non-null; peer credentials |

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
| `fds` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FileDescriptor](../java.io/FileDescriptor.md)!\>!:non-null; file descriptors to send. |

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
