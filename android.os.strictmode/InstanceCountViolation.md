# InstanceCountViolation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstanceCountViolation

Kotlin| [Java](InstanceCountViolation.md) 
| --- | --- |

```
open class InstanceCountViolation : Violation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [android.os.strictmode.Violation](Violation.md) ||
| | | ↳ | [android.os.strictmode.InstanceCountViolation](InstanceCountViolation.md) |
| --- | --- | --- | --- |

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNumberOfInstances](InstanceCountViolation.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [Violation](Violation.md) |----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [fillInStackTrace](Violation.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Violation.md))`()` <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [initCause](Violation.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStackTrace](Violation.md))`(`stackTrace:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StackTraceElement](../java.lang/StackTraceElement.md)!>`)` <br /> | ||

## Public methods

### getNumberOfInstances

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumberOfInstances(): Long
```
