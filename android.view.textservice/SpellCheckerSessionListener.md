# SpellCheckerSession.SpellCheckerSessionListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SpellCheckerSessionListener

Kotlin| [Java](https://developer.android.com/reference/android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener "View this page in Java") 
| --- | --- |

```
interface SpellCheckerSessionListener
```

| [android.view.textservice.SpellCheckerSession.SpellCheckerSessionListener](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener#) |

Callback for getting results from text services

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGetSentenceSuggestions](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener#onGetSentenceSuggestions(kotlin.Array))`(`results:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [SentenceSuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo)!>!`)` Callback for[SpellCheckerSession.getSentenceSuggestions(TextInfo[], int)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSentenceSuggestions(kotlin.Array,%20kotlin.Int)) |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGetSuggestions](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener#onGetSuggestions(kotlin.Array))`(`results:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo)!>!`)` Callback for [SpellCheckerSession.getSuggestions(TextInfo, int)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSuggestions(android.view.textservice.TextInfo,%20kotlin.Int))and[SpellCheckerSession.getSuggestions(TextInfo[], int, boolean)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSuggestions(kotlin.Array,%20kotlin.Int,%20kotlin.Boolean)) |

## Public methods

### onGetSentenceSuggestions

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGetSentenceSuggestions(results: Array<SentenceSuggestionsInfo!>!): Unit
```

Callback for[SpellCheckerSession.getSentenceSuggestions(TextInfo[], int)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSentenceSuggestions(kotlin.Array,%20kotlin.Int))

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `results` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [SentenceSuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo)!\>!:an array of [SentenceSuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo) s. These results are suggestions for [TextInfo](https://developer.android.com/reference/kotlin/android/view/textservice/TextInfo) s queried by[SpellCheckerSession.getSentenceSuggestions(TextInfo[], int)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSentenceSuggestions(kotlin.Array,%20kotlin.Int)). |

### onGetSuggestions

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGetSuggestions(results: Array<SuggestionsInfo!>!): Unit
```

Callback for [SpellCheckerSession.getSuggestions(TextInfo, int)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSuggestions(android.view.textservice.TextInfo,%20kotlin.Int))and[SpellCheckerSession.getSuggestions(TextInfo[], int, boolean)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSuggestions(kotlin.Array,%20kotlin.Int,%20kotlin.Boolean))

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `results` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo)!\>!:an array of [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo) s. These results are suggestions for [TextInfo](https://developer.android.com/reference/kotlin/android/view/textservice/TextInfo) s queried by [SpellCheckerSession.getSuggestions(TextInfo, int)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSuggestions(android.view.textservice.TextInfo,%20kotlin.Int))or[SpellCheckerSession.getSuggestions(TextInfo[], int, boolean)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSuggestions(kotlin.Array,%20kotlin.Int,%20kotlin.Boolean)) |
