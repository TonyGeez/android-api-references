# KeyguardManager.OnKeyguardExitResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnKeyguardExitResult

Kotlin| [Java](https://developer.android.com/reference/android/app/KeyguardManager.OnKeyguardExitResult "View this page in Java") 

```
interface OnKeyguardExitResult
```

| [android.app.KeyguardManager.OnKeyguardExitResult](https://developer.android.com/reference/kotlin/android/app/KeyguardManager.OnKeyguardExitResult#) |

| **This interface was deprecated in API level 26.**
|
| Use [KeyguardDismissCallback](https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardDismissCallback)

Callback passed to [KeyguardManager.exitKeyguardSecurely](https://developer.android.com/reference/kotlin/android/app/KeyguardManager#exitKeyguardSecurely(android.app.KeyguardManager.OnKeyguardExitResult))to notify caller of result.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onKeyguardExitResult](https://developer.android.com/reference/kotlin/android/app/KeyguardManager.OnKeyguardExitResult#onKeyguardExitResult(kotlin.Boolean))`(`success:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |

## Public methods

### onKeyguardExitResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onKeyguardExitResult(success: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `success` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the user was able to authenticate, false if not. |
