# ForegroundServiceTypeException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ForegroundServiceTypeException

Kotlin| [Java](https://developer.android.com/reference/android/app/ForegroundServiceTypeException "View this page in Java") 

```
abstract class ForegroundServiceTypeException : ServiceStartNotAllowedException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) |||
| | | | | ↳ | [android.app.ServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/ServiceStartNotAllowedException) ||
| | | | | | ↳ | [android.app.ForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/ForegroundServiceTypeException#) |

| Known Direct Subclasses [InvalidForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/InvalidForegroundServiceTypeException), [MissingForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/MissingForegroundServiceTypeException) |-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InvalidForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/InvalidForegroundServiceTypeException) | Exception thrown when an app tries to start a foreground [Service](https://developer.android.com/reference/kotlin/android/app/Service) with an invalid type. | | [MissingForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/MissingForegroundServiceTypeException) | Exception thrown when an app tries to start a foreground [Service](https://developer.android.com/reference/kotlin/android/app/Service) without a type. | |

Base exception thrown when an app tries to start a foreground [Service](https://developer.android.com/reference/kotlin/android/app/Service) without a valid type.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/ForegroundServiceTypeException#ForegroundServiceTypeException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructor. |

| Inherited properties ||
|---|---|
| From class [ServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/ServiceStartNotAllowedException) |-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](https://developer.android.com/reference/kotlin/android/app/ServiceStartNotAllowedException#cause:kotlin.Throwable) <br /> | ||

## Public constructors

### ForegroundServiceTypeException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ForegroundServiceTypeException(message: String)
```

Constructor.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
