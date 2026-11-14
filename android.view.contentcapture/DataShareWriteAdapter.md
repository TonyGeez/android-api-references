# DataShareWriteAdapter

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataShareWriteAdapter

Kotlin| [Java](https://developer.android.com/reference/android/view/contentcapture/DataShareWriteAdapter "View this page in Java") 
| --- | --- |

```
interface DataShareWriteAdapter
```

| [android.view.contentcapture.DataShareWriteAdapter](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataShareWriteAdapter#) |

Adapter class used by apps to share data with the Content Capture service.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataShareWriteAdapter#onError(kotlin.Int))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Method invoked when an error occurred, for example sessions has not been started or terminated unsuccessfully. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRejected](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataShareWriteAdapter#onRejected())`()` Data share sessions has been rejected by the Content Capture service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWrite](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataShareWriteAdapter#onWrite(android.os.ParcelFileDescriptor))`(`destination:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)`)` Method invoked when the data share session has been started and the app needs to start writing into the file used for sharing. |
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
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the error code corresponding to an ERROR_\* value. Value is [android.view.contentcapture.ContentCaptureManager#DATA_SHARE_ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#DATA_SHARE_ERROR_UNKNOWN:kotlin.Int), [android.view.contentcapture.ContentCaptureManager#DATA_SHARE_ERROR_CONCURRENT_REQUEST](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#DATA_SHARE_ERROR_CONCURRENT_REQUEST:kotlin.Int), or [android.view.contentcapture.ContentCaptureManager#DATA_SHARE_ERROR_TIMEOUT_INTERRUPTED](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#DATA_SHARE_ERROR_TIMEOUT_INTERRUPTED:kotlin.Int) |

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
| `destination` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#):file descriptor used to write data into. This value cannot be`null`. |
