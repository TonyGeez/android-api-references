# MediaCasStateException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaCasStateException

Kotlin| [Java](MediaCasStateException.md) 
| --- | --- |

```
open class MediaCasStateException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java.lang/IllegalStateException.md) ||
| | | | | ↳ | [android.media.MediaCasStateException](MediaCasStateException.md) |

Base class for MediaCas runtime exceptions

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDiagnosticInfo](MediaCasStateException.md))`()` Retrieve a developer-readable diagnostic information string associated with the exception. |

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
