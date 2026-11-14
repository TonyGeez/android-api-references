Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppFunctionObserver

```
interface AppFunctionObserver
```

| [android.app.appfunctions.AppFunctionObserver](AppFunctionObserver.md) |

Interface for observing changes to app functions provided to observeAppFunctions.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAppFunctionMetadataChanged Called when changes occur to a package exposing app functions that may impact the state or metadata of its contained functions. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAppFunctionStatesChanged Called when the runtime state of one or more app functions changes. |

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
- The package's AppFunctionPackageMetadata has been updated.

Upon receiving this notification, clients can call searchAppFunctions with setPackageNames to retrieve the updated AppFunctionMetadata for affected functions.

Clients should call getAppFunctionStates to retrieve the latest AppFunctionState for packages affected by these changes.

**Note:** If packages are reported to have changed but are not returned from searchAppFunctions, it means that the packages have been uninstalled or no longer have functions.

| Parameters ||
|---|---|
| `changedPackageNames` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: The names of the updated packages. This value cannot be `null`. |

### onAppFunctionStatesChanged

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onAppFunctionStatesChanged(changedFunctionNames: MutableSet<AppFunctionName!>): Unit
```

Called when the runtime state of one or more app functions changes.

Upon receiving this notification, clients can call getAppFunctionStates to retrieve the updated AppFunctionState for the affected functions.

| Parameters ||
|---|---|
| `changedFunctionNames` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppFunctionName](../android/app/appfunctions/AppFunctionName.md)!\>: The set of AppFunctionNames for the functions whose state has changed. This value cannot be `null`. |
