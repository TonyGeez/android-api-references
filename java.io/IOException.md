Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IOException

```
open class IOException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException#) |

Known Direct Subclasses [Base64DataException](https://developer.android.com/reference/kotlin/android/util/Base64DataException.html#), [BluetoothSocketException](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException.html#), [CharConversionException](https://developer.android.com/reference/kotlin/java/io/CharConversionException), [CharacterCodingException](https://developer.android.com/reference/kotlin/java/nio/charset/CharacterCodingException.html#), [ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException.html#), [EOFException](https://developer.android.com/reference/kotlin/java/io/EOFException), [FileLockInterruptionException](https://developer.android.com/reference/kotlin/java/nio/channels/FileLockInterruptionException.html#), [FileNotFoundException](https://developer.android.com/reference/kotlin/java/io/FileNotFoundException), [FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException.html#), [HttpException](https://developer.android.com/reference/kotlin/android/net/http/HttpException.html#), [HttpRetryException](https://developer.android.com/reference/kotlin/java/net/HttpRetryException.html#), [IkeTimeoutException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeTimeoutException.html#), and 22 others. [Base64DataException](https://developer.android.com/reference/kotlin/android/util/Base64DataException.html#) This exception is thrown by `https://developer.android.com/reference/kotlin/android/util/Base64InputStream.html#` or `https://developer.android.com/reference/kotlin/android/util/Base64OutputStream.html#` when an error is detected in the data being decoded.
[BluetoothSocketException](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException.html#) Thrown when an error occurs during a Bluetooth Socket related exception.
[CharConversionException](https://developer.android.com/reference/kotlin/java/io/CharConversionException) Base class for character conversion exceptions.
[CharacterCodingException](https://developer.android.com/reference/kotlin/java/nio/charset/CharacterCodingException.html#) Checked exception thrown when a character encoding or decoding error occurs.
[ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException.html#) Checked exception thrown when an attempt is made to invoke or complete an I/O operation upon channel that is closed, or at least closed to that operation.
[EOFException](https://developer.android.com/reference/kotlin/java/io/EOFException) Signals that an end of file or end of stream has been reached unexpectedly during input.
[FileLockInterruptionException](https://developer.android.com/reference/kotlin/java/nio/channels/FileLockInterruptionException.html#) Checked exception received by a thread when another thread interrupts it while it is waiting to acquire a file lock.
[FileNotFoundException](https://developer.android.com/reference/kotlin/java/io/FileNotFoundException) Signals that an attempt to open the file denoted by a specified pathname has failed.
[FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException.html#) Thrown when a file system operation fails on one or two files.
[HttpException](https://developer.android.com/reference/kotlin/android/net/http/HttpException.html#) Base exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)`.
[HttpRetryException](https://developer.android.com/reference/kotlin/java/net/HttpRetryException.html#) Thrown to indicate that a HTTP request needs to be retried but cannot be retried automatically, due to streaming mode being enabled.
[IkeTimeoutException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeTimeoutException.html#) This exception is thrown when there is an IKE retransmission timeout.
[ImageDecoder.DecodeException](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.DecodeException.html#) Information about an interrupted decode.
[InterruptedByTimeoutException](https://developer.android.com/reference/kotlin/java/nio/channels/InterruptedByTimeoutException.html#) Checked exception received by a thread when a timeout elapses before an asynchronous operation completes.
[InterruptedIOException](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException) Signals that an I/O operation has been interrupted.
[InvalidPropertiesFormatException](https://developer.android.com/reference/kotlin/java/util/InvalidPropertiesFormatException.html#) Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of properties, as per the `https://developer.android.com/reference/kotlin/java/util/Properties.html#` specification.
[MalformedJsonException](https://developer.android.com/reference/kotlin/android/util/MalformedJsonException.html#) Thrown when a reader encounters malformed JSON.
[MalformedURLException](https://developer.android.com/reference/kotlin/java/net/MalformedURLException.html#) Thrown to indicate that a malformed URL has occurred.
[MediaParser.ParsingException](https://developer.android.com/reference/kotlin/android/media/MediaParser.ParsingException.html#) Thrown when an error occurs while parsing a media stream.
[MediaParser.UnrecognizedInputFormatException](https://developer.android.com/reference/kotlin/android/media/MediaParser.UnrecognizedInputFormatException.html#) Thrown if all parser implementations provided to `https://developer.android.com/reference/kotlin/android/media/MediaParser.html#create(android.media.MediaParser.OutputConsumer,%20kotlin.String)` failed to sniff the input content.
[ObjectStreamException](https://developer.android.com/reference/kotlin/java/io/ObjectStreamException) Superclass of all exceptions specific to Object Stream classes.
[ParcelFileDescriptor.FileDescriptorDetachedException](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.FileDescriptorDetachedException.html#) Exception that indicates that the file descriptor was detached.
[ProtocolException](https://developer.android.com/reference/kotlin/java/net/ProtocolException.html#) Thrown to indicate that there is an error in the underlying protocol, such as a TCP error.
[SSLException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLException.html#) Indicates some kind of error detected by an SSL subsystem.
[SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException.html#) Thrown to indicate that there is an error creating or accessing a Socket.
[SyncFailedException](https://developer.android.com/reference/kotlin/java/io/SyncFailedException) Signals that a sync operation has failed.
[TagLostException](https://developer.android.com/reference/kotlin/android/nfc/TagLostException.html#) <br />

[UTFDataFormatException](https://developer.android.com/reference/kotlin/java/io/UTFDataFormatException) Signals that a malformed string in [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) format has been read in a data input stream or by any class that implements the data input interface.
[UnknownHostException](https://developer.android.com/reference/kotlin/java/net/UnknownHostException.html#) Thrown to indicate that the IP address of a host could not be determined.
[UnknownServiceException](https://developer.android.com/reference/kotlin/java/net/UnknownServiceException.html#) Thrown to indicate that an unknown service exception has occurred.
[UnsupportedEncodingException](https://developer.android.com/reference/kotlin/java/io/UnsupportedEncodingException) The Character Encoding is not supported.
[UserPrincipalNotFoundException](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalNotFoundException.html#) Checked exception thrown when a lookup of `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal.html#` fails because the principal does not exist.
[VibrationEffect.VibrationParseException](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.VibrationParseException.html#) Exception thrown when parsing a vibration XML fails due to invalid format or values.
[ZipException](https://developer.android.com/reference/kotlin/java/util/zip/ZipException.html#) Signals that a Zip exception of some sort has occurred.
Known Indirect Subclasses [AccessDeniedException](https://developer.android.com/reference/kotlin/java/nio/file/AccessDeniedException.html#), [AsynchronousCloseException](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousCloseException.html#), [AtomicMoveNotSupportedException](https://developer.android.com/reference/kotlin/java/nio/file/AtomicMoveNotSupportedException.html#), [BindException](https://developer.android.com/reference/kotlin/java/net/BindException.html#), [CallbackException](https://developer.android.com/reference/kotlin/android/net/http/CallbackException.html#), [ClosedByInterruptException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedByInterruptException.html#), [ConnectException](https://developer.android.com/reference/kotlin/java/net/ConnectException.html#), [ConnectTimeoutException](https://developer.android.com/reference/kotlin/org/apache/http/conn/ConnectTimeoutException.html#), [DirectoryNotEmptyException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryNotEmptyException.html#), [EchConfigMismatchException](https://developer.android.com/reference/kotlin/android/net/ssl/EchConfigMismatchException.html#), [FileAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileAlreadyExistsException.html#), [FileSystemLoopException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemLoopException.html#), and 23 others. [AccessDeniedException](https://developer.android.com/reference/kotlin/java/nio/file/AccessDeniedException.html#) Checked exception thrown when a file system operation is denied, typically due to a file permission or other access check.
[AsynchronousCloseException](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousCloseException.html#) Checked exception received by a thread when another thread closes the channel or the part of the channel upon which it is blocked in an I/O operation.
[AtomicMoveNotSupportedException](https://developer.android.com/reference/kotlin/java/nio/file/AtomicMoveNotSupportedException.html#) Checked exception thrown when a file cannot be moved as an atomic file system operation.
[BindException](https://developer.android.com/reference/kotlin/java/net/BindException.html#) Signals that an error occurred while attempting to bind a socket to a local address and port.
[CallbackException](https://developer.android.com/reference/kotlin/android/net/http/CallbackException.html#) Exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` when `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#` or `https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider.html#` method throws an exception.
[ClosedByInterruptException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedByInterruptException.html#) Checked exception received by a thread when another thread interrupts it while it is blocked in an I/O operation upon a channel.
[ConnectException](https://developer.android.com/reference/kotlin/java/net/ConnectException.html#) Signals that an error occurred while attempting to connect a socket to a remote address and port.
[ConnectTimeoutException](https://developer.android.com/reference/kotlin/org/apache/http/conn/ConnectTimeoutException.html#) A timeout while connecting to an HTTP server or waiting for an available connection from an HttpConnectionManager.
[DirectoryNotEmptyException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryNotEmptyException.html#) Checked exception thrown when a file system operation fails because a directory is not empty.
[EchConfigMismatchException](https://developer.android.com/reference/kotlin/android/net/ssl/EchConfigMismatchException.html#) Exception thrown when the provided ECH (Encrypted Client Hello) config does not match the server.
[FileAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileAlreadyExistsException.html#) Checked exception thrown when an attempt is made to create a file or directory and a file of that name already exists.
[FileSystemLoopException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemLoopException.html#) Checked exception thrown when a file system loop, or cycle, is encountered.
[InvalidClassException](https://developer.android.com/reference/kotlin/java/io/InvalidClassException) Thrown when the Serialization runtime detects one of the following problems with a Class.
[InvalidEchDataException](https://developer.android.com/reference/kotlin/android/net/ssl/InvalidEchDataException.html#) Exception thrown when the ECH (Encrypted Client Hello) data is empty or invalid.
[InvalidObjectException](https://developer.android.com/reference/kotlin/java/io/InvalidObjectException) Indicates that one or more deserialized objects failed validation tests.
[JarException](https://developer.android.com/reference/kotlin/java/util/jar/JarException.html#) Signals that an error of some sort has occurred while reading from or writing to a JAR file.
[MalformedInputException](https://developer.android.com/reference/kotlin/java/nio/charset/MalformedInputException.html#) Checked exception thrown when an input byte sequence is not legal for given charset, or an input character sequence is not a legal sixteen-bit Unicode sequence.
[NetworkException](https://developer.android.com/reference/kotlin/android/net/http/NetworkException.html#) Exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` when the HTTP stack fails to process a network request.
[NoRouteToHostException](https://developer.android.com/reference/kotlin/java/net/NoRouteToHostException.html#) Signals that an error occurred while attempting to connect a socket to a remote address and port.
[NoSuchFileException](https://developer.android.com/reference/kotlin/java/nio/file/NoSuchFileException.html#) Checked exception thrown when an attempt is made to access a file that does not exist.
[NotActiveException](https://developer.android.com/reference/kotlin/java/io/NotActiveException) Thrown when serialization or deserialization is not active.
[NotDirectoryException](https://developer.android.com/reference/kotlin/java/nio/file/NotDirectoryException.html#) Checked exception thrown when a file system operation, intended for a directory, fails because the file is not a directory.
[NotLinkException](https://developer.android.com/reference/kotlin/java/nio/file/NotLinkException.html#) Checked exception thrown when a file system operation fails because a file is not a symbolic link.
[NotSerializableException](https://developer.android.com/reference/kotlin/java/io/NotSerializableException) Thrown when an instance is required to have a Serializable interface.
[OptionalDataException](https://developer.android.com/reference/kotlin/java/io/OptionalDataException) Exception indicating the failure of an object read operation due to unread primitive data, or the end of data belonging to a serialized object in the stream.
[PortUnreachableException](https://developer.android.com/reference/kotlin/java/net/PortUnreachableException.html#) Signals that an ICMP Port Unreachable message has been received on a connected datagram.
[QuicException](https://developer.android.com/reference/kotlin/android/net/http/QuicException.html#) Subclass of `https://developer.android.com/reference/kotlin/android/net/http/NetworkException.html#` which contains a detailed [QUIC](https://www.chromium.org/quic) error code from [QuicErrorCode](https://cs.chromium.org/search/?q=symbol:%5CbQuicErrorCode%5Cb).
[SSLHandshakeException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLHandshakeException.html#) Indicates that the client and server could not negotiate the desired level of security.
[SSLKeyException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLKeyException.html#) Reports a bad SSL key.
[SSLPeerUnverifiedException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPeerUnverifiedException.html#) Indicates that the peer's identity has not been verified.
[SSLProtocolException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLProtocolException.html#) Reports an error in the operation of the SSL protocol.
[SocketTimeoutException](https://developer.android.com/reference/kotlin/java/net/SocketTimeoutException.html#) Signals that a timeout has occurred on a socket read or accept.
[StreamCorruptedException](https://developer.android.com/reference/kotlin/java/io/StreamCorruptedException) Thrown when control information that was read from an object stream violates internal consistency checks.
[UnmappableCharacterException](https://developer.android.com/reference/kotlin/java/nio/charset/UnmappableCharacterException.html#) Checked exception thrown when an input character (or byte) sequence is valid but cannot be mapped to an output byte (or character) sequence.
[WriteAbortedException](https://developer.android.com/reference/kotlin/java/io/WriteAbortedException) Signals that one of the ObjectStreamExceptions was thrown during a write operation.

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
