# Flushable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Flushable

```
interface Flushable
```

| [java.io.Flushable](../java/io/Flushable.md) |

| Known Direct Subclasses [Console](../java/io/Console.md), [Formatter](../java/util/Formatter.md), [OutputStream](../java/io/OutputStream.md), [Writer](../java/io/Writer.md) |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------| | [Console](../java/io/Console.md) | Methods to access the character-based console device, if any, associated with the current Java virtual machine. | | [Formatter](../java/util/Formatter.md) | An interpreter for printf-style format strings. | | [OutputStream](../java/io/OutputStream.md) | This abstract class is the superclass of all classes representing an output stream of bytes. | | [Writer](../java/io/Writer.md) | Abstract class for writing to character streams. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AssetFileDescriptor.AutoCloseOutputStream](../android/content/res/AssetFileDescriptor.AutoCloseOutputStream.md), [Base64OutputStream](../android/util/Base64OutputStream.md), [BufferedOutputStream](../java/io/BufferedOutputStream.md), [BufferedWriter](../java/io/BufferedWriter.md), [ByteArrayOutputStream](../java/io/ByteArrayOutputStream.md), [CharArrayWriter](../java/io/CharArrayWriter.md), [CheckedOutputStream](../java/util/zip/CheckedOutputStream.md), [CipherOutputStream](../javax/crypto/CipherOutputStream.md), [DataOutputStream](../java/io/DataOutputStream.md), [DeflaterOutputStream](../java/util/zip/DeflaterOutputStream.md), [DigestOutputStream](../java/security/DigestOutputStream.md), [FileOutputStream](../java/io/FileOutputStream.md), and 15 others. |-----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AssetFileDescriptor.AutoCloseOutputStream](../android/content/res/AssetFileDescriptor.AutoCloseOutputStream.md) | An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android. | | [Base64OutputStream](../android/util/Base64OutputStream.md) | An OutputStream that does Base64 encoding on the data written to it, writing the resulting data to another OutputStream. | | [BufferedOutputStream](../java/io/BufferedOutputStream.md) | The class implements a buffered output stream. | | [BufferedWriter](../java/io/BufferedWriter.md) | Writes text to a character-output stream, buffering characters so as to provide for the efficient writing of single characters, arrays, and strings. | | [ByteArrayOutputStream](../java/io/ByteArrayOutputStream.md) | This class implements an output stream in which the data is written into a byte array. | | [CharArrayWriter](../java/io/CharArrayWriter.md) | This class implements a character buffer that can be used as an Writer. | | [CheckedOutputStream](../java/util/zip/CheckedOutputStream.md) | An output stream that also maintains a checksum of the data being written. | | [CipherOutputStream](../javax/crypto/CipherOutputStream.md) | A CipherOutputStream is composed of an OutputStream and a Cipher so that write() methods first process the data before writing them out to the underlying OutputStream. | | [DataOutputStream](../java/io/DataOutputStream.md) | A data output stream lets an application write primitive Java data types to an output stream in a portable way. | | [DeflaterOutputStream](../java/util/zip/DeflaterOutputStream.md) | This class implements an output stream filter for compressing data in the "deflate" compression format. | | [DigestOutputStream](../java/security/DigestOutputStream.md) | A transparent stream that updates the associated message digest using the bits going through the stream. | | [FileOutputStream](../java/io/FileOutputStream.md) | A file output stream is an output stream for writing data to a`File`or to a`FileDescriptor`. | | [FileWriter](../java/io/FileWriter.md) | Writes text to character files using a default buffer size. | | [FilterOutputStream](../java/io/FilterOutputStream.md) | This class is the superclass of all classes that filter output streams. | | [FilterWriter](../java/io/FilterWriter.md) | Abstract class for writing filtered character streams. | | [GZIPOutputStream](../java/util/zip/GZIPOutputStream.md) | This class implements a stream filter for writing compressed data in the GZIP file format. | | [InflaterOutputStream](../java/util/zip/InflaterOutputStream.md) | Implements an output stream filter for uncompressing data stored in the "deflate" compression format. | | [JarOutputStream](../java/util/jar/JarOutputStream.md) | The`JarOutputStream`class is used to write the contents of a JAR file to any output stream. | | [ObjectOutputStream](../java/io/ObjectOutputStream.md) | An ObjectOutputStream writes primitive data types and graphs of Java objects to an OutputStream. | | [OutputStreamWriter](../java/io/OutputStreamWriter.md) | An OutputStreamWriter is a bridge from character streams to byte streams: Characters written to it are encoded into bytes using a specified . | | [ParcelFileDescriptor.AutoCloseOutputStream](../android/os/ParcelFileDescriptor.AutoCloseOutputStream.md) | An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android. | | [PipedOutputStream](../java/io/PipedOutputStream.md) | A piped output stream can be connected to a piped input stream to create a communications pipe. | | [PipedWriter](../java/io/PipedWriter.md) | Piped character-output streams. | | [PrintStream](../java/io/PrintStream.md) | A`PrintStream`adds functionality to another output stream, namely the ability to print representations of various data values conveniently. | | [PrintWriter](../java/io/PrintWriter.md) | Prints formatted representations of objects to a text-output stream. | | [StringWriter](../java/io/StringWriter.md) | A character stream that collects its output in a string buffer, which can then be used to construct a string. | | [ZipOutputStream](../java/util/zip/ZipOutputStream.md) | This class implements an output stream filter for writing files in the ZIP file format. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A`Flushable`is a destination of data that can be flushed. The flush method is invoked to write any buffered output to the underlying stream.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](../java/io/Flushable.md))`()` Flushes this stream by writing any buffered output to the underlying stream. |

## Public methods

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun flush(): Unit
```

Flushes this stream by writing any buffered output to the underlying stream.

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |
