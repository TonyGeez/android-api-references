# ModelDownloadListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ModelDownloadListener

Kotlin| [Java](ModelDownloadListener.md) 
| --- | --- |

```
interface ModelDownloadListener
```

| [android.speech.ModelDownloadListener](ModelDownloadListener.md) |

Listener for model download events. It makes [RecognitionService](RecognitionService.md) let callers know about the progress of model download for a single recognition request.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](ModelDownloadListener.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` A network or scheduling error occurred. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProgress](ModelDownloadListener.md))`(`completedPercent:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called by [RecognitionService](RecognitionService.md) only if the download has started after the request. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScheduled](ModelDownloadListener.md))`()` Called when [RecognitionService](RecognitionService.md) scheduled the download, but won't satisfy it immediately. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](ModelDownloadListener.md))`()` This method is called: - if the model is already available; - if the [RecognitionService](RecognitionService.md) has started and completed the download. Once this method is called, the model can be safely used to satisfy recognition requests. |

## Public methods

### onError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onError(error: Int): Unit
```

A network or scheduling error occurred.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code is defined in [SpeechRecognizer](SpeechRecognizer.md) Value is [android.speech.SpeechRecognizer#ERROR_NETWORK_TIMEOUT](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_NETWORK](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_AUDIO](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_SERVER](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_CLIENT](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_SPEECH_TIMEOUT](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_NO_MATCH](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_RECOGNIZER_BUSY](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_INSUFFICIENT_PERMISSIONS](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_TOO_MANY_REQUESTS](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_SERVER_DISCONNECTED](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_LANGUAGE_NOT_SUPPORTED](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_LANGUAGE_UNAVAILABLE](SpeechRecognizer.md), [android.speech.SpeechRecognizer#ERROR_CANNOT_CHECK_SUPPORT](SpeechRecognizer.md), or [android.speech.SpeechRecognizer#ERROR_CANNOT_LISTEN_TO_DOWNLOAD_EVENTS](SpeechRecognizer.md) |

### onProgress

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onProgress(completedPercent: Int): Unit
```

Called by [RecognitionService](RecognitionService.md) only if the download has started after the request.

The number of calls to this method varies depending of the [RecognitionService](RecognitionService.md) implementation. If the download finished quickly enough, [onSuccess()](ModelDownloadListener.md))may be called directly. In other cases, this method may be called any number of times during the download.

| Parameters ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| `completedPercent` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the percentage of download that is completed |

### onScheduled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScheduled(): Unit
```

Called when [RecognitionService](RecognitionService.md) scheduled the download, but won't satisfy it immediately. There will be no further updates on this listener. 

### onSuccess

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuccess(): Unit
```

This method is called:
- if the model is already available;
- if the [RecognitionService](RecognitionService.md) has started and completed the download.

 Once this method is called, the model can be safely used to satisfy recognition requests.
