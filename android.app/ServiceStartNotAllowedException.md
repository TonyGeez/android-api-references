Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceStartNotAllowedException

Kotlin | [Java](ServiceStartNotAllowedException.md)
| --- | --- |

```
abstract class ServiceStartNotAllowedException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java.lang/IllegalStateException.md) ||
| | | | | ↳ | [android.app.ServiceStartNotAllowedException](ServiceStartNotAllowedException.md) |

| Known Direct Subclasses [BackgroundServiceStartNotAllowedException](BackgroundServiceStartNotAllowedException.md), [ForegroundServiceStartNotAllowedException](ForegroundServiceStartNotAllowedException.md), [ForegroundServiceTypeException](ForegroundServiceTypeException.md) |---|---| | [BackgroundServiceStartNotAllowedException](BackgroundServiceStartNotAllowedException.md) | Exception thrown when an app tries to start a background Service when it's not allowed to do so. | | [ForegroundServiceStartNotAllowedException](ForegroundServiceStartNotAllowedException.md) | Exception thrown when an app tries to start a foreground Service when it's not allowed to do so. | | [ForegroundServiceTypeException](ForegroundServiceTypeException.md) | Base exception thrown when an app tries to start a foreground Service without a valid type. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [InvalidForegroundServiceTypeException](InvalidForegroundServiceTypeException.md), [MissingForegroundServiceTypeException](MissingForegroundServiceTypeException.md) |---|---| | [InvalidForegroundServiceTypeException](InvalidForegroundServiceTypeException.md) | Exception thrown when an app tries to start a foreground Service with an invalid type. | | [MissingForegroundServiceTypeException](MissingForegroundServiceTypeException.md) | Exception thrown when an app tries to start a foreground Service without a type. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Exception thrown when an app tries to start a Service when it's not allowed to do so.

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

This implementation returns the cause that was supplied via one of the constructors requiring a `Throwable`, or that was set after creation with the initCause method. While it is typically unnecessary to override this method, a subclass can override it to return a cause set by some other means. This is appropriate for a "legacy chained throwable" that predates the addition of chained exceptions to `Throwable`. Note that it is *not* necessary to override any of the `PrintStackTrace` methods, all of which invoke the `getCause` method to determine the cause of a throwable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html?` | the cause of this throwable or `null` if the cause is nonexistent or unknown. |
