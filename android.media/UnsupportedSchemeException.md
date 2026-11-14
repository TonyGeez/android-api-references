# UnsupportedSchemeException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedSchemeException

Kotlin| [Java](https://developer.android.com/reference/android/media/UnsupportedSchemeException "View this page in Java") 

```
class UnsupportedSchemeException : MediaDrmException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [android.media.MediaDrmException](https://developer.android.com/reference/kotlin/android/media/MediaDrmException) ||
| | | | ↳ | [android.media.UnsupportedSchemeException](https://developer.android.com/reference/kotlin/android/media/UnsupportedSchemeException#) |

Exception thrown when an attempt is made to construct a MediaDrm object using a crypto scheme UUID that is not supported by the device

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnsupportedSchemeException](https://developer.android.com/reference/kotlin/android/media/UnsupportedSchemeException#UnsupportedSchemeException(kotlin.String))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MediaDrmException](https://developer.android.com/reference/kotlin/android/media/MediaDrmException) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getErrorContext())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getOemError())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getVendorError())`()` <br /> | ||

## Public constructors

### UnsupportedSchemeException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnsupportedSchemeException(detailMessage: String!)
```
