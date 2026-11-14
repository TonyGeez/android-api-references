# android.app.appfunctions

## Interfaces

| [AppFunction](AppFunction.md) | An interface for implementing the logic of an app function registered at runtime using registerAppFunction. |
| --- | --- |
| [AppFunctionObservation](AppFunctionObservation.md) | Result of observeAppFunctions. |
| [AppFunctionObserver](AppFunctionObserver.md) | Interface for observing changes to app functions provided to observeAppFunctions. |
| [AppFunctionRegistration](AppFunctionRegistration.md) | Result of registerAppFunction. |
| --- | --- |

## Classes

| [AppFunctionActivityId](../android/app/appfunctions/AppFunctionActivityId.md) | An identifier of an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` an app function can be associated with. |
| --- | --- |
| [AppFunctionActivityState](AppFunctionActivityState.md) | The state of an activity from the perspective of app functions, retrieved using getAppFunctionActivityStates. |
| [AppFunctionManager](AppFunctionManager.md) | Provides access to App Functions. |
| [AppFunctionMetadata](AppFunctionMetadata.md) | Contains an app function's metadata, essential for its invocation and discovery, retrieved using searchAppFunctions. |
| --- | --- |
| [AppFunctionName](../android/app/appfunctions/AppFunctionName.md) | Globally unique identifier for an app function. |
| [AppFunctionPackageMetadata](../android/app/appfunctions/AppFunctionPackageMetadata.md) | Contains metadata about a package providing app functions. |
| [AppFunctionSchemaMetadata](AppFunctionSchemaMetadata.md) | Contains identifying metadata for a predefined schema, which can describe well-known function signatures. |
| --- | --- |
| [AppFunctionSearchSpec](AppFunctionSearchSpec.md) | Filter criteria for searchAppFunctions. |
| [AppFunctionService](AppFunctionService.md) | Extend this class to implement app functions, that can be executed by android. |
| [AppFunctionState](../android/app/appfunctions/AppFunctionState.md) | Runtime state of an app function, retrieved using getAppFunctionStates. |
| --- | --- |
| [AppFunctionUriGrant](AppFunctionUriGrant.md) | `https://developer.android.com/reference/kotlin/android/net/Uri.html#` for which access permission is to be granted to the caller of android. |
| [ExecuteAppFunctionRequest](ExecuteAppFunctionRequest.md) | A request to execute an app function, provided to android. |
| [ExecuteAppFunctionResponse](ExecuteAppFunctionResponse.md) | The response to an app function execution, returned by android. |
| --- | --- |
| [RegisterAppFunctionRequest](../android/app/appfunctions/RegisterAppFunctionRequest.md) | A request to register an AppFunction implementation, provided to registerAppFunctions. |

## Exceptions

| [AppFunctionException](AppFunctionException.md) | App function related error. |
| --- | --- |
