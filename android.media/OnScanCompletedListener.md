# MediaScannerConnection.OnScanCompletedListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnScanCompletedListener

Kotlin| [Java](../android/media/MediaScannerConnection.OnScanCompletedListener.md) 
| --- | --- |

```
interface OnScanCompletedListener
```

| [android.media.MediaScannerConnection.OnScanCompletedListener](../android/media/MediaScannerConnection.OnScanCompletedListener.md) |

| Known Direct Subclasses [MediaScannerConnection.MediaScannerConnectionClient](../android/media/MediaScannerConnection.MediaScannerConnectionClient.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MediaScannerConnection.MediaScannerConnectionClient](../android/media/MediaScannerConnection.MediaScannerConnectionClient.md) | An interface for notifying clients of MediaScannerConnection when a connection to the MediaScanner service has been established and when the scanning of a file has completed. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface for notifying clients of the result of scanning a requested media file.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScanCompleted](../android/media/MediaScannerConnection.OnScanCompletedListener.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `uri:` ` [Uri](../android.net/Uri.md)!`)` Called to notify the client when the media scanner has finished scanning a file. |

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
| `uri` | [Uri](../android.net/Uri.md)!:the Uri for the file if the scanning operation succeeded and the file was added to the media database, or null if scanning failed. |
