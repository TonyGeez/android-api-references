# MediaCryptoException

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaCryptoException

Kotlin| [Java](MediaCryptoException.md) 
| --- | --- |

```
class MediaCryptoException : Exception, MediaDrmThrowable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.media.MediaCryptoException](MediaCryptoException.md) |
| --- | --- | --- | --- |

Exception thrown if MediaCrypto object could not be instantiated or if unable to perform an operation on the MediaCrypto object.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaCryptoException](MediaCryptoException.md))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](MediaCryptoException.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](MediaCryptoException.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](MediaCryptoException.md))`()` <br /> |
| --- | --- |

## Public constructors

### MediaCryptoException

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaCryptoException(detailMessage: String?)
```

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------|
| `detailMessage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |

## Public methods

### getErrorContext

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getErrorContext(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an opaque integer that would help the @ [MediaDrm](MediaDrm.md) vendor locate the source of the error if available, otherwise 0. |

### getOemError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOemError(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an OEM or SOC specific error code if available, otherwise 0. |

### getVendorError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVendorError(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an error code defined by the [MediaDrm](MediaDrm.md) plugin vendor if available, otherwise 0. |
