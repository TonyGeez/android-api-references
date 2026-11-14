# BadParcelableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BadParcelableException

Kotlin| [Java](https://developer.android.com/reference/android/os/BadParcelableException "View this page in Java") 

```
open class BadParcelableException : AndroidRuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [android.util.AndroidRuntimeException](https://developer.android.com/reference/kotlin/android/util/AndroidRuntimeException.html#) ||
| | | | | ↳ | [android.os.BadParcelableException](https://developer.android.com/reference/kotlin/android/os/BadParcelableException#) |

Exception thrown when a [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable) is malformed or otherwise invalid.

This is typically encountered when a custom [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable) object is passed to another process that doesn't have the same [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable) class in its [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BadParcelableException](https://developer.android.com/reference/kotlin/android/os/BadParcelableException#BadParcelableException(java.lang.Exception))`(`cause:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`)` <br /> |
| [BadParcelableException](https://developer.android.com/reference/kotlin/android/os/BadParcelableException#BadParcelableException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### BadParcelableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BadParcelableException(cause: Exception!)
```  

### BadParcelableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BadParcelableException(msg: String!)
```
