Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputMethodService

```
open class InputMethodService : AbstractInputMethodService
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [android.content.Context](../android.content/Context.md) |||||
| | ↳ | [android.content.ContextWrapper](../android.content/ContextWrapper.md) ||||
| | | ↳ | [android.app.Service](../android.app/Service.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.inputmethodservice.AbstractInputMethodService](AbstractInputMethodService.md) ||
| | | | | ↳ | [android.inputmethodservice.InputMethodService](InputMethodService.md) |

InputMethodService provides a standard implementation of an InputMethod, which final implementations can derive from and customize. See the base class `https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService` and the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod.html#` interface for more information on the basics of writing input methods.

In addition to the normal Service lifecycle methods, this class introduces some new specific callbacks that most subclasses will want to make use of:

- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onInitializeInterface()` for user-interface initialization, in particular to deal with configuration changes while the service is running.
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onBindInput()` to find out about switching to a new client.
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInput(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)` to deal with an input session starting with the client.
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateInputView()`, `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateCandidatesView()`, and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateExtractTextView()` for non-demand generation of the UI.
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInputView(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)` to deal with input starting within the input area of the IME.

An input method has significant discretion in how it goes about its work: the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#` provides a basic framework for standard UI elements (input view, candidates view, and running in fullscreen mode), but it is up to a particular implementor to decide how to use them. For example, one input method could implement an input area with a keyboard, another could allow the user to draw text, while a third could have no input area (and thus not be visible to the user) but instead listen to audio and perform text to speech conversion.

In the implementation provided here, all of these elements are placed together in a single window managed by the InputMethodService. It will execute callbacks as it needs information about them, and provides APIs for programmatic control over them. They layout of these elements is explicitly defined:

- The soft input view, if available, is placed at the bottom of the screen.
- The candidates view, if currently shown, is placed above the soft input view.
- If not running fullscreen, the application is moved or resized to be above these views; if running fullscreen, the window will completely cover the application and its top part will contain the extract text of what is currently being edited by the application.

### Soft Input View

Central to most input methods is the soft input view. This is where most user interaction occurs: pressing on soft keys, drawing characters, or however else your input method wants to generate text. Most implementations will simply have their own view doing all of this work, and return a new instance of it when `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateInputView()` is called. At that point, as long as the input view is visible, you will see user interaction in that view and can call back on the InputMethodService to interact with the application as appropriate.

There are some situations where you want to decide whether or not your soft input view should be shown to the user. This is done by implementing the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onEvaluateInputViewShown()` to return true or false based on whether it should be shown in the current environment. If any of your state has changed that may impact this, call `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#updateInputViewShown()` to have it re-evaluated. The default implementation always shows the input view unless there is a hard keyboard available, which is the appropriate behavior for most input methods.

### Candidates View

Often while the user is generating raw text, an input method wants to provide them with a list of possible interpretations of that text that can be selected for use. This is accomplished with the candidates view, and like the soft input view you implement `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateCandidatesView()` to instantiate your own view implementing your candidates UI.

Management of the candidates view is a little different than the input view, because the candidates view tends to be more transient, being shown only when there are possible candidates for the current text being entered by the user. To control whether the candidates view is shown, you use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setCandidatesViewShown(kotlin.Boolean)`. Note that because the candidate view tends to be shown and hidden a lot, it does not impact the application UI in the same way as the soft input view: it will never cause application windows to resize, only cause them to be panned if needed for the user to see the current focus.

### Fullscreen Mode

Sometimes your input method UI is too large to integrate with the application UI, so you just want to take over the screen. This is accomplished by switching to full-screen mode, causing the input method window to fill the entire screen and add its own "extracted text" editor showing the user the text that is being typed. Unlike the other UI elements, there is a standard implementation for the extract editor that you should not need to change. The editor is placed at the top of the IME, above the input and candidates views.

Similar to the input view, you control whether the IME is running in fullscreen mode by implementing `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onEvaluateFullscreenMode()` to return true or false based on whether it should be fullscreen in the current environment. If any of your state has changed that may impact this, call `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#updateFullscreenMode()` to have it re-evaluated. The default implementation selects fullscreen mode when the screen is in a landscape orientation, which is appropriate behavior for most input methods that have a significant input area.

When in fullscreen mode, you have some special requirements because the user can not see the application UI. In particular, you should implement `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onDisplayCompletions(kotlin.Array)` to show completions generated by your application, typically in your candidates view like you would normally show candidates.

### Generating Text

The key part of an IME is of course generating text for the application. This is done through calls to the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#` interface to the application, which can be retrieved from `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getCurrentInputConnection()`. This interface allows you to generate raw key events or, if the target supports it, directly edit in strings of candidates and committed text.

Information about what the target is expected and supports can be found through the `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#` class, which is retrieved with `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getCurrentInputEditorInfo()` method. The most important part of this is `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#inputType:kotlin.Int`; in particular, if this is `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NULL:kotlin.Int`, then the target does not support complex edits and you need to only deliver raw key events to it. An input method will also want to look at other values here, to for example detect password mode, auto complete text views, phone number entry, etc.

When the user switches between input targets, you will receive calls to `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishInput()` and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInput(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)`. You can use these to reset and initialize your input state for the current target. For example, you will often want to clear any input state, and update a soft keyboard to be appropriate for the new inputType.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.InputMethodImpl` Concrete implementation of `https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodImpl` that provides all of the standard behavior for an input method. |
| open | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.InputMethodSessionImpl` Concrete implementation of `https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodSessionImpl` that provides all of the standard behavior for an input method session. |
| | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.Insets` Information about where interesting parts of the input method UI appear. |
| --- | --- |

| XML attributes ||
|---|---|
| [`android:imeExtractEnterAnimation`](InputMethodService.md) | Animation to use when showing the fullscreen extract UI after it had previously been hidden. |
| [`android:imeExtractExitAnimation`](InputMethodService.md) | Animation to use when hiding the fullscreen extract UI after it had previously been shown. |
| [`android:imeFullscreenBackground`](InputMethodService.md) | Background to use for entire input method when it is being shown in fullscreen mode with the extract view, to ensure that it completely covers the application. |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_ADJUST_NOTHING:kotlin.Int` Asks the system to not adjust the back button affordance even when the software keyboard is shown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_DEFAULT:kotlin.Int` Allows the system to optimize the back button affordance based on the presence of software keyboard. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_WILL_DISMISS:kotlin.Int` Deprecated flag. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_WILL_NOT_DISMISS:kotlin.Int` Deprecated flag. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ACCESSIBILITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.html#` for giving the user feedback for UI events through the registered event listeners.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ACCOUNT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#` for receiving intents at a time of your choosing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ACTIVITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#` for interacting with the global system state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ADVANCED_PROTECTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.html#`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ALARM_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#` for receiving intents at a time of your choosing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APPWIDGET_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager.html#` for accessing AppWidgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_FUNCTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager.html#` for executing app functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_INTERACTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager.html#` for managing app interactions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_OPS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#` for tracking application operations on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_SEARCH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.html#` for indexing and querying app data managed by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#AUDIO_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#` for handling management of volume, ringer modes and audio routing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#AUTHENTICATION_POLICY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#AUTOFILL_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BATTERY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#` for managing battery state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ABOVE_CLIENT:kotlin.Int`

Flag for #bindService: indicates that the client application binding to this service considers the service to be more important than the app itself. When set, the platform will try to have the out of memory killer kill the app before it kills the service it is bound to, though this is not guaranteed to be the case.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`

Flag for #bindService: If binding from an activity, allow the target service's process importance to be raised based on whether the activity is visible to the user, regardless whether another flag is used to reduce the amount that the client process's overall importance is used to impact it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ALLOW_ACTIVITY_STARTS:kotlin.Int`

Flag for #bindService: If binding from an app that is visible, the bound service is allowed to start an activity from background. This was the default behavior before SDK version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`. Since then, the default behavior changed to disallow the bound service to start a background activity even if the app bound to it is in foreground, unless this flag is specified when binding.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ALLOW_OOM_MANAGEMENT:kotlin.Int`

Flag for #bindService: allow the process hosting the bound service to go through its normal memory management. It will be treated more like a running service, allowing the system to (temporarily) expunge the process if low on memory or for some other whim it may have, and being more aggressive about making it a candidate to be killed (and restarted) if running for a long time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_AUTO_CREATE:kotlin.Int`

Flag for #bindService: automatically create the service as long as the binding exists. Note that while this will create the service, its `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` method will still only be called due to an explicit call to `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`. Even without that, though, this still provides you with access to the service object while the service is created.

Note that prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, not supplying this flag would also impact how important the system consider's the target service's process to be. When set, the only way for it to be raised was by binding from a service in which case it will only be important when that activity is in the foreground. Now to achieve this behavior you must explicitly supply the new flag `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`. For compatibility, old applications that don't specify `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_AUTO_CREATE:kotlin.Int` will automatically have the flags `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_WAIVE_PRIORITY:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int` set for them in order to achieve the same result.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_DEBUG_UNBIND:kotlin.Int`

Flag for #bindService: include debugging help for mismatched calls to unbind. When this flag is set, the callstack of the following `https://developer.android.com/reference/kotlin/android/content/Context.html#unbindService(android.content.ServiceConnection)` call is retained, to be printed if a later incorrect unbind call is made. Note that doing this requires retaining information about the binding that was made for the lifetime of the app, resulting in a leak -- this should only be used for debugging.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE:kotlin.Int`

Flag for #bindService: The service being bound is an `https://developer.android.com/reference/kotlin/android/R.attr.html#isolatedProcess:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#externalService:kotlin.Int` service. This binds the service into the calling application's package, rather than the package in which the service is declared.

When using this flag, the code for the service being bound will execute under the calling application's package name and user ID. Because the service must be an isolated process, it will not have direct access to the application's data, though. The purpose of this flag is to allow applications to provide services that are attributed to the app using the service, rather than the application providing the service.
*This flag is NOT compatible with `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#`. If you need to use `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#`, you must use `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE_LONG:kotlin.Long` instead.*

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE_LONG:kotlin.Long`

Works in the same way as `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE:kotlin.Int`, but it's defined as a `long` value that is compatible to `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_IMPORTANT:kotlin.Int`

Flag for #bindService: this service is very important to the client, so should be brought to the foreground process level when the client is. Normally a process can only be raised to the visibility level by a client, even if that client is in the foreground.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_INCLUDE_CAPABILITIES:kotlin.Int`

Flag for #bindService: If binding from an app that has specific capabilities due to its foreground state such as an activity or foreground service, then this flag will allow the bound app to get the same capabilities, as long as it has the required permissions as well. If binding from a top app and its target SDK version is at or above `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, the app needs to explicitly use BIND_INCLUDE_CAPABILITIES flag to pass all capabilities to the service so the other app can have while-in-use access such as location, camera, microphone from background. If binding from a top app and its target SDK version is below `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, BIND_INCLUDE_CAPABILITIES is implicit.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_NOT_FOREGROUND:kotlin.Int`

Flag for #bindService: don't allow this binding to raise the target service's process to the foreground scheduling priority. It will still be raised to at least the same memory priority as the client (so that its process will not be killable in any situation where the client is not killable), but for CPU scheduling purposes it may be left in the background. This only has an impact in the situation where the binding client is a foreground process and the target service is in a background process.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_NOT_PERCEPTIBLE:kotlin.Int`

Flag for #bindService: If binding from an app that is visible or user-perceptible, lower the target service's importance to below the perceptible level. This allows the system to (temporarily) expunge the bound process from memory to make room for more important user-perceptible processes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_PACKAGE_ISOLATED_PROCESS:kotlin.Int`

Flag for #bindIsolatedService: Bind the service into a shared isolated process, but only with other isolated services from the same package that declare the same process name.

Specifying this flag allows multiple isolated services defined in the same package to be running in a single shared isolated process. This shared isolated process must be specified since this flag will not work with the default application process.

This flag is different from `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_SHARED_ISOLATED_PROCESS:kotlin.Int` since it only allows binding services from the same package in the same shared isolated process. This also means the shared package isolated process is global, and not scoped to each potential calling app.

The shared isolated process instance is identified by the "android:process" attribute defined by the service. This flag cannot be used without this attribute set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_SHARED_ISOLATED_PROCESS:kotlin.Int`

Flag for #bindIsolatedService: Bind the service into a shared isolated process. Specifying this flag allows multiple isolated services to be running in a single shared isolated process. The shared isolated process instance is identified by the instanceName parameter in `https://developer.android.com/reference/kotlin/android/content/Context.html#bindIsolatedService(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)`. Subsequent calls to #bindIsolatedService with the same instanceName will cause the isolated service to be co-located in the same shared isolated process. Note that the shared isolated process is scoped to the calling app; once created, only the calling app can bind additional isolated services into the shared process. However, the services themselves can come from different APKs and therefore different vendors. Only services that set the `https://developer.android.com/reference/kotlin/android/R.attr.html#allowSharedIsolatedProcess:kotlin.Int` attribute to `true` are allowed to be bound into a shared isolated process.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_WAIVE_PRIORITY:kotlin.Int`

Flag for #bindService: don't impact the scheduling or memory management priority of the target service's hosting process. Allows the service's process to be managed on the background LRU list just like a regular application process in the background.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIOMETRIC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.html#` for handling biometric and PIN/pattern/password authentication.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BLOB_STORE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.html#` for contributing and accessing data blobs from the blob store maintained by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BLUETOOTH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager.html#` for using Bluetooth.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BUGREPORT_SERVICE:kotlin.String`

Service to capture a bugreport.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CAMERA_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#` for interacting with camera devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CAPTIONING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.html#` for obtaining captioning properties and listening for changes in captioning preferences.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CARRIER_CONFIG_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#` for reading carrier configuration values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CHOOSER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserManager.html#`.

**Note:** This service is not available on Wear OS, Android TV, or Android Auto devices. On these form factors, calls to `getSystemService` for this service will return `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CLIPBOARD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/ClipboardManager.html#` for accessing and modifying the contents of the global clipboard.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#COMPANION_DEVICE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#` for managing companion devices

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONNECTIVITY_DIAGNOSTICS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager.html#` for performing network connectivity diagnostics as well as receiving network connectivity information from the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONNECTIVITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#` for handling management of network connections.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONSUMER_IR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager.html#` for transmitting infrared signals from the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTACT_KEYS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/provider/E2eeContactKeysManager.html#` to managing contact keys.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTENT_RESTRICTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentSafetyManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_IGNORE_SECURITY:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#createPackageContext(kotlin.String,%20kotlin.Int)`: ignore any security restrictions on the Context being requested, allowing it to always be loaded. For use with `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_INCLUDE_CODE:kotlin.Int` to allow code to be loaded into a process even when it isn't safe to do so. Use with extreme care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_INCLUDE_CODE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#createPackageContext(kotlin.String,%20kotlin.Int)`: include the application code with the context. This means loading code into the caller's process, so that `https://developer.android.com/reference/kotlin/android/content/Context.html#getClassLoader()` can be used to instantiate the application's classes. Setting this flags imposes security restrictions on what application context you can access; if the requested application can not be safely loaded into your process, java.lang.SecurityException will be thrown. If this flag is not set, there will be no restrictions on the packages that can be loaded, but `https://developer.android.com/reference/kotlin/android/content/Context.html#getClassLoader()` will always return the default system class loader.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_RESTRICTED:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#createPackageContext(kotlin.String,%20kotlin.Int)`: a restricted context may disable specific features. For instance, a View associated with a restricted context would ignore particular XML attributes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CREDENTIAL_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` to authenticate a user to your app.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CROSS_PROFILE_APPS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps.html#` for cross profile operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int`

The default device ID, which is the ID of the primary (non-virtual) device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_INVALID:kotlin.Int`

Invalid device ID.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_LOCK_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#` for working with global device policy management.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DISPLAY_HASH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to access `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` to handle display hashes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DISPLAY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#` for interacting with display devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DOMAIN_VERIFICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to access `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager.html#` to retrieve approval and user state for declared web domains.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DOWNLOAD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#` for requesting HTTP downloads.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DROPBOX_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/DropBoxManager.html#` instance for recording diagnostic logs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#EUICC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager.html#` to manage the device eUICC (embedded SIM).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#FILE_INTEGRITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/security/FileIntegrityManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#FILE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/storage/FileManager.html#` for handling file operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#GAME_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/GameManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#GRAMMATICAL_INFLECTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/GrammaticalInflectionManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#HARDWARE_PROPERTIES_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager.html#` for accessing the hardware properties service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#HEALTHCONNECT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#HID_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager.html#` for interacting with HID devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#INPUT_METHOD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#` for accessing input methods.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#INPUT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.html#` for interacting with input devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#IPSEC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#` for encrypting Sockets or Networks with IPSec.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#JOB_SCHEDULER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#` instance for managing occasional background tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYCHAIN_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/security/KeyChainManager.html#` for managing KeyChain certificates and grants.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#` for controlling keyguard.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYSTORE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager.html#` for accessing [Android Keystore](../privacy-and-security/keystore.md) functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LAUNCHER_APPS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.html#` for querying and monitoring launchable apps across profiles of a user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LAYOUT_INFLATER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` for inflating layout resources in this context.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LOCALE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/LocaleManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LOCATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#` for controlling location updates.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_COMMUNICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/MediaCommunicationManager.html#` for managing `https://developer.android.com/reference/kotlin/android/media/MediaSession2.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_METRICS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager.html#` for interacting with media metrics on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_PROJECTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager.html#` instance for managing media projection sessions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_QUALITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.html#` for standardize picture and audio API parameters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_ROUTER_SERVICE:kotlin.String`

Use with #getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/MediaRouter.html#` for controlling and managing routing of media.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_SESSION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.html#` for managing media Sessions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEMORY_BUDGET_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.html#` for monitoring memory budgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MIDI_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.html#` for accessing the MIDI service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_APPEND:kotlin.Int`

File creation mode: for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#openFileOutput(kotlin.String,%20kotlin.Int)`, if the file already exists then write data to the end of the existing file instead of erasing it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int`

Database open flag: when set, the database is opened with write-ahead logging enabled by default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_MULTI_PROCESS:kotlin.Int`

SharedPreference loading flag: when set, the file on disk will be checked for modification even if the shared preferences instance is already loaded in this process. This behavior is sometimes desired in cases where the application has multiple processes, all writing to the same SharedPreferences file. Generally there are better forms of communication between processes, though.

This was the legacy (but undocumented) behavior in and before Gingerbread (Android 2.3) and this flag is implied when targeting such releases. For applications targeting SDK versions *greater than* Android 2.3, this flag must be explicitly set if desired.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_NO_LOCALIZED_COLLATORS:kotlin.Int`

Database open flag: when set, the database is opened without support for localized collators.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_PRIVATE:kotlin.Int`

File creation mode: the default mode, where the created file can only be accessed by the calling application (or all applications sharing the same user ID).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_WORLD_READABLE:kotlin.Int`

File creation mode: allow all other applications to have read access to the created file.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, attempting to use this mode throws a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_WORLD_WRITEABLE:kotlin.Int`

File creation mode: allow all other applications to have write access to the created file.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, attempting to use this mode will throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MULTISENSORY_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve the service that plays multisensory feedback.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NETWORK_STATS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#` for querying network usage stats.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NFC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/nfc/NfcManager.html#` for using NFC.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NOTIFICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#` for informing the user of background events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NPU_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NSD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.html#` for handling management of network service discovery

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#OVERLAY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/om/OverlayManager.html#` for managing overlay packages.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PCC_SANDBOX_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PEOPLE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to access a `https://developer.android.com/reference/kotlin/android/app/people/PeopleManager.html#` to interact with your published conversations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PERFORMANCE_HINT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/PerformanceHintManager.html#` for accessing the performance hinting service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PERSISTENT_DATA_BLOCK_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/service/persistentdata/PersistentDataBlockManager.html#` instance for interacting with a storage device that lives across factory resets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#POWER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#` for controlling power management, including "wake locks," which let you keep the device on while you're running long tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PRINT_SERVICE:kotlin.String`

`https://developer.android.com/reference/kotlin/android/print/PrintManager.html#` for printing and managing printers and print tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PROFILING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/os/ProfilingManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_EXPORTED:kotlin.Int`

Flag for #registerReceiver: The receiver can receive broadcasts from other Apps. Has the same behavior as marking a statically registered receiver with "exported=true"

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_NOT_EXPORTED:kotlin.Int`

Flag for #registerReceiver: The receiver cannot receive broadcasts from other Apps. Has the same behavior as marking a statically registered receiver with "exported=false"

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int`

Flag for #registerReceiver: The receiver can receive broadcasts from Instant Apps.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#RESTRICTIONS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager.html#` for retrieving application restrictions and requesting permissions for restricted operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ROLE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#` for managing roles.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SATELLITE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager.html#` for accessing satellite functionality.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SEARCH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#` for handling searches.

`https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_WATCH:kotlin.Int` does not support `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SECURITY_STATE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager.html#` for accessing the security state manager service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SENSOR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/SensorManager.html#` for accessing sensors.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SERIAL_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialManager.html#` for access to serial ports.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager.html#` for accessing the launcher shortcut service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#STATUS_BAR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/StatusBarManager.html#` for interacting with the status bar and quick settings.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#STORAGE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#` for accessing system storage functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#STORAGE_STATS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/StorageStatsManager.html#` for accessing system storage statistics.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SYSTEM_HEALTH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager.html#` for accessing system health (battery, power, memory, etc) metrics.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELECOM_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#` to manage telecom-related features of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_IMS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_PHONE_NUMBER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberManager.html#` for parsing phone numbers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#` for handling management the telephony features of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_SUBSCRIPTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#` for handling management the telephony subscriptions of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TETHERING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/TetheringManager.html#` for managing tethering functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TEXT_CLASSIFICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager.html#` for text classification services.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TEXT_SERVICES_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/textservice/TextServicesManager.html#` for accessing text services.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TIME_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/time/TimeManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TV_AD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager.html#` for interacting with TV client-side advertisement services on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TV_INPUT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager.html#` for interacting with TV inputs on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TV_INTERACTIVE_APP_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.html#` for interacting with TV interactive applications on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#UI_MODE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#` for controlling UI modes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#USAGE_STATS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager.html#` for querying device usage stats.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager.html#` for access to USB devices (as a USB host) and for controlling this device's behavior as a USB device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#USER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/UserManager.html#` for managing users on devices that support multiple users.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/VibratorManager.html#` for accessing the device vibrators, interacting with individual ones and playing synchronized effects on multiple vibrators.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#` for interacting with the vibration hardware.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VIRTUAL_DEVICE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.html#` for managing virtual devices. On devices without `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` system feature the `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` will return `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VPN_MANAGEMENT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/VpnManager.html#` to manage profiles for the platform built-in VPN.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a com.android.server.WallpaperService for accessing wallpapers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WEB_APP_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/webapp/WebAppManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager.html#` for handling management of Wi-Fi Aware.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#` for handling management of Wi-Fi peer-to-peer connections.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_RTT_RANGING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/WifiRttManager.html#` for ranging devices with wifi.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` for handling management of Wi-Fi access.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WINDOW_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` for accessing the system's window manager.

<br />

From class `https://developer.android.com/reference/kotlin/android/app/Service.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_CONTINUATION_MASK:kotlin.Int`

Bits returned by `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` describing how to continue the service if it is killed. May be `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/Service.html#START_NOT_STICKY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/Service.html#START_REDELIVER_INTENT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY_COMPATIBILITY:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_FLAG_REDELIVERY:kotlin.Int`

This flag is set in `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` if the Intent is a re-delivery of a previously delivered intent, because the service had previously returned `https://developer.android.com/reference/kotlin/android/app/Service.html#START_REDELIVER_INTENT:kotlin.Int` but had been killed before calling `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf(kotlin.Int)` for that Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_FLAG_RETRY:kotlin.Int`

This flag is set in `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` if the Intent is a retry because the original attempt never got to or returned from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_NOT_STICKY:kotlin.Int`

Constant to return from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`: if this service's process is killed while it is started (after returning from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`), and there are no new start intents to deliver to it, then take the service out of the started state and don't recreate until a future explicit call to `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`. The service will not receive a `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` call with a null Intent because it will not be restarted if there are no pending Intents to deliver.

This mode makes sense for things that want to do some work as a result of being started, but can be stopped when under memory pressure and will explicit start themselves again later to do more work. An example of such a service would be one that polls for data from a server: it could schedule an alarm to poll every N minutes by having the alarm start its service. When its `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` is called from the alarm, it schedules a new alarm for N minutes later, and spawns a thread to do its networking. If its process is killed while doing that check, the service will not be restarted until the alarm goes off.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_REDELIVER_INTENT:kotlin.Int`

Constant to return from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`: if this service's process is killed while it is started (after returning from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`), then it will be scheduled for a restart and the last delivered Intent re-delivered to it again via `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`. This Intent will remain scheduled for redelivery until the service calls `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf(kotlin.Int)` with the start ID provided to `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`. The service will not receive a `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` call with a null Intent because it will only be restarted if it is not finished processing all Intents sent to it (and any such pending events will be delivered at the point of restart).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY:kotlin.Int`

Constant to return from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`: if this service's process is killed while it is started (after returning from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`), then leave it in the started state but don't retain this delivered intent. Later the system will try to re-create the service. Because it is in the started state, it will guarantee to call `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` after creating the new service instance; if there are not any pending start commands to be delivered to the service, it will be called with a null intent object, so you must take care to check for this.

This mode makes sense for things that will be explicitly started and stopped to run for arbitrary periods of time, such as a service performing background music playback.

Since Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or above are disallowed to start a foreground service from the background, but the restriction doesn't impact *restarts* of a sticky foreground service. However, when apps start a sticky foreground service from the background, the same restriction still applies.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY_COMPATIBILITY:kotlin.Int`

Constant to return from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`: compatibility version of `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY:kotlin.Int` that does not guarantee that `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` will be called again after being killed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#STOP_FOREGROUND_DETACH:kotlin.Int`

Selector for `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)`: if set, the notification previously supplied to #startForeground will be detached from the service's lifecycle. The notification will remain shown even after the service is stopped and destroyed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#STOP_FOREGROUND_LEGACY:kotlin.Int`

Selector for `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)`: equivalent to passing `false` to the legacy API `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Boolean)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#STOP_FOREGROUND_REMOVE:kotlin.Int`

Selector for `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)`: if supplied, the notification previously supplied to #startForeground will be cancelled and removed from display.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()` called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#InputMethodService()()` <br /> |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#enableHardwareAcceleration()()` You can call this to try to enable accelerated drawing for your IME. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#finishConnectionlessStylusHandwriting(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Finishes the current connectionless stylus handwriting session and delivers the result. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#finishStylusHandwriting()()` Finish the current stylus handwriting session. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getBackDisposition()()` Retrieves the current disposition mode that indicates the expected back button affordance. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getCandidatesHiddenVisibility()()` Returns the visibility mode (either `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View.html#GONE:kotlin.Int`) of the candidates view when it is not shown. |
| open [InputBinding](../android.view.inputmethod/InputBinding.md)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getCurrentInputBinding()()` Return the currently active InputBinding for the input method, or null if there is none. |
| --- | --- |
| open [InputConnection](../android.view.inputmethod/InputConnection.md)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getCurrentInputConnection()()` Retrieve the currently active InputConnection that is bound to the input method, or null if there is none. |
| open [EditorInfo](../android.view.inputmethod/EditorInfo.md)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getCurrentInputEditorInfo()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getCurrentInputStarted()()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getInputMethodWindowRecommendedHeight()()` Aimed to return the previous input method's `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.Insets#contentTopInsets:kotlin.Int`, but its actual semantics has never been well defined. |
| open [LayoutInflater](../android.view/LayoutInflater.md)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getLayoutInflater()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getMaxWidth()()` Return the maximum width, in pixels, available the input method. |
| --- | --- |
| static [Duration](../java.time/Duration.md) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingIdleTimeoutMax()()` Returns the maximum stylus handwriting session idle-timeout for use with `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setStylusHandwritingSessionTimeout(java.time.Duration)`. |
| [Duration](../java.time/Duration.md) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingSessionTimeout()()` Returns the duration after which an ongoing stylus handwriting session that hasn't received new `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`s will time out and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#finishStylusHandwriting()` will be called. |
| [Window](../android.view/Window.md)? | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingWindow()()` Returns the stylus handwriting inking window. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getSystemService(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Return the handle to a system-level service by name. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getTextForImeAction(kotlin.Int)(imeOptions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return text that can be used as a button label for the given `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#imeOptions:kotlin.Int`. |
| open [Dialog](../android.app/Dialog.md)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getWindow()()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#hideStatusIcon()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#hideWindow()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#isExtractViewShown()()` Return whether the fullscreen extract view is shown. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#isFullscreenMode()()` Return whether the input method is *currently* running in fullscreen mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#isInputViewShown()()` Returns whether the window is currently requested to be shown. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#isShowInputRequested()()` Returns whether the window is currently requested to be shown with the input area *and* can currently be shown. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onAppPrivateCommand(kotlin.String,%20android.os.Bundle)(action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, data: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Not implemented in this class. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onBindInput()()` Called when a new client has bound to the input method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onComputeInsets(android.inputmethodservice.InputMethodService.Insets)(outInsets: https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.Insets!)` Compute the interesting insets into your UI. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)` Take care of handling configuration changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onConfigureWindow(android.view.Window,%20kotlin.Boolean,%20kotlin.Boolean)(win: https://developer.android.com/reference/kotlin/android/view/Window.html#!, isFullscreen: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, isCandidatesOnly: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Update the given window's parameters for the given mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreate()()` Called by the system when the service is first created. |
| --- | --- |
| open [View](../android.view/View.md)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateCandidatesView()()` Create and return the view hierarchy used to show candidates. |
| open [View](../android.view/View.md)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateExtractTextView()()` Called by the framework to create the layout for showing extracted text. |
| open [InlineSuggestionsRequest](../android.view.inputmethod/InlineSuggestionsRequest.md)? | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateInlineSuggestionsRequest(android.os.Bundle)(uiExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Called when Autofill is requesting an `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#` from the IME. |
| --- | --- |
| open [AbstractInputMethodService.AbstractInputMethodImpl](../android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodImpl.md)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateInputMethodInterface()()` Implement to return our standard `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.InputMethodImpl`. |
| open [AbstractInputMethodService.AbstractInputMethodSessionImpl](../android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodSessionImpl.md)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateInputMethodSessionInterface()()` Implement to return our standard `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.InputMethodSessionImpl`. |
| open [View](../android.view/View.md)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateInputView()()` Create and return the view hierarchy used for the input area (such as a soft keyboard). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCustomImeSwitcherButtonRequestedVisible(kotlin.Boolean)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when the requested visibility of a custom IME Switcher button changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onDestroy()()` Called by the system to notify a Service that it is no longer used and is being removed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onDisplayCompletions(kotlin.Array)(completions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/view/inputmethod/CompletionInfo.html#!>!)` Called when the application has reported auto-completion candidates that it would like to have the input method displayed. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onEvaluateFullscreenMode()()` Override this to control when the input method should run in fullscreen mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onEvaluateInputViewShown()()` Override this to control when the soft input area should be shown to the user. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onExtractTextContextMenuItem(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This is called when the user has selected a context menu item from the extracted text view, when running in fullscreen mode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onExtractedCursorMovement(kotlin.Int,%20kotlin.Int)(dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This is called when the user has performed a cursor movement in the extracted text view, when it is running in fullscreen mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onExtractedSelectionChanged(kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This is called when the user has moved the cursor in the extracted text view, when running in fullsreen mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onExtractedTextClicked()()` This is called when the user has clicked on the extracted text view, when running in fullscreen mode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onExtractingInputChanged(android.view.inputmethod.EditorInfo)(ei: https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#!)` This is called when, while currently displayed in extract mode, the current input target changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishCandidatesView(kotlin.Boolean)(finishingInput: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when the candidates view is being hidden from the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishInput()()` Called to inform the input method that text input has finished in the last editor. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishInputView(kotlin.Boolean)(finishingInput: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when the input view is being hidden from the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishStylusHandwriting()()` Called when the current stylus handwriting session was finished (either by the system or via `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#finishStylusHandwriting()`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onGenericMotionEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#!)` Override this to intercept generic motion events before they are processed by the application. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onInitializeInterface()()` This is a hook that subclasses can use to perform initialization of their interface. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onInlineSuggestionsResponse(android.view.inputmethod.InlineSuggestionsResponse)(response: https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsResponse.html#)` Called when Autofill responds back with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsResponse.html#` containing inline suggestions. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onKeyDown(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Called back when a `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#` is forwarded from the target application. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Default implementation of `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)`: always returns false (doesn't handle the event). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Override this to intercept special key multiple events before they are processed by the application. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onKeyUp(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Override this to intercept key up events before they are processed by the application. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onPrepareStylusHandwriting()()` Called to prepare stylus handwriting. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onShouldVerifyKeyEvent(android.view.KeyEvent)(keyEvent: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)` Received by the IME before dispatching to `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onKeyDown(kotlin.Int,%20android.view.KeyEvent)` to determine if the `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#` requires system-level verification of its authenticity. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onShowInputRequested(kotlin.Int,%20kotlin.Boolean)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, configChange: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` The system has decided that it may be time to show your input method. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartCandidatesView(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)(editorInfo: https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#!, restarting: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when only the candidates view has been shown for showing processing as the user enters text through a hard keyboard. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartConnectionlessStylusHandwriting(kotlin.Int,%20android.view.inputmethod.CursorAnchorInfo)(inputType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, cursorAnchorInfo: https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo.html#?)` Called when an app requests to start a connectionless stylus handwriting session using one of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#startConnectionlessStylusHandwriting(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`, or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20kotlin.String,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInput(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)(attribute: https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#!, restarting: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called to inform the input method that text input has started in an editor. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInputView(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)(editorInfo: https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#!, restarting: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when the input view is being shown and input has started on a new editor. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartStylusHandwriting()()` Called when an app requests stylus handwriting `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#startStylusHandwriting(android.view.View)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStylusHandwritingMotionEvent(android.view.MotionEvent)(motionEvent: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)` Called after `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartStylusHandwriting()` returns `true` for every Stylus `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onTrackballEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#!)` Override this to intercept trackball motion events before they are processed by the application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUnbindInput()()` Called when the previous bound client is no longer associated with the input method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateCursor(android.graphics.Rect)(newCursor: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Called when the application has reported a new location of its text cursor. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateCursorAnchorInfo(android.view.inputmethod.CursorAnchorInfo)(cursorAnchorInfo: https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo.html#!)` Called when the application has reported a new location of its text insertion point and characters in the composition string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateEditorToolType(kotlin.Int)(toolType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when the user tapped or clicked an editor. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateExtractedText(kotlin.Int,%20android.view.inputmethod.ExtractedText)(token: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, text: https://developer.android.com/reference/kotlin/android/view/inputmethod/ExtractedText.html#!)` Called when the application has reported new extracted text to be shown due to changes in its current text state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateExtractingViews(android.view.inputmethod.EditorInfo)(ei: https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#!)` Called when the fullscreen-mode extracting editor info has changed, to update the state of its UI such as the action buttons shown. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateExtractingVisibility(android.view.inputmethod.EditorInfo)(ei: https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#!)` Called when the fullscreen-mode extracting editor info has changed, to determine whether the extracting (extract text and candidates) portion of the UI should be shown. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateSelection(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(oldSelStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, oldSelEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newSelStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newSelEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, candidatesStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, candidatesEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when the application has reported a new selection region of the text. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onViewClicked(kotlin.Boolean)(focusChanged: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when the user tapped or clicked a text view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onWindowHidden()()` Called when the input method window has been hidden from the user, after previously being visible. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onWindowShown()()` Called immediately before the input method window is shown to the user. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#requestHideSelf(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Close this input method's soft input area, removing it from the display. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#requestShowSelf(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Show the input method's soft input area, so the user sees the input method window and can interact with it. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#sendDefaultEditorAction(kotlin.Boolean)(fromEnterKey: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Ask the input target to execute its default action via `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#performEditorAction(kotlin.Int)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#sendDownUpKeyEvents(kotlin.Int)(keyEventCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Send the given key event code (as defined by `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#`) to the current input connection is a key down + key up event pair. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#sendKeyChar(kotlin.Char)(charCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Send the given UTF-16 character to the current input connection. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setBackDisposition(kotlin.Int)(disposition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the disposition mode that indicates the expected affordance for the back button. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setCandidatesView(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Replaces the current candidates view with a new one. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setCandidatesViewShown(kotlin.Boolean)(shown: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Controls the visibility of the candidates display area. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setExtractView(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setExtractViewShown(kotlin.Boolean)(shown: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Controls the visibility of the extracted text area. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setInputView(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Replaces the current input view with a new one. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setStylusHandwritingRegion(android.graphics.Region)(handwritingRegion: https://developer.android.com/reference/kotlin/android/graphics/Region.html#)` Sets a new stylus handwriting region as user continues to write on an editor on screen. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setStylusHandwritingSessionTimeout(java.time.Duration)(duration: https://developer.android.com/reference/kotlin/java/time/Duration.html#)` Sets the duration after which an ongoing stylus handwriting session that hasn't received new `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`s will time out and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#finishStylusHandwriting()` will be called. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setTheme(kotlin.Int)(theme: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` You can call this to customize the theme used by your IME's window. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#shouldOfferSwitchingToNextInputMethod()()` Returns true if the current IME needs to offer the users ways to switch to a next input method (e.g. a globe key.). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#showStatusIcon(kotlin.Int)(iconResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#showWindow(kotlin.Boolean)(showInput: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#switchInputMethod(kotlin.String)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Force switch to a new input method, as identified by id. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#switchInputMethod(kotlin.String,%20android.view.inputmethod.InputMethodSubtype)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, subtype: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype.html#!)` Force switch to a new input method, as identified by `id`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#switchToNextInputMethod(kotlin.Boolean)(onlyCurrentIme: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Force switch to the next input method and subtype. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#switchToPreviousInputMethod()()` Force switch to the last used input method and subtype. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#updateFullscreenMode()()` Re-evaluate whether the input method should be running in fullscreen mode, and update its UI if this has changed since the last time it was evaluated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#updateInputViewShown()()` Re-evaluate whether the soft input area should currently be shown, and update its UI if this has changed since the last time it was evaluated. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#dump(java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, fout: https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#!, args: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Performs a dump of the InputMethodService's internal state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCurrentInputMethodSubtypeChanged(android.view.inputmethod.InputMethodSubtype)(newSubtype: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype.html#!)` Called when the subtype was changed. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/app/Service.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#attachBaseContext(android.content.Context)(newBase: https://developer.android.com/reference/kotlin/android/content/Context.html#!)`

Set the base context for this ContextWrapper. All calls will then be delegated to the base context. Throws IllegalStateException if a base context has already been set.

<br />

`https://developer.android.com/reference/kotlin/android/app/Application.html#!` `https://developer.android.com/reference/kotlin/android/app/Service.html#getApplication()()`

Return the application that owns this service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#getForegroundServiceType()()`

If the service has become a foreground service by calling `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification)` or `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification,%20kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/app/Service.html#getForegroundServiceType()` returns the current foreground service type.

If there is no foregroundServiceType specified in manifest, `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_NONE:kotlin.Int` is returned.

If the service is not a foreground service, `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_NONE:kotlin.Int` is returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onCreate()()`

Called by the system when the service is first created. Do not call this method directly.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onRebind(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Called when new clients have connected to the service, after it had previously been notified that all had disconnected in its `https://developer.android.com/reference/kotlin/android/app/Service.html#onUnbind(android.content.Intent)`. This will only be called if the implementation of `https://developer.android.com/reference/kotlin/android/app/Service.html#onUnbind(android.content.Intent)` was overridden to return true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onStart(android.content.Intent,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, startId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, startId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called by the system every time a client explicitly starts the service by calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`, providing the arguments it supplied and a unique integer token representing the start request. Do not call this method directly.

For backwards compatibility, the default implementation calls `https://developer.android.com/reference/kotlin/android/app/Service.html#onStart(android.content.Intent,%20kotlin.Int)` and returns either `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY_COMPATIBILITY:kotlin.Int`.

Note that the system calls this on your service's main thread. A service's main thread is the same thread where UI operations take place for Activities running in the same process. You should always avoid stalling the main thread's event loop. When doing long-running operations, network calls, or heavy disk I/O, you should kick off a new thread, or use `https://developer.android.com/reference/kotlin/android/os/AsyncTask.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onTaskRemoved(android.content.Intent)(rootIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

This is called if the service is currently running and the user has removed a task that comes from the service's application. If you have set `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FLAG_STOP_WITH_TASK:kotlin.Int` then you will not receive this callback; instead, the service will simply be stopped.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int)(startId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Callback called on timeout for `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int`. See `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` for more details.

If the foreground service of type `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` doesn't finish even after it's timed out, the app will be declared an ANR after a short grace period of several seconds.

Starting from Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int,%20kotlin.Int)` will also be called when a foreground service of type `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` times out. Developers do not need to implement both of the callbacks on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` and onwards.

Note, even though `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` was added on Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, it can be also used on on prior android versions (just like other new foreground service types can be used). However, because `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int)` did not exist on prior versions, it will never called on such versions. Because of this, developers must make sure to stop the foreground service even if `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int)` is not called on such versions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int,%20kotlin.Int)(startId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fgsType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Callback called when a particular foreground service type has timed out.

This callback is meant to give the app a small grace period of a few seconds to finish the foreground service of the associated type - if it fails to do so, the app will crash.

The foreground service of the associated type can be stopped within the time limit by `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` or their overloads. `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)` can be used as well, which demotes the service to a "background" service, which will soon be stopped by the system.

The specific time limit for each type (if one exists) is mentioned in the documentation for that foreground service type. See `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_DATA_SYNC:kotlin.Int` for example.

Note: time limits are restricted to a rolling 24-hour window - for example, if a foreground service type has a time limit of 6 hours, that time counter begins as soon as the foreground service starts. This time limit will only be reset once every 24 hours or if the app comes into the foreground state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onUnbind(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Called when all clients have disconnected from a particular interface published by the service. The default implementation does nothing and returns false.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, notification: https://developer.android.com/reference/kotlin/android/app/Notification.html#!)`

If your service is started (running through `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`), then also make this service run in the foreground, supplying the ongoing notification to be shown to the user while in this state. By default started services are background, meaning that their process won't be given foreground CPU scheduling (unless something else in that process is foreground) and, if the system needs to kill them to reclaim more memory (such as to display a large page in a web browser), they can be killed without too much harm. You use #startForeground if killing your service would be disruptive to the user, such as if your service is performing background music playback, so the user would notice if their music stopped playing.

Note that calling this method does *not* put the service in the started state itself, even though the name sounds like it. You must always call `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startService(android.content.Intent)` first to tell the system it should keep the service running, and then use this method to tell it to keep it running harder.

Apps targeting API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` or later must request the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE:kotlin.String` in order to use this API.

Apps built with SDK version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or later can specify the foreground service types using attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` in service element of manifest file. The value of attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` can be multiple flags ORed together.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](https://developer.android.com/about/versions/12/behavior-changes-12) for more details.

<br />

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` or higher are not allowed to start foreground services without specifying a valid foreground service type in the manifest attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int`. See [Behavior changes: Apps targeting Android 14](https://developer.android.com/about/versions/14/behavior-changes-14) for more details.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification,%20kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, notification: https://developer.android.com/reference/kotlin/android/app/Notification.html#, foregroundServiceType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

An overloaded version of `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification)` with additional foregroundServiceType parameter.

Apps built with SDK version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or later can specify the foreground service types using attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` in service element of manifest file. The value of attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` can be multiple flags ORed together.

The foregroundServiceType parameter must be a subset flags of what is specified in manifest attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int`, if not, an IllegalArgumentException is thrown. Specify foregroundServiceType parameter as `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_MANIFEST:kotlin.Int` to use all flags that is specified in manifest attribute foregroundServiceType.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](https://developer.android.com/about/versions/12/behavior-changes-12) for more details.

<br />

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` or higher are not allowed to start foreground services without specifying a valid foreground service type in the manifest attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int`, and the parameter `foregroundServiceType` here must not be the `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_NONE:kotlin.Int`. See [Behavior changes: Apps targeting Android 14](https://developer.android.com/about/versions/14/behavior-changes-14) for more details.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Boolean)(removeNotification: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Legacy version of `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)(notificationBehavior: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Remove this service from foreground state, allowing it to be killed if more memory is needed. This does not stop the service from running (for that you use `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf()` or related methods), just takes it out of the foreground state.

If `https://developer.android.com/reference/kotlin/android/app/Service.html#STOP_FOREGROUND_REMOVE:kotlin.Int` is supplied, the service's associated notification will be cancelled immediately.

If `https://developer.android.com/reference/kotlin/android/app/Service.html#STOP_FOREGROUND_DETACH:kotlin.Int` is supplied, the service's association with the notification will be severed. If the notification had not yet been shown, due to foreground-service notification deferral policy, it is immediately posted when `stopForeground(STOP_FOREGROUND_DETACH)` is called. In all cases, the notification remains shown even after this service is stopped fully and destroyed.

If `zero` is passed as the argument, the result will be the legacy behavior as defined prior to Android L: the notification will remain posted until the service is fully stopped, at which time it will automatically be cancelled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf()()`

Stop the service, if it was previously started. This is the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` for this particular service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf(kotlin.Int)(startId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Old version of `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelfResult(kotlin.Int)` that doesn't return a result.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelfResult(kotlin.Int)(startId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Stop the service if the most recent time it was started was startId. This is the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` for this particular service but allows you to safely avoid stopping if there is a start request from a client that you haven't yet seen in `https://developer.android.com/reference/kotlin/android/app/Service.html#onStart(android.content.Intent,%20kotlin.Int)`.

*Be careful about ordering of your calls to this function.*. If you call this function with the most-recently received ID before you have called it for previously received IDs, the service will be immediately stopped anyway. If you may end up processing IDs out of order (such as by dispatching them on separate threads), then you are responsible for stopping them in the same order you received them.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindIsolatedService(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, instanceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

Variation of #bindService that, in the specific case of isolated services, allows the caller to generate multiple instances of a service from a single component declaration. In other words, you can use this to bind to a service that has specified `https://developer.android.com/reference/kotlin/android/R.attr.html#isolatedProcess:kotlin.Int` and, in addition to the existing behavior of running in an isolated process, you can also through the arguments here have the system bring up multiple concurrent processes hosting their own instances of that service. The instanceName you provide here identifies the different instances, and you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#updateServiceGroup(android.content.ServiceConnection,%20kotlin.Int,%20kotlin.Int)` to tell the system how it should manage each of these instances.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindService(android.content.Intent,%20android.content.Context.BindServiceFlags,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

See `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Connects to an application service, creating it if needed. This defines a dependency between your application and the service. The given conn will receive the service object when it is created and be told if it dies and restarts. The service will be considered required by the system only for as long as the calling context exists. For example, if this Context is an Activity that is stopped, the service will not be required to continue running until the Activity is resumed.

If the service does not support binding, it may return `null` from its `https://developer.android.com/reference/kotlin/android/app/Service.html#onBind(android.content.Intent)` method. If it does, then the ServiceConnection's `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#onNullBinding(android.content.ComponentName)` method will be invoked instead of `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#onServiceConnected(android.content.ComponentName,%20android.os.IBinder)`.

**Note:** This method *cannot* be called from a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` component. A pattern you can use to communicate from a BroadcastReceiver to a Service is to call `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)` with the arguments containing the command to be sent, with the service calling its `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf(kotlin.Int)` method when done executing that command. See the API demo App/Service/Service Start Arguments Controller for an illustration of this. It is okay, however, to use this method from a BroadcastReceiver that has been registered with #registerReceiver, since the lifetime of this BroadcastReceiver is tied to another object (the one that registered it).

This method only accepts a int type flag, to pass in a long type flag, call `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)` instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindService(android.content.Intent,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

Same as `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)` with executor to control ServiceConnection callbacks.

This method only accepts a 32 bits flag, to pass in a 64 bits flag, call `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.Context.BindServiceFlags,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20android.content.Context.BindServiceFlags,%20android.os.UserHandle)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`

See `https://developer.android.com/reference/kotlin/android/content/Context.html#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int,%20android.os.UserHandle)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int,%20android.os.UserHandle)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`

Binds to a service in the given `user` in the same manner as #bindService.

Requires that one of the following conditions are met:

- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS_FULL`
- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS` and is the same package as the `service` (determined by its component's package) and the Android version is at least `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`
- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS` and is in same profile group as the given `user`
- caller has `android.Manifest.permission.INTERACT_ACROSS_PROFILES` and is in same profile group as the given `user` and is the same package as the `service`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingOrSelfPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Determine whether the calling process of an IPC *or you* have been granted a particular permission. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#checkCallingPermission(kotlin.String)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingOrSelfUriPermission(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the calling process of an IPC *or you* has been granted permission to access a specific URI. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#checkCallingUriPermission(android.net.Uri,%20kotlin.Int)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingOrSelfUriPermissions(kotlin.collections.MutableList,%20kotlin.Int)(uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the calling process of an IPC *or you* has been granted permission to access a list of URIs. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#checkCallingUriPermission(android.net.Uri,%20kotlin.Int)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Determine whether the calling process of an IPC you are handling has been granted a particular permission. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always fail. This is done to protect against accidentally leaking permissions; you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#checkCallingOrSelfPermission(kotlin.String)` to avoid this protection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingUriPermission(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the calling process and uid has been granted permission to access a specific URI. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingUriPermissions(kotlin.collections.MutableList,%20kotlin.Int)(uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the calling process and uid has been granted permission to access a list of URIs. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermissions(kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkContentUriPermissionFull(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether a particular process and uid has been granted permission to access a specific content URI.

Unlike `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, this method checks for general access to the URI's content provider, as well as explicitly granted permissions.

Note, this check will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` for non-content URIs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the given permission is allowed for a particular process and user ID running in the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkSelfPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Determine whether *you* have been granted a particular permission.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether a particular process and uid has been granted permission to access a specific URI. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkUriPermission(android.net.Uri,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, readPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, writePermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Check both a Uri and normal permission. This allows you to perform both `https://developer.android.com/reference/kotlin/android/content/Context.html#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)` and #checkUriPermission in one call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkUriPermissions(kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether a particular process and uid has been granted permission to access a list of URIs. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail. **Note:** On SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, calling this method from a secondary-user's context will incorrectly return `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_DENIED:kotlin.Int` for all {code uris}.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#clearWallpaper()()`

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createAttributionContext(kotlin.String)(attributionTag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Return a new Context object for the current Context but attribute to a different tag. In complex apps attribution tagging can be used to distinguish between separate logical parts.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createConfigurationContext(android.content.res.Configuration)(overrideConfiguration: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`

Return a new Context object for the current Context but whose resources are adjusted to match the given Configuration. Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same configuration) may be so the Context itself can be fairly lightweight.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createContext(android.content.ContextParams)(contextParams: https://developer.android.com/reference/kotlin/android/content/ContextParams.html#)`

Creates a context with specific properties and behaviors.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createContextForSplit(kotlin.String)(splitName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Return a new Context object for the given split name. The new Context has a ClassLoader and Resources object that can access the split's and all of its dependencies' code/resources. Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same split) may be so the Context itself can be fairly lightweight.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createDeviceContext(kotlin.Int)(deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a new `Context` object from the current context but with device association given by the `deviceId`. Each call to this method returns a new instance of a context object. Context objects are not shared; however, common state (such as the `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` and other resources for the same configuration) can be shared, so the `Context` itself is lightweight.

Applications that run on virtual devices may use this method to access the default device capabilities and functionality (by passing `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int`. Similarly, applications running on the default device may access the functionality of virtual devices.

Note that the newly created instance will be associated with the same display as the parent Context, regardless of the device ID passed here.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createDeviceProtectedStorageContext()()`

Return a new Context object for the current Context but whose storage APIs are backed by device-protected storage.

On devices with direct boot, data stored in this location is encrypted with a key tied to the physical device, and it can be accessed immediately after the device has booted successfully, both *before and after* the user has authenticated with their credentials (such as a lock pattern or PIN).

Because device-protected data is available without user authentication, you should carefully limit the data you store using this Context. For example, storing sensitive authentication tokens or passwords in the device-protected area is strongly discouraged.

If the underlying device does not have the ability to store device-protected and credential-protected data using different keys, then both storage areas will become available at the same time. They remain as two distinct storage locations on disk, and only the window of availability changes.

Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same configuration) may be so the Context itself can be fairly lightweight.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createDisplayContext(android.view.Display)(display: https://developer.android.com/reference/kotlin/android/view/Display.html#)`

Returns a new `Context` object from the current context but with resources adjusted to match the metrics of `display`. Each call to this method returns a new instance of a context object. Context objects are not shared; however, common state (such as the `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` and other resources for the same configuration) can be shared, so the `Context` itself is lightweight.

**Note:** This `Context` is **not** expected to be updated with new configuration if the underlying display configuration changes and the cached `Resources` it returns could be stale. It is suggested to use `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener.html#` to listen for changes and re-create an instance if necessary.

This `Context` is **not** a UI context, do not use it to access UI components or obtain a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` instance.

To obtain an instance of `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` configured to show windows on the given display, call `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)` on the returned display context, then call `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` or `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(java.lang.Class)` on the returned window context.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createPackageContext(kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return a new Context object for the given application name. This Context is the same as what the named application gets when it is launched, containing the same resources and class loader. Each call to this method returns a new instance of a Context object; Context objects are not shared, however they share common state (Resources, ClassLoader, etc) so the Context instance itself is fairly lightweight.

Throws `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.NameNotFoundException.html#` if there is no application with the given package name.

Throws `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if the Context requested can not be loaded into the caller's process for security reasons (see `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_INCLUDE_CODE:kotlin.Int` for more information}.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createWindowContext(android.view.Display,%20kotlin.Int,%20android.os.Bundle)(display: https://developer.android.com/reference/kotlin/android/view/Display.html#, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Creates a `Context` for a non-`https://developer.android.com/reference/kotlin/android/app/Activity.html#` window on the given `https://developer.android.com/reference/kotlin/android/view/Display.html#`.

Similar to `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, but the `display` is passed in, instead of implicitly using the `https://developer.android.com/reference/kotlin/android/content/Context.html#getDisplay()`.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createWindowContext(kotlin.Int,%20android.os.Bundle)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Creates a Context for a non-activity window.

A window context is a context that can be used to add non-activity windows, such as `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_OVERLAY:kotlin.Int`. A window context must be created from a context that has an associated `https://developer.android.com/reference/kotlin/android/view/Display.html#`, such as `https://developer.android.com/reference/kotlin/android/app/Activity.html#` or a context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createDisplayContext(android.view.Display)`.

The window context is created with the appropriate `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` for the area of the display that the windows created with it can occupy; it must be used when `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` views, such that they can be inflated with proper `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#`. Below is a sample code to **add an application overlay window on the primary display:**

```kotlin
...
  final DisplayManager dm = anyContext.getSystemService(DisplayManager.class);
  final Display primaryDisplay = dm.getDisplay(DEFAULT_DISPLAY);
  final Context windowContext = anyContext.createDisplayContext(primaryDisplay)
          .createWindowContext(TYPE_APPLICATION_OVERLAY, null);
  final View overlayView = Inflater.from(windowContext).inflate(someLayoutXml, null);
 
  // WindowManager.LayoutParams initialization
  ...
  // The types used in addView and createWindowContext must match.
  mParams.type = TYPE_APPLICATION_OVERLAY;
  ...
 
  windowContext.getSystemService(WindowManager.class).addView(overlayView, mParams);
  
```

This context's configuration and resources are adjusted to an area of the display where the windows with provided type will be added. **Note that all windows associated with the same context will have an affinity and can only be moved together between different displays or areas on a display.** If there is a need to add different window types, or non-associated windows, separate Contexts should be used.

Creating a window context is an expensive operation. Misuse of this API may lead to a huge performance drop. The best practice is to use the same window context when possible. An approach is to create one window context with specific window type and display and use it everywhere it's needed.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, window context provides the capability to receive configuration changes for existing token by overriding the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#token:android.os.IBinder` of the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#` passed in `https://developer.android.com/reference/kotlin/android/view/ViewManager.html#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)`. This is useful when an application needs to attach its window to an existing activity for window token sharing use-case.

Note that the window context in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` didn't have this capability. This is a no-op for the window context in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`.
Below is sample code to **attach an existing token to a window context:**

```kotlin
final DisplayManager dm = anyContext.getSystemService(DisplayManager.class);
  final Display primaryDisplay = dm.getDisplay(DEFAULT_DISPLAY);
  final Context windowContext = anyContext.createWindowContext(primaryDisplay,
          TYPE_APPLICATION, null);
 
  // Get an existing token.
  final IBinder existingToken = activity.getWindow().getAttributes().token;
 
  // The types used in addView() and createWindowContext() must match.
  final WindowManager.LayoutParams params = new WindowManager.LayoutParams(TYPE_APPLICATION);
  params.token = existingToken;
 
  // After WindowManager#addView(), the server side will extract the provided token from
  // LayoutParams#token (existingToken in the sample code), and switch to propagate
  // configuration changes from the node associated with the provided token.
  windowContext.getSystemService(WindowManager.class).addView(overlayView, mParams);
  
```

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, window context provides the capability to listen to its `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` changes by calling `https://developer.android.com/reference/kotlin/android/content/Context.html#registerComponentCallbacks(android.content.ComponentCallbacks)`, while other kinds of `https://developer.android.com/reference/kotlin/android/content/Context.html#` will register the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to `https://developer.android.com/reference/kotlin/android/content/Context.html#getApplicationContext()`. Note that window context only propagate `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration)` callback. `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()` or other callbacks in `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#` won't be invoked.

Note that using `https://developer.android.com/reference/kotlin/android/app/Application.html#` or `https://developer.android.com/reference/kotlin/android/app/Service.html#` context for UI-related queries may result in layout or continuity issues on devices with variable screen sizes (e.g. foldables) or in multi-window modes, since these non-UI contexts may not reflect the `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` changes for the visual container.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#databaseList()()`

Returns an array of strings naming the private databases associated with this Context's application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#deleteDatabase(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Delete an existing private SQLiteDatabase associated with this Context's application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#deleteFile(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Delete the given private file associated with this Context's application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#deleteSharedPreferences(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Delete an existing shared preferences file.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceCallingOrSelfPermission(kotlin.String,%20kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

If neither you nor the calling process of an IPC you are handling has been granted a particular permission, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#enforceCallingPermission(kotlin.String,%20kotlin.String)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceCallingOrSelfUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

If the calling process of an IPC *or you* has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#enforceCallingUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.String)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceCallingPermission(kotlin.String,%20kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

If the calling process of an IPC you are handling has not been granted a particular permission, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#enforcePermission(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always throw the SecurityException. This is done to protect against accidentally leaking permissions; you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#enforceCallingOrSelfPermission(kotlin.String,%20kotlin.String)` to avoid this protection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceCallingUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

If the calling process and uid has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#enforceUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always throw a SecurityException.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforcePermission(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

If the given permission is not allowed for a particular process and user ID running in the system, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

If a particular process and uid has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceUriPermission(android.net.Uri,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, readPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, writePermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Enforce both a Uri and normal permission. This allows you to perform both `https://developer.android.com/reference/kotlin/android/content/Context.html#enforcePermission(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)` and #enforceUriPermission in one call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#fileList()()`

Returns an array of strings naming the private files associated with this Context's application package.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getApplicationContext()()`

Return the context of the single, global Application object of the current process. This generally should only be used if you need a Context whose lifecycle is separate from the current context, that is tied to the lifetime of the process rather than the current component.

Consider for example how this interacts with `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`:

- If used from an Activity context, the receiver is being registered within that activity. This means that you are expected to unregister before the activity is done being destroyed; in fact if you do not do so, the framework will clean up your leaked registration as it removes the activity and log an error. Thus, if you use the Activity context to register a receiver that is static (global to the process, not associated with an Activity instance) then that registration will be removed on you at whatever point the activity you used is destroyed.

- If used from the Context returned here, the receiver is being registered with the global state associated with your application. Thus it will never be unregistered for you. This is necessary if the receiver is associated with static data, not a particular component. However using the ApplicationContext elsewhere can easily lead to serious leaks if you forget to unregister, unbind, etc.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getApplicationInfo()()`

Return the full application info for this context's package.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/AssetManager.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getAssets()()`

Returns an AssetManager instance for the application's package.

**Note:** Implementations of this method should return an AssetManager instance that is consistent with the Resources instance returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getResources()`. For example, they should share the same `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` object.

<br />

`https://developer.android.com/reference/kotlin/android/content/AttributionSource.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getAttributionSource()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getAttributionTag()()`

Attribution can be used in complex apps to logically separate parts of the app. E.g. a blogging app might also have a instant messaging app built in. In this case two separate tags can for used each sub-feature.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getBaseContext()()`

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getCacheDir()()`

Returns the absolute path to the application specific cache directory on the filesystem.

The system will automatically delete files in this directory as disk space is needed elsewhere on the device. The system will always delete older files first, as reported by `https://developer.android.com/reference/kotlin/java/io/File.html#lastModified()`. If desired, you can exert more control over how files are deleted using `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#setCacheBehaviorGroup(java.io.File,%20kotlin.Boolean)` and `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#setCacheBehaviorTombstone(java.io.File,%20kotlin.Boolean)`.

Apps are strongly encouraged to keep their usage of cache space below the quota returned by `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#getCacheQuotaBytes(java.util.UUID)`. If your app goes above this quota, your cached files will be some of the first to be deleted when additional disk space is needed. Conversely, if your app stays under this quota, your cached files will be some of the last to be deleted when additional disk space is needed.

Note that your cache quota will change over time depending on how frequently the user interacts with your app, and depending on how much system-wide disk space is used.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

<br />

`https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getClassLoader()()`

Return a class loader you can use to retrieve classes in this package.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getCodeCacheDir()()`

Returns the absolute path to the application specific cache directory on the filesystem designed for storing cached code.

The system will delete any files stored in this location both when your specific application is upgraded, and when the entire platform is upgraded.

This location is optimal for storing compiled or optimized code generated by your application at runtime.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

<br />

`https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getContentResolver()()`

Return a ContentResolver instance for your application's package.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDataDir()()`

Returns the absolute path to the directory on the filesystem where all private files belonging to this app are stored. Apps should not use this path directly; they should instead use `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#getDir(kotlin.String,%20kotlin.Int)`, or other storage APIs on this class.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDatabasePath(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Returns the absolute path on the filesystem where a database created with #openOrCreateDatabase is stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDeviceId()()`

Gets the device ID this context is associated with. Applications can use this method to determine whether they are running on a virtual device and identify that device. The device ID of the host device is `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int`

If the underlying device ID is changed by the system, for example, when an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` is moved to a different virtual device, applications can register to listen to changes by calling `https://developer.android.com/reference/kotlin/android/content/Context.html#registerDeviceIdChangeListener(java.util.concurrent.Executor,%20java.util.function.IntConsumer)`.

This method will only return a reliable value for this instance if it was created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createDeviceContext(kotlin.Int)`, or if this instance is a UI or Display Context. Contexts created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createDeviceContext(kotlin.Int)` will have an explicit device association, which will never change, even if the underlying device is closed or is removed. UI Contexts and Display Contexts are already associated with a display, so if the device association is not explicitly given, `https://developer.android.com/reference/kotlin/android/content/Context.html#getDeviceId()` will return the ID of the device associated with the associated display. The system can assign an arbitrary device id value for Contexts not logically associated with a device.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDir(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve, creating if needed, a new directory in which the application can place its own custom data files. You can use the returned File object to create and access files in this directory. Note that files created through a File object will only be accessible by your own application; you can only set the mode of the entire directory, not of individual files.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

<br />

`https://developer.android.com/reference/kotlin/android/view/Display.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDisplay()()`

Get the display this context is associated with. Applications should use this method with `https://developer.android.com/reference/kotlin/android/app/Activity.html#` or a context associated with a `https://developer.android.com/reference/kotlin/android/view/Display.html#` via `https://developer.android.com/reference/kotlin/android/content/Context.html#createDisplayContext(android.view.Display)` to get a display object associated with a Context, or `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplay(kotlin.Int)` to get a display object by id.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalCacheDir()()`

Returns absolute path to application-specific directory on the primary shared/external storage device where the application can place cache files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- The platform does not always monitor the space available in shared storage, and thus may not automatically delete these files. Apps should always manage the maximum space used in this location. Currently the only time files here will be deleted by the platform is when running on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int` or later and `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)` returns true.
- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directory returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()`.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the returned path; it's always accessible to the calling app. This only applies to paths generated for package name of the calling application. To access paths belonging to other packages, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` are required.

On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalCacheDirs()()`

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place cache files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- The platform does not always monitor the space available in shared storage, and thus may not automatically delete these files. Apps should always manage the maximum space used in this location. Currently the only time files here will be deleted by the platform is when running on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int` or later and `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)` returns true.
- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directory returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()`.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned paths may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalFilesDir(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Returns the absolute path to the directory on the primary shared/external storage device where the application can place persistent files it owns. These files are internal to the applications, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directories returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`, etc.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the returned path; it's always accessible to the calling app. This only applies to paths generated for package name of the calling application. To access paths belonging to other packages, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` are required.

On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

Here is an example of typical code to manipulate a file in an application's shared storage:

If you supply a non-null type to this function, the returned file will be a path to a sub-directory of the given type. Though these files are not automatically scanned by the media scanner, you can explicitly add them to the media database with `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.html#scanFile(android.content.Context,%20kotlin.Array,%20kotlin.Array,%20android.media.MediaScannerConnection.OnScanCompletedListener)`. Note that this is not the same as `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStoragePublicDirectory(kotlin.String)`, which provides directories of media shared by all applications. The directories returned here are owned by the application, and their contents will be removed when the application is uninstalled. Unlike `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStoragePublicDirectory(kotlin.String)`, the directory returned here will be automatically created for you.

Here is an example of typical code to manipulate a picture in an application's shared storage and add it to the media database:

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalFilesDirs(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place persistent files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directories returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`, etc.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalMediaDirs()()`

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place media files. These files are scanned and made available to other apps through `https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#`.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDirs(kotlin.String)` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned paths may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getFileStreamPath(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Returns the absolute path on the filesystem where a file created with `https://developer.android.com/reference/kotlin/android/content/Context.html#openFileOutput(kotlin.String,%20kotlin.Int)` is stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getFilesDir()()`

Returns the absolute path to the directory on the filesystem where files created with `https://developer.android.com/reference/kotlin/android/content/Context.html#openFileOutput(kotlin.String,%20kotlin.Int)` are stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

<br />

`https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getMainExecutor()()`

Return an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that will run enqueued tasks on the main thread associated with this context. This is the thread used to dispatch calls to application components (activities, services, etc).

<br />

`https://developer.android.com/reference/kotlin/android/os/Looper.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getMainLooper()()`

Return the Looper for the main thread of the current process. This is the thread used to dispatch calls to application components (activities, services, etc).

By definition, this method returns the same result as would be obtained by calling `https://developer.android.com/reference/kotlin/android/os/Looper.html#getMainLooper()`.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getNoBackupFilesDir()()`

Returns the absolute path to the directory on the filesystem similar to `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`. The difference is that files placed under this directory will be excluded from automatic backup to remote storage. See `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent.html#` for a full discussion of the automatic backup mechanism in Android.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getObbDir()()`

Return the primary shared/external storage directory where this application's OBB files (if there are any) can be found. Note if the application does not have any OBB files, this directory may not exist.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the path that this method returns. However, starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, to read the OBB expansion files, you must declare the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission in the app manifest and ask for permission at runtime as follows:

`<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" android:maxSdkVersion="23" />`

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission is not required, so don't ask for this permission at runtime. To handle both cases, your app must first try to read the OBB file, and if it fails, you must request `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission at runtime.

The following code snippet shows how to do this:

```kotlin
File obb = new File(obb_filename);
  boolean open_failed = false;
 
  try {
      BufferedReader br = new BufferedReader(new FileReader(obb));
      open_failed = false;
      ReadObbFile(br);
  } catch (IOException e) {
      open_failed = true;
  }
 
  if (open_failed) {
      // request READ_EXTERNAL_STORAGE permission before reading OBB file
      ReadObbFileWithPermission();
  }
  
```
On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), multiple users may share the same OBB storage location. Applications should ensure that multiple instances running under different users don't interfere with each other.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getObbDirs()()`

Returns absolute paths to application-specific directories on all shared/external storage devices where the application's OBB files (if there are any) can be found. Note if the application does not have any OBB files, these directories may not exist.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getOpPackageName()()`

Return the package name that should be used for `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#` calls from this context, so that app ops manager's uid verification will work with the name.

This is not generally intended for third party application developers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getPackageCodePath()()`

Return the full path to this context's primary Android package. The Android package is a ZIP file which contains application's primary code and assets.

Note: this is not generally useful for applications, since they should not be directly accessing the file system.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getPackageManager()()`

Return PackageManager instance to find global package information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getPackageName()()`

Return the name of this application's package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getPackageResourcePath()()`

Return the full path to this context's primary Android package. The Android package is a ZIP file which contains the application's primary resources.

Note: this is not generally useful for applications, since they should not be directly accessing the file system.

<br />

`https://developer.android.com/reference/kotlin/android/content/ContextParams.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getParams()()`

Return the set of parameters which this Context was created with, if it was created via `https://developer.android.com/reference/kotlin/android/content/Context.html#createContext(android.content.ContextParams)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getResources()()`

Returns a Resources instance for the application's package.

**Note:** Implementations of this method should return a Resources instance that is consistent with the AssetManager instance returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getAssets()`. For example, they should share the same `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` object.

<br />

`https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getSharedPreferences(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve and hold the contents of the preferences file 'name', returning a SharedPreferences through which you can retrieve and modify its values. Only one instance of the SharedPreferences object is returned to any callers for the same name, meaning they will see each other's edits as soon as they are made.

This method is thread-safe.

If the preferences directory does not already exist, it will be created when this method is called.

If a preferences file by this name does not exist, it will be created when you retrieve an editor (`https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#edit()`) and then commit changes (`https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#commit()` or `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#apply()`).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getSystemService(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Return the handle to a system-level service by name. The class of the returned object varies by the requested name. Currently available names are:

`https://developer.android.com/reference/kotlin/android/content/Context.html#WINDOW_SERVICE:kotlin.String` ("window")
: The top-level window manager in which you can place custom windows. The returned object is a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#LAYOUT_INFLATER_SERVICE:kotlin.String` ("layout_inflater")
: A `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` for inflating layout resources in this context. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#ACTIVITY_SERVICE:kotlin.String` ("activity")
: A `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#` for interacting with the global activity state of the system.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String` ("wallpaper")
: A `https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.html#` for accessing wallpapers in this context. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#POWER_SERVICE:kotlin.String` ("power")
: A `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#` for controlling power management.

`https://developer.android.com/reference/kotlin/android/content/Context.html#ALARM_SERVICE:kotlin.String` ("alarm")
: A `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#` for receiving intents at the time of your choosing.

`https://developer.android.com/reference/kotlin/android/content/Context.html#NOTIFICATION_SERVICE:kotlin.String` ("notification")
: A `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#` for informing the user of background events.

`https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String` ("keyguard")
: A `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#` for controlling keyguard.

`https://developer.android.com/reference/kotlin/android/content/Context.html#LOCATION_SERVICE:kotlin.String` ("location")
: A `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#` for controlling location (e.g., GPS) updates.

`https://developer.android.com/reference/kotlin/android/content/Context.html#SEARCH_SERVICE:kotlin.String` ("search")
: A `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#` for handling search.

`https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_MANAGER_SERVICE:kotlin.String` ("vibrator_manager")
: A `https://developer.android.com/reference/kotlin/android/os/VibratorManager.html#` for accessing the device vibrators, interacting with individual ones and playing synchronized effects on multiple vibrators.

`https://developer.android.com/reference/kotlin/android/content/Context.html#MULTISENSORY_MANAGER_SERVICE:kotlin.String` ("multisensory_manager")
: A `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager.html#` for delivering audio-haptic feedback in the Multisensory Design System

`https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_SERVICE:kotlin.String` ("vibrator")
: A `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#` for interacting with the vibrator hardware.

`https://developer.android.com/reference/kotlin/android/content/Context.html#CONNECTIVITY_SERVICE:kotlin.String` ("connectivity")
: A `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#` for handling management of network connections.

`https://developer.android.com/reference/kotlin/android/content/Context.html#IPSEC_SERVICE:kotlin.String` ("ipsec")
: A `https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#` for managing IPSec on sockets and networks.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String` ("wifi")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` for management of Wi-Fi connectivity. On releases before Android 7, it should only be obtained from an application context, and not from any other derived context to avoid memory leaks within the calling process.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String` ("wifiaware")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager.html#` for management of Wi-Fi Aware discovery and connectivity.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String` ("wifip2p")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#` for management of Wi-Fi Direct connectivity.

`https://developer.android.com/reference/kotlin/android/content/Context.html#INPUT_METHOD_SERVICE:kotlin.String` ("input_method")
: An `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#` for management of input methods.

`https://developer.android.com/reference/kotlin/android/content/Context.html#UI_MODE_SERVICE:kotlin.String` ("uimode")
: An `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#` for controlling UI modes.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DOWNLOAD_SERVICE:kotlin.String` ("download")
: A `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#` for requesting HTTP downloads

`https://developer.android.com/reference/kotlin/android/content/Context.html#BATTERY_SERVICE:kotlin.String` ("batterymanager")
: A `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#` for managing battery state

`https://developer.android.com/reference/kotlin/android/content/Context.html#JOB_SCHEDULER_SERVICE:kotlin.String` ("taskmanager")
: A `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#` for managing scheduled tasks

`https://developer.android.com/reference/kotlin/android/content/Context.html#NETWORK_STATS_SERVICE:kotlin.String` ("netstats")
: A `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#` for querying network usage statistics.

`https://developer.android.com/reference/kotlin/android/content/Context.html#HARDWARE_PROPERTIES_SERVICE:kotlin.String` ("hardware_properties")
: A `https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager.html#` for accessing hardware properties.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DOMAIN_VERIFICATION_SERVICE:kotlin.String` ("domain_verification")
: A `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager.html#` for accessing web domain approval state.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DISPLAY_HASH_SERVICE:kotlin.String` ("display_hash")
: A `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` for management of display hashes.

`https://developer.android.com/reference/kotlin/android/content/Context.html#AUTHENTICATION_POLICY_SERVICE:kotlin.String` ("authentication_policy")
: A `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#` for managing authentication related policies on the device.

<br />

Note: System services obtained via this API may be closely associated with the Context in which they are obtained from. In general, do not share the service objects between various different contexts (Activities, Applications, Services, Providers, etc.)

Note: Instant apps, for which `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isInstantApp()` returns true, don't have access to the following system services: `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`, #FINGERPRINT_SERVICE, `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`. For these services this method will return `null`. Generally, if you are running as an instant app you should always check whether the result of this method is `null`.

Note: When implementing this method, keep in mind that new services can be added on newer Android releases, so if you're looking for just the explicit names mentioned above, make sure to return `null` when you don't recognize the name --- if you throw a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` exception instead, your app might break on new Android releases.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getSystemServiceName(java.lang.Class)(serviceClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>)`

Gets the name of the system-level service that is represented by the specified class.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getTheme()()`

Return the Theme object associated with this Context.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getWallpaper()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getWallpaperDesiredMinimumHeight()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getWallpaperDesiredMinimumWidth()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)(toPackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Grant permission to access a specific Uri to another package, regardless of whether that package has general permission to access the Uri's content provider. This can be used to grant specific, temporary permissions, typically in response to user interaction (such as the user opening an attachment that you would like someone else to display).

Normally you should use `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` with the Intent being used to start an activity instead of this function directly. If you use this function directly, you should be sure to call #revokeUriPermission when the target should no longer be allowed to access it.

To succeed, the content provider owning the Uri must have set the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestProvider_grantUriPermissions:kotlin.Int` attribute in its manifest or included the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestGrantUriPermission:kotlin.IntArray` tag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#isDeviceProtectedStorage()()`

Indicates if the storage APIs of this Context are backed by device-protected storage.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#isRestricted()()`

Indicates whether this Context is restricted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#isUiContext()()`

Returns `true` if the context is a UI context which can access UI components such as `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`, `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` or `https://developer.android.com/reference/kotlin/android/app/WallpaperManager.html#`. Accessing UI components from non-UI contexts throws `https://developer.android.com/reference/kotlin/android/os/strictmode/Violation.html#` if `https://developer.android.com/reference/kotlin/android/os/StrictMode.VmPolicy.Builder.html#detectIncorrectContextUse()` is enabled.

Examples of UI contexts are an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, a context created from `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)` or `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#`

Note that even if it is allowed programmatically, it is not suggested to override this method to bypass `https://developer.android.com/reference/kotlin/android/os/strictmode/IncorrectContextUseViolation.html#` verification.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#moveDatabaseFrom(android.content.Context,%20kotlin.String)(sourceContext: https://developer.android.com/reference/kotlin/android/content/Context.html#!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Move an existing database file from the given source storage context to this context. This is typically used to migrate data between storage locations after an upgrade, such as migrating to device protected storage.

The database must be closed before being moved.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#moveSharedPreferencesFrom(android.content.Context,%20kotlin.String)(sourceContext: https://developer.android.com/reference/kotlin/android/content/Context.html#!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Move an existing shared preferences file from the given source storage context to this context. This is typically used to migrate data between storage locations after an upgrade, such as moving to device protected storage.

<br />

`https://developer.android.com/reference/kotlin/java/io/FileInputStream.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#openFileInput(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Open a private file associated with this Context's application package for reading.

<br />

`https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#openFileOutput(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Open a private file associated with this Context's application package for writing. Creates the file if it doesn't already exist.

No additional permissions are required for the calling app to read or write the returned file.

<br />

`https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#openOrCreateDatabase(kotlin.String,%20kotlin.Int,%20android.database.sqlite.SQLiteDatabase.CursorFactory)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory.html#!)`

Open a new private SQLiteDatabase associated with this Context's application package. Create the database file if it doesn't exist.

<br />

`https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#openOrCreateDatabase(kotlin.String,%20kotlin.Int,%20android.database.sqlite.SQLiteDatabase.CursorFactory,%20android.database.DatabaseErrorHandler)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory.html#!, errorHandler: https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#?)`

Open a new private SQLiteDatabase associated with this Context's application package. Creates the database file if it doesn't exist.

Accepts input param: a concrete instance of `https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#` to be used to handle corruption when sqlite reports database corruption.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#peekWallpaper()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#rebindService(android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)(conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#)`

Rebind an application service with updated bind service flags

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerComponentCallbacks(android.content.ComponentCallbacks)(callback: https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#!)`

Add a new `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to the base application of the Context, which will be called at the same times as the ComponentCallbacks methods of activities and other components are called. Note that you *must* be sure to use `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterComponentCallbacks(android.content.ComponentCallbacks)` when appropriate in the future; this will not be removed for you.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` will be registered to `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getBaseContext()`, and can be only used after `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#attachBaseContext(android.content.Context)`. Users can still call to `getApplicationContext().registerComponentCallbacks(ComponentCallbacks)` to add `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to the base application.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerDeviceIdChangeListener(java.util.concurrent.Executor,%20java.util.function.IntConsumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)`

Adds a new device ID changed listener to the `Context`, which will be called when the device association is changed by the system.

The callback can be called when an app is moved to a different device and the `Context` is not explicitly associated with a specific device.

When an application receives a device id update callback, this Context is guaranteed to also have an updated display ID(if any) and `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#`.

<br />

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!)`

Register a BroadcastReceiver to be run in the main activity thread. The receiver will be called with any broadcast Intent that matches filter, in the main application thread.

The system may broadcast Intents that are "sticky" -- these stay around after the broadcast has finished, to be sent to any later registrations. If your IntentFilter matches one of these sticky Intents, that Intent will be returned by this function **and** sent to your receiver as if it had just been broadcast.

There may be multiple sticky Intents that match filter, in which case each of these will be sent to receiver. In this case, only one of these can be returned directly by the function; which of these that is returned is arbitrarily decided by the system.

If you know the Intent you are registering for is sticky, you can supply null for your receiver. In this case, no receiver is registered -- the function simply returns the sticky Intent that matches filter. In the case of multiple matches, the same rules as described above apply.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, either `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_EXPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_NOT_EXPORTED:kotlin.Int` must be specified if the receiver is not being registered for [system broadcasts](https://developer.android.com/guide/components/broadcasts#system-broadcasts) or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.Int)` to register a receiver with flags.

Note: this method *cannot be called from a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` component;* that is, from a BroadcastReceiver that is declared in an application's manifest. It is okay, however, to call this method from another BroadcastReceiver that has itself been registered at run time with #registerReceiver, since the lifetime of such a registered BroadcastReceiver is tied to the object that registered it.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.Int)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Register to receive intent broadcasts, with the receiver optionally being exposed to Instant Apps. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)` for more information. By default Instant Apps cannot interact with receivers in other applications, this allows you to expose a receiver that Instant Apps can interact with.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!, broadcastPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)`

Register to receive intent broadcasts, to run in the context of scheduler. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)` for more information. This allows you to enforce permissions on who can broadcast intents to your receiver, or have the receiver run in a different thread than the main application thread.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, either `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_EXPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_NOT_EXPORTED:kotlin.Int` must be specified if the receiver is not being registered for [system broadcasts](https://developer.android.com/guide/components/broadcasts#system-broadcasts) or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler,%20kotlin.Int)` to register a receiver with flags.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler,%20kotlin.Int)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!, broadcastPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Register to receive intent broadcasts, to run in the context of scheduler. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler)` for more information.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#removeStickyBroadcast(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Remove the data previously sent with #sendStickyBroadcast, so that it is as if the sticky broadcast had never happened. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#removeStickyBroadcastAsUser(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#removeStickyBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

You must hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String` permission in order to use this API. If you do not hold that permission, `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#revokeSelfPermissionsOnKill(kotlin.collections.MutableCollection)(permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)`

Triggers the revocation of one or more permissions for the calling package. A package is only able to revoke runtime permissions. If a permission is not currently granted, it is ignored and will not get revoked (even if later granted by the user). Ultimately, you should never make assumptions about a permission status as users may grant or revoke them at any time.

Background permissions which have no corresponding foreground permission still granted once the revocation is effective will also be revoked.

The revocation happens asynchronously and kills all processes running in the calling UID. It will be triggered once it is safe to do so. In particular, it will not be triggered as long as the package remains in the foreground, or has any active manifest components (e.g. when another app is accessing a content provider in the package).

If you want to revoke the permissions right away, you could call `System.exit()` in `Handler.postDelayed` with a delay to allow completion of async IPC, But `System.exit()` could affect other apps that are accessing your app at the moment. For example, apps accessing a content provider in your app will all crash.

Note that the settings UI shows a permission group as granted as long as at least one permission in the group is granted. If you want the user to observe the revocation in the settings, you should revoke every permission in the target group. To learn the current list of permissions in a group, you may use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getGroupOfPlatformPermission(kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPlatformPermissionsForGroup(kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`. This list of permissions may evolve over time, so it is recommended to check whether it contains any permission you wish to retain before trying to revoke an entire group.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#revokeUriPermission(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Remove all permissions to access a particular content provider Uri that were previously added with `https://developer.android.com/reference/kotlin/android/content/Context.html#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` or *any other* mechanism. The given Uri will match all previously granted Uris that are the same or a sub-path of the given Uri. That is, revoking "content://foo/target" will revoke both "content://foo/target" and "content://foo/target/sub", but not "content://foo". It will not remove any prefix grants that exist at a higher level.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, if you did not have regular permission access to a Uri, but had received access to it through a specific Uri permission grant, you could not revoke that grant with this function and a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` would be thrown. As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, this function will not throw a security exception, but will remove whatever permission grants to the Uri had been given to the app (or none).

Unlike `https://developer.android.com/reference/kotlin/android/content/Context.html#revokeUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)`, this method impacts all permission grants matching the given Uri, for any package they had been granted to, through any mechanism this had happened (such as indirectly through the clipboard, activity launch, service start, etc). That means this can be potentially dangerous to use, as it can revoke grants that another app could be strongly expecting to stick around.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#revokeUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)(targetPackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Remove permissions to access a particular content provider Uri that were previously added with `https://developer.android.com/reference/kotlin/android/content/Context.html#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` for a specific target package. The given Uri will match all previously granted Uris that are the same or a sub-path of the given Uri. That is, revoking "content://foo/target" will revoke both "content://foo/target" and "content://foo/target/sub", but not "content://foo". It will not remove any prefix grants that exist at a higher level.

Unlike `https://developer.android.com/reference/kotlin/android/content/Context.html#revokeUriPermission(android.net.Uri,%20kotlin.Int)`, this method will *only* revoke permissions that had been explicitly granted through `https://developer.android.com/reference/kotlin/android/content/Context.html#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` and only for the package specified. Any matching grants that have happened through other mechanisms (clipboard, activity launching, service starting, etc) will not be removed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Broadcast the given intent to all interested BroadcastReceivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent,%20kotlin.String)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Broadcast the given intent to all interested BroadcastReceivers, allowing an optional required permission to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Broadcast the given intent to all interested BroadcastReceivers, allowing an optional required permission to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcastAsUser(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcastAsUser(android.content.Intent,%20android.os.UserHandle,%20kotlin.String)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent,%20kotlin.String)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.String,%20android.os.Bundle,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, receiverAppOp: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Broadcast the given intent to all interested BroadcastReceivers, delivering them one at a time to allow more preferred receivers to consume the broadcast before it is delivered to less preferred receivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)` method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

Like `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`, this method is asynchronous; it will return before resultReceiver.onReceive() is called.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Broadcast the given intent to all interested BroadcastReceivers, delivering them one at a time to allow more preferred receivers to consume the broadcast before it is delivered to less preferred receivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.os.Bundle,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)` method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

Like `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`, this method is asynchronous; it will return before resultReceiver.onReceive() is called.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, receiverAppOp: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the App Op to enforce restrictions on which receivers the broadcast will be sent to.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcastAsUser(android.content.Intent,%20android.os.UserHandle,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyBroadcast(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Perform a `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` that is "sticky," meaning the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. In all other ways, this behaves the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyBroadcast(android.content.Intent,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Perform a `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent)` that is "sticky," meaning the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. In all other ways, this behaves the same as `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyBroadcastAsUser(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendStickyBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyOrderedBroadcast(android.content.Intent,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of #sendStickyBroadcast that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)` method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

Like `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`, this method is asynchronous; it will return before resultReceiver.onReceive() is called. Note that the sticky data stored is only the data you initially supply to the broadcast, not the result of any changes made by the receivers.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyOrderedBroadcastAsUser(android.content.Intent,%20android.os.UserHandle,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendStickyOrderedBroadcast(android.content.Intent,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#setTheme(kotlin.Int)(resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the base theme for this context. Note that this should be called before any views are instantiated in the Context (for example before calling android.app.Activity#setContentView or android.view.LayoutInflater#inflate).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#setWallpaper(android.graphics.Bitmap)(bitmap: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#setWallpaper(java.io.InputStream)(data: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#shouldShowRequestPermissionRationale(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Gets whether you should show UI with rationale before requesting a permission. If the permission does not exist on this SDK level or is not visible to this app, the method will return `false`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startActivities(kotlin.Array)(intents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent.html#!>!)`

Same as `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivities(kotlin.Array,%20android.os.Bundle)` with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startActivities(kotlin.Array,%20android.os.Bundle)(intents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent.html#!>!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Launch multiple new activities. This is generally the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` for the first Intent in the array, that activity during its creation calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` for the second entry, etc. Note that unlike that approach, generally none of the activities except the last in the array will be created at this point, but rather will be created when the user first visits them (due to pressing back from the activity on top).

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found for *any* given Intent. In this case the state of the activity stack is undefined (some Intents in the list may be on it, some not), so you probably want to avoid such situations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startActivity(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Same as `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)` with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startActivity(android.content.Intent,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Launch a new activity. You will not receive any information about when the activity exits.

Note that if this method is being called from outside of an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` Context, then the Intent must include the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` launch flag. This is because, without being started from an existing Activity, there is no existing task in which to place the new activity and thus it needs to be placed in its own separate task.

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found to run the given Intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startForegroundService(android.content.Intent)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Similar to `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`, but with an implicit promise that the Service will call `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification)` once it begins running. The service is given an amount of time comparable to the ANR interval to do this, otherwise the system will automatically crash the process, in which case an internal exception `ForegroundServiceDidNotStartInTimeException` is logged on logcat on devices running SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or later. On older Android versions, an internal exception `RemoteServiceException` is logged instead, with a corresponding message.

Unlike the ordinary `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`, this method can be used at any time, regardless of whether the app hosting the service is in a foreground state.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](../about/versions/12/behavior-changes-12.md) for more details.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startInstrumentation(android.content.ComponentName,%20kotlin.String,%20android.os.Bundle)(className: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, profileFile: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, arguments: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Start executing an `https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#` class. The given Instrumentation component will be run by killing its target application (if currently running), starting the target process, instantiating the instrumentation component, and then letting it drive the application.

This function is not synchronous -- it returns as soon as the instrumentation has started and while it is running.

Instrumentation is normally only allowed to run against a package that is either unsigned or signed with a signature that the the instrumentation package is also signed with (ensuring the target trusts the instrumentation).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Same as `https://developer.android.com/reference/kotlin/android/content/Context.html#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)` with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Like `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)`, but taking a IntentSender to start. If the IntentSender is for an activity, that activity will be started as if you had called the regular `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` here; otherwise, its associated action will be executed (such as sending a broadcast) as if you had called android.content.IntentSender#sendIntent on it.

<br />

`https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startService(android.content.Intent)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Request that a given application service be started. The Intent should either contain the complete class name of a specific service implementation to start, or a specific package name to target. If the Intent is less specified, it logs a warning about this. In this case any of the multiple matching services may be used. If this service is not already running, it will be instantiated and started (creating a process for it if needed); if it is running then it remains running.

Every call to this method will result in a corresponding call to the target service's `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` method, with the intent given here. This provides a convenient way to submit jobs to a service without having to bind and call on to its interface.

Using startService() overrides the default service lifetime that is managed by #bindService: it requires the service to remain running until `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` is called, regardless of whether any clients are connected to it. Note that calls to startService() do not nest: no matter how many times you call startService(), a single call to `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` will stop it.

The system attempts to keep running services around as much as possible. The only time they should be stopped is if the current foreground application is using so many resources that the service needs to be killed. If any errors happen in the service's process, it will automatically be restarted.

This function will throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if you do not have permission to start the given service.

**Note:** Each call to startService() results in significant work done by the system to manage service lifecycle surrounding the processing of the intent, which can take multiple milliseconds of CPU time. Due to this cost, startService() should not be used for frequent intent delivery to a service, and only for scheduling significant work. Use #bindService for high frequency calls.
Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` or higher are not allowed to start background services from the background. See [Background Execution Limits](../about/versions/oreo/background.md) for more details.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](../about/versions/12/behavior-changes-12.md) for more details.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#stopService(android.content.Intent)(name: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Request that a given application service be stopped. If the service is not running, nothing happens. Otherwise it is stopped. Note that calls to startService() are not counted -- this stops the service no matter how many times it was started.

If the service is running as a foreground service when it is stopped, its associated notification will be removed. To avoid this, apps can use `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)` to decouple the notification from the service's lifecycle before stopping it.

Note that if a stopped service still has `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#` objects bound to it with the `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_AUTO_CREATE:kotlin.Int` set, it will not be destroyed until all of these bindings are removed. See the `https://developer.android.com/reference/kotlin/android/app/Service.html#` documentation for more details on a service's lifecycle.

This function will throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if you do not have permission to stop the given service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unbindService(android.content.ServiceConnection)(conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

Disconnect from an application service. You will no longer receive calls as the service is restarted, and the service is now allowed to stop at any time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterComponentCallbacks(android.content.ComponentCallbacks)(callback: https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#!)`

Remove a `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` object that was previously registered with `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerComponentCallbacks(android.content.ComponentCallbacks)`.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` will be unregistered to `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getBaseContext()`, and can be only used after `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#attachBaseContext(android.content.Context)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterDeviceIdChangeListener(java.util.function.IntConsumer)(listener: https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)`

Removes a device ID changed listener from the Context. It's a no-op if the listener is not already registered.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterReceiver(android.content.BroadcastReceiver)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#!)`

Unregister a previously registered BroadcastReceiver. *All* filters that have been registered for this BroadcastReceiver will be removed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#updateServiceBindings(kotlin.collections.MutableCollection)(params: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/content/Context.UpdateBindingParams.html#!>)`

Perform a batch update of existing bindings. Existing bindings can be rebound with an updated set of flags, or unbound. Only flags returned from `https://developer.android.com/reference/kotlin/android/content/Context.html#getUpdateableFlags()` may be added or removed.

This API behaves as if the `https://developer.android.com/reference/kotlin/android/content/Context.html#rebindService(android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)` and `https://developer.android.com/reference/kotlin/android/content/Context.html#unbindService(android.content.ServiceConnection)` API are called in the same order as the params are iterated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#updateServiceGroup(android.content.ServiceConnection,%20kotlin.Int,%20kotlin.Int)(conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, group: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, importance: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

For a service previously bound with #bindService or a related method, change how the system manages that service's process in relation to other processes. This doesn't modify the original bind flags that were passed in when binding, but adjusts how the process will be managed in some cases based on those flags. Currently only works on isolated processes (will be ignored for non-isolated processes).

Note that this call does not take immediate effect, but will be applied the next time the impacted process is adjusted for some other reason. Typically you would call this before then calling a new #bindIsolatedService on the service of interest, with that binding causing the process to be shuffled accordingly.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#bindIsolatedService(android.content.Intent,%20android.content.Context.BindServiceFlags,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#, instanceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

See `https://developer.android.com/reference/kotlin/android/content/Context.html#bindIsolatedService(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#getColor(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a color associated with a particular resource ID and styled for the current theme.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#getColorStateList(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a color state list associated with a particular resource ID and styled for the current theme.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` `https://developer.android.com/reference/kotlin/android/content/Context.html#getDrawable(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a drawable object associated with a particular resource ID and styled for the current theme.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#getString(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a localized string from the application's package's default string table.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#getString(kotlin.Int,%20kotlin.Any)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, vararg formatArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)`

Returns a localized formatted string from the application's package's default string table, substituting the format arguments as defined in `https://developer.android.com/reference/kotlin/java/util/Formatter.html#` and java.lang.String#format.

<br />

`T` `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(java.lang.Class)(serviceClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)`

Return the handle to a system-level service by class.

Currently available classes are: `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`, `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#`, `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#`, `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#`, `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#`, `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#`, `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#`, `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#`, `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#`, `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#`, `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#`, `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#`, `https://developer.android.com/reference/kotlin/android/media/MediaRouter.html#`, `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#`, `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#`, `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#`, `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#`, `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#`, `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#`, `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#`, `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager.html#`, `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#`.

Note: System services obtained via this API may be closely associated with the Context in which they are obtained from. In general, do not share the service objects between various different contexts (Activities, Applications, Services, Providers, etc.)

Note: Instant apps, for which `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isInstantApp()` returns true, don't have access to the following system services: `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`, #FINGERPRINT_SERVICE, `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`. For these services this method will return `null`. Generally, if you are running as an instant app you should always check whether the result of this method is `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#getText(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return a localized, styled CharSequence from the application's package's default string table.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#getUpdateableFlags()()`

Gets the list of bind flags that may be updated (i.e. added or removed) for an existing connection. Includes:

- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_NOT_FOREGROUND:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ABOVE_CLIENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ALLOW_OOM_MANAGEMENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_WAIVE_PRIORITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_IMPORTANT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_NOT_PERCEPTIBLE:kotlin.Int`

<br />

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray)(set: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#?, attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)(set: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#?, attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, defStyleAttr: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, defStyleRes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#obtainStyledAttributes(kotlin.Int,%20kotlin.IntArray)(resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(kotlin.Int,%20kotlin.IntArray)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#obtainStyledAttributes(kotlin.IntArray)(attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(kotlin.IntArray)` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#revokeSelfPermissionOnKill(kotlin.String)(permName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Triggers the asynchronous revocation of a runtime permission. If the permission is not currently granted, nothing happens (even if later granted by the user).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcastWithMultiplePermissions(android.content.Intent,%20kotlin.Array)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)`

Broadcast the given intent to all interested BroadcastReceivers, allowing an array of required permissions to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

From class `https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService` `https://developer.android.com/reference/kotlin/android/view/KeyEvent.DispatcherState.html#!` `https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService#getKeyDispatcherState()()`

Return the global `https://developer.android.com/reference/kotlin/android/view/KeyEvent.DispatcherState.html#` for used for processing events from the target application. Normally you will not need to use this directly, but just use the standard high-level event callbacks like `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyDown(kotlin.Int,%20android.view.KeyEvent)`.

<br />

`https://developer.android.com/reference/kotlin/android/os/IBinder.html#?` `https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService#onBind(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Return the communication channel to the service. May return null if clients can not bind to the service. The returned `https://developer.android.com/reference/kotlin/android/os/IBinder.html#` is usually for a complex interface that has been [described using aidl](https://developer.android.com/guide/components/aidl.html).

*Note that unlike other application components, calls on to the IBinder interface returned here may not happen on the main thread of the process* . More information about the main thread can be found in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService#onLowMemory()()`

Override `https://developer.android.com/reference/kotlin/android/app/Service.html#`'s empty implementation and listen to `ActivityThread` for low memory and trim memory events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService#onTrimMemory(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. You should never compare to exact values of the level, since new intermediate values may be added -- you will typically want to compare if the value is greater or equal to a level you are interested in.

To retrieve the processes current trim level at any point, you can use `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#getMyMemoryState(android.app.ActivityManager.RunningAppProcessInfo)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService#registerComponentCallbacks(android.content.ComponentCallbacks)(callback: https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#)`

Here we override to prevent WindowProviderService from invoking Application.registerComponentCallback, which will result in callback registered for process-level Configuration change updates.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService#unregisterComponentCallbacks(android.content.ComponentCallbacks)(callback: https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#)`

Remove a `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` object that was previously registered with `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerComponentCallbacks(android.content.ComponentCallbacks)`.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` will be unregistered to `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getBaseContext()`, and can be only used after `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#attachBaseContext(android.content.Context)`

<br />

From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`

Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources.

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()()`

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing.

<br />

From class `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyDown(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)`

Called when a key down event has occurred. If you return true, you can first call `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#startTracking()` to have the framework track the event through its `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyUp(kotlin.Int,%20android.view.KeyEvent)` and also call your `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)` if it occurs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)`

Called when a long press has occurred. If you return true, the final key up will have `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#FLAG_CANCELED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#FLAG_CANCELED_LONG_PRESS:kotlin.Int` set. Note that in order to receive this callback, someone in the event change *must* return true from `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyDown(kotlin.Int,%20android.view.KeyEvent)` *and* call `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#startTracking()` on the event.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)`

Called when a user's interaction with an analog control, such as flinging a trackball, generates simulated down/up events for the same key multiple times in quick succession.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyUp(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)`

Called when a key up event has occurred.

<br />

## XML attributes

### android:imeExtractEnterAnimation

```
android:imeExtractEnterAnimation
```
Animation to use when showing the fullscreen extract UI after it had previously been hidden.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:imeExtractExitAnimation

```
android:imeExtractExitAnimation
```
Animation to use when hiding the fullscreen extract UI after it had previously been shown.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:imeFullscreenBackground

```
android:imeFullscreenBackground
```
Background to use for entire input method when it is being shown in fullscreen mode with the extract view, to ensure that it completely covers the application. This allows, for example, the candidate view to be hidden while in fullscreen mode without having the application show through behind it.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

May be a color value, in the form of "`rgb`", "`argb`", "`rrggbb`", or "`aarrggbb`".

## Constants

### BACK_DISPOSITION_ADJUST_NOTHING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BACK_DISPOSITION_ADJUST_NOTHING: Int
```

Asks the system to not adjust the back button affordance even when the software keyboard is shown.

This mode is useful for UI modes where IME's main soft input window is used for some supplemental UI, such as floating candidate window for languages such as Chinese and Japanese, where users expect the back button is, or at least looks to be, handled by the target application rather than the UI shown by the IME even while `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#isInputViewShown()` returns `true`.

Note that `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` events continue to be sent to `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onKeyDown(kotlin.Int,%20android.view.KeyEvent)` even when this mode is specified. The default implementation of `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onKeyDown(kotlin.Int,%20android.view.KeyEvent)` for `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` does not take this mode into account.

For IMEs targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int` or higher with `android:enableOnBackInvokedCallback="true"` set in the manifest, specifying this mode causes back events to bypass the IME and be sent directly to the application. If the IME still wants to receive back events in this mode, it must register a custom `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback.html#`.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setBackDisposition(kotlin.Int)`

### BACK_DISPOSITION_DEFAULT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BACK_DISPOSITION_DEFAULT: Int
```

Allows the system to optimize the back button affordance based on the presence of software keyboard.

For instance, on devices that have navigation bar and software-rendered back button, the system may use a different icon while `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#isInputViewShown()` returns `true`, to indicate that the back button has "dismiss" affordance.

Note that `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` events continue to be sent to `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onKeyDown(kotlin.Int,%20android.view.KeyEvent)` even when this mode is specified. The default implementation of `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onKeyDown(kotlin.Int,%20android.view.KeyEvent)` for `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` does not take this mode into account.

For API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O_MR1:kotlin.Int` and lower devices, this is the only mode you can safely specify without worrying about the compatibility.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setBackDisposition(kotlin.Int)`

### BACK_DISPOSITION_WILL_DISMISS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BACK_DISPOSITION_WILL_DISMISS: Int
```

**Deprecated:** *on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and later devices, this flag is handled as a synonym of `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_DEFAULT:kotlin.Int`. On `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O_MR1:kotlin.Int` and prior devices, expected behavior of this mode had not been well defined. In AOSP implementation running on devices that have navigation bar, specifying this flag could change the software back button to "Dismiss" icon no matter whether the software keyboard is shown or not, but there would be no easy way to restore the icon state even after IME lost the connection to the application. To avoid user confusions, do not specify this mode anyway*

Deprecated flag.

To avoid compatibility issues, IME developers should not use this flag.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setBackDisposition(kotlin.Int)`

### BACK_DISPOSITION_WILL_NOT_DISMISS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BACK_DISPOSITION_WILL_NOT_DISMISS: Int
```

**Deprecated:** *on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and later devices, this flag is handled as a synonym of `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_DEFAULT:kotlin.Int`. On `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O_MR1:kotlin.Int` and prior devices, expected behavior of this mode had not been well defined. Most likely the end result would be the same as `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_DEFAULT:kotlin.Int`. Either way it is not recommended to use this mode*

Deprecated flag.

To avoid compatibility issues, IME developers should not use this flag.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setBackDisposition(kotlin.Int)`

## Public constructors

### InputMethodService

```
InputMethodService()
```

## Public methods

### enableHardwareAcceleration

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun enableHardwareAcceleration(): Boolean
```

**Deprecated:** *Starting in API 21, hardware acceleration is always enabled on capable devices*

You can call this to try to enable accelerated drawing for your IME. This must be set before `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreate()`, so you will typically call it in your constructor. It is not always possible to use hardware accelerated drawing in an IME (for example on low-end devices that do not have the resources to support this), so the call `true` if it succeeds otherwise `false` if you will need to draw in software. You must be able to handle either case.

In API 21 and later, system may automatically enable hardware accelerated drawing for your IME on capable devices even if this method is not explicitly called. Make sure that your IME is able to handle either case.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if accelerated drawing is successfully enabled otherwise `false`. On API 21 and later devices the return value is basically just a hint and your IME does not need to change the behavior based on the it |

### finishConnectionlessStylusHandwriting

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun finishConnectionlessStylusHandwriting(text: CharSequence?): Unit
```

Finishes the current connectionless stylus handwriting session and delivers the result.

This dismisses the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingWindow()` and stops intercepting stylus `MotionEvent`s.

Note for IME developers: Call this method at any time to finish the current handwriting session. Generally, this should be invoked after a short timeout, giving the user enough time to start the next stylus stroke, if any. By default, system will time-out after few seconds. To override default timeout, use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setStylusHandwritingSessionTimeout(java.time.Duration)`.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: This value may be `null`. |

### finishStylusHandwriting

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun finishStylusHandwriting(): Unit
```

Finish the current stylus handwriting session.

This dismisses the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingWindow()` and stops intercepting stylus `MotionEvent`s.

Connectionless handwriting sessions should be finished using `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#finishConnectionlessStylusHandwriting(kotlin.CharSequence)`.

Note for IME developers: Call this method at any time to finish the current handwriting session. Generally, this should be invoked after a short timeout, giving the user enough time to start the next stylus stroke, if any. By default, system will time-out after few seconds. To override default timeout, use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setStylusHandwritingSessionTimeout(java.time.Duration)`.

Handwriting session will be finished by framework on next `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishInput()`.

### getBackDisposition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBackDisposition(): Int
```

Retrieves the current disposition mode that indicates the expected back button affordance.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | currently selected disposition mode. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_WILL_NOT_DISMISS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_WILL_DISMISS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_ADJUST_NOTHING:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setBackDisposition(kotlin.Int)`

### getCandidatesHiddenVisibility

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCandidatesHiddenVisibility(): Int
```

Returns the visibility mode (either `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View.html#GONE:kotlin.Int`) of the candidates view when it is not shown. The default implementation returns GONE when `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#isExtractViewShown()` returns true, otherwise INVISIBLE. Be careful if you change this to return GONE in other situations -- if showing or hiding the candidates view causes your window to resize, this can cause temporary drawing artifacts as the resize takes place.

### getCurrentInputBinding

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrentInputBinding(): InputBinding!
```

Return the currently active InputBinding for the input method, or null if there is none.

### getCurrentInputConnection

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrentInputConnection(): InputConnection!
```

Retrieve the currently active InputConnection that is bound to the input method, or null if there is none.

### getCurrentInputEditorInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrentInputEditorInfo(): EditorInfo!
```

### getCurrentInputStarted

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrentInputStarted(): Boolean
```

### getInputMethodWindowRecommendedHeight

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInputMethodWindowRecommendedHeight(): Int
```

**Deprecated:** *the actual behavior of this method has never been well defined. You cannot use this method in a reliable and predictable way*

Aimed to return the previous input method's `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.Insets#contentTopInsets:kotlin.Int`, but its actual semantics has never been well defined.

Note that the previous document clearly mentioned that this method could return `0` at any time for whatever reason. Now this method is just always returning `0`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | on Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later devices this method always returns `0` |

### getLayoutInflater

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayoutInflater(): LayoutInflater!
```

### getMaxWidth

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxWidth(): Int
```

Return the maximum width, in pixels, available the input method. Input methods are positioned at the bottom of the screen and, unless running in fullscreen, will generally want to be as short as possible so should compute their height based on their contents. However, they can stretch as much as needed horizontally. The function returns to you the maximum amount of space available horizontally, which you can use if needed for UI placement.

In many cases this is not needed, you can just rely on the normal view layout mechanisms to position your views within the full horizontal space given to the input method.

Note that this value can change dynamically, in particular when the screen orientation changes.

### getStylusHandwritingIdleTimeoutMax

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getStylusHandwritingIdleTimeoutMax(): Duration
```

Returns the maximum stylus handwriting session idle-timeout for use with `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setStylusHandwritingSessionTimeout(java.time.Duration)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartStylusHandwriting()`
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishStylusHandwriting()`
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingSessionTimeout()`

### getStylusHandwritingSessionTimeout

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStylusHandwritingSessionTimeout(): Duration
```

Returns the duration after which an ongoing stylus handwriting session that hasn't received new `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`s will time out and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#finishStylusHandwriting()` will be called. The current timeout can be changed using `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setStylusHandwritingSessionTimeout(java.time.Duration)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingIdleTimeoutMax()`
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartStylusHandwriting()`
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishStylusHandwriting()`

### getStylusHandwritingWindow

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStylusHandwritingWindow(): Window?
```

Returns the stylus handwriting inking window. IMEs supporting stylus input are expected to attach their inking views to this window (e.g. with `https://developer.android.com/reference/kotlin/android/view/Window.html#setContentView(android.view.View)` )). Handwriting-related `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`s are dispatched to the attached view hierarchy. Note: This returns `null` if IME doesn't support stylus handwriting i.e. if `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo.html#supportsStylusHandwriting()` is false. This method should be called after `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartStylusHandwriting()`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartStylusHandwriting()`

### getSystemService

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemService(name: String): Any?
```

Return the handle to a system-level service by name. The class of the returned object varies by the requested name. Currently available names are:

`https://developer.android.com/reference/kotlin/android/content/Context.html#WINDOW_SERVICE:kotlin.String` ("window")
: The top-level window manager in which you can place custom windows. The returned object is a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#LAYOUT_INFLATER_SERVICE:kotlin.String` ("layout_inflater")
: A `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` for inflating layout resources in this context. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#ACTIVITY_SERVICE:kotlin.String` ("activity")
: A `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#` for interacting with the global activity state of the system.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String` ("wallpaper")
: A `https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.html#` for accessing wallpapers in this context. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#POWER_SERVICE:kotlin.String` ("power")
: A `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#` for controlling power management.

`https://developer.android.com/reference/kotlin/android/content/Context.html#ALARM_SERVICE:kotlin.String` ("alarm")
: A `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#` for receiving intents at the time of your choosing.

`https://developer.android.com/reference/kotlin/android/content/Context.html#NOTIFICATION_SERVICE:kotlin.String` ("notification")
: A `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#` for informing the user of background events.

`https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String` ("keyguard")
: A `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#` for controlling keyguard.

`https://developer.android.com/reference/kotlin/android/content/Context.html#LOCATION_SERVICE:kotlin.String` ("location")
: A `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#` for controlling location (e.g., GPS) updates.

`https://developer.android.com/reference/kotlin/android/content/Context.html#SEARCH_SERVICE:kotlin.String` ("search")
: A `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#` for handling search.

`https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_MANAGER_SERVICE:kotlin.String` ("vibrator_manager")
: A `https://developer.android.com/reference/kotlin/android/os/VibratorManager.html#` for accessing the device vibrators, interacting with individual ones and playing synchronized effects on multiple vibrators.

`https://developer.android.com/reference/kotlin/android/content/Context.html#MULTISENSORY_MANAGER_SERVICE:kotlin.String` ("multisensory_manager")
: A `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager.html#` for delivering audio-haptic feedback in the Multisensory Design System

`https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_SERVICE:kotlin.String` ("vibrator")
: A `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#` for interacting with the vibrator hardware.

`https://developer.android.com/reference/kotlin/android/content/Context.html#CONNECTIVITY_SERVICE:kotlin.String` ("connectivity")
: A `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#` for handling management of network connections.

`https://developer.android.com/reference/kotlin/android/content/Context.html#IPSEC_SERVICE:kotlin.String` ("ipsec")
: A `https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#` for managing IPSec on sockets and networks.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String` ("wifi")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` for management of Wi-Fi connectivity. On releases before Android 7, it should only be obtained from an application context, and not from any other derived context to avoid memory leaks within the calling process.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String` ("wifiaware")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager.html#` for management of Wi-Fi Aware discovery and connectivity.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String` ("wifip2p")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#` for management of Wi-Fi Direct connectivity.

`https://developer.android.com/reference/kotlin/android/content/Context.html#INPUT_METHOD_SERVICE:kotlin.String` ("input_method")
: An `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#` for management of input methods.

`https://developer.android.com/reference/kotlin/android/content/Context.html#UI_MODE_SERVICE:kotlin.String` ("uimode")
: An `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#` for controlling UI modes.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DOWNLOAD_SERVICE:kotlin.String` ("download")
: A `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#` for requesting HTTP downloads

`https://developer.android.com/reference/kotlin/android/content/Context.html#BATTERY_SERVICE:kotlin.String` ("batterymanager")
: A `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#` for managing battery state

`https://developer.android.com/reference/kotlin/android/content/Context.html#JOB_SCHEDULER_SERVICE:kotlin.String` ("taskmanager")
: A `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#` for managing scheduled tasks

`https://developer.android.com/reference/kotlin/android/content/Context.html#NETWORK_STATS_SERVICE:kotlin.String` ("netstats")
: A `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#` for querying network usage statistics.

`https://developer.android.com/reference/kotlin/android/content/Context.html#HARDWARE_PROPERTIES_SERVICE:kotlin.String` ("hardware_properties")
: A `https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager.html#` for accessing hardware properties.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DOMAIN_VERIFICATION_SERVICE:kotlin.String` ("domain_verification")
: A `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager.html#` for accessing web domain approval state.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DISPLAY_HASH_SERVICE:kotlin.String` ("display_hash")
: A `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` for management of display hashes.

`https://developer.android.com/reference/kotlin/android/content/Context.html#AUTHENTICATION_POLICY_SERVICE:kotlin.String` ("authentication_policy")
: A `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#` for managing authentication related policies on the device.

<br />

Note: System services obtained via this API may be closely associated with the Context in which they are obtained from. In general, do not share the service objects between various different contexts (Activities, Applications, Services, Providers, etc.)

Note: Instant apps, for which `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isInstantApp()` returns true, don't have access to the following system services: `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`, #FINGERPRINT_SERVICE, `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`. For these services this method will return `null`. Generally, if you are running as an instant app you should always check whether the result of this method is `null`.

Note: When implementing this method, keep in mind that new services can be added on newer Android releases, so if you're looking for just the explicit names mentioned above, make sure to return `null` when you don't recognize the name --- if you throw a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` exception instead, your app might break on new Android releases.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | This value may be `null`. |

### getTextForImeAction

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextForImeAction(imeOptions: Int): CharSequence!
```

Return text that can be used as a button label for the given `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#imeOptions:kotlin.Int`. Returns null if there is no action requested. Note that there is no guarantee that the returned text will be relatively short, so you probably do not want to use it as text on a soft keyboard key label.

| Parameters ||
|---|---|
| `imeOptions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value from `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#imeOptions:kotlin.Int`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | Returns a label to use, or null if there is no action. |

### getWindow

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWindow(): Dialog!
```

### hideStatusIcon

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hideStatusIcon(): Unit
```

### hideWindow

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hideWindow(): Unit
```

### isExtractViewShown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isExtractViewShown(): Boolean
```

Return whether the fullscreen extract view is shown. This will only return true if `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#isFullscreenMode()` returns true, and in that case its value depends on the last call to `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setExtractViewShown(kotlin.Boolean)`. This effectively lets you determine if the application window is entirely covered (when this returns true) or if some part of it may be shown (if this returns false, though if `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#isFullscreenMode()` returns true in that case then it is probably only a sliver of the application).

### isFullscreenMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFullscreenMode(): Boolean
```

Return whether the input method is *currently* running in fullscreen mode. This is the mode that was last determined and applied by `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#updateFullscreenMode()`.

### isInputViewShown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInputViewShown(): Boolean
```

Returns whether the window is currently requested to be shown. Note that despite the method's name, the returned value does not reflect the window's *actual* visibility.

### isShowInputRequested

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isShowInputRequested(): Boolean
```

Returns whether the window is currently requested to be shown with the input area *and* can currently be shown. Note that the returned value does not reflect the window's *actual* visibility.

### onAppPrivateCommand

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onAppPrivateCommand(
    action: String!, 
    data: Bundle!
): Unit
```

Not implemented in this class.

### onBindInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onBindInput(): Unit
```

Called when a new client has bound to the input method. This may be followed by a series of `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInput(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)` and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishInput()` calls as the user navigates through its UI. Upon this call you know that `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getCurrentInputBinding()` and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getCurrentInputConnection()` return valid objects.

### onComputeInsets

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onComputeInsets(outInsets: InputMethodService.Insets!): Unit
```

Compute the interesting insets into your UI. The default implementation uses the top of the candidates frame for the visible insets, and the top of the input frame for the content insets. The default touchable insets are `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.Insets#TOUCHABLE_INSETS_VISIBLE:kotlin.Int`.

Note that this method is not called when `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#isExtractViewShown()` returns true, since in that case the application is left as-is behind the input method and not impacted by anything in its UI.

| Parameters ||
|---|---|
| `outInsets` | [InputMethodService.Insets](../android/inputmethodservice/InputMethodService.Insets.md)!: Fill in with the current UI insets. |

### onConfigurationChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConfigurationChanged(newConfig: Configuration): Unit
```

Take care of handling configuration changes. Subclasses of InputMethodService generally don't need to deal directly with this on their own; the standard implementation here takes care of regenerating the input method UI as a result of the configuration change, so you can rely on your `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateInputView()` and other methods being called as appropriate due to a configuration change.

When a configuration change does happen, `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onInitializeInterface()` is guaranteed to be called the next time prior to any of the other input or UI creation callbacks. The following will be called immediately depending if appropriate for current state: `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInput(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)` if input is active, and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateInputView()` and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInputView(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)` and related appropriate functions if the UI is displayed.

From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` and then starting with android.os.Build.VERSION_CODES#CINNAMON_BUN_1, IMEs can opt into handling configuration changes themselves instead of being restarted with `https://developer.android.com/reference/kotlin/android/R.styleable.html#InputMethod_configChanges:kotlin.Int`.

Between `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, configuration changes that IMEs declared for themselves to handle were not recognized due to an XML parsing error.

| Parameters ||
|---|---|
| `newConfig` | [Configuration](../android.content.res/Configuration.md): The new device configuration. This value cannot be `null`. |
| `configuration` | This value cannot be `null`. |

### onConfigureWindow

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConfigureWindow(
    win: Window!, 
    isFullscreen: Boolean, 
    isCandidatesOnly: Boolean
): Unit
```

Update the given window's parameters for the given mode. This is called when the window is first displayed and each time the fullscreen or candidates only mode changes.

The default implementation makes the layout for the window MATCH_PARENT x MATCH_PARENT when in fullscreen mode, and MATCH_PARENT x WRAP_CONTENT when in non-fullscreen mode.

| Parameters ||
|---|---|
| `win` | [Window](../android.view/Window.md)!: The input method's window. |
| `isFullscreen` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, the window is running in fullscreen mode and intended to cover the entire application display. |
| `isCandidatesOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, the window is only showing the candidates view and none of the rest of its UI. This is mutually exclusive with fullscreen mode. |
| --- | --- |

### onCreate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreate(): Unit
```

Called by the system when the service is first created. Do not call this method directly.

### onCreateCandidatesView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateCandidatesView(): View!
```

Create and return the view hierarchy used to show candidates. This will be called once, when the candidates are first displayed. You can return null to have no candidates view; the default implementation returns null.

To control when the candidates view is displayed, use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setCandidatesViewShown(kotlin.Boolean)`. To change the candidates view after the first one is created by this function, use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setCandidatesView(android.view.View)`.

### onCreateExtractTextView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateExtractTextView(): View!
```

Called by the framework to create the layout for showing extracted text. Only called when in fullscreen mode. The returned view hierarchy must have an `https://developer.android.com/reference/kotlin/android/inputmethodservice/ExtractEditText` whose ID is `https://developer.android.com/reference/kotlin/android/R.id.html#inputExtractEditText:kotlin.Int`, with action ID `https://developer.android.com/reference/kotlin/android/R.id.html#inputExtractAction:kotlin.Int` and accessories ID `https://developer.android.com/reference/kotlin/android/R.id.html#inputExtractAccessories:kotlin.Int`.

### onCreateInlineSuggestionsRequest

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateInlineSuggestionsRequest(uiExtras: Bundle): InlineSuggestionsRequest?
```

Called when Autofill is requesting an `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#` from the IME.

The Autofill Framework will first request the IME to create and send an `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#` back. Once Autofill Framework receives a valid request and also receives valid inline suggestions, they will be returned via `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onInlineSuggestionsResponse(android.view.inputmethod.InlineSuggestionsResponse)`.

IME Lifecycle - The request will wait to be created after inputStarted

If the IME wants to support displaying inline suggestions, they must set supportsInlineSuggestions in its XML and implement this method to return a valid `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#`.

| Parameters ||
|---|---|
| `uiExtras` | [Bundle](../android.os/Bundle.md): the extras that contain the UI renderer related information. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#?` | an `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#` to be sent to Autofill. This value may be `null`. |

### onCreateInputMethodInterface

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateInputMethodInterface(): AbstractInputMethodService.AbstractInputMethodImpl!
```

**Deprecated:** *Overriding or calling this method is strongly discouraged. A future version of Android will remove the ability to use this method. Use the callbacks on `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#` as `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onBindInput()`, `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUnbindInput()`, `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onWindowShown()`, `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onWindowHidden()`, etc.*

Implement to return our standard `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.InputMethodImpl`.

### onCreateInputMethodSessionInterface

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateInputMethodSessionInterface(): AbstractInputMethodService.AbstractInputMethodSessionImpl!
```

**Deprecated:** *Overriding or calling this method is strongly discouraged. Most methods in `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.InputMethodSessionImpl` have corresponding callbacks. Use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishInput()`, `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onDisplayCompletions(kotlin.Array)`, `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateExtractedText(kotlin.Int,%20android.view.inputmethod.ExtractedText)`, `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateSelection(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` instead.*

Implement to return our standard `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.InputMethodSessionImpl`.

IMEs targeting on Android U and above cannot override this method, or an `https://developer.android.com/reference/kotlin/java/lang/LinkageError.html#` would be thrown.

### onCreateInputView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateInputView(): View!
```

Create and return the view hierarchy used for the input area (such as a soft keyboard). This will be called once, when the input area is first displayed. You can return null to have no input area; the default implementation returns null.

To control when the input view is displayed, implement `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onEvaluateInputViewShown()`. To change the input view after the first one is created by this function, use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setInputView(android.view.View)`.

### onCustomImeSwitcherButtonRequestedVisible

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCustomImeSwitcherButtonRequestedVisible(visible: Boolean): Unit
```

Called when the requested visibility of a custom IME Switcher button changes.

When this method is called with `true` by the system, the IME must show a button within its UI to switch IMEs. When it is called with `false`, it must hide this button.

Normally, the system provides a button for switching to a different IME when that is appropriate. Under certain circumstances, namely when the IME successfully asks to hide the system-provided navigation bar (with `getWindowInsetsController().hide(captionBar())`), providing this button is delegated to the IME through this callback.

This does not depend on the current visibility of the IME. It could be called with `true` while the IME is hidden, in which case the IME should prepare to show the button as soon as the IME itself is shown.

This is only called when the requested visibility changes. The default value is `false` and as such, this will not be called initially if the resulting value is `false`.

This can be called at any time after `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreate()`, even if the IME is not currently visible. However, this is not guaranteed to be called before the IME is shown, as it may depend on the IME requesting to hide the system-provided navigation bar. If the request is sent during the showing flow (e.g. during `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInputView(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)`), this will be called shortly after `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onWindowShown()`, but before the first IME frame is drawn.

| Parameters ||
|---|---|
| `visible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the button is requested visible or not. |

### onDestroy

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDestroy(): Unit
```

Called by the system to notify a Service that it is no longer used and is being removed. The service should clean up any resources it holds (threads, registered receivers, etc) at this point. Upon return, there will be no more calls in to this Service object and it is effectively dead. Do not call this method directly. If you override this method you *must* call through to the superclass implementation.

### onDisplayCompletions

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDisplayCompletions(completions: Array<CompletionInfo!>!): Unit
```

Called when the application has reported auto-completion candidates that it would like to have the input method displayed. Typically these are only used when an input method is running in full-screen mode, since otherwise the user can see and interact with the pop-up window of completions shown by the application.

The default implementation here does nothing.

### onEvaluateFullscreenMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onEvaluateFullscreenMode(): Boolean
```

Override this to control when the input method should run in fullscreen mode. The default implementation runs in fullsceen only when the screen is in landscape mode. If you change what this returns, you will need to call `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#updateFullscreenMode()` yourself whenever the returned value may have changed to have it re-evaluated and applied.

### onEvaluateInputViewShown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onEvaluateInputViewShown(): Boolean
```

Override this to control when the soft input area should be shown to the user. The default implementation returns `false` when there is no hard keyboard or the keyboard is hidden unless the user shows an intention to use software keyboard. If you change what this returns, you will need to call `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#updateInputViewShown()` yourself whenever the returned value may have changed to have it re-evaluated and applied.

When you override this method, it is recommended to call `super.onEvaluateInputViewShown()` and return `true` when `true` is returned.
. 
If you override this method you *must* call through to the superclass implementation.

### onExtractTextContextMenuItem

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onExtractTextContextMenuItem(id: Int): Boolean
```

This is called when the user has selected a context menu item from the extracted text view, when running in fullscreen mode. The default implementation sends this action to the current InputConnection's `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#performContextMenuAction(kotlin.Int)`, for it to be processed in underlying "real" editor. Re-implement this to provide whatever behavior you want.

### onExtractedCursorMovement

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onExtractedCursorMovement(
    dx: Int, 
    dy: Int
): Unit
```

This is called when the user has performed a cursor movement in the extracted text view, when it is running in fullscreen mode. The default implementation hides the candidates view when a vertical movement happens, but only if the extracted text editor has a vertical scroll bar because its text doesn't fit. Re-implement this to provide whatever behavior you want.

| Parameters ||
|---|---|
| `dx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The amount of cursor movement in the x dimension. |
| `dy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The amount of cursor movement in the y dimension. |

### onExtractedSelectionChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onExtractedSelectionChanged(
    start: Int, 
    end: Int
): Unit
```

This is called when the user has moved the cursor in the extracted text view, when running in fullsreen mode. The default implementation performs the corresponding selection change on the underlying text editor.

### onExtractedTextClicked

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onExtractedTextClicked(): Unit
```

This is called when the user has clicked on the extracted text view, when running in fullscreen mode. The default implementation hides the candidates view when this happens, but only if the extracted text editor has a vertical scroll bar because its text doesn't fit. Re-implement this to provide whatever behavior you want.

### onExtractingInputChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onExtractingInputChanged(ei: EditorInfo!): Unit
```

This is called when, while currently displayed in extract mode, the current input target changes. The default implementation will auto-hide the IME if the new target is not a full editor, since this can be a confusing experience for the user.

### onFinishCandidatesView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onFinishCandidatesView(finishingInput: Boolean): Unit
```

Called when the candidates view is being hidden from the user. This will be called either prior to hiding the window, or prior to switching to another target for editing.

The default implementation uses the InputConnection to clear any active composing text; you can override this (not calling the base class implementation) to perform whatever behavior you would like.

| Parameters ||
|---|---|
| `finishingInput` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishInput()` will be called immediately after. |

### onFinishInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onFinishInput(): Unit
```

Called to inform the input method that text input has finished in the last editor. At this point there may be a call to `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInput(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)` to perform input in a new editor, or the input method may be left idle. This method is *not* called when input restarts in the same editor.

The default implementation uses the InputConnection to clear any active composing text; you can override this (not calling the base class implementation) to perform whatever behavior you would like.

### onFinishInputView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onFinishInputView(finishingInput: Boolean): Unit
```

Called when the input view is being hidden from the user. This will be called either prior to hiding the window, or prior to switching to another target for editing.

The default implementation uses the InputConnection to clear any active composing text; you can override this (not calling the base class implementation) to perform whatever behavior you would like.

| Parameters ||
|---|---|
| `finishingInput` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishInput()` will be called immediately after. |

### onFinishStylusHandwriting

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onFinishStylusHandwriting(): Unit
```

Called when the current stylus handwriting session was finished (either by the system or via `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#finishStylusHandwriting()`. When this is called, the ink window has been made invisible, and the IME no longer intercepts handwriting-related `MotionEvent`s.

### onGenericMotionEvent

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onGenericMotionEvent(event: MotionEvent!): Boolean
```

Override this to intercept generic motion events before they are processed by the application. If you return true, the application will not itself process the event. If you return false, the normal application processing will occur as if the IME had not seen the event at all.

| Parameters ||
|---|---|
| `event` | [MotionEvent](../android.view/MotionEvent.md)!: The motion event being received. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled in this function, false otherwise. |

### onInitializeInterface

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onInitializeInterface(): Unit
```

This is a hook that subclasses can use to perform initialization of their interface. It is called for you prior to any of your UI objects being created, both after the service is first created and after a configuration change happens.

### onInlineSuggestionsResponse

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onInlineSuggestionsResponse(response: InlineSuggestionsResponse): Boolean
```

Called when Autofill responds back with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsResponse.html#` containing inline suggestions.

Should be implemented by subclasses.

| Parameters ||
|---|---|
| `response` | [InlineSuggestionsResponse](../android.view.inputmethod/InlineSuggestionsResponse.md): `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsResponse.html#` passed back by Autofill. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the IME will use and render the inline suggestions. |

### onKeyDown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyDown(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

Called back when a `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#` is forwarded from the target application.

The default implementation intercepts `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` if the IME is currently shown , to possibly hide it when the key goes up (if not canceled or long pressed). In addition, in fullscreen mode only, it will consume DPAD movement events to move the cursor in the extracted text view, not allowing them to perform navigation in the underlying application.

The default implementation does not take flags specified to `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setBackDisposition(kotlin.Int)` into account, even on API version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and later devices. IME developers are responsible for making sure that their special handling for `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` are consistent with the flag they specified to `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#setBackDisposition(kotlin.Int)`.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value in `event.getKeyCode()` |
| `event` | [KeyEvent](../android.view/KeyEvent.md)!: Description of the key event |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the event is consumed by the IME and the application no longer needs to consume it. Return `false` when the event should be handled as if the IME had not seen the event at all. |

### onKeyLongPress

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyLongPress(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

Default implementation of `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)`: always returns false (doesn't handle the event).

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value in event.getKeyCode(). |
| `event` | [KeyEvent](../android.view/KeyEvent.md)!: Description of the key event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyMultiple

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyMultiple(
    keyCode: Int, 
    count: Int, 
    event: KeyEvent!
): Boolean
```

Override this to intercept special key multiple events before they are processed by the application. If you return true, the application will not itself process the event. If you return false, the normal application processing will occur as if the IME had not seen the event at all.

The default implementation always returns false, except when in fullscreen mode, where it will consume DPAD movement events to move the cursor in the extracted text view, not allowing them to perform navigation in the underlying application.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value in event.getKeyCode(). |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of pairs as returned by event.getRepeatCount(). |
| `event` | [KeyEvent](../android.view/KeyEvent.md)!: Description of the key event. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyUp

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyUp(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

Override this to intercept key up events before they are processed by the application. If you return true, the application will not itself process the event. If you return false, the normal application processing will occur as if the IME had not seen the event at all.

The default implementation intercepts `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` to hide the current IME UI if it is shown. In addition, in fullscreen mode only, it will consume DPAD movement events to move the cursor in the extracted text view, not allowing them to perform navigation in the underlying application.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value in event.getKeyCode(). |
| `event` | [KeyEvent](../android.view/KeyEvent.md)!: Description of the key event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onPrepareStylusHandwriting

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPrepareStylusHandwriting(): Unit
```

Called to prepare stylus handwriting. The system calls this before the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartStylusHandwriting()` request.

Note: The system tries to call this as early as possible, when it detects that handwriting stylus input is imminent. However, that a subsequent call to `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartStylusHandwriting()` actually happens is not guaranteed.

### onShouldVerifyKeyEvent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onShouldVerifyKeyEvent(keyEvent: KeyEvent): Boolean
```

Received by the IME before dispatching to `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onKeyDown(kotlin.Int,%20android.view.KeyEvent)` to determine if the `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#` requires system-level verification of its authenticity.

KeyEvents may originate from outside the system (e.g., injected via shell or third-party applications). Sensitive keys or those that trigger critical IME actions should be marked for verification. When marked for verification, the system will check whether the event originated from a trusted source.

To protect against replay attacks or unauthorized input injection, the system will drop events that cannot be verified as authentic when they are delivered after an unexpected delay (exceeding a system-defined threshold). In such cases, the event will not be delivered to the IME's key handling methods.

| Parameters ||
|---|---|
| `event` | This value cannot be `null`. |
| `keyEvent` | [KeyEvent](../android.view/KeyEvent.md): the event that may need verification. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#` should be verified for authenticity before dispatch, `false` otherwise. |

### onShowInputRequested

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onShowInputRequested(
    flags: Int, 
    configChange: Boolean
): Boolean
```

The system has decided that it may be time to show your input method. This is called due to a corresponding call to your `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod.html#showSoftInput(kotlin.Int,%20android.os.ResultReceiver)` method. The default implementation uses `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onEvaluateInputViewShown()`, `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onEvaluateFullscreenMode()`, and the current configuration to decide whether the input view should be shown at this point.

| Parameters ||
|---|---|
| `configChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): This is true if we are re-showing due to a configuration change. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true to indicate that the window should be shown. |

### onStartCandidatesView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStartCandidatesView(
    editorInfo: EditorInfo!, 
    restarting: Boolean
): Unit
```

Called when only the candidates view has been shown for showing processing as the user enters text through a hard keyboard. This will always be called after `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInput(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)`, allowing you to do your general setup there and just view-specific setup here. You are guaranteed that `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateCandidatesView()` will have been called some time before this function is called.

Note that this will *not* be called when the input method is running in full editing mode, and thus receiving `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInputView(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)` to initiate that operation. This is only for the case when candidates are being shown while the input method editor is hidden but wants to show its candidates UI as text is entered through some other mechanism.

| Parameters ||
|---|---|
| `editorInfo` | [EditorInfo](../android.view.inputmethod/EditorInfo.md)!: Description of the type of text being edited. |
| `restarting` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to true if we are restarting input on the same text field as before. |

### onStartConnectionlessStylusHandwriting

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStartConnectionlessStylusHandwriting(
    inputType: Int, 
    cursorAnchorInfo: CursorAnchorInfo?
): Boolean
```

Called when an app requests to start a connectionless stylus handwriting session using one of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#startConnectionlessStylusHandwriting(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`, or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20kotlin.String,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`.

A connectionless stylus handwriting session differs from a regular session in that an input connection is not used to communicate with a text editor. Instead, the recognised text is delivered when the IME finishes the connectionless session using `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#finishConnectionlessStylusHandwriting(kotlin.CharSequence)`.

If the IME can start the connectionless handwriting session, it should return `true`, ensure its inking views are attached to the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingWindow()`, and handle stylus input received from `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStylusHandwritingMotionEvent(android.view.MotionEvent)` on the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingWindow()`.

| Parameters ||
|---|---|
| `cursorAnchorInfo` | [CursorAnchorInfo](../android.view.inputmethod/CursorAnchorInfo.md)?: This value may be `null`. |

### onStartInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStartInput(
    attribute: EditorInfo!, 
    restarting: Boolean
): Unit
```

Called to inform the input method that text input has started in an editor. You should use this callback to initialize the state of your input to match the state of the editor given to it.

| Parameters ||
|---|---|
| `attribute` | [EditorInfo](../android.view.inputmethod/EditorInfo.md)!: The attributes of the editor that input is starting in. |
| `restarting` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to true if input is restarting in the same editor such as because the application has changed the text in the editor. Otherwise will be false, indicating this is a new session with the editor. |

### onStartInputView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStartInputView(
    editorInfo: EditorInfo!, 
    restarting: Boolean
): Unit
```

Called when the input view is being shown and input has started on a new editor. This will always be called after `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInput(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)`, allowing you to do your general setup there and just view-specific setup here. You are guaranteed that `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateInputView()` will have been called some time before this function is called.

| Parameters ||
|---|---|
| `editorInfo` | [EditorInfo](../android.view.inputmethod/EditorInfo.md)!: Description of the type of text being edited. |
| `restarting` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to true if we are restarting input on the same text field as before. |

### onStartStylusHandwriting

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStartStylusHandwriting(): Boolean
```

Called when an app requests stylus handwriting `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#startStylusHandwriting(android.view.View)`. This will always be preceded by `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInput(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)` for the `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#` for which stylus handwriting is being requested. If the IME supports handwriting for the current input, it should return `true`, ensure its inking views are attached to the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingWindow()`, and handle stylus input received from `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStylusHandwritingMotionEvent(android.view.MotionEvent)` on the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingWindow()` via `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getCurrentInputConnection()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if IME can honor the request, `false` if IME cannot at this time. |

### onStylusHandwritingMotionEvent

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStylusHandwritingMotionEvent(motionEvent: MotionEvent): Unit
```

Called after `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartStylusHandwriting()` returns `true` for every Stylus `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`. By default, this method forwards all `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`s to the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingWindow()` once its visible, however IME can override it to receive them sooner.

| Parameters ||
|---|---|
| `motionEvent` | [MotionEvent](../android.view/MotionEvent.md): `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#` from stylus. This value cannot be `null`. |

### onTrackballEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTrackballEvent(event: MotionEvent!): Boolean
```

Override this to intercept trackball motion events before they are processed by the application. If you return true, the application will not itself process the event. If you return false, the normal application processing will occur as if the IME had not seen the event at all.

| Parameters ||
|---|---|
| `event` | [MotionEvent](../android.view/MotionEvent.md)!: The motion event being received. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled in this function, false otherwise. |

### onUnbindInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUnbindInput(): Unit
```

Called when the previous bound client is no longer associated with the input method. After returning `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getCurrentInputBinding()` and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getCurrentInputConnection()` will no longer return valid objects.

### onUpdateCursor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUpdateCursor(newCursor: Rect!): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateCursorAnchorInfo(android.view.inputmethod.CursorAnchorInfo)` instead.*

Called when the application has reported a new location of its text cursor. This is only called if explicitly requested by the input method. The default implementation does nothing.

### onUpdateCursorAnchorInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUpdateCursorAnchorInfo(cursorAnchorInfo: CursorAnchorInfo!): Unit
```

Called when the application has reported a new location of its text insertion point and characters in the composition string. This is only called if explicitly requested by the input method. The default implementation does nothing.

| Parameters ||
|---|---|
| `cursorAnchorInfo` | [CursorAnchorInfo](../android.view.inputmethod/CursorAnchorInfo.md)!: The positional information of the text insertion point and the composition string. |

### onUpdateEditorToolType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUpdateEditorToolType(toolType: Int): Unit
```

Called when the user tapped or clicked an editor. This can be useful when IME makes a decision of showing Virtual keyboard based on what `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getToolType(kotlin.Int)` was used to click the editor. e.g. when toolType is `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_STYLUS:kotlin.Int`, IME may choose to show a companion widget instead of normal virtual keyboard.

This method is called after `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInput(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)` and before `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartInputView(android.view.inputmethod.EditorInfo,%20kotlin.Boolean)` when editor was clicked with a known tool type.

Default implementation does nothing.

| Parameters ||
|---|---|
| `toolType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): what `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getToolType(kotlin.Int)` was used to click on editor. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_FINGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_STYLUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_MOUSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_ERASER:kotlin.Int` |

### onUpdateExtractedText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUpdateExtractedText(
    token: Int, 
    text: ExtractedText!
): Unit
```

Called when the application has reported new extracted text to be shown due to changes in its current text state. The default implementation here places the new text in the extract edit text, when the input method is running in fullscreen mode.

### onUpdateExtractingViews

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUpdateExtractingViews(ei: EditorInfo!): Unit
```

Called when the fullscreen-mode extracting editor info has changed, to update the state of its UI such as the action buttons shown. You do not need to deal with this if you are using the standard full screen extract UI. If replacing it, you will need to re-implement this to put the appropriate action button in your own UI and handle it, and perform any other changes.

The standard implementation turns on or off its accessory area depending on whether there is an action button, and hides or shows the entire extract area depending on whether it makes sense for the current editor. In particular, a `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NULL:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_FILTER:kotlin.Int` input type will turn off the extract area since there is no text to be shown.

### onUpdateExtractingVisibility

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUpdateExtractingVisibility(ei: EditorInfo!): Unit
```

Called when the fullscreen-mode extracting editor info has changed, to determine whether the extracting (extract text and candidates) portion of the UI should be shown. The standard implementation hides or shows the extract area depending on whether it makes sense for the current editor. In particular, a `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NULL:kotlin.Int` input type or `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#IME_FLAG_NO_EXTRACT_UI:kotlin.Int` flag will turn off the extract area since there is no text to be shown.

### onUpdateSelection

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUpdateSelection(
    oldSelStart: Int, 
    oldSelEnd: Int, 
    newSelStart: Int, 
    newSelEnd: Int, 
    candidatesStart: Int, 
    candidatesEnd: Int
): Unit
```

Called when the application has reported a new selection region of the text. This is called whether or not the input method has requested extracted text updates, although if so it will not receive this call if the extracted text has changed as well.

The default implementation takes care of updating the cursor in the extract text, if it is being shown.

### onViewClicked

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onViewClicked(focusChanged: Boolean): Unit
```

**Deprecated:** *The method may not be called for composite `https://developer.android.com/reference/kotlin/android/view/View.html#` that works as a giant "Canvas", which can host its own UI hierarchy and sub focus state. `https://developer.android.com/reference/kotlin/android/webkit/WebView.html#` is a good example. Application / IME developers should not rely on this method. If your goal is just being notified when an on-going input is interrupted, simply monitor `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishInput()`. If your goal is to know what `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getToolType(kotlin.Int)` clicked on editor, use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateEditorToolType(kotlin.Int)` instead.*

Called when the user tapped or clicked a text view. IMEs can't rely on this method being called because this was not part of the original IME protocol, so applications with custom text editing written before this method appeared will not call to inform the IME of this interaction.

| Parameters ||
|---|---|
| `focusChanged` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the user changed the focused view by this click. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#viewClicked(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateEditorToolType(kotlin.Int)`

### onWindowHidden

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onWindowHidden(): Unit
```

Called when the input method window has been hidden from the user, after previously being visible.

### onWindowShown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onWindowShown(): Unit
```

Called immediately before the input method window is shown to the user. You could override this to prepare for the window to be shown (update view structure etc).

### requestHideSelf

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestHideSelf(flags: Int): Unit
```

Close this input method's soft input area, removing it from the display. The input method will continue running, but the user can no longer use it to generate input by touching the screen.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#HIDE_IMPLICIT_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#HIDE_NOT_ALWAYS:kotlin.Int` |

### requestShowSelf

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestShowSelf(flags: Int): Unit
```

Show the input method's soft input area, so the user sees the input method window and can interact with it.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#SHOW_IMPLICIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#SHOW_FORCED:kotlin.Int` |

### sendDefaultEditorAction

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendDefaultEditorAction(fromEnterKey: Boolean): Boolean
```

Ask the input target to execute its default action via `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#performEditorAction(kotlin.Int)`.

For compatibility, this method does not execute a custom action even if `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#actionLabel:kotlin.CharSequence` is set. The implementor should directly call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#performEditorAction(kotlin.Int)` with `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#actionId:kotlin.Int` if they want to execute a custom action.

| Parameters ||
|---|---|
| `fromEnterKey` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, this will be executed as if the user had pressed an enter key on the keyboard, that is it will *not* be done if the editor has set `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#IME_FLAG_NO_ENTER_ACTION:kotlin.Int`. If false, the action will be sent regardless of how the editor has set that flag. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns a boolean indicating whether an action has been sent. If false, either the editor did not specify a default action or it does not want an action from the enter key. If true, the action was sent (or there was no input connection at all). |

### sendDownUpKeyEvents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendDownUpKeyEvents(keyEventCode: Int): Unit
```

Send the given key event code (as defined by `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#`) to the current input connection is a key down + key up event pair. The sent events have `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#FLAG_SOFT_KEYBOARD:kotlin.Int` set, so that the recipient can identify them as coming from a software input method, and `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#FLAG_KEEP_TOUCH_MODE:kotlin.Int`, so that they don't impact the current touch mode of the UI.

Note that it's discouraged to send such key events in normal operation; this is mainly for use with `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NULL:kotlin.Int` type text fields, or for non-rich input methods. A reasonably capable software input method should use the android.view.inputmethod.InputConnection#commitText family of methods to send text to an application, rather than sending key events.

| Parameters ||
|---|---|
| `keyEventCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The raw key code to send, as defined by `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#`. |

### sendKeyChar

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendKeyChar(charCode: Char): Unit
```

Send the given UTF-16 character to the current input connection. Most characters will be delivered simply by calling android.view.inputmethod.InputConnection#commitText with the character; some, however, may be handled different. In particular, the enter character ('\\n') will either be delivered as an action code or a raw key event, as appropriate. Consider this as a convenience method for IMEs that do not have a full implementation of actions; a fully complying IME will decide of the right action for each event and will likely never call this method except maybe to handle events coming from an actual hardware keyboard.

| Parameters ||
|---|---|
| `charCode` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The UTF-16 character code to send. |

### setBackDisposition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackDisposition(disposition: Int): Unit
```

Sets the disposition mode that indicates the expected affordance for the back button.

Keep in mind that specifying this flag does not change the the default behavior of `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onKeyDown(kotlin.Int,%20android.view.KeyEvent)`. It is IME developers' responsibility for making sure that their custom implementation of `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onKeyDown(kotlin.Int,%20android.view.KeyEvent)` is consistent with the mode specified to this API.

Note: For IMEs targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int` or higher with `android:enableOnBackInvokedCallback="true"` set in the manifest, setting the mode to `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_ADJUST_NOTHING:kotlin.Int` will cause back events to bypass the IME and be sent directly to the application.

| Parameters ||
|---|---|
| `disposition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): disposition mode to be set. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_WILL_NOT_DISMISS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_WILL_DISMISS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#BACK_DISPOSITION_ADJUST_NOTHING:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getBackDisposition()`

### setCandidatesView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCandidatesView(view: View!): Unit
```

Replaces the current candidates view with a new one. You only need to call this when dynamically changing the view; normally, you should implement `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateCandidatesView()` and create your view when first needed by the input method.

### setCandidatesViewShown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCandidatesViewShown(shown: Boolean): Unit
```

Controls the visibility of the candidates display area. By default it is hidden.

### setExtractView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExtractView(view: View!): Unit
```

### setExtractViewShown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExtractViewShown(shown: Boolean): Unit
```

Controls the visibility of the extracted text area. This only applies when the input method is in fullscreen mode, and thus showing extracted text. When false, the extracted text will not be shown, allowing some of the application to be seen behind. This is normally set for you by `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onUpdateExtractingVisibility(android.view.inputmethod.EditorInfo)`. This controls the visibility of both the extracted text and candidate view; the latter since it is not useful if there is no text to see.

### setInputView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInputView(view: View!): Unit
```

Replaces the current input view with a new one. You only need to call this when dynamically changing the view; normally, you should implement `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreateInputView()` and create your view when first needed by the input method.

### setStylusHandwritingRegion

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setStylusHandwritingRegion(handwritingRegion: Region): Unit
```

Sets a new stylus handwriting region as user continues to write on an editor on screen. Stylus strokes that are started within the `touchableRegion` are treated as continuation of handwriting and all the events outside are passed-through to the IME target app, causing stylus handwriting to finish `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#finishStylusHandwriting()`. By default, the entire screen area is handwritable and `touchableRegion` resets after each handwriting session.

For example, the IME can use this API to dynamically expand the stylus handwriting region on every stylus stroke as user continues to write on an editor. The region should grow around the last stroke so that a UI element below the IME window is still interactable when it is spaced sufficiently away (\~2 character dimensions) from last stroke.

Note: Setting handwriting touchable region is supported on IMEs that support stylus handwriting `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo.html#supportsStylusHandwriting()`.

Note: If the IME decides to use this API, it should be updating the desired region accordingly, on configuration changes, such as changes of screen bounds, density.

| Parameters ||
|---|---|
| `handwritingRegion` | [Region](../android.graphics/Region.md): new stylus handwritable `https://developer.android.com/reference/kotlin/android/graphics/Region.html#` that can accept stylus touch. This value cannot be `null`. |

### setStylusHandwritingSessionTimeout

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setStylusHandwritingSessionTimeout(duration: Duration): Unit
```

Sets the duration after which an ongoing stylus handwriting session that hasn't received new `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`s will time out and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#finishStylusHandwriting()` will be called. The maximum allowed duration is returned by `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingIdleTimeoutMax()`, larger values will be clamped. Note: this value is bound to the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#` instance and resets to the default whenever a new instance is constructed.

| Parameters ||
|---|---|
| `duration` | [Duration](../java.time/Duration.md): timeout to set. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onStartStylusHandwriting()`
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onFinishStylusHandwriting()`
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#getStylusHandwritingSessionTimeout()`

### setTheme

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTheme(theme: Int): Unit
```

You can call this to customize the theme used by your IME's window. This theme should typically be one that derives from `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_InputMethod:kotlin.Int`, which is the default theme you will get. This must be set before `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onCreate()`, so you will typically call it in your constructor with the resource ID of your custom theme.

| Parameters ||
|---|---|
| `resid` | The style resource describing the theme. |

### shouldOfferSwitchingToNextInputMethod

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun shouldOfferSwitchingToNextInputMethod(): Boolean
```

Returns true if the current IME needs to offer the users ways to switch to a next input method (e.g. a globe key.). When an IME sets supportsSwitchingToNextInputMethod and this method returns true, the IME has to offer ways to to invoke `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#switchToNextInputMethod(kotlin.Boolean)` accordingly.

Note that the system determines the most appropriate next input method and subtype in order to provide the consistent user experience in switching between IMEs and subtypes.

### showStatusIcon

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun showStatusIcon(iconResId: Int): Unit
```

### showWindow

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun showWindow(showInput: Boolean): Unit
```

### switchInputMethod

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun switchInputMethod(id: String!): Unit
```

Force switch to a new input method, as identified by id. This input method will be destroyed, and the requested one started on the current input field.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Unique identifier of the new input method to start. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the input method is unknown or filtered by the rules of [package visibility](../training/basics/intents/package-visibility.md). |

### switchInputMethod

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun switchInputMethod(
    id: String!, 
    subtype: InputMethodSubtype!
): Unit
```

Force switch to a new input method, as identified by `id`. This input method will be destroyed, and the requested one started on the current input field.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Unique identifier of the new input method to start. |
| `subtype` | [InputMethodSubtype](../android.view.inputmethod/InputMethodSubtype.md)!: The new subtype of the new input method to be switched to. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the input method is unknown or filtered by the rules of [package visibility](../training/basics/intents/package-visibility.md). |

### switchToNextInputMethod

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun switchToNextInputMethod(onlyCurrentIme: Boolean): Boolean
```

Force switch to the next input method and subtype. If there is no IME enabled except current IME and subtype, do nothing.

| Parameters ||
|---|---|
| `onlyCurrentIme` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, the framework will find the next subtype which belongs to the current IME |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the current input method and subtype was successfully switched to the next input method and subtype. |

### switchToPreviousInputMethod

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun switchToPreviousInputMethod(): Boolean
```

Force switch to the last used input method and subtype. If the last input method didn't have any subtypes, the framework will simply switch to the last input method with no subtype specified.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the current input method and subtype was successfully switched to the last used input method and subtype. |

### updateFullscreenMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateFullscreenMode(): Unit
```

Re-evaluate whether the input method should be running in fullscreen mode, and update its UI if this has changed since the last time it was evaluated. This will call `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onEvaluateFullscreenMode()` to determine whether it should currently run in fullscreen mode. You can use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#isFullscreenMode()` to determine if the input method is currently running in fullscreen mode.

### updateInputViewShown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateInputViewShown(): Unit
```

Re-evaluate whether the soft input area should currently be shown, and update its UI if this has changed since the last time it was evaluated. This will call `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService#onEvaluateInputViewShown()` to determine whether the input view should currently be shown.

## Protected methods

### dump

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dump(
    fd: FileDescriptor!, 
    fout: PrintWriter!, 
    args: Array<String!>!
): Unit
```

Performs a dump of the InputMethodService's internal state. Override to add your own information to the dump.

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md)!: The raw file descriptor that the dump is being sent to. |
| `writer` | The PrintWriter to which you should dump your state. This will be closed for you after you return. |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: additional arguments to the dump request. |
| --- | --- |

### onCurrentInputMethodSubtypeChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onCurrentInputMethodSubtypeChanged(newSubtype: InputMethodSubtype!): Unit
```

Called when the subtype was changed.

| Parameters ||
|---|---|
| `newSubtype` | [InputMethodSubtype](../android.view.inputmethod/InputMethodSubtype.md)!: the subtype which is being changed to. |
