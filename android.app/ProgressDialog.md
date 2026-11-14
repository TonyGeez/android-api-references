# ProgressDialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProgressDialog

Kotlin| [Java](../android/app/ProgressDialog.md) 
| --- | --- |

```
open class ProgressDialog : AlertDialog
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.app.Dialog](../android/app/Dialog.md) |||
| | ↳ | [android.app.AlertDialog](../android/app/AlertDialog.md) ||
| | | ↳ | [android.app.ProgressDialog](../android/app/ProgressDialog.md) |
| --- | --- | --- | --- |

| **This class was deprecated in API level 26.**
|
| `ProgressDialog`is a modal dialog, which prevents the user from interacting with the app. Instead of using this class, you should use a progress indicator like [android.widget.ProgressBar](../android/widget/ProgressBar.md), which can be embedded in your app's UI. Alternatively, you can use a [notification](../guide/topics/ui/notifiers/notifications.md) to inform the user of the task's progress.

A dialog showing a progress indicator and an optional text message or view. Only a text message or a view can be used at the same time.

The dialog can be made cancelable on back key press.

The progress range is 0 to [max](../android/app/ProgressDialog.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STYLE_HORIZONTAL](../android/app/ProgressDialog.md) Creates a ProgressDialog with a horizontal progress bar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STYLE_SPINNER](../android/app/ProgressDialog.md) Creates a ProgressDialog with a circular, spinning progress bar. |

| Inherited constants ||
|---|---|
| From class [DialogInterface](../android/content/DialogInterface.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON1](../android/content/DialogInterface.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON2](../android/content/DialogInterface.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON3](../android/content/DialogInterface.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEGATIVE](../android/content/DialogInterface.md) <br /> The identifier for the negative button. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEUTRAL](../android/content/DialogInterface.md) <br /> The identifier for the neutral button. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_POSITIVE](../android/content/DialogInterface.md) <br /> The identifier for the positive button. <br /> | ||
| From class [AlertDialog](../android/app/AlertDialog.md) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THEME_DEVICE_DEFAULT_DARK](../android/app/AlertDialog.md) <br /> Special theme constant for [AlertDialog(android.content.Context,int)](../android/app/AlertDialog.md)): use the device's default alert theme with a dark background. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THEME_DEVICE_DEFAULT_LIGHT](../android/app/AlertDialog.md) <br /> Special theme constant for [AlertDialog(android.content.Context,int)](../android/app/AlertDialog.md)): use the device's default alert theme with a light background. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THEME_HOLO_DARK](../android/app/AlertDialog.md) <br /> Special theme constant for [AlertDialog(android.content.Context,int)](../android/app/AlertDialog.md)): use the holographic alert theme with a dark background. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THEME_HOLO_LIGHT](../android/app/AlertDialog.md) <br /> Special theme constant for [AlertDialog(android.content.Context,int)](../android/app/AlertDialog.md)): use the holographic alert theme with a light background. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THEME_TRADITIONAL](../android/app/AlertDialog.md) <br /> Special theme constant for [AlertDialog(android.content.Context,int)](../android/app/AlertDialog.md)): use the traditional (pre-Holo) alert dialog theme. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProgressDialog](../android/app/ProgressDialog.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Creates a Progress dialog. |
| [ProgressDialog](../android/app/ProgressDialog.md))`(`context:` ` [Context](../android/content/Context.md)!`, `theme:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a Progress dialog. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMax](../android/app/ProgressDialog.md))`()` Gets the maximum allowed progress value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getProgress](../android/app/ProgressDialog.md))`()` Gets the current progress. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecondaryProgress](../android/app/ProgressDialog.md))`()` Gets the current secondary progress. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [incrementProgressBy](../android/app/ProgressDialog.md))`(`diff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increments the current progress value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [incrementSecondaryProgressBy](../android/app/ProgressDialog.md))`(`diff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increments the current secondary progress value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIndeterminate](../android/app/ProgressDialog.md))`()` Whether this ProgressDialog is in indeterminate mode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](../android/app/ProgressDialog.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIndeterminate](../android/app/ProgressDialog.md))`(`indeterminate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Change the indeterminate mode for this ProgressDialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIndeterminateDrawable](../android/app/ProgressDialog.md))`(`d:` ` [Drawable](../android/graphics/drawable/Drawable.md)!`)` Sets the drawable to be used to display the indeterminate progress value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMax](../android/app/ProgressDialog.md))`(`max:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum allowed progress value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMessage](../android/app/ProgressDialog.md))`(`message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProgress](../android/app/ProgressDialog.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the current progress. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProgressDrawable](../android/app/ProgressDialog.md))`(`d:` ` [Drawable](../android/graphics/drawable/Drawable.md)!`)` Sets the drawable to be used to display the progress value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProgressNumberFormat](../android/app/ProgressDialog.md))`(`format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Change the format of the small text showing current and maximum units of progress. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProgressPercentFormat](../android/app/ProgressDialog.md))`(`format:` ` [NumberFormat](../java/text/NumberFormat.md)!`)` Change the format of the small text showing the percentage of progress. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProgressStyle](../android/app/ProgressDialog.md))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the style of this ProgressDialog, either [STYLE_SPINNER](../android/app/ProgressDialog.md) or [STYLE_HORIZONTAL](../android/app/ProgressDialog.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSecondaryProgress](../android/app/ProgressDialog.md))`(`secondaryProgress:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the secondary progress. |
| openstatic [ProgressDialog](../android/app/ProgressDialog.md)! | [show](../android/app/ProgressDialog.md))`(`context:` ` [Context](../android/content/Context.md)!`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Creates and shows a ProgressDialog. |
| --- | --- |
| openstatic [ProgressDialog](../android/app/ProgressDialog.md)! | [show](../android/app/ProgressDialog.md))`(`context:` ` [Context](../android/content/Context.md)!`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `indeterminate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates and shows a ProgressDialog. |
| openstatic [ProgressDialog](../android/app/ProgressDialog.md)! | [show](../android/app/ProgressDialog.md))`(`context:` ` [Context](../android/content/Context.md)!`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `indeterminate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `cancelable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates and shows a ProgressDialog. |
| openstatic [ProgressDialog](../android/app/ProgressDialog.md)! | [show](../android/app/ProgressDialog.md))`(`context:` ` [Context](../android/content/Context.md)!`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `indeterminate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `cancelable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `cancelListener:` ` [DialogInterface.OnCancelListener](../android/content/DialogInterface.OnCancelListener.md)!`)` Creates and shows a ProgressDialog. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreate](../android/app/ProgressDialog.md))`(`savedInstanceState:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStop](../android/app/ProgressDialog.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [Dialog](../android/app/Dialog.md) |------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addContentView](../android/app/Dialog.md))`(`view:` ` [View](../android/view/View.md)`, `params:` ` [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)?`)` <br /> Add an additional content view to the screen. Added after any existing ones in the screen -- existing views are NOT removed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../android/app/Dialog.md))`()` <br /> Cancel the dialog. This is essentially the same as calling [dismiss()](../android/app/Dialog.md)), but it will also call your [DialogInterface.OnCancelListener](../android/content/DialogInterface.OnCancelListener.md)(if registered). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeOptionsMenu](../android/app/Dialog.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [create](../android/app/Dialog.md))`()` <br /> Forces immediate creation of the dialog. Note that you should not override this method to perform dialog creation. Rather, override [onCreate(android.os.Bundle)](../android/app/Dialog.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](../android/app/Dialog.md))`()` <br /> Dismiss this dialog, removing it from the screen. This method can be invoked safely from any thread. Note that you should not override this method to do cleanup when the dialog is dismissed, instead implement that in [onStop](../android/app/Dialog.md)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchGenericMotionEvent](../android/app/Dialog.md))`(`ev:` ` [MotionEvent](../android/view/MotionEvent.md)`)` <br /> Called to process generic motion events. You can override this to intercept all generic motion events before they are dispatched to the window. Be sure to call this implementation for generic motion events that should be handled normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchKeyEvent](../android/app/Dialog.md))`(`event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` <br /> Called to process key events. You can override this to intercept all key events before they are dispatched to the window. Be sure to call this implementation for key events that should be handled normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchKeyShortcutEvent](../android/app/Dialog.md))`(`event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` <br /> Called to process a key shortcut event. You can override this to intercept all key shortcut events before they are dispatched to the window. Be sure to call this implementation for key shortcut events that should be handled normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchPopulateAccessibilityEvent](../android/app/Dialog.md))`(`event:` ` [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)`)` <br /> Called to process population of [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) s. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchTouchEvent](../android/app/Dialog.md))`(`ev:` ` [MotionEvent](../android/view/MotionEvent.md)`)` <br /> Called to process touch screen events. You can override this to intercept all touch screen events before they are dispatched to the window. Be sure to call this implementation for touch screen events that should be handled normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchTrackballEvent](../android/app/Dialog.md))`(`ev:` ` [MotionEvent](../android/view/MotionEvent.md)`)` <br /> Called to process trackball events. You can override this to intercept all trackball events before they are dispatched to the window. Be sure to call this implementation for trackball events that should be handled normally. <br /> | | T | [findViewById](../android/app/Dialog.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Finds the first descendant view with the given ID or`null`if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via [show()](../android/app/Dialog.md))or [create()](../android/app/Dialog.md))). **Note:**In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary. <br /> | | [ActionBar](../android/app/ActionBar.md)? | [getActionBar](../android/app/Dialog.md))`()` <br /> Retrieve the [ActionBar](../android/app/ActionBar.md) attached to this dialog, if present. <br /> | | [Context](../android/content/Context.md) | [getContext](../android/app/Dialog.md))`()` <br /> Retrieve the Context this Dialog is running in. <br /> | | [View](../android/view/View.md)? | [getCurrentFocus](../android/app/Dialog.md))`()` <br /> Call [android.view.Window#getCurrentFocus](../android/view/Window.md))on the Window if this Activity to return the currently focused view. <br /> | | [LayoutInflater](../android/view/LayoutInflater.md) | [getLayoutInflater](../android/app/Dialog.md))`()` <br /> | | [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md) | [getOnBackInvokedDispatcher](../android/app/Dialog.md))`()` <br /> Returns the [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md) instance associated with the window that this dialog is attached to. <br /> | | [Activity](../android/app/Activity.md)? | [getOwnerActivity](../android/app/Dialog.md))`()` <br /> Returns the Activity that owns this Dialog. For example, if [Activity.showDialog(int)](../android/app/Activity.md))is used to show this Dialog, that Activity will be the owner (by default). Depending on how this dialog was created, this may return null. <br /> | | [SearchEvent](../android/view/SearchEvent.md)? | [getSearchEvent](../android/app/Dialog.md))`()` <br /> During the onSearchRequested() callbacks, this function will return the [SearchEvent](../android/view/SearchEvent.md) that triggered the callback, if it exists. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolumeControlStream](../android/app/Dialog.md))`()` <br /> | | [Window](../android/view/Window.md)? | [getWindow](../android/app/Dialog.md))`()` <br /> Retrieve the current Window for the activity. This can be used to directly access parts of the Window API that are not available through Activity/Screen. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hide](../android/app/Dialog.md))`()` <br /> Hide the dialog, but do not dismiss it. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateOptionsMenu](../android/app/Dialog.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShowing](../android/app/Dialog.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionModeFinished](../android/app/Dialog.md))`(`mode:` ` [ActionMode](../android/view/ActionMode.md)!`)` <br /> Called when an action mode has been finished. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeFinished(mode). If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionModeStarted](../android/app/Dialog.md))`(`mode:` ` [ActionMode](../android/view/ActionMode.md)!`)` <br /> Called when an action mode has been started. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeStarted(mode). If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToWindow](../android/app/Dialog.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBackPressed](../android/app/Dialog.md))`()` <br /> Called when the dialog has detected the user's press of the back key. The default implementation simply cancels the dialog (only if it is cancelable), but you can override this to do whatever you want. If you target version [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md) or later, you should not use this method but register an [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md) on an [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md) that you can retrieve using [getOnBackInvokedDispatcher()](../android/app/Dialog.md)). You should also set`android:enableOnBackInvokedCallback="true"`in the application manifest. Alternatively, you can use`androidx.activity.ComponentDialog#getOnBackPressedDispatcher()`for backward compatibility. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](../android/app/Dialog.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onContextItemSelected](../android/app/Dialog.md))`(`item:` ` [MenuItem](../android/view/MenuItem.md)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContextMenuClosed](../android/app/Dialog.md))`(`menu:` ` [Menu](../android/view/Menu.md)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreateContextMenu](../android/app/Dialog.md))`(`menu:` ` [ContextMenu](../android/view/ContextMenu.md)!`, `v:` ` [View](../android/view/View.md)!`, `menuInfo:` ` [ContextMenu.ContextMenuInfo](../android/view/ContextMenu.ContextMenuInfo.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreateOptionsMenu](../android/app/Dialog.md))`(`menu:` ` [Menu](../android/view/Menu.md)`)` <br /> It is usually safe to proxy this call to the owner activity's [Activity.onCreateOptionsMenu(Menu)](../android/app/Activity.md))if the client desires the same menu for this Dialog. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreatePanelMenu](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](../android/view/Menu.md)`)` <br /> | | [View](../android/view/View.md)? | [onCreatePanelView](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDetachedFromWindow](../android/app/Dialog.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](../android/app/Dialog.md))`(`event:` ` [MotionEvent](../android/view/MotionEvent.md)`)` <br /> Called when a generic motion event was not handled by any of the views inside of the dialog. Generic motion events describe joystick movements, mouse hovers, track pad touches, scroll wheel movements and other input events. The [source](../android/view/MotionEvent.md))of the motion event specifies the class of input that was received. Implementations of this method must examine the bits in the source before processing the event. The following code example shows how this is done. Generic motion events with source class [android.view.InputDevice#SOURCE_CLASS_POINTER](../android/view/InputDevice.md) are delivered to the view under the pointer. All other generic motion events are delivered to the focused view. See [View.onGenericMotionEvent(MotionEvent)](../android/view/View.md))for an example of how to handle this event. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyLongPress](../android/app/Dialog.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` <br /> Default implementation of [KeyEvent.Callback.onKeyLongPress()](../android/view/KeyEvent.Callback.md)): always returns false (doesn't handle the event). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyMultiple](../android/app/Dialog.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `repeatCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` <br /> Default implementation of [KeyEvent.Callback.onKeyMultiple()](../android/view/KeyEvent.Callback.md)): always returns false (doesn't handle the event). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyShortcut](../android/app/Dialog.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` <br /> Called when a key shortcut event is not handled by any of the views in the Dialog. Override this method to implement global key shortcuts for the Dialog. Key shortcuts can also be implemented by setting the [shortcut](../android/view/MenuItem.md))property of menu items. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMenuItemSelected](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `item:` ` [MenuItem](../android/view/MenuItem.md)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMenuOpened](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](../android/view/Menu.md)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onOptionsItemSelected](../android/app/Dialog.md))`(`item:` ` [MenuItem](../android/view/MenuItem.md)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOptionsMenuClosed](../android/app/Dialog.md))`(`menu:` ` [Menu](../android/view/Menu.md)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPanelClosed](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](../android/view/Menu.md)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPrepareOptionsMenu](../android/app/Dialog.md))`(`menu:` ` [Menu](../android/view/Menu.md)`)` <br /> It is usually safe to proxy this call to the owner activity's [Activity.onPrepareOptionsMenu(Menu)](../android/app/Activity.md))if the client desires the same menu for this Dialog. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPreparePanel](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `view:` ` [View](../android/view/View.md)?`, `menu:` ` [Menu](../android/view/Menu.md)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestoreInstanceState](../android/app/Dialog.md))`(`savedInstanceState:` ` [Bundle](../android/os/Bundle.md)`)` <br /> Restore the state of the dialog from a previously saved bundle. The default implementation restores the state of the dialog's view hierarchy that was saved in the default implementation of [onSaveInstanceState()](../android/app/Dialog.md)), so be sure to call through to super when overriding unless you want to do all restoring of state yourself. <br /> | | [Bundle](../android/os/Bundle.md) | [onSaveInstanceState](../android/app/Dialog.md))`()` <br /> Saves the state of the dialog into a bundle. The default implementation saves the state of its view hierarchy, so you'll likely want to call through to super if you override this to save additional state. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSearchRequested](../android/app/Dialog.md))`()` <br /> This hook is called when the user signals the desire to start a search. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSearchRequested](../android/app/Dialog.md))`(`searchEvent:` ` [SearchEvent](../android/view/SearchEvent.md)`)` <br /> This hook is called when the user signals the desire to start a search. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](../android/app/Dialog.md))`()` <br /> Called when the dialog is starting. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStop](../android/app/Dialog.md))`()` <br /> Called to tell you that you're stopping. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](../android/app/Dialog.md))`(`event:` ` [MotionEvent](../android/view/MotionEvent.md)`)` <br /> Called when a touch screen event was not handled by any of the views under it. This is most useful to process touch events that happen outside of your window bounds, where there is no view to receive it. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTrackballEvent](../android/app/Dialog.md))`(`event:` ` [MotionEvent](../android/view/MotionEvent.md)`)` <br /> Called when the trackball was moved and not handled by any of the views inside of the activity. So, for example, if the trackball moves while focus is on a button, you will receive a call here because buttons do not normally do anything with trackball events. The call here happens*before*trackball movements are converted to DPAD key events, which then get sent back to the view hierarchy, and will be processed at the point for things like focus navigation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowAttributesChanged](../android/app/Dialog.md))`(`params:` ` [WindowManager.LayoutParams](../android/view/WindowManager.LayoutParams.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowFocusChanged](../android/app/Dialog.md))`(`hasFocus:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [ActionMode](../android/view/ActionMode.md)? | [onWindowStartingActionMode](../android/app/Dialog.md))`(`callback:` ` [ActionMode.Callback](../android/view/ActionMode.Callback.md)!`)` <br /> | | [ActionMode](../android/view/ActionMode.md)? | [onWindowStartingActionMode](../android/app/Dialog.md))`(`callback:` ` [ActionMode.Callback](../android/view/ActionMode.Callback.md)!`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openContextMenu](../android/app/Dialog.md))`(`view:` ` [View](../android/view/View.md)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openOptionsMenu](../android/app/Dialog.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerForContextMenu](../android/app/Dialog.md))`(`view:` ` [View](../android/view/View.md)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requestWindowFeature](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Enable extended window features. This is a convenience for calling [getWindow().requestFeature()](../android/view/Window.md)). <br /> | | T | [requireViewById](../android/app/Dialog.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Finds the first descendant view with the given ID or throws an IllegalArgumentException if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via [show()](../android/app/Dialog.md))or [create()](../android/app/Dialog.md))). **Note:**In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCancelMessage](../android/app/Dialog.md))`(`msg:` ` [Message](../android/os/Message.md)?`)` <br /> Set a message to be sent when the dialog is canceled. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCancelable](../android/app/Dialog.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this dialog is cancelable with the [BACK](../android/view/KeyEvent.md) key. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCanceledOnTouchOutside](../android/app/Dialog.md))`(`cancel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this dialog is canceled when touched outside the window's bounds. If setting to true, the dialog is set to be cancelable if not already set. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](../android/app/Dialog.md))`(`view:` ` [View](../android/view/View.md)`)` <br /> Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](../android/app/Dialog.md))`(`view:` ` [View](../android/view/View.md)`, `params:` ` [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)?`)` <br /> Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](../android/app/Dialog.md))`(`layoutResID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the screen content from a layout resource. The resource will be inflated, adding all top-level views to the screen. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDismissMessage](../android/app/Dialog.md))`(`msg:` ` [Message](../android/os/Message.md)?`)` <br /> Set a message to be sent when the dialog is dismissed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawable](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `drawable:` ` [Drawable](../android/graphics/drawable/Drawable.md)?`)` <br /> Convenience for calling [android.view.Window#setFeatureDrawable(int, Drawable)](../android/view/Window.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawableAlpha](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Convenience for calling [android.view.Window#setFeatureDrawableAlpha](../android/view/Window.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawableResource](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Convenience for calling [android.view.Window#setFeatureDrawableResource](../android/view/Window.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawableUri](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uri:` ` [Uri](../android/net/Uri.md)?`)` <br /> Convenience for calling [android.view.Window#setFeatureDrawableUri](../android/view/Window.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnCancelListener](../android/app/Dialog.md))`(`listener:` ` [DialogInterface.OnCancelListener](../android/content/DialogInterface.OnCancelListener.md)?`)` <br /> Set a listener to be invoked when the dialog is canceled. This will only be invoked when the dialog is canceled. Cancel events alone will not capture all ways that the dialog might be dismissed. If the creator needs to know when a dialog is dismissed in general, use [setOnDismissListener](../android/app/Dialog.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDismissListener](../android/app/Dialog.md))`(`listener:` ` [DialogInterface.OnDismissListener](../android/content/DialogInterface.OnDismissListener.md)?`)` <br /> Set a listener to be invoked when the dialog is dismissed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnKeyListener](../android/app/Dialog.md))`(`onKeyListener:` ` [DialogInterface.OnKeyListener](../android/content/DialogInterface.OnKeyListener.md)?`)` <br /> Sets the callback that will be called if a key is dispatched to the dialog. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnShowListener](../android/app/Dialog.md))`(`listener:` ` [DialogInterface.OnShowListener](../android/content/DialogInterface.OnShowListener.md)?`)` <br /> Sets a listener to be invoked when the dialog is shown. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOwnerActivity](../android/app/Dialog.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` <br /> Sets the Activity that owns this dialog. An example use: This Dialog will use the suggested volume control stream of the Activity. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](../android/app/Dialog.md))`(`titleId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the title text for this dialog's window. The text is retrieved from the resources with the supplied identifier. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVolumeControlStream](../android/app/Dialog.md))`(`streamType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> By default, this will use the owner Activity's suggested stream type. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](../android/app/Dialog.md))`()` <br /> Start the dialog and display it on screen. The window is placed in the application layer and opaque. Note that you should not override this method to do initialization when the dialog is shown, instead implement that in [onStart](../android/app/Dialog.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [takeKeyEvents](../android/app/Dialog.md))`(`get:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Request that key events come to this dialog. Use this if your dialog has no views with focus, but the dialog still wants a chance to process key events. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterForContextMenu](../android/app/Dialog.md))`(`view:` ` [View](../android/view/View.md)`)` <br /> | ||
| From class [AlertDialog](../android/app/AlertDialog.md) |-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Button](../android/widget/Button.md)! | [getButton](../android/app/AlertDialog.md))`(`whichButton:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets one of the buttons used in the dialog. Returns null if the specified button does not exist or the dialog has not yet been fully created (for example, via [show()](../android/app/Dialog.md))or [create()](../android/app/Dialog.md))). <br /> | | [ListView](../android/widget/ListView.md)! | [getListView](../android/app/AlertDialog.md))`()` <br /> Gets the list view used in the dialog. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](../android/app/AlertDialog.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](../android/app/AlertDialog.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton](../android/app/AlertDialog.md))`(`whichButton:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `listener:` ` [DialogInterface.OnClickListener](../android/content/DialogInterface.OnClickListener.md)!`)` <br /> Set a listener to be invoked when the specified button of the dialog is pressed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton](../android/app/AlertDialog.md))`(`whichButton:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `msg:` ` [Message](../android/os/Message.md)!`)` <br /> Set a message to be sent when a button is pressed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton](../android/app/AlertDialog.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `listener:` ` [DialogInterface.OnClickListener](../android/content/DialogInterface.OnClickListener.md)!`)` <br /> Set a listener to be invoked when button 1 of the dialog is pressed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton](../android/app/AlertDialog.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `msg:` ` [Message](../android/os/Message.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton2](../android/app/AlertDialog.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `listener:` ` [DialogInterface.OnClickListener](../android/content/DialogInterface.OnClickListener.md)!`)` <br /> Set a listener to be invoked when button 2 of the dialog is pressed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton2](../android/app/AlertDialog.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `msg:` ` [Message](../android/os/Message.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton3](../android/app/AlertDialog.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `listener:` ` [DialogInterface.OnClickListener](../android/content/DialogInterface.OnClickListener.md)!`)` <br /> Set a listener to be invoked when button 3 of the dialog is pressed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton3](../android/app/AlertDialog.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `msg:` ` [Message](../android/os/Message.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCustomTitle](../android/app/AlertDialog.md))`(`customTitleView:` ` [View](../android/view/View.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](../android/app/AlertDialog.md))`(`icon:` ` [Drawable](../android/graphics/drawable/Drawable.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](../android/app/AlertDialog.md))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set resId to 0 if you don't want an icon. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIconAttribute](../android/app/AlertDialog.md))`(`attrId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set an icon as supplied by a theme attribute. e.g. android.R.attr.alertDialogIcon <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInverseBackgroundForced](../android/app/AlertDialog.md))`(`forceInverseBackground:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](../android/app/AlertDialog.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setView](../android/app/AlertDialog.md))`(`view:` ` [View](../android/view/View.md)!`)` <br /> Set the view to display in that dialog. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setView](../android/app/AlertDialog.md))`(`view:` ` [View](../android/view/View.md)!`, `viewSpacingLeft:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `viewSpacingTop:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `viewSpacingRight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `viewSpacingBottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the view to display in that dialog, specifying the spacing to appear around that view. <br /> | ||
| From class [Callback](../android/view/Window.Callback.md) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPointerCaptureChanged](../android/view/Window.Callback.md))`(`hasCapture:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Called when pointer capture is enabled or disabled for the current window. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProvideKeyboardShortcuts](../android/view/Window.Callback.md))`(`data:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [KeyboardShortcutGroup](../android/view/KeyboardShortcutGroup.md)!>!`, `menu:` ` [Menu](../android/view/Menu.md)?`, `deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when Keyboard Shortcuts are requested for the current window. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Constants

### STYLE_HORIZONTAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STYLE_HORIZONTAL: Int
```

**Deprecated:** *Deprecated in Java.*

Creates a ProgressDialog with a horizontal progress bar. 

 Value: 1

### STYLE_SPINNER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STYLE_SPINNER: Int
```

**Deprecated:** *Deprecated in Java.*

Creates a ProgressDialog with a circular, spinning progress bar. This is the default. 

 Value: 0

## Public constructors

### ProgressDialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProgressDialog(context: Context!)
```

Creates a Progress dialog.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the parent context |

### ProgressDialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProgressDialog(
    context: Context!, 
    theme: Int)
```

Creates a Progress dialog.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the parent context |
| `theme` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the resource ID of the theme against which to inflate this dialog, or`0`to use the parent`context`'s default alert dialog theme |

## Public methods

### getMax

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMax(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the maximum allowed progress value. The default value is 100.

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum value |

### getProgress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProgress(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the current progress.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current progress, a value between 0 and [getMax()](../android/app/ProgressDialog.md)) |

### getSecondaryProgress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSecondaryProgress(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the current secondary progress.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current secondary progress, a value between 0 and [getMax()](../android/app/ProgressDialog.md)) |

### incrementProgressBy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun incrementProgressBy(diff: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Increments the current progress value.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `diff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount by which the current progress will be incremented, up to [getMax()](../android/app/ProgressDialog.md)) |

### incrementSecondaryProgressBy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun incrementSecondaryProgressBy(diff: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Increments the current secondary progress value.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `diff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount by which the current secondary progress will be incremented, up to [getMax()](../android/app/ProgressDialog.md)) |

### isIndeterminate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isIndeterminate(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Whether this ProgressDialog is in indeterminate mode.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the dialog is in indeterminate mode, false otherwise |

### onStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStart(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setIndeterminate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIndeterminate(indeterminate: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Change the indeterminate mode for this ProgressDialog. In indeterminate mode, the progress is ignored and the dialog shows an infinite animation instead.

**Note:** A ProgressDialog with style [STYLE_SPINNER](../android/app/ProgressDialog.md) is always indeterminate and will ignore this setting.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `indeterminate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to enable indeterminate mode, false otherwise |

**See Also**

- [#setProgressStyle(int)](../android/app/ProgressDialog.md)) 

### setIndeterminateDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIndeterminateDrawable(d: Drawable!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the drawable to be used to display the indeterminate progress value.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------|
| `d` | [Drawable](../android/graphics/drawable/Drawable.md)!:the drawable to be used |

**See Also**

- [android.widget.ProgressBar#setProgressDrawable(Drawable)](../android/widget/ProgressBar.md))
- [#setIndeterminate(boolean)](../android/app/ProgressDialog.md)) 

### setMax

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMax(max: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the maximum allowed progress value. 

### setMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMessage(message: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setProgress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProgress(value: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the current progress.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current progress, a value between 0 and [getMax()](../android/app/ProgressDialog.md)) |

**See Also**

- [android.widget.ProgressBar#setProgress(int)](../android/widget/ProgressBar.md)) 

### setProgressDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProgressDrawable(d: Drawable!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the drawable to be used to display the progress value.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------|
| `d` | [Drawable](../android/graphics/drawable/Drawable.md)!:the drawable to be used |

**See Also**

- [android.widget.ProgressBar#setProgressDrawable(Drawable)](../android/widget/ProgressBar.md)) 

### setProgressNumberFormat

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProgressNumberFormat(format: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Change the format of the small text showing current and maximum units of progress. The default is "%1d/%2d". Should not be called during the number is progressing.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string passed to java.lang.String#format; use "%1d" for the current number and "%2d" for the maximum. If null, nothing will be shown. |

### setProgressPercentFormat

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProgressPercentFormat(format: NumberFormat!): Unit
```

**Deprecated:** *Deprecated in Java.*

Change the format of the small text showing the percentage of progress. The default is [NumberFormat.getPercentageInstnace().](../java/text/NumberFormat.md))Should not be called during the number is progressing.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [NumberFormat](../java/text/NumberFormat.md)!:An instance of a [NumberFormat](../java/text/NumberFormat.md) to generate the percentage text. If null, nothing will be shown. |

### setProgressStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProgressStyle(style: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the style of this ProgressDialog, either [STYLE_SPINNER](../android/app/ProgressDialog.md) or [STYLE_HORIZONTAL](../android/app/ProgressDialog.md). The default is [STYLE_SPINNER](../android/app/ProgressDialog.md).

**Note:** A ProgressDialog with style [STYLE_SPINNER](../android/app/ProgressDialog.md) is always indeterminate and will ignore the [indeterminate](../android/app/ProgressDialog.md))setting.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the style of this ProgressDialog, either [STYLE_SPINNER](../android/app/ProgressDialog.md) or [STYLE_HORIZONTAL](../android/app/ProgressDialog.md) |

### setSecondaryProgress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSecondaryProgress(secondaryProgress: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the secondary progress.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `secondaryProgress` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current secondary progress, a value between 0 and [getMax()](../android/app/ProgressDialog.md)) |

**See Also**

- [android.widget.ProgressBar#setSecondaryProgress(int)](../android/widget/ProgressBar.md)) 

### show

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun show(
    context: Context!, 
    title: CharSequence!, 
    message: CharSequence!
): ProgressDialog!
```

**Deprecated:** *Deprecated in Java.*

Creates and shows a ProgressDialog.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the parent context |
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the title text for the dialog's window |
| `message` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to be displayed in the dialog |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------|
| [ProgressDialog](../android/app/ProgressDialog.md)! | the ProgressDialog |

### show

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun show(
    context: Context!, 
    title: CharSequence!, 
    message: CharSequence!, 
    indeterminate: Boolean
): ProgressDialog!
```

**Deprecated:** *Deprecated in Java.*

Creates and shows a ProgressDialog.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the parent context |
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the title text for the dialog's window |
| `message` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to be displayed in the dialog |
| --- | --- |
| `indeterminate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the dialog should be [indeterminate](../android/app/ProgressDialog.md)), false otherwise |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------|
| [ProgressDialog](../android/app/ProgressDialog.md)! | the ProgressDialog |

### show

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun show(
    context: Context!, 
    title: CharSequence!, 
    message: CharSequence!, 
    indeterminate: Boolean, 
    cancelable: Boolean
): ProgressDialog!
```

**Deprecated:** *Deprecated in Java.*

Creates and shows a ProgressDialog.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the parent context |
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the title text for the dialog's window |
| `message` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to be displayed in the dialog |
| --- | --- |
| `indeterminate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the dialog should be [indeterminate](../android/app/ProgressDialog.md)), false otherwise |
| `cancelable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the dialog is [cancelable](../android/app/Dialog.md)), false otherwise |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------|
| [ProgressDialog](../android/app/ProgressDialog.md)! | the ProgressDialog |

### show

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun show(
    context: Context!, 
    title: CharSequence!, 
    message: CharSequence!, 
    indeterminate: Boolean, 
    cancelable: Boolean, 
    cancelListener: DialogInterface.OnCancelListener!
): ProgressDialog!
```

**Deprecated:** *Deprecated in Java.*

Creates and shows a ProgressDialog.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the parent context |
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the title text for the dialog's window |
| `message` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to be displayed in the dialog |
| --- | --- |
| `indeterminate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the dialog should be [indeterminate](../android/app/ProgressDialog.md)), false otherwise |
| `cancelable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the dialog is [cancelable](../android/app/Dialog.md)), false otherwise |
| `cancelListener` | [DialogInterface.OnCancelListener](../android/content/DialogInterface.OnCancelListener.md)!:the [listener](../android/app/Dialog.md))to be invoked when the dialog is canceled |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------|
| [ProgressDialog](../android/app/ProgressDialog.md)! | the ProgressDialog |

## Protected methods

### onCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onCreate(savedInstanceState: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `savedInstanceState` | [Bundle](../android/os/Bundle.md)!:If this dialog is being reinitialized after a the hosting activity was previously shut down, holds the result from the most recent call to [onSaveInstanceState](../android/app/Dialog.md)), or null if this is the first time. |

### onStop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStop(): Unit
```

**Deprecated:** *Deprecated in Java.*
