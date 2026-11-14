# SynthesisRequest

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SynthesisRequest

Kotlin| [Java](https://developer.android.com/reference/android/speech/tts/SynthesisRequest "View this page in Java") 

```
class SynthesisRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.speech.tts.SynthesisRequest](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#) |

Contains data required by engines to synthesize speech. This data is:

- The text to synthesize
- The synthesis locale, represented as a language, country and a variant. The language is an ISO 639-3 letter language code, and the country is an ISO 3166 alpha 3 code. The variant is not specified.
- The name of the voice requested for this synthesis. May be empty if the client uses [TextToSpeech.setLanguage](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#setLanguage(java.util.Locale))instead of [TextToSpeech.setVoice](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#setVoice(android.speech.tts.Voice))
- The synthesis speech rate, with 100 being the normal, and higher values representing higher speech rates.
- The voice pitch, with 100 being the default pitch.

Any additional parameters sent to the text to speech service are passed in uninterpreted, see the`params`argument in android.speech.tts.TextToSpeech#speak and android.speech.tts.TextToSpeech#synthesizeToFile.

<br />

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SynthesisRequest](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#SynthesisRequest(kotlin.CharSequence,%20android.os.Bundle))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `params:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> |
| [SynthesisRequest](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#SynthesisRequest(kotlin.String,%20android.os.Bundle))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCallerUid](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#getCallerUid())`()` Gets the request caller Uid. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getCharSequenceText](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#getCharSequenceText())`()` Gets the text which should be synthesized. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCountry](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#getCountry())`()` Gets the ISO 3-letter country code for the language to use. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLanguage](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#getLanguage())`()` Gets the ISO 3-letter language code for the language to use. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getParams](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#getParams())`()` Gets the additional params, if any. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPitch](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#getPitch())`()` Gets the pitch to use. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpeechRate](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#getSpeechRate())`()` Gets the speech rate to use. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getText](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#getText())`()` Gets the text which should be synthesized. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getVariant](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#getVariant())`()` Gets the language variant to use. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getVoiceName](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#getVoiceName())`()` Gets the name of the voice to use. |

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

**Deprecated:** *As of API level 21, replaced by [getCharSequenceText](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisRequest#getCharSequenceText()).*

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
