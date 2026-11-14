# DownloadStatusListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DownloadStatusListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/mbms/DownloadStatusListener "View this page in Java") 
| --- | --- |

```
open class DownloadStatusListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.mbms.DownloadStatusListener](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadStatusListener#) |

A optional listener class used by download clients to track progress. Apps should extend this class and pass an instance into [MbmsDownloadSession.download(DownloadRequest)](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession.html#download(android.telephony.mbms.DownloadRequest))This is optionally specified when requesting a download and will only be called while the app is running.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DownloadStatusListener](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadStatusListener#DownloadStatusListener())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStatusUpdated](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadStatusListener#onStatusUpdated(android.telephony.mbms.DownloadRequest,%20android.telephony.mbms.FileInfo,%20kotlin.Int))`(`request:` ` [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest)!`, `fileInfo:` ` [FileInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileInfo)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gives download status callbacks for a file in a [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest). |

## Public constructors

### DownloadStatusListener

```
DownloadStatusListener()
```

## Public methods

### onStatusUpdated

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStatusUpdated(
    request: DownloadRequest!, 
    fileInfo: FileInfo!, 
    status: Int
): Unit
```

Gives download status callbacks for a file in a [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest)!:a [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest), indicating which download is being referenced. |
| `fileInfo` | [FileInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileInfo)!:a [FileInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileInfo) specifying the file to report progress on. Note that the request may result in many files being downloaded and the client may not have been able to get a list of them in advance. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current status of the download. Value is [android.telephony.MbmsDownloadSession#STATUS_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession.html#STATUS_UNKNOWN:kotlin.Int), [android.telephony.MbmsDownloadSession#STATUS_ACTIVELY_DOWNLOADING](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession.html#STATUS_ACTIVELY_DOWNLOADING:kotlin.Int), [android.telephony.MbmsDownloadSession#STATUS_PENDING_DOWNLOAD](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession.html#STATUS_PENDING_DOWNLOAD:kotlin.Int), [android.telephony.MbmsDownloadSession#STATUS_PENDING_REPAIR](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession.html#STATUS_PENDING_REPAIR:kotlin.Int), or [android.telephony.MbmsDownloadSession#STATUS_PENDING_DOWNLOAD_WINDOW](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession.html#STATUS_PENDING_DOWNLOAD_WINDOW:kotlin.Int) |
| --- | --- |
