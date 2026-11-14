# SpellCheckerSession

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SpellCheckerSession

Kotlin| [Java](SpellCheckerSession.md) 
| --- | --- |

```
open class SpellCheckerSession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textservice.SpellCheckerSession](SpellCheckerSession.md) |

The SpellCheckerSession interface provides the per client functionality of SpellCheckerService.

### Applications

<br />

In most cases, applications that are using the standard [android.widget.TextView](../android.widget/TextView.md) or its subclasses will have little they need to do to work well with spell checker services. The main things you need to be aware of are:

- Properly set the [android.R.attr#inputType](../android/R.attr.md) in your editable text views, so that the spell checker will have enough context to help the user in editing text in them.

For the rare people amongst us writing client applications that use the spell checker service directly, you will need to use [getSuggestions(android.view.textservice.TextInfo,int)](SpellCheckerSession.md))or[getSuggestions(android.view.textservice.TextInfo[],int,boolean)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSuggestions(kotlin.Array,%20kotlin.Int,%20kotlin.Boolean))for obtaining results from the spell checker service by yourself.

### Security

There are a lot of security issues associated with spell checkers, since they could monitor all the text being sent to them through, for instance, [android.widget.TextView](../android.widget/TextView.md). The Android spell checker framework also allows arbitrary third party spell checkers, so care must be taken to restrict their selection and interactions.

Here are some key points about the security architecture behind the spell checker framework:

- Only the system is allowed to directly access a spell checker framework's [android.service.textservice.SpellCheckerService](../android.service.textservice/SpellCheckerService.md) interface, via the [android.Manifest.permission#BIND_TEXT_SERVICE](../android/Manifest.permission.md) permission. This is enforced in the system by not binding to a spell checker service that does not require this permission.
- The user must explicitly enable a new spell checker in settings before they can be enabled, to confirm with the system that they know about it and want to make it available for use.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [SpellCheckerSessionListener](../android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener.md) Callback for getting results from text services |
| open | [SpellCheckerSessionParams](../android/view/textservice/SpellCheckerSession.SpellCheckerSessionParams.md) Parameters used to create a [SpellCheckerSession](SpellCheckerSession.md). |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SERVICE_META_DATA](SpellCheckerSession.md) Name under which a SpellChecker service component publishes information about itself. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](SpellCheckerSession.md))`()` Cancel pending and running spell check tasks |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](SpellCheckerSession.md))`()` Finish this session and allow TextServicesManagerService to disconnect the bound spell checker. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getSentenceSuggestions](SpellCheckerSession.md))`(`textInfos:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TextInfo](TextInfo.md)!>!`, `suggestionsLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get suggestions from the specified sentences |
| --- | --- |
| open [SpellCheckerInfo](SpellCheckerInfo.md)! | [getSpellChecker](SpellCheckerSession.md))`()` Get the spell checker service info this spell checker session has. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getSuggestions](SpellCheckerSession.md))`(`textInfo:` ` [TextInfo](TextInfo.md)!`, `suggestionsLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get candidate strings for a substring of the specified text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getSuggestions](SpellCheckerSession.md))`(`textInfos:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TextInfo](TextInfo.md)!>!`, `suggestionsLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sequentialWords:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` A batch process of getSuggestions |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSessionDisconnected](SpellCheckerSession.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](SpellCheckerSession.md))`()` <br /> |

## Constants

### SERVICE_META_DATA

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_META_DATA: String
```

Name under which a SpellChecker service component publishes information about itself. This meta-data must reference an XML resource. 

 Value: "android.view.textservice.scs"

## Public methods

### cancel

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(): Unit
```

Cancel pending and running spell check tasks 

### close

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Finish this session and allow TextServicesManagerService to disconnect the bound spell checker. 

### getSentenceSuggestions

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSentenceSuggestions(
    textInfos: Array<TextInfo!>!, 
    suggestionsLimit: Int
): Unit
```

Get suggestions from the specified sentences

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `textInfos` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TextInfo](TextInfo.md)!\>!:an array of text metadata for a spell checker |
| `suggestionsLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of suggestions that will be returned |

### getSpellChecker

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpellChecker(): SpellCheckerInfo!
```

Get the spell checker service info this spell checker session has.

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [SpellCheckerInfo](SpellCheckerInfo.md)! | SpellCheckerInfo for the specified locale. |

### getSuggestions

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSuggestions(
    textInfo: TextInfo!, 
    suggestionsLimit: Int
): Unit
```

**Deprecated:** *use[SpellCheckerSession.getSentenceSuggestions(TextInfo[], int)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSentenceSuggestions(kotlin.Array,%20kotlin.Int))instead*

Get candidate strings for a substring of the specified text.

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `textInfo` | [TextInfo](TextInfo.md)!:text metadata for a spell checker |
| `suggestionsLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of suggestions that will be returned |

### getSuggestions

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSuggestions(
    textInfos: Array<TextInfo!>!, 
    suggestionsLimit: Int, 
    sequentialWords: Boolean
): Unit
```

**Deprecated:** *use[SpellCheckerSession.getSentenceSuggestions(TextInfo[], int)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSentenceSuggestions(kotlin.Array,%20kotlin.Int))instead*

A batch process of getSuggestions

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `textInfos` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TextInfo](TextInfo.md)!\>!:an array of text metadata for a spell checker |
| `suggestionsLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of suggestions that will be returned |
| `sequentialWords` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if textInfos can be treated as sequential words. |
| --- | --- |

### isSessionDisconnected

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSessionDisconnected(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the connection to a text service of this session is disconnected and not alive. |

## Protected methods

### finalize

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
