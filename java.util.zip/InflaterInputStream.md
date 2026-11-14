# InflaterInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InflaterInputStream

```
open class InflaterInputStream : FilterInputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) |||
| | ↳ | [java.io.FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#) ||
| | | ↳ | [java.util.zip.InflaterInputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#) |
| --- | --- | --- | --- |

| Known Direct Subclasses [GZIPInputStream](https://developer.android.com/reference/kotlin/java/util/zip/GZIPInputStream), [ZipInputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream) |-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------| | [GZIPInputStream](https://developer.android.com/reference/kotlin/java/util/zip/GZIPInputStream) | This class implements a stream filter for reading compressed data in the GZIP file format. | | [ZipInputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream) | This class implements an input stream filter for reading files in the ZIP file format. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [JarInputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream.html#) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------| | [JarInputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream.html#) | The`JarInputStream`class is used to read the contents of a JAR file from any input stream. | |
| --- | --- | --- | --- | --- | --- | --- |

This class implements a stream filter for uncompressing data in the "deflate" compression format. It is also used as the basis for other decompression filters, such as GZIPInputStream.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InflaterInputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#InflaterInputStream(java.io.InputStream))`(`in:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Creates a new input stream with a default decompressor and buffer size. |
| [InflaterInputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#InflaterInputStream(java.io.InputStream,%20java.util.zip.Inflater))`(`in:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `inf:` ` [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater)!`)` Creates a new input stream with the specified decompressor and a default buffer size. |
| [InflaterInputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#InflaterInputStream(java.io.InputStream,%20java.util.zip.Inflater,%20kotlin.Int))`(`in:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `inf:` ` [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new input stream with the specified decompressor and buffer size. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#available())`()` Returns 0 after EOF has been reached, otherwise always return 1. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#close())`()` Closes this input stream and releases any system resources associated with the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#mark(kotlin.Int))`(`readlimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Marks the current position in this input stream. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#markSupported())`()` Tests if this input stream supports the`mark`and`reset`methods. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#read())`()` Reads a byte of uncompressed data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads uncompressed data into an array of bytes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#reset())`()` Repositions this stream to the position at the time the`mark`method was last called on this input stream. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips specified number of bytes of uncompressed data. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fill](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#fill())`()` Fills input buffer with more data to decompress. |

| Inherited functions ||
|---|---|
| From class [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [nullInputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#nullInputStream())`()` <br /> Returns a new`InputStream`that reads no bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`available()`,`read()`,`read(byte[])`,`read(byte[], int, int)`,`readAllBytes()`,`readNBytes(byte[], int, int)`,`readNBytes(int)`,`skip(long)`,`skipNBytes(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`method does nothing, and the`reset()`method throws`IOException`. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](https://developer.android.com/reference/kotlin/java/io/InputStream.html#readAllBytes())`()` <br /> Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream.html#readNBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads the requested number of bytes from the input stream into the given byte array. This method blocks until`len`bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before`len`bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If`len`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read up to`len`bytes. The first byte read is stored into element`b[off]`, the next one in to`b[off+1]`, and so on. The number of bytes read is, at most, equal to`len`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[off]`through`b[off+`*k* `-1]`, leaving elements`b[off+`*k* `]`through`b[off+len-1]`unaffected. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of`b`have been updated with data from the input stream. Consequently the input stream and`b`may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream.html#readNBytes(kotlin.Int))`(`len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If`len`is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to`len`bytes are read from the stream. Fewer than`len`bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by`len`. Therefore, the method may be safely called with very large values of`len`provided sufficient memory is available. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream.html#skipNBytes(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips over and discards exactly`n`bytes of data from this input stream. If`n`is zero, then no bytes are skipped. If`n`is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an`EOFException`is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](https://developer.android.com/reference/kotlin/java/io/InputStream.html#transferTo(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` <br /> Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is*asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||
| From class [FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#read(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Reads up to`b.length`bytes of data from this input stream into an array of bytes. This method blocks until some input is available. This method simply performs the call`read(b, 0, b.length)`and returns the result. It is important that it does*not* do`in.read(b)`instead; certain subclasses of`FilterInputStream`depend on the implementation strategy actually used. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [buf](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#buf:kotlin.ByteArray) Input buffer for decompression. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [closed](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#closed:kotlin.Boolean) Indicates whether the #close() method has been called, internal use only. |
| [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater)! | [inf](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#inf:java.util.zip.Inflater) Decompressor for this stream. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [len](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#len:kotlin.Int) Length of input buffer. |

| Inherited properties ||
|---|---|
| From class [FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#) |------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#in:java.io.InputStream) <br /> The input stream to be filtered. <br /> | ||

## Public constructors

### InflaterInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InflaterInputStream(in: InputStream!)
```

Creates a new input stream with a default decompressor and buffer size.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the input stream |

### InflaterInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InflaterInputStream(
    in: InputStream!, 
    inf: Inflater!)
```

Creates a new input stream with the specified decompressor and a default buffer size.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the input stream |
| `inf` | [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater)!:the decompressor ("inflater") |

### InflaterInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InflaterInputStream(
    in: InputStream!, 
    inf: Inflater!, 
    size: Int)
```

Creates a new input stream with the specified decompressor and buffer size.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the input stream |
| `inf` | [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater)!:the decompressor ("inflater") |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input buffer size |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------|
| `java.lang.IllegalArgumentException` | if`size <= 0` |

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun available(): Int
```

Returns 0 after EOF has been reached, otherwise always return 1.

Programs should not count on this method to return the actual number of bytes that could be read without blocking.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 1 before EOF and 0 after EOF. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this input stream and releases any system resources associated with the stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error has occurred |

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mark(readlimit: Int): Unit
```

Marks the current position in this input stream.

The`mark`method of`InflaterInputStream`does nothing.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `readlimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum limit of bytes that can be read before the mark position becomes invalid. |

**See Also**

- [java.io.InputStream#reset()](https://developer.android.com/reference/kotlin/java/io/InputStream.html#reset()) 

### markSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun markSupported(): Boolean
```

Tests if this input stream supports the`mark`and`reset`methods. The`markSupported`method of`InflaterInputStream`returns`false`.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if this stream type supports the`mark`and`reset`methods. |

**See Also**

- [java.io.InputStream#mark(int)](https://developer.android.com/reference/kotlin/java/io/InputStream.html#mark(kotlin.Int))
- [java.io.InputStream#reset()](https://developer.android.com/reference/kotlin/java/io/InputStream.html#reset()) 

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

Reads a byte of uncompressed data. This method will block until enough input is available for decompression.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the byte read, or -1 if end of compressed input is reached |

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads uncompressed data into an array of bytes. If`len`is not zero, the method will block until some input can be decompressed; otherwise, no bytes are read and`0`is returned.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the destination array`b` |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes read |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of bytes read, or -1 if the end of the compressed input is reached or a preset dictionary is needed |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.NullPointerException` | If`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative,`len`is negative, or`len`is greater than`b.length - off` |
| --- | --- |
| `java.util.zip.ZipException` | if a ZIP format error has occurred |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Repositions this stream to the position at the time the`mark`method was last called on this input stream.

The method`reset`for class`InflaterInputStream`does nothing except throw an`IOException`.

| Exceptions ||
|-----------------------|----------------------------|
| `java.io.IOException` | if this method is invoked. |

**See Also**

- [java.io.InputStream#mark(int)](https://developer.android.com/reference/kotlin/java/io/InputStream.html#mark(kotlin.Int))
- [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) 

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

Skips specified number of bytes of uncompressed data.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to skip |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the actual number of bytes skipped. |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.IllegalArgumentException` | if`n < 0` |

## Protected methods

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun fill(): Unit
```

Fills input buffer with more data to decompress.

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

## Properties

### buf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var buf: ByteArray!
```

Input buffer for decompression. 

### closed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var closed: Boolean
```

**Deprecated:** *This field will be removed from a future version of Android and should not be used. Subclasses that access this field need to be modified to keep track of their own closed state by overriding close().*

Indicates whether the #close() method has been called, internal use only. 

### inf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var inf: Inflater!
```

Decompressor for this stream. 

### len

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var len: Int
```

Length of input buffer.
