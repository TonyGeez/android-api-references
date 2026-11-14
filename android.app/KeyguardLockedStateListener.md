# KeyguardManager.KeyguardLockedStateListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyguardLockedStateListener

Kotlin| [Java](https://developer.android.com/reference/android/app/KeyguardManager.KeyguardLockedStateListener "View this page in Java") 

```
@FunctionalInterface interface KeyguardLockedStateListener
```

| [android.app.KeyguardManager.KeyguardLockedStateListener](https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardLockedStateListener#) |

Listener for keyguard locked state changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onKeyguardLockedStateChanged](https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardLockedStateListener#onKeyguardLockedStateChanged(kotlin.Boolean))`(`isKeyguardLocked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback function that executes when the keyguard locked state changes. |

## Public methods

### onKeyguardLockedStateChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onKeyguardLockedStateChanged(isKeyguardLocked: Boolean): Unit
```

Callback function that executes when the keyguard locked state changes.
