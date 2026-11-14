# DownloadManager

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DownloadManager

Kotlin| [Java](DownloadManager.md) 
| --- | --- |

```
open class DownloadManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.DownloadManager](DownloadManager.md) |

The download manager is a system service that handles long-running HTTP downloads. Clients may request that a URI be downloaded to a particular destination file. The download manager will conduct the download in the background, taking care of HTTP interactions and retrying downloads after failures or across connectivity changes and system reboots.

Apps that request downloads through this API should register a broadcast receiver for [ACTION_NOTIFICATION_CLICKED](DownloadManager.md) to appropriately handle when the user clicks on a running download in a notification or from the downloads UI.

Note that the application must have the [android.Manifest.permission#INTERNET](../android/Manifest.permission.md) permission to use this class.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Query](../android/app/DownloadManager.Query.md) This class may be used to filter download manager queries. |
| open | [Request](../android/app/DownloadManager.Request.md) This class contains all the information necessary to request a new download. |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DOWNLOAD_COMPLETE](DownloadManager.md) Broadcast intent action sent by the download manager when a download completes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_NOTIFICATION_CLICKED](DownloadManager.md) Broadcast intent action sent by the download manager when the user clicks on a running download, either from a system notification or from the downloads UI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_VIEW_DOWNLOADS](DownloadManager.md) Intent action to launch an activity to display all downloads. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_BYTES_DOWNLOADED_SO_FAR](DownloadManager.md) Number of bytes download so far. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_DESCRIPTION](DownloadManager.md) The client-supplied description of this download. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_ID](DownloadManager.md) An identifier for a particular download, unique across the system. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_LAST_MODIFIED_TIMESTAMP](DownloadManager.md) Timestamp when the download was last modified, in [System.currentTimeMillis()](../java.lang/System.md))(wall clock time in UTC). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_LOCAL_FILENAME](DownloadManager.md) Path to the downloaded file on disk. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_LOCAL_URI](DownloadManager.md) Uri where downloaded file will be stored. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_MEDIAPROVIDER_URI](DownloadManager.md) The URI to the corresponding entry in MediaProvider for this downloaded entry. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_MEDIA_TYPE](DownloadManager.md) Internet Media Type of the downloaded file. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_REASON](DownloadManager.md) Provides more detail on the status of the download. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_STATUS](DownloadManager.md) Current status of the download, as one of the STATUS_\* constants. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_TITLE](DownloadManager.md) The client-supplied title for this download. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_TOTAL_SIZE_BYTES](DownloadManager.md) Total size of the download in bytes. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_URI](DownloadManager.md) URI to be downloaded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CANNOT_RESUME](DownloadManager.md) Value of [COLUMN_REASON](DownloadManager.md) when some possibly transient error occurred but we can't resume the download. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEVICE_NOT_FOUND](DownloadManager.md) Value of [COLUMN_REASON](DownloadManager.md) when no external storage device was found. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_FILE_ALREADY_EXISTS](DownloadManager.md) Value of [COLUMN_REASON](DownloadManager.md) when the requested destination file already exists (the download manager will not overwrite an existing file). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_FILE_ERROR](DownloadManager.md) Value of [COLUMN_REASON](DownloadManager.md) when a storage issue arises which doesn't fit under any other error code. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_HTTP_DATA_ERROR](DownloadManager.md) Value of [COLUMN_REASON](DownloadManager.md) when an error receiving or processing data occurred at the HTTP level. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INSUFFICIENT_SPACE](DownloadManager.md) Value of [COLUMN_REASON](DownloadManager.md) when there was insufficient storage space. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TOO_MANY_REDIRECTS](DownloadManager.md) Value of [COLUMN_REASON](DownloadManager.md) when there were too many redirects. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNHANDLED_HTTP_CODE](DownloadManager.md) Value of [COLUMN_REASON](DownloadManager.md) when an HTTP code was received that download manager can't handle. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](DownloadManager.md) Value of COLUMN_ERROR_CODE when the download has completed with an error that doesn't fit under any other error code. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DOWNLOAD_ID](DownloadManager.md) Intent extra included with [ACTION_DOWNLOAD_COMPLETE](DownloadManager.md) intents, indicating the ID (as a long) of the download that just completed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_NOTIFICATION_CLICK_DOWNLOAD_IDS](DownloadManager.md) When clicks on multiple notifications are received, the following provides an array of download ids corresponding to the download notification that was clicked. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_EXTRAS_SORT_BY_SIZE](DownloadManager.md) Intent extra included with [ACTION_VIEW_DOWNLOADS](DownloadManager.md) to start DownloadApp in sort-by-size mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAUSED_QUEUED_FOR_WIFI](DownloadManager.md) Value of [COLUMN_REASON](DownloadManager.md) when the download exceeds a size limit for downloads over the mobile network and the download manager is waiting for a Wi-Fi connection to proceed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAUSED_UNKNOWN](DownloadManager.md) Value of [COLUMN_REASON](DownloadManager.md) when the download is paused for some other reason. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAUSED_WAITING_FOR_NETWORK](DownloadManager.md) Value of [COLUMN_REASON](DownloadManager.md) when the download is waiting for network connectivity to proceed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAUSED_WAITING_TO_RETRY](DownloadManager.md) Value of [COLUMN_REASON](DownloadManager.md) when the download is paused because some network error occurred and the download manager is waiting before retrying the request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILED](DownloadManager.md) Value of [COLUMN_STATUS](DownloadManager.md) when the download has failed (and will not be retried). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_PAUSED](DownloadManager.md) Value of [COLUMN_STATUS](DownloadManager.md) when the download is waiting to retry or resume. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_PENDING](DownloadManager.md) Value of [COLUMN_STATUS](DownloadManager.md) when the download is waiting to start. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_RUNNING](DownloadManager.md) Value of [COLUMN_STATUS](DownloadManager.md) when the download is currently running. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_SUCCESSFUL](DownloadManager.md) Value of [COLUMN_STATUS](DownloadManager.md) when the download has successfully completed. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [addCompletedDownload](DownloadManager.md))`(`title:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `isMediaScannerScannable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `showNotification:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Adds a file to the downloads database system, so it could appear in Downloads App (and thus become eligible for management by the Downloads App). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [addCompletedDownload](DownloadManager.md))`(`title:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `isMediaScannerScannable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `showNotification:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `uri:` ` [Uri](../android.net/Uri.md)!`, `referer:` ` [Uri](../android.net/Uri.md)!`)` Adds a file to the downloads database system, so it could appear in Downloads App (and thus become eligible for management by the Downloads App). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [enqueue](DownloadManager.md))`(`request:` ` [DownloadManager.Request](../android/app/DownloadManager.Request.md)!`)` Enqueue a new download. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)! | [getMaxBytesOverMobile](DownloadManager.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Returns maximum size, in bytes, of downloads that may go over a mobile connection; or null if there's no limit |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMimeTypeForDownloadedFile](DownloadManager.md))`(`id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the media type of the given downloaded file id, if the file was downloaded successfully. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)! | [getRecommendedMaxBytesOverMobile](DownloadManager.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Returns recommended maximum size, in bytes, of downloads that may go over a mobile connection; or null if there's no recommended limit. |
| --- | --- |
| open [Uri](../android.net/Uri.md)! | [getUriForDownloadedFile](DownloadManager.md))`(`id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the [Uri](../android.net/Uri.md) of the given downloaded file id, if the file is downloaded successfully. |
| open [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)! | [openDownloadedFile](DownloadManager.md))`(`id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Open a downloaded file for reading. |
| open [Cursor](../android.database/Cursor.md)! | [query](DownloadManager.md))`(`query:` ` [DownloadManager.Query](../android/app/DownloadManager.Query.md)!`)` Query the download manager about downloads that have been requested. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remove](DownloadManager.md))`(`vararg` `ids:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Cancel downloads and remove them from the download manager. |

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

Timestamp when the download was last modified, in [System.currentTimeMillis()](../java.lang/System.md))(wall clock time in UTC). 

 Value: "last_modified_timestamp"

### COLUMN_LOCAL_FILENAME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_LOCAL_FILENAME: String
```

**Deprecated:** *apps should transition to using [ContentResolver.openFileDescriptor(Uri, String)](../android.content/ContentResolver.md))instead.*

Path to the downloaded file on disk.

Note that apps may not have filesystem permissions to directly access this path. Instead of trying to open this path directly, apps should use [ContentResolver.openFileDescriptor(Uri, String)](../android.content/ContentResolver.md))to gain access. 

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

Provides more detail on the status of the download. Its meaning depends on the value of [COLUMN_STATUS](DownloadManager.md). When [COLUMN_STATUS](DownloadManager.md) is [STATUS_FAILED](DownloadManager.md), this indicates the type of error that occurred. If an HTTP error occurred, this will hold the HTTP status code as defined in RFC 2616. Otherwise, it will hold one of the ERROR_\* constants. When [COLUMN_STATUS](DownloadManager.md) is [STATUS_PAUSED](DownloadManager.md), this indicates why the download is paused. It will hold one of the PAUSED_\* constants. If [COLUMN_STATUS](DownloadManager.md) is neither [STATUS_FAILED](DownloadManager.md) nor [STATUS_PAUSED](DownloadManager.md), this column's value is undefined. 

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

Value of [COLUMN_REASON](DownloadManager.md) when some possibly transient error occurred but we can't resume the download. 

 Value: 1008

### ERROR_DEVICE_NOT_FOUND

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DEVICE_NOT_FOUND: Int
```

Value of [COLUMN_REASON](DownloadManager.md) when no external storage device was found. Typically, this is because the SD card is not mounted. 

 Value: 1007

### ERROR_FILE_ALREADY_EXISTS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_FILE_ALREADY_EXISTS: Int
```

Value of [COLUMN_REASON](DownloadManager.md) when the requested destination file already exists (the download manager will not overwrite an existing file). 

 Value: 1009

### ERROR_FILE_ERROR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_FILE_ERROR: Int
```

Value of [COLUMN_REASON](DownloadManager.md) when a storage issue arises which doesn't fit under any other error code. Use the more specific [ERROR_INSUFFICIENT_SPACE](DownloadManager.md) and [ERROR_DEVICE_NOT_FOUND](DownloadManager.md) when appropriate. 

 Value: 1001

### ERROR_HTTP_DATA_ERROR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_HTTP_DATA_ERROR: Int
```

Value of [COLUMN_REASON](DownloadManager.md) when an error receiving or processing data occurred at the HTTP level. 

 Value: 1004

### ERROR_INSUFFICIENT_SPACE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INSUFFICIENT_SPACE: Int
```

Value of [COLUMN_REASON](DownloadManager.md) when there was insufficient storage space. Typically, this is because the SD card is full. 

 Value: 1006

### ERROR_TOO_MANY_REDIRECTS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TOO_MANY_REDIRECTS: Int
```

Value of [COLUMN_REASON](DownloadManager.md) when there were too many redirects. 

 Value: 1005

### ERROR_UNHANDLED_HTTP_CODE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNHANDLED_HTTP_CODE: Int
```

Value of [COLUMN_REASON](DownloadManager.md) when an HTTP code was received that download manager can't handle. 

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

Intent extra included with [ACTION_DOWNLOAD_COMPLETE](DownloadManager.md) intents, indicating the ID (as a long) of the download that just completed. 

 Value: "extra_download_id"

### EXTRA_NOTIFICATION_CLICK_DOWNLOAD_IDS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_NOTIFICATION_CLICK_DOWNLOAD_IDS: String
```

When clicks on multiple notifications are received, the following provides an array of download ids corresponding to the download notification that was clicked. It can be retrieved by the receiver of this Intent using [android.content.Intent#getLongArrayExtra(String)](../android.content/Intent.md)). 

 Value: "extra_click_download_ids"

### INTENT_EXTRAS_SORT_BY_SIZE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_EXTRAS_SORT_BY_SIZE: String
```

Intent extra included with [ACTION_VIEW_DOWNLOADS](DownloadManager.md) to start DownloadApp in sort-by-size mode. 

 Value: "android.app.DownloadManager.extra_sortBySize"

### PAUSED_QUEUED_FOR_WIFI

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAUSED_QUEUED_FOR_WIFI: Int
```

Value of [COLUMN_REASON](DownloadManager.md) when the download exceeds a size limit for downloads over the mobile network and the download manager is waiting for a Wi-Fi connection to proceed. 

 Value: 3

### PAUSED_UNKNOWN

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAUSED_UNKNOWN: Int
```

Value of [COLUMN_REASON](DownloadManager.md) when the download is paused for some other reason. 

 Value: 4

### PAUSED_WAITING_FOR_NETWORK

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAUSED_WAITING_FOR_NETWORK: Int
```

Value of [COLUMN_REASON](DownloadManager.md) when the download is waiting for network connectivity to proceed. 

 Value: 2

### PAUSED_WAITING_TO_RETRY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAUSED_WAITING_TO_RETRY: Int
```

Value of [COLUMN_REASON](DownloadManager.md) when the download is paused because some network error occurred and the download manager is waiting before retrying the request. 

 Value: 1

### STATUS_FAILED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILED: Int
```

Value of [COLUMN_STATUS](DownloadManager.md) when the download has failed (and will not be retried). 

 Value: 16

### STATUS_PAUSED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_PAUSED: Int
```

Value of [COLUMN_STATUS](DownloadManager.md) when the download is waiting to retry or resume. 

 Value: 4

### STATUS_PENDING

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_PENDING: Int
```

Value of [COLUMN_STATUS](DownloadManager.md) when the download is waiting to start. 

 Value: 1

### STATUS_RUNNING

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_RUNNING: Int
```

Value of [COLUMN_STATUS](DownloadManager.md) when the download is currently running. 

 Value: 2

### STATUS_SUCCESSFUL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_SUCCESSFUL: Int
```

Value of [COLUMN_STATUS](DownloadManager.md) when the download has successfully completed. 

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

**Deprecated:** *Apps should instead contribute files to [android.provider.MediaStore.Downloads](../android/provider/MediaStore.Downloads.md) collection to make them available to user as part of Downloads.*

Adds a file to the downloads database system, so it could appear in Downloads App (and thus become eligible for management by the Downloads App).

It is helpful to make the file scannable by MediaScanner by setting the param isMediaScannerScannable to true. It makes the file visible in media managing applications such as Gallery App, which could be a useful purpose of using this API.

For applications targeting [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md) or above,`path`must be within directories owned by the application {e.g. [Context.getExternalFilesDir(String)](../android.content/Context.md))} or if the application is running under the legacy storage model (see [android:requestLegacyExternalStorage](../android/R.styleable.md)),`path`can also be within the top-level Downloads directory (as returned by [Environment.getExternalStoragePublicDirectory(String)](../android.os/Environment.md))with [Environment.DIRECTORY_DOWNLOADS](../android.os/Environment.md)).

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

**Deprecated:** *Apps should instead contribute files to [android.provider.MediaStore.Downloads](../android/provider/MediaStore.Downloads.md) collection to make them available to user as part of Downloads.*

Adds a file to the downloads database system, so it could appear in Downloads App (and thus become eligible for management by the Downloads App).

It is helpful to make the file scannable by MediaScanner by setting the param isMediaScannerScannable to true. It makes the file visible in media managing applications such as Gallery App, which could be a useful purpose of using this API.

For applications targeting [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md) or above,`path`must be within directories owned by the application {e.g. [Context.getExternalFilesDir(String)](../android.content/Context.md))} or if the application is running under the legacy storage model (see [android:requestLegacyExternalStorage](../android/R.styleable.md)),`path`can also be within the top-level Downloads directory (as returned by [Environment.getExternalStoragePublicDirectory(String)](../android.os/Environment.md))with [Environment.DIRECTORY_DOWNLOADS](../android.os/Environment.md)).

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
| `uri` | [Uri](../android.net/Uri.md)!:the original HTTP URI of the download |
| `referer` | [Uri](../android.net/Uri.md)!:the HTTP Referer for the download |
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
| `request` | [DownloadManager.Request](../android/app/DownloadManager.Request.md)!:the parameters specifying this download |

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
| `context` | [Context](../android.content/Context.md)!:the [Context](../android.content/Context.md) to use for accessing the [ContentResolver](../android.content/ContentResolver.md) |

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
| `context` | [Context](../android.content/Context.md)!:the [Context](../android.content/Context.md) to use for accessing the [ContentResolver](../android.content/ContentResolver.md) |

| Return ||
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)! | recommended maximum size, in bytes, of downloads that may go over a mobile connection; or null if there's no recommended limit. |

### getUriForDownloadedFile

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUriForDownloadedFile(id: Long): Uri!
```

Returns the [Uri](../android.net/Uri.md) of the given downloaded file id, if the file is downloaded successfully. Otherwise, null is returned.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------|
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the id of the downloaded file. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](../android.net/Uri.md)! | the [Uri](../android.net/Uri.md) of the given downloaded file id, if download was successful. null otherwise. |

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
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)! | a read-only [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md) |

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
| `query` | [DownloadManager.Query](../android/app/DownloadManager.Query.md)!:parameters specifying filters for this query |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Cursor](../android.database/Cursor.md)! | a Cursor over the result set of downloads, with columns consisting of all the COLUMN_\* constants. |

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
