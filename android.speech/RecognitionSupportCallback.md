# RecognitionSupportCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecognitionSupportCallback

Kotlin| [Java](RecognitionSupportCallback.md) 
| --- | --- |

```
interface RecognitionSupportCallback
```

| [android.speech.RecognitionSupportCallback](RecognitionSupportCallback.md) |

Used for receiving notifications from the SpeechRecognizer about the device support status for the given recognition request.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](RecognitionSupportCallback.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notifies the caller about an error during the recognition support request |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSupportResult](RecognitionSupportCallback.md))`(`recognitionSupport:` ` [RecognitionSupport](RecognitionSupport.md)`)` Notifies the caller about the support for the given request. |

## Public methods

### onError

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onError(error: Int): Unit
```

Notifies the caller about an error during the recognition support request

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.speech.SpeechRecognizer#ERROR_NETWORK_TIMEOUT](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_NETWORK](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_AUDIO](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_SERVER](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_CLIENT](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_SPEECH_TIMEOUT](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_NO_MATCH](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_RECOGNIZER_BUSY](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_INSUFFICIENT_PERMISSIONS](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_TOO_MANY_REQUESTS](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_SERVER_DISCONNECTED](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_LANGUAGE_NOT_SUPPORTED](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_LANGUAGE_UNAVAILABLE](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_CANNOT_CHECK_SUPPORT](SpeechRecognizer.md), or [android.speech.SpeechRecognizer#ERROR_CANNOT_LISTEN_TO_DOWNLOAD_EVENTS](SpeechRecognizer.md) |

### onSupportResult

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSupportResult(recognitionSupport: RecognitionSupport): Unit
```

Notifies the caller about the support for the given request.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `recognitionSupport` | [RecognitionSupport](RecognitionSupport.md):This value cannot be`null`. |
