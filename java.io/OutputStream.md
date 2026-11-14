# OutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OutputStream

```
abstract class OutputStream : Closeable, Flushable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.io.OutputStream](../java/io/OutputStream.md) |

| Known Direct Subclasses [ByteArrayOutputStream](../java/io/ByteArrayOutputStream.md), [FileOutputStream](../java/io/FileOutputStream.md), [FilterOutputStream](../java/io/FilterOutputStream.md), [ObjectOutputStream](../java/io/ObjectOutputStream.md), [PipedOutputStream](../java/io/PipedOutputStream.md) |-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------| | [ByteArrayOutputStream](../java/io/ByteArrayOutputStream.md) | This class implements an output stream in which the data is written into a byte array. | | [FileOutputStream](../java/io/FileOutputStream.md) | A file output stream is an output stream for writing data to a`File`or to a`FileDescriptor`. | | [FilterOutputStream](../java/io/FilterOutputStream.md) | This class is the superclass of all classes that filter output streams. | | [ObjectOutputStream](../java/io/ObjectOutputStream.md) | An ObjectOutputStream writes primitive data types and graphs of Java objects to an OutputStream. | | [PipedOutputStream](../java/io/PipedOutputStream.md) | A piped output stream can be connected to a piped input stream to create a communications pipe. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AssetFileDescriptor.AutoCloseOutputStream](../android/content/res/AssetFileDescriptor.AutoCloseOutputStream.md), [Base64OutputStream](../android/util/Base64OutputStream.md), [BufferedOutputStream](../java/io/BufferedOutputStream.md), [CheckedOutputStream](../java/util/zip/CheckedOutputStream.md), [CipherOutputStream](../javax/crypto/CipherOutputStream.md), [DataOutputStream](../java/io/DataOutputStream.md), [DeflaterOutputStream](../java/util/zip/DeflaterOutputStream.md), [DigestOutputStream](../java/security/DigestOutputStream.md), [GZIPOutputStream](../java/util/zip/GZIPOutputStream.md), [InflaterOutputStream](../java/util/zip/InflaterOutputStream.md), [JarOutputStream](../java/util/jar/JarOutputStream.md), [ParcelFileDescriptor.AutoCloseOutputStream](../android/os/ParcelFileDescriptor.AutoCloseOutputStream.md), and 2 others. |-----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AssetFileDescriptor.AutoCloseOutputStream](../android/content/res/AssetFileDescriptor.AutoCloseOutputStream.md) | An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android. | | [Base64OutputStream](../android/util/Base64OutputStream.md) | An OutputStream that does Base64 encoding on the data written to it, writing the resulting data to another OutputStream. | | [BufferedOutputStream](../java/io/BufferedOutputStream.md) | The class implements a buffered output stream. | | [CheckedOutputStream](../java/util/zip/CheckedOutputStream.md) | An output stream that also maintains a checksum of the data being written. | | [CipherOutputStream](../javax/crypto/CipherOutputStream.md) | A CipherOutputStream is composed of an OutputStream and a Cipher so that write() methods first process the data before writing them out to the underlying OutputStream. | | [DataOutputStream](../java/io/DataOutputStream.md) | A data output stream lets an application write primitive Java data types to an output stream in a portable way. | | [DeflaterOutputStream](../java/util/zip/DeflaterOutputStream.md) | This class implements an output stream filter for compressing data in the "deflate" compression format. | | [DigestOutputStream](../java/security/DigestOutputStream.md) | A transparent stream that updates the associated message digest using the bits going through the stream. | | [GZIPOutputStream](../java/util/zip/GZIPOutputStream.md) | This class implements a stream filter for writing compressed data in the GZIP file format. | | [InflaterOutputStream](../java/util/zip/InflaterOutputStream.md) | Implements an output stream filter for uncompressing data stored in the "deflate" compression format. | | [JarOutputStream](../java/util/jar/JarOutputStream.md) | The`JarOutputStream`class is used to write the contents of a JAR file to any output stream. | | [ParcelFileDescriptor.AutoCloseOutputStream](../android/os/ParcelFileDescriptor.AutoCloseOutputStream.md) | An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android. | | [PrintStream](../java/io/PrintStream.md) | A`PrintStream`adds functionality to another output stream, namely the ability to print representations of various data values conveniently. | | [ZipOutputStream](../java/util/zip/ZipOutputStream.md) | This class implements an output stream filter for writing files in the ZIP file format. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This abstract class is the superclass of all classes representing an output stream of bytes. An output stream accepts output bytes and sends them to some sink.

Applications that need to define a subclass of`OutputStream`must always provide at least a method that writes one byte of output.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OutputStream](../java/io/OutputStream.md))`()` Constructor for subclasses to call. |

| Public methods ||
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/io/OutputStream.md))`()` Closes this output stream and releases any system resources associated with this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](../java/io/OutputStream.md))`()` Flushes this output stream and forces any buffered output bytes to be written out. |
| openstatic [OutputStream](../java/io/OutputStream.md)! | [nullOutputStream](../java/io/OutputStream.md))`()` Returns a new`OutputStream`which discards all bytes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/OutputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes`b.length`bytes from the specified byte array to this output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/OutputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes`len`bytes from the specified byte array starting at offset`off`to this output stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/OutputStream.md))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes the specified byte to this output stream. |
| --- | --- |

## Public constructors

### OutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OutputStream()
```

Constructor for subclasses to call.

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this output stream and releases any system resources associated with this stream. The general contract of`close`is that it closes the output stream. A closed stream cannot perform output operations and cannot be reopened.

The`close`method of`OutputStream`does nothing.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Flushes this output stream and forces any buffered output bytes to be written out. The general contract of`flush`is that calling it is an indication that, if any bytes previously written have been buffered by the implementation of the output stream, such bytes should immediately be written to their intended destination.

If the intended destination of this stream is an abstraction provided by the underlying operating system, for example a file, then flushing the stream guarantees only that bytes previously written to the stream are passed to the operating system for writing; it does not guarantee that they are actually written to a physical device such as a disk drive.

The`flush`method of`OutputStream`does nothing.

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### nullOutputStream

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun nullOutputStream(): OutputStream!
```

Returns a new`OutputStream`which discards all bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect.

While the stream is open, the`write(int)`,`write(byte[])`, and`write(byte[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`.

The`flush()`method does nothing.

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------|
| [OutputStream](../java/io/OutputStream.md)! | an`OutputStream`which discards all bytes |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: ByteArray!): Unit
```

Writes`b.length`bytes from the specified byte array to this output stream. The general contract for`write(b)`is that it should have exactly the same effect as the call`write(b, 0, b.length)`.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- [java.io.OutputStream#write(byte[], int, int)](https://developer.android.com/reference/kotlin/java/io/OutputStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)) 

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes`len`bytes from the specified byte array starting at offset`off`to this output stream. The general contract for`write(b, off, len)`is that some of the bytes in the array`b`are written to the output stream in order; element`b[off]`is the first byte written and`b[off+len-1]`is the last byte written by this operation.

The`write`method of`OutputStream`calls the write method of one argument on each of the bytes to be written out. Subclasses are encouraged to override this method and provide a more efficient implementation.

If`b`is`null`, a`NullPointerException`is thrown.

If`off`is negative, or`len`is negative, or`off+len`is greater than the length of the array`b`, then an`IndexOutOfBoundsException`is thrown.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to write. |
| --- | --- |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs. In particular, an`IOException`is thrown if the output stream is closed. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(b: Int): Unit
```

Writes the specified byte to this output stream. The general contract for`write`is that one byte is written to the output stream. The byte to be written is the eight low-order bits of the argument`b`. The 24 high-order bits of`b`are ignored.

Subclasses of`OutputStream`must provide an implementation for this method.

| Parameters ||
|-----|---------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`byte`. |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs. In particular, an`IOException`may be thrown if the output stream has been closed. |
