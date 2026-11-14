Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MbmsDownloadSession

Kotlin | [Java](../android/telephony/MbmsDownloadSession.md)
| --- | --- |

```
open class MbmsDownloadSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.MbmsDownloadSession](../android/telephony/MbmsDownloadSession.md) |

This class provides functionality for file download over MBMS.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#DEFAULT_TOP_LEVEL_TEMP_DIRECTORY:kotlin.String` The default directory name for all MBMS temp files. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#EXTRA_MBMS_COMPLETED_FILE_URI:kotlin.String` `https://developer.android.com/reference/kotlin/android/net/Uri.html#` extra that Android will attach to the intent supplied via `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest.Builder#setAppIntent(android.content.Intent)` Indicates the location of the successfully downloaded file within the directory that the app provided via the builder. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#EXTRA_MBMS_DOWNLOAD_REQUEST:kotlin.String` Extra containing the `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` for which the download result or file descriptor request is for. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#EXTRA_MBMS_DOWNLOAD_RESULT:kotlin.String` Integer extra that Android will attach to the intent supplied via `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest.Builder#setAppIntent(android.content.Intent)` Indicates the result code of the download. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#EXTRA_MBMS_FILE_INFO:kotlin.String` `https://developer.android.com/reference/kotlin/android/telephony/mbms/FileInfo` extra that Android will attach to the intent supplied via `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest.Builder#setAppIntent(android.content.Intent)` Indicates the file for which the download result is for. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_CANCELLED:kotlin.Int` Indicates that the download was cancelled via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#cancelDownload(android.telephony.mbms.DownloadRequest)`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_DOWNLOAD_FAILURE:kotlin.Int` Indicates that there was an error while processing downloaded files, such as a file repair or file decoding error and is not due to a file I/O error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_EXPIRED:kotlin.Int` Indicates that the download will not be completed due to the expiration of its download window on the carrier's network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_FILE_ROOT_UNREACHABLE:kotlin.Int` Indicates that the file root that was set is currently unreachable. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_IO_ERROR:kotlin.Int` Indicates that the download will not be completed due to an I/O error incurred while writing to temp files. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_OUT_OF_STORAGE:kotlin.Int` Indicates that the file system is full and the `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` can not complete. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_SERVICE_ID_NOT_DEFINED:kotlin.Int` Indicates that the Service ID specified in the `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` is incorrect due to the Id being incorrect, stale, expired, or similar. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_SUCCESSFUL:kotlin.Int` Indicates that the download was successful. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#STATUS_ACTIVELY_DOWNLOADING:kotlin.Int` Indicates that the file is actively being downloaded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#STATUS_PENDING_DOWNLOAD:kotlin.Int` Indicates that the file is awaiting the next download or repair operations. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#STATUS_PENDING_DOWNLOAD_WINDOW:kotlin.Int` Indicates that the file is waiting to download because its download window has not yet started and is scheduled for a future time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#STATUS_PENDING_REPAIR:kotlin.Int` Indicates that the file is awaiting file repair after the download has ended. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#STATUS_UNKNOWN:kotlin.Int` Indicates that the middleware has no information on the file. |
| --- | --- |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#addProgressListener(android.telephony.mbms.DownloadRequest,%20java.util.concurrent.Executor,%20android.telephony.mbms.DownloadProgressListener)(request: https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadProgressListener)` Registers a progress listener for a `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` previously requested via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#download(android.telephony.mbms.DownloadRequest)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#addServiceAnnouncement(kotlin.ByteArray)(contents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Inform the middleware of a service announcement descriptor received from a group communication server. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#addStatusListener(android.telephony.mbms.DownloadRequest,%20java.util.concurrent.Executor,%20android.telephony.mbms.DownloadStatusListener)(request: https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadStatusListener)` Registers a download status listener for a `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` previously requested via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#download(android.telephony.mbms.DownloadRequest)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#cancelDownload(android.telephony.mbms.DownloadRequest)(downloadRequest: https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest)` Attempts to cancel the specified `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#close()()` Terminates this instance. |
| open static [MbmsDownloadSession](../android/telephony/MbmsDownloadSession.md)! | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#create(android.content.Context,%20java.util.concurrent.Executor,%20android.telephony.mbms.MbmsDownloadSessionCallback)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback)` Create a new `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#` using the system default data subscription ID. |
| --- | --- |
| open static [MbmsDownloadSession](../android/telephony/MbmsDownloadSession.md)? | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#create(android.content.Context,%20java.util.concurrent.Executor,%20kotlin.Int,%20android.telephony.mbms.MbmsDownloadSessionCallback)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, callback: https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback)` Create a new MbmsDownloadManager using the given subscription ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#download(android.telephony.mbms.DownloadRequest)(request: https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest)` Requests the download of a file or set of files that the carrier has indicated to be available. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#getMaximumServiceAnnouncementSize()()` Returns the maximum size of the service announcement descriptor that can be provided via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#addServiceAnnouncement(kotlin.ByteArray)` |
| --- | --- |
| open [File](../java/io/File.md)? | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#getTempFileRootDirectory()()` Retrieves the currently configured temp file root directory. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [DownloadRequest](../android/telephony/mbms/DownloadRequest.md)!\> | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#listPendingDownloads()()` Returns a list of pending `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest`s that originated from this application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#removeProgressListener(android.telephony.mbms.DownloadRequest,%20android.telephony.mbms.DownloadProgressListener)(request: https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest, listener: https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadProgressListener)` Un-register a listener previously registered via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#addProgressListener(android.telephony.mbms.DownloadRequest,%20java.util.concurrent.Executor,%20android.telephony.mbms.DownloadProgressListener)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#removeStatusListener(android.telephony.mbms.DownloadRequest,%20android.telephony.mbms.DownloadStatusListener)(request: https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest, listener: https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadStatusListener)` Un-register a listener previously registered via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#addStatusListener(android.telephony.mbms.DownloadRequest,%20java.util.concurrent.Executor,%20android.telephony.mbms.DownloadStatusListener)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#requestDownloadState(android.telephony.mbms.DownloadRequest,%20android.telephony.mbms.FileInfo)(downloadRequest: https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest!, fileInfo: https://developer.android.com/reference/kotlin/android/telephony/mbms/FileInfo!)` Requests information about the state of a file pending download. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#requestUpdateFileServices(kotlin.collections.MutableList)(classList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` An inspection API to retrieve the list of available `https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo`s currently being advertised. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#resetDownloadKnowledge(android.telephony.mbms.DownloadRequest)(downloadRequest: https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest!)` Resets the middleware's knowledge of previously-downloaded files in this download request. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#setTempFileRootDirectory(java.io.File)(tempFileRootDirectory: https://developer.android.com/reference/kotlin/java/io/File.html#)` Sets the temp file root for downloads. |

## Constants

### DEFAULT_TOP_LEVEL_TEMP_DIRECTORY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT_TOP_LEVEL_TEMP_DIRECTORY: String
```

The default directory name for all MBMS temp files. If you call `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#download(android.telephony.mbms.DownloadRequest)` without first calling `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#setTempFileRootDirectory(java.io.File)`, this directory will be created for you under the path returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`.

 Value: "androidMbmsTempFileRoot"

### EXTRA_MBMS_COMPLETED_FILE_URI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MBMS_COMPLETED_FILE_URI: String
```

`https://developer.android.com/reference/kotlin/android/net/Uri.html#` extra that Android will attach to the intent supplied via `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest.Builder#setAppIntent(android.content.Intent)` Indicates the location of the successfully downloaded file within the directory that the app provided via the builder. Will always be set to a non-null value if `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#EXTRA_MBMS_DOWNLOAD_RESULT:kotlin.String` is set to `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_SUCCESSFUL:kotlin.Int`.

 Value: "android.telephony.extra.MBMS_COMPLETED_FILE_URI"

### EXTRA_MBMS_DOWNLOAD_REQUEST

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MBMS_DOWNLOAD_REQUEST: String
```

Extra containing the `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` for which the download result or file descriptor request is for. Must not be null.

 Value: "android.telephony.extra.MBMS_DOWNLOAD_REQUEST"

### EXTRA_MBMS_DOWNLOAD_RESULT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MBMS_DOWNLOAD_RESULT: String
```

Integer extra that Android will attach to the intent supplied via `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest.Builder#setAppIntent(android.content.Intent)` Indicates the result code of the download. One of `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_SUCCESSFUL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_EXPIRED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_CANCELLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_IO_ERROR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_DOWNLOAD_FAILURE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_OUT_OF_STORAGE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_SERVICE_ID_NOT_DEFINED:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#RESULT_FILE_ROOT_UNREACHABLE:kotlin.Int`. This extra may also be used by the middleware when it is sending intents to the app.

 Value: "android.telephony.extra.MBMS_DOWNLOAD_RESULT"

### EXTRA_MBMS_FILE_INFO

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MBMS_FILE_INFO: String
```

`https://developer.android.com/reference/kotlin/android/telephony/mbms/FileInfo` extra that Android will attach to the intent supplied via `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest.Builder#setAppIntent(android.content.Intent)` Indicates the file for which the download result is for. Never null. This extra may also be used by the middleware when it is sending intents to the app.

 Value: "android.telephony.extra.MBMS_FILE_INFO"

### RESULT_CANCELLED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_CANCELLED: Int
```

Indicates that the download was cancelled via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#cancelDownload(android.telephony.mbms.DownloadRequest)`.

 Value: 2

### RESULT_DOWNLOAD_FAILURE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_DOWNLOAD_FAILURE: Int
```

Indicates that there was an error while processing downloaded files, such as a file repair or file decoding error and is not due to a file I/O error. This is likely a transient error and another `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` should be sent to try the download again.

 Value: 6

### RESULT_EXPIRED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_EXPIRED: Int
```

Indicates that the download will not be completed due to the expiration of its download window on the carrier's network.

 Value: 3

### RESULT_FILE_ROOT_UNREACHABLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_FILE_ROOT_UNREACHABLE: Int
```

Indicates that the file root that was set is currently unreachable. This can happen if the temp files are set to be stored on external storage and the SD card was removed, for example. The temp file root should be changed before sending another DownloadRequest.

 Value: 8

### RESULT_IO_ERROR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_IO_ERROR: Int
```

Indicates that the download will not be completed due to an I/O error incurred while writing to temp files. This is likely a transient error and another `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` should be sent to try the download again.

 Value: 4

### RESULT_OUT_OF_STORAGE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_OUT_OF_STORAGE: Int
```

Indicates that the file system is full and the `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` can not complete. Either space must be made on the current file system or the temp file root location must be changed to a location that is not full to download the temp files.

 Value: 7

### RESULT_SERVICE_ID_NOT_DEFINED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_SERVICE_ID_NOT_DEFINED: Int
```

Indicates that the Service ID specified in the `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` is incorrect due to the Id being incorrect, stale, expired, or similar.

 Value: 5

### RESULT_SUCCESSFUL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_SUCCESSFUL: Int
```

Indicates that the download was successful.

 Value: 1

### STATUS_ACTIVELY_DOWNLOADING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_ACTIVELY_DOWNLOADING: Int
```

Indicates that the file is actively being downloaded.

 Value: 1

### STATUS_PENDING_DOWNLOAD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_PENDING_DOWNLOAD: Int
```

Indicates that the file is awaiting the next download or repair operations. When a more precise status is known, the status will change to either `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#STATUS_PENDING_REPAIR:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#STATUS_PENDING_DOWNLOAD_WINDOW:kotlin.Int`.

 Value: 2

### STATUS_PENDING_DOWNLOAD_WINDOW

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_PENDING_DOWNLOAD_WINDOW: Int
```

Indicates that the file is waiting to download because its download window has not yet started and is scheduled for a future time.

 Value: 4

### STATUS_PENDING_REPAIR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_PENDING_REPAIR: Int
```

Indicates that the file is awaiting file repair after the download has ended.

 Value: 3

### STATUS_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_UNKNOWN: Int
```

Indicates that the middleware has no information on the file.

 Value: 0

## Public methods

### addProgressListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addProgressListener(
    request: DownloadRequest, 
    executor: Executor, 
    listener: DownloadProgressListener
): Unit
```

Registers a progress listener for a `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` previously requested via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#download(android.telephony.mbms.DownloadRequest)`. This listener will only be called as long as both this app and the middleware are both running -- if either one stops, no further calls on the provided `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadProgressListener` will be enqueued. If the middleware is not aware of the specified download request, this method will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`. If the operation encountered an error, the error code will be delivered via `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onError(kotlin.Int,%20kotlin.String)`. Repeated calls to this method for the same `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` will replace the previously registered listener.

| Parameters ||
|---|---|
| `request` | [DownloadRequest](../android/telephony/mbms/DownloadRequest.md): The `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` that you want updates on. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which calls to `listener` should be executed. This value cannot be `null`. |
| `listener` | [DownloadProgressListener](../android/telephony/mbms/DownloadProgressListener.md): The listener that should be called when the middleware has information to share on the progress of the download. This value cannot be `null`. |
| --- | --- |

### addServiceAnnouncement

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addServiceAnnouncement(contents: ByteArray): Unit
```

Inform the middleware of a service announcement descriptor received from a group communication server. When participating in a group call via the `https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession` API, applications may receive a service announcement descriptor from the group call server that informs them of files that may be relevant to users communicating on the group call. After supplying the service announcement descriptor received from the server to the middleware via this API, applications will receive information on the available files via `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onFileServicesUpdated(kotlin.collections.MutableList)`, and the available files will be downloadable via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#download(android.telephony.mbms.DownloadRequest)` like other files published via `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onFileServicesUpdated(kotlin.collections.MutableList)`. Asynchronous error codes via the `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onError(kotlin.Int,%20kotlin.String)` callback may include any of the errors that are not specific to the streaming use-case. May throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` when the middleware has not yet been bound, or an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` if the byte array is too large, or an `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#` if the middleware has not implemented this method.

| Parameters ||
|---|---|
| `contents` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The contents of the service announcement descriptor received from the group call server. If the size of this array is greater than the value of `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#getMaximumServiceAnnouncementSize()`, an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown. This value cannot be `null`. |

### addStatusListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addStatusListener(
    request: DownloadRequest, 
    executor: Executor, 
    listener: DownloadStatusListener
): Unit
```

Registers a download status listener for a `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` previously requested via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#download(android.telephony.mbms.DownloadRequest)`. This callback will only be called as long as both this app and the middleware are both running -- if either one stops, no further calls on the provided `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadStatusListener` will be enqueued. If the middleware is not aware of the specified download request, this method will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`. If the operation encountered an error, the error code will be delivered via `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onError(kotlin.Int,%20kotlin.String)`. Repeated calls to this method for the same `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` will replace the previously registered listener.

| Parameters ||
|---|---|
| `request` | [DownloadRequest](../android/telephony/mbms/DownloadRequest.md): The `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` that you want updates on. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which calls to `listener ` should be executed. This value cannot be `null`. |
| `listener` | [DownloadStatusListener](../android/telephony/mbms/DownloadStatusListener.md): The listener that should be called when the middleware has information to share on the status download. This value cannot be `null`. |
| --- | --- |

### cancelDownload

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancelDownload(downloadRequest: DownloadRequest): Unit
```

Attempts to cancel the specified `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest`. If the operation encountered an error, the error code will be delivered via `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onError(kotlin.Int,%20kotlin.String)`.

| Parameters ||
|---|---|
| `downloadRequest` | [DownloadRequest](../android/telephony/mbms/DownloadRequest.md): The download request that you wish to cancel. This value cannot be `null`. |

### close

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Terminates this instance. After this method returns, no further callbacks originating from the middleware will be enqueued on the provided instance of `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback`, but callbacks that have already been enqueued will still be delivered. It is safe to call `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#create(android.content.Context,%20java.util.concurrent.Executor,%20kotlin.Int,%20android.telephony.mbms.MbmsDownloadSessionCallback)` to obtain another instance of `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#` immediately after this method returns. May throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### create

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun create(
    context: Context, 
    executor: Executor, 
    callback: MbmsDownloadSessionCallback
): MbmsDownloadSession!
```

Create a new `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#` using the system default data subscription ID. See `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#create(android.content.Context,%20java.util.concurrent.Executor,%20kotlin.Int,%20android.telephony.mbms.MbmsDownloadSessionCallback)`

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md): This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): This value cannot be `null`. |
| `callback` | [MbmsDownloadSessionCallback](../android/telephony/mbms/MbmsDownloadSessionCallback.md): This value cannot be `null`. |
| --- | --- |

### create

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun create(
    context: Context, 
    executor: Executor, 
    subscriptionId: Int, 
    callback: MbmsDownloadSessionCallback
): MbmsDownloadSession?
```

Create a new MbmsDownloadManager using the given subscription ID. Note that this call will bind a remote service and that may take a bit. The instance of `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#` that is returned will not be ready for use until `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onMiddlewareReady()` is called on the provided callback. If you attempt to use the instance before it is ready, an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` will be thrown or an error will be delivered through `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onError(kotlin.Int,%20kotlin.String)`. This also may throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`. You may only have one instance of `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#` per UID. If you call this method while there is an active instance of `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#` in your process (in other words, one that has not had `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#close()` called on it), this method will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. If you call this method in a different process running under the same UID, an error will be indicated via `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onError(kotlin.Int,%20kotlin.String)`. Note that initialization may fail asynchronously. If you wish to try again after you receive such an asynchronous error, you must call `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#close()` on the instance of `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#` that you received before calling this method again.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md): The instance of `https://developer.android.com/reference/kotlin/android/content/Context.html#` to use. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): The executor on which you wish to execute callbacks. This value cannot be `null`. |
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The data subscription ID to use |
| --- | --- |
| `callback` | [MbmsDownloadSessionCallback](../android/telephony/mbms/MbmsDownloadSessionCallback.md): A callback to get asynchronous error messages and file service updates. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#?` | A new instance of `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#`, or null if an error occurred during setup. |

### download

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun download(request: DownloadRequest): Unit
```

Requests the download of a file or set of files that the carrier has indicated to be available. May throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` If `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#setTempFileRootDirectory(java.io.File)` has not called after the app has been installed, this method will create a directory at the default location defined at `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#DEFAULT_TOP_LEVEL_TEMP_DIRECTORY:kotlin.String` and store that as the temp file root directory. If the `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` has a destination that is not on the same filesystem as the temp file directory provided via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#getTempFileRootDirectory()`, an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown. Asynchronous errors through the callback may include any error not specific to the streaming use-case. If no error is delivered via the callback after calling this method, that means that the middleware has successfully started the download or scheduled the download, if the download is at a future time.

| Parameters ||
|---|---|
| `request` | [DownloadRequest](../android/telephony/mbms/DownloadRequest.md): The request that specifies what should be downloaded. This value cannot be `null`. |

### getMaximumServiceAnnouncementSize

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getMaximumServiceAnnouncementSize(): Int
```

Returns the maximum size of the service announcement descriptor that can be provided via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#addServiceAnnouncement(kotlin.ByteArray)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The maximum length of the byte array passed as an argument to `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#addServiceAnnouncement(kotlin.ByteArray)`. |

### getTempFileRootDirectory

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTempFileRootDirectory(): File?
```

Retrieves the currently configured temp file root directory. Returns the file that was configured via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#setTempFileRootDirectory(java.io.File)` or the default directory `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#download(android.telephony.mbms.DownloadRequest)` was called without ever setting the temp file root. If neither method has been called since the last time the app's shared preferences were reset, returns `null`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/File.html#?` | A `https://developer.android.com/reference/kotlin/java/io/File.html#` pointing to the configured temp file directory, or null if not yet configured. |

### listPendingDownloads

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun listPendingDownloads(): MutableList<DownloadRequest!>
```

Returns a list of pending `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest`s that originated from this application. A pending request is one that was issued via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#download(android.telephony.mbms.DownloadRequest)` but not cancelled through `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#cancelDownload(android.telephony.mbms.DownloadRequest)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest!>` | A list, possibly empty, of `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest`s. This value cannot be `null`. |

### removeProgressListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeProgressListener(
    request: DownloadRequest, 
    listener: DownloadProgressListener
): Unit
```

Un-register a listener previously registered via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#addProgressListener(android.telephony.mbms.DownloadRequest,%20java.util.concurrent.Executor,%20android.telephony.mbms.DownloadProgressListener)`. After this method is called, no further callbacks will be enqueued on the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` provided upon registration, even if this method throws an exception. If the middleware is not aware of the specified download request, this method will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`. If the operation encountered an error, the error code will be delivered via `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onError(kotlin.Int,%20kotlin.String)`.

| Parameters ||
|---|---|
| `request` | [DownloadRequest](../android/telephony/mbms/DownloadRequest.md): The `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` provided during registration. This value cannot be `null`. |
| `listener` | [DownloadProgressListener](../android/telephony/mbms/DownloadProgressListener.md): The listener provided during registration. This value cannot be `null`. |

### removeStatusListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeStatusListener(
    request: DownloadRequest, 
    listener: DownloadStatusListener
): Unit
```

Un-register a listener previously registered via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#addStatusListener(android.telephony.mbms.DownloadRequest,%20java.util.concurrent.Executor,%20android.telephony.mbms.DownloadStatusListener)`. After this method is called, no further calls will be enqueued on the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` provided upon registration, even if this method throws an exception. If the middleware is not aware of the specified download request, this method will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`. If the operation encountered an error, the error code will be delivered via `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onError(kotlin.Int,%20kotlin.String)`.

| Parameters ||
|---|---|
| `request` | [DownloadRequest](../android/telephony/mbms/DownloadRequest.md): The `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest` provided during registration. This value cannot be `null`. |
| `listener` | [DownloadStatusListener](../android/telephony/mbms/DownloadStatusListener.md): The listener provided during registration. This value cannot be `null`. |

### requestDownloadState

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestDownloadState(
    downloadRequest: DownloadRequest!, 
    fileInfo: FileInfo!
): Unit
```

Requests information about the state of a file pending download. The state will be delivered as a callback via `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadStatusListener#onStatusUpdated(android.telephony.mbms.DownloadRequest,%20android.telephony.mbms.FileInfo,%20kotlin.Int)`. If no such callback has been registered via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#addProgressListener(android.telephony.mbms.DownloadRequest,%20java.util.concurrent.Executor,%20android.telephony.mbms.DownloadProgressListener)`, this method will be a no-op. If the middleware has no record of the file indicated by `fileInfo` being associated with `downloadRequest`, an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown.

| Parameters ||
|---|---|
| `downloadRequest` | [DownloadRequest](../android/telephony/mbms/DownloadRequest.md)!: The download request to query. |
| `fileInfo` | [FileInfo](../android/telephony/mbms/FileInfo.md)!: The particular file within the request to get information on. |

### requestUpdateFileServices

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestUpdateFileServices(classList: MutableList<String!>): Unit
```

An inspection API to retrieve the list of available `https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo`s currently being advertised. The results are returned asynchronously via a call to `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onFileServicesUpdated(kotlin.collections.MutableList)` Asynchronous error codes via the `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onError(kotlin.Int,%20kotlin.String)` callback may include any of the errors that are not specific to the streaming use-case. May throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` or `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

| Parameters ||
|---|---|
| `classList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: A list of service classes which the app wishes to receive `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onFileServicesUpdated(kotlin.collections.MutableList)` callbacks about. Subsequent calls to this method will replace this list of service classes (i.e. the middleware will no longer send updates for services matching classes only in the old list). Values in this list should be negotiated with the wireless carrier prior to using this API. This value cannot be `null`. |

### resetDownloadKnowledge

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resetDownloadKnowledge(downloadRequest: DownloadRequest!): Unit
```

Resets the middleware's knowledge of previously-downloaded files in this download request. Normally, the middleware keeps track of the hashes of downloaded files and won't re-download files whose server-reported hash matches one of the already-downloaded files. This means that if the file is accidentally deleted by the user or by the app, the middleware will not try to download it again. This method will reset the middleware's cache of hashes for the provided `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest`, so that previously downloaded content will be downloaded again when available. This will not interrupt in-progress downloads. This is distinct from cancelling and re-issuing the download request -- if you cancel and re-issue, the middleware will not clear its cache of download state information. If the middleware is not aware of the specified download request, an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown.

| Parameters ||
|---|---|
| `downloadRequest` | [DownloadRequest](../android/telephony/mbms/DownloadRequest.md)!: The request to re-download files for. |

### setTempFileRootDirectory

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTempFileRootDirectory(tempFileRootDirectory: File): Unit
```

Sets the temp file root for downloads. All temp files created for the middleware to write to will be contained in the specified directory. Applications that wish to specify a location only need to call this method once as long their data is persisted in storage -- the argument will be stored both in a local instance of `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` and by the middleware. If this method is not called at least once before calling `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#download(android.telephony.mbms.DownloadRequest)`, the framework will default to a directory formed by the concatenation of the app's files directory and `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#DEFAULT_TOP_LEVEL_TEMP_DIRECTORY:kotlin.String`. Before calling this method, the app must cancel all of its pending `https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest`s via `https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession#cancelDownload(android.telephony.mbms.DownloadRequest)`. If this is not done, you will receive an asynchronous error with code `https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.DownloadErrors#ERROR_CANNOT_CHANGE_TEMP_FILE_ROOT:kotlin.Int` unless the provided directory is the same as what has been previously configured. The `https://developer.android.com/reference/kotlin/java/io/File.html#` supplied as a root temp file directory must already exist. If not, an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown. In addition, as an additional correctness check, an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown if you attempt to set the temp file root directory to one of your data roots (the value of `https://developer.android.com/reference/kotlin/android/content/Context.html#getDataDir()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`, or `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()`).

| Parameters ||
|---|---|
| `tempFileRootDirectory` | [File](../java/io/File.md): A directory to place temp files in. This value cannot be `null`. |
