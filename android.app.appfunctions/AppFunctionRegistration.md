Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppFunctionRegistration

```
interface AppFunctionRegistration
```

| [android.app.appfunctions.AppFunctionRegistration](AppFunctionRegistration.md) |

Result of registerAppFunction.

The caller should retain a reference to this object and call unregister when the app function is no longer relevant (e.g., in onStop or before android.app.Service#stopForeground).

Failing to unregister the app function can lead to memory leaks and unexpected behavior, as the system will continue to hold a reference to the AppFunction object.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregister Unregisters the app function previously registered with registerAppFunction. |

## Public methods

### unregister

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun unregister(): Unit
```

Unregisters the app function previously registered with registerAppFunction.

If the app function was already unregistered, this method has no effect.
