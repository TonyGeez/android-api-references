Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputMethodManager

```
class InputMethodManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.InputMethodManager](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#) |

Central system API to the overall input method framework (IMF) architecture, which arbitrates interaction between applications and the current input method.

Topics covered here:

1. [Architecture Overview](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#ArchitectureOverview)
2. [Applications](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#Applications)
3. [Input Methods](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#InputMethods)
4. [Security](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#Security)

### Architecture Overview

There are three primary parties involved in the input method framework (IMF) architecture:

- The **input method manager** as expressed by this class is the central point of the system that manages interaction between all other parts. It is expressed as the client-side API here which exists in each application context and communicates with a global system service that manages the interaction across all processes.
- An **input method (IME)** implements a particular interaction model allowing the user to generate text. The system binds to the current input method that is in use, causing it to be created and run, and tells it when to hide and show its UI. Only one IME is running at a time.
- Multiple **client applications** arbitrate with the input method manager for input focus and control over the state of the IME. Only one such client is ever active (working with the IME) at a time.

### Applications

In most cases, applications that are using the standard `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` or its subclasses will have little they need to do to work well with soft input methods. The main things you need to be aware of are:

- Properly set the `https://developer.android.com/reference/kotlin/android/R.attr.html#inputType:kotlin.Int` in your editable text views, so that the input method will have enough context to help the user in entering text into them.
- Deal well with losing screen space when the input method is displayed. Ideally an application should handle its window being resized smaller, but it can rely on the system performing panning of the window if needed. You should set the `https://developer.android.com/reference/kotlin/android/R.attr.html#windowSoftInputMode:kotlin.Int` attribute on your activity or the corresponding values on windows you create to help the system determine whether to pan or resize (it will try to determine this automatically but may get it wrong).
- You can also control the preferred soft input state (open, closed, etc) for your window using the same `https://developer.android.com/reference/kotlin/android/R.attr.html#windowSoftInputMode:kotlin.Int` attribute.

More finer-grained control is available through the APIs here to directly interact with the IMF and its IME -- either showing or hiding the input area, letting the user pick an input method, etc.

For the rare people amongst us writing their own text editors, you will need to implement `https://developer.android.com/reference/kotlin/android/view/View.html#onCreateInputConnection(android.view.inputmethod.EditorInfo)` to return a new instance of your own `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` interface allowing the IME to interact with your editor.

### Input Methods

An input method (IME) is implemented as a `https://developer.android.com/reference/kotlin/android/app/Service.html#`, typically deriving from `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#`. It must provide the core `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod` interface, though this is normally handled by `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#` and implementors will only need to deal with the higher-level API there.
See the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#` class for more information on implementing IMEs.

### Security

There are a lot of security issues associated with input methods, since they essentially have freedom to completely drive the UI and monitor everything the user enters. The Android input method framework also allows arbitrary third party IMEs, so care must be taken to restrict their selection and interactions.

Here are some key points about the security architecture behind the IMF:

- Only the system is allowed to directly access an IME's `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod` interface, via the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BIND_INPUT_METHOD:kotlin.String` permission. This is enforced in the system by not binding to an input method service that does not require this permission, so the system can guarantee no other untrusted clients are accessing the current input method outside of its control.

- There may be many client processes of the IMF, but only one may be active at a time. The inactive clients can not interact with key parts of the IMF through the mechanisms described below.

- Clients of an input method are only given access to its `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession` interface. One instance of this interface is created for each client, and only calls from the session associated with the active client will be processed by the current IME. This is enforced by `https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService.html#` for normal IMEs, but must be explicitly handled by an IME that is customizing the raw `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession` implementation.

- Only the active client's `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` will accept operations. The IMF tells each client process whether it is active, and the framework enforces that in inactive processes calls on to the current InputConnection will be ignored. This ensures that the current IME can only deliver events and text edits to the UI that the user sees as being in focus.

- An IME can never interact with an `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` while the screen is off. This is enforced by making all clients inactive while the screen is off, and prevents bad IMEs from driving the UI when the user can not be aware of its behavior.

- A client application can ask that the system let the user pick a new IME, but can not programmatically switch to one itself. This avoids malicious applications from switching the user to their own IME, which remains running when the user navigates away to another application. An IME, on the other hand, *is* allowed to programmatically switch the system to another IME, since it already has full control of user input.

- The user must explicitly enable a new IME in settings before they can switch to it, to confirm with the system that they know about it and want to make it available for use.

If your app targets Android 11 (API level 30) or higher, the methods in this class each return a filtered result by the rules of [package visibility](https://developer.android.com/reference/kotlin/training/basics/intents/package-visibility), except for the currently connected IME. Apps having a query for the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#SERVICE_INTERFACE:kotlin.String` see all IMEs.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_INPUT_METHODS:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HANDWRITING_DELEGATE_FLAG_HOME_DELEGATOR_ALLOWED:kotlin.Int` Flag indicating that views from the default home screen (`https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HOME:kotlin.String`) may act as a handwriting delegator for the delegate editor view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_IMPLICIT_ONLY:kotlin.Int` Flag for #hideSoftInputFromWindow and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#requestHideSelf(kotlin.Int)` to indicate that the soft input window should only be hidden if it was not explicitly shown by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_NOT_ALWAYS:kotlin.Int` Flag for #hideSoftInputFromWindow and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#requestShowSelf(kotlin.Int)` to indicate that the soft input window should normally be hidden, unless it was originally shown with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_FORCED:kotlin.Int`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_HIDDEN:kotlin.Int` Flag for the `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` result code from `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int,%20android.os.ResultReceiver)` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int,%20android.os.ResultReceiver)`: the state of the soft input window changed from shown to hidden. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_SHOWN:kotlin.Int` Flag for the `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` result code from `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int,%20android.os.ResultReceiver)` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int,%20android.os.ResultReceiver)`: the state of the soft input window changed from hidden to shown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_UNCHANGED_HIDDEN:kotlin.Int` Flag for the `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` result code from `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int,%20android.os.ResultReceiver)` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int,%20android.os.ResultReceiver)`: the state of the soft input window was unchanged and remains hidden. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_UNCHANGED_SHOWN:kotlin.Int` Flag for the `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` result code from `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int,%20android.os.ResultReceiver)` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int,%20android.os.ResultReceiver)`: the state of the soft input window was unchanged and remains shown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_FORCED:kotlin.Int` Flag for #showSoftInput to indicate that the user has forced the input method open (such as by long-pressing menu) so it should not be closed until they explicitly do so. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_IMPLICIT:kotlin.Int` Flag for #showSoftInput to indicate that this is an implicit request to show the input window, not as the result of a direct request by the user. |
| --- | --- |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View)(delegateView: https://developer.android.com/reference/kotlin/android/view/View.html#)` Accepts and starts a stylus handwriting session on the delegate view, if handwriting initiation delegation was previously requested using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View)` from the delegator. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View,%20kotlin.String)(delegateView: https://developer.android.com/reference/kotlin/android/view/View.html#, delegatorPackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Accepts and starts a stylus handwriting session on the delegate view, if handwriting initiation delegation was previously requested using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)` from the delegator and the view belongs to a specified delegate package. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View,%20kotlin.String,%20kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(delegateView: https://developer.android.com/reference/kotlin/android/view/View.html#, delegatorPackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>)` Accepts and starts a stylus handwriting session on the delegate view, if handwriting initiation delegation was previously requested using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)` from the delegator and the view belongs to a specified delegate package. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View,%20kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(delegateView: https://developer.android.com/reference/kotlin/android/view/View.html#, delegatorPackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>)` Accepts and starts a stylus handwriting session on the delegate view, if handwriting initiation delegation was previously requested using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)` from the delegator and the view belongs to a specified delegate package. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#dispatchKeyEventFromInputMethod(android.view.View,%20android.view.KeyEvent)(targetView: https://developer.android.com/reference/kotlin/android/view/View.html#?, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)` Provides the default implementation of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#sendKeyEvent(android.view.KeyEvent)`, which is expected to dispatch an keyboard event sent from the IME to an appropriate event target depending on the given `https://developer.android.com/reference/kotlin/android/view/View.html#` and the current focus state. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#displayCompletions(android.view.View,%20kotlin.Array)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, completions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/view/inputmethod/CompletionInfo!>!)` <br /> |
| --- | --- |
| [InputMethodInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#getCurrentInputMethodInfo()()` Returns the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo` of the currently selected input method (for the process's user). |
| [InputMethodSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#getCurrentInputMethodSubtype()()` Returns the current input method subtype. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InputMethodInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo)!\> | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#getEnabledInputMethodList()()` Returns the list of enabled input methods. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InputMethodSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype)!\> | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#getEnabledInputMethodSubtypeList(android.view.inputmethod.InputMethodInfo,%20kotlin.Boolean)(imi: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo?, allowsImplicitlyEnabledSubtypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns a list of enabled input method subtypes for the specified input method info. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#getImeHideAnimationDurationOverrideMillis(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#)` Returns the IME hide animation duration override for a given view tree in milliseconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#getImeShowAnimationDurationOverrideMillis(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#)` Returns the IME show animation duration override for a given view tree in milliseconds. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InputMethodInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo)!\> | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#getInputMethodList()()` Returns the list of installed input methods. |
| [InputMethodSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#getLastInputMethodSubtype()()` Returns the last used `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype` in system history. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [InputMethodInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InputMethodSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype)!\>!\>! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#getShortcutInputMethodsAndSubtypes()()` Returns a map of all shortcut input method info and their subtypes. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromInputMethod(android.os.IBinder,%20kotlin.Int)(token: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Close/hide the input method's soft input area, so the user no longer sees it or can interact with it. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int)(windowToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Request to hide the soft input window from the context of the window that is currently accepting input. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int,%20android.os.ResultReceiver)(windowToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, resultReceiver: https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#!)` Request to hide the soft input window from the context of the window that is currently accepting input. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideStatusIcon(android.os.IBinder)(imeToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#invalidateInput(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#)` Gives a hint to the system that the text associated with `view` is updated by something that is not an input method editor (IME), so that the system can cancel any pending text editing requests from the IME until it receives the new editing context such as surrounding text provided by `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#takeSnapshot()`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#isAcceptingText()()` Return `true` if the currently served view is accepting full text edits. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#isActive()()` Return `true` if any view is currently active for the input method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#isActive(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Return `true` if the given view is the currently active view for the input method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#isConnectionlessStylusHandwritingAvailable()()` Returns `true` if the currently selected IME supports connectionless stylus handwriting sessions and is enabled. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#isFullscreenMode()()` Allows you to discover whether the attached input method is running in fullscreen mode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#isInputMethodSuppressingSpellChecker()()` Return `true` if the input method is suppressing system spell checker. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#isStylusHandwritingAvailable()()` Returns `true` if currently selected IME supports Stylus handwriting \& is enabled. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#isWatchingCursor(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Return true if the current input method wants to watch the location of the input editor's cursor in its window. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View)(delegatorView: https://developer.android.com/reference/kotlin/android/view/View.html#)` Prepares delegation of starting stylus handwriting session to a different editor in same or different window than the view on which initial handwriting stroke was detected. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)(delegatorView: https://developer.android.com/reference/kotlin/android/view/View.html#, delegatePackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Prepares delegation of starting stylus handwriting session to a different editor in same or a different window in a different package than the view on which initial handwriting stroke was detected. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#restartInput(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)` If the input method is currently connected to the given view, restart it with its new contents. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#sendAppPrivateCommand(android.view.View,%20kotlin.String,%20android.os.Bundle)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, data: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#appPrivateCommand(kotlin.String,%20android.os.Bundle)` on the current Input Method. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#setAdditionalInputMethodSubtypes(kotlin.String,%20kotlin.Array)(imiId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, subtypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype!>)` Set additional input method subtypes. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#setCurrentInputMethodSubtype(android.view.inputmethod.InputMethodSubtype)(subtype: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype!)` Switch to a new input method subtype of the current input method. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#setExplicitlyEnabledInputMethodSubtypes(kotlin.String,%20kotlin.IntArray)(imiId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, subtypeHashCodes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Updates the list of explicitly enabled `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype` for a given IME owned by the calling process. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#setImeHideAnimationDurationOverrideMillis(android.view.View,%20kotlin.Long)(view: https://developer.android.com/reference/kotlin/android/view/View.html#, durationMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets or clears the IME hide animation duration override. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#setImeShowAnimationDurationOverrideMillis(android.view.View,%20kotlin.Long)(view: https://developer.android.com/reference/kotlin/android/view/View.html#, durationMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets or clears the IME show animation duration override. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#setInputMethod(android.os.IBinder,%20kotlin.String)(token: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!, id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Force switch to a new input method component. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#setInputMethodAndSubtype(android.os.IBinder,%20kotlin.String,%20android.view.inputmethod.InputMethodSubtype)(token: https://developer.android.com/reference/kotlin/android/os/IBinder.html#, id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, subtype: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype!)` Force switch to a new input method and subtype. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#shouldOfferSwitchingToNextInputMethod(android.os.IBinder)(imeToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!)` Returns true if the current IME needs to offer the users ways to switch to a next input method (e.g. a globe key.). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showInputMethodAndSubtypeEnabler(kotlin.String)(imiId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Show the settings for enabling subtypes of the specified input method. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showInputMethodPicker()()` Show IME picker popup window. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Explicitly request that the current input method's soft input area be shown to the user, if needed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int,%20android.os.ResultReceiver)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, resultReceiver: https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#!)` Explicitly request that the current input method's soft input area be shown to the user, if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInputFromInputMethod(android.os.IBinder,%20kotlin.Int)(token: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Show the input method's soft input area, so the user sees the input method window and can interact with it. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showStatusIcon(android.os.IBinder,%20kotlin.String,%20kotlin.Int)(imeToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!, packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, iconId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwriting(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)(view: https://developer.android.com/reference/kotlin/android/view/View.html#, cursorAnchorInfo: https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo?, callbackExecutor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback)` Starts a connectionless stylus handwriting session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20kotlin.String,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)(delegatorView: https://developer.android.com/reference/kotlin/android/view/View.html#, cursorAnchorInfo: https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo?, delegatePackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, callbackExecutor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback)` Starts a connectionless stylus handwriting session (see `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwriting(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`) and additionally enables the recognised handwritten text to be later committed to a text editor using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View,%20kotlin.String)`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)(delegatorView: https://developer.android.com/reference/kotlin/android/view/View.html#, cursorAnchorInfo: https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo?, callbackExecutor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback)` Starts a connectionless stylus handwriting session (see `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwriting(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`) and additionally enables the recognised handwritten text to be later committed to a text editor using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View)`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#)` Start stylus handwriting session. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#switchToLastInputMethod(android.os.IBinder)(imeToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!)` Force switch to the last used input method and subtype. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#switchToNextInputMethod(android.os.IBinder,%20kotlin.Boolean)(imeToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!, onlyCurrentIme: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Force switch to the next input method and subtype. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#toggleSoftInput(kotlin.Int,%20kotlin.Int)(showFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hideFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This method toggles the input method window display. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#toggleSoftInputFromWindow(android.os.IBinder,%20kotlin.Int,%20kotlin.Int)(windowToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!, showFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hideFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This method toggles the input method window display. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateCursor(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Report the current cursor location in its window. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateCursorAnchorInfo(android.view.View,%20android.view.inputmethod.CursorAnchorInfo)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, cursorAnchorInfo: https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo!)` Report positional change of the text insertion point and/or characters in the composition string. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateExtractedText(android.view.View,%20kotlin.Int,%20android.view.inputmethod.ExtractedText)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, token: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, text: https://developer.android.com/reference/kotlin/android/view/inputmethod/ExtractedText!)` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateSelection(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, selStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, selEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, candidatesStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, candidatesEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Report the current selection range. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#viewClicked(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Notify the event when the user tapped or clicked the text view. |

## Constants

### HANDWRITING_DELEGATE_FLAG_HOME_DELEGATOR_ALLOWED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HANDWRITING_DELEGATE_FLAG_HOME_DELEGATOR_ALLOWED: Int
```

Flag indicating that views from the default home screen (`https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HOME:kotlin.String`) may act as a handwriting delegator for the delegate editor view. If set, views from the home screen package will be trusted for handwriting delegation, in addition to views in the `delegatorPackageName` passed to `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View,%20kotlin.String,%20kotlin.Int,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` .

 Value: 1

### HIDE_IMPLICIT_ONLY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HIDE_IMPLICIT_ONLY: Int
```

**Deprecated:** *Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, this flag has no effect anymore.*

Flag for #hideSoftInputFromWindow and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#requestHideSelf(kotlin.Int)` to indicate that the soft input window should only be hidden if it was not explicitly shown by the user.

 Value: 1

### HIDE_NOT_ALWAYS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HIDE_NOT_ALWAYS: Int
```

**Deprecated:** *Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, this flag has no effect anymore.*

Flag for #hideSoftInputFromWindow and `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#requestShowSelf(kotlin.Int)` to indicate that the soft input window should normally be hidden, unless it was originally shown with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_FORCED:kotlin.Int`.

 Value: 2

### RESULT_HIDDEN

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_HIDDEN: Int
```

Flag for the `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` result code from `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int,%20android.os.ResultReceiver)` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int,%20android.os.ResultReceiver)`: the state of the soft input window changed from shown to hidden.

 Value: 3

### RESULT_SHOWN

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_SHOWN: Int
```

Flag for the `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` result code from `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int,%20android.os.ResultReceiver)` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int,%20android.os.ResultReceiver)`: the state of the soft input window changed from hidden to shown.

 Value: 2

### RESULT_UNCHANGED_HIDDEN

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_UNCHANGED_HIDDEN: Int
```

Flag for the `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` result code from `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int,%20android.os.ResultReceiver)` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int,%20android.os.ResultReceiver)`: the state of the soft input window was unchanged and remains hidden.

 Value: 1

### RESULT_UNCHANGED_SHOWN

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_UNCHANGED_SHOWN: Int
```

Flag for the `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` result code from `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int,%20android.os.ResultReceiver)` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int,%20android.os.ResultReceiver)`: the state of the soft input window was unchanged and remains shown.

 Value: 0

### SHOW_FORCED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHOW_FORCED: Int
```

**Deprecated:** *Use #showSoftInput without this flag instead. Using this flag can lead to the soft input remaining visible even when the calling application is closed. The use of this flag can make the soft input remain visible globally. Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, this flag only has an effect while the caller is currently focused. Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, this flag has no effect anymore.*

Flag for #showSoftInput to indicate that the user has forced the input method open (such as by long-pressing menu) so it should not be closed until they explicitly do so.

 Value: 2

### SHOW_IMPLICIT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHOW_IMPLICIT: Int
```

**Deprecated:** *Use #showSoftInput without this flag instead. Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, this flag has no effect anymore.*

Flag for #showSoftInput to indicate that this is an implicit request to show the input window, not as the result of a direct request by the user. The window may not be shown in this case.

 Value: 1

## Public methods

### acceptStylusHandwritingDelegation

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun acceptStylusHandwritingDelegation(delegateView: View): Boolean
```

Accepts and starts a stylus handwriting session on the delegate view, if handwriting initiation delegation was previously requested using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View)` from the delegator.

Otherwise, if the delegator view previously started delegation using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`, requests the IME to commit the recognised handwritten text from the connectionless session to the delegate view.

Note: If delegator and delegate are in different application packages, use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View,%20kotlin.String)` instead.

| Parameters ||
|---|---|
| `delegateView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): delegate view capable of receiving input via `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if view belongs to same application package as used in `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View)` and delegation is accepted |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`

### acceptStylusHandwritingDelegation

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun acceptStylusHandwritingDelegation(
    delegateView: View, 
    delegatorPackageName: String
): Boolean
```

Accepts and starts a stylus handwriting session on the delegate view, if handwriting initiation delegation was previously requested using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)` from the delegator and the view belongs to a specified delegate package.

Otherwise, if the delegator view previously started delegation using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20kotlin.String,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`, requests the IME to commit the recognised handwritten text from the connectionless session to the delegate view.

Note: If delegator and delegate are in the same application package, use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View)` instead.

| Parameters ||
|---|---|
| `delegateView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): delegate view capable of receiving input via `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` This value cannot be `null`. |
| `delegatorPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): package name of the delegator that handled initial stylus stroke. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if view belongs to allowed delegate package declared in `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)` and delegation is accepted |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20kotlin.String,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`

### acceptStylusHandwritingDelegation

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun acceptStylusHandwritingDelegation(
    delegateView: View, 
    delegatorPackageName: String, 
    flags: Int, 
    executor: Executor, 
    callback: Consumer<Boolean!>
): Unit
```

Accepts and starts a stylus handwriting session on the delegate view, if handwriting initiation delegation was previously requested using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)` from the delegator and the view belongs to a specified delegate package.

Otherwise, if the delegator view previously started delegation using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20kotlin.String,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`, requests the IME to commit the recognised handwritten text from the connectionless session to the delegate view.

Note: If delegator and delegate are in the same application package, use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View)` instead.

| Parameters ||
|---|---|
| `delegateView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): delegate view capable of receiving input via `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` This value cannot be `null`. |
| `delegatorPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): package name of the delegator that handled initial stylus stroke. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HANDWRITING_DELEGATE_FLAG_HOME_DELEGATOR_ALLOWED:kotlin.Int` or `0` Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HANDWRITING_DELEGATE_FLAG_HOME_DELEGATOR_ALLOWED:kotlin.Int` |
| --- | --- |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor to run the callback on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>: `true` would be received if delegation was accepted. The caller should hold a reference to the callback. The framework only holds a weak reference. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20kotlin.String,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`

### acceptStylusHandwritingDelegation

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun acceptStylusHandwritingDelegation(
    delegateView: View, 
    delegatorPackageName: String, 
    executor: Executor, 
    callback: Consumer<Boolean!>
): Unit
```

Accepts and starts a stylus handwriting session on the delegate view, if handwriting initiation delegation was previously requested using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)` from the delegator and the view belongs to a specified delegate package.

Otherwise, if the delegator view previously started delegation using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20kotlin.String,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`, requests the IME to commit the recognised handwritten text from the connectionless session to the delegate view.

| Parameters ||
|---|---|
| `delegateView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): delegate view capable of receiving input via `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` on which `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)` will be called. This value cannot be `null`. |
| `delegatorPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): package name of the delegator that handled initial stylus stroke. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor to run the callback on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>: Consumer callback that provides `true` if view belongs to allowed delegate package declared in `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)` and handwriting session can start. Note: The caller should hold a reference to the callback. The framework only holds a weak reference. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20kotlin.String,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`

### dispatchKeyEventFromInputMethod

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dispatchKeyEventFromInputMethod(
    targetView: View?, 
    event: KeyEvent
): Unit
```

Provides the default implementation of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#sendKeyEvent(android.view.KeyEvent)`, which is expected to dispatch an keyboard event sent from the IME to an appropriate event target depending on the given `https://developer.android.com/reference/kotlin/android/view/View.html#` and the current focus state.

CAUTION: This method is provided only for the situation where `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#sendKeyEvent(android.view.KeyEvent)` needs to be implemented without relying on `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection`. Do not use this API for anything else.

| Parameters ||
|---|---|
| `targetView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)?: the default target view. If `null` is specified, then this method tries to find a good event target based on the current focus state. |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#): the key event to be dispatched. This value cannot be `null`. |

### displayCompletions

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun displayCompletions(
    view: View!, 
    completions: Array<CompletionInfo!>!
): Unit
```

### getCurrentInputMethodInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCurrentInputMethodInfo(): InputMethodInfo?
```

Returns the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo` of the currently selected input method (for the process's user).

On multi user environment, this API returns a result for the calling process user.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo?` | This value may be `null`. |

### getCurrentInputMethodSubtype

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCurrentInputMethodSubtype(): InputMethodSubtype?
```

Returns the current input method subtype. This subtype is one of the subtypes in the current input method. This method returns null when the current input method doesn't have any input method subtype.

### getEnabledInputMethodList

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEnabledInputMethodList(): MutableList<InputMethodInfo!>
```

Returns the list of enabled input methods.

On multi user environment, this API returns a result for the calling process user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo!>` | `https://developer.android.com/reference/kotlin/java/util/List.html#` of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo`. This value cannot be `null`. |

### getEnabledInputMethodSubtypeList

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEnabledInputMethodSubtypeList(
    imi: InputMethodInfo?, 
    allowsImplicitlyEnabledSubtypes: Boolean
): MutableList<InputMethodSubtype!>
```

Returns a list of enabled input method subtypes for the specified input method info.

On multi user environment, this API returns a result for the calling process user.

| Parameters ||
|---|---|
| `imi` | [InputMethodInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo)?: The `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo` whose subtypes list will be returned. If `null`, returns enabled subtypes for the currently selected `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo`. |
| `allowsImplicitlyEnabledSubtypes` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): A boolean flag to allow to return the implicitly enabled subtypes. If an input method info doesn't have enabled subtypes, the framework will implicitly enable subtypes according to the current system language. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype!>` | This value cannot be `null`. |

### getImeHideAnimationDurationOverrideMillis

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getImeHideAnimationDurationOverrideMillis(view: View): Long
```

Returns the IME hide animation duration override for a given view tree in milliseconds.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): the view to query the view tree of. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the duration override in milliseconds, or `-1` if no override is set or if the view has no associated `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.html#` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#setImeHideAnimationDurationOverrideMillis(android.view.View,%20kotlin.Long)`

### getImeShowAnimationDurationOverrideMillis

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getImeShowAnimationDurationOverrideMillis(view: View): Long
```

Returns the IME show animation duration override for a given view tree in milliseconds.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): the view to query the view tree of. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the duration override in milliseconds, or `-1` if no override is set or if the view has no associated `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.html#` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#setImeShowAnimationDurationOverrideMillis(android.view.View,%20kotlin.Long)`

### getInputMethodList

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInputMethodList(): MutableList<InputMethodInfo!>
```

Returns the list of installed input methods.

On multi user environment, this API returns a result for the calling process user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo!>` | `https://developer.android.com/reference/kotlin/java/util/List.html#` of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo`. This value cannot be `null`. |

### getLastInputMethodSubtype

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLastInputMethodSubtype(): InputMethodSubtype?
```

Returns the last used `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype` in system history.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype?` | the last `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype`, `null` if last IME have no subtype. |

### getShortcutInputMethodsAndSubtypes

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getShortcutInputMethodsAndSubtypes(): MutableMap<InputMethodInfo!, MutableList<InputMethodSubtype!>!>!
```

Returns a map of all shortcut input method info and their subtypes.

### hideSoftInputFromInputMethod

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hideSoftInputFromInputMethod(
    token: IBinder!, 
    flags: Int
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#requestHideSelf(kotlin.Int)` instead. This method was intended for IME developers who should be accessing APIs through the service. APIs in this class are intended for app developers interacting with the IME.*

Close/hide the input method's soft input area, so the user no longer sees it or can interact with it. This can only be called from the currently active input method, as validated by the given token.

| Parameters ||
|---|---|
| `token` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!: Supplies the identifying token given to an input method when it was started, which allows it to perform this operation on itself. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_IMPLICIT_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_NOT_ALWAYS:kotlin.Int` |

### hideSoftInputFromWindow

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hideSoftInputFromWindow(
    windowToken: IBinder!, 
    flags: Int
): Boolean
```

Request to hide the soft input window from the context of the window that is currently accepting input. This should be called as a result of the user doing some actually than fairly explicitly requests to have the input window hidden.

| Parameters ||
|---|---|
| `windowToken` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!: The token of the window that is making the request, as returned by `https://developer.android.com/reference/kotlin/android/view/View.html#getWindowToken()`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_IMPLICIT_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_NOT_ALWAYS:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | For apps targeting Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, onwards, it will always return `true`. To see when the IME is hidden, use `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener.html#` and verify the provided `https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#` for the visibility of IME. For apps targeting releases before Android Baklava: returns `true` if a request was sent to system_server, `false` otherwise. Note: This does not return the result of that request (i.e. whether the IME was actually hidden). If result is needed, use `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.html#hide(kotlin.Int)` instead and set a `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener.html#` and verify the provided `https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#` for the visibility of IME. |

### hideSoftInputFromWindow

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hideSoftInputFromWindow(
    windowToken: IBinder!, 
    flags: Int, 
    resultReceiver: ResultReceiver!
): Boolean
```

**Deprecated:** *The `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` is not a reliable way of determining whether the Input Method is actually shown or hidden. If result is needed, use `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.html#hide(kotlin.Int)` instead and set a `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener.html#` and verify the provided `https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#` for the visibility of IME. If result is not needed, use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int)` instead.*

Request to hide the soft input window from the context of the window that is currently accepting input. This should be called as a result of the user doing some actually than fairly explicitly requests to have the input window hidden.

**Caveat:** `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` instance passed to this method can be a long-lived object, because it may not be garbage-collected until all the corresponding `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` objects transferred to different processes get garbage-collected. Follow the general patterns to avoid memory leaks in Android. Consider to use `https://developer.android.com/reference/kotlin/java/lang/ref/WeakReference.html#` so that application logic objects such as `https://developer.android.com/reference/kotlin/android/app/Activity.html#` and `https://developer.android.com/reference/kotlin/android/content/Context.html#` can be garbage collected regardless of the lifetime of `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#`.

| Parameters ||
|---|---|
| `windowToken` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!: The token of the window that is making the request, as returned by `https://developer.android.com/reference/kotlin/android/view/View.html#getWindowToken()`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_IMPLICIT_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_NOT_ALWAYS:kotlin.Int` |
| `resultReceiver` | [ResultReceiver](https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#)!: If non-null, this will be called by the IME when it has processed your request to tell you what it has done. The result code you receive may be either `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_UNCHANGED_SHOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_UNCHANGED_HIDDEN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_SHOWN:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_HIDDEN:kotlin.Int`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if a request was sent to system_server, `false` otherwise. Note: This does not return the result of that request (i.e. whether the IME was actually hidden). For result use `resultReceiver` instead. |

### hideStatusIcon

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hideStatusIcon(imeToken: IBinder!): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#hideStatusIcon()` instead. This method was intended for IME developers who should be accessing APIs through the service. APIs in this class are intended for app developers interacting with the IME.*

### invalidateInput

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun invalidateInput(view: View): Unit
```

Gives a hint to the system that the text associated with `view` is updated by something that is not an input method editor (IME), so that the system can cancel any pending text editing requests from the IME until it receives the new editing context such as surrounding text provided by `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#takeSnapshot()`.

When `view` does not support `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#takeSnapshot()` protocol, calling this method may trigger `https://developer.android.com/reference/kotlin/android/view/View.html#onCreateInputConnection(android.view.inputmethod.EditorInfo)`.

Unlike `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#restartInput(android.view.View)`, this API does not immediately interact with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection`. Instead, the application may later receive `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#takeSnapshot()` as needed so that the system can capture new editing context for the IME. For instance, successive invocations of this API can be coerced into a single (or zero) callback of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#takeSnapshot()`.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): The view whose text has changed. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#restartInput(android.view.View)`

### isAcceptingText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAcceptingText(): Boolean
```

Return `true` if the currently served view is accepting full text edits. If `false`, it has no input connection, so it can only handle raw key events.

### isActive

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isActive(): Boolean
```

Return `true` if any view is currently active for the input method.

### isActive

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isActive(view: View!): Boolean
```

Return `true` if the given view is the currently active view for the input method.

### isConnectionlessStylusHandwritingAvailable

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isConnectionlessStylusHandwritingAvailable(): Boolean
```

Returns `true` if the currently selected IME supports connectionless stylus handwriting sessions and is enabled.

### isFullscreenMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFullscreenMode(): Boolean
```

Allows you to discover whether the attached input method is running in fullscreen mode. Return true if it is fullscreen, entirely covering your UI, else returns false.

### isInputMethodSuppressingSpellChecker

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isInputMethodSuppressingSpellChecker(): Boolean
```

Return `true` if the input method is suppressing system spell checker.

### isStylusHandwritingAvailable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isStylusHandwritingAvailable(): Boolean
```

Returns `true` if currently selected IME supports Stylus handwriting \& is enabled. If the method returns `false`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)` shouldn't be called and Stylus touch should continue as normal touch input.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)`

### isWatchingCursor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isWatchingCursor(view: View!): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestCursorUpdates(kotlin.Int)` instead.*

Return true if the current input method wants to watch the location of the input editor's cursor in its window.

### prepareStylusHandwritingDelegation

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun prepareStylusHandwritingDelegation(delegatorView: View): Unit
```

Prepares delegation of starting stylus handwriting session to a different editor in same or different window than the view on which initial handwriting stroke was detected. Delegation can be used to start stylus handwriting session before the `Editor` view or its `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` is started. Calling this method starts buffering of stylus motion events until `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View)` is called, at which point the handwriting session can be started and the buffered stylus motion events will be delivered to the IME. e.g. Delegation can be used when initial handwriting stroke is on a pseudo `Editor` like widget (with no `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection`) but actual `Editor` is on a different window.

Note: If an actual `Editor` capable of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` is being scribbled upon using stylus, use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)` instead.

| Parameters ||
|---|---|
| `delegatorView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): the view that receives initial stylus stroke and delegates it to the actual editor. Its window must `https://developer.android.com/reference/kotlin/android/view/View.html#hasWindowFocus()`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)`

### prepareStylusHandwritingDelegation

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun prepareStylusHandwritingDelegation(
    delegatorView: View, 
    delegatePackageName: String
): Unit
```

Prepares delegation of starting stylus handwriting session to a different editor in same or a different window in a different package than the view on which initial handwriting stroke was detected. Delegation can be used to start stylus handwriting session before the `Editor` view or its `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` is started. Calling this method starts buffering of stylus motion events until `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View,%20kotlin.String)` is called, at which point the handwriting session can be started and the buffered stylus motion events will be delivered to the IME. e.g. Delegation can be used when initial handwriting stroke is on a pseudo `Editor` like widget (with no `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection`) but actual `Editor` is on a different window in the given package.

Note: If delegator and delegate are in same package use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View)` instead.

| Parameters ||
|---|---|
| `delegatorView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): the view that receives initial stylus stroke and delegates it to the actual editor. Its window must `https://developer.android.com/reference/kotlin/android/view/View.html#hasWindowFocus()`. This value cannot be `null`. |
| `delegatePackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): package name that contains actual `Editor` which should start stylus handwriting session by calling #acceptStylusHandwritingDelegation. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#prepareStylusHandwritingDelegation(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View,%20kotlin.String)`

### restartInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun restartInput(view: View!): Unit
```

If the input method is currently connected to the given view, restart it with its new contents. You should call this when the text within your view changes outside of the normal input method or key input flow, such as when an application calls TextView.setText().

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The view whose text has changed. |

### sendAppPrivateCommand

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendAppPrivateCommand(
    view: View!, 
    action: String!, 
    data: Bundle!
): Unit
```

Call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#appPrivateCommand(kotlin.String,%20android.os.Bundle)` on the current Input Method.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: Optional View that is sending the command, or null if you want to send the command regardless of the view that is attached to the input method. |
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of the command to be performed. This *must* be a scoped name, i.e. prefixed with a package name you own, so that different developers will not create conflicting commands. |
| `data` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Any data to include with the command. |
| --- | --- |

### setAdditionalInputMethodSubtypes

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAdditionalInputMethodSubtypes(
    imiId: String, 
    subtypes: Array<InputMethodSubtype!>
): Unit
```

**Deprecated:** *For IMEs that have already implemented features like customizable/downloadable keyboard layouts/languages, please start migration to other approaches. One idea would be exposing only one unified `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype` then implement IME's own language switching mechanism within that unified subtype. The support of "Additional Subtype" may be completely dropped in a future version of Android.*

Set additional input method subtypes. Only a process which shares the same uid with the IME can add additional input method subtypes to the IME. Please note that a subtype's status is stored in the system. For example, enabled subtypes are remembered by the framework even after they are removed by using this method. If you re-add the same subtypes again, they will just get enabled. If you want to avoid such conflicts, for instance, you may want to create a "different" new subtype even with the same locale and mode, by changing its extra value. The different subtype won't get affected by the stored past status. (You may want to take a look at `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#hashCode()` to refer to the current implementation.)

NOTE: If the same subtype exists in both the manifest XML file and additional subtypes specified by `subtypes`, those multiple instances are automatically merged into one instance.

CAVEAT: In API Level 23 and prior, the system may do nothing if an empty `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype` is specified in `subtypes`, which prevents you from removing the last one entry of additional subtypes. If your IME statically defines one or more subtypes in the manifest XML file, you may be able to work around this limitation by specifying one of those statically defined subtypes in `subtypes`.

| Parameters ||
|---|---|
| `imiId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Id of InputMethodInfo which additional input method subtypes will be added to. If the imiId is `null`, system would do nothing for this operation. |
| `subtypes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [InputMethodSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype)!\>: subtypes will be added as additional subtypes of the current input method. If the subtypes is `null`, system would do nothing for this operation. |

### setCurrentInputMethodSubtype

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCurrentInputMethodSubtype(subtype: InputMethodSubtype!): Boolean
```

**Deprecated:** *If the calling process is an IME, use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#switchInputMethod(kotlin.String,%20android.view.inputmethod.InputMethodSubtype)`, which does not require any permission as long as the caller is the current IME. If the calling process is some privileged app that already has `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SECURE_SETTINGS:kotlin.String` permission, just directly update `https://developer.android.com/reference/kotlin/android/provider/Settings.Secure.html#SELECTED_INPUT_METHOD_SUBTYPE:kotlin.String`.*

Switch to a new input method subtype of the current input method. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SECURE_SETTINGS:kotlin.String`

| Parameters ||
|---|---|
| `subtype` | [InputMethodSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype)!: A new input method subtype to switch. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the current subtype was successfully switched. When the specified subtype is null, this method returns false. |

### setExplicitlyEnabledInputMethodSubtypes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setExplicitlyEnabledInputMethodSubtypes(
    imiId: String, 
    subtypeHashCodes: IntArray
): Unit
```

Updates the list of explicitly enabled `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype` for a given IME owned by the calling process.

By default each IME has no explicitly enabled `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype`. In this state the system will decide what `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype` should be enabled by using information available at runtime as per-user language settings. Users can, however, manually pick up one or more `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype` to be enabled on an Activity shown by `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showInputMethodAndSubtypeEnabler(kotlin.String)`. Such a manual change is stored in `https://developer.android.com/reference/kotlin/android/provider/Settings.Secure.html#ENABLED_INPUT_METHODS:kotlin.String` so that the change can persist across reboots. `https://developer.android.com/reference/kotlin/android/provider/Settings.Secure.html#ENABLED_INPUT_METHODS:kotlin.String` stores `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#hashCode()` as the identifier of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype` for historical reasons.

This API provides a safe and managed way for IME developers to modify what `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype` are referenced in `https://developer.android.com/reference/kotlin/android/provider/Settings.Secure.html#ENABLED_INPUT_METHODS:kotlin.String` for their own IME. One use case is when IME developers want to use their own Activity for users to pick up `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype`. Another use case is for IME developers to fix up any stale and/or invalid value stored in `https://developer.android.com/reference/kotlin/android/provider/Settings.Secure.html#ENABLED_INPUT_METHODS:kotlin.String` without bothering users. Passing an empty `subtypeHashCodes` is guaranteed to reset the state to default.

### To control the return value of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#hashCode()`

`https://developer.android.com/reference/kotlin/android/R.attr.html#subtypeId:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype.InputMethodSubtypeBuilder#setSubtypeId(kotlin.Int)` are available for IME developers to control the return value of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#hashCode()`. Beware that `-1` is not a valid value of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#hashCode()` for historical reasons.

### Note for Direct Boot support

While IME developers can call this API even before `https://developer.android.com/reference/kotlin/android/os/UserManager.html#isUserUnlocked()` becomes `true`, such a change is volatile thus remains effective only until `https://developer.android.com/reference/kotlin/android/os/UserManager.html#isUserUnlocked()` becomes `true` or the device is rebooted. To make the change persistent IME developers need to call this API again after receiving `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_USER_UNLOCKED:kotlin.String`.

| Parameters ||
|---|---|
| `imiId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): IME ID. The specified IME and the calling process need to belong to the same package. Otherwise `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. This value cannot be `null`. |
| `subtypeHashCodes` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): An arrays of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#hashCode()` to be explicitly enabled. Entries that are found in the specified IME will be silently ignored. Pass an empty array to reset the state to default. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `subtypeHashCodes` is `null`. |
| `java.lang.SecurityException` | if the specified IME and the calling process do not belong to the same package. |

### setImeHideAnimationDurationOverrideMillis

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setImeHideAnimationDurationOverrideMillis(
    view: View, 
    durationMillis: Long
): Unit
```

Sets or clears the IME hide animation duration override.

When set, this value is used as the requested duration for the animation of the IME hiding. This also includes animations during which where the IME is animated simultaneously with other insets. Note that there are factors which may cause the actual animation duration to differ from this requested value, including:

- The value getting clamped to a reasonable range by the system. Call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#getImeHideAnimationDurationOverrideMillis(android.view.View)` after calling this setter to obtain the value after it has been clamped.
- The current `https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.html#getDurationScale()`.
- Whether the relevant window is in multi-window mode, in which case the system directly controls IME animations, rather than the application.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): the view whose tree the duration override is to be applied to. This value cannot be `null`. |
| `durationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the non-negative duration override in milliseconds being set, or `-1` to clear the duration override. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the provided duration is negative and not `-1` |

### setImeShowAnimationDurationOverrideMillis

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setImeShowAnimationDurationOverrideMillis(
    view: View, 
    durationMillis: Long
): Unit
```

Sets or clears the IME show animation duration override.

When set, this value is used as the requested duration for the animation of the IME showing. This also includes animations during which the IME is animated simultaneously with other insets. Note that there are factors which may cause the actual animation duration to differ from this requested value, including:

- The value getting clamped to a reasonable range by the system. Call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#getImeShowAnimationDurationOverrideMillis(android.view.View)` after calling this setter to obtain the value after it has been clamped.
- The current `https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.html#getDurationScale()`.
- Whether the relevant window is in multi-window mode, in which case the system directly controls IME animations, rather than the application.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): the view whose tree the duration override is to be applied to. This value cannot be `null`. |
| `durationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the non-negative duration override in milliseconds being set, or `-1` to clear the duration override. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the provided duration is negative and not `-1` |

### setInputMethod

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setInputMethod(
    token: IBinder!, 
    id: String!
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#switchInputMethod(kotlin.String)` instead. This method was intended for IME developers who should be accessing APIs through the service. APIs in this class are intended for app developers interacting with the IME.*

Force switch to a new input method component. This can only be called from an application or a service which has a token of the currently active input method.

On Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later devices, the undocumented behavior that token can be `null` when the caller has `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SECURE_SETTINGS:kotlin.String` is deprecated. Instead, update `https://developer.android.com/reference/kotlin/android/provider/Settings.Secure.html#DEFAULT_INPUT_METHOD:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/Settings.Secure.html#SELECTED_INPUT_METHOD_SUBTYPE:kotlin.String` directly.

| Parameters ||
|---|---|
| `token` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!: Supplies the identifying token given to an input method when it was started, which allows it to perform this operation on itself. |
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The unique identifier for the new input method to be switched to. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the input method is unknown or filtered by the rules of [package visibility](https://developer.android.com/reference/kotlin/training/basics/intents/package-visibility). |

### setInputMethodAndSubtype

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setInputMethodAndSubtype(
    token: IBinder, 
    id: String!, 
    subtype: InputMethodSubtype!
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#switchInputMethod(kotlin.String,%20android.view.inputmethod.InputMethodSubtype)` instead. This method was intended for IME developers who should be accessing APIs through the service. APIs in this class are intended for app developers interacting with the IME.*

Force switch to a new input method and subtype. This can only be called from an application or a service which has a token of the currently active input method.

On Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later devices, `token` cannot be `null` even with `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SECURE_SETTINGS:kotlin.String`. Instead, update `https://developer.android.com/reference/kotlin/android/provider/Settings.Secure.html#DEFAULT_INPUT_METHOD:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/Settings.Secure.html#SELECTED_INPUT_METHOD_SUBTYPE:kotlin.String` directly.

| Parameters ||
|---|---|
| `token` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#): Supplies the identifying token given to an input method when it was started, which allows it to perform this operation on itself. This value cannot be `null`. |
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The unique identifier for the new input method to be switched to. |
| `subtype` | [InputMethodSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype)!: The new subtype of the new input method to be switched to. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the input method is unknown or filtered by the rules of [package visibility](https://developer.android.com/reference/kotlin/training/basics/intents/package-visibility). |

### shouldOfferSwitchingToNextInputMethod

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun shouldOfferSwitchingToNextInputMethod(imeToken: IBinder!): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#shouldOfferSwitchingToNextInputMethod()` instead. This method was intended for IME developers who should be accessing APIs through the service. APIs in this class are intended for app developers interacting with the IME.*

Returns true if the current IME needs to offer the users ways to switch to a next input method (e.g. a globe key.). When an IME sets supportsSwitchingToNextInputMethod and this method returns true, the IME has to offer ways to to invoke `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#switchToNextInputMethod(android.os.IBinder,%20kotlin.Boolean)` accordingly.

Note that the system determines the most appropriate next input method and subtype in order to provide the consistent user experience in switching between IMEs and subtypes.

| Parameters ||
|---|---|
| `imeToken` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!: Supplies the identifying token given to an input method when it was started, which allows it to perform this operation on itself. |

### showInputMethodAndSubtypeEnabler

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun showInputMethodAndSubtypeEnabler(imiId: String?): Unit
```

Show the settings for enabling subtypes of the specified input method.

| Parameters ||
|---|---|
| `imiId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: An input method, whose subtypes settings will be shown. If imiId is null, subtypes of all input methods will be shown. |

### showInputMethodPicker

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun showInputMethodPicker(): Unit
```

Show IME picker popup window.

Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_INPUT_METHODS:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

### showSoftInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun showSoftInput(
    view: View!, 
    flags: Int
): Boolean
```

Explicitly request that the current input method's soft input area be shown to the user, if needed. Call this if the user interacts with your view in such a way that they have expressed they would like to start performing input into it.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The currently focused view, which would like to receive soft keyboard input. Note that this view is only considered focused here if both it itself has `https://developer.android.com/reference/kotlin/android/view/View.html#isFocused()`, and its containing window has `https://developer.android.com/reference/kotlin/android/view/View.html#hasWindowFocus()`. Otherwise the call fails and returns `false`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_IMPLICIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_FORCED:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if a request was sent to system_server, `false` otherwise. Note: this does not return result of the request. If result is needed, use `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.html#show(kotlin.Int)` instead and set a `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener.html#` and verify the provided `https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#` for the visibility of IME. |

### showSoftInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun showSoftInput(
    view: View!, 
    flags: Int, 
    resultReceiver: ResultReceiver!
): Boolean
```

**Deprecated:** *The `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` is not a reliable way of determining whether the Input Method is actually shown or hidden. If result is needed, use `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.html#show(kotlin.Int)` instead and set a `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener.html#` and verify the provided `https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#` for the visibility of IME. If result is not needed, use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int)` instead.*

Explicitly request that the current input method's soft input area be shown to the user, if needed. Call this if the user interacts with your view in such a way that they have expressed they would like to start performing input into it.

**Caveat:** `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` instance passed to this method can be a long-lived object, because it may not be garbage-collected until all the corresponding `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` objects transferred to different processes get garbage-collected. Follow the general patterns to avoid memory leaks in Android. Consider to use `https://developer.android.com/reference/kotlin/java/lang/ref/WeakReference.html#` so that application logic objects such as `https://developer.android.com/reference/kotlin/android/app/Activity.html#` and `https://developer.android.com/reference/kotlin/android/content/Context.html#` can be garbage collected regardless of the lifetime of `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#`.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The currently focused view, which would like to receive soft keyboard input. Note that this view is only considered focused here if both it itself has `https://developer.android.com/reference/kotlin/android/view/View.html#isFocused()`, and its containing window has `https://developer.android.com/reference/kotlin/android/view/View.html#hasWindowFocus()`. Otherwise the call fails and returns `false`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_IMPLICIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_FORCED:kotlin.Int` |
| `resultReceiver` | [ResultReceiver](https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#)!: If non-null, this will be called by the IME when it has processed your request to tell you what it has done. The result code you receive may be either `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_UNCHANGED_SHOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_UNCHANGED_HIDDEN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_SHOWN:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_HIDDEN:kotlin.Int`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if a request was sent to system_server, `false` otherwise. Note: this does not return result of the request. For result use `resultReceiver` instead. |

### showSoftInputFromInputMethod

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun showSoftInputFromInputMethod(
    token: IBinder!, 
    flags: Int
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#requestShowSelf(kotlin.Int)` instead. This method was intended for IME developers who should be accessing APIs through the service. APIs in this class are intended for app developers interacting with the IME.*

Show the input method's soft input area, so the user sees the input method window and can interact with it. This can only be called from the currently active input method, as validated by the given token.

| Parameters ||
|---|---|
| `token` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!: Supplies the identifying token given to an input method when it was started, which allows it to perform this operation on itself. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_IMPLICIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_FORCED:kotlin.Int` |

### showStatusIcon

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun showStatusIcon(
    imeToken: IBinder!, 
    packageName: String!, 
    iconId: Int
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#showStatusIcon(kotlin.Int)` instead. This method was intended for IME developers who should be accessing APIs through the service. APIs in this class are intended for app developers interacting with the IME.*

### startConnectionlessStylusHandwriting

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startConnectionlessStylusHandwriting(
    view: View, 
    cursorAnchorInfo: CursorAnchorInfo?, 
    callbackExecutor: Executor, 
    callback: ConnectionlessHandwritingCallback
): Unit
```

Starts a connectionless stylus handwriting session. A connectionless session differs from a regular stylus handwriting session in that the IME does not use an input connection to communicate with a text editor. Instead, the IME directly returns recognised handwritten text via a callback.

The {code cursorAnchorInfo} may be used by the IME to improve the handwriting recognition accuracy and user experience of the handwriting session. Usually connectionless handwriting is used for a view which appears like a text editor but does not really support text editing. For best results, the {code cursorAnchorInfo} should be populated as it would be for a real text editor (for example, the insertion marker location can be set to where the user would expect it to be, even if there is no visible cursor).

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): the view receiving stylus events. This value cannot be `null`. |
| `cursorAnchorInfo` | [CursorAnchorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo)?: positional information about the view receiving stylus events. This value may be `null`. |
| `callbackExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor to run the callback on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [ConnectionlessHandwritingCallback](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback): the callback to receive the result. This value cannot be `null`. |

### startConnectionlessStylusHandwritingForDelegation

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startConnectionlessStylusHandwritingForDelegation(
    delegatorView: View, 
    cursorAnchorInfo: CursorAnchorInfo?, 
    delegatePackageName: String, 
    callbackExecutor: Executor, 
    callback: ConnectionlessHandwritingCallback
): Unit
```

Starts a connectionless stylus handwriting session (see `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwriting(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`) and additionally enables the recognised handwritten text to be later committed to a text editor using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View,%20kotlin.String)`.

After a connectionless session started using this method completes successfully, a text editor view, called the delegate view, may call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View,%20kotlin.String)` which will request the IME to commit the recognised handwritten text from the connectionless session to the delegate view.

The delegate view must belong to `delegatePackageName` for the delegation to succeed.

| Parameters ||
|---|---|
| `delegatorView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): the view receiving stylus events. This value cannot be `null`. |
| `cursorAnchorInfo` | [CursorAnchorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo)?: positional information about the view receiving stylus events. This value may be `null`. |
| `delegatePackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name of the package containing the delegate view which will accept the delegation. This value cannot be `null`. |
| --- | --- |
| `callbackExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor to run the callback on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [ConnectionlessHandwritingCallback](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback): the callback to receive the result. This value cannot be `null`. |

### startConnectionlessStylusHandwritingForDelegation

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startConnectionlessStylusHandwritingForDelegation(
    delegatorView: View, 
    cursorAnchorInfo: CursorAnchorInfo?, 
    callbackExecutor: Executor, 
    callback: ConnectionlessHandwritingCallback
): Unit
```

Starts a connectionless stylus handwriting session (see `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwriting(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)`) and additionally enables the recognised handwritten text to be later committed to a text editor using `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View)`.

After a connectionless session started using this method completes successfully, a text editor view, called the delegate view, may call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#acceptStylusHandwritingDelegation(android.view.View)` which will request the IME to commit the recognised handwritten text from the connectionless session to the delegate view.

The delegate view must belong to the same package as the delegator view for the delegation to succeed. If the delegate view belongs to a different package, use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20kotlin.String,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)` instead.

| Parameters ||
|---|---|
| `delegatorView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): the view receiving stylus events. This value cannot be `null`. |
| `cursorAnchorInfo` | [CursorAnchorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo)?: positional information about the view receiving stylus events. This value may be `null`. |
| `callbackExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor to run the callback on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [ConnectionlessHandwritingCallback](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback): the callback to receive the result. This value cannot be `null`. |

### startStylusHandwriting

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startStylusHandwriting(view: View): Unit
```

Start stylus handwriting session. If supported by the current input method, a stylus handwriting session is started on the given View, capturing all stylus input and converting it to InputConnection commands. If handwriting mode is started successfully by the IME, any currently dispatched stylus pointers will be `android.view.MotionEvent#FLAG_CANCELED` cancelled. If Stylus handwriting mode is not supported or cannot be fulfilled for any reason by IME, request will be ignored and Stylus touch will continue as normal touch input. Ideally, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#isStylusHandwritingAvailable()` should be called first to determine if stylus handwriting is supported by IME.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): the View for which stylus handwriting is requested. It and `https://developer.android.com/reference/kotlin/android/view/View.html#hasWindowFocus()` must be `https://developer.android.com/reference/kotlin/android/view/View.html#hasFocus()`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#isStylusHandwritingAvailable()`

### switchToLastInputMethod

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun switchToLastInputMethod(imeToken: IBinder!): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#switchToPreviousInputMethod()` instead. This method was intended for IME developers who should be accessing APIs through the service. APIs in this class are intended for app developers interacting with the IME.*

Force switch to the last used input method and subtype. If the last input method didn't have any subtypes, the framework will simply switch to the last input method with no subtype specified.

| Parameters ||
|---|---|
| `imeToken` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!: Supplies the identifying token given to an input method when it was started, which allows it to perform this operation on itself. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the current input method and subtype was successfully switched to the last used input method and subtype. |

### switchToNextInputMethod

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun switchToNextInputMethod(
    imeToken: IBinder!, 
    onlyCurrentIme: Boolean
): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#switchToNextInputMethod(kotlin.Boolean)` instead. This method was intended for IME developers who should be accessing APIs through the service. APIs in this class are intended for app developers interacting with the IME.*

Force switch to the next input method and subtype. If there is no IME enabled except current IME and subtype, do nothing.

| Parameters ||
|---|---|
| `imeToken` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!: Supplies the identifying token given to an input method when it was started, which allows it to perform this operation on itself. |
| `onlyCurrentIme` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, the framework will find the next subtype which belongs to the current IME |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the current input method and subtype was successfully switched to the next input method and subtype. |

### toggleSoftInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toggleSoftInput(
    showFlags: Int, 
    hideFlags: Int
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int)` explicitly instead. In particular during focus changes, the current visibility of the IME is not well defined. Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, this only has an effect if the calling app is the current IME focus.*

This method toggles the input method window display. If the input window is already displayed, it gets hidden. If not the input window will be displayed.

| Parameters ||
|---|---|
| `showFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_IMPLICIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_FORCED:kotlin.Int` |
| `hideFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_IMPLICIT_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_NOT_ALWAYS:kotlin.Int` |

### toggleSoftInputFromWindow

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toggleSoftInputFromWindow(
    windowToken: IBinder!, 
    showFlags: Int, 
    hideFlags: Int
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#showSoftInput(android.view.View,%20kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#hideSoftInputFromWindow(android.os.IBinder,%20kotlin.Int)` explicitly instead. In particular during focus changes, the current visibility of the IME is not well defined. Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, this only has an effect if the calling app is the current IME focus.*

This method toggles the input method window display. If the input window is already displayed, it gets hidden. If not the input window will be displayed.

| Parameters ||
|---|---|
| `windowToken` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!: The token of the window that is making the request, as returned by `https://developer.android.com/reference/kotlin/android/view/View.html#getWindowToken()`. |
| `showFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_IMPLICIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_FORCED:kotlin.Int` |
| `hideFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_IMPLICIT_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_NOT_ALWAYS:kotlin.Int` |
| --- | --- |

### updateCursor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun updateCursor(
    view: View!, 
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateCursorAnchorInfo(android.view.View,%20android.view.inputmethod.CursorAnchorInfo)` instead.*

Report the current cursor location in its window.

### updateCursorAnchorInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun updateCursorAnchorInfo(
    view: View!, 
    cursorAnchorInfo: CursorAnchorInfo!
): Unit
```

Report positional change of the text insertion point and/or characters in the composition string.

### updateExtractedText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun updateExtractedText(
    view: View!, 
    token: Int, 
    text: ExtractedText!
): Unit
```

### updateSelection

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun updateSelection(
    view: View!, 
    selStart: Int, 
    selEnd: Int, 
    candidatesStart: Int, 
    candidatesEnd: Int
): Unit
```

Report the current selection range.

**Editor authors** , you need to call this method whenever the cursor moves in your editor. Remember that in addition to doing this, your editor needs to always supply current cursor values in `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#initialSelStart:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#initialSelEnd:kotlin.Int` every time `https://developer.android.com/reference/kotlin/android/view/View.html#onCreateInputConnection(android.view.inputmethod.EditorInfo)` is called, which happens whenever the keyboard shows up or the focus changes to a text field, among other cases.

### viewClicked

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun viewClicked(view: View!): Unit
```

**Deprecated:** *The semantics of this method can never be defined well for composite `https://developer.android.com/reference/kotlin/android/view/View.html#` that works as a giant "Canvas", which can host its own UI hierarchy and sub focus state. `https://developer.android.com/reference/kotlin/android/webkit/WebView.html#` is a good example. Application / IME developers should not rely on this method.*

Notify the event when the user tapped or clicked the text view.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: `https://developer.android.com/reference/kotlin/android/view/View.html#` which is being clicked. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#onViewClicked(kotlin.Boolean)`
