# DownloadStatusListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DownloadStatusListener

Kotlin| [Java](../android/telephony/mbms/DownloadStatusListener.md) 
| --- | --- |

```
open class DownloadStatusListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.mbms.DownloadStatusListener](../android/telephony/mbms/DownloadStatusListener.md) |

A optional listener class used by download clients to track progress. Apps should extend this class and pass an instance into [MbmsDownloadSession.download(DownloadRequest)](../android/telephony/MbmsDownloadSession.md))This is optionally specified when requesting a download and will only be called while the app is running.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DownloadStatusListener](../android/telephony/mbms/DownloadStatusListener.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStatusUpdated](../android/telephony/mbms/DownloadStatusListener.md))`(`request:` ` [DownloadRequest](../android/telephony/mbms/DownloadRequest.md)!`, `fileInfo:` ` [FileInfo](../android/telephony/mbms/FileInfo.md)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gives download status callbacks for a file in a [DownloadRequest](../android/telephony/mbms/DownloadRequest.md). |

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

Gives download status callbacks for a file in a [DownloadRequest](../android/telephony/mbms/DownloadRequest.md).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [DownloadRequest](../android/telephony/mbms/DownloadRequest.md)!:a [DownloadRequest](../android/telephony/mbms/DownloadRequest.md), indicating which download is being referenced. |
| `fileInfo` | [FileInfo](../android/telephony/mbms/FileInfo.md)!:a [FileInfo](../android/telephony/mbms/FileInfo.md) specifying the file to report progress on. Note that the request may result in many files being downloaded and the client may not have been able to get a list of them in advance. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current status of the download. Value is [android.telephony.MbmsDownloadSession#STATUS_UNKNOWN](../android/telephony/MbmsDownloadSession.md), [android.telephony.MbmsDownloadSession#STATUS_ACTIVELY_DOWNLOADING](../android/telephony/MbmsDownloadSession.md), [android.telephony.MbmsDownloadSession#STATUS_PENDING_DOWNLOAD](../android/telephony/MbmsDownloadSession.md), [android.telephony.MbmsDownloadSession#STATUS_PENDING_REPAIR](../android/telephony/MbmsDownloadSession.md), or [android.telephony.MbmsDownloadSession#STATUS_PENDING_DOWNLOAD_WINDOW](../android/telephony/MbmsDownloadSession.md) |
| --- | --- |
