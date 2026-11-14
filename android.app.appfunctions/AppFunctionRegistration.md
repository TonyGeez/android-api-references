Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppFunctionRegistration

```
interface AppFunctionRegistration
```

| [android.app.appfunctions.AppFunctionRegistration](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionRegistration#) |

Result of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#registerAppFunction(kotlin.String,%20java.util.concurrent.Executor,%20android.app.appfunctions.AppFunction)`.

The caller should retain a reference to this object and call `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionRegistration#unregister()` when the app function is no longer relevant (e.g., in `https://developer.android.com/reference/kotlin/android/app/Activity.html#onStop()` or before android.app.Service#stopForeground).

Failing to unregister the app function can lead to memory leaks and unexpected behavior, as the system will continue to hold a reference to the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunction` object.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionRegistration#unregister()()` Unregisters the app function previously registered with `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#registerAppFunction(kotlin.String,%20java.util.concurrent.Executor,%20android.app.appfunctions.AppFunction)`. |

## Public methods

### unregister

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun unregister(): Unit
```

Unregisters the app function previously registered with `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#registerAppFunction(kotlin.String,%20java.util.concurrent.Executor,%20android.app.appfunctions.AppFunction)`.

If the app function was already unregistered, this method has no effect.
