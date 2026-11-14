# MediaDrmResetException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaDrmResetException

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaDrmResetException "View this page in Java") 

```
open class MediaDrmResetException : IllegalStateException, MediaDrmThrowable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [android.media.MediaDrmResetException](https://developer.android.com/reference/kotlin/android/media/MediaDrmResetException#) |

This exception is thrown when the MediaDrm instance has become unusable due to a restart of the mediaserver process. To continue, the app must release the MediaDrm object, then create and initialize a new one.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaDrmResetException](https://developer.android.com/reference/kotlin/android/media/MediaDrmResetException#MediaDrmResetException(kotlin.String))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MediaDrmThrowable](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#getErrorContext())`()` <br /> Returns [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin vendor defined error context associated with this [MediaDrmThrowable](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable). Please consult the [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin vendor for details on the error context. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#getOemError())`()` <br /> Returns OEM or SOC specific error code associated with this [MediaDrmThrowable](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable). Please consult the [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin, chip, or device vendor for details on the error code. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#getVendorError())`()` <br /> Returns [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin vendor defined error code associated with this [MediaDrmThrowable](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable). Please consult the [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin vendor for details on the error code. <br /> | ||

## Public constructors

### MediaDrmResetException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaDrmResetException(detailMessage: String!)
```
