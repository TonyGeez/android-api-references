# VoiceInteractor

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VoiceInteractor

Kotlin| [Java](../android/app/VoiceInteractor.md) 
| --- | --- |

```
class VoiceInteractor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.VoiceInteractor](../android/app/VoiceInteractor.md) |

Interface for an [Activity](../android/app/Activity.md) to interact with the user through voice. Use [Activity.getVoiceInteractor](../android/app/Activity.md))to retrieve the interface, if the activity is currently involved in a voice interaction.

The voice interactor revolves around submitting voice interaction requests to the back-end voice interaction service that is working with the user. These requests are submitted with #submitRequest, providing a new instance of a [Request](../android/app/VoiceInteractor.Request.md) subclass describing the type of operation to perform -- currently the possible requests are [ConfirmationRequest](../android/app/VoiceInteractor.ConfirmationRequest.md) and [CommandRequest](../android/app/VoiceInteractor.CommandRequest.md).

Once a request is submitted, the voice system will process it and eventually deliver the result to the request object. The application can cancel a pending request at any time.

The VoiceInteractor is integrated with Activity's state saving mechanism, so that if an activity is being restarted with retained state, it will retain the current VoiceInteractor and any outstanding requests. Because of this, you should always use [Request.getActivity](../android/app/VoiceInteractor.Request.md))to get back to the activity of a request, rather than holding on to the activity instance yourself, either explicitly or implicitly through a non-static inner class.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [AbortVoiceRequest](../android/app/VoiceInteractor.AbortVoiceRequest.md) Reports that the current interaction can not be complete with voice, so the application will need to switch to a traditional input UI. |
| | [CommandRequest](../android/app/VoiceInteractor.CommandRequest.md) Execute a vendor-specific command using the trusted system VoiceInteractionService. |
| | [CompleteVoiceRequest](../android/app/VoiceInteractor.CompleteVoiceRequest.md) Reports that the current interaction was successfully completed with voice, so the application can report the final status to the user. |
| --- | --- |
| | [ConfirmationRequest](../android/app/VoiceInteractor.ConfirmationRequest.md) Confirms an operation with the user via the trusted system VoiceInteractionService. |
| | [PickOptionRequest](../android/app/VoiceInteractor.PickOptionRequest.md) Select a single option from multiple potential options with the user via the trusted system VoiceInteractionService. |
| | [Prompt](../android/app/VoiceInteractor.Prompt.md) A set of voice prompts to use with the voice interaction system to confirm an action, select an option, or do similar operations. |
| --- | --- |
| abstract | [Request](../android/app/VoiceInteractor.Request.md) Base class for voice interaction requests that can be submitted to the interactor. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [VoiceInteractor.Request](../android/app/VoiceInteractor.Request.md)! | [getActiveRequest](../android/app/VoiceInteractor.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return any currently active request that was submitted with the given name. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [VoiceInteractor.Request](../android/app/VoiceInteractor.Request.md)!\>! | [getActiveRequests](../android/app/VoiceInteractor.md))`()` Return all currently active requests. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackageName](../android/app/VoiceInteractor.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDestroyed](../android/app/VoiceInteractor.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDirectActionsChanged](../android/app/VoiceInteractor.md))`()` Notifies the assist framework that the direct actions supported by the app changed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerOnDestroyedCallback](../android/app/VoiceInteractor.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [Runnable](../java/lang/Runnable.md)`)` Registers a callback to be called when the VoiceInteractor is destroyed. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [submitRequest](../android/app/VoiceInteractor.md))`(`request:` ` [VoiceInteractor.Request](../android/app/VoiceInteractor.Request.md)!`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [submitRequest](../android/app/VoiceInteractor.md))`(`request:` ` [VoiceInteractor.Request](../android/app/VoiceInteractor.Request.md)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Submit a new [Request](../android/app/VoiceInteractor.Request.md) to the voice interaction service. |
| [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)! | [supportsCommands](../android/app/VoiceInteractor.md))`(`commands:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Queries the supported commands available from the VoiceInteractionService. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unregisterOnDestroyedCallback](../android/app/VoiceInteractor.md))`(`callback:` ` [Runnable](../java/lang/Runnable.md)`)` Unregisters a previously registered onDestroy callback |

## Public methods

### getActiveRequest

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActiveRequest(name: String!): VoiceInteractor.Request!
```

Return any currently active request that was submitted with the given name.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name used to submit the request, as per [submitRequest(android.app.VoiceInteractor.Request,java.lang.String)](../android/app/VoiceInteractor.md)). |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [VoiceInteractor.Request](../android/app/VoiceInteractor.Request.md)! | Returns the active request with that name, or null if there was none. |

### getActiveRequests

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActiveRequests(): Array<VoiceInteractor.Request!>!
```

Return all currently active requests. 

### getPackageName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageName(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the package name of the service providing the VoiceInteractionService. This value cannot be`null`. |

### isDestroyed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDestroyed(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the voice interactor is destroyed. You should not interact with a destroyed voice interactor. |

### notifyDirectActionsChanged

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyDirectActionsChanged(): Unit
```

Notifies the assist framework that the direct actions supported by the app changed. 

### registerOnDestroyedCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerOnDestroyedCallback(
    executor: Executor, 
    callback: Runnable
): Boolean
```

Registers a callback to be called when the VoiceInteractor is destroyed.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):Executor on which to run the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [Runnable](../java/lang/Runnable.md):The callback to run. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the callback was registered. |

### submitRequest

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun submitRequest(request: VoiceInteractor.Request!): Boolean
```  

### submitRequest

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun submitRequest(
    request: VoiceInteractor.Request!, 
    name: String!
): Boolean
```

Submit a new [Request](../android/app/VoiceInteractor.Request.md) to the voice interaction service. The request must be one of the available subclasses -- [ConfirmationRequest](../android/app/VoiceInteractor.ConfirmationRequest.md), [PickOptionRequest](../android/app/VoiceInteractor.PickOptionRequest.md), [CompleteVoiceRequest](../android/app/VoiceInteractor.CompleteVoiceRequest.md), [AbortVoiceRequest](../android/app/VoiceInteractor.AbortVoiceRequest.md), or [CommandRequest](../android/app/VoiceInteractor.CommandRequest.md).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [VoiceInteractor.Request](../android/app/VoiceInteractor.Request.md)!:The desired request to submit. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:An optional name for this request, or null. This can be used later with [getActiveRequests](../android/app/VoiceInteractor.md))and [getActiveRequest](../android/app/VoiceInteractor.md))to find the request. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true of the request was successfully submitted, else false. |

### supportsCommands

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun supportsCommands(commands: Array<String!>!): BooleanArray!
```

Queries the supported commands available from the VoiceInteractionService. The command is a string that describes the generic operation to be performed. An example might be "org.example.commands.PICK_DATE" to ask the user to pick a date. (Note: This is not an actual working example.)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `commands` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The array of commands to query for support. |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)! | Array of booleans indicating whether each command is supported or not. |

### unregisterOnDestroyedCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterOnDestroyedCallback(callback: Runnable): Boolean
```

Unregisters a previously registered onDestroy callback

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Runnable](../java/lang/Runnable.md):The callback to remove. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the callback was unregistered. |
