# RecognizerIntent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecognizerIntent

Kotlin| [Java](../android/speech/RecognizerIntent.md) 
| --- | --- |

```
open class RecognizerIntent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.speech.RecognizerIntent](../android/speech/RecognizerIntent.md) |

Constants for supporting speech recognition through starting an [Intent](../android/content/Intent.md)

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_GET_LANGUAGE_DETAILS](../android/speech/RecognizerIntent.md) A broadcast intent which can be fired to the [BroadcastReceiver](../android/content/BroadcastReceiver.md) component specified in the meta-data defined in the [DETAILS_META_DATA](../android/speech/RecognizerIntent.md) meta-data of an [Activity](../android/app/Activity.md) satisfying [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_RECOGNIZE_SPEECH](../android/speech/RecognizerIntent.md) Starts an activity that will prompt the user for speech and send it through a speech recognizer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_VOICE_SEARCH_HANDS_FREE](../android/speech/RecognizerIntent.md) Starts an activity that will prompt the user for speech without requiring the user's visual attention or touch input. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md) Starts an activity that will prompt the user for speech, send it through a speech recognizer, and either display a web search result or trigger another type of action based on the user's speech. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DETAILS_META_DATA](../android/speech/RecognizerIntent.md) Meta-data name under which an [Activity](../android/app/Activity.md) implementing [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md) can use to expose the class name of a [BroadcastReceiver](../android/content/BroadcastReceiver.md) which can respond to request for more information, from any of the broadcast intents specified in this class. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_INJECT_SOURCE](../android/speech/RecognizerIntent.md) The extra key used in an intent which is providing an already opened audio source for the RecognitionService to use. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SOURCE](../android/speech/RecognizerIntent.md) Optional [android.os.ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) pointing to an already opened audio source for the recognizer to use. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SOURCE_CHANNEL_COUNT](../android/speech/RecognizerIntent.md) Optional integer, to be used with [EXTRA_AUDIO_SOURCE](../android/speech/RecognizerIntent.md), to indicate the number of channels in the audio. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SOURCE_ENCODING](../android/speech/RecognizerIntent.md) Optional integer (from [android.media.AudioFormat](../android/media/AudioFormat.md)), to be used with [EXTRA_AUDIO_SOURCE](../android/speech/RecognizerIntent.md), to indicate the audio encoding. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SOURCE_SAMPLING_RATE](../android/speech/RecognizerIntent.md) Optional integer, to be used with [EXTRA_AUDIO_SOURCE](../android/speech/RecognizerIntent.md), to indicate the sampling rate of the audio. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_BIASING_STRINGS](../android/speech/RecognizerIntent.md) Optional list of strings, towards which the recognizer should bias the recognition results. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CALLING_PACKAGE](../android/speech/RecognizerIntent.md) The extra key used in an intent to the speech recognizer for voice search. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CONFIDENCE_SCORES](../android/speech/RecognizerIntent.md) A float array of confidence scores of the recognition results when performing [ACTION_RECOGNIZE_SPEECH](../android/speech/RecognizerIntent.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ENABLE_BIASING_DEVICE_CONTEXT](../android/speech/RecognizerIntent.md) Optional boolean to enable biasing towards device context. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ENABLE_FORMATTING](../android/speech/RecognizerIntent.md) Optional string to enable text formatting (e.g. unspoken punctuation (examples: question mark, comma, period, etc.), capitalization, etc. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ENABLE_LANGUAGE_DETECTION](../android/speech/RecognizerIntent.md) Optional boolean indicating whether to enable language detection. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md) Optional string to enable automatic switching to the language being spoken with the desired sensitivity level, instead of being restricted to a single language. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_HIDE_PARTIAL_TRAILING_PUNCTUATION](../android/speech/RecognizerIntent.md) Optional boolean, to be used with [EXTRA_ENABLE_FORMATTING](../android/speech/RecognizerIntent.md), to prevent the recognizer adding punctuation after the last word of the partial results. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LANGUAGE](../android/speech/RecognizerIntent.md) Optional IETF language tag (as defined by BCP 47), for example "en-US". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LANGUAGE_DETECTION_ALLOWED_LANGUAGES](../android/speech/RecognizerIntent.md) Optional list of IETF language tags (as defined by BCP 47, e.g. "en-US", "de-DE"). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LANGUAGE_MODEL](../android/speech/RecognizerIntent.md) Informs the recognizer which speech model to prefer when performing [ACTION_RECOGNIZE_SPEECH](../android/speech/RecognizerIntent.md). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LANGUAGE_PREFERENCE](../android/speech/RecognizerIntent.md) The key to the extra in the [Bundle](../android/os/Bundle.md) returned by [ACTION_GET_LANGUAGE_DETAILS](../android/speech/RecognizerIntent.md) which is a [String](../java/lang/String.md) that represents the current language preference this user has specified - a locale string like "en-US". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LANGUAGE_SWITCH_ALLOWED_LANGUAGES](../android/speech/RecognizerIntent.md) Optional list of IETF language tags (as defined by BCP 47, e.g. "en-US", "de-DE"). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LANGUAGE_SWITCH_INITIAL_ACTIVE_DURATION_TIME_MILLIS](../android/speech/RecognizerIntent.md) Optional integer to use for [EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LANGUAGE_SWITCH_MAX_SWITCHES](../android/speech/RecognizerIntent.md) Optional integer to use for [EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_MASK_OFFENSIVE_WORDS](../android/speech/RecognizerIntent.md) Optional boolean indicating whether the recognizer should mask the offensive words in recognition results. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_MAX_RESULTS](../android/speech/RecognizerIntent.md) Optional limit on the maximum number of results to return. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ONLY_RETURN_LANGUAGE_PREFERENCE](../android/speech/RecognizerIntent.md) Specify this boolean extra in a broadcast of [ACTION_GET_LANGUAGE_DETAILS](../android/speech/RecognizerIntent.md) to indicate that only the current language preference is needed in the response. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ORIGIN](../android/speech/RecognizerIntent.md) Optional value which can be used to indicate the referer url of a page in which speech was requested. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PARTIAL_RESULTS](../android/speech/RecognizerIntent.md) Optional boolean to indicate whether partial results should be returned by the recognizer as the user speaks (default is false). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PREFER_OFFLINE](../android/speech/RecognizerIntent.md) Optional boolean, to be used with [ACTION_RECOGNIZE_SPEECH](../android/speech/RecognizerIntent.md), [ACTION_VOICE_SEARCH_HANDS_FREE](../android/speech/RecognizerIntent.md), [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md) to indicate whether to only use an offline speech recognition engine. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROMPT](../android/speech/RecognizerIntent.md) Optional text prompt to show to the user when asking them to speak. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_REQUEST_WORD_CONFIDENCE](../android/speech/RecognizerIntent.md) Optional boolean indicating whether the recognizer should return the confidence level of each word in the final recognition results. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_REQUEST_WORD_TIMING](../android/speech/RecognizerIntent.md) Optional boolean indicating whether the recognizer should return the timestamp of each word in the final recognition results. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_RESULTS](../android/speech/RecognizerIntent.md) An ArrayList\<String\> of the recognition results when performing [ACTION_RECOGNIZE_SPEECH](../android/speech/RecognizerIntent.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_RESULTS_PENDINGINTENT](../android/speech/RecognizerIntent.md) When the intent is [ACTION_RECOGNIZE_SPEECH](../android/speech/RecognizerIntent.md), the speech input activity will return results to you via the activity results mechanism. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_RESULTS_PENDINGINTENT_BUNDLE](../android/speech/RecognizerIntent.md) If you use [EXTRA_RESULTS_PENDINGINTENT](../android/speech/RecognizerIntent.md) to supply a forwarding intent, you can also use this extra to supply additional extras for the final intent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SECURE](../android/speech/RecognizerIntent.md) Optional boolean to indicate that a "hands free" voice search was performed while the device was in a secure mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SEGMENTED_SESSION](../android/speech/RecognizerIntent.md) Optional string to enable segmented session mode of the specified type, which can be [EXTRA_AUDIO_SOURCE](../android/speech/RecognizerIntent.md), [EXTRA_SPEECH_INPUT_MINIMUM_LENGTH_MILLIS](../android/speech/RecognizerIntent.md) or [EXTRA_SPEECH_INPUT_COMPLETE_SILENCE_LENGTH_MILLIS](../android/speech/RecognizerIntent.md). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SPEECH_INPUT_COMPLETE_SILENCE_LENGTH_MILLIS](../android/speech/RecognizerIntent.md) The amount of time that it should take after the recognizer stops hearing speech to consider the input complete hence end the recognition session. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SPEECH_INPUT_MINIMUM_LENGTH_MILLIS](../android/speech/RecognizerIntent.md) Optional integer to indicate the minimum length of the recognition session. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SPEECH_INPUT_POSSIBLY_COMPLETE_SILENCE_LENGTH_MILLIS](../android/speech/RecognizerIntent.md) The amount of time that it should take after we stop hearing speech to consider the input possibly complete. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SUPPORTED_LANGUAGES](../android/speech/RecognizerIntent.md) The key to the extra in the [Bundle](../android/os/Bundle.md) returned by [ACTION_GET_LANGUAGE_DETAILS](../android/speech/RecognizerIntent.md) which is an [ArrayList](../java/util/ArrayList.md) of [String](../java/lang/String.md) s that represents the languages supported by this implementation of voice recognition - a list of strings like "en-US", "cmn-Hans-CN", etc. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_WEB_SEARCH_ONLY](../android/speech/RecognizerIntent.md) Optional boolean, to be used with [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md), to indicate whether to only fire web searches in response to a user's speech. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMATTING_OPTIMIZE_LATENCY](../android/speech/RecognizerIntent.md) Optimizes formatting latency. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMATTING_OPTIMIZE_QUALITY](../android/speech/RecognizerIntent.md) Optimizes formatting quality. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LANGUAGE_MODEL_FREE_FORM](../android/speech/RecognizerIntent.md) Use a language model based on free-form speech recognition. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LANGUAGE_MODEL_WEB_SEARCH](../android/speech/RecognizerIntent.md) Use a language model based on web search terms. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LANGUAGE_SWITCH_BALANCED](../android/speech/RecognizerIntent.md) A value to use for [EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LANGUAGE_SWITCH_HIGH_PRECISION](../android/speech/RecognizerIntent.md) A value to use for [EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LANGUAGE_SWITCH_QUICK_RESPONSE](../android/speech/RecognizerIntent.md) A value to use for [EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_AUDIO_ERROR](../android/speech/RecognizerIntent.md) Result code returned when an audio error was encountered |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_CLIENT_ERROR](../android/speech/RecognizerIntent.md) Result code returned when there is a generic client error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_NETWORK_ERROR](../android/speech/RecognizerIntent.md) Result code returned when a network error was encountered |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_NO_MATCH](../android/speech/RecognizerIntent.md) Result code returned when no matches are found for the given speech |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_SERVER_ERROR](../android/speech/RecognizerIntent.md) Result code returned when the recognition server returns an error |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Intent](../android/content/Intent.md)! | [getVoiceDetailsIntent](../android/speech/RecognizerIntent.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Returns the broadcast intent to fire with [Context.sendOrderedBroadcast(Intent, String, BroadcastReceiver, android.os.Handler, int, String, Bundle)](../android/content/Context.md))to receive details from the package that implements voice search. |

## Constants

### ACTION_GET_LANGUAGE_DETAILS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_GET_LANGUAGE_DETAILS: String
```

A broadcast intent which can be fired to the [BroadcastReceiver](../android/content/BroadcastReceiver.md) component specified in the meta-data defined in the [DETAILS_META_DATA](../android/speech/RecognizerIntent.md) meta-data of an [Activity](../android/app/Activity.md) satisfying [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md).

When fired with [Context.sendOrderedBroadcast(Intent, String, BroadcastReceiver, android.os.Handler, int, String, android.os.Bundle)](../android/content/Context.md)), a [Bundle](../android/os/Bundle.md) of extras will be returned to the provided result receiver, and should ideally contain values for [EXTRA_LANGUAGE_PREFERENCE](../android/speech/RecognizerIntent.md) and [EXTRA_SUPPORTED_LANGUAGES](../android/speech/RecognizerIntent.md).

(Whether these are actually provided is up to the particular implementation. It is recommended that [Activity](../android/app/Activity.md) s implementing [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md) provide this information, but it is not required.) 

 Value: "android.speech.action.GET_LANGUAGE_DETAILS"

### ACTION_RECOGNIZE_SPEECH

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_RECOGNIZE_SPEECH: String
```

Starts an activity that will prompt the user for speech and send it through a speech recognizer. The results will be returned via activity results (in android.app.Activity#onActivityResult, if you start the intent using [Activity.startActivityForResult(Intent, int)](../android/app/Activity.md))), or forwarded via a PendingIntent if one is provided.

Starting this intent with just android.app.Activity#startActivity(android.content.Intent) is not supported. You must either use [Activity.startActivityForResult(Intent, int)](../android/app/Activity.md)), or provide a PendingIntent, to receive recognition results.

The implementation of this API is likely to stream audio to remote servers to perform speech recognition which can use a substantial amount of bandwidth.

Required extras:

- [EXTRA_LANGUAGE_MODEL](../android/speech/RecognizerIntent.md)

Optional extras:

- [EXTRA_PROMPT](../android/speech/RecognizerIntent.md)
- [EXTRA_LANGUAGE](../android/speech/RecognizerIntent.md)
- [EXTRA_MAX_RESULTS](../android/speech/RecognizerIntent.md)
- [EXTRA_RESULTS_PENDINGINTENT](../android/speech/RecognizerIntent.md)
- [EXTRA_RESULTS_PENDINGINTENT_BUNDLE](../android/speech/RecognizerIntent.md)

Result extras (returned in the result, not to be specified in the request):

- [EXTRA_RESULTS](../android/speech/RecognizerIntent.md)

NOTE: There may not be any applications installed to handle this action, so you should make sure to catch [ActivityNotFoundException](../android/content/ActivityNotFoundException.md). 

 Value: "android.speech.action.RECOGNIZE_SPEECH"

### ACTION_VOICE_SEARCH_HANDS_FREE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_VOICE_SEARCH_HANDS_FREE: String
```

Starts an activity that will prompt the user for speech without requiring the user's visual attention or touch input. It will send it through a speech recognizer, and either synthesize speech for a web search result or trigger another type of action based on the user's speech. This activity may be launched while device is locked in a secure mode. Special care must be taken to ensure that the voice actions that are performed while hands free cannot compromise the device's security. The activity should check the value of the [EXTRA_SECURE](../android/speech/RecognizerIntent.md) extra to determine whether the device has been securely locked. If so, the activity should either restrict the set of voice actions that are permitted or require some form of secure authentication before proceeding. To ensure that the activity's user interface is visible while the lock screen is showing, the activity should set the [android.view.WindowManager.LayoutParams#FLAG_SHOW_WHEN_LOCKED](../android/view/WindowManager.LayoutParams.md) window flag. Otherwise the activity's user interface may be hidden by the lock screen. The activity should take care not to leak private information when the device is securely locked.

Optional extras:

- [EXTRA_SECURE](../android/speech/RecognizerIntent.md)

In some cases, a matching Activity may not exist, so ensure you safeguard against this. 

 Value: "android.speech.action.VOICE_SEARCH_HANDS_FREE"

### ACTION_WEB_SEARCH

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_WEB_SEARCH: String
```

Starts an activity that will prompt the user for speech, send it through a speech recognizer, and either display a web search result or trigger another type of action based on the user's speech.

If you want to avoid triggering any type of action besides web search, you can use the [EXTRA_WEB_SEARCH_ONLY](../android/speech/RecognizerIntent.md) extra.

Required extras:

- [EXTRA_LANGUAGE_MODEL](../android/speech/RecognizerIntent.md)

Optional extras:

- [EXTRA_PROMPT](../android/speech/RecognizerIntent.md)
- [EXTRA_LANGUAGE](../android/speech/RecognizerIntent.md)
- [EXTRA_MAX_RESULTS](../android/speech/RecognizerIntent.md)
- [EXTRA_PARTIAL_RESULTS](../android/speech/RecognizerIntent.md)
- [EXTRA_WEB_SEARCH_ONLY](../android/speech/RecognizerIntent.md)
- [EXTRA_ORIGIN](../android/speech/RecognizerIntent.md)

Result extras (returned in the result, not to be specified in the request):

- [EXTRA_RESULTS](../android/speech/RecognizerIntent.md)
- [EXTRA_CONFIDENCE_SCORES](../android/speech/RecognizerIntent.md)(optional)

NOTE: There may not be any applications installed to handle this action, so you should make sure to catch [ActivityNotFoundException](../android/content/ActivityNotFoundException.md). 

 Value: "android.speech.action.WEB_SEARCH"

### DETAILS_META_DATA

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DETAILS_META_DATA: String
```

Meta-data name under which an [Activity](../android/app/Activity.md) implementing [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md) can use to expose the class name of a [BroadcastReceiver](../android/content/BroadcastReceiver.md) which can respond to request for more information, from any of the broadcast intents specified in this class.

Broadcast intents can be directed to the class name specified in the meta-data by creating an [Intent](../android/content/Intent.md), setting the component with [Intent.setComponent(android.content.ComponentName)](../android/content/Intent.md)), and using [Context.sendOrderedBroadcast(Intent, String, BroadcastReceiver, android.os.Handler, int, String, android.os.Bundle)](../android/content/Context.md))with another [BroadcastReceiver](../android/content/BroadcastReceiver.md) which can receive the results.

The [getVoiceDetailsIntent(android.content.Context)](../android/speech/RecognizerIntent.md))method is provided as a convenience to create a broadcast intent based on the value of this meta-data, if available.

This is optional and not all [Activity](../android/app/Activity.md) s which implement [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md) are required to implement this. Thus retrieving this meta-data may be null. 

 Value: "android.speech.DETAILS"

### EXTRA_AUDIO_INJECT_SOURCE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_AUDIO_INJECT_SOURCE: String
```

**Deprecated:** *Replaced with [EXTRA_AUDIO_SOURCE](../android/speech/RecognizerIntent.md)*

The extra key used in an intent which is providing an already opened audio source for the RecognitionService to use. Data should be a URI to an audio resource.

Depending on the recognizer implementation, this value may have no effect. 

 Value: "android.speech.extra.AUDIO_INJECT_SOURCE"

### EXTRA_AUDIO_SOURCE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_AUDIO_SOURCE: String
```

Optional [android.os.ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) pointing to an already opened audio source for the recognizer to use. The caller of the recognizer is responsible for closing the audio. If this extra is not set or the recognizer does not support this feature, the recognizer will open the mic for audio and close it when the recognition is finished.

Along with this extra, please send [EXTRA_AUDIO_SOURCE_CHANNEL_COUNT](../android/speech/RecognizerIntent.md), [EXTRA_AUDIO_SOURCE_ENCODING](../android/speech/RecognizerIntent.md), and [EXTRA_AUDIO_SOURCE_SAMPLING_RATE](../android/speech/RecognizerIntent.md) extras, otherwise the default values of these extras will be used.

Additionally, [EXTRA_ENABLE_BIASING_DEVICE_CONTEXT](../android/speech/RecognizerIntent.md) may have no effect when this extra is set.

This can also be used as the string value for [EXTRA_SEGMENTED_SESSION](../android/speech/RecognizerIntent.md) to enable segmented session mode. The audio must be passed in using this extra. The recognition session will end when and only when the audio is closed. 

 Value: "android.speech.extra.AUDIO_SOURCE"

**See Also**

- [#EXTRA_SEGMENTED_SESSION](../android/speech/RecognizerIntent.md) 

### EXTRA_AUDIO_SOURCE_CHANNEL_COUNT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_AUDIO_SOURCE_CHANNEL_COUNT: String
```

Optional integer, to be used with [EXTRA_AUDIO_SOURCE](../android/speech/RecognizerIntent.md), to indicate the number of channels in the audio. The default value is 1. 

 Value: "android.speech.extra.AUDIO_SOURCE_CHANNEL_COUNT"

### EXTRA_AUDIO_SOURCE_ENCODING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_AUDIO_SOURCE_ENCODING: String
```

Optional integer (from [android.media.AudioFormat](../android/media/AudioFormat.md)), to be used with [EXTRA_AUDIO_SOURCE](../android/speech/RecognizerIntent.md), to indicate the audio encoding. The default value is [android.media.AudioFormat#ENCODING_PCM_16BIT](../android/media/AudioFormat.md). 

 Value: "android.speech.extra.AUDIO_SOURCE_ENCODING"

### EXTRA_AUDIO_SOURCE_SAMPLING_RATE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_AUDIO_SOURCE_SAMPLING_RATE: String
```

Optional integer, to be used with [EXTRA_AUDIO_SOURCE](../android/speech/RecognizerIntent.md), to indicate the sampling rate of the audio. The default value is 16000. 

 Value: "android.speech.extra.AUDIO_SOURCE_SAMPLING_RATE"

### EXTRA_BIASING_STRINGS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_BIASING_STRINGS: String
```

Optional list of strings, towards which the recognizer should bias the recognition results. These are separate from the device context. 

 Value: "android.speech.extra.BIASING_STRINGS"

### EXTRA_CALLING_PACKAGE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CALLING_PACKAGE: String
```

The extra key used in an intent to the speech recognizer for voice search. Not generally to be used by developers. The system search dialog uses this, for example, to set a calling package for identification by a voice search API. If this extra is set by anyone but the system process, it should be overridden by the voice search implementation. 

 Value: "calling_package"

### EXTRA_CONFIDENCE_SCORES

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CONFIDENCE_SCORES: String
```

A float array of confidence scores of the recognition results when performing [ACTION_RECOGNIZE_SPEECH](../android/speech/RecognizerIntent.md). The array should be the same size as the ArrayList returned in [EXTRA_RESULTS](../android/speech/RecognizerIntent.md), and should contain values ranging from 0.0 to 1.0, or -1 to represent an unavailable confidence score.

Confidence values close to 1.0 indicate high confidence (the speech recognizer is confident that the recognition result is correct), while values close to 0.0 indicate low confidence.

Returned in the results; not to be specified in the recognition request. This extra is optional and might not be provided. Only present when [Activity.RESULT_OK](../android/app/Activity.md) is returned in an activity result. 

 Value: "android.speech.extra.CONFIDENCE_SCORES"

### EXTRA_ENABLE_BIASING_DEVICE_CONTEXT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ENABLE_BIASING_DEVICE_CONTEXT: String
```

Optional boolean to enable biasing towards device context. The recognizer will use the device context to tune the recognition results.

Depending on the recognizer implementation, this value may have no effect. 

 Value: "android.speech.extra.ENABLE_BIASING_DEVICE_CONTEXT"

### EXTRA_ENABLE_FORMATTING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ENABLE_FORMATTING: String
```

Optional string to enable text formatting (e.g. unspoken punctuation (examples: question mark, comma, period, etc.), capitalization, etc.) and specify the optimization strategy. If set, the partial and final result texts will be formatted. Each result list will contain two hypotheses in the order of 1) formatted text 2) raw text.

Depending on the recognizer implementation, this value may have no effect. 

 Value: "android.speech.extra.ENABLE_FORMATTING"

**See Also**

- [#FORMATTING_OPTIMIZE_QUALITY](../android/speech/RecognizerIntent.md)
- [#FORMATTING_OPTIMIZE_LATENCY](../android/speech/RecognizerIntent.md) 

### EXTRA_ENABLE_LANGUAGE_DETECTION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ENABLE_LANGUAGE_DETECTION: String
```

Optional boolean indicating whether to enable language detection. When enabled, the recognizer will consistently identify the language of the current spoken utterance and provide that info via [RecognitionListener.onLanguageDetection(Bundle)](../android/speech/RecognitionListener.md)).

Depending on the recognizer implementation, this flag may have no effect. 

 Value: "android.speech.extra.ENABLE_LANGUAGE_DETECTION"

### EXTRA_ENABLE_LANGUAGE_SWITCH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ENABLE_LANGUAGE_SWITCH: String
```

Optional string to enable automatic switching to the language being spoken with the desired sensitivity level, instead of being restricted to a single language. The corresponding language models must be downloaded to support the switch. Otherwise, the recognizer will report an error on a switch failure. The recognizer provides the switch results via [RecognitionListener.onLanguageDetection(Bundle)](../android/speech/RecognitionListener.md)).

Since detection is a necessary requirement for the language switching, setting this value implicitly enables [EXTRA_ENABLE_LANGUAGE_DETECTION](../android/speech/RecognizerIntent.md).

Depending on the recognizer implementation, this value may have no effect. 

 Value: "android.speech.extra.ENABLE_LANGUAGE_SWITCH"

**See Also**

- [#LANGUAGE_SWITCH_HIGH_PRECISION](../android/speech/RecognizerIntent.md)
- [#LANGUAGE_SWITCH_BALANCED](../android/speech/RecognizerIntent.md)
- [#LANGUAGE_SWITCH_QUICK_RESPONSE](../android/speech/RecognizerIntent.md) 

### EXTRA_HIDE_PARTIAL_TRAILING_PUNCTUATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_HIDE_PARTIAL_TRAILING_PUNCTUATION: String
```

Optional boolean, to be used with [EXTRA_ENABLE_FORMATTING](../android/speech/RecognizerIntent.md), to prevent the recognizer adding punctuation after the last word of the partial results. The default is false. 

 Value: "android.speech.extra.HIDE_PARTIAL_TRAILING_PUNCTUATION"

### EXTRA_LANGUAGE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LANGUAGE: String
```

Optional IETF language tag (as defined by BCP 47), for example "en-US". This tag informs the recognizer to perform speech recognition in a language different than the one set in the [java.util.Locale#getDefault()](../java/util/Locale.md)). 

 Value: "android.speech.extra.LANGUAGE"

### EXTRA_LANGUAGE_DETECTION_ALLOWED_LANGUAGES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LANGUAGE_DETECTION_ALLOWED_LANGUAGES: String
```

Optional list of IETF language tags (as defined by BCP 47, e.g. "en-US", "de-DE"). This extra is to be used with [EXTRA_ENABLE_LANGUAGE_DETECTION](../android/speech/RecognizerIntent.md). If set, the recognizer will constrain the language detection output to this list of languages, potentially improving detection accuracy. 

 Value: "android.speech.extra.LANGUAGE_DETECTION_ALLOWED_LANGUAGES"

### EXTRA_LANGUAGE_MODEL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LANGUAGE_MODEL: String
```

Informs the recognizer which speech model to prefer when performing [ACTION_RECOGNIZE_SPEECH](../android/speech/RecognizerIntent.md). The recognizer uses this information to fine tune the results. This extra is required. Activities implementing [ACTION_RECOGNIZE_SPEECH](../android/speech/RecognizerIntent.md) may interpret the values as they see fit. 

 Value: "android.speech.extra.LANGUAGE_MODEL"

**See Also**

- [#LANGUAGE_MODEL_FREE_FORM](../android/speech/RecognizerIntent.md)
- [#LANGUAGE_MODEL_WEB_SEARCH](../android/speech/RecognizerIntent.md) 

### EXTRA_LANGUAGE_PREFERENCE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LANGUAGE_PREFERENCE: String
```

The key to the extra in the [Bundle](../android/os/Bundle.md) returned by [ACTION_GET_LANGUAGE_DETAILS](../android/speech/RecognizerIntent.md) which is a [String](../java/lang/String.md) that represents the current language preference this user has specified - a locale string like "en-US". 

 Value: "android.speech.extra.LANGUAGE_PREFERENCE"

### EXTRA_LANGUAGE_SWITCH_ALLOWED_LANGUAGES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LANGUAGE_SWITCH_ALLOWED_LANGUAGES: String
```

Optional list of IETF language tags (as defined by BCP 47, e.g. "en-US", "de-DE"). This extra is to be used with [EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md). If set, the recognizer will apply the auto switch only to these languages, even if the speech models of other languages also exist. The corresponding language models must be downloaded to support the switch. Otherwise, the recognizer will report an error on a switch failure. 

 Value: "android.speech.extra.LANGUAGE_SWITCH_ALLOWED_LANGUAGES"

### EXTRA_LANGUAGE_SWITCH_INITIAL_ACTIVE_DURATION_TIME_MILLIS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LANGUAGE_SWITCH_INITIAL_ACTIVE_DURATION_TIME_MILLIS: String
```

Optional integer to use for [EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md). If set, the language switch will only be activated for this value of ms of audio since the START_OF_SPEECH. This could provide a more stable recognition result when the language switch is only required in the beginning of the session.

Depending on the recognizer implementation, this flag may have no effect. 

 Value: "android.speech.extra.LANGUAGE_SWITCH_INITIAL_ACTIVE_DURATION_TIME_MILLIS"

**See Also**

- [#EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md) 

### EXTRA_LANGUAGE_SWITCH_MAX_SWITCHES

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LANGUAGE_SWITCH_MAX_SWITCHES: String
```

Optional integer to use for [EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md). If set, the language switch will be deactivated when LANGUAGE_SWITCH_MAX_SWITCHES reached.

Depending on the recognizer implementation, this flag may have no effect. 

 Value: "android.speech.extra.LANGUAGE_SWITCH_MAX_SWITCHES"

**See Also**

- [#EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md) 

### EXTRA_MASK_OFFENSIVE_WORDS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_MASK_OFFENSIVE_WORDS: String
```

Optional boolean indicating whether the recognizer should mask the offensive words in recognition results. The Default is true. 

 Value: "android.speech.extra.MASK_OFFENSIVE_WORDS"

### EXTRA_MAX_RESULTS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_MAX_RESULTS: String
```

Optional limit on the maximum number of results to return. If omitted the recognizer will choose how many results to return. Must be an integer. 

 Value: "android.speech.extra.MAX_RESULTS"

### EXTRA_ONLY_RETURN_LANGUAGE_PREFERENCE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ONLY_RETURN_LANGUAGE_PREFERENCE: String
```

Specify this boolean extra in a broadcast of [ACTION_GET_LANGUAGE_DETAILS](../android/speech/RecognizerIntent.md) to indicate that only the current language preference is needed in the response. This avoids any additional computation if all you need is [EXTRA_LANGUAGE_PREFERENCE](../android/speech/RecognizerIntent.md) in the response. 

 Value: "android.speech.extra.ONLY_RETURN_LANGUAGE_PREFERENCE"

### EXTRA_ORIGIN

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ORIGIN: String
```

Optional value which can be used to indicate the referer url of a page in which speech was requested. For example, a web browser may choose to provide this for uses of speech on a given page. 

 Value: "android.speech.extra.ORIGIN"

### EXTRA_PARTIAL_RESULTS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PARTIAL_RESULTS: String
```

Optional boolean to indicate whether partial results should be returned by the recognizer as the user speaks (default is false). The server may ignore a request for partial results in some or all cases. 

 Value: "android.speech.extra.PARTIAL_RESULTS"

### EXTRA_PREFER_OFFLINE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PREFER_OFFLINE: String
```

Optional boolean, to be used with [ACTION_RECOGNIZE_SPEECH](../android/speech/RecognizerIntent.md), [ACTION_VOICE_SEARCH_HANDS_FREE](../android/speech/RecognizerIntent.md), [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md) to indicate whether to only use an offline speech recognition engine. The default is false, meaning that either network or offline recognition engines may be used.

Depending on the recognizer implementation, these values may have no effect. 

 Value: "android.speech.extra.PREFER_OFFLINE"

### EXTRA_PROMPT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PROMPT: String
```

Optional text prompt to show to the user when asking them to speak. 

 Value: "android.speech.extra.PROMPT"

### EXTRA_REQUEST_WORD_CONFIDENCE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_REQUEST_WORD_CONFIDENCE: String
```

Optional boolean indicating whether the recognizer should return the confidence level of each word in the final recognition results. 

 Value: "android.speech.extra.REQUEST_WORD_CONFIDENCE"

### EXTRA_REQUEST_WORD_TIMING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_REQUEST_WORD_TIMING: String
```

Optional boolean indicating whether the recognizer should return the timestamp of each word in the final recognition results. 

 Value: "android.speech.extra.REQUEST_WORD_TIMING"

### EXTRA_RESULTS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_RESULTS: String
```

An ArrayList\<String\> of the recognition results when performing [ACTION_RECOGNIZE_SPEECH](../android/speech/RecognizerIntent.md). Generally this list should be ordered in descending order of speech recognizer confidence. (See [EXTRA_CONFIDENCE_SCORES](../android/speech/RecognizerIntent.md)). Returned in the results; not to be specified in the recognition request. Only present when [Activity.RESULT_OK](../android/app/Activity.md) is returned in an activity result. In a PendingIntent, the lack of this extra indicates failure. 

 Value: "android.speech.extra.RESULTS"

### EXTRA_RESULTS_PENDINGINTENT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_RESULTS_PENDINGINTENT: String
```

When the intent is [ACTION_RECOGNIZE_SPEECH](../android/speech/RecognizerIntent.md), the speech input activity will return results to you via the activity results mechanism. Alternatively, if you use this extra to supply a PendingIntent, the results will be added to its bundle and the PendingIntent will be sent to its target. 

 Value: "android.speech.extra.RESULTS_PENDINGINTENT"

### EXTRA_RESULTS_PENDINGINTENT_BUNDLE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_RESULTS_PENDINGINTENT_BUNDLE: String
```

If you use [EXTRA_RESULTS_PENDINGINTENT](../android/speech/RecognizerIntent.md) to supply a forwarding intent, you can also use this extra to supply additional extras for the final intent. The search results will be added to this bundle, and the combined bundle will be sent to the target. 

 Value: "android.speech.extra.RESULTS_PENDINGINTENT_BUNDLE"

### EXTRA_SECURE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SECURE: String
```

Optional boolean to indicate that a "hands free" voice search was performed while the device was in a secure mode. An example of secure mode is when the device's screen lock is active, and it requires some form of authentication to be unlocked. When the device is securely locked, the voice search activity should either restrict the set of voice actions that are permitted, or require some form of secure authentication before proceeding. 

 Value: "android.speech.extras.EXTRA_SECURE"

### EXTRA_SEGMENTED_SESSION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SEGMENTED_SESSION: String
```

Optional string to enable segmented session mode of the specified type, which can be [EXTRA_AUDIO_SOURCE](../android/speech/RecognizerIntent.md), [EXTRA_SPEECH_INPUT_MINIMUM_LENGTH_MILLIS](../android/speech/RecognizerIntent.md) or [EXTRA_SPEECH_INPUT_COMPLETE_SILENCE_LENGTH_MILLIS](../android/speech/RecognizerIntent.md). When segmented session mode is supported by the recognizer implementation and this extra is set, it will return the recognition results in segments via [RecognitionListener.onSegmentResults(Bundle)](../android/speech/RecognitionListener.md))and terminate the session with [RecognitionListener.onEndOfSegmentedSession()](../android/speech/RecognitionListener.md)).

When setting this extra, make sure the extra used as the string value here is also set in the same intent with proper value.

Depending on the recognizer implementation, this value may have no effect. 

 Value: "android.speech.extra.SEGMENTED_SESSION"

**See Also**

- [#EXTRA_AUDIO_SOURCE](../android/speech/RecognizerIntent.md)
- [#EXTRA_SPEECH_INPUT_MINIMUM_LENGTH_MILLIS](../android/speech/RecognizerIntent.md)
- [#EXTRA_SPEECH_INPUT_COMPLETE_SILENCE_LENGTH_MILLIS](../android/speech/RecognizerIntent.md) 

### EXTRA_SPEECH_INPUT_COMPLETE_SILENCE_LENGTH_MILLIS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SPEECH_INPUT_COMPLETE_SILENCE_LENGTH_MILLIS: String
```

The amount of time that it should take after the recognizer stops hearing speech to consider the input complete hence end the recognition session.

Note that it is extremely rare you'd want to specify this value in an intent. Generally, it should be specified only when it is also used as the value for [EXTRA_SEGMENTED_SESSION](../android/speech/RecognizerIntent.md) to enable segmented session mode. Note also that certain values may cause undesired or unexpected results - use judiciously!

Depending on the recognizer implementation, these values may have no effect. 

 Value: "android.speech.extras.SPEECH_INPUT_COMPLETE_SILENCE_LENGTH_MILLIS"

### EXTRA_SPEECH_INPUT_MINIMUM_LENGTH_MILLIS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SPEECH_INPUT_MINIMUM_LENGTH_MILLIS: String
```

Optional integer to indicate the minimum length of the recognition session. The recognizer will not stop recognizing speech before this amount of time.

Note that it is extremely rare you'd want to specify this value in an intent. Generally, it should be specified only when it is also used as the value for [EXTRA_SEGMENTED_SESSION](../android/speech/RecognizerIntent.md) to enable segmented session mode. Note also that certain values may cause undesired or unexpected results - use judiciously!

Depending on the recognizer implementation, these values may have no effect. 

 Value: "android.speech.extras.SPEECH_INPUT_MINIMUM_LENGTH_MILLIS"

### EXTRA_SPEECH_INPUT_POSSIBLY_COMPLETE_SILENCE_LENGTH_MILLIS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SPEECH_INPUT_POSSIBLY_COMPLETE_SILENCE_LENGTH_MILLIS: String
```

The amount of time that it should take after we stop hearing speech to consider the input possibly complete. This is used to prevent the endpointer cutting off during very short mid-speech pauses. Note that it is extremely rare you'd want to specify this value in an intent. If you don't have a very good reason to change these, you should leave them as they are. Note also that certain values may cause undesired or unexpected results - use judiciously! Additionally, depending on the recognizer implementation, these values may have no effect. 

 Value: "android.speech.extras.SPEECH_INPUT_POSSIBLY_COMPLETE_SILENCE_LENGTH_MILLIS"

### EXTRA_SUPPORTED_LANGUAGES

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SUPPORTED_LANGUAGES: String
```

The key to the extra in the [Bundle](../android/os/Bundle.md) returned by [ACTION_GET_LANGUAGE_DETAILS](../android/speech/RecognizerIntent.md) which is an [ArrayList](../java/util/ArrayList.md) of [String](../java/lang/String.md) s that represents the languages supported by this implementation of voice recognition - a list of strings like "en-US", "cmn-Hans-CN", etc. 

 Value: "android.speech.extra.SUPPORTED_LANGUAGES"

### EXTRA_WEB_SEARCH_ONLY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_WEB_SEARCH_ONLY: String
```

Optional boolean, to be used with [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md), to indicate whether to only fire web searches in response to a user's speech. The default is false, meaning that other types of actions can be taken based on the user's speech. 

 Value: "android.speech.extra.WEB_SEARCH_ONLY"

### FORMATTING_OPTIMIZE_LATENCY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMATTING_OPTIMIZE_LATENCY: String
```

Optimizes formatting latency. This will result in a slightly lower quality of punctuation but can improve the experience for real-time use cases. This is a value to use for [EXTRA_ENABLE_FORMATTING](../android/speech/RecognizerIntent.md). 

 Value: "latency"

**See Also**

- [#EXTRA_ENABLE_FORMATTING](../android/speech/RecognizerIntent.md) 

### FORMATTING_OPTIMIZE_QUALITY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMATTING_OPTIMIZE_QUALITY: String
```

Optimizes formatting quality. This will increase latency but provide the highest punctuation quality. This is a value to use for [EXTRA_ENABLE_FORMATTING](../android/speech/RecognizerIntent.md). 

 Value: "quality"

**See Also**

- [#EXTRA_ENABLE_FORMATTING](../android/speech/RecognizerIntent.md) 

### LANGUAGE_MODEL_FREE_FORM

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LANGUAGE_MODEL_FREE_FORM: String
```

Use a language model based on free-form speech recognition. This is a value to use for [EXTRA_LANGUAGE_MODEL](../android/speech/RecognizerIntent.md). 

 Value: "free_form"

**See Also**

- [#EXTRA_LANGUAGE_MODEL](../android/speech/RecognizerIntent.md) 

### LANGUAGE_MODEL_WEB_SEARCH

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LANGUAGE_MODEL_WEB_SEARCH: String
```

Use a language model based on web search terms. This is a value to use for [EXTRA_LANGUAGE_MODEL](../android/speech/RecognizerIntent.md). 

 Value: "web_search"

**See Also**

- [#EXTRA_LANGUAGE_MODEL](../android/speech/RecognizerIntent.md) 

### LANGUAGE_SWITCH_BALANCED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LANGUAGE_SWITCH_BALANCED: String
```

A value to use for [EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md).

Enables language switch only when a new language is detected as at least [SpeechRecognizer.LANGUAGE_DETECTION_CONFIDENCE_LEVEL_CONFIDENT](../android/speech/SpeechRecognizer.md), which means the service is balancing between detecting a new language confidently and switching early. 

 Value: "balanced"

**See Also**

- [#EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md) 

### LANGUAGE_SWITCH_HIGH_PRECISION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LANGUAGE_SWITCH_HIGH_PRECISION: String
```

A value to use for [EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md).

Enables language switch only when a new language is detected as [SpeechRecognizer.LANGUAGE_DETECTION_CONFIDENCE_LEVEL_HIGHLY_CONFIDENT](../android/speech/SpeechRecognizer.md), which means the service may wait for longer before switching. 

 Value: "high_precision"

**See Also**

- [#EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md) 

### LANGUAGE_SWITCH_QUICK_RESPONSE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LANGUAGE_SWITCH_QUICK_RESPONSE: String
```

A value to use for [EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md).

Enables language switch only when a new language is detected as at least [SpeechRecognizer.LANGUAGE_DETECTION_CONFIDENCE_LEVEL_NOT_CONFIDENT](../android/speech/SpeechRecognizer.md), which means the service should switch at the earliest moment possible. 

 Value: "quick_response"

**See Also**

- [#EXTRA_ENABLE_LANGUAGE_SWITCH](../android/speech/RecognizerIntent.md) 

### RESULT_AUDIO_ERROR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_AUDIO_ERROR: Int
```

Result code returned when an audio error was encountered 

 Value: 5

### RESULT_CLIENT_ERROR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_CLIENT_ERROR: Int
```

Result code returned when there is a generic client error 

 Value: 2

### RESULT_NETWORK_ERROR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_NETWORK_ERROR: Int
```

Result code returned when a network error was encountered 

 Value: 4

### RESULT_NO_MATCH

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_NO_MATCH: Int
```

Result code returned when no matches are found for the given speech 

 Value: 1

### RESULT_SERVER_ERROR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_SERVER_ERROR: Int
```

Result code returned when the recognition server returns an error 

 Value: 3

## Public methods

### getVoiceDetailsIntent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getVoiceDetailsIntent(context: Context!): Intent!
```

Returns the broadcast intent to fire with [Context.sendOrderedBroadcast(Intent, String, BroadcastReceiver, android.os.Handler, int, String, Bundle)](../android/content/Context.md))to receive details from the package that implements voice search.

This is based on the value specified by the voice search [Activity](../android/app/Activity.md) in [DETAILS_META_DATA](../android/speech/RecognizerIntent.md), and if this is not specified, will return null. Also if there is no chosen default to resolve for [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md), this will return null.

If an intent is returned and is fired, a [Bundle](../android/os/Bundle.md) of extras will be returned to the provided result receiver, and should ideally contain values for [EXTRA_LANGUAGE_PREFERENCE](../android/speech/RecognizerIntent.md) and [EXTRA_SUPPORTED_LANGUAGES](../android/speech/RecognizerIntent.md).

(Whether these are actually provided is up to the particular implementation. It is recommended that [Activity](../android/app/Activity.md) s implementing [ACTION_WEB_SEARCH](../android/speech/RecognizerIntent.md) provide this information, but it is not required.)

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:a context object |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Intent](../android/content/Intent.md)! | the broadcast intent to fire or null if not available |
