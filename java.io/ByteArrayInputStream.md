# ByteArrayInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ByteArrayInputStream

```
open class ByteArrayInputStream : InputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.InputStream](InputStream.md) ||
| | ↳ | [java.io.ByteArrayInputStream](ByteArrayInputStream.md) |

A`ByteArrayInputStream`contains an internal buffer that contains bytes that may be read from the stream. An internal counter keeps track of the next byte to be supplied by the`read`method.

Closing a`ByteArrayInputStream`has no effect. The methods in this class can be called after the stream has been closed without generating an`IOException`.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ByteArrayInputStream](ByteArrayInputStream.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates a`ByteArrayInputStream`so that it uses`buf`as its buffer array. |
| [ByteArrayInputStream](ByteArrayInputStream.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates`ByteArrayInputStream`that uses`buf`as its buffer array. |

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](ByteArrayInputStream.md))`()` Returns the number of remaining bytes that can be read (or skipped over) from this input stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](ByteArrayInputStream.md))`()` Closing a`ByteArrayInputStream`has no effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](ByteArrayInputStream.md))`(`readAheadLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the current marked position in the stream. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](ByteArrayInputStream.md))`()` Tests if this`InputStream`supports mark/reset. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](ByteArrayInputStream.md))`()` Reads the next byte of data from this input stream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](ByteArrayInputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to`len`bytes of data into an array of bytes from this input stream. |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](ByteArrayInputStream.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readNBytes](ByteArrayInputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](ByteArrayInputStream.md))`()` Resets the buffer to the marked position. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](ByteArrayInputStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips`n`bytes of input from this input stream. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](ByteArrayInputStream.md))`(`out:` ` [OutputStream](OutputStream.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [InputStream](InputStream.md) |------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](InputStream.md)! | [nullInputStream](InputStream.md))`()` <br /> Returns a new`InputStream`that reads no bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`available()`,`read()`,`read(byte[])`,`read(byte[], int, int)`,`readAllBytes()`,`readNBytes(byte[], int, int)`,`readNBytes(int)`,`skip(long)`,`skipNBytes(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`method does nothing, and the`reset()`method throws`IOException`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](InputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Reads some number of bytes from the input stream and stores them into the buffer array`b`. The number of bytes actually read is returned as an integer. This method blocks until input data is available, end of file is detected, or an exception is thrown. If the length of`b`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read at least one byte. If no byte is available because the stream is at the end of the file, the value`-1`is returned; otherwise, at least one byte is read and stored into`b`. The first byte read is stored into element`b[0]`, the next one into`b[1]`, and so on. The number of bytes read is, at most, equal to the length of`b`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[0]`through`b[`*k* `-1]`, leaving elements`b[`*k* `]`through`b[b.length-1]`unaffected. The`read(b)`method for class`InputStream`has the same effect as: ```kotlin <code>read(b, 0, b.length) </code> ``` <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readNBytes](InputStream.md))`(`len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If`len`is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to`len`bytes are read from the stream. Fewer than`len`bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by`len`. Therefore, the method may be safely called with very large values of`len`provided sufficient memory is available. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipNBytes](InputStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips over and discards exactly`n`bytes of data from this input stream. If`n`is zero, then no bytes are skipped. If`n`is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an`EOFException`is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [buf](ByteArrayInputStream.md) An array of bytes that was provided by the creator of the stream. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [count](ByteArrayInputStream.md) The index one greater than the last valid character in the input stream buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mark](ByteArrayInputStream.md) The currently marked position in the stream. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [pos](ByteArrayInputStream.md) The index of the next character to read from the input stream buffer. |

## Public constructors

### ByteArrayInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ByteArrayInputStream(buf: ByteArray!)
```

Creates a`ByteArrayInputStream`so that it uses`buf`as its buffer array. The buffer array is not copied. The initial value of`pos`is`0`and the initial value of`count`is the length of`buf`.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the input buffer. |

### ByteArrayInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ByteArrayInputStream(
    buf: ByteArray!, 
    offset: Int, 
    length: Int)
```

Creates`ByteArrayInputStream`that uses`buf`as its buffer array. The initial value of`pos`is`offset`and the initial value of`count`is the minimum of`offset+length`and`buf.length`. The buffer array is not copied. The buffer's mark is set to the specified offset.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the input buffer. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in the buffer of the first byte to read. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes to read from the buffer. |
| --- | --- |

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun available(): Int
```

Returns the number of remaining bytes that can be read (or skipped over) from this input stream.

The value returned is`count - pos`, which is the number of bytes remaining to be read from the input buffer.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of remaining bytes that can be read (or skipped over) from this input stream without blocking. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closing a`ByteArrayInputStream`has no effect. The methods in this class can be called after the stream has been closed without generating an`IOException`.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mark(readAheadLimit: Int): Unit
```

Set the current marked position in the stream. ByteArrayInputStream objects are marked at position zero by default when constructed. They may be marked at another position within the buffer by this method.

If no mark has been set, then the value of the mark is the offset passed to the constructor (or 0 if the offset was not supplied).

Note: The`readAheadLimit`for this class has no meaning.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------|
| `readlimit` | the maximum limit of bytes that can be read before the mark position becomes invalid. |

### markSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun markSupported(): Boolean
```

Tests if this`InputStream`supports mark/reset. The`markSupported`method of`ByteArrayInputStream`always returns`true`.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this stream instance supports the mark and reset methods;`false`otherwise. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

Reads the next byte of data from this input stream. The value byte is returned as an`int`in the range`0`to`255`. If no byte is available because the end of the stream has been reached, the value`-1`is returned.

This`read`method cannot block.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next byte of data, or`-1`if the end of the stream has been reached. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads up to`len`bytes of data into an array of bytes from this input stream. If`pos`equals`count`, then`-1`is returned to indicate end of file. Otherwise, the number`k`of bytes read is equal to the smaller of`len`and`count-pos`. If`k`is positive, then bytes`buf[pos]`through`buf[pos+k-1]`are copied into`b[off]`through`b[off+k-1]`in the manner performed by`System.arraycopy`. The value`k`is added into`pos`and`k`is returned.

This`read`method cannot block.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the destination array`b` |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes read. |
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

### readAllBytes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readAllBytes(): ByteArray!
```

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

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets the buffer to the marked position. The marked position is 0 unless another position was marked or an offset was specified in the constructor.

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------|
| `java.io.IOException` | if this stream has not been marked or if the mark has been invalidated. |

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

Skips`n`bytes of input from this input stream. Fewer bytes might be skipped if the end of the input stream is reached. The actual number`k`of bytes to be skipped is equal to the smaller of`n`and`count-pos`. The value`k`is added into`pos`and`k`is returned.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to be skipped. |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the actual number of bytes skipped. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### transferTo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun transferTo(out: OutputStream!): Long
```

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](OutputStream.md)!:the output stream, non-null |

| Return ||
|------------------------------------------------------------------------------|---------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of bytes transferred |

| Exceptions ||
|----------------------------------|------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when reading or writing |
| `java.lang.NullPointerException` | if`out`is`null` |

## Properties

### buf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var buf: ByteArray!
```

An array of bytes that was provided by the creator of the stream. Elements`buf[0]`through`buf[count-1]`are the only bytes that can ever be read from the stream; element`buf[pos]`is the next byte to be read. 

### count

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var count: Int
```

The index one greater than the last valid character in the input stream buffer. This value should always be nonnegative and not larger than the length of`buf`. It is one greater than the position of the last byte within`buf`that can ever be read from the input stream buffer. 

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mark: Int
```

The currently marked position in the stream. ByteArrayInputStream objects are marked at position zero by default when constructed. They may be marked at another position within the buffer by the`mark()`method. The current buffer position is set to this point by the`reset()`method.

If no mark has been set, then the value of mark is the offset passed to the constructor (or 0 if the offset was not supplied). 

### pos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var pos: Int
```

The index of the next character to read from the input stream buffer. This value should always be nonnegative and not larger than the value of`count`. The next byte to be read from the input stream buffer will be`buf[pos]`.
