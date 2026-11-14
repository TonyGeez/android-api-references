# FileInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileInputStream

```
open class FileInputStream : InputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.InputStream](InputStream.md) ||
| | ↳ | [java.io.FileInputStream](FileInputStream.md) |

| Known Direct Subclasses [ParcelFileDescriptor.AutoCloseInputStream](../android/os/ParcelFileDescriptor.AutoCloseInputStream.md) |--------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [ParcelFileDescriptor.AutoCloseInputStream](../android/os/ParcelFileDescriptor.AutoCloseInputStream.md) | An InputStream you can create on a ParcelFileDescriptor, which will take care of calling android. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AssetFileDescriptor.AutoCloseInputStream](../android/content/res/AssetFileDescriptor.AutoCloseInputStream.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [AssetFileDescriptor.AutoCloseInputStream](../android/content/res/AssetFileDescriptor.AutoCloseInputStream.md) | An InputStream you can create on a ParcelFileDescriptor, which will take care of calling android. | |
| --- | --- | --- | --- | --- | --- | --- |

A`FileInputStream`obtains input bytes from a file in a file system. What files are available depends on the host environment.

`FileInputStream`is meant for reading streams of raw bytes such as image data. For reading streams of characters, consider using`FileReader`.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileInputStream](FileInputStream.md))`(`file:` ` [File](File.md)!`)` Creates a`FileInputStream`by opening a connection to an actual file, the file named by the`File`object`file`in the file system. |
| [FileInputStream](FileInputStream.md))`(`fdObj:` ` [FileDescriptor](FileDescriptor.md)!`)` Creates a`FileInputStream`by using the file descriptor`fdObj`, which represents an existing connection to an actual file in the file system. |
| [FileInputStream](FileInputStream.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`FileInputStream`by opening a connection to an actual file, the file named by the path name`name`in the file system. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](FileInputStream.md))`()` Returns an estimate of the number of remaining bytes that can be read (or skipped over) from this input stream without blocking by the next invocation of a method for this input stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](FileInputStream.md))`()` Closes this file input stream and releases any system resources associated with the stream. |
| open [FileChannel](../java.nio.channels/FileChannel.md)! | [getChannel](FileInputStream.md))`()` Returns the unique [FileChannel](../java.nio.channels/FileChannel.md) object associated with this file input stream. |
| --- | --- |
| [FileDescriptor](FileDescriptor.md)! | [getFD](FileInputStream.md))`()` Returns the`FileDescriptor`object that represents the connection to the actual file in the file system being used by this`FileInputStream`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](FileInputStream.md))`()` Reads a byte of data from this input stream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](FileInputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Reads up to`b.length`bytes of data from this input stream into an array of bytes. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](FileInputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to`len`bytes of data from this input stream into an array of bytes. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](FileInputStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips over and discards`n`bytes of data from the input stream. |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](FileInputStream.md))`()` Ensures that the`close`method of this file input stream is called when there are no more references to it. |

| Inherited functions ||
|---|---|
| From class [InputStream](InputStream.md) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](InputStream.md))`(`readlimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Marks the current position in this input stream. A subsequent call to the`reset`method repositions this stream at the last marked position so that subsequent reads re-read the same bytes. The`readlimit`arguments tells this input stream to allow that many bytes to be read before the mark position gets invalidated. The general contract of`mark`is that, if the method`markSupported`returns`true`, the stream somehow remembers all the bytes read after the call to`mark`and stands ready to supply those same bytes again if and whenever the method`reset`is called. However, the stream is not required to remember any data at all if more than`readlimit`bytes are read from the stream before`reset`is called. Marking a closed stream should not have any effect on the stream. The`mark`method of`InputStream`does nothing. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](InputStream.md))`()` <br /> Tests if this input stream supports the`mark`and`reset`methods. Whether or not`mark`and`reset`are supported is an invariant property of a particular input stream instance. The`markSupported`method of`InputStream`returns`false`. <br /> | | [InputStream](InputStream.md)! | [nullInputStream](InputStream.md))`()` <br /> Returns a new`InputStream`that reads no bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`available()`,`read()`,`read(byte[])`,`read(byte[], int, int)`,`readAllBytes()`,`readNBytes(byte[], int, int)`,`readNBytes(int)`,`skip(long)`,`skipNBytes(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`method does nothing, and the`reset()`method throws`IOException`. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](InputStream.md))`()` <br /> Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readNBytes](InputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads the requested number of bytes from the input stream into the given byte array. This method blocks until`len`bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before`len`bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If`len`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read up to`len`bytes. The first byte read is stored into element`b[off]`, the next one in to`b[off+1]`, and so on. The number of bytes read is, at most, equal to`len`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[off]`through`b[off+`*k* `-1]`, leaving elements`b[off+`*k* `]`through`b[off+len-1]`unaffected. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of`b`have been updated with data from the input stream. Consequently the input stream and`b`may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readNBytes](InputStream.md))`(`len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If`len`is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to`len`bytes are read from the stream. Fewer than`len`bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by`len`. Therefore, the method may be safely called with very large values of`len`provided sufficient memory is available. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](InputStream.md))`()` <br /> Repositions this stream to the position at the time the`mark`method was last called on this input stream. The general contract of`reset`is: - If the method`markSupported`returns`true`, then: - If the method`mark`has not been called since the stream was created, or the number of bytes read from the stream since`mark`was last called is larger than the argument to`mark`at that last call, then an`IOException`might be thrown. - If such an`IOException`is not thrown, then the stream is reset to a state such that all the bytes read since the most recent call to`mark`(or since the start of the file, if`mark`has not been called) will be resupplied to subsequent callers of the`read`method, followed by any bytes that otherwise would have been the next input data as of the time of the call to`reset`. - If the method`markSupported`returns`false`, then: - The call to`reset`may throw an`IOException`. - If an`IOException`is not thrown, then the stream is reset to a fixed state that depends on the particular type of the input stream and how it was created. The bytes that will be supplied to subsequent callers of the`read`method depend on the particular type of the input stream. The method`reset`for class`InputStream`does nothing except throw an`IOException`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipNBytes](InputStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips over and discards exactly`n`bytes of data from this input stream. If`n`is zero, then no bytes are skipped. If`n`is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an`EOFException`is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](InputStream.md))`(`out:` ` [OutputStream](OutputStream.md)!`)` <br /> Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is*asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

## Public constructors

### FileInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileInputStream(file: File!)
```

Creates a`FileInputStream`by opening a connection to an actual file, the file named by the`File`object`file`in the file system. A new`FileDescriptor`object is created to represent this file connection.

First, if there is a security manager, its`checkRead`method is called with the path represented by the`file`argument as its argument.

If the named file does not exist, is a directory rather than a regular file, or for some other reason cannot be opened for reading then a`FileNotFoundException`is thrown.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `file` | [File](File.md)!:the file to be opened for reading. |

| Exceptions ||
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | if the file does not exist, is a directory rather than a regular file, or for some other reason cannot be opened for reading. |
| `java.lang.SecurityException` | if a security manager exists and its`checkRead`method denies read access to the file. |

**See Also**

- [java.io.File#getPath()](File.md))
- [java.lang.SecurityManager#checkRead(java.lang.String)](../java.lang/SecurityManager.md)) 

### FileInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileInputStream(fdObj: FileDescriptor!)
```

Creates a`FileInputStream`by using the file descriptor`fdObj`, which represents an existing connection to an actual file in the file system.

If there is a security manager, its`checkRead`method is called with the file descriptor`fdObj`as its argument to see if it's ok to read the file descriptor. If read access is denied to the file descriptor a`SecurityException`is thrown.

If`fdObj`is null then a`NullPointerException`is thrown.

This constructor does not throw an exception if`fdObj`is [invalid](FileDescriptor.md)). However, if the methods are invoked on the resulting stream to attempt I/O on the stream, an`IOException`is thrown.

Android-specific warning: #close() method doesn't close the`fdObj`provided, because this object doesn't own the file descriptor, but the caller does. The caller can call [android.system.Os#close(FileDescriptor)](../android.system/Os.md))to close the fd.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `fdObj` | [FileDescriptor](FileDescriptor.md)!:the file descriptor to be opened for reading. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkRead`method denies read access to the file descriptor. |

**See Also**

- [java.lang.SecurityManager#checkRead(java.io.FileDescriptor)](../java.lang/SecurityManager.md)) 

### FileInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileInputStream(name: String!)
```

Creates a`FileInputStream`by opening a connection to an actual file, the file named by the path name`name`in the file system. A new`FileDescriptor`object is created to represent this file connection.

First, if there is a security manager, its`checkRead`method is called with the`name`argument as its argument.

If the named file does not exist, is a directory rather than a regular file, or for some other reason cannot be opened for reading then a`FileNotFoundException`is thrown.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the system-dependent file name. |

| Exceptions ||
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | if the file does not exist, is a directory rather than a regular file, or for some other reason cannot be opened for reading. |
| `java.lang.SecurityException` | if a security manager exists and its`checkRead`method denies read access to the file. |

**See Also**

- [java.lang.SecurityManager#checkRead(java.lang.String)](../java.lang/SecurityManager.md))

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun available(): Int
```

Returns an estimate of the number of remaining bytes that can be read (or skipped over) from this input stream without blocking by the next invocation of a method for this input stream. Returns 0 when the file position is beyond EOF. The next invocation might be the same thread or another thread. A single read or skip of this many bytes will not block, but may read or skip fewer bytes.

In some cases, a non-blocking read (or skip) may appear to be blocked when it is merely slow, for example when reading large files over slow networks.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an estimate of the number of remaining bytes that can be read (or skipped over) from this input stream without blocking. |

| Exceptions ||
|-----------------------|------------------------------------------------------------------------------------|
| `java.io.IOException` | if this file input stream has been closed by calling`close`or an I/O error occurs. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this file input stream and releases any system resources associated with the stream.

If this stream has an associated channel then the channel is closed as well.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |

### getChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChannel(): FileChannel!
```

Returns the unique [FileChannel](../java.nio.channels/FileChannel.md) object associated with this file input stream.

The initial [position](../java.nio.channels/FileChannel.md))of the returned channel will be equal to the number of bytes read from the file so far. Reading bytes from this stream will increment the channel's position. Changing the channel's position, either explicitly or by reading, will change this stream's file position.

| Return ||
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [FileChannel](../java.nio.channels/FileChannel.md)! | the file channel associated with this file input stream |

### getFD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFD(): FileDescriptor!
```

Returns the`FileDescriptor`object that represents the connection to the actual file in the file system being used by this`FileInputStream`.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [FileDescriptor](FileDescriptor.md)! | the file descriptor object associated with this stream. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- [java.io.FileDescriptor](FileDescriptor.md) 

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

Reads a byte of data from this input stream. This method blocks if no input is yet available.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next byte of data, or`-1`if the end of the file is reached. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(b: ByteArray!): Int
```

Reads up to`b.length`bytes of data from this input stream into an array of bytes. This method blocks until some input is available.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of bytes read into the buffer, or`-1`if there is no more data because the end of the file has been reached. |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.lang.NullPointerException` | if`b`is`null`. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads up to`len`bytes of data from this input stream into an array of bytes. If`len`is not zero, the method blocks until some input is available; otherwise, no bytes are read and`0`is returned.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the destination array`b` |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes read. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of bytes read into the buffer, or`-1`if there is no more data because the end of the file has been reached. |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.lang.NullPointerException` | If`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative,`len`is negative, or`len`is greater than`b.length - off` |
| --- | --- |

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

Skips over and discards`n`bytes of data from the input stream.

The`skip`method may, for a variety of reasons, end up skipping over some smaller number of bytes, possibly`0`. If`n`is negative, the method will try to skip backwards. In case the backing file does not support backward skip at its current position, an`IOException`is thrown. The actual number of bytes skipped is returned. If it skips forwards, it returns a positive value. If it skips backwards, it returns a negative value.

This method may skip more bytes than what are remaining in the backing file. This produces no exception and the number of bytes skipped may include some number of bytes that were beyond the EOF of the backing file. Attempting to read from the stream after skipping past the end will result in -1 indicating the end of the file.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to be skipped. |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the actual number of bytes skipped. |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------|
| `java.io.IOException` | if n is negative, if the stream does not support seek, or if an I/O error occurs. |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

Ensures that the`close`method of this file input stream is called when there are no more references to it.

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
| `java.io.IOException` | if an I/O error occurs. |

**See Also**
