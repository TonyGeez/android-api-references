# VoiceInteractionSession

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VoiceInteractionSession

Kotlin| [Java](https://developer.android.com/reference/android/service/voice/VoiceInteractionSession "View this page in Java") 
| --- | --- |

```
open class VoiceInteractionSession : ComponentCallbacks2, KeyEvent.Callback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.voice.VoiceInteractionSession](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#) |

An active voice interaction session, providing a facility for the implementation to interact with the user in the voice interaction layer. The user interface is initially shown by default, and can be created by overriding [onCreateContentView()](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onCreateContentView())in which the UI can be built.

A voice interaction session can be self-contained, ultimately calling [finish](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#finish())when done. It can also initiate voice interactions with applications by calling [startVoiceActivity](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#startVoiceActivity(android.content.Intent))
.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [AbortVoiceRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.AbortVoiceRequest) A request to report that the current user interaction can not be completed with voice, as per [VoiceInteractor.AbortVoiceRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.AbortVoiceRequest.html#). |
| open | [ActivityId](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.ActivityId) Represents the id of an assist source activity. |
| | [AssistState](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.AssistState) Represents assist state captured when this session was started. |
| --- | --- |
| | [CommandRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.CommandRequest) A generic vendor-specific request, as per [VoiceInteractor.CommandRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.CommandRequest.html#). |
| | [CompleteVoiceRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.CompleteVoiceRequest) A request to simply inform the user that the voice operation has completed, as per [VoiceInteractor.CompleteVoiceRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.CompleteVoiceRequest.html#). |
| | [ConfirmationRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.ConfirmationRequest) A request for confirmation from the user of an operation, as per [VoiceInteractor.ConfirmationRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.ConfirmationRequest.html#). |
| --- | --- |
| | [Insets](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.Insets) Information about where interesting parts of the input method UI appear. |
| | [PickOptionRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.PickOptionRequest) A request for the user to pick from a set of option, as per [VoiceInteractor.PickOptionRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.PickOptionRequest.html#). |
| open | [Request](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.Request) Base class representing a request from a voice-driver app to perform a particular voice operation with the user. |
| --- | --- |
| abstract | [VisibleActivityCallback](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.VisibleActivityCallback) Callback interface for receiving visible activity changes used for assistant usage. |

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_FOREGROUND_ACTIVITIES](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#KEY_FOREGROUND_ACTIVITIES:kotlin.String) Bundle key used to specify foreground activity app components. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_SHOW_SESSION_ID](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#KEY_SHOW_SESSION_ID:kotlin.String) Bundle key used to specify the id when the system prepares to show session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_SOURCE_ACTIVITY](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_SOURCE_ACTIVITY:kotlin.Int) Flag for use with [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): indicates that an Activity has invoked the voice interaction service for a local interaction using [Activity.startLocalVoiceInteraction(Bundle)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startLocalVoiceInteraction(android.os.Bundle)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_SOURCE_APPLICATION](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_SOURCE_APPLICATION:kotlin.Int) Flag for use with [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): indicates that the application itself has invoked the assistant. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_SOURCE_ASSIST_GESTURE](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_SOURCE_ASSIST_GESTURE:kotlin.Int) Flag for use with [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): indicates that the session has been started from the system assist gesture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_SOURCE_AUTOMOTIVE_SYSTEM_UI](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_SOURCE_AUTOMOTIVE_SYSTEM_UI:kotlin.Int) Flag for use with [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): indicates that the voice interaction service was invoked from an Android automotive system UI. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_SOURCE_NOTIFICATION](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_SOURCE_NOTIFICATION:kotlin.Int) Flag for use with [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): indicates that the voice interaction service was invoked from a notification. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_SOURCE_PUSH_TO_TALK](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_SOURCE_PUSH_TO_TALK:kotlin.Int) Flag for use with [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): indicates that the voice interaction service was invoked from a physical button. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_WITH_ASSIST](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_WITH_ASSIST:kotlin.Int) Flag received in [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): originator requested that the session be started with assist data from the currently focused activity. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_WITH_SCREENSHOT](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_WITH_SCREENSHOT:kotlin.Int) Flag received in [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): originator requested that the session be started with a screen shot of the currently focused activity. |

| Inherited constants ||
|---|---|
| From class [ComponentCallbacks2](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_BACKGROUND](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_COMPLETE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_CRITICAL](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is [onLowMemory()](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory())called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_LOW](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_UI_HIDDEN](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [VoiceInteractionSession](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#VoiceInteractionSession(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` <br /> |
| [VoiceInteractionSession](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#VoiceInteractionSession(android.content.Context,%20android.os.Handler))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeSystemDialogs](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#closeSystemDialogs())`()` Request that all system dialogs (and status bar shade etc) be closed, allowing access to the session's UI. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#dump(kotlin.String,%20java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`, `writer:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Print the Service's state into the given stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#finish())`()` Finish the session. |
| --- | --- |
| open [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getContext](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#getContext())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDisabledShowContext](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#getDisabledShowContext())`()` Equivalent to [VoiceInteractionService.getDisabledShowContext](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService#getDisabledShowContext()). |
| open [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#)! | [getLayoutInflater](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#getLayoutInflater())`()` Convenience for inflating views. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUserDisabledShowContext](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#getUserDisabledShowContext())`()` Return which show context flags have been disabled by the user through the system settings UI, so the session will never get this data. |
| open [Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog.html#)! | [getWindow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#getWindow())`()` Retrieve the window being used to show the session's UI. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hide](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#hide())`()` Hide the session's UI, if currently shown. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAssistStructureFailure](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onAssistStructureFailure(kotlin.Throwable))`(`failure:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Called when there has been a failure transferring the [AssistStructure](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.html#) to the assistant. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBackPressed](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onBackPressed())`()` Called when the user presses the back button while focus is in the session UI. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCancelRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onCancelRequest(android.service.voice.VoiceInteractionSession.Request))`(`request:` ` [VoiceInteractionSession.Request](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.Request)!`)` Called when the [android.app.VoiceInteractor](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.html#) has asked to cancel a [Request](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.Request) that was previously delivered to [onRequestConfirmation](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestConfirmation(android.service.voice.VoiceInteractionSession.ConfirmationRequest)), [onRequestPickOption](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestPickOption(android.service.voice.VoiceInteractionSession.PickOptionRequest)), [onRequestCompleteVoice](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestCompleteVoice(android.service.voice.VoiceInteractionSession.CompleteVoiceRequest)), [onRequestAbortVoice](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestAbortVoice(android.service.voice.VoiceInteractionSession.AbortVoiceRequest)), or [onRequestCommand](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestCommand(android.service.voice.VoiceInteractionSession.CommandRequest)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCloseSystemDialogs](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onCloseSystemDialogs())`()` Sessions automatically watch for requests that all system UI be closed (such as when the user presses HOME), which will appear here. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onComputeInsets](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onComputeInsets(android.service.voice.VoiceInteractionSession.Insets))`(`outInsets:` ` [VoiceInteractionSession.Insets](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.Insets)!`)` Compute the interesting insets into your UI. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfigurationChanged](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onConfigurationChanged(android.content.res.Configuration))`(`newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreate](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onCreate())`()` Initiatize a new session. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [onCreateContentView](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onCreateContentView())`()` Hook in which to create the session's UI. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroy](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onDestroy())`()` Last callback to the session as it is being finished. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDirectActionsInvalidated](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onDirectActionsInvalidated(android.service.voice.VoiceInteractionSession.ActivityId))`(`activityId:` ` [VoiceInteractionSession.ActivityId](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.ActivityId)`)` Called when the direct actions are invalidated. |
| open [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)! | [onGetSupportedCommands](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onGetSupportedCommands(kotlin.Array))`(`commands:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Request to query for what extended commands the session supports. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHandleAssist](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onHandleAssist(android.os.Bundle,%20android.app.assist.AssistStructure,%20android.app.assist.AssistContent))`(`data:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `structure:` ` [AssistStructure](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.html#)?`, `content:` ` [AssistContent](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent.html#)?`)` Called to receive data from the application that the user was currently viewing when - \* an assist session is started. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHandleAssist](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onHandleAssist(android.service.voice.VoiceInteractionSession.AssistState))`(`state:` ` [VoiceInteractionSession.AssistState](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.AssistState)`)` Called to receive data from the application that the user was currently viewing when an assist session is started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHandleAssistSecondary](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onHandleAssistSecondary(android.os.Bundle,%20android.app.assist.AssistStructure,%20android.app.assist.AssistContent,%20kotlin.Int,%20kotlin.Int))`(`data:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `structure:` ` [AssistStructure](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.html#)?`, `content:` ` [AssistContent](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent.html#)?`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to receive data from other applications that the user was or is interacting with, that are currently on the screen in a multi-window display environment, not including the currently focused activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHandleScreenshot](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onHandleScreenshot(android.graphics.Bitmap))`(`screenshot:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)?`)` Called to receive a screenshot of what the user was currently viewing when an assist session is started. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHide](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onHide())`()` Called immediately after stopping to show the session UI. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onKeyDown(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyLongPress](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyMultiple](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onKeyUp(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLockscreenShown](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onLockscreenShown())`()` Called when the lockscreen was shown. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLowMemory](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onLowMemory())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onPrepareShow(android.os.Bundle,%20kotlin.Int))`(`args:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`, `showFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called prior to [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int))before any UI setup has occurred. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRequestAbortVoice](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestAbortVoice(android.service.voice.VoiceInteractionSession.AbortVoiceRequest))`(`request:` ` [VoiceInteractionSession.AbortVoiceRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.AbortVoiceRequest)!`)` Request to abort the voice interaction session because the voice activity can not complete its interaction using voice. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRequestCommand](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestCommand(android.service.voice.VoiceInteractionSession.CommandRequest))`(`request:` ` [VoiceInteractionSession.CommandRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.CommandRequest)!`)` Process an arbitrary extended command from the caller, corresponding to a [VoiceInteractor.CommandRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.CommandRequest.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRequestCompleteVoice](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestCompleteVoice(android.service.voice.VoiceInteractionSession.CompleteVoiceRequest))`(`request:` ` [VoiceInteractionSession.CompleteVoiceRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.CompleteVoiceRequest)!`)` Request to complete the voice interaction session because the voice activity successfully completed its interaction using voice. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRequestConfirmation](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestConfirmation(android.service.voice.VoiceInteractionSession.ConfirmationRequest))`(`request:` ` [VoiceInteractionSession.ConfirmationRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.ConfirmationRequest)!`)` Request to confirm with the user before proceeding with an unrecoverable operation, corresponding to a [VoiceInteractor.ConfirmationRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.ConfirmationRequest.html#). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRequestPickOption](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestPickOption(android.service.voice.VoiceInteractionSession.PickOptionRequest))`(`request:` ` [VoiceInteractionSession.PickOptionRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.PickOptionRequest)!`)` Request for the user to pick one of N options, corresponding to a [VoiceInteractor.PickOptionRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.PickOptionRequest.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int))`(`args:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `showFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the session UI is going to be shown. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTaskFinished](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onTaskFinished(android.content.Intent,%20kotlin.Int))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `taskId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the last activity of a task initiated by [startVoiceActivity(android.content.Intent)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#startVoiceActivity(android.content.Intent))has finished. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTaskStarted](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onTaskStarted(android.content.Intent,%20kotlin.Int))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `taskId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a task initiated by [startVoiceActivity(android.content.Intent)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#startVoiceActivity(android.content.Intent))has actually started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTrimMemory](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onTrimMemory(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [performDirectAction](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#performDirectAction(android.app.DirectAction,%20android.os.Bundle,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`action:` ` [DirectAction](https://developer.android.com/reference/kotlin/android/app/DirectAction.html#)`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`, `resultExecutor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `resultListener:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!>`)` Asks that an action be performed by the app. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerVisibleActivityCallback](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#registerVisibleActivityCallback(java.util.concurrent.Executor,%20android.service.voice.VoiceInteractionSession.VisibleActivityCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [VoiceInteractionSession.VisibleActivityCallback](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.VisibleActivityCallback)`)` Registers a callback that will be notified when visible activities have been changed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestDirectActions](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#requestDirectActions(android.service.voice.VoiceInteractionSession.ActivityId,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`activityId:` ` [VoiceInteractionSession.ActivityId](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.ActivityId)`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`, `resultExecutor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [DirectAction](https://developer.android.com/reference/kotlin/android/app/DirectAction.html#)!>!>`)` Requests a list of supported actions from an app. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#setContentView(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDisabledShowContext](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#setDisabledShowContext(kotlin.Int))`(`flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Equivalent to [VoiceInteractionService.setDisabledShowContext(int)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService#setDisabledShowContext(kotlin.Int)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKeepAwake](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#setKeepAwake(kotlin.Boolean))`(`keepAwake:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether this session will keep the device awake while it is running a voice activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTheme](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#setTheme(kotlin.Int))`(`theme:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` You can call this to customize the theme used by your IME's window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUiEnabled](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#setUiEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether the UI layer for this session is enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#show(android.os.Bundle,%20kotlin.Int))`(`args:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Show the UI for this session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAssistantActivity](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#startAssistantActivity(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Ask that a new assistant activity be started. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAssistantActivity](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#startAssistantActivity(android.content.Intent,%20android.os.Bundle))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)`, `bundle:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Ask that a new assistant activity be started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startVoiceActivity](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#startVoiceActivity(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Ask that a new activity be started for voice interaction. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterVisibleActivityCallback](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#unregisterVisibleActivityCallback(android.service.voice.VoiceInteractionSession.VisibleActivityCallback))`(`callback:` ` [VoiceInteractionSession.VisibleActivityCallback](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.VisibleActivityCallback)`)` Unregisters the callback. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [ComponentCallbacks](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfigurationChanged](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration))`(`newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`)` <br /> Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLowMemory](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory())`()` <br /> This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. <br /> | ||

## Constants

### KEY_FOREGROUND_ACTIVITIES

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_FOREGROUND_ACTIVITIES: String
```

Bundle key used to specify foreground activity app components.

Type: ArrayList\&ltComponentName\> 

 Value: "android.service.voice.FOREGROUND_ACTIVITIES"

**See Also**

- [#onShow(Bundle, int)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)) 

### KEY_SHOW_SESSION_ID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_SHOW_SESSION_ID: String
```

Bundle key used to specify the id when the system prepares to show session. It increases for each request.

Type: int 

 Value: "android.service.voice.SHOW_SESSION_ID"

**See Also**

- [android.service.voice.VoiceInteractionService#showSession(Bundle, int)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService#showSession(android.os.Bundle,%20kotlin.Int))
- [android.service.voice.VoiceInteractionService#onPrepareToShowSession(Bundle, int)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService#onPrepareToShowSession(android.os.Bundle,%20kotlin.Int))
- [android.service.voice.VoiceInteractionService#onShowSessionFailed(Bundle)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService#onShowSessionFailed(android.os.Bundle))
- [#onShow(Bundle, int)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int))
- [#show(Bundle, int)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#show(android.os.Bundle,%20kotlin.Int)) 

### SHOW_SOURCE_ACTIVITY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_SOURCE_ACTIVITY: Int
```

Flag for use with [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): indicates that an Activity has invoked the voice interaction service for a local interaction using [Activity.startLocalVoiceInteraction(Bundle)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startLocalVoiceInteraction(android.os.Bundle)). 

 Value: 16

### SHOW_SOURCE_APPLICATION

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_SOURCE_APPLICATION: Int
```

Flag for use with [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): indicates that the application itself has invoked the assistant. 

 Value: 8

### SHOW_SOURCE_ASSIST_GESTURE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_SOURCE_ASSIST_GESTURE: Int
```

Flag for use with [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): indicates that the session has been started from the system assist gesture. 

 Value: 4

### SHOW_SOURCE_AUTOMOTIVE_SYSTEM_UI

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_SOURCE_AUTOMOTIVE_SYSTEM_UI: Int
```

Flag for use with [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): indicates that the voice interaction service was invoked from an Android automotive system UI. 

 Value: 128

### SHOW_SOURCE_NOTIFICATION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_SOURCE_NOTIFICATION: Int
```

Flag for use with [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): indicates that the voice interaction service was invoked from a notification. 

 Value: 64

### SHOW_SOURCE_PUSH_TO_TALK

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_SOURCE_PUSH_TO_TALK: Int
```

Flag for use with [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): indicates that the voice interaction service was invoked from a physical button. 

 Value: 32

### SHOW_WITH_ASSIST

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_WITH_ASSIST: Int
```

Flag received in [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): originator requested that the session be started with assist data from the currently focused activity. 

 Value: 1

### SHOW_WITH_SCREENSHOT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_WITH_SCREENSHOT: Int
```

Flag received in [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)): originator requested that the session be started with a screen shot of the currently focused activity. 

 Value: 2

## Public constructors

### VoiceInteractionSession

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VoiceInteractionSession(context: Context!)
```  

### VoiceInteractionSession

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VoiceInteractionSession(
    context: Context!, 
    handler: Handler!)
```

## Public methods

### closeSystemDialogs

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun closeSystemDialogs(): Unit
```

Request that all system dialogs (and status bar shade etc) be closed, allowing access to the session's UI. This will*not*cause the lock screen to be dismissed. 

### dump

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dump(
    prefix: String!, 
    fd: FileDescriptor!, 
    writer: PrintWriter!, 
    args: Array<String!>!
): Unit
```

Print the Service's state into the given stream. This gets invoked by [VoiceInteractionSessionService](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSessionService) when its Service [android.app.Service#dump](https://developer.android.com/reference/kotlin/android/app/Service.html#dump(java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array))method is called.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Text to print at the front of each line. |
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!:The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!:The PrintWriter to which you should dump your state. This will be closed for you after you return. |
| --- | --- |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:additional arguments to the dump request. |

### finish

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finish(): Unit
```

Finish the session. This completely destroys the session -- the next time it is shown, an entirely new one will be created. You do not normally call this function; instead, use [hide](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#hide())and allow the system to destroy your session if it needs its RAM. 

### getContext

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(): Context!
```  

### getDisabledShowContext

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisabledShowContext(): Int
```

Equivalent to [VoiceInteractionService.getDisabledShowContext](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService#getDisabledShowContext()). 

### getLayoutInflater

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLayoutInflater(): LayoutInflater!
```

Convenience for inflating views. 

### getUserDisabledShowContext

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUserDisabledShowContext(): Int
```

Return which show context flags have been disabled by the user through the system settings UI, so the session will never get this data. Returned flags are any combination of [VoiceInteractionSession.SHOW_WITH_ASSIST](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_WITH_ASSIST:kotlin.Int) and [VoiceInteractionSession.SHOW_WITH_SCREENSHOT](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_WITH_SCREENSHOT:kotlin.Int). Note that this only tells you about global user settings, not about restrictions that may be applied contextual based on the current application the user is in or other transient states. 

### getWindow

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWindow(): Dialog!
```

Retrieve the window being used to show the session's UI. 

### hide

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hide(): Unit
```

Hide the session's UI, if currently shown. Call this when you are done with your user interaction. 

### onAssistStructureFailure

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAssistStructureFailure(failure: Throwable!): Unit
```

Called when there has been a failure transferring the [AssistStructure](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.html#) to the assistant. This may happen, for example, if the data is too large and results in an out of memory exception, the data has been cleared during transferring due to the new incoming assist data, or the client has provided corrupt data. This will be called immediately before #onHandleAssist and the AssistStructure supplied there afterwards will be null.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `failure` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The failure exception that was thrown when building the [AssistStructure](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.html#). |

### onBackPressed

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onBackPressed(): Unit
```

Called when the user presses the back button while focus is in the session UI. Note that this will only happen if the session UI has requested input focus in its window; otherwise, the back key will go to whatever window has focus and do whatever behavior it normally has there. The default implementation simply calls [hide](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#hide()). 

### onCancelRequest

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCancelRequest(request: VoiceInteractionSession.Request!): Unit
```

Called when the [android.app.VoiceInteractor](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.html#) has asked to cancel a [Request](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.Request) that was previously delivered to [onRequestConfirmation](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestConfirmation(android.service.voice.VoiceInteractionSession.ConfirmationRequest)), [onRequestPickOption](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestPickOption(android.service.voice.VoiceInteractionSession.PickOptionRequest)), [onRequestCompleteVoice](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestCompleteVoice(android.service.voice.VoiceInteractionSession.CompleteVoiceRequest)), [onRequestAbortVoice](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestAbortVoice(android.service.voice.VoiceInteractionSession.AbortVoiceRequest)), or [onRequestCommand](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestCommand(android.service.voice.VoiceInteractionSession.CommandRequest)).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [VoiceInteractionSession.Request](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.Request)!:The request that is being canceled. |

### onCloseSystemDialogs

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCloseSystemDialogs(): Unit
```

Sessions automatically watch for requests that all system UI be closed (such as when the user presses HOME), which will appear here. The default implementation always calls [hide](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#hide()). 

### onComputeInsets

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onComputeInsets(outInsets: VoiceInteractionSession.Insets!): Unit
```

Compute the interesting insets into your UI. The default implementation sets [outInsets.contentInsets.top](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.Insets#contentInsets:android.graphics.Rect) to the height of the window, meaning it should not adjust content underneath. The default touchable insets are [Insets.TOUCHABLE_INSETS_FRAME](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.Insets#TOUCHABLE_INSETS_FRAME:kotlin.Int), meaning it consumes all touch events within its window frame.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outInsets` | [VoiceInteractionSession.Insets](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.Insets)!:Fill in with the current UI insets. |

### onConfigurationChanged

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onConfigurationChanged(newConfig: Configuration): Unit
```

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newConfig` | [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#):The new device configuration. This value cannot be`null`. |

### onCreate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreate(): Unit
```

Initiatize a new session. At this point you don't know exactly what this session will be used for; you will find that out in [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)). 

### onCreateContentView

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateContentView(): View!
```

Hook in which to create the session's UI. 

### onDestroy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDestroy(): Unit
```

Last callback to the session as it is being finished. 

### onDirectActionsInvalidated

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDirectActionsInvalidated(activityId: VoiceInteractionSession.ActivityId): Unit
```

Called when the direct actions are invalidated.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `activityId` | [VoiceInteractionSession.ActivityId](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.ActivityId):This value cannot be`null`. |

### onGetSupportedCommands

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGetSupportedCommands(commands: Array<String!>!): BooleanArray!
```

Request to query for what extended commands the session supports.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `commands` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:An array of commands that are being queried. |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)! | Return an array of booleans indicating which of each entry in the command array is supported. A true entry in the array indicates the command is supported; false indicates it is not. The default implementation returns an array of all false entries. |

### onHandleAssist

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onHandleAssist(
    data: Bundle?, 
    structure: AssistStructure?, 
    content: AssistContent?
): Unit
```

**Deprecated:** *use [onHandleAssist(android.service.voice.VoiceInteractionSession.AssistState)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onHandleAssist(android.service.voice.VoiceInteractionSession.AssistState))*

Called to receive data from the application that the user was currently viewing when - \* an assist session is started. If the original show request did not specify [SHOW_WITH_ASSIST](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_WITH_ASSIST:kotlin.Int), this method will not be called.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Arbitrary data supplied by the app through [Activity.onProvideAssistData](https://developer.android.com/reference/kotlin/android/app/Activity.html#onProvideAssistData(android.os.Bundle)). May be null if assist data has been disabled by the user or device policy. |
| `structure` | [AssistStructure](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.html#)?:If available, the structure definition of all windows currently displayed by the app. May be null if assist data has been disabled by the user or device policy; will be an empty stub if the application has disabled assist by marking its window as secure. |
| `content` | [AssistContent](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent.html#)?:Additional content data supplied by the app through [Activity.onProvideAssistContent](https://developer.android.com/reference/kotlin/android/app/Activity.html#onProvideAssistContent(android.app.assist.AssistContent)). May be null if assist data has been disabled by the user or device policy; will not be automatically filled in with data from the app if the app has marked its window as secure. |
| --- | --- |

### onHandleAssist

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onHandleAssist(state: VoiceInteractionSession.AssistState): Unit
```

Called to receive data from the application that the user was currently viewing when an assist session is started. If the original show request did not specify [SHOW_WITH_ASSIST](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_WITH_ASSIST:kotlin.Int), [AssistState](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.AssistState) parameter will only provide [ActivityId](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.ActivityId). If there was a failure to write the assist data to [AssistStructure](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.html#), the [AssistState.getAssistStructure()](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.AssistState#getAssistStructure())will return null.

This method is called for all activities along with an index and count that indicates which activity the data is for.`index`will be between 0 and`count`-1 and this method is called once for each activity in no particular order. The`count`indicates how many activities to expect assist data for, including the top focused one. The focused activity can be determined by calling [AssistState.isFocused()](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.AssistState#isFocused()).

To be responsive to assist requests, process assist data as soon as it is received, without waiting for all queued activities to return assist data.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [VoiceInteractionSession.AssistState](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.AssistState):The state object capturing the state of an activity. This value cannot be`null`. |

### onHandleAssistSecondary

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onHandleAssistSecondary(
    data: Bundle?, 
    structure: AssistStructure?, 
    content: AssistContent?, 
    index: Int, 
    count: Int
): Unit
```

**Deprecated:** *use [onHandleAssist(android.service.voice.VoiceInteractionSession.AssistState)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onHandleAssist(android.service.voice.VoiceInteractionSession.AssistState))*

Called to receive data from other applications that the user was or is interacting with, that are currently on the screen in a multi-window display environment, not including the currently focused activity. This could be a free-form window, a picture-in-picture window, or another window in a split-screen display.

This method is very similar to #onHandleAssist except that it is called for additional non-focused activities along with an index and count that indicates which additional activity the data is for.`index`will be between 1 and`count`-1 and this method is called once for each additional window, in no particular order. The`count`indicates how many windows to expect assist data for, including the top focused activity, which continues to be returned via #onHandleAssist.

To be responsive to assist requests, process assist data as soon as it is received, without waiting for all queued activities to return assist data.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Arbitrary data supplied by the app through [Activity.onProvideAssistData](https://developer.android.com/reference/kotlin/android/app/Activity.html#onProvideAssistData(android.os.Bundle)). May be null if assist data has been disabled by the user or device policy. |
| `structure` | [AssistStructure](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.html#)?:If available, the structure definition of all windows currently displayed by the app. May be null if assist data has been disabled by the user or device policy; will be an empty stub if the application has disabled assist by marking its window as secure. |
| `content` | [AssistContent](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent.html#)?:Additional content data supplied by the app through [Activity.onProvideAssistContent](https://developer.android.com/reference/kotlin/android/app/Activity.html#onProvideAssistContent(android.app.assist.AssistContent)). May be null if assist data has been disabled by the user or device policy; will not be automatically filled in with data from the app if the app has marked its window as secure. |
| --- | --- |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the additional activity that this data is for. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the total number of additional activities for which the assist data is being returned, including the focused activity that is returned via #onHandleAssist. |

### onHandleScreenshot

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onHandleScreenshot(screenshot: Bitmap?): Unit
```

Called to receive a screenshot of what the user was currently viewing when an assist session is started. May be null if screenshots are disabled by the user, policy, or application. If the original show request did not specify [SHOW_WITH_SCREENSHOT](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_WITH_SCREENSHOT:kotlin.Int), this method will not be called.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------|
| `screenshot` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)?:This value may be`null`. |

### onHide

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onHide(): Unit
```

Called immediately after stopping to show the session UI. 

### onKeyDown

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyDown(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!:Description of the key event. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyLongPress

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyLongPress(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!:Description of the key event. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyMultiple

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyMultiple(
    keyCode: Int, 
    count: Int, 
    event: KeyEvent!
): Boolean
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of pairs as returned by event.getRepeatCount(). |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!:Description of the key event. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyUp

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyUp(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!:Description of the key event. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onLockscreenShown

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onLockscreenShown(): Unit
```

Called when the lockscreen was shown. 

### onLowMemory

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onLowMemory(): Unit
```  

### onPrepareShow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPrepareShow(
    args: Bundle!, 
    showFlags: Int
): Unit
```

Called prior to [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int))before any UI setup has occurred. Not generally useful.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:The arguments that were supplied to [VoiceInteractionService.showSession](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService#showSession(android.os.Bundle,%20kotlin.Int)). |
| `showFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The show flags originally provided to [VoiceInteractionService.showSession](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService#showSession(android.os.Bundle,%20kotlin.Int)). |

### onRequestAbortVoice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRequestAbortVoice(request: VoiceInteractionSession.AbortVoiceRequest!): Unit
```

Request to abort the voice interaction session because the voice activity can not complete its interaction using voice. Corresponds to [VoiceInteractor.AbortVoiceRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.AbortVoiceRequest.html#). The default implementation just sends an empty confirmation back to allow the activity to exit.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [VoiceInteractionSession.AbortVoiceRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.AbortVoiceRequest)!:The active request. |

### onRequestCommand

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRequestCommand(request: VoiceInteractionSession.CommandRequest!): Unit
```

Process an arbitrary extended command from the caller, corresponding to a [VoiceInteractor.CommandRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.CommandRequest.html#).

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [VoiceInteractionSession.CommandRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.CommandRequest)!:The active request. |

### onRequestCompleteVoice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRequestCompleteVoice(request: VoiceInteractionSession.CompleteVoiceRequest!): Unit
```

Request to complete the voice interaction session because the voice activity successfully completed its interaction using voice. Corresponds to [VoiceInteractor.CompleteVoiceRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.CompleteVoiceRequest.html#). The default implementation just sends an empty confirmation back to allow the activity to exit.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [VoiceInteractionSession.CompleteVoiceRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.CompleteVoiceRequest)!:The active request. |

### onRequestConfirmation

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRequestConfirmation(request: VoiceInteractionSession.ConfirmationRequest!): Unit
```

Request to confirm with the user before proceeding with an unrecoverable operation, corresponding to a [VoiceInteractor.ConfirmationRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.ConfirmationRequest.html#).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [VoiceInteractionSession.ConfirmationRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.ConfirmationRequest)!:The active request. |

### onRequestPickOption

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRequestPickOption(request: VoiceInteractionSession.PickOptionRequest!): Unit
```

Request for the user to pick one of N options, corresponding to a [VoiceInteractor.PickOptionRequest](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.PickOptionRequest.html#).

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [VoiceInteractionSession.PickOptionRequest](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.PickOptionRequest)!:The active request. |

### onShow

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onShow(
    args: Bundle?, 
    showFlags: Int
): Unit
```

Called when the session UI is going to be shown. This is called after [onCreateContentView](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onCreateContentView())(if the session's content UI needed to be created) and immediately prior to the window being shown. This may be called while the window is already shown, if a show request has come in while it is shown, to allow you to update the UI to match the new show arguments.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:The arguments that were supplied to [VoiceInteractionService.showSession](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService#showSession(android.os.Bundle,%20kotlin.Int)). Some example keys include : - invocation_type - invocation_phone_state - [KEY_SHOW_SESSION_ID](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#KEY_SHOW_SESSION_ID:kotlin.String) - invocation_time_ms - Intent.EXTRA_TIME ("android.intent.extra.TIME") indicating timing in milliseconds of the KeyEvent that triggered Assistant - Intent.EXTRA_ASSIST_INPUT_DEVICE_ID (android.intent.extra.ASSIST_INPUT_DEVICE_ID) referring to the device that sent the request - [KEY_FOREGROUND_ACTIVITIES](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#KEY_FOREGROUND_ACTIVITIES:kotlin.String) provides foreground activities of up coming onHandleAssist/onHandleScreenshot calls earlier. This is only populated if session was requested with VoiceInteractionSession.SHOW_WITH_ASSIST show flag. - Starting from Android 14, the system will add [KEY_SHOW_SESSION_ID](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#KEY_SHOW_SESSION_ID:kotlin.String), the Bundle is not null. But the application should handle null case before Android 14. |
| `showFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The show flags originally provided to [VoiceInteractionService.showSession](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService#showSession(android.os.Bundle,%20kotlin.Int)). |

### onTaskFinished

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTaskFinished(
    intent: Intent!, 
    taskId: Int
): Unit
```

Called when the last activity of a task initiated by [startVoiceActivity(android.content.Intent)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#startVoiceActivity(android.content.Intent))has finished. The default implementation calls [finish()](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#finish())on the assumption that this represents the completion of a voice action. You can override the implementation if you would like a different behavior.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The original [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) supplied to [startVoiceActivity(android.content.Intent)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#startVoiceActivity(android.content.Intent)). |
| `taskId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique ID of the finished task. |

### onTaskStarted

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTaskStarted(
    intent: Intent!, 
    taskId: Int
): Unit
```

Called when a task initiated by [startVoiceActivity(android.content.Intent)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#startVoiceActivity(android.content.Intent))has actually started.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The original [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) supplied to [startVoiceActivity(android.content.Intent)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#startVoiceActivity(android.content.Intent)). |
| `taskId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique ID of the now running task. |

### onTrimMemory

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTrimMemory(level: Int): Unit
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The context of the trim, giving a hint of the amount of trimming the application may like to perform. Value is [android.content.ComponentCallbacks2#TRIM_MEMORY_COMPLETE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_BACKGROUND](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_UI_HIDDEN](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_RUNNING_CRITICAL](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_RUNNING_LOW](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int), or [android.content.ComponentCallbacks2#TRIM_MEMORY_RUNNING_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int) |

### performDirectAction

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun performDirectAction(
    action: DirectAction, 
    extras: Bundle?, 
    cancellationSignal: CancellationSignal?, 
    resultExecutor: Executor, 
    resultListener: Consumer<Bundle!>
): Unit
```

Asks that an action be performed by the app. This will send a request to the app which provided this action.

An action could take time to execute and the result is provided asynchronously via a callback. If the action is taking longer and you want to cancel its execution you can pass in a cancellation signal through which to notify the app to abort the action.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [DirectAction](https://developer.android.com/reference/kotlin/android/app/DirectAction.html#):The action to be performed. This value cannot be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Any optional extras sent to the app as part of the request This value may be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or`null`if none. |
| --- | --- |
| `resultExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The handler to receive the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `resultListener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>:The callback to receive the response. This value cannot be`null`. |

**See Also**

- [#requestDirectActions(ActivityId, CancellationSignal, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#requestDirectActions(android.service.voice.VoiceInteractionSession.ActivityId,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))
- [android.app.Activity#onGetDirectActions(CancellationSignal, Consumer)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onGetDirectActions(android.os.CancellationSignal,%20java.util.function.Consumer)) 

### registerVisibleActivityCallback

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerVisibleActivityCallback(
    executor: Executor, 
    callback: VoiceInteractionSession.VisibleActivityCallback
): Unit
```

Registers a callback that will be notified when visible activities have been changed. Note: The [VisibleActivityCallback.onVisible(VisibleActivityInfo)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.VisibleActivityCallback#onVisible(android.service.voice.VisibleActivityInfo))will be called immediately with current visible activities when the callback is registered for the first time. If the callback is already registered, this method does nothing.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor which will be used to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [VoiceInteractionSession.VisibleActivityCallback](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.VisibleActivityCallback):The callback to receive the response. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------|
| `java.lang.IllegalStateException` | if calling this method before onCreate(). |

### requestDirectActions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requestDirectActions(
    activityId: VoiceInteractionSession.ActivityId, 
    cancellationSignal: CancellationSignal?, 
    resultExecutor: Executor, 
    callback: Consumer<MutableList<DirectAction!>!>
): Unit
```

Requests a list of supported actions from an app.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `activityId` | [VoiceInteractionSession.ActivityId](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.ActivityId):Ths activity id of the app to get the actions from. This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or`null`if none. |
| `resultExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The handler to receive the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [DirectAction](https://developer.android.com/reference/kotlin/android/app/DirectAction.html#)!\>!\>:The callback to receive the response. This value cannot be`null`. |

### setContentView

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentView(view: View!): Unit
```  

### setDisabledShowContext

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDisabledShowContext(flags: Int): Unit
```

Equivalent to [VoiceInteractionService.setDisabledShowContext(int)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService#setDisabledShowContext(kotlin.Int)). 

### setKeepAwake

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setKeepAwake(keepAwake: Boolean): Unit
```

Set whether this session will keep the device awake while it is running a voice activity. By default, the system holds a wake lock for it while in this state, so that it can work even if the screen is off. Setting this to false removes that wake lock, allowing the CPU to go to sleep. This is typically used if the session decides it has been waiting too long for a response from the user and doesn't want to let this continue to drain the battery.

Passing false here will release the wake lock, and you can call later with true to re-acquire it. It will also be automatically re-acquired for you each time you start a new voice activity task -- that is when you call [startVoiceActivity](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#startVoiceActivity(android.content.Intent)). 

### setTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTheme(theme: Int): Unit
```

You can call this to customize the theme used by your IME's window. This must be set before [onCreate](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onCreate()), so you will typically call it in your constructor with the resource ID of your custom theme. 

### setUiEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setUiEnabled(enabled: Boolean): Unit
```

Control whether the UI layer for this session is enabled. It is enabled by default. If set to false, you will not be able to provide a UI through [onCreateContentView()](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onCreateContentView()). 

### show

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun show(
    args: Bundle!, 
    flags: Int
): Unit
```

Show the UI for this session. This asks the system to go through the process of showing your UI, which will eventually culminate in [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)). This is similar to calling [VoiceInteractionService.showSession](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService#showSession(android.os.Bundle,%20kotlin.Int)).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Arbitrary arguments that will be propagated [onShow](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onShow(android.os.Bundle,%20kotlin.Int)). |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Indicates additional optional behavior that should be performed. May be any combination of [VoiceInteractionSession.SHOW_WITH_ASSIST](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_WITH_ASSIST:kotlin.Int) and [VoiceInteractionSession.SHOW_WITH_SCREENSHOT](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#SHOW_WITH_SCREENSHOT:kotlin.Int) to request that the system generate and deliver assist data on the current foreground app as part of showing the session UI. |

### startAssistantActivity

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startAssistantActivity(intent: Intent!): Unit
```

Ask that a new assistant activity be started. This will create a new task in the in activity manager: this means that [Intent.FLAG_ACTIVITY_NEW_TASK](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int) will be set for you to make it a new task.

The newly started activity will be displayed on top of other activities in the system in a new layer that is not affected by multi-window mode. Tasks started from this activity will go into the normal activity layer and not this new layer.

By default, the system will create a window for the UI for this session. If you are using an assistant activity instead, then you can disable the window creation by calling [setUiEnabled](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#setUiEnabled(kotlin.Boolean))in [onPrepareShow(android.os.Bundle,int)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onPrepareShow(android.os.Bundle,%20kotlin.Int)).
NOTE: if the app would like to override some options to start the Activity, use [startAssistantActivity(android.content.Intent,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#startAssistantActivity(android.content.Intent,%20android.os.Bundle))instead. 

### startAssistantActivity

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startAssistantActivity(
    intent: Intent, 
    bundle: Bundle
): Unit
```

Ask that a new assistant activity be started. This will create a new task in the in activity manager: this means that [Intent.FLAG_ACTIVITY_NEW_TASK](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int) will be set for you to make it a new task.

The newly started activity will be displayed on top of other activities in the system in a new layer that is not affected by multi-window mode. Tasks started from this activity will go into the normal activity layer and not this new layer.

By default, the system will create a window for the UI for this session. If you are using an assistant activity instead, then you can disable the window creation by calling [setUiEnabled](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#setUiEnabled(kotlin.Boolean))in [onPrepareShow(android.os.Bundle,int)](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onPrepareShow(android.os.Bundle,%20kotlin.Int)).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#):the intent used to start an assistant activity This value cannot be`null`. |
| `bundle` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):Additional options for how the Activity should be started. See [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#) for how to build the Bundle supplied here. This value cannot be`null`. |

### startVoiceActivity

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startVoiceActivity(intent: Intent!): Unit
```

Ask that a new activity be started for voice interaction. This will create a new dedicated task in the activity manager for this voice interaction session; this means that [Intent.FLAG_ACTIVITY_NEW_TASK](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int) will be set for you to make it a new task.

The newly started activity will be displayed to the user in a special way, as a layer under the voice interaction UI.

As the voice activity runs, it can retrieve a [android.app.VoiceInteractor](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.html#) through which it can perform voice interactions through your session. These requests for voice interactions will appear as callbacks on [onGetSupportedCommands](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onGetSupportedCommands(kotlin.Array)), [onRequestConfirmation](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestConfirmation(android.service.voice.VoiceInteractionSession.ConfirmationRequest)), [onRequestPickOption](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestPickOption(android.service.voice.VoiceInteractionSession.PickOptionRequest)), [onRequestCompleteVoice](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestCompleteVoice(android.service.voice.VoiceInteractionSession.CompleteVoiceRequest)), [onRequestAbortVoice](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestAbortVoice(android.service.voice.VoiceInteractionSession.AbortVoiceRequest)), or [onRequestCommand](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onRequestCommand(android.service.voice.VoiceInteractionSession.CommandRequest))

You will receive a call to [onTaskStarted](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onTaskStarted(android.content.Intent,%20kotlin.Int))when the task starts up and [onTaskFinished](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession#onTaskFinished(android.content.Intent,%20kotlin.Int))when the last activity has finished.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The Intent to start this voice interaction. The given Intent will always have [Intent.CATEGORY_VOICE](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_VOICE:kotlin.String) added to it, since this is part of a voice interaction. |

### unregisterVisibleActivityCallback

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterVisibleActivityCallback(callback: VoiceInteractionSession.VisibleActivityCallback): Unit
```

Unregisters the callback.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [VoiceInteractionSession.VisibleActivityCallback](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.VisibleActivityCallback):The callback to receive the response. This value cannot be`null`. |
