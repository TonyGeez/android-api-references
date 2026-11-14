# KeyguardManager.KeyguardLockedStateListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyguardLockedStateListener

Kotlin| [Java](../android/app/KeyguardManager.KeyguardLockedStateListener.md) 
| --- | --- |

```
@FunctionalInterface interface KeyguardLockedStateListener
```

| [android.app.KeyguardManager.KeyguardLockedStateListener](../android/app/KeyguardManager.KeyguardLockedStateListener.md) |

Listener for keyguard locked state changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onKeyguardLockedStateChanged](../android/app/KeyguardManager.KeyguardLockedStateListener.md))`(`isKeyguardLocked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback function that executes when the keyguard locked state changes. |

## Public methods

### onKeyguardLockedStateChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onKeyguardLockedStateChanged(isKeyguardLocked: Boolean): Unit
```

Callback function that executes when the keyguard locked state changes.
