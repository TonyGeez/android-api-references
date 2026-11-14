# MediaScannerConnection.MediaScannerConnectionClient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaScannerConnectionClient

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaScannerConnection.MediaScannerConnectionClient "View this page in Java") 
| --- | --- |

```
interface MediaScannerConnectionClient : MediaScannerConnection.OnScanCompletedListener
```

| [android.media.MediaScannerConnection.MediaScannerConnectionClient](https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.MediaScannerConnectionClient#) |

An interface for notifying clients of MediaScannerConnection when a connection to the MediaScanner service has been established and when the scanning of a file has completed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMediaScannerConnected](https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.MediaScannerConnectionClient#onMediaScannerConnected())`()` Called to notify the client when a connection to the MediaScanner service has been established. |

| Inherited functions ||
|---|---|
| From class [OnScanCompletedListener](https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.OnScanCompletedListener) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScanCompleted](https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.OnScanCompletedListener#onScanCompleted(kotlin.String,%20android.net.Uri))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` <br /> Called to notify the client when the media scanner has finished scanning a file. <br /> | ||

## Public methods

### onMediaScannerConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMediaScannerConnected(): Unit
```

Called to notify the client when a connection to the MediaScanner service has been established.
