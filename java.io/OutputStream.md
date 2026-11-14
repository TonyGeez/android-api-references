# OutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OutputStream

```
abstract class OutputStream : Closeable, Flushable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.io.OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream#) |

| Known Direct Subclasses [ByteArrayOutputStream](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream), [FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream), [FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream), [ObjectOutputStream](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream), [PipedOutputStream](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream) |-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------| | [ByteArrayOutputStream](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream) | This class implements an output stream in which the data is written into a byte array. | | [FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream) | A file output stream is an output stream for writing data to a`File`or to a`FileDescriptor`. | | [FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream) | This class is the superclass of all classes that filter output streams. | | [ObjectOutputStream](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream) | An ObjectOutputStream writes primitive data types and graphs of Java objects to an OutputStream. | | [PipedOutputStream](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream) | A piped output stream can be connected to a piped input stream to create a communications pipe. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AssetFileDescriptor.AutoCloseOutputStream](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.AutoCloseOutputStream.html#), [Base64OutputStream](https://developer.android.com/reference/kotlin/android/util/Base64OutputStream.html#), [BufferedOutputStream](https://developer.android.com/reference/kotlin/java/io/BufferedOutputStream), [CheckedOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/CheckedOutputStream.html#), [CipherOutputStream](https://developer.android.com/reference/kotlin/javax/crypto/CipherOutputStream.html#), [DataOutputStream](https://developer.android.com/reference/kotlin/java/io/DataOutputStream), [DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream.html#), [DigestOutputStream](https://developer.android.com/reference/kotlin/java/security/DigestOutputStream.html#), [GZIPOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/GZIPOutputStream.html#), [InflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream.html#), [JarOutputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarOutputStream.html#), [ParcelFileDescriptor.AutoCloseOutputStream](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.AutoCloseOutputStream.html#), and 2 others. |-----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AssetFileDescriptor.AutoCloseOutputStream](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.AutoCloseOutputStream.html#) | An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android. | | [Base64OutputStream](https://developer.android.com/reference/kotlin/android/util/Base64OutputStream.html#) | An OutputStream that does Base64 encoding on the data written to it, writing the resulting data to another OutputStream. | | [BufferedOutputStream](https://developer.android.com/reference/kotlin/java/io/BufferedOutputStream) | The class implements a buffered output stream. | | [CheckedOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/CheckedOutputStream.html#) | An output stream that also maintains a checksum of the data being written. | | [CipherOutputStream](https://developer.android.com/reference/kotlin/javax/crypto/CipherOutputStream.html#) | A CipherOutputStream is composed of an OutputStream and a Cipher so that write() methods first process the data before writing them out to the underlying OutputStream. | | [DataOutputStream](https://developer.android.com/reference/kotlin/java/io/DataOutputStream) | A data output stream lets an application write primitive Java data types to an output stream in a portable way. | | [DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream.html#) | This class implements an output stream filter for compressing data in the "deflate" compression format. | | [DigestOutputStream](https://developer.android.com/reference/kotlin/java/security/DigestOutputStream.html#) | A transparent stream that updates the associated message digest using the bits going through the stream. | | [GZIPOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/GZIPOutputStream.html#) | This class implements a stream filter for writing compressed data in the GZIP file format. | | [InflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream.html#) | Implements an output stream filter for uncompressing data stored in the "deflate" compression format. | | [JarOutputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarOutputStream.html#) | The`JarOutputStream`class is used to write the contents of a JAR file to any output stream. | | [ParcelFileDescriptor.AutoCloseOutputStream](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.AutoCloseOutputStream.html#) | An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android. | | [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream) | A`PrintStream`adds functionality to another output stream, namely the ability to print representations of various data values conveniently. | | [ZipOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#) | This class implements an output stream filter for writing files in the ZIP file format. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This abstract class is the superclass of all classes representing an output stream of bytes. An output stream accepts output bytes and sends them to some sink.

Applications that need to define a subclass of`OutputStream`must always provide at least a method that writes one byte of output.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream#OutputStream())`()` Constructor for subclasses to call. |

| Public methods ||
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/OutputStream#close())`()` Closes this output stream and releases any system resources associated with this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/io/OutputStream#flush())`()` Flushes this output stream and forces any buffered output bytes to be written out. |
| openstatic [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream#)! | [nullOutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream#nullOutputStream())`()` Returns a new`OutputStream`which discards all bytes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/OutputStream#write(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes`b.length`bytes from the specified byte array to this output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/OutputStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes`len`bytes from the specified byte array starting at offset`off`to this output stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/OutputStream#write(kotlin.Int))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes the specified byte to this output stream. |
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
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream#)! | an`OutputStream`which discards all bytes |

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
