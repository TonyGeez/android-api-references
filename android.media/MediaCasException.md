# MediaCasException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaCasException

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaCasException "View this page in Java") 
| --- | --- |

```
open class MediaCasException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.media.MediaCasException](https://developer.android.com/reference/kotlin/android/media/MediaCasException#) |
| --- | --- | --- | --- |

| Known Direct Subclasses [MediaCasException.DeniedByServerException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.DeniedByServerException), [MediaCasException.InsufficientResourceException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.InsufficientResourceException), [MediaCasException.NotProvisionedException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.NotProvisionedException), [MediaCasException.ResourceBusyException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.ResourceBusyException), [MediaCasException.UnsupportedCasException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.UnsupportedCasException) |-----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MediaCasException.DeniedByServerException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.DeniedByServerException) | Exception thrown when the provisioning server or key server denies a license for a device. | | [MediaCasException.InsufficientResourceException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.InsufficientResourceException) | Exception thrown when an operation on a MediaCas object is attempted and hardware resources are not sufficient to allocate, due to client's lower priority. | | [MediaCasException.NotProvisionedException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.NotProvisionedException) | Exception thrown when an operation on a MediaCas object is attempted before it's provisioned successfully. | | [MediaCasException.ResourceBusyException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.ResourceBusyException) | Exception thrown when an operation on a MediaCas object is attempted and hardware resources are not available, due to being in use. | | [MediaCasException.UnsupportedCasException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.UnsupportedCasException) | Exception thrown when an attempt is made to construct a MediaCas object using a CA_system_id that is not supported by the device | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for MediaCas exceptions

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [DeniedByServerException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.DeniedByServerException) Exception thrown when the provisioning server or key server denies a license for a device. |
| | [InsufficientResourceException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.InsufficientResourceException) Exception thrown when an operation on a MediaCas object is attempted and hardware resources are not sufficient to allocate, due to client's lower priority. |
| | [NotProvisionedException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.NotProvisionedException) Exception thrown when an operation on a MediaCas object is attempted before it's provisioned successfully. |
| --- | --- |
| | [ResourceBusyException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.ResourceBusyException) Exception thrown when an operation on a MediaCas object is attempted and hardware resources are not available, due to being in use. |
| | [UnsupportedCasException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.UnsupportedCasException) Exception thrown when an attempt is made to construct a MediaCas object using a CA_system_id that is not supported by the device |
