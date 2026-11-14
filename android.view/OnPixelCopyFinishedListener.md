# PixelCopy.OnPixelCopyFinishedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPixelCopyFinishedListener

Kotlin| [Java](https://developer.android.com/reference/android/view/PixelCopy.OnPixelCopyFinishedListener "View this page in Java") 

```
interface OnPixelCopyFinishedListener
```

| [android.view.PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener#) |

Listener for observing the completion of a PixelCopy request.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPixelCopyFinished](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener#onPixelCopyFinished(kotlin.Int))`(`copyResult:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback for when a pixel copy request has completed. |

## Public methods

### onPixelCopyFinished

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPixelCopyFinished(copyResult: Int): Unit
```

Callback for when a pixel copy request has completed. This will be called regardless of whether the copy succeeded or failed.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `copyResult` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Contains the resulting status of the copy request. This will either be [PixelCopy.SUCCESS](https://developer.android.com/reference/kotlin/android/view/PixelCopy#SUCCESS:kotlin.Int) or one of the`PixelCopy.ERROR_*`values. Value is [android.view.PixelCopy#SUCCESS](https://developer.android.com/reference/kotlin/android/view/PixelCopy#SUCCESS:kotlin.Int), [android.view.PixelCopy#ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/PixelCopy#ERROR_UNKNOWN:kotlin.Int), [android.view.PixelCopy#ERROR_TIMEOUT](https://developer.android.com/reference/kotlin/android/view/PixelCopy#ERROR_TIMEOUT:kotlin.Int), [android.view.PixelCopy#ERROR_SOURCE_NO_DATA](https://developer.android.com/reference/kotlin/android/view/PixelCopy#ERROR_SOURCE_NO_DATA:kotlin.Int), [android.view.PixelCopy#ERROR_SOURCE_INVALID](https://developer.android.com/reference/kotlin/android/view/PixelCopy#ERROR_SOURCE_INVALID:kotlin.Int), or [android.view.PixelCopy#ERROR_DESTINATION_INVALID](https://developer.android.com/reference/kotlin/android/view/PixelCopy#ERROR_DESTINATION_INVALID:kotlin.Int) |
