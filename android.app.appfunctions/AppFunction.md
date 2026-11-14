Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppFunction

```
interface AppFunction
```

| [android.app.appfunctions.AppFunction](AppFunction.md) |

An interface for implementing the logic of an app function registered at runtime using registerAppFunction.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onExecuteAppFunction Called when the app function is invoked using android. |

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
| `request` | [ExecuteAppFunctionRequest](ExecuteAppFunctionRequest.md): The ExecuteAppFunctionRequest containing the parameters for this execution. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md): A signal to cancel the execution. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [ExecuteAppFunctionResponse](ExecuteAppFunctionResponse.md)!, [AppFunctionException](AppFunctionException.md)!\>: The `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#` that the implementation must use to return the result of the execution. It must be called exactly once with either a successful ExecuteAppFunctionResponse or an AppFunctionException in case of an error. This value cannot be `null`. |
| --- | --- |
