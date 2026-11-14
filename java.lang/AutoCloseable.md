Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AutoCloseable

```
interface AutoCloseable
```

| [java.lang.AutoCloseable](../java/lang/AutoCloseable.md) |

Known Direct Subclasses [AppInteractionSession](../android/app/AppInteractionSession.md), [AssetManager](../android/content/res/AssetManager.md), [BaseStream](../java/util/stream/BaseStream.md), [BluetoothCsipSetCoordinator](../android/bluetooth/BluetoothCsipSetCoordinator.md), [BluetoothLeAudio](../android/bluetooth/BluetoothLeAudio.md), [BundleSession](../android/media/metrics/BundleSession.md), [CameraCaptureSession](../android/hardware/camera2/CameraCaptureSession.md), [CameraDevice](../android/hardware/camera2/CameraDevice.md), [CameraExtensionSession](../android/hardware/camera2/CameraExtensionSession.md), [Closeable](../java/io/Closeable.md), [Connection](../java/sql/Connection.md), [ContentCaptureSession](../android/view/contentcapture/ContentCaptureSession.md), and 62 others. [AppInteractionSession](../android/app/AppInteractionSession.md) Represents an app interaction session.
[AssetManager](../android/content/res/AssetManager.md) Provides access to an application's raw asset files; see `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` for the way most applications will want to retrieve their resource data.
[BaseStream](../java/util/stream/BaseStream.md) Base interface for streams, which are sequences of elements supporting sequential and parallel aggregate operations.
[BluetoothCsipSetCoordinator](../android/bluetooth/BluetoothCsipSetCoordinator.md) This class provides the public APIs to control the Bluetooth CSIP set coordinator.
[BluetoothLeAudio](../android/bluetooth/BluetoothLeAudio.md) This class provides the public APIs to control the LeAudio profile.
[BundleSession](../android/media/metrics/BundleSession.md) An instance of this class represents a session with data stored in a bundle.
[CameraCaptureSession](../android/hardware/camera2/CameraCaptureSession.md) A configured capture session for a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#`, used for capturing images from the camera or reprocessing images captured from the camera in the same session previously.
[CameraDevice](../android/hardware/camera2/CameraDevice.md) The CameraDevice class is a representation of a single camera connected to an Android device, allowing for fine-grain control of image capture and post-processing at high frame rates.
[CameraExtensionSession](../android/hardware/camera2/CameraExtensionSession.md) A camera capture session that enables access to device-specific camera extensions, which often use multi-frame bursts and sophisticated post-process algorithms for image capture.
[Closeable](../java/io/Closeable.md) A `Closeable` is a source or destination of data that can be closed.
[Connection](../java/sql/Connection.md) A connection (session) with a specific database.
[ContentCaptureSession](../android/view/contentcapture/ContentCaptureSession.md) Session used when notifying the Android system about events associated with views.
[ContentProviderClient](../android/content/ContentProviderClient.md) The public interface object used to interact with a specific `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`.
[DiscoverySession](../android/net/wifi/aware/DiscoverySession.md) A class representing a single publish or subscribe Aware session.
[DngCreator](../android/hardware/camera2/DngCreator.md) The `https://developer.android.com/reference/kotlin/android/hardware/camera2/DngCreator.html#` class provides functions to write raw pixel data as a DNG file.
[DrmManagerClient](../android/drm/DrmManagerClient.md) The main programming interface for the DRM framework.
[EditingSession](../android/media/metrics/EditingSession.md) Represents a session of media editing, for example, transcoding between formats, transmuxing or applying trimming or audio/video effects to a stream.
[ExecutorService](../java/util/concurrent/ExecutorService.md) An `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that provides methods to manage termination and methods that can produce a `https://developer.android.com/reference/kotlin/java/util/concurrent/Future.html#` for tracking progress of one or more asynchronous tasks.
[FileLock](../java/nio/channels/FileLock.md) A token representing a lock on a region of a file.
[GroupCall](../android/telephony/mbms/GroupCall.md) Class used to represent a single MBMS group call.
[HapticGenerator](../android/media/audiofx/HapticGenerator.md) Haptic Generator(HG).
[HardwareBuffer](../android/hardware/HardwareBuffer.md) HardwareBuffer wraps a native `AHardwareBuffer` object, which is a low-level object representing a memory buffer accessible by various hardware units.
[HardwareBufferRenderer](../android/graphics/HardwareBufferRenderer.md) Creates an instance of a hardware-accelerated renderer.
[HidDevice](../android/hardware/hid/HidDevice.md) Represents a Human Interface Device (HID) connected to the system.
[IkeSession](../android/net/ipsec/ike/IkeSession.md) This class represents an IKE Session management object that allows for keying and management of `https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#`s.
[Image](../android/media/Image.md) A single complete image buffer to use with a media source such as a `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#` or a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#`.
[ImageDecoder](../android/graphics/ImageDecoder.md) A class for converting encoded images (like `PNG`, `JPEG`, `WEBP`, `GIF`, or `HEIF`) into `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` objects.
[ImageReader](../android/media/ImageReader.md) The ImageReader class allows direct application access to image data rendered into a `https://developer.android.com/reference/kotlin/android/view/Surface.html#`
[ImageWriter](../android/media/ImageWriter.md) The ImageWriter class allows an application to produce Image data into a `https://developer.android.com/reference/kotlin/android/view/Surface.html#`, and have it be consumed by another component like `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#`.
[IpSecManager.SecurityParameterIndex](../android/net/IpSecManager.SecurityParameterIndex.md) This class represents a reserved SPI.
[IpSecManager.UdpEncapsulationSocket](../android/net/IpSecManager.UdpEncapsulationSocket.md) This class provides access to a UDP encapsulation Socket.
[IpSecTransform](../android/net/IpSecTransform.md) This class represents a transform, which roughly corresponds to an IPsec Security Association.
[LightsManager.LightsSession](../android/hardware/lights/LightsManager.LightsSession.md) Encapsulates a session that can be used to control device lights and represents the lifetime of the requests.
[LocationButtonSession](../android/app/permissionui/LocationButtonSession.md) This interface defines location button session, and allows apps to change/customize the appearance of the button.
[LoudnessCodecController](../android/media/LoudnessCodecController.md) Class for getting recommended loudness parameter updates for audio decoders as they are used to play back media content according to the encoded format and current audio routing.
[MbmsDownloadSession](../android/telephony/MbmsDownloadSession.md) This class provides functionality for file download over MBMS.
[MbmsGroupCallSession](../android/telephony/MbmsGroupCallSession.md) This class provides functionality for accessing group call functionality over MBMS.
[MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md) This class provides functionality for streaming media over MBMS.
[MediaCas](../android/media/MediaCas.md) MediaCas can be used to obtain keys for descrambling protected media streams, in conjunction with `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler.html#`.
[MediaCas.Session](../android/media/MediaCas.Session.md) Class for an open session with the CA system.
[MediaController2](../android/media/MediaController2.md) This API is not generally intended for third party application developers.
[MediaDescrambler](../android/media/MediaDescrambler.md) MediaDescrambler class can be used in conjunction with `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#` and `https://developer.android.com/reference/kotlin/android/media/MediaExtractor.html#` to decode media data scrambled by conditional access (CA) systems such as those in the ISO/IEC13818-1.
[MediaDrm](../android/media/MediaDrm.md) MediaDrm can be used to obtain keys for decrypting protected media streams, in conjunction with `https://developer.android.com/reference/kotlin/android/media/MediaCrypto.html#`.
[MediaMetadataRetriever](../android/media/MediaMetadataRetriever.md) MediaMetadataRetriever class provides a unified interface for retrieving frame and meta data from an input media file.
[MediaSession2](../android/media/MediaSession2.md) This API is not generally intended for third party application developers.
[MultiResolutionImageReader](../android/hardware/camera2/MultiResolutionImageReader.md) The MultiResolutionImageReader class wraps a group of `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` with the same format and different sizes, source camera Id, or camera sensor modes.
[NetworkStats](../android/app/usage/NetworkStats.md) Class providing enumeration over buckets of network usage statistics.
[ObjectInput](../java/io/ObjectInput.md) ObjectInput extends the DataInput interface to include the reading of objects.
[ObjectOutput](../java/io/ObjectOutput.md) ObjectOutput extends the DataOutput interface to include writing of objects.
[PdfRenderer](../android/graphics/pdf/PdfRenderer.md) This class enables rendering a PDF document and selecting, searching, fast scrolling, annotations, etc.
[PdfRenderer.Page](../android/graphics/pdf/PdfRenderer.Page.md) This class represents a PDF document page for rendering.
[PdfRendererPreV](../android/graphics/pdf/PdfRendererPreV.md) This class enables rendering a PDF document and selecting, searching, fast scrolling, annotations, etc from Android R till Android U.
[PdfRendererPreV.Page](../android/graphics/pdf/PdfRendererPreV.Page.md) This class represents a PDF document page for rendering.
[PlaybackSession](../android/media/metrics/PlaybackSession.md) An instance of this class represents a session of media playback used to report playback metrics and events.
[Proxy.HttpConnectCallback.Request](../android/net/http/Proxy.HttpConnectCallback.Request.md) Represents an HTTP CONNECT request being sent to the proxy server.
[RangingSession](../android/ranging/RangingSession.md) Represents a session for performing ranging operations.
[RecordingSession](../android/media/metrics/RecordingSession.md) An instances of this class represents a session of media recording.
[ResourcesProvider](../android/content/res/loader/ResourcesProvider.md) Provides methods to load resources data from APKs (`.apk`) and resources tables (eg.
[ResultSet](../java/sql/ResultSet.md) A table of data representing a database result set, which is usually generated by executing a statement that queries the database.
[SQLiteOpenHelper](../android/database/sqlite/SQLiteOpenHelper.md) A helper class to manage database creation and version management.
[SettingsPreferenceServiceClient](../android/service/settings/preferences/SettingsPreferenceServiceClient.md) Client class responsible for binding to and interacting with an instance of `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceService.html#`.
[SocketKeepalive](../android/net/SocketKeepalive.md) Allows applications to request that the system periodically send specific packets on their behalf, using hardware offload to save battery power.
[Statement](../java/sql/Statement.md) The object used for executing a static SQL statement and returning the results it produces.
[StreamingService](../android/telephony/mbms/StreamingService.md) Class used to represent a single MBMS stream.
[SubmissionPublisher](../java/util/concurrent/SubmissionPublisher.md) A `https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Publisher.html#` that asynchronously issues submitted (non-null) items to current subscribers until it is closed.
[SyncFence](../android/hardware/SyncFence.md) A SyncFence represents a synchronization primitive which signals when hardware units have completed work on a particular resource.
[TranscodingSession](../android/media/metrics/TranscodingSession.md) An instances of this class represents a session of media Transcoding.
[TransportHandle](../android/ranging/oob/TransportHandle.md) TransportHandle is used as the Out-Of-Band (OOB) transport mechanism by ranging module.
[TypedArray](../android/content/res/TypedArray.md) Container for an array of values that were retrieved with `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#obtainAttributes(android.util.AttributeSet,%20kotlin.IntArray)`.
[VolumeShaper](../android/media/VolumeShaper.md) The `VolumeShaper` class is used to automatically control audio volume during media playback, allowing simple implementation of transition effects and ducking.
[WifiAwareSession](../android/net/wifi/aware/WifiAwareSession.md) This class represents a Wi-Fi Aware session - an attachment to the Wi-Fi Aware service through which the app can execute discovery operations.
[WifiManager.LocalOnlyHotspotReservation](../android/net/wifi/WifiManager.LocalOnlyHotspotReservation.md) LocalOnlyHotspotReservation that contains the `https://developer.android.com/reference/kotlin/android/net/wifi/SoftApConfiguration.html#` for the active LocalOnlyHotspot request.
[WifiP2pManager.Channel](../android/net/wifi/p2p/WifiP2pManager.Channel.md) A channel that connects the application to the Wifi p2p framework.
[XmlResourceParser](../android/content/res/XmlResourceParser.md) The XML parsing interface returned for an XML resource.
Known Indirect Subclasses [AbstractCursor](../android/database/AbstractCursor.md), [AbstractExecutorService](../java/util/concurrent/AbstractExecutorService.md), [AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md), [AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md), [AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md), [AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md), [AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md), [AbstractSelector](../java/nio/channels/spi/AbstractSelector.md), [AbstractWindowedCursor](../android/database/AbstractWindowedCursor.md), [AppSearchSession](../android/app/appsearch/AppSearchSession.md), [AssetFileDescriptor](../android/content/res/AssetFileDescriptor.md), [AssetFileDescriptor.AutoCloseInputStream](../android/content/res/AssetFileDescriptor.AutoCloseInputStream.md), and 211 others. [AbstractCursor](../android/database/AbstractCursor.md) This is an abstract cursor class that handles a lot of the common code that all cursors need to deal with and is provided for convenience reasons.
[AbstractExecutorService](../java/util/concurrent/AbstractExecutorService.md) Provides default implementations of `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#` execution methods.
[AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md) Base implementation class for interruptible channels.
[AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md) Base implementation class for interruptible channels.
[AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md) Base implementation class for selectable channels.
[AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md) Base implementation class for selectable channels.
[AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md) Base implementation class for selectable channels.
[AbstractSelector](../java/nio/channels/spi/AbstractSelector.md) Base implementation class for selectors.
[AbstractWindowedCursor](../android/database/AbstractWindowedCursor.md) A base class for Cursors that store their data in `https://developer.android.com/reference/kotlin/android/database/CursorWindow.html#`s.
[AppSearchSession](../android/app/appsearch/AppSearchSession.md) Provides a connection to a single AppSearch database.
[AssetFileDescriptor](../android/content/res/AssetFileDescriptor.md) File descriptor of an entry in the AssetManager.
[AssetFileDescriptor.AutoCloseInputStream](../android/content/res/AssetFileDescriptor.AutoCloseInputStream.md) An InputStream you can create on a ParcelFileDescriptor, which will take care of calling android.
[AssetFileDescriptor.AutoCloseOutputStream](../android/content/res/AssetFileDescriptor.AutoCloseOutputStream.md) An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android.
[AssetManager.AssetInputStream](../android/content/res/AssetManager.AssetInputStream.md) <br />

[AsynchronousByteChannel](../java/nio/channels/AsynchronousByteChannel.md) An asynchronous channel that can read and write bytes.
[AsynchronousChannel](../java/nio/channels/AsynchronousChannel.md) A channel that supports asynchronous I/O operations.
[AsynchronousFileChannel](../java/nio/channels/AsynchronousFileChannel.md) An asynchronous channel for reading, writing, and manipulating a file.
[AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md) An asynchronous channel for stream-oriented listening sockets.
[AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md) An asynchronous channel for stream-oriented listening sockets.
[AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md) An asynchronous channel for stream-oriented connecting sockets.
[AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md) An asynchronous channel for stream-oriented connecting sockets.
[BackupDataInputStream](../android/app/backup/BackupDataInputStream.md) Provides an `https://developer.android.com/reference/kotlin/java/io/InputStream.html#`-like interface for accessing an entity's data during a restore operation.
[Base64InputStream](../android/util/Base64InputStream.md) An InputStream that does Base64 decoding on the data read through it.
[Base64OutputStream](../android/util/Base64OutputStream.md) An OutputStream that does Base64 encoding on the data written to it, writing the resulting data to another OutputStream.
[BlobStoreManager.Session](../android/app/blob/BlobStoreManager.Session.md) Represents an ongoing session of a blob's contribution to the blob store managed by the system.
[BluetoothServerSocket](../android/bluetooth/BluetoothServerSocket.md) A listening Bluetooth socket.
[BluetoothSocket](../android/bluetooth/BluetoothSocket.md) A connected or connecting Bluetooth socket.
[BufferedInputStream](../java/io/BufferedInputStream.md) A `BufferedInputStream` adds functionality to another input stream-namely, the ability to buffer the input and to support the `mark` and `reset` methods.
[BufferedOutputStream](../java/io/BufferedOutputStream.md) The class implements a buffered output stream.
[BufferedReader](../java/io/BufferedReader.md) Reads text from a character-input stream, buffering characters so as to provide for the efficient reading of characters, arrays, and lines.
[BufferedWriter](../java/io/BufferedWriter.md) Writes text to a character-output stream, buffering characters so as to provide for the efficient writing of single characters, arrays, and strings.
[ByteArrayInputStream](../java/io/ByteArrayInputStream.md) A `ByteArrayInputStream` contains an internal buffer that contains bytes that may be read from the stream.
[ByteArrayOutputStream](../java/io/ByteArrayOutputStream.md) This class implements an output stream in which the data is written into a byte array.
[ByteChannel](../java/nio/channels/ByteChannel.md) A channel that can read and write bytes.
[ByteChannel](../java/nio/channels/ByteChannel.md) A channel that can read and write bytes.
[CallableStatement](../java/sql/CallableStatement.md) The interface used to execute SQL stored procedures.
[CameraConstrainedHighSpeedCaptureSession](../android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession.md) A constrained high speed capture session for a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#`, used for capturing high speed images from the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#` for high speed video recording use case.
[CameraOfflineSession](../android/hardware/camera2/CameraOfflineSession.md) A camera capture session that was switched to offline mode via successful call to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.html#switchToOffline(kotlin.collections.MutableCollection,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraOfflineSession.CameraOfflineSessionCallback)`.
[Channel](../java/nio/channels/Channel.md) A nexus for I/O operations.
[Channel](../android/se/omapi/Channel.md) Instances of this class represent an ISO/IEC 7816-4 channel opened to a Secure Element.
[CharArrayReader](../java/io/CharArrayReader.md) This class implements a character buffer that can be used as a character-input stream.
[CharArrayWriter](../java/io/CharArrayWriter.md) This class implements a character buffer that can be used as an Writer.
[CheckedInputStream](../java/util/zip/CheckedInputStream.md) An input stream that also maintains a checksum of the data being read.
[CheckedOutputStream](../java/util/zip/CheckedOutputStream.md) An output stream that also maintains a checksum of the data being written.
[CipherInputStream](../javax/crypto/CipherInputStream.md) A CipherInputStream is composed of an InputStream and a Cipher so that read() methods return data that are read in from the underlying InputStream but have been additionally processed by the Cipher.
[CipherOutputStream](../javax/crypto/CipherOutputStream.md) A CipherOutputStream is composed of an OutputStream and a Cipher so that write() methods first process the data before writing them out to the underlying OutputStream.
[CrossProcessCursor](../android/database/CrossProcessCursor.md) A cross process cursor is an extension of a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` that also supports usage from remote processes.
[CrossProcessCursorWrapper](../android/database/CrossProcessCursorWrapper.md) Cursor wrapper that implements `https://developer.android.com/reference/kotlin/android/database/CrossProcessCursor.html#`.
[CrossProcessCursorWrapper](../android/database/CrossProcessCursorWrapper.md) Cursor wrapper that implements `https://developer.android.com/reference/kotlin/android/database/CrossProcessCursor.html#`.
[Cursor](../android/database/Cursor.md) This interface provides random read-write access to the result set returned by a database query.
[CursorWindow](../android/database/CursorWindow.md) A buffer containing multiple cursor rows.
[CursorWrapper](../android/database/CursorWrapper.md) Wrapper class for Cursor that delegates all calls to the actual cursor object.
[DataInputStream](../java/io/DataInputStream.md) A data input stream lets an application read primitive Java data types from an underlying input stream in a machine-independent way.
[DataOutputStream](../java/io/DataOutputStream.md) A data output stream lets an application write primitive Java data types to an output stream in a portable way.
[DatagramChannel](../java/nio/channels/DatagramChannel.md) A selectable channel for datagram-oriented sockets.
[DatagramChannel](../java/nio/channels/DatagramChannel.md) A selectable channel for datagram-oriented sockets.
[DatagramChannel](../java/nio/channels/DatagramChannel.md) A selectable channel for datagram-oriented sockets.
[DatagramChannel](../java/nio/channels/DatagramChannel.md) A selectable channel for datagram-oriented sockets.
[DatagramChannel](../java/nio/channels/DatagramChannel.md) A selectable channel for datagram-oriented sockets.
[DatagramChannel](../java/nio/channels/DatagramChannel.md) A selectable channel for datagram-oriented sockets.
[DatagramChannel](../java/nio/channels/DatagramChannel.md) A selectable channel for datagram-oriented sockets.
[DatagramChannel](../java/nio/channels/DatagramChannel.md) A selectable channel for datagram-oriented sockets.
[DatagramSocket](../java/net/DatagramSocket.md) This class represents a socket for sending and receiving datagram packets.
[DeflaterInputStream](../java/util/zip/DeflaterInputStream.md) Implements an input stream filter for compressing data in the "deflate" compression format.
[DeflaterOutputStream](../java/util/zip/DeflaterOutputStream.md) This class implements an output stream filter for compressing data in the "deflate" compression format.
[DigestInputStream](../java/security/DigestInputStream.md) A transparent stream that updates the associated message digest using the bits going through the stream.
[DigestOutputStream](../java/security/DigestOutputStream.md) A transparent stream that updates the associated message digest using the bits going through the stream.
[DirectoryStream](../java/nio/file/DirectoryStream.md) An object to iterate over the entries in a directory.
[DoubleStream](../java/util/stream/DoubleStream.md) A sequence of primitive double-valued elements supporting sequential and parallel aggregate operations.
[DropBoxManager.Entry](../android/os/DropBoxManager.Entry.md) A single entry retrieved from the drop box.
[FileChannel](../java/nio/channels/FileChannel.md) A channel for reading, writing, mapping, and manipulating a file.
[FileChannel](../java/nio/channels/FileChannel.md) A channel for reading, writing, mapping, and manipulating a file.
[FileChannel](../java/nio/channels/FileChannel.md) A channel for reading, writing, mapping, and manipulating a file.
[FileChannel](../java/nio/channels/FileChannel.md) A channel for reading, writing, mapping, and manipulating a file.
[FileChannel](../java/nio/channels/FileChannel.md) A channel for reading, writing, mapping, and manipulating a file.
[FileChannel](../java/nio/channels/FileChannel.md) A channel for reading, writing, mapping, and manipulating a file.
[FileInputStream](../java/io/FileInputStream.md) A `FileInputStream` obtains input bytes from a file in a file system.
[FileOutputStream](../java/io/FileOutputStream.md) A file output stream is an output stream for writing data to a `File` or to a `FileDescriptor`.
[FileReader](../java/io/FileReader.md) Reads text from character files using a default buffer size.
[FileSystem](../java/nio/file/FileSystem.md) Provides an interface to a file system and is the factory for objects to access files and other objects in the file system.
[FileWriter](../java/io/FileWriter.md) Writes text to character files using a default buffer size.
[FilterInputStream](../java/io/FilterInputStream.md) A `FilterInputStream` contains some other input stream, which it uses as its basic source of data, possibly transforming the data along the way or providing additional functionality.
[FilterOutputStream](../java/io/FilterOutputStream.md) This class is the superclass of all classes that filter output streams.
[FilterReader](../java/io/FilterReader.md) Abstract class for reading filtered character streams.
[FilterWriter](../java/io/FilterWriter.md) Abstract class for writing filtered character streams.
[ForkJoinPool](../java/util/concurrent/ForkJoinPool.md) An `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#` for running `https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask.html#`s.
[Formatter](../java/util/Formatter.md) An interpreter for printf-style format strings.
[GZIPInputStream](../java/util/zip/GZIPInputStream.md) This class implements a stream filter for reading compressed data in the GZIP file format.
[GZIPOutputStream](../java/util/zip/GZIPOutputStream.md) This class implements a stream filter for writing compressed data in the GZIP file format.
[GatheringByteChannel](../java/nio/channels/GatheringByteChannel.md) A channel that can write bytes from a sequence of buffers.
[GlobalSearchSession](../android/app/appsearch/GlobalSearchSession.md) Provides a connection to all AppSearch databases the querying application has been granted access to.
[HttpResponseCache](../android/net/http/HttpResponseCache.md) Caches HTTP and HTTPS responses to the filesystem so they may be reused, saving time and bandwidth.
[InflaterInputStream](../java/util/zip/InflaterInputStream.md) This class implements a stream filter for uncompressing data in the "deflate" compression format.
[InflaterOutputStream](../java/util/zip/InflaterOutputStream.md) Implements an output stream filter for uncompressing data stored in the "deflate" compression format.
[InputStream](../java/io/InputStream.md) This abstract class is the superclass of all classes representing an input stream of bytes.
[InputStreamReader](../java/io/InputStreamReader.md) An InputStreamReader is a bridge from byte streams to character streams: It reads bytes and decodes them into characters using a specified `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#`.
[IntStream](../java/util/stream/IntStream.md) A sequence of primitive int-valued elements supporting sequential and parallel aggregate operations.
[InterruptibleChannel](../java/nio/channels/InterruptibleChannel.md) A channel that can be asynchronously closed and interrupted.
[IsoDep](../android/nfc/tech/IsoDep.md) Provides access to ISO-DEP (ISO 14443-4) properties and I/O operations on a `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#`.
[JarFile](../java/util/jar/JarFile.md) The `JarFile` class is used to read the contents of a jar file from any file that can be opened with `java.io.RandomAccessFile`.
[JarInputStream](../java/util/jar/JarInputStream.md) The `JarInputStream` class is used to read the contents of a JAR file from any input stream.
[JarOutputStream](../java/util/jar/JarOutputStream.md) The `JarOutputStream` class is used to write the contents of a JAR file to any output stream.
[JsonReader](../android/util/JsonReader.md) Reads a JSON ([RFC 4627](http://www.ietf.org/rfc/rfc4627.txt)) encoded value as a stream of tokens.
[JsonWriter](../android/util/JsonWriter.md) Writes a JSON ([RFC 4627](http://www.ietf.org/rfc/rfc4627.txt)) encoded value to a stream, one token at a time.
[LineNumberInputStream](../java/io/LineNumberInputStream.md) This class is an input stream filter that provides the added functionality of keeping track of the current line number.
[LineNumberReader](../java/io/LineNumberReader.md) A buffered character-input stream that keeps track of line numbers.
[LocalServerSocket](../android/net/LocalServerSocket.md) Non-standard class for creating an inbound UNIX-domain socket in the Linux abstract namespace.
[LocalSocket](../android/net/LocalSocket.md) Creates a (non-server) socket in the UNIX-domain namespace.
[LongStream](../java/util/stream/LongStream.md) A sequence of primitive long-valued elements supporting sequential and parallel aggregate operations.
[MatrixCursor](../android/database/MatrixCursor.md) A mutable cursor implementation backed by an array of `Object`s.
[MediaDataSource](../android/media/MediaDataSource.md) For supplying media data to the framework.
[MergeCursor](../android/database/MergeCursor.md) A convenience class that lets you present an array of Cursors as a single linear Cursor.
[MidiDevice](../android/media/midi/MidiDevice.md) This class is used for sending and receiving data to and from a MIDI device Instances of this class are created by `https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.html#openDevice(android.media.midi.MidiDeviceInfo,%20android.media.midi.MidiManager.OnDeviceOpenedListener,%20android.os.Handler)`.
[MidiDevice.MidiConnection](../android/media/midi/MidiDevice.MidiConnection.md) This class represents a connection between the output port of one device and the input port of another.
[MidiInputPort](../android/media/midi/MidiInputPort.md) This class is used for sending data to a port on a MIDI device
[MidiOutputPort](../android/media/midi/MidiOutputPort.md) This class is used for receiving data from a port on a MIDI device
[MifareClassic](../android/nfc/tech/MifareClassic.md) Provides access to MIFARE Classic properties and I/O operations on a `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#`.
[MifareUltralight](../android/nfc/tech/MifareUltralight.md) Provides access to MIFARE Ultralight properties and I/O operations on a `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#`.
[MockCursor](../android/test/mock/MockCursor.md) A mock `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` class that isolates the test code from real Cursor implementation.
[MulticastChannel](../java/nio/channels/MulticastChannel.md) A network channel that supports Internet Protocol (IP) multicasting.
[MulticastSocket](../java/net/MulticastSocket.md) The multicast datagram socket class is useful for sending and receiving IP multicast packets.
[Ndef](../android/nfc/tech/Ndef.md) Provides access to NDEF content and operations on a `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#`.
[NdefFormatable](../android/nfc/tech/NdefFormatable.md) Provide access to NDEF format operations on a `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#`.
[NetworkChannel](../java/nio/channels/NetworkChannel.md) A channel to a network socket.
[NfcA](../android/nfc/tech/NfcA.md) Provides access to NFC-A (ISO 14443-3A) properties and I/O operations on a `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#`.
[NfcB](../android/nfc/tech/NfcB.md) Provides access to NFC-B (ISO 14443-3B) properties and I/O operations on a `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#`.
[NfcBarcode](../android/nfc/tech/NfcBarcode.md) Provides access to tags containing just a barcode.
[NfcF](../android/nfc/tech/NfcF.md) Provides access to NFC-F (JIS 6319-4) properties and I/O operations on a `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#`.
[NfcV](../android/nfc/tech/NfcV.md) Provides access to NFC-V (ISO 15693) properties and I/O operations on a `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#`.
[ObjectInputStream](../java/io/ObjectInputStream.md) An ObjectInputStream deserializes primitive data and objects previously written using an ObjectOutputStream.
[ObjectInputStream](../java/io/ObjectInputStream.md) An ObjectInputStream deserializes primitive data and objects previously written using an ObjectOutputStream.
[ObjectOutputStream](../java/io/ObjectOutputStream.md) An ObjectOutputStream writes primitive data types and graphs of Java objects to an OutputStream.
[ObjectOutputStream](../java/io/ObjectOutputStream.md) An ObjectOutputStream writes primitive data types and graphs of Java objects to an OutputStream.
[OpenBlobForReadResponse](../android/app/appsearch/OpenBlobForReadResponse.md) The response to provide batch operation results of `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession.html#openBlobForRead(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`.
[OpenBlobForWriteResponse](../android/app/appsearch/OpenBlobForWriteResponse.md) The response to provide batch operation results of `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession.html#openBlobForWrite(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`.
[OutputStream](../java/io/OutputStream.md) This abstract class is the superclass of all classes representing an output stream of bytes.
[OutputStreamWriter](../java/io/OutputStreamWriter.md) An OutputStreamWriter is a bridge from character streams to byte streams: Characters written to it are encoded into bytes using a specified `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#`.
[PackageInstaller.Session](../android/content/pm/PackageInstaller.Session.md) An installation that is being actively staged.
[ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) The FileDescriptor returned by `https://developer.android.com/reference/kotlin/android/os/Parcel.html#readFileDescriptor()`, allowing you to close it when done with it.
[ParcelFileDescriptor.AutoCloseInputStream](../android/os/ParcelFileDescriptor.AutoCloseInputStream.md) An InputStream you can create on a ParcelFileDescriptor, which will take care of calling android.
[ParcelFileDescriptor.AutoCloseOutputStream](../android/os/ParcelFileDescriptor.AutoCloseOutputStream.md) An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android.
[PerformanceHintManager.Session](../android/os/PerformanceHintManager.Session.md) A Session represents a group of threads with an inter-related workload such that hints for their performance should be considered as a unit.
[Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) A channel representing the writable end of a `https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#`.
[Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) A channel representing the writable end of a `https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#`.
[Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) A channel representing the writable end of a `https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#`.
[Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) A channel representing the writable end of a `https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#`.
[Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) A channel representing the writable end of a `https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#`.
[Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) A channel representing the readable end of a `https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#`.
[Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) A channel representing the readable end of a `https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#`.
[Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) A channel representing the readable end of a `https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#`.
[Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) A channel representing the readable end of a `https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#`.
[Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) A channel representing the readable end of a `https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#`.
[PipedInputStream](../java/io/PipedInputStream.md) A piped input stream should be connected to a piped output stream; the piped input stream then provides whatever data bytes are written to the piped output stream.
[PipedOutputStream](../java/io/PipedOutputStream.md) A piped output stream can be connected to a piped input stream to create a communications pipe.
[PipedReader](../java/io/PipedReader.md) Piped character-input streams.
[PipedWriter](../java/io/PipedWriter.md) Piped character-output streams.
[PreparedStatement](../java/sql/PreparedStatement.md) An object that represents a precompiled SQL statement.
[PrintStream](../java/io/PrintStream.md) A `PrintStream` adds functionality to another output stream, namely the ability to print representations of various data values conveniently.
[PrintStream](../java/io/PrintStream.md) A `PrintStream` adds functionality to another output stream, namely the ability to print representations of various data values conveniently.
[PrintWriter](../java/io/PrintWriter.md) Prints formatted representations of objects to a text-output stream.
[PublishDiscoverySession](../android/net/wifi/aware/PublishDiscoverySession.md) A class representing a Aware publish session.
[PushbackInputStream](../java/io/PushbackInputStream.md) A `PushbackInputStream` adds functionality to another input stream, namely the ability to "push back" or "unread" bytes, by storing pushed-back bytes in an internal buffer.
[PushbackReader](../java/io/PushbackReader.md) A character-stream reader that allows characters to be pushed back into the stream.
[RandomAccessFile](../java/io/RandomAccessFile.md) Instances of this class support both reading and writing to a random access file.
[ReadableByteChannel](../java/nio/channels/ReadableByteChannel.md) A channel that can read bytes.
[Reader](../java/io/Reader.md) Abstract class for reading character streams.
[ResourcesProvider](../android/content/res/loader/ResourcesProvider.md) Provides methods to load resources data from APKs (`.apk`) and resources tables (eg.
[RowSet](../javax/sql/RowSet.md) The interface that adds support to the JDBC API for the JavaBeansTM component model.
[SQLiteClosable](../android/database/sqlite/SQLiteClosable.md) An object created from a SQLiteDatabase that can be closed.
[SQLiteCursor](../android/database/sqlite/SQLiteCursor.md) A Cursor implementation that exposes results from a query on a `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#`.
[SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md) Exposes methods to manage a SQLite database.
[SQLiteProgram](../android/database/sqlite/SQLiteProgram.md) A base class for compiled SQLite programs.
[SQLiteQuery](../android/database/sqlite/SQLiteQuery.md) Represents a query that reads the resulting rows into a `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery.html#`.
[SQLiteRawStatement](../android/database/sqlite/SQLiteRawStatement.md) A represents a SQLite prepared statement.
[SQLiteStatement](../android/database/sqlite/SQLiteStatement.md) Represents a statement that can be executed against a database.
[SSLServerSocket](../javax/net/ssl/SSLServerSocket.md) This class extends `ServerSocket`s and provides secure server sockets using protocols such as the Secure Sockets Layer (SSL) or Transport Layer Security (TLS) protocols.
[SSLSocket](../javax/net/ssl/SSLSocket.md) This class extends `Socket`s and provides secure socket using protocols such as the "Secure Sockets Layer" (SSL) or IETF "Transport Layer Security" (TLS) protocols.
[Scanner](../java/util/Scanner.md) A simple text scanner which can parse primitive types and strings using regular expressions.
[ScatteringByteChannel](../java/nio/channels/ScatteringByteChannel.md) A channel that can read bytes into a sequence of buffers.
[ScheduledExecutorService](../java/util/concurrent/ScheduledExecutorService.md) An `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#` that can schedule commands to run after a given delay, or to execute periodically.
[ScheduledThreadPoolExecutor](../java/util/concurrent/ScheduledThreadPoolExecutor.md) A `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.html#` that can additionally schedule commands to run after a given delay, or to execute periodically.
[ScheduledThreadPoolExecutor](../java/util/concurrent/ScheduledThreadPoolExecutor.md) A `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.html#` that can additionally schedule commands to run after a given delay, or to execute periodically.
[SearchResults](../android/app/appsearch/SearchResults.md) Encapsulates results of a search operation.
[SecureDirectoryStream](../java/nio/file/SecureDirectoryStream.md) A `DirectoryStream` that defines operations on files that are located relative to an open directory.
[SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md) A byte channel that maintains a current *position* and allows the position to be changed.
[SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md) A byte channel that maintains a current *position* and allows the position to be changed.
[SelectableChannel](../java/nio/channels/SelectableChannel.md) A channel that can be multiplexed via a `https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#`.
[SelectableChannel](../java/nio/channels/SelectableChannel.md) A channel that can be multiplexed via a `https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#`.
[SelectableChannel](../java/nio/channels/SelectableChannel.md) A channel that can be multiplexed via a `https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#`.
[Selector](../java/nio/channels/Selector.md) A multiplexor of `https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel.html#` objects.
[SensorDirectChannel](../android/hardware/SensorDirectChannel.md) Class representing a sensor direct channel.
[SequenceInputStream](../java/io/SequenceInputStream.md) A `SequenceInputStream` represents the logical concatenation of other input streams.
[ServerSocket](../java/net/ServerSocket.md) This class implements server sockets.
[ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md) A selectable channel for stream-oriented listening sockets.
[ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md) A selectable channel for stream-oriented listening sockets.
[ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md) A selectable channel for stream-oriented listening sockets.
[ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md) A selectable channel for stream-oriented listening sockets.
[SharedMemory](../android/os/SharedMemory.md) SharedMemory enables the creation, mapping, and protection control over anonymous shared memory.
[Socket](../java/net/Socket.md) This class implements client sockets (also called just "sockets").
[SocketChannel](../java/nio/channels/SocketChannel.md) A selectable channel for stream-oriented connecting sockets.
[SocketChannel](../java/nio/channels/SocketChannel.md) A selectable channel for stream-oriented connecting sockets.
[SocketChannel](../java/nio/channels/SocketChannel.md) A selectable channel for stream-oriented connecting sockets.
[SocketChannel](../java/nio/channels/SocketChannel.md) A selectable channel for stream-oriented connecting sockets.
[SocketChannel](../java/nio/channels/SocketChannel.md) A selectable channel for stream-oriented connecting sockets.
[SocketChannel](../java/nio/channels/SocketChannel.md) A selectable channel for stream-oriented connecting sockets.
[SocketChannel](../java/nio/channels/SocketChannel.md) A selectable channel for stream-oriented connecting sockets.
[SocketChannel](../java/nio/channels/SocketChannel.md) A selectable channel for stream-oriented connecting sockets.
[Stream](../java/util/stream/Stream.md) A sequence of elements supporting sequential and parallel aggregate operations.
[StringBufferInputStream](../java/io/StringBufferInputStream.md) This class allows an application to create an input stream in which the bytes read are supplied by the contents of a string.
[StringReader](../java/io/StringReader.md) A character stream whose source is a string.
[StringWriter](../java/io/StringWriter.md) A character stream that collects its output in a string buffer, which can then be used to construct a string.
[SubscribeDiscoverySession](../android/net/wifi/aware/SubscribeDiscoverySession.md) A class representing a Aware subscribe session.
[SurfaceControl.Transaction](../android/view/SurfaceControl.Transaction.md) An atomic set of changes to a set of SurfaceControl.
[TagTechnology](../android/nfc/tech/TagTechnology.md) is an interface to a technology in a `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#`
[ThreadPoolExecutor](../java/util/concurrent/ThreadPoolExecutor.md) An `https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#` that executes each submitted task using one of possibly several pooled threads, normally configured using `https://developer.android.com/reference/kotlin/java/util/concurrent/Executors.html#` factory methods.
[URLClassLoader](../java/net/URLClassLoader.md) This class loader is used to load classes and resources from a search path of URLs referring to both JAR files and directories.
[UploadDataProvider](../android/net/http/UploadDataProvider.md) Abstract class allowing the embedder to provide an upload body to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.html#`.
[WatchService](../java/nio/file/WatchService.md) A watch service that *watches* registered objects for changes and events.
[WritableByteChannel](../java/nio/channels/WritableByteChannel.md) A channel that can write bytes.
[Writer](../java/io/Writer.md) Abstract class for writing to character streams.
[ZipFile](../java/util/zip/ZipFile.md) This class is used to read entries from a zip file.
[ZipInputStream](../java/util/zip/ZipInputStream.md) This class implements an input stream filter for reading files in the ZIP file format.
[ZipOutputStream](../java/util/zip/ZipOutputStream.md) This class implements an output stream filter for writing files in the ZIP file format.

An object that may hold resources (such as file or socket handles) until it is closed. The `https://developer.android.com/reference/kotlin/java/lang/AutoCloseable#close()` method of an `AutoCloseable` object is called automatically when exiting a `try`-with-resources block for which the object has been declared in the resource specification header. This construction ensures prompt release, avoiding resource exhaustion exceptions and errors that may otherwise occur.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/AutoCloseable#close()()` Closes this resource, relinquishing any underlying resources. |

## Public methods

### close

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun close(): Unit
```

Closes this resource, relinquishing any underlying resources. This method is invoked automatically on objects managed by the `try`-with-resources statement.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
