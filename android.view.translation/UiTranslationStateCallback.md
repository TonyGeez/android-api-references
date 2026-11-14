# UiTranslationStateCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UiTranslationStateCallback

Kotlin| [Java](../android/view/translation/UiTranslationStateCallback.md) 
| --- | --- |

```
interface UiTranslationStateCallback
```

| [android.view.translation.UiTranslationStateCallback](../android/view/translation/UiTranslationStateCallback.md) |

Callback for listening to UI Translation state changes. See [android.view.translation.UiTranslationManager#registerUiTranslationStateCallback(java.util.concurrent.Executor,android.view.translation.UiTranslationStateCallback)](../android/view/translation/UiTranslationManager.md)).

Prior to Android version [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md):

- Callback methods*without* `packageName`are invoked. Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md)*must*implement those methods if they want to handle the events.
- Callback methods for a particular event*may* be called multiple times consecutively, even when the translation state has not changed (e.g., [onStarted(android.icu.util.ULocale,android.icu.util.ULocale,java.lang.String)](../android/view/translation/UiTranslationStateCallback.md))may be called multiple times even after translation has already started).

In Android version [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md) and later:

- If both methods with and without`packageName`are implemented (e.g., [onFinished()](../android/view/translation/UiTranslationStateCallback.md))and [onFinished(java.lang.String)](../android/view/translation/UiTranslationStateCallback.md)), only the one*with* `packageName`will be called.
- Callback methods for a particular event will*not* be called multiple times consecutively. They will only be called when the translation state has actually changed (e.g., from "started" to "paused"). Note: "resumed" is not considered a separate state from "started", so [onResumed(android.icu.util.ULocale,android.icu.util.ULocale,java.lang.String)](../android/view/translation/UiTranslationStateCallback.md))will never be called after [onStarted(android.icu.util.ULocale,android.icu.util.ULocale,java.lang.String)](../android/view/translation/UiTranslationStateCallback.md)).\<

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFinished](../android/view/translation/UiTranslationStateCallback.md))`()` The UI Translation session has ended. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFinished](../android/view/translation/UiTranslationStateCallback.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` The UI Translation session has ended. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPaused](../android/view/translation/UiTranslationStateCallback.md))`()` The system is requesting that the application temporarily show the UI contents in their original language. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPaused](../android/view/translation/UiTranslationStateCallback.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` The system is requesting that the application temporarily show the UI contents in their original language. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResumed](../android/view/translation/UiTranslationStateCallback.md))`(`sourceLocale:` ` [ULocale](../android/icu/util/ULocale.md)`, `targetLocale:` ` [ULocale](../android/icu/util/ULocale.md)`)` The system is requesting that the application restore from the temporarily paused state and show the content in the translated language. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResumed](../android/view/translation/UiTranslationStateCallback.md))`(`sourceLocale:` ` [ULocale](../android/icu/util/ULocale.md)`, `targetLocale:` ` [ULocale](../android/icu/util/ULocale.md)`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` The system is requesting that the application restore from the temporarily paused state and show the content in the translated language. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStarted](../android/view/translation/UiTranslationStateCallback.md))`(`sourceLocale:` ` [ULocale](../android/icu/util/ULocale.md)`, `targetLocale:` ` [ULocale](../android/icu/util/ULocale.md)`)` The system is requesting translation of the UI from`sourceLocale`to`targetLocale`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStarted](../android/view/translation/UiTranslationStateCallback.md))`(`sourceLocale:` ` [ULocale](../android/icu/util/ULocale.md)`, `targetLocale:` ` [ULocale](../android/icu/util/ULocale.md)`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` The system is requesting translation of the UI from`sourceLocale`to`targetLocale`. |

## Public methods

### onFinished

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFinished(): Unit
```

The UI Translation session has ended.

Apps should implement [onFinished(java.lang.String)](../android/view/translation/UiTranslationStateCallback.md))as well if they need the name of the package that owns the activity being translated. 

### onFinished

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFinished(packageName: String): Unit
```

The UI Translation session has ended.

Apps*may* implement [onFinished()](../android/view/translation/UiTranslationStateCallback.md))instead if they don't need the name of the package that owns the activity being translated.

Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md)*must* implement [onFinished()](../android/view/translation/UiTranslationStateCallback.md))if they want to handle the "finished" event.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the package that owns the activity being translated. This value cannot be`null`. |

### onPaused

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPaused(): Unit
```

The system is requesting that the application temporarily show the UI contents in their original language.

Apps should implement [onPaused(java.lang.String)](../android/view/translation/UiTranslationStateCallback.md))as well if they need the name of the package that owns the activity being translated. 

### onPaused

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPaused(packageName: String): Unit
```

The system is requesting that the application temporarily show the UI contents in their original language.

Apps*may* implement [onPaused()](../android/view/translation/UiTranslationStateCallback.md))instead if they don't need the name of the package that owns the activity being translated.

Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md)*must* implement [onPaused()](../android/view/translation/UiTranslationStateCallback.md))if they want to handle the "paused" event.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

### onResumed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onResumed(
    sourceLocale: ULocale, 
    targetLocale: ULocale
): Unit
```

The system is requesting that the application restore from the temporarily paused state and show the content in the translated language.

Apps should implement [onResumed(android.icu.util.ULocale,android.icu.util.ULocale,java.lang.String)](../android/view/translation/UiTranslationStateCallback.md))instead if they need the name of the package that owns the activity being translated.

Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md)*must*implement this method if they want to handle the "resumed" event.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceLocale` | [ULocale](../android/icu/util/ULocale.md): [ULocale](../android/icu/util/ULocale.md) the UI is being translated from. This value cannot be`null`. |
| `targetLocale` | [ULocale](../android/icu/util/ULocale.md): [ULocale](../android/icu/util/ULocale.md) the UI is being translated to. This value cannot be`null`. |

### onResumed

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onResumed(
    sourceLocale: ULocale, 
    targetLocale: ULocale, 
    packageName: String
): Unit
```

The system is requesting that the application restore from the temporarily paused state and show the content in the translated language.

Apps*may* implement [onResumed(android.icu.util.ULocale,android.icu.util.ULocale)](../android/view/translation/UiTranslationStateCallback.md))instead if they don't need the name of the package that owns the activity being translated.

Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md)*must* implement [onResumed(android.icu.util.ULocale,android.icu.util.ULocale)](../android/view/translation/UiTranslationStateCallback.md))if they want to handle the "resumed" event.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceLocale` | [ULocale](../android/icu/util/ULocale.md): [ULocale](../android/icu/util/ULocale.md) the UI is being translated from. This value cannot be`null`. |
| `targetLocale` | [ULocale](../android/icu/util/ULocale.md): [ULocale](../android/icu/util/ULocale.md) the UI is being translated to. This value cannot be`null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the package that owns the activity being translated. This value cannot be`null`. |
| --- | --- |

### onStarted

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStarted(
    sourceLocale: ULocale, 
    targetLocale: ULocale
): Unit
```

The system is requesting translation of the UI from`sourceLocale`to`targetLocale`.

This is also called if either the requested`sourceLocale`or`targetLocale`has changed.

Apps should implement [onStarted(android.icu.util.ULocale,android.icu.util.ULocale,java.lang.String)](../android/view/translation/UiTranslationStateCallback.md))instead if they need the name of the package that owns the activity being translated.

Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md)*must*implement this method if they want to handle the "started" event.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceLocale` | [ULocale](../android/icu/util/ULocale.md): [ULocale](../android/icu/util/ULocale.md) the UI is being translated from. This value cannot be`null`. |
| `targetLocale` | [ULocale](../android/icu/util/ULocale.md): [ULocale](../android/icu/util/ULocale.md) the UI is being translated to. This value cannot be`null`. |

### onStarted

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStarted(
    sourceLocale: ULocale, 
    targetLocale: ULocale, 
    packageName: String
): Unit
```

The system is requesting translation of the UI from`sourceLocale`to`targetLocale`.

This is also called if either the requested`sourceLocale`or`targetLocale`has changed.

Apps*may* implement [onStarted(android.icu.util.ULocale,android.icu.util.ULocale)](../android/view/translation/UiTranslationStateCallback.md))instead if they don't need the name of the package that owns the activity being translated.

Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md)*must* implement [onStarted(android.icu.util.ULocale,android.icu.util.ULocale)](../android/view/translation/UiTranslationStateCallback.md))if they want to handle the "started" event.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceLocale` | [ULocale](../android/icu/util/ULocale.md): [ULocale](../android/icu/util/ULocale.md) the UI is being translated from. This value cannot be`null`. |
| `targetLocale` | [ULocale](../android/icu/util/ULocale.md): [ULocale](../android/icu/util/ULocale.md) the UI is being translated to. This value cannot be`null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the package that owns the activity being translated. This value cannot be`null`. |
| --- | --- |
