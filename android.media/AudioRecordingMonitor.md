# AudioRecordingMonitor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioRecordingMonitor

Kotlin| [Java](../android/media/AudioRecordingMonitor.md) 
| --- | --- |

```
interface AudioRecordingMonitor
```

| [android.media.AudioRecordingMonitor](../android/media/AudioRecordingMonitor.md) |

| Known Direct Subclasses [AudioRecord](../android/media/AudioRecord.md), [MediaRecorder](../android/media/MediaRecorder.md) |---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------| | [AudioRecord](../android/media/AudioRecord.md) | The AudioRecord class manages the audio resources for Java applications to record audio from the audio input hardware of the platform. | | [MediaRecorder](../android/media/MediaRecorder.md) | Used to record audio and video. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

AudioRecordingMonitor defines an interface implemented by [AudioRecord](../android/media/AudioRecord.md) and [MediaRecorder](../android/media/MediaRecorder.md) allowing applications to install a callback and be notified of changes in the capture path while recoding is active.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [AudioRecordingConfiguration](../android/media/AudioRecordingConfiguration.md)? | [getActiveRecordingConfiguration](../android/media/AudioRecordingMonitor.md))`()` Returns the current active audio recording for this audio recorder. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAudioRecordingCallback](../android/media/AudioRecordingMonitor.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `cb:` ` [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md)`)` Register a callback to be notified of audio capture changes via a [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAudioRecordingCallback](../android/media/AudioRecordingMonitor.md))`(`cb:` ` [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md)`)` Unregister an audio recording callback previously registered with [registerAudioRecordingCallback(java.util.concurrent.Executor,android.media.AudioManager.AudioRecordingCallback)](../android/media/AudioRecordingMonitor.md)). |
| --- | --- |

## Public methods

### getActiveRecordingConfiguration

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getActiveRecordingConfiguration(): AudioRecordingConfiguration?
```

Returns the current active audio recording for this audio recorder.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AudioRecordingConfiguration](../android/media/AudioRecordingConfiguration.md)? | a valid [AudioRecordingConfiguration](../android/media/AudioRecordingConfiguration.md) if this recorder is active or null otherwise. |

**See Also**

- [android.media.AudioRecordingConfiguration](../android/media/AudioRecordingConfiguration.md) 

### registerAudioRecordingCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerAudioRecordingCallback(
    executor: Executor, 
    cb: AudioManager.AudioRecordingCallback
): Unit
```

Register a callback to be notified of audio capture changes via a [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md). A callback is received when the capture path configuration changes (pre-processing, format, sampling rate...) or capture is silenced/unsilenced by the system.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md): [Executor](../java/util/concurrent/Executor.md) to handle the callbacks. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `cb` | [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md):non-null callback to register |

### unregisterAudioRecordingCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterAudioRecordingCallback(cb: AudioManager.AudioRecordingCallback): Unit
```

Unregister an audio recording callback previously registered with [registerAudioRecordingCallback(java.util.concurrent.Executor,android.media.AudioManager.AudioRecordingCallback)](../android/media/AudioRecordingMonitor.md)).

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md):non-null callback to unregister |
