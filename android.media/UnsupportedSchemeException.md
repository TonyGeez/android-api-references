# UnsupportedSchemeException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedSchemeException

Kotlin| [Java](UnsupportedSchemeException.md) 
| --- | --- |

```
class UnsupportedSchemeException : MediaDrmException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [android.media.MediaDrmException](MediaDrmException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.media.UnsupportedSchemeException](UnsupportedSchemeException.md) |

Exception thrown when an attempt is made to construct a MediaDrm object using a crypto scheme UUID that is not supported by the device

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnsupportedSchemeException](UnsupportedSchemeException.md))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MediaDrmException](MediaDrmException.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](MediaDrmException.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](MediaDrmException.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](MediaDrmException.md))`()` <br /> | ||

## Public constructors

### UnsupportedSchemeException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnsupportedSchemeException(detailMessage: String!)
```
