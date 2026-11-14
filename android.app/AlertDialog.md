Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlertDialog

Kotlin | [Java](AlertDialog.md)
| --- | --- |

```
open class AlertDialog : Dialog, DialogInterface
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.app.Dialog](Dialog.md) ||
| | ↳ | [android.app.AlertDialog](AlertDialog.md) |

| Known Direct Subclasses [DatePickerDialog](DatePickerDialog.md), [ProgressDialog](ProgressDialog.md), [TimePickerDialog](TimePickerDialog.md) |---|---| | [DatePickerDialog](DatePickerDialog.md) | A simple dialog containing an `https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#`. | | [ProgressDialog](ProgressDialog.md) | A dialog showing a progress indicator and an optional text message or view. | | [TimePickerDialog](TimePickerDialog.md) | A dialog that prompts the user for the time of day using a `https://developer.android.com/reference/kotlin/android/widget/TimePicker.html#`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A subclass of Dialog that can display one, two or three buttons. If you only want to display a String in this dialog box, use the setMessage() method. If you want to display a more complex view, look up the FrameLayout called "custom" and add your view to it:

```kotlin
FrameLayout fl = findViewById(android.R.id.custom);
  fl.addView(myView, new LayoutParams(MATCH_PARENT, WRAP_CONTENT));
  
```

<br />

The AlertDialog class takes care of automatically setting `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_ALT_FOCUSABLE_IM:kotlin.Int` for you based on whether any views in the dialog return true from onCheckIsTextEditor. Generally you want this set for a Dialog without text editors, so that it will be placed on top of the current input method UI. You can modify this behavior by forcing the flag to your desired mode after calling onCreate.
|
| ### Developer Guides
|
| For more information about creating dialogs, read the [Dialogs](https://developer.android.com/guide/topics/ui/dialogs.html) developer guide.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/app/AlertDialog.Builder` <br /> |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_DEVICE_DEFAULT_DARK:kotlin.Int` Special theme constant for AlertDialog: use the device's default alert theme with a dark background. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_DEVICE_DEFAULT_LIGHT:kotlin.Int` Special theme constant for AlertDialog: use the device's default alert theme with a light background. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_HOLO_DARK:kotlin.Int` Special theme constant for AlertDialog: use the holographic alert theme with a dark background. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_HOLO_LIGHT:kotlin.Int` Special theme constant for AlertDialog: use the holographic alert theme with a light background. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_TRADITIONAL:kotlin.Int` Special theme constant for AlertDialog: use the traditional (pre-Holo) alert dialog theme. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON1:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON2:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON3:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEGATIVE:kotlin.Int` The identifier for the negative button. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEUTRAL:kotlin.Int` The identifier for the neutral button. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int` The identifier for the positive button. <br /> | ||

| Protected constructors ||
|---|---|
| AlertDialog Creates an alert dialog that uses the default alert dialog theme. |
| AlertDialog Creates an alert dialog that uses the default alert dialog theme and a custom cancel listener. |
| AlertDialog Creates an alert dialog that uses an explicit theme resource. |

| Public methods ||
|---|---|
| open [Button](../android.widget/Button.md)! | getButton Gets one of the buttons used in the dialog. |
| open [ListView](../android.widget/ListView.md)! | getListView Gets the list view used in the dialog. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onKeyDown A key was pressed down. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onKeyUp A key was released. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setButton Set a listener to be invoked when the specified button of the dialog is pressed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setButton Set a message to be sent when a button is pressed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setButton Set a listener to be invoked when button 1 of the dialog is pressed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setButton <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setButton2 Set a listener to be invoked when button 2 of the dialog is pressed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setButton2 <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setButton3 Set a listener to be invoked when button 3 of the dialog is pressed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setButton3 <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCustomTitle <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setIcon <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setIcon Set resId to 0 if you don't want an icon. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setIconAttribute Set an icon as supplied by a theme attribute. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setInverseBackgroundForced <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMessage <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTitle Set the title text for this dialog's window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setView Set the view to display in that dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setView Set the view to display in that dialog, specifying the spacing to appear around that view. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onCreate Similar to android. |

| Inherited functions ||
|---|---|
| From class Dialog |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | addContentView Add an additional content view to the screen. Added after any existing ones in the screen -- existing views are NOT removed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | cancel Cancel the dialog. This is essentially the same as calling dismiss, but it will also call your `https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#` (if registered). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | closeOptionsMenu <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | create Forces immediate creation of the dialog. Note that you should not override this method to perform dialog creation. Rather, override onCreate. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | dismiss Dismiss this dialog, removing it from the screen. This method can be invoked safely from any thread. Note that you should not override this method to do cleanup when the dialog is dismissed, instead implement that in onStop. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | dispatchGenericMotionEvent Called to process generic motion events. You can override this to intercept all generic motion events before they are dispatched to the window. Be sure to call this implementation for generic motion events that should be handled normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | dispatchKeyEvent Called to process key events. You can override this to intercept all key events before they are dispatched to the window. Be sure to call this implementation for key events that should be handled normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | dispatchKeyShortcutEvent Called to process a key shortcut event. You can override this to intercept all key shortcut events before they are dispatched to the window. Be sure to call this implementation for key shortcut events that should be handled normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | dispatchPopulateAccessibilityEvent Called to process population of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#`s. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | dispatchTouchEvent Called to process touch screen events. You can override this to intercept all touch screen events before they are dispatched to the window. Be sure to call this implementation for touch screen events that should be handled normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | dispatchTrackballEvent Called to process trackball events. You can override this to intercept all trackball events before they are dispatched to the window. Be sure to call this implementation for trackball events that should be handled normally. <br /> | | `T` | findViewById Finds the first descendant view with the given ID or `null` if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via show or create). **Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary. <br /> | | ActionBar | getActionBar Retrieve the ActionBar attached to this dialog, if present. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#` | getContext Retrieve the Context this Dialog is running in. <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#?` | getCurrentFocus Call getCurrentFocus on the Window if this Activity to return the currently focused view. <br /> | | `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` | getLayoutInflater <br /> | | `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` | getOnBackInvokedDispatcher Returns the `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` instance associated with the window that this dialog is attached to. <br /> | | Activity | getOwnerActivity Returns the Activity that owns this Dialog. For example, if showDialog is used to show this Dialog, that Activity will be the owner (by default). Depending on how this dialog was created, this may return null. <br /> | | `https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#?` | getSearchEvent During the onSearchRequested() callbacks, this function will return the `https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#` that triggered the callback, if it exists. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getVolumeControlStream <br /> | | `https://developer.android.com/reference/kotlin/android/view/Window.html#?` | getWindow Retrieve the current Window for the activity. This can be used to directly access parts of the Window API that are not available through Activity/Screen. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | hide Hide the dialog, but do not dismiss it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | invalidateOptionsMenu <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isShowing <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onActionModeFinished Called when an action mode has been finished. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeFinished(mode). If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onActionModeStarted Called when an action mode has been started. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeStarted(mode). If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onAttachedToWindow Called when the window has been attached to the window manager. See onAttachedToWindow for more information. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onBackPressed Called when the dialog has detected the user's press of the back key. The default implementation simply cancels the dialog (only if it is cancelable), but you can override this to do whatever you want. If you target version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, you should not use this method but register an `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback.html#` on an `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` that you can retrieve using getOnBackInvokedDispatcher. You should also set `android:enableOnBackInvokedCallback="true"` in the application manifest. Alternatively, you can use `androidx.activity.ComponentDialog#getOnBackPressedDispatcher()` for backward compatibility. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onContentChanged This hook is called whenever the content view of the screen changes (due to a call to setContentView or addContentView). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onContextItemSelected <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onContextMenuClosed <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onCreateContextMenu <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onCreateOptionsMenu It is usually safe to proxy this call to the owner activity's onCreateOptionsMenu if the client desires the same menu for this Dialog. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onCreatePanelMenu <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#?` | onCreatePanelView <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onDetachedFromWindow Called when the window has been detached from the window manager. See onDetachedFromWindow for more information. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onGenericMotionEvent Called when a generic motion event was not handled by any of the views inside of the dialog. Generic motion events describe joystick movements, mouse hovers, track pad touches, scroll wheel movements and other input events. The getSource of the motion event specifies the class of input that was received. Implementations of this method must examine the bits in the source before processing the event. The following code example shows how this is done. Generic motion events with source class `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_CLASS_POINTER:kotlin.Int` are delivered to the view under the pointer. All other generic motion events are delivered to the focused view. See onGenericMotionEvent for an example of how to handle this event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyLongPress Default implementation of onKeyLongPress: always returns false (doesn't handle the event). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyMultiple Default implementation of onKeyMultiple: always returns false (doesn't handle the event). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyShortcut Called when a key shortcut event is not handled by any of the views in the Dialog. Override this method to implement global key shortcuts for the Dialog. Key shortcuts can also be implemented by setting the setShortcut property of menu items. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onMenuItemSelected <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onMenuOpened <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onOptionsItemSelected <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onOptionsMenuClosed <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onPanelClosed <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onPrepareOptionsMenu It is usually safe to proxy this call to the owner activity's onPrepareOptionsMenu if the client desires the same menu for this Dialog. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onPreparePanel <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onRestoreInstanceState Restore the state of the dialog from a previously saved bundle. The default implementation restores the state of the dialog's view hierarchy that was saved in the default implementation of onSaveInstanceState, so be sure to call through to super when overriding unless you want to do all restoring of state yourself. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | onSaveInstanceState Saves the state of the dialog into a bundle. The default implementation saves the state of its view hierarchy, so you'll likely want to call through to super if you override this to save additional state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onSearchRequested This hook is called when the user signals the desire to start a search. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onSearchRequested This hook is called when the user signals the desire to start a search. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onStart Called when the dialog is starting. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onStop Called to tell you that you're stopping. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onTouchEvent Called when a touch screen event was not handled by any of the views under it. This is most useful to process touch events that happen outside of your window bounds, where there is no view to receive it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onTrackballEvent Called when the trackball was moved and not handled by any of the views inside of the activity. So, for example, if the trackball moves while focus is on a button, you will receive a call here because buttons do not normally do anything with trackball events. The call here happens *before* trackball movements are converted to DPAD key events, which then get sent back to the view hierarchy, and will be processed at the point for things like focus navigation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onWindowAttributesChanged This is called whenever the current window attributes change. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onWindowFocusChanged This hook is called whenever the window focus changes. See onWindowFocusChanged for more information. <br /> | | `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#?` | onWindowStartingActionMode Called when an action mode is being started for this window. Gives the callback an opportunity to handle the action mode in its own unique and beautiful way. If this method returns null the system can choose a way to present the mode or choose not to start the mode at all. This is equivalent to onWindowStartingActionMode with type `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#TYPE_PRIMARY:kotlin.Int`. <br /> | | `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#?` | onWindowStartingActionMode Called when an action mode is being started for this window. Gives the callback an opportunity to handle the action mode in its own unique and beautiful way. If this method returns null the system can choose a way to present the mode or choose not to start the mode at all. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | openContextMenu <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | openOptionsMenu <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | registerForContextMenu <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | requestWindowFeature Enable extended window features. This is a convenience for calling requestFeature. <br /> | | `T` | requireViewById Finds the first descendant view with the given ID or throws an IllegalArgumentException if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via show or create). **Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setCancelMessage Set a message to be sent when the dialog is canceled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setCancelable Sets whether this dialog is cancelable with the `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setCanceledOnTouchOutside Sets whether this dialog is canceled when touched outside the window's bounds. If setting to true, the dialog is set to be cancelable if not already set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setContentView Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setContentView Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setContentView Set the screen content from a layout resource. The resource will be inflated, adding all top-level views to the screen. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDismissMessage Set a message to be sent when the dialog is dismissed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFeatureDrawable Convenience for calling setFeatureDrawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFeatureDrawableAlpha Convenience for calling setFeatureDrawableAlpha. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFeatureDrawableResource Convenience for calling setFeatureDrawableResource. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFeatureDrawableUri Convenience for calling setFeatureDrawableUri. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOnCancelListener Set a listener to be invoked when the dialog is canceled. This will only be invoked when the dialog is canceled. Cancel events alone will not capture all ways that the dialog might be dismissed. If the creator needs to know when a dialog is dismissed in general, use setOnDismissListener. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOnDismissListener Set a listener to be invoked when the dialog is dismissed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOnKeyListener Sets the callback that will be called if a key is dispatched to the dialog. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOnShowListener Sets a listener to be invoked when the dialog is shown. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOwnerActivity Sets the Activity that owns this dialog. An example use: This Dialog will use the suggested volume control stream of the Activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTitle Set the title text for this dialog's window. The text is retrieved from the resources with the supplied identifier. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setVolumeControlStream By default, this will use the owner Activity's suggested stream type. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | show Start the dialog and display it on screen. The window is placed in the application layer and opaque. Note that you should not override this method to do initialization when the dialog is shown, instead implement that in onStart. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | takeKeyEvents Request that key events come to this dialog. Use this if your dialog has no views with focus, but the dialog still wants a chance to process key events. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unregisterForContextMenu <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onPointerCaptureChanged Called when pointer capture is enabled or disabled for the current window. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onProvideKeyboardShortcuts Called when Keyboard Shortcuts are requested for the current window. <br /> | ||

## Constants

### THEME_DEVICE_DEFAULT_DARK

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THEME_DEVICE_DEFAULT_DARK: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_DeviceDefault_Dialog_Alert:kotlin.Int`.*

Special theme constant for AlertDialog: use the device's default alert theme with a dark background.

 Value: 4

### THEME_DEVICE_DEFAULT_LIGHT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THEME_DEVICE_DEFAULT_LIGHT: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_DeviceDefault_Light_Dialog_Alert:kotlin.Int`.*

Special theme constant for AlertDialog: use the device's default alert theme with a light background.

 Value: 5

### THEME_HOLO_DARK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THEME_HOLO_DARK: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_Material_Dialog_Alert:kotlin.Int`.*

Special theme constant for AlertDialog: use the holographic alert theme with a dark background.

 Value: 2

### THEME_HOLO_LIGHT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THEME_HOLO_LIGHT: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_Material_Light_Dialog_Alert:kotlin.Int`.*

Special theme constant for AlertDialog: use the holographic alert theme with a light background.

 Value: 3

### THEME_TRADITIONAL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THEME_TRADITIONAL: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_Material_Dialog_Alert:kotlin.Int`.*

Special theme constant for AlertDialog: use the traditional (pre-Holo) alert dialog theme.

 Value: 1

## Protected constructors

### AlertDialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected AlertDialog(context: Context!)
```

Creates an alert dialog that uses the default alert dialog theme.

The default alert dialog theme is defined by `https://developer.android.com/reference/kotlin/android/R.attr.html#alertDialogTheme:kotlin.Int` within the parent `context`'s theme.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: the parent context |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_alertDialogTheme:kotlin.Int`

### AlertDialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected AlertDialog(
    context: Context!, 
    cancelable: Boolean, 
    cancelListener: DialogInterface.OnCancelListener!)
```

Creates an alert dialog that uses the default alert dialog theme and a custom cancel listener.

This is functionally identical to:

```kotlin
AlertDialog dialog = new AlertDialog(context);
      alertDialog.setCancelable(cancelable);
      alertDialog.setOnCancelListener(cancelListener);
  
```

The default alert dialog theme is defined by `https://developer.android.com/reference/kotlin/android/R.attr.html#alertDialogTheme:kotlin.Int` within the parent `context`'s theme.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: the parent context |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_alertDialogTheme:kotlin.Int`

### AlertDialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected AlertDialog(
    context: Context!, 
    themeResId: Int)
```

Creates an alert dialog that uses an explicit theme resource.

The specified theme resource (`themeResId`) is applied on top of the parent `context`'s theme. It may be specified as a style resource containing a fully-populated theme, such as `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_Material_Dialog:kotlin.Int`, to replace all attributes in the parent `context`'s theme including primary and accent colors.

To preserve attributes such as primary and accent colors, the `themeResId` may instead be specified as an overlay theme such as `https://developer.android.com/reference/kotlin/android/R.style.html#ThemeOverlay_Material_Dialog:kotlin.Int`. This will override only the window attributes necessary to style the alert window as a dialog.

Alternatively, the `themeResId` may be specified as `0` to use the parent `context`'s resolved value for `https://developer.android.com/reference/kotlin/android/R.attr.html#alertDialogTheme:kotlin.Int`.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: the parent context |
| `themeResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the resource ID of the theme against which to inflate this dialog, or `0` to use the parent `context`'s default alert dialog theme |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_alertDialogTheme:kotlin.Int`

## Public methods

### getButton

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getButton(whichButton: Int): Button!
```

Gets one of the buttons used in the dialog. Returns null if the specified button does not exist or the dialog has not yet been fully created (for example, via show or create).

| Parameters ||
|---|---|
| `whichButton` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The identifier of the button that should be returned. For example, this can be `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/widget/Button.html#!` | The button from the dialog, or null if a button does not exist. |

### getListView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getListView(): ListView!
```

Gets the list view used in the dialog.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/widget/ListView.html#!` | The `https://developer.android.com/reference/kotlin/android/widget/ListView.html#` from the dialog. |

### onKeyDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyDown(
    keyCode: Int, 
    event: KeyEvent
): Boolean
```

A key was pressed down.

If the focused view didn't want this event, this method is called.

Default implementation consumes `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` and, as of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_ESCAPE:kotlin.Int` to later handle them in onKeyUp.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value in event.getKeyCode(). |
| `event` | [KeyEvent](../android.view/KeyEvent.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyUp(
    keyCode: Int, 
    event: KeyEvent
): Boolean
```

A key was released.

Default implementation consumes `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` and, as of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_ESCAPE:kotlin.Int` to close the dialog.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value in event.getKeyCode(). |
| `event` | [KeyEvent](../android.view/KeyEvent.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### setButton

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton(
    whichButton: Int, 
    text: CharSequence!, 
    listener: DialogInterface.OnClickListener!
): Unit
```

Set a listener to be invoked when the specified button of the dialog is pressed.

| Parameters ||
|---|---|
| `whichButton` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which button to set the listener on, can be one of `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEGATIVE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEUTRAL:kotlin.Int` |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to display in positive button. |
| `listener` | [DialogInterface.OnClickListener](../android/content/DialogInterface.OnClickListener.md)!: The `https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#` to use. |
| --- | --- |

### setButton

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton(
    whichButton: Int, 
    text: CharSequence!, 
    msg: Message!
): Unit
```

Set a message to be sent when a button is pressed.

| Parameters ||
|---|---|
| `whichButton` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which button to set the message for, can be one of `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEGATIVE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEUTRAL:kotlin.Int` |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to display in positive button. |
| `msg` | [Message](../android.os/Message.md)!: The `https://developer.android.com/reference/kotlin/android/os/Message.html#` to be sent when clicked. |
| --- | --- |

### setButton

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton(
    text: CharSequence!, 
    listener: DialogInterface.OnClickListener!
): Unit
```

**Deprecated:** *Use setButton with `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int`*

Set a listener to be invoked when button 1 of the dialog is pressed.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to display in button 1. |
| `listener` | [DialogInterface.OnClickListener](../android/content/DialogInterface.OnClickListener.md)!: The `https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#` to use. |

### setButton

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton(
    text: CharSequence!, 
    msg: Message!
): Unit
```

**Deprecated:** *Use setButton with `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int`.*

### setButton2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton2(
    text: CharSequence!, 
    listener: DialogInterface.OnClickListener!
): Unit
```

**Deprecated:** *Use setButton with `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEGATIVE:kotlin.Int`*

Set a listener to be invoked when button 2 of the dialog is pressed.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to display in button 2. |
| `listener` | [DialogInterface.OnClickListener](../android/content/DialogInterface.OnClickListener.md)!: The `https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#` to use. |

### setButton2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton2(
    text: CharSequence!, 
    msg: Message!
): Unit
```

**Deprecated:** *Use setButton with `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEGATIVE:kotlin.Int`.*

### setButton3

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton3(
    text: CharSequence!, 
    listener: DialogInterface.OnClickListener!
): Unit
```

**Deprecated:** *Use setButton with `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEUTRAL:kotlin.Int`*

Set a listener to be invoked when button 3 of the dialog is pressed.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to display in button 3. |
| `listener` | [DialogInterface.OnClickListener](../android/content/DialogInterface.OnClickListener.md)!: The `https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#` to use. |

### setButton3

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton3(
    text: CharSequence!, 
    msg: Message!
): Unit
```

**Deprecated:** *Use setButton with `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEUTRAL:kotlin.Int`.*

### setCustomTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCustomTitle(customTitleView: View!): Unit
```
**See Also**

- setCustomTitle

### setIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIcon(icon: Drawable!): Unit
```

### setIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIcon(resId: Int): Unit
```

Set resId to 0 if you don't want an icon.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the resourceId of the drawable to use as the icon or 0 if you don't want an icon. |

### setIconAttribute

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIconAttribute(attrId: Int): Unit
```

Set an icon as supplied by a theme attribute. e.g. android.R.attr.alertDialogIcon

| Parameters ||
|---|---|
| `attrId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): ID of a theme attribute that points to a drawable resource. |

### setInverseBackgroundForced

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInverseBackgroundForced(forceInverseBackground: Boolean): Unit
```

### setMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMessage(message: CharSequence!): Unit
```

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTitle(title: CharSequence?): Unit
```

Set the title text for this dialog's window.

| Parameters ||
|---|---|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The new text to display in the title. This value may be `null`. |

### setView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setView(view: View!): Unit
```

Set the view to display in that dialog.

### setView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setView(
    view: View!, 
    viewSpacingLeft: Int, 
    viewSpacingTop: Int, 
    viewSpacingRight: Int, 
    viewSpacingBottom: Int
): Unit
```

Set the view to display in that dialog, specifying the spacing to appear around that view.

| Parameters ||
|---|---|
| `view` | [View](../android.view/View.md)!: The view to show in the content area of the dialog |
| `viewSpacingLeft` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Extra space to appear to the left of `view` |
| `viewSpacingTop` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Extra space to appear above `view` |
| --- | --- |
| `viewSpacingRight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Extra space to appear to the right of `view` |
| `viewSpacingBottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Extra space to appear below `view` |

## Protected methods

### onCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onCreate(savedInstanceState: Bundle!): Unit
```

Similar to android.app.Activity#onCreate, you should initialize your dialog in this method, including calling #setContentView.

| Parameters ||
|---|---|
| `savedInstanceState` | [Bundle](../android.os/Bundle.md)!: If this dialog is being reinitialized after a the hosting activity was previously shut down, holds the result from the most recent call to onSaveInstanceState, or null if this is the first time. |
