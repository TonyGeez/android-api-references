# SynthesisCallback

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SynthesisCallback

Kotlin| [Java](https://developer.android.com/reference/android/speech/tts/SynthesisCallback "View this page in Java") 
| --- | --- |

```
interface SynthesisCallback
```

| [android.speech.tts.SynthesisCallback](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#) |

A callback to return speech data synthesized by a text to speech engine. The engine can provide streaming audio by calling [start](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#start(kotlin.Int,%20kotlin.Int,%20kotlin.Int)), then [audioAvailable](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#audioAvailable(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))until all audio has been provided, then finally [done](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#done()). #error can be called at any stage in the synthesis process to indicate that an error has occurred, but if the call is made after a call to [done](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#done()), it might be discarded. [done](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#done())must be called at the end of synthesis, regardless of errors. All methods can be only called on the synthesis thread.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [audioAvailable](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#audioAvailable(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The service should call this method when synthesized audio is ready for consumption. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [done](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#done())`()` The service should call this method when all the synthesized audio for a request has been passed to [audioAvailable](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#audioAvailable(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [error](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#error())`()` The service should call this method if the speech synthesis fails. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [error](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#error(kotlin.Int))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The service should call this method if the speech synthesis fails. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxBufferSize](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#getMaxBufferSize())`()` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFinished](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#hasFinished())`()` Check if [done](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#done())was called or not. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStarted](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#hasStarted())`()` Check if [start](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#start(kotlin.Int,%20kotlin.Int,%20kotlin.Int))was called or not. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rangeStart](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#rangeStart(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`markerInFrames:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The service may call this method to provide timing information about the spoken text. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [start](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#start(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`sampleRateInHz:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `channelCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The service should call this when it starts to synthesize audio for this request. |
| --- | --- |

## Public methods

### audioAvailable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun audioAvailable(
    buffer: ByteArray!, 
    offset: Int, 
    length: Int
): Int
```

The service should call this method when synthesized audio is ready for consumption.

This method should only be called on the synthesis thread, while in [android.speech.tts.TextToSpeechService#onSynthesizeText](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeechService#onSynthesizeText(android.speech.tts.SynthesisRequest,%20android.speech.tts.SynthesisCallback)).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The generated audio data. This method will not hold on to`buffer`, so the caller is free to modify it after this method returns. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset into`buffer`where the audio data starts. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of bytes of audio data in`buffer`. This must be less than or equal to the return value of [getMaxBufferSize](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#getMaxBufferSize()). |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [android.speech.tts.TextToSpeech#SUCCESS](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#SUCCESS:kotlin.Int), [android.speech.tts.TextToSpeech#ERROR](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#ERROR:kotlin.Int) or [android.speech.tts.TextToSpeech#STOPPED](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#STOPPED:kotlin.Int). |

### done

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun done(): Int
```

The service should call this method when all the synthesized audio for a request has been passed to [audioAvailable](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#audioAvailable(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)).

This method should only be called on the synthesis thread, while in [android.speech.tts.TextToSpeechService#onSynthesizeText](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeechService#onSynthesizeText(android.speech.tts.SynthesisRequest,%20android.speech.tts.SynthesisCallback)).

This method has to be called if [start](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#start(kotlin.Int,%20kotlin.Int,%20kotlin.Int))and/or #error was called.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [android.speech.tts.TextToSpeech#SUCCESS](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#SUCCESS:kotlin.Int), [android.speech.tts.TextToSpeech#ERROR](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#ERROR:kotlin.Int) or [android.speech.tts.TextToSpeech#STOPPED](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#STOPPED:kotlin.Int). |

### error

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun error(): Unit
```

The service should call this method if the speech synthesis fails.

This method should only be called on the synthesis thread, while in [android.speech.tts.TextToSpeechService#onSynthesizeText](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeechService#onSynthesizeText(android.speech.tts.SynthesisRequest,%20android.speech.tts.SynthesisCallback)). 

### error

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun error(errorCode: Int): Unit
```

The service should call this method if the speech synthesis fails.

This method should only be called on the synthesis thread, while in [android.speech.tts.TextToSpeechService#onSynthesizeText](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeechService#onSynthesizeText(android.speech.tts.SynthesisRequest,%20android.speech.tts.SynthesisCallback)).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Error code to pass to the client. One of the ERROR_ values from Value is [android.speech.tts.TextToSpeech#ERROR_SYNTHESIS](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#ERROR_SYNTHESIS:kotlin.Int), [android.speech.tts.TextToSpeech#ERROR_SERVICE](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#ERROR_SERVICE:kotlin.Int), [android.speech.tts.TextToSpeech#ERROR_OUTPUT](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#ERROR_OUTPUT:kotlin.Int), [android.speech.tts.TextToSpeech#ERROR_NETWORK](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#ERROR_NETWORK:kotlin.Int), [android.speech.tts.TextToSpeech#ERROR_NETWORK_TIMEOUT](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#ERROR_NETWORK_TIMEOUT:kotlin.Int), [android.speech.tts.TextToSpeech#ERROR_INVALID_REQUEST](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#ERROR_INVALID_REQUEST:kotlin.Int), or [android.speech.tts.TextToSpeech#ERROR_NOT_INSTALLED_YET](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#ERROR_NOT_INSTALLED_YET:kotlin.Int) |

### getMaxBufferSize

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxBufferSize(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes that the TTS engine can pass in a single call of [audioAvailable](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#audioAvailable(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)). Calls to [audioAvailable](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#audioAvailable(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))with data lengths larger than this value will not succeed. |

### hasFinished

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasFinished(): Boolean
```

Check if [done](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#done())was called or not.

This method should only be called on the synthesis thread, while in [android.speech.tts.TextToSpeechService#onSynthesizeText](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeechService#onSynthesizeText(android.speech.tts.SynthesisRequest,%20android.speech.tts.SynthesisCallback)).

Useful for checking if a fallback from network request is possible. 

### hasStarted

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasStarted(): Boolean
```

Check if [start](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#start(kotlin.Int,%20kotlin.Int,%20kotlin.Int))was called or not.

This method should only be called on the synthesis thread, while in [android.speech.tts.TextToSpeechService#onSynthesizeText](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeechService#onSynthesizeText(android.speech.tts.SynthesisRequest,%20android.speech.tts.SynthesisCallback)).

Useful for checking if a fallback from network request is possible. 

### rangeStart

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rangeStart(
    markerInFrames: Int, 
    start: Int, 
    end: Int
): Unit
```

The service may call this method to provide timing information about the spoken text.

Calling this method means that at the given audio frame, the given range of the input is about to be spoken. If this method is called the client will receive a callback on the listener ([UtteranceProgressListener.onRangeStart](https://developer.android.com/reference/kotlin/android/speech/tts/UtteranceProgressListener#onRangeStart(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))) at the moment that frame has been reached by the playback head.

This information can be used by the client, for example, to highlight ranges of the text while it is spoken.

The markerInFrames is a frame index into the audio for this synthesis request, i.e. into the concatenation of the audio bytes sent to audioAvailable for this synthesis request. The definition of a frame depends on the format given by [start](https://developer.android.com/reference/kotlin/android/speech/tts/SynthesisCallback#start(kotlin.Int,%20kotlin.Int,%20kotlin.Int)). See [AudioFormat](https://developer.android.com/reference/kotlin/android/media/AudioFormat.html#) for more information.

This method should only be called on the synthesis thread, while in [android.speech.tts.TextToSpeechService#onSynthesizeText](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeechService#onSynthesizeText(android.speech.tts.SynthesisRequest,%20android.speech.tts.SynthesisCallback)).

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `markerInFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position in frames in the audio where this range is spoken. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start index of the range in the input text. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The end index (exclusive) of the range in the input text. |
| --- | --- |

### start

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun start(
    sampleRateInHz: Int, 
    audioFormat: Int, 
    channelCount: Int
): Int
```

The service should call this when it starts to synthesize audio for this request.

This method should only be called on the synthesis thread, while in [android.speech.tts.TextToSpeechService#onSynthesizeText](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeechService#onSynthesizeText(android.speech.tts.SynthesisRequest,%20android.speech.tts.SynthesisCallback)).

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sampleRateInHz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Sample rate in HZ of the generated audio. |
| `audioFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Audio format of the generated audio. Must be one of [android.media.AudioFormat#ENCODING_PCM_8BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat.html#ENCODING_PCM_8BIT:kotlin.Int) or [AudioFormat.ENCODING_PCM_16BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat.html#ENCODING_PCM_16BIT:kotlin.Int). Can also be [AudioFormat.ENCODING_PCM_FLOAT](https://developer.android.com/reference/kotlin/android/media/AudioFormat.html#ENCODING_PCM_FLOAT:kotlin.Int) when targetting Android N and above. Value is [android.media.AudioFormat#ENCODING_PCM_8BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat.html#ENCODING_PCM_8BIT:kotlin.Int), [android.media.AudioFormat#ENCODING_PCM_16BIT](https://developer.android.com/reference/kotlin/android/media/AudioFormat.html#ENCODING_PCM_16BIT:kotlin.Int), or [android.media.AudioFormat#ENCODING_PCM_FLOAT](https://developer.android.com/reference/kotlin/android/media/AudioFormat.html#ENCODING_PCM_FLOAT:kotlin.Int) |
| `channelCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of channels. Must be`1`or`2`. Value is between 1 and 2 inclusive |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [android.speech.tts.TextToSpeech#SUCCESS](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#SUCCESS:kotlin.Int), [android.speech.tts.TextToSpeech#ERROR](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#ERROR:kotlin.Int) or [android.speech.tts.TextToSpeech#STOPPED](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#STOPPED:kotlin.Int). |
