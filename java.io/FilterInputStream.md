Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FilterInputStream

```
open class FilterInputStream : InputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.InputStream](../java/io/InputStream.md) ||
| | ↳ | [java.io.FilterInputStream](../java/io/FilterInputStream.md) |

| Known Direct Subclasses [Base64InputStream](../android/util/Base64InputStream.md), [BufferedInputStream](../java/io/BufferedInputStream.md), [CheckedInputStream](../java/util/zip/CheckedInputStream.md), [CipherInputStream](../javax/crypto/CipherInputStream.md), [DataInputStream](../java/io/DataInputStream.md), [DeflaterInputStream](../java/util/zip/DeflaterInputStream.md), [DigestInputStream](../java/security/DigestInputStream.md), [InflaterInputStream](../java/util/zip/InflaterInputStream.md), [LineNumberInputStream](../java/io/LineNumberInputStream.md), [PushbackInputStream](../java/io/PushbackInputStream.md) |---|---| | [Base64InputStream](../android/util/Base64InputStream.md) | An InputStream that does Base64 decoding on the data read through it. | | [BufferedInputStream](../java/io/BufferedInputStream.md) | A `BufferedInputStream` adds functionality to another input stream-namely, the ability to buffer the input and to support the `mark` and `reset` methods. | | [CheckedInputStream](../java/util/zip/CheckedInputStream.md) | An input stream that also maintains a checksum of the data being read. | | [CipherInputStream](../javax/crypto/CipherInputStream.md) | A CipherInputStream is composed of an InputStream and a Cipher so that read() methods return data that are read in from the underlying InputStream but have been additionally processed by the Cipher. | | [DataInputStream](../java/io/DataInputStream.md) | A data input stream lets an application read primitive Java data types from an underlying input stream in a machine-independent way. | | [DeflaterInputStream](../java/util/zip/DeflaterInputStream.md) | Implements an input stream filter for compressing data in the "deflate" compression format. | | [DigestInputStream](../java/security/DigestInputStream.md) | A transparent stream that updates the associated message digest using the bits going through the stream. | | [InflaterInputStream](../java/util/zip/InflaterInputStream.md) | This class implements a stream filter for uncompressing data in the "deflate" compression format. | | [LineNumberInputStream](../java/io/LineNumberInputStream.md) | This class is an input stream filter that provides the added functionality of keeping track of the current line number. | | [PushbackInputStream](../java/io/PushbackInputStream.md) | A `PushbackInputStream` adds functionality to another input stream, namely the ability to "push back" or "unread" bytes, by storing pushed-back bytes in an internal buffer. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [GZIPInputStream](../java/util/zip/GZIPInputStream.md), [JarInputStream](../java/util/jar/JarInputStream.md), [ZipInputStream](../java/util/zip/ZipInputStream.md) |---|---| | [GZIPInputStream](../java/util/zip/GZIPInputStream.md) | This class implements a stream filter for reading compressed data in the GZIP file format. | | [JarInputStream](../java/util/jar/JarInputStream.md) | The `JarInputStream` class is used to read the contents of a JAR file from any input stream. | | [ZipInputStream](../java/util/zip/ZipInputStream.md) | This class implements an input stream filter for reading files in the ZIP file format. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A `FilterInputStream` contains some other input stream, which it uses as its basic source of data, possibly transforming the data along the way or providing additional functionality. The class `FilterInputStream` itself simply overrides all methods of `InputStream` with versions that pass all requests to the contained input stream. Subclasses of `FilterInputStream` may further override some of these methods and may also provide additional methods and fields.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#FilterInputStream(java.io.InputStream)(in: https://developer.android.com/reference/kotlin/java/io/InputStream!)` Creates a `FilterInputStream` by assigning the argument `in` to the field `this.in` so as to remember it for later use. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#available()()` Returns an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking by the next caller of a method for this input stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#close()()` Closes this input stream and releases any system resources associated with the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#mark(kotlin.Int)(readlimit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Marks the current position in this input stream. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#markSupported()()` Tests if this input stream supports the `mark` and `reset` methods. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#read()()` Reads the next byte of data from this input stream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#read(kotlin.ByteArray)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Reads up to `b.length` bytes of data from this input stream into an array of bytes. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads up to `len` bytes of data from this input stream into an array of bytes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#reset()()` Repositions this stream to the position at the time the `mark` method was last called on this input stream. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#skip(kotlin.Long)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Skips over and discards `n` bytes of data from the input stream. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/InputStream` |---|---| | `https://developer.android.com/reference/kotlin/java/io/InputStream!` | `https://developer.android.com/reference/kotlin/java/io/InputStream#nullInputStream()()` Returns a new `InputStream` that reads no bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `available()`, `read()`, `read(byte[])`, `read(byte[], int, int)`, `readAllBytes()`, `readNBytes(byte[], int, int)`, `readNBytes(int)`, `skip(long)`, `skipNBytes(long)`, and `transferTo()` methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw `IOException`. The `markSupported()` method returns `false`. The `mark()` method does nothing, and the `reset()` method throws `IOException`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/io/InputStream#readAllBytes()()` Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#readNBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads the requested number of bytes from the input stream into the given byte array. This method blocks until `len` bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before `len` bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If `len` is zero, then no bytes are read and `0` is returned; otherwise, there is an attempt to read up to `len` bytes. The first byte read is stored into element `b[off]`, the next one in to `b[off+1]`, and so on. The number of bytes read is, at most, equal to `len`. Let *k* be the number of bytes actually read; these bytes will be stored in elements `b[off]` through `b[off+`*k* `-1]`, leaving elements `b[off+`*k* `]` through `b[off+len-1]` unaffected. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of `b` have been updated with data from the input stream. Consequently the input stream and `b` may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/io/InputStream#readNBytes(kotlin.Int)(len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If `len` is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to `len` bytes are read from the stream. Fewer than `len` bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by `len`. Therefore, the method may be safely called with very large values of `len` provided sufficient memory is available. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#skipNBytes(kotlin.Long)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Skips over and discards exactly `n` bytes of data from this input stream. If `n` is zero, then no bytes are skipped. If `n` is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an `EOFException` is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#transferTo(java.io.OutputStream)(out: https://developer.android.com/reference/kotlin/java/io/OutputStream!)` Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is *asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Properties ||
|---|---|
| [InputStream](../java/io/InputStream.md)! | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream` The input stream to be filtered. |

## Protected constructors

### FilterInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected FilterInputStream(in: InputStream!)
```

Creates a `FilterInputStream` by assigning the argument `in` to the field `this.in` so as to remember it for later use.

| Parameters ||
|---|---|
| `in` | [InputStream](../java/io/InputStream.md)!: the underlying input stream, or `null` if this instance is to be created without an underlying stream. |

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun available(): Int
```

Returns an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking by the next caller of a method for this input stream. The next caller might be the same thread or another thread. A single read or skip of this many bytes will not block, but may read or skip fewer bytes.

This method returns the result of `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream`.available().

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes this input stream and releases any system resources associated with the stream. This method simply performs `in.close()`.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream`

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mark(readlimit: Int): Unit
```

Marks the current position in this input stream. A subsequent call to the `reset` method repositions this stream at the last marked position so that subsequent reads re-read the same bytes.

The `readlimit` argument tells this input stream to allow that many bytes to be read before the mark position gets invalidated.

This method simply performs `in.mark(readlimit)`.

| Parameters ||
|---|---|
| `readlimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum limit of bytes that can be read before the mark position becomes invalid. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream`
- `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#reset()`

### markSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun markSupported(): Boolean
```

Tests if this input stream supports the `mark` and `reset` methods. This method simply performs `in.markSupported()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this stream type supports the `mark` and `reset` method; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream`
- `https://developer.android.com/reference/kotlin/java/io/InputStream#mark(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/io/InputStream#reset()`

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(): Int
```

Reads the next byte of data from this input stream. The value byte is returned as an `int` in the range `0` to `255`. If no byte is available because the end of the stream has been reached, the value `-1` is returned. This method blocks until input data is available, the end of the stream is detected, or an exception is thrown.

This method simply performs `in.read()` and returns the result.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the next byte of data, or `-1` if the end of the stream is reached. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream`

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(b: ByteArray!): Int
```

Reads up to `b.length` bytes of data from this input stream into an array of bytes. This method blocks until some input is available.

This method simply performs the call `read(b, 0, b.length)` and returns the result. It is important that it does *not* do `in.read(b)` instead; certain subclasses of `FilterInputStream` depend on the implementation strategy actually used.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer into which the data is read. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the total number of bytes read into the buffer, or `-1` if there is no more data because the end of the stream has been reached. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |
| `java.lang.NullPointerException` | if `b` is `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)`

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads up to `len` bytes of data from this input stream into an array of bytes. If `len` is not zero, the method blocks until some input is available; otherwise, no bytes are read and `0` is returned.

This method simply performs `in.read(b, off, len)` and returns the result.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset in the destination array `b` |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of bytes read. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the total number of bytes read into the buffer, or `-1` if there is no more data because the end of the stream has been reached. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |
| `java.lang.IndexOutOfBoundsException` | If `off` is negative, `len` is negative, or `len` is greater than `b.length - off` |
| `java.lang.NullPointerException` | If `b` is `null`. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream`

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reset(): Unit
```

Repositions this stream to the position at the time the `mark` method was last called on this input stream.

This method simply performs `in.reset()`.

Stream marks are intended to be used in situations where you need to read ahead a little to see what's in the stream. Often this is most easily done by invoking some general parser. If the stream is of the type handled by the parse, it just chugs along happily. If the stream is not of that type, the parser should toss an exception when it fails. If this happens within readlimit bytes, it allows the outer code to reset the stream and try another parser.

| Exceptions ||
|---|---|
| `java.io.IOException` | if the stream has not been marked or if the mark has been invalidated. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream`
- `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#mark(kotlin.Int)`

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun skip(n: Long): Long
```

Skips over and discards `n` bytes of data from the input stream. The `skip` method may, for a variety of reasons, end up skipping over some smaller number of bytes, possibly `0`. The actual number of bytes skipped is returned.

This method simply performs `in.skip(n)`.

| Parameters ||
|---|---|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of bytes to be skipped. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the actual number of bytes skipped. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if `in.skip(n)` throws an IOException. |

## Properties

### in

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var in: InputStream!
```

The input stream to be filtered.
