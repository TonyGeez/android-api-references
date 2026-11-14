# TextToSpeech.OnUtteranceCompletedListener

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnUtteranceCompletedListener

Kotlin| [Java](https://developer.android.com/reference/android/speech/tts/TextToSpeech.OnUtteranceCompletedListener "View this page in Java") 

```
interface OnUtteranceCompletedListener
```

| [android.speech.tts.TextToSpeech.OnUtteranceCompletedListener](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech.OnUtteranceCompletedListener#) |

| **This interface was deprecated in API level 18.**
|
| Use [UtteranceProgressListener](https://developer.android.com/reference/kotlin/android/speech/tts/UtteranceProgressListener) instead.

Listener that will be called when the TTS service has completed synthesizing an utterance. This is only called if the utterance has an utterance ID (see [TextToSpeech.Engine.KEY_PARAM_UTTERANCE_ID](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech.Engine#KEY_PARAM_UTTERANCE_ID:kotlin.String)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUtteranceCompleted](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech.OnUtteranceCompletedListener#onUtteranceCompleted(kotlin.String))`(`utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called when an utterance has been synthesized. |

## Public methods

### onUtteranceCompleted

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUtteranceCompleted(utteranceId: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when an utterance has been synthesized.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------|
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the identifier of the utterance. |
