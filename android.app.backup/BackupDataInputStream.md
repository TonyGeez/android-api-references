Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BackupDataInputStream

Kotlin | [Java](BackupDataInputStream.md)
| --- | --- |

```
open class BackupDataInputStream : InputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.InputStream](../java.io/InputStream.md) ||
| | ↳ | [android.app.backup.BackupDataInputStream](BackupDataInputStream.md) |

Provides an `https://developer.android.com/reference/kotlin/java/io/InputStream.html#`-like interface for accessing an entity's data during a restore operation. Used by `https://developer.android.com/reference/kotlin/android/app/backup/BackupHelper` classes within the `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper` mechanism.

When `https://developer.android.com/reference/kotlin/android/app/backup/BackupHelper#restoreEntity(android.app.backup.BackupDataInputStream)` is called, the current entity's header has already been read from the underlying `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput`. The entity's key string and total data size are available through this class's `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream#getKey()` and `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream#size()` methods, respectively.

**Note:** The caller should take care not to seek or close the underlying data source, nor read more than `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream#size()` bytes from the stream.

## Summary

| Public methods ||
|---|---|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream#getKey()()` Report the key string associated with this entity within the backup data set. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream#read()()` Read one byte of entity data from the stream, returning it as an integer value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream#read(kotlin.ByteArray)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Read enough entity data into a byte array to fill the array. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Read up to `size` bytes of data into a byte array, beginning at position `offset` within the array. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream#size()()` Report the total number of bytes of data available for the current entity. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/InputStream.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#available()()` Returns an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking, which may be 0, or 0 when end of stream is detected. The read might be on the same thread or another thread. A single read or skip of this many bytes will not block, but may read or skip fewer bytes. Note that while some implementations of `InputStream` will return the total number of bytes in the stream, many will not. It is never correct to use the return value of this method to allocate a buffer intended to hold all data in this stream. A subclass's implementation of this method may choose to throw an `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if this input stream has been closed by invoking the #close() method. The `available` method of `InputStream` always returns `0`. This method should be overridden by subclasses. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#close()()` Closes this input stream and releases any system resources associated with the stream. The `close` method of `InputStream` does nothing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#mark(kotlin.Int)(readlimit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Marks the current position in this input stream. A subsequent call to the `reset` method repositions this stream at the last marked position so that subsequent reads re-read the same bytes. The `readlimit` arguments tells this input stream to allow that many bytes to be read before the mark position gets invalidated. The general contract of `mark` is that, if the method `markSupported` returns `true`, the stream somehow remembers all the bytes read after the call to `mark` and stands ready to supply those same bytes again if and whenever the method `reset` is called. However, the stream is not required to remember any data at all if more than `readlimit` bytes are read from the stream before `reset` is called. Marking a closed stream should not have any effect on the stream. The `mark` method of `InputStream` does nothing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#markSupported()()` Tests if this input stream supports the `mark` and `reset` methods. Whether or not `mark` and `reset` are supported is an invariant property of a particular input stream instance. The `markSupported` method of `InputStream` returns `false`. <br /> | | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#nullInputStream()()` Returns a new `InputStream` that reads no bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `available()`, `read()`, `read(byte[])`, `read(byte[], int, int)`, `readAllBytes()`, `readNBytes(byte[], int, int)`, `readNBytes(int)`, `skip(long)`, `skipNBytes(long)`, and `transferTo()` methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw `IOException`. The `markSupported()` method returns `false`. The `mark()` method does nothing, and the `reset()` method throws `IOException`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#readAllBytes()()` Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#readNBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads the requested number of bytes from the input stream into the given byte array. This method blocks until `len` bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before `len` bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If `len` is zero, then no bytes are read and `0` is returned; otherwise, there is an attempt to read up to `len` bytes. The first byte read is stored into element `b[off]`, the next one in to `b[off+1]`, and so on. The number of bytes read is, at most, equal to `len`. Let *k* be the number of bytes actually read; these bytes will be stored in elements `b[off]` through `b[off+`*k* `-1]`, leaving elements `b[off+`*k* `]` through `b[off+len-1]` unaffected. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of `b` have been updated with data from the input stream. Consequently the input stream and `b` may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#readNBytes(kotlin.Int)(len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If `len` is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to `len` bytes are read from the stream. Fewer than `len` bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by `len`. Therefore, the method may be safely called with very large values of `len` provided sufficient memory is available. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#reset()()` Repositions this stream to the position at the time the `mark` method was last called on this input stream. The general contract of `reset` is: - If the method `markSupported` returns `true`, then: - If the method `mark` has not been called since the stream was created, or the number of bytes read from the stream since `mark` was last called is larger than the argument to `mark` at that last call, then an `IOException` might be thrown. - If such an `IOException` is not thrown, then the stream is reset to a state such that all the bytes read since the most recent call to `mark` (or since the start of the file, if `mark` has not been called) will be resupplied to subsequent callers of the `read` method, followed by any bytes that otherwise would have been the next input data as of the time of the call to `reset`. - If the method `markSupported` returns `false`, then: - The call to `reset` may throw an `IOException`. - If an `IOException` is not thrown, then the stream is reset to a fixed state that depends on the particular type of the input stream and how it was created. The bytes that will be supplied to subsequent callers of the `read` method depend on the particular type of the input stream. The method `reset` for class `InputStream` does nothing except throw an `IOException`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#skip(kotlin.Long)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Skips over and discards `n` bytes of data from this input stream. The `skip` method may, for a variety of reasons, end up skipping over some smaller number of bytes, possibly `0`. This may result from any of a number of conditions; reaching end of file before `n` bytes have been skipped is only one possibility. The actual number of bytes skipped is returned. If `n` is negative, the `skip` method for class `InputStream` always returns 0, and no bytes are skipped. Subclasses may handle the negative value differently. The `skip` method implementation of this class creates a byte array and then repeatedly reads into it until `n` bytes have been read or the end of the stream has been reached. Subclasses are encouraged to provide a more efficient implementation of this method. For instance, the implementation may depend on the ability to seek. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#skipNBytes(kotlin.Long)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Skips over and discards exactly `n` bytes of data from this input stream. If `n` is zero, then no bytes are skipped. If `n` is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an `EOFException` is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#transferTo(java.io.OutputStream)(out: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!)` Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is *asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

## Public methods

### getKey

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getKey(): String!
```

Report the key string associated with this entity within the backup data set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The key string for this entity, equivalent to calling `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput#getKey()` on the underlying `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput`. |

### read

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(): Int
```

Read one byte of entity data from the stream, returning it as an integer value. If more than `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream#size()` bytes of data are read from the stream, the output of this method is undefined.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The byte read, or undefined if the end of the stream has been reached. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### read

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(b: ByteArray!): Int
```

Read enough entity data into a byte array to fill the array.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: Byte array to fill with data from the stream. If the stream does not have sufficient data to fill the array, then the contents of the remainder of the array will be undefined. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of bytes of data read, or zero if all of the entity's data has already been read. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If the first byte cannot be read for any reason other than the end of the file, if the input stream has been closed, or if some other I/O error occurs. |
| `java.lang.NullPointerException` | if `b` is `null`. |

### read

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(
    b: ByteArray!, 
    offset: Int, 
    size: Int
): Int
```

Read up to `size` bytes of data into a byte array, beginning at position `offset` within the array.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: Byte array into which the data will be read |
| `off` | the start offset in array `b` at which the data is written. |
| `len` | the maximum number of bytes to read. |
| --- | --- |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The data will be stored in `b` beginning at this index within the array. |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes to read in this operation. If insufficient data exists within the entity to fulfill this request, only as much data will be read as is available. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of bytes of data read, or zero if all of the entity's data has already been read. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If the first byte cannot be read for any reason other than end of file, or if the input stream has been closed, or if some other I/O error occurs. |
| `java.lang.IndexOutOfBoundsException` | If `off` is negative, `len` is negative, or `len` is greater than `b.length - off` |
| `java.lang.NullPointerException` | If `b` is `null`. |
| --- | --- |

### size

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun size(): Int
```

Report the total number of bytes of data available for the current entity.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of data bytes available, equivalent to calling `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput#getDataSize()` on the underlying `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput`. |
