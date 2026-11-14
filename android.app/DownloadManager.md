# DownloadManager

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DownloadManager

Kotlin| [Java](https://developer.android.com/reference/android/app/DownloadManager "View this page in Java") 
| --- | --- |

```
open class DownloadManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.DownloadManager](https://developer.android.com/reference/kotlin/android/app/DownloadManager#) |

The download manager is a system service that handles long-running HTTP downloads. Clients may request that a URI be downloaded to a particular destination file. The download manager will conduct the download in the background, taking care of HTTP interactions and retrying downloads after failures or across connectivity changes and system reboots.

Apps that request downloads through this API should register a broadcast receiver for [ACTION_NOTIFICATION_CLICKED](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ACTION_NOTIFICATION_CLICKED:kotlin.String) to appropriately handle when the user clicks on a running download in a notification or from the downloads UI.

Note that the application must have the [android.Manifest.permission#INTERNET](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERNET:kotlin.String) permission to use this class.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Query](https://developer.android.com/reference/kotlin/android/app/DownloadManager.Query) This class may be used to filter download manager queries. |
| open | [Request](https://developer.android.com/reference/kotlin/android/app/DownloadManager.Request) This class contains all the information necessary to request a new download. |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DOWNLOAD_COMPLETE](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ACTION_DOWNLOAD_COMPLETE:kotlin.String) Broadcast intent action sent by the download manager when a download completes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_NOTIFICATION_CLICKED](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ACTION_NOTIFICATION_CLICKED:kotlin.String) Broadcast intent action sent by the download manager when the user clicks on a running download, either from a system notification or from the downloads UI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_VIEW_DOWNLOADS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ACTION_VIEW_DOWNLOADS:kotlin.String) Intent action to launch an activity to display all downloads. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_BYTES_DOWNLOADED_SO_FAR](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_BYTES_DOWNLOADED_SO_FAR:kotlin.String) Number of bytes download so far. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_DESCRIPTION](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_DESCRIPTION:kotlin.String) The client-supplied description of this download. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_ID](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_ID:kotlin.String) An identifier for a particular download, unique across the system. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_LAST_MODIFIED_TIMESTAMP](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_LAST_MODIFIED_TIMESTAMP:kotlin.String) Timestamp when the download was last modified, in [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis())(wall clock time in UTC). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_LOCAL_FILENAME](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_LOCAL_FILENAME:kotlin.String) Path to the downloaded file on disk. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_LOCAL_URI](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_LOCAL_URI:kotlin.String) Uri where downloaded file will be stored. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_MEDIAPROVIDER_URI](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_MEDIAPROVIDER_URI:kotlin.String) The URI to the corresponding entry in MediaProvider for this downloaded entry. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_MEDIA_TYPE](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_MEDIA_TYPE:kotlin.String) Internet Media Type of the downloaded file. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) Provides more detail on the status of the download. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) Current status of the download, as one of the STATUS_\* constants. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_TITLE](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_TITLE:kotlin.String) The client-supplied title for this download. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_TOTAL_SIZE_BYTES](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_TOTAL_SIZE_BYTES:kotlin.String) Total size of the download in bytes. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_URI](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_URI:kotlin.String) URI to be downloaded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CANNOT_RESUME](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ERROR_CANNOT_RESUME:kotlin.Int) Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when some possibly transient error occurred but we can't resume the download. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEVICE_NOT_FOUND](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ERROR_DEVICE_NOT_FOUND:kotlin.Int) Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when no external storage device was found. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_FILE_ALREADY_EXISTS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ERROR_FILE_ALREADY_EXISTS:kotlin.Int) Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when the requested destination file already exists (the download manager will not overwrite an existing file). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_FILE_ERROR](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ERROR_FILE_ERROR:kotlin.Int) Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when a storage issue arises which doesn't fit under any other error code. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_HTTP_DATA_ERROR](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ERROR_HTTP_DATA_ERROR:kotlin.Int) Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when an error receiving or processing data occurred at the HTTP level. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INSUFFICIENT_SPACE](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ERROR_INSUFFICIENT_SPACE:kotlin.Int) Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when there was insufficient storage space. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TOO_MANY_REDIRECTS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ERROR_TOO_MANY_REDIRECTS:kotlin.Int) Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when there were too many redirects. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNHANDLED_HTTP_CODE](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ERROR_UNHANDLED_HTTP_CODE:kotlin.Int) Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when an HTTP code was received that download manager can't handle. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ERROR_UNKNOWN:kotlin.Int) Value of COLUMN_ERROR_CODE when the download has completed with an error that doesn't fit under any other error code. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DOWNLOAD_ID](https://developer.android.com/reference/kotlin/android/app/DownloadManager#EXTRA_DOWNLOAD_ID:kotlin.String) Intent extra included with [ACTION_DOWNLOAD_COMPLETE](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ACTION_DOWNLOAD_COMPLETE:kotlin.String) intents, indicating the ID (as a long) of the download that just completed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_NOTIFICATION_CLICK_DOWNLOAD_IDS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#EXTRA_NOTIFICATION_CLICK_DOWNLOAD_IDS:kotlin.String) When clicks on multiple notifications are received, the following provides an array of download ids corresponding to the download notification that was clicked. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_EXTRAS_SORT_BY_SIZE](https://developer.android.com/reference/kotlin/android/app/DownloadManager#INTENT_EXTRAS_SORT_BY_SIZE:kotlin.String) Intent extra included with [ACTION_VIEW_DOWNLOADS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ACTION_VIEW_DOWNLOADS:kotlin.String) to start DownloadApp in sort-by-size mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAUSED_QUEUED_FOR_WIFI](https://developer.android.com/reference/kotlin/android/app/DownloadManager#PAUSED_QUEUED_FOR_WIFI:kotlin.Int) Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when the download exceeds a size limit for downloads over the mobile network and the download manager is waiting for a Wi-Fi connection to proceed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAUSED_UNKNOWN](https://developer.android.com/reference/kotlin/android/app/DownloadManager#PAUSED_UNKNOWN:kotlin.Int) Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when the download is paused for some other reason. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAUSED_WAITING_FOR_NETWORK](https://developer.android.com/reference/kotlin/android/app/DownloadManager#PAUSED_WAITING_FOR_NETWORK:kotlin.Int) Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when the download is waiting for network connectivity to proceed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAUSED_WAITING_TO_RETRY](https://developer.android.com/reference/kotlin/android/app/DownloadManager#PAUSED_WAITING_TO_RETRY:kotlin.Int) Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when the download is paused because some network error occurred and the download manager is waiting before retrying the request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILED](https://developer.android.com/reference/kotlin/android/app/DownloadManager#STATUS_FAILED:kotlin.Int) Value of [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) when the download has failed (and will not be retried). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_PAUSED](https://developer.android.com/reference/kotlin/android/app/DownloadManager#STATUS_PAUSED:kotlin.Int) Value of [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) when the download is waiting to retry or resume. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_PENDING](https://developer.android.com/reference/kotlin/android/app/DownloadManager#STATUS_PENDING:kotlin.Int) Value of [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) when the download is waiting to start. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_RUNNING](https://developer.android.com/reference/kotlin/android/app/DownloadManager#STATUS_RUNNING:kotlin.Int) Value of [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) when the download is currently running. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_SUCCESSFUL](https://developer.android.com/reference/kotlin/android/app/DownloadManager#STATUS_SUCCESSFUL:kotlin.Int) Value of [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) when the download has successfully completed. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [addCompletedDownload](https://developer.android.com/reference/kotlin/android/app/DownloadManager#addCompletedDownload(kotlin.String,%20kotlin.String,%20kotlin.Boolean,%20kotlin.String,%20kotlin.String,%20kotlin.Long,%20kotlin.Boolean))`(`title:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `isMediaScannerScannable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `showNotification:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Adds a file to the downloads database system, so it could appear in Downloads App (and thus become eligible for management by the Downloads App). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [addCompletedDownload](https://developer.android.com/reference/kotlin/android/app/DownloadManager#addCompletedDownload(kotlin.String,%20kotlin.String,%20kotlin.Boolean,%20kotlin.String,%20kotlin.String,%20kotlin.Long,%20kotlin.Boolean,%20android.net.Uri,%20android.net.Uri))`(`title:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `isMediaScannerScannable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `showNotification:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `referer:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Adds a file to the downloads database system, so it could appear in Downloads App (and thus become eligible for management by the Downloads App). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [enqueue](https://developer.android.com/reference/kotlin/android/app/DownloadManager#enqueue(android.app.DownloadManager.Request))`(`request:` ` [DownloadManager.Request](https://developer.android.com/reference/kotlin/android/app/DownloadManager.Request)!`)` Enqueue a new download. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)! | [getMaxBytesOverMobile](https://developer.android.com/reference/kotlin/android/app/DownloadManager#getMaxBytesOverMobile(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Returns maximum size, in bytes, of downloads that may go over a mobile connection; or null if there's no limit |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMimeTypeForDownloadedFile](https://developer.android.com/reference/kotlin/android/app/DownloadManager#getMimeTypeForDownloadedFile(kotlin.Long))`(`id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the media type of the given downloaded file id, if the file was downloaded successfully. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)! | [getRecommendedMaxBytesOverMobile](https://developer.android.com/reference/kotlin/android/app/DownloadManager#getRecommendedMaxBytesOverMobile(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Returns recommended maximum size, in bytes, of downloads that may go over a mobile connection; or null if there's no recommended limit. |
| --- | --- |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [getUriForDownloadedFile](https://developer.android.com/reference/kotlin/android/app/DownloadManager#getUriForDownloadedFile(kotlin.Long))`(`id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) of the given downloaded file id, if the file is downloaded successfully. |
| open [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)! | [openDownloadedFile](https://developer.android.com/reference/kotlin/android/app/DownloadManager#openDownloadedFile(kotlin.Long))`(`id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Open a downloaded file for reading. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [query](https://developer.android.com/reference/kotlin/android/app/DownloadManager#query(android.app.DownloadManager.Query))`(`query:` ` [DownloadManager.Query](https://developer.android.com/reference/kotlin/android/app/DownloadManager.Query)!`)` Query the download manager about downloads that have been requested. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remove](https://developer.android.com/reference/kotlin/android/app/DownloadManager#remove(kotlin.Long))`(`vararg` `ids:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Cancel downloads and remove them from the download manager. |

## Constants

### ACTION_DOWNLOAD_COMPLETE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_DOWNLOAD_COMPLETE: String
```

Broadcast intent action sent by the download manager when a download completes. 

 Value: "android.intent.action.DOWNLOAD_COMPLETE"

### ACTION_NOTIFICATION_CLICKED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_NOTIFICATION_CLICKED: String
```

Broadcast intent action sent by the download manager when the user clicks on a running download, either from a system notification or from the downloads UI. 

 Value: "android.intent.action.DOWNLOAD_NOTIFICATION_CLICKED"

### ACTION_VIEW_DOWNLOADS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_VIEW_DOWNLOADS: String
```

Intent action to launch an activity to display all downloads. 

 Value: "android.intent.action.VIEW_DOWNLOADS"

### COLUMN_BYTES_DOWNLOADED_SO_FAR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_BYTES_DOWNLOADED_SO_FAR: String
```

Number of bytes download so far. 

 Value: "bytes_so_far"

### COLUMN_DESCRIPTION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_DESCRIPTION: String
```

The client-supplied description of this download. This will be displayed in system notifications. Defaults to the empty string. 

 Value: "description"

### COLUMN_ID

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_ID: String
```

An identifier for a particular download, unique across the system. Clients use this ID to make subsequent calls related to the download. 

 Value: "_id"

### COLUMN_LAST_MODIFIED_TIMESTAMP

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_LAST_MODIFIED_TIMESTAMP: String
```

Timestamp when the download was last modified, in [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis())(wall clock time in UTC). 

 Value: "last_modified_timestamp"

### COLUMN_LOCAL_FILENAME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_LOCAL_FILENAME: String
```

**Deprecated:** *apps should transition to using [ContentResolver.openFileDescriptor(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String))instead.*

Path to the downloaded file on disk.

Note that apps may not have filesystem permissions to directly access this path. Instead of trying to open this path directly, apps should use [ContentResolver.openFileDescriptor(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String))to gain access. 

 Value: "local_filename"

### COLUMN_LOCAL_URI

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_LOCAL_URI: String
```

Uri where downloaded file will be stored. If a destination is supplied by client, that URI will be used here. Otherwise, the value will initially be null and will be filled in with a generated URI once the download has started. 

 Value: "local_uri"

### COLUMN_MEDIAPROVIDER_URI

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_MEDIAPROVIDER_URI: String
```

The URI to the corresponding entry in MediaProvider for this downloaded entry. It is used to delete the entries from MediaProvider database when it is deleted from the downloaded list. 

 Value: "mediaprovider_uri"

### COLUMN_MEDIA_TYPE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_MEDIA_TYPE: String
```

Internet Media Type of the downloaded file. If no value is provided upon creation, this will initially be null and will be filled in based on the server's response once the download has started. 

 Value: "media_type"

**See Also**

### COLUMN_REASON

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_REASON: String
```

Provides more detail on the status of the download. Its meaning depends on the value of [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String). When [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) is [STATUS_FAILED](https://developer.android.com/reference/kotlin/android/app/DownloadManager#STATUS_FAILED:kotlin.Int), this indicates the type of error that occurred. If an HTTP error occurred, this will hold the HTTP status code as defined in RFC 2616. Otherwise, it will hold one of the ERROR_\* constants. When [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) is [STATUS_PAUSED](https://developer.android.com/reference/kotlin/android/app/DownloadManager#STATUS_PAUSED:kotlin.Int), this indicates why the download is paused. It will hold one of the PAUSED_\* constants. If [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) is neither [STATUS_FAILED](https://developer.android.com/reference/kotlin/android/app/DownloadManager#STATUS_FAILED:kotlin.Int) nor [STATUS_PAUSED](https://developer.android.com/reference/kotlin/android/app/DownloadManager#STATUS_PAUSED:kotlin.Int), this column's value is undefined. 

 Value: "reason"

**See Also**

### COLUMN_STATUS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_STATUS: String
```

Current status of the download, as one of the STATUS_\* constants. 

 Value: "status"

### COLUMN_TITLE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_TITLE: String
```

The client-supplied title for this download. This will be displayed in system notifications. Defaults to the empty string. 

 Value: "title"

### COLUMN_TOTAL_SIZE_BYTES

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_TOTAL_SIZE_BYTES: String
```

Total size of the download in bytes. This will initially be -1 and will be filled in once the download starts. 

 Value: "total_size"

### COLUMN_URI

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_URI: String
```

URI to be downloaded. 

 Value: "uri"

### ERROR_CANNOT_RESUME

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CANNOT_RESUME: Int
```

Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when some possibly transient error occurred but we can't resume the download. 

 Value: 1008

### ERROR_DEVICE_NOT_FOUND

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DEVICE_NOT_FOUND: Int
```

Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when no external storage device was found. Typically, this is because the SD card is not mounted. 

 Value: 1007

### ERROR_FILE_ALREADY_EXISTS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_FILE_ALREADY_EXISTS: Int
```

Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when the requested destination file already exists (the download manager will not overwrite an existing file). 

 Value: 1009

### ERROR_FILE_ERROR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_FILE_ERROR: Int
```

Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when a storage issue arises which doesn't fit under any other error code. Use the more specific [ERROR_INSUFFICIENT_SPACE](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ERROR_INSUFFICIENT_SPACE:kotlin.Int) and [ERROR_DEVICE_NOT_FOUND](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ERROR_DEVICE_NOT_FOUND:kotlin.Int) when appropriate. 

 Value: 1001

### ERROR_HTTP_DATA_ERROR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_HTTP_DATA_ERROR: Int
```

Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when an error receiving or processing data occurred at the HTTP level. 

 Value: 1004

### ERROR_INSUFFICIENT_SPACE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INSUFFICIENT_SPACE: Int
```

Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when there was insufficient storage space. Typically, this is because the SD card is full. 

 Value: 1006

### ERROR_TOO_MANY_REDIRECTS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TOO_MANY_REDIRECTS: Int
```

Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when there were too many redirects. 

 Value: 1005

### ERROR_UNHANDLED_HTTP_CODE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNHANDLED_HTTP_CODE: Int
```

Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when an HTTP code was received that download manager can't handle. 

 Value: 1002

### ERROR_UNKNOWN

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNKNOWN: Int
```

Value of COLUMN_ERROR_CODE when the download has completed with an error that doesn't fit under any other error code. 

 Value: 1000

### EXTRA_DOWNLOAD_ID

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DOWNLOAD_ID: String
```

Intent extra included with [ACTION_DOWNLOAD_COMPLETE](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ACTION_DOWNLOAD_COMPLETE:kotlin.String) intents, indicating the ID (as a long) of the download that just completed. 

 Value: "extra_download_id"

### EXTRA_NOTIFICATION_CLICK_DOWNLOAD_IDS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_NOTIFICATION_CLICK_DOWNLOAD_IDS: String
```

When clicks on multiple notifications are received, the following provides an array of download ids corresponding to the download notification that was clicked. It can be retrieved by the receiver of this Intent using [android.content.Intent#getLongArrayExtra(String)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getLongArrayExtra(kotlin.String)). 

 Value: "extra_click_download_ids"

### INTENT_EXTRAS_SORT_BY_SIZE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_EXTRAS_SORT_BY_SIZE: String
```

Intent extra included with [ACTION_VIEW_DOWNLOADS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#ACTION_VIEW_DOWNLOADS:kotlin.String) to start DownloadApp in sort-by-size mode. 

 Value: "android.app.DownloadManager.extra_sortBySize"

### PAUSED_QUEUED_FOR_WIFI

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAUSED_QUEUED_FOR_WIFI: Int
```

Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when the download exceeds a size limit for downloads over the mobile network and the download manager is waiting for a Wi-Fi connection to proceed. 

 Value: 3

### PAUSED_UNKNOWN

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAUSED_UNKNOWN: Int
```

Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when the download is paused for some other reason. 

 Value: 4

### PAUSED_WAITING_FOR_NETWORK

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAUSED_WAITING_FOR_NETWORK: Int
```

Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when the download is waiting for network connectivity to proceed. 

 Value: 2

### PAUSED_WAITING_TO_RETRY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAUSED_WAITING_TO_RETRY: Int
```

Value of [COLUMN_REASON](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_REASON:kotlin.String) when the download is paused because some network error occurred and the download manager is waiting before retrying the request. 

 Value: 1

### STATUS_FAILED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILED: Int
```

Value of [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) when the download has failed (and will not be retried). 

 Value: 16

### STATUS_PAUSED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_PAUSED: Int
```

Value of [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) when the download is waiting to retry or resume. 

 Value: 4

### STATUS_PENDING

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_PENDING: Int
```

Value of [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) when the download is waiting to start. 

 Value: 1

### STATUS_RUNNING

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_RUNNING: Int
```

Value of [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) when the download is currently running. 

 Value: 2

### STATUS_SUCCESSFUL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_SUCCESSFUL: Int
```

Value of [COLUMN_STATUS](https://developer.android.com/reference/kotlin/android/app/DownloadManager#COLUMN_STATUS:kotlin.String) when the download has successfully completed. 

 Value: 8

## Public methods

### addCompletedDownload

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addCompletedDownload(
    title: String!, 
    description: String!, 
    isMediaScannerScannable: Boolean, 
    mimeType: String!, 
    path: String!, 
    length: Long, 
    showNotification: Boolean
): Long
```

**Deprecated:** *Apps should instead contribute files to [android.provider.MediaStore.Downloads](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Downloads.html#) collection to make them available to user as part of Downloads.*

Adds a file to the downloads database system, so it could appear in Downloads App (and thus become eligible for management by the Downloads App).

It is helpful to make the file scannable by MediaScanner by setting the param isMediaScannerScannable to true. It makes the file visible in media managing applications such as Gallery App, which could be a useful purpose of using this API.

For applications targeting [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int) or above,`path`must be within directories owned by the application {e.g. [Context.getExternalFilesDir(String)](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDir(kotlin.String))} or if the application is running under the legacy storage model (see [android:requestLegacyExternalStorage](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_requestLegacyExternalStorage:kotlin.Int)),`path`can also be within the top-level Downloads directory (as returned by [Environment.getExternalStoragePublicDirectory(String)](https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStoragePublicDirectory(kotlin.String))with [Environment.DIRECTORY_DOWNLOADS](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_DOWNLOADS:kotlin.String)).

| Parameters ||
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `title` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the title that would appear for this file in Downloads App. |
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the description that would appear for this file in Downloads App. |
| `isMediaScannerScannable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the file is to be scanned by MediaScanner. Files scanned by MediaScanner appear in the applications used to view media (for example, Gallery app). |
| --- | --- |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:mimetype of the file. |
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:absolute pathname to the file. The file should be world-readable, so that it can be managed by the Downloads App and any other app that is used to read it (for example, Gallery app to display the file, if the file contents represent a video/image). |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):length of the downloaded file |
| --- | --- |
| `showNotification` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if a notification is to be sent, false otherwise |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | an ID for the download entry added to the downloads app, unique across the system This ID is used to make future calls related to this download. |

### addCompletedDownload

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addCompletedDownload(
    title: String!, 
    description: String!, 
    isMediaScannerScannable: Boolean, 
    mimeType: String!, 
    path: String!, 
    length: Long, 
    showNotification: Boolean, 
    uri: Uri!, 
    referer: Uri!
): Long
```

**Deprecated:** *Apps should instead contribute files to [android.provider.MediaStore.Downloads](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Downloads.html#) collection to make them available to user as part of Downloads.*

Adds a file to the downloads database system, so it could appear in Downloads App (and thus become eligible for management by the Downloads App).

It is helpful to make the file scannable by MediaScanner by setting the param isMediaScannerScannable to true. It makes the file visible in media managing applications such as Gallery App, which could be a useful purpose of using this API.

For applications targeting [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int) or above,`path`must be within directories owned by the application {e.g. [Context.getExternalFilesDir(String)](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDir(kotlin.String))} or if the application is running under the legacy storage model (see [android:requestLegacyExternalStorage](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_requestLegacyExternalStorage:kotlin.Int)),`path`can also be within the top-level Downloads directory (as returned by [Environment.getExternalStoragePublicDirectory(String)](https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStoragePublicDirectory(kotlin.String))with [Environment.DIRECTORY_DOWNLOADS](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_DOWNLOADS:kotlin.String)).

| Parameters ||
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `title` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the title that would appear for this file in Downloads App. |
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the description that would appear for this file in Downloads App. |
| `isMediaScannerScannable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the file is to be scanned by MediaScanner. Files scanned by MediaScanner appear in the applications used to view media (for example, Gallery app). |
| --- | --- |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:mimetype of the file. |
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:absolute pathname to the file. The file should be world-readable, so that it can be managed by the Downloads App and any other app that is used to read it (for example, Gallery app to display the file, if the file contents represent a video/image). |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):length of the downloaded file |
| --- | --- |
| `showNotification` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if a notification is to be sent, false otherwise |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:the original HTTP URI of the download |
| `referer` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:the HTTP Referer for the download |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | an ID for the download entry added to the downloads app, unique across the system This ID is used to make future calls related to this download. |

### enqueue

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enqueue(request: DownloadManager.Request!): Long
```

Enqueue a new download. The download will start automatically once the download manager is ready to execute it and connectivity is available.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [DownloadManager.Request](https://developer.android.com/reference/kotlin/android/app/DownloadManager.Request)!:the parameters specifying this download |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | an ID for the download, unique across the system. This ID is used to make future calls related to this download. Returns -1 if the operation fails. |

### getMaxBytesOverMobile

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMaxBytesOverMobile(context: Context!): Long!
```

Returns maximum size, in bytes, of downloads that may go over a mobile connection; or null if there's no limit

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) to use for accessing the [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#) |

| Return ||
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)! | maximum size, in bytes, of downloads that may go over a mobile connection; or null if there's no limit |

### getMimeTypeForDownloadedFile

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMimeTypeForDownloadedFile(id: Long): String!
```

Returns the media type of the given downloaded file id, if the file was downloaded successfully. Otherwise, null is returned.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------|
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the id of the downloaded file. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the media type of the given downloaded file id, if download was successful. null otherwise. |

### getRecommendedMaxBytesOverMobile

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRecommendedMaxBytesOverMobile(context: Context!): Long!
```

Returns recommended maximum size, in bytes, of downloads that may go over a mobile connection; or null if there's no recommended limit. The user will have the option to bypass this limit.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) to use for accessing the [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#) |

| Return ||
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)! | recommended maximum size, in bytes, of downloads that may go over a mobile connection; or null if there's no recommended limit. |

### getUriForDownloadedFile

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUriForDownloadedFile(id: Long): Uri!
```

Returns the [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) of the given downloaded file id, if the file is downloaded successfully. Otherwise, null is returned.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------|
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the id of the downloaded file. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | the [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) of the given downloaded file id, if download was successful. null otherwise. |

### openDownloadedFile

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openDownloadedFile(id: Long): ParcelFileDescriptor!
```

Open a downloaded file for reading. The download must have completed.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------|
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the ID of the download |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)! | a read-only [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) |

| Exceptions ||
|---------------------------------|------------------------------------------------|
| `java.io.FileNotFoundException` | if the destination file does not already exist |

### query

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun query(query: DownloadManager.Query!): Cursor!
```

Query the download manager about downloads that have been requested.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `query` | [DownloadManager.Query](https://developer.android.com/reference/kotlin/android/app/DownloadManager.Query)!:parameters specifying filters for this query |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | a Cursor over the result set of downloads, with columns consisting of all the COLUMN_\* constants. |

### remove

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(vararg ids: Long): Int
```

Cancel downloads and remove them from the download manager. Each download will be stopped if it was running, and it will no longer be accessible through the download manager. If there is a downloaded file, partial or complete, it is deleted.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------|
| `ids` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the IDs of the downloads to remove |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of downloads actually removed |
