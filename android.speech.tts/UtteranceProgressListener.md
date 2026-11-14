# UtteranceProgressListener

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UtteranceProgressListener

Kotlin| [Java](UtteranceProgressListener.md) 
| --- | --- |

```
abstract class UtteranceProgressListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.speech.tts.UtteranceProgressListener](UtteranceProgressListener.md) |

Listener for events relating to the progress of an utterance through the synthesis queue. Each utterance is associated with a call to android.speech.tts.TextToSpeech#speak or android.speech.tts.TextToSpeech#synthesizeToFile with an associated utterance identifier, as per [TextToSpeech.Engine.KEY_PARAM_UTTERANCE_ID](../android/speech/tts/TextToSpeech.Engine.md). The callbacks specified in this method can be called from multiple threads.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UtteranceProgressListener](UtteranceProgressListener.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAudioAvailable](UtteranceProgressListener.md))`(`utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `audio:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` This is called when a chunk of audio is ready for consumption. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBeginSynthesis](UtteranceProgressListener.md))`(`utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sampleRateInHz:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `channelCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the TTS engine begins to synthesize the audio for a request. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDone](UtteranceProgressListener.md))`(`utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called when an utterance has successfully completed processing. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](UtteranceProgressListener.md))`(`utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called when an error has occurred during processing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](UtteranceProgressListener.md))`(`utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an error has occurred during processing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRangeStart](UtteranceProgressListener.md))`(`utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `frame:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This is called when the TTS service is about to speak the specified range of the utterance with the given utteranceId. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](UtteranceProgressListener.md))`(`utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called when an utterance "starts" as perceived by the caller. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStop](UtteranceProgressListener.md))`(`utteranceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `interrupted:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when an utterance has been stopped while in progress or flushed from the synthesis queue. |

## Public constructors

### UtteranceProgressListener

```
UtteranceProgressListener()
```

## Public methods

### onAudioAvailable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAudioAvailable(
    utteranceId: String!, 
    audio: ByteArray!
): Unit
```

This is called when a chunk of audio is ready for consumption.

The audio parameter is a copy of what will be synthesized to the speakers (when synthesis was initiated with a android.speech.tts.TextToSpeech#speak call) or written to the file system (for android.speech.tts.TextToSpeech#synthesizeToFile). The audio bytes are delivered in one or more chunks; if [onDone](UtteranceProgressListener.md))or #onError is called all chunks have been received.

The audio received here may not be played for some time depending on buffer sizes and the amount of items on the synthesis queue.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The utterance ID of the utterance. |
| `audio` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:A chunk of audio; the format can be known by listening to [onBeginSynthesis(java.lang.String,int,int,int)](UtteranceProgressListener.md)). |

### onBeginSynthesis

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onBeginSynthesis(
    utteranceId: String!, 
    sampleRateInHz: Int, 
    audioFormat: Int, 
    channelCount: Int
): Unit
```

Called when the TTS engine begins to synthesize the audio for a request.

It provides information about the format of the byte array for subsequent [onAudioAvailable](UtteranceProgressListener.md))calls.

This is called when the TTS engine starts synthesizing audio for the request. If an application wishes to know when the audio is about to start playing, {#onStart(String)} should be used instead.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The utterance ID of the utterance. |
| `sampleRateInHz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Sample rate in hertz of the generated audio. |
| `audioFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Audio format of the generated audio. Should be one of [AudioFormat.ENCODING_PCM_8BIT](../android.media/AudioFormat.md), [AudioFormat.ENCODING_PCM_16BIT](../android.media/AudioFormat.md) or [AudioFormat.ENCODING_PCM_FLOAT](../android.media/AudioFormat.md). |
| --- | --- |
| `channelCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of channels. |

### onDone

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDone(utteranceId: String!): Unit
```

Called when an utterance has successfully completed processing. All audio will have been played back by this point for audible output, and all output will have been written to disk for file synthesis requests. This request is guaranteed to be called after [onStart(java.lang.String)](UtteranceProgressListener.md)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------|
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The utterance ID of the utterance. |

### onError

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onError(utteranceId: String!): Unit
```

**Deprecated:** *Use [onError(java.lang.String,int)](UtteranceProgressListener.md))instead*

Called when an error has occurred during processing. This can be called at any point in the synthesis process. Note that there might be calls to [onStart(java.lang.String)](UtteranceProgressListener.md))for specified utteranceId but there will never be a call to both [onDone(java.lang.String)](UtteranceProgressListener.md))and [onError(java.lang.String)](UtteranceProgressListener.md))for the same utterance.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------|
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The utterance ID of the utterance. |

### onError

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onError(
    utteranceId: String!, 
    errorCode: Int
): Unit
```

Called when an error has occurred during processing. This can be called at any point in the synthesis process. Note that there might be calls to [onStart(java.lang.String)](UtteranceProgressListener.md))for specified utteranceId but there will never be a call to both [onDone(java.lang.String)](UtteranceProgressListener.md))and [onError(java.lang.String,int)](UtteranceProgressListener.md))for the same utterance. The default implementation calls [onError(java.lang.String)](UtteranceProgressListener.md)).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The utterance ID of the utterance. |
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the ERROR_\* codes from [TextToSpeech](TextToSpeech.md) |

### onRangeStart

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRangeStart(
    utteranceId: String!, 
    start: Int, 
    end: Int, 
    frame: Int
): Unit
```

This is called when the TTS service is about to speak the specified range of the utterance with the given utteranceId.

This method is called when the audio is expected to start playing on the speaker. Note that this is different from [onAudioAvailable](UtteranceProgressListener.md))which is called as soon as the audio is generated.

This information can be used, for example, to highlight ranges of the text while it is spoken.

Only called if the engine supplies timing information by calling [android.speech.tts.SynthesisCallback#rangeStart(int,int,int)](SynthesisCallback.md)).

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Unique id identifying the synthesis request. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start index of the range in the utterance text. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The end index of the range (exclusive) in the utterance text. |
| --- | --- |
| `frame` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position in frames in the audio of the request where this range is spoken. |

### onStart

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStart(utteranceId: String!): Unit
```

Called when an utterance "starts" as perceived by the caller. This will be soon before audio is played back in the case of a android.speech.tts.TextToSpeech#speak or before the first bytes of a file are written to the file system in the case of android.speech.tts.TextToSpeech#synthesizeToFile.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------|
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The utterance ID of the utterance. |

### onStop

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStop(
    utteranceId: String!, 
    interrupted: Boolean
): Unit
```

Called when an utterance has been stopped while in progress or flushed from the synthesis queue. This can happen if a client calls [TextToSpeech.stop()](TextToSpeech.md))or uses [TextToSpeech.QUEUE_FLUSH](TextToSpeech.md) as an argument with the android.speech.tts.TextToSpeech#speak or android.speech.tts.TextToSpeech#synthesizeToFile methods.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `utteranceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The utterance ID of the utterance. |
| `interrupted` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, then the utterance was interrupted while being synthesized and its output is incomplete. If false, then the utterance was flushed before the synthesis started. |
