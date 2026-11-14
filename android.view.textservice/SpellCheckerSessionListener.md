# SpellCheckerSession.SpellCheckerSessionListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SpellCheckerSessionListener

Kotlin| [Java](../android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener.md) 
| --- | --- |

```
interface SpellCheckerSessionListener
```

| [android.view.textservice.SpellCheckerSession.SpellCheckerSessionListener](../android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener.md) |

Callback for getting results from text services

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGetSentenceSuggestions](../android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener.md))`(`results:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [SentenceSuggestionsInfo](SentenceSuggestionsInfo.md)!>!`)` Callback for[SpellCheckerSession.getSentenceSuggestions(TextInfo[], int)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSentenceSuggestions(kotlin.Array,%20kotlin.Int)) |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGetSuggestions](../android/view/textservice/SpellCheckerSession.SpellCheckerSessionListener.md))`(`results:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [SuggestionsInfo](SuggestionsInfo.md)!>!`)` Callback for [SpellCheckerSession.getSuggestions(TextInfo, int)](SpellCheckerSession.md))and[SpellCheckerSession.getSuggestions(TextInfo[], int, boolean)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSuggestions(kotlin.Array,%20kotlin.Int,%20kotlin.Boolean)) |

## Public methods

### onGetSentenceSuggestions

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGetSentenceSuggestions(results: Array<SentenceSuggestionsInfo!>!): Unit
```

Callback for[SpellCheckerSession.getSentenceSuggestions(TextInfo[], int)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSentenceSuggestions(kotlin.Array,%20kotlin.Int))

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `results` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [SentenceSuggestionsInfo](SentenceSuggestionsInfo.md)!\>!:an array of [SentenceSuggestionsInfo](SentenceSuggestionsInfo.md) s. These results are suggestions for [TextInfo](TextInfo.md) s queried by[SpellCheckerSession.getSentenceSuggestions(TextInfo[], int)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSentenceSuggestions(kotlin.Array,%20kotlin.Int)). |

### onGetSuggestions

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGetSuggestions(results: Array<SuggestionsInfo!>!): Unit
```

Callback for [SpellCheckerSession.getSuggestions(TextInfo, int)](SpellCheckerSession.md))and[SpellCheckerSession.getSuggestions(TextInfo[], int, boolean)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSuggestions(kotlin.Array,%20kotlin.Int,%20kotlin.Boolean))

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `results` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [SuggestionsInfo](SuggestionsInfo.md)!\>!:an array of [SuggestionsInfo](SuggestionsInfo.md) s. These results are suggestions for [TextInfo](TextInfo.md) s queried by [SpellCheckerSession.getSuggestions(TextInfo, int)](SpellCheckerSession.md))or[SpellCheckerSession.getSuggestions(TextInfo[], int, boolean)](https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerSession#getSuggestions(kotlin.Array,%20kotlin.Int,%20kotlin.Boolean)) |
