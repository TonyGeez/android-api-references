Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecognitionListener

Kotlin | [Java](https://developer.android.com/reference/android/speech/RecognitionListener "View this page in Java")

```
interface RecognitionListener
```

| [android.speech.RecognitionListener](https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#) |

Used for receiving notifications from the SpeechRecognizer when the recognition related events occur. All the callbacks are executed on the Application main thread.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onBeginningOfSpeech()()` The user has started to speak. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onBufferReceived(kotlin.ByteArray)(buffer: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` More sound has been received. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onEndOfSegmentedSession()()` Called at the end of a segmented recognition request. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onEndOfSpeech()()` Called after the user stops speaking. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onError(kotlin.Int)(error: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` A network or recognition error occurred. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onEvent(kotlin.Int,%20android.os.Bundle)(eventType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, params: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Reserved for adding future events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onLanguageDetection(android.os.Bundle)(results: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Called when the language detection (and switching) results are available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onPartialResults(android.os.Bundle)(partialResults: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Called when partial recognition results are available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onReadyForSpeech(android.os.Bundle)(params: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Called when the endpointer is ready for the user to start speaking. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onResults(android.os.Bundle)(results: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Called when recognition results are ready. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onRmsChanged(kotlin.Float)(rmsdB: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` The sound level in the audio stream has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onSegmentResults(android.os.Bundle)(segmentResults: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Called for each ready segment of a recognition request. |

## Public methods

### onBeginningOfSpeech

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onBeginningOfSpeech(): Unit
```

The user has started to speak.

### onBufferReceived

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onBufferReceived(buffer: ByteArray!): Unit
```

More sound has been received. The purpose of this function is to allow giving feedback to the user regarding the captured audio. There is no guarantee that this method will be called.

| Parameters ||
|---|---|
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: a buffer containing a sequence of big-endian 16-bit integers representing a single channel audio stream. The sample rate is implementation dependent. |

### onEndOfSegmentedSession

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onEndOfSegmentedSession(): Unit
```

Called at the end of a segmented recognition request. To request segmented speech results use `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_SEGMENTED_SESSION:kotlin.String`.

### onEndOfSpeech

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onEndOfSpeech(): Unit
```

Called after the user stops speaking.

### onError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onError(error: Int): Unit
```

A network or recognition error occurred.

| Parameters ||
|---|---|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): code is defined in `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer`. Implementations need to handle any integer error constant to be passed here beyond constants prefixed with ERROR_. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_NETWORK_TIMEOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_NETWORK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_AUDIO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_SERVER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_CLIENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_SPEECH_TIMEOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_NO_MATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_RECOGNIZER_BUSY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_INSUFFICIENT_PERMISSIONS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_TOO_MANY_REQUESTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_SERVER_DISCONNECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_LANGUAGE_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_LANGUAGE_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_CANNOT_CHECK_SUPPORT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_CANNOT_LISTEN_TO_DOWNLOAD_EVENTS:kotlin.Int` |

### onEvent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onEvent(
    eventType: Int, 
    params: Bundle!
): Unit
```

Reserved for adding future events.

| Parameters ||
|---|---|
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the type of the occurred event |
| `params` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: a Bundle containing the passed parameters |

### onLanguageDetection

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onLanguageDetection(results: Bundle): Unit
```

Called when the language detection (and switching) results are available. This callback can be invoked on any number of occasions at any time between `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onBeginningOfSpeech()` and `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onEndOfSpeech()`, depending on the speech recognition service implementation.

To request language detection, use `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_ENABLE_LANGUAGE_DETECTION:kotlin.String`.

To request automatic language switching, use `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_ENABLE_LANGUAGE_SWITCH:kotlin.String`.

| Parameters ||
|---|---|
| `results` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): the returned language detection (and switching) results. To retrieve the most confidently detected language IETF tag (as defined by BCP 47, e.g., "en-US", "de-DE"), use `https://developer.android.com/reference/kotlin/android/os/BaseBundle.html#getString(kotlin.String)` with `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#DETECTED_LANGUAGE:kotlin.String` as the parameter. To retrieve the language detection confidence level represented by a value prefixed by `LANGUAGE_DETECTION_CONFIDENCE_LEVEL_` and defined in `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer`, use `https://developer.android.com/reference/kotlin/android/os/BaseBundle.html#getInt(kotlin.String)` with `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#LANGUAGE_DETECTION_CONFIDENCE_LEVEL:kotlin.String` as the parameter. To retrieve the alternative locales for the same language retrieved by the key `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#DETECTED_LANGUAGE:kotlin.String`, use `https://developer.android.com/reference/kotlin/android/os/Bundle.html#getStringArrayList(kotlin.String)` with `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#TOP_LOCALE_ALTERNATIVES:kotlin.String` as the parameter. To retrieve the language switching results represented by a value prefixed by `LANGUAGE_SWITCH_RESULT_` and defined in `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer`, use `https://developer.android.com/reference/kotlin/android/os/BaseBundle.html#getInt(kotlin.String)` with `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#LANGUAGE_SWITCH_RESULT:kotlin.String` as the parameter. This value cannot be `null`. |

### onPartialResults

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onPartialResults(partialResults: Bundle!): Unit
```

Called when partial recognition results are available. The callback might be called at any time between `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onBeginningOfSpeech()` and `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onResults(android.os.Bundle)` when partial results are ready. This method may be called zero, one or multiple times for each call to `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#startListening(android.content.Intent)`, depending on the speech recognition service implementation. To request partial results, use `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_PARTIAL_RESULTS:kotlin.String`

| Parameters ||
|---|---|
| `partialResults` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: the returned results. To retrieve the results in ArrayList\<String\> format use `https://developer.android.com/reference/kotlin/android/os/Bundle.html#getStringArrayList(kotlin.String)` with `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#RESULTS_RECOGNITION:kotlin.String` as a parameter |

### onReadyForSpeech

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onReadyForSpeech(params: Bundle!): Unit
```

Called when the endpointer is ready for the user to start speaking.

| Parameters ||
|---|---|
| `params` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: parameters set by the recognition service. Reserved for future use. |

### onResults

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onResults(results: Bundle!): Unit
```

Called when recognition results are ready.

Called with the results for the full speech since `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onReadyForSpeech(android.os.Bundle)`. To get recognition results in segments rather than for the full session see `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_SEGMENTED_SESSION:kotlin.String`.

| Parameters ||
|---|---|
| `results` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: the recognition results. To retrieve the results in `ArrayList<String>` format use `https://developer.android.com/reference/kotlin/android/os/Bundle.html#getStringArrayList(kotlin.String)` with `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#RESULTS_RECOGNITION:kotlin.String` as a parameter. A float array of confidence values might also be given in `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#CONFIDENCE_SCORES:kotlin.String`. |

### onRmsChanged

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onRmsChanged(rmsdB: Float): Unit
```

The sound level in the audio stream has changed. There is no guarantee that this method will be called.

| Parameters ||
|---|---|
| `rmsdB` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the new RMS dB value |

### onSegmentResults

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSegmentResults(segmentResults: Bundle): Unit
```

Called for each ready segment of a recognition request. To request segmented speech results use `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_SEGMENTED_SESSION:kotlin.String`. The callback might be called any number of times between `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onReadyForSpeech(android.os.Bundle)` and `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onEndOfSegmentedSession()`.

| Parameters ||
|---|---|
| `segmentResults` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): the returned results. To retrieve the results in ArrayList\<String\> format use `https://developer.android.com/reference/kotlin/android/os/Bundle.html#getStringArrayList(kotlin.String)` with `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#RESULTS_RECOGNITION:kotlin.String` as a parameter. This value cannot be `null`. |
