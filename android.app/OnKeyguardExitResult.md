# KeyguardManager.OnKeyguardExitResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnKeyguardExitResult

Kotlin| [Java](../android/app/KeyguardManager.OnKeyguardExitResult.md) 
| --- | --- |

```
interface OnKeyguardExitResult
```

| [android.app.KeyguardManager.OnKeyguardExitResult](../android/app/KeyguardManager.OnKeyguardExitResult.md) |

| **This interface was deprecated in API level 26.**
|
| Use [KeyguardDismissCallback](../android/app/KeyguardManager.KeyguardDismissCallback.md)

Callback passed to [KeyguardManager.exitKeyguardSecurely](../android/app/KeyguardManager.md))to notify caller of result.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onKeyguardExitResult](../android/app/KeyguardManager.OnKeyguardExitResult.md))`(`success:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |

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
