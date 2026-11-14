# FileLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileLock

```
abstract class FileLock : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.nio.channels.FileLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#) |

A token representing a lock on a region of a file.

A file-lock object is created each time a lock is acquired on a file via one of the [lock](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#lock(kotlin.Long,%20kotlin.Long,%20kotlin.Boolean))or [tryLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#tryLock(kotlin.Long,%20kotlin.Long,%20kotlin.Boolean))methods of the [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel) class, or the [lock](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousFileChannel#lock(kotlin.Long,%20kotlin.Long,%20kotlin.Boolean,%20java.nio.channels.AsynchronousFileChannel.lock.A,%20java.nio.channels.CompletionHandler))or [tryLock](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousFileChannel#tryLock(kotlin.Long,%20kotlin.Long,%20kotlin.Boolean))methods of the [AsynchronousFileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousFileChannel) class.

A file-lock object is initially valid. It remains valid until the lock is released by invoking the [release](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#release())method, by closing the channel that was used to acquire it, or by the termination of the Java virtual machine, whichever comes first. The validity of a lock may be tested by invoking its [isValid](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#isValid())method.

A file lock is either*exclusive* or*shared*. A shared lock prevents other concurrently-running programs from acquiring an overlapping exclusive lock, but does allow them to acquire overlapping shared locks. An exclusive lock prevents other programs from acquiring an overlapping lock of either type. Once it is released, a lock has no further effect on the locks that may be acquired by other programs.

Whether a lock is exclusive or shared may be determined by invoking its [isShared](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#isShared())method. Some platforms do not support shared locks, in which case a request for a shared lock is automatically converted into a request for an exclusive lock.

The locks held on a particular file by a single Java virtual machine do not overlap. The [overlaps](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#overlaps(kotlin.Long,%20kotlin.Long))method may be used to test whether a candidate lock range overlaps an existing lock.

A file-lock object records the file channel upon whose file the lock is held, the type and validity of the lock, and the position and size of the locked region. Only the validity of a lock is subject to change over time; all other aspects of a lock's state are immutable.

File locks are held on behalf of the entire Java virtual machine. They are not suitable for controlling access to a file by multiple threads within the same virtual machine.

File-lock objects are safe for use by multiple concurrent threads.

## Platform dependencies

This file-locking API is intended to map directly to the native locking facility of the underlying operating system. Thus the locks held on a file should be visible to all programs that have access to the file, regardless of the language in which those programs are written.

Whether or not a lock actually prevents another program from accessing the content of the locked region is system-dependent and therefore unspecified. The native file-locking facilities of some systems are merely*advisory* , meaning that programs must cooperatively observe a known locking protocol in order to guarantee data integrity. On other systems native file locks are*mandatory*, meaning that if one program locks a region of a file then other programs are actually prevented from accessing that region in a way that would violate the lock. On yet other systems, whether native file locks are advisory or mandatory is configurable on a per-file basis. To ensure consistent and correct behavior across platforms, it is strongly recommended that the locks provided by this API be used as if they were advisory locks.

On some systems, acquiring a mandatory lock on a region of a file prevents that region from being [*mapped into memory*](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel#map(java.nio.channels.FileChannel.MapMode,%20kotlin.Long,%20kotlin.Long)), and vice versa. Programs that combine locking and mapping should be prepared for this combination to fail.

On some systems, closing a channel releases all locks held by the Java virtual machine on the underlying file regardless of whether the locks were acquired via that channel or via another channel open on the same file. It is strongly recommended that, within a program, a unique channel be used to acquire all locks on any given file.

Some network filesystems permit file locking to be used with memory-mapped files only when the locked regions are page-aligned and a whole multiple of the underlying hardware's page size. Some network filesystems do not implement file locks on regions that extend past a certain position, often 230 or 231. In general, great care should be taken when locking files that reside on network filesystems.

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#FileLock(java.nio.channels.AsynchronousFileChannel,%20kotlin.Long,%20kotlin.Long,%20kotlin.Boolean))`(`channel:` ` [AsynchronousFileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousFileChannel)!`, `position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `shared:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Initializes a new instance of this class. |
| [FileLock](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#FileLock(java.nio.channels.FileChannel,%20kotlin.Long,%20kotlin.Long,%20kotlin.Boolean))`(`channel:` ` [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel)!`, `position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `shared:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Initializes a new instance of this class. |

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel)! | [acquiredBy](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#acquiredBy())`()` Returns the channel upon whose file this lock was acquired. |
| [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel)! | [channel](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#channel())`()` Returns the file channel upon whose file this lock was acquired. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#close())`()` This method invokes the [release](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#release())method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShared](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#isShared())`()` Tells whether this lock is shared. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#isValid())`()` Tells whether or not this lock is valid. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [overlaps](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#overlaps(kotlin.Long,%20kotlin.Long))`(`position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Tells whether or not this lock overlaps the given lock range. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [position](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#position())`()` Returns the position within the file of the first byte of the locked region. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#release())`()` Releases this lock. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [size](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#size())`()` Returns the size of the locked region in bytes. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#toString())`()` Returns a string describing the range, type, and validity of this lock. |

## Protected constructors

### FileLock

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected FileLock(
    channel: AsynchronousFileChannel!, 
    position: Long, 
    size: Long, 
    shared: Boolean)
```

Initializes a new instance of this class.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `channel` | [AsynchronousFileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousFileChannel)!:The channel upon whose file this lock is held |
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The position within the file at which the locked region starts; must be non-negative |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The size of the locked region; must be non-negative, and the sum`position`+`size`must be non-negative |
| `shared` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if this lock is shared,`false`if it is exclusive |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |

### FileLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected FileLock(
    channel: FileChannel!, 
    position: Long, 
    size: Long, 
    shared: Boolean)
```

Initializes a new instance of this class.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `channel` | [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel)!:The file channel upon whose file this lock is held |
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The position within the file at which the locked region starts; must be non-negative |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The size of the locked region; must be non-negative, and the sum`position`+`size`must be non-negative |
| `shared` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if this lock is shared,`false`if it is exclusive |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameters do not hold |

## Public methods

### acquiredBy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun acquiredBy(): Channel!
```

Returns the channel upon whose file this lock was acquired.

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel)! | The channel upon whose file this lock was acquired. |

### channel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun channel(): FileChannel!
```

Returns the file channel upon whose file this lock was acquired.

This method has been superseded by the [acquiredBy](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#acquiredBy())method.

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel)! | The file channel, or`null`if the file lock was not acquired by a file channel. |

### close

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

This method invokes the [release](https://developer.android.com/reference/kotlin/java/nio/channels/FileLock#release())method. It was added to the class so that it could be used in conjunction with the automatic resource management block construct.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### isShared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isShared(): Boolean
```

Tells whether this lock is shared.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if lock is shared,`false`if it is exclusive |

### isValid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isValid(): Boolean
```

Tells whether or not this lock is valid.

A lock object remains valid until it is released or the associated file channel is closed, whichever comes first.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this lock is valid |

### overlaps

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun overlaps(
    position: Long, 
    size: Long
): Boolean
```

Tells whether or not this lock overlaps the given lock range.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The starting position of the lock range |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The size of the lock range |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this lock and the given lock range overlap by at least one byte |

### position

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun position(): Long
```

Returns the position within the file of the first byte of the locked region.

A locked region need not be contained within, or even overlap, the actual underlying file, so the value returned by this method may exceed the file's current size.

| Return ||
|------------------------------------------------------------------------------|--------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The position |

### release

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun release(): Unit
```

Releases this lock.

If this lock object is valid then invoking this method releases the lock and renders the object invalid. If this lock object is invalid then invoking this method has no effect.

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If the channel that was used to acquire this lock is no longer open |
| `java.io.IOException` | If an I/O error occurs |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun size(): Long
```

Returns the size of the locked region in bytes.

A locked region need not be contained within, or even overlap, the actual underlying file, so the value returned by this method may exceed the file's current size.

| Return ||
|------------------------------------------------------------------------------|-------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The size of the locked region |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string describing the range, type, and validity of this lock.

| Return ||
|----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A descriptive string |
