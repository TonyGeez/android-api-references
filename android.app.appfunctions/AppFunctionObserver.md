Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppFunctionObserver

```
interface AppFunctionObserver
```

| [android.app.appfunctions.AppFunctionObserver](AppFunctionObserver.md) |

Interface for observing changes to app functions provided to `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#observeAppFunctions(java.util.concurrent.Executor,%20android.app.appfunctions.AppFunctionObserver)`.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionObserver#onAppFunctionMetadataChanged(kotlin.collections.MutableSet)(changedPackageNames: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Called when changes occur to a package exposing app functions that may impact the state or metadata of its contained functions. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionObserver#onAppFunctionStatesChanged(kotlin.collections.MutableSet)(changedFunctionNames: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionName!>)` Called when the runtime state of one or more app functions changes. |

## Public methods

### onAppFunctionMetadataChanged

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onAppFunctionMetadataChanged(changedPackageNames: MutableSet<String!>): Unit
```

Called when changes occur to a package exposing app functions that may impact the state or metadata of its contained functions.

This includes changes such as:

- The definition of a function metadata exposed by the package has changed (e.g, the parameters of the function have changed).
- All functions within the package are added or removed due to the package being installed or uninstalled.
- The package's `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionPackageMetadata` has been updated.

Upon receiving this notification, clients can call `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#searchAppFunctions(android.app.appfunctions.AppFunctionSearchSpec,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` with `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionSearchSpec.Builder#setPackageNames(kotlin.collections.MutableSet)` to retrieve the updated `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata` for affected functions.

Clients should call `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#getAppFunctionStates(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` to retrieve the latest `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionState` for packages affected by these changes.

**Note:** If packages are reported to have changed but are not returned from `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#searchAppFunctions(android.app.appfunctions.AppFunctionSearchSpec,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`, it means that the packages have been uninstalled or no longer have functions.

| Parameters ||
|---|---|
| `changedPackageNames` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: The names of the updated packages. This value cannot be `null`. |

### onAppFunctionStatesChanged

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onAppFunctionStatesChanged(changedFunctionNames: MutableSet<AppFunctionName!>): Unit
```

Called when the runtime state of one or more app functions changes.

Upon receiving this notification, clients can call `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#getAppFunctionStates(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` to retrieve the updated `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionState` for the affected functions.

| Parameters ||
|---|---|
| `changedFunctionNames` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppFunctionName](../android/app/appfunctions/AppFunctionName.md)!\>: The set of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionName`s for the functions whose state has changed. This value cannot be `null`. |
