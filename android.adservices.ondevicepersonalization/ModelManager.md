# ModelManager

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ModelManager

Kotlin| [Java](https://developer.android.com/reference/android/adservices/ondevicepersonalization/ModelManager "View this page in Java") 
| --- | --- |

```
open class ModelManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.ModelManager](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ModelManager#) |

Handles model inference and only support TFLite model inference now. See [android.adservices.ondevicepersonalization.IsolatedService#getModelManager](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService#getModelManager(android.adservices.ondevicepersonalization.RequestToken)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ModelManager#run(android.adservices.ondevicepersonalization.InferenceInput,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`input:` ` [InferenceInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [InferenceOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Run a single model inference. |

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
| `input` | [InferenceInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput):contains all the information needed for a run of model inference. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [InferenceOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:this returns a [InferenceOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput) which contains model inference result or [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) on failure. This value cannot be`null`. |
| --- | --- |
