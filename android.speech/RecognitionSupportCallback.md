# RecognitionSupportCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecognitionSupportCallback

Kotlin| [Java](https://developer.android.com/reference/android/speech/RecognitionSupportCallback "View this page in Java") 
| --- | --- |

```
interface RecognitionSupportCallback
```

| [android.speech.RecognitionSupportCallback](https://developer.android.com/reference/kotlin/android/speech/RecognitionSupportCallback#) |

Used for receiving notifications from the SpeechRecognizer about the device support status for the given recognition request.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](https://developer.android.com/reference/kotlin/android/speech/RecognitionSupportCallback#onError(kotlin.Int))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notifies the caller about an error during the recognition support request |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSupportResult](https://developer.android.com/reference/kotlin/android/speech/RecognitionSupportCallback#onSupportResult(android.speech.RecognitionSupport))`(`recognitionSupport:` ` [RecognitionSupport](https://developer.android.com/reference/kotlin/android/speech/RecognitionSupport)`)` Notifies the caller about the support for the given request. |

## Public methods

### onError

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onError(error: Int): Unit
```

Notifies the caller about an error during the recognition support request

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.speech.SpeechRecognizer#ERROR_NETWORK_TIMEOUT](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_NETWORK_TIMEOUT:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_NETWORK](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_NETWORK:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_AUDIO](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_AUDIO:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_SERVER](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_SERVER:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_CLIENT](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_CLIENT:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_SPEECH_TIMEOUT](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_SPEECH_TIMEOUT:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_NO_MATCH](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_NO_MATCH:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_RECOGNIZER_BUSY](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_RECOGNIZER_BUSY:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_INSUFFICIENT_PERMISSIONS](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_INSUFFICIENT_PERMISSIONS:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_TOO_MANY_REQUESTS](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_TOO_MANY_REQUESTS:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_SERVER_DISCONNECTED](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_SERVER_DISCONNECTED:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_LANGUAGE_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_LANGUAGE_NOT_SUPPORTED:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_LANGUAGE_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_LANGUAGE_UNAVAILABLE:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_CANNOT_CHECK_SUPPORT](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_CANNOT_CHECK_SUPPORT:kotlin.Int), or [android.speech.SpeechRecognizer#ERROR_CANNOT_LISTEN_TO_DOWNLOAD_EVENTS](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_CANNOT_LISTEN_TO_DOWNLOAD_EVENTS:kotlin.Int) |

### onSupportResult

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSupportResult(recognitionSupport: RecognitionSupport): Unit
```

Notifies the caller about the support for the given request.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `recognitionSupport` | [RecognitionSupport](https://developer.android.com/reference/kotlin/android/speech/RecognitionSupport):This value cannot be`null`. |
