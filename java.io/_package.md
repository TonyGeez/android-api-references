# java.io

# java.io

## Interfaces

| [Closeable](../java/io/Closeable.md) | A`Closeable`is a source or destination of data that can be closed. |
| --- | --- |
| [DataInput](../java/io/DataInput.md) | The`DataInput`interface provides for reading bytes from a binary stream and reconstructing from them data in any of the Java primitive types. |
| [DataOutput](../java/io/DataOutput.md) | The`DataOutput`interface provides for converting data from any of the Java primitive types to a series of bytes and writing these bytes to a binary stream. |
| [Externalizable](../java/io/Externalizable.md) | Only the identity of the class of an Externalizable instance is written in the serialization stream and it is the responsibility of the class to save and restore the contents of its instances. |
| --- | --- |
| [FileFilter](../java/io/FileFilter.md) | A filter for abstract pathnames. |
| [FilenameFilter](../java/io/FilenameFilter.md) | Instances of classes that implement this interface are used to filter filenames. |
| [Flushable](../java/io/Flushable.md) | A`Flushable`is a destination of data that can be flushed. |
| --- | --- |
| [ObjectInput](../java/io/ObjectInput.md) | ObjectInput extends the DataInput interface to include the reading of objects. |
| [ObjectInputValidation](../java/io/ObjectInputValidation.md) | Callback interface to allow validation of objects within a graph. |
| [ObjectOutput](../java/io/ObjectOutput.md) | ObjectOutput extends the DataOutput interface to include writing of objects. |
| --- | --- |
| [ObjectStreamConstants](../java/io/ObjectStreamConstants.md) | Constants written into the Object Serialization Stream. |
| [Serializable](../java/io/Serializable.md) | Serializability of a class is enabled by the class implementing the java. |

## Classes

| [BufferedInputStream](../java/io/BufferedInputStream.md) | A`BufferedInputStream`adds functionality to another input stream-namely, the ability to buffer the input and to support the`mark`and`reset`methods. |
| --- | --- |
| [BufferedOutputStream](../java/io/BufferedOutputStream.md) | The class implements a buffered output stream. |
| [BufferedReader](../java/io/BufferedReader.md) | Reads text from a character-input stream, buffering characters so as to provide for the efficient reading of characters, arrays, and lines. |
| [BufferedWriter](../java/io/BufferedWriter.md) | Writes text to a character-output stream, buffering characters so as to provide for the efficient writing of single characters, arrays, and strings. |
| --- | --- |
| [ByteArrayInputStream](../java/io/ByteArrayInputStream.md) | A`ByteArrayInputStream`contains an internal buffer that contains bytes that may be read from the stream. |
| [ByteArrayOutputStream](../java/io/ByteArrayOutputStream.md) | This class implements an output stream in which the data is written into a byte array. |
| [CharArrayReader](../java/io/CharArrayReader.md) | This class implements a character buffer that can be used as a character-input stream. |
| --- | --- |
| [CharArrayWriter](../java/io/CharArrayWriter.md) | This class implements a character buffer that can be used as an Writer. |
| [Console](../java/io/Console.md) | Methods to access the character-based console device, if any, associated with the current Java virtual machine. |
| [DataInputStream](../java/io/DataInputStream.md) | A data input stream lets an application read primitive Java data types from an underlying input stream in a machine-independent way. |
| --- | --- |
| [DataOutputStream](../java/io/DataOutputStream.md) | A data output stream lets an application write primitive Java data types to an output stream in a portable way. |
| [File](../java/io/File.md) | An abstract representation of file and directory pathnames. |
| [FileDescriptor](../java/io/FileDescriptor.md) | Instances of the file descriptor class serve as an opaque handle to the underlying machine-specific structure representing an open file, an open socket, or another source or sink of bytes. |
| --- | --- |
| [FileInputStream](../java/io/FileInputStream.md) | A`FileInputStream`obtains input bytes from a file in a file system. |
| [FileOutputStream](../java/io/FileOutputStream.md) | A file output stream is an output stream for writing data to a`File`or to a`FileDescriptor`. |
| [FilePermission](../java/io/FilePermission.md) | Legacy security code; do not use. |
| --- | --- |
| [FileReader](../java/io/FileReader.md) | Reads text from character files using a default buffer size. |
| [FileWriter](../java/io/FileWriter.md) | Writes text to character files using a default buffer size. |
| [FilterInputStream](../java/io/FilterInputStream.md) | A`FilterInputStream`contains some other input stream, which it uses as its basic source of data, possibly transforming the data along the way or providing additional functionality. |
| --- | --- |
| [FilterOutputStream](../java/io/FilterOutputStream.md) | This class is the superclass of all classes that filter output streams. |
| [FilterReader](../java/io/FilterReader.md) | Abstract class for reading filtered character streams. |
| [FilterWriter](../java/io/FilterWriter.md) | Abstract class for writing filtered character streams. |
| --- | --- |
| [InputStream](../java/io/InputStream.md) | This abstract class is the superclass of all classes representing an input stream of bytes. |
| [InputStreamReader](../java/io/InputStreamReader.md) | An InputStreamReader is a bridge from byte streams to character streams: It reads bytes and decodes them into characters using a specified . |
| [LineNumberInputStream](../java/io/LineNumberInputStream.md) | This class is an input stream filter that provides the added functionality of keeping track of the current line number. |
| --- | --- |
| [LineNumberReader](../java/io/LineNumberReader.md) | A buffered character-input stream that keeps track of line numbers. |
| [ObjectInputStream](../java/io/ObjectInputStream.md) | An ObjectInputStream deserializes primitive data and objects previously written using an ObjectOutputStream. |
| [ObjectOutputStream](../java/io/ObjectOutputStream.md) | An ObjectOutputStream writes primitive data types and graphs of Java objects to an OutputStream. |
| --- | --- |
| [ObjectStreamClass](../java/io/ObjectStreamClass.md) | Serialization's descriptor for classes. |
| [ObjectStreamField](../java/io/ObjectStreamField.md) | A description of a Serializable field from a Serializable class. |
| [OutputStream](../java/io/OutputStream.md) | This abstract class is the superclass of all classes representing an output stream of bytes. |
| --- | --- |
| [OutputStreamWriter](../java/io/OutputStreamWriter.md) | An OutputStreamWriter is a bridge from character streams to byte streams: Characters written to it are encoded into bytes using a specified . |
| [PipedInputStream](../java/io/PipedInputStream.md) | A piped input stream should be connected to a piped output stream; the piped input stream then provides whatever data bytes are written to the piped output stream. |
| [PipedOutputStream](../java/io/PipedOutputStream.md) | A piped output stream can be connected to a piped input stream to create a communications pipe. |
| --- | --- |
| [PipedReader](../java/io/PipedReader.md) | Piped character-input streams. |
| [PipedWriter](../java/io/PipedWriter.md) | Piped character-output streams. |
| [PrintStream](../java/io/PrintStream.md) | A`PrintStream`adds functionality to another output stream, namely the ability to print representations of various data values conveniently. |
| --- | --- |
| [PrintWriter](../java/io/PrintWriter.md) | Prints formatted representations of objects to a text-output stream. |
| [PushbackInputStream](../java/io/PushbackInputStream.md) | A`PushbackInputStream`adds functionality to another input stream, namely the ability to "push back" or "unread" bytes, by storing pushed-back bytes in an internal buffer. |
| [PushbackReader](../java/io/PushbackReader.md) | A character-stream reader that allows characters to be pushed back into the stream. |
| --- | --- |
| [RandomAccessFile](../java/io/RandomAccessFile.md) | Instances of this class support both reading and writing to a random access file. |
| [Reader](../java/io/Reader.md) | Abstract class for reading character streams. |
| [SequenceInputStream](../java/io/SequenceInputStream.md) | A`SequenceInputStream`represents the logical concatenation of other input streams. |
| --- | --- |
| [SerializablePermission](../java/io/SerializablePermission.md) | This legacy security is not supported on Android. |
| [StreamTokenizer](../java/io/StreamTokenizer.md) | The`StreamTokenizer`class takes an input stream and parses it into "tokens", allowing the tokens to be read one at a time. |
| [StringBufferInputStream](../java/io/StringBufferInputStream.md) | This class allows an application to create an input stream in which the bytes read are supplied by the contents of a string. |
| --- | --- |
| [StringReader](../java/io/StringReader.md) | A character stream whose source is a string. |
| [StringWriter](../java/io/StringWriter.md) | A character stream that collects its output in a string buffer, which can then be used to construct a string. |
| [Writer](../java/io/Writer.md) | Abstract class for writing to character streams. |
| --- | --- |

## Exceptions

| [CharConversionException](../java/io/CharConversionException.md) | Base class for character conversion exceptions. |
| --- | --- |
| [EOFException](../java/io/EOFException.md) | Signals that an end of file or end of stream has been reached unexpectedly during input. |
| [FileNotFoundException](../java/io/FileNotFoundException.md) | Signals that an attempt to open the file denoted by a specified pathname has failed. |
| [InterruptedIOException](../java/io/InterruptedIOException.md) | Signals that an I/O operation has been interrupted. |
| --- | --- |
| [InvalidClassException](../java/io/InvalidClassException.md) | Thrown when the Serialization runtime detects one of the following problems with a Class. |
| [InvalidObjectException](../java/io/InvalidObjectException.md) | Indicates that one or more deserialized objects failed validation tests. |
| [IOError](../java/io/IOError.md) | Thrown when a serious I/O error has occurred. |
| --- | --- |
| [IOException](../java/io/IOException.md) | Signals that an I/O exception of some sort has occurred. |
| [NotActiveException](../java/io/NotActiveException.md) | Thrown when serialization or deserialization is not active. |
| [NotSerializableException](../java/io/NotSerializableException.md) | Thrown when an instance is required to have a Serializable interface. |
| --- | --- |
| [ObjectStreamException](../java/io/ObjectStreamException.md) | Superclass of all exceptions specific to Object Stream classes. |
| [OptionalDataException](../java/io/OptionalDataException.md) | Exception indicating the failure of an object read operation due to unread primitive data, or the end of data belonging to a serialized object in the stream. |
| [StreamCorruptedException](../java/io/StreamCorruptedException.md) | Thrown when control information that was read from an object stream violates internal consistency checks. |
| --- | --- |
| [SyncFailedException](../java/io/SyncFailedException.md) | Signals that a sync operation has failed. |
| [UncheckedIOException](../java/io/UncheckedIOException.md) | Wraps an [IOException](../java/io/IOException.md) with an unchecked exception. |
| [UnsupportedEncodingException](../java/io/UnsupportedEncodingException.md) | The Character Encoding is not supported. |
| --- | --- |
| [UTFDataFormatException](../java/io/UTFDataFormatException.md) | Signals that a malformed string in [modified UTF-8](../java/io/DataInput.md) format has been read in a data input stream or by any class that implements the data input interface. |
| [WriteAbortedException](../java/io/WriteAbortedException.md) | Signals that one of the ObjectStreamExceptions was thrown during a write operation. |

## Annotations

| [Serial](../java/io/Serial.md) | Indicates that an annotated field or method is part of the [serialization mechanism](../java/io/Serializable.md) defined by the Java Object Serialization Specification. |
| --- | --- |
