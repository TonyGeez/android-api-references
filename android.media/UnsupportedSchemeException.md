# UnsupportedSchemeException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedSchemeException

Kotlin| [Java](../android/media/UnsupportedSchemeException.md) 
| --- | --- |

```
class UnsupportedSchemeException : MediaDrmException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [android.media.MediaDrmException](../android/media/MediaDrmException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.media.UnsupportedSchemeException](../android/media/UnsupportedSchemeException.md) |

Exception thrown when an attempt is made to construct a MediaDrm object using a crypto scheme UUID that is not supported by the device

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnsupportedSchemeException](../android/media/UnsupportedSchemeException.md))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MediaDrmException](../android/media/MediaDrmException.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](../android/media/MediaDrmException.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](../android/media/MediaDrmException.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](../android/media/MediaDrmException.md))`()` <br /> | ||

## Public constructors

### UnsupportedSchemeException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnsupportedSchemeException(detailMessage: String!)
```
