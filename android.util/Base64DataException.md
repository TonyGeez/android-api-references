# Base64DataException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Base64DataException

Kotlin| [Java](../android/util/Base64DataException.md) 
| --- | --- |

```
open class Base64DataException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.util.Base64DataException](../android/util/Base64DataException.md) |

This exception is thrown by [Base64InputStream](../android/util/Base64InputStream.md) or [Base64OutputStream](../android/util/Base64OutputStream.md) when an error is detected in the data being decoded. This allows problems with the base64 data to be disambiguated from errors in the underlying streams (e.g. actual connection errors.)

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Base64DataException](../android/util/Base64DataException.md))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### Base64DataException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Base64DataException(detailMessage: String!)
```
