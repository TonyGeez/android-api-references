Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IOException

```
open class IOException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [java.io.IOException](IOException.md) |
| --- | --- | --- | --- |

Known Direct Subclasses [Base64DataException](../android.util/Base64DataException.md), [BluetoothSocketException](../android.bluetooth/BluetoothSocketException.md), [CharConversionException](CharConversionException.md), [CharacterCodingException](../java.nio.charset/CharacterCodingException.md), [ClosedChannelException](../java.nio.channels/ClosedChannelException.md), [EOFException](EOFException.md), [FileLockInterruptionException](../java.nio.channels/FileLockInterruptionException.md), [FileNotFoundException](FileNotFoundException.md), [FileSystemException](../java.nio.file/FileSystemException.md), [HttpException](../android.net.http/HttpException.md), [HttpRetryException](../java.net/HttpRetryException.md), [IkeTimeoutException](../android.net.ipsec.ike.exceptions/IkeTimeoutException.md), and 22 others. [Base64DataException](../android.util/Base64DataException.md) This exception is thrown by `https://developer.android.com/reference/kotlin/android/util/Base64InputStream.html#` or `https://developer.android.com/reference/kotlin/android/util/Base64OutputStream.html#` when an error is detected in the data being decoded.
[BluetoothSocketException](../android.bluetooth/BluetoothSocketException.md) Thrown when an error occurs during a Bluetooth Socket related exception.
[CharConversionException](CharConversionException.md) Base class for character conversion exceptions.
[CharacterCodingException](../java.nio.charset/CharacterCodingException.md) Checked exception thrown when a character encoding or decoding error occurs.
[ClosedChannelException](../java.nio.channels/ClosedChannelException.md) Checked exception thrown when an attempt is made to invoke or complete an I/O operation upon channel that is closed, or at least closed to that operation.
[EOFException](EOFException.md) Signals that an end of file or end of stream has been reached unexpectedly during input.
[FileLockInterruptionException](../java.nio.channels/FileLockInterruptionException.md) Checked exception received by a thread when another thread interrupts it while it is waiting to acquire a file lock.
[FileNotFoundException](FileNotFoundException.md) Signals that an attempt to open the file denoted by a specified pathname has failed.
[FileSystemException](../java.nio.file/FileSystemException.md) Thrown when a file system operation fails on one or two files.
[HttpException](../android.net.http/HttpException.md) Base exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)`.
[HttpRetryException](../java.net/HttpRetryException.md) Thrown to indicate that a HTTP request needs to be retried but cannot be retried automatically, due to streaming mode being enabled.
[IkeTimeoutException](../android.net.ipsec.ike.exceptions/IkeTimeoutException.md) This exception is thrown when there is an IKE retransmission timeout.
[ImageDecoder.DecodeException](../android/graphics/ImageDecoder.DecodeException.md) Information about an interrupted decode.
[InterruptedByTimeoutException](../java.nio.channels/InterruptedByTimeoutException.md) Checked exception received by a thread when a timeout elapses before an asynchronous operation completes.
[InterruptedIOException](InterruptedIOException.md) Signals that an I/O operation has been interrupted.
[InvalidPropertiesFormatException](../java.util/InvalidPropertiesFormatException.md) Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of properties, as per the `https://developer.android.com/reference/kotlin/java/util/Properties.html#` specification.
[MalformedJsonException](../android.util/MalformedJsonException.md) Thrown when a reader encounters malformed JSON.
[MalformedURLException](../java.net/MalformedURLException.md) Thrown to indicate that a malformed URL has occurred.
[MediaParser.ParsingException](../android/media/MediaParser.ParsingException.md) Thrown when an error occurs while parsing a media stream.
[MediaParser.UnrecognizedInputFormatException](../android/media/MediaParser.UnrecognizedInputFormatException.md) Thrown if all parser implementations provided to `https://developer.android.com/reference/kotlin/android/media/MediaParser.html#create(android.media.MediaParser.OutputConsumer,%20kotlin.String)` failed to sniff the input content.
[ObjectStreamException](ObjectStreamException.md) Superclass of all exceptions specific to Object Stream classes.
[ParcelFileDescriptor.FileDescriptorDetachedException](../android/os/ParcelFileDescriptor.FileDescriptorDetachedException.md) Exception that indicates that the file descriptor was detached.
[ProtocolException](../java.net/ProtocolException.md) Thrown to indicate that there is an error in the underlying protocol, such as a TCP error.
[SSLException](../javax.net.ssl/SSLException.md) Indicates some kind of error detected by an SSL subsystem.
[SocketException](../java.net/SocketException.md) Thrown to indicate that there is an error creating or accessing a Socket.
[SyncFailedException](SyncFailedException.md) Signals that a sync operation has failed.
[TagLostException](../android.nfc/TagLostException.md) <br />

[UTFDataFormatException](UTFDataFormatException.md) Signals that a malformed string in [modified UTF-8](DataInput.md) format has been read in a data input stream or by any class that implements the data input interface.
[UnknownHostException](../java.net/UnknownHostException.md) Thrown to indicate that the IP address of a host could not be determined.
[UnknownServiceException](../java.net/UnknownServiceException.md) Thrown to indicate that an unknown service exception has occurred.
[UnsupportedEncodingException](UnsupportedEncodingException.md) The Character Encoding is not supported.
[UserPrincipalNotFoundException](../java.nio.file.attribute/UserPrincipalNotFoundException.md) Checked exception thrown when a lookup of `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal.html#` fails because the principal does not exist.
[VibrationEffect.VibrationParseException](../android/os/VibrationEffect.VibrationParseException.md) Exception thrown when parsing a vibration XML fails due to invalid format or values.
[ZipException](../java.util.zip/ZipException.md) Signals that a Zip exception of some sort has occurred.
Known Indirect Subclasses [AccessDeniedException](../java.nio.file/AccessDeniedException.md), [AsynchronousCloseException](../java.nio.channels/AsynchronousCloseException.md), [AtomicMoveNotSupportedException](../java.nio.file/AtomicMoveNotSupportedException.md), [BindException](../java.net/BindException.md), [CallbackException](../android.net.http/CallbackException.md), [ClosedByInterruptException](../java.nio.channels/ClosedByInterruptException.md), [ConnectException](../java.net/ConnectException.md), [ConnectTimeoutException](../org.apache.http.conn/ConnectTimeoutException.md), [DirectoryNotEmptyException](../java.nio.file/DirectoryNotEmptyException.md), [EchConfigMismatchException](../android/net/ssl/EchConfigMismatchException.md), [FileAlreadyExistsException](../java.nio.file/FileAlreadyExistsException.md), [FileSystemLoopException](../java.nio.file/FileSystemLoopException.md), and 23 others. [AccessDeniedException](../java.nio.file/AccessDeniedException.md) Checked exception thrown when a file system operation is denied, typically due to a file permission or other access check.
[AsynchronousCloseException](../java.nio.channels/AsynchronousCloseException.md) Checked exception received by a thread when another thread closes the channel or the part of the channel upon which it is blocked in an I/O operation.
[AtomicMoveNotSupportedException](../java.nio.file/AtomicMoveNotSupportedException.md) Checked exception thrown when a file cannot be moved as an atomic file system operation.
[BindException](../java.net/BindException.md) Signals that an error occurred while attempting to bind a socket to a local address and port.
[CallbackException](../android.net.http/CallbackException.md) Exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` when `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#` or `https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider.html#` method throws an exception.
[ClosedByInterruptException](../java.nio.channels/ClosedByInterruptException.md) Checked exception received by a thread when another thread interrupts it while it is blocked in an I/O operation upon a channel.
[ConnectException](../java.net/ConnectException.md) Signals that an error occurred while attempting to connect a socket to a remote address and port.
[ConnectTimeoutException](../org.apache.http.conn/ConnectTimeoutException.md) A timeout while connecting to an HTTP server or waiting for an available connection from an HttpConnectionManager.
[DirectoryNotEmptyException](../java.nio.file/DirectoryNotEmptyException.md) Checked exception thrown when a file system operation fails because a directory is not empty.
[EchConfigMismatchException](../android/net/ssl/EchConfigMismatchException.md) Exception thrown when the provided ECH (Encrypted Client Hello) config does not match the server.
[FileAlreadyExistsException](../java.nio.file/FileAlreadyExistsException.md) Checked exception thrown when an attempt is made to create a file or directory and a file of that name already exists.
[FileSystemLoopException](../java.nio.file/FileSystemLoopException.md) Checked exception thrown when a file system loop, or cycle, is encountered.
[InvalidClassException](InvalidClassException.md) Thrown when the Serialization runtime detects one of the following problems with a Class.
[InvalidEchDataException](../android/net/ssl/InvalidEchDataException.md) Exception thrown when the ECH (Encrypted Client Hello) data is empty or invalid.
[InvalidObjectException](InvalidObjectException.md) Indicates that one or more deserialized objects failed validation tests.
[JarException](../java.util.jar/JarException.md) Signals that an error of some sort has occurred while reading from or writing to a JAR file.
[MalformedInputException](../java.nio.charset/MalformedInputException.md) Checked exception thrown when an input byte sequence is not legal for given charset, or an input character sequence is not a legal sixteen-bit Unicode sequence.
[NetworkException](../android.net.http/NetworkException.md) Exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` when the HTTP stack fails to process a network request.
[NoRouteToHostException](../java.net/NoRouteToHostException.md) Signals that an error occurred while attempting to connect a socket to a remote address and port.
[NoSuchFileException](../java.nio.file/NoSuchFileException.md) Checked exception thrown when an attempt is made to access a file that does not exist.
[NotActiveException](NotActiveException.md) Thrown when serialization or deserialization is not active.
[NotDirectoryException](../java.nio.file/NotDirectoryException.md) Checked exception thrown when a file system operation, intended for a directory, fails because the file is not a directory.
[NotLinkException](../java.nio.file/NotLinkException.md) Checked exception thrown when a file system operation fails because a file is not a symbolic link.
[NotSerializableException](NotSerializableException.md) Thrown when an instance is required to have a Serializable interface.
[OptionalDataException](OptionalDataException.md) Exception indicating the failure of an object read operation due to unread primitive data, or the end of data belonging to a serialized object in the stream.
[PortUnreachableException](../java.net/PortUnreachableException.md) Signals that an ICMP Port Unreachable message has been received on a connected datagram.
[QuicException](../android.net.http/QuicException.md) Subclass of `https://developer.android.com/reference/kotlin/android/net/http/NetworkException.html#` which contains a detailed [QUIC](https://www.chromium.org/quic) error code from [QuicErrorCode](https://cs.chromium.org/search/?q=symbol:%5CbQuicErrorCode%5Cb).
[SSLHandshakeException](../javax.net.ssl/SSLHandshakeException.md) Indicates that the client and server could not negotiate the desired level of security.
[SSLKeyException](../javax.net.ssl/SSLKeyException.md) Reports a bad SSL key.
[SSLPeerUnverifiedException](../javax.net.ssl/SSLPeerUnverifiedException.md) Indicates that the peer's identity has not been verified.
[SSLProtocolException](../javax.net.ssl/SSLProtocolException.md) Reports an error in the operation of the SSL protocol.
[SocketTimeoutException](../java.net/SocketTimeoutException.md) Signals that a timeout has occurred on a socket read or accept.
[StreamCorruptedException](StreamCorruptedException.md) Thrown when control information that was read from an object stream violates internal consistency checks.
[UnmappableCharacterException](../java.nio.charset/UnmappableCharacterException.md) Checked exception thrown when an input character (or byte) sequence is valid but cannot be mapped to an output byte (or character) sequence.
[WriteAbortedException](WriteAbortedException.md) Signals that one of the ObjectStreamExceptions was thrown during a write operation.

Signals that an I/O exception of some sort has occurred. This class is the general class of exceptions produced by failed or interrupted I/O operations.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/IOException#IOException()()` Constructs an `IOException` with `null` as its error detail message. |
| `https://developer.android.com/reference/kotlin/java/io/IOException#IOException(kotlin.String)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructs an `IOException` with the specified detail message. |
| `https://developer.android.com/reference/kotlin/java/io/IOException#IOException(kotlin.String,%20kotlin.Throwable)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Constructs an `IOException` with the specified detail message and cause. |
| `https://developer.android.com/reference/kotlin/java/io/IOException#IOException(kotlin.Throwable)(cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Constructs an `IOException` with the specified cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`). |

## Public constructors

### IOException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IOException()
```

Constructs an `IOException` with `null` as its error detail message.

### IOException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IOException(message: String!)
```

Constructs an `IOException` with the specified detail message.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The detail message (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage()` method) |

### IOException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IOException(
    message: String!, 
    cause: Throwable!)
```

Constructs an `IOException` with the specified detail message and cause.

Note that the detail message associated with `cause` is *not* automatically incorporated into this exception's detail message.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The detail message (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage()` method) |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: The cause (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()` method). (A null value is permitted, and indicates that the cause is nonexistent or unknown.) |

### IOException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IOException(cause: Throwable!)
```

Constructs an `IOException` with the specified cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`). This constructor is useful for IO exceptions that are little more than wrappers for other throwables.

| Parameters ||
|---|---|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: The cause (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()` method). (A null value is permitted, and indicates that the cause is nonexistent or unknown.) |
