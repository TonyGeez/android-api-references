# CredentialProtectedWhileLockedViolation

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CredentialProtectedWhileLockedViolation

Kotlin| [Java](CredentialProtectedWhileLockedViolation.md) 
| --- | --- |

```
class CredentialProtectedWhileLockedViolation : Violation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [android.os.strictmode.Violation](Violation.md) ||
| | | ↳ | [android.os.strictmode.CredentialProtectedWhileLockedViolation](CredentialProtectedWhileLockedViolation.md) |
| --- | --- | --- | --- |

Subclass of`Violation`that is used when a process accesses filesystem paths stored in credential protected storage areas while the user is locked.

When a user is locked, credential protected storage is unavailable, and files stored in these locations appear to not exist, which can result in subtle app bugs if they assume default behaviors or empty states. Instead, apps should store data needed while a user is locked under device protected storage areas.

## Summary

| Inherited functions ||
|---|---|
| From class [Violation](Violation.md) |----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [fillInStackTrace](Violation.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Violation.md))`()` <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [initCause](Violation.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStackTrace](Violation.md))`(`stackTrace:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StackTraceElement](../java.lang/StackTraceElement.md)!>`)` <br /> | ||
