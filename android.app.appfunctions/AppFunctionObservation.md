Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppFunctionObservation

```
interface AppFunctionObservation
```

| [android.app.appfunctions.AppFunctionObservation](AppFunctionObservation.md) |

Result of observeAppFunctions.

The caller should retain a reference to this object and call cancel when receiving updates to app functions is no longer required.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancel Stops the observation previously started using observeAppFunctions from receiving updates. |

## Public methods

### cancel

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun cancel(): Unit
```

Stops the observation previously started using observeAppFunctions from receiving updates.

If the observation is already canceled, this method has no effect.
