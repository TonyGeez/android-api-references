# ImplicitDirectBootViolation

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImplicitDirectBootViolation

Kotlin| [Java](../android/os/strictmode/ImplicitDirectBootViolation.md) 
| --- | --- |

```
class ImplicitDirectBootViolation : Violation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [android.os.strictmode.Violation](../android/os/strictmode/Violation.md) ||
| | | ↳ | [android.os.strictmode.ImplicitDirectBootViolation](../android/os/strictmode/ImplicitDirectBootViolation.md) |
| --- | --- | --- | --- |

Subclass of`Violation`that is used when a process implicitly relies on automatic Direct Boot filtering.

## Summary

| Inherited functions ||
|---|---|
| From class [Violation](../android/os/strictmode/Violation.md) |----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [fillInStackTrace](../android/os/strictmode/Violation.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/os/strictmode/Violation.md))`()` <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [initCause](../android/os/strictmode/Violation.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStackTrace](../android/os/strictmode/Violation.md))`(`stackTrace:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StackTraceElement](../java/lang/StackTraceElement.md)!>`)` <br /> | ||
