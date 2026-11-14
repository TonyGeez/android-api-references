# ResourceBusyException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResourceBusyException

Kotlin| [Java](ResourceBusyException.md) 
| --- | --- |

```
class ResourceBusyException : MediaDrmException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [android.media.MediaDrmException](MediaDrmException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.media.ResourceBusyException](ResourceBusyException.md) |

Exception thrown when an operation on a MediaDrm object is attempted and hardware resources are not available, due to being in use.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ResourceBusyException](ResourceBusyException.md))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MediaDrmException](MediaDrmException.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](MediaDrmException.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](MediaDrmException.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](MediaDrmException.md))`()` <br /> | ||

## Public constructors

### ResourceBusyException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ResourceBusyException(detailMessage: String!)
```
