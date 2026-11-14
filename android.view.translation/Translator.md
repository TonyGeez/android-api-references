# Translator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Translator

Kotlin| [Java](https://developer.android.com/reference/android/view/translation/Translator "View this page in Java") 

```
open class Translator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.translation.Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator#) |

The [Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator#) for translation, defined by a [TranslationContext](https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](https://developer.android.com/reference/kotlin/android/view/translation/Translator#destroy())`()` Destroy this Translator. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDestroyed](https://developer.android.com/reference/kotlin/android/view/translation/Translator#isDestroyed())`()` Returns whether or not this Translator has been destroyed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [translate](https://developer.android.com/reference/kotlin/android/view/translation/Translator#translate(android.view.translation.TranslationRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`request:` ` [TranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest)`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [TranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse)!>`)` Requests a translation for the provided [TranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest) using the Translator's source spec and destination spec. |

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

Requests a translation for the provided [TranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest) using the Translator's source spec and destination spec.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [TranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest): [TranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest) request to be translate. This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:signal to cancel the operation in progress. This value may be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):Executor to run callback operations This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [TranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse)!\>: [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#) to receive the translation response. Multiple responses may be received if [TranslationRequest.FLAG_PARTIAL_RESPONSES](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_PARTIAL_RESPONSES:kotlin.Int) is set. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value may be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------|
| `java.lang.IllegalStateException` | if this Translator session was destroyed when called. |
