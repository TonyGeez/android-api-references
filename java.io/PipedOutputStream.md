Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PipedOutputStream

```
open class PipedOutputStream : OutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.OutputStream](OutputStream.md) ||
| | ↳ | [java.io.PipedOutputStream](PipedOutputStream.md) |

A piped output stream can be connected to a piped input stream to create a communications pipe. The piped output stream is the sending end of the pipe. Typically, data is written to a `PipedOutputStream` object by one thread and data is read from the connected `PipedInputStream` by some other thread. Attempting to use both objects from a single thread is not recommended as it may deadlock the thread. The pipe is said to be *broken* if a thread that was reading data bytes from the connected piped input stream is no longer alive.

## Summary

| Public constructors ||
|---|---|
| PipedOutputStream Creates a piped output stream that is not yet connected to a piped input stream. |
| PipedOutputStream Creates a piped output stream connected to the specified piped input stream. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | close Closes this piped output stream and releases any system resources associated with this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | connect Connects this piped output stream to a receiver. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | flush Flushes this output stream and forces any buffered output bytes to be written out. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | write Writes `len` bytes from the specified byte array starting at offset `off` to this piped output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | write Writes the specified `byte` to the piped output stream. |

| Inherited functions ||
|---|---|
| From class OutputStream |---|---| | `https://developer.android.com/reference/kotlin/java/io/OutputStream!` | nullOutputStream Returns a new `OutputStream` which discards all bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `write(int)`, `write(byte[])`, and `write(byte[], int, int)` methods do nothing. After the stream has been closed, these methods all throw `IOException`. The `flush()` method does nothing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | write Writes `b.length` bytes from the specified byte array to this output stream. The general contract for `write(b)` is that it should have exactly the same effect as the call `write(b, 0, b.length)`. <br /> | ||

## Public constructors

### PipedOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PipedOutputStream()
```

Creates a piped output stream that is not yet connected to a piped input stream. It must be connected to a piped input stream, either by the receiver or the sender, before being used.
**See Also**

- connect
- connect

### PipedOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PipedOutputStream(snk: PipedInputStream!)
```

Creates a piped output stream connected to the specified piped input stream. Data bytes written to this stream will then be available as input from `snk`.

| Parameters ||
|---|---|
| `snk` | [PipedInputStream](PipedInputStream.md)!: The piped input stream to connect to. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes this piped output stream and releases any system resources associated with this stream. This stream may no longer be used for writing bytes.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun connect(snk: PipedInputStream!): Unit
```

Connects this piped output stream to a receiver. If this object is already connected to some other piped input stream, an `IOException` is thrown.

If `snk` is an unconnected piped input stream and `src` is an unconnected piped output stream, they may be connected by either the call:

```kotlin
src.connect(snk)
```
or the call:

```kotlin
snk.connect(src)
```
The two calls have the same effect.

| Parameters ||
|---|---|
| `snk` | [PipedInputStream](PipedInputStream.md)!: the piped input stream to connect to. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun flush(): Unit
```

Flushes this output stream and forces any buffered output bytes to be written out. This will notify any readers that bytes are waiting in the pipe.

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes `len` bytes from the specified byte array starting at offset `off` to this piped output stream. This method blocks until all the bytes are written to the output stream.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the data. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset in the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes to write. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the pipe is [broken](PipedOutputStream.md), connect, closed, or if an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(b: Int): Unit
```

Writes the specified `byte` to the piped output stream.

Implements the `write` method of `OutputStream`.

| Parameters ||
|---|---|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the `byte` to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the pipe is [broken](PipedOutputStream.md), connect, closed, or if an I/O error occurs. |
