Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlertDialog

Kotlin | [Java](https://developer.android.com/reference/android/app/AlertDialog "View this page in Java")
| --- | --- |

```
open class AlertDialog : Dialog, DialogInterface
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.app.Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog) ||
| | ↳ | [android.app.AlertDialog](https://developer.android.com/reference/kotlin/android/app/AlertDialog#) |

| Known Direct Subclasses [DatePickerDialog](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog), [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog), [TimePickerDialog](https://developer.android.com/reference/kotlin/android/app/TimePickerDialog) |---|---| | [DatePickerDialog](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog) | A simple dialog containing an `https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#`. | | [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog) | A dialog showing a progress indicator and an optional text message or view. | | [TimePickerDialog](https://developer.android.com/reference/kotlin/android/app/TimePickerDialog) | A dialog that prompts the user for the time of day using a `https://developer.android.com/reference/kotlin/android/widget/TimePicker.html#`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A subclass of Dialog that can display one, two or three buttons. If you only want to display a String in this dialog box, use the setMessage() method. If you want to display a more complex view, look up the FrameLayout called "custom" and add your view to it:

```kotlin
FrameLayout fl = findViewById(android.R.id.custom);
  fl.addView(myView, new LayoutParams(MATCH_PARENT, WRAP_CONTENT));
  
```

<br />

The AlertDialog class takes care of automatically setting `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_ALT_FOCUSABLE_IM:kotlin.Int` for you based on whether any views in the dialog return true from `https://developer.android.com/reference/kotlin/android/view/View.html#onCheckIsTextEditor()`. Generally you want this set for a Dialog without text editors, so that it will be placed on top of the current input method UI. You can modify this behavior by forcing the flag to your desired mode after calling `https://developer.android.com/reference/kotlin/android/app/AlertDialog#onCreate(android.os.Bundle)`.
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
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_DEVICE_DEFAULT_DARK:kotlin.Int` Special theme constant for `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)`: use the device's default alert theme with a dark background. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_DEVICE_DEFAULT_LIGHT:kotlin.Int` Special theme constant for `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)`: use the device's default alert theme with a light background. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_HOLO_DARK:kotlin.Int` Special theme constant for `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)`: use the holographic alert theme with a dark background. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_HOLO_LIGHT:kotlin.Int` Special theme constant for `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)`: use the holographic alert theme with a light background. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_TRADITIONAL:kotlin.Int` Special theme constant for `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)`: use the traditional (pre-Holo) alert dialog theme. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON1:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON2:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON3:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEGATIVE:kotlin.Int` The identifier for the negative button. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEUTRAL:kotlin.Int` The identifier for the neutral button. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int` The identifier for the positive button. <br /> | ||

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Creates an alert dialog that uses the default alert dialog theme. |
| `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Boolean,%20android.content.DialogInterface.OnCancelListener)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, cancelable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, cancelListener: https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#!)` Creates an alert dialog that uses the default alert dialog theme and a custom cancel listener. |
| `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, themeResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates an alert dialog that uses an explicit theme resource. |

| Public methods ||
|---|---|
| open [Button](https://developer.android.com/reference/kotlin/android/widget/Button.html#)! | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#getButton(kotlin.Int)(whichButton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets one of the buttons used in the dialog. |
| open [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#)! | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#getListView()()` Gets the list view used in the dialog. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#onKeyDown(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)` A key was pressed down. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#onKeyUp(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)` A key was released. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.Int,%20kotlin.CharSequence,%20android.content.DialogInterface.OnClickListener)(whichButton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, listener: https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#!)` Set a listener to be invoked when the specified button of the dialog is pressed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.Int,%20kotlin.CharSequence,%20android.os.Message)(whichButton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, msg: https://developer.android.com/reference/kotlin/android/os/Message.html#!)` Set a message to be sent when a button is pressed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.CharSequence,%20android.content.DialogInterface.OnClickListener)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, listener: https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#!)` Set a listener to be invoked when button 1 of the dialog is pressed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.CharSequence,%20android.os.Message)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, msg: https://developer.android.com/reference/kotlin/android/os/Message.html#!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton2(kotlin.CharSequence,%20android.content.DialogInterface.OnClickListener)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, listener: https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#!)` Set a listener to be invoked when button 2 of the dialog is pressed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton2(kotlin.CharSequence,%20android.os.Message)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, msg: https://developer.android.com/reference/kotlin/android/os/Message.html#!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton3(kotlin.CharSequence,%20android.content.DialogInterface.OnClickListener)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, listener: https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#!)` Set a listener to be invoked when button 3 of the dialog is pressed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton3(kotlin.CharSequence,%20android.os.Message)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, msg: https://developer.android.com/reference/kotlin/android/os/Message.html#!)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setCustomTitle(android.view.View)(customTitleView: https://developer.android.com/reference/kotlin/android/view/View.html#!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setIcon(android.graphics.drawable.Drawable)(icon: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setIcon(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set resId to 0 if you don't want an icon. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setIconAttribute(kotlin.Int)(attrId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set an icon as supplied by a theme attribute. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setInverseBackgroundForced(kotlin.Boolean)(forceInverseBackground: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setMessage(kotlin.CharSequence)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setTitle(kotlin.CharSequence)(title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Set the title text for this dialog's window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setView(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Set the view to display in that dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setView(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, viewSpacingLeft: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, viewSpacingTop: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, viewSpacingRight: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, viewSpacingBottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the view to display in that dialog, specifying the spacing to appear around that view. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlertDialog#onCreate(android.os.Bundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Similar to android. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/app/Dialog` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#addContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)(view: https://developer.android.com/reference/kotlin/android/view/View.html#, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#?)` Add an additional content view to the screen. Added after any existing ones in the screen -- existing views are NOT removed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#cancel()()` Cancel the dialog. This is essentially the same as calling `https://developer.android.com/reference/kotlin/android/app/Dialog#dismiss()`, but it will also call your `https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#` (if registered). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#closeOptionsMenu()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#create()()` Forces immediate creation of the dialog. Note that you should not override this method to perform dialog creation. Rather, override `https://developer.android.com/reference/kotlin/android/app/Dialog#onCreate(android.os.Bundle)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#dismiss()()` Dismiss this dialog, removing it from the screen. This method can be invoked safely from any thread. Note that you should not override this method to do cleanup when the dialog is dismissed, instead implement that in `https://developer.android.com/reference/kotlin/android/app/Dialog#onStop()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchGenericMotionEvent(android.view.MotionEvent)(ev: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)` Called to process generic motion events. You can override this to intercept all generic motion events before they are dispatched to the window. Be sure to call this implementation for generic motion events that should be handled normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchKeyEvent(android.view.KeyEvent)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)` Called to process key events. You can override this to intercept all key events before they are dispatched to the window. Be sure to call this implementation for key events that should be handled normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchKeyShortcutEvent(android.view.KeyEvent)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)` Called to process a key shortcut event. You can override this to intercept all key shortcut events before they are dispatched to the window. Be sure to call this implementation for key shortcut events that should be handled normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchPopulateAccessibilityEvent(android.view.accessibility.AccessibilityEvent)(event: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#)` Called to process population of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#`s. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchTouchEvent(android.view.MotionEvent)(ev: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)` Called to process touch screen events. You can override this to intercept all touch screen events before they are dispatched to the window. Be sure to call this implementation for touch screen events that should be handled normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchTrackballEvent(android.view.MotionEvent)(ev: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)` Called to process trackball events. You can override this to intercept all trackball events before they are dispatched to the window. Be sure to call this implementation for trackball events that should be handled normally. <br /> | | `T` | `https://developer.android.com/reference/kotlin/android/app/Dialog#findViewById(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Finds the first descendant view with the given ID or `null` if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via `https://developer.android.com/reference/kotlin/android/app/Dialog#show()` or `https://developer.android.com/reference/kotlin/android/app/Dialog#create()`). **Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary. <br /> | | `https://developer.android.com/reference/kotlin/android/app/ActionBar?` | `https://developer.android.com/reference/kotlin/android/app/Dialog#getActionBar()()` Retrieve the `https://developer.android.com/reference/kotlin/android/app/ActionBar` attached to this dialog, if present. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#` | `https://developer.android.com/reference/kotlin/android/app/Dialog#getContext()()` Retrieve the Context this Dialog is running in. <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#?` | `https://developer.android.com/reference/kotlin/android/app/Dialog#getCurrentFocus()()` Call `https://developer.android.com/reference/kotlin/android/view/Window.html#getCurrentFocus()` on the Window if this Activity to return the currently focused view. <br /> | | `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` | `https://developer.android.com/reference/kotlin/android/app/Dialog#getLayoutInflater()()` <br /> | | `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` | `https://developer.android.com/reference/kotlin/android/app/Dialog#getOnBackInvokedDispatcher()()` Returns the `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` instance associated with the window that this dialog is attached to. <br /> | | `https://developer.android.com/reference/kotlin/android/app/Activity?` | `https://developer.android.com/reference/kotlin/android/app/Dialog#getOwnerActivity()()` Returns the Activity that owns this Dialog. For example, if `https://developer.android.com/reference/kotlin/android/app/Activity#showDialog(kotlin.Int)` is used to show this Dialog, that Activity will be the owner (by default). Depending on how this dialog was created, this may return null. <br /> | | `https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#?` | `https://developer.android.com/reference/kotlin/android/app/Dialog#getSearchEvent()()` During the onSearchRequested() callbacks, this function will return the `https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#` that triggered the callback, if it exists. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#getVolumeControlStream()()` <br /> | | `https://developer.android.com/reference/kotlin/android/view/Window.html#?` | `https://developer.android.com/reference/kotlin/android/app/Dialog#getWindow()()` Retrieve the current Window for the activity. This can be used to directly access parts of the Window API that are not available through Activity/Screen. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#hide()()` Hide the dialog, but do not dismiss it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#invalidateOptionsMenu()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#isShowing()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onActionModeFinished(android.view.ActionMode)(mode: https://developer.android.com/reference/kotlin/android/view/ActionMode.html#!)` Called when an action mode has been finished. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeFinished(mode). If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onActionModeStarted(android.view.ActionMode)(mode: https://developer.android.com/reference/kotlin/android/view/ActionMode.html#!)` Called when an action mode has been started. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeStarted(mode). If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onAttachedToWindow()()` Called when the window has been attached to the window manager. See `https://developer.android.com/reference/kotlin/android/view/View.html#onAttachedToWindow()` for more information. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onBackPressed()()` Called when the dialog has detected the user's press of the back key. The default implementation simply cancels the dialog (only if it is cancelable), but you can override this to do whatever you want. If you target version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, you should not use this method but register an `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback.html#` on an `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` that you can retrieve using `https://developer.android.com/reference/kotlin/android/app/Dialog#getOnBackInvokedDispatcher()`. You should also set `android:enableOnBackInvokedCallback="true"` in the application manifest. Alternatively, you can use `androidx.activity.ComponentDialog#getOnBackPressedDispatcher()` for backward compatibility. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onContentChanged()()` This hook is called whenever the content view of the screen changes (due to a call to `https://developer.android.com/reference/kotlin/android/view/Window.html#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)` or `https://developer.android.com/reference/kotlin/android/view/Window.html#addContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)`). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onContextItemSelected(android.view.MenuItem)(item: https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onContextMenuClosed(android.view.Menu)(menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo)(menu: https://developer.android.com/reference/kotlin/android/view/ContextMenu.html#!, v: https://developer.android.com/reference/kotlin/android/view/View.html#!, menuInfo: https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo.html#!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onCreateOptionsMenu(android.view.Menu)(menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)` It is usually safe to proxy this call to the owner activity's `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateOptionsMenu(android.view.Menu)` if the client desires the same menu for this Dialog. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onCreatePanelMenu(kotlin.Int,%20android.view.Menu)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)` <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#?` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onCreatePanelView(kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onDetachedFromWindow()()` Called when the window has been detached from the window manager. See `https://developer.android.com/reference/kotlin/android/view/View.html#onDetachedFromWindow()` for more information. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onGenericMotionEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)` Called when a generic motion event was not handled by any of the views inside of the dialog. Generic motion events describe joystick movements, mouse hovers, track pad touches, scroll wheel movements and other input events. The `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getSource()` of the motion event specifies the class of input that was received. Implementations of this method must examine the bits in the source before processing the event. The following code example shows how this is done. Generic motion events with source class `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_CLASS_POINTER:kotlin.Int` are delivered to the view under the pointer. All other generic motion events are delivered to the focused view. See `https://developer.android.com/reference/kotlin/android/view/View.html#onGenericMotionEvent(android.view.MotionEvent)` for an example of how to handle this event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)` Default implementation of `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)`: always returns false (doesn't handle the event). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, repeatCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)` Default implementation of `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent)`: always returns false (doesn't handle the event). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyShortcut(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)` Called when a key shortcut event is not handled by any of the views in the Dialog. Override this method to implement global key shortcuts for the Dialog. Key shortcuts can also be implemented by setting the `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#setShortcut(kotlin.Char,%20kotlin.Char)` property of menu items. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onMenuItemSelected(kotlin.Int,%20android.view.MenuItem)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, item: https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onMenuOpened(kotlin.Int,%20android.view.Menu)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onOptionsItemSelected(android.view.MenuItem)(item: https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onOptionsMenuClosed(android.view.Menu)(menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onPanelClosed(kotlin.Int,%20android.view.Menu)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onPrepareOptionsMenu(android.view.Menu)(menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)` It is usually safe to proxy this call to the owner activity's `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareOptionsMenu(android.view.Menu)` if the client desires the same menu for this Dialog. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onPreparePanel(kotlin.Int,%20android.view.View,%20android.view.Menu)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, view: https://developer.android.com/reference/kotlin/android/view/View.html#?, menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onRestoreInstanceState(android.os.Bundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Restore the state of the dialog from a previously saved bundle. The default implementation restores the state of the dialog's view hierarchy that was saved in the default implementation of `https://developer.android.com/reference/kotlin/android/app/Dialog#onSaveInstanceState()`, so be sure to call through to super when overriding unless you want to do all restoring of state yourself. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onSaveInstanceState()()` Saves the state of the dialog into a bundle. The default implementation saves the state of its view hierarchy, so you'll likely want to call through to super if you override this to save additional state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onSearchRequested()()` This hook is called when the user signals the desire to start a search. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onSearchRequested(android.view.SearchEvent)(searchEvent: https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#)` This hook is called when the user signals the desire to start a search. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onStart()()` Called when the dialog is starting. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onStop()()` Called to tell you that you're stopping. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onTouchEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)` Called when a touch screen event was not handled by any of the views under it. This is most useful to process touch events that happen outside of your window bounds, where there is no view to receive it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onTrackballEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)` Called when the trackball was moved and not handled by any of the views inside of the activity. So, for example, if the trackball moves while focus is on a button, you will receive a call here because buttons do not normally do anything with trackball events. The call here happens *before* trackball movements are converted to DPAD key events, which then get sent back to the view hierarchy, and will be processed at the point for things like focus navigation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onWindowAttributesChanged(android.view.WindowManager.LayoutParams)(params: https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#!)` This is called whenever the current window attributes change. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onWindowFocusChanged(kotlin.Boolean)(hasFocus: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` This hook is called whenever the window focus changes. See `https://developer.android.com/reference/kotlin/android/view/View.html#onWindowFocusChanged(kotlin.Boolean)` for more information. <br /> | | `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#?` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onWindowStartingActionMode(android.view.ActionMode.Callback)(callback: https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#!)` Called when an action mode is being started for this window. Gives the callback an opportunity to handle the action mode in its own unique and beautiful way. If this method returns null the system can choose a way to present the mode or choose not to start the mode at all. This is equivalent to `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onWindowStartingActionMode(android.view.ActionMode.Callback,%20kotlin.Int)` with type `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#TYPE_PRIMARY:kotlin.Int`. <br /> | | `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#?` | `https://developer.android.com/reference/kotlin/android/app/Dialog#onWindowStartingActionMode(android.view.ActionMode.Callback,%20kotlin.Int)(callback: https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#!, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when an action mode is being started for this window. Gives the callback an opportunity to handle the action mode in its own unique and beautiful way. If this method returns null the system can choose a way to present the mode or choose not to start the mode at all. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#openContextMenu(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#openOptionsMenu()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#registerForContextMenu(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#requestWindowFeature(kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Enable extended window features. This is a convenience for calling `https://developer.android.com/reference/kotlin/android/view/Window.html#requestFeature(kotlin.Int)`. <br /> | | `T` | `https://developer.android.com/reference/kotlin/android/app/Dialog#requireViewById(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Finds the first descendant view with the given ID or throws an IllegalArgumentException if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via `https://developer.android.com/reference/kotlin/android/app/Dialog#show()` or `https://developer.android.com/reference/kotlin/android/app/Dialog#create()`). **Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setCancelMessage(android.os.Message)(msg: https://developer.android.com/reference/kotlin/android/os/Message.html#?)` Set a message to be sent when the dialog is canceled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setCancelable(kotlin.Boolean)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this dialog is cancelable with the `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setCanceledOnTouchOutside(kotlin.Boolean)(cancel: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this dialog is canceled when touched outside the window's bounds. If setting to true, the dialog is set to be cancelable if not already set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setContentView(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#)` Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)(view: https://developer.android.com/reference/kotlin/android/view/View.html#, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#?)` Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setContentView(kotlin.Int)(layoutResID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the screen content from a layout resource. The resource will be inflated, adding all top-level views to the screen. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setDismissMessage(android.os.Message)(msg: https://developer.android.com/reference/kotlin/android/os/Message.html#?)` Set a message to be sent when the dialog is dismissed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setFeatureDrawable(kotlin.Int,%20android.graphics.drawable.Drawable)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?)` Convenience for calling `https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawable(kotlin.Int,%20android.graphics.drawable.Drawable)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setFeatureDrawableAlpha(kotlin.Int,%20kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, alpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Convenience for calling `https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableAlpha(kotlin.Int,%20kotlin.Int)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setFeatureDrawableResource(kotlin.Int,%20kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Convenience for calling `https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableResource(kotlin.Int,%20kotlin.Int)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setFeatureDrawableUri(kotlin.Int,%20android.net.Uri)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?)` Convenience for calling `https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableUri(kotlin.Int,%20android.net.Uri)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setOnCancelListener(android.content.DialogInterface.OnCancelListener)(listener: https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#?)` Set a listener to be invoked when the dialog is canceled. This will only be invoked when the dialog is canceled. Cancel events alone will not capture all ways that the dialog might be dismissed. If the creator needs to know when a dialog is dismissed in general, use `https://developer.android.com/reference/kotlin/android/app/Dialog#setOnDismissListener(android.content.DialogInterface.OnDismissListener)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setOnDismissListener(android.content.DialogInterface.OnDismissListener)(listener: https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnDismissListener.html#?)` Set a listener to be invoked when the dialog is dismissed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setOnKeyListener(android.content.DialogInterface.OnKeyListener)(onKeyListener: https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnKeyListener.html#?)` Sets the callback that will be called if a key is dispatched to the dialog. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setOnShowListener(android.content.DialogInterface.OnShowListener)(listener: https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnShowListener.html#?)` Sets a listener to be invoked when the dialog is shown. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setOwnerActivity(android.app.Activity)(activity: https://developer.android.com/reference/kotlin/android/app/Activity)` Sets the Activity that owns this dialog. An example use: This Dialog will use the suggested volume control stream of the Activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setTitle(kotlin.Int)(titleId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the title text for this dialog's window. The text is retrieved from the resources with the supplied identifier. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#setVolumeControlStream(kotlin.Int)(streamType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` By default, this will use the owner Activity's suggested stream type. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#show()()` Start the dialog and display it on screen. The window is placed in the application layer and opaque. Note that you should not override this method to do initialization when the dialog is shown, instead implement that in `https://developer.android.com/reference/kotlin/android/app/Dialog#onStart()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#takeKeyEvents(kotlin.Boolean)(get: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Request that key events come to this dialog. Use this if your dialog has no views with focus, but the dialog still wants a chance to process key events. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/app/Dialog#unregisterForContextMenu(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#)` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onPointerCaptureChanged(kotlin.Boolean)(hasCapture: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when pointer capture is enabled or disabled for the current window. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onProvideKeyboardShortcuts(kotlin.collections.MutableList,%20android.view.Menu,%20kotlin.Int)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutGroup.html#!>!, menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#?, deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when Keyboard Shortcuts are requested for the current window. <br /> | ||

## Constants

### THEME_DEVICE_DEFAULT_DARK

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THEME_DEVICE_DEFAULT_DARK: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_DeviceDefault_Dialog_Alert:kotlin.Int`.*

Special theme constant for `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)`: use the device's default alert theme with a dark background.

 Value: 4

### THEME_DEVICE_DEFAULT_LIGHT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THEME_DEVICE_DEFAULT_LIGHT: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_DeviceDefault_Light_Dialog_Alert:kotlin.Int`.*

Special theme constant for `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)`: use the device's default alert theme with a light background.

 Value: 5

### THEME_HOLO_DARK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THEME_HOLO_DARK: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_Material_Dialog_Alert:kotlin.Int`.*

Special theme constant for `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)`: use the holographic alert theme with a dark background.

 Value: 2

### THEME_HOLO_LIGHT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THEME_HOLO_LIGHT: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_Material_Light_Dialog_Alert:kotlin.Int`.*

Special theme constant for `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)`: use the holographic alert theme with a light background.

 Value: 3

### THEME_TRADITIONAL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THEME_TRADITIONAL: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_Material_Dialog_Alert:kotlin.Int`.*

Special theme constant for `https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)`: use the traditional (pre-Holo) alert dialog theme.

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: the parent context |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: the parent context |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: the parent context |
| `themeResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the resource ID of the theme against which to inflate this dialog, or `0` to use the parent `context`'s default alert dialog theme |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_alertDialogTheme:kotlin.Int`

## Public methods

### getButton

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getButton(whichButton: Int): Button!
```

Gets one of the buttons used in the dialog. Returns null if the specified button does not exist or the dialog has not yet been fully created (for example, via `https://developer.android.com/reference/kotlin/android/app/Dialog#show()` or `https://developer.android.com/reference/kotlin/android/app/Dialog#create()`).

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

Default implementation consumes `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` and, as of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_ESCAPE:kotlin.Int` to later handle them in `https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyUp(kotlin.Int,%20android.view.KeyEvent)`.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value in event.getKeyCode(). |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#): This value cannot be `null`. |

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
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#): This value cannot be `null`. |

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
| `listener` | [DialogInterface.OnClickListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#)!: The `https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#` to use. |
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
| `msg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!: The `https://developer.android.com/reference/kotlin/android/os/Message.html#` to be sent when clicked. |
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

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.Int,%20kotlin.CharSequence,%20android.content.DialogInterface.OnClickListener)` with `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int`*

Set a listener to be invoked when button 1 of the dialog is pressed.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to display in button 1. |
| `listener` | [DialogInterface.OnClickListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#)!: The `https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#` to use. |

### setButton

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton(
    text: CharSequence!, 
    msg: Message!
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.Int,%20kotlin.CharSequence,%20android.os.Message)` with `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int`.*

### setButton2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton2(
    text: CharSequence!, 
    listener: DialogInterface.OnClickListener!
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.Int,%20kotlin.CharSequence,%20android.content.DialogInterface.OnClickListener)` with `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEGATIVE:kotlin.Int`*

Set a listener to be invoked when button 2 of the dialog is pressed.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to display in button 2. |
| `listener` | [DialogInterface.OnClickListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#)!: The `https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#` to use. |

### setButton2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton2(
    text: CharSequence!, 
    msg: Message!
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.Int,%20kotlin.CharSequence,%20android.os.Message)` with `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEGATIVE:kotlin.Int`.*

### setButton3

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton3(
    text: CharSequence!, 
    listener: DialogInterface.OnClickListener!
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.Int,%20kotlin.CharSequence,%20android.content.DialogInterface.OnClickListener)` with `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEUTRAL:kotlin.Int`*

Set a listener to be invoked when button 3 of the dialog is pressed.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to display in button 3. |
| `listener` | [DialogInterface.OnClickListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#)!: The `https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#` to use. |

### setButton3

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setButton3(
    text: CharSequence!, 
    msg: Message!
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.Int,%20kotlin.CharSequence,%20android.os.Message)` with `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEUTRAL:kotlin.Int`.*

### setCustomTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCustomTitle(customTitleView: View!): Unit
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/AlertDialog.Builder#setCustomTitle(android.view.View)`

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
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The view to show in the content area of the dialog |
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
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: If this dialog is being reinitialized after a the hosting activity was previously shut down, holds the result from the most recent call to `https://developer.android.com/reference/kotlin/android/app/Dialog#onSaveInstanceState()`, or null if this is the first time. |
