# UiTranslationStateCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UiTranslationStateCallback

Kotlin| [Java](https://developer.android.com/reference/android/view/translation/UiTranslationStateCallback "View this page in Java") 
| --- | --- |

```
interface UiTranslationStateCallback
```

| [android.view.translation.UiTranslationStateCallback](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#) |

Callback for listening to UI Translation state changes. See [android.view.translation.UiTranslationManager#registerUiTranslationStateCallback(java.util.concurrent.Executor,android.view.translation.UiTranslationStateCallback)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationManager#registerUiTranslationStateCallback(java.util.concurrent.Executor,%20android.view.translation.UiTranslationStateCallback)).

Prior to Android version [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int):

- Callback methods*without* `packageName`are invoked. Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int)*must*implement those methods if they want to handle the events.
- Callback methods for a particular event*may* be called multiple times consecutively, even when the translation state has not changed (e.g., [onStarted(android.icu.util.ULocale,android.icu.util.ULocale,java.lang.String)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onStarted(android.icu.util.ULocale,%20android.icu.util.ULocale,%20kotlin.String))may be called multiple times even after translation has already started).

In Android version [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int) and later:

- If both methods with and without`packageName`are implemented (e.g., [onFinished()](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onFinished())and [onFinished(java.lang.String)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onFinished(kotlin.String)), only the one*with* `packageName`will be called.
- Callback methods for a particular event will*not* be called multiple times consecutively. They will only be called when the translation state has actually changed (e.g., from "started" to "paused"). Note: "resumed" is not considered a separate state from "started", so [onResumed(android.icu.util.ULocale,android.icu.util.ULocale,java.lang.String)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onResumed(android.icu.util.ULocale,%20android.icu.util.ULocale,%20kotlin.String))will never be called after [onStarted(android.icu.util.ULocale,android.icu.util.ULocale,java.lang.String)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onStarted(android.icu.util.ULocale,%20android.icu.util.ULocale,%20kotlin.String)).\<

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFinished](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onFinished())`()` The UI Translation session has ended. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFinished](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onFinished(kotlin.String))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` The UI Translation session has ended. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPaused](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onPaused())`()` The system is requesting that the application temporarily show the UI contents in their original language. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPaused](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onPaused(kotlin.String))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` The system is requesting that the application temporarily show the UI contents in their original language. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResumed](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onResumed(android.icu.util.ULocale,%20android.icu.util.ULocale))`(`sourceLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)`, `targetLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)`)` The system is requesting that the application restore from the temporarily paused state and show the content in the translated language. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResumed](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onResumed(android.icu.util.ULocale,%20android.icu.util.ULocale,%20kotlin.String))`(`sourceLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)`, `targetLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` The system is requesting that the application restore from the temporarily paused state and show the content in the translated language. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStarted](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onStarted(android.icu.util.ULocale,%20android.icu.util.ULocale))`(`sourceLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)`, `targetLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)`)` The system is requesting translation of the UI from`sourceLocale`to`targetLocale`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStarted](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onStarted(android.icu.util.ULocale,%20android.icu.util.ULocale,%20kotlin.String))`(`sourceLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)`, `targetLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` The system is requesting translation of the UI from`sourceLocale`to`targetLocale`. |

## Public methods

### onFinished

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFinished(): Unit
```

The UI Translation session has ended.

Apps should implement [onFinished(java.lang.String)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onFinished(kotlin.String))as well if they need the name of the package that owns the activity being translated. 

### onFinished

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFinished(packageName: String): Unit
```

The UI Translation session has ended.

Apps*may* implement [onFinished()](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onFinished())instead if they don't need the name of the package that owns the activity being translated.

Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int)*must* implement [onFinished()](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onFinished())if they want to handle the "finished" event.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the package that owns the activity being translated. This value cannot be`null`. |

### onPaused

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPaused(): Unit
```

The system is requesting that the application temporarily show the UI contents in their original language.

Apps should implement [onPaused(java.lang.String)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onPaused(kotlin.String))as well if they need the name of the package that owns the activity being translated. 

### onPaused

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPaused(packageName: String): Unit
```

The system is requesting that the application temporarily show the UI contents in their original language.

Apps*may* implement [onPaused()](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onPaused())instead if they don't need the name of the package that owns the activity being translated.

Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int)*must* implement [onPaused()](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onPaused())if they want to handle the "paused" event.

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

Apps should implement [onResumed(android.icu.util.ULocale,android.icu.util.ULocale,java.lang.String)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onResumed(android.icu.util.ULocale,%20android.icu.util.ULocale,%20kotlin.String))instead if they need the name of the package that owns the activity being translated.

Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int)*must*implement this method if they want to handle the "resumed" event.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#): [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#) the UI is being translated from. This value cannot be`null`. |
| `targetLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#): [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#) the UI is being translated to. This value cannot be`null`. |

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

Apps*may* implement [onResumed(android.icu.util.ULocale,android.icu.util.ULocale)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onResumed(android.icu.util.ULocale,%20android.icu.util.ULocale))instead if they don't need the name of the package that owns the activity being translated.

Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int)*must* implement [onResumed(android.icu.util.ULocale,android.icu.util.ULocale)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onResumed(android.icu.util.ULocale,%20android.icu.util.ULocale))if they want to handle the "resumed" event.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#): [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#) the UI is being translated from. This value cannot be`null`. |
| `targetLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#): [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#) the UI is being translated to. This value cannot be`null`. |
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

Apps should implement [onStarted(android.icu.util.ULocale,android.icu.util.ULocale,java.lang.String)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onStarted(android.icu.util.ULocale,%20android.icu.util.ULocale,%20kotlin.String))instead if they need the name of the package that owns the activity being translated.

Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int)*must*implement this method if they want to handle the "started" event.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#): [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#) the UI is being translated from. This value cannot be`null`. |
| `targetLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#): [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#) the UI is being translated to. This value cannot be`null`. |

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

Apps*may* implement [onStarted(android.icu.util.ULocale,android.icu.util.ULocale)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onStarted(android.icu.util.ULocale,%20android.icu.util.ULocale))instead if they don't need the name of the package that owns the activity being translated.

Apps with minSdkVersion lower than [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int)*must* implement [onStarted(android.icu.util.ULocale,android.icu.util.ULocale)](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback#onStarted(android.icu.util.ULocale,%20android.icu.util.ULocale))if they want to handle the "started" event.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#): [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#) the UI is being translated from. This value cannot be`null`. |
| `targetLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#): [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#) the UI is being translated to. This value cannot be`null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the package that owns the activity being translated. This value cannot be`null`. |
| --- | --- |
