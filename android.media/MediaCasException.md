# MediaCasException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaCasException

Kotlin| [Java](MediaCasException.md) 
| --- | --- |

```
open class MediaCasException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.media.MediaCasException](MediaCasException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [MediaCasException.DeniedByServerException](../android/media/MediaCasException.DeniedByServerException.md), [MediaCasException.InsufficientResourceException](../android/media/MediaCasException.InsufficientResourceException.md), [MediaCasException.NotProvisionedException](../android/media/MediaCasException.NotProvisionedException.md), [MediaCasException.ResourceBusyException](../android/media/MediaCasException.ResourceBusyException.md), [MediaCasException.UnsupportedCasException](../android/media/MediaCasException.UnsupportedCasException.md) |-----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MediaCasException.DeniedByServerException](../android/media/MediaCasException.DeniedByServerException.md) | Exception thrown when the provisioning server or key server denies a license for a device. | | [MediaCasException.InsufficientResourceException](../android/media/MediaCasException.InsufficientResourceException.md) | Exception thrown when an operation on a MediaCas object is attempted and hardware resources are not sufficient to allocate, due to client's lower priority. | | [MediaCasException.NotProvisionedException](../android/media/MediaCasException.NotProvisionedException.md) | Exception thrown when an operation on a MediaCas object is attempted before it's provisioned successfully. | | [MediaCasException.ResourceBusyException](../android/media/MediaCasException.ResourceBusyException.md) | Exception thrown when an operation on a MediaCas object is attempted and hardware resources are not available, due to being in use. | | [MediaCasException.UnsupportedCasException](../android/media/MediaCasException.UnsupportedCasException.md) | Exception thrown when an attempt is made to construct a MediaCas object using a CA_system_id that is not supported by the device | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for MediaCas exceptions

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [DeniedByServerException](../android/media/MediaCasException.DeniedByServerException.md) Exception thrown when the provisioning server or key server denies a license for a device. |
| | [InsufficientResourceException](../android/media/MediaCasException.InsufficientResourceException.md) Exception thrown when an operation on a MediaCas object is attempted and hardware resources are not sufficient to allocate, due to client's lower priority. |
| | [NotProvisionedException](../android/media/MediaCasException.NotProvisionedException.md) Exception thrown when an operation on a MediaCas object is attempted before it's provisioned successfully. |
| --- | --- |
| | [ResourceBusyException](../android/media/MediaCasException.ResourceBusyException.md) Exception thrown when an operation on a MediaCas object is attempted and hardware resources are not available, due to being in use. |
| | [UnsupportedCasException](../android/media/MediaCasException.UnsupportedCasException.md) Exception thrown when an attempt is made to construct a MediaCas object using a CA_system_id that is not supported by the device |
