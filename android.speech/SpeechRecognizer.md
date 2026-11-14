Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SpeechRecognizer

```
open class SpeechRecognizer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.speech.SpeechRecognizer](../android/speech/SpeechRecognizer.md) |

This class provides access to the speech recognition service. This service allows access to the speech recognizer. Do not instantiate this class directly, instead, call `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#createSpeechRecognizer(android.content.Context)`. This class's methods must be invoked only from the main application thread.

**Important:** the caller MUST invoke `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#destroy()` on a SpeechRecognizer object when it is no longer needed.

The implementation of this API is likely to stream audio to remote servers to perform speech recognition. As such this API is not intended to be used for continuous recognition, which would consume a significant amount of battery and bandwidth.

Please note that the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RECORD_AUDIO:kotlin.String` permission to use this class.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#CONFIDENCE_SCORES:kotlin.String` Key used to retrieve a float array from the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to the `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onResults(android.os.Bundle)` and `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onPartialResults(android.os.Bundle)` methods. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#DETECTED_LANGUAGE:kotlin.String` Key used to retrieve a `https://developer.android.com/reference/kotlin/java/lang/String.html#` representation of the IETF language tag (as defined by BCP 47, e.g., "en-US", "de-DE") of the detected language of the most recent audio chunk. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_AUDIO:kotlin.Int` Audio recording error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_CANNOT_CHECK_SUPPORT:kotlin.Int` The service does not allow to check for support. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_CANNOT_LISTEN_TO_DOWNLOAD_EVENTS:kotlin.Int` The service does not support listening to model downloads events. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_CLIENT:kotlin.Int` Other client side errors. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_INSUFFICIENT_PERMISSIONS:kotlin.Int` Insufficient permissions |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_LANGUAGE_NOT_SUPPORTED:kotlin.Int` Requested language is not available to be used with the current recognizer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_LANGUAGE_UNAVAILABLE:kotlin.Int` Requested language is supported, but not available currently (e.g. not downloaded yet). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_NETWORK:kotlin.Int` Other network related errors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_NETWORK_TIMEOUT:kotlin.Int` Network operation timed out. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_NO_MATCH:kotlin.Int` No recognition result matched. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_RECOGNIZER_BUSY:kotlin.Int` RecognitionService busy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_SERVER:kotlin.Int` Server sends error status. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_SERVER_DISCONNECTED:kotlin.Int` Server has been disconnected, e. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_SPEECH_TIMEOUT:kotlin.Int` No speech input |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#ERROR_TOO_MANY_REQUESTS:kotlin.Int` Too many requests from the same client. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#LANGUAGE_DETECTION_CONFIDENCE_LEVEL:kotlin.String` Key used to retrieve the level of confidence of the detected language of the most recent audio chunk, represented by an `int` value prefixed by `LANGUAGE_DETECTION_CONFIDENCE_LEVEL_`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#LANGUAGE_DETECTION_CONFIDENCE_LEVEL_CONFIDENT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#LANGUAGE_DETECTION_CONFIDENCE_LEVEL_HIGHLY_CONFIDENT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#LANGUAGE_DETECTION_CONFIDENCE_LEVEL_NOT_CONFIDENT:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#LANGUAGE_DETECTION_CONFIDENCE_LEVEL_UNKNOWN:kotlin.Int` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#LANGUAGE_SWITCH_RESULT:kotlin.String` Key used to retrieve the result of the language switch of the most recent audio chunk, represented by an `int` value prefixed by `LANGUAGE_SWITCH_`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#LANGUAGE_SWITCH_RESULT_FAILED:kotlin.Int` Switch attempted and failed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#LANGUAGE_SWITCH_RESULT_NOT_ATTEMPTED:kotlin.Int` Switch not attempted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#LANGUAGE_SWITCH_RESULT_SKIPPED_NO_MODEL:kotlin.Int` Switch skipped because the language model is missing or the language is not allowlisted for auto switch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#LANGUAGE_SWITCH_RESULT_SUCCEEDED:kotlin.Int` Switch attempted and succeeded. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#RECOGNITION_PARTS:kotlin.String` Key used to receive an ArrayList\<`https://developer.android.com/reference/kotlin/android/speech/RecognitionPart`\> object from the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to the `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onResults(android.os.Bundle)` and `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onSegmentResults(android.os.Bundle)` methods. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#RESULTS_ALTERNATIVES:kotlin.String` Key used to retrieve an ArrayList\<`https://developer.android.com/reference/kotlin/android/speech/AlternativeSpans`\> from the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to the `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onResults(android.os.Bundle)` and `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onPartialResults(android.os.Bundle)` methods. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#RESULTS_RECOGNITION:kotlin.String` Key used to retrieve an `ArrayList<String>` from the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to the `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onResults(android.os.Bundle)` and `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onPartialResults(android.os.Bundle)` methods. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#TOP_LOCALE_ALTERNATIVES:kotlin.String` Key used to retrieve an ArrayList\<`https://developer.android.com/reference/kotlin/java/lang/String.html#`\> containing representations of the IETF language tags (as defined by BCP 47, e.g., "en-US", "en-UK") denoting the alternative locales for the same language retrieved by the key |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#cancel()()` Cancels the speech recognition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#checkRecognitionSupport(android.content.Intent,%20java.util.concurrent.Executor,%20android.speech.RecognitionSupportCallback)(recognizerIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, supportListener: https://developer.android.com/reference/kotlin/android/speech/RecognitionSupportCallback)` Checks whether `recognizerIntent` is supported by `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#startListening(android.content.Intent)`. |
| open static [SpeechRecognizer](../android/speech/SpeechRecognizer.md) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#createOnDeviceSpeechRecognizer(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Factory method to create a new `SpeechRecognizer`. |
| --- | --- |
| open static [SpeechRecognizer](../android/speech/SpeechRecognizer.md)! | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#createSpeechRecognizer(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Factory method to create a new `SpeechRecognizer`. |
| open static [SpeechRecognizer](../android/speech/SpeechRecognizer.md)! | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#createSpeechRecognizer(android.content.Context,%20android.content.ComponentName)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, serviceComponent: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!)` Factory method to create a new `SpeechRecognizer`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#destroy()()` Destroys the `SpeechRecognizer` object. |
| --- | --- |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#isOnDeviceRecognitionAvailable(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Checks whether an on-device speech recognition service is available on the system. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#isRecognitionAvailable(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Checks whether a speech recognition service is available on the system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#setRecognitionListener(android.speech.RecognitionListener)(listener: https://developer.android.com/reference/kotlin/android/speech/RecognitionListener!)` Sets the listener that will receive all the callbacks. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#startListening(android.content.Intent)(recognizerIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)` Starts listening for speech. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#stopListening()()` Stops listening for speech. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#triggerModelDownload(android.content.Intent)(recognizerIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#)` Attempts to download the support for the given `recognizerIntent`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#triggerModelDownload(android.content.Intent,%20java.util.concurrent.Executor,%20android.speech.ModelDownloadListener)(recognizerIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener)` Attempts to download the support for the given `recognizerIntent`. |

## Constants

### CONFIDENCE_SCORES

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIDENCE_SCORES: String
```

Key used to retrieve a float array from the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to the `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onResults(android.os.Bundle)` and `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onPartialResults(android.os.Bundle)` methods. The array should be the same size as the ArrayList provided in `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#RESULTS_RECOGNITION:kotlin.String`, and should contain values ranging from 0.0 to 1.0, or -1 to represent an unavailable confidence score.

Confidence values close to 1.0 indicate high confidence (the speech recognizer is confident that the recognition result is correct), while values close to 0.0 indicate low confidence.

This value is optional and might not be provided.

 Value: "confidence_scores"

### DETECTED_LANGUAGE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DETECTED_LANGUAGE: String
```

Key used to retrieve a `https://developer.android.com/reference/kotlin/java/lang/String.html#` representation of the IETF language tag (as defined by BCP 47, e.g., "en-US", "de-DE") of the detected language of the most recent audio chunk.

This info is returned to the client in the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onLanguageDetection(android.os.Bundle)` only if `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_ENABLE_LANGUAGE_DETECTION:kotlin.String` is set. Additionally, if `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_LANGUAGE_DETECTION_ALLOWED_LANGUAGES:kotlin.String` are listed, the detected language is constrained to be one from the list.

 Value: "detected_language"

### ERROR_AUDIO

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_AUDIO: Int
```

Audio recording error.

 Value: 3

### ERROR_CANNOT_CHECK_SUPPORT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CANNOT_CHECK_SUPPORT: Int
```

The service does not allow to check for support.

 Value: 14

### ERROR_CANNOT_LISTEN_TO_DOWNLOAD_EVENTS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CANNOT_LISTEN_TO_DOWNLOAD_EVENTS: Int
```

The service does not support listening to model downloads events.

 Value: 15

### ERROR_CLIENT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CLIENT: Int
```

Other client side errors.

 Value: 5

### ERROR_INSUFFICIENT_PERMISSIONS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_INSUFFICIENT_PERMISSIONS: Int
```

Insufficient permissions

 Value: 9

### ERROR_LANGUAGE_NOT_SUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_LANGUAGE_NOT_SUPPORTED: Int
```

Requested language is not available to be used with the current recognizer.

 Value: 12

### ERROR_LANGUAGE_UNAVAILABLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_LANGUAGE_UNAVAILABLE: Int
```

Requested language is supported, but not available currently (e.g. not downloaded yet).

 Value: 13

### ERROR_NETWORK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_NETWORK: Int
```

Other network related errors.

 Value: 2

### ERROR_NETWORK_TIMEOUT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_NETWORK_TIMEOUT: Int
```

Network operation timed out.

 Value: 1

### ERROR_NO_MATCH

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_NO_MATCH: Int
```

No recognition result matched.

 Value: 7

### ERROR_RECOGNIZER_BUSY

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_RECOGNIZER_BUSY: Int
```

RecognitionService busy.

 Value: 8

### ERROR_SERVER

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_SERVER: Int
```

Server sends error status.

 Value: 4

### ERROR_SERVER_DISCONNECTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_SERVER_DISCONNECTED: Int
```

Server has been disconnected, e.g. because the app has crashed.

 Value: 11

### ERROR_SPEECH_TIMEOUT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_SPEECH_TIMEOUT: Int
```

No speech input

 Value: 6

### ERROR_TOO_MANY_REQUESTS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_TOO_MANY_REQUESTS: Int
```

Too many requests from the same client.

 Value: 10

### LANGUAGE_DETECTION_CONFIDENCE_LEVEL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LANGUAGE_DETECTION_CONFIDENCE_LEVEL: String
```

Key used to retrieve the level of confidence of the detected language of the most recent audio chunk, represented by an `int` value prefixed by `LANGUAGE_DETECTION_CONFIDENCE_LEVEL_`.

This info is returned to the client in the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onLanguageDetection(android.os.Bundle)` only if `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_ENABLE_LANGUAGE_DETECTION:kotlin.String` is set.

 Value: "language_detection_confidence_level"

### LANGUAGE_DETECTION_CONFIDENCE_LEVEL_CONFIDENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LANGUAGE_DETECTION_CONFIDENCE_LEVEL_CONFIDENT: Int
```

 Value: 2

### LANGUAGE_DETECTION_CONFIDENCE_LEVEL_HIGHLY_CONFIDENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LANGUAGE_DETECTION_CONFIDENCE_LEVEL_HIGHLY_CONFIDENT: Int
```

 Value: 3

### LANGUAGE_DETECTION_CONFIDENCE_LEVEL_NOT_CONFIDENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LANGUAGE_DETECTION_CONFIDENCE_LEVEL_NOT_CONFIDENT: Int
```

 Value: 1

### LANGUAGE_DETECTION_CONFIDENCE_LEVEL_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LANGUAGE_DETECTION_CONFIDENCE_LEVEL_UNKNOWN: Int
```

 Value: 0

### LANGUAGE_SWITCH_RESULT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LANGUAGE_SWITCH_RESULT: String
```

Key used to retrieve the result of the language switch of the most recent audio chunk, represented by an `int` value prefixed by `LANGUAGE_SWITCH_`.

This info is returned to the client in the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to the `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onLanguageDetection(android.os.Bundle)` only if `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_ENABLE_LANGUAGE_SWITCH:kotlin.String` is set.

 Value: "language_switch_result"

### LANGUAGE_SWITCH_RESULT_FAILED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LANGUAGE_SWITCH_RESULT_FAILED: Int
```

Switch attempted and failed.

 Value: 2

### LANGUAGE_SWITCH_RESULT_NOT_ATTEMPTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LANGUAGE_SWITCH_RESULT_NOT_ATTEMPTED: Int
```

Switch not attempted.

 Value: 0

### LANGUAGE_SWITCH_RESULT_SKIPPED_NO_MODEL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LANGUAGE_SWITCH_RESULT_SKIPPED_NO_MODEL: Int
```

Switch skipped because the language model is missing or the language is not allowlisted for auto switch.

 Value: 3

### LANGUAGE_SWITCH_RESULT_SUCCEEDED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LANGUAGE_SWITCH_RESULT_SUCCEEDED: Int
```

Switch attempted and succeeded.

 Value: 1

### RECOGNITION_PARTS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RECOGNITION_PARTS: String
```

Key used to receive an ArrayList\<`https://developer.android.com/reference/kotlin/android/speech/RecognitionPart`\> object from the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to the `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onResults(android.os.Bundle)` and `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onSegmentResults(android.os.Bundle)` methods.

A single `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#` result is represented as a `https://developer.android.com/reference/kotlin/java/lang/String.html#`. Each word of the resulting String, as well as any potential adjacent punctuation, is represented by a `https://developer.android.com/reference/kotlin/android/speech/RecognitionPart` item from the ArrayList retrieved by this key.

 Value: "recognition_parts"

### RESULTS_ALTERNATIVES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULTS_ALTERNATIVES: String
```

Key used to retrieve an ArrayList\<`https://developer.android.com/reference/kotlin/android/speech/AlternativeSpans`\> from the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to the `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onResults(android.os.Bundle)` and `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onPartialResults(android.os.Bundle)` methods. The list should be the same size as the ArrayList provided in `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#RESULTS_RECOGNITION:kotlin.String`.

A single `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#` result is represented as a `https://developer.android.com/reference/kotlin/java/lang/String.html#`. For a specific span (substring) of the originally recognized result string the recognizer provides a list of alternative hypotheses in the form of an `https://developer.android.com/reference/kotlin/android/speech/AlternativeSpan` object. Alternatives for different spans of a result string are listed in an `https://developer.android.com/reference/kotlin/android/speech/AlternativeSpans` object. Each item from the ArrayList retrieved by this key corresponds to a single result string provided in `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#RESULTS_RECOGNITION:kotlin.String`.

This value is optional and might not be provided.

 Value: "results_alternatives"

### RESULTS_RECOGNITION

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULTS_RECOGNITION: String
```

Key used to retrieve an `ArrayList<String>` from the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to the `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onResults(android.os.Bundle)` and `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onPartialResults(android.os.Bundle)` methods. These strings are the possible recognition results, where the first element is the most likely candidate.

 Value: "results_recognition"

### TOP_LOCALE_ALTERNATIVES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOP_LOCALE_ALTERNATIVES: String
```

Key used to retrieve an ArrayList\<`https://developer.android.com/reference/kotlin/java/lang/String.html#`\> containing representations of the IETF language tags (as defined by BCP 47, e.g., "en-US", "en-UK") denoting the alternative locales for the same language retrieved by the key `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#DETECTED_LANGUAGE:kotlin.String`. This info is returned to the client in the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onLanguageDetection(android.os.Bundle)` only if `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_ENABLE_LANGUAGE_DETECTION:kotlin.String` is set.

 Value: "top_locale_alternatives"

## Public methods

### cancel

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancel(): Unit
```

Cancels the speech recognition. Please note that `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#setRecognitionListener(android.speech.RecognitionListener)` should be called beforehand, otherwise no notifications will be received. 
This method must be called from the main thread of your app.

### checkRecognitionSupport

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkRecognitionSupport(
    recognizerIntent: Intent, 
    executor: Executor, 
    supportListener: RecognitionSupportCallback
): Unit
```

Checks whether `recognizerIntent` is supported by `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#startListening(android.content.Intent)`.

| Parameters ||
|---|---|
| `recognizerIntent` | [Intent](../android/content/Intent.md): contains parameters for the recognition to be performed. The intent may also contain optional extras. See `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent` for the list of supported extras, any unlisted extra might be ignored. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `supportListener` | [RecognitionSupportCallback](../android/speech/RecognitionSupportCallback.md): the listener on which to receive the support query results. This value cannot be `null`. |
| --- | --- |

### createOnDeviceSpeechRecognizer

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createOnDeviceSpeechRecognizer(context: Context): SpeechRecognizer
```

Factory method to create a new `SpeechRecognizer`.

Please note that `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#setRecognitionListener(android.speech.RecognitionListener)` should be called before dispatching any command to the created `SpeechRecognizer`, otherwise no notifications will be received.

**Important:** the caller MUST invoke `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#destroy()` on a SpeechRecognizer object when it is no longer needed. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md): in which to create `SpeechRecognizer` This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#` | a new on-device `SpeechRecognizer`. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | iff `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#isOnDeviceRecognitionAvailable(android.content.Context)` is false |

### createSpeechRecognizer

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createSpeechRecognizer(context: Context!): SpeechRecognizer!
```

Factory method to create a new `SpeechRecognizer`. Please note that `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#setRecognitionListener(android.speech.RecognitionListener)` should be called before dispatching any command to the created `SpeechRecognizer`, otherwise no notifications will be received.

**Important:** the caller MUST invoke `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#destroy()` on a SpeechRecognizer object when it is no longer needed.

For apps targeting Android 11 (API level 30) interaction with a speech recognition service requires element to be added to the manifest file:

```kotlin
<code>&lt;queries&gt;
    &lt;intent&gt;
      &lt;action
         android:name="android.speech.RecognitionService" /&gt;
    &lt;/intent&gt;
  &lt;/queries&gt;
  </code>
```
. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md)!: in which to create `SpeechRecognizer` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#!` | a new `SpeechRecognizer` |

### createSpeechRecognizer

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createSpeechRecognizer(
    context: Context!, 
    serviceComponent: ComponentName!
): SpeechRecognizer!
```

Factory method to create a new `SpeechRecognizer`. Please note that `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#setRecognitionListener(android.speech.RecognitionListener)` should be called before dispatching any command to the created `SpeechRecognizer`, otherwise no notifications will be received. Use this version of the method to specify a specific service to direct this `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#` to.

**Important:** the caller MUST invoke `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#destroy()` on a SpeechRecognizer object when it is no longer needed.

**Important** : before calling this method, please check via `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentServices(android.content.Intent,%20kotlin.Int)` that `serviceComponent` actually exists and provides `https://developer.android.com/reference/kotlin/android/speech/RecognitionService#SERVICE_INTERFACE:kotlin.String`. Normally you would not use this; call `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#createSpeechRecognizer(android.content.Context)` to use the system default recognition service instead.

For apps targeting Android 11 (API level 30) interaction with a speech recognition service requires element to be added to the manifest file:

```kotlin
<code>&lt;queries&gt;
    &lt;intent&gt;
      &lt;action
         android:name="android.speech.RecognitionService" /&gt;
    &lt;/intent&gt;
  &lt;/queries&gt;
  </code>
```
. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md)!: in which to create `SpeechRecognizer` |
| `serviceComponent` | [ComponentName](../android/content/ComponentName.md)!: the `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of a specific service to direct this `SpeechRecognizer` to |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#!` | a new `SpeechRecognizer` |

### destroy

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun destroy(): Unit
```

Destroys the `SpeechRecognizer` object.

### isOnDeviceRecognitionAvailable

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isOnDeviceRecognitionAvailable(context: Context): Boolean
```

Checks whether an on-device speech recognition service is available on the system. If this method returns `false`, `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#createOnDeviceSpeechRecognizer(android.content.Context)` will fail.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md): with which on-device `SpeechRecognizer` will be created. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if on-device recognition is available, `false` otherwise |

### isRecognitionAvailable

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isRecognitionAvailable(context: Context): Boolean
```

Checks whether a speech recognition service is available on the system. If this method returns `false`, `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#createSpeechRecognizer(android.content.Context)` will fail.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md): with which `SpeechRecognizer` will be created. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if recognition is available, `false` otherwise |

### setRecognitionListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRecognitionListener(listener: RecognitionListener!): Unit
```

Sets the listener that will receive all the callbacks. The previous unfinished commands will be executed with the old listener, while any following command will be executed with the new listener. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `listener` | [RecognitionListener](../android/speech/RecognitionListener.md)!: listener that will receive all the callbacks from the created `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#`, this must not be null. |

### startListening

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startListening(recognizerIntent: Intent!): Unit
```

Starts listening for speech. Please note that `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#setRecognitionListener(android.speech.RecognitionListener)` should be called beforehand, otherwise no notifications will be received. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `recognizerIntent` | [Intent](../android/content/Intent.md)!: contains parameters for the recognition to be performed. The intent may also contain optional extras, see `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent`. If these values are not set explicitly, default values will be used by the recognizer. |

### stopListening

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stopListening(): Unit
```

Stops listening for speech. Speech captured so far will be recognized as if the user had stopped speaking at this point.

Note that in the default case, this does not need to be called, as the speech endpointer will automatically stop the recognizer listening when it determines speech has completed. However, you can manipulate endpointer parameters directly using the intent extras defined in `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent`, in which case you may sometimes want to manually call this method to stop listening sooner.

Upon invocation clients must wait until `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onResults(android.os.Bundle)` or `https://developer.android.com/reference/kotlin/android/speech/RecognitionListener#onError(kotlin.Int)` are invoked before calling `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#startListening(android.content.Intent)` again. Otherwise such an attempt would be rejected by recognition service.

Please note that `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#setRecognitionListener(android.speech.RecognitionListener)` should be called beforehand, otherwise no notifications will be received. 
This method must be called from the main thread of your app.

### triggerModelDownload

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun triggerModelDownload(recognizerIntent: Intent): Unit
```

Attempts to download the support for the given `recognizerIntent`. This might trigger user interaction to approve the download. Callers can verify the status of the request via `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#checkRecognitionSupport(android.content.Intent,%20java.util.concurrent.Executor,%20android.speech.RecognitionSupportCallback)`.

| Parameters ||
|---|---|
| `recognizerIntent` | [Intent](../android/content/Intent.md): contains parameters for the recognition to be performed. The intent may also contain optional extras, see `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent`. This value cannot be `null`. |

### triggerModelDownload

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun triggerModelDownload(
    recognizerIntent: Intent, 
    executor: Executor, 
    listener: ModelDownloadListener
): Unit
```

Attempts to download the support for the given `recognizerIntent`. This might trigger user interaction to approve the download. Callers can verify the status of the request via `https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer#checkRecognitionSupport(android.content.Intent,%20java.util.concurrent.Executor,%20android.speech.RecognitionSupportCallback)`.

The updates about the model download request are received via the given `https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener`:
- If the model is already available, `https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener#onSuccess()` will be called directly. The model can be safely used afterwards.
- If the `https://developer.android.com/reference/kotlin/android/speech/RecognitionService` has started the download, `https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener#onProgress(kotlin.Int)` will be called an unspecified (zero or more) number of times until the download is complete. When the download finishes, `https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener#onSuccess()` will be called. The model can be safely used afterwards.
- If the `https://developer.android.com/reference/kotlin/android/speech/RecognitionService` has only scheduled the download, but won't satisfy it immediately, `https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener#onScheduled()` will be called. There will be no further updates on this listener.
- If the request fails at any time due to a network or scheduling error, `https://developer.android.com/reference/kotlin/android/speech/ModelDownloadListener#onError(kotlin.Int)` will be called.

| Parameters ||
|---|---|
| `recognizerIntent` | [Intent](../android/content/Intent.md): contains parameters for the recognition to be performed. The intent may also contain optional extras, see `https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent`. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): for dispatching listener callbacks. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [ModelDownloadListener](../android/speech/ModelDownloadListener.md): on which to receive updates about the model download request. This value cannot be `null`. |
| --- | --- |
