# java.nio.channels

# java.nio.channels

## Interfaces

| [AsynchronousByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousByteChannel) | An asynchronous channel that can read and write bytes. |
| [AsynchronousChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannel) | A channel that supports asynchronous I/O operations. |
| [ByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ByteChannel) | A channel that can read and write bytes. |
| [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel) | A nexus for I/O operations. |
| [CompletionHandler](https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler) | A handler for consuming the result of an asynchronous I/O operation. |
| [GatheringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/GatheringByteChannel) | A channel that can write bytes from a sequence of buffers. |
| [InterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/InterruptibleChannel) | A channel that can be asynchronously closed and interrupted. |
| [MulticastChannel](https://developer.android.com/reference/kotlin/java/nio/channels/MulticastChannel) | A network channel that supports Internet Protocol (IP) multicasting. |
| [NetworkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel) | A channel to a network socket. |
| [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel) | A channel that can read bytes. |
| [ScatteringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel) | A channel that can read bytes into a sequence of buffers. |
| [SeekableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SeekableByteChannel) | A byte channel that maintains a current*position*and allows the position to be changed. |
| [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel) | A channel that can write bytes. |

## Classes

| [AsynchronousChannelGroup](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousChannelGroup) | A grouping of asynchronous channels for the purpose of resource sharing. |
| [AsynchronousFileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousFileChannel) | An asynchronous channel for reading, writing, and manipulating a file. |
| [AsynchronousServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousServerSocketChannel) | An asynchronous channel for stream-oriented listening sockets. |
| [AsynchronousSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousSocketChannel) | An asynchronous channel for stream-oriented connecting sockets. |
| [Channels](https://developer.android.com/reference/kotlin/java/nio/channels/Channels) | Utility methods for channels and streams. |
| [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel) | A selectable channel for datagram-oriented sockets. |
| [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel) | A channel for reading, writing, mapping, and manipulating a file. |
| [FileLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock) | A token representing a lock on a region of a file. |
| [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey) | A token representing the membership of an Internet Protocol (IP) multicast group. |
| [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe) | A pair of channels that implements a unidirectional pipe. |
| [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel) | A channel that can be multiplexed via a [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector). |
| [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey) | A token representing the registration of a [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel) with a [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector). |
| [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector) | A multiplexor of [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel) objects. |
| [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel) | A selectable channel for stream-oriented listening sockets. |
| [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) | A selectable channel for stream-oriented connecting sockets. |

## Exceptions

| [AcceptPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/AcceptPendingException) | Unchecked exception thrown when an attempt is made to initiate an accept operation on a channel and a previous accept operation has not completed. |
| [AlreadyBoundException](https://developer.android.com/reference/kotlin/java/nio/channels/AlreadyBoundException) | Unchecked exception thrown when an attempt is made to bind the socket a network oriented channel that is already bound. |
| [AlreadyConnectedException](https://developer.android.com/reference/kotlin/java/nio/channels/AlreadyConnectedException) | Unchecked exception thrown when an attempt is made to connect a [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) that is already connected. |
| [AsynchronousCloseException](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousCloseException) | Checked exception received by a thread when another thread closes the channel or the part of the channel upon which it is blocked in an I/O operation. |
| [CancelledKeyException](https://developer.android.com/reference/kotlin/java/nio/channels/CancelledKeyException) | Unchecked exception thrown when an attempt is made to use a selection key that is no longer valid. |
| [ClosedByInterruptException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedByInterruptException) | Checked exception received by a thread when another thread interrupts it while it is blocked in an I/O operation upon a channel. |
| [ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException) | Checked exception thrown when an attempt is made to invoke or complete an I/O operation upon channel that is closed, or at least closed to that operation. |
| [ClosedSelectorException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedSelectorException) | Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a closed selector. |
| [ConnectionPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/ConnectionPendingException) | Unchecked exception thrown when an attempt is made to connect a [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) for which a non-blocking connection operation is already in progress. |
| [FileLockInterruptionException](https://developer.android.com/reference/kotlin/java/nio/channels/FileLockInterruptionException) | Checked exception received by a thread when another thread interrupts it while it is waiting to acquire a file lock. |
| [IllegalBlockingModeException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalBlockingModeException) | Unchecked exception thrown when a blocking-mode-specific operation is invoked upon a channel in the incorrect blocking mode. |
| [IllegalChannelGroupException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalChannelGroupException) | Unchecked exception thrown when an attempt is made to open a channel in a group that was not created by the same provider. |
| [IllegalSelectorException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalSelectorException) | Unchecked exception thrown when an attempt is made to register a channel with a selector that was not created by the provider that created the channel. |
| [InterruptedByTimeoutException](https://developer.android.com/reference/kotlin/java/nio/channels/InterruptedByTimeoutException) | Checked exception received by a thread when a timeout elapses before an asynchronous operation completes. |
| [NoConnectionPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/NoConnectionPendingException) | Unchecked exception thrown when the [finishConnect](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel#finishConnect())method of a [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) is invoked without first successfully invoking its [connect](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel#connect(java.net.SocketAddress))method. |
| [NonReadableChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/NonReadableChannelException) | Unchecked exception thrown when an attempt is made to read from a channel that was not originally opened for reading. |
| [NonWritableChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/NonWritableChannelException) | Unchecked exception thrown when an attempt is made to write to a channel that was not originally opened for writing. |
| [NotYetBoundException](https://developer.android.com/reference/kotlin/java/nio/channels/NotYetBoundException) | Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a server socket channel that is not yet bound. |
| [NotYetConnectedException](https://developer.android.com/reference/kotlin/java/nio/channels/NotYetConnectedException) | Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a socket channel that is not yet connected. |
| [OverlappingFileLockException](https://developer.android.com/reference/kotlin/java/nio/channels/OverlappingFileLockException) | Unchecked exception thrown when an attempt is made to acquire a lock on a region of a file that overlaps a region already locked by the same Java virtual machine, or when another thread is already waiting to lock an overlapping region of the same file. |
| [ReadPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/ReadPendingException) | Unchecked exception thrown when an attempt is made to read from an asynchronous socket channel and a previous read has not completed. |
| [ShutdownChannelGroupException](https://developer.android.com/reference/kotlin/java/nio/channels/ShutdownChannelGroupException) | Unchecked exception thrown when an attempt is made to construct a channel in a group that is shutdown or the completion handler for an I/O operation cannot be invoked because the channel group has terminated. |
| [UnresolvedAddressException](https://developer.android.com/reference/kotlin/java/nio/channels/UnresolvedAddressException) | Unchecked exception thrown when an attempt is made to invoke a network operation upon an unresolved socket address. |
| [UnsupportedAddressTypeException](https://developer.android.com/reference/kotlin/java/nio/channels/UnsupportedAddressTypeException) | Unchecked exception thrown when an attempt is made to bind or connect to a socket address of a type that is not supported. |
| [WritePendingException](https://developer.android.com/reference/kotlin/java/nio/channels/WritePendingException) | Unchecked exception thrown when an attempt is made to write to an asynchronous socket channel and a previous write has not completed. |
