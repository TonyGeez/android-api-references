# TextToSpeech.OnInitListener

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnInitListener

Kotlin| [Java](https://developer.android.com/reference/android/speech/tts/TextToSpeech.OnInitListener "View this page in Java") 
| --- | --- |

```
interface OnInitListener
```

| [android.speech.tts.TextToSpeech.OnInitListener](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech.OnInitListener#) |

Interface definition of a callback to be invoked indicating the completion of the TextToSpeech engine initialization.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInit](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech.OnInitListener#onInit(kotlin.Int))`(`status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to signal the completion of the TextToSpeech engine initialization. |

## Public methods

### onInit

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onInit(status: Int): Unit
```

Called to signal the completion of the TextToSpeech engine initialization.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): [TextToSpeech.SUCCESS](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#SUCCESS:kotlin.Int) or [TextToSpeech.ERROR](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#ERROR:kotlin.Int). |
