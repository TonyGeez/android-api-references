# Channel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Channel

```
interface Channel : Closeable
```

| [java.nio.channels.Channel](Channel.md) |

| Known Direct Subclasses [AbstractInterruptibleChannel](../java.nio.channels.spi/AbstractInterruptibleChannel.md), [AsynchronousChannel](AsynchronousChannel.md), [Channel](../android.se.omapi/Channel.md), [InterruptibleChannel](InterruptibleChannel.md), [NetworkChannel](NetworkChannel.md), [ReadableByteChannel](ReadableByteChannel.md), [SelectableChannel](SelectableChannel.md), [SensorDirectChannel](../android.hardware/SensorDirectChannel.md), [WritableByteChannel](WritableByteChannel.md) |-----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [AbstractInterruptibleChannel](../java.nio.channels.spi/AbstractInterruptibleChannel.md) | Base implementation class for interruptible channels. | | [AsynchronousChannel](AsynchronousChannel.md) | A channel that supports asynchronous I/O operations. | | [Channel](../android.se.omapi/Channel.md) | Instances of this class represent an ISO/IEC 7816-4 channel opened to a Secure Element. | | [InterruptibleChannel](InterruptibleChannel.md) | A channel that can be asynchronously closed and interrupted. | | [NetworkChannel](NetworkChannel.md) | A channel to a network socket. | | [ReadableByteChannel](ReadableByteChannel.md) | A channel that can read bytes. | | [SelectableChannel](SelectableChannel.md) | A channel that can be multiplexed via a [Selector](Selector.md). | | [SensorDirectChannel](../android.hardware/SensorDirectChannel.md) | Class representing a sensor direct channel. | | [WritableByteChannel](WritableByteChannel.md) | A channel that can write bytes. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbstractInterruptibleChannel](../java.nio.channels.spi/AbstractInterruptibleChannel.md), [AbstractSelectableChannel](../java.nio.channels.spi/AbstractSelectableChannel.md), [AbstractSelectableChannel](../java.nio.channels.spi/AbstractSelectableChannel.md), [AbstractSelectableChannel](../java.nio.channels.spi/AbstractSelectableChannel.md), [AsynchronousByteChannel](AsynchronousByteChannel.md), [AsynchronousFileChannel](AsynchronousFileChannel.md), [AsynchronousServerSocketChannel](AsynchronousServerSocketChannel.md), [AsynchronousServerSocketChannel](AsynchronousServerSocketChannel.md), [AsynchronousSocketChannel](AsynchronousSocketChannel.md), [AsynchronousSocketChannel](AsynchronousSocketChannel.md), [ByteChannel](ByteChannel.md), [ByteChannel](ByteChannel.md), and 43 others. |-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [AbstractInterruptibleChannel](../java.nio.channels.spi/AbstractInterruptibleChannel.md) | Base implementation class for interruptible channels. | | [AbstractSelectableChannel](../java.nio.channels.spi/AbstractSelectableChannel.md) | Base implementation class for selectable channels. | | [AbstractSelectableChannel](../java.nio.channels.spi/AbstractSelectableChannel.md) | Base implementation class for selectable channels. | | [AbstractSelectableChannel](../java.nio.channels.spi/AbstractSelectableChannel.md) | Base implementation class for selectable channels. | | [AsynchronousByteChannel](AsynchronousByteChannel.md) | An asynchronous channel that can read and write bytes. | | [AsynchronousFileChannel](AsynchronousFileChannel.md) | An asynchronous channel for reading, writing, and manipulating a file. | | [AsynchronousServerSocketChannel](AsynchronousServerSocketChannel.md) | An asynchronous channel for stream-oriented listening sockets. | | [AsynchronousServerSocketChannel](AsynchronousServerSocketChannel.md) | An asynchronous channel for stream-oriented listening sockets. | | [AsynchronousSocketChannel](AsynchronousSocketChannel.md) | An asynchronous channel for stream-oriented connecting sockets. | | [AsynchronousSocketChannel](AsynchronousSocketChannel.md) | An asynchronous channel for stream-oriented connecting sockets. | | [ByteChannel](ByteChannel.md) | A channel that can read and write bytes. | | [ByteChannel](ByteChannel.md) | A channel that can read and write bytes. | | [DatagramChannel](DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [DatagramChannel](DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [DatagramChannel](DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [DatagramChannel](DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [DatagramChannel](DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [DatagramChannel](DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [DatagramChannel](DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [DatagramChannel](DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [FileChannel](FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. | | [FileChannel](FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. | | [FileChannel](FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. | | [FileChannel](FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. | | [FileChannel](FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. | | [FileChannel](FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. | | [GatheringByteChannel](GatheringByteChannel.md) | A channel that can write bytes from a sequence of buffers. | | [MulticastChannel](MulticastChannel.md) | A network channel that supports Internet Protocol (IP) multicasting. | | [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) | A channel representing the writable end of a [Pipe](Pipe.md). | | [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) | A channel representing the writable end of a [Pipe](Pipe.md). | | [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) | A channel representing the writable end of a [Pipe](Pipe.md). | | [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) | A channel representing the writable end of a [Pipe](Pipe.md). | | [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) | A channel representing the writable end of a [Pipe](Pipe.md). | | [Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) | A channel representing the readable end of a [Pipe](Pipe.md). | | [Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) | A channel representing the readable end of a [Pipe](Pipe.md). | | [Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) | A channel representing the readable end of a [Pipe](Pipe.md). | | [Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) | A channel representing the readable end of a [Pipe](Pipe.md). | | [Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) | A channel representing the readable end of a [Pipe](Pipe.md). | | [ScatteringByteChannel](ScatteringByteChannel.md) | A channel that can read bytes into a sequence of buffers. | | [SeekableByteChannel](SeekableByteChannel.md) | A byte channel that maintains a current*position*and allows the position to be changed. | | [SeekableByteChannel](SeekableByteChannel.md) | A byte channel that maintains a current*position*and allows the position to be changed. | | [SelectableChannel](SelectableChannel.md) | A channel that can be multiplexed via a [Selector](Selector.md). | | [SelectableChannel](SelectableChannel.md) | A channel that can be multiplexed via a [Selector](Selector.md). | | [ServerSocketChannel](ServerSocketChannel.md) | A selectable channel for stream-oriented listening sockets. | | [ServerSocketChannel](ServerSocketChannel.md) | A selectable channel for stream-oriented listening sockets. | | [ServerSocketChannel](ServerSocketChannel.md) | A selectable channel for stream-oriented listening sockets. | | [ServerSocketChannel](ServerSocketChannel.md) | A selectable channel for stream-oriented listening sockets. | | [SocketChannel](SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | | [SocketChannel](SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | | [SocketChannel](SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | | [SocketChannel](SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | | [SocketChannel](SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | | [SocketChannel](SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | | [SocketChannel](SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | | [SocketChannel](SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A nexus for I/O operations.

A channel represents an open connection to an entity such as a hardware device, a file, a network socket, or a program component that is capable of performing one or more distinct I/O operations, for example reading or writing.

A channel is either open or closed. A channel is open upon creation, and once closed it remains closed. Once a channel is closed, any attempt to invoke an I/O operation upon it will cause a [ClosedChannelException](ClosedChannelException.md) to be thrown. Whether or not a channel is open may be tested by invoking its [isOpen](Channel.md))method.

Channels are, in general, intended to be safe for multithreaded access as described in the specifications of the interfaces and classes that extend and implement this interface.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](Channel.md))`()` Closes this channel. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](Channel.md))`()` Tells whether or not this channel is open. |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes this channel.

After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](ClosedChannelException.md) to be thrown.

If this channel is already closed then invoking this method has no effect.

This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |

### isOpen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isOpen(): Boolean
```

Tells whether or not this channel is open.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this channel is open |
