# TextToSpeech

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextToSpeech

Kotlin| [Java](TextToSpeech.md) 
| --- | --- |

```
open class TextToSpeech
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.speech.tts.TextToSpeech](TextToSpeech.md) |

Synthesizes speech from text for immediate playback or to create a sound file.

A TextToSpeech instance can only be used to synthesize text once it has completed its initialization. Implement the [TextToSpeech.OnInitListener](../android/speech/tts/TextToSpeech.OnInitListener.md) to be notified of the completion of the initialization. 
When you are done using the TextToSpeech instance, call the [shutdown()](TextToSpeech.md))method to release the native resources used by the TextToSpeech engine. Apps targeting Android 11 that use text-to-speech should declare [android.speech.tts.TextToSpeech.Engine#INTENT_ACTION_TTS_SERVICE](../android/speech/tts/TextToSpeech.Engine.md) in the`queries`elements of their manifest: 

```kotlin
<queries>
    ...
   <intent>
       <action android:name="android.intent.action.TTS_SERVICE" />
   </intent>
  </queries>
  
```

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Engine](../android/speech/tts/TextToSpeech.Engine.md) Constants and parameter names for controlling text-to-speech. |
| open | [EngineInfo](../android/speech/tts/TextToSpeech.EngineInfo.md) Information about an installed text-to-speech engine. |
| abstract | [OnInitListener](../android/speech/tts/TextToSpeech.OnInitListener.md) Interface definition of a callback to be invoked indicating the completion of the TextToSpeech engine initialization. |
| --- | --- |
| abstract | [OnUtteranceCompletedListener](../android/speech/tts/TextToSpeech.OnUtteranceCompletedListener.md) Listener that will be called when the TTS service has completed synthesizing an utterance. |

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_TTS_QUEUE_PROCESSING_COMPLETED](TextToSpeech.md) Broadcast Action: The TextToSpeech synthesizer has completed processing of all the text in the speech queue. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) Denotes a generic operation failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_REQUEST](TextToSpeech.md) Denotes a failure caused by an invalid request. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NETWORK](TextToSpeech.md) Denotes a failure caused by a network connectivity problems. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NETWORK_TIMEOUT](TextToSpeech.md) Denotes a failure caused by network timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NOT_INSTALLED_YET](TextToSpeech.md) Denotes a failure caused by an unfinished download of the voice data. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_OUTPUT](TextToSpeech.md) Denotes a failure related to the output (audio device or a file). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SERVICE](TextToSpeech.md) Denotes a failure of a TTS service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SYNTHESIS](TextToSpeech.md) Denotes a failure of a TTS engine to synthesize the given input. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LANG_AVAILABLE](TextToSpeech.md) Denotes the language is available for the language by the locale, but not the country and variant. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LANG_COUNTRY_AVAILABLE](TextToSpeech.md) Denotes the language is available for the language and country specified by the locale, but not the variant. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LANG_COUNTRY_VAR_AVAILABLE](TextToSpeech.md) Denotes the language is available exactly as specified by the locale. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LANG_MISSING_DATA](TextToSpeech.md) Denotes the language data is missing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LANG_NOT_SUPPORTED](TextToSpeech.md) Denotes the language is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUEUE_ADD](TextToSpeech.md) Queue mode where the new entry is added at the end of the playback queue. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUEUE_FLUSH](TextToSpeech.md) Queue mode where all entries in the playback queue (media to be played and text to be synthesized) are dropped and replaced by the new entry. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOPPED](TextToSpeech.md) Denotes a stop requested by a client. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](TextToSpeech.md) Denotes a successful operation. |
| --- | --- |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TextToSpeech](TextToSpeech.md))`(`context:` ` [Context](../android.content/Context.md)!`, `listener:` ` [TextToSpeech.OnInitListener](../android/speech/tts/TextToSpeech.OnInitListener.md)!`)` The constructor for the TextToSpeech class, using the default TTS engine. |
| [TextToSpeech](TextToSpeech.md))`(`context:` ` [Context](../android.content/Context.md)!`, `listener:` ` [TextToSpeech.OnInitListener](../android/speech/tts/TextToSpeech.OnInitListener.md)!`, `engine:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The constructor for the TextToSpeech class, using the given TTS engine. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addEarcon](TextToSpeech.md))`(`earcon:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `uri:` ` [Uri](../android.net/Uri.md)`)` Adds a mapping between a string of text and a sound file. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addEarcon](TextToSpeech.md))`(`earcon:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `file:` ` [File](../java.io/File.md)!`)` Adds a mapping between a string of text and a sound file. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addEarcon](TextToSpeech.md))`(`earcon:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `filename:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adds a mapping between a string of text and a sound file. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addEarcon](TextToSpeech.md))`(`earcon:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `packagename:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds a mapping between a string of text and a sound resource in a package. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addSpeech](TextToSpeech.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `uri:` ` [Uri](../android.net/Uri.md)`)` Adds a mapping between a CharSequence (may be spanned with TtsSpans) and a sound file. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addSpeech](TextToSpeech.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `file:` ` [File](../java.io/File.md)!`)` Adds a mapping between a CharSequence (may be spanned with TtsSpans) and a sound file. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addSpeech](TextToSpeech.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `packagename:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds a mapping between a CharSequence (may be spanned with TtsSpans) of text and a sound resource in a package. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addSpeech](TextToSpeech.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `filename:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adds a mapping between a string of text and a sound file. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addSpeech](TextToSpeech.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `packagename:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds a mapping between a string of text and a sound resource in a package. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areDefaultsEnforced](TextToSpeech.md))`()` Checks whether the user's settings should override settings requested by the calling application. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Locale](../java.util/Locale.md)!\>! | [getAvailableLanguages](TextToSpeech.md))`()` Query the engine about the set of available languages. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultEngine](TextToSpeech.md))`()` Gets the package name of the default speech synthesis engine. |
| --- | --- |
| open [Locale](../java.util/Locale.md)! | [getDefaultLanguage](TextToSpeech.md))`()` Returns a Locale instance describing the language currently being used as the default Text-to-speech language. |
| open [Voice](Voice.md)! | [getDefaultVoice](TextToSpeech.md))`()` Returns a Voice instance that's the default voice for the default Text-to-speech language. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TextToSpeech.EngineInfo](../android/speech/tts/TextToSpeech.EngineInfo.md)!\>! | [getEngines](TextToSpeech.md))`()` Gets a list of all installed TTS engines. |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getFeatures](TextToSpeech.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`)` Queries the engine for the set of features it supports for a given locale. |
| open [Locale](../java.util/Locale.md)! | [getLanguage](TextToSpeech.md))`()` Returns a Locale instance describing the language currently being used for synthesis requests sent to the TextToSpeech engine. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSpeechInputLength](TextToSpeech.md))`()` Limit of length of input string passed to speak and synthesizeToFile. |
| --- | --- |
| open [Voice](Voice.md)! | [getVoice](TextToSpeech.md))`()` Returns a Voice instance describing the voice currently being used for synthesis requests sent to the TextToSpeech engine. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Voice](Voice.md)!\>! | [getVoices](TextToSpeech.md))`()` Query the engine about the set of available voices. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [isLanguageAvailable](TextToSpeech.md))`(`loc:` ` [Locale](../java.util/Locale.md)!`)` Checks if the specified language as represented by the Locale is available and supported. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpeaking](TextToSpeech.md))`()` Checks whether the TTS engine is busy speaking. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [playEarcon](TextToSpeech.md))`(`earcon:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `queueMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [Bundle](../android.os/Bundle.md)!`, `utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Plays the earcon using the specified queueing mode and parameters. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [playEarcon](TextToSpeech.md))`(`earcon:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `queueMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [HashMap](../java.util/HashMap.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Plays the earcon using the specified queueing mode and parameters. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [playSilence](TextToSpeech.md))`(`durationInMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `queueMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [HashMap](../java.util/HashMap.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Plays silence for the specified amount of time using the specified queue mode. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [playSilentUtterance](TextToSpeech.md))`(`durationInMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `queueMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Plays silence for the specified amount of time using the specified queue mode. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setAudioAttributes](TextToSpeech.md))`(`audioAttributes:` ` [AudioAttributes](../android.media/AudioAttributes.md)!`)` Sets the audio attributes to be used when speaking text or playing back a file. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setEngineByPackageName](TextToSpeech.md))`(`enginePackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the TTS engine to use. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setLanguage](TextToSpeech.md))`(`loc:` ` [Locale](../java.util/Locale.md)!`)` Sets the text-to-speech language. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setOnUtteranceCompletedListener](TextToSpeech.md))`(`listener:` ` [TextToSpeech.OnUtteranceCompletedListener](../android/speech/tts/TextToSpeech.OnUtteranceCompletedListener.md)!`)` Sets the listener that will be notified when synthesis of an utterance completes. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setOnUtteranceProgressListener](TextToSpeech.md))`(`listener:` ` [UtteranceProgressListener](UtteranceProgressListener.md)!`)` Sets the listener that will be notified of various events related to the synthesis of a given utterance. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setPitch](TextToSpeech.md))`(`pitch:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the speech pitch for the TextToSpeech engine. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setSpeechRate](TextToSpeech.md))`(`speechRate:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the speech rate. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setVoice](TextToSpeech.md))`(`voice:` ` [Voice](Voice.md)!`)` Sets the text-to-speech voice. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](TextToSpeech.md))`()` Releases the resources used by the TextToSpeech engine. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [speak](TextToSpeech.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `queueMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [Bundle](../android.os/Bundle.md)!`, `utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Speaks the text using the specified queuing strategy and speech parameters, the text may be spanned with TtsSpans. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [speak](TextToSpeech.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `queueMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [HashMap](../java.util/HashMap.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Speaks the string using the specified queuing strategy and speech parameters. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [stop](TextToSpeech.md))`()` Interrupts the current utterance (whether played or rendered to file) and discards other utterances in the queue. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [synthesizeToFile](TextToSpeech.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `params:` ` [Bundle](../android.os/Bundle.md)`, `fileDescriptor:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)`, `utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Synthesizes the given text to a ParcelFileDescriptor using the specified parameters. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [synthesizeToFile](TextToSpeech.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `params:` ` [Bundle](../android.os/Bundle.md)!`, `file:` ` [File](../java.io/File.md)!`, `utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Synthesizes the given text to a file using the specified parameters. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [synthesizeToFile](TextToSpeech.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [HashMap](../java.util/HashMap.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `filename:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Synthesizes the given text to a file using the specified parameters. |

## Constants

### ACTION_TTS_QUEUE_PROCESSING_COMPLETED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_TTS_QUEUE_PROCESSING_COMPLETED: String
```

Broadcast Action: The TextToSpeech synthesizer has completed processing of all the text in the speech queue. Note that this notifies callers when the**engine** has finished has processing text data. Audio playback might not have completed (or even started) at this point. If you wish to be notified when this happens, see [OnUtteranceCompletedListener](../android/speech/tts/TextToSpeech.OnUtteranceCompletedListener.md). 

 Value: "android.speech.tts.TTS_QUEUE_PROCESSING_COMPLETED"

### ERROR

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR: Int
```

Denotes a generic operation failure. 

 Value: -1

### ERROR_INVALID_REQUEST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_REQUEST: Int
```

Denotes a failure caused by an invalid request. 

 Value: -8

### ERROR_NETWORK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NETWORK: Int
```

Denotes a failure caused by a network connectivity problems. 

 Value: -6

### ERROR_NETWORK_TIMEOUT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NETWORK_TIMEOUT: Int
```

Denotes a failure caused by network timeout. 

 Value: -7

### ERROR_NOT_INSTALLED_YET

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NOT_INSTALLED_YET: Int
```

Denotes a failure caused by an unfinished download of the voice data. 

 Value: -9

**See Also**

- [android.speech.tts.TextToSpeech.Engine#KEY_FEATURE_NOT_INSTALLED](../android/speech/tts/TextToSpeech.Engine.md) 

### ERROR_OUTPUT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_OUTPUT: Int
```

Denotes a failure related to the output (audio device or a file). 

 Value: -5

### ERROR_SERVICE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_SERVICE: Int
```

Denotes a failure of a TTS service. 

 Value: -4

### ERROR_SYNTHESIS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_SYNTHESIS: Int
```

Denotes a failure of a TTS engine to synthesize the given input. 

 Value: -3

### LANG_AVAILABLE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LANG_AVAILABLE: Int
```

Denotes the language is available for the language by the locale, but not the country and variant. 

 Value: 0

### LANG_COUNTRY_AVAILABLE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LANG_COUNTRY_AVAILABLE: Int
```

Denotes the language is available for the language and country specified by the locale, but not the variant. 

 Value: 1

### LANG_COUNTRY_VAR_AVAILABLE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LANG_COUNTRY_VAR_AVAILABLE: Int
```

Denotes the language is available exactly as specified by the locale. 

 Value: 2

### LANG_MISSING_DATA

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LANG_MISSING_DATA: Int
```

Denotes the language data is missing. 

 Value: -1

### LANG_NOT_SUPPORTED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LANG_NOT_SUPPORTED: Int
```

Denotes the language is not supported. 

 Value: -2

### QUEUE_ADD

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUEUE_ADD: Int
```

Queue mode where the new entry is added at the end of the playback queue. 

 Value: 1

### QUEUE_FLUSH

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUEUE_FLUSH: Int
```

Queue mode where all entries in the playback queue (media to be played and text to be synthesized) are dropped and replaced by the new entry. Queues are flushed with respect to a given calling app. Entries in the queue from other callees are not discarded. 

 Value: 0

### STOPPED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOPPED: Int
```

Denotes a stop requested by a client. It's used only on the service side of the API, client should never expect to see this result code. 

 Value: -2

### SUCCESS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUCCESS: Int
```

Denotes a successful operation. 

 Value: 0

## Public constructors

### TextToSpeech

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextToSpeech(
    context: Context!, 
    listener: TextToSpeech.OnInitListener!)
```

The constructor for the TextToSpeech class, using the default TTS engine. This will also initialize the associated TextToSpeech engine if it isn't already running.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The context this instance is running in. |
| `listener` | [TextToSpeech.OnInitListener](../android/speech/tts/TextToSpeech.OnInitListener.md)!:The [TextToSpeech.OnInitListener](../android/speech/tts/TextToSpeech.OnInitListener.md) that will be called when the TextToSpeech engine has initialized. In a case of a failure the listener may be called immediately, before TextToSpeech instance is fully constructed. |

### TextToSpeech

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextToSpeech(
    context: Context!, 
    listener: TextToSpeech.OnInitListener!, 
    engine: String!)
```

The constructor for the TextToSpeech class, using the given TTS engine. This will also initialize the associated TextToSpeech engine if it isn't already running.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The context this instance is running in. |
| `listener` | [TextToSpeech.OnInitListener](../android/speech/tts/TextToSpeech.OnInitListener.md)!:The [TextToSpeech.OnInitListener](../android/speech/tts/TextToSpeech.OnInitListener.md) that will be called when the TextToSpeech engine has initialized. In a case of a failure the listener may be called immediately, before TextToSpeech instance is fully constructed. |
| `engine` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Package name of the TTS engine to use. |
| --- | --- |

## Public methods

### addEarcon

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addEarcon(
    earcon: String, 
    uri: Uri
): Int
```

Adds a mapping between a string of text and a sound file. Use this to add custom earcons.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `earcon` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the earcon. Example:`"[tick]"`This value cannot be`null`. |
| `uri` | [Uri](../android.net/Uri.md):Uri object pointing to the sound file. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Code indicating success or failure. See [ERROR](TextToSpeech.md) and [SUCCESS](TextToSpeech.md). |

**See Also**

- [#playEarcon(String, int, HashMap)](TextToSpeech.md)) 

### addEarcon

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addEarcon(
    earcon: String!, 
    file: File!
): Int
```

Adds a mapping between a string of text and a sound file. Use this to add custom earcons.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `earcon` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the earcon. Example:`"[tick]"` |
| `file` | [File](../java.io/File.md)!:File object pointing to the sound file. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Code indicating success or failure. See [ERROR](TextToSpeech.md) and [SUCCESS](TextToSpeech.md). |

**See Also**

- [#playEarcon(String, int, HashMap)](TextToSpeech.md)) 

### addEarcon

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addEarcon(
    earcon: String!, 
    filename: String!
): Int
```

**Deprecated:** *As of API level 21, replaced by [addEarcon(java.lang.String,java.io.File)](TextToSpeech.md)).*

Adds a mapping between a string of text and a sound file. Use this to add custom earcons.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `earcon` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the earcon. Example:`"[tick]"` |
| `filename` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The full path to the sound file (for example: "/sdcard/mysounds/tick.wav") |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Code indicating success or failure. See [ERROR](TextToSpeech.md) and [SUCCESS](TextToSpeech.md). |

**See Also**

- [#playEarcon(String, int, HashMap)](TextToSpeech.md)) 

### addEarcon

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addEarcon(
    earcon: String!, 
    packagename: String!, 
    resourceId: Int
): Int
```

Adds a mapping between a string of text and a sound resource in a package. Use this to add custom earcons.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `earcon` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the earcon. Example:`"[tick]"` |
| `packagename` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the package name of the application that contains the resource. This can for instance be the package name of your own application. Example:**"com.google.marvin.compass"** The package name can be found in the AndroidManifest.xml of the application containing the resource. `<manifest xmlns:android="..." package="`**com.google.marvin.compass**`">` |
| `resourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Example:`R.raw.tick_snd` |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Code indicating success or failure. See [ERROR](TextToSpeech.md) and [SUCCESS](TextToSpeech.md). |

**See Also**

- [#playEarcon(String, int, HashMap)](TextToSpeech.md)) 

### addSpeech

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addSpeech(
    text: CharSequence, 
    uri: Uri
): Int
```

Adds a mapping between a CharSequence (may be spanned with TtsSpans) and a sound file. Using this, it is possible to add custom pronounciations for a string of text. After a call to this method, subsequent calls to [speak(java.lang.CharSequence,int,android.os.Bundle,java.lang.String)](TextToSpeech.md))will play the specified sound resource if it is available, or synthesize the text it is missing.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):The string of text. Example:`"south_south_east"`This value cannot be`null`. |
| `uri` | [Uri](../android.net/Uri.md):Uri object pointing to the sound file. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Code indicating success or failure. See [ERROR](TextToSpeech.md) and [SUCCESS](TextToSpeech.md). |

### addSpeech

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addSpeech(
    text: CharSequence!, 
    file: File!
): Int
```

Adds a mapping between a CharSequence (may be spanned with TtsSpans) and a sound file. Using this, it is possible to add custom pronounciations for a string of text. After a call to this method, subsequent calls to [speak(java.lang.CharSequence,int,android.os.Bundle,java.lang.String)](TextToSpeech.md))will play the specified sound resource if it is available, or synthesize the text it is missing.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The string of text. Example:`"south_south_east"` |
| `file` | [File](../java.io/File.md)!:File object pointing to the sound file. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Code indicating success or failure. See [ERROR](TextToSpeech.md) and [SUCCESS](TextToSpeech.md). |

### addSpeech

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addSpeech(
    text: CharSequence!, 
    packagename: String!, 
    resourceId: Int
): Int
```

Adds a mapping between a CharSequence (may be spanned with TtsSpans) of text and a sound resource in a package. After a call to this method, subsequent calls to [speak(java.lang.CharSequence,int,android.os.Bundle,java.lang.String)](TextToSpeech.md))will play the specified sound resource if it is available, or synthesize the text it is missing.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The string of text. Example:`"south_south_east"` |
| `packagename` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Pass the packagename of the application that contains the resource. If the resource is in your own application (this is the most common case), then put the packagename of your application here. Example:**"com.google.marvin.compass"** The packagename can be found in the AndroidManifest.xml of your application. `<manifest xmlns:android="..." package="`**com.google.marvin.compass**`">` |
| `resourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Example:`R.raw.south_south_east` |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Code indicating success or failure. See [ERROR](TextToSpeech.md) and [SUCCESS](TextToSpeech.md). |

### addSpeech

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addSpeech(
    text: String!, 
    filename: String!
): Int
```

Adds a mapping between a string of text and a sound file. Using this, it is possible to add custom pronounciations for a string of text. After a call to this method, subsequent calls to [speak(java.lang.CharSequence,int,android.os.Bundle,java.lang.String)](TextToSpeech.md))will play the specified sound resource if it is available, or synthesize the text it is missing.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The string of text. Example:`"south_south_east"` |
| `filename` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The full path to the sound file (for example: "/sdcard/mysounds/hello.wav") |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Code indicating success or failure. See [ERROR](TextToSpeech.md) and [SUCCESS](TextToSpeech.md). |

### addSpeech

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addSpeech(
    text: String!, 
    packagename: String!, 
    resourceId: Int
): Int
```

Adds a mapping between a string of text and a sound resource in a package. After a call to this method, subsequent calls to [speak(java.lang.CharSequence,int,android.os.Bundle,java.lang.String)](TextToSpeech.md))will play the specified sound resource if it is available, or synthesize the text it is missing.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The string of text. Example:`"south_south_east"` |
| `packagename` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Pass the packagename of the application that contains the resource. If the resource is in your own application (this is the most common case), then put the packagename of your application here. Example:**"com.google.marvin.compass"** The packagename can be found in the AndroidManifest.xml of your application. `<manifest xmlns:android="..." package="`**com.google.marvin.compass**`">` |
| `resourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Example:`R.raw.south_south_east` |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Code indicating success or failure. See [ERROR](TextToSpeech.md) and [SUCCESS](TextToSpeech.md). |

### areDefaultsEnforced

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun areDefaultsEnforced(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether the user's settings should override settings requested by the calling application. As of the Ice cream sandwich release, user settings never forcibly override the app's settings. 

### getAvailableLanguages

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAvailableLanguages(): MutableSet<Locale!>!
```

Query the engine about the set of available languages. 

### getDefaultEngine

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDefaultEngine(): String!
```

Gets the package name of the default speech synthesis engine.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Package name of the TTS engine that the user has chosen as their default. |

### getDefaultLanguage

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDefaultLanguage(): Locale!
```

**Deprecated:** *As of API level 21, use`getDefaultVoice().getLocale()`([getDefaultVoice()](TextToSpeech.md)))*

Returns a Locale instance describing the language currently being used as the default Text-to-speech language. The locale object returned by this method is NOT a valid one. It has identical form to the one in [getLanguage()](TextToSpeech.md)). Please refer to [getLanguage()](TextToSpeech.md))for more information.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Locale](../java.util/Locale.md)! | language, country (if any) and variant (if any) used by the client stored in a Locale instance, or`null`on error. |

### getDefaultVoice

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDefaultVoice(): Voice!
```

Returns a Voice instance that's the default voice for the default Text-to-speech language.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Voice](Voice.md)! | The default voice instance for the default language, or`null`if not set or on error. |

### getEngines

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEngines(): MutableList<TextToSpeech.EngineInfo!>!
```

Gets a list of all installed TTS engines.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TextToSpeech.EngineInfo](../android/speech/tts/TextToSpeech.EngineInfo.md)!>! | A list of engine info objects. The list can be empty, but never`null`. |

### getFeatures

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFeatures(locale: Locale!): MutableSet<String!>!
```

**Deprecated:** *As of API level 21, please use voices. In order to query features of the voice, call [getVoices()](TextToSpeech.md))to retrieve the list of available voices and [Voice.getFeatures()](Voice.md))to retrieve the set of features.*

Queries the engine for the set of features it supports for a given locale. Features can either be framework defined, e.g. [TextToSpeech.Engine.KEY_FEATURE_NETWORK_SYNTHESIS](../android/speech/tts/TextToSpeech.Engine.md) or engine specific. Engine specific keys must be prefixed by the name of the engine they are intended for. These keys can be used as parameters to [TextToSpeech.speak(String, int, java.util.HashMap)](TextToSpeech.md))and [TextToSpeech.synthesizeToFile(String, java.util.HashMap, String)](TextToSpeech.md)). Features values are strings and their values must meet restrictions described in their documentation.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:The locale to query features for. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | Set instance. May return`null`on error. |

### getLanguage

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLanguage(): Locale!
```

**Deprecated:** *As of API level 21, please use`getVoice().getLocale()`([getVoice()](TextToSpeech.md))).*

Returns a Locale instance describing the language currently being used for synthesis requests sent to the TextToSpeech engine. In Android 4.2 and before (API \<= 17) this function returns the language that is currently being used by the TTS engine. That is the last language set by this or any other client by a [TextToSpeech.setLanguage](TextToSpeech.md))call to the same engine. In Android versions after 4.2 this function returns the language that is currently being used for the synthesis requests sent from this client. That is the last language set by a [TextToSpeech.setLanguage](TextToSpeech.md))call on this instance. If a voice is set (by [setVoice(android.speech.tts.Voice)](TextToSpeech.md))), getLanguage will return the language of the currently set voice. Please note that the Locale object returned by this method is NOT a valid Locale object. Its language field contains a three-letter ISO 639-2/T code (where a proper Locale would use a two-letter ISO 639-1 code), and the country field contains a three-letter ISO 3166 country code (where a proper Locale would use a two-letter ISO 3166-1 code).

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Locale](../java.util/Locale.md)! | language, country (if any) and variant (if any) used by the client stored in a Locale instance, or`null`on error. |

### getMaxSpeechInputLength

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMaxSpeechInputLength(): Int
```

Limit of length of input string passed to speak and synthesizeToFile. 
**See Also**

### getVoice

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVoice(): Voice!
```

Returns a Voice instance describing the voice currently being used for synthesis requests sent to the TextToSpeech engine.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Voice](Voice.md)! | Voice instance used by the client, or`null`if not set or on error. |

**See Also**

- [#getVoices](TextToSpeech.md))
- [#setVoice](TextToSpeech.md))
- [android.speech.tts.Voice](Voice.md) 

### getVoices

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVoices(): MutableSet<Voice!>!
```

Query the engine about the set of available voices. Each TTS Engine can expose multiple voices for each locale, each with a different set of features. 
**See Also**

- [#setVoice(Voice)](TextToSpeech.md))
- [android.speech.tts.Voice](Voice.md) 

### isLanguageAvailable

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLanguageAvailable(loc: Locale!): Int
```

Checks if the specified language as represented by the Locale is available and supported.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------|
| `loc` | [Locale](../java.util/Locale.md)!:The Locale describing the language to be used. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Code indicating the support status for the locale. See [LANG_AVAILABLE](TextToSpeech.md), [LANG_COUNTRY_AVAILABLE](TextToSpeech.md), [LANG_COUNTRY_VAR_AVAILABLE](TextToSpeech.md), [LANG_MISSING_DATA](TextToSpeech.md) and [LANG_NOT_SUPPORTED](TextToSpeech.md). |

### isSpeaking

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSpeaking(): Boolean
```

Checks whether the TTS engine is busy speaking. Note that a speech item is considered complete once it's audio data has been sent to the audio mixer, or written to a file. There might be a finite lag between this point, and when the audio hardware completes playback.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the TTS engine is speaking. |

### playEarcon

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun playEarcon(
    earcon: String!, 
    queueMode: Int, 
    params: Bundle!, 
    utteranceId: String!
): Int
```

Plays the earcon using the specified queueing mode and parameters. The earcon must already have been added with [addEarcon(java.lang.String,java.lang.String)](TextToSpeech.md))or [addEarcon(java.lang.String,java.lang.String,int)](TextToSpeech.md)). This method is asynchronous, i.e. the method just adds the request to the queue of TTS requests and then returns. The synthesis might not have finished (or even started!) at the time when this method returns. In order to reliably detect errors during synthesis, we recommend setting an utterance progress listener (see [setOnUtteranceProgressListener](TextToSpeech.md))) and using the [Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md) parameter.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `earcon` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The earcon that should be played |
| `queueMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): [QUEUE_ADD](TextToSpeech.md) or [QUEUE_FLUSH](TextToSpeech.md). |
| `params` | [Bundle](../android.os/Bundle.md)!:Parameters for the request. Can be null. Supported parameter names: [Engine.KEY_PARAM_STREAM](../android/speech/tts/TextToSpeech.Engine.md), Engine specific parameters may be passed in but the parameter keys must be prefixed by the name of the engine they are intended for. For example the keys "com.svox.pico_foo" and "com.svox.pico:bar" will be passed to the engine named "com.svox.pico" if it is being used. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md) of**queuing**the playEarcon operation. |

### playEarcon

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun playEarcon(
    earcon: String!, 
    queueMode: Int, 
    params: HashMap<String!, String!>!
): Int
```

**Deprecated:** *As of API level 21, replaced by [playEarcon(java.lang.String,int,android.os.Bundle,java.lang.String)](TextToSpeech.md)).*

Plays the earcon using the specified queueing mode and parameters. The earcon must already have been added with [addEarcon(java.lang.String,java.lang.String)](TextToSpeech.md))or [addEarcon(java.lang.String,java.lang.String,int)](TextToSpeech.md)). This method is asynchronous, i.e. the method just adds the request to the queue of TTS requests and then returns. The synthesis might not have finished (or even started!) at the time when this method returns. In order to reliably detect errors during synthesis, we recommend setting an utterance progress listener (see [setOnUtteranceProgressListener](TextToSpeech.md))) and using the [Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md) parameter.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `earcon` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The earcon that should be played |
| `queueMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): [QUEUE_ADD](TextToSpeech.md) or [QUEUE_FLUSH](TextToSpeech.md). |
| `params` | [HashMap](../java.util/HashMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Parameters for the request. Can be null. Supported parameter names: [Engine.KEY_PARAM_STREAM](../android/speech/tts/TextToSpeech.Engine.md), [Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md). Engine specific parameters may be passed in but the parameter keys must be prefixed by the name of the engine they are intended for. For example the keys "com.svox.pico_foo" and "com.svox.pico:bar" will be passed to the engine named "com.svox.pico" if it is being used. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md) of**queuing**the playEarcon operation. |

### playSilence

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun playSilence(
    durationInMs: Long, 
    queueMode: Int, 
    params: HashMap<String!, String!>!
): Int
```

**Deprecated:** *As of API level 21, replaced by [playSilentUtterance(long,int,java.lang.String)](TextToSpeech.md)).*

Plays silence for the specified amount of time using the specified queue mode. This method is asynchronous, i.e. the method just adds the request to the queue of TTS requests and then returns. The synthesis might not have finished (or even started!) at the time when this method returns. In order to reliably detect errors during synthesis, we recommend setting an utterance progress listener (see [setOnUtteranceProgressListener](TextToSpeech.md))) and using the [Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md) parameter.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `durationInMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The duration of the silence. |
| `queueMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): [QUEUE_ADD](TextToSpeech.md) or [QUEUE_FLUSH](TextToSpeech.md). |
| `params` | [HashMap](../java.util/HashMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Parameters for the request. Can be null. Supported parameter names: [Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md). Engine specific parameters may be passed in but the parameter keys must be prefixed by the name of the engine they are intended for. For example the keys "com.svox.pico_foo" and "com.svox.pico:bar" will be passed to the engine named "com.svox.pico" if it is being used. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md) of**queuing**the playSilence operation. |

### playSilentUtterance

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun playSilentUtterance(
    durationInMs: Long, 
    queueMode: Int, 
    utteranceId: String!
): Int
```

Plays silence for the specified amount of time using the specified queue mode. This method is asynchronous, i.e. the method just adds the request to the queue of TTS requests and then returns. The synthesis might not have finished (or even started!) at the time when this method returns. In order to reliably detect errors during synthesis, we recommend setting an utterance progress listener (see [setOnUtteranceProgressListener](TextToSpeech.md))) and using the [Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md) parameter.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `durationInMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The duration of the silence. |
| `queueMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): [QUEUE_ADD](TextToSpeech.md) or [QUEUE_FLUSH](TextToSpeech.md). |
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:An unique identifier for this request. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md) of**queuing**the playSilentUtterance operation. |

### setAudioAttributes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAudioAttributes(audioAttributes: AudioAttributes!): Int
```

Sets the audio attributes to be used when speaking text or playing back a file.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `audioAttributes` | [AudioAttributes](../android.media/AudioAttributes.md)!:Valid AudioAttributes instance. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md). |

### setEngineByPackageName

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEngineByPackageName(enginePackageName: String!): Int
```

**Deprecated:** *This doesn't inform callers when the TTS engine has been initialized. [TextToSpeech(android.content.Context,android.speech.tts.TextToSpeech.OnInitListener,java.lang.String)](TextToSpeech.md))can be used with the appropriate engine name. Also, there is no guarantee that the engine specified will be loaded. If it isn't installed or disabled, the user / system wide defaults will apply.*

Sets the TTS engine to use.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `enginePackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package name for the synthesis engine (e.g. "com.svox.pico") |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md). |

### setLanguage

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLanguage(loc: Locale!): Int
```

Sets the text-to-speech language. The TTS engine will try to use the closest match to the specified language as represented by the Locale, but there is no guarantee that the exact same Locale will be used. Use [isLanguageAvailable(java.util.Locale)](TextToSpeech.md))to check the level of support before choosing the language to use for the next utterances. This method sets the current voice to the default one for the given Locale; [getVoice()](TextToSpeech.md))can be used to retrieve it.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------|
| `loc` | [Locale](../java.util/Locale.md)!:The locale describing the language to be used. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Code indicating the support status for the locale. See [LANG_AVAILABLE](TextToSpeech.md), [LANG_COUNTRY_AVAILABLE](TextToSpeech.md), [LANG_COUNTRY_VAR_AVAILABLE](TextToSpeech.md), [LANG_MISSING_DATA](TextToSpeech.md) and [LANG_NOT_SUPPORTED](TextToSpeech.md). |

### setOnUtteranceCompletedListener

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnUtteranceCompletedListener(listener: TextToSpeech.OnUtteranceCompletedListener!): Int
```

**Deprecated:** *Use [setOnUtteranceProgressListener(android.speech.tts.UtteranceProgressListener)](TextToSpeech.md))instead.*

Sets the listener that will be notified when synthesis of an utterance completes.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [TextToSpeech.OnUtteranceCompletedListener](../android/speech/tts/TextToSpeech.OnUtteranceCompletedListener.md)!:The listener to use. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md). |

### setOnUtteranceProgressListener

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnUtteranceProgressListener(listener: UtteranceProgressListener!): Int
```

Sets the listener that will be notified of various events related to the synthesis of a given utterance. See [UtteranceProgressListener](UtteranceProgressListener.md) and [TextToSpeech.Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [UtteranceProgressListener](UtteranceProgressListener.md)!:the listener to use. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md) |

### setPitch

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPitch(pitch: Float): Int
```

Sets the speech pitch for the TextToSpeech engine. This has no effect on any pre-recorded speech.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pitch` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Speech pitch.`1.0`is the normal pitch, lower values lower the tone of the synthesized voice, greater values increase it. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md). |

### setSpeechRate

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSpeechRate(speechRate: Float): Int
```

Sets the speech rate. This has no effect on any pre-recorded speech.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `speechRate` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Speech rate.`1.0`is the normal speech rate, lower values slow down the speech (`0.5`is half the normal speech rate), greater values accelerate it (`2.0`is twice the normal speech rate). |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md). |

### setVoice

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVoice(voice: Voice!): Int
```

Sets the text-to-speech voice.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `voice` | [Voice](Voice.md)!:One of objects returned by [getVoices()](TextToSpeech.md)). |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md). |

**See Also**

- [#getVoices](TextToSpeech.md))
- [android.speech.tts.Voice](Voice.md) 

### shutdown

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shutdown(): Unit
```

Releases the resources used by the TextToSpeech engine. It is good practice for instance to call this method in the onDestroy() method of an Activity so the TextToSpeech engine can be cleanly stopped. 

### speak

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun speak(
    text: CharSequence!, 
    queueMode: Int, 
    params: Bundle!, 
    utteranceId: String!
): Int
```

Speaks the text using the specified queuing strategy and speech parameters, the text may be spanned with TtsSpans. This method is asynchronous, i.e. the method just adds the request to the queue of TTS requests and then returns. The synthesis might not have finished (or even started!) at the time when this method returns. In order to reliably detect errors during synthesis, we recommend setting an utterance progress listener (see [setOnUtteranceProgressListener](TextToSpeech.md))) and using the [Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md) parameter.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The string of text to be spoken. No longer than [getMaxSpeechInputLength()](TextToSpeech.md))characters. |
| `queueMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The queuing strategy to use, [QUEUE_ADD](TextToSpeech.md) or [QUEUE_FLUSH](TextToSpeech.md). |
| `params` | [Bundle](../android.os/Bundle.md)!:Parameters for the request. Can be null. Supported parameter names: [Engine.KEY_PARAM_STREAM](../android/speech/tts/TextToSpeech.Engine.md), [Engine.KEY_PARAM_VOLUME](../android/speech/tts/TextToSpeech.Engine.md), [Engine.KEY_PARAM_PAN](../android/speech/tts/TextToSpeech.Engine.md). Engine specific parameters may be passed in but the parameter keys must be prefixed by the name of the engine they are intended for. For example the keys "com.svox.pico_foo" and "com.svox.pico:bar" will be passed to the engine named "com.svox.pico" if it is being used. |
| --- | --- |
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:An unique identifier for this request. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md) of**queuing**the speak operation. |

### speak

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun speak(
    text: String!, 
    queueMode: Int, 
    params: HashMap<String!, String!>!
): Int
```

**Deprecated:** *As of API level 21, replaced by [speak(java.lang.CharSequence,int,android.os.Bundle,java.lang.String)](TextToSpeech.md)).*

Speaks the string using the specified queuing strategy and speech parameters. This method is asynchronous, i.e. the method just adds the request to the queue of TTS requests and then returns. The synthesis might not have finished (or even started!) at the time when this method returns. In order to reliably detect errors during synthesis, we recommend setting an utterance progress listener (see [setOnUtteranceProgressListener](TextToSpeech.md))) and using the [Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md) parameter.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The string of text to be spoken. No longer than [getMaxSpeechInputLength()](TextToSpeech.md))characters. |
| `queueMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The queuing strategy to use, [QUEUE_ADD](TextToSpeech.md) or [QUEUE_FLUSH](TextToSpeech.md). |
| `params` | [HashMap](../java.util/HashMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Parameters for the request. Can be null. Supported parameter names: [Engine.KEY_PARAM_STREAM](../android/speech/tts/TextToSpeech.Engine.md), [Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md), [Engine.KEY_PARAM_VOLUME](../android/speech/tts/TextToSpeech.Engine.md), [Engine.KEY_PARAM_PAN](../android/speech/tts/TextToSpeech.Engine.md). Engine specific parameters may be passed in but the parameter keys must be prefixed by the name of the engine they are intended for. For example the keys "com.svox.pico_foo" and "com.svox.pico:bar" will be passed to the engine named "com.svox.pico" if it is being used. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md) of**queuing**the speak operation. |

### stop

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stop(): Int
```

Interrupts the current utterance (whether played or rendered to file) and discards other utterances in the queue.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md). |

### synthesizeToFile

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun synthesizeToFile(
    text: CharSequence, 
    params: Bundle, 
    fileDescriptor: ParcelFileDescriptor, 
    utteranceId: String
): Int
```

Synthesizes the given text to a ParcelFileDescriptor using the specified parameters. This method is asynchronous, i.e. the method just adds the request to the queue of TTS requests and then returns. The synthesis might not have finished (or even started!) at the time when this method returns. In order to reliably detect errors during synthesis, we recommend setting an utterance progress listener (see [setOnUtteranceProgressListener](TextToSpeech.md))).

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):The text that should be synthesized. No longer than [getMaxSpeechInputLength()](TextToSpeech.md))characters. This value cannot be`null`. |
| `params` | [Bundle](../android.os/Bundle.md):Parameters for the request. Engine specific parameters may be passed in but the parameter keys must be prefixed by the name of the engine they are intended for. For example the keys "com.svox.pico_foo" and "com.svox.pico:bar" will be passed to the engine named "com.svox.pico" if it is being used. This value cannot be`null`. |
| `fileDescriptor` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md):ParcelFileDescriptor to write the generated audio data to. This value cannot be`null`. |
| --- | --- |
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):An unique identifier for this request. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md) of**queuing**the synthesizeToFile operation. |

### synthesizeToFile

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun synthesizeToFile(
    text: CharSequence!, 
    params: Bundle!, 
    file: File!, 
    utteranceId: String!
): Int
```

Synthesizes the given text to a file using the specified parameters. This method is asynchronous, i.e. the method just adds the request to the queue of TTS requests and then returns. The synthesis might not have finished (or even started!) at the time when this method returns. In order to reliably detect errors during synthesis, we recommend setting an utterance progress listener (see [setOnUtteranceProgressListener](TextToSpeech.md))).

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The text that should be synthesized. No longer than [getMaxSpeechInputLength()](TextToSpeech.md))characters. |
| `params` | [Bundle](../android.os/Bundle.md)!:Parameters for the request. Cannot be null. Engine specific parameters may be passed in but the parameter keys must be prefixed by the name of the engine they are intended for. For example the keys "com.svox.pico_foo" and "com.svox.pico:bar" will be passed to the engine named "com.svox.pico" if it is being used. |
| `file` | [File](../java.io/File.md)!:File to write the generated audio data to. |
| --- | --- |
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:An unique identifier for this request. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md) of**queuing**the synthesizeToFile operation. |

### synthesizeToFile

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun synthesizeToFile(
    text: String!, 
    params: HashMap<String!, String!>!, 
    filename: String!
): Int
```

**Deprecated:** *As of API level 21, replaced by [synthesizeToFile(java.lang.CharSequence,android.os.Bundle,java.io.File,java.lang.String)](TextToSpeech.md)).*

Synthesizes the given text to a file using the specified parameters. This method is asynchronous, i.e. the method just adds the request to the queue of TTS requests and then returns. The synthesis might not have finished (or even started!) at the time when this method returns. In order to reliably detect errors during synthesis, we recommend setting an utterance progress listener (see [setOnUtteranceProgressListener](TextToSpeech.md))) and using the [Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md) parameter.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The text that should be synthesized. No longer than [getMaxSpeechInputLength()](TextToSpeech.md))characters. |
| `params` | [HashMap](../java.util/HashMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Parameters for the request. Cannot be null. Supported parameter names: [Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md). Engine specific parameters may be passed in but the parameter keys must be prefixed by the name of the engine they are intended for. For example the keys "com.svox.pico_foo" and "com.svox.pico:bar" will be passed to the engine named "com.svox.pico" if it is being used. |
| `filename` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Absolute file filename to write the generated audio data to.It should be something like "/sdcard/myappsounds/mysound.wav". |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](TextToSpeech.md) or [SUCCESS](TextToSpeech.md) of**queuing**the synthesizeToFile operation. |
