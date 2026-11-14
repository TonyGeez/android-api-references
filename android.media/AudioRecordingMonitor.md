# AudioRecordingMonitor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioRecordingMonitor

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioRecordingMonitor "View this page in Java") 

```
interface AudioRecordingMonitor
```

| [android.media.AudioRecordingMonitor](https://developer.android.com/reference/kotlin/android/media/AudioRecordingMonitor#) |

| Known Direct Subclasses [AudioRecord](https://developer.android.com/reference/kotlin/android/media/AudioRecord), [MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder) |---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------| | [AudioRecord](https://developer.android.com/reference/kotlin/android/media/AudioRecord) | The AudioRecord class manages the audio resources for Java applications to record audio from the audio input hardware of the platform. | | [MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder) | Used to record audio and video. | |

AudioRecordingMonitor defines an interface implemented by [AudioRecord](https://developer.android.com/reference/kotlin/android/media/AudioRecord) and [MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder) allowing applications to install a callback and be notified of changes in the capture path while recoding is active.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [AudioRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration)? | [getActiveRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecordingMonitor#getActiveRecordingConfiguration())`()` Returns the current active audio recording for this audio recorder. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioRecordingMonitor#registerAudioRecordingCallback(java.util.concurrent.Executor,%20android.media.AudioManager.AudioRecordingCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `cb:` ` [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback)`)` Register a callback to be notified of audio capture changes via a [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioRecordingMonitor#unregisterAudioRecordingCallback(android.media.AudioManager.AudioRecordingCallback))`(`cb:` ` [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback)`)` Unregister an audio recording callback previously registered with [registerAudioRecordingCallback(java.util.concurrent.Executor,android.media.AudioManager.AudioRecordingCallback)](https://developer.android.com/reference/kotlin/android/media/AudioRecordingMonitor#registerAudioRecordingCallback(java.util.concurrent.Executor,%20android.media.AudioManager.AudioRecordingCallback)). |

## Public methods

### getActiveRecordingConfiguration

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getActiveRecordingConfiguration(): AudioRecordingConfiguration?
```

Returns the current active audio recording for this audio recorder.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AudioRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration)? | a valid [AudioRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration) if this recorder is active or null otherwise. |

**See Also**

- [android.media.AudioRecordingConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration) 

### registerAudioRecordingCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerAudioRecordingCallback(
    executor: Executor, 
    cb: AudioManager.AudioRecordingCallback
): Unit
```

Register a callback to be notified of audio capture changes via a [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback). A callback is received when the capture path configuration changes (pre-processing, format, sampling rate...) or capture is silenced/unsilenced by the system.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) to handle the callbacks. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `cb` | [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback):non-null callback to register |

### unregisterAudioRecordingCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterAudioRecordingCallback(cb: AudioManager.AudioRecordingCallback): Unit
```

Unregister an audio recording callback previously registered with [registerAudioRecordingCallback(java.util.concurrent.Executor,android.media.AudioManager.AudioRecordingCallback)](https://developer.android.com/reference/kotlin/android/media/AudioRecordingMonitor#registerAudioRecordingCallback(java.util.concurrent.Executor,%20android.media.AudioManager.AudioRecordingCallback)).

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [AudioManager.AudioRecordingCallback](https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback):non-null callback to unregister |
