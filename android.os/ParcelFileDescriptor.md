# ParcelFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParcelFileDescriptor

Kotlin| [Java](../android/os/ParcelFileDescriptor.md) 
| --- | --- |

```
open class ParcelFileDescriptor : Closeable, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) |

The FileDescriptor returned by [Parcel.readFileDescriptor](../android/os/Parcel.md)), allowing you to close it when done with it.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [AutoCloseInputStream](../android/os/ParcelFileDescriptor.AutoCloseInputStream.md) An InputStream you can create on a ParcelFileDescriptor, which will take care of calling android. |
| open | [AutoCloseOutputStream](../android/os/ParcelFileDescriptor.AutoCloseOutputStream.md) An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android. |
| open | [FileDescriptorDetachedException](../android/os/ParcelFileDescriptor.FileDescriptorDetachedException.md) Exception that indicates that the file descriptor was detached. |
| --- | --- |
| abstract | [OnCloseListener](../android/os/ParcelFileDescriptor.OnCloseListener.md) Callback indicating that a ParcelFileDescriptor has been closed. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_APPEND](../android/os/ParcelFileDescriptor.md) For use with #open: append to end of file while writing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_CREATE](../android/os/ParcelFileDescriptor.md) For use with #open: create the file if it doesn't already exist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_READ_ONLY](../android/os/ParcelFileDescriptor.md) For use with #open: open the file with read-only access. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_READ_WRITE](../android/os/ParcelFileDescriptor.md) For use with #open: open the file with read and write access. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_TRUNCATE](../android/os/ParcelFileDescriptor.md) For use with #open: erase contents of file when opening. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_WORLD_READABLE](../android/os/ParcelFileDescriptor.md) For use with #open: if [MODE_CREATE](../android/os/ParcelFileDescriptor.md) has been supplied and this file doesn't already exist, then create the file with permissions such that any application can read it. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_WORLD_WRITEABLE](../android/os/ParcelFileDescriptor.md) For use with #open: if [MODE_CREATE](../android/os/ParcelFileDescriptor.md) has been supplied and this file doesn't already exist, then create the file with permissions such that any application can write it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_WRITE_ONLY](../android/os/ParcelFileDescriptor.md) For use with #open: open the file with write-only access. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md))`(`wrapped:` ` [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!`)` Create a new ParcelFileDescriptor wrapped around another descriptor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | [adoptFd](../android/os/ParcelFileDescriptor.md))`(`fd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Take ownership of a raw native fd in to a new ParcelFileDescriptor. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canDetectErrors](../android/os/ParcelFileDescriptor.md))`()` Indicates if this ParcelFileDescriptor can communicate and detect remote errors/crashes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkError](../android/os/ParcelFileDescriptor.md))`()` Detect and throw if the other end of a pipe or socket pair encountered an error or crashed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/os/ParcelFileDescriptor.md))`()` Close the ParcelFileDescriptor. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeWithError](../android/os/ParcelFileDescriptor.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Close the ParcelFileDescriptor, informing any peer that an error occurred while processing. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!\>! | [createPipe](../android/os/ParcelFileDescriptor.md))`()` Create two ParcelFileDescriptors structured as a data pipe. |
| --- | --- |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!\>! | [createReliablePipe](../android/os/ParcelFileDescriptor.md))`()` Create two ParcelFileDescriptors structured as a data pipe. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!\>! | [createReliableSocketPair](../android/os/ParcelFileDescriptor.md))`()` Create two ParcelFileDescriptors structured as a pair of sockets connected to each other. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!\>! | [createSocketPair](../android/os/ParcelFileDescriptor.md))`()` Create two ParcelFileDescriptors structured as a pair of sockets connected to each other. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/os/ParcelFileDescriptor.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [detachFd](../android/os/ParcelFileDescriptor.md))`()` Return the native fd int for this ParcelFileDescriptor and detach it from the object here. |
| open [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | [dup](../android/os/ParcelFileDescriptor.md))`()` Create a new ParcelFileDescriptor that is a dup of the existing FileDescriptor. |
| --- | --- |
| openstatic [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | [dup](../android/os/ParcelFileDescriptor.md))`(`orig:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`)` Create a new ParcelFileDescriptor that is a dup of an existing FileDescriptor. |
| openstatic [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | [fromDatagramSocket](../android/os/ParcelFileDescriptor.md))`(`datagramSocket:` ` [DatagramSocket](../java/net/DatagramSocket.md)!`)` Create a new ParcelFileDescriptor from the specified DatagramSocket. |
| openstatic [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | [fromFd](../android/os/ParcelFileDescriptor.md))`(`fd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new ParcelFileDescriptor from a raw native fd. |
| --- | --- |
| openstatic [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | [fromSocket](../android/os/ParcelFileDescriptor.md))`(`socket:` ` [Socket](../java/net/Socket.md)!`)` Create a new ParcelFileDescriptor from the specified Socket. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFd](../android/os/ParcelFileDescriptor.md))`()` Return the native fd int for this ParcelFileDescriptor. |
| open [FileDescriptor](../java/io/FileDescriptor.md)! | [getFileDescriptor](../android/os/ParcelFileDescriptor.md))`()` Retrieve the actual FileDescriptor associated with this object. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStatSize](../android/os/ParcelFileDescriptor.md))`()` Return the total size of the file representing this fd, as determined by`stat()`. |
| openstatic [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | [open](../android/os/ParcelFileDescriptor.md))`(`file:` ` [File](../java/io/File.md)!`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new ParcelFileDescriptor accessing a given file. |
| openstatic [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | [open](../android/os/ParcelFileDescriptor.md))`(`file:` ` [File](../java/io/File.md)!`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `handler:` ` [Handler](../android/os/Handler.md)!`, `listener:` ` [ParcelFileDescriptor.OnCloseListener](../android/os/ParcelFileDescriptor.OnCloseListener.md)!`)` Create a new ParcelFileDescriptor accessing a given file. |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parseMode](../android/os/ParcelFileDescriptor.md))`(`mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Converts a string representing a file mode, such as "rw", into a bitmask suitable for use with #open. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/os/ParcelFileDescriptor.md))`()` <br /> |
| openstatic [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) | [wrap](../android/os/ParcelFileDescriptor.md))`(`pfd:` ` [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)`, `handler:` ` [Handler](../android/os/Handler.md)`, `listener:` ` [ParcelFileDescriptor.OnCloseListener](../android/os/ParcelFileDescriptor.OnCloseListener.md)`)` Create a new ParcelFileDescriptor wrapping an already-opened file. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/os/ParcelFileDescriptor.md))`(`out:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/os/ParcelFileDescriptor.md))`()` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!\> | [CREATOR](../android/os/ParcelFileDescriptor.md) <br /> |

## Constants

### MODE_APPEND

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_APPEND: Int
```

For use with #open: append to end of file while writing. 

 Value: 33554432

### MODE_CREATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_CREATE: Int
```

For use with #open: create the file if it doesn't already exist. 

 Value: 134217728

### MODE_READ_ONLY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_READ_ONLY: Int
```

For use with #open: open the file with read-only access. 

 Value: 268435456

### MODE_READ_WRITE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_READ_WRITE: Int
```

For use with #open: open the file with read and write access. 

 Value: 805306368

### MODE_TRUNCATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_TRUNCATE: Int
```

For use with #open: erase contents of file when opening. 

 Value: 67108864

### MODE_WORLD_READABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_WORLD_READABLE: Int
```

**Deprecated:** *Creating world-readable files is very dangerous, and likely to cause security holes in applications. It is strongly discouraged; instead, applications should use more formal mechanism for interactions such as [ContentProvider](../android/content/ContentProvider.md), [BroadcastReceiver](../android/content/BroadcastReceiver.md), and [android.app.Service](../android/app/Service.md). There are no guarantees that this access mode will remain on a file, such as when it goes through a backup and restore.*

For use with #open: if [MODE_CREATE](../android/os/ParcelFileDescriptor.md) has been supplied and this file doesn't already exist, then create the file with permissions such that any application can read it. 

 Value: 1

### MODE_WORLD_WRITEABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_WORLD_WRITEABLE: Int
```

**Deprecated:** *Creating world-writable files is very dangerous, and likely to cause security holes in applications. It is strongly discouraged; instead, applications should use more formal mechanism for interactions such as [ContentProvider](../android/content/ContentProvider.md), [BroadcastReceiver](../android/content/BroadcastReceiver.md), and [android.app.Service](../android/app/Service.md). There are no guarantees that this access mode will remain on a file, such as when it goes through a backup and restore.*

For use with #open: if [MODE_CREATE](../android/os/ParcelFileDescriptor.md) has been supplied and this file doesn't already exist, then create the file with permissions such that any application can write it. 

 Value: 2

### MODE_WRITE_ONLY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_WRITE_ONLY: Int
```

For use with #open: open the file with write-only access. 

 Value: 536870912

## Public constructors

### ParcelFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ParcelFileDescriptor(wrapped: ParcelFileDescriptor!)
```

Create a new ParcelFileDescriptor wrapped around another descriptor. By default all method calls are delegated to the wrapped descriptor.

## Public methods

### adoptFd

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun adoptFd(fd: Int): ParcelFileDescriptor!
```

Take ownership of a raw native fd in to a new ParcelFileDescriptor. The returned ParcelFileDescriptor now owns the given fd, and will be responsible for closing it.

**WARNING:**You must not close the fd yourself after this call, and ownership of the file descriptor must have been released prior to the call to this function.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The native fd that the ParcelFileDescriptor should adopt. |

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | Returns a new ParcelFileDescriptor holding a FileDescriptor for the given fd. |

### canDetectErrors

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun canDetectErrors(): Boolean
```

Indicates if this ParcelFileDescriptor can communicate and detect remote errors/crashes. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#checkError()> 

### checkError

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkError(): Unit
```

Detect and throw if the other end of a pipe or socket pair encountered an error or crashed. This allows a reader to distinguish between a valid EOF and an error/crash.

If this ParcelFileDescriptor is unable to detect remote errors, it will return silently.

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | for normal errors. |
| `android.os.ParcelFileDescriptor.FileDescriptorDetachedException` | if the remote side called [detachFd()](../android/os/ParcelFileDescriptor.md)). Once detached, the remote side is unable to communicate any errors through [closeWithError(java.lang.String)](../android/os/ParcelFileDescriptor.md)). |

**See Also**

- <https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#canDetectErrors()> 

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Close the ParcelFileDescriptor. This implementation closes the underlying OS resources allocated to represent this stream.

| Exceptions ||
|-----------------------|-------------------------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an error occurs attempting to close this ParcelFileDescriptor. |

### closeWithError

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun closeWithError(msg: String!): Unit
```

Close the ParcelFileDescriptor, informing any peer that an error occurred while processing. If the creator of this descriptor is not observing errors, it will close normally.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:describing the error; must not be null. |

### createPipe

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createPipe(): Array<ParcelFileDescriptor!>!
```

Create two ParcelFileDescriptors structured as a data pipe. The first ParcelFileDescriptor in the returned array is the read side; the second is the write side. 

### createReliablePipe

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createReliablePipe(): Array<ParcelFileDescriptor!>!
```

Create two ParcelFileDescriptors structured as a data pipe. The first ParcelFileDescriptor in the returned array is the read side; the second is the write side.

The write end has the ability to deliver an error message through [closeWithError(java.lang.String)](../android/os/ParcelFileDescriptor.md))which can be handled by the read end calling [checkError()](../android/os/ParcelFileDescriptor.md)), usually after detecting an EOF. This can also be used to detect remote crashes. 

### createReliableSocketPair

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createReliableSocketPair(): Array<ParcelFileDescriptor!>!
```

Create two ParcelFileDescriptors structured as a pair of sockets connected to each other. The two sockets are indistinguishable.

Both ends have the ability to deliver an error message through [closeWithError(java.lang.String)](../android/os/ParcelFileDescriptor.md))which can be detected by the other end calling [checkError()](../android/os/ParcelFileDescriptor.md)), usually after detecting an EOF. This can also be used to detect remote crashes. 

### createSocketPair

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createSocketPair(): Array<ParcelFileDescriptor!>!
```

Create two ParcelFileDescriptors structured as a pair of sockets connected to each other. The two sockets are indistinguishable. 

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### detachFd

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun detachFd(): Int
```

Return the native fd int for this ParcelFileDescriptor and detach it from the object here. You are now responsible for closing the fd in native code.

You should not detach when the original creator of the descriptor is expecting a reliable signal through #close() or [closeWithError(java.lang.String)](../android/os/ParcelFileDescriptor.md)). 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#canDetectErrors()> 

### dup

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dup(): ParcelFileDescriptor!
```

Create a new ParcelFileDescriptor that is a dup of the existing FileDescriptor. This obeys standard POSIX semantics, where the new file descriptor shared state such as file position with the original file descriptor. 

### dup

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dup(orig: FileDescriptor!): ParcelFileDescriptor!
```

Create a new ParcelFileDescriptor that is a dup of an existing FileDescriptor. This obeys standard POSIX semantics, where the new file descriptor shared state such as file position with the original file descriptor. 

### fromDatagramSocket

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromDatagramSocket(datagramSocket: DatagramSocket!): ParcelFileDescriptor!
```

Create a new ParcelFileDescriptor from the specified DatagramSocket. The new ParcelFileDescriptor holds a dup of the original FileDescriptor in the DatagramSocket, so you must still close the DatagramSocket as well as the new ParcelFileDescriptor.

**WARNING:**Prior to API level 29, this function would not actually dup the DatagramSocket's FileDescriptor, and would take a reference to the its internal FileDescriptor instead. If the DatagramSocket gets garbage collected before the ParcelFileDescriptor, this may lead to the ParcelFileDescriptor being unexpectedly closed. To avoid this, the following pattern can be used: 

```kotlin
<code>ParcelFileDescriptor pfd = ParcelFileDescriptor.fromDatagramSocket(socket).dup();
  </code>
```

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `datagramSocket` | [DatagramSocket](../java/net/DatagramSocket.md)!:The DatagramSocket whose FileDescriptor is used to create a new ParcelFileDescriptor. |

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | A new ParcelFileDescriptor with a duped copy of the FileDescriptor of the specified Socket. |

| Exceptions ||
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.UncheckedIOException` | if [dup(java.io.FileDescriptor)](../android/os/ParcelFileDescriptor.md))throws IOException. |

### fromFd

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromFd(fd: Int): ParcelFileDescriptor!
```

Create a new ParcelFileDescriptor from a raw native fd. The new ParcelFileDescriptor holds a dup of the original fd passed in here, so you must still close that fd as well as the new ParcelFileDescriptor.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The native fd that the ParcelFileDescriptor should dup. |

| Return ||
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | Returns a new ParcelFileDescriptor holding a FileDescriptor for a dup of the given fd. |

### fromSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromSocket(socket: Socket!): ParcelFileDescriptor!
```

Create a new ParcelFileDescriptor from the specified Socket. The new ParcelFileDescriptor holds a dup of the original FileDescriptor in the Socket, so you must still close the Socket as well as the new ParcelFileDescriptor.

**WARNING:**Prior to API level 29, this function would not actually dup the Socket's FileDescriptor, and would take a reference to the its internal FileDescriptor instead. If the Socket gets garbage collected before the ParcelFileDescriptor, this may lead to the ParcelFileDescriptor being unexpectedly closed. To avoid this, the following pattern can be used: 

```kotlin
<code>ParcelFileDescriptor pfd = ParcelFileDescriptor.fromSocket(socket).dup();
  </code>
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `socket` | [Socket](../java/net/Socket.md)!:The Socket whose FileDescriptor is used to create a new ParcelFileDescriptor. |

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | A new ParcelFileDescriptor with a duped copy of the FileDescriptor of the specified Socket. |

| Exceptions ||
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.UncheckedIOException` | if [dup(java.io.FileDescriptor)](../android/os/ParcelFileDescriptor.md))throws IOException. |

### getFd

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFd(): Int
```

Return the native fd int for this ParcelFileDescriptor. The ParcelFileDescriptor still owns the fd, and it still must be closed through this API.

**WARNING:**Do not call close on the return value of this function or pass it to a function that assumes ownership of the fd. 

### getFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFileDescriptor(): FileDescriptor!
```

Retrieve the actual FileDescriptor associated with this object.

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [FileDescriptor](../java/io/FileDescriptor.md)! | Returns the FileDescriptor associated with this object. |

### getStatSize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatSize(): Long
```

Return the total size of the file representing this fd, as determined by`stat()`. Returns -1 if the fd is not a file. 

### open

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(
    file: File!, 
    mode: Int
): ParcelFileDescriptor!
```

Create a new ParcelFileDescriptor accessing a given file.

This method should only be used for files that you have direct access to; if you'd like to work with files hosted outside your app, use an API like [ContentResolver.openFile(Uri, String, CancellationSignal)](../android/content/ContentResolver.md)).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](../java/io/File.md)!:The file to be opened. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired access mode, must be one of [MODE_READ_ONLY](../android/os/ParcelFileDescriptor.md), [MODE_WRITE_ONLY](../android/os/ParcelFileDescriptor.md), or [MODE_READ_WRITE](../android/os/ParcelFileDescriptor.md); may also be any combination of [MODE_CREATE](../android/os/ParcelFileDescriptor.md), [MODE_TRUNCATE](../android/os/ParcelFileDescriptor.md), [MODE_WORLD_READABLE](../android/os/ParcelFileDescriptor.md), and [MODE_WORLD_WRITEABLE](../android/os/ParcelFileDescriptor.md). |

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | a new ParcelFileDescriptor pointing to the given file. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | if the given file does not exist or can not be opened with the requested mode. |

**See Also**

- [#parseMode(String)](../android/os/ParcelFileDescriptor.md)) 

### open

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(
    file: File!, 
    mode: Int, 
    handler: Handler!, 
    listener: ParcelFileDescriptor.OnCloseListener!
): ParcelFileDescriptor!
```

Create a new ParcelFileDescriptor accessing a given file.

This method should only be used for files that you have direct access to; if you'd like to work with files hosted outside your app, use an API like [ContentResolver.openFile(Uri, String, CancellationSignal)](../android/content/ContentResolver.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](../java/io/File.md)!:The file to be opened. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired access mode, must be one of [MODE_READ_ONLY](../android/os/ParcelFileDescriptor.md), [MODE_WRITE_ONLY](../android/os/ParcelFileDescriptor.md), or [MODE_READ_WRITE](../android/os/ParcelFileDescriptor.md); may also be any combination of [MODE_CREATE](../android/os/ParcelFileDescriptor.md), [MODE_TRUNCATE](../android/os/ParcelFileDescriptor.md), [MODE_WORLD_READABLE](../android/os/ParcelFileDescriptor.md), and [MODE_WORLD_WRITEABLE](../android/os/ParcelFileDescriptor.md). |
| `handler` | [Handler](../android/os/Handler.md)!:to call listener from; must not be null. |
| --- | --- |
| `listener` | [ParcelFileDescriptor.OnCloseListener](../android/os/ParcelFileDescriptor.OnCloseListener.md)!:to be invoked when the returned descriptor has been closed; must not be null. |

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | a new ParcelFileDescriptor pointing to the given file. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | if the given file does not exist or can not be opened with the requested mode. |

**See Also**

- [#parseMode(String)](../android/os/ParcelFileDescriptor.md)) 

### parseMode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parseMode(mode: String!): Int
```

Converts a string representing a file mode, such as "rw", into a bitmask suitable for use with #open.

The argument must define at least one of the following base access modes:

- "r" indicates the file should be opened in read-only mode, equivalent to [OsConstants.O_RDONLY](../android/system/OsConstants.md).
- "w" indicates the file should be opened in write-only mode, equivalent to [OsConstants.O_WRONLY](../android/system/OsConstants.md).
- "rw" indicates the file should be opened in read-write mode, equivalent to [OsConstants.O_RDWR](../android/system/OsConstants.md).

In addition to a base access mode, the following additional modes may requested:

<!-- -->

- "a" indicates the file should be opened in append mode, equivalent to [OsConstants.O_APPEND](../android/system/OsConstants.md). Before each write, the file offset is positioned at the end of the file.
- "t" indicates the file should be opened in truncate mode, equivalent to [OsConstants.O_TRUNC](../android/system/OsConstants.md). If the file already exists and is a regular file and is opened for writing, it will be truncated to length 0.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A bitmask representing the given file mode. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the given string does not match a known file mode. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### wrap

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(
    pfd: ParcelFileDescriptor, 
    handler: Handler, 
    listener: ParcelFileDescriptor.OnCloseListener
): ParcelFileDescriptor
```

Create a new ParcelFileDescriptor wrapping an already-opened file.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pfd` | [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md):The already-opened file. This value cannot be`null`. |
| `handler` | [Handler](../android/os/Handler.md):to call listener from. This value cannot be`null`. |
| `listener` | [ParcelFileDescriptor.OnCloseListener](../android/os/ParcelFileDescriptor.OnCloseListener.md):to be invoked when the returned descriptor has been closed. This value cannot be`null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) | a new ParcelFileDescriptor pointing to the given file. This value cannot be`null`. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel. If [Parcelable.PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) is set in flags, the file descriptor will be closed after a copy is written to the Parcel.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ParcelFileDescriptor!>
```
