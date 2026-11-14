# DownloadProgressListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DownloadProgressListener

Kotlin| [Java](DownloadProgressListener.md) 
| --- | --- |

```
open class DownloadProgressListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.mbms.DownloadProgressListener](DownloadProgressListener.md) |

A optional listener class used by download clients to track progress. Apps should extend this class and pass an instance into [MbmsDownloadSession.download(DownloadRequest)](../android.telephony/MbmsDownloadSession.md))This is optionally specified when requesting a download and will only be called while the app is running.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DownloadProgressListener](DownloadProgressListener.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProgressUpdated](DownloadProgressListener.md))`(`request:` ` [DownloadRequest](DownloadRequest.md)!`, `fileInfo:` ` [FileInfo](FileInfo.md)!`, `currentDownloadSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fullDownloadSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `currentDecodedSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fullDecodedSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the middleware wants to report progress for a file in a [DownloadRequest](DownloadRequest.md). |

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

Called when the middleware wants to report progress for a file in a [DownloadRequest](DownloadRequest.md).

| Parameters ||
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [DownloadRequest](DownloadRequest.md)!:a [DownloadRequest](DownloadRequest.md), indicating which download is being referenced. |
| `fileInfo` | [FileInfo](FileInfo.md)!:a [FileInfo](FileInfo.md) specifying the file to report progress on. Note that the request may result in many files being downloaded and the client may not have been able to get a list of them in advance. |
| `currentDownloadSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the current amount downloaded. |
| --- | --- |
| `fullDownloadSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the total number of bytes that make up the downloaded content. This may be different from the decoded final size, but is useful in gauging download progress. |
| `currentDecodedSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the number of bytes that have been decoded. |
| `fullDecodedSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the total number of bytes that make up the final decoded content. |
| --- | --- |
