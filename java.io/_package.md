# java.io

# java.io

## Interfaces

| [Closeable](https://developer.android.com/reference/kotlin/java/io/Closeable) | A`Closeable`is a source or destination of data that can be closed. |
| [DataInput](https://developer.android.com/reference/kotlin/java/io/DataInput) | The`DataInput`interface provides for reading bytes from a binary stream and reconstructing from them data in any of the Java primitive types. |
| [DataOutput](https://developer.android.com/reference/kotlin/java/io/DataOutput) | The`DataOutput`interface provides for converting data from any of the Java primitive types to a series of bytes and writing these bytes to a binary stream. |
| [Externalizable](https://developer.android.com/reference/kotlin/java/io/Externalizable) | Only the identity of the class of an Externalizable instance is written in the serialization stream and it is the responsibility of the class to save and restore the contents of its instances. |
| [FileFilter](https://developer.android.com/reference/kotlin/java/io/FileFilter) | A filter for abstract pathnames. |
| [FilenameFilter](https://developer.android.com/reference/kotlin/java/io/FilenameFilter) | Instances of classes that implement this interface are used to filter filenames. |
| [Flushable](https://developer.android.com/reference/kotlin/java/io/Flushable) | A`Flushable`is a destination of data that can be flushed. |
| [ObjectInput](https://developer.android.com/reference/kotlin/java/io/ObjectInput) | ObjectInput extends the DataInput interface to include the reading of objects. |
| [ObjectInputValidation](https://developer.android.com/reference/kotlin/java/io/ObjectInputValidation) | Callback interface to allow validation of objects within a graph. |
| [ObjectOutput](https://developer.android.com/reference/kotlin/java/io/ObjectOutput) | ObjectOutput extends the DataOutput interface to include writing of objects. |
| [ObjectStreamConstants](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants) | Constants written into the Object Serialization Stream. |
| [Serializable](https://developer.android.com/reference/kotlin/java/io/Serializable) | Serializability of a class is enabled by the class implementing the java. |

## Classes

| [BufferedInputStream](https://developer.android.com/reference/kotlin/java/io/BufferedInputStream) | A`BufferedInputStream`adds functionality to another input stream-namely, the ability to buffer the input and to support the`mark`and`reset`methods. |
| [BufferedOutputStream](https://developer.android.com/reference/kotlin/java/io/BufferedOutputStream) | The class implements a buffered output stream. |
| [BufferedReader](https://developer.android.com/reference/kotlin/java/io/BufferedReader) | Reads text from a character-input stream, buffering characters so as to provide for the efficient reading of characters, arrays, and lines. |
| [BufferedWriter](https://developer.android.com/reference/kotlin/java/io/BufferedWriter) | Writes text to a character-output stream, buffering characters so as to provide for the efficient writing of single characters, arrays, and strings. |
| [ByteArrayInputStream](https://developer.android.com/reference/kotlin/java/io/ByteArrayInputStream) | A`ByteArrayInputStream`contains an internal buffer that contains bytes that may be read from the stream. |
| [ByteArrayOutputStream](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream) | This class implements an output stream in which the data is written into a byte array. |
| [CharArrayReader](https://developer.android.com/reference/kotlin/java/io/CharArrayReader) | This class implements a character buffer that can be used as a character-input stream. |
| [CharArrayWriter](https://developer.android.com/reference/kotlin/java/io/CharArrayWriter) | This class implements a character buffer that can be used as an Writer. |
| [Console](https://developer.android.com/reference/kotlin/java/io/Console) | Methods to access the character-based console device, if any, associated with the current Java virtual machine. |
| [DataInputStream](https://developer.android.com/reference/kotlin/java/io/DataInputStream) | A data input stream lets an application read primitive Java data types from an underlying input stream in a machine-independent way. |
| [DataOutputStream](https://developer.android.com/reference/kotlin/java/io/DataOutputStream) | A data output stream lets an application write primitive Java data types to an output stream in a portable way. |
| [File](https://developer.android.com/reference/kotlin/java/io/File) | An abstract representation of file and directory pathnames. |
| [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor) | Instances of the file descriptor class serve as an opaque handle to the underlying machine-specific structure representing an open file, an open socket, or another source or sink of bytes. |
| [FileInputStream](https://developer.android.com/reference/kotlin/java/io/FileInputStream) | A`FileInputStream`obtains input bytes from a file in a file system. |
| [FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream) | A file output stream is an output stream for writing data to a`File`or to a`FileDescriptor`. |
| [FilePermission](https://developer.android.com/reference/kotlin/java/io/FilePermission) | Legacy security code; do not use. |
| [FileReader](https://developer.android.com/reference/kotlin/java/io/FileReader) | Reads text from character files using a default buffer size. |
| [FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter) | Writes text to character files using a default buffer size. |
| [FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream) | A`FilterInputStream`contains some other input stream, which it uses as its basic source of data, possibly transforming the data along the way or providing additional functionality. |
| [FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream) | This class is the superclass of all classes that filter output streams. |
| [FilterReader](https://developer.android.com/reference/kotlin/java/io/FilterReader) | Abstract class for reading filtered character streams. |
| [FilterWriter](https://developer.android.com/reference/kotlin/java/io/FilterWriter) | Abstract class for writing filtered character streams. |
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream) | This abstract class is the superclass of all classes representing an input stream of bytes. |
| [InputStreamReader](https://developer.android.com/reference/kotlin/java/io/InputStreamReader) | An InputStreamReader is a bridge from byte streams to character streams: It reads bytes and decodes them into characters using a specified . |
| [LineNumberInputStream](https://developer.android.com/reference/kotlin/java/io/LineNumberInputStream) | This class is an input stream filter that provides the added functionality of keeping track of the current line number. |
| [LineNumberReader](https://developer.android.com/reference/kotlin/java/io/LineNumberReader) | A buffered character-input stream that keeps track of line numbers. |
| [ObjectInputStream](https://developer.android.com/reference/kotlin/java/io/ObjectInputStream) | An ObjectInputStream deserializes primitive data and objects previously written using an ObjectOutputStream. |
| [ObjectOutputStream](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream) | An ObjectOutputStream writes primitive data types and graphs of Java objects to an OutputStream. |
| [ObjectStreamClass](https://developer.android.com/reference/kotlin/java/io/ObjectStreamClass) | Serialization's descriptor for classes. |
| [ObjectStreamField](https://developer.android.com/reference/kotlin/java/io/ObjectStreamField) | A description of a Serializable field from a Serializable class. |
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream) | This abstract class is the superclass of all classes representing an output stream of bytes. |
| [OutputStreamWriter](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter) | An OutputStreamWriter is a bridge from character streams to byte streams: Characters written to it are encoded into bytes using a specified . |
| [PipedInputStream](https://developer.android.com/reference/kotlin/java/io/PipedInputStream) | A piped input stream should be connected to a piped output stream; the piped input stream then provides whatever data bytes are written to the piped output stream. |
| [PipedOutputStream](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream) | A piped output stream can be connected to a piped input stream to create a communications pipe. |
| [PipedReader](https://developer.android.com/reference/kotlin/java/io/PipedReader) | Piped character-input streams. |
| [PipedWriter](https://developer.android.com/reference/kotlin/java/io/PipedWriter) | Piped character-output streams. |
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream) | A`PrintStream`adds functionality to another output stream, namely the ability to print representations of various data values conveniently. |
| [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter) | Prints formatted representations of objects to a text-output stream. |
| [PushbackInputStream](https://developer.android.com/reference/kotlin/java/io/PushbackInputStream) | A`PushbackInputStream`adds functionality to another input stream, namely the ability to "push back" or "unread" bytes, by storing pushed-back bytes in an internal buffer. |
| [PushbackReader](https://developer.android.com/reference/kotlin/java/io/PushbackReader) | A character-stream reader that allows characters to be pushed back into the stream. |
| [RandomAccessFile](https://developer.android.com/reference/kotlin/java/io/RandomAccessFile) | Instances of this class support both reading and writing to a random access file. |
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader) | Abstract class for reading character streams. |
| [SequenceInputStream](https://developer.android.com/reference/kotlin/java/io/SequenceInputStream) | A`SequenceInputStream`represents the logical concatenation of other input streams. |
| [SerializablePermission](https://developer.android.com/reference/kotlin/java/io/SerializablePermission) | This legacy security is not supported on Android. |
| [StreamTokenizer](https://developer.android.com/reference/kotlin/java/io/StreamTokenizer) | The`StreamTokenizer`class takes an input stream and parses it into "tokens", allowing the tokens to be read one at a time. |
| [StringBufferInputStream](https://developer.android.com/reference/kotlin/java/io/StringBufferInputStream) | This class allows an application to create an input stream in which the bytes read are supplied by the contents of a string. |
| [StringReader](https://developer.android.com/reference/kotlin/java/io/StringReader) | A character stream whose source is a string. |
| [StringWriter](https://developer.android.com/reference/kotlin/java/io/StringWriter) | A character stream that collects its output in a string buffer, which can then be used to construct a string. |
| [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | Abstract class for writing to character streams. |

## Exceptions

| [CharConversionException](https://developer.android.com/reference/kotlin/java/io/CharConversionException) | Base class for character conversion exceptions. |
| [EOFException](https://developer.android.com/reference/kotlin/java/io/EOFException) | Signals that an end of file or end of stream has been reached unexpectedly during input. |
| [FileNotFoundException](https://developer.android.com/reference/kotlin/java/io/FileNotFoundException) | Signals that an attempt to open the file denoted by a specified pathname has failed. |
| [InterruptedIOException](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException) | Signals that an I/O operation has been interrupted. |
| [InvalidClassException](https://developer.android.com/reference/kotlin/java/io/InvalidClassException) | Thrown when the Serialization runtime detects one of the following problems with a Class. |
| [InvalidObjectException](https://developer.android.com/reference/kotlin/java/io/InvalidObjectException) | Indicates that one or more deserialized objects failed validation tests. |
| [IOError](https://developer.android.com/reference/kotlin/java/io/IOError) | Thrown when a serious I/O error has occurred. |
| [IOException](https://developer.android.com/reference/kotlin/java/io/IOException) | Signals that an I/O exception of some sort has occurred. |
| [NotActiveException](https://developer.android.com/reference/kotlin/java/io/NotActiveException) | Thrown when serialization or deserialization is not active. |
| [NotSerializableException](https://developer.android.com/reference/kotlin/java/io/NotSerializableException) | Thrown when an instance is required to have a Serializable interface. |
| [ObjectStreamException](https://developer.android.com/reference/kotlin/java/io/ObjectStreamException) | Superclass of all exceptions specific to Object Stream classes. |
| [OptionalDataException](https://developer.android.com/reference/kotlin/java/io/OptionalDataException) | Exception indicating the failure of an object read operation due to unread primitive data, or the end of data belonging to a serialized object in the stream. |
| [StreamCorruptedException](https://developer.android.com/reference/kotlin/java/io/StreamCorruptedException) | Thrown when control information that was read from an object stream violates internal consistency checks. |
| [SyncFailedException](https://developer.android.com/reference/kotlin/java/io/SyncFailedException) | Signals that a sync operation has failed. |
| [UncheckedIOException](https://developer.android.com/reference/kotlin/java/io/UncheckedIOException) | Wraps an [IOException](https://developer.android.com/reference/kotlin/java/io/IOException) with an unchecked exception. |
| [UnsupportedEncodingException](https://developer.android.com/reference/kotlin/java/io/UnsupportedEncodingException) | The Character Encoding is not supported. |
| [UTFDataFormatException](https://developer.android.com/reference/kotlin/java/io/UTFDataFormatException) | Signals that a malformed string in [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) format has been read in a data input stream or by any class that implements the data input interface. |
| [WriteAbortedException](https://developer.android.com/reference/kotlin/java/io/WriteAbortedException) | Signals that one of the ObjectStreamExceptions was thrown during a write operation. |

## Annotations

| [Serial](https://developer.android.com/reference/kotlin/java/io/Serial) | Indicates that an annotated field or method is part of the [serialization mechanism](https://developer.android.com/reference/kotlin/java/io/Serializable) defined by the Java Object Serialization Specification. |
