# IllegalStateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalStateException

```
open class IllegalStateException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java/lang/IllegalStateException.md) |

| Known Direct Subclasses [AcceptPendingException](../java/nio/channels/AcceptPendingException.md), [AlreadyBoundException](../java/nio/channels/AlreadyBoundException.md), [AlreadyConnectedException](../java/nio/channels/AlreadyConnectedException.md), [CancellationException](../java/util/concurrent/CancellationException.md), [CancelledKeyException](../java/nio/channels/CancelledKeyException.md), [ClosedDirectoryStreamException](../java/nio/file/ClosedDirectoryStreamException.md), [ClosedFileSystemException](../java/nio/file/ClosedFileSystemException.md), [ClosedSelectorException](../java/nio/channels/ClosedSelectorException.md), [ClosedWatchServiceException](../java/nio/file/ClosedWatchServiceException.md), [ConnectionPendingException](../java/nio/channels/ConnectionPendingException.md), [FormatterClosedException](../java/util/FormatterClosedException.md), [IllegalBlockingModeException](../java/nio/channels/IllegalBlockingModeException.md), and 18 others. |-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AcceptPendingException](../java/nio/channels/AcceptPendingException.md) | Unchecked exception thrown when an attempt is made to initiate an accept operation on a channel and a previous accept operation has not completed. | | [AlreadyBoundException](../java/nio/channels/AlreadyBoundException.md) | Unchecked exception thrown when an attempt is made to bind the socket a network oriented channel that is already bound. | | [AlreadyConnectedException](../java/nio/channels/AlreadyConnectedException.md) | Unchecked exception thrown when an attempt is made to connect a [SocketChannel](../java/nio/channels/SocketChannel.md) that is already connected. | | [CancellationException](../java/util/concurrent/CancellationException.md) | Exception indicating that the result of a value-producing task, such as a [FutureTask](../java/util/concurrent/FutureTask.md), cannot be retrieved because the task was cancelled. | | [CancelledKeyException](../java/nio/channels/CancelledKeyException.md) | Unchecked exception thrown when an attempt is made to use a selection key that is no longer valid. | | [ClosedDirectoryStreamException](../java/nio/file/ClosedDirectoryStreamException.md) | Unchecked exception thrown when an attempt is made to invoke an operation on a directory stream that is closed. | | [ClosedFileSystemException](../java/nio/file/ClosedFileSystemException.md) | Unchecked exception thrown when an attempt is made to invoke an operation on a file and the file system is closed. | | [ClosedSelectorException](../java/nio/channels/ClosedSelectorException.md) | Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a closed selector. | | [ClosedWatchServiceException](../java/nio/file/ClosedWatchServiceException.md) | Unchecked exception thrown when an attempt is made to invoke an operation on a watch service that is closed. | | [ConnectionPendingException](../java/nio/channels/ConnectionPendingException.md) | Unchecked exception thrown when an attempt is made to connect a [SocketChannel](../java/nio/channels/SocketChannel.md) for which a non-blocking connection operation is already in progress. | | [FormatterClosedException](../java/util/FormatterClosedException.md) | Unchecked exception thrown when the formatter has been closed. | | [IllegalBlockingModeException](../java/nio/channels/IllegalBlockingModeException.md) | Unchecked exception thrown when a blocking-mode-specific operation is invoked upon a channel in the incorrect blocking mode. | | [InvalidMarkException](../java/nio/InvalidMarkException.md) | Unchecked exception thrown when an attempt is made to reset a buffer when its mark is not defined. | | [LimitExceededException](../android/os/LimitExceededException.md) | Indicates that the app has exceeded a limit set by the System. | | [MediaCasStateException](../android/media/MediaCasStateException.md) | Base class for MediaCas runtime exceptions | | [MediaCodec.CodecException](../android/media/MediaCodec.CodecException.md) | Thrown when an internal codec error occurs. | | [MediaDrm.MediaDrmStateException](../android/media/MediaDrm.MediaDrmStateException.md) | Thrown when a general failure occurs during a MediaDrm operation. | | [MediaDrmResetException](../android/media/MediaDrmResetException.md) | This exception is thrown when the MediaDrm instance has become unusable due to a restart of the mediaserver process. | | [NoConnectionPendingException](../java/nio/channels/NoConnectionPendingException.md) | Unchecked exception thrown when the [finishConnect](../java/nio/channels/SocketChannel.md))method of a [SocketChannel](../java/nio/channels/SocketChannel.md) is invoked without first successfully invoking its [connect](../java/nio/channels/SocketChannel.md))method. | | [NonReadableChannelException](../java/nio/channels/NonReadableChannelException.md) | Unchecked exception thrown when an attempt is made to read from a channel that was not originally opened for reading. | | [NonWritableChannelException](../java/nio/channels/NonWritableChannelException.md) | Unchecked exception thrown when an attempt is made to write to a channel that was not originally opened for writing. | | [NotYetBoundException](../java/nio/channels/NotYetBoundException.md) | Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a server socket channel that is not yet bound. | | [NotYetConnectedException](../java/nio/channels/NotYetConnectedException.md) | Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a socket channel that is not yet connected. | | [OverlappingFileLockException](../java/nio/channels/OverlappingFileLockException.md) | Unchecked exception thrown when an attempt is made to acquire a lock on a region of a file that overlaps a region already locked by the same Java virtual machine, or when another thread is already waiting to lock an overlapping region of the same file. | | [ReadPendingException](../java/nio/channels/ReadPendingException.md) | Unchecked exception thrown when an attempt is made to read from an asynchronous socket channel and a previous read has not completed. | | [ServiceStartNotAllowedException](../android/app/ServiceStartNotAllowedException.md) | Exception thrown when an app tries to start a [Service](../android/app/Service.md) when it's not allowed to do so. | | [ShutdownChannelGroupException](../java/nio/channels/ShutdownChannelGroupException.md) | Unchecked exception thrown when an attempt is made to construct a channel in a group that is shutdown or the completion handler for an I/O operation cannot be invoked because the channel group has terminated. | | [StartForegroundCalledOnStoppedServiceException](../android/app/StartForegroundCalledOnStoppedServiceException.md) | Exception thrown when android. | | [UnsafeStateException](../android/app/admin/UnsafeStateException.md) | Exception thrown when a [android.app.admin.DevicePolicyManager](../android/app/admin/DevicePolicyManager.md) operation failed because it was not safe to be executed at that moment. | | [WritePendingException](../java/nio/channels/WritePendingException.md) | Unchecked exception thrown when an attempt is made to write to an asynchronous socket channel and a previous write has not completed. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [BackgroundServiceStartNotAllowedException](../android/app/BackgroundServiceStartNotAllowedException.md), [ForegroundServiceStartNotAllowedException](../android/app/ForegroundServiceStartNotAllowedException.md), [ForegroundServiceTypeException](../android/app/ForegroundServiceTypeException.md), [InvalidForegroundServiceTypeException](../android/app/InvalidForegroundServiceTypeException.md), [MissingForegroundServiceTypeException](../android/app/MissingForegroundServiceTypeException.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BackgroundServiceStartNotAllowedException](../android/app/BackgroundServiceStartNotAllowedException.md) | Exception thrown when an app tries to start a background [Service](../android/app/Service.md) when it's not allowed to do so. | | [ForegroundServiceStartNotAllowedException](../android/app/ForegroundServiceStartNotAllowedException.md) | Exception thrown when an app tries to start a foreground [Service](../android/app/Service.md) when it's not allowed to do so. | | [ForegroundServiceTypeException](../android/app/ForegroundServiceTypeException.md) | Base exception thrown when an app tries to start a foreground [Service](../android/app/Service.md) without a valid type. | | [InvalidForegroundServiceTypeException](../android/app/InvalidForegroundServiceTypeException.md) | Exception thrown when an app tries to start a foreground [Service](../android/app/Service.md) with an invalid type. | | [MissingForegroundServiceTypeException](../android/app/MissingForegroundServiceTypeException.md) | Exception thrown when an app tries to start a foreground [Service](../android/app/Service.md) without a type. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Signals that a method has been invoked at an illegal or inappropriate time. In other words, the Java environment or Java application is not in an appropriate state for the requested operation.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalStateException](../java/lang/IllegalStateException.md))`()` Constructs an IllegalStateException with no detail message. |
| [IllegalStateException](../java/lang/IllegalStateException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an IllegalStateException with the specified detail message. |
| [IllegalStateException](../java/lang/IllegalStateException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new exception with the specified detail message and cause. |
| [IllegalStateException](../java/lang/IllegalStateException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new exception with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### IllegalStateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalStateException()
```

Constructs an IllegalStateException with no detail message. A detail message is a String that describes this particular exception. 

### IllegalStateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalStateException(s: String!)
```

Constructs an IllegalStateException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the String that contains a detailed message |

### IllegalStateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalStateException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new exception with the specified detail message and cause.

Note that the detail message associated with`cause`is*not*automatically incorporated in this exception's detail message.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [Throwable.getMessage()](../java/lang/Throwable.md))method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [Throwable.getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### IllegalStateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalStateException(cause: Throwable!)
```

Constructs a new exception with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). This constructor is useful for exceptions that are little more than wrappers for other throwables (for example, ).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [Throwable.getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
