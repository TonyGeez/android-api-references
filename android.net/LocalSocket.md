# LocalSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalSocket

Kotlin| [Java](https://developer.android.com/reference/android/net/LocalSocket "View this page in Java") 

```
open class LocalSocket : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.LocalSocket](https://developer.android.com/reference/kotlin/android/net/LocalSocket#) |

Creates a (non-server) socket in the UNIX-domain namespace. The interface here is not entirely unlike that of java.net.Socket. This class and the streams returned from it may be used from multiple threads.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_DGRAM](https://developer.android.com/reference/kotlin/android/net/LocalSocket#SOCKET_DGRAM:kotlin.Int) Datagram socket type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_SEQPACKET](https://developer.android.com/reference/kotlin/android/net/LocalSocket#SOCKET_SEQPACKET:kotlin.Int) Sequential packet socket type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_STREAM](https://developer.android.com/reference/kotlin/android/net/LocalSocket#SOCKET_STREAM:kotlin.Int) Stream socket type |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LocalSocket](https://developer.android.com/reference/kotlin/android/net/LocalSocket#LocalSocket())`()` Creates a AF_LOCAL/UNIX domain stream socket. |
| [LocalSocket](https://developer.android.com/reference/kotlin/android/net/LocalSocket#LocalSocket(kotlin.Int))`(`sockType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a AF_LOCAL/UNIX domain socket with the given socket type. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bind](https://developer.android.com/reference/kotlin/android/net/LocalSocket#bind(android.net.LocalSocketAddress))`(`bindpoint:` ` [LocalSocketAddress](https://developer.android.com/reference/kotlin/android/net/LocalSocketAddress)!`)` Binds this socket to an endpoint name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/net/LocalSocket#close())`()` Closes the socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/net/LocalSocket#connect(android.net.LocalSocketAddress))`(`endpoint:` ` [LocalSocketAddress](https://developer.android.com/reference/kotlin/android/net/LocalSocketAddress)!`)` Connects this socket to an endpoint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/net/LocalSocket#connect(android.net.LocalSocketAddress,%20kotlin.Int))`(`endpoint:` ` [LocalSocketAddress](https://developer.android.com/reference/kotlin/android/net/LocalSocketAddress)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!\>! | [getAncillaryFileDescriptors](https://developer.android.com/reference/kotlin/android/net/LocalSocket#getAncillaryFileDescriptors())`()` Retrieves a set of file descriptors that a peer has sent through an ancillary message. |
| open [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)! | [getFileDescriptor](https://developer.android.com/reference/kotlin/android/net/LocalSocket#getFileDescriptor())`()` Returns file descriptor or null if not yet open/already closed |
| open [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [getInputStream](https://developer.android.com/reference/kotlin/android/net/LocalSocket#getInputStream())`()` Retrieves the input stream for this instance. |
| open [LocalSocketAddress](https://developer.android.com/reference/kotlin/android/net/LocalSocketAddress)! | [getLocalSocketAddress](https://developer.android.com/reference/kotlin/android/net/LocalSocket#getLocalSocketAddress())`()` Retrieves the name that this socket is bound to, if any. |
| open [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [getOutputStream](https://developer.android.com/reference/kotlin/android/net/LocalSocket#getOutputStream())`()` Retrieves the output stream for this instance. |
| open [Credentials](https://developer.android.com/reference/kotlin/android/net/Credentials)! | [getPeerCredentials](https://developer.android.com/reference/kotlin/android/net/LocalSocket#getPeerCredentials())`()` Retrieves the credentials of this socket's peer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReceiveBufferSize](https://developer.android.com/reference/kotlin/android/net/LocalSocket#getReceiveBufferSize())`()` <br /> |
| open [LocalSocketAddress](https://developer.android.com/reference/kotlin/android/net/LocalSocketAddress)! | [getRemoteSocketAddress](https://developer.android.com/reference/kotlin/android/net/LocalSocket#getRemoteSocketAddress())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSendBufferSize](https://developer.android.com/reference/kotlin/android/net/LocalSocket#getSendBufferSize())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoTimeout](https://developer.android.com/reference/kotlin/android/net/LocalSocket#getSoTimeout())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBound](https://developer.android.com/reference/kotlin/android/net/LocalSocket#isBound())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](https://developer.android.com/reference/kotlin/android/net/LocalSocket#isClosed())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/net/LocalSocket#isConnected())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInputShutdown](https://developer.android.com/reference/kotlin/android/net/LocalSocket#isInputShutdown())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOutputShutdown](https://developer.android.com/reference/kotlin/android/net/LocalSocket#isOutputShutdown())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFileDescriptorsForSend](https://developer.android.com/reference/kotlin/android/net/LocalSocket#setFileDescriptorsForSend(kotlin.Array))`(`fds:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!>!`)` Enqueues a set of file descriptors to send to the peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReceiveBufferSize](https://developer.android.com/reference/kotlin/android/net/LocalSocket#setReceiveBufferSize(kotlin.Int))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSendBufferSize](https://developer.android.com/reference/kotlin/android/net/LocalSocket#setSendBufferSize(kotlin.Int))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSoTimeout](https://developer.android.com/reference/kotlin/android/net/LocalSocket#setSoTimeout(kotlin.Int))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdownInput](https://developer.android.com/reference/kotlin/android/net/LocalSocket#shutdownInput())`()` Shuts down the input side of the socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdownOutput](https://developer.android.com/reference/kotlin/android/net/LocalSocket#shutdownOutput())`()` Shuts down the output side of the socket. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/LocalSocket#toString())`()` Returns a string representation of the object. |

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
| `sockType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):either [SOCKET_DGRAM](https://developer.android.com/reference/kotlin/android/net/LocalSocket#SOCKET_DGRAM:kotlin.Int), [SOCKET_STREAM](https://developer.android.com/reference/kotlin/android/net/LocalSocket#SOCKET_STREAM:kotlin.Int) or [SOCKET_SEQPACKET](https://developer.android.com/reference/kotlin/android/net/LocalSocket#SOCKET_SEQPACKET:kotlin.Int) |

## Public methods

### bind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bind(bindpoint: LocalSocketAddress!): Unit
```

Binds this socket to an endpoint name. May only be called on an instance that has not yet been bound.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------|
| `bindpoint` | [LocalSocketAddress](https://developer.android.com/reference/kotlin/android/net/LocalSocketAddress)!:endpoint address |

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
| `endpoint` | [LocalSocketAddress](https://developer.android.com/reference/kotlin/android/net/LocalSocketAddress)!:endpoint address |

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
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!>! | null or file descriptor array |

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
| [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)! | fd or null |

### getInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputStream(): InputStream!
```

Retrieves the input stream for this instance. Closing this stream is equivalent to closing the entire socket and its associated streams using #close().

| Return ||
|------------------------------------------------------------------------------------------|--------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | input stream |

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
| [LocalSocketAddress](https://developer.android.com/reference/kotlin/android/net/LocalSocketAddress)! | Local address or null if anonymous |

### getOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutputStream(): OutputStream!
```

Retrieves the output stream for this instance. Closing this stream is equivalent to closing the entire socket and its associated streams using #close().

| Return ||
|--------------------------------------------------------------------------------------------|---------------|
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | output stream |

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
| [Credentials](https://developer.android.com/reference/kotlin/android/net/Credentials)! | non-null; peer credentials |

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
| `fds` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!\>!:non-null; file descriptors to send. |

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
