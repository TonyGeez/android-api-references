# ProgressDialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProgressDialog

Kotlin| [Java](https://developer.android.com/reference/android/app/ProgressDialog "View this page in Java") 

```
open class ProgressDialog : AlertDialog
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [android.app.Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog) |||
| | ↳ | [android.app.AlertDialog](https://developer.android.com/reference/kotlin/android/app/AlertDialog) ||
| | | ↳ | [android.app.ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#) |

| **This class was deprecated in API level 26.**
|
| `ProgressDialog`is a modal dialog, which prevents the user from interacting with the app. Instead of using this class, you should use a progress indicator like [android.widget.ProgressBar](https://developer.android.com/reference/kotlin/android/widget/ProgressBar.html#), which can be embedded in your app's UI. Alternatively, you can use a [notification](https://developer.android.com/reference/kotlin/guide/topics/ui/notifiers/notifications.html) to inform the user of the task's progress.

A dialog showing a progress indicator and an optional text message or view. Only a text message or a view can be used at the same time.

The dialog can be made cancelable on back key press.

The progress range is 0 to [max](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#getMax()).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STYLE_HORIZONTAL](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#STYLE_HORIZONTAL:kotlin.Int) Creates a ProgressDialog with a horizontal progress bar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STYLE_SPINNER](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#STYLE_SPINNER:kotlin.Int) Creates a ProgressDialog with a circular, spinning progress bar. |

| Inherited constants ||
|---|---|
| From class [DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON1](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON1:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON2](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON2:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON3](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON3:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEGATIVE](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEGATIVE:kotlin.Int) <br /> The identifier for the negative button. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEUTRAL](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEUTRAL:kotlin.Int) <br /> The identifier for the neutral button. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_POSITIVE](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int) <br /> The identifier for the positive button. <br /> | ||
| From class [AlertDialog](https://developer.android.com/reference/kotlin/android/app/AlertDialog) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THEME_DEVICE_DEFAULT_DARK](https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_DEVICE_DEFAULT_DARK:kotlin.Int) <br /> Special theme constant for [AlertDialog(android.content.Context,int)](https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)): use the device's default alert theme with a dark background. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THEME_DEVICE_DEFAULT_LIGHT](https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_DEVICE_DEFAULT_LIGHT:kotlin.Int) <br /> Special theme constant for [AlertDialog(android.content.Context,int)](https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)): use the device's default alert theme with a light background. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THEME_HOLO_DARK](https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_HOLO_DARK:kotlin.Int) <br /> Special theme constant for [AlertDialog(android.content.Context,int)](https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)): use the holographic alert theme with a dark background. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THEME_HOLO_LIGHT](https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_HOLO_LIGHT:kotlin.Int) <br /> Special theme constant for [AlertDialog(android.content.Context,int)](https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)): use the holographic alert theme with a light background. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THEME_TRADITIONAL](https://developer.android.com/reference/kotlin/android/app/AlertDialog#THEME_TRADITIONAL:kotlin.Int) <br /> Special theme constant for [AlertDialog(android.content.Context,int)](https://developer.android.com/reference/kotlin/android/app/AlertDialog#AlertDialog(android.content.Context,%20kotlin.Int)): use the traditional (pre-Holo) alert dialog theme. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#ProgressDialog(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Creates a Progress dialog. |
| [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#ProgressDialog(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `theme:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a Progress dialog. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMax](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#getMax())`()` Gets the maximum allowed progress value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getProgress](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#getProgress())`()` Gets the current progress. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecondaryProgress](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#getSecondaryProgress())`()` Gets the current secondary progress. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [incrementProgressBy](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#incrementProgressBy(kotlin.Int))`(`diff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increments the current progress value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [incrementSecondaryProgressBy](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#incrementSecondaryProgressBy(kotlin.Int))`(`diff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increments the current secondary progress value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIndeterminate](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#isIndeterminate())`()` Whether this ProgressDialog is in indeterminate mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#onStart())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIndeterminate](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setIndeterminate(kotlin.Boolean))`(`indeterminate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Change the indeterminate mode for this ProgressDialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIndeterminateDrawable](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setIndeterminateDrawable(android.graphics.drawable.Drawable))`(`d:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!`)` Sets the drawable to be used to display the indeterminate progress value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMax](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setMax(kotlin.Int))`(`max:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum allowed progress value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMessage](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setMessage(kotlin.CharSequence))`(`message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProgress](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setProgress(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the current progress. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProgressDrawable](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setProgressDrawable(android.graphics.drawable.Drawable))`(`d:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!`)` Sets the drawable to be used to display the progress value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProgressNumberFormat](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setProgressNumberFormat(kotlin.String))`(`format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Change the format of the small text showing current and maximum units of progress. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProgressPercentFormat](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setProgressPercentFormat(java.text.NumberFormat))`(`format:` ` [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat.html#)!`)` Change the format of the small text showing the percentage of progress. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProgressStyle](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setProgressStyle(kotlin.Int))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the style of this ProgressDialog, either [STYLE_SPINNER](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#STYLE_SPINNER:kotlin.Int) or [STYLE_HORIZONTAL](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#STYLE_HORIZONTAL:kotlin.Int). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSecondaryProgress](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setSecondaryProgress(kotlin.Int))`(`secondaryProgress:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the secondary progress. |
| openstatic [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#)! | [show](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#show(android.content.Context,%20kotlin.CharSequence,%20kotlin.CharSequence))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Creates and shows a ProgressDialog. |
| openstatic [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#)! | [show](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#show(android.content.Context,%20kotlin.CharSequence,%20kotlin.CharSequence,%20kotlin.Boolean))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `indeterminate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates and shows a ProgressDialog. |
| openstatic [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#)! | [show](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#show(android.content.Context,%20kotlin.CharSequence,%20kotlin.CharSequence,%20kotlin.Boolean,%20kotlin.Boolean))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `indeterminate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `cancelable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates and shows a ProgressDialog. |
| openstatic [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#)! | [show](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#show(android.content.Context,%20kotlin.CharSequence,%20kotlin.CharSequence,%20kotlin.Boolean,%20kotlin.Boolean,%20android.content.DialogInterface.OnCancelListener))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `indeterminate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `cancelable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `cancelListener:` ` [DialogInterface.OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#)!`)` Creates and shows a ProgressDialog. |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreate](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#onCreate(android.os.Bundle))`(`savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStop](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#onStop())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog) |------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addContentView](https://developer.android.com/reference/kotlin/android/app/Dialog#addContentView(android.view.View,%20android.view.ViewGroup.LayoutParams))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `params:` ` [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#)?`)` <br /> Add an additional content view to the screen. Added after any existing ones in the screen -- existing views are NOT removed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/app/Dialog#cancel())`()` <br /> Cancel the dialog. This is essentially the same as calling [dismiss()](https://developer.android.com/reference/kotlin/android/app/Dialog#dismiss()), but it will also call your [DialogInterface.OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#)(if registered). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#closeOptionsMenu())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [create](https://developer.android.com/reference/kotlin/android/app/Dialog#create())`()` <br /> Forces immediate creation of the dialog. Note that you should not override this method to perform dialog creation. Rather, override [onCreate(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Dialog#onCreate(android.os.Bundle)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](https://developer.android.com/reference/kotlin/android/app/Dialog#dismiss())`()` <br /> Dismiss this dialog, removing it from the screen. This method can be invoked safely from any thread. Note that you should not override this method to do cleanup when the dialog is dismissed, instead implement that in [onStop](https://developer.android.com/reference/kotlin/android/app/Dialog#onStop()). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchGenericMotionEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchGenericMotionEvent(android.view.MotionEvent))`(`ev:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` <br /> Called to process generic motion events. You can override this to intercept all generic motion events before they are dispatched to the window. Be sure to call this implementation for generic motion events that should be handled normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchKeyEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchKeyEvent(android.view.KeyEvent))`(`event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` <br /> Called to process key events. You can override this to intercept all key events before they are dispatched to the window. Be sure to call this implementation for key events that should be handled normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchKeyShortcutEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchKeyShortcutEvent(android.view.KeyEvent))`(`event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` <br /> Called to process a key shortcut event. You can override this to intercept all key shortcut events before they are dispatched to the window. Be sure to call this implementation for key shortcut events that should be handled normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchPopulateAccessibilityEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchPopulateAccessibilityEvent(android.view.accessibility.AccessibilityEvent))`(`event:` ` [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#)`)` <br /> Called to process population of [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#) s. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchTouchEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchTouchEvent(android.view.MotionEvent))`(`ev:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` <br /> Called to process touch screen events. You can override this to intercept all touch screen events before they are dispatched to the window. Be sure to call this implementation for touch screen events that should be handled normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchTrackballEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchTrackballEvent(android.view.MotionEvent))`(`ev:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` <br /> Called to process trackball events. You can override this to intercept all trackball events before they are dispatched to the window. Be sure to call this implementation for trackball events that should be handled normally. <br /> | | T | [findViewById](https://developer.android.com/reference/kotlin/android/app/Dialog#findViewById(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Finds the first descendant view with the given ID or`null`if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via [show()](https://developer.android.com/reference/kotlin/android/app/Dialog#show())or [create()](https://developer.android.com/reference/kotlin/android/app/Dialog#create())). **Note:**In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary. <br /> | | [ActionBar](https://developer.android.com/reference/kotlin/android/app/ActionBar)? | [getActionBar](https://developer.android.com/reference/kotlin/android/app/Dialog#getActionBar())`()` <br /> Retrieve the [ActionBar](https://developer.android.com/reference/kotlin/android/app/ActionBar) attached to this dialog, if present. <br /> | | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) | [getContext](https://developer.android.com/reference/kotlin/android/app/Dialog#getContext())`()` <br /> Retrieve the Context this Dialog is running in. <br /> | | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | [getCurrentFocus](https://developer.android.com/reference/kotlin/android/app/Dialog#getCurrentFocus())`()` <br /> Call [android.view.Window#getCurrentFocus](https://developer.android.com/reference/kotlin/android/view/Window.html#getCurrentFocus())on the Window if this Activity to return the currently focused view. <br /> | | [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#) | [getLayoutInflater](https://developer.android.com/reference/kotlin/android/app/Dialog#getLayoutInflater())`()` <br /> | | [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#) | [getOnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/app/Dialog#getOnBackInvokedDispatcher())`()` <br /> Returns the [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#) instance associated with the window that this dialog is attached to. <br /> | | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)? | [getOwnerActivity](https://developer.android.com/reference/kotlin/android/app/Dialog#getOwnerActivity())`()` <br /> Returns the Activity that owns this Dialog. For example, if [Activity.showDialog(int)](https://developer.android.com/reference/kotlin/android/app/Activity#showDialog(kotlin.Int))is used to show this Dialog, that Activity will be the owner (by default). Depending on how this dialog was created, this may return null. <br /> | | [SearchEvent](https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#)? | [getSearchEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#getSearchEvent())`()` <br /> During the onSearchRequested() callbacks, this function will return the [SearchEvent](https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#) that triggered the callback, if it exists. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolumeControlStream](https://developer.android.com/reference/kotlin/android/app/Dialog#getVolumeControlStream())`()` <br /> | | [Window](https://developer.android.com/reference/kotlin/android/view/Window.html#)? | [getWindow](https://developer.android.com/reference/kotlin/android/app/Dialog#getWindow())`()` <br /> Retrieve the current Window for the activity. This can be used to directly access parts of the Window API that are not available through Activity/Screen. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hide](https://developer.android.com/reference/kotlin/android/app/Dialog#hide())`()` <br /> Hide the dialog, but do not dismiss it. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#invalidateOptionsMenu())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShowing](https://developer.android.com/reference/kotlin/android/app/Dialog#isShowing())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionModeFinished](https://developer.android.com/reference/kotlin/android/app/Dialog#onActionModeFinished(android.view.ActionMode))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)!`)` <br /> Called when an action mode has been finished. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeFinished(mode). If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionModeStarted](https://developer.android.com/reference/kotlin/android/app/Dialog#onActionModeStarted(android.view.ActionMode))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)!`)` <br /> Called when an action mode has been started. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeStarted(mode). If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToWindow](https://developer.android.com/reference/kotlin/android/app/Dialog#onAttachedToWindow())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBackPressed](https://developer.android.com/reference/kotlin/android/app/Dialog#onBackPressed())`()` <br /> Called when the dialog has detected the user's press of the back key. The default implementation simply cancels the dialog (only if it is cancelable), but you can override this to do whatever you want. If you target version [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int) or later, you should not use this method but register an [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback.html#) on an [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#) that you can retrieve using [getOnBackInvokedDispatcher()](https://developer.android.com/reference/kotlin/android/app/Dialog#getOnBackInvokedDispatcher()). You should also set`android:enableOnBackInvokedCallback="true"`in the application manifest. Alternatively, you can use`androidx.activity.ComponentDialog#getOnBackPressedDispatcher()`for backward compatibility. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](https://developer.android.com/reference/kotlin/android/app/Dialog#onContentChanged())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onContextItemSelected](https://developer.android.com/reference/kotlin/android/app/Dialog#onContextItemSelected(android.view.MenuItem))`(`item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContextMenuClosed](https://developer.android.com/reference/kotlin/android/app/Dialog#onContextMenuClosed(android.view.Menu))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreateContextMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo))`(`menu:` ` [ContextMenu](https://developer.android.com/reference/kotlin/android/view/ContextMenu.html#)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `menuInfo:` ` [ContextMenu.ContextMenuInfo](https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo.html#)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreateOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#onCreateOptionsMenu(android.view.Menu))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> It is usually safe to proxy this call to the owner activity's [Activity.onCreateOptionsMenu(Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onCreateOptionsMenu(android.view.Menu))if the client desires the same menu for this Dialog. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreatePanelMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#onCreatePanelMenu(kotlin.Int,%20android.view.Menu))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> | | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | [onCreatePanelView](https://developer.android.com/reference/kotlin/android/app/Dialog#onCreatePanelView(kotlin.Int))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDetachedFromWindow](https://developer.android.com/reference/kotlin/android/app/Dialog#onDetachedFromWindow())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#onGenericMotionEvent(android.view.MotionEvent))`(`event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` <br /> Called when a generic motion event was not handled by any of the views inside of the dialog. Generic motion events describe joystick movements, mouse hovers, track pad touches, scroll wheel movements and other input events. The [source](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getSource())of the motion event specifies the class of input that was received. Implementations of this method must examine the bits in the source before processing the event. The following code example shows how this is done. Generic motion events with source class [android.view.InputDevice#SOURCE_CLASS_POINTER](https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_CLASS_POINTER:kotlin.Int) are delivered to the view under the pointer. All other generic motion events are delivered to the focused view. See [View.onGenericMotionEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View.html#onGenericMotionEvent(android.view.MotionEvent))for an example of how to handle this event. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyLongPress](https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` <br /> Default implementation of [KeyEvent.Callback.onKeyLongPress()](https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)): always returns false (doesn't handle the event). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyMultiple](https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `repeatCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` <br /> Default implementation of [KeyEvent.Callback.onKeyMultiple()](https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent)): always returns false (doesn't handle the event). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyShortcut](https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyShortcut(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` <br /> Called when a key shortcut event is not handled by any of the views in the Dialog. Override this method to implement global key shortcuts for the Dialog. Key shortcuts can also be implemented by setting the [shortcut](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#setShortcut(kotlin.Char,%20kotlin.Char))property of menu items. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMenuItemSelected](https://developer.android.com/reference/kotlin/android/app/Dialog#onMenuItemSelected(kotlin.Int,%20android.view.MenuItem))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMenuOpened](https://developer.android.com/reference/kotlin/android/app/Dialog#onMenuOpened(kotlin.Int,%20android.view.Menu))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onOptionsItemSelected](https://developer.android.com/reference/kotlin/android/app/Dialog#onOptionsItemSelected(android.view.MenuItem))`(`item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOptionsMenuClosed](https://developer.android.com/reference/kotlin/android/app/Dialog#onOptionsMenuClosed(android.view.Menu))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPanelClosed](https://developer.android.com/reference/kotlin/android/app/Dialog#onPanelClosed(kotlin.Int,%20android.view.Menu))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPrepareOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#onPrepareOptionsMenu(android.view.Menu))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> It is usually safe to proxy this call to the owner activity's [Activity.onPrepareOptionsMenu(Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareOptionsMenu(android.view.Menu))if the client desires the same menu for this Dialog. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPreparePanel](https://developer.android.com/reference/kotlin/android/app/Dialog#onPreparePanel(kotlin.Int,%20android.view.View,%20android.view.Menu))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)?`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestoreInstanceState](https://developer.android.com/reference/kotlin/android/app/Dialog#onRestoreInstanceState(android.os.Bundle))`(`savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` <br /> Restore the state of the dialog from a previously saved bundle. The default implementation restores the state of the dialog's view hierarchy that was saved in the default implementation of [onSaveInstanceState()](https://developer.android.com/reference/kotlin/android/app/Dialog#onSaveInstanceState()), so be sure to call through to super when overriding unless you want to do all restoring of state yourself. <br /> | | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [onSaveInstanceState](https://developer.android.com/reference/kotlin/android/app/Dialog#onSaveInstanceState())`()` <br /> Saves the state of the dialog into a bundle. The default implementation saves the state of its view hierarchy, so you'll likely want to call through to super if you override this to save additional state. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSearchRequested](https://developer.android.com/reference/kotlin/android/app/Dialog#onSearchRequested())`()` <br /> This hook is called when the user signals the desire to start a search. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSearchRequested](https://developer.android.com/reference/kotlin/android/app/Dialog#onSearchRequested(android.view.SearchEvent))`(`searchEvent:` ` [SearchEvent](https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#)`)` <br /> This hook is called when the user signals the desire to start a search. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](https://developer.android.com/reference/kotlin/android/app/Dialog#onStart())`()` <br /> Called when the dialog is starting. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStop](https://developer.android.com/reference/kotlin/android/app/Dialog#onStop())`()` <br /> Called to tell you that you're stopping. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#onTouchEvent(android.view.MotionEvent))`(`event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` <br /> Called when a touch screen event was not handled by any of the views under it. This is most useful to process touch events that happen outside of your window bounds, where there is no view to receive it. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTrackballEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#onTrackballEvent(android.view.MotionEvent))`(`event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` <br /> Called when the trackball was moved and not handled by any of the views inside of the activity. So, for example, if the trackball moves while focus is on a button, you will receive a call here because buttons do not normally do anything with trackball events. The call here happens*before*trackball movements are converted to DPAD key events, which then get sent back to the view hierarchy, and will be processed at the point for things like focus navigation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowAttributesChanged](https://developer.android.com/reference/kotlin/android/app/Dialog#onWindowAttributesChanged(android.view.WindowManager.LayoutParams))`(`params:` ` [WindowManager.LayoutParams](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowFocusChanged](https://developer.android.com/reference/kotlin/android/app/Dialog#onWindowFocusChanged(kotlin.Boolean))`(`hasFocus:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)? | [onWindowStartingActionMode](https://developer.android.com/reference/kotlin/android/app/Dialog#onWindowStartingActionMode(android.view.ActionMode.Callback))`(`callback:` ` [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#)!`)` <br /> | | [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)? | [onWindowStartingActionMode](https://developer.android.com/reference/kotlin/android/app/Dialog#onWindowStartingActionMode(android.view.ActionMode.Callback,%20kotlin.Int))`(`callback:` ` [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#)!`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openContextMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#openContextMenu(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#openOptionsMenu())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerForContextMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#registerForContextMenu(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requestWindowFeature](https://developer.android.com/reference/kotlin/android/app/Dialog#requestWindowFeature(kotlin.Int))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Enable extended window features. This is a convenience for calling [getWindow().requestFeature()](https://developer.android.com/reference/kotlin/android/view/Window.html#requestFeature(kotlin.Int)). <br /> | | T | [requireViewById](https://developer.android.com/reference/kotlin/android/app/Dialog#requireViewById(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Finds the first descendant view with the given ID or throws an IllegalArgumentException if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via [show()](https://developer.android.com/reference/kotlin/android/app/Dialog#show())or [create()](https://developer.android.com/reference/kotlin/android/app/Dialog#create())). **Note:**In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCancelMessage](https://developer.android.com/reference/kotlin/android/app/Dialog#setCancelMessage(android.os.Message))`(`msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)?`)` <br /> Set a message to be sent when the dialog is canceled. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCancelable](https://developer.android.com/reference/kotlin/android/app/Dialog#setCancelable(kotlin.Boolean))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this dialog is cancelable with the [BACK](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int) key. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCanceledOnTouchOutside](https://developer.android.com/reference/kotlin/android/app/Dialog#setCanceledOnTouchOutside(kotlin.Boolean))`(`cancel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this dialog is canceled when touched outside the window's bounds. If setting to true, the dialog is set to be cancelable if not already set. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](https://developer.android.com/reference/kotlin/android/app/Dialog#setContentView(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` <br /> Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](https://developer.android.com/reference/kotlin/android/app/Dialog#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `params:` ` [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#)?`)` <br /> Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](https://developer.android.com/reference/kotlin/android/app/Dialog#setContentView(kotlin.Int))`(`layoutResID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the screen content from a layout resource. The resource will be inflated, adding all top-level views to the screen. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDismissMessage](https://developer.android.com/reference/kotlin/android/app/Dialog#setDismissMessage(android.os.Message))`(`msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)?`)` <br /> Set a message to be sent when the dialog is dismissed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawable](https://developer.android.com/reference/kotlin/android/app/Dialog#setFeatureDrawable(kotlin.Int,%20android.graphics.drawable.Drawable))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `drawable:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)?`)` <br /> Convenience for calling [android.view.Window#setFeatureDrawable(int, Drawable)](https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawable(kotlin.Int,%20android.graphics.drawable.Drawable)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawableAlpha](https://developer.android.com/reference/kotlin/android/app/Dialog#setFeatureDrawableAlpha(kotlin.Int,%20kotlin.Int))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Convenience for calling [android.view.Window#setFeatureDrawableAlpha](https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableAlpha(kotlin.Int,%20kotlin.Int)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawableResource](https://developer.android.com/reference/kotlin/android/app/Dialog#setFeatureDrawableResource(kotlin.Int,%20kotlin.Int))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Convenience for calling [android.view.Window#setFeatureDrawableResource](https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableResource(kotlin.Int,%20kotlin.Int)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawableUri](https://developer.android.com/reference/kotlin/android/app/Dialog#setFeatureDrawableUri(kotlin.Int,%20android.net.Uri))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?`)` <br /> Convenience for calling [android.view.Window#setFeatureDrawableUri](https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableUri(kotlin.Int,%20android.net.Uri)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnCancelListener](https://developer.android.com/reference/kotlin/android/app/Dialog#setOnCancelListener(android.content.DialogInterface.OnCancelListener))`(`listener:` ` [DialogInterface.OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#)?`)` <br /> Set a listener to be invoked when the dialog is canceled. This will only be invoked when the dialog is canceled. Cancel events alone will not capture all ways that the dialog might be dismissed. If the creator needs to know when a dialog is dismissed in general, use [setOnDismissListener](https://developer.android.com/reference/kotlin/android/app/Dialog#setOnDismissListener(android.content.DialogInterface.OnDismissListener)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDismissListener](https://developer.android.com/reference/kotlin/android/app/Dialog#setOnDismissListener(android.content.DialogInterface.OnDismissListener))`(`listener:` ` [DialogInterface.OnDismissListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnDismissListener.html#)?`)` <br /> Set a listener to be invoked when the dialog is dismissed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnKeyListener](https://developer.android.com/reference/kotlin/android/app/Dialog#setOnKeyListener(android.content.DialogInterface.OnKeyListener))`(`onKeyListener:` ` [DialogInterface.OnKeyListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnKeyListener.html#)?`)` <br /> Sets the callback that will be called if a key is dispatched to the dialog. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnShowListener](https://developer.android.com/reference/kotlin/android/app/Dialog#setOnShowListener(android.content.DialogInterface.OnShowListener))`(`listener:` ` [DialogInterface.OnShowListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnShowListener.html#)?`)` <br /> Sets a listener to be invoked when the dialog is shown. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOwnerActivity](https://developer.android.com/reference/kotlin/android/app/Dialog#setOwnerActivity(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` <br /> Sets the Activity that owns this dialog. An example use: This Dialog will use the suggested volume control stream of the Activity. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](https://developer.android.com/reference/kotlin/android/app/Dialog#setTitle(kotlin.Int))`(`titleId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the title text for this dialog's window. The text is retrieved from the resources with the supplied identifier. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVolumeControlStream](https://developer.android.com/reference/kotlin/android/app/Dialog#setVolumeControlStream(kotlin.Int))`(`streamType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> By default, this will use the owner Activity's suggested stream type. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](https://developer.android.com/reference/kotlin/android/app/Dialog#show())`()` <br /> Start the dialog and display it on screen. The window is placed in the application layer and opaque. Note that you should not override this method to do initialization when the dialog is shown, instead implement that in [onStart](https://developer.android.com/reference/kotlin/android/app/Dialog#onStart()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [takeKeyEvents](https://developer.android.com/reference/kotlin/android/app/Dialog#takeKeyEvents(kotlin.Boolean))`(`get:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Request that key events come to this dialog. Use this if your dialog has no views with focus, but the dialog still wants a chance to process key events. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterForContextMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#unregisterForContextMenu(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` <br /> | ||
| From class [AlertDialog](https://developer.android.com/reference/kotlin/android/app/AlertDialog) |-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Button](https://developer.android.com/reference/kotlin/android/widget/Button.html#)! | [getButton](https://developer.android.com/reference/kotlin/android/app/AlertDialog#getButton(kotlin.Int))`(`whichButton:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets one of the buttons used in the dialog. Returns null if the specified button does not exist or the dialog has not yet been fully created (for example, via [show()](https://developer.android.com/reference/kotlin/android/app/Dialog#show())or [create()](https://developer.android.com/reference/kotlin/android/app/Dialog#create())). <br /> | | [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#)! | [getListView](https://developer.android.com/reference/kotlin/android/app/AlertDialog#getListView())`()` <br /> Gets the list view used in the dialog. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](https://developer.android.com/reference/kotlin/android/app/AlertDialog#onKeyDown(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](https://developer.android.com/reference/kotlin/android/app/AlertDialog#onKeyUp(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.Int,%20kotlin.CharSequence,%20android.content.DialogInterface.OnClickListener))`(`whichButton:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `listener:` ` [DialogInterface.OnClickListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#)!`)` <br /> Set a listener to be invoked when the specified button of the dialog is pressed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.Int,%20kotlin.CharSequence,%20android.os.Message))`(`whichButton:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!`)` <br /> Set a message to be sent when a button is pressed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.CharSequence,%20android.content.DialogInterface.OnClickListener))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `listener:` ` [DialogInterface.OnClickListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#)!`)` <br /> Set a listener to be invoked when button 1 of the dialog is pressed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton(kotlin.CharSequence,%20android.os.Message))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton2](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton2(kotlin.CharSequence,%20android.content.DialogInterface.OnClickListener))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `listener:` ` [DialogInterface.OnClickListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#)!`)` <br /> Set a listener to be invoked when button 2 of the dialog is pressed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton2](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton2(kotlin.CharSequence,%20android.os.Message))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton3](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton3(kotlin.CharSequence,%20android.content.DialogInterface.OnClickListener))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `listener:` ` [DialogInterface.OnClickListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#)!`)` <br /> Set a listener to be invoked when button 3 of the dialog is pressed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setButton3](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setButton3(kotlin.CharSequence,%20android.os.Message))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCustomTitle](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setCustomTitle(android.view.View))`(`customTitleView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setIcon(android.graphics.drawable.Drawable))`(`icon:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setIcon(kotlin.Int))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set resId to 0 if you don't want an icon. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIconAttribute](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setIconAttribute(kotlin.Int))`(`attrId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set an icon as supplied by a theme attribute. e.g. android.R.attr.alertDialogIcon <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInverseBackgroundForced](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setInverseBackgroundForced(kotlin.Boolean))`(`forceInverseBackground:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setTitle(kotlin.CharSequence))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setView](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setView(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` <br /> Set the view to display in that dialog. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setView](https://developer.android.com/reference/kotlin/android/app/AlertDialog#setView(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `viewSpacingLeft:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `viewSpacingTop:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `viewSpacingRight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `viewSpacingBottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the view to display in that dialog, specifying the spacing to appear around that view. <br /> | ||
| From class [Callback](https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPointerCaptureChanged](https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onPointerCaptureChanged(kotlin.Boolean))`(`hasCapture:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Called when pointer capture is enabled or disabled for the current window. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProvideKeyboardShortcuts](https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onProvideKeyboardShortcuts(kotlin.collections.MutableList,%20android.view.Menu,%20kotlin.Int))`(`data:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [KeyboardShortcutGroup](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutGroup.html#)!>!`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)?`, `deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when Keyboard Shortcuts are requested for the current window. <br /> | ||

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the parent context |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the parent context |
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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current progress, a value between 0 and [getMax()](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#getMax()) |

### getSecondaryProgress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSecondaryProgress(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the current secondary progress.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current secondary progress, a value between 0 and [getMax()](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#getMax()) |

### incrementProgressBy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun incrementProgressBy(diff: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Increments the current progress value.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `diff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount by which the current progress will be incremented, up to [getMax()](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#getMax()) |

### incrementSecondaryProgressBy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun incrementSecondaryProgressBy(diff: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Increments the current secondary progress value.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `diff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount by which the current secondary progress will be incremented, up to [getMax()](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#getMax()) |

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

**Note:** A ProgressDialog with style [STYLE_SPINNER](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#STYLE_SPINNER:kotlin.Int) is always indeterminate and will ignore this setting.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `indeterminate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to enable indeterminate mode, false otherwise |

**See Also**

- [#setProgressStyle(int)](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setProgressStyle(kotlin.Int)) 

### setIndeterminateDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIndeterminateDrawable(d: Drawable!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the drawable to be used to display the indeterminate progress value.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------|
| `d` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!:the drawable to be used |

**See Also**

- [android.widget.ProgressBar#setProgressDrawable(Drawable)](https://developer.android.com/reference/kotlin/android/widget/ProgressBar.html#setProgressDrawable(android.graphics.drawable.Drawable))
- [#setIndeterminate(boolean)](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setIndeterminate(kotlin.Boolean)) 

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
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current progress, a value between 0 and [getMax()](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#getMax()) |

**See Also**

- [android.widget.ProgressBar#setProgress(int)](https://developer.android.com/reference/kotlin/android/widget/ProgressBar.html#setProgress(kotlin.Int)) 

### setProgressDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProgressDrawable(d: Drawable!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the drawable to be used to display the progress value.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------|
| `d` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!:the drawable to be used |

**See Also**

- [android.widget.ProgressBar#setProgressDrawable(Drawable)](https://developer.android.com/reference/kotlin/android/widget/ProgressBar.html#setProgressDrawable(android.graphics.drawable.Drawable)) 

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

Change the format of the small text showing the percentage of progress. The default is [NumberFormat.getPercentageInstnace().](https://developer.android.com/reference/kotlin/java/text/NumberFormat.html#getPercentInstance())Should not be called during the number is progressing.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat.html#)!:An instance of a [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat.html#) to generate the percentage text. If null, nothing will be shown. |

### setProgressStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProgressStyle(style: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the style of this ProgressDialog, either [STYLE_SPINNER](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#STYLE_SPINNER:kotlin.Int) or [STYLE_HORIZONTAL](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#STYLE_HORIZONTAL:kotlin.Int). The default is [STYLE_SPINNER](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#STYLE_SPINNER:kotlin.Int).

**Note:** A ProgressDialog with style [STYLE_SPINNER](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#STYLE_SPINNER:kotlin.Int) is always indeterminate and will ignore the [indeterminate](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setIndeterminate(kotlin.Boolean))setting.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the style of this ProgressDialog, either [STYLE_SPINNER](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#STYLE_SPINNER:kotlin.Int) or [STYLE_HORIZONTAL](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#STYLE_HORIZONTAL:kotlin.Int) |

### setSecondaryProgress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSecondaryProgress(secondaryProgress: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the secondary progress.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `secondaryProgress` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current secondary progress, a value between 0 and [getMax()](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#getMax()) |

**See Also**

- [android.widget.ProgressBar#setSecondaryProgress(int)](https://developer.android.com/reference/kotlin/android/widget/ProgressBar.html#setSecondaryProgress(kotlin.Int)) 

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the parent context |
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the title text for the dialog's window |
| `message` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to be displayed in the dialog |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------|
| [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#)! | the ProgressDialog |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the parent context |
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the title text for the dialog's window |
| `message` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to be displayed in the dialog |
| `indeterminate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the dialog should be [indeterminate](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setIndeterminate(kotlin.Boolean)), false otherwise |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------|
| [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#)! | the ProgressDialog |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the parent context |
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the title text for the dialog's window |
| `message` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to be displayed in the dialog |
| `indeterminate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the dialog should be [indeterminate](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setIndeterminate(kotlin.Boolean)), false otherwise |
| `cancelable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the dialog is [cancelable](https://developer.android.com/reference/kotlin/android/app/Dialog#setCancelable(kotlin.Boolean)), false otherwise |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------|
| [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#)! | the ProgressDialog |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the parent context |
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the title text for the dialog's window |
| `message` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to be displayed in the dialog |
| `indeterminate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the dialog should be [indeterminate](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#setIndeterminate(kotlin.Boolean)), false otherwise |
| `cancelable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the dialog is [cancelable](https://developer.android.com/reference/kotlin/android/app/Dialog#setCancelable(kotlin.Boolean)), false otherwise |
| `cancelListener` | [DialogInterface.OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#)!:the [listener](https://developer.android.com/reference/kotlin/android/app/Dialog#setOnCancelListener(android.content.DialogInterface.OnCancelListener))to be invoked when the dialog is canceled |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------|
| [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog#)! | the ProgressDialog |

## Protected methods

### onCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onCreate(savedInstanceState: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:If this dialog is being reinitialized after a the hosting activity was previously shut down, holds the result from the most recent call to [onSaveInstanceState](https://developer.android.com/reference/kotlin/android/app/Dialog#onSaveInstanceState()), or null if this is the first time. |

### onStop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStop(): Unit
```

**Deprecated:** *Deprecated in Java.*
