# ForegroundServiceTypeException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ForegroundServiceTypeException

Kotlin| [Java](../android/app/ForegroundServiceTypeException.md) 
| --- | --- |

```
abstract class ForegroundServiceTypeException : ServiceStartNotAllowedException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java/lang/IllegalStateException.md) |||
| | | | | ↳ | [android.app.ServiceStartNotAllowedException](../android/app/ServiceStartNotAllowedException.md) ||
| | | | | | ↳ | [android.app.ForegroundServiceTypeException](../android/app/ForegroundServiceTypeException.md) |
| --- | --- | --- | --- | --- | --- | --- |

| Known Direct Subclasses [InvalidForegroundServiceTypeException](../android/app/InvalidForegroundServiceTypeException.md), [MissingForegroundServiceTypeException](../android/app/MissingForegroundServiceTypeException.md) |-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InvalidForegroundServiceTypeException](../android/app/InvalidForegroundServiceTypeException.md) | Exception thrown when an app tries to start a foreground [Service](../android/app/Service.md) with an invalid type. | | [MissingForegroundServiceTypeException](../android/app/MissingForegroundServiceTypeException.md) | Exception thrown when an app tries to start a foreground [Service](../android/app/Service.md) without a type. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base exception thrown when an app tries to start a foreground [Service](../android/app/Service.md) without a valid type.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ForegroundServiceTypeException](../android/app/ForegroundServiceTypeException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructor. |

| Inherited properties ||
|---|---|
| From class [ServiceStartNotAllowedException](../android/app/ServiceStartNotAllowedException.md) |-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](../android/app/ServiceStartNotAllowedException.md) <br /> | ||

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
