# SeekableByteChannel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SeekableByteChannel

```
interface SeekableByteChannel : ByteChannel
```

| [java.nio.channels.SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md) |

| Known Direct Subclasses [FileChannel](../java/nio/channels/FileChannel.md) |---------------------------------------------------------------------------------------------|-------------------------------------------------------------------| | [FileChannel](../java/nio/channels/FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. | |
| --- | --- | --- | --- | --- | --- | --- |

A byte channel that maintains a current*position*and allows the position to be changed.

A seekable byte channel is connected to an entity, typically a file, that contains a variable-length sequence of bytes that can be read and written. The current position can be [*queried*](../java/nio/channels/SeekableByteChannel.md))and [*modified*](../java/nio/channels/SeekableByteChannel.md)). The channel also provides access to the current*size* of the entity to which the channel is connected. The size increases when bytes are written beyond its current size; the size decreases when it is [*truncated*](../java/nio/channels/SeekableByteChannel.md)).

The [position](../java/nio/channels/SeekableByteChannel.md))and [truncate](../java/nio/channels/SeekableByteChannel.md))methods which do not otherwise have a value to return are specified to return the channel upon which they are invoked. This allows method invocations to be chained. Implementations of this interface should specialize the return type so that method invocations on the implementation class can be chained.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [position](../java/nio/channels/SeekableByteChannel.md))`()` Returns this channel's position. |
| abstract [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md)! | [position](../java/nio/channels/SeekableByteChannel.md))`(`newPosition:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets this channel's position. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](../java/nio/channels/SeekableByteChannel.md))`(`dst:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` Reads a sequence of bytes from this channel into the given buffer. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [size](../java/nio/channels/SeekableByteChannel.md))`()` Returns the current size of entity to which this channel is connected. |
| abstract [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md)! | [truncate](../java/nio/channels/SeekableByteChannel.md))`(`size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Truncates the entity, to which this channel is connected, to the given size. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [write](../java/nio/channels/SeekableByteChannel.md))`(`src:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` Writes a sequence of bytes to this channel from the given buffer. |
| --- | --- |

## Public methods

### position

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun position(): Long
```

Returns this channel's position.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | This channel's position, a non-negative integer counting the number of bytes from the beginning of the entity to the current position |

| Exceptions ||
|--------------------------------------------|--------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If some other I/O error occurs |

### position

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun position(newPosition: Long): SeekableByteChannel!
```

Sets this channel's position.

Setting the position to a value that is greater than the current size is legal but does not change the size of the entity. A later attempt to read bytes at such a position will immediately return an end-of-file indication. A later attempt to write bytes at such a position will cause the entity to grow to accommodate the new bytes; the values of any bytes between the previous end-of-file and the newly-written bytes are unspecified.

Setting the channel's position is not recommended when connected to an entity, typically a file, that is opened with the [APPEND](../java/nio/file/StandardOpenOption.md) option. When opened for append, the position is first advanced to the end before writing.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newPosition` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The new position, a non-negative integer counting the number of bytes from the beginning of the entity |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------|
| [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md)! | This channel |

| Exceptions ||
|--------------------------------------------|---------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.lang.IllegalArgumentException` | If the new position is negative |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

### read

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(dst: ByteBuffer!): Int
```

Reads a sequence of bytes from this channel into the given buffer.

Bytes are read starting at this channel's current position, and then the position is updated with the number of bytes actually read. Otherwise this method behaves exactly as specified in the [ReadableByteChannel](../java/nio/channels/ReadableByteChannel.md) interface.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [ByteBuffer](../java/nio/ByteBuffer.md)!:The buffer into which bytes are to be transferred |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes read, possibly zero, or`-1`if the channel has reached end-of-stream |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |

### size

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun size(): Long
```

Returns the current size of entity to which this channel is connected.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The current size, measured in bytes |

| Exceptions ||
|--------------------------------------------|--------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If some other I/O error occurs |

### truncate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun truncate(size: Long): SeekableByteChannel!
```

Truncates the entity, to which this channel is connected, to the given size.

If the given size is less than the current size then the entity is truncated, discarding any bytes beyond the new end. If the given size is greater than or equal to the current size then the entity is not modified. In either case, if the current position is greater than the given size then it is set to that size.

An implementation of this interface may prohibit truncation when connected to an entity, typically a file, opened with the [APPEND](../java/nio/file/StandardOpenOption.md) option.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The new size, a non-negative byte count |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------|
| [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md)! | This channel |

| Exceptions ||
|-------------------------------------------------|--------------------------------------------|
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.lang.IllegalArgumentException` | If the new size is negative |
| --- | --- |
| `java.io.IOException` | If some other I/O error occurs |

### write

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(src: ByteBuffer!): Int
```

Writes a sequence of bytes to this channel from the given buffer.

Bytes are written starting at this channel's current position, unless the channel is connected to an entity such as a file that is opened with the [APPEND](../java/nio/file/StandardOpenOption.md) option, in which case the position is first advanced to the end. The entity to which the channel is connected is grown, if necessary, to accommodate the written bytes, and then the position is updated with the number of bytes actually written. Otherwise this method behaves exactly as specified by the [WritableByteChannel](../java/nio/channels/WritableByteChannel.md) interface.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](../java/nio/ByteBuffer.md)!:The buffer from which bytes are to be retrieved |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes written, possibly zero |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
