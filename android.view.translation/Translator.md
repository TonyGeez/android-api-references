# Translator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Translator

Kotlin| [Java](../android/view/translation/Translator.md) 
| --- | --- |

```
open class Translator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.translation.Translator](../android/view/translation/Translator.md) |

The [Translator](../android/view/translation/Translator.md) for translation, defined by a [TranslationContext](../android/view/translation/TranslationContext.md).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](../android/view/translation/Translator.md))`()` Destroy this Translator. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDestroyed](../android/view/translation/Translator.md))`()` Returns whether or not this Translator has been destroyed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [translate](../android/view/translation/Translator.md))`(`request:` ` [TranslationRequest](../android/view/translation/TranslationRequest.md)`, `cancellationSignal:` ` [CancellationSignal](../android/os/CancellationSignal.md)?`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [Consumer](../java/util/function/Consumer.md)< [TranslationResponse](../android/view/translation/TranslationResponse.md)!>`)` Requests a translation for the provided [TranslationRequest](../android/view/translation/TranslationRequest.md) using the Translator's source spec and destination spec. |
| --- | --- |

## Public methods

### destroy

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun destroy(): Unit
```

Destroy this Translator. 

### isDestroyed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDestroyed(): Boolean
```

Returns whether or not this Translator has been destroyed. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/view/translation/Translator#destroy()> 

### translate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun translate(
    request: TranslationRequest, 
    cancellationSignal: CancellationSignal?, 
    executor: Executor, 
    callback: Consumer<TranslationResponse!>
): Unit
```

Requests a translation for the provided [TranslationRequest](../android/view/translation/TranslationRequest.md) using the Translator's source spec and destination spec.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [TranslationRequest](../android/view/translation/TranslationRequest.md): [TranslationRequest](../android/view/translation/TranslationRequest.md) request to be translate. This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](../android/os/CancellationSignal.md)?:signal to cancel the operation in progress. This value may be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):Executor to run callback operations This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](../java/util/function/Consumer.md)\< [TranslationResponse](../android/view/translation/TranslationResponse.md)!\>: [Consumer](../java/util/function/Consumer.md) to receive the translation response. Multiple responses may be received if [TranslationRequest.FLAG_PARTIAL_RESPONSES](../android/view/translation/TranslationRequest.md) is set. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value may be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------|
| `java.lang.IllegalStateException` | if this Translator session was destroyed when called. |
