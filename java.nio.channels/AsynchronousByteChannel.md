# AsynchronousByteChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsynchronousByteChannel

```
interface AsynchronousByteChannel : AsynchronousChannel
```

| [java.nio.channels.AsynchronousByteChannel](AsynchronousByteChannel.md) |

| Known Direct Subclasses [AsynchronousSocketChannel](AsynchronousSocketChannel.md) |-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------| | [AsynchronousSocketChannel](AsynchronousSocketChannel.md) | An asynchronous channel for stream-oriented connecting sockets. | |
| --- | --- | --- | --- | --- | --- | --- |

An asynchronous channel that can read and write bytes.

Some channels may not allow more than one read or write to be outstanding at any given time. If a thread invokes a read method before a previous read operation has completed then a [ReadPendingException](ReadPendingException.md) will be thrown. Similarly, if a write method is invoked before a previous write has completed then [WritePendingException](WritePendingException.md) is thrown. Whether or not other kinds of I/O operations may proceed concurrently with a read operation depends upon the type of the channel.

Note that [ByteBuffers](../java.nio/ByteBuffer.md) are not safe for use by multiple concurrent threads. When a read or write operation is initiated then care must be taken to ensure that the buffer is not accessed until the operation completes.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Future](../java.util.concurrent/Future.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | [read](AsynchronousByteChannel.md))`(`dst:` ` [ByteBuffer](../java.nio/ByteBuffer.md)!`)` Reads a sequence of bytes from this channel into the given buffer. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [read](AsynchronousByteChannel.md))`(`dst:` ` [ByteBuffer](../java.nio/ByteBuffer.md)!`, `attachment:` `A`, `handler:` ` [CompletionHandler](CompletionHandler.md)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` `in` `A>!`)` Reads a sequence of bytes from this channel into the given buffer. |
| abstract [Future](../java.util.concurrent/Future.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | [write](AsynchronousByteChannel.md))`(`src:` ` [ByteBuffer](../java.nio/ByteBuffer.md)!`)` Writes a sequence of bytes to this channel from the given buffer. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](AsynchronousByteChannel.md))`(`src:` ` [ByteBuffer](../java.nio/ByteBuffer.md)!`, `attachment:` `A`, `handler:` ` [CompletionHandler](CompletionHandler.md)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` `in` `A>!`)` Writes a sequence of bytes to this channel from the given buffer. |

| Inherited functions ||
|---|---|
| From class [AsynchronousChannel](AsynchronousChannel.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](AsynchronousChannel.md))`()` <br /> Closes this channel. Any outstanding asynchronous operations upon this channel will complete with the exception [AsynchronousCloseException](AsynchronousCloseException.md). After a channel is closed, further attempts to initiate asynchronous I/O operations complete immediately with cause [ClosedChannelException](ClosedChannelException.md). This method otherwise behaves exactly as specified by the [Channel](Channel.md) interface. <br /> | ||
| From class [Channel](Channel.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](Channel.md))`()` <br /> Tells whether or not this channel is open. <br /> | ||

## Public methods

### read

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(dst: ByteBuffer!): Future<Int!>!
```

Reads a sequence of bytes from this channel into the given buffer.

This method initiates an asynchronous read operation to read a sequence of bytes from this channel into the given buffer. The method behaves in exactly the same manner as the [read(ByteBuffer,Object,CompletionHandler)](AsynchronousByteChannel.md))method except that instead of specifying a completion handler, this method returns a`Future`representing the pending result. The`Future`'s [get](../java.util.concurrent/Future.md))method returns the number of bytes read or`-1`if no bytes could be read because the channel has reached end-of-stream.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [ByteBuffer](../java.nio/ByteBuffer.md)!:The buffer into which bytes are to be transferred |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [Future](../java.util.concurrent/Future.md)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>! | A Future representing the result of the operation |

| Exceptions ||
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the buffer is read-only |
| `java.nio.channels.ReadPendingException` | If the channel does not allow more than one read to be outstanding and a previous read has not completed |

### read

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <A : Any!> read(
    dst: ByteBuffer!, 
    attachment: A, 
    handler: CompletionHandler<Int!, in A>!
): Unit
```

Reads a sequence of bytes from this channel into the given buffer.

This method initiates an asynchronous read operation to read a sequence of bytes from this channel into the given buffer. The`handler`parameter is a completion handler that is invoked when the read operation completes (or fails). The result passed to the completion handler is the number of bytes read or`-1`if no bytes could be read because the channel has reached end-of-stream.

The read operation may read up to*r* bytes from the channel, where*r* is the number of bytes remaining in the buffer, that is,`dst.remaining()`at the time that the read is attempted. Where*r* is 0, the read operation completes immediately with a result of`0`without initiating an I/O operation.

Suppose that a byte sequence of length*n* is read, where`0``<`*n* `<=`*r* . This byte sequence will be transferred into the buffer so that the first byte in the sequence is at index*p* and the last byte is at index*p* `+`*n* `-``1`, where*p* is the buffer's position at the moment the read is performed. Upon completion the buffer's position will be equal to*p* `+`*n*; its limit will not have changed.

Buffers are not safe for use by multiple concurrent threads so care should be taken to not access the buffer until the operation has completed.

This method may be invoked at any time. Some channel types may not allow more than one read to be outstanding at any given time. If a thread initiates a read operation before a previous read operation has completed then a [ReadPendingException](ReadPendingException.md) will be thrown.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<A>` | The type of the attachment |
| `dst` | [ByteBuffer](../java.nio/ByteBuffer.md)!:The buffer into which bytes are to be transferred |
| `attachment` | A:The object to attach to the I/O operation; can be`null` |
| --- | --- |
| `handler` | [CompletionHandler](CompletionHandler.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,inA\>!:The completion handler |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the buffer is read-only |
| `java.nio.channels.ReadPendingException` | If the channel does not allow more than one read to be outstanding and a previous read has not completed |
| `java.nio.channels.ShutdownChannelGroupException` | If the channel is associated with a [group](AsynchronousChannelGroup.md) that has terminated |
| --- | --- |

### write

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(src: ByteBuffer!): Future<Int!>!
```

Writes a sequence of bytes to this channel from the given buffer.

This method initiates an asynchronous write operation to write a sequence of bytes to this channel from the given buffer. The method behaves in exactly the same manner as the [write(ByteBuffer,Object,CompletionHandler)](AsynchronousByteChannel.md))method except that instead of specifying a completion handler, this method returns a`Future`representing the pending result. The`Future`'s [get](../java.util.concurrent/Future.md))method returns the number of bytes written.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](../java.nio/ByteBuffer.md)!:The buffer from which bytes are to be retrieved |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [Future](../java.util.concurrent/Future.md)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>! | A Future representing the result of the operation |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.WritePendingException` | If the channel does not allow more than one write to be outstanding and a previous write has not completed |

### write

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <A : Any!> write(
    src: ByteBuffer!, 
    attachment: A, 
    handler: CompletionHandler<Int!, in A>!
): Unit
```

Writes a sequence of bytes to this channel from the given buffer.

This method initiates an asynchronous write operation to write a sequence of bytes to this channel from the given buffer. The`handler`parameter is a completion handler that is invoked when the write operation completes (or fails). The result passed to the completion handler is the number of bytes written.

The write operation may write up to*r* bytes to the channel, where*r* is the number of bytes remaining in the buffer, that is,`src.remaining()`at the time that the write is attempted. Where*r* is 0, the write operation completes immediately with a result of`0`without initiating an I/O operation.

Suppose that a byte sequence of length*n* is written, where`0``<`*n* `<=`*r* . This byte sequence will be transferred from the buffer starting at index*p* , where*p* is the buffer's position at the moment the write is performed; the index of the last byte written will be*p* `+`*n* `-``1`. Upon completion the buffer's position will be equal to*p* `+`*n*; its limit will not have changed.

Buffers are not safe for use by multiple concurrent threads so care should be taken to not access the buffer until the operation has completed.

This method may be invoked at any time. Some channel types may not allow more than one write to be outstanding at any given time. If a thread initiates a write operation before a previous write operation has completed then a [WritePendingException](WritePendingException.md) will be thrown.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<A>` | The type of the attachment |
| `src` | [ByteBuffer](../java.nio/ByteBuffer.md)!:The buffer from which bytes are to be retrieved |
| `attachment` | A:The object to attach to the I/O operation; can be`null` |
| --- | --- |
| `handler` | [CompletionHandler](CompletionHandler.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,inA\>!:The completion handler object |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.WritePendingException` | If the channel does not allow more than one write to be outstanding and a previous write has not completed |
| `java.nio.channels.ShutdownChannelGroupException` | If the channel is associated with a [group](AsynchronousChannelGroup.md) that has terminated |
