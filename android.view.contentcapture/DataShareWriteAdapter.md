# DataShareWriteAdapter

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataShareWriteAdapter

Kotlin| [Java](DataShareWriteAdapter.md) 
| --- | --- |

```
interface DataShareWriteAdapter
```

| [android.view.contentcapture.DataShareWriteAdapter](DataShareWriteAdapter.md) |

Adapter class used by apps to share data with the Content Capture service.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](DataShareWriteAdapter.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Method invoked when an error occurred, for example sessions has not been started or terminated unsuccessfully. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRejected](DataShareWriteAdapter.md))`()` Data share sessions has been rejected by the Content Capture service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWrite](DataShareWriteAdapter.md))`(`destination:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)`)` Method invoked when the data share session has been started and the app needs to start writing into the file used for sharing. |
| --- | --- |

## Public methods

### onError

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onError(errorCode: Int): Unit
```

Method invoked when an error occurred, for example sessions has not been started or terminated unsuccessfully.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the error code corresponding to an ERROR_\* value. Value is [android.view.contentcapture.ContentCaptureManager#DATA_SHARE_ERROR_UNKNOWN](ContentCaptureManager.md), [android.view.contentcapture.ContentCaptureManager#DATA_SHARE_ERROR_CONCURRENT_REQUEST](ContentCaptureManager.md), or [android.view.contentcapture.ContentCaptureManager#DATA_SHARE_ERROR_TIMEOUT_INTERRUPTED](ContentCaptureManager.md) |

### onRejected

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRejected(): Unit
```

Data share sessions has been rejected by the Content Capture service. 

### onWrite

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onWrite(destination: ParcelFileDescriptor): Unit
```

Method invoked when the data share session has been started and the app needs to start writing into the file used for sharing.

App needs to handle explicitly cases when the file descriptor is closed and handle gracefully if IOExceptions happen.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `destination` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md):file descriptor used to write data into. This value cannot be`null`. |
