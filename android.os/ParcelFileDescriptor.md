# ParcelFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParcelFileDescriptor

Kotlin| [Java](https://developer.android.com/reference/android/os/ParcelFileDescriptor "View this page in Java") 
| --- | --- |

```
open class ParcelFileDescriptor : Closeable, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#) |

The FileDescriptor returned by [Parcel.readFileDescriptor](https://developer.android.com/reference/kotlin/android/os/Parcel#readFileDescriptor()), allowing you to close it when done with it.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [AutoCloseInputStream](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.AutoCloseInputStream) An InputStream you can create on a ParcelFileDescriptor, which will take care of calling android. |
| open | [AutoCloseOutputStream](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.AutoCloseOutputStream) An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android. |
| open | [FileDescriptorDetachedException](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.FileDescriptorDetachedException) Exception that indicates that the file descriptor was detached. |
| --- | --- |
| abstract | [OnCloseListener](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.OnCloseListener) Callback indicating that a ParcelFileDescriptor has been closed. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_APPEND](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_APPEND:kotlin.Int) For use with #open: append to end of file while writing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_CREATE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_CREATE:kotlin.Int) For use with #open: create the file if it doesn't already exist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_READ_ONLY](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_READ_ONLY:kotlin.Int) For use with #open: open the file with read-only access. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_READ_WRITE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_READ_WRITE:kotlin.Int) For use with #open: open the file with read and write access. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_TRUNCATE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_TRUNCATE:kotlin.Int) For use with #open: erase contents of file when opening. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_WORLD_READABLE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_WORLD_READABLE:kotlin.Int) For use with #open: if [MODE_CREATE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_CREATE:kotlin.Int) has been supplied and this file doesn't already exist, then create the file with permissions such that any application can read it. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_WORLD_WRITEABLE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_WORLD_WRITEABLE:kotlin.Int) For use with #open: if [MODE_CREATE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_CREATE:kotlin.Int) has been supplied and this file doesn't already exist, then create the file with permissions such that any application can write it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_WRITE_ONLY](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_WRITE_ONLY:kotlin.Int) For use with #open: open the file with write-only access. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#ParcelFileDescriptor(android.os.ParcelFileDescriptor))`(`wrapped:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)!`)` Create a new ParcelFileDescriptor wrapped around another descriptor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | [adoptFd](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#adoptFd(kotlin.Int))`(`fd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Take ownership of a raw native fd in to a new ParcelFileDescriptor. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canDetectErrors](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#canDetectErrors())`()` Indicates if this ParcelFileDescriptor can communicate and detect remote errors/crashes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkError](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#checkError())`()` Detect and throw if the other end of a pipe or socket pair encountered an error or crashed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#close())`()` Close the ParcelFileDescriptor. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeWithError](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#closeWithError(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Close the ParcelFileDescriptor, informing any peer that an error occurred while processing. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)!\>! | [createPipe](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#createPipe())`()` Create two ParcelFileDescriptors structured as a data pipe. |
| --- | --- |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)!\>! | [createReliablePipe](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#createReliablePipe())`()` Create two ParcelFileDescriptors structured as a data pipe. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)!\>! | [createReliableSocketPair](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#createReliableSocketPair())`()` Create two ParcelFileDescriptors structured as a pair of sockets connected to each other. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)!\>! | [createSocketPair](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#createSocketPair())`()` Create two ParcelFileDescriptors structured as a pair of sockets connected to each other. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#describeContents())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [detachFd](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#detachFd())`()` Return the native fd int for this ParcelFileDescriptor and detach it from the object here. |
| open [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | [dup](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#dup())`()` Create a new ParcelFileDescriptor that is a dup of the existing FileDescriptor. |
| --- | --- |
| openstatic [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | [dup](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#dup(java.io.FileDescriptor))`(`orig:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`)` Create a new ParcelFileDescriptor that is a dup of an existing FileDescriptor. |
| openstatic [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | [fromDatagramSocket](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#fromDatagramSocket(java.net.DatagramSocket))`(`datagramSocket:` ` [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#)!`)` Create a new ParcelFileDescriptor from the specified DatagramSocket. |
| openstatic [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | [fromFd](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#fromFd(kotlin.Int))`(`fd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new ParcelFileDescriptor from a raw native fd. |
| --- | --- |
| openstatic [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | [fromSocket](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#fromSocket(java.net.Socket))`(`socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`)` Create a new ParcelFileDescriptor from the specified Socket. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFd](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#getFd())`()` Return the native fd int for this ParcelFileDescriptor. |
| open [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)! | [getFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#getFileDescriptor())`()` Retrieve the actual FileDescriptor associated with this object. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStatSize](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#getStatSize())`()` Return the total size of the file representing this fd, as determined by`stat()`. |
| openstatic [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | [open](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#open(java.io.File,%20kotlin.Int))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new ParcelFileDescriptor accessing a given file. |
| openstatic [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | [open](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#open(java.io.File,%20kotlin.Int,%20android.os.Handler,%20android.os.ParcelFileDescriptor.OnCloseListener))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`, `listener:` ` [ParcelFileDescriptor.OnCloseListener](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.OnCloseListener)!`)` Create a new ParcelFileDescriptor accessing a given file. |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parseMode](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#parseMode(kotlin.String))`(`mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Converts a string representing a file mode, such as "rw", into a bitmask suitable for use with #open. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#toString())`()` <br /> |
| openstatic [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#) | [wrap](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#wrap(android.os.ParcelFileDescriptor,%20android.os.Handler,%20android.os.ParcelFileDescriptor.OnCloseListener))`(`pfd:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)`, `listener:` ` [ParcelFileDescriptor.OnCloseListener](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.OnCloseListener)`)` Create a new ParcelFileDescriptor wrapping an already-opened file. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#finalize())`()` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator)\< [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#CREATOR:android.os.Parcelable.Creator) <br /> |

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

**Deprecated:** *Creating world-readable files is very dangerous, and likely to cause security holes in applications. It is strongly discouraged; instead, applications should use more formal mechanism for interactions such as [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#), [BroadcastReceiver](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#), and [android.app.Service](https://developer.android.com/reference/kotlin/android/app/Service.html#). There are no guarantees that this access mode will remain on a file, such as when it goes through a backup and restore.*

For use with #open: if [MODE_CREATE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_CREATE:kotlin.Int) has been supplied and this file doesn't already exist, then create the file with permissions such that any application can read it. 

 Value: 1

### MODE_WORLD_WRITEABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_WORLD_WRITEABLE: Int
```

**Deprecated:** *Creating world-writable files is very dangerous, and likely to cause security holes in applications. It is strongly discouraged; instead, applications should use more formal mechanism for interactions such as [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#), [BroadcastReceiver](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#), and [android.app.Service](https://developer.android.com/reference/kotlin/android/app/Service.html#). There are no guarantees that this access mode will remain on a file, such as when it goes through a backup and restore.*

For use with #open: if [MODE_CREATE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_CREATE:kotlin.Int) has been supplied and this file doesn't already exist, then create the file with permissions such that any application can write it. 

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
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | Returns a new ParcelFileDescriptor holding a FileDescriptor for the given fd. |

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
| `android.os.ParcelFileDescriptor.FileDescriptorDetachedException` | if the remote side called [detachFd()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#detachFd()). Once detached, the remote side is unable to communicate any errors through [closeWithError(java.lang.String)](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#closeWithError(kotlin.String)). |

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

The write end has the ability to deliver an error message through [closeWithError(java.lang.String)](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#closeWithError(kotlin.String))which can be handled by the read end calling [checkError()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#checkError()), usually after detecting an EOF. This can also be used to detect remote crashes. 

### createReliableSocketPair

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createReliableSocketPair(): Array<ParcelFileDescriptor!>!
```

Create two ParcelFileDescriptors structured as a pair of sockets connected to each other. The two sockets are indistinguishable.

Both ends have the ability to deliver an error message through [closeWithError(java.lang.String)](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#closeWithError(kotlin.String))which can be detected by the other end calling [checkError()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#checkError()), usually after detecting an EOF. This can also be used to detect remote crashes. 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### detachFd

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun detachFd(): Int
```

Return the native fd int for this ParcelFileDescriptor and detach it from the object here. You are now responsible for closing the fd in native code.

You should not detach when the original creator of the descriptor is expecting a reliable signal through #close() or [closeWithError(java.lang.String)](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#closeWithError(kotlin.String)). 
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
| `datagramSocket` | [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#)!:The DatagramSocket whose FileDescriptor is used to create a new ParcelFileDescriptor. |

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | A new ParcelFileDescriptor with a duped copy of the FileDescriptor of the specified Socket. |

| Exceptions ||
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.UncheckedIOException` | if [dup(java.io.FileDescriptor)](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#dup(java.io.FileDescriptor))throws IOException. |

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
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | Returns a new ParcelFileDescriptor holding a FileDescriptor for a dup of the given fd. |

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
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:The Socket whose FileDescriptor is used to create a new ParcelFileDescriptor. |

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | A new ParcelFileDescriptor with a duped copy of the FileDescriptor of the specified Socket. |

| Exceptions ||
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.UncheckedIOException` | if [dup(java.io.FileDescriptor)](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#dup(java.io.FileDescriptor))throws IOException. |

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
| [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)! | Returns the FileDescriptor associated with this object. |

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

This method should only be used for files that you have direct access to; if you'd like to work with files hosted outside your app, use an API like [ContentResolver.openFile(Uri, String, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:The file to be opened. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired access mode, must be one of [MODE_READ_ONLY](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_READ_ONLY:kotlin.Int), [MODE_WRITE_ONLY](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_WRITE_ONLY:kotlin.Int), or [MODE_READ_WRITE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_READ_WRITE:kotlin.Int); may also be any combination of [MODE_CREATE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_CREATE:kotlin.Int), [MODE_TRUNCATE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_TRUNCATE:kotlin.Int), [MODE_WORLD_READABLE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_WORLD_READABLE:kotlin.Int), and [MODE_WORLD_WRITEABLE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_WORLD_WRITEABLE:kotlin.Int). |

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | a new ParcelFileDescriptor pointing to the given file. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | if the given file does not exist or can not be opened with the requested mode. |

**See Also**

- [#parseMode(String)](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#parseMode(kotlin.String)) 

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

This method should only be used for files that you have direct access to; if you'd like to work with files hosted outside your app, use an API like [ContentResolver.openFile(Uri, String, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:The file to be opened. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired access mode, must be one of [MODE_READ_ONLY](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_READ_ONLY:kotlin.Int), [MODE_WRITE_ONLY](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_WRITE_ONLY:kotlin.Int), or [MODE_READ_WRITE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_READ_WRITE:kotlin.Int); may also be any combination of [MODE_CREATE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_CREATE:kotlin.Int), [MODE_TRUNCATE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_TRUNCATE:kotlin.Int), [MODE_WORLD_READABLE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_WORLD_READABLE:kotlin.Int), and [MODE_WORLD_WRITEABLE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#MODE_WORLD_WRITEABLE:kotlin.Int). |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!:to call listener from; must not be null. |
| --- | --- |
| `listener` | [ParcelFileDescriptor.OnCloseListener](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.OnCloseListener)!:to be invoked when the returned descriptor has been closed; must not be null. |

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#)! | a new ParcelFileDescriptor pointing to the given file. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | if the given file does not exist or can not be opened with the requested mode. |

**See Also**

- [#parseMode(String)](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#parseMode(kotlin.String)) 

### parseMode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parseMode(mode: String!): Int
```

Converts a string representing a file mode, such as "rw", into a bitmask suitable for use with #open.

The argument must define at least one of the following base access modes:

- "r" indicates the file should be opened in read-only mode, equivalent to [OsConstants.O_RDONLY](https://developer.android.com/reference/kotlin/android/system/OsConstants.html#O_RDONLY:kotlin.Int).
- "w" indicates the file should be opened in write-only mode, equivalent to [OsConstants.O_WRONLY](https://developer.android.com/reference/kotlin/android/system/OsConstants.html#O_WRONLY:kotlin.Int).
- "rw" indicates the file should be opened in read-write mode, equivalent to [OsConstants.O_RDWR](https://developer.android.com/reference/kotlin/android/system/OsConstants.html#O_RDWR:kotlin.Int).

In addition to a base access mode, the following additional modes may requested:

<!-- -->

- "a" indicates the file should be opened in append mode, equivalent to [OsConstants.O_APPEND](https://developer.android.com/reference/kotlin/android/system/OsConstants.html#O_APPEND:kotlin.Int). Before each write, the file offset is positioned at the end of the file.
- "t" indicates the file should be opened in truncate mode, equivalent to [OsConstants.O_TRUNC](https://developer.android.com/reference/kotlin/android/system/OsConstants.html#O_TRUNC:kotlin.Int). If the file already exists and is a regular file and is opened for writing, it will be truncated to length 0.

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
| `pfd` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#):The already-opened file. This value cannot be`null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler):to call listener from. This value cannot be`null`. |
| `listener` | [ParcelFileDescriptor.OnCloseListener](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.OnCloseListener):to be invoked when the returned descriptor has been closed. This value cannot be`null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#) | a new ParcelFileDescriptor pointing to the given file. This value cannot be`null`. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel. If [Parcelable.PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) is set in flags, the file descriptor will be closed after a copy is written to the Parcel.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

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
