# Dialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Dialog

Kotlin| [Java](../android/app/Dialog.md) 
| --- | --- |

```
open class Dialog : DialogInterface, KeyEvent.Callback, View.OnCreateContextMenuListener, Window.Callback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.Dialog](../android/app/Dialog.md) |

| Known Direct Subclasses [AlertDialog](../android/app/AlertDialog.md), [CharacterPickerDialog](../android/text/method/CharacterPickerDialog.md), [Presentation](../android/app/Presentation.md) |-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------| | [AlertDialog](../android/app/AlertDialog.md) | A subclass of Dialog that can display one, two or three buttons. | | [CharacterPickerDialog](../android/text/method/CharacterPickerDialog.md) | Dialog for choosing accented characters related to a base character. | | [Presentation](../android/app/Presentation.md) | Base class for presentations. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DatePickerDialog](../android/app/DatePickerDialog.md), [ProgressDialog](../android/app/ProgressDialog.md), [TimePickerDialog](../android/app/TimePickerDialog.md) |-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------| | [DatePickerDialog](../android/app/DatePickerDialog.md) | A simple dialog containing an [android.widget.DatePicker](../android/widget/DatePicker.md). | | [ProgressDialog](../android/app/ProgressDialog.md) | A dialog showing a progress indicator and an optional text message or view. | | [TimePickerDialog](../android/app/TimePickerDialog.md) | A dialog that prompts the user for the time of day using a [TimePicker](../android/widget/TimePicker.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for Dialogs.

Note: Activities provide a facility to manage the creation, saving and restoring of dialogs. See [Activity.onCreateDialog(int)](../android/app/Activity.md)), [Activity.onPrepareDialog(int, Dialog)](../android/app/Activity.md)), [Activity.showDialog(int)](../android/app/Activity.md)), and [Activity.dismissDialog(int)](../android/app/Activity.md)). If these methods are used, [getOwnerActivity()](../android/app/Dialog.md))will return the Activity that managed this dialog.

Often you will want to have a Dialog display on top of the current input method, because there is no reason for it to accept text. You can do this by setting the [WindowManager.LayoutParams.FLAG_ALT_FOCUSABLE_IM](../android/view/WindowManager.LayoutParams.md) window flag (assuming your Dialog takes input focus, as it the default) with the following code: 

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
| From class [DialogInterface](../android/content/DialogInterface.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON1](../android/content/DialogInterface.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON2](../android/content/DialogInterface.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON3](../android/content/DialogInterface.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEGATIVE](../android/content/DialogInterface.md) <br /> The identifier for the negative button. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEUTRAL](../android/content/DialogInterface.md) <br /> The identifier for the neutral button. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_POSITIVE](../android/content/DialogInterface.md) <br /> The identifier for the positive button. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Dialog](../android/app/Dialog.md))`(`context:` ` [Context](../android/content/Context.md)`)` Creates a dialog window that uses the default dialog theme. |
| [Dialog](../android/app/Dialog.md))`(`context:` ` [Context](../android/content/Context.md)`, `themeResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a dialog window that uses a custom dialog style. |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Dialog](../android/app/Dialog.md))`(`context:` ` [Context](../android/content/Context.md)`, `cancelable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `cancelListener:` ` [DialogInterface.OnCancelListener](../android/content/DialogInterface.OnCancelListener.md)?`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addContentView](../android/app/Dialog.md))`(`view:` ` [View](../android/view/View.md)`, `params:` ` [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)?`)` Add an additional content view to the screen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../android/app/Dialog.md))`()` Cancel the dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeOptionsMenu](../android/app/Dialog.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [create](../android/app/Dialog.md))`()` Forces immediate creation of the dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](../android/app/Dialog.md))`()` Dismiss this dialog, removing it from the screen. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchGenericMotionEvent](../android/app/Dialog.md))`(`ev:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Called to process generic motion events. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchKeyEvent](../android/app/Dialog.md))`(`event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` Called to process key events. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchKeyShortcutEvent](../android/app/Dialog.md))`(`event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` Called to process a key shortcut event. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchPopulateAccessibilityEvent](../android/app/Dialog.md))`(`event:` ` [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)`)` Called to process population of [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) s. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchTouchEvent](../android/app/Dialog.md))`(`ev:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Called to process touch screen events. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchTrackballEvent](../android/app/Dialog.md))`(`ev:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Called to process trackball events. |
| openT | [findViewById](../android/app/Dialog.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Finds the first descendant view with the given ID or`null`if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via [show()](../android/app/Dialog.md))or [create()](../android/app/Dialog.md))). |
| --- | --- |
| open [ActionBar](../android/app/ActionBar.md)? | [getActionBar](../android/app/Dialog.md))`()` Retrieve the [ActionBar](../android/app/ActionBar.md) attached to this dialog, if present. |
| [Context](../android/content/Context.md) | [getContext](../android/app/Dialog.md))`()` Retrieve the Context this Dialog is running in. |
| open [View](../android/view/View.md)? | [getCurrentFocus](../android/app/Dialog.md))`()` Call [android.view.Window#getCurrentFocus](../android/view/Window.md))on the Window if this Activity to return the currently focused view. |
| --- | --- |
| open [LayoutInflater](../android/view/LayoutInflater.md) | [getLayoutInflater](../android/app/Dialog.md))`()` <br /> |
| open [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md) | [getOnBackInvokedDispatcher](../android/app/Dialog.md))`()` Returns the [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md) instance associated with the window that this dialog is attached to. |
| [Activity](../android/app/Activity.md)? | [getOwnerActivity](../android/app/Dialog.md))`()` Returns the Activity that owns this Dialog. |
| --- | --- |
| [SearchEvent](../android/view/SearchEvent.md)? | [getSearchEvent](../android/app/Dialog.md))`()` During the onSearchRequested() callbacks, this function will return the [SearchEvent](../android/view/SearchEvent.md) that triggered the callback, if it exists. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolumeControlStream](../android/app/Dialog.md))`()` <br /> |
| open [Window](../android/view/Window.md)? | [getWindow](../android/app/Dialog.md))`()` Retrieve the current Window for the activity. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hide](../android/app/Dialog.md))`()` Hide the dialog, but do not dismiss it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateOptionsMenu](../android/app/Dialog.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShowing](../android/app/Dialog.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionModeFinished](../android/app/Dialog.md))`(`mode:` ` [ActionMode](../android/view/ActionMode.md)!`)` Called when an action mode has been finished. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionModeStarted](../android/app/Dialog.md))`(`mode:` ` [ActionMode](../android/view/ActionMode.md)!`)` Called when an action mode has been started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToWindow](../android/app/Dialog.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBackPressed](../android/app/Dialog.md))`()` Called when the dialog has detected the user's press of the back key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](../android/app/Dialog.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onContextItemSelected](../android/app/Dialog.md))`(`item:` ` [MenuItem](../android/view/MenuItem.md)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContextMenuClosed](../android/app/Dialog.md))`(`menu:` ` [Menu](../android/view/Menu.md)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreateContextMenu](../android/app/Dialog.md))`(`menu:` ` [ContextMenu](../android/view/ContextMenu.md)!`, `v:` ` [View](../android/view/View.md)!`, `menuInfo:` ` [ContextMenu.ContextMenuInfo](../android/view/ContextMenu.ContextMenuInfo.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreateOptionsMenu](../android/app/Dialog.md))`(`menu:` ` [Menu](../android/view/Menu.md)`)` It is usually safe to proxy this call to the owner activity's [Activity.onCreateOptionsMenu(Menu)](../android/app/Activity.md))if the client desires the same menu for this Dialog. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreatePanelMenu](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](../android/view/Menu.md)`)` <br /> |
| open [View](../android/view/View.md)? | [onCreatePanelView](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDetachedFromWindow](../android/app/Dialog.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](../android/app/Dialog.md))`(`event:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Called when a generic motion event was not handled by any of the views inside of the dialog. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](../android/app/Dialog.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` A key was pressed down. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyLongPress](../android/app/Dialog.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` Default implementation of [KeyEvent.Callback.onKeyLongPress()](../android/view/KeyEvent.Callback.md)): always returns false (doesn't handle the event). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyMultiple](../android/app/Dialog.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `repeatCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` Default implementation of [KeyEvent.Callback.onKeyMultiple()](../android/view/KeyEvent.Callback.md)): always returns false (doesn't handle the event). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyShortcut](../android/app/Dialog.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` Called when a key shortcut event is not handled by any of the views in the Dialog. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](../android/app/Dialog.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` A key was released. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMenuItemSelected](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `item:` ` [MenuItem](../android/view/MenuItem.md)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMenuOpened](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](../android/view/Menu.md)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onOptionsItemSelected](../android/app/Dialog.md))`(`item:` ` [MenuItem](../android/view/MenuItem.md)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOptionsMenuClosed](../android/app/Dialog.md))`(`menu:` ` [Menu](../android/view/Menu.md)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPanelClosed](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](../android/view/Menu.md)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPrepareOptionsMenu](../android/app/Dialog.md))`(`menu:` ` [Menu](../android/view/Menu.md)`)` It is usually safe to proxy this call to the owner activity's [Activity.onPrepareOptionsMenu(Menu)](../android/app/Activity.md))if the client desires the same menu for this Dialog. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPreparePanel](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `view:` ` [View](../android/view/View.md)?`, `menu:` ` [Menu](../android/view/Menu.md)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestoreInstanceState](../android/app/Dialog.md))`(`savedInstanceState:` ` [Bundle](../android/os/Bundle.md)`)` Restore the state of the dialog from a previously saved bundle. |
| open [Bundle](../android/os/Bundle.md) | [onSaveInstanceState](../android/app/Dialog.md))`()` Saves the state of the dialog into a bundle. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSearchRequested](../android/app/Dialog.md))`()` This hook is called when the user signals the desire to start a search. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSearchRequested](../android/app/Dialog.md))`(`searchEvent:` ` [SearchEvent](../android/view/SearchEvent.md)`)` This hook is called when the user signals the desire to start a search. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](../android/app/Dialog.md))`(`event:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Called when a touch screen event was not handled by any of the views under it. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTrackballEvent](../android/app/Dialog.md))`(`event:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Called when the trackball was moved and not handled by any of the views inside of the activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowAttributesChanged](../android/app/Dialog.md))`(`params:` ` [WindowManager.LayoutParams](../android/view/WindowManager.LayoutParams.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowFocusChanged](../android/app/Dialog.md))`(`hasFocus:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| open [ActionMode](../android/view/ActionMode.md)? | [onWindowStartingActionMode](../android/app/Dialog.md))`(`callback:` ` [ActionMode.Callback](../android/view/ActionMode.Callback.md)!`)` <br /> |
| open [ActionMode](../android/view/ActionMode.md)? | [onWindowStartingActionMode](../android/app/Dialog.md))`(`callback:` ` [ActionMode.Callback](../android/view/ActionMode.Callback.md)!`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openContextMenu](../android/app/Dialog.md))`(`view:` ` [View](../android/view/View.md)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openOptionsMenu](../android/app/Dialog.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerForContextMenu](../android/app/Dialog.md))`(`view:` ` [View](../android/view/View.md)`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requestWindowFeature](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Enable extended window features. |
| --- | --- |
| T | [requireViewById](../android/app/Dialog.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Finds the first descendant view with the given ID or throws an IllegalArgumentException if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via [show()](../android/app/Dialog.md))or [create()](../android/app/Dialog.md))). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCancelMessage](../android/app/Dialog.md))`(`msg:` ` [Message](../android/os/Message.md)?`)` Set a message to be sent when the dialog is canceled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCancelable](../android/app/Dialog.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this dialog is cancelable with the [BACK](../android/view/KeyEvent.md) key. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCanceledOnTouchOutside](../android/app/Dialog.md))`(`cancel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this dialog is canceled when touched outside the window's bounds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](../android/app/Dialog.md))`(`view:` ` [View](../android/view/View.md)`)` Set the screen content to an explicit view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](../android/app/Dialog.md))`(`view:` ` [View](../android/view/View.md)`, `params:` ` [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)?`)` Set the screen content to an explicit view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](../android/app/Dialog.md))`(`layoutResID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the screen content from a layout resource. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDismissMessage](../android/app/Dialog.md))`(`msg:` ` [Message](../android/os/Message.md)?`)` Set a message to be sent when the dialog is dismissed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawable](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `drawable:` ` [Drawable](../android/graphics/drawable/Drawable.md)?`)` Convenience for calling [android.view.Window#setFeatureDrawable(int, Drawable)](../android/view/Window.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawableAlpha](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convenience for calling [android.view.Window#setFeatureDrawableAlpha](../android/view/Window.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawableResource](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convenience for calling [android.view.Window#setFeatureDrawableResource](../android/view/Window.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeatureDrawableUri](../android/app/Dialog.md))`(`featureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uri:` ` [Uri](../android/net/Uri.md)?`)` Convenience for calling [android.view.Window#setFeatureDrawableUri](../android/view/Window.md)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnCancelListener](../android/app/Dialog.md))`(`listener:` ` [DialogInterface.OnCancelListener](../android/content/DialogInterface.OnCancelListener.md)?`)` Set a listener to be invoked when the dialog is canceled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDismissListener](../android/app/Dialog.md))`(`listener:` ` [DialogInterface.OnDismissListener](../android/content/DialogInterface.OnDismissListener.md)?`)` Set a listener to be invoked when the dialog is dismissed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnKeyListener](../android/app/Dialog.md))`(`onKeyListener:` ` [DialogInterface.OnKeyListener](../android/content/DialogInterface.OnKeyListener.md)?`)` Sets the callback that will be called if a key is dispatched to the dialog. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnShowListener](../android/app/Dialog.md))`(`listener:` ` [DialogInterface.OnShowListener](../android/content/DialogInterface.OnShowListener.md)?`)` Sets a listener to be invoked when the dialog is shown. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOwnerActivity](../android/app/Dialog.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Sets the Activity that owns this dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](../android/app/Dialog.md))`(`titleId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the title text for this dialog's window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](../android/app/Dialog.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Set the title text for this dialog's window. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVolumeControlStream](../android/app/Dialog.md))`(`streamType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` By default, this will use the owner Activity's suggested stream type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](../android/app/Dialog.md))`()` Start the dialog and display it on screen. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [takeKeyEvents](../android/app/Dialog.md))`(`get:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Request that key events come to this dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterForContextMenu](../android/app/Dialog.md))`(`view:` ` [View](../android/view/View.md)`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreate](../android/app/Dialog.md))`(`savedInstanceState:` ` [Bundle](../android/os/Bundle.md)!`)` Similar to android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](../android/app/Dialog.md))`()` Called when the dialog is starting. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStop](../android/app/Dialog.md))`()` Called to tell you that you're stopping. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Callback](../android/view/Window.Callback.md) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPointerCaptureChanged](../android/view/Window.Callback.md))`(`hasCapture:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Called when pointer capture is enabled or disabled for the current window. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProvideKeyboardShortcuts](../android/view/Window.Callback.md))`(`data:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [KeyboardShortcutGroup](../android/view/KeyboardShortcutGroup.md)!>!`, `menu:` ` [Menu](../android/view/Menu.md)?`, `deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when Keyboard Shortcuts are requested for the current window. <br /> | ||

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
| `context` | [Context](../android/content/Context.md):the context in which the dialog should run This value cannot be`null`. |

**See Also**

- [android.R.styleable#Theme_dialogTheme](../android/R.styleable.md) 

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
| `context` | [Context](../android/content/Context.md):the context in which the dialog should run This value cannot be`null`. |
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
| `context` | [Context](../android/content/Context.md):This value cannot be`null`. |
| `cancelListener` | [DialogInterface.OnCancelListener](../android/content/DialogInterface.OnCancelListener.md)?:This value may be`null`. |

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
| `view` | [View](../android/view/View.md):The desired content to display. This value cannot be`null`. |
| `params` | [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)?:Layout parameters for the view. This value may be`null`. |

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(): Unit
```

Cancel the dialog. This is essentially the same as calling [dismiss()](../android/app/Dialog.md)), but it will also call your [DialogInterface.OnCancelListener](../android/content/DialogInterface.OnCancelListener.md)(if registered). 

### closeOptionsMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun closeOptionsMenu(): Unit
```  
**See Also**

- [android.app.Activity#closeOptionsMenu()](../android/app/Activity.md)) 

### create

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun create(): Unit
```

Forces immediate creation of the dialog.

Note that you should not override this method to perform dialog creation. Rather, override [onCreate(android.os.Bundle)](../android/app/Dialog.md)). 

### dismiss

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dismiss(): Unit
```

Dismiss this dialog, removing it from the screen. This method can be invoked safely from any thread. Note that you should not override this method to do cleanup when the dialog is dismissed, instead implement that in [onStop](../android/app/Dialog.md)). 

### dispatchGenericMotionEvent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchGenericMotionEvent(ev: MotionEvent): Boolean
```

Called to process generic motion events. You can override this to intercept all generic motion events before they are dispatched to the window. Be sure to call this implementation for generic motion events that should be handled normally.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | The generic motion event. |
| `ev` | [MotionEvent](../android/view/MotionEvent.md):The generic motion event. This value cannot be`null`. |

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
| `event` | [KeyEvent](../android/view/KeyEvent.md):The key event. This value cannot be`null`. |

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
| `event` | [KeyEvent](../android/view/KeyEvent.md):The key shortcut event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this event was consumed. |

### dispatchPopulateAccessibilityEvent

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchPopulateAccessibilityEvent(event: AccessibilityEvent): Boolean
```

Called to process population of [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) s.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md):This value cannot be`null`. |

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
| `ev` | [MotionEvent](../android/view/MotionEvent.md):The touch screen event. This value cannot be`null`. |

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
| `ev` | [MotionEvent](../android/view/MotionEvent.md):The trackball event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Return true if this event was consumed. |

### findViewById

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : View!> findViewById(id: Int): T
```

Finds the first descendant view with the given ID or`null`if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via [show()](../android/app/Dialog.md))or [create()](../android/app/Dialog.md))).

**Note:**In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ID to search for |

| Return ||
|---|--------------------------------------------------|
| T | a view with given ID if found, or`null`otherwise |

**See Also**

- [android.view.View#findViewById(int)](../android/view/View.md))
- [android.app.Dialog#requireViewById(int)](../android/app/Dialog.md)) 

### getActionBar

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActionBar(): ActionBar?
```

Retrieve the [ActionBar](../android/app/ActionBar.md) attached to this dialog, if present.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ActionBar](../android/app/ActionBar.md)? | The ActionBar attached to the dialog or null if no ActionBar is present. |

### getContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContext(): Context
```

Retrieve the Context this Dialog is running in.

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Context](../android/content/Context.md) | Context The Context used by the Dialog. This value cannot be`null`. |

### getCurrentFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrentFocus(): View?
```

Call [android.view.Window#getCurrentFocus](../android/view/Window.md))on the Window if this Activity to return the currently focused view.

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------|
| [View](../android/view/View.md)? | View The current View with focus or null. |

**See Also**

- [#getWindow](../android/app/Dialog.md))
- [android.view.Window#getCurrentFocus](../android/view/Window.md)) 

### getLayoutInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLayoutInflater(): LayoutInflater
```

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------|
| [LayoutInflater](../android/view/LayoutInflater.md) | This value cannot be`null`. |

### getOnBackInvokedDispatcher

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOnBackInvokedDispatcher(): OnBackInvokedDispatcher
```

Returns the [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md) instance associated with the window that this dialog is attached to.

| Return ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md) | This value cannot be`null`. |

### getOwnerActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOwnerActivity(): Activity?
```

Returns the Activity that owns this Dialog. For example, if [Activity.showDialog(int)](../android/app/Activity.md))is used to show this Dialog, that Activity will be the owner (by default). Depending on how this dialog was created, this may return null.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------|
| [Activity](../android/app/Activity.md)? | The Activity that owns this Dialog. |

### getSearchEvent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSearchEvent(): SearchEvent?
```

During the onSearchRequested() callbacks, this function will return the [SearchEvent](../android/view/SearchEvent.md) that triggered the callback, if it exists.

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [SearchEvent](../android/view/SearchEvent.md)? | SearchEvent The SearchEvent that triggered the #onSearchRequested callback. This value may be`null`. |

### getVolumeControlStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolumeControlStream(): Int
```  
**See Also**

- [android.app.Activity#getVolumeControlStream()](../android/app/Activity.md)) 

### getWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWindow(): Window?
```

Retrieve the current Window for the activity. This can be used to directly access parts of the Window API that are not available through Activity/Screen.

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Window](../android/view/Window.md)? | Window The current window, or null if the activity is not visual. |

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

- [android.app.Activity#invalidateOptionsMenu()](../android/app/Activity.md)) 

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
| `mode` | [ActionMode](../android/view/ActionMode.md)!:The mode that was just finished. |

### onActionModeStarted

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActionModeStarted(mode: ActionMode!): Unit
```

Called when an action mode has been started. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeStarted(mode). 
If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [ActionMode](../android/view/ActionMode.md)!:The new mode that has just been started. |

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

**Deprecated:** *Use [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md) or`androidx.activity.OnBackPressedCallback`to handle back navigation instead.*

*Starting from Android 13 (API level 33), back event handling is moving to an ahead-of-time model and [onBackPressed()](../android/app/Dialog.md))and [KeyEvent.KEYCODE_BACK](../android/view/KeyEvent.md) should not be used to handle back events (back gesture or back button click). Instead, an [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md) should be registered using [Dialog.getOnBackInvokedDispatcher()](../android/app/Dialog.md)) [.registerOnBackInvokedCallback(priority, callback)](../android/window/OnBackInvokedDispatcher.md)).*

<br />

Called when the dialog has detected the user's press of the back key. The default implementation simply cancels the dialog (only if it is cancelable), but you can override this to do whatever you want.

If you target version [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md) or later, you should not use this method but register an [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md) on an [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md) that you can retrieve using [getOnBackInvokedDispatcher()](../android/app/Dialog.md)). You should also set`android:enableOnBackInvokedCallback="true"`in the application manifest.

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
| `item` | [MenuItem](../android/view/MenuItem.md):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onContextItemSelected(MenuItem)](../android/app/Activity.md)) 

### onContextMenuClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onContextMenuClosed(menu: Menu): Unit
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](../android/view/Menu.md):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onContextMenuClosed(Menu)](../android/app/Activity.md)) 

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
| `menu` | [ContextMenu](../android/view/ContextMenu.md)!:The context menu that is being built |
| `v` | [View](../android/view/View.md)!:The view for which the context menu is being built |
| `menuInfo` | [ContextMenu.ContextMenuInfo](../android/view/ContextMenu.ContextMenuInfo.md)!:Extra information about the item for which the context menu should be shown. This information will vary depending on the class of v. |
| --- | --- |

**See Also**

- [android.app.Activity#onCreateContextMenu(ContextMenu, View, ContextMenuInfo)](../android/app/Activity.md)) 

### onCreateOptionsMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateOptionsMenu(menu: Menu): Boolean
```

It is usually safe to proxy this call to the owner activity's [Activity.onCreateOptionsMenu(Menu)](../android/app/Activity.md))if the client desires the same menu for this Dialog.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](../android/view/Menu.md):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onCreateOptionsMenu(Menu)](../android/app/Activity.md))
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
| `menu` | [Menu](../android/view/Menu.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean You must return true for the panel to be displayed; if you return false it will not be shown. |

**See Also**

- [android.app.Activity#onCreatePanelMenu(int, Menu)](../android/app/Activity.md)) 

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
| [View](../android/view/View.md)? | view The top-level view to place in the panel. |

**See Also**

- [android.app.Activity#onCreatePanelView(int)](../android/app/Activity.md)) 

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

Generic motion events describe joystick movements, mouse hovers, track pad touches, scroll wheel movements and other input events. The [source](../android/view/MotionEvent.md))of the motion event specifies the class of input that was received. Implementations of this method must examine the bits in the source before processing the event. The following code example shows how this is done.

Generic motion events with source class [android.view.InputDevice#SOURCE_CLASS_POINTER](../android/view/InputDevice.md) are delivered to the view under the pointer. All other generic motion events are delivered to the focused view.

See [View.onGenericMotionEvent(MotionEvent)](../android/view/View.md))for an example of how to handle this event.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [MotionEvent](../android/view/MotionEvent.md):The generic motion event being processed. This value cannot be`null`. |

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

Default implementation consumes [KEYCODE_BACK](../android/view/KeyEvent.md) and, as of [P](../android/os/Build.VERSION_CODES.md), [KEYCODE_ESCAPE](../android/view/KeyEvent.md) to later handle them in [onKeyUp](../android/app/Dialog.md)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `event` | [KeyEvent](../android/view/KeyEvent.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

**See Also**

- [#onKeyUp](../android/app/Dialog.md))
- [android.view.KeyEvent](../android/view/KeyEvent.md) 

### onKeyLongPress

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyLongPress(
    keyCode: Int, 
    event: KeyEvent
): Boolean
```

Default implementation of [KeyEvent.Callback.onKeyLongPress()](../android/view/KeyEvent.Callback.md)): always returns false (doesn't handle the event).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `event` | [KeyEvent](../android/view/KeyEvent.md):This value cannot be`null`. |

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

Default implementation of [KeyEvent.Callback.onKeyMultiple()](../android/view/KeyEvent.Callback.md)): always returns false (doesn't handle the event).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `count` | Number of pairs as returned by event.getRepeatCount(). |
| `event` | [KeyEvent](../android/view/KeyEvent.md):This value cannot be`null`. |
| --- | --- |

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

Called when a key shortcut event is not handled by any of the views in the Dialog. Override this method to implement global key shortcuts for the Dialog. Key shortcuts can also be implemented by setting the [shortcut](../android/view/MenuItem.md))property of menu items.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `event` | [KeyEvent](../android/view/KeyEvent.md):Description of the key event. This value cannot be`null`. |

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

Default implementation consumes [KEYCODE_BACK](../android/view/KeyEvent.md) and, as of [P](../android/os/Build.VERSION_CODES.md), [KEYCODE_ESCAPE](../android/view/KeyEvent.md) to close the dialog.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value in event.getKeyCode(). |
| `event` | [KeyEvent](../android/view/KeyEvent.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

**See Also**

- [#onKeyDown](../android/app/Dialog.md))
- [android.view.KeyEvent](../android/view/KeyEvent.md) 

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
| `item` | [MenuItem](../android/view/MenuItem.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Return true to finish processing of selection, or false to perform the normal menu handling (calling its Runnable or sending a Message to its target Handler). |

**See Also**

- [android.app.Activity#onMenuItemSelected(int, MenuItem)](../android/app/Activity.md)) 

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
| `menu` | [Menu](../android/view/Menu.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Return true to allow the menu to open, or false to prevent the menu from opening. |

**See Also**

- [android.app.Activity#onMenuOpened(int, Menu)](../android/app/Activity.md)) 

### onOptionsItemSelected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onOptionsItemSelected(item: MenuItem): Boolean
```

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `item` | [MenuItem](../android/view/MenuItem.md):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onOptionsItemSelected(MenuItem)](../android/app/Activity.md)) 

### onOptionsMenuClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onOptionsMenuClosed(menu: Menu): Unit
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](../android/view/Menu.md):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onOptionsMenuClosed(Menu)](../android/app/Activity.md)) 

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
| `menu` | [Menu](../android/view/Menu.md):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onPanelClosed(int, Menu)](../android/app/Activity.md)) 

### onPrepareOptionsMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPrepareOptionsMenu(menu: Menu): Boolean
```

It is usually safe to proxy this call to the owner activity's [Activity.onPrepareOptionsMenu(Menu)](../android/app/Activity.md))if the client desires the same menu for this Dialog.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](../android/view/Menu.md):This value cannot be`null`. |

**See Also**

- [android.app.Activity#onPrepareOptionsMenu(Menu)](../android/app/Activity.md))
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
| `view` | [View](../android/view/View.md)?:This value may be`null`. |
| `menu` | [Menu](../android/view/Menu.md):This value cannot be`null`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean You must return true for the panel to be displayed; if you return false it will not be shown. |

**See Also**

- [android.app.Activity#onPreparePanel(int, View, Menu)](../android/app/Activity.md)) 

### onRestoreInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRestoreInstanceState(savedInstanceState: Bundle): Unit
```

Restore the state of the dialog from a previously saved bundle. The default implementation restores the state of the dialog's view hierarchy that was saved in the default implementation of [onSaveInstanceState()](../android/app/Dialog.md)), so be sure to call through to super when overriding unless you want to do all restoring of state yourself.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `savedInstanceState` | [Bundle](../android/os/Bundle.md):The state of the dialog previously saved by [onSaveInstanceState()](../android/app/Dialog.md)). This value cannot be`null`. |

### onSaveInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSaveInstanceState(): Bundle
```

Saves the state of the dialog into a bundle. The default implementation saves the state of its view hierarchy, so you'll likely want to call through to super if you override this to save additional state.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Bundle](../android/os/Bundle.md) | A bundle with the state of the dialog. This value cannot be`null`. |

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
| `searchEvent` | [SearchEvent](../android/view/SearchEvent.md):This value cannot be`null`. |

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
| `event` | [MotionEvent](../android/view/MotionEvent.md):The touch screen event being processed. This value cannot be`null`. |

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
| `event` | [MotionEvent](../android/view/MotionEvent.md):The trackball event being processed. This value cannot be`null`. |

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
| `callback` | [ActionMode.Callback](../android/view/ActionMode.Callback.md)!:Callback to control the lifecycle of this action mode |

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ActionMode](../android/view/ActionMode.md)? | The ActionMode that was started, or null if the system should present it |

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
| `callback` | [ActionMode.Callback](../android/view/ActionMode.Callback.md)!:Callback to control the lifecycle of this action mode |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [ActionMode.TYPE_PRIMARY](../android/view/ActionMode.md) or [ActionMode.TYPE_FLOATING](../android/view/ActionMode.md). |

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ActionMode](../android/view/ActionMode.md)? | The ActionMode that was started, or null if the system should present it |

### openContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openContextMenu(view: View): Unit
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md):This value cannot be`null`. |

**See Also**

- [android.app.Activity#openContextMenu(View)](../android/app/Activity.md)) 

### openOptionsMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openOptionsMenu(): Unit
```  
**See Also**

- [android.app.Activity#openOptionsMenu()](../android/app/Activity.md)) 

### registerForContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerForContextMenu(view: View): Unit
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md):This value cannot be`null`. |

**See Also**

- [android.app.Activity#registerForContextMenu(View)](../android/app/Activity.md)) 

### requestWindowFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requestWindowFeature(featureId: Int): Boolean
```

Enable extended window features. This is a convenience for calling [getWindow().requestFeature()](../android/view/Window.md)).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired feature as defined in [android.view.Window](../android/view/Window.md). |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if the requested feature is supported and now enabled. |

**See Also**

- [android.view.Window#requestFeature](../android/view/Window.md)) 

### requireViewById

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : View!> requireViewById(id: Int): T
```

Finds the first descendant view with the given ID or throws an IllegalArgumentException if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via [show()](../android/app/Dialog.md))or [create()](../android/app/Dialog.md))).

**Note:**In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ID to search for |

| Return ||
|---|--------------------------------------------------|
| T | a view with given ID This value cannot be`null`. |

**See Also**

- [android.view.View#requireViewById(int)](../android/view/View.md))
- [android.app.Dialog#findViewById(int)](../android/app/Dialog.md)) 

### setCancelMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCancelMessage(msg: Message?): Unit
```

Set a message to be sent when the dialog is canceled.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [Message](../android/os/Message.md)?:The msg to send when the dialog is canceled. This value may be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/app/Dialog#setOnCancelListener(android.content.DialogInterface.OnCancelListener)> 

### setCancelable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCancelable(flag: Boolean): Unit
```

Sets whether this dialog is cancelable with the [BACK](../android/view/KeyEvent.md) key. 

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
| `view` | [View](../android/view/View.md):The desired content to display. This value cannot be`null`. |

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
| `view` | [View](../android/view/View.md):The desired content to display. This value cannot be`null`. |
| `params` | [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)?:Layout parameters for the view. This value may be`null`. |

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
| `msg` | [Message](../android/os/Message.md)?:The msg to send when the dialog is dismissed. This value may be`null`. |

### setFeatureDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFeatureDrawable(
    featureId: Int, 
    drawable: Drawable?
): Unit
```

Convenience for calling [android.view.Window#setFeatureDrawable(int, Drawable)](../android/view/Window.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `drawable` | [Drawable](../android/graphics/drawable/Drawable.md)?:This value may be`null`. |

### setFeatureDrawableAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFeatureDrawableAlpha(
    featureId: Int, 
    alpha: Int
): Unit
```

Convenience for calling [android.view.Window#setFeatureDrawableAlpha](../android/view/Window.md)). 

### setFeatureDrawableResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFeatureDrawableResource(
    featureId: Int, 
    resId: Int
): Unit
```

Convenience for calling [android.view.Window#setFeatureDrawableResource](../android/view/Window.md)). 

### setFeatureDrawableUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFeatureDrawableUri(
    featureId: Int, 
    uri: Uri?
): Unit
```

Convenience for calling [android.view.Window#setFeatureDrawableUri](../android/view/Window.md)).

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md)?:This value may be`null`. |

### setOnCancelListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnCancelListener(listener: DialogInterface.OnCancelListener?): Unit
```

Set a listener to be invoked when the dialog is canceled.

This will only be invoked when the dialog is canceled. Cancel events alone will not capture all ways that the dialog might be dismissed. If the creator needs to know when a dialog is dismissed in general, use [setOnDismissListener](../android/app/Dialog.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [DialogInterface.OnCancelListener](../android/content/DialogInterface.OnCancelListener.md)?:The [DialogInterface.OnCancelListener](../android/content/DialogInterface.OnCancelListener.md) to use. This value may be`null`. |

### setOnDismissListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnDismissListener(listener: DialogInterface.OnDismissListener?): Unit
```

Set a listener to be invoked when the dialog is dismissed.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [DialogInterface.OnDismissListener](../android/content/DialogInterface.OnDismissListener.md)?:The [DialogInterface.OnDismissListener](../android/content/DialogInterface.OnDismissListener.md) to use. This value may be`null`. |

### setOnKeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnKeyListener(onKeyListener: DialogInterface.OnKeyListener?): Unit
```

Sets the callback that will be called if a key is dispatched to the dialog.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `onKeyListener` | [DialogInterface.OnKeyListener](../android/content/DialogInterface.OnKeyListener.md)?:This value may be`null`. |

### setOnShowListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnShowListener(listener: DialogInterface.OnShowListener?): Unit
```

Sets a listener to be invoked when the dialog is shown.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [DialogInterface.OnShowListener](../android/content/DialogInterface.OnShowListener.md)?:The [DialogInterface.OnShowListener](../android/content/DialogInterface.OnShowListener.md) to use. This value may be`null`. |

### setOwnerActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOwnerActivity(activity: Activity): Unit
```

Sets the Activity that owns this dialog. An example use: This Dialog will use the suggested volume control stream of the Activity.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):The Activity that owns this dialog. This value cannot be`null`. |

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

- [android.app.Activity#setVolumeControlStream(int)](../android/app/Activity.md))
- [#setOwnerActivity(Activity)](../android/app/Dialog.md)) 

### show

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun show(): Unit
```

Start the dialog and display it on screen. The window is placed in the application layer and opaque. Note that you should not override this method to do initialization when the dialog is shown, instead implement that in [onStart](../android/app/Dialog.md)). 

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

- [android.view.Window#takeKeyEvents](../android/view/Window.md)) 

### unregisterForContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterForContextMenu(view: View): Unit
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md):This value cannot be`null`. |

**See Also**

- [android.app.Activity#unregisterForContextMenu(View)](../android/app/Activity.md))

## Protected methods

### onCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onCreate(savedInstanceState: Bundle!): Unit
```

Similar to android.app.Activity#onCreate, you should initialize your dialog in this method, including calling #setContentView.

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `savedInstanceState` | [Bundle](../android/os/Bundle.md)!:If this dialog is being reinitialized after a the hosting activity was previously shut down, holds the result from the most recent call to [onSaveInstanceState](../android/app/Dialog.md)), or null if this is the first time. |

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
