# ResourceBusyException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResourceBusyException

Kotlin| [Java](https://developer.android.com/reference/android/media/ResourceBusyException "View this page in Java") 
| --- | --- |

```
class ResourceBusyException : MediaDrmException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [android.media.MediaDrmException](https://developer.android.com/reference/kotlin/android/media/MediaDrmException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.media.ResourceBusyException](https://developer.android.com/reference/kotlin/android/media/ResourceBusyException#) |

Exception thrown when an operation on a MediaDrm object is attempted and hardware resources are not available, due to being in use.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ResourceBusyException](https://developer.android.com/reference/kotlin/android/media/ResourceBusyException#ResourceBusyException(kotlin.String))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MediaDrmException](https://developer.android.com/reference/kotlin/android/media/MediaDrmException) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getErrorContext())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getOemError())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getVendorError())`()` <br /> | ||

## Public constructors

### ResourceBusyException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ResourceBusyException(detailMessage: String!)
```
