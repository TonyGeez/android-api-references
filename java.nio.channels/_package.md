# java.nio.channels

# java.nio.channels

## Interfaces

| [AsynchronousByteChannel](../java/nio/channels/AsynchronousByteChannel.md) | An asynchronous channel that can read and write bytes. |
| --- | --- |
| [AsynchronousChannel](../java/nio/channels/AsynchronousChannel.md) | A channel that supports asynchronous I/O operations. |
| [ByteChannel](../java/nio/channels/ByteChannel.md) | A channel that can read and write bytes. |
| [Channel](../java/nio/channels/Channel.md) | A nexus for I/O operations. |
| --- | --- |
| [CompletionHandler](../java/nio/channels/CompletionHandler.md) | A handler for consuming the result of an asynchronous I/O operation. |
| [GatheringByteChannel](../java/nio/channels/GatheringByteChannel.md) | A channel that can write bytes from a sequence of buffers. |
| [InterruptibleChannel](../java/nio/channels/InterruptibleChannel.md) | A channel that can be asynchronously closed and interrupted. |
| --- | --- |
| [MulticastChannel](../java/nio/channels/MulticastChannel.md) | A network channel that supports Internet Protocol (IP) multicasting. |
| [NetworkChannel](../java/nio/channels/NetworkChannel.md) | A channel to a network socket. |
| [ReadableByteChannel](../java/nio/channels/ReadableByteChannel.md) | A channel that can read bytes. |
| --- | --- |
| [ScatteringByteChannel](../java/nio/channels/ScatteringByteChannel.md) | A channel that can read bytes into a sequence of buffers. |
| [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md) | A byte channel that maintains a current*position*and allows the position to be changed. |
| [WritableByteChannel](../java/nio/channels/WritableByteChannel.md) | A channel that can write bytes. |
| --- | --- |

## Classes

| [AsynchronousChannelGroup](../java/nio/channels/AsynchronousChannelGroup.md) | A grouping of asynchronous channels for the purpose of resource sharing. |
| --- | --- |
| [AsynchronousFileChannel](../java/nio/channels/AsynchronousFileChannel.md) | An asynchronous channel for reading, writing, and manipulating a file. |
| [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md) | An asynchronous channel for stream-oriented listening sockets. |
| [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md) | An asynchronous channel for stream-oriented connecting sockets. |
| --- | --- |
| [Channels](../java/nio/channels/Channels.md) | Utility methods for channels and streams. |
| [DatagramChannel](../java/nio/channels/DatagramChannel.md) | A selectable channel for datagram-oriented sockets. |
| [FileChannel](../java/nio/channels/FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. |
| --- | --- |
| [FileLock](../java/nio/channels/FileLock.md) | A token representing a lock on a region of a file. |
| [MembershipKey](../java/nio/channels/MembershipKey.md) | A token representing the membership of an Internet Protocol (IP) multicast group. |
| [Pipe](../java/nio/channels/Pipe.md) | A pair of channels that implements a unidirectional pipe. |
| --- | --- |
| [SelectableChannel](../java/nio/channels/SelectableChannel.md) | A channel that can be multiplexed via a [Selector](../java/nio/channels/Selector.md). |
| [SelectionKey](../java/nio/channels/SelectionKey.md) | A token representing the registration of a [SelectableChannel](../java/nio/channels/SelectableChannel.md) with a [Selector](../java/nio/channels/Selector.md). |
| [Selector](../java/nio/channels/Selector.md) | A multiplexor of [SelectableChannel](../java/nio/channels/SelectableChannel.md) objects. |
| --- | --- |
| [ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md) | A selectable channel for stream-oriented listening sockets. |
| [SocketChannel](../java/nio/channels/SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. |

## Exceptions

| [AcceptPendingException](../java/nio/channels/AcceptPendingException.md) | Unchecked exception thrown when an attempt is made to initiate an accept operation on a channel and a previous accept operation has not completed. |
| --- | --- |
| [AlreadyBoundException](../java/nio/channels/AlreadyBoundException.md) | Unchecked exception thrown when an attempt is made to bind the socket a network oriented channel that is already bound. |
| [AlreadyConnectedException](../java/nio/channels/AlreadyConnectedException.md) | Unchecked exception thrown when an attempt is made to connect a [SocketChannel](../java/nio/channels/SocketChannel.md) that is already connected. |
| [AsynchronousCloseException](../java/nio/channels/AsynchronousCloseException.md) | Checked exception received by a thread when another thread closes the channel or the part of the channel upon which it is blocked in an I/O operation. |
| --- | --- |
| [CancelledKeyException](../java/nio/channels/CancelledKeyException.md) | Unchecked exception thrown when an attempt is made to use a selection key that is no longer valid. |
| [ClosedByInterruptException](../java/nio/channels/ClosedByInterruptException.md) | Checked exception received by a thread when another thread interrupts it while it is blocked in an I/O operation upon a channel. |
| [ClosedChannelException](../java/nio/channels/ClosedChannelException.md) | Checked exception thrown when an attempt is made to invoke or complete an I/O operation upon channel that is closed, or at least closed to that operation. |
| --- | --- |
| [ClosedSelectorException](../java/nio/channels/ClosedSelectorException.md) | Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a closed selector. |
| [ConnectionPendingException](../java/nio/channels/ConnectionPendingException.md) | Unchecked exception thrown when an attempt is made to connect a [SocketChannel](../java/nio/channels/SocketChannel.md) for which a non-blocking connection operation is already in progress. |
| [FileLockInterruptionException](../java/nio/channels/FileLockInterruptionException.md) | Checked exception received by a thread when another thread interrupts it while it is waiting to acquire a file lock. |
| --- | --- |
| [IllegalBlockingModeException](../java/nio/channels/IllegalBlockingModeException.md) | Unchecked exception thrown when a blocking-mode-specific operation is invoked upon a channel in the incorrect blocking mode. |
| [IllegalChannelGroupException](../java/nio/channels/IllegalChannelGroupException.md) | Unchecked exception thrown when an attempt is made to open a channel in a group that was not created by the same provider. |
| [IllegalSelectorException](../java/nio/channels/IllegalSelectorException.md) | Unchecked exception thrown when an attempt is made to register a channel with a selector that was not created by the provider that created the channel. |
| --- | --- |
| [InterruptedByTimeoutException](../java/nio/channels/InterruptedByTimeoutException.md) | Checked exception received by a thread when a timeout elapses before an asynchronous operation completes. |
| [NoConnectionPendingException](../java/nio/channels/NoConnectionPendingException.md) | Unchecked exception thrown when the [finishConnect](../java/nio/channels/SocketChannel.md))method of a [SocketChannel](../java/nio/channels/SocketChannel.md) is invoked without first successfully invoking its [connect](../java/nio/channels/SocketChannel.md))method. |
| [NonReadableChannelException](../java/nio/channels/NonReadableChannelException.md) | Unchecked exception thrown when an attempt is made to read from a channel that was not originally opened for reading. |
| --- | --- |
| [NonWritableChannelException](../java/nio/channels/NonWritableChannelException.md) | Unchecked exception thrown when an attempt is made to write to a channel that was not originally opened for writing. |
| [NotYetBoundException](../java/nio/channels/NotYetBoundException.md) | Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a server socket channel that is not yet bound. |
| [NotYetConnectedException](../java/nio/channels/NotYetConnectedException.md) | Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a socket channel that is not yet connected. |
| --- | --- |
| [OverlappingFileLockException](../java/nio/channels/OverlappingFileLockException.md) | Unchecked exception thrown when an attempt is made to acquire a lock on a region of a file that overlaps a region already locked by the same Java virtual machine, or when another thread is already waiting to lock an overlapping region of the same file. |
| [ReadPendingException](../java/nio/channels/ReadPendingException.md) | Unchecked exception thrown when an attempt is made to read from an asynchronous socket channel and a previous read has not completed. |
| [ShutdownChannelGroupException](../java/nio/channels/ShutdownChannelGroupException.md) | Unchecked exception thrown when an attempt is made to construct a channel in a group that is shutdown or the completion handler for an I/O operation cannot be invoked because the channel group has terminated. |
| --- | --- |
| [UnresolvedAddressException](../java/nio/channels/UnresolvedAddressException.md) | Unchecked exception thrown when an attempt is made to invoke a network operation upon an unresolved socket address. |
| [UnsupportedAddressTypeException](../java/nio/channels/UnsupportedAddressTypeException.md) | Unchecked exception thrown when an attempt is made to bind or connect to a socket address of a type that is not supported. |
| [WritePendingException](../java/nio/channels/WritePendingException.md) | Unchecked exception thrown when an attempt is made to write to an asynchronous socket channel and a previous write has not completed. |
| --- | --- |
