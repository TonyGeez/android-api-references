# TextToSpeech.OnUtteranceCompletedListener

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnUtteranceCompletedListener

Kotlin| [Java](../android/speech/tts/TextToSpeech.OnUtteranceCompletedListener.md) 
| --- | --- |

```
interface OnUtteranceCompletedListener
```

| [android.speech.tts.TextToSpeech.OnUtteranceCompletedListener](../android/speech/tts/TextToSpeech.OnUtteranceCompletedListener.md) |

| **This interface was deprecated in API level 18.**
|
| Use [UtteranceProgressListener](UtteranceProgressListener.md) instead.

Listener that will be called when the TTS service has completed synthesizing an utterance. This is only called if the utterance has an utterance ID (see [TextToSpeech.Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUtteranceCompleted](../android/speech/tts/TextToSpeech.OnUtteranceCompletedListener.md))`(`utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called when an utterance has been synthesized. |

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
