# android.app.appfunctions

## Interfaces

| [AppFunction](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunction) | An interface for implementing the logic of an app function registered at runtime using `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#registerAppFunction(kotlin.String,%20java.util.concurrent.Executor,%20android.app.appfunctions.AppFunction)`. |
| [AppFunctionObservation](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionObservation) | Result of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#observeAppFunctions(java.util.concurrent.Executor,%20android.app.appfunctions.AppFunctionObserver)`. |
| [AppFunctionObserver](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionObserver) | Interface for observing changes to app functions provided to `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#observeAppFunctions(java.util.concurrent.Executor,%20android.app.appfunctions.AppFunctionObserver)`. |
| [AppFunctionRegistration](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionRegistration) | Result of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#registerAppFunction(kotlin.String,%20java.util.concurrent.Executor,%20android.app.appfunctions.AppFunction)`. |

## Classes

| [AppFunctionActivityId](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionActivityId) | An identifier of an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` an app function can be associated with. |
| [AppFunctionActivityState](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionActivityState) | The state of an activity from the perspective of app functions, retrieved using `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#getAppFunctionActivityStates(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [AppFunctionManager](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager) | Provides access to App Functions. |
| [AppFunctionMetadata](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata) | Contains an app function's metadata, essential for its invocation and discovery, retrieved using `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#searchAppFunctions(android.app.appfunctions.AppFunctionSearchSpec,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [AppFunctionName](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionName) | Globally unique identifier for an app function. |
| [AppFunctionPackageMetadata](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionPackageMetadata) | Contains metadata about a package providing app functions. |
| [AppFunctionSchemaMetadata](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionSchemaMetadata) | Contains identifying metadata for a predefined schema, which can describe well-known function signatures. |
| [AppFunctionSearchSpec](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionSearchSpec) | Filter criteria for `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#searchAppFunctions(android.app.appfunctions.AppFunctionSearchSpec,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [AppFunctionService](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionService) | Extend this class to implement app functions, that can be executed by android. |
| [AppFunctionState](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionState) | Runtime state of an app function, retrieved using `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#getAppFunctionStates(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [AppFunctionUriGrant](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant) | `https://developer.android.com/reference/kotlin/android/net/Uri.html#` for which access permission is to be granted to the caller of android. |
| [ExecuteAppFunctionRequest](https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest) | A request to execute an app function, provided to android. |
| [ExecuteAppFunctionResponse](https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse) | The response to an app function execution, returned by android. |
| [RegisterAppFunctionRequest](https://developer.android.com/reference/kotlin/android/app/appfunctions/RegisterAppFunctionRequest) | A request to register an `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunction` implementation, provided to `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#registerAppFunctions(kotlin.collections.MutableList)`. |

## Exceptions

| [AppFunctionException](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException) | App function related error. |
