# MediaScannerConnection.OnScanCompletedListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnScanCompletedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaScannerConnection.OnScanCompletedListener "View this page in Java") 

```
interface OnScanCompletedListener
```

| [android.media.MediaScannerConnection.OnScanCompletedListener](https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.OnScanCompletedListener#) |

| Known Direct Subclasses [MediaScannerConnection.MediaScannerConnectionClient](https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.MediaScannerConnectionClient) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MediaScannerConnection.MediaScannerConnectionClient](https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.MediaScannerConnectionClient) | An interface for notifying clients of MediaScannerConnection when a connection to the MediaScanner service has been established and when the scanning of a file has completed. | |

Interface for notifying clients of the result of scanning a requested media file.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScanCompleted](https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.OnScanCompletedListener#onScanCompleted(kotlin.String,%20android.net.Uri))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Called to notify the client when the media scanner has finished scanning a file. |

## Public methods

### onScanCompleted

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScanCompleted(
    path: String!, 
    uri: Uri!
): Unit
```

Called to notify the client when the media scanner has finished scanning a file.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path to the file that has been scanned. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:the Uri for the file if the scanning operation succeeded and the file was added to the media database, or null if scanning failed. |
