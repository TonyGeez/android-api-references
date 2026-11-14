Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppFunction

```
interface AppFunction
```

| [android.app.appfunctions.AppFunction](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunction#) |

An interface for implementing the logic of an app function registered at runtime using `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#registerAppFunction(kotlin.String,%20java.util.concurrent.Executor,%20android.app.appfunctions.AppFunction)`.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunction#onExecuteAppFunction(android.app.appfunctions.ExecuteAppFunctionRequest,%20android.os.CancellationSignal,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse!, https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException!>)` Called when the app function is invoked using android. |

## Public methods

### onExecuteAppFunction

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onExecuteAppFunction(
    request: ExecuteAppFunctionRequest, 
    cancellationSignal: CancellationSignal, 
    callback: OutcomeReceiver<ExecuteAppFunctionResponse!, AppFunctionException!>
): Unit
```

Called when the app function is invoked using android.app.appfunctions.AppFunctionManager#executeAppFunction.

The implementation should try to respect the provided `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#`, if possible.

| Parameters ||
|---|---|
| `request` | [ExecuteAppFunctionRequest](https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest): The `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest` containing the parameters for this execution. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#): A signal to cancel the execution. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [ExecuteAppFunctionResponse](https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse)!, [AppFunctionException](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException)!\>: The `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#` that the implementation must use to return the result of the execution. It must be called exactly once with either a successful `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse` or an `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException` in case of an error. This value cannot be `null`. |
| --- | --- |
