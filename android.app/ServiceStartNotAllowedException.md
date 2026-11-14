Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceStartNotAllowedException

Kotlin | [Java](https://developer.android.com/reference/android/app/ServiceStartNotAllowedException "View this page in Java")
| --- | --- |

```
abstract class ServiceStartNotAllowedException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [android.app.ServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/ServiceStartNotAllowedException#) |

| Known Direct Subclasses [BackgroundServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/BackgroundServiceStartNotAllowedException), [ForegroundServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/ForegroundServiceStartNotAllowedException), [ForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/ForegroundServiceTypeException) |---|---| | [BackgroundServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/BackgroundServiceStartNotAllowedException) | Exception thrown when an app tries to start a background `https://developer.android.com/reference/kotlin/android/app/Service` when it's not allowed to do so. | | [ForegroundServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/ForegroundServiceStartNotAllowedException) | Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service` when it's not allowed to do so. | | [ForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/ForegroundServiceTypeException) | Base exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service` without a valid type. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [InvalidForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/InvalidForegroundServiceTypeException), [MissingForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/MissingForegroundServiceTypeException) |---|---| | [InvalidForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/InvalidForegroundServiceTypeException) | Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service` with an invalid type. | | [MissingForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/MissingForegroundServiceTypeException) | Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service` without a type. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Exception thrown when an app tries to start a `https://developer.android.com/reference/kotlin/android/app/Service` when it's not allowed to do so.

## Summary

| Properties ||
|---|---|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | `https://developer.android.com/reference/kotlin/android/app/ServiceStartNotAllowedException#cause:kotlin.Throwable` Returns the cause of this throwable or `null` if the cause is nonexistent or unknown. |

## Properties

### cause

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val cause: Throwable?
```

Returns the cause of this throwable or `null` if the cause is nonexistent or unknown. (The cause is the throwable that caused this throwable to get thrown.)

This implementation returns the cause that was supplied via one of the constructors requiring a `Throwable`, or that was set after creation with the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable)` method. While it is typically unnecessary to override this method, a subclass can override it to return a cause set by some other means. This is appropriate for a "legacy chained throwable" that predates the addition of chained exceptions to `Throwable`. Note that it is *not* necessary to override any of the `PrintStackTrace` methods, all of which invoke the `getCause` method to determine the cause of a throwable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html?` | the cause of this throwable or `null` if the cause is nonexistent or unknown. |
