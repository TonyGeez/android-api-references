# ForegroundServiceTypeException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ForegroundServiceTypeException

Kotlin| [Java](ForegroundServiceTypeException.md) 
| --- | --- |

```
abstract class ForegroundServiceTypeException : ServiceStartNotAllowedException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java.lang/IllegalStateException.md) |||
| | | | | ↳ | [android.app.ServiceStartNotAllowedException](ServiceStartNotAllowedException.md) ||
| | | | | | ↳ | [android.app.ForegroundServiceTypeException](ForegroundServiceTypeException.md) |
| --- | --- | --- | --- | --- | --- | --- |

| Known Direct Subclasses [InvalidForegroundServiceTypeException](InvalidForegroundServiceTypeException.md), [MissingForegroundServiceTypeException](MissingForegroundServiceTypeException.md) |-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InvalidForegroundServiceTypeException](InvalidForegroundServiceTypeException.md) | Exception thrown when an app tries to start a foreground [Service](Service.md) with an invalid type. | | [MissingForegroundServiceTypeException](MissingForegroundServiceTypeException.md) | Exception thrown when an app tries to start a foreground [Service](Service.md) without a type. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base exception thrown when an app tries to start a foreground [Service](Service.md) without a valid type.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ForegroundServiceTypeException](ForegroundServiceTypeException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructor. |

| Inherited properties ||
|---|---|
| From class [ServiceStartNotAllowedException](ServiceStartNotAllowedException.md) |-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](ServiceStartNotAllowedException.md) <br /> | ||

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
