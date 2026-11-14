# Dialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Dialog

Kotlin| [Java](https://developer.android.com/reference/android/app/Dialog "View this page in Java") 

```
open class Dialog : DialogInterface, KeyEvent.Callback, View.OnCreateContextMenuListener, Window.Callback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog#) |

| Known Direct Subclasses [AlertDialog](https://developer.android.com/reference/kotlin/android/app/AlertDialog), [CharacterPickerDialog](https://developer.android.com/reference/kotlin/android/text/method/CharacterPickerDialog.html#), [Presentation](https://developer.android.com/reference/kotlin/android/app/Presentation) |-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------| | [AlertDialog](https://developer.android.com/reference/kotlin/android/app/AlertDialog) | A subclass of Dialog that can display one, two or three buttons. | | [CharacterPickerDialog](https://developer.android.com/reference/kotlin/android/text/method/CharacterPickerDialog.html#) | Dialog for choosing accented characters related to a base character. | | [Presentation](https://developer.android.com/reference/kotlin/android/app/Presentation) | Base class for presentations. | |

| Known Indirect Subclasses [DatePickerDialog](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog), [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog), [TimePickerDialog](https://developer.android.com/reference/kotlin/android/app/TimePickerDialog) |-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------| | [DatePickerDialog](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog) | A simple dialog containing an [android.widget.DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#). | | [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog) | A dialog showing a progress indicator and an optional text message or view. | | [TimePickerDialog](https://developer.android.com/reference/kotlin/android/app/TimePickerDialog) | A dialog that prompts the user for the time of day using a [TimePicker](https://developer.android.com/reference/kotlin/android/widget/TimePicker.html#). | |

Base class for Dialogs.

Note: Activities provide a facility to manage the creation, saving and restoring of dialogs. See [Activity.onCreateDialog(int)](https://developer.android.com/reference/kotlin/android/app/Activity#onCreateDialog(kotlin.Int)), [Activity.onPrepareDialog(int, Dialog)](https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareDialog(kotlin.Int,%20android.app.Dialog)), [Activity.showDialog(int)](https://developer.android.com/reference/kotlin/android/app/Activity#showDialog(kotlin.Int)), and [Activity.dismissDialog(int)](https://developer.android.com/reference/kotlin/android/app/Activity#dismissDialog(kotlin.Int)). If these methods are used, [getOwnerActivity()](https://developer.android.com/reference/kotlin/android/app/Dialog#getOwnerActivity())will return the Activity that managed this dialog.

Often you will want to have a Dialog display on top of the current input method, because there is no reason for it to accept text. You can do this by setting the [WindowManager.LayoutParams.FLAG_ALT_FOCUSABLE_IM](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_ALT_FOCUSABLE_IM:kotlin.Int) window flag (assuming your Dialog takes input focus, as it the default) with the following code: 

```kotlin
getWindow().setFlags(WindowManager.LayoutParams.FLAG_ALT_FOCUSABLE_IM,
          WindowManager.LayoutParams.FLAG_ALT_FOCUSABLE_IM);
```
|
| ### Developer Guides
|
| For more information about creating dialogs, read the [Dialogs](https://developer.android.com/guide/topics/ui/dialogs.html) developer guide.

## Summary

| Inherited constants ||
|---|---|
| From class [DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON1](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON1:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON2](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON2:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON3](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON3:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEGATIVE](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEGATIVE:kotlin.Int) <br /> The identifier for the negative button. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEUTRAL](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEUTRAL:kotlin.Int) <br /> The identifier for the neutral button. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_POSITIVE](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int) <br /> The identifier for the positive button. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog#Dialog(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`)` Creates a dialog window that uses the default dialog theme. |
| [Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog#Dialog(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `themeResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a dialog window that uses a custom dialog style. |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog#Dialog(android.content.Context,%20kotlin.Boolean,%20android.content.DialogInterface.OnCancelListener))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `cancelable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `cancelListener:` ` [DialogInterface.OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#)?`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addContentView](https://developer.android.com/reference/kotlin/android/app/Dialog#addContentView(android.view.View,%20android.view.ViewGroup.LayoutParams))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `params:` ` [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#)?`)` Add an additional content view to the screen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/app/Dialog#cancel())`()` Cancel the dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#closeOptionsMenu())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [create](https://developer.android.com/reference/kotlin/android/app/Dialog#create())`()` Forces immediate creation of the dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](https://developer.android.com/reference/kotlin/android/app/Dialog#dismiss())`()` Dismiss this dialog, removing it from the screen. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchGenericMotionEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchGenericMotionEvent(android.view.MotionEvent))`(`ev:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` Called to process generic motion events. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchKeyEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchKeyEvent(android.view.KeyEvent))`(`event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` Called to process key events. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchKeyShortcutEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchKeyShortcutEvent(android.view.KeyEvent))`(`event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` Called to process a key shortcut event. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchPopulateAccessibilityEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchPopulateAccessibilityEvent(android.view.accessibility.AccessibilityEvent))`(`event:` ` [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#)`)` Called to process population of [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#) s. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchTouchEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchTouchEvent(android.view.MotionEvent))`(`ev:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` Called to process touch screen events. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchTrackballEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#dispatchTrackballEvent(android.view.MotionEvent))`(`ev:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` Called to process trackball events. |
| openT | [findViewById](https://developer.android.com/reference/kotlin/android/app/Dialog#findViewById(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Finds the first descendant view with the given ID or`null`if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via [show()](https://developer.android.com/reference/kotlin/android/app/Dialog#show())or [create()](https://developer.android.com/reference/kotlin/android/app/Dialog#create())). |
| open [ActionBar](https://developer.android.com/reference/kotlin/android/app/ActionBar)? | [getActionBar](https://developer.android.com/reference/kotlin/android/app/Dialog#getActionBar())`()` Retrieve the [ActionBar](https://developer.android.com/reference/kotlin/android/app/ActionBar) attached to this dialog, if present. |
| [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) | [getContext](https://developer.android.com/reference/kotlin/android/app/Dialog#getContext())`()` Retrieve the Context this Dialog is running in. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | [getCurrentFocus](https://developer.android.com/reference/kotlin/android/app/Dialog#getCurrentFocus())`()` Call [android.view.Window#getCurrentFocus](https://developer.android.com/reference/kotlin/android/view/Window.html#getCurrentFocus())on the Window if this Activity to return the currently focused view. |
| open [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#) | [getLayoutInflater](https://developer.android.com/reference/kotlin/android/app/Dialog#getLayoutInflater())`()` <br /> |
| open [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#) | [getOnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/app/Dialog#getOnBackInvokedDispatcher())`()` Returns the [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#) instance associated with the window that this dialog is attached to. |
| [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)? | [getOwnerActivity](https://developer.android.com/reference/kotlin/android/app/Dialog#getOwnerActivity())`()` Returns the Activity that owns this Dialog. |
| [SearchEvent](https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#)? | [getSearchEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#getSearchEvent())`()` During the onSearchRequested() callbacks, this function will return the [SearchEvent](https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#) that triggered the callback, if it exists. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolumeControlStream](https://developer.android.com/reference/kotlin/android/app/Dialog#getVolumeControlStream())`()` <br /> |
| open [Window](https://developer.android.com/reference/kotlin/android/view/Window.html#)? | [getWindow](https://developer.android.com/reference/kotlin/android/app/Dialog#getWindow())`()` Retrieve the current Window for the activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hide](https://developer.android.com/reference/kotlin/android/app/Dialog#hide())`()` Hide the dialog, but do not dismiss it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#invalidateOptionsMenu())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShowing](https://developer.android.com/reference/kotlin/android/app/Dialog#isShowing())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionModeFinished](https://developer.android.com/reference/kotlin/android/app/Dialog#onActionModeFinished(android.view.ActionMode))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)!`)` Called when an action mode has been finished. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionModeStarted](https://developer.android.com/reference/kotlin/android/app/Dialog#onActionModeStarted(android.view.ActionMode))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)!`)` Called when an action mode has been started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToWindow](https://developer.android.com/reference/kotlin/android/app/Dialog#onAttachedToWindow())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBackPressed](https://developer.android.com/reference/kotlin/android/app/Dialog#onBackPressed())`()` Called when the dialog has detected the user's press of the back key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](https://developer.android.com/reference/kotlin/android/app/Dialog#onContentChanged())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onContextItemSelected](https://developer.android.com/reference/kotlin/android/app/Dialog#onContextItemSelected(android.view.MenuItem))`(`item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContextMenuClosed](https://developer.android.com/reference/kotlin/android/app/Dialog#onContextMenuClosed(android.view.Menu))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreateContextMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo))`(`menu:` ` [ContextMenu](https://developer.android.com/reference/kotlin/android/view/ContextMenu.html#)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `menuInfo:` ` [ContextMenu.ContextMenuInfo](https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreateOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#onCreateOptionsMenu(android.view.Menu))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` It is usually safe to proxy this call to the owner activity's [Activity.onCreateOptionsMenu(Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onCreateOptionsMenu(android.view.Menu))if the client desires the same menu for this Dialog. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreatePanelMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#onCreatePanelMenu(kotlin.Int,%20android.view.Menu))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | [onCreatePanelView](https://developer.android.com/reference/kotlin/android/app/Dialog#onCreatePanelView(kotlin.Int))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDetachedFromWindow](https://developer.android.com/reference/kotlin/android/app/Dialog#onDetachedFromWindow())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#onGenericMotionEvent(android.view.MotionEvent))`(`event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` Called when a generic motion event was not handled by any of the views inside of the dialog. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyDown(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` A key was pressed down. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyLongPress](https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` Default implementation of [KeyEvent.Callback.onKeyLongPress()](https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)): always returns false (doesn't handle the event). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyMultiple](https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `repeatCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` Default implementation of [KeyEvent.Callback.onKeyMultiple()](https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent)): always returns false (doesn't handle the event). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyShortcut](https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyShortcut(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` Called when a key shortcut event is not handled by any of the views in the Dialog. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyUp(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` A key was released. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMenuItemSelected](https://developer.android.com/reference/kotlin/android/app/Dialog#onMenuItemSelected(kotlin.Int,%20android.view.MenuItem))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMenuOpened](https://developer.android.com/reference/kotlin/android/app/Dialog#onMenuOpened(kotlin.Int,%20android.view.Menu))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onOptionsItemSelected](https://developer.android.com/reference/kotlin/android/app/Dialog#onOptionsItemSelected(android.view.MenuItem))`(`item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOptionsMenuClosed](https://developer.android.com/reference/kotlin/android/app/Dialog#onOptionsMenuClosed(android.view.Menu))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPanelClosed](https://developer.android.com/reference/kotlin/android/app/Dialog#onPanelClosed(kotlin.Int,%20android.view.Menu))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPrepareOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#onPrepareOptionsMenu(android.view.Menu))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` It is usually safe to proxy this call to the owner activity's [Activity.onPrepareOptionsMenu(Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareOptionsMenu(android.view.Menu))if the client desires the same menu for this Dialog. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPreparePanel](https://developer.android.com/reference/kotlin/android/app/Dialog#onPreparePanel(kotlin.Int,%20android.view.View,%20android.view.Menu))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)?`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestoreInstanceState](https://developer.android.com/reference/kotlin/android/app/Dialog#onRestoreInstanceState(android.os.Bundle))`(`savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Restore the state of the dialog from a previously saved bundle. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [onSaveInstanceState](https://developer.android.com/reference/kotlin/android/app/Dialog#onSaveInstanceState())`()` Saves the state of the dialog into a bundle. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSearchRequested](https://developer.android.com/reference/kotlin/android/app/Dialog#onSearchRequested())`()` This hook is called when the user signals the desire to start a search. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSearchRequested](https://developer.android.com/reference/kotlin/android/app/Dialog#onSearchRequested(android.view.SearchEvent))`(`searchEvent:` ` [SearchEvent](https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#)`)` This hook is called when the user signals the desire to start a search. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#onTouchEvent(android.view.MotionEvent))`(`event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` Called when a touch screen event was not handled by any of the views under it. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTrackballEvent](https://developer.android.com/reference/kotlin/android/app/Dialog#onTrackballEvent(android.view.MotionEvent))`(`event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` Called when the trackball was moved and not handled by any of the views inside of the activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowAttributesChanged](https://developer.android.com/reference/kotlin/android/app/Dialog#onWindowAttributesChanged(android.view.WindowManager.LayoutParams))`(`params:` ` [WindowManager.LayoutParams](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowFocusChanged](https://developer.android.com/reference/kotlin/android/app/Dialog#onWindowFocusChanged(kotlin.Boolean))`(`hasFocus:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)? | [onWindowStartingActionMode](https://developer.android.com/reference/kotlin/android/app/Dialog#onWindowStartingActionMode(android.view.ActionMode.Callback))`(`callback:` ` [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#)!`)` <br /> |
| open [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)? | [onWindowStartingActionMode](https://developer.android.com/reference/kotlin/android/app/Dialog#onWindowStartingActionMode(android.view.ActionMode.Callback,%20kotlin.Int))`(`callback:` ` [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#)!`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openContextMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#openContextMenu(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#openOptionsMenu())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerForContextMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#registerForContextMenu(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requestWindowFeature](https://developer.android.com/reference/kotlin/android/app/Dialog#requestWindowFeature(kotlin.Int))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Enable extended window features. |
| T | [requireViewById](https://developer.android.com/reference/kotlin/android/app/Dialog#requireViewById(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Finds the first descendant view with the given ID or throws an IllegalArgumentException if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via [show()](https://developer.android.com/reference/kotlin/android/app/Dialog#show())or [create()](https://developer.android.com/reference/kotlin/android/app/Dialog#create())). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCancelMessage](https://developer.android.com/reference/kotlin/android/app/Dialog#setCancelMessage(android.os.Message))`(`msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)?`)` Set a message to be sent when the dialog is canceled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCancelable](https://developer.android.com/reference/kotlin/android/app/Dialog#setCancelable(kotlin.Boolean))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this dialog is cancelable with the [BACK](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int) key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCanceledOnTouchOutside](https://developer.android.com/reference/kotlin/android/app/Dialog#setCanceledOnTouchOutside(kotlin.Boolean))`(`cancel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this dialog is canceled when touched outside the window's bounds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](https://developer.android.com/reference/kotlin/android/app/Dialog#setContentView(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` Set the screen content to an explicit view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](https://developer.android.com/reference/kotlin/android/app/Dialog#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `params:` ` [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#)?`)` Set the screen content to an explicit view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](https://developer.android.com/reference/kotlin/android/app/Dialog#setContentView(kotlin.Int))`(`layoutResID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the screen content from a layout resource. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDismissMessage](https://developer.android.com/reference/kotlin/android/app/Dialog#setDismissMessage(android.os.Message))`(`msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)?`)` Set a message to be sent when the dialog is dismissed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawable](https://developer.android.com/reference/kotlin/android/app/Dialog#setFeatureDrawable(kotlin.Int,%20android.graphics.drawable.Drawable))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `drawable:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)?`)` Convenience for calling [android.view.Window#setFeatureDrawable(int, Drawable)](https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawable(kotlin.Int,%20android.graphics.drawable.Drawable)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawableAlpha](https://developer.android.com/reference/kotlin/android/app/Dialog#setFeatureDrawableAlpha(kotlin.Int,%20kotlin.Int))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convenience for calling [android.view.Window#setFeatureDrawableAlpha](https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableAlpha(kotlin.Int,%20kotlin.Int)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawableResource](https://developer.android.com/reference/kotlin/android/app/Dialog#setFeatureDrawableResource(kotlin.Int,%20kotlin.Int))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convenience for calling [android.view.Window#setFeatureDrawableResource](https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableResource(kotlin.Int,%20kotlin.Int)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawableUri](https://developer.android.com/reference/kotlin/android/app/Dialog#setFeatureDrawableUri(kotlin.Int,%20android.net.Uri))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?`)` Convenience for calling [android.view.Window#setFeatureDrawableUri](https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableUri(kotlin.Int,%20android.net.Uri)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnCancelListener](https://developer.android.com/reference/kotlin/android/app/Dialog#setOnCancelListener(android.content.DialogInterface.OnCancelListener))`(`listener:` ` [DialogInterface.OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#)?`)` Set a listener to be invoked when the dialog is canceled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDismissListener](https://developer.android.com/reference/kotlin/android/app/Dialog#setOnDismissListener(android.content.DialogInterface.OnDismissListener))`(`listener:` ` [DialogInterface.OnDismissListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnDismissListener.html#)?`)` Set a listener to be invoked when the dialog is dismissed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnKeyListener](https://developer.android.com/reference/kotlin/android/app/Dialog#setOnKeyListener(android.content.DialogInterface.OnKeyListener))`(`onKeyListener:` ` [DialogInterface.OnKeyListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnKeyListener.html#)?`)` Sets the callback that will be called if a key is dispatched to the dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnShowListener](https://developer.android.com/reference/kotlin/android/app/Dialog#setOnShowListener(android.content.DialogInterface.OnShowListener))`(`listener:` ` [DialogInterface.OnShowListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnShowListener.html#)?`)` Sets a listener to be invoked when the dialog is shown. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOwnerActivity](https://developer.android.com/reference/kotlin/android/app/Dialog#setOwnerActivity(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Sets the Activity that owns this dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](https://developer.android.com/reference/kotlin/android/app/Dialog#setTitle(kotlin.Int))`(`titleId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the title text for this dialog's window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](https://developer.android.com/reference/kotlin/android/app/Dialog#setTitle(kotlin.CharSequence))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Set the title text for this dialog's window. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVolumeControlStream](https://developer.android.com/reference/kotlin/android/app/Dialog#setVolumeControlStream(kotlin.Int))`(`streamType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` By default, this will use the owner Activity's suggested stream type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](https://developer.android.com/reference/kotlin/android/app/Dialog#show())`()` Start the dialog and display it on screen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [takeKeyEvents](https://developer.android.com/reference/kotlin/android/app/Dialog#takeKeyEvents(kotlin.Boolean))`(`get:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Request that key events come to this dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterForContextMenu](https://developer.android.com/reference/kotlin/android/app/Dialog#unregisterForContextMenu(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreate](https://developer.android.com/reference/kotlin/android/app/Dialog#onCreate(android.os.Bundle))`(`savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Similar to android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](https://developer.android.com/reference/kotlin/android/app/Dialog#onStart())`()` Called when the dialog is starting. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStop](https://developer.android.com/reference/kotlin/android/app/Dialog#onStop())`()` Called to tell you that you're stopping. |

| Inherited functions ||
|---|---|
| From class [Callback](https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPointerCaptureChanged](https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onPointerCaptureChanged(kotlin.Boolean))`(`hasCapture:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Called when pointer capture is enabled or disabled for the current window. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProvideKeyboardShortcuts](https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onProvideKeyboardShortcuts(kotlin.collections.MutableList,%20android.view.Menu,%20kotlin.Int))`(`data:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [KeyboardShortcutGroup](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutGroup.html#)!>!`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)?`, `deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when Keyboard Shortcuts are requested for the current window. <br /> | ||

## Public constructors

### Dialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Dialog(context: Context)
```

Creates a dialog window that uses the default dialog theme.

The supplied`context`is used to obtain the window manager and base theme used to present the dialog.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):the context in which the dialog should run This value cannot be`null`. |

**See Also**

- [android.R.styleable#Theme_dialogTheme](https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_dialogTheme:kotlin.Int) 

### Dialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Dialog(
    context: Context, 
    themeResId: Int)
```

Creates a dialog window that uses a custom dialog style.

The supplied`context`is used to obtain the window manager and base theme used to present the dialog.

The supplied`theme`is applied on top of the context's theme. See [Style and Theme Resources](https://developer.android.com/guide/topics/resources/available-resources.html#stylesandthemes) for more information about defining and using styles.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):the context in which the dialog should run This value cannot be`null`. |
| `themeResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a style resource describing the theme to use for the window, or`0`to use the default dialog theme |

## Protected constructors

### Dialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Dialog(
    context: Context, 
    cancelable: Boolean, 
    cancelListener: DialogInterface.OnCancelListener?)
```

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):This value cannot be`null`. |
| `cancelListener` | [DialogInterface.OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#)?:This value may be`null`. |

## Public methods

### addContentView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addContentView(
    view: View, 
    params: ViewGroup.LayoutParams?
): Unit
```

Add an additional content view to the screen. Added after any existing ones in the screen -- existing views are NOT removed.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):The desired content to display. This value cannot be`null`. |
| `params` | [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#)?:Layout parameters for the view. This value may be`null`. |

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(): Unit
```

Cancel the dialog. This is essentially the same as calling [dismiss()](https://developer.android.com/reference/kotlin/android/app/Dialog#dismiss()), but it will also call your [DialogInterface.OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#)(if registered). 

### closeOptionsMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun closeOptionsMenu(): Unit
```  
**See Also**

- [android.app.Activity#closeOptionsMenu()](https://developer.android.com/reference/kotlin/android/app/Activity#closeOptionsMenu()) 

### create

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun create(): Unit
```

Forces immediate creation of the dialog.

Note that you should not override this method to perform dialog creation. Rather, override [onCreate(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Dialog#onCreate(android.os.Bundle)). 

### dismiss

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dismiss(): Unit
```

Dismiss this dialog, removing it from the screen. This method can be invoked safely from any thread. Note that you should not override this method to do cleanup when the dialog is dismissed, instead implement that in [onStop](https://developer.android.com/reference/kotlin/android/app/Dialog#onStop()). 

### dispatchGenericMotionEvent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchGenericMotionEvent(ev: MotionEvent): Boolean
```

Called to process generic motion events. You can override this to intercept all generic motion events before they are dispatched to the window. Be sure to call this implementation for generic motion events that should be handled normally.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | The generic motion event. |
| `ev` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#):The generic motion event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Return true if this event was consumed. |

### dispatchKeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchKeyEvent(event: KeyEvent): Boolean
```

Called to process key events. You can override this to intercept all key events before they are dispatched to the window. Be sure to call this implementation for key events that should be handled normally.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#):The key event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Return true if this event was consumed. |

### dispatchKeyShortcutEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchKeyShortcutEvent(event: KeyEvent): Boolean
```

Called to process a key shortcut event. You can override this to intercept all key shortcut events before they are dispatched to the window. Be sure to call this implementation for key shortcut events that should be handled normally.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#):The key shortcut event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this event was consumed. |

### dispatchPopulateAccessibilityEvent

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchPopulateAccessibilityEvent(event: AccessibilityEvent): Boolean
```

Called to process population of [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#) s.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Return true if event population was completed. |

### dispatchTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchTouchEvent(ev: MotionEvent): Boolean
```

Called to process touch screen events. You can override this to intercept all touch screen events before they are dispatched to the window. Be sure to call this implementation for touch screen events that should be handled normally.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | The touch screen event. |
| `ev` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#):The touch screen event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Return true if this event was consumed. |

### dispatchTrackballEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchTrackballEvent(ev: MotionEvent): Boolean
```

Called to process trackball events. You can override this to intercept all trackball events before they are dispatched to the window. Be sure to call this implementation for trackball events that should be handled normally.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | The trackball event. |
| `ev` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#):The trackball event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Return true if this event was consumed. |

### findViewById

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : View!> findViewById(id: Int): T
```

Finds the first descendant view with the given ID or`null`if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via [show()](https://developer.android.com/reference/kotlin/android/app/Dialog#show())or [create()](https://developer.android.com/reference/kotlin/android/app/Dialog#create())).

**Note:**In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ID to search for |

| Return ||
|---|--------------------------------------------------|
| T | a view with given ID if found, or`null`otherwise |

**See Also**

- [android.view.View#findViewById(int)](https://developer.android.com/reference/kotlin/android/view/View.html#findViewById(kotlin.Int))
- [android.app.Dialog#requireViewById(int)](https://developer.android.com/reference/kotlin/android/app/Dialog#requireViewById(kotlin.Int)) 

### getActionBar

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActionBar(): ActionBar?
```

Retrieve the [ActionBar](https://developer.android.com/reference/kotlin/android/app/ActionBar) attached to this dialog, if present.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ActionBar](https://developer.android.com/reference/kotlin/android/app/ActionBar)? | The ActionBar attached to the dialog or null if no ActionBar is present. |

### getContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContext(): Context
```

Retrieve the Context this Dialog is running in.

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) | Context The Context used by the Dialog. This value cannot be`null`. |

### getCurrentFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrentFocus(): View?
```

Call [android.view.Window#getCurrentFocus](https://developer.android.com/reference/kotlin/android/view/Window.html#getCurrentFocus())on the Window if this Activity to return the currently focused view.

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | View The current View with focus or null. |

**See Also**

- [#getWindow](https://developer.android.com/reference/kotlin/android/app/Dialog#getWindow())
- [android.view.Window#getCurrentFocus](https://developer.android.com/reference/kotlin/android/view/Window.html#getCurrentFocus()) 

### getLayoutInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLayoutInflater(): LayoutInflater
```

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------|
| [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#) | This value cannot be`null`. |

### getOnBackInvokedDispatcher

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOnBackInvokedDispatcher(): OnBackInvokedDispatcher
```

Returns the [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#) instance associated with the window that this dialog is attached to.

| Return ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#) | This value cannot be`null`. |

### getOwnerActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOwnerActivity(): Activity?
```

Returns the Activity that owns this Dialog. For example, if [Activity.showDialog(int)](https://developer.android.com/reference/kotlin/android/app/Activity#showDialog(kotlin.Int))is used to show this Dialog, that Activity will be the owner (by default). Depending on how this dialog was created, this may return null.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------|
| [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)? | The Activity that owns this Dialog. |

### getSearchEvent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSearchEvent(): SearchEvent?
```

During the onSearchRequested() callbacks, this function will return the [SearchEvent](https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#) that triggered the callback, if it exists.

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [SearchEvent](https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#)? | SearchEvent The SearchEvent that triggered the #onSearchRequested callback. This value may be`null`. |

### getVolumeControlStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolumeControlStream(): Int
```  
**See Also**

- [android.app.Activity#getVolumeControlStream()](https://developer.android.com/reference/kotlin/android/app/Activity#getVolumeControlStream()) 

### getWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWindow(): Window?
```

Retrieve the current Window for the activity. This can be used to directly access parts of the Window API that are not available through Activity/Screen.

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Window](https://developer.android.com/reference/kotlin/android/view/Window.html#)? | Window The current window, or null if the activity is not visual. |

### hide

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hide(): Unit
```

Hide the dialog, but do not dismiss it. 

### invalidateOptionsMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun invalidateOptionsMenu(): Unit
```  
**See Also**

- [android.app.Activity#invalidateOptionsMenu()](https://developer.android.com/reference/kotlin/android/app/Activity#invalidateOptionsMenu()) 

### isShowing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isShowing(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the dialog is currently showing. |

### onActionModeFinished

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActionModeFinished(mode: ActionMode!): Unit
```

Called when an action mode has been finished. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeFinished(mode). 
If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)!:The mode that was just finished. |

### onActionModeStarted

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActionModeStarted(mode: ActionMode!): Unit
```

Called when an action mode has been started. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeStarted(mode). 
If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)!:The new mode that has just been started. |

### onAttachedToWindow

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAttachedToWindow(): Unit
```  

### onBackPressed

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onBackPressed(): Unit
```

**Deprecated:** *Use [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback.html#) or`androidx.activity.OnBackPressedCallback`to handle back navigation instead.*

*Starting from Android 13 (API level 33), back event handling is moving to an ahead-of-time model and [onBackPressed()](https://developer.android.com/reference/kotlin/android/app/Dialog#onBackPressed())and [KeyEvent.KEYCODE_BACK](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int) should not be used to handle back events (back gesture or back button click). Instead, an [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback.html#) should be registered using [Dialog.getOnBackInvokedDispatcher()](https://developer.android.com/reference/kotlin/android/app/Dialog#getOnBackInvokedDispatcher()) [.registerOnBackInvokedCallback(priority, callback)](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#registerOnBackInvokedCallback(kotlin.Int,%20android.window.OnBackInvokedCallback)).*

<br />

Called when the dialog has detected the user's press of the back key. The default implementation simply cancels the dialog (only if it is cancelable), but you can override this to do whatever you want.

If you target version [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int) or later, you should not use this method but register an [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback.html#) on an [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#) that you can retrieve using [getOnBackInvokedDispatcher()](https://developer.android.com/reference/kotlin/android/app/Dialog#getOnBackInvokedDispatcher()). You should also set`android:enableOnBackInvokedCallback="true"`in the application manifest.

Alternatively, you can use`androidx.activity.ComponentDialog#getOnBackPressedDispatcher()`for backward compatibility. 

### onContentChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onContentChanged(): Unit
```  

### onContextItemSelected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onContextItemSelected(item: MenuItem): Boolean
```

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `item` | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onContextItemSelected(MenuItem)](https://developer.android.com/reference/kotlin/android/app/Activity#onContextItemSelected(android.view.MenuItem)) 

### onContextMenuClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onContextMenuClosed(menu: Menu): Unit
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onContextMenuClosed(Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onContextMenuClosed(android.view.Menu)) 

### onCreateContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateContextMenu(
    menu: ContextMenu!, 
    v: View!, 
    menuInfo: ContextMenu.ContextMenuInfo!
): Unit
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menu` | [ContextMenu](https://developer.android.com/reference/kotlin/android/view/ContextMenu.html#)!:The context menu that is being built |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view for which the context menu is being built |
| `menuInfo` | [ContextMenu.ContextMenuInfo](https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo.html#)!:Extra information about the item for which the context menu should be shown. This information will vary depending on the class of v. |

**See Also**

- [android.app.Activity#onCreateContextMenu(ContextMenu, View, ContextMenuInfo)](https://developer.android.com/reference/kotlin/android/app/Activity#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo)) 

### onCreateOptionsMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateOptionsMenu(menu: Menu): Boolean
```

It is usually safe to proxy this call to the owner activity's [Activity.onCreateOptionsMenu(Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onCreateOptionsMenu(android.view.Menu))if the client desires the same menu for this Dialog.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onCreateOptionsMenu(Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onCreateOptionsMenu(android.view.Menu))
- <https://developer.android.com/reference/kotlin/android/app/Dialog#getOwnerActivity()> 

### onCreatePanelMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreatePanelMenu(
    featureId: Int, 
    menu: Menu
): Boolean
```

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The panel being created. |
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean You must return true for the panel to be displayed; if you return false it will not be shown. |

**See Also**

- [android.app.Activity#onCreatePanelMenu(int, Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onCreatePanelMenu(kotlin.Int,%20android.view.Menu)) 

### onCreatePanelView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreatePanelView(featureId: Int): View?
```

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which panel is being created. |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | view The top-level view to place in the panel. |

**See Also**

- [android.app.Activity#onCreatePanelView(int)](https://developer.android.com/reference/kotlin/android/app/Activity#onCreatePanelView(kotlin.Int)) 

### onDetachedFromWindow

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDetachedFromWindow(): Unit
```  

### onGenericMotionEvent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGenericMotionEvent(event: MotionEvent): Boolean
```

Called when a generic motion event was not handled by any of the views inside of the dialog.

Generic motion events describe joystick movements, mouse hovers, track pad touches, scroll wheel movements and other input events. The [source](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getSource())of the motion event specifies the class of input that was received. Implementations of this method must examine the bits in the source before processing the event. The following code example shows how this is done.

Generic motion events with source class [android.view.InputDevice#SOURCE_CLASS_POINTER](https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_CLASS_POINTER:kotlin.Int) are delivered to the view under the pointer. All other generic motion events are delivered to the focused view.

See [View.onGenericMotionEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View.html#onGenericMotionEvent(android.view.MotionEvent))for an example of how to handle this event.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#):The generic motion event being processed. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Return true if you have consumed the event, false if you haven't. The default implementation always returns false. |

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

Default implementation consumes [KEYCODE_BACK](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int) and, as of [P](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int), [KEYCODE_ESCAPE](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_ESCAPE:kotlin.Int) to later handle them in [onKeyUp](https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyUp(kotlin.Int,%20android.view.KeyEvent)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

**See Also**

- [#onKeyUp](https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyUp(kotlin.Int,%20android.view.KeyEvent))
- [android.view.KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#) 

### onKeyLongPress

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyLongPress(
    keyCode: Int, 
    event: KeyEvent
): Boolean
```

Default implementation of [KeyEvent.Callback.onKeyLongPress()](https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)): always returns false (doesn't handle the event).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyMultiple

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyMultiple(
    keyCode: Int, 
    repeatCount: Int, 
    event: KeyEvent
): Boolean
```

Default implementation of [KeyEvent.Callback.onKeyMultiple()](https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent)): always returns false (doesn't handle the event).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `count` | Number of pairs as returned by event.getRepeatCount(). |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyShortcut

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyShortcut(
    keyCode: Int, 
    event: KeyEvent
): Boolean
```

Called when a key shortcut event is not handled by any of the views in the Dialog. Override this method to implement global key shortcuts for the Dialog. Key shortcuts can also be implemented by setting the [shortcut](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#setShortcut(kotlin.Char,%20kotlin.Char))property of menu items.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#):Description of the key event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the key shortcut was handled. |

### onKeyUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyUp(
    keyCode: Int, 
    event: KeyEvent
): Boolean
```

A key was released.

Default implementation consumes [KEYCODE_BACK](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int) and, as of [P](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int), [KEYCODE_ESCAPE](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_ESCAPE:kotlin.Int) to close the dialog.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

**See Also**

- [#onKeyDown](https://developer.android.com/reference/kotlin/android/app/Dialog#onKeyDown(kotlin.Int,%20android.view.KeyEvent))
- [android.view.KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#) 

### onMenuItemSelected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMenuItemSelected(
    featureId: Int, 
    item: MenuItem
): Boolean
```

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The panel that the menu is in. |
| `item` | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Return true to finish processing of selection, or false to perform the normal menu handling (calling its Runnable or sending a Message to its target Handler). |

**See Also**

- [android.app.Activity#onMenuItemSelected(int, MenuItem)](https://developer.android.com/reference/kotlin/android/app/Activity#onMenuItemSelected(kotlin.Int,%20android.view.MenuItem)) 

### onMenuOpened

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMenuOpened(
    featureId: Int, 
    menu: Menu
): Boolean
```

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The panel that the menu is in. |
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Return true to allow the menu to open, or false to prevent the menu from opening. |

**See Also**

- [android.app.Activity#onMenuOpened(int, Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onMenuOpened(kotlin.Int,%20android.view.Menu)) 

### onOptionsItemSelected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onOptionsItemSelected(item: MenuItem): Boolean
```

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `item` | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onOptionsItemSelected(MenuItem)](https://developer.android.com/reference/kotlin/android/app/Activity#onOptionsItemSelected(android.view.MenuItem)) 

### onOptionsMenuClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onOptionsMenuClosed(menu: Menu): Unit
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onOptionsMenuClosed(Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onOptionsMenuClosed(android.view.Menu)) 

### onPanelClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPanelClosed(
    featureId: Int, 
    menu: Menu
): Unit
```

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The panel that is being displayed. |
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onPanelClosed(int, Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onPanelClosed(kotlin.Int,%20android.view.Menu)) 

### onPrepareOptionsMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPrepareOptionsMenu(menu: Menu): Boolean
```

It is usually safe to proxy this call to the owner activity's [Activity.onPrepareOptionsMenu(Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareOptionsMenu(android.view.Menu))if the client desires the same menu for this Dialog.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onPrepareOptionsMenu(Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareOptionsMenu(android.view.Menu))
- <https://developer.android.com/reference/kotlin/android/app/Dialog#getOwnerActivity()> 

### onPreparePanel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPreparePanel(
    featureId: Int, 
    view: View?, 
    menu: Menu
): Boolean
```

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The panel that is being displayed. |
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)?:This value may be`null`. |
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean You must return true for the panel to be displayed; if you return false it will not be shown. |

**See Also**

- [android.app.Activity#onPreparePanel(int, View, Menu)](https://developer.android.com/reference/kotlin/android/app/Activity#onPreparePanel(kotlin.Int,%20android.view.View,%20android.view.Menu)) 

### onRestoreInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRestoreInstanceState(savedInstanceState: Bundle): Unit
```

Restore the state of the dialog from a previously saved bundle. The default implementation restores the state of the dialog's view hierarchy that was saved in the default implementation of [onSaveInstanceState()](https://developer.android.com/reference/kotlin/android/app/Dialog#onSaveInstanceState()), so be sure to call through to super when overriding unless you want to do all restoring of state yourself.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):The state of the dialog previously saved by [onSaveInstanceState()](https://developer.android.com/reference/kotlin/android/app/Dialog#onSaveInstanceState()). This value cannot be`null`. |

### onSaveInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSaveInstanceState(): Bundle
```

Saves the state of the dialog into a bundle. The default implementation saves the state of its view hierarchy, so you'll likely want to call through to super if you override this to save additional state.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | A bundle with the state of the dialog. This value cannot be`null`. |

### onSearchRequested

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSearchRequested(): Boolean
```

This hook is called when the user signals the desire to start a search.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if search launched, false if activity refuses (blocks) |

### onSearchRequested

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSearchRequested(searchEvent: SearchEvent): Boolean
```

This hook is called when the user signals the desire to start a search.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------|
| `searchEvent` | [SearchEvent](https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if search launched, false if activity refuses (blocks) |

### onTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTouchEvent(event: MotionEvent): Boolean
```

Called when a touch screen event was not handled by any of the views under it. This is most useful to process touch events that happen outside of your window bounds, where there is no view to receive it.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#):The touch screen event being processed. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Return true if you have consumed the event, false if you haven't. The default implementation will cancel the dialog when a touch happens outside of the window bounds. |

### onTrackballEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTrackballEvent(event: MotionEvent): Boolean
```

Called when the trackball was moved and not handled by any of the views inside of the activity. So, for example, if the trackball moves while focus is on a button, you will receive a call here because buttons do not normally do anything with trackball events. The call here happens*before*trackball movements are converted to DPAD key events, which then get sent back to the view hierarchy, and will be processed at the point for things like focus navigation.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#):The trackball event being processed. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Return true if you have consumed the event, false if you haven't. The default implementation always returns false. |

### onWindowAttributesChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onWindowAttributesChanged(params: WindowManager.LayoutParams!): Unit
```  

### onWindowFocusChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onWindowFocusChanged(hasFocus: Boolean): Unit
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `hasFocus` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the window now has focus. |

### onWindowStartingActionMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onWindowStartingActionMode(callback: ActionMode.Callback!): ActionMode?
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#)!:Callback to control the lifecycle of this action mode |

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)? | The ActionMode that was started, or null if the system should present it |

### onWindowStartingActionMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onWindowStartingActionMode(
    callback: ActionMode.Callback!, 
    type: Int
): ActionMode?
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#)!:Callback to control the lifecycle of this action mode |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [ActionMode.TYPE_PRIMARY](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#TYPE_PRIMARY:kotlin.Int) or [ActionMode.TYPE_FLOATING](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#TYPE_FLOATING:kotlin.Int). |

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)? | The ActionMode that was started, or null if the system should present it |

### openContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openContextMenu(view: View): Unit
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):This value cannot be`null`. |

**See Also**

- [android.app.Activity#openContextMenu(View)](https://developer.android.com/reference/kotlin/android/app/Activity#openContextMenu(android.view.View)) 

### openOptionsMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openOptionsMenu(): Unit
```  
**See Also**

- [android.app.Activity#openOptionsMenu()](https://developer.android.com/reference/kotlin/android/app/Activity#openOptionsMenu()) 

### registerForContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerForContextMenu(view: View): Unit
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):This value cannot be`null`. |

**See Also**

- [android.app.Activity#registerForContextMenu(View)](https://developer.android.com/reference/kotlin/android/app/Activity#registerForContextMenu(android.view.View)) 

### requestWindowFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requestWindowFeature(featureId: Int): Boolean
```

Enable extended window features. This is a convenience for calling [getWindow().requestFeature()](https://developer.android.com/reference/kotlin/android/view/Window.html#requestFeature(kotlin.Int)).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired feature as defined in [android.view.Window](https://developer.android.com/reference/kotlin/android/view/Window.html#). |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if the requested feature is supported and now enabled. |

**See Also**

- [android.view.Window#requestFeature](https://developer.android.com/reference/kotlin/android/view/Window.html#requestFeature(kotlin.Int)) 

### requireViewById

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : View!> requireViewById(id: Int): T
```

Finds the first descendant view with the given ID or throws an IllegalArgumentException if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via [show()](https://developer.android.com/reference/kotlin/android/app/Dialog#show())or [create()](https://developer.android.com/reference/kotlin/android/app/Dialog#create())).

**Note:**In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ID to search for |

| Return ||
|---|--------------------------------------------------|
| T | a view with given ID This value cannot be`null`. |

**See Also**

- [android.view.View#requireViewById(int)](https://developer.android.com/reference/kotlin/android/view/View.html#requireViewById(kotlin.Int))
- [android.app.Dialog#findViewById(int)](https://developer.android.com/reference/kotlin/android/app/Dialog#findViewById(kotlin.Int)) 

### setCancelMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCancelMessage(msg: Message?): Unit
```

Set a message to be sent when the dialog is canceled.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)?:The msg to send when the dialog is canceled. This value may be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/app/Dialog#setOnCancelListener(android.content.DialogInterface.OnCancelListener)> 

### setCancelable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCancelable(flag: Boolean): Unit
```

Sets whether this dialog is cancelable with the [BACK](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int) key. 

### setCanceledOnTouchOutside

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCanceledOnTouchOutside(cancel: Boolean): Unit
```

Sets whether this dialog is canceled when touched outside the window's bounds. If setting to true, the dialog is set to be cancelable if not already set.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cancel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the dialog should be canceled when touched outside the window. |

### setContentView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentView(view: View): Unit
```

Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):The desired content to display. This value cannot be`null`. |

### setContentView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentView(
    view: View, 
    params: ViewGroup.LayoutParams?
): Unit
```

Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):The desired content to display. This value cannot be`null`. |
| `params` | [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#)?:Layout parameters for the view. This value may be`null`. |

### setContentView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentView(layoutResID: Int): Unit
```

Set the screen content from a layout resource. The resource will be inflated, adding all top-level views to the screen.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------|
| `layoutResID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource ID to be inflated. |

### setDismissMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDismissMessage(msg: Message?): Unit
```

Set a message to be sent when the dialog is dismissed.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)?:The msg to send when the dialog is dismissed. This value may be`null`. |

### setFeatureDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFeatureDrawable(
    featureId: Int, 
    drawable: Drawable?
): Unit
```

Convenience for calling [android.view.Window#setFeatureDrawable(int, Drawable)](https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawable(kotlin.Int,%20android.graphics.drawable.Drawable)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `drawable` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)?:This value may be`null`. |

### setFeatureDrawableAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFeatureDrawableAlpha(
    featureId: Int, 
    alpha: Int
): Unit
```

Convenience for calling [android.view.Window#setFeatureDrawableAlpha](https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableAlpha(kotlin.Int,%20kotlin.Int)). 

### setFeatureDrawableResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFeatureDrawableResource(
    featureId: Int, 
    resId: Int
): Unit
```

Convenience for calling [android.view.Window#setFeatureDrawableResource](https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableResource(kotlin.Int,%20kotlin.Int)). 

### setFeatureDrawableUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFeatureDrawableUri(
    featureId: Int, 
    uri: Uri?
): Unit
```

Convenience for calling [android.view.Window#setFeatureDrawableUri](https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableUri(kotlin.Int,%20android.net.Uri)).

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?:This value may be`null`. |

### setOnCancelListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnCancelListener(listener: DialogInterface.OnCancelListener?): Unit
```

Set a listener to be invoked when the dialog is canceled.

This will only be invoked when the dialog is canceled. Cancel events alone will not capture all ways that the dialog might be dismissed. If the creator needs to know when a dialog is dismissed in general, use [setOnDismissListener](https://developer.android.com/reference/kotlin/android/app/Dialog#setOnDismissListener(android.content.DialogInterface.OnDismissListener)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [DialogInterface.OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#)?:The [DialogInterface.OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#) to use. This value may be`null`. |

### setOnDismissListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnDismissListener(listener: DialogInterface.OnDismissListener?): Unit
```

Set a listener to be invoked when the dialog is dismissed.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [DialogInterface.OnDismissListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnDismissListener.html#)?:The [DialogInterface.OnDismissListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnDismissListener.html#) to use. This value may be`null`. |

### setOnKeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnKeyListener(onKeyListener: DialogInterface.OnKeyListener?): Unit
```

Sets the callback that will be called if a key is dispatched to the dialog.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `onKeyListener` | [DialogInterface.OnKeyListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnKeyListener.html#)?:This value may be`null`. |

### setOnShowListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnShowListener(listener: DialogInterface.OnShowListener?): Unit
```

Sets a listener to be invoked when the dialog is shown.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [DialogInterface.OnShowListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnShowListener.html#)?:The [DialogInterface.OnShowListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnShowListener.html#) to use. This value may be`null`. |

### setOwnerActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOwnerActivity(activity: Activity): Unit
```

Sets the Activity that owns this dialog. An example use: This Dialog will use the suggested volume control stream of the Activity.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):The Activity that owns this dialog. This value cannot be`null`. |

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTitle(titleId: Int): Unit
```

Set the title text for this dialog's window. The text is retrieved from the resources with the supplied identifier.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `titleId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the title's text resource identifier |

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTitle(title: CharSequence?): Unit
```

Set the title text for this dialog's window.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The new text to display in the title. This value may be`null`. |

### setVolumeControlStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setVolumeControlStream(streamType: Int): Unit
```

By default, this will use the owner Activity's suggested stream type. 
**See Also**

- [android.app.Activity#setVolumeControlStream(int)](https://developer.android.com/reference/kotlin/android/app/Activity#setVolumeControlStream(kotlin.Int))
- [#setOwnerActivity(Activity)](https://developer.android.com/reference/kotlin/android/app/Dialog#setOwnerActivity(android.app.Activity)) 

### show

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun show(): Unit
```

Start the dialog and display it on screen. The window is placed in the application layer and opaque. Note that you should not override this method to do initialization when the dialog is shown, instead implement that in [onStart](https://developer.android.com/reference/kotlin/android/app/Dialog#onStart()). 

### takeKeyEvents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun takeKeyEvents(get: Boolean): Unit
```

Request that key events come to this dialog. Use this if your dialog has no views with focus, but the dialog still wants a chance to process key events.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `get` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the dialog should receive key events, false otherwise |

**See Also**

- [android.view.Window#takeKeyEvents](https://developer.android.com/reference/kotlin/android/view/Window.html#takeKeyEvents(kotlin.Boolean)) 

### unregisterForContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterForContextMenu(view: View): Unit
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):This value cannot be`null`. |

**See Also**

- [android.app.Activity#unregisterForContextMenu(View)](https://developer.android.com/reference/kotlin/android/app/Activity#unregisterForContextMenu(android.view.View))

## Protected methods

### onCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onCreate(savedInstanceState: Bundle!): Unit
```

Similar to android.app.Activity#onCreate, you should initialize your dialog in this method, including calling #setContentView.

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:If this dialog is being reinitialized after a the hosting activity was previously shut down, holds the result from the most recent call to [onSaveInstanceState](https://developer.android.com/reference/kotlin/android/app/Dialog#onSaveInstanceState()), or null if this is the first time. |

### onStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStart(): Unit
```

Called when the dialog is starting. 

### onStop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStop(): Unit
```

Called to tell you that you're stopping.
