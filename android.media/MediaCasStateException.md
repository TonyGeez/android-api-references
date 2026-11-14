# MediaCasStateException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaCasStateException

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaCasStateException "View this page in Java") 

```
open class MediaCasStateException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [android.media.MediaCasStateException](https://developer.android.com/reference/kotlin/android/media/MediaCasStateException#) |

Base class for MediaCas runtime exceptions

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDiagnosticInfo](https://developer.android.com/reference/kotlin/android/media/MediaCasStateException#getDiagnosticInfo())`()` Retrieve a developer-readable diagnostic information string associated with the exception. |

## Public methods

### getDiagnosticInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDiagnosticInfo(): String
```

Retrieve a developer-readable diagnostic information string associated with the exception. Do not show this to end-users, since this string will not be localized or generally comprehensible to end-users.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |
