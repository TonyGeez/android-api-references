Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PushbackInputStream

```
open class PushbackInputStream : FilterInputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream) |||
| | ↳ | [java.io.FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream) ||
| | | ↳ | [java.io.PushbackInputStream](https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#) |

A `PushbackInputStream` adds functionality to another input stream, namely the ability to "push back" or "unread" bytes, by storing pushed-back bytes in an internal buffer. This is useful in situations where it is convenient for a fragment of code to read an indefinite number of data bytes that are delimited by a particular byte value; after reading the terminating byte, the code fragment can "unread" it, so that the next read operation on the input stream will reread the byte that was pushed back. For example, bytes representing the characters constituting an identifier might be terminated by a byte representing an operator character; a method whose job is to read just an identifier can read until it sees the operator and then push the operator back to be re-read.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#PushbackInputStream(java.io.InputStream)(in: https://developer.android.com/reference/kotlin/java/io/InputStream!)` Creates a `PushbackInputStream` with a 1-byte pushback buffer, and saves its argument, the input stream `in`, for later use. |
| `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#PushbackInputStream(java.io.InputStream,%20kotlin.Int)(in: https://developer.android.com/reference/kotlin/java/io/InputStream!, size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `PushbackInputStream` with a pushback buffer of the specified `size`, and saves its argument, the input stream `in`, for later use. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#available()()` Returns an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking by the next invocation of a method for this input stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#close()()` Closes this input stream and releases any system resources associated with the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#mark(kotlin.Int)(readlimit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Marks the current position in this input stream. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#markSupported()()` Tests if this input stream supports the `mark` and `reset` methods, which it does not. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#read()()` Reads the next byte of data from this input stream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads up to `len` bytes of data from this input stream into an array of bytes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#reset()()` Repositions this stream to the position at the time the `mark` method was last called on this input stream. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#skip(kotlin.Long)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Skips over and discards `n` bytes of data from this input stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#unread(kotlin.ByteArray)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Pushes back an array of bytes by copying it to the front of the pushback buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#unread(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Pushes back a portion of an array of bytes by copying it to the front of the pushback buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#unread(kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Pushes back a byte by copying it to the front of the pushback buffer. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/InputStream` |---|---| | `https://developer.android.com/reference/kotlin/java/io/InputStream!` | `https://developer.android.com/reference/kotlin/java/io/InputStream#nullInputStream()()` Returns a new `InputStream` that reads no bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `available()`, `read()`, `read(byte[])`, `read(byte[], int, int)`, `readAllBytes()`, `readNBytes(byte[], int, int)`, `readNBytes(int)`, `skip(long)`, `skipNBytes(long)`, and `transferTo()` methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw `IOException`. The `markSupported()` method returns `false`. The `mark()` method does nothing, and the `reset()` method throws `IOException`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/io/InputStream#readAllBytes()()` Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#readNBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads the requested number of bytes from the input stream into the given byte array. This method blocks until `len` bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before `len` bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If `len` is zero, then no bytes are read and `0` is returned; otherwise, there is an attempt to read up to `len` bytes. The first byte read is stored into element `b[off]`, the next one in to `b[off+1]`, and so on. The number of bytes read is, at most, equal to `len`. Let *k* be the number of bytes actually read; these bytes will be stored in elements `b[off]` through `b[off+`*k* `-1]`, leaving elements `b[off+`*k* `]` through `b[off+len-1]` unaffected. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of `b` have been updated with data from the input stream. Consequently the input stream and `b` may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/io/InputStream#readNBytes(kotlin.Int)(len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If `len` is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to `len` bytes are read from the stream. Fewer than `len` bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by `len`. Therefore, the method may be safely called with very large values of `len` provided sufficient memory is available. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#skipNBytes(kotlin.Long)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Skips over and discards exactly `n` bytes of data from this input stream. If `n` is zero, then no bytes are skipped. If `n` is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an `EOFException` is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#transferTo(java.io.OutputStream)(out: https://developer.android.com/reference/kotlin/java/io/OutputStream!)` Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is *asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/io/FilterInputStream` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#read(kotlin.ByteArray)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Reads up to `b.length` bytes of data from this input stream into an array of bytes. This method blocks until some input is available. This method simply performs the call `read(b, 0, b.length)` and returns the result. It is important that it does *not* do `in.read(b)` instead; certain subclasses of `FilterInputStream` depend on the implementation strategy actually used. <br /> | ||

| Properties ||
|---|---|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#buf:kotlin.ByteArray` The pushback buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/PushbackInputStream#pos:kotlin.Int` The position within the pushback buffer from which the next byte will be read. |

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/FilterInputStream` |---|---| | `https://developer.android.com/reference/kotlin/java/io/InputStream!` | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream` The input stream to be filtered. <br /> | ||

## Public constructors

### PushbackInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PushbackInputStream(in: InputStream!)
```

Creates a `PushbackInputStream` with a 1-byte pushback buffer, and saves its argument, the input stream `in`, for later use. Initially, the pushback buffer is empty.

| Parameters ||
|---|---|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)!: the input stream from which bytes will be read. |

### PushbackInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PushbackInputStream(
    in: InputStream!, 
    size: Int)
```

Creates a `PushbackInputStream` with a pushback buffer of the specified `size`, and saves its argument, the input stream `in`, for later use. Initially, the pushback buffer is empty.

| Parameters ||
|---|---|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)!: the input stream from which bytes will be read. |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the size of the pushback buffer. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `size <= 0` |

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun available(): Int
```

Returns an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking by the next invocation of a method for this input stream. The next invocation might be the same thread or another thread. A single read or skip of this many bytes will not block, but may read or skip fewer bytes.

The method returns the sum of the number of bytes that have been pushed back and the value returned by `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#available()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of bytes that can be read (or skipped over) from the input stream without blocking. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if this input stream has been closed by invoking its #close() method, or an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream`
- `https://developer.android.com/reference/kotlin/java/io/InputStream#available()`

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes this input stream and releases any system resources associated with the stream. Once the stream has been closed, further read(), unread(), available(), reset(), or skip() invocations will throw an IOException. Closing a previously closed stream has no effect.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mark(readlimit: Int): Unit
```

Marks the current position in this input stream.

The `mark` method of `PushbackInputStream` does nothing.

| Parameters ||
|---|---|
| `readlimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum limit of bytes that can be read before the mark position becomes invalid. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/InputStream#reset()`

### markSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun markSupported(): Boolean
```

Tests if this input stream supports the `mark` and `reset` methods, which it does not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `false`, since this class does not support the `mark` and `reset` methods. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/InputStream#mark(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/io/InputStream#reset()`

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(): Int
```

Reads the next byte of data from this input stream. The value byte is returned as an `int` in the range `0` to `255`. If no byte is available because the end of the stream has been reached, the value `-1` is returned. This method blocks until input data is available, the end of the stream is detected, or an exception is thrown.

This method returns the most recently pushed-back byte, if there is one, and otherwise calls the `read` method of its underlying input stream and returns whatever value that method returns.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the next byte of data, or `-1` if the end of the stream has been reached. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if this input stream has been closed by invoking its #close() method, or an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/InputStream#read()`

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads up to `len` bytes of data from this input stream into an array of bytes. This method first reads any pushed-back bytes; after that, if fewer than `len` bytes have been read then it reads from the underlying input stream. If `len` is not zero, the method blocks until at least 1 byte of input is available; otherwise, no bytes are read and `0` is returned.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset in the destination array `b` |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of bytes read. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the total number of bytes read into the buffer, or `-1` if there is no more data because the end of the stream has been reached. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if this input stream has been closed by invoking its #close() method, or an I/O error occurs. |
| `java.lang.IndexOutOfBoundsException` | If `off` is negative, `len` is negative, or `len` is greater than `b.length - off` |
| `java.lang.NullPointerException` | If `b` is `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/InputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)`

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reset(): Unit
```

Repositions this stream to the position at the time the `mark` method was last called on this input stream.

The method `reset` for class `PushbackInputStream` does nothing except throw an `IOException`.

| Exceptions ||
|---|---|
| `java.io.IOException` | if this method is invoked. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/InputStream#mark(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/io/IOException`

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun skip(n: Long): Long
```

Skips over and discards `n` bytes of data from this input stream. The `skip` method may, for a variety of reasons, end up skipping over some smaller number of bytes, possibly zero. If `n` is negative, no bytes are skipped.

The `skip` method of `PushbackInputStream` first skips over the bytes in the pushback buffer, if any. It then calls the `skip` method of the underlying input stream if more bytes need to be skipped. The actual number of bytes skipped is returned.

| Parameters ||
|---|---|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of bytes to be skipped. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the actual number of bytes skipped. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the stream has been closed by invoking its #close() method, `in.skip(n)` throws an IOException, or an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream`
- `https://developer.android.com/reference/kotlin/java/io/InputStream#skip(kotlin.Long)`

### unread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unread(b: ByteArray!): Unit
```

Pushes back an array of bytes by copying it to the front of the pushback buffer. After this method returns, the next byte to be read will have the value `b[0]`, the byte after that will have the value `b[1]`, and so forth.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the byte array to push back |

| Exceptions ||
|---|---|
| `java.io.IOException` | If there is not enough room in the pushback buffer for the specified number of bytes, or this input stream has been closed by invoking its #close() method. |

### unread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unread(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Pushes back a portion of an array of bytes by copying it to the front of the pushback buffer. After this method returns, the next byte to be read will have the value `b[off]`, the byte after that will have the value `b[off+1]`, and so forth.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the byte array to push back. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset of the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes to push back. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If there is not enough room in the pushback buffer for the specified number of bytes, or this input stream has been closed by invoking its #close() method. |

### unread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unread(b: Int): Unit
```

Pushes back a byte by copying it to the front of the pushback buffer. After this method returns, the next byte to be read will have the value `(byte)b`.

| Parameters ||
|---|---|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the `int` value whose low-order byte is to be pushed back. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If there is not enough room in the pushback buffer for the byte, or this input stream has been closed by invoking its #close() method. |

## Properties

### buf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var buf: ByteArray!
```

The pushback buffer.

### pos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var pos: Int
```

The position within the pushback buffer from which the next byte will be read. When the buffer is empty, `pos` is equal to `buf.length`; when the buffer is full, `pos` is equal to zero.
