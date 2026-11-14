# DeniedByServerException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeniedByServerException

Kotlin| [Java](https://developer.android.com/reference/android/media/DeniedByServerException "View this page in Java") 

```
class DeniedByServerException : MediaDrmException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [android.media.MediaDrmException](https://developer.android.com/reference/kotlin/android/media/MediaDrmException) ||
| | | | ↳ | [android.media.DeniedByServerException](https://developer.android.com/reference/kotlin/android/media/DeniedByServerException#) |

Exception thrown when the provisioning server or key server denies a certficate or license for a device.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DeniedByServerException](https://developer.android.com/reference/kotlin/android/media/DeniedByServerException#DeniedByServerException(kotlin.String))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MediaDrmException](https://developer.android.com/reference/kotlin/android/media/MediaDrmException) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getErrorContext())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getOemError())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getVendorError())`()` <br /> | ||

## Public constructors

### DeniedByServerException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeniedByServerException(detailMessage: String!)
```
