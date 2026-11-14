# NonSdkApiUsedViolation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NonSdkApiUsedViolation

Kotlin| [Java](../android/os/strictmode/NonSdkApiUsedViolation.md) 
| --- | --- |

```
class NonSdkApiUsedViolation : Violation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [android.os.strictmode.Violation](../android/os/strictmode/Violation.md) ||
| | | ↳ | [android.os.strictmode.NonSdkApiUsedViolation](../android/os/strictmode/NonSdkApiUsedViolation.md) |
| --- | --- | --- | --- |

Subclass of`Violation`that is used when a process accesses a non SDK API.

## Summary

| Inherited functions ||
|---|---|
| From class [Violation](../android/os/strictmode/Violation.md) |----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [fillInStackTrace](../android/os/strictmode/Violation.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/os/strictmode/Violation.md))`()` <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [initCause](../android/os/strictmode/Violation.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStackTrace](../android/os/strictmode/Violation.md))`(`stackTrace:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StackTraceElement](../java/lang/StackTraceElement.md)!>`)` <br /> | ||
