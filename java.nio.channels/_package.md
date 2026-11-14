# java.nio.channels

# java.nio.channels

## Interfaces

| [AsynchronousByteChannel](AsynchronousByteChannel.md) | An asynchronous channel that can read and write bytes. |
| --- | --- |
| [AsynchronousChannel](AsynchronousChannel.md) | A channel that supports asynchronous I/O operations. |
| [ByteChannel](ByteChannel.md) | A channel that can read and write bytes. |
| [Channel](Channel.md) | A nexus for I/O operations. |
| --- | --- |
| [CompletionHandler](CompletionHandler.md) | A handler for consuming the result of an asynchronous I/O operation. |
| [GatheringByteChannel](GatheringByteChannel.md) | A channel that can write bytes from a sequence of buffers. |
| [InterruptibleChannel](InterruptibleChannel.md) | A channel that can be asynchronously closed and interrupted. |
| --- | --- |
| [MulticastChannel](MulticastChannel.md) | A network channel that supports Internet Protocol (IP) multicasting. |
| [NetworkChannel](NetworkChannel.md) | A channel to a network socket. |
| [ReadableByteChannel](ReadableByteChannel.md) | A channel that can read bytes. |
| --- | --- |
| [ScatteringByteChannel](ScatteringByteChannel.md) | A channel that can read bytes into a sequence of buffers. |
| [SeekableByteChannel](SeekableByteChannel.md) | A byte channel that maintains a current*position*and allows the position to be changed. |
| [WritableByteChannel](WritableByteChannel.md) | A channel that can write bytes. |
| --- | --- |

## Classes

| [AsynchronousChannelGroup](AsynchronousChannelGroup.md) | A grouping of asynchronous channels for the purpose of resource sharing. |
| --- | --- |
| [AsynchronousFileChannel](AsynchronousFileChannel.md) | An asynchronous channel for reading, writing, and manipulating a file. |
| [AsynchronousServerSocketChannel](AsynchronousServerSocketChannel.md) | An asynchronous channel for stream-oriented listening sockets. |
| [AsynchronousSocketChannel](AsynchronousSocketChannel.md) | An asynchronous channel for stream-oriented connecting sockets. |
| --- | --- |
| [Channels](Channels.md) | Utility methods for channels and streams. |
| [DatagramChannel](DatagramChannel.md) | A selectable channel for datagram-oriented sockets. |
| [FileChannel](FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. |
| --- | --- |
| [FileLock](FileLock.md) | A token representing a lock on a region of a file. |
| [MembershipKey](MembershipKey.md) | A token representing the membership of an Internet Protocol (IP) multicast group. |
| [Pipe](Pipe.md) | A pair of channels that implements a unidirectional pipe. |
| --- | --- |
| [SelectableChannel](SelectableChannel.md) | A channel that can be multiplexed via a [Selector](Selector.md). |
| [SelectionKey](SelectionKey.md) | A token representing the registration of a [SelectableChannel](SelectableChannel.md) with a [Selector](Selector.md). |
| [Selector](Selector.md) | A multiplexor of [SelectableChannel](SelectableChannel.md) objects. |
| --- | --- |
| [ServerSocketChannel](ServerSocketChannel.md) | A selectable channel for stream-oriented listening sockets. |
| [SocketChannel](SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. |

## Exceptions

| [AcceptPendingException](AcceptPendingException.md) | Unchecked exception thrown when an attempt is made to initiate an accept operation on a channel and a previous accept operation has not completed. |
| --- | --- |
| [AlreadyBoundException](AlreadyBoundException.md) | Unchecked exception thrown when an attempt is made to bind the socket a network oriented channel that is already bound. |
| [AlreadyConnectedException](AlreadyConnectedException.md) | Unchecked exception thrown when an attempt is made to connect a [SocketChannel](SocketChannel.md) that is already connected. |
| [AsynchronousCloseException](AsynchronousCloseException.md) | Checked exception received by a thread when another thread closes the channel or the part of the channel upon which it is blocked in an I/O operation. |
| --- | --- |
| [CancelledKeyException](CancelledKeyException.md) | Unchecked exception thrown when an attempt is made to use a selection key that is no longer valid. |
| [ClosedByInterruptException](ClosedByInterruptException.md) | Checked exception received by a thread when another thread interrupts it while it is blocked in an I/O operation upon a channel. |
| [ClosedChannelException](ClosedChannelException.md) | Checked exception thrown when an attempt is made to invoke or complete an I/O operation upon channel that is closed, or at least closed to that operation. |
| --- | --- |
| [ClosedSelectorException](ClosedSelectorException.md) | Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a closed selector. |
| [ConnectionPendingException](ConnectionPendingException.md) | Unchecked exception thrown when an attempt is made to connect a [SocketChannel](SocketChannel.md) for which a non-blocking connection operation is already in progress. |
| [FileLockInterruptionException](FileLockInterruptionException.md) | Checked exception received by a thread when another thread interrupts it while it is waiting to acquire a file lock. |
| --- | --- |
| [IllegalBlockingModeException](IllegalBlockingModeException.md) | Unchecked exception thrown when a blocking-mode-specific operation is invoked upon a channel in the incorrect blocking mode. |
| [IllegalChannelGroupException](IllegalChannelGroupException.md) | Unchecked exception thrown when an attempt is made to open a channel in a group that was not created by the same provider. |
| [IllegalSelectorException](IllegalSelectorException.md) | Unchecked exception thrown when an attempt is made to register a channel with a selector that was not created by the provider that created the channel. |
| --- | --- |
| [InterruptedByTimeoutException](InterruptedByTimeoutException.md) | Checked exception received by a thread when a timeout elapses before an asynchronous operation completes. |
| [NoConnectionPendingException](NoConnectionPendingException.md) | Unchecked exception thrown when the [finishConnect](SocketChannel.md))method of a [SocketChannel](SocketChannel.md) is invoked without first successfully invoking its [connect](SocketChannel.md))method. |
| [NonReadableChannelException](NonReadableChannelException.md) | Unchecked exception thrown when an attempt is made to read from a channel that was not originally opened for reading. |
| --- | --- |
| [NonWritableChannelException](NonWritableChannelException.md) | Unchecked exception thrown when an attempt is made to write to a channel that was not originally opened for writing. |
| [NotYetBoundException](NotYetBoundException.md) | Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a server socket channel that is not yet bound. |
| [NotYetConnectedException](NotYetConnectedException.md) | Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a socket channel that is not yet connected. |
| --- | --- |
| [OverlappingFileLockException](OverlappingFileLockException.md) | Unchecked exception thrown when an attempt is made to acquire a lock on a region of a file that overlaps a region already locked by the same Java virtual machine, or when another thread is already waiting to lock an overlapping region of the same file. |
| [ReadPendingException](ReadPendingException.md) | Unchecked exception thrown when an attempt is made to read from an asynchronous socket channel and a previous read has not completed. |
| [ShutdownChannelGroupException](ShutdownChannelGroupException.md) | Unchecked exception thrown when an attempt is made to construct a channel in a group that is shutdown or the completion handler for an I/O operation cannot be invoked because the channel group has terminated. |
| --- | --- |
| [UnresolvedAddressException](UnresolvedAddressException.md) | Unchecked exception thrown when an attempt is made to invoke a network operation upon an unresolved socket address. |
| [UnsupportedAddressTypeException](UnsupportedAddressTypeException.md) | Unchecked exception thrown when an attempt is made to bind or connect to a socket address of a type that is not supported. |
| [WritePendingException](WritePendingException.md) | Unchecked exception thrown when an attempt is made to write to an asynchronous socket channel and a previous write has not completed. |
| --- | --- |
