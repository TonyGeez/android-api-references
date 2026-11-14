# ModelManager

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ModelManager

Kotlin| [Java](ModelManager.md) 
| --- | --- |

```
open class ModelManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.ModelManager](ModelManager.md) |

Handles model inference and only support TFLite model inference now. See [android.adservices.ondevicepersonalization.IsolatedService#getModelManager](IsolatedService.md)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](ModelManager.md))`(`input:` ` [InferenceInput](InferenceInput.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [InferenceOutput](InferenceOutput.md)!,` ` [Exception](../java.lang/Exception.md)!>`)` Run a single model inference. |

## Public methods

### run

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun run(
    input: InferenceInput, 
    executor: Executor, 
    receiver: OutcomeReceiver<InferenceOutput!, Exception!>
): Unit
```

Run a single model inference. Only supports TFLite model inference now. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [InferenceInput](InferenceInput.md):contains all the information needed for a run of model inference. This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):the [Executor](../java.util.concurrent/Executor.md) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [InferenceOutput](InferenceOutput.md)!, [Exception](../java.lang/Exception.md)!\>:this returns a [InferenceOutput](InferenceOutput.md) which contains model inference result or [Exception](../java.lang/Exception.md) on failure. This value cannot be`null`. |
| --- | --- |
