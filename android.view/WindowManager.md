Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowManager

```
interface WindowManager : ViewManager
```

| [android.view.WindowManager](../android/view/WindowManager.md) |

The interface that apps use to talk to the window manager.

Each window manager instance is bound to a `https://developer.android.com/reference/kotlin/android/view/Display`. To obtain the `WindowManager` associated with a display, call `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(android.view.Display,%20kotlin.Int,%20android.os.Bundle)` to get the display's UI context, then call `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` or `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(java.lang.Class)` on the UI context.

The simplest way to show a window on a particular display is to create a `https://developer.android.com/reference/kotlin/android/app/Presentation.html#`, which automatically obtains a `WindowManager` and context for the display.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/view/WindowManager.BadTokenException` Exception that is thrown when trying to add view whose `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams` `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#token:android.os.IBinder` is invalid. |
| | `https://developer.android.com/reference/kotlin/android/view/WindowManager.DisplayEngagementModeState` A class that holds information about the display engagement mode. |
| open | `https://developer.android.com/reference/kotlin/android/view/WindowManager.InvalidDisplayException` Exception that is thrown when calling `https://developer.android.com/reference/kotlin/android/view/ViewManager#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)` to a secondary display that cannot be found. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams` <br /> |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#COMPAT_SMALL_COVER_SCREEN_OPT_IN:kotlin.Int` Value applicable for the `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_SMALL_COVER_SCREEN:kotlin.String` property to provide a signal to the system that an application or its specific activities explicitly opt into being displayed on small cover screens on flippable style foldable devices that measure at least 1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#ENGAGEMENT_CONTROL_FLAG_SUSTAIN_VISUALS:kotlin.Int` Flags for requesting engagement visual state to be sustained. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#ENGAGEMENT_MODE_FLAG_AUDIO_ON:kotlin.Int` A flag indicating the engagement mode includes an audio presentation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#ENGAGEMENT_MODE_FLAG_VISUALS_ON:kotlin.Int` A flag indicating the engagement mode includes a visual presentation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_ACTIVITY_EMBEDDING_ALLOW_SYSTEM_OVERRIDE:kotlin.String` Application-level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag that specifies whether OEMs are permitted to provide activity embedding split-rule configurations on behalf of the app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_ACTIVITY_EMBEDDING_SPLITS_ENABLED:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` that an app can specify to inform the system that the app is activity embedding split feature enabled. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_CAMERA_COMPAT_ALLOW_FORCE_ROTATION:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app should be excluded from the camera compatibility force rotation treatment. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_CAMERA_COMPAT_ALLOW_REFRESH:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app should be excluded from the activity "refresh" after the camera compatibility force rotation treatment. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_CAMERA_COMPAT_ALLOW_SIMULATE_REQUESTED_ORIENTATION:kotlin.String` Application-level \[PackageManager\]\[android. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_CAMERA_COMPAT_ENABLE_REFRESH_VIA_PAUSE:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the activity should be or shouldn't be "refreshed" after the camera compatibility force rotation treatment using "paused -\> resumed" cycle rather than "stopped -\> resumed". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_DISPLAY_ORIENTATION_OVERRIDE:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app should be opted-out from the compatibility override that fixes display orientation to landscape natural orientation when an activity is fullscreen. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_EXCLUDE_CAPTION_INSETS:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that it needs to be opted-out from the compatibility treatment that sandboxes the `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` API when caption insets are force consumed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_IGNORING_ORIENTATION_REQUEST_WHEN_LOOP_DETECTED:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app can be opted-out from the compatibility treatment that avoids `https://developer.android.com/reference/kotlin/android/app/Activity.html#setRequestedOrientation(kotlin.Int)` loops. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_MIN_ASPECT_RATIO_OVERRIDE:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app should be opted-out from the compatibility override that changes the min aspect ratio. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_ORIENTATION_OVERRIDE:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app should be excluded from the compatibility override for orientation set by the device manufacturer. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_RESIZEABLE_ACTIVITY_OVERRIDES:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app should be opted-out from the compatibility overrides that change the resizability of the app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_SANDBOXING_VIEW_BOUNDS_APIS:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that it needs to be opted-out from the compatibility treatment that sandboxes the `https://developer.android.com/reference/kotlin/android/view/View` API. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_SMALL_COVER_SCREEN:kotlin.String` Application or Activity level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` to provide any preferences for showing all or specific Activities on small cover displays of foldable style devices. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_FULLSCREEN_OVERRIDE:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag that (when set to false) informs the system the app has opted out of the full-screen option of the user aspect ratio compatibility override settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_OVERRIDE:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag that (when set to false) informs the system the app has opted out of the user-facing aspect ratio compatibility override. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ENABLE_FAKE_FOCUS:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the application can be opted-in or opted-out from the compatibility treatment that enables sending a fake focus event for unfocused resumed split-screen activities. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_IGNORE_REQUESTED_ORIENTATION:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app can be opted-in or opted-out from the compatibility treatment that avoids `https://developer.android.com/reference/kotlin/android/app/Activity.html#setRequestedOrientation(kotlin.Int)` loops. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_SUPPORTS_MULTI_INSTANCE_SYSTEM_UI:kotlin.String` Activity or Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to declare that System UI should be shown for this app/component to allow it to be launched as multiple instances. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#SCREEN_RECORDING_STATE_NOT_VISIBLE:kotlin.Int` Indicates the app that registered the callback is not visible in screen recording. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#SCREEN_RECORDING_STATE_VISIBLE:kotlin.Int` Indicates the app that registered the callback is visible in screen recording. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#addCrossWindowBlurEnabledListener(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>)` Adds a listener, which will be called when cross-window blurs are enabled/disabled at runtime. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#addCrossWindowBlurEnabledListener(java.util.function.Consumer)(listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>)` Adds a listener, which will be called when cross-window blurs are enabled/disabled at runtime. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#addProposedRotationListener(java.util.concurrent.Executor,%20java.util.function.IntConsumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)` Adds a listener to start monitoring the proposed rotation of the current associated context. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#addScreenRecordingCallback(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>)` Adds a screen recording callback. |
| open [WindowMetrics](../android/view/WindowMetrics.md) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#getCurrentWindowMetrics()()` Returns the `https://developer.android.com/reference/kotlin/android/view/WindowMetrics` according to the current system state. |
| abstract [Display](../android/view/Display.md)! | `https://developer.android.com/reference/kotlin/android/view/WindowManager#getDefaultDisplay()()` Returns the `https://developer.android.com/reference/kotlin/android/view/Display` upon which this `https://developer.android.com/reference/kotlin/android/view/WindowManager#` instance will create new windows. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#getDisplayEngagementMode(kotlin.Int)(displayId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the user engagement mode for a specific display. |
| open [WindowMetrics](../android/view/WindowMetrics.md) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#getMaximumWindowMetrics()()` Returns the largest `https://developer.android.com/reference/kotlin/android/view/WindowMetrics` an app may expect in the current system state. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#isCrossWindowBlurEnabled()()` Returns whether cross-window blur is currently enabled. |
| --- | --- |
| open [InputTransferToken](../android/window/InputTransferToken.md) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#registerBatchedSurfaceControlInputReceiver(android.window.InputTransferToken,%20android.view.SurfaceControl,%20android.view.Choreographer,%20android.view.SurfaceControlInputReceiver)(hostInputTransferToken: https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#, surfaceControl: https://developer.android.com/reference/kotlin/android/view/SurfaceControl, choreographer: https://developer.android.com/reference/kotlin/android/view/Choreographer, receiver: https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver)` Registers a `https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver` for a `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` that will receive batched input event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#registerDisplayEngagementModeCallback(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/view/WindowManager.DisplayEngagementModeState!>)` Registers a callback for display engagement mode changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#registerTrustedPresentationListener(android.os.IBinder,%20android.window.TrustedPresentationThresholds,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(window: https://developer.android.com/reference/kotlin/android/os/IBinder.html#, thresholds: https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>)` Sets a callback to receive feedback about the presentation of a `https://developer.android.com/reference/kotlin/android/view/Window`. |
| --- | --- |
| open [InputTransferToken](../android/window/InputTransferToken.md) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#registerUnbatchedSurfaceControlInputReceiver(android.window.InputTransferToken,%20android.view.SurfaceControl,%20android.os.Looper,%20android.view.SurfaceControlInputReceiver)(hostInputTransferToken: https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#, surfaceControl: https://developer.android.com/reference/kotlin/android/view/SurfaceControl, looper: https://developer.android.com/reference/kotlin/android/os/Looper.html#, receiver: https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver)` Registers a `https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver` for a `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` that will receive every input event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#removeCrossWindowBlurEnabledListener(java.util.function.Consumer)(listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>)` Removes a listener, previously added with #addCrossWindowBlurEnabledListener |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#removeProposedRotationListener(java.util.function.IntConsumer)(listener: https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)` Removes a listener, previously added with `https://developer.android.com/reference/kotlin/android/view/WindowManager#addProposedRotationListener(java.util.concurrent.Executor,%20java.util.function.IntConsumer)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#removeScreenRecordingCallback(java.util.function.Consumer)(callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>)` Removes a screen recording callback. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#removeViewImmediate(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View!)` Special variation of `https://developer.android.com/reference/kotlin/android/view/ViewManager#removeView(android.view.View)` that immediately invokes the given view hierarchy's `https://developer.android.com/reference/kotlin/android/view/View#onDetachedFromWindow()` methods before returning. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#requestEngagementControlState(kotlin.Int)(engagementControlFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Requests an engagement control state. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#transferTouchGesture(android.window.InputTransferToken,%20android.window.InputTransferToken)(transferFromToken: https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#, transferToToken: https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#)` Transfer the currently in progress touch gesture from the transferFromToken to the transferToToken. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#unregisterDisplayEngagementModeCallback(java.util.function.Consumer)(callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/view/WindowManager.DisplayEngagementModeState!>)` Unregisters a callback for display engagement mode changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#unregisterSurfaceControlInputReceiver(android.view.SurfaceControl)(surfaceControl: https://developer.android.com/reference/kotlin/android/view/SurfaceControl)` Unregisters and cleans up the registered `https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver` for the specified token. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/WindowManager#unregisterTrustedPresentationListener(java.util.function.Consumer)(listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>)` Removes a presentation listener associated with a window. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/view/ViewManager` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewManager#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)(view: https://developer.android.com/reference/kotlin/android/view/View!, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!)`

Assign the passed LayoutParams to the passed View and add the view to the window.

Throws `https://developer.android.com/reference/kotlin/android/view/WindowManager.BadTokenException` for certain programming errors, such as adding a second view to a window without removing the first view.

Throws `https://developer.android.com/reference/kotlin/android/view/WindowManager.InvalidDisplayException` if the window is on a secondary `https://developer.android.com/reference/kotlin/android/view/Display` and the specified display can't be found (see `https://developer.android.com/reference/kotlin/android/app/Presentation.html#`).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewManager#removeView(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewManager#updateViewLayout(android.view.View,%20android.view.ViewGroup.LayoutParams)(view: https://developer.android.com/reference/kotlin/android/view/View!, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!)`

<br />

## Constants

### COMPAT_SMALL_COVER_SCREEN_OPT_IN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMPAT_SMALL_COVER_SCREEN_OPT_IN: Int
```

Value applicable for the `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_SMALL_COVER_SCREEN:kotlin.String` property to provide a signal to the system that an application or its specific activities explicitly opt into being displayed on small cover screens on flippable style foldable devices that measure at least 1.5 inches up to 2.2 inches for the shorter dimension and at least 2.4 inches up to 3.4 inches for the longer dimension. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/view/WindowManager#COMPAT_SMALL_COVER_SCREEN_OPT_IN:kotlin.Int`

<br />

 Value: 1

### ENGAGEMENT_CONTROL_FLAG_SUSTAIN_VISUALS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENGAGEMENT_CONTROL_FLAG_SUSTAIN_VISUALS: Int
```

Flags for requesting engagement visual state to be sustained.

 Value: 1

### ENGAGEMENT_MODE_FLAG_AUDIO_ON

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENGAGEMENT_MODE_FLAG_AUDIO_ON: Int
```

A flag indicating the engagement mode includes an audio presentation. This can be set with or without `https://developer.android.com/reference/kotlin/android/view/WindowManager#ENGAGEMENT_MODE_FLAG_VISUALS_ON:kotlin.Int`. When set without, it signifies an audio-only experience. This should be kept in sync with

 Value: 2

**See Also**

### ENGAGEMENT_MODE_FLAG_VISUALS_ON

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENGAGEMENT_MODE_FLAG_VISUALS_ON: Int
```

A flag indicating the engagement mode includes a visual presentation. When this flag is set, it means the user can visually see the app UI on visible window. This should be kept in sync with

 Value: 1

**See Also**

### PROPERTY_ACTIVITY_EMBEDDING_ALLOW_SYSTEM_OVERRIDE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_ACTIVITY_EMBEDDING_ALLOW_SYSTEM_OVERRIDE: String
```

Application-level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag that specifies whether OEMs are permitted to provide activity embedding split-rule configurations on behalf of the app.

If `true`, the system is permitted to override the app's windowing behavior and implement activity embedding split rules, such as displaying activities side by side. A system override informs the app that the activity embedding APIs are disabled so the app doesn't provide its own activity embedding rules, which would conflict with the system's rules.

If `false`, the system is not permitted to override the windowing behavior of the app. Set the property to `false` if the app provides its own activity embedding split rules, or if you want to prevent the system override for any other reason.

The default value is `false`.

**Note:** Refusal to permit the system override is not enforceable. OEMs can override the app's activity embedding implementation whether or not this property is specified and set to `false`. The property is, in effect, a hint to OEMs.

OEMs can implement activity embedding on any API level. The best practice for apps is to always explicitly set this property in the app manifest file regardless of targeted API level rather than rely on the default value.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_ACTIVITY_EMBEDDING_ALLOW_SYSTEM_OVERRIDE"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_ACTIVITY_EMBEDDING_ALLOW_SYSTEM_OVERRIDE"

### PROPERTY_ACTIVITY_EMBEDDING_SPLITS_ENABLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_ACTIVITY_EMBEDDING_SPLITS_ENABLED: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` that an app can specify to inform the system that the app is activity embedding split feature enabled.

With this property, the system could provide custom behaviors for the apps that are activity embedding split feature enabled. For example, the fixed-portrait orientation requests of the activities could be ignored by the system in order to provide seamless activity embedding split experiences while holding large screen devices in landscape orientation.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_ACTIVITY_EMBEDDING_SPLITS_ENABLED"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_ACTIVITY_EMBEDDING_SPLITS_ENABLED"

### PROPERTY_CAMERA_COMPAT_ALLOW_FORCE_ROTATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_CAMERA_COMPAT_ALLOW_FORCE_ROTATION: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app should be excluded from the camera compatibility force rotation treatment.

The camera compatibility treatment aligns portrait app windows with the natural orientation of the device and landscape app windows opposite the device natural orientation. Mismatch between the orientations can lead to camera issues like a sideways or stretched viewfinder since this is one of the strongest assumptions that apps make when they implement camera previews. Since app and device natural orientations aren't guaranteed to match, the rotation can cause letterboxing. The forced rotation is triggered as soon as an app opens the camera and is removed once camera is closed.

Camera compatibility can be enabled by device manufacturers on displays that have the ignore requested orientation display setting enabled, which enables compatibility mode for fixed-orientation apps on Android 12 (API level 31) or higher. See [Device compatibility mode](https://developer.android.com/guide/practices/device-compatibility-mode) for more details.

With this property set to `true` or unset, the system may apply the force rotation treatment to fixed-orientation activities. Device manufacturers can exclude packages from the treatment using their discretion to improve display compatibility.

With this property set to `false`, the system will not apply the force rotation treatment.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_CAMERA_COMPAT_ALLOW_FORCE_ROTATION"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_CAMERA_COMPAT_ALLOW_FORCE_ROTATION"

### PROPERTY_CAMERA_COMPAT_ALLOW_REFRESH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_CAMERA_COMPAT_ALLOW_REFRESH: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app should be excluded from the activity "refresh" after the camera compatibility force rotation treatment.

The camera compatibility treatment aligns portrait app windows with the natural orientation of the device and landscape app windows opposite the device natural orientation. Mismatch between the orientations can lead to camera issues like a sideways or stretched viewfinder since this is one of the strongest assumptions that apps make when they implement camera previews. Since app and device natural orientations aren't guaranteed to match, the rotation can cause letterboxing. The forced rotation is triggered as soon as an app opens the camera and is removed once camera is closed.

Force rotation is followed by the "Refresh" of the activity by going through "resumed -\> ... -\> stopped -\> ... -\> resumed" cycle (by default) or "resumed -\> paused -\> resumed" cycle (if overridden, see `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_CAMERA_COMPAT_ENABLE_REFRESH_VIA_PAUSE:kotlin.String` for context). This allows to clear cached values in apps (e.g. display or camera rotation) that influence camera preview and can lead to sideways or stretching issues persisting even after force rotation.

The camera compatibility can be enabled by device manufacturers on displays that have the ignore requested orientation display setting enabled, which enables compatibility mode for fixed-orientation apps on Android 12 (API level 31) or higher. See [Device compatibility mode](https://developer.android.com/guide/practices/device-compatibility-mode) for more details.

With this property set to `true` or unset, the system may "refresh" activity after the force rotation treatment. Device manufacturers can exclude packages from the "refresh" using their discretion to improve display compatibility.

With this property set to `false`, the system will not "refresh" activity after the force rotation treatment.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_CAMERA_COMPAT_ALLOW_REFRESH"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_CAMERA_COMPAT_ALLOW_REFRESH"

### PROPERTY_CAMERA_COMPAT_ALLOW_SIMULATE_REQUESTED_ORIENTATION

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_CAMERA_COMPAT_ALLOW_SIMULATE_REQUESTED_ORIENTATION: String
```

Application-level \[PackageManager\]\[android.content.pm.PackageManager.Property\] tag that (when set to false) informs the system the app has opted out of the camera compatibility treatment for fixed-orientation apps, which simulates running on a portrait device, in the orientation requested by the app.

This treatment aims to mitigate camera issues on large screens, like stretched or sideways previews. It simulates running on a portrait device by:

- Letterboxing the app window,
- Cropping the camera buffer to match the app's requested orientation,
- Setting the camera sensor orientation to portrait.
- Setting the display rotation to match the app's requested orientation, given portrait natural orientation,
- Refreshes the activity to trigger new camera setup, with sandboxed values.

To opt out of the camera compatibility treatment, add this property to your app manifest and set the value to `false`.

Not setting this property at all, or setting this property to `true` has no effect.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_CAMERA_COMPAT_ALLOW_SIMULATE_REQUESTED_ORIENTATION"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_CAMERA_COMPAT_ALLOW_SIMULATE_REQUESTED_ORIENTATION"

### PROPERTY_CAMERA_COMPAT_ENABLE_REFRESH_VIA_PAUSE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_CAMERA_COMPAT_ENABLE_REFRESH_VIA_PAUSE: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the activity should be or shouldn't be "refreshed" after the camera compatibility force rotation treatment using "paused -\> resumed" cycle rather than "stopped -\> resumed".

The camera compatibility treatment aligns orientations of portrait app window and natural orientation of the device. Mismatch between the orientations can lead to camera issues like a sideways or stretched viewfinder since this is one of the strongest assumptions that apps make when they implement camera previews. Since app and natural display orientations aren't guaranteed to match, the rotation can cause letterboxing. The forced rotation is triggered as soon as app opens the camera and is removed once camera is closed.

Force rotation is followed by the "Refresh" of the activity by going through "resumed -\> ... -\> stopped -\> ... -\> resumed" cycle (by default) or "resumed -\> paused -\> resumed" cycle (if overridden by device manufacturers or using this property). This allows to clear cached values in apps (e.g., display or camera rotation) that influence camera preview and can lead to sideways or stretching issues persisting even after force rotation.

The camera compatibility can be enabled by device manufacturers on displays that have the ignore requested orientation display setting enabled, which enables compatibility mode for fixed-orientation apps on Android 12 (API level 31) or higher. See [Device compatibility mode](https://developer.android.com/guide/practices/device-compatibility-mode) for more details.

Device manufacturers can override packages to "refresh" via "resumed -\> paused -\> resumed" cycle using their discretion to improve display compatibility.

With this property set to `true`, the system will "refresh" activity after the force rotation treatment using "resumed -\> paused -\> resumed" cycle.

With this property set to `false`, the system will not "refresh" activity after the force rotation treatment using "resumed -\> paused -\> resumed" cycle even if the device manufacturer adds the corresponding override.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_CAMERA_COMPAT_ENABLE_REFRESH_VIA_PAUSE"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_CAMERA_COMPAT_ENABLE_REFRESH_VIA_PAUSE"

### PROPERTY_COMPAT_ALLOW_DISPLAY_ORIENTATION_OVERRIDE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_ALLOW_DISPLAY_ORIENTATION_OVERRIDE: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app should be opted-out from the compatibility override that fixes display orientation to landscape natural orientation when an activity is fullscreen.

When this compat override is enabled and while display is fixed to the landscape natural orientation, the orientation requested by the activity will be still respected by bounds resolution logic. For instance, if an activity requests portrait orientation, then activity appears in letterbox mode for fixed-orientation apps with the display rotated to the lanscape natural orientation.

The treatment is disabled by default but device manufacturers can enable the treatment using their discretion to improve display compatibility on displays that have the ignore orientation request display setting enabled by OEMs on the device, which enables compatibility mode for fixed-orientation apps on Android 12 (API level 31) or higher. See [Device compatibility mode](https://developer.android.com/guide/practices/device-compatibility-mode) for more details.

With this property set to `true` or unset, the system wiil use landscape display orientation when the following conditions are met:

- Natural orientation of the display is landscape
- ignore requested orientation display setting is enabled
- Activity is fullscreen.
- Device manufacturer enabled the treatment.

With this property set to `false`, device manufacturer per-app override for display orientation won't be applied.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_COMPAT_ALLOW_DISPLAY_ORIENTATION_OVERRIDE"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_COMPAT_ALLOW_DISPLAY_ORIENTATION_OVERRIDE"

### PROPERTY_COMPAT_ALLOW_EXCLUDE_CAPTION_INSETS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_ALLOW_EXCLUDE_CAPTION_INSETS: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that it needs to be opted-out from the compatibility treatment that sandboxes the `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` API when caption insets are force consumed.

The treatment can be enabled by device manufacturers for applications that don't handle consumption of `https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#captionBar()` insets which can lead to top or bottom UI elements being cropped. The treatment will sandbox `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#screenHeightDp:kotlin.Int` to exclude caption insets.

Setting this property to `false` informs the system that the application must be opted-out from the exclude caption insets from app bounds treatment even if the device manufacturer has opted the app into the treatment.

Not setting this property at all, or setting this property to `true` has no effect.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_COMPAT_ALLOW_EXCLUDE_CAPTION_INSETS"
      android:value="false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_COMPAT_ALLOW_EXCLUDE_CAPTION_INSETS"

### PROPERTY_COMPAT_ALLOW_IGNORING_ORIENTATION_REQUEST_WHEN_LOOP_DETECTED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_ALLOW_IGNORING_ORIENTATION_REQUEST_WHEN_LOOP_DETECTED: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app can be opted-out from the compatibility treatment that avoids `https://developer.android.com/reference/kotlin/android/app/Activity.html#setRequestedOrientation(kotlin.Int)` loops. Loops can be triggered by the OEM-configured ignore requested orientation display setting (on Android 12 (API level 31) and higher) or by the landscape natural orientation of the device.

The system could ignore `https://developer.android.com/reference/kotlin/android/app/Activity.html#setRequestedOrientation(kotlin.Int)` call from an app if both of the following conditions are true:

- Activity has requested orientation more than two times within one-second timer
- Activity is not letterboxed for fixed-orientation apps

Setting this property to `false` informs the system that the app must be opted-out from the compatibility treatment even if the device manufacturer has opted the app into the treatment.

Not setting this property at all, or setting this property to `true` has no effect.

**Syntax:**

```kotlin
<application>
    <property
      android:name=
        "android.window.PROPERTY_COMPAT_ALLOW_IGNORING_ORIENTATION_REQUEST_WHEN_LOOP_DETECTED"
      android:value="false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_COMPAT_ALLOW_IGNORING_ORIENTATION_REQUEST_WHEN_LOOP_DETECTED"

### PROPERTY_COMPAT_ALLOW_MIN_ASPECT_RATIO_OVERRIDE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_ALLOW_MIN_ASPECT_RATIO_OVERRIDE: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app should be opted-out from the compatibility override that changes the min aspect ratio.

When this compat override is enabled the min aspect ratio given in the app's manifest can be overridden by the device manufacturer using their discretion to improve display compatibility unless the app's manifest value is higher. This treatment will also apply if no min aspect ratio value is provided in the manifest. These treatments can apply either in specific cases (e.g. device is in portrait) or each time the app is displayed on screen.

Setting this property to `false` informs the system that the app must be opted-out from the compatibility treatment even if the device manufacturer has opted the app into the treatment.

Not setting this property at all, or setting this property to `true` has no effect.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_COMPAT_ALLOW_MIN_ASPECT_RATIO_OVERRIDE"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_COMPAT_ALLOW_MIN_ASPECT_RATIO_OVERRIDE"

### PROPERTY_COMPAT_ALLOW_ORIENTATION_OVERRIDE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_ALLOW_ORIENTATION_OVERRIDE: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app should be excluded from the compatibility override for orientation set by the device manufacturer. When the orientation override is applied it can:

- Replace the specific orientation requested by the app with another selected by the device manufacturer; for example, replace undefined requested by the app with portrait.
- Always use an orientation selected by the device manufacturer.
- Do one of the above but only when camera connection is open.

<br />

This property is different from `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_IGNORE_REQUESTED_ORIENTATION:kotlin.String` (which is used to avoid orientation loops caused by the incorrect use of `https://developer.android.com/reference/kotlin/android/app/Activity.html#setRequestedOrientation(kotlin.Int)`) because this property overrides the app to an orientation selected by the device manufacturer rather than ignoring one of orientation requests coming from the app while respecting the previous one.

With this property set to `true` or unset, device manufacturers can override orientation for the app using their discretion to improve display compatibility.

With this property set to `false`, device manufacturer per-app override for orientation won't be applied.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_COMPAT_ALLOW_ORIENTATION_OVERRIDE"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_COMPAT_ALLOW_ORIENTATION_OVERRIDE"

### PROPERTY_COMPAT_ALLOW_RESIZEABLE_ACTIVITY_OVERRIDES

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_ALLOW_RESIZEABLE_ACTIVITY_OVERRIDES: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app should be opted-out from the compatibility overrides that change the resizability of the app.

When these compat overrides are enabled they force the packages they are applied to to be resizable/unresizable. If the app is forced to be resizable this won't change whether the app can be put into multi-windowing mode, but allow the app to resize without going into size compatibility mode when the window container resizes, such as display size change or screen rotation.

Setting this property to `false` informs the system that the app must be opted-out from the compatibility treatment even if the device manufacturer has opted the app into the treatment.

Not setting this property at all, or setting this property to `true` has no effect.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_COMPAT_ALLOW_RESIZEABLE_ACTIVITY_OVERRIDES"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_COMPAT_ALLOW_RESIZEABLE_ACTIVITY_OVERRIDES"

### PROPERTY_COMPAT_ALLOW_SANDBOXING_VIEW_BOUNDS_APIS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_ALLOW_SANDBOXING_VIEW_BOUNDS_APIS: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that it needs to be opted-out from the compatibility treatment that sandboxes the `https://developer.android.com/reference/kotlin/android/view/View` API.

The treatment can be enabled by device manufacturers for applications which misuse `https://developer.android.com/reference/kotlin/android/view/View` APIs by expecting that `https://developer.android.com/reference/kotlin/android/view/View#getLocationOnScreen(kotlin.IntArray)` and `https://developer.android.com/reference/kotlin/android/view/View#getWindowVisibleDisplayFrame(android.graphics.Rect)` return coordinates as if an activity is positioned in the top-left corner of the screen, with left coordinate equal to 0. This may not be the case for applications in multi-window and letterbox modes.

Setting this property to `false` informs the system that the application must be opted-out from the "Sandbox View API to Activity bounds" treatment even if the device manufacturer has opted the app into the treatment.

Not setting this property at all, or setting this property to `true` has no effect.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_COMPAT_ALLOW_SANDBOXING_VIEW_BOUNDS_APIS"
      android:value="false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_COMPAT_ALLOW_SANDBOXING_VIEW_BOUNDS_APIS"

### PROPERTY_COMPAT_ALLOW_SMALL_COVER_SCREEN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_ALLOW_SMALL_COVER_SCREEN: String
```

Application or Activity level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` to provide any preferences for showing all or specific Activities on small cover displays of foldable style devices.

The only supported value for the property is `https://developer.android.com/reference/kotlin/android/view/WindowManager#COMPAT_SMALL_COVER_SCREEN_OPT_IN:kotlin.Int`.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_COMPAT_ALLOW_SMALL_COVER_SCREEN"
      android:value=1 
<!-- COMPAT_COVER_SCREEN_OPT_IN -->/>
  </application>
  
```

 Value: "android.window.PROPERTY_COMPAT_ALLOW_SMALL_COVER_SCREEN"

### PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_FULLSCREEN_OVERRIDE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_FULLSCREEN_OVERRIDE: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag that (when set to false) informs the system the app has opted out of the full-screen option of the user aspect ratio compatibility override settings. (For background information about the user aspect ratio compatibility override, see `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_OVERRIDE:kotlin.String`.)

When users apply the full-screen compatibility override, the orientation of the activity is forced to `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#SCREEN_ORIENTATION_USER:kotlin.Int`.

The user override is intended to improve the app experience on devices that have the ignore orientation request display setting enabled by OEMs, which enables compatibility mode for fixed-orientation apps on Android 12 (API level 31) or higher. See [Device compatibility mode](https://developer.android.com/guide/practices/device-compatibility-mode) for more details.

To opt out of the full-screen option of the user aspect ratio compatibility override, add this property to your app manifest and set the value to `false`. Your app will have full-screen option removed from the list of user aspect ratio override options in device settings, and users will not be able to apply full-screen override to your app.

**Note:** If `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_OVERRIDE:kotlin.String` is `false`, this property has no effect.

Not setting this property at all, or setting this property to `true` has no effect.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_FULLSCREEN_OVERRIDE"
      android:value="false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_FULLSCREEN_OVERRIDE"

### PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_OVERRIDE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_OVERRIDE: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag that (when set to false) informs the system the app has opted out of the user-facing aspect ratio compatibility override.

The compatibility override enables device users to set the app's aspect ratio or force the app to fill the display regardless of the aspect ratio or orientation specified in the app manifest.

The aspect ratio compatibility override is exposed to users in device settings. A menu in device settings lists all apps that have not opted out of the compatibility override. Users select apps from the menu and set the app aspect ratio on a per-app basis. Typically, the menu is available only on large screen devices.

When users apply the aspect ratio override, the minimum aspect ratio specified in the app manifest is overridden. If users choose a full-screen aspect ratio, the orientation of the activity is forced to `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#SCREEN_ORIENTATION_USER:kotlin.Int`; see `https://developer.android.com/reference/kotlin/android/view/WindowManager#PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_FULLSCREEN_OVERRIDE:kotlin.String` to disable the full-screen option only.

The user override is intended to improve the app experience on devices that have the ignore orientation request display setting enabled by OEMs, which enables compatibility mode for fixed-orientation apps on Android 12 (API level 31) or higher. See [Device compatibility mode](https://developer.android.com/guide/practices/device-compatibility-mode) for more details.

To opt out of the user aspect ratio compatibility override, add this property to your app manifest and set the value to `false`. Your app will be excluded from the list of apps in device settings, and users will not be able to override the app's aspect ratio.

Not setting this property at all, or setting this property to `true` has no effect.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_OVERRIDE"
      android:value="false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_COMPAT_ALLOW_USER_ASPECT_RATIO_OVERRIDE"

### PROPERTY_COMPAT_ENABLE_FAKE_FOCUS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_ENABLE_FAKE_FOCUS: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the application can be opted-in or opted-out from the compatibility treatment that enables sending a fake focus event for unfocused resumed split-screen activities. This is needed because some game engines wait to get focus before drawing the content of the app which isn't guaranteed by default in multi-window mode.

Device manufacturers can enable this treatment using their discretion on a per-device basis to improve display compatibility. The treatment also needs to be specifically enabled on a per-app basis afterwards. This can either be done by device manufacturers or developers.

With this property set to `true`, the system will apply the treatment only if the device manufacturer had previously enabled it on the device. A fake focus event will be sent to the app after it is resumed only if the app is in split-screen.

Setting this property to `false` informs the system that the activity must be opted-out from the compatibility treatment even if the device manufacturer has opted the app into the treatment.

If the property remains unset the system will apply the treatment only if it had previously been enabled both at the device and app level by the device manufacturer.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_COMPAT_ENABLE_FAKE_FOCUS"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_COMPAT_ENABLE_FAKE_FOCUS"

### PROPERTY_COMPAT_IGNORE_REQUESTED_ORIENTATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_IGNORE_REQUESTED_ORIENTATION: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app can be opted-in or opted-out from the compatibility treatment that avoids `https://developer.android.com/reference/kotlin/android/app/Activity.html#setRequestedOrientation(kotlin.Int)` loops. Loops can be triggered by the OEM-configured ignore requested orientation display setting (on Android 12 (API level 31) and higher) or by the landscape natural orientation of the device.

The treatment is disabled by default but device manufacturers can enable the treatment using their discretion to improve display compatibility.

With this property set to `true`, the system could ignore `https://developer.android.com/reference/kotlin/android/app/Activity.html#setRequestedOrientation(kotlin.Int)` call from an app if one of the following conditions are true:

- Activity is relaunching due to the previous `https://developer.android.com/reference/kotlin/android/app/Activity.html#setRequestedOrientation(kotlin.Int)` call.
- Camera compatibility force rotation treatment is active for the package.

Setting this property to `false` informs the system that the app must be opted-out from the compatibility treatment even if the device manufacturer has opted the app into the treatment.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.window.PROPERTY_COMPAT_IGNORE_REQUESTED_ORIENTATION"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.window.PROPERTY_COMPAT_IGNORE_REQUESTED_ORIENTATION"

### PROPERTY_SUPPORTS_MULTI_INSTANCE_SYSTEM_UI

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_SUPPORTS_MULTI_INSTANCE_SYSTEM_UI: String
```

Activity or Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to declare that System UI should be shown for this app/component to allow it to be launched as multiple instances. This property only affects SystemUI behavior and does _not_ affect whether a component can actually be launched into multiple instances, which is determined by the Activity's `launchMode` or the launching Intent's flags. If the property is set on the Application, then all components within that application will use that value unless specified per component. The value must be a boolean string.

**Syntax:**

```kotlin
<activity>
    <property
      android:name="android.window.PROPERTY_SUPPORTS_MULTI_INSTANCE_SYSTEM_UI"
      android:value="true|false"/>
  </activity>
  
```

 Value: "android.window.PROPERTY_SUPPORTS_MULTI_INSTANCE_SYSTEM_UI"

### SCREEN_RECORDING_STATE_NOT_VISIBLE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_RECORDING_STATE_NOT_VISIBLE: Int
```

Indicates the app that registered the callback is not visible in screen recording.

 Value: 0

### SCREEN_RECORDING_STATE_VISIBLE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_RECORDING_STATE_VISIBLE: Int
```

Indicates the app that registered the callback is visible in screen recording.

 Value: 1

## Public methods

### addCrossWindowBlurEnabledListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addCrossWindowBlurEnabledListener(
    executor: Executor, 
    listener: Consumer<Boolean!>
): Unit
```

Adds a listener, which will be called when cross-window blurs are enabled/disabled at runtime. This affects both window blur behind (see `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#setBlurBehindRadius(kotlin.Int)`) and window background blur (see `https://developer.android.com/reference/kotlin/android/view/Window#setBackgroundBlurRadius(kotlin.Int)`).

Cross-window blur might not be supported by some devices due to GPU limitations. It can also be disabled at runtime, e.g. during battery saving mode, when multimedia tunneling is used or when minimal post processing is requested. In such situations, no blur will be computed or drawn, so the blur target area will not be blurred. To handle this, the app might want to change its theme to one that does not use blurs.

If the listener is added successfully, it will be called immediately with the current cross-window blur enabled state.

| Parameters ||
|---|---|
| `executor` | [Executor](../java/util/concurrent/Executor.md): `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` to handle the listener callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [Consumer](../java/util/function/Consumer.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>: the listener to be added. It will be called back with a boolean parameter, which is true if cross-window blur is enabled and false if it is disabled. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/WindowManager#removeCrossWindowBlurEnabledListener(java.util.function.Consumer)`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager#isCrossWindowBlurEnabled()`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#setBlurBehindRadius(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/Window#setBackgroundBlurRadius(kotlin.Int)`

### addCrossWindowBlurEnabledListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addCrossWindowBlurEnabledListener(listener: Consumer<Boolean!>): Unit
```

Adds a listener, which will be called when cross-window blurs are enabled/disabled at runtime. This affects both window blur behind (see `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#setBlurBehindRadius(kotlin.Int)`) and window background blur (see `https://developer.android.com/reference/kotlin/android/view/Window#setBackgroundBlurRadius(kotlin.Int)`).

Cross-window blur might not be supported by some devices due to GPU limitations. It can also be disabled at runtime, e.g. during battery saving mode, when multimedia tunneling is used or when minimal post processing is requested. In such situations, no blur will be computed or drawn, so the blur target area will not be blurred. To handle this, the app might want to change its theme to one that does not use blurs.

The listener will be called on the main thread.

If the listener is added successfully, it will be called immediately with the current cross-window blur enabled state.

| Parameters ||
|---|---|
| `listener` | [Consumer](../java/util/function/Consumer.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>: the listener to be added. It will be called back with a boolean parameter, which is true if cross-window blur is enabled and false if it is disabled. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/WindowManager#removeCrossWindowBlurEnabledListener(java.util.function.Consumer)`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager#isCrossWindowBlurEnabled()`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#setBlurBehindRadius(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/Window#setBackgroundBlurRadius(kotlin.Int)`

### addProposedRotationListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addProposedRotationListener(
    executor: Executor, 
    listener: IntConsumer
): Unit
```

Adds a listener to start monitoring the proposed rotation of the current associated context. It reports the current recommendation for the rotation that takes various factors (e.g. sensor, context, device state, etc) into account. The proposed rotation might not be applied by the system automatically due to the application's active preference to lock the orientation (e.g. with `https://developer.android.com/reference/kotlin/android/app/Activity.html#setRequestedOrientation(kotlin.Int)`). This listener gives application an opportunity to selectively react to device orientation changes. The newly added listener will be called with current proposed rotation. Note that the context of this window manager instance must be a `UiContext`.

| Parameters ||
|---|---|
| `executor` | [Executor](../java/util/concurrent/Executor.md): The executor on which callback method will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [IntConsumer](../java/util/function/IntConsumer.md): Called when the proposed rotation for the context is being delivered. The reported rotation can be `https://developer.android.com/reference/kotlin/android/view/Surface#ROTATION_0:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/Surface#ROTATION_90:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/Surface#ROTATION_180:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/Surface#ROTATION_270:kotlin.Int`. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this method is called on an instance that is not associated with a `UiContext`. |

### addScreenRecordingCallback

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addScreenRecordingCallback(
    executor: Executor, 
    callback: Consumer<Int!>
): Int
```

Adds a screen recording callback. The callback will be invoked whenever the app becomes visible in screen recording or was visible in screen recording and becomes invisible in screen recording.

An app is considered visible in screen recording if any activities owned by the registering process's UID are being recorded.

Example:

```kotlin
windowManager.addScreenRecordingCallback(state -> {
      // handle change in screen recording state
  });
  
```
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DETECT_SCREEN_RECORDING:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java/util/concurrent/Executor.md): The executor on which callback method will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java/util/function/Consumer.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: The callback that will be invoked when screen recording visibility changes. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current screen recording state. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/WindowManager#SCREEN_RECORDING_STATE_NOT_VISIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager#SCREEN_RECORDING_STATE_VISIBLE:kotlin.Int`

### getCurrentWindowMetrics

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrentWindowMetrics(): WindowMetrics
```

Returns the `https://developer.android.com/reference/kotlin/android/view/WindowMetrics` according to the current system state.

The metrics describe the size of the area the window would occupy with `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams#MATCH_PARENT:kotlin.Int` width and height, and the `https://developer.android.com/reference/kotlin/android/view/WindowInsets` such a window would have. The `https://developer.android.com/reference/kotlin/android/view/WindowInsets` are not deducted from the bounds.

The value of this is based on the **current** windowing state of the system. For example, for activities in multi-window mode, the metrics returned are based on the current bounds that the user has selected for the `https://developer.android.com/reference/kotlin/android/app/Activity.html#`'s task.

In most scenarios, `https://developer.android.com/reference/kotlin/android/view/WindowManager#getCurrentWindowMetrics()` rather than `https://developer.android.com/reference/kotlin/android/view/WindowManager#getMaximumWindowMetrics()` is the correct API to use, since it ensures values reflect window size when the app is not fullscreen.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/WindowMetrics` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/WindowManager#getMaximumWindowMetrics()`
- `https://developer.android.com/reference/kotlin/android/view/WindowMetrics`

### getDefaultDisplay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDefaultDisplay(): Display!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/content/Context.html#getDisplay()` instead.*

Returns the `https://developer.android.com/reference/kotlin/android/view/Display` upon which this `https://developer.android.com/reference/kotlin/android/view/WindowManager#` instance will create new windows.

Despite the name of this method, the display that is returned is not necessarily the primary display of the system (see `https://developer.android.com/reference/kotlin/android/view/Display#DEFAULT_DISPLAY:kotlin.Int`). The returned display could instead be a secondary display that this window manager instance is managing. Think of it as the display that this `https://developer.android.com/reference/kotlin/android/view/WindowManager#` instance uses by default.

To create windows on a different display, you need to obtain a `https://developer.android.com/reference/kotlin/android/view/WindowManager#` for that `https://developer.android.com/reference/kotlin/android/view/Display`. (See the `https://developer.android.com/reference/kotlin/android/view/WindowManager#` class documentation for more information.)

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Display!` | The display that this window manager is managing. |

### getDisplayEngagementMode

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplayEngagementMode(displayId: Int): Int
```

Gets the user engagement mode for a specific display.

| Parameters ||
|---|---|
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The display to get the engagement mode for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The engagement mode for the given display. Returns the system default if the display is not found. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/WindowManager#ENGAGEMENT_MODE_FLAG_VISUALS_ON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager#ENGAGEMENT_MODE_FLAG_AUDIO_ON:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/WindowManager#ENGAGEMENT_MODE_FLAG_VISUALS_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager#ENGAGEMENT_MODE_FLAG_AUDIO_ON:kotlin.Int`

### getMaximumWindowMetrics

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaximumWindowMetrics(): WindowMetrics
```

Returns the largest `https://developer.android.com/reference/kotlin/android/view/WindowMetrics` an app may expect in the current system state.

The value of this is based on the largest **potential** windowing state of the system. For example, for activities in multi-window mode, the metrics returned are based on the what the bounds would be if the user expanded the `https://developer.android.com/reference/kotlin/android/app/Activity.html#`'s task to cover the entire screen.

The metrics describe the size of the largest potential area the window might occupy with `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams#MATCH_PARENT:kotlin.Int` width and height, and the `https://developer.android.com/reference/kotlin/android/view/WindowInsets` such a window would have. The `https://developer.android.com/reference/kotlin/android/view/WindowInsets` are not deducted from the bounds.

Note that this might still be smaller than the size of the physical display if certain areas of the display are not available to windows created in this `https://developer.android.com/reference/kotlin/android/content/Context.html#`. For example, given that there's a device which have a multi-task mode to limit activities to a half screen. In this case, `https://developer.android.com/reference/kotlin/android/view/WindowManager#getMaximumWindowMetrics()` reports the bounds of the half screen which the activity is located.

**Generally `https://developer.android.com/reference/kotlin/android/view/WindowManager#getCurrentWindowMetrics()` is the correct API to use** for choosing UI layouts. `https://developer.android.com/reference/kotlin/android/view/WindowManager#getMaximumWindowMetrics()` are only appropriate when the application needs to know the largest possible size it can occupy if the user expands/maximizes it on the screen.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/WindowMetrics` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/WindowManager#getCurrentWindowMetrics()`
- `https://developer.android.com/reference/kotlin/android/view/WindowMetrics`
- `https://developer.android.com/reference/kotlin/android/view/Display#getRealSize(android.graphics.Point)`

### isCrossWindowBlurEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCrossWindowBlurEnabled(): Boolean
```

Returns whether cross-window blur is currently enabled. This affects both window blur behind (see `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#setBlurBehindRadius(kotlin.Int)`) and window background blur (see `https://developer.android.com/reference/kotlin/android/view/Window#setBackgroundBlurRadius(kotlin.Int)`).

Cross-window blur might not be supported by some devices due to GPU limitations. It can also be disabled at runtime, e.g. during battery saving mode, when multimedia tunneling is used or when minimal post processing is requested. In such situations, no blur will be computed or drawn, so the blur target area will not be blurred. To handle this, the app might want to change its theme to one that does not use blurs. To listen for cross-window blur enabled/disabled events, use #addCrossWindowBlurEnabledListener.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#setBlurBehindRadius(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/Window#setBackgroundBlurRadius(kotlin.Int)`

### registerBatchedSurfaceControlInputReceiver

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerBatchedSurfaceControlInputReceiver(
    hostInputTransferToken: InputTransferToken, 
    surfaceControl: SurfaceControl, 
    choreographer: Choreographer, 
    receiver: SurfaceControlInputReceiver
): InputTransferToken
```

Registers a `https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver` for a `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` that will receive batched input event. For those events that are batched, the invocation will happen once per `https://developer.android.com/reference/kotlin/android/view/Choreographer` frame, and other input events will be delivered immediately. This is different from #registerUnbatchedSurfaceControlInputReceiver(int,android.window.InputTransferToken,android.view.SurfaceControl,android.os.Looper,android.view.SurfaceControlInputReceiver) in that the input events are received batched. The caller must invoke `https://developer.android.com/reference/kotlin/android/view/WindowManager#unregisterSurfaceControlInputReceiver(android.view.SurfaceControl)` to clean up the resources when no longer needing to use the `https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver`

| Parameters ||
|---|---|
| `hostInputTransferToken` | [InputTransferToken](../android/window/InputTransferToken.md): The host token to link the embedded. This is used to handle transferring touch gesture from host to embedded and for ANRs to ensure the host receives the ANR if any issues with touch on the embedded. This value cannot be `null`. |
| `surfaceControl` | [SurfaceControl](../android/view/SurfaceControl.md): The SurfaceControl to register the InputChannel for. This value cannot be `null`. |
| `choreographer` | [Choreographer](../android/view/Choreographer.md): The Choreographer used for batching. This should match the rendering Choreographer. This value cannot be `null`. |
| --- | --- |
| `receiver` | [SurfaceControlInputReceiver](../android/view/SurfaceControlInputReceiver.md): The SurfaceControlInputReceiver that will receive the input events. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#` | Returns the `https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#` that can be used to transfer touch gesture to or from other windows. This value cannot be `null`. |

### registerDisplayEngagementModeCallback

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerDisplayEngagementModeCallback(
    executor: Executor, 
    callback: Consumer<WindowManager.DisplayEngagementModeState!>
): Unit
```

Registers a callback for display engagement mode changes. The callback will be invoked with the latest engagement mode flags upon registration. If the specified callback instance is already registered, this call does nothing.

| Parameters ||
|---|---|
| `executor` | [Executor](../java/util/concurrent/Executor.md): The executor to run the callback on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java/util/function/Consumer.md)\< [WindowManager.DisplayEngagementModeState](../android/view/WindowManager.DisplayEngagementModeState.md)!\>: The callback to register. This value cannot be `null`. |

### registerTrustedPresentationListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerTrustedPresentationListener(
    window: IBinder, 
    thresholds: TrustedPresentationThresholds, 
    executor: Executor, 
    listener: Consumer<Boolean!>
): Unit
```

Sets a callback to receive feedback about the presentation of a `https://developer.android.com/reference/kotlin/android/view/Window`. When the `https://developer.android.com/reference/kotlin/android/view/Window` is presented according to the passed in `https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds.html#`, it is said to "enter the state", and receives the callback with `true`. When the conditions fall out of thresholds, it is then said to leave the state and the caller will receive a callback with `false`. The callbacks be sent for every state transition thereafter.

There are a few simple thresholds:

- minAlpha: Lower bound on computed alpha
- minFractionRendered: Lower bounds on fraction of pixels that were rendered
- stabilityThresholdMs: A time that alpha and fraction rendered must remain within bounds before we can "enter the state"

The fraction of pixels rendered is a computation based on scale, crop and occlusion. The calculation may be somewhat counterintuitive, so we can work through an example. Imagine we have a Window with a 100x100 buffer which is occluded by (10x100) pixels on the left, and cropped by (100x10) pixels on the top. Furthermore imagine this Window is scaled by 0.9 in both dimensions. (c=crop,o=occluded,b=both,x=none)

| b | c | c | c |
| --- | --- | --- | --- |
| o | x | x | x |
| o | x | x | x |
| o | x | x | x |
| --- | --- | --- | --- |

We first start by computing fr=xscale\*yscale=0.9\*0.9=0.81, indicating that "81%" of the pixels were rendered. This corresponds to what was 100 pixels being displayed in 81 pixels. This is somewhat of an abuse of language, as the information of merged pixels isn't totally lost, but we err on the conservative side.

We then repeat a similar process for the crop and covered regions and accumulate the results: fr = fr \* (fractionNotCropped) \* (fractionNotCovered) So for this example we would get 0.9\*0.9\*0.9\*0.9=0.65...

Notice that this is not completely accurate, as we have double counted the region marked as b. However we only wanted a "lower bound" and so it is ok to err in this direction. Selection of the threshold will ultimately be somewhat arbitrary, and so there are some somewhat arbitrary decisions in this API as well.

<br />

| Parameters ||
|---|---|
| `window` | [IBinder](../android/os/IBinder.md): The Window to add the trusted presentation listener for. This can be retrieved from `https://developer.android.com/reference/kotlin/android/view/View#getWindowToken()`. This value cannot be `null`. |
| `thresholds` | [TrustedPresentationThresholds](../android/window/TrustedPresentationThresholds.md): The `https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds.html#` that will specify when the to invoke the callback. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` where the callback will be invoked on. This value cannot be `null`. |
| --- | --- |
| `listener` | [Consumer](../java/util/function/Consumer.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>: The `https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#` that will receive the callbacks when entered or exited trusted presentation per the thresholds. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds.html#`

### registerUnbatchedSurfaceControlInputReceiver

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerUnbatchedSurfaceControlInputReceiver(
    hostInputTransferToken: InputTransferToken, 
    surfaceControl: SurfaceControl, 
    looper: Looper, 
    receiver: SurfaceControlInputReceiver
): InputTransferToken
```

Registers a `https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver` for a `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` that will receive every input event. This is different than calling `https://developer.android.com/reference/kotlin/android/view/WindowManager#registerBatchedSurfaceControlInputReceiver(android.window.InputTransferToken,%20android.view.SurfaceControl,%20android.view.Choreographer,%20android.view.SurfaceControlInputReceiver)` in that the input events are received unbatched. The caller must invoke `https://developer.android.com/reference/kotlin/android/view/WindowManager#unregisterSurfaceControlInputReceiver(android.view.SurfaceControl)` to clean up the resources when no longer needing to use the `https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver`

| Parameters ||
|---|---|
| `hostInputTransferToken` | [InputTransferToken](../android/window/InputTransferToken.md): The host token to link the embedded. This is used to handle transferring touch gesture from host to embedded and for ANRs to ensure the host receives the ANR if any issues with touch on the embedded. This value cannot be `null`. |
| `surfaceControl` | [SurfaceControl](../android/view/SurfaceControl.md): The SurfaceControl to register the InputChannel for. This value cannot be `null`. |
| `looper` | [Looper](../android/os/Looper.md): The looper to use when invoking callbacks. This value cannot be `null`. |
| --- | --- |
| `receiver` | [SurfaceControlInputReceiver](../android/view/SurfaceControlInputReceiver.md): The SurfaceControlInputReceiver that will receive the input events. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#` | Returns the `https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#` that can be used to transfer touch gesture to or from other windows. This value cannot be `null`. |

### removeCrossWindowBlurEnabledListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeCrossWindowBlurEnabledListener(listener: Consumer<Boolean!>): Unit
```

Removes a listener, previously added with #addCrossWindowBlurEnabledListener

| Parameters ||
|---|---|
| `listener` | [Consumer](../java/util/function/Consumer.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>: the listener to be removed. This value cannot be `null`. |

**See Also**

### removeProposedRotationListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeProposedRotationListener(listener: IntConsumer): Unit
```

Removes a listener, previously added with `https://developer.android.com/reference/kotlin/android/view/WindowManager#addProposedRotationListener(java.util.concurrent.Executor,%20java.util.function.IntConsumer)`. It is recommended to call when the associated context no longer has visible components. No-op if the provided listener is not registered.

| Parameters ||
|---|---|
| `listener` | [IntConsumer](../java/util/function/IntConsumer.md): The listener to be removed. This value cannot be `null`. |

### removeScreenRecordingCallback

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeScreenRecordingCallback(callback: Consumer<Int!>): Unit
```

Removes a screen recording callback. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DETECT_SCREEN_RECORDING:kotlin.String`

| Parameters ||
|---|---|
| `callback` | [Consumer](../java/util/function/Consumer.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: The callback to remove. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/WindowManager#addScreenRecordingCallback(java.util.concurrent.Executor,%20java.util.function.Consumer)`

### removeViewImmediate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeViewImmediate(view: View!): Unit
```

Special variation of `https://developer.android.com/reference/kotlin/android/view/ViewManager#removeView(android.view.View)` that immediately invokes the given view hierarchy's `https://developer.android.com/reference/kotlin/android/view/View#onDetachedFromWindow()` methods before returning. This is not for normal applications; using it correctly requires great care.

| Parameters ||
|---|---|
| `view` | [View](../android/view/View.md)!: The view to be removed. |

### requestEngagementControlState

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestEngagementControlState(engagementControlFlags: Int): Unit
```

Requests an engagement control state. Allows applications to request physical display state behaviors, such as keeping the screen on for XR glasses. Note: This is a request. The system determines if the requested state will be respected. Applications should use \`registerDisplayEngagementModeCallback\` to observe the actual applied state.

| Parameters ||
|---|---|
| `engagementControlFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A bitmask of requested engagement states. Pass 0 to clear all requests. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/WindowManager#ENGAGEMENT_CONTROL_FLAG_SUSTAIN_VISUALS:kotlin.Int` |

### transferTouchGesture

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun transferTouchGesture(
    transferFromToken: InputTransferToken, 
    transferToToken: InputTransferToken
): Boolean
```

Transfer the currently in progress touch gesture from the transferFromToken to the transferToToken.

<br />

This requires that the fromToken and toToken are associated with each other. The association can be done different ways, depending on how the embedded window is created.

- Creating a `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost` and passing the host's `https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#` for `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#SurfaceControlViewHost(android.content.Context,%20android.view.Display,%20android.window.InputTransferToken)`.
- Registering a SurfaceControl for input and passing the host's token to either `https://developer.android.com/reference/kotlin/android/view/WindowManager#registerBatchedSurfaceControlInputReceiver(android.window.InputTransferToken,%20android.view.SurfaceControl,%20android.view.Choreographer,%20android.view.SurfaceControlInputReceiver)` or `https://developer.android.com/reference/kotlin/android/view/WindowManager#registerUnbatchedSurfaceControlInputReceiver(android.window.InputTransferToken,%20android.view.SurfaceControl,%20android.os.Looper,%20android.view.SurfaceControlInputReceiver)`.

The host is likely to be an `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl` so the host token can be retrieved via `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#getInputTransferToken()`.

<br />

When the host wants to transfer touch gesture to the embedded, it can retrieve the embedded token via `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage#getInputTransferToken()` or use the value returned from either `https://developer.android.com/reference/kotlin/android/view/WindowManager#registerBatchedSurfaceControlInputReceiver(android.window.InputTransferToken,%20android.view.SurfaceControl,%20android.view.Choreographer,%20android.view.SurfaceControlInputReceiver)` or `https://developer.android.com/reference/kotlin/android/view/WindowManager#registerUnbatchedSurfaceControlInputReceiver(android.window.InputTransferToken,%20android.view.SurfaceControl,%20android.os.Looper,%20android.view.SurfaceControlInputReceiver)` and pass its own token as the transferFromToken.

When the embedded wants to transfer touch gesture to the host, it can pass in its own token as the transferFromToken and use the associated host's `https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#` as the transferToToken

<br />

When the touch is transferred, the window currently receiving touch gets an ACTION_CANCEL and does not receive any further input events for this gesture.

The transferred-to window receives an ACTION_DOWN event and then the remainder of the input events for this gesture. It does not receive any of the previous events of this gesture that the originating window received.

The transferTouchGesture API only works for the current gesture. When a new gesture arrives, input dispatcher will do a new round of hit testing. So, if the host window is still the first thing that's being touched, then it will receive the new gesture again. It will again be up to the host to transfer this new gesture to the embedded.

<br />

The call can fail for the following reasons:

- Caller attempts to transfer touch gesture from a token that doesn't have an active gesture.
- The gesture is transferred to a token that is not associated with the transferFromToken. For example, if the caller transfers to a `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost` not attached to the host window via android.view.SurfaceView#setChildSurfacePackage(SurfacePackage).
- The active gesture completes before the transfer is complete, such as in the case of a fling.

<br />

| Parameters ||
|---|---|
| `transferFromToken` | [InputTransferToken](../android/window/InputTransferToken.md): the InputTransferToken for the currently active gesture. This value cannot be `null`. |
| `transferToToken` | [InputTransferToken](../android/window/InputTransferToken.md): the InputTransferToken to transfer the gesture to. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the touch stream was transferred. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage#getInputTransferToken()`
- `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#getInputTransferToken()`

### unregisterDisplayEngagementModeCallback

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterDisplayEngagementModeCallback(callback: Consumer<WindowManager.DisplayEngagementModeState!>): Unit
```

Unregisters a callback for display engagement mode changes.

| Parameters ||
|---|---|
| `callback` | [Consumer](../java/util/function/Consumer.md)\< [WindowManager.DisplayEngagementModeState](../android/view/WindowManager.DisplayEngagementModeState.md)!\>: The callback to unregister. This value cannot be `null`. |

### unregisterSurfaceControlInputReceiver

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterSurfaceControlInputReceiver(surfaceControl: SurfaceControl): Unit
```

Unregisters and cleans up the registered `https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver` for the specified token.

Must be called on the same `https://developer.android.com/reference/kotlin/android/os/Looper.html#` thread to which was passed to the `https://developer.android.com/reference/kotlin/android/view/WindowManager#registerBatchedSurfaceControlInputReceiver(android.window.InputTransferToken,%20android.view.SurfaceControl,%20android.view.Choreographer,%20android.view.SurfaceControlInputReceiver)` or `https://developer.android.com/reference/kotlin/android/view/WindowManager#registerUnbatchedSurfaceControlInputReceiver(android.window.InputTransferToken,%20android.view.SurfaceControl,%20android.os.Looper,%20android.view.SurfaceControlInputReceiver)`

| Parameters ||
|---|---|
| `surfaceControl` | [SurfaceControl](../android/view/SurfaceControl.md): The SurfaceControl to remove and unregister the input channel for. This value cannot be `null`. |

### unregisterTrustedPresentationListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterTrustedPresentationListener(listener: Consumer<Boolean!>): Unit
```

Removes a presentation listener associated with a window. If the listener was not previously registered, the call will be a noop.

| Parameters ||
|---|---|
| `listener` | [Consumer](../java/util/function/Consumer.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>: This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/WindowManager#registerTrustedPresentationListener(android.os.IBinder,%20android.window.TrustedPresentationThresholds,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`
