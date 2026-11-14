# TranslationManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TranslationManager

Kotlin| [Java](https://developer.android.com/reference/android/view/translation/TranslationManager "View this page in Java") 

```
class TranslationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.translation.TranslationManager](https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager#) |

The [TranslationManager](https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager#) class provides ways for apps to integrate and use the translation framework.

The TranslationManager manages [Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator) s and help bridge client calls to the server translation service

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnDeviceTranslationCapabilityUpdateListener](https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager#addOnDeviceTranslationCapabilityUpdateListener(java.util.concurrent.Executor,%20java.util.function.Consumer))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `capabilityListener:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability)!>`)` Adds a [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) Consumer to listen for updates on states of on-device [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) s. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createOnDeviceTranslator](https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager#createOnDeviceTranslator(android.view.translation.TranslationContext,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`translationContext:` ` [TranslationContext](https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator)!>`)` Creates an on-device Translator for natural language translation. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability)!\> | [getOnDeviceTranslationCapabilities](https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager#getOnDeviceTranslationCapabilities(kotlin.Int,%20kotlin.Int))`(`sourceFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `targetFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a set of [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) s describing the capabilities for on-device [Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator) s. |
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)? | [getOnDeviceTranslationSettingsActivityIntent](https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager#getOnDeviceTranslationSettingsActivityIntent())`()` Returns an immutable PendingIntent which can be used to launch an activity to view/edit on-device translation settings. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnDeviceTranslationCapabilityUpdateListener](https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager#removeOnDeviceTranslationCapabilityUpdateListener(java.util.function.Consumer))`(`capabilityListener:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability)!>`)` Removes a [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) Consumer to listen for updates on states of on-device [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) s. |

## Public methods

### addOnDeviceTranslationCapabilityUpdateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addOnDeviceTranslationCapabilityUpdateListener(
    executor: Executor, 
    capabilityListener: Consumer<TranslationCapability!>
): Unit
```

Adds a [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) Consumer to listen for updates on states of on-device [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) s.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capabilityListener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability)!\>:a [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) Consumer to receive the updated [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) from the on-device translation service. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |

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
| `translationContext` | [TranslationContext](https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext): [TranslationContext](https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext) containing the specs for creating the Translator. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):Executor to run callback operations This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator)!\>: [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#) to receive the translator. A`null`value is returned if the service could not create the translator. |

### getOnDeviceTranslationCapabilities

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOnDeviceTranslationCapabilities(
    sourceFormat: Int, 
    targetFormat: Int
): MutableSet<TranslationCapability!>
```

Returns a set of [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) s describing the capabilities for on-device [Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator) s.

These translation capabilities contains a source and target [TranslationSpec](https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec) representing the data expected for both ends of translation process. The capabilities provides the information and limitations for generating a [TranslationContext](https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext). The context object can then be used by [createOnDeviceTranslator(android.view.translation.TranslationContext,java.util.concurrent.Executor,java.util.function.Consumer)](https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager#createOnDeviceTranslator(android.view.translation.TranslationContext,%20java.util.concurrent.Executor,%20java.util.function.Consumer))to obtain a [Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator) for translations.

**NOTE:** Call on a worker thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):data format for the input data to be translated. Value is [android.view.translation.TranslationSpec#DATA_FORMAT_TEXT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec#DATA_FORMAT_TEXT:kotlin.Int) |
| `targetFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):data format for the expected translated output data. Value is [android.view.translation.TranslationSpec#DATA_FORMAT_TEXT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec#DATA_FORMAT_TEXT:kotlin.Int) |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability)!> | A set of [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) s. This value cannot be`null`. |

### getOnDeviceTranslationSettingsActivityIntent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOnDeviceTranslationSettingsActivityIntent(): PendingIntent?
```

Returns an immutable PendingIntent which can be used to launch an activity to view/edit on-device translation settings.

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)? | An immutable PendingIntent or`null`if one of reason met: - Device manufacturer (OEM) does not provide TranslationService. - The TranslationService doesn't provide the Settings. |

### removeOnDeviceTranslationCapabilityUpdateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeOnDeviceTranslationCapabilityUpdateListener(capabilityListener: Consumer<TranslationCapability!>): Unit
```

Removes a [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) Consumer to listen for updates on states of on-device [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) s.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capabilityListener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability)!\>:the [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) Consumer to unregister This value cannot be`null`. |
