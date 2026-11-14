# TvRecordingClient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvRecordingClient

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/TvRecordingClient "View this page in Java") 
| --- | --- |

```
open class TvRecordingClient
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.TvRecordingClient](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#) |

The public interface object used to interact with a specific TV input service for TV program recording.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [RecordingCallback](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback) Callback used to receive various status updates on the [android.media.tv.TvInputService.RecordingSession](https://developer.android.com/reference/kotlin/android/media/tv/TvInputService.RecordingSession) |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TvRecordingClient](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#TvRecordingClient(android.content.Context,%20kotlin.String,%20android.media.tv.TvRecordingClient.RecordingCallback,%20android.os.Handler))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `callback:` ` [TvRecordingClient.RecordingCallback](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Creates a new TvRecordingClient object. |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pauseRecording](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#pauseRecording())`()` Pause TV program recording in the current recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pauseRecording](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#pauseRecording(android.os.Bundle))`(`params:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Pause TV program recording in the current recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#release())`()` Releases the resources in the current recording session immediately. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resumeRecording](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#resumeRecording())`()` Resume TV program recording only in recording pause status in the current recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resumeRecording](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#resumeRecording(android.os.Bundle))`(`params:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Resume TV program recording only in recording pause status in the current recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendAppPrivateCommand](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#sendAppPrivateCommand(kotlin.String,%20android.os.Bundle))`(`action:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `data:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Sends a private command to the underlying TV input. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTvInteractiveAppView](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#setTvInteractiveAppView(android.media.tv.interactive.TvInteractiveAppView,%20kotlin.String))`(`view:` ` [TvInteractiveAppView](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView)?`, `recordingId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the related [TvInteractiveAppView](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView) instance so the interactive app service can be notified for recording events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startRecording](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#startRecording(android.net.Uri))`(`programUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?`)` Starts TV program recording in the current recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startRecording](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#startRecording(android.net.Uri,%20android.os.Bundle))`(`programUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?`, `params:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Starts TV program recording in the current recording session. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopRecording](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#stopRecording())`()` Stops TV program recording in the current recording session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tune](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#tune(kotlin.String,%20android.net.Uri))`(`inputId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `channelUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Tunes to a given channel for TV program recording. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tune](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#tune(kotlin.String,%20android.net.Uri,%20android.os.Bundle))`(`inputId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `channelUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `params:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Tunes to a given channel for TV program recording. |
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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The application context to create a TvRecordingClient with. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A short name for debugging purposes. |
| `callback` | [TvRecordingClient.RecordingCallback](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback):The callback to receive recording status changes. This value cannot be`null`. |
| --- | --- |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:The handler to invoke the callback on. |

## Public methods

### pauseRecording

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pauseRecording(): Unit
```

Pause TV program recording in the current recording session. Recording is expected to pause immediately when this method is called. If recording has not yet started in the current recording session, this method does nothing.

In pause status, the application can tune during recording. To continue recording, please call [TvRecordingClient.resumeRecording()](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#resumeRecording())to resume instead of [TvRecordingClient.startRecording(Uri)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#startRecording(android.net.Uri)). Application can stop the recording with [TvRecordingClient.stopRecording()](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#stopRecording())in recording pause status.

If the pause request cannot be fulfilled, the recording session will respond by calling [RecordingCallback.onError(int)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback#onError(kotlin.Int)). 

### pauseRecording

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pauseRecording(params: Bundle): Unit
```

Pause TV program recording in the current recording session. Recording is expected to pause immediately when this method is called. If recording has not yet started in the current recording session, this method does nothing.

In pause status, the application can tune during recording. To continue recording, please call [TvRecordingClient.resumeRecording()](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#resumeRecording())to resume instead of [TvRecordingClient.startRecording(Uri)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#startRecording(android.net.Uri)). Application can stop the recording with [TvRecordingClient.stopRecording()](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#stopRecording())in recording pause status.

If the pause request cannot be fulfilled, the recording session will respond by calling [RecordingCallback.onError(int)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback#onError(kotlin.Int)).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):Domain-specific data for this request. This value cannot be`null`. |

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

When record is resumed, the recording is continue and can not re-tune. Application can stop the recording with [TvRecordingClient.stopRecording()](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#stopRecording())after record resumed.

If the pause request cannot be fulfilled, the recording session will respond by calling [RecordingCallback.onError(int)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback#onError(kotlin.Int)). 

### resumeRecording

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resumeRecording(params: Bundle): Unit
```

Resume TV program recording only in recording pause status in the current recording session. Recording is expected to resume immediately when this method is called. If recording has not yet paused in the current recording session, this method does nothing.

When record is resumed, the recording is continues and can not re-tune. Application can stop the recording with [TvRecordingClient.stopRecording()](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#stopRecording())after record resumed.

If the resume request cannot be fulfilled, the recording session will respond by calling [RecordingCallback.onError(int)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback#onError(kotlin.Int)).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):Domain-specific data for this request. This value cannot be`null`. |

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
| `data` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:An optional bundle to send with the command. |

### setTvInteractiveAppView

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTvInteractiveAppView(
    view: TvInteractiveAppView?, 
    recordingId: String?
): Unit
```

Sets the related [TvInteractiveAppView](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView) instance so the interactive app service can be notified for recording events.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [TvInteractiveAppView](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView)?:The related [TvInteractiveAppView](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView) instance that is linked to this TV recording client.`null`to unlink the view. |
| `recordingId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The ID of the recording which is assigned by the TV application.`null`if and only if the TvInteractiveAppView parameter is`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when recording ID is`null`and the TvInteractiveAppView is not`null`; or when recording ID is not`null`and the TvInteractiveAppView is`null`. |

**See Also**

- [android.media.tv.interactive.TvInteractiveAppView#notifyRecordingScheduled(String, String)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView#notifyRecordingScheduled(kotlin.String,%20kotlin.String))
- [android.media.tv.interactive.TvInteractiveAppView#notifyRecordingStarted(String, String)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView#notifyRecordingStarted(kotlin.String,%20kotlin.String)) 

### startRecording

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startRecording(programUri: Uri?): Unit
```

Starts TV program recording in the current recording session. Recording is expected to start immediately when this method is called. If the current recording session has not yet tuned to any channel, this method throws an exception.

The application may supply the URI for a TV program for filling in program specific data fields in the [android.media.tv.TvContract.RecordedPrograms](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.RecordedPrograms) table. A non-null`programUri`implies the started recording should be of that specific program, whereas null`programUri`does not impose such a requirement and the recording can span across multiple TV programs. In either case, the application must call [TvRecordingClient.stopRecording()](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#stopRecording())to stop the recording.

The recording session will respond by calling [RecordingCallback.onError(int)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback#onError(kotlin.Int))if the start request cannot be fulfilled.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `programUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?:The URI for the TV program to record, built by [TvContract.buildProgramUri(long)](https://developer.android.com/reference/kotlin/android/media/tv/TvContract#buildProgramUri(kotlin.Long)). Can be`null`. |

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

The application may supply the URI for a TV program for filling in program specific data fields in the [android.media.tv.TvContract.RecordedPrograms](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.RecordedPrograms) table. A non-null`programUri`implies the started recording should be of that specific program, whereas null`programUri`does not impose such a requirement and the recording can span across multiple TV programs. In either case, the application must call [TvRecordingClient.stopRecording()](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient#stopRecording())to stop the recording.

The recording session will respond by calling [RecordingCallback.onError(int)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback#onError(kotlin.Int))if the start request cannot be fulfilled.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `programUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?:The URI for the TV program to record, built by [TvContract.buildProgramUri(long)](https://developer.android.com/reference/kotlin/android/media/tv/TvContract#buildProgramUri(kotlin.Long)). Can be`null`. |
| `params` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):Domain-specific data for this request. Keys*must* be a scoped name, i.e. prefixed with a package name you own, so that different developers will not create conflicting keys. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------|
| `java.lang.IllegalStateException` | If #tune request hasn't been handled yet or during pause. |

### stopRecording

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stopRecording(): Unit
```

Stops TV program recording in the current recording session. Recording is expected to stop immediately when this method is called. If recording has not yet started in the current recording session, this method does nothing.

The recording session is expected to create a new data entry in the [android.media.tv.TvContract.RecordedPrograms](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.RecordedPrograms) table that describes the newly recorded program and pass the URI to that entry through to [RecordingCallback.onRecordingStopped(Uri)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback#onRecordingStopped(android.net.Uri)). If the stop request cannot be fulfilled, the recording session will respond by calling [RecordingCallback.onError(int)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback#onError(kotlin.Int)). 

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

The recording session will respond by calling [RecordingCallback.onTuned(Uri)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback#onTuned(android.net.Uri))if the tune request was fulfilled, or [RecordingCallback.onError(int)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback#onError(kotlin.Int))otherwise.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------|
| `inputId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The ID of the TV input for the given channel. |
| `channelUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:The URI of a channel. |

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

The recording session will respond by calling [RecordingCallback.onTuned(Uri)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback#onTuned(android.net.Uri))if the tune request was fulfilled, or [RecordingCallback.onError(int)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingClient.RecordingCallback#onError(kotlin.Int))otherwise.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The ID of the TV input for the given channel. |
| `channelUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:The URI of a channel. |
| `params` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Domain-specific data for this tune request. Keys*must*be a scoped name, i.e. prefixed with a package name you own, so that different developers will not create conflicting keys. |
| --- | --- |

| Exceptions ||
|-----------------------------------|----------------------------------|
| `java.lang.IllegalStateException` | If recording is already started. |
