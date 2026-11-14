# Base64DataException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Base64DataException

Kotlin| [Java](https://developer.android.com/reference/android/util/Base64DataException "View this page in Java") 

```
open class Base64DataException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| | | | ↳ | [android.util.Base64DataException](https://developer.android.com/reference/kotlin/android/util/Base64DataException#) |

This exception is thrown by [Base64InputStream](https://developer.android.com/reference/kotlin/android/util/Base64InputStream) or [Base64OutputStream](https://developer.android.com/reference/kotlin/android/util/Base64OutputStream) when an error is detected in the data being decoded. This allows problems with the base64 data to be disambiguated from errors in the underlying streams (e.g. actual connection errors.)

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Base64DataException](https://developer.android.com/reference/kotlin/android/util/Base64DataException#Base64DataException(kotlin.String))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### Base64DataException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Base64DataException(detailMessage: String!)
```
