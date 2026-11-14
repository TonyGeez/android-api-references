# DownloadProgressListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DownloadProgressListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/mbms/DownloadProgressListener "View this page in Java") 
| --- | --- |

```
open class DownloadProgressListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.mbms.DownloadProgressListener](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadProgressListener#) |

A optional listener class used by download clients to track progress. Apps should extend this class and pass an instance into [MbmsDownloadSession.download(DownloadRequest)](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession.html#download(android.telephony.mbms.DownloadRequest))This is optionally specified when requesting a download and will only be called while the app is running.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DownloadProgressListener](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadProgressListener#DownloadProgressListener())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProgressUpdated](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadProgressListener#onProgressUpdated(android.telephony.mbms.DownloadRequest,%20android.telephony.mbms.FileInfo,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`request:` ` [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest)!`, `fileInfo:` ` [FileInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileInfo)!`, `currentDownloadSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fullDownloadSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `currentDecodedSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fullDecodedSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the middleware wants to report progress for a file in a [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest). |

## Public constructors

### DownloadProgressListener

```
DownloadProgressListener()
```

## Public methods

### onProgressUpdated

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onProgressUpdated(
    request: DownloadRequest!, 
    fileInfo: FileInfo!, 
    currentDownloadSize: Int, 
    fullDownloadSize: Int, 
    currentDecodedSize: Int, 
    fullDecodedSize: Int
): Unit
```

Called when the middleware wants to report progress for a file in a [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest).

| Parameters ||
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest)!:a [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest), indicating which download is being referenced. |
| `fileInfo` | [FileInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileInfo)!:a [FileInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileInfo) specifying the file to report progress on. Note that the request may result in many files being downloaded and the client may not have been able to get a list of them in advance. |
| `currentDownloadSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the current amount downloaded. |
| --- | --- |
| `fullDownloadSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the total number of bytes that make up the downloaded content. This may be different from the decoded final size, but is useful in gauging download progress. |
| `currentDecodedSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the number of bytes that have been decoded. |
| `fullDecodedSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the total number of bytes that make up the final decoded content. |
| --- | --- |
