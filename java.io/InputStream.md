# InputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputStream

```
abstract class InputStream : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.io.InputStream](../java/io/InputStream.md) |

| Known Direct Subclasses [AssetManager.AssetInputStream](../android/content/res/AssetManager.AssetInputStream.md), [BackupDataInputStream](../android/app/backup/BackupDataInputStream.md), [ByteArrayInputStream](../java/io/ByteArrayInputStream.md), [FileInputStream](../java/io/FileInputStream.md), [FilterInputStream](../java/io/FilterInputStream.md), [ObjectInputStream](../java/io/ObjectInputStream.md), [PipedInputStream](../java/io/PipedInputStream.md), [SequenceInputStream](../java/io/SequenceInputStream.md), [StringBufferInputStream](../java/io/StringBufferInputStream.md) |-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AssetManager.AssetInputStream](../android/content/res/AssetManager.AssetInputStream.md) | <br /> | | [BackupDataInputStream](../android/app/backup/BackupDataInputStream.md) | Provides an [java.io.InputStream](../java/io/InputStream.md)-like interface for accessing an entity's data during a restore operation. | | [ByteArrayInputStream](../java/io/ByteArrayInputStream.md) | A`ByteArrayInputStream`contains an internal buffer that contains bytes that may be read from the stream. | | [FileInputStream](../java/io/FileInputStream.md) | A`FileInputStream`obtains input bytes from a file in a file system. | | [FilterInputStream](../java/io/FilterInputStream.md) | A`FilterInputStream`contains some other input stream, which it uses as its basic source of data, possibly transforming the data along the way or providing additional functionality. | | [ObjectInputStream](../java/io/ObjectInputStream.md) | An ObjectInputStream deserializes primitive data and objects previously written using an ObjectOutputStream. | | [PipedInputStream](../java/io/PipedInputStream.md) | A piped input stream should be connected to a piped output stream; the piped input stream then provides whatever data bytes are written to the piped output stream. | | [SequenceInputStream](../java/io/SequenceInputStream.md) | A`SequenceInputStream`represents the logical concatenation of other input streams. | | [StringBufferInputStream](../java/io/StringBufferInputStream.md) | This class allows an application to create an input stream in which the bytes read are supplied by the contents of a string. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AssetFileDescriptor.AutoCloseInputStream](../android/content/res/AssetFileDescriptor.AutoCloseInputStream.md), [Base64InputStream](../android/util/Base64InputStream.md), [BufferedInputStream](../java/io/BufferedInputStream.md), [CheckedInputStream](../java/util/zip/CheckedInputStream.md), [CipherInputStream](../javax/crypto/CipherInputStream.md), [DataInputStream](../java/io/DataInputStream.md), [DeflaterInputStream](../java/util/zip/DeflaterInputStream.md), [DigestInputStream](../java/security/DigestInputStream.md), [GZIPInputStream](../java/util/zip/GZIPInputStream.md), [InflaterInputStream](../java/util/zip/InflaterInputStream.md), [JarInputStream](../java/util/jar/JarInputStream.md), [LineNumberInputStream](../java/io/LineNumberInputStream.md), and 3 others. |---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AssetFileDescriptor.AutoCloseInputStream](../android/content/res/AssetFileDescriptor.AutoCloseInputStream.md) | An InputStream you can create on a ParcelFileDescriptor, which will take care of calling android. | | [Base64InputStream](../android/util/Base64InputStream.md) | An InputStream that does Base64 decoding on the data read through it. | | [BufferedInputStream](../java/io/BufferedInputStream.md) | A`BufferedInputStream`adds functionality to another input stream-namely, the ability to buffer the input and to support the`mark`and`reset`methods. | | [CheckedInputStream](../java/util/zip/CheckedInputStream.md) | An input stream that also maintains a checksum of the data being read. | | [CipherInputStream](../javax/crypto/CipherInputStream.md) | A CipherInputStream is composed of an InputStream and a Cipher so that read() methods return data that are read in from the underlying InputStream but have been additionally processed by the Cipher. | | [DataInputStream](../java/io/DataInputStream.md) | A data input stream lets an application read primitive Java data types from an underlying input stream in a machine-independent way. | | [DeflaterInputStream](../java/util/zip/DeflaterInputStream.md) | Implements an input stream filter for compressing data in the "deflate" compression format. | | [DigestInputStream](../java/security/DigestInputStream.md) | A transparent stream that updates the associated message digest using the bits going through the stream. | | [GZIPInputStream](../java/util/zip/GZIPInputStream.md) | This class implements a stream filter for reading compressed data in the GZIP file format. | | [InflaterInputStream](../java/util/zip/InflaterInputStream.md) | This class implements a stream filter for uncompressing data in the "deflate" compression format. | | [JarInputStream](../java/util/jar/JarInputStream.md) | The`JarInputStream`class is used to read the contents of a JAR file from any input stream. | | [LineNumberInputStream](../java/io/LineNumberInputStream.md) | This class is an input stream filter that provides the added functionality of keeping track of the current line number. | | [ParcelFileDescriptor.AutoCloseInputStream](../android/os/ParcelFileDescriptor.AutoCloseInputStream.md) | An InputStream you can create on a ParcelFileDescriptor, which will take care of calling android. | | [PushbackInputStream](../java/io/PushbackInputStream.md) | A`PushbackInputStream`adds functionality to another input stream, namely the ability to "push back" or "unread" bytes, by storing pushed-back bytes in an internal buffer. | | [ZipInputStream](../java/util/zip/ZipInputStream.md) | This class implements an input stream filter for reading files in the ZIP file format. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This abstract class is the superclass of all classes representing an input stream of bytes.

Applications that need to define a subclass of`InputStream`must always provide a method that returns the next byte of input.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------|---|
| [InputStream](../java/io/InputStream.md))`()` Constructor for subclasses to call. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](../java/io/InputStream.md))`()` Returns an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking, which may be 0, or 0 when end of stream is detected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/io/InputStream.md))`()` Closes this input stream and releases any system resources associated with the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](../java/io/InputStream.md))`(`readlimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Marks the current position in this input stream. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](../java/io/InputStream.md))`()` Tests if this input stream supports the`mark`and`reset`methods. |
| openstatic [InputStream](../java/io/InputStream.md)! | [nullInputStream](../java/io/InputStream.md))`()` Returns a new`InputStream`that reads no bytes. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](../java/io/InputStream.md))`()` Reads the next byte of data from the input stream. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](../java/io/InputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Reads some number of bytes from the input stream and stores them into the buffer array`b`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](../java/io/InputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to`len`bytes of data from the input stream into an array of bytes. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](../java/io/InputStream.md))`()` Reads all remaining bytes from the input stream. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readNBytes](../java/io/InputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads the requested number of bytes from the input stream into the given byte array. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readNBytes](../java/io/InputStream.md))`(`len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to a specified number of bytes from the input stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../java/io/InputStream.md))`()` Repositions this stream to the position at the time the`mark`method was last called on this input stream. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](../java/io/InputStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips over and discards`n`bytes of data from this input stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipNBytes](../java/io/InputStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips over and discards exactly`n`bytes of data from this input stream. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](../java/io/InputStream.md))`(`out:` ` [OutputStream](../java/io/OutputStream.md)!`)` Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. |
| --- | --- |

## Public constructors

### InputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputStream()
```

Constructor for subclasses to call.

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun available(): Int
```

Returns an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking, which may be 0, or 0 when end of stream is detected. The read might be on the same thread or another thread. A single read or skip of this many bytes will not block, but may read or skip fewer bytes.

Note that while some implementations of`InputStream`will return the total number of bytes in the stream, many will not. It is never correct to use the return value of this method to allocate a buffer intended to hold all data in this stream.

A subclass's implementation of this method may choose to throw an [IOException](../java/io/IOException.md) if this input stream has been closed by invoking the #close() method.

The`available`method of`InputStream`always returns`0`.

This method should be overridden by subclasses.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking or`0`when it reaches the end of the input stream. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this input stream and releases any system resources associated with the stream.

The`close`method of`InputStream`does nothing.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mark(readlimit: Int): Unit
```

Marks the current position in this input stream. A subsequent call to the`reset`method repositions this stream at the last marked position so that subsequent reads re-read the same bytes.

The`readlimit`arguments tells this input stream to allow that many bytes to be read before the mark position gets invalidated.

The general contract of`mark`is that, if the method`markSupported`returns`true`, the stream somehow remembers all the bytes read after the call to`mark`and stands ready to supply those same bytes again if and whenever the method`reset`is called. However, the stream is not required to remember any data at all if more than`readlimit`bytes are read from the stream before`reset`is called.

Marking a closed stream should not have any effect on the stream.

The`mark`method of`InputStream`does nothing.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `readlimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum limit of bytes that can be read before the mark position becomes invalid. |

**See Also**

- [java.io.InputStream#reset()](../java/io/InputStream.md)) 

### markSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun markSupported(): Boolean
```

Tests if this input stream supports the`mark`and`reset`methods. Whether or not`mark`and`reset`are supported is an invariant property of a particular input stream instance. The`markSupported`method of`InputStream`returns`false`.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this stream instance supports the mark and reset methods;`false`otherwise. |

**See Also**

- [java.io.InputStream#mark(int)](../java/io/InputStream.md))
- [java.io.InputStream#reset()](../java/io/InputStream.md)) 

### nullInputStream

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun nullInputStream(): InputStream!
```

Returns a new`InputStream`that reads no bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect.

While the stream is open, the`available()`,`read()`,`read(byte[])`,`read(byte[], int, int)`,`readAllBytes()`,`readNBytes(byte[], int, int)`,`readNBytes(int)`,`skip(long)`,`skipNBytes(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`.

The`markSupported()`method returns`false`. The`mark()`method does nothing, and the`reset()`method throws`IOException`.

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------|
| [InputStream](../java/io/InputStream.md)! | an`InputStream`which contains no bytes |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(): Int
```

Reads the next byte of data from the input stream. The value byte is returned as an`int`in the range`0`to`255`. If no byte is available because the end of the stream has been reached, the value`-1`is returned. This method blocks until input data is available, the end of the stream is detected, or an exception is thrown.

A subclass must provide an implementation of this method.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next byte of data, or`-1`if the end of the stream is reached. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(b: ByteArray!): Int
```

Reads some number of bytes from the input stream and stores them into the buffer array`b`. The number of bytes actually read is returned as an integer. This method blocks until input data is available, end of file is detected, or an exception is thrown.

If the length of`b`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read at least one byte. If no byte is available because the stream is at the end of the file, the value`-1`is returned; otherwise, at least one byte is read and stored into`b`.

The first byte read is stored into element`b[0]`, the next one into`b[1]`, and so on. The number of bytes read is, at most, equal to the length of`b`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[0]`through`b[`*k* `-1]`, leaving elements`b[`*k* `]`through`b[b.length-1]`unaffected.

The`read(b)`method for class`InputStream`has the same effect as: 

```kotlin
<code>read(b, 0, b.length) </code>
```

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of bytes read into the buffer, or`-1`if there is no more data because the end of the stream has been reached. |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If the first byte cannot be read for any reason other than the end of the file, if the input stream has been closed, or if some other I/O error occurs. |
| `java.lang.NullPointerException` | if`b`is`null`. |

**See Also**

- [java.io.InputStream#read(byte[], int, int)](https://developer.android.com/reference/kotlin/java/io/InputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)) 

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads up to`len`bytes of data from the input stream into an array of bytes. An attempt is made to read as many as`len`bytes, but a smaller number may be read. The number of bytes actually read is returned as an integer.

This method blocks until input data is available, end of file is detected, or an exception is thrown.

If`len`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read at least one byte. If no byte is available because the stream is at end of file, the value`-1`is returned; otherwise, at least one byte is read and stored into`b`.

The first byte read is stored into element`b[off]`, the next one into`b[off+1]`, and so on. The number of bytes read is, at most, equal to`len`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[off]`through`b[off+`*k* `-1]`, leaving elements`b[off+`*k* `]`through`b[off+len-1]`unaffected.

In every case, elements`b[0]`through`b[off-1]`and elements`b[off+len]`through`b[b.length-1]`are unaffected.

The`read(b, off, len)`method for class`InputStream`simply calls the method`read()`repeatedly. If the first such call results in an`IOException`, that exception is returned from the call to the`read(b,``off,``len)`method. If any subsequent call to`read()`results in a`IOException`, the exception is caught and treated as if it were end of file; the bytes read up to that point are stored into`b`and the number of bytes read before the exception occurred is returned. The default implementation of this method blocks until the requested amount of input data`len`has been read, end of file is detected, or an exception is thrown. Subclasses are encouraged to provide a more efficient implementation of this method.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in array`b`at which the data is written. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes to read. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of bytes read into the buffer, or`-1`if there is no more data because the end of the stream has been reached. |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If the first byte cannot be read for any reason other than end of file, or if the input stream has been closed, or if some other I/O error occurs. |
| `java.lang.NullPointerException` | If`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative,`len`is negative, or`len`is greater than`b.length - off` |
| --- | --- |

**See Also**

- [java.io.InputStream#read()](../java/io/InputStream.md)) 

### readAllBytes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readAllBytes(): ByteArray!
```

Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream.

When this stream reaches end of stream, further invocations of this method will return an empty byte array.

Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data.

The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified.

If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array containing the bytes read from this input stream |

| Exceptions ||
|------------------------------|-------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.OutOfMemoryError` | if an array of the required size cannot be allocated. |

### readNBytes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readNBytes(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads the requested number of bytes from the input stream into the given byte array. This method blocks until`len`bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream.

In the case where end of stream is reached before`len`bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero.

If`len`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read up to`len`bytes.

The first byte read is stored into element`b[off]`, the next one in to`b[off+1]`, and so on. The number of bytes read is, at most, equal to`len`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[off]`through`b[off+`*k* `-1]`, leaving elements`b[off+`*k* `]`through`b[off+len-1]`unaffected.

The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified.

If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of`b`have been updated with data from the input stream. Consequently the input stream and`b`may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the byte array into which the data is read |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in`b`at which the data is written |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes to read |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of bytes read into the buffer |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.NullPointerException` | if`b`is`null` |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative,`len`is negative, or`len`is greater than`b.length - off` |
| --- | --- |

### readNBytes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readNBytes(len: Int): ByteArray!
```

Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream.

The length of the returned array equals the number of bytes read from the stream. If`len`is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to`len`bytes are read from the stream. Fewer than`len`bytes may be read if end of stream is encountered.

When this stream reaches end of stream, further invocations of this method will return an empty byte array.

Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by`len`. Therefore, the method may be safely called with very large values of`len`provided sufficient memory is available.

The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified.

If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------|
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes to read |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array containing the bytes read from this input stream |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`length`is negative |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.OutOfMemoryError` | if an array of the required size cannot be allocated. |
| --- | --- |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Repositions this stream to the position at the time the`mark`method was last called on this input stream.

The general contract of`reset`is:

- If the method`markSupported`returns`true`, then:
 - If the method`mark`has not been called since the stream was created, or the number of bytes read from the stream since`mark`was last called is larger than the argument to`mark`at that last call, then an`IOException`might be thrown.
 - If such an`IOException`is not thrown, then the stream is reset to a state such that all the bytes read since the most recent call to`mark`(or since the start of the file, if`mark`has not been called) will be resupplied to subsequent callers of the`read`method, followed by any bytes that otherwise would have been the next input data as of the time of the call to`reset`.
- If the method`markSupported`returns`false`, then:
 - The call to`reset`may throw an`IOException`.
 - If an`IOException`is not thrown, then the stream is reset to a fixed state that depends on the particular type of the input stream and how it was created. The bytes that will be supplied to subsequent callers of the`read`method depend on the particular type of the input stream.

The method`reset`for class`InputStream`does nothing except throw an`IOException`.

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------|
| `java.io.IOException` | if this stream has not been marked or if the mark has been invalidated. |

**See Also**

- [java.io.InputStream#mark(int)](../java/io/InputStream.md))
- [java.io.IOException](../java/io/IOException.md) 

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

Skips over and discards`n`bytes of data from this input stream. The`skip`method may, for a variety of reasons, end up skipping over some smaller number of bytes, possibly`0`. This may result from any of a number of conditions; reaching end of file before`n`bytes have been skipped is only one possibility. The actual number of bytes skipped is returned. If`n`is negative, the`skip`method for class`InputStream`always returns 0, and no bytes are skipped. Subclasses may handle the negative value differently.

The`skip`method implementation of this class creates a byte array and then repeatedly reads into it until`n`bytes have been read or the end of the stream has been reached. Subclasses are encouraged to provide a more efficient implementation of this method. For instance, the implementation may depend on the ability to seek.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to be skipped. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the actual number of bytes skipped which might be zero. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- [java.io.InputStream#skipNBytes(long)](../java/io/InputStream.md)) 

### skipNBytes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skipNBytes(n: Long): Unit
```

Skips over and discards exactly`n`bytes of data from this input stream. If`n`is zero, then no bytes are skipped. If`n`is negative, then no bytes are skipped. Subclasses may handle the negative value differently.

This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown.

If end of stream is reached before the stream is at the desired position, then an`EOFException`is thrown.

If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to be skipped. |

| Exceptions ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if end of stream is encountered before the stream can be positioned`n`bytes beyond its position when this method was invoked. |
| `java.io.IOException` | if the stream cannot be positioned properly or if an I/O error occurs. |

**See Also**

- [java.io.InputStream#skip(long)](../java/io/InputStream.md)) 

### transferTo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun transferTo(out: OutputStream!): Long
```

Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream.

This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is*asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified.

If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java/io/OutputStream.md)!:the output stream, non-null |

| Return ||
|------------------------------------------------------------------------------|---------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of bytes transferred |

| Exceptions ||
|----------------------------------|------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when reading or writing |
| `java.lang.NullPointerException` | if`out`is`null` |
