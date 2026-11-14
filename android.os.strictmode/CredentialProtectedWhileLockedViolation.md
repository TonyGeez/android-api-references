# CredentialProtectedWhileLockedViolation

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CredentialProtectedWhileLockedViolation

Kotlin| [Java](https://developer.android.com/reference/android/os/strictmode/CredentialProtectedWhileLockedViolation "View this page in Java") 
| --- | --- |

```
class CredentialProtectedWhileLockedViolation : Violation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [android.os.strictmode.Violation](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation) ||
| | | ↳ | [android.os.strictmode.CredentialProtectedWhileLockedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/CredentialProtectedWhileLockedViolation#) |
| --- | --- | --- | --- |

Subclass of`Violation`that is used when a process accesses filesystem paths stored in credential protected storage areas while the user is locked.

When a user is locked, credential protected storage is unavailable, and files stored in these locations appear to not exist, which can result in subtle app bugs if they assume default behaviors or empty states. Instead, apps should store data needed while a user is locked under device protected storage areas.

## Summary

| Inherited functions ||
|---|---|
| From class [Violation](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation) |----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [fillInStackTrace](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation#fillInStackTrace())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation#hashCode())`()` <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [initCause](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation#initCause(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStackTrace](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation#setStackTrace(kotlin.Array))`(`stackTrace:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StackTraceElement](https://developer.android.com/reference/kotlin/java/lang/StackTraceElement.html#)!>`)` <br /> | ||
