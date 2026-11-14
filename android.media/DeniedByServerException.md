# DeniedByServerException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeniedByServerException

Kotlin| [Java](../android/media/DeniedByServerException.md) 
| --- | --- |

```
class DeniedByServerException : MediaDrmException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [android.media.MediaDrmException](../android/media/MediaDrmException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.media.DeniedByServerException](../android/media/DeniedByServerException.md) |

Exception thrown when the provisioning server or key server denies a certficate or license for a device.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DeniedByServerException](../android/media/DeniedByServerException.md))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MediaDrmException](../android/media/MediaDrmException.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](../android/media/MediaDrmException.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](../android/media/MediaDrmException.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](../android/media/MediaDrmException.md))`()` <br /> | ||

## Public constructors

### DeniedByServerException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeniedByServerException(detailMessage: String!)
```
