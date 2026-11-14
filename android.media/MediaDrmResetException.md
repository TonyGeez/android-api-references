# MediaDrmResetException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaDrmResetException

Kotlin| [Java](MediaDrmResetException.md) 
| --- | --- |

```
open class MediaDrmResetException : IllegalStateException, MediaDrmThrowable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java.lang/IllegalStateException.md) ||
| | | | | ↳ | [android.media.MediaDrmResetException](MediaDrmResetException.md) |

This exception is thrown when the MediaDrm instance has become unusable due to a restart of the mediaserver process. To continue, the app must release the MediaDrm object, then create and initialize a new one.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaDrmResetException](MediaDrmResetException.md))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MediaDrmThrowable](MediaDrmThrowable.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](MediaDrmThrowable.md))`()` <br /> Returns [MediaDrm](MediaDrm.md) plugin vendor defined error context associated with this [MediaDrmThrowable](MediaDrmThrowable.md). Please consult the [MediaDrm](MediaDrm.md) plugin vendor for details on the error context. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](MediaDrmThrowable.md))`()` <br /> Returns OEM or SOC specific error code associated with this [MediaDrmThrowable](MediaDrmThrowable.md). Please consult the [MediaDrm](MediaDrm.md) plugin, chip, or device vendor for details on the error code. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](MediaDrmThrowable.md))`()` <br /> Returns [MediaDrm](MediaDrm.md) plugin vendor defined error code associated with this [MediaDrmThrowable](MediaDrmThrowable.md). Please consult the [MediaDrm](MediaDrm.md) plugin vendor for details on the error code. <br /> | ||

## Public constructors

### MediaDrmResetException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaDrmResetException(detailMessage: String!)
```
