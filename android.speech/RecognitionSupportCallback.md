# RecognitionSupportCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecognitionSupportCallback

Kotlin| [Java](../android/speech/RecognitionSupportCallback.md) 
| --- | --- |

```
interface RecognitionSupportCallback
```

| [android.speech.RecognitionSupportCallback](../android/speech/RecognitionSupportCallback.md) |

Used for receiving notifications from the SpeechRecognizer about the device support status for the given recognition request.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](../android/speech/RecognitionSupportCallback.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notifies the caller about an error during the recognition support request |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSupportResult](../android/speech/RecognitionSupportCallback.md))`(`recognitionSupport:` ` [RecognitionSupport](../android/speech/RecognitionSupport.md)`)` Notifies the caller about the support for the given request. |

## Public methods

### onError

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onError(error: Int): Unit
```

Notifies the caller about an error during the recognition support request

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.speech.SpeechRecognizer#ERROR_NETWORK_TIMEOUT](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_NETWORK](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_AUDIO](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_SERVER](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_CLIENT](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_SPEECH_TIMEOUT](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_NO_MATCH](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_RECOGNIZER_BUSY](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_INSUFFICIENT_PERMISSIONS](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_TOO_MANY_REQUESTS](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_SERVER_DISCONNECTED](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_LANGUAGE_NOT_SUPPORTED](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_LANGUAGE_UNAVAILABLE](../android/speech/SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_CANNOT_CHECK_SUPPORT](../android/speech/SpeechRecognizer.md), or [android.speech.SpeechRecognizer#ERROR_CANNOT_LISTEN_TO_DOWNLOAD_EVENTS](../android/speech/SpeechRecognizer.md) |

### onSupportResult

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSupportResult(recognitionSupport: RecognitionSupport): Unit
```

Notifies the caller about the support for the given request.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `recognitionSupport` | [RecognitionSupport](../android/speech/RecognitionSupport.md):This value cannot be`null`. |
