# TvRecordingClient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvRecordingClient

Kotlin| [Java](../android/media/tv/TvRecordingClient.md) 
| --- | --- |

```
open class TvRecordingClient
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.TvRecordingClient](../android/media/tv/TvRecordingClient.md) |

The public interface object used to interact with a specific TV input service for TV program recording.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [RecordingCallback](../android/media/tv/TvRecordingClient.RecordingCallback.md) Callback used to receive various status updates on the [android.media.tv.TvInputService.RecordingSession](../android/media/tv/TvInputService.RecordingSession.md) |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TvRecordingClient](../android/media/tv/TvRecordingClient.md))`(`context:` ` [Context](../android/content/Context.md)!`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `callback:` ` [TvRecordingClient.RecordingCallback](../android/media/tv/TvRecordingClient.RecordingCallback.md)`, `handler:` ` [Handler](../android/os/Handler.md)!`)` Creates a new TvRecordingClient object. |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pauseRecording](../android/media/tv/TvRecordingClient.md))`()` Pause TV program recording in the current recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pauseRecording](../android/media/tv/TvRecordingClient.md))`(`params:` ` [Bundle](../android/os/Bundle.md)`)` Pause TV program recording in the current recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](../android/media/tv/TvRecordingClient.md))`()` Releases the resources in the current recording session immediately. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resumeRecording](../android/media/tv/TvRecordingClient.md))`()` Resume TV program recording only in recording pause status in the current recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resumeRecording](../android/media/tv/TvRecordingClient.md))`(`params:` ` [Bundle](../android/os/Bundle.md)`)` Resume TV program recording only in recording pause status in the current recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendAppPrivateCommand](../android/media/tv/TvRecordingClient.md))`(`action:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `data:` ` [Bundle](../android/os/Bundle.md)!`)` Sends a private command to the underlying TV input. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTvInteractiveAppView](../android/media/tv/TvRecordingClient.md))`(`view:` ` [TvInteractiveAppView](../android/media/tv/interactive/TvInteractiveAppView.md)?`, `recordingId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the related [TvInteractiveAppView](../android/media/tv/interactive/TvInteractiveAppView.md) instance so the interactive app service can be notified for recording events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startRecording](../android/media/tv/TvRecordingClient.md))`(`programUri:` ` [Uri](../android/net/Uri.md)?`)` Starts TV program recording in the current recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startRecording](../android/media/tv/TvRecordingClient.md))`(`programUri:` ` [Uri](../android/net/Uri.md)?`, `params:` ` [Bundle](../android/os/Bundle.md)`)` Starts TV program recording in the current recording session. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopRecording](../android/media/tv/TvRecordingClient.md))`()` Stops TV program recording in the current recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tune](../android/media/tv/TvRecordingClient.md))`(`inputId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `channelUri:` ` [Uri](../android/net/Uri.md)!`)` Tunes to a given channel for TV program recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tune](../android/media/tv/TvRecordingClient.md))`(`inputId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `channelUri:` ` [Uri](../android/net/Uri.md)!`, `params:` ` [Bundle](../android/os/Bundle.md)!`)` Tunes to a given channel for TV program recording. |
| --- | --- |

## Public constructors

### TvRecordingClient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TvRecordingClient(
    context: Context!, 
    tag: String!, 
    callback: TvRecordingClient.RecordingCallback, 
    handler: Handler!)
```

Creates a new TvRecordingClient object.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The application context to create a TvRecordingClient with. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A short name for debugging purposes. |
| `callback` | [TvRecordingClient.RecordingCallback](../android/media/tv/TvRecordingClient.RecordingCallback.md):The callback to receive recording status changes. This value cannot be`null`. |
| --- | --- |
| `handler` | [Handler](../android/os/Handler.md)!:The handler to invoke the callback on. |

## Public methods

### pauseRecording

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pauseRecording(): Unit
```

Pause TV program recording in the current recording session. Recording is expected to pause immediately when this method is called. If recording has not yet started in the current recording session, this method does nothing.

In pause status, the application can tune during recording. To continue recording, please call [TvRecordingClient.resumeRecording()](../android/media/tv/TvRecordingClient.md))to resume instead of [TvRecordingClient.startRecording(Uri)](../android/media/tv/TvRecordingClient.md)). Application can stop the recording with [TvRecordingClient.stopRecording()](../android/media/tv/TvRecordingClient.md))in recording pause status.

If the pause request cannot be fulfilled, the recording session will respond by calling [RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md)). 

### pauseRecording

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pauseRecording(params: Bundle): Unit
```

Pause TV program recording in the current recording session. Recording is expected to pause immediately when this method is called. If recording has not yet started in the current recording session, this method does nothing.

In pause status, the application can tune during recording. To continue recording, please call [TvRecordingClient.resumeRecording()](../android/media/tv/TvRecordingClient.md))to resume instead of [TvRecordingClient.startRecording(Uri)](../android/media/tv/TvRecordingClient.md)). Application can stop the recording with [TvRecordingClient.stopRecording()](../android/media/tv/TvRecordingClient.md))in recording pause status.

If the pause request cannot be fulfilled, the recording session will respond by calling [RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md)).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [Bundle](../android/os/Bundle.md):Domain-specific data for this request. This value cannot be`null`. |

### release

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Releases the resources in the current recording session immediately. This may be called at any time, however if the session is already released, it does nothing. 

### resumeRecording

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resumeRecording(): Unit
```

Resume TV program recording only in recording pause status in the current recording session. Recording is expected to resume immediately when this method is called. If recording has not yet paused in the current recording session, this method does nothing.

When record is resumed, the recording is continue and can not re-tune. Application can stop the recording with [TvRecordingClient.stopRecording()](../android/media/tv/TvRecordingClient.md))after record resumed.

If the pause request cannot be fulfilled, the recording session will respond by calling [RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md)). 

### resumeRecording

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resumeRecording(params: Bundle): Unit
```

Resume TV program recording only in recording pause status in the current recording session. Recording is expected to resume immediately when this method is called. If recording has not yet paused in the current recording session, this method does nothing.

When record is resumed, the recording is continues and can not re-tune. Application can stop the recording with [TvRecordingClient.stopRecording()](../android/media/tv/TvRecordingClient.md))after record resumed.

If the resume request cannot be fulfilled, the recording session will respond by calling [RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md)).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [Bundle](../android/os/Bundle.md):Domain-specific data for this request. This value cannot be`null`. |

### sendAppPrivateCommand

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendAppPrivateCommand(
    action: String, 
    data: Bundle!
): Unit
```

Sends a private command to the underlying TV input. This can be used to provide domain-specific features that are only known between certain clients and their TV inputs.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the private command to send. This*must* be a scoped name, i.e. prefixed with a package name you own, so that different developers will not create conflicting commands. This value cannot be`null`. |
| `data` | [Bundle](../android/os/Bundle.md)!:An optional bundle to send with the command. |

### setTvInteractiveAppView

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTvInteractiveAppView(
    view: TvInteractiveAppView?, 
    recordingId: String?
): Unit
```

Sets the related [TvInteractiveAppView](../android/media/tv/interactive/TvInteractiveAppView.md) instance so the interactive app service can be notified for recording events.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [TvInteractiveAppView](../android/media/tv/interactive/TvInteractiveAppView.md)?:The related [TvInteractiveAppView](../android/media/tv/interactive/TvInteractiveAppView.md) instance that is linked to this TV recording client.`null`to unlink the view. |
| `recordingId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The ID of the recording which is assigned by the TV application.`null`if and only if the TvInteractiveAppView parameter is`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when recording ID is`null`and the TvInteractiveAppView is not`null`; or when recording ID is not`null`and the TvInteractiveAppView is`null`. |

**See Also**

- [android.media.tv.interactive.TvInteractiveAppView#notifyRecordingScheduled(String, String)](../android/media/tv/interactive/TvInteractiveAppView.md))
- [android.media.tv.interactive.TvInteractiveAppView#notifyRecordingStarted(String, String)](../android/media/tv/interactive/TvInteractiveAppView.md)) 

### startRecording

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startRecording(programUri: Uri?): Unit
```

Starts TV program recording in the current recording session. Recording is expected to start immediately when this method is called. If the current recording session has not yet tuned to any channel, this method throws an exception.

The application may supply the URI for a TV program for filling in program specific data fields in the [android.media.tv.TvContract.RecordedPrograms](../android/media/tv/TvContract.RecordedPrograms.md) table. A non-null`programUri`implies the started recording should be of that specific program, whereas null`programUri`does not impose such a requirement and the recording can span across multiple TV programs. In either case, the application must call [TvRecordingClient.stopRecording()](../android/media/tv/TvRecordingClient.md))to stop the recording.

The recording session will respond by calling [RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md))if the start request cannot be fulfilled.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `programUri` | [Uri](../android/net/Uri.md)?:The URI for the TV program to record, built by [TvContract.buildProgramUri(long)](../android/media/tv/TvContract.md)). Can be`null`. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------|
| `java.lang.IllegalStateException` | If #tune request hasn't been handled yet or during pause. |

### startRecording

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startRecording(
    programUri: Uri?, 
    params: Bundle
): Unit
```

Starts TV program recording in the current recording session. Recording is expected to start immediately when this method is called. If the current recording session has not yet tuned to any channel, this method throws an exception.

The application may supply the URI for a TV program for filling in program specific data fields in the [android.media.tv.TvContract.RecordedPrograms](../android/media/tv/TvContract.RecordedPrograms.md) table. A non-null`programUri`implies the started recording should be of that specific program, whereas null`programUri`does not impose such a requirement and the recording can span across multiple TV programs. In either case, the application must call [TvRecordingClient.stopRecording()](../android/media/tv/TvRecordingClient.md))to stop the recording.

The recording session will respond by calling [RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md))if the start request cannot be fulfilled.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `programUri` | [Uri](../android/net/Uri.md)?:The URI for the TV program to record, built by [TvContract.buildProgramUri(long)](../android/media/tv/TvContract.md)). Can be`null`. |
| `params` | [Bundle](../android/os/Bundle.md):Domain-specific data for this request. Keys*must* be a scoped name, i.e. prefixed with a package name you own, so that different developers will not create conflicting keys. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------|
| `java.lang.IllegalStateException` | If #tune request hasn't been handled yet or during pause. |

### stopRecording

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stopRecording(): Unit
```

Stops TV program recording in the current recording session. Recording is expected to stop immediately when this method is called. If recording has not yet started in the current recording session, this method does nothing.

The recording session is expected to create a new data entry in the [android.media.tv.TvContract.RecordedPrograms](../android/media/tv/TvContract.RecordedPrograms.md) table that describes the newly recorded program and pass the URI to that entry through to [RecordingCallback.onRecordingStopped(Uri)](../android/media/tv/TvRecordingClient.RecordingCallback.md)). If the stop request cannot be fulfilled, the recording session will respond by calling [RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md)). 

### tune

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tune(
    inputId: String!, 
    channelUri: Uri!
): Unit
```

Tunes to a given channel for TV program recording. The first tune request will create a new recording session for the corresponding TV input and establish a connection between the application and the session. If recording has already started in the current recording session, this method throws an exception.

The application may call this method before starting or after stopping recording, but not during recording.

The recording session will respond by calling [RecordingCallback.onTuned(Uri)](../android/media/tv/TvRecordingClient.RecordingCallback.md))if the tune request was fulfilled, or [RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md))otherwise.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------|
| `inputId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The ID of the TV input for the given channel. |
| `channelUri` | [Uri](../android/net/Uri.md)!:The URI of a channel. |

| Exceptions ||
|-----------------------------------|----------------------------------|
| `java.lang.IllegalStateException` | If recording is already started. |

### tune

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tune(
    inputId: String!, 
    channelUri: Uri!, 
    params: Bundle!
): Unit
```

Tunes to a given channel for TV program recording. The first tune request will create a new recording session for the corresponding TV input and establish a connection between the application and the session. If recording has already started in the current recording session, this method throws an exception. This can be used to provide domain-specific features that are only known between certain client and their TV inputs.

The application may call this method before starting or after stopping recording, but not during recording.

The recording session will respond by calling [RecordingCallback.onTuned(Uri)](../android/media/tv/TvRecordingClient.RecordingCallback.md))if the tune request was fulfilled, or [RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md))otherwise.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The ID of the TV input for the given channel. |
| `channelUri` | [Uri](../android/net/Uri.md)!:The URI of a channel. |
| `params` | [Bundle](../android/os/Bundle.md)!:Domain-specific data for this tune request. Keys*must*be a scoped name, i.e. prefixed with a package name you own, so that different developers will not create conflicting keys. |
| --- | --- |

| Exceptions ||
|-----------------------------------|----------------------------------|
| `java.lang.IllegalStateException` | If recording is already started. |
