# TextServicesManager

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextServicesManager

Kotlin| [Java](TextServicesManager.md) 
| --- | --- |

```
class TextServicesManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textservice.TextServicesManager](TextServicesManager.md) |

System API to the overall text services, which arbitrates interaction between applications and text services. The user can change the current text services in Settings. And also applications can specify the target text services.

### Architecture Overview

<br />

There are three primary parties involved in the text services framework (TSF) architecture:

- The**text services manager**as expressed by this class is the central point of the system that manages interaction between all other parts. It is expressed as the client-side API here which exists in each application context and communicates with a global system service that manages the interaction across all processes.
- A**text service**implements a particular interaction model allowing the client application to retrieve information of text. The system binds to the current text service that is in use, causing it to be created and run.
- Multiple**client applications**arbitrate with the text service manager for connections to text services.

### Text services sessions

- The**spell checker session** is one of the text services. [android.view.textservice.SpellCheckerSession](SpellCheckerSession.md)

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SpellCheckerInfo](SpellCheckerInfo.md)? | [getCurrentSpellCheckerInfo](TextServicesManager.md))`()` Retrieve the currently active spell checker, or null if there is none. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SpellCheckerInfo](SpellCheckerInfo.md)!\> | [getEnabledSpellCheckerInfos](TextServicesManager.md))`()` Retrieve the list of currently enabled spell checkers. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpellCheckerEnabled](TextServicesManager.md))`()` Return whether the spell checker is enabled or not. |
| --- | --- |
| [SpellCheckerSession](SpellCheckerSession.md)? | [newSpellCheckerSession](TextServicesManager.md))`(`bundle:` ` [Bundle](../android.os/Bundle.md)?`, `locale:` ` [Locale](../java.util/Locale.md)?`, `listener:` ` [SpellCheckerSession.SpellCheckerSessionListener](../android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener.md)`, `referToSpellCheckerLanguageSettings:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Get a spell checker session from the spell checker. |
| [SpellCheckerSession](SpellCheckerSession.md)? | [newSpellCheckerSession](TextServicesManager.md))`(`params:` ` [SpellCheckerSession.SpellCheckerSessionParams](../android/view/textservice/SpellCheckerSession.SpellCheckerSessionParams.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `listener:` ` [SpellCheckerSession.SpellCheckerSessionListener](../android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener.md)`)` Get a spell checker session from the spell checker. |

## Public methods

### getCurrentSpellCheckerInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrentSpellCheckerInfo(): SpellCheckerInfo?
```

Retrieve the currently active spell checker, or null if there is none.

| Return ||
|---------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [SpellCheckerInfo](SpellCheckerInfo.md)? | The current active spell checker info. |

### getEnabledSpellCheckerInfos

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEnabledSpellCheckerInfos(): MutableList<SpellCheckerInfo!>
```

Retrieve the list of currently enabled spell checkers.

Note: The results are filtered by the rules of [package visibility](../training/basics/intents/package-visibility.md), except for the currently active spell checker.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [SpellCheckerInfo](SpellCheckerInfo.md)!> | The list of currently enabled spell checkers. This value cannot be`null`. |

### isSpellCheckerEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSpellCheckerEnabled(): Boolean
```

Return whether the spell checker is enabled or not.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if spell checker is enabled,`false`otherwise. |

### newSpellCheckerSession

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun newSpellCheckerSession(
    bundle: Bundle?, 
    locale: Locale?, 
    listener: SpellCheckerSession.SpellCheckerSessionListener, 
    referToSpellCheckerLanguageSettings: Boolean
): SpellCheckerSession?
```

Get a spell checker session from the spell checker.

[SuggestionsInfo.RESULT_ATTR_IN_THE_DICTIONARY](SuggestionsInfo.md), [SuggestionsInfo.RESULT_ATTR_LOOKS_LIKE_TYPO](SuggestionsInfo.md), and [SuggestionsInfo.RESULT_ATTR_HAS_RECOMMENDED_SUGGESTIONS](SuggestionsInfo.md) will be passed to the spell checker as supported attributes.

| Parameters ||
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)?:the locale for the spell checker. If`locale`is null and referToSpellCheckerLanguageSettings is true, the locale specified in Settings will be returned. If`locale`is not null and referToSpellCheckerLanguageSettings is true, the locale specified in Settings will be returned only when it is same as`locale`. Exceptionally, when referToSpellCheckerLanguageSettings is true and`locale`is only language (e.g. "en"), the specified locale in Settings (e.g. "en_US") will be selected. |
| `listener` | [SpellCheckerSession.SpellCheckerSessionListener](../android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener.md):a spell checker session lister for getting results from the spell checker. This value cannot be`null`. |
| `referToSpellCheckerLanguageSettings` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, the session for one of enabled languages in settings will be returned. |
| --- | --- |
| `bundle` | [Bundle](../android.os/Bundle.md)?:This value may be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [SpellCheckerSession](SpellCheckerSession.md)? | a spell checker session of the spell checker This value may be`null`. |

### newSpellCheckerSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun newSpellCheckerSession(
    params: SpellCheckerSession.SpellCheckerSessionParams, 
    executor: Executor, 
    listener: SpellCheckerSession.SpellCheckerSessionListener
): SpellCheckerSession?
```

Get a spell checker session from the spell checker.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [SpellCheckerSession.SpellCheckerSessionParams](../android/view/textservice/SpellCheckerSession.SpellCheckerSessionParams.md):The parameters passed to the spell checker. This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The executor on which`listener`will be called back. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `listener` | [SpellCheckerSession.SpellCheckerSessionListener](../android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener.md):a spell checker session lister for getting results from the spell checker. This value cannot be`null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [SpellCheckerSession](SpellCheckerSession.md)? | The spell checker session of the spell checker. This value may be`null`. |
