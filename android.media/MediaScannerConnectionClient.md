# MediaScannerConnection.MediaScannerConnectionClient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaScannerConnectionClient

Kotlin| [Java](../android/media/MediaScannerConnection.MediaScannerConnectionClient.md) 
| --- | --- |

```
interface MediaScannerConnectionClient : MediaScannerConnection.OnScanCompletedListener
```

| [android.media.MediaScannerConnection.MediaScannerConnectionClient](../android/media/MediaScannerConnection.MediaScannerConnectionClient.md) |

An interface for notifying clients of MediaScannerConnection when a connection to the MediaScanner service has been established and when the scanning of a file has completed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMediaScannerConnected](../android/media/MediaScannerConnection.MediaScannerConnectionClient.md))`()` Called to notify the client when a connection to the MediaScanner service has been established. |

| Inherited functions ||
|---|---|
| From class [OnScanCompletedListener](../android/media/MediaScannerConnection.OnScanCompletedListener.md) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScanCompleted](../android/media/MediaScannerConnection.OnScanCompletedListener.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `uri:` ` [Uri](../android.net/Uri.md)!`)` <br /> Called to notify the client when the media scanner has finished scanning a file. <br /> | ||

## Public methods

### onMediaScannerConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMediaScannerConnected(): Unit
```

Called to notify the client when a connection to the MediaScanner service has been established.
