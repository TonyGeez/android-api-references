# FilterOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FilterOutputStream

```
open class FilterOutputStream : OutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.OutputStream](../java/io/OutputStream.md) ||
| | ↳ | [java.io.FilterOutputStream](../java/io/FilterOutputStream.md) |

| Known Direct Subclasses [Base64OutputStream](../android/util/Base64OutputStream.md), [BufferedOutputStream](../java/io/BufferedOutputStream.md), [CheckedOutputStream](../java/util/zip/CheckedOutputStream.md), [CipherOutputStream](../javax/crypto/CipherOutputStream.md), [DataOutputStream](../java/io/DataOutputStream.md), [DeflaterOutputStream](../java/util/zip/DeflaterOutputStream.md), [DigestOutputStream](../java/security/DigestOutputStream.md), [InflaterOutputStream](../java/util/zip/InflaterOutputStream.md), [PrintStream](../java/io/PrintStream.md) |-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Base64OutputStream](../android/util/Base64OutputStream.md) | An OutputStream that does Base64 encoding on the data written to it, writing the resulting data to another OutputStream. | | [BufferedOutputStream](../java/io/BufferedOutputStream.md) | The class implements a buffered output stream. | | [CheckedOutputStream](../java/util/zip/CheckedOutputStream.md) | An output stream that also maintains a checksum of the data being written. | | [CipherOutputStream](../javax/crypto/CipherOutputStream.md) | A CipherOutputStream is composed of an OutputStream and a Cipher so that write() methods first process the data before writing them out to the underlying OutputStream. | | [DataOutputStream](../java/io/DataOutputStream.md) | A data output stream lets an application write primitive Java data types to an output stream in a portable way. | | [DeflaterOutputStream](../java/util/zip/DeflaterOutputStream.md) | This class implements an output stream filter for compressing data in the "deflate" compression format. | | [DigestOutputStream](../java/security/DigestOutputStream.md) | A transparent stream that updates the associated message digest using the bits going through the stream. | | [InflaterOutputStream](../java/util/zip/InflaterOutputStream.md) | Implements an output stream filter for uncompressing data stored in the "deflate" compression format. | | [PrintStream](../java/io/PrintStream.md) | A`PrintStream`adds functionality to another output stream, namely the ability to print representations of various data values conveniently. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [GZIPOutputStream](../java/util/zip/GZIPOutputStream.md), [JarOutputStream](../java/util/jar/JarOutputStream.md), [ZipOutputStream](../java/util/zip/ZipOutputStream.md) |---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------| | [GZIPOutputStream](../java/util/zip/GZIPOutputStream.md) | This class implements a stream filter for writing compressed data in the GZIP file format. | | [JarOutputStream](../java/util/jar/JarOutputStream.md) | The`JarOutputStream`class is used to write the contents of a JAR file to any output stream. | | [ZipOutputStream](../java/util/zip/ZipOutputStream.md) | This class implements an output stream filter for writing files in the ZIP file format. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class is the superclass of all classes that filter output streams. These streams sit on top of an already existing output stream (the*underlying*output stream) which it uses as its basic sink of data, but possibly transforming the data along the way or providing additional functionality.

The class`FilterOutputStream`itself simply overrides all methods of`OutputStream`with versions that pass all requests to the underlying output stream. Subclasses of`FilterOutputStream`may further override some of these methods as well as provide additional methods and fields.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FilterOutputStream](../java/io/FilterOutputStream.md))`(`out:` ` [OutputStream](../java/io/OutputStream.md)!`)` Creates an output stream filter built on top of the specified underlying output stream. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/io/FilterOutputStream.md))`()` Closes this output stream and releases any system resources associated with the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](../java/io/FilterOutputStream.md))`()` Flushes this output stream and forces any buffered output bytes to be written out to the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/FilterOutputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes`b.length`bytes to this output stream. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/FilterOutputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes`len`bytes from the specified`byte`array starting at offset`off`to this output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/FilterOutputStream.md))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes the specified`byte`to this output stream. |

| Inherited functions ||
|---|---|
| From class [OutputStream](../java/io/OutputStream.md) |--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](../java/io/OutputStream.md)! | [nullOutputStream](../java/io/OutputStream.md))`()` <br /> Returns a new`OutputStream`which discards all bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`write(int)`,`write(byte[])`, and`write(byte[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The`flush()`method does nothing. <br /> | ||

| Properties ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [OutputStream](../java/io/OutputStream.md)! | [out](../java/io/FilterOutputStream.md) The underlying output stream to be filtered. |

## Public constructors

### FilterOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FilterOutputStream(out: OutputStream!)
```

Creates an output stream filter built on top of the specified underlying output stream.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java/io/OutputStream.md)!:the underlying output stream to be assigned to the field`this.out`for later use, or`null`if this instance is to be created without an underlying stream. |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this output stream and releases any system resources associated with the stream.

When not already closed, the`close`method of`FilterOutputStream`calls its`flush`method, and then calls the`close`method of its underlying output stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if an I/O error occurs. |
| --- | --- |

**See Also**

- [java.io.FilterOutputStream#out](../java/io/FilterOutputStream.md) 

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Flushes this output stream and forces any buffered output bytes to be written out to the stream.

The`flush`method of`FilterOutputStream`calls the`flush`method of its underlying output stream.

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- [java.io.FilterOutputStream#out](../java/io/FilterOutputStream.md) 

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: ByteArray!): Unit
```

Writes`b.length`bytes to this output stream.

The`write`method of`FilterOutputStream`calls its`write`method of three arguments with the arguments`b`,`0`, and`b.length`.

Note that this method does not call the one-argument`write`method of its underlying output stream with the single argument`b`.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- [java.io.FilterOutputStream#write(byte[], int, int)](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)) 

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes`len`bytes from the specified`byte`array starting at offset`off`to this output stream.

The`write`method of`FilterOutputStream`calls the`write`method of one argument on each`byte`to output.

Note that this method does not call the`write`method of its underlying output stream with the same arguments. Subclasses of`FilterOutputStream`should provide a more efficient implementation of this method.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to write. |
| --- | --- |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs. In particular, an`IOException`is thrown if the output stream is closed. |
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- [java.io.FilterOutputStream#write(int)](../java/io/FilterOutputStream.md)) 

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: Int): Unit
```

Writes the specified`byte`to this output stream.

The`write`method of`FilterOutputStream`calls the`write`method of its underlying output stream, that is, it performs`out.write(b)`.

Implements the abstract`write`method of`OutputStream`.

| Parameters ||
|-----|---------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`byte`. |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs. In particular, an`IOException`may be thrown if the output stream has been closed. |
| `java.io.IOException` | if an I/O error occurs. |

## Properties

### out

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var out: OutputStream!
```

The underlying output stream to be filtered.
