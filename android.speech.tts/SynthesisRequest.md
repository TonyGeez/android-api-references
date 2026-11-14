# SynthesisRequest

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SynthesisRequest

Kotlin| [Java](SynthesisRequest.md) 
| --- | --- |

```
class SynthesisRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.speech.tts.SynthesisRequest](SynthesisRequest.md) |

Contains data required by engines to synthesize speech. This data is:

- The text to synthesize
- The synthesis locale, represented as a language, country and a variant. The language is an ISO 639-3 letter language code, and the country is an ISO 3166 alpha 3 code. The variant is not specified.
- The name of the voice requested for this synthesis. May be empty if the client uses [TextToSpeech.setLanguage](TextToSpeech.md))instead of [TextToSpeech.setVoice](TextToSpeech.md))
- The synthesis speech rate, with 100 being the normal, and higher values representing higher speech rates.
- The voice pitch, with 100 being the default pitch.

Any additional parameters sent to the text to speech service are passed in uninterpreted, see the`params`argument in android.speech.tts.TextToSpeech#speak and android.speech.tts.TextToSpeech#synthesizeToFile.

<br />

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SynthesisRequest](SynthesisRequest.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `params:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> |
| [SynthesisRequest](SynthesisRequest.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCallerUid](SynthesisRequest.md))`()` Gets the request caller Uid. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getCharSequenceText](SynthesisRequest.md))`()` Gets the text which should be synthesized. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCountry](SynthesisRequest.md))`()` Gets the ISO 3-letter country code for the language to use. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLanguage](SynthesisRequest.md))`()` Gets the ISO 3-letter language code for the language to use. |
| [Bundle](../android.os/Bundle.md)! | [getParams](SynthesisRequest.md))`()` Gets the additional params, if any. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPitch](SynthesisRequest.md))`()` Gets the pitch to use. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpeechRate](SynthesisRequest.md))`()` Gets the speech rate to use. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getText](SynthesisRequest.md))`()` Gets the text which should be synthesized. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getVariant](SynthesisRequest.md))`()` Gets the language variant to use. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getVoiceName](SynthesisRequest.md))`()` Gets the name of the voice to use. |

## Public constructors

### SynthesisRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SynthesisRequest(
    text: CharSequence!, 
    params: Bundle!)
```  

### SynthesisRequest

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SynthesisRequest(
    text: String!, 
    params: Bundle!)
```

## Public methods

### getCallerUid

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallerUid(): Int
```

Gets the request caller Uid. 

### getCharSequenceText

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCharSequenceText(): CharSequence!
```

Gets the text which should be synthesized. 

### getCountry

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCountry(): String!
```

Gets the ISO 3-letter country code for the language to use. 

### getLanguage

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLanguage(): String!
```

Gets the ISO 3-letter language code for the language to use. 

### getParams

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParams(): Bundle!
```

Gets the additional params, if any. 

### getPitch

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPitch(): Int
```

Gets the pitch to use. The normal pitch is 100. 

### getSpeechRate

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSpeechRate(): Int
```

Gets the speech rate to use. The normal rate is 100. 

### getText

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getText(): String!
```

**Deprecated:** *As of API level 21, replaced by [getCharSequenceText](SynthesisRequest.md)).*

Gets the text which should be synthesized. 

### getVariant

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVariant(): String!
```

Gets the language variant to use. 

### getVoiceName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVoiceName(): String!
```

Gets the name of the voice to use.
