# ModelDownloadListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ModelDownloadListener

Kotlin| [Java](https://developer.android.com/reference/android/speech/ModelDownloadListener "View this page in Java") 

```
interface ModelDownloadListener
```

| [android.speech.ModelDownloadListener](https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener#) |

Listener for model download events. It makes [RecognitionService](https://developer.android.com/reference/kotlin/android/speech/RecognitionService) let callers know about the progress of model download for a single recognition request.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener#onError(kotlin.Int))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` A network or scheduling error occurred. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProgress](https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener#onProgress(kotlin.Int))`(`completedPercent:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called by [RecognitionService](https://developer.android.com/reference/kotlin/android/speech/RecognitionService) only if the download has started after the request. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScheduled](https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener#onScheduled())`()` Called when [RecognitionService](https://developer.android.com/reference/kotlin/android/speech/RecognitionService) scheduled the download, but won't satisfy it immediately. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener#onSuccess())`()` This method is called: - if the model is already available; - if the [RecognitionService](https://developer.android.com/reference/kotlin/android/speech/RecognitionService) has started and completed the download. Once this method is called, the model can be safely used to satisfy recognition requests. |

## Public methods

### onError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onError(error: Int): Unit
```

A network or scheduling error occurred.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code is defined in [SpeechRecognizer](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer) Value is [android.speech.SpeechRecognizer#ERROR_NETWORK_TIMEOUT](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_NETWORK_TIMEOUT:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_NETWORK](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_NETWORK:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_AUDIO](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_AUDIO:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_SERVER](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_SERVER:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_CLIENT](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_CLIENT:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_SPEECH_TIMEOUT](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_SPEECH_TIMEOUT:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_NO_MATCH](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_NO_MATCH:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_RECOGNIZER_BUSY](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_RECOGNIZER_BUSY:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_INSUFFICIENT_PERMISSIONS](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_INSUFFICIENT_PERMISSIONS:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_TOO_MANY_REQUESTS](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_TOO_MANY_REQUESTS:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_SERVER_DISCONNECTED](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_SERVER_DISCONNECTED:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_LANGUAGE_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_LANGUAGE_NOT_SUPPORTED:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_LANGUAGE_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_LANGUAGE_UNAVAILABLE:kotlin.Int), [android.speech.SpeechRecognizer#ERROR_CANNOT_CHECK_SUPPORT](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_CANNOT_CHECK_SUPPORT:kotlin.Int), or [android.speech.SpeechRecognizer#ERROR_CANNOT_LISTEN_TO_DOWNLOAD_EVENTS](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_CANNOT_LISTEN_TO_DOWNLOAD_EVENTS:kotlin.Int) |

### onProgress

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onProgress(completedPercent: Int): Unit
```

Called by [RecognitionService](https://developer.android.com/reference/kotlin/android/speech/RecognitionService) only if the download has started after the request.

The number of calls to this method varies depending of the [RecognitionService](https://developer.android.com/reference/kotlin/android/speech/RecognitionService) implementation. If the download finished quickly enough, [onSuccess()](https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener#onSuccess())may be called directly. In other cases, this method may be called any number of times during the download.

| Parameters ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| `completedPercent` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the percentage of download that is completed |

### onScheduled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScheduled(): Unit
```

Called when [RecognitionService](https://developer.android.com/reference/kotlin/android/speech/RecognitionService) scheduled the download, but won't satisfy it immediately. There will be no further updates on this listener. 

### onSuccess

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuccess(): Unit
```

This method is called:
- if the model is already available;
- if the [RecognitionService](https://developer.android.com/reference/kotlin/android/speech/RecognitionService) has started and completed the download.

 Once this method is called, the model can be safely used to satisfy recognition requests.
