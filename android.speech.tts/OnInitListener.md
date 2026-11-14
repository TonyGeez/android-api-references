# TextToSpeech.OnInitListener

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnInitListener

Kotlin| [Java](../android/speech/tts/TextToSpeech.OnInitListener.md) 
| --- | --- |

```
interface OnInitListener
```

| [android.speech.tts.TextToSpeech.OnInitListener](../android/speech/tts/TextToSpeech.OnInitListener.md) |

Interface definition of a callback to be invoked indicating the completion of the TextToSpeech engine initialization.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInit](../android/speech/tts/TextToSpeech.OnInitListener.md))`(`status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to signal the completion of the TextToSpeech engine initialization. |

## Public methods

### onInit

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onInit(status: Int): Unit
```

Called to signal the completion of the TextToSpeech engine initialization.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): [TextToSpeech.SUCCESS](TextToSpeech.md) or [TextToSpeech.ERROR](TextToSpeech.md). |
