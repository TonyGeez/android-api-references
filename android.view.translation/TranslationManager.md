# TranslationManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TranslationManager

Kotlin| [Java](TranslationManager.md) 
| --- | --- |

```
class TranslationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.translation.TranslationManager](TranslationManager.md) |

The [TranslationManager](TranslationManager.md) class provides ways for apps to integrate and use the translation framework.

The TranslationManager manages [Translator](Translator.md) s and help bridge client calls to the server translation service

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnDeviceTranslationCapabilityUpdateListener](TranslationManager.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `capabilityListener:` ` [Consumer](../java.util.function/Consumer.md)< [TranslationCapability](TranslationCapability.md)!>`)` Adds a [TranslationCapability](TranslationCapability.md) Consumer to listen for updates on states of on-device [TranslationCapability](TranslationCapability.md) s. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createOnDeviceTranslator](TranslationManager.md))`(`translationContext:` ` [TranslationContext](TranslationContext.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [Consumer](../java.util.function/Consumer.md)< [Translator](Translator.md)!>`)` Creates an on-device Translator for natural language translation. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [TranslationCapability](TranslationCapability.md)!\> | [getOnDeviceTranslationCapabilities](TranslationManager.md))`(`sourceFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `targetFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a set of [TranslationCapability](TranslationCapability.md) s describing the capabilities for on-device [Translator](Translator.md) s. |
| --- | --- |
| [PendingIntent](../android.app/PendingIntent.md)? | [getOnDeviceTranslationSettingsActivityIntent](TranslationManager.md))`()` Returns an immutable PendingIntent which can be used to launch an activity to view/edit on-device translation settings. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnDeviceTranslationCapabilityUpdateListener](TranslationManager.md))`(`capabilityListener:` ` [Consumer](../java.util.function/Consumer.md)< [TranslationCapability](TranslationCapability.md)!>`)` Removes a [TranslationCapability](TranslationCapability.md) Consumer to listen for updates on states of on-device [TranslationCapability](TranslationCapability.md) s. |

## Public methods

### addOnDeviceTranslationCapabilityUpdateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addOnDeviceTranslationCapabilityUpdateListener(
    executor: Executor, 
    capabilityListener: Consumer<TranslationCapability!>
): Unit
```

Adds a [TranslationCapability](TranslationCapability.md) Consumer to listen for updates on states of on-device [TranslationCapability](TranslationCapability.md) s.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capabilityListener` | [Consumer](../java.util.function/Consumer.md)\< [TranslationCapability](TranslationCapability.md)!\>:a [TranslationCapability](TranslationCapability.md) Consumer to receive the updated [TranslationCapability](TranslationCapability.md) from the on-device translation service. This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |

### createOnDeviceTranslator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createOnDeviceTranslator(
    translationContext: TranslationContext, 
    executor: Executor, 
    callback: Consumer<Translator!>
): Unit
```

Creates an on-device Translator for natural language translation.

In Android 12, this method provided the same cached Translator object when given the same TranslationContext object. Do not use a Translator destroyed elsewhere as this will cause an exception on Android 12.

In later versions, this method never returns a cached Translator.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `translationContext` | [TranslationContext](TranslationContext.md): [TranslationContext](TranslationContext.md) containing the specs for creating the Translator. This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):Executor to run callback operations This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [Translator](Translator.md)!\>: [Consumer](../java.util.function/Consumer.md) to receive the translator. A`null`value is returned if the service could not create the translator. |
| --- | --- |

### getOnDeviceTranslationCapabilities

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOnDeviceTranslationCapabilities(
    sourceFormat: Int, 
    targetFormat: Int
): MutableSet<TranslationCapability!>
```

Returns a set of [TranslationCapability](TranslationCapability.md) s describing the capabilities for on-device [Translator](Translator.md) s.

These translation capabilities contains a source and target [TranslationSpec](TranslationSpec.md) representing the data expected for both ends of translation process. The capabilities provides the information and limitations for generating a [TranslationContext](TranslationContext.md). The context object can then be used by [createOnDeviceTranslator(android.view.translation.TranslationContext,java.util.concurrent.Executor,java.util.function.Consumer)](TranslationManager.md))to obtain a [Translator](Translator.md) for translations.

**NOTE:** Call on a worker thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):data format for the input data to be translated. Value is [android.view.translation.TranslationSpec#DATA_FORMAT_TEXT](TranslationSpec.md) |
| `targetFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):data format for the expected translated output data. Value is [android.view.translation.TranslationSpec#DATA_FORMAT_TEXT](TranslationSpec.md) |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [TranslationCapability](TranslationCapability.md)!> | A set of [TranslationCapability](TranslationCapability.md) s. This value cannot be`null`. |

### getOnDeviceTranslationSettingsActivityIntent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOnDeviceTranslationSettingsActivityIntent(): PendingIntent?
```

Returns an immutable PendingIntent which can be used to launch an activity to view/edit on-device translation settings.

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PendingIntent](../android.app/PendingIntent.md)? | An immutable PendingIntent or`null`if one of reason met: - Device manufacturer (OEM) does not provide TranslationService. - The TranslationService doesn't provide the Settings. |

### removeOnDeviceTranslationCapabilityUpdateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeOnDeviceTranslationCapabilityUpdateListener(capabilityListener: Consumer<TranslationCapability!>): Unit
```

Removes a [TranslationCapability](TranslationCapability.md) Consumer to listen for updates on states of on-device [TranslationCapability](TranslationCapability.md) s.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capabilityListener` | [Consumer](../java.util.function/Consumer.md)\< [TranslationCapability](TranslationCapability.md)!\>:the [TranslationCapability](TranslationCapability.md) Consumer to unregister This value cannot be`null`. |
