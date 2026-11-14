# BufferedInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BufferedInputStream

```
open class BufferedInputStream : FilterInputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream) |||
| | ↳ | [java.io.FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream) ||
| | | ↳ | [java.io.BufferedInputStream](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#) |
| --- | --- | --- | --- |

A `BufferedInputStream` adds functionality to another input stream-namely, the ability to buffer the input and to support the `mark` and `reset` methods. When the `BufferedInputStream` is created, an internal buffer array is created. As bytes from the stream are read or skipped, the internal buffer is refilled as necessary from the contained input stream, many bytes at a time. The `mark` operation remembers a point in the input stream and the `reset` operation causes all the bytes read since the most recent `mark` operation to be reread before new bytes are taken from the contained input stream.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BufferedInputStream](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#BufferedInputStream(java.io.InputStream))`(`in:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)!`)` Creates a `BufferedInputStream` and saves its argument, the input stream `in`, for later use. |
| [BufferedInputStream](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#BufferedInputStream(java.io.InputStream,%20kotlin.Int))`(`in:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `BufferedInputStream` with the specified buffer size, and saves its argument, the input stream `in`, for later use. |

| Public methods ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#available())`()` Returns an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking by the next invocation of a method for this input stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#close())`()` Closes this input stream and releases any system resources associated with the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#mark(kotlin.Int))`(`readlimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` See the general contract of the `mark` method of `InputStream`. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#markSupported())`()` Tests if this input stream supports the `mark` and `reset` methods. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#read())`()` See the general contract of the `read` method of `InputStream`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads bytes from this byte-input stream into the specified byte array, starting at the given offset. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#reset())`()` See the general contract of the `reset` method of `InputStream`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` See the general contract of the `skip` method of `InputStream`. |

| Inherited functions ||
|---|---|
| From class [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream) |------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)! | [nullInputStream](https://developer.android.com/reference/kotlin/java/io/InputStream#nullInputStream())`()` Returns a new `InputStream` that reads no bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `available()`, `read()`, `read(byte[])`, `read(byte[], int, int)`, `readAllBytes()`, `readNBytes(byte[], int, int)`, `readNBytes(int)`, `skip(long)`, `skipNBytes(long)`, and `transferTo()` methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw `IOException`. The `markSupported()` method returns `false`. The `mark()` method does nothing, and the `reset()` method throws `IOException`. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](https://developer.android.com/reference/kotlin/java/io/InputStream#readAllBytes())`()` Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream#readNBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads the requested number of bytes from the input stream into the given byte array. This method blocks until `len` bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before `len` bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If `len` is zero, then no bytes are read and `0` is returned; otherwise, there is an attempt to read up to `len` bytes. The first byte read is stored into element `b[off]`, the next one in to `b[off+1]`, and so on. The number of bytes read is, at most, equal to `len`. Let *k* be the number of bytes actually read; these bytes will be stored in elements `b[off]` through `b[off+`*k* `-1]`, leaving elements `b[off+`*k* `]` through `b[off+len-1]` unaffected. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of `b` have been updated with data from the input stream. Consequently the input stream and `b` may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream#readNBytes(kotlin.Int))`(`len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If `len` is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to `len` bytes are read from the stream. Fewer than `len` bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by `len`. Therefore, the method may be safely called with very large values of `len` provided sufficient memory is available. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream#skipNBytes(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips over and discards exactly `n` bytes of data from this input stream. If `n` is zero, then no bytes are skipped. If `n` is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an `EOFException` is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](https://developer.android.com/reference/kotlin/java/io/InputStream#transferTo(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!`)` Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is *asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||
| From class [FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#read(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Reads up to `b.length` bytes of data from this input stream into an array of bytes. This method blocks until some input is available. This method simply performs the call `read(b, 0, b.length)` and returns the result. It is important that it does *not* do `in.read(b)` instead; certain subclasses of `FilterInputStream` depend on the implementation strategy actually used. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [buf](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#buf:kotlin.ByteArray) The internal buffer array where the data is stored. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [count](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#count:kotlin.Int) The index one greater than the index of the last valid byte in the buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [marklimit](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#marklimit:kotlin.Int) The maximum read ahead allowed after a call to the `mark` method before subsequent calls to the `reset` method fail. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [markpos](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#markpos:kotlin.Int) The value of the `pos` field at the time the last `mark` method was called. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [pos](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#pos:kotlin.Int) The current position in the buffer. |

| Inherited properties ||
|---|---|
| From class [FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)! | [in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) The input stream to be filtered. <br /> | ||

## Public constructors

### BufferedInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BufferedInputStream(in: InputStream!)
```

Creates a `BufferedInputStream` and saves its argument, the input stream `in`, for later use. An internal buffer array is created and stored in `buf`.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)!: the underlying input stream. |

### BufferedInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BufferedInputStream(
    in: InputStream!, 
    size: Int)
```

Creates a `BufferedInputStream` with the specified buffer size, and saves its argument, the input stream `in`, for later use. An internal buffer array of length `size` is created and stored in `buf`.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)!: the underlying input stream. |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the buffer size. |

| Exceptions ||
|--------------------------------------|-----------------|
| `java.lang.IllegalArgumentException` | if `size <= 0`. |

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun available(): Int
```

Returns an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking by the next invocation of a method for this input stream. The next invocation might be the same thread or another thread. A single read or skip of this many bytes will not block, but may read or skip fewer bytes.

This method returns the sum of the number of bytes remaining to be read in the buffer (`count - pos`) and the result of calling the [in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream)`.available()`.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking. |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------|
| `java.io.IOException` | if this input stream has been closed by invoking its #close() method, or an I/O error occurs. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this input stream and releases any system resources associated with the stream. Once the stream has been closed, further read(), available(), reset(), or skip() invocations will throw an IOException. Closing a previously closed stream has no effect.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mark(readlimit: Int): Unit
```

See the general contract of the `mark` method of `InputStream`.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `readlimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum limit of bytes that can be read before the mark position becomes invalid. |

**See Also**

### markSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun markSupported(): Boolean
```

Tests if this input stream supports the `mark` and `reset` methods. The `markSupported` method of `BufferedInputStream` returns `true`.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a `boolean` indicating if this stream type supports the `mark` and `reset` methods. |

**See Also**

- [java.io.InputStream#mark(int)](https://developer.android.com/reference/kotlin/java/io/InputStream#mark(kotlin.Int))
- [java.io.InputStream#reset()](https://developer.android.com/reference/kotlin/java/io/InputStream#reset()) 

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

See the general contract of the `read` method of `InputStream`.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next byte of data, or `-1` if the end of the stream is reached. |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------|
| `java.io.IOException` | if this input stream has been closed by invoking its #close() method, or an I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) 

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads bytes from this byte-input stream into the specified byte array, starting at the given offset.

This method implements the general contract of the corresponding [read](https://developer.android.com/reference/kotlin/java/io/InputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)) method of the [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream) class. As an additional convenience, it attempts to read as many bytes as possible by repeatedly invoking the `read` method of the underlying stream. This iterated `read` continues until one of the following conditions becomes true:

- The specified number of bytes have been read,
- The `read` method of the underlying stream returns `-1`, indicating end-of-file, or
- The `available` method of the underlying stream returns zero, indicating that further input requests would block.

If the first `read` on the underlying stream returns `-1` to indicate end-of-file then this method returns `-1`. Otherwise this method returns the number of bytes actually read.

Subclasses of this class are encouraged, but not required, to attempt to read as many bytes as possible in the same fashion.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: destination buffer. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): offset at which to start storing bytes. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): maximum number of bytes to read. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes read, or `-1` if the end of the stream has been reached. |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.io.IOException` | if this input stream has been closed by invoking its #close() method, or an I/O error occurs. |
| `java.lang.NullPointerException` | If `b` is `null`. |
| `java.lang.IndexOutOfBoundsException` | If `off` is negative, `len` is negative, or `len` is greater than `b.length - off` |
| --- | --- |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

See the general contract of the `reset` method of `InputStream`.

If `markpos` is `-1` (no mark has been set or the mark has been invalidated), an `IOException` is thrown. Otherwise, `pos` is set equal to `markpos`.

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if this stream has not been marked or, if the mark has been invalidated, or the stream has been closed by invoking its #close() method, or an I/O error occurs. |

**See Also**

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

See the general contract of the `skip` method of `InputStream`.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of bytes to be skipped. |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the actual number of bytes skipped. |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if this input stream has been closed by invoking its #close() method, `in.skip(n)` throws an IOException, or an I/O error occurs. |

## Properties

### buf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var buf: ByteArray!
```

The internal buffer array where the data is stored. When necessary, it may be replaced by another array of a different size. 

### count

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var count: Int
```

The index one greater than the index of the last valid byte in the buffer. This value is always in the range `0` through `buf.length`; elements `buf[0]` through `buf[count-1]` contain buffered input data obtained from the underlying input stream. 

### marklimit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var marklimit: Int
```

The maximum read ahead allowed after a call to the `mark` method before subsequent calls to the `reset` method fail. Whenever the difference between `pos` and `markpos` exceeds `marklimit`, then the mark may be dropped by setting `markpos` to `-1`. 
**See Also**

### markpos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var markpos: Int
```

The value of the `pos` field at the time the last `mark` method was called.

This value is always in the range `-1` through `pos`. If there is no marked position in the input stream, this field is `-1`. If there is a marked position in the input stream, then `buf[markpos]` is the first byte to be supplied as input after a `reset` operation. If `markpos` is not `-1`, then all bytes from positions `buf[markpos]` through `buf[pos-1]` must remain in the buffer array (though they may be moved to another place in the buffer array, with suitable adjustments to the values of `count`, `pos`, and `markpos`); they may not be discarded unless and until the difference between `pos` and `markpos` exceeds `marklimit`. 
**See Also**

- [java.io.BufferedInputStream#pos](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#pos:kotlin.Int) 

### pos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var pos: Int
```

The current position in the buffer. This is the index of the next character to be read from the `buf` array.

This value is always in the range `0` through `count`. If it is less than `count`, then `buf[pos]` is the next byte to be supplied as input; if it is equal to `count`, then the next `read` or `skip` operation will require more bytes to be read from the contained input stream. 
**See Also**

- [java.io.BufferedInputStream#buf](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream#buf:kotlin.ByteArray)
