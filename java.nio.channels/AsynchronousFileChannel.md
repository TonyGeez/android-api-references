# AsynchronousFileChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsynchronousFileChannel

```
abstract class AsynchronousFileChannel : AsynchronousChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.channels.AsynchronousFileChannel](AsynchronousFileChannel.md) |

An asynchronous channel for reading, writing, and manipulating a file.

An asynchronous file channel is created when a file is opened by invoking one of the #open methods defined by this class. The file contains a variable-length sequence of bytes that can be read and written and whose current size can be [queried](AsynchronousFileChannel.md)). The size of the file increases when bytes are written beyond its current size; the size of the file decreases when it is [truncated](AsynchronousFileChannel.md)).

An asynchronous file channel does not have a*current position* within the file. Instead, the file position is specified to each read and write method that initiates asynchronous operations. A [CompletionHandler](CompletionHandler.md) is specified as a parameter and is invoked to consume the result of the I/O operation. This class also defines read and write methods that initiate asynchronous operations, returning a [Future](../java.util.concurrent/Future.md) to represent the pending result of the operation. The`Future`may be used to check if the operation has completed, wait for its completion, and retrieve the result.

In addition to read and write operations, this class defines the following operations:

- Updates made to a file may be [*forced*](AsynchronousFileChannel.md))*to the underlying storage device, ensuring that data are not lost in the event of a system crash.*
*- A region of a file may be #lock against access by other programs.*

*An`AsynchronousFileChannel`is associated with a thread pool to which tasks are submitted to handle I/O events and dispatch to completion handlers that consume the results of I/O operations on the channel. The completion handler for an I/O operation initiated on a channel is guaranteed to be invoked by one of the threads in the thread pool (This ensures that the completion handler is run by a thread with the expected*identity* ). Where an I/O operation completes immediately, and the initiating thread is itself a thread in the thread pool, then the completion handler may be invoked directly by the initiating thread. When an`AsynchronousFileChannel`is created without specifying a thread pool then the channel is associated with a system-dependent default thread pool that may be shared with other channels. The default thread pool is configured by the system properties defined by the [AsynchronousChannelGroup](AsynchronousChannelGroup.md) class.
Channels of this type are safe for use by multiple concurrent threads. The java.nio.channels.Channel#close method may be invoked at any time, as specified by the [Channel](Channel.md) interface. This causes all outstanding asynchronous operations on the channel to complete with the exception [AsynchronousCloseException](AsynchronousCloseException.md). Multiple read and write operations may be outstanding at the same time. When multiple read and write operations are outstanding then the ordering of the I/O operations, and the order that the completion handlers are invoked, is not specified; they are not, in particular, guaranteed to execute in the order that the operations were initiated. The [ByteBuffers](../java.nio/ByteBuffer.md) used when reading or writing are not safe for use by multiple concurrent I/O operations. Furthermore, after an I/O operation is initiated then care should be taken to ensure that the buffer is not accessed until after the operation has completed.
As with [FileChannel](FileChannel.md), the view of a file provided by an instance of this class is guaranteed to be consistent with other views of the same file provided by other instances in the same program. The view provided by an instance of this class may or may not, however, be consistent with the views seen by other concurrently-running programs due to caching performed by the underlying operating system and delays induced by network-filesystem protocols. This is true regardless of the language in which these other programs are written, and whether they are running on the same machine or on some other machine. The exact nature of any such inconsistencies are system-dependent and are therefore unspecified.*

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AsynchronousFileChannel](AsynchronousFileChannel.md))`()` Initializes a new instance of this class. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [force](AsynchronousFileChannel.md))`(`metaData:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Forces any updates to this channel's file to be written to the storage device that contains it. |
| [Future](../java.util.concurrent/Future.md)\< [FileLock](FileLock.md)!\>! | [lock](AsynchronousFileChannel.md))`()` Acquires an exclusive lock on this channel's file. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lock](AsynchronousFileChannel.md))`(`attachment:` `A`, `handler:` ` [CompletionHandler](CompletionHandler.md)< [FileLock](FileLock.md)!,` `in` `A>!`)` Acquires an exclusive lock on this channel's file. |
| --- | --- |
| abstract [Future](../java.util.concurrent/Future.md)\< [FileLock](FileLock.md)!\>! | [lock](AsynchronousFileChannel.md))`(`position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `shared:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Acquires a lock on the given region of this channel's file. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lock](AsynchronousFileChannel.md))`(`position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `shared:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `attachment:` `A`, `handler:` ` [CompletionHandler](CompletionHandler.md)< [FileLock](FileLock.md)!,` `in` `A>!`)` Acquires a lock on the given region of this channel's file. |
| openstatic [AsynchronousFileChannel](AsynchronousFileChannel.md)! | [open](AsynchronousFileChannel.md))`(`file:` ` [Path](../java.nio.file/Path.md)!`, `vararg` `options:` ` [OpenOption](../java.nio.file/OpenOption.md)!`)` Opens or creates a file for reading and/or writing, returning an asynchronous file channel to access the file. |
| --- | --- |
| openstatic [AsynchronousFileChannel](AsynchronousFileChannel.md)! | [open](AsynchronousFileChannel.md))`(`file:` ` [Path](../java.nio.file/Path.md)!`, `options:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<out` ` [OpenOption](../java.nio.file/OpenOption.md)!>!`, `executor:` ` [ExecutorService](../java.util.concurrent/ExecutorService.md)!`, `vararg` `attrs:` ` [FileAttribute](../java.nio.file.attribute/FileAttribute.md)<*>!`)` Opens or creates a file for reading and/or writing, returning an asynchronous file channel to access the file. |
| abstract [Future](../java.util.concurrent/Future.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | [read](AsynchronousFileChannel.md))`(`dst:` ` [ByteBuffer](../java.nio/ByteBuffer.md)!`, `position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Reads a sequence of bytes from this channel into the given buffer, starting at the given file position. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [read](AsynchronousFileChannel.md))`(`dst:` ` [ByteBuffer](../java.nio/ByteBuffer.md)!`, `position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `attachment:` `A`, `handler:` ` [CompletionHandler](CompletionHandler.md)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` `in` `A>!`)` Reads a sequence of bytes from this channel into the given buffer, starting at the given file position. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [size](AsynchronousFileChannel.md))`()` Returns the current size of this channel's file. |
| abstract [AsynchronousFileChannel](AsynchronousFileChannel.md)! | [truncate](AsynchronousFileChannel.md))`(`size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Truncates this channel's file to the given size. |
| [FileLock](FileLock.md)! | [tryLock](AsynchronousFileChannel.md))`()` Attempts to acquire an exclusive lock on this channel's file. |
| --- | --- |
| abstract [FileLock](FileLock.md)! | [tryLock](AsynchronousFileChannel.md))`(`position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `shared:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Attempts to acquire a lock on the given region of this channel's file. |
| abstract [Future](../java.util.concurrent/Future.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | [write](AsynchronousFileChannel.md))`(`src:` ` [ByteBuffer](../java.nio/ByteBuffer.md)!`, `position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Writes a sequence of bytes to this channel from the given buffer, starting at the given file position. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](AsynchronousFileChannel.md))`(`src:` ` [ByteBuffer](../java.nio/ByteBuffer.md)!`, `position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `attachment:` `A`, `handler:` ` [CompletionHandler](CompletionHandler.md)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` `in` `A>!`)` Writes a sequence of bytes to this channel from the given buffer, starting at the given file position. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [AsynchronousChannel](AsynchronousChannel.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](AsynchronousChannel.md))`()` <br /> Closes this channel. Any outstanding asynchronous operations upon this channel will complete with the exception [AsynchronousCloseException](AsynchronousCloseException.md). After a channel is closed, further attempts to initiate asynchronous I/O operations complete immediately with cause [ClosedChannelException](ClosedChannelException.md). This method otherwise behaves exactly as specified by the [Channel](Channel.md) interface. <br /> | ||
| From class [Channel](Channel.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](Channel.md))`()` <br /> Tells whether or not this channel is open. <br /> | ||

## Protected constructors

### AsynchronousFileChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AsynchronousFileChannel()
```

Initializes a new instance of this class.

## Public methods

### force

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun force(metaData: Boolean): Unit
```

Forces any updates to this channel's file to be written to the storage device that contains it.

If this channel's file resides on a local storage device then when this method returns it is guaranteed that all changes made to the file since this channel was created, or since this method was last invoked, will have been written to that device. This is useful for ensuring that critical information is not lost in the event of a system crash.

If the file does not reside on a local device then no such guarantee is made.

The`metaData`parameter can be used to limit the number of I/O operations that this method is required to perform. Passing`false`for this parameter indicates that only updates to the file's content need be written to storage; passing`true`indicates that updates to both the file's content and metadata must be written, which generally requires at least one more I/O operation. Whether this parameter actually has any effect is dependent upon the underlying operating system and is therefore unspecified.

Invoking this method may cause an I/O operation to occur even if the channel was only opened for reading. Some operating systems, for example, maintain a last-access time as part of a file's metadata, and this time is updated whenever the file is read. Whether or not this is actually done is system-dependent and is therefore unspecified.

This method is only guaranteed to force changes that were made to this channel's file via the methods defined in this class.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `metaData` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If`true`then this method is required to force changes to both the file's content and metadata to be written to storage; otherwise, it need only force content changes to be written |

| Exceptions ||
|--------------------------------------------|--------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If some other I/O error occurs |

### lock

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lock(): Future<FileLock!>!
```

Acquires an exclusive lock on this channel's file.

This method initiates an operation to acquire an exclusive lock on this channel's file. The method returns a`Future`representing the pending result of the operation. The`Future`'s [get](../java.util.concurrent/Future.md))method returns the [FileLock](FileLock.md) on successful completion.

An invocation of this method behaves in exactly the same way as the invocation 

```kotlin
ch.<code><a docref="java.nio.channels.AsynchronousFileChannel$lock(kotlin.Long, kotlin.Long, kotlin.Boolean)">lock</a></code>(0L, Long.MAX_VALUE, false)
  
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [Future](../java.util.concurrent/Future.md)< [FileLock](FileLock.md)!>! | a`Future`object representing the pending result |

| Exceptions ||
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.OverlappingFileLockException` | If a lock is already held by this Java virtual machine, or there is already a pending attempt to lock a region |
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |

### lock

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <A : Any!> lock(
    attachment: A, 
    handler: CompletionHandler<FileLock!, in A>!
): Unit
```

Acquires an exclusive lock on this channel's file.

This method initiates an operation to acquire a lock on the given region of this channel's file. The`handler`parameter is a completion handler that is invoked when the lock is acquired (or the operation fails). The result passed to the completion handler is the resulting`FileLock`.

An invocation of this method of the form`ch.lock(att,handler)`behaves in exactly the same way as the invocation 

```kotlin
ch.<code><a docref="java.nio.channels.AsynchronousFileChannel$lock(kotlin.Long, kotlin.Long, kotlin.Boolean, java.nio.channels.AsynchronousFileChannel.lock.A, java.nio.channels.CompletionHandler((java.nio.channels.FileLock, java.nio.channels.AsynchronousFileChannel.lock.A)))">lock</a></code>(0L, Long.MAX_VALUE, false, att, handler)
  
```

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<A>` | The type of the attachment |
| `attachment` | A:The object to attach to the I/O operation; can be`null` |
| `handler` | [CompletionHandler](CompletionHandler.md)\< [FileLock](FileLock.md)!,inA\>!:The handler for consuming the result |
| --- | --- |

| Exceptions ||
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.OverlappingFileLockException` | If a lock is already held by this Java virtual machine, or there is already a pending attempt to lock a region |
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |

### lock

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lock(
    position: Long, 
    size: Long, 
    shared: Boolean
): Future<FileLock!>!
```

Acquires a lock on the given region of this channel's file.

This method initiates an operation to acquire a lock on the given region of this channel's file. The method behaves in exactly the same manner as the [lock(long,long,boolean,java.lang.Object,java.nio.channels.CompletionHandler)](AsynchronousFileChannel.md))method except that instead of specifying a completion handler, this method returns a`Future`representing the pending result. The`Future`'s [get](../java.util.concurrent/Future.md))method returns the [FileLock](FileLock.md) on successful completion.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The position at which the locked region is to start; must be non-negative |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The size of the locked region; must be non-negative, and the sum`position`+`size`must be non-negative |
| `shared` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to request a shared lock, in which case this channel must be open for reading (and possibly writing);`false`to request an exclusive lock, in which case this channel must be open for writing (and possibly reading) |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [Future](../java.util.concurrent/Future.md)< [FileLock](FileLock.md)!>! | a`Future`object representing the pending result |

| Exceptions ||
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.OverlappingFileLockException` | If a lock is already held by this Java virtual machine, or there is already a pending attempt to lock a region |
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |
| `java.nio.channels.NonReadableChannelException` | If`shared`is true but this channel was not opened for reading |
| --- | --- |
| `java.nio.channels.NonWritableChannelException` | If`shared`is false but this channel was not opened for writing |

### lock

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <A : Any!> lock(
    position: Long, 
    size: Long, 
    shared: Boolean, 
    attachment: A, 
    handler: CompletionHandler<FileLock!, in A>!
): Unit
```

Acquires a lock on the given region of this channel's file.

This method initiates an operation to acquire a lock on the given region of this channel's file. The`handler`parameter is a completion handler that is invoked when the lock is acquired (or the operation fails). The result passed to the completion handler is the resulting`FileLock`.

The region specified by the`position`and`size`parameters need not be contained within, or even overlap, the actual underlying file. Lock regions are fixed in size; if a locked region initially contains the end of the file and the file grows beyond the region then the new portion of the file will not be covered by the lock. If a file is expected to grow in size and a lock on the entire file is required then a region starting at zero, and no smaller than the expected maximum size of the file, should be locked. The two-argument [lock(java.lang.Object,java.nio.channels.CompletionHandler)](AsynchronousFileChannel.md))method simply locks a region of size [Long.MAX_VALUE](../java.lang/Long.md). If a lock that overlaps the requested region is already held by this Java virtual machine, or this method has been invoked to lock an overlapping region and that operation has not completed, then this method throws [OverlappingFileLockException](OverlappingFileLockException.md).

Some operating systems do not support a mechanism to acquire a file lock in an asynchronous manner. Consequently an implementation may acquire the file lock in a background thread or from a task executed by a thread in the associated thread pool. If there are many lock operations outstanding then it may consume threads in the Java virtual machine for indefinite periods.

Some operating systems do not support shared locks, in which case a request for a shared lock is automatically converted into a request for an exclusive lock. Whether the newly-acquired lock is shared or exclusive may be tested by invoking the resulting lock object's [isShared](FileLock.md))method.

File locks are held on behalf of the entire Java virtual machine. They are not suitable for controlling access to a file by multiple threads within the same virtual machine.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<A>` | The type of the attachment |
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The position at which the locked region is to start; must be non-negative |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The size of the locked region; must be non-negative, and the sum`position`+`size`must be non-negative |
| --- | --- |
| `shared` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to request a shared lock, in which case this channel must be open for reading (and possibly writing);`false`to request an exclusive lock, in which case this channel must be open for writing (and possibly reading) |
| `attachment` | A:The object to attach to the I/O operation; can be`null` |
| `handler` | [CompletionHandler](CompletionHandler.md)\< [FileLock](FileLock.md)!,inA\>!:The handler for consuming the result |
| --- | --- |

| Exceptions ||
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.OverlappingFileLockException` | If a lock that overlaps the requested region is already held by this Java virtual machine, or there is already a pending attempt to lock an overlapping region |
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |
| `java.nio.channels.NonReadableChannelException` | If`shared`is true but this channel was not opened for reading |
| --- | --- |
| `java.nio.channels.NonWritableChannelException` | If`shared`is false but this channel was not opened for writing |

### open

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(
    file: Path!, 
    vararg options: OpenOption!
): AsynchronousFileChannel!
```

Opens or creates a file for reading and/or writing, returning an asynchronous file channel to access the file.

An invocation of this method behaves in exactly the same way as the invocation 

```kotlin
ch.<code><a docref="java.nio.channels.AsynchronousFileChannel$open(java.nio.file.Path, kotlin.collections.MutableSet((java.nio.file.OpenOption)), java.util.concurrent.ExecutorService, kotlin.Array((java.nio.file.attribute.FileAttribute((kotlin.Any)))))"> open</a></code>(file, opts, null, new FileAttribute<?>[0]);
  
```
where`opts`is a`Set`containing the options specified to this method.

The resulting channel is associated with default thread pool to which tasks are submitted to handle I/O events and dispatch to completion handlers that consume the result of asynchronous operations performed on the resulting channel.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [Path](../java.nio.file/Path.md)!:The path of the file to open or create |
| `options` | [OpenOption](../java.nio.file/OpenOption.md)!:Options specifying how the file is opened |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [AsynchronousFileChannel](AsynchronousFileChannel.md)! | A new asynchronous file channel |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the set contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | If the`file`is associated with a provider that does not support creating file channels, or an unsupported open option is specified |
| `java.io.IOException` | If an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | If a security manager is installed and it denies an unspecified permission required by the implementation. In the case of the default provider, the [java.lang.SecurityManager#checkRead(java.lang.String)](../java.lang/SecurityManager.md))method is invoked to check read access if the file is opened for reading. The [java.lang.SecurityManager#checkWrite(java.lang.String)](../java.lang/SecurityManager.md))method is invoked to check write access if the file is opened for writing |

### open

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(
    file: Path!, 
    options: MutableSet<out OpenOption!>!, 
    executor: ExecutorService!, 
    vararg attrs: FileAttribute<*>!
): AsynchronousFileChannel!
```

Opens or creates a file for reading and/or writing, returning an asynchronous file channel to access the file.

The`options`parameter determines how the file is opened. The [READ](../java.nio.file/StandardOpenOption.md) and [WRITE](../java.nio.file/StandardOpenOption.md) options determines if the file should be opened for reading and/or writing. If neither option is contained in the array then an existing file is opened for reading.

In addition to`READ`and`WRITE`, the following options may be present:

| Option | Description |
| --- | --- |
| [TRUNCATE_EXISTING](../java.nio.file/StandardOpenOption.md) | When opening an existing file, the file is first truncated to a size of 0 bytes. This option is ignored when the file is opened only for reading. |
| [CREATE_NEW](../java.nio.file/StandardOpenOption.md) | If this option is present then a new file is created, failing if the file already exists. When creating a file the check for the existence of the file and the creation of the file if it does not exist is atomic with respect to other file system operations. This option is ignored when the file is opened only for reading. |
| [CREATE](../java.nio.file/StandardOpenOption.md) | If this option is present then an existing file is opened if it exists, otherwise a new file is created. When creating a file the check for the existence of the file and the creation of the file if it does not exist is atomic with respect to other file system operations. This option is ignored if the`CREATE_NEW`option is also present or the file is opened only for reading. |
| --- | --- |
| [DELETE_ON_CLOSE](../java.nio.file/StandardOpenOption.md) | When this option is present then the implementation makes a*best effort* attempt to delete the file when closed by the #close method. If the`close`method is not invoked then a*best effort*attempt is made to delete the file when the Java virtual machine terminates. |
| [SPARSE](../java.nio.file/StandardOpenOption.md) | When creating a new file this option is a*hint*that the new file will be sparse. This option is ignored when not creating a new file. |
| [SYNC](../java.nio.file/StandardOpenOption.md) | Requires that every update to the file's content or metadata be written synchronously to the underlying storage device. (see [Synchronized I/O file integrity](../java.nio.file/_package.md)). |
| --- | --- |
| [DSYNC](../java.nio.file/StandardOpenOption.md) | Requires that every update to the file's content be written synchronously to the underlying storage device. (see [Synchronized I/O file integrity](../java.nio.file/_package.md)). |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

An implementation may also support additional options.

The`executor`parameter is the [ExecutorService](../java.util.concurrent/ExecutorService.md) to which tasks are submitted to handle I/O events and dispatch completion results for operations initiated on resulting channel. The nature of these tasks is highly implementation specific and so care should be taken when configuring the`Executor`. Minimally it should support an unbounded work queue and should not run tasks on the caller thread of the [execute](../java.util.concurrent/Executor.md))method. Shutting down the executor service while the channel is open results in unspecified behavior.

The`attrs`parameter is an optional array of file [file-attributes](../java.nio.file.attribute/FileAttribute.md) to set atomically when creating the file.

The new channel is created by invoking the [newFileChannel](../java.nio.file.spi/FileSystemProvider.md))method on the provider that created the`Path`.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [Path](../java.nio.file/Path.md)!:The path of the file to open or create |
| `options` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<out [OpenOption](../java.nio.file/OpenOption.md)!\>!:Options specifying how the file is opened |
| `executor` | [ExecutorService](../java.util.concurrent/ExecutorService.md)!:The thread pool or`null`to associate the channel with the default thread pool |
| --- | --- |
| `attrs` | [FileAttribute](../java.nio.file.attribute/FileAttribute.md)\<\*\>!:An optional list of file attributes to set atomically when creating the file |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [AsynchronousFileChannel](AsynchronousFileChannel.md)! | A new asynchronous file channel |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the set contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | If the`file`is associated with a provider that does not support creating asynchronous file channels, or an unsupported open option is specified, or the array contains an attribute that cannot be set atomically when creating the file |
| `java.io.IOException` | If an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | If a security manager is installed and it denies an unspecified permission required by the implementation. In the case of the default provider, the [java.lang.SecurityManager#checkRead(java.lang.String)](../java.lang/SecurityManager.md))method is invoked to check read access if the file is opened for reading. The [java.lang.SecurityManager#checkWrite(java.lang.String)](../java.lang/SecurityManager.md))method is invoked to check write access if the file is opened for writing |

### read

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(
    dst: ByteBuffer!, 
    position: Long
): Future<Int!>!
```

Reads a sequence of bytes from this channel into the given buffer, starting at the given file position.

This method initiates the reading of a sequence of bytes from this channel into the given buffer, starting at the given file position. This method returns a`Future`representing the pending result of the operation. The`Future`'s [get](../java.util.concurrent/Future.md))method returns the number of bytes read or`-1`if the given position is greater than or equal to the file's size at the time that the read is attempted.

This method works in the same manner as the [java.nio.channels.AsynchronousByteChannel#read(java.nio.ByteBuffer)](AsynchronousByteChannel.md))method, except that bytes are read starting at the given file position. If the given file position is greater than the file's size at the time that the read is attempted then no bytes are read.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [ByteBuffer](../java.nio/ByteBuffer.md)!:The buffer into which bytes are to be transferred |
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The file position at which the transfer is to begin; must be non-negative |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [Future](../java.util.concurrent/Future.md)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>! | A`Future`object representing the pending result |

| Exceptions ||
|-------------------------------------------------|--------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the position is negative or the buffer is read-only |
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |

### read

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <A : Any!> read(
    dst: ByteBuffer!, 
    position: Long, 
    attachment: A, 
    handler: CompletionHandler<Int!, in A>!
): Unit
```

Reads a sequence of bytes from this channel into the given buffer, starting at the given file position.

This method initiates the reading of a sequence of bytes from this channel into the given buffer, starting at the given file position. The result of the read is the number of bytes read or`-1`if the given position is greater than or equal to the file's size at the time that the read is attempted.

This method works in the same manner as the [java.nio.channels.AsynchronousByteChannel#read(java.nio.ByteBuffer,java.lang.Object,java.nio.channels.CompletionHandler)](AsynchronousByteChannel.md))method, except that bytes are read starting at the given file position. If the given file position is greater than the file's size at the time that the read is attempted then no bytes are read.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<A>` | The type of the attachment |
| `dst` | [ByteBuffer](../java.nio/ByteBuffer.md)!:The buffer into which bytes are to be transferred |
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The file position at which the transfer is to begin; must be non-negative |
| --- | --- |
| `attachment` | A:The object to attach to the I/O operation; can be`null` |
| `handler` | [CompletionHandler](CompletionHandler.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,inA\>!:The handler for consuming the result |

| Exceptions ||
|-------------------------------------------------|--------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the position is negative or the buffer is read-only |
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |

### size

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### truncate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun truncate(size: Long): AsynchronousFileChannel!
```

Truncates this channel's file to the given size.

If the given size is less than the file's current size then the file is truncated, discarding any bytes beyond the new end of the file. If the given size is greater than or equal to the file's current size then the file is not modified.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The new size, a non-negative byte count |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|-------------------|
| [AsynchronousFileChannel](AsynchronousFileChannel.md)! | This file channel |

| Exceptions ||
|-------------------------------------------------|--------------------------------------------|
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.lang.IllegalArgumentException` | If the new size is negative |
| --- | --- |
| `java.io.IOException` | If some other I/O error occurs |

### tryLock

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun tryLock(): FileLock!
```

Attempts to acquire an exclusive lock on this channel's file.

An invocation of this method of the form`ch.tryLock()`behaves in exactly the same way as the invocation 

```kotlin
ch.<code><a docref="java.nio.channels.AsynchronousFileChannel$tryLock(kotlin.Long, kotlin.Long, kotlin.Boolean)">tryLock</a></code>(0L, Long.MAX_VALUE, false) 
```

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [FileLock](FileLock.md)! | A lock object representing the newly-acquired lock, or`null`if the lock could not be acquired because another program holds an overlapping lock |

| Exceptions ||
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.OverlappingFileLockException` | If a lock that overlaps the requested region is already held by this Java virtual machine, or if another thread is already blocked in this method and is attempting to lock an overlapping region |
| `java.nio.channels.NonWritableChannelException` | If`shared`is false but this channel was not opened for writing |
| --- | --- |
| `java.io.IOException` | If some other I/O error occurs |

**See Also**

- [#lock(Object,CompletionHandler)](AsynchronousFileChannel.md))
- [#lock(long,long,boolean,Object,CompletionHandler)](AsynchronousFileChannel.md))
- [#tryLock(long,long,boolean)](AsynchronousFileChannel.md)) 

### tryLock

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun tryLock(
    position: Long, 
    size: Long, 
    shared: Boolean
): FileLock!
```

Attempts to acquire a lock on the given region of this channel's file.

This method does not block. An invocation always returns immediately, either having acquired a lock on the requested region or having failed to do so. If it fails to acquire a lock because an overlapping lock is held by another program then it returns`null`. If it fails to acquire a lock for any other reason then an appropriate exception is thrown.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The position at which the locked region is to start; must be non-negative |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The size of the locked region; must be non-negative, and the sum`position`+`size`must be non-negative |
| `shared` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to request a shared lock,`false`to request an exclusive lock |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [FileLock](FileLock.md)! | A lock object representing the newly-acquired lock, or`null`if the lock could not be acquired because another program holds an overlapping lock |

| Exceptions ||
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.OverlappingFileLockException` | If a lock that overlaps the requested region is already held by this Java virtual machine, or if another thread is already blocked in this method and is attempting to lock an overlapping region of the same file |
| --- | --- |
| `java.nio.channels.NonReadableChannelException` | If`shared`is true but this channel was not opened for reading |
| `java.nio.channels.NonWritableChannelException` | If`shared`is false but this channel was not opened for writing |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |

**See Also**

- [#lock(Object,CompletionHandler)](AsynchronousFileChannel.md))
- [#lock(long,long,boolean,Object,CompletionHandler)](AsynchronousFileChannel.md))
- <https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousFileChannel#tryLock()> 

### write

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(
    src: ByteBuffer!, 
    position: Long
): Future<Int!>!
```

Writes a sequence of bytes to this channel from the given buffer, starting at the given file position.

This method initiates the writing of a sequence of bytes to this channel from the given buffer, starting at the given file position. The method returns a`Future`representing the pending result of the write operation. The`Future`'s [get](../java.util.concurrent/Future.md))method returns the number of bytes written.

This method works in the same manner as the [java.nio.channels.AsynchronousByteChannel#write(java.nio.ByteBuffer)](AsynchronousByteChannel.md))method, except that bytes are written starting at the given file position. If the given position is greater than the file's size, at the time that the write is attempted, then the file will be grown to accommodate the new bytes; the values of any bytes between the previous end-of-file and the newly-written bytes are unspecified.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](../java.nio/ByteBuffer.md)!:The buffer from which bytes are to be transferred |
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The file position at which the transfer is to begin; must be non-negative |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [Future](../java.util.concurrent/Future.md)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>! | A`Future`object representing the pending result |

| Exceptions ||
|-------------------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | If the position is negative |
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |

### write

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <A : Any!> write(
    src: ByteBuffer!, 
    position: Long, 
    attachment: A, 
    handler: CompletionHandler<Int!, in A>!
): Unit
```

Writes a sequence of bytes to this channel from the given buffer, starting at the given file position.

This method works in the same manner as the [java.nio.channels.AsynchronousByteChannel#write(java.nio.ByteBuffer,java.lang.Object,java.nio.channels.CompletionHandler)](AsynchronousByteChannel.md))method, except that bytes are written starting at the given file position. If the given position is greater than the file's size, at the time that the write is attempted, then the file will be grown to accommodate the new bytes; the values of any bytes between the previous end-of-file and the newly-written bytes are unspecified.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<A>` | The type of the attachment |
| `src` | [ByteBuffer](../java.nio/ByteBuffer.md)!:The buffer from which bytes are to be transferred |
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The file position at which the transfer is to begin; must be non-negative |
| --- | --- |
| `attachment` | A:The object to attach to the I/O operation; can be`null` |
| `handler` | [CompletionHandler](CompletionHandler.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,inA\>!:The handler for consuming the result |

| Exceptions ||
|-------------------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | If the position is negative |
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
