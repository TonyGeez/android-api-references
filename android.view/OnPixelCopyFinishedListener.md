# PixelCopy.OnPixelCopyFinishedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPixelCopyFinishedListener

Kotlin| [Java](../android/view/PixelCopy.OnPixelCopyFinishedListener.md) 
| --- | --- |

```
interface OnPixelCopyFinishedListener
```

| [android.view.PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md) |

Listener for observing the completion of a PixelCopy request.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPixelCopyFinished](../android/view/PixelCopy.OnPixelCopyFinishedListener.md))`(`copyResult:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback for when a pixel copy request has completed. |

## Public methods

### onPixelCopyFinished

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPixelCopyFinished(copyResult: Int): Unit
```

Callback for when a pixel copy request has completed. This will be called regardless of whether the copy succeeded or failed.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `copyResult` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Contains the resulting status of the copy request. This will either be [PixelCopy.SUCCESS](PixelCopy.md) or one of the`PixelCopy.ERROR_*`values. Value is [android.view.PixelCopy#SUCCESS](PixelCopy.md), [android.view.PixelCopy#ERROR_UNKNOWN](PixelCopy.md), [android.view.PixelCopy#ERROR_TIMEOUT](PixelCopy.md), [android.view.PixelCopy#ERROR_SOURCE_NO_DATA](PixelCopy.md), [android.view.PixelCopy#ERROR_SOURCE_INVALID](PixelCopy.md), or [android.view.PixelCopy#ERROR_DESTINATION_INVALID](PixelCopy.md) |
