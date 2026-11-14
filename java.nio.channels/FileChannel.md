# FileChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileChannel

```
abstract class FileChannel : AbstractInterruptibleChannel, GatheringByteChannel, ScatteringByteChannel, SeekableByteChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.nio.channels.spi.AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) ||
| | ↳ | [java.nio.channels.FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#) |

A channel for reading, writing, mapping, and manipulating a file.

A file channel is a [SeekableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SeekableByteChannel) that is connected to a file. It has a current*position* within its file which can be both [*queried*](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#position())and [*modified*](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#position(kotlin.Long)). The file itself contains a variable-length sequence of bytes that can be read and written and whose current [*size*](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#size())can be queried. The size of the file increases when bytes are written beyond its current size; the size of the file decreases when it is [*truncated*](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#truncate(kotlin.Long)). The file may also have some associated*metadata*such as access permissions, content type, and last-modification time; this class does not define methods for metadata access.

In addition to the familiar read, write, and close operations of byte channels, this class defines the following file-specific operations:

- Bytes may be [read](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#read(java.nio.ByteBuffer,%20kotlin.Long))or [*written*](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#write(java.nio.ByteBuffer,%20kotlin.Long))at an absolute position in a file in a way that does not affect the channel's current position.
- A region of a file may be [*mapped*](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#map(java.nio.channels.FileChannel.MapMode,%20kotlin.Long,%20kotlin.Long))directly into memory; for large files this is often much more efficient than invoking the usual`read`or`write`methods.
- Updates made to a file may be [*forced*](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#force(kotlin.Boolean))*to the underlying storage device, ensuring that data are not lost in the event of a system crash.*
*- Bytes can be transferred from a file [*to*](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#transferTo(kotlin.Long,%20kotlin.Long,%20java.nio.channels.WritableByteChannel))*, and [*vice*](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#transferFrom(java.nio.channels.ReadableByteChannel,%20kotlin.Long,%20kotlin.Long))*, in a way that can be optimized by many operating systems into a very fast transfer directly to or from the filesystem cache.**
**- A region of a file may be [*locked*](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock) against access by other programs.***

**File channels are safe for use by multiple concurrent threads. The java.nio.channels.Channel#close method may be invoked at any time, as specified by the [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel) interface. Only one operation that involves the channel's position or can change its file's size may be in progress at any given time; attempts to initiate a second such operation while the first is still in progress will block until the first operation completes. Other operations, in particular those that take an explicit position, may proceed concurrently; whether they in fact do so is dependent upon the underlying implementation and is therefore unspecified.
The view of a file provided by an instance of this class is guaranteed to be consistent with other views of the same file provided by other instances in the same program. The view provided by an instance of this class may or may not, however, be consistent with the views seen by other concurrently-running programs due to caching performed by the underlying operating system and delays induced by network-filesystem protocols. This is true regardless of the language in which these other programs are written, and whether they are running on the same machine or on some other machine. The exact nature of any such inconsistencies are system-dependent and are therefore unspecified.
A file channel is created by invoking one of the #open methods defined by this class. A file channel can also be obtained from an existing [FileInputStream](https://developer.android.com/reference/kotlin/java/io/FileInputStream.html#getChannel()), [FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#getChannel()), or [RandomAccessFile](https://developer.android.com/reference/kotlin/java/io/RandomAccessFile.html#getChannel())object by invoking that object's`getChannel`method, which returns a file channel that is connected to the same underlying file. Where the file channel is obtained from an existing stream or random access file then the state of the file channel is intimately connected to that of the object whose`getChannel`method returned the channel. Changing the channel's position, whether explicitly or by reading or writing bytes, will change the file position of the originating object, and vice versa. Changing the file's length via the file channel will change the length seen via the originating object, and vice versa. Changing the file's content by writing bytes will change the content seen by the originating object, and vice versa.
At various points this class specifies that an instance that is "open for reading," "open for writing," or "open for reading and writing" is required. A channel obtained via the [getChannel](https://developer.android.com/reference/kotlin/java/io/FileInputStream.html#getChannel())method of a instance will be open for reading. A channel obtained via the [getChannel](https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#getChannel())method of a [java.io.FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#) instance will be open for writing. Finally, a channel obtained via the [getChannel](https://developer.android.com/reference/kotlin/java/io/RandomAccessFile.html#getChannel())method of a instance will be open for reading if the instance was created with mode`"r"`and will be open for reading and writing if the instance was created with mode`"rw"`.
A file channel that is open for writing may be in*append mode* , for example if it was obtained from a file-output stream that was created by invoking the [FileOutputStream(File,boolean)](https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#FileOutputStream(java.io.File,%20kotlin.Boolean))constructor and passing`true`for the second parameter. In this mode each invocation of a relative write operation first advances the position to the end of the file and then writes the requested data. Whether the advancement of the position and the writing of the data are done in a single atomic operation is system-dependent and therefore unspecified.**

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [MapMode](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode) A typesafe enumeration for file-mapping modes. |

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#FileChannel())`()` Initializes a new instance of this class. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [force](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#force(kotlin.Boolean))`(`metaData:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Forces any updates to this channel's file to be written to the storage device that contains it. |
| [FileLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock)! | [lock](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#lock())`()` Acquires an exclusive lock on this channel's file. |
| abstract [FileLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock)! | [lock](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#lock(kotlin.Long,%20kotlin.Long,%20kotlin.Boolean))`(`position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `shared:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Acquires a lock on the given region of this channel's file. |
| --- | --- |
| abstract [MappedByteBuffer](https://developer.android.com/reference/kotlin/java/nio/MappedByteBuffer.html#)! | [map](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#map(java.nio.channels.FileChannel.MapMode,%20kotlin.Long,%20kotlin.Long))`(`mode:` ` [FileChannel.MapMode](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode)!`, `position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Maps a region of this channel's file directly into memory. |
| openstatic [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#)! | [open](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#open(java.nio.file.Path,%20java.nio.file.OpenOption))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `vararg` `options:` ` [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!`)` Opens or creates a file, returning a file channel to access the file. |
| openstatic [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#)! | [open](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#open(java.nio.file.Path,%20kotlin.collections.MutableSet,%20java.nio.file.attribute.FileAttribute))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `options:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<out` ` [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!>!`, `vararg` `attrs:` ` [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#)<*>!`)` Opens or creates a file, returning a file channel to access the file. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [position](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#position())`()` Returns this channel's file position. |
| abstract [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#)! | [position](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#position(kotlin.Long))`(`newPosition:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets this channel's file position. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#read(java.nio.ByteBuffer))`(`dst:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Reads a sequence of bytes from this channel into the given buffer. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#read(java.nio.ByteBuffer,%20kotlin.Long))`(`dst:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`, `position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Reads a sequence of bytes from this channel into the given buffer, starting at the given file position. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [read](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#read(kotlin.Array))`(`dsts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`)` Reads a sequence of bytes from this channel into the given buffers. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [read](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#read(kotlin.Array,%20kotlin.Int,%20kotlin.Int))`(`dsts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads a sequence of bytes from this channel into a subsequence of the given buffers. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [size](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#size())`()` Returns the current size of this channel's file. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferFrom](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#transferFrom(java.nio.channels.ReadableByteChannel,%20kotlin.Long,%20kotlin.Long))`(`src:` ` [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel)!`, `position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `count:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Transfers bytes into this channel's file from the given readable byte channel. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#transferTo(kotlin.Long,%20kotlin.Long,%20java.nio.channels.WritableByteChannel))`(`position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `count:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `target:` ` [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel)!`)` Transfers bytes from this channel's file to the given writable byte channel. |
| --- | --- |
| abstract [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#)! | [truncate](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#truncate(kotlin.Long))`(`size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Truncates this channel's file to the given size. |
| [FileLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock)! | [tryLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#tryLock())`()` Attempts to acquire an exclusive lock on this channel's file. |
| abstract [FileLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock)! | [tryLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#tryLock(kotlin.Long,%20kotlin.Long,%20kotlin.Boolean))`(`position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `shared:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Attempts to acquire a lock on the given region of this channel's file. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [write](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#write(java.nio.ByteBuffer))`(`src:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Writes a sequence of bytes to this channel from the given buffer. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [write](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#write(java.nio.ByteBuffer,%20kotlin.Long))`(`src:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`, `position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Writes a sequence of bytes to this channel from the given buffer, starting at the given file position. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [write](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#write(kotlin.Array))`(`srcs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`)` Writes a sequence of bytes to this channel from the given buffers. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [write](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#write(kotlin.Array,%20kotlin.Int,%20kotlin.Int))`(`srcs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a sequence of bytes to this channel from a subsequence of the given buffers. |

| Inherited functions ||
|---|---|
| From class [AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())`()` <br /> Marks the beginning of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#be), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#close())`()` <br /> Closes this channel. If the channel has already been closed then this method returns immediately. Otherwise it marks the channel as closed and then invokes the [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())method in order to complete the close operation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))`(`completed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Marks the end of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#be), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())`()` <br /> Closes this channel. This method is invoked by the #close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once. An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#isOpen())`()` <br /> | ||

## Protected constructors

### FileChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected FileChannel()
```

Initializes a new instance of this class.

## Public methods

### force

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun force(metaData: Boolean): Unit
```

Forces any updates to this channel's file to be written to the storage device that contains it.

If this channel's file resides on a local storage device then when this method returns it is guaranteed that all changes made to the file since this channel was created, or since this method was last invoked, will have been written to that device. This is useful for ensuring that critical information is not lost in the event of a system crash.

If the file does not reside on a local device then no such guarantee is made.

The`metaData`parameter can be used to limit the number of I/O operations that this method is required to perform. Passing`false`for this parameter indicates that only updates to the file's content need be written to storage; passing`true`indicates that updates to both the file's content and metadata must be written, which generally requires at least one more I/O operation. Whether this parameter actually has any effect is dependent upon the underlying operating system and is therefore unspecified.

Invoking this method may cause an I/O operation to occur even if the channel was only opened for reading. Some operating systems, for example, maintain a last-access time as part of a file's metadata, and this time is updated whenever the file is read. Whether or not this is actually done is system-dependent and is therefore unspecified.

This method is only guaranteed to force changes that were made to this channel's file via the methods defined in this class. It may or may not force changes that were made by modifying the content of a [*mapped byte buffer*](https://developer.android.com/reference/kotlin/java/nio/MappedByteBuffer.html#) obtained by invoking the [map](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#map(java.nio.channels.FileChannel.MapMode,%20kotlin.Long,%20kotlin.Long))method. Invoking the java.nio.MappedByteBuffer#force method of the mapped byte buffer will force changes made to the buffer's content to be written.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `metaData` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If`true`then this method is required to force changes to both the file's content and metadata to be written to storage; otherwise, it need only force content changes to be written |

| Exceptions ||
|--------------------------------------------|--------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If some other I/O error occurs |

### lock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lock(): FileLock!
```

Acquires an exclusive lock on this channel's file.

An invocation of this method of the form`fc.lock()`behaves in exactly the same way as the invocation 

```kotlin
fc.<code><a docref="java.nio.channels.FileChannel$lock(kotlin.Long, kotlin.Long, kotlin.Boolean)">lock</a></code>(0L, Long.MAX_VALUE, false) 
```

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------|
| [FileLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock)! | A lock object representing the newly-acquired lock |

| Exceptions ||
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the invoking thread is blocked in this method |
| `java.nio.channels.FileLockInterruptionException` | If the invoking thread is interrupted while blocked in this method |
| --- | --- |
| `java.nio.channels.OverlappingFileLockException` | If a lock that overlaps the requested region is already held by this Java virtual machine, or if another thread is already blocked in this method and is attempting to lock an overlapping region of the same file |
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

**See Also**

- [#lock(long,long,boolean)](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#lock(kotlin.Long,%20kotlin.Long,%20kotlin.Boolean))
- <https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#tryLock()>
- [#tryLock(long,long,boolean)](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#tryLock(kotlin.Long,%20kotlin.Long,%20kotlin.Boolean)) 

### lock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lock(
    position: Long, 
    size: Long, 
    shared: Boolean
): FileLock!
```

Acquires a lock on the given region of this channel's file.

An invocation of this method will block until the region can be locked, this channel is closed, or the invoking thread is interrupted, whichever comes first.

If this channel is closed by another thread during an invocation of this method then an [AsynchronousCloseException](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousCloseException) will be thrown.

If the invoking thread is interrupted while waiting to acquire the lock then its interrupt status will be set and a [FileLockInterruptionException](https://developer.android.com/reference/kotlin/java/nio/channels/FileLockInterruptionException) will be thrown. If the invoker's interrupt status is set when this method is invoked then that exception will be thrown immediately; the thread's interrupt status will not be changed.

The region specified by the`position`and`size`parameters need not be contained within, or even overlap, the actual underlying file. Lock regions are fixed in size; if a locked region initially contains the end of the file and the file grows beyond the region then the new portion of the file will not be covered by the lock. If a file is expected to grow in size and a lock on the entire file is required then a region starting at zero, and no smaller than the expected maximum size of the file, should be locked. The zero-argument [lock()](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#lock())method simply locks a region of size [java.lang.Long#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Long.html#MAX_VALUE:kotlin.Long).

Some operating systems do not support shared locks, in which case a request for a shared lock is automatically converted into a request for an exclusive lock. Whether the newly-acquired lock is shared or exclusive may be tested by invoking the resulting lock object's [isShared](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#isShared())method.

File locks are held on behalf of the entire Java virtual machine. They are not suitable for controlling access to a file by multiple threads within the same virtual machine.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The position at which the locked region is to start; must be non-negative |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The size of the locked region; must be non-negative, and the sum`position`+`size`must be non-negative |
| `shared` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to request a shared lock, in which case this channel must be open for reading (and possibly writing);`false`to request an exclusive lock, in which case this channel must be open for writing (and possibly reading) |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------|
| [FileLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock)! | A lock object representing the newly-acquired lock |

| Exceptions ||
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the invoking thread is blocked in this method |
| --- | --- |
| `java.nio.channels.FileLockInterruptionException` | If the invoking thread is interrupted while blocked in this method |
| `java.nio.channels.OverlappingFileLockException` | If a lock that overlaps the requested region is already held by this Java virtual machine, or if another thread is already blocked in this method and is attempting to lock an overlapping region |
| `java.nio.channels.NonReadableChannelException` | If`shared`is`true`this channel was not opened for reading |
| --- | --- |
| `java.nio.channels.NonWritableChannelException` | If`shared`is`false`but this channel was not opened for writing |
| `java.io.IOException` | If some other I/O error occurs |

**See Also**

- <https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#lock()>
- <https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#tryLock()>
- [#tryLock(long,long,boolean)](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#tryLock(kotlin.Long,%20kotlin.Long,%20kotlin.Boolean)) 

### map

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun map(
    mode: FileChannel.MapMode!, 
    position: Long, 
    size: Long
): MappedByteBuffer!
```

Maps a region of this channel's file directly into memory.

A region of a file may be mapped into memory in one of three modes:

- *Read-only:* Any attempt to modify the resulting buffer will cause a [java.nio.ReadOnlyBufferException](https://developer.android.com/reference/kotlin/java/nio/ReadOnlyBufferException.html#) to be thrown. ([MapMode.READ_ONLY](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode#READ_ONLY:java.nio.channels.FileChannel.MapMode))
- *Read/write:* Changes made to the resulting buffer will eventually be propagated to the file; they may or may not be made visible to other programs that have mapped the same file. ([MapMode.READ_WRITE](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode#READ_WRITE:java.nio.channels.FileChannel.MapMode))
- *Private:* Changes made to the resulting buffer will not be propagated to the file and will not be visible to other programs that have mapped the same file; instead, they will cause private copies of the modified portions of the buffer to be created. ([MapMode.PRIVATE](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode#PRIVATE:java.nio.channels.FileChannel.MapMode))

For a read-only mapping, this channel must have been opened for reading; for a read/write or private mapping, this channel must have been opened for both reading and writing.

The [*mapped byte buffer*](https://developer.android.com/reference/kotlin/java/nio/MappedByteBuffer.html#) returned by this method will have a position of zero and a limit and capacity of`size`; its mark will be undefined. The buffer and the mapping that it represents will remain valid until the buffer itself is garbage-collected.

A mapping, once established, is not dependent upon the file channel that was used to create it. Closing the channel, in particular, has no effect upon the validity of the mapping.

Many of the details of memory-mapped files are inherently dependent upon the underlying operating system and are therefore unspecified. The behavior of this method when the requested region is not completely contained within this channel's file is unspecified. Whether changes made to the content or size of the underlying file, by this program or another, are propagated to the buffer is unspecified. The rate at which changes to the buffer are propagated to the file is unspecified.

For most operating systems, mapping a file into memory is more expensive than reading or writing a few tens of kilobytes of data via the usual #read and #write methods. From the standpoint of performance it is generally only worth mapping relatively large files into memory.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [FileChannel.MapMode](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode)!:One of the constants [READ_ONLY](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode#READ_ONLY:java.nio.channels.FileChannel.MapMode), [READ_WRITE](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode#READ_WRITE:java.nio.channels.FileChannel.MapMode), or [PRIVATE](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode#PRIVATE:java.nio.channels.FileChannel.MapMode) defined in the [MapMode](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode) class, according to whether the file is to be mapped read-only, read/write, or privately (copy-on-write), respectively |
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The position within the file at which the mapped region is to start; must be non-negative |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The size of the region to be mapped; must be non-negative and no greater than [java.lang.Integer#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int) |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------|
| [MappedByteBuffer](https://developer.android.com/reference/kotlin/java/nio/MappedByteBuffer.html#)! | The mapped byte buffer |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonReadableChannelException` | If the`mode`is [READ_ONLY](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode#READ_ONLY:java.nio.channels.FileChannel.MapMode) but this channel was not opened for reading |
| `java.nio.channels.NonWritableChannelException` | If the`mode`is [READ_WRITE](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode#READ_WRITE:java.nio.channels.FileChannel.MapMode) or [PRIVATE](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode#PRIVATE:java.nio.channels.FileChannel.MapMode) but this channel was not opened for both reading and writing |
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |
| --- | --- |
| `java.io.IOException` | If some other I/O error occurs |

**See Also**

- [java.nio.channels.FileChannel.MapMode](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.MapMode)
- [java.nio.MappedByteBuffer](https://developer.android.com/reference/kotlin/java/nio/MappedByteBuffer.html#) 

### open

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(
    path: Path!, 
    vararg options: OpenOption!
): FileChannel!
```

Opens or creates a file, returning a file channel to access the file.

An invocation of this method behaves in exactly the same way as the invocation 

```kotlin
fc.<code><a docref="java.nio.channels.FileChannel$open(java.nio.file.Path, kotlin.collections.MutableSet((java.nio.file.OpenOption)), kotlin.Array((java.nio.file.attribute.FileAttribute((kotlin.Any)))))">open</a></code>(file, opts, new FileAttribute<?>[0]);
  
```
where`opts`is a set of the options specified in the`options`array.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:The path of the file to open or create |
| `options` | [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!:Options specifying how the file is opened |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------|
| [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#)! | A new file channel |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the set contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | If the`path`is associated with a provider that does not support creating file channels, or an unsupported open option is specified |
| `java.io.IOException` | If an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | If a security manager is installed and it denies an unspecified permission required by the implementation. In the case of the default provider, the [java.lang.SecurityManager#checkRead(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access if the file is opened for reading. The [java.lang.SecurityManager#checkWrite(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method is invoked to check write access if the file is opened for writing |

### open

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(
    path: Path!, 
    options: MutableSet<out OpenOption!>!, 
    vararg attrs: FileAttribute<*>!
): FileChannel!
```

Opens or creates a file, returning a file channel to access the file.

The`options`parameter determines how the file is opened. The [READ](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption.html#) and [WRITE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption.html#) options determine if the file should be opened for reading and/or writing. If neither option (or the [APPEND](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption.html#) option) is contained in the array then the file is opened for reading. By default reading or writing commences at the beginning of the file.

In the addition to`READ`and`WRITE`, the following options may be present:

| Option | Description |
| --- | --- |
| [APPEND](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption.html#) | If this option is present then the file is opened for writing and each invocation of the channel's`write`method first advances the position to the end of the file and then writes the requested data. Whether the advancement of the position and the writing of the data are done in a single atomic operation is system-dependent and therefore unspecified. This option may not be used in conjunction with the`READ`or`TRUNCATE_EXISTING`options. |
| [TRUNCATE_EXISTING](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption.html#) | If this option is present then the existing file is truncated to a size of 0 bytes. This option is ignored when the file is opened only for reading. |
| [CREATE_NEW](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption.html#) | If this option is present then a new file is created, failing if the file already exists. When creating a file the check for the existence of the file and the creation of the file if it does not exist is atomic with respect to other file system operations. This option is ignored when the file is opened only for reading. |
| --- | --- |
| [CREATE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption.html#) | If this option is present then an existing file is opened if it exists, otherwise a new file is created. When creating a file the check for the existence of the file and the creation of the file if it does not exist is atomic with respect to other file system operations. This option is ignored if the`CREATE_NEW`option is also present or the file is opened only for reading. |
| [DELETE_ON_CLOSE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption.html#) | When this option is present then the implementation makes a*best effort* attempt to delete the file when closed by the #close method. If the`close`method is not invoked then a*best effort*attempt is made to delete the file when the Java virtual machine terminates. |
| [SPARSE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption.html#) | When creating a new file this option is a*hint*that the new file will be sparse. This option is ignored when not creating a new file. |
| --- | --- |
| [SYNC](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption.html#) | Requires that every update to the file's content or metadata be written synchronously to the underlying storage device. (see [Synchronized I/O file integrity](https://developer.android.com/reference/kotlin/java/nio/file/package-summary.html#integrity)). |
| [DSYNC](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption.html#) | Requires that every update to the file's content be written synchronously to the underlying storage device. (see [Synchronized I/O file integrity](https://developer.android.com/reference/kotlin/java/nio/file/package-summary.html#integrity)). |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

An implementation may also support additional options.

The`attrs`parameter is an optional array of file [file-attributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#) to set atomically when creating the file.

The new channel is created by invoking the [newFileChannel](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider.html#newFileChannel(java.nio.file.Path,%20kotlin.collections.MutableSet,%20java.nio.file.attribute.FileAttribute))method on the provider that created the`Path`.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:The path of the file to open or create |
| `options` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<out [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!\>!:Options specifying how the file is opened |
| `attrs` | [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#)\<\*\>!:An optional list of file attributes to set atomically when creating the file |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------|
| [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#)! | A new file channel |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the set contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | If the`path`is associated with a provider that does not support creating file channels, or an unsupported open option is specified, or the array contains an attribute that cannot be set atomically when creating the file |
| `java.io.IOException` | If an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | If a security manager is installed and it denies an unspecified permission required by the implementation. In the case of the default provider, the [java.lang.SecurityManager#checkRead(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access if the file is opened for reading. The [java.lang.SecurityManager#checkWrite(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method is invoked to check write access if the file is opened for writing |

### position

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun position(): Long
```

Returns this channel's file position.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | This channel's file position, a non-negative integer counting the number of bytes from the beginning of the file to the current position |

| Exceptions ||
|--------------------------------------------|--------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If some other I/O error occurs |

### position

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun position(newPosition: Long): FileChannel!
```

Sets this channel's file position.

Setting the position to a value that is greater than the file's current size is legal but does not change the size of the file. A later attempt to read bytes at such a position will immediately return an end-of-file indication. A later attempt to write bytes at such a position will cause the file to be grown to accommodate the new bytes; the values of any bytes between the previous end-of-file and the newly-written bytes are unspecified.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newPosition` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The new position, a non-negative integer counting the number of bytes from the beginning of the file |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------|
| [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#)! | This file channel |

| Exceptions ||
|--------------------------------------------|---------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.lang.IllegalArgumentException` | If the new position is negative |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(dst: ByteBuffer!): Int
```

Reads a sequence of bytes from this channel into the given buffer.

Bytes are read starting at this channel's current file position, and then the file position is updated with the number of bytes actually read. Otherwise this method behaves exactly as specified in the [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel) interface.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:The buffer into which bytes are to be transferred |

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

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(
    dst: ByteBuffer!, 
    position: Long
): Int
```

Reads a sequence of bytes from this channel into the given buffer, starting at the given file position.

This method works in the same manner as the [read(java.nio.ByteBuffer)](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#read(java.nio.ByteBuffer))method, except that bytes are read starting at the given file position rather than at the channel's current position. This method does not modify this channel's position. If the given position is greater than the file's current size then no bytes are read.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:The buffer into which bytes are to be transferred |
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The file position at which the transfer is to begin; must be non-negative |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes read, possibly zero, or`-1`if the given position is greater than or equal to the file's current size |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the position is negative |
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun read(dsts: Array<ByteBuffer!>!): Long
```

Reads a sequence of bytes from this channel into the given buffers.

Bytes are read starting at this channel's current file position, and then the file position is updated with the number of bytes actually read. Otherwise this method behaves exactly as specified in the [ScatteringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel) interface.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dsts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!:The buffers into which bytes are to be transferred |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes read, possibly zero, or`-1`if the channel has reached end-of-stream |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(
    dsts: Array<ByteBuffer!>!, 
    offset: Int, 
    length: Int
): Long
```

Reads a sequence of bytes from this channel into a subsequence of the given buffers.

Bytes are read starting at this channel's current file position, and then the file position is updated with the number of bytes actually read. Otherwise this method behaves exactly as specified in the [ScatteringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel) interface.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dsts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!:The buffers into which bytes are to be transferred |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the buffer array of the first buffer into which bytes are to be transferred; must be non-negative and no larger than`dsts.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of buffers to be accessed; must be non-negative and no larger than`dsts.length`-`offset` |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes read, possibly zero, or`-1`if the channel has reached end-of-stream |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun size(): Long
```

Returns the current size of this channel's file.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The current size of this channel's file, measured in bytes |

| Exceptions ||
|--------------------------------------------|--------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If some other I/O error occurs |

### transferFrom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun transferFrom(
    src: ReadableByteChannel!, 
    position: Long, 
    count: Long
): Long
```

Transfers bytes into this channel's file from the given readable byte channel.

An attempt is made to read up to`count`bytes from the source channel and write them to this channel's file starting at the given`position`. An invocation of this method may or may not transfer all of the requested bytes; whether or not it does so depends upon the natures and states of the channels. Fewer than the requested number of bytes will be transferred if the source channel has fewer than`count`bytes remaining, or if the source channel is non-blocking and has fewer than`count`bytes immediately available in its input buffer.

This method does not modify this channel's position. If the given position is greater than the file's current size then no bytes are transferred. If the source channel has a position then bytes are read starting at that position and then the position is incremented by the number of bytes read.

This method is potentially much more efficient than a simple loop that reads from the source channel and writes to this channel. Many operating systems can transfer bytes directly from the source channel into the filesystem cache without actually copying them.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel)!:The source channel |
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The position within the file at which the transfer is to begin; must be non-negative |
| `count` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The maximum number of bytes to be transferred; must be non-negative |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes, possibly zero, that were actually transferred |

| Exceptions ||
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |
| `java.nio.channels.NonReadableChannelException` | If the source channel was not opened for reading |
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| --- | --- |
| `java.nio.channels.ClosedChannelException` | If either this channel or the source channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes either channel while the transfer is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the transfer is in progress, thereby closing both channels and setting the current thread's interrupt status |
| --- | --- |
| `java.io.IOException` | If some other I/O error occurs |

### transferTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun transferTo(
    position: Long, 
    count: Long, 
    target: WritableByteChannel!
): Long
```

Transfers bytes from this channel's file to the given writable byte channel.

An attempt is made to read up to`count`bytes starting at the given`position`in this channel's file and write them to the target channel. An invocation of this method may or may not transfer all of the requested bytes; whether or not it does so depends upon the natures and states of the channels. Fewer than the requested number of bytes are transferred if this channel's file contains fewer than`count`bytes starting at the given`position`, or if the target channel is non-blocking and it has fewer than`count`bytes free in its output buffer.

This method does not modify this channel's position. If the given position is greater than the file's current size then no bytes are transferred. If the target channel has a position then bytes are written starting at that position and then the position is incremented by the number of bytes written.

This method is potentially much more efficient than a simple loop that reads from this channel and writes to the target channel. Many operating systems can transfer bytes directly from the filesystem cache to the target channel without actually copying them.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The position within the file at which the transfer is to begin; must be non-negative |
| `count` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The maximum number of bytes to be transferred; must be non-negative |
| `target` | [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel)!:The target channel |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes, possibly zero, that were actually transferred |

| Exceptions ||
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.NonWritableChannelException` | If the target channel was not opened for writing |
| --- | --- |
| `java.nio.channels.ClosedChannelException` | If either this channel or the target channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes either channel while the transfer is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the transfer is in progress, thereby closing both channels and setting the current thread's interrupt status |
| --- | --- |
| `java.io.IOException` | If some other I/O error occurs |

### truncate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun truncate(size: Long): FileChannel!
```

Truncates this channel's file to the given size.

If the given size is less than the file's current size then the file is truncated, discarding any bytes beyond the new end of the file. If the given size is greater than or equal to the file's current size then the file is not modified. In either case, if this channel's file position is greater than the given size then it is set to that size.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The new size, a non-negative byte count |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------|
| [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#)! | This file channel |

| Exceptions ||
|-------------------------------------------------|--------------------------------------------|
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.lang.IllegalArgumentException` | If the new size is negative |
| --- | --- |
| `java.io.IOException` | If some other I/O error occurs |

### tryLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun tryLock(): FileLock!
```

Attempts to acquire an exclusive lock on this channel's file.

An invocation of this method of the form`fc.tryLock()`behaves in exactly the same way as the invocation 

```kotlin
fc.<code><a docref="java.nio.channels.FileChannel$tryLock(kotlin.Long, kotlin.Long, kotlin.Boolean)">tryLock</a></code>(0L, Long.MAX_VALUE, false) 
```

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [FileLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock)! | A lock object representing the newly-acquired lock, or`null`if the lock could not be acquired because another program holds an overlapping lock |

| Exceptions ||
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.OverlappingFileLockException` | If a lock that overlaps the requested region is already held by this Java virtual machine, or if another thread is already blocked in this method and is attempting to lock an overlapping region |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

**See Also**

- <https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#lock()>
- [#lock(long,long,boolean)](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#lock(kotlin.Long,%20kotlin.Long,%20kotlin.Boolean))
- [#tryLock(long,long,boolean)](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#tryLock(kotlin.Long,%20kotlin.Long,%20kotlin.Boolean)) 

### tryLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun tryLock(
    position: Long, 
    size: Long, 
    shared: Boolean
): FileLock!
```

Attempts to acquire a lock on the given region of this channel's file.

This method does not block. An invocation always returns immediately, either having acquired a lock on the requested region or having failed to do so. If it fails to acquire a lock because an overlapping lock is held by another program then it returns`null`. If it fails to acquire a lock for any other reason then an appropriate exception is thrown.

The region specified by the`position`and`size`parameters need not be contained within, or even overlap, the actual underlying file. Lock regions are fixed in size; if a locked region initially contains the end of the file and the file grows beyond the region then the new portion of the file will not be covered by the lock. If a file is expected to grow in size and a lock on the entire file is required then a region starting at zero, and no smaller than the expected maximum size of the file, should be locked. The zero-argument [tryLock()](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#tryLock())method simply locks a region of size [java.lang.Long#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Long.html#MAX_VALUE:kotlin.Long).

Some operating systems do not support shared locks, in which case a request for a shared lock is automatically converted into a request for an exclusive lock. Whether the newly-acquired lock is shared or exclusive may be tested by invoking the resulting lock object's [isShared](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#isShared())method.

File locks are held on behalf of the entire Java virtual machine. They are not suitable for controlling access to a file by multiple threads within the same virtual machine.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The position at which the locked region is to start; must be non-negative |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The size of the locked region; must be non-negative, and the sum`position`+`size`must be non-negative |
| `shared` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to request a shared lock,`false`to request an exclusive lock |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [FileLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock)! | A lock object representing the newly-acquired lock, or`null`if the lock could not be acquired because another program holds an overlapping lock |

| Exceptions ||
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.OverlappingFileLockException` | If a lock that overlaps the requested region is already held by this Java virtual machine, or if another thread is already blocked in this method and is attempting to lock an overlapping region of the same file |
| --- | --- |
| `java.io.IOException` | If some other I/O error occurs |

**See Also**

- <https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#lock()>
- [#lock(long,long,boolean)](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#lock(kotlin.Long,%20kotlin.Long,%20kotlin.Boolean))
- <https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#tryLock()> 

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(src: ByteBuffer!): Int
```

Writes a sequence of bytes to this channel from the given buffer.

Bytes are written starting at this channel's current file position unless the channel is in append mode, in which case the position is first advanced to the end of the file. The file is grown, if necessary, to accommodate the written bytes, and then the file position is updated with the number of bytes actually written. Otherwise this method behaves exactly as specified by the [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel) interface.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:The buffer from which bytes are to be retrieved |

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

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(
    src: ByteBuffer!, 
    position: Long
): Int
```

Writes a sequence of bytes to this channel from the given buffer, starting at the given file position.

This method works in the same manner as the [write(java.nio.ByteBuffer)](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#write(java.nio.ByteBuffer))method, except that bytes are written starting at the given file position rather than at the channel's current position. This method does not modify this channel's position. If the given position is greater than the file's current size then the file will be grown to accommodate the new bytes; the values of any bytes between the previous end-of-file and the newly-written bytes are unspecified.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:The buffer from which bytes are to be transferred |
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The file position at which the transfer is to begin; must be non-negative |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes written, possibly zero |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the position is negative |
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun write(srcs: Array<ByteBuffer!>!): Long
```

Writes a sequence of bytes to this channel from the given buffers.

Bytes are written starting at this channel's current file position unless the channel is in append mode, in which case the position is first advanced to the end of the file. The file is grown, if necessary, to accommodate the written bytes, and then the file position is updated with the number of bytes actually written. Otherwise this method behaves exactly as specified in the [GatheringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/GatheringByteChannel) interface.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `srcs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!:The buffers from which bytes are to be retrieved |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes written, possibly zero |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(
    srcs: Array<ByteBuffer!>!, 
    offset: Int, 
    length: Int
): Long
```

Writes a sequence of bytes to this channel from a subsequence of the given buffers.

Bytes are written starting at this channel's current file position unless the channel is in append mode, in which case the position is first advanced to the end of the file. The file is grown, if necessary, to accommodate the written bytes, and then the file position is updated with the number of bytes actually written. Otherwise this method behaves exactly as specified in the [GatheringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/GatheringByteChannel) interface.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `srcs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!:The buffers from which bytes are to be retrieved |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the buffer array of the first buffer from which bytes are to be retrieved; must be non-negative and no larger than`srcs.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of buffers to be accessed; must be non-negative and no larger than`srcs.length`-`offset` |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes written, possibly zero |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |
