Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppFunctionObservation

```
interface AppFunctionObservation
```

| [android.app.appfunctions.AppFunctionObservation](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionObservation#) |

Result of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#observeAppFunctions(java.util.concurrent.Executor,%20android.app.appfunctions.AppFunctionObserver)`.

The caller should retain a reference to this object and call `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionObservation#cancel()` when receiving updates to app functions is no longer required.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionObservation#cancel()()` Stops the observation previously started using `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#observeAppFunctions(java.util.concurrent.Executor,%20android.app.appfunctions.AppFunctionObserver)` from receiving updates. |

## Public methods

### cancel

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun cancel(): Unit
```

Stops the observation previously started using `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#observeAppFunctions(java.util.concurrent.Executor,%20android.app.appfunctions.AppFunctionObserver)` from receiving updates.

If the observation is already canceled, this method has no effect.
