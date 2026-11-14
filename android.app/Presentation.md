Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Presentation

```
open class Presentation : Dialog
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.app.Dialog](Dialog.md) ||
| | ↳ | [android.app.Presentation](Presentation.md) |

Base class for presentations.

A presentation is a special kind of dialog whose purpose is to present content on another display. While traditionally used for external displays, starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/Display.html#FLAG_PRESENTATION:kotlin.Int` can now also be attached to built-in internal displays, allowing presentations to be shown on them as well. On earlier releases, internal displays were not suitable for presentations and attempting to show one would always result in an exception. A Presentation is associated with the target `https://developer.android.com/reference/kotlin/android/view/Display.html#` at creation time and configures its context and resource configuration according to the display's metrics.

Notably, the `https://developer.android.com/reference/kotlin/android/content/Context.html#` of a presentation is different from the context of its containing Activity. It is important to inflate the layout of a presentation and load other resources using the presentation's own context to ensure that assets of the correct size and density for the target display are loaded.

A presentation is automatically canceled (see cancel) when the display to which it is attached is removed or when the application's associated task is removed. An activity should take care of pausing and resuming whatever content is playing within the presentation whenever the activity itself is paused or resumed.

### Choosing a presentation display

Before showing a Presentation it's important to choose the `https://developer.android.com/reference/kotlin/android/view/Display.html#` on which it will appear. Choosing a presentation display is sometimes difficult because there may be multiple displays attached. Rather than trying to guess which display is best, an application should let the system choose a suitable presentation display.

There are two main ways to choose a `https://developer.android.com/reference/kotlin/android/view/Display.html#`.

#### Using the media router to choose a presentation display

The easiest way to choose a presentation display is to use the `https://developer.android.com/reference/kotlin/android/media/MediaRouter.html#` API. The media router service keeps track of which audio and video routes are available on the system. The media router sends notifications whenever routes are selected or unselected or when the preferred presentation display of a route changes. So an application can simply watch for these notifications and show or dismiss a presentation on the preferred presentation display automatically.

The preferred presentation display is the display that the media router recommends that the application should use if it wants to show content on another display. Sometimes there may not be a preferred presentation display in which case the application should show its content locally without using a presentation.

Here's how to use the media router to create and show a presentation on the preferred presentation display using getPresentationDisplay.

```kotlin
MediaRouter mediaRouter = (MediaRouter) context.getSystemService(Context.MEDIA_ROUTER_SERVICE);
  MediaRouter.RouteInfo route = mediaRouter.getSelectedRoute(MediaRouter.ROUTE_TYPE_LIVE_VIDEO);
  if (route != null) {
      Display presentationDisplay = route.getPresentationDisplay();
      if (presentationDisplay != null) {
          Presentation presentation = new MyPresentation(context, presentationDisplay);
          presentation.show();
      }
  }
```

The following sample code from `ApiDemos` demonstrates how to use the media router to automatically switch between showing content in the application's activity and showing the content in a presentation when a presentation display is available.

#### Using the display manager to choose a presentation display

Another way to choose a presentation display is to use the `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#` API directly. The display manager service provides functions to enumerate and describe all displays that are attached to the system including displays that may be used for presentations.

The display manager keeps track of all displays in the system. However, not all displays are appropriate for showing presentations. For example, a presentation is disallowed on the same display as the application's top visible task to prevent it from obscuring its own content. Additionally, presentations on internal displays are restricted and may require the application's task to be focused on a different display to ensure the user is actively interacting with the application. Violating these rules will result in `https://developer.android.com/reference/kotlin/android/view/WindowManager.InvalidDisplayException.html#` being thrown when invoking show. If the conditions for showing a presentation are no longer met while it is already visible, the system will automatically dismiss it and the application will receive the onStop callback. When shown, a presentation will occlude other activities on the target display for security reasons.

Here's how to identify suitable displays for showing presentations using getDisplays and the `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#DISPLAY_CATEGORY_PRESENTATION:kotlin.String` category.

```kotlin
DisplayManager displayManager = (DisplayManager) context.getSystemService(Context.DISPLAY_SERVICE);
  Display[] presentationDisplays = displayManager.getDisplays(DisplayManager.DISPLAY_CATEGORY_PRESENTATION);
  if (presentationDisplays.length > 0) {
      // If there is more than one suitable presentation display, then we could consider
      // giving the user a choice.  For this example, we simply choose the first display
      // which is the one the system recommends as the preferred presentation display.
      Display display = presentationDisplays[0];
      Presentation presentation = new MyPresentation(context, presentationDisplay);
      presentation.show();
  }
```

The following sample code from `ApiDemos` demonstrates how to use the display manager to enumerate displays and show content on multiple presentation displays simultaneously.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON1:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON2:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON3:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEGATIVE:kotlin.Int` The identifier for the negative button. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEUTRAL:kotlin.Int` The identifier for the neutral button. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int` The identifier for the positive button. <br /> | ||

| Public constructors ||
|---|---|
| Presentation Creates a new presentation that is attached to the specified display using the default theme. |
| Presentation Creates a new presentation that is attached to the specified display using the optionally specified theme. |

| Public methods ||
|---|---|
| open [Display](../android.view/Display.md)! | getDisplay Gets the `https://developer.android.com/reference/kotlin/android/view/Display.html#` that this presentation appears on. |
| open [Resources](../android.content.res/Resources.md)! | getResources Gets the `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` that should be used to inflate the layout of this presentation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDisplayChanged Called by the system when the properties of the `https://developer.android.com/reference/kotlin/android/view/Display.html#` to which the presentation is attached have changed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDisplayRemoved Called by the system when the `https://developer.android.com/reference/kotlin/android/view/Display.html#` to which the presentation is attached has been removed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | show Inherited from show. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onStart Called when the dialog is starting. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onStop Called to tell you that you're stopping. |

| Inherited functions ||
|---|---|
| From class Dialog |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | addContentView Add an additional content view to the screen. Added after any existing ones in the screen -- existing views are NOT removed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | cancel Cancel the dialog. This is essentially the same as calling dismiss, but it will also call your `https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener.html#` (if registered). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | closeOptionsMenu <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | create Forces immediate creation of the dialog. Note that you should not override this method to perform dialog creation. Rather, override onCreate. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | dismiss Dismiss this dialog, removing it from the screen. This method can be invoked safely from any thread. Note that you should not override this method to do cleanup when the dialog is dismissed, instead implement that in onStop. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | dispatchGenericMotionEvent Called to process generic motion events. You can override this to intercept all generic motion events before they are dispatched to the window. Be sure to call this implementation for generic motion events that should be handled normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | dispatchKeyEvent Called to process key events. You can override this to intercept all key events before they are dispatched to the window. Be sure to call this implementation for key events that should be handled normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | dispatchKeyShortcutEvent Called to process a key shortcut event. You can override this to intercept all key shortcut events before they are dispatched to the window. Be sure to call this implementation for key shortcut events that should be handled normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | dispatchPopulateAccessibilityEvent Called to process population of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#`s. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | dispatchTouchEvent Called to process touch screen events. You can override this to intercept all touch screen events before they are dispatched to the window. Be sure to call this implementation for touch screen events that should be handled normally. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | dispatchTrackballEvent Called to process trackball events. You can override this to intercept all trackball events before they are dispatched to the window. Be sure to call this implementation for trackball events that should be handled normally. <br /> | | `T` | findViewById Finds the first descendant view with the given ID or `null` if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via show or create). **Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary. <br /> | | ActionBar | getActionBar Retrieve the ActionBar attached to this dialog, if present. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#` | getContext Retrieve the Context this Dialog is running in. <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#?` | getCurrentFocus Call getCurrentFocus on the Window if this Activity to return the currently focused view. <br /> | | `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` | getLayoutInflater <br /> | | `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` | getOnBackInvokedDispatcher Returns the `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` instance associated with the window that this dialog is attached to. <br /> | | Activity | getOwnerActivity Returns the Activity that owns this Dialog. For example, if showDialog is used to show this Dialog, that Activity will be the owner (by default). Depending on how this dialog was created, this may return null. <br /> | | `https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#?` | getSearchEvent During the onSearchRequested() callbacks, this function will return the `https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#` that triggered the callback, if it exists. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getVolumeControlStream <br /> | | `https://developer.android.com/reference/kotlin/android/view/Window.html#?` | getWindow Retrieve the current Window for the activity. This can be used to directly access parts of the Window API that are not available through Activity/Screen. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | hide Hide the dialog, but do not dismiss it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | invalidateOptionsMenu <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isShowing <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onActionModeFinished Called when an action mode has been finished. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeFinished(mode). If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onActionModeStarted Called when an action mode has been started. The appropriate mode callback method will have already been invoked. Note that if you override this method you should always call through to the superclass implementation by calling super.onActionModeStarted(mode). If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onAttachedToWindow Called when the window has been attached to the window manager. See onAttachedToWindow for more information. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onBackPressed Called when the dialog has detected the user's press of the back key. The default implementation simply cancels the dialog (only if it is cancelable), but you can override this to do whatever you want. If you target version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, you should not use this method but register an `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback.html#` on an `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` that you can retrieve using getOnBackInvokedDispatcher. You should also set `android:enableOnBackInvokedCallback="true"` in the application manifest. Alternatively, you can use `androidx.activity.ComponentDialog#getOnBackPressedDispatcher()` for backward compatibility. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onContentChanged This hook is called whenever the content view of the screen changes (due to a call to setContentView or addContentView). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onContextItemSelected <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onContextMenuClosed <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onCreate Similar to android.app.Activity#onCreate, you should initialize your dialog in this method, including calling #setContentView. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onCreateContextMenu <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onCreateOptionsMenu It is usually safe to proxy this call to the owner activity's onCreateOptionsMenu if the client desires the same menu for this Dialog. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onCreatePanelMenu <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#?` | onCreatePanelView <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onDetachedFromWindow Called when the window has been detached from the window manager. See onDetachedFromWindow for more information. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onGenericMotionEvent Called when a generic motion event was not handled by any of the views inside of the dialog. Generic motion events describe joystick movements, mouse hovers, track pad touches, scroll wheel movements and other input events. The getSource of the motion event specifies the class of input that was received. Implementations of this method must examine the bits in the source before processing the event. The following code example shows how this is done. Generic motion events with source class `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_CLASS_POINTER:kotlin.Int` are delivered to the view under the pointer. All other generic motion events are delivered to the focused view. See onGenericMotionEvent for an example of how to handle this event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyDown A key was pressed down. If the focused view didn't want this event, this method is called. Default implementation consumes `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` and, as of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_ESCAPE:kotlin.Int` to later handle them in onKeyUp. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyLongPress Default implementation of onKeyLongPress: always returns false (doesn't handle the event). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyMultiple Default implementation of onKeyMultiple: always returns false (doesn't handle the event). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyShortcut Called when a key shortcut event is not handled by any of the views in the Dialog. Override this method to implement global key shortcuts for the Dialog. Key shortcuts can also be implemented by setting the setShortcut property of menu items. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyUp A key was released. Default implementation consumes `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` and, as of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_ESCAPE:kotlin.Int` to close the dialog. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onMenuItemSelected <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onMenuOpened <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onOptionsItemSelected <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onOptionsMenuClosed <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onPanelClosed <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onPrepareOptionsMenu It is usually safe to proxy this call to the owner activity's onPrepareOptionsMenu if the client desires the same menu for this Dialog. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onPreparePanel <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onRestoreInstanceState Restore the state of the dialog from a previously saved bundle. The default implementation restores the state of the dialog's view hierarchy that was saved in the default implementation of onSaveInstanceState, so be sure to call through to super when overriding unless you want to do all restoring of state yourself. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | onSaveInstanceState Saves the state of the dialog into a bundle. The default implementation saves the state of its view hierarchy, so you'll likely want to call through to super if you override this to save additional state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onSearchRequested This hook is called when the user signals the desire to start a search. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onSearchRequested This hook is called when the user signals the desire to start a search. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onTouchEvent Called when a touch screen event was not handled by any of the views under it. This is most useful to process touch events that happen outside of your window bounds, where there is no view to receive it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onTrackballEvent Called when the trackball was moved and not handled by any of the views inside of the activity. So, for example, if the trackball moves while focus is on a button, you will receive a call here because buttons do not normally do anything with trackball events. The call here happens *before* trackball movements are converted to DPAD key events, which then get sent back to the view hierarchy, and will be processed at the point for things like focus navigation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onWindowAttributesChanged This is called whenever the current window attributes change. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onWindowFocusChanged This hook is called whenever the window focus changes. See onWindowFocusChanged for more information. <br /> | | `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#?` | onWindowStartingActionMode Called when an action mode is being started for this window. Gives the callback an opportunity to handle the action mode in its own unique and beautiful way. If this method returns null the system can choose a way to present the mode or choose not to start the mode at all. This is equivalent to onWindowStartingActionMode with type `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#TYPE_PRIMARY:kotlin.Int`. <br /> | | `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#?` | onWindowStartingActionMode Called when an action mode is being started for this window. Gives the callback an opportunity to handle the action mode in its own unique and beautiful way. If this method returns null the system can choose a way to present the mode or choose not to start the mode at all. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | openContextMenu <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | openOptionsMenu <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | registerForContextMenu <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | requestWindowFeature Enable extended window features. This is a convenience for calling requestFeature. <br /> | | `T` | requireViewById Finds the first descendant view with the given ID or throws an IllegalArgumentException if the ID is invalid (\< 0), there is no matching view in the hierarchy, or the dialog has not yet been fully created (for example, via show or create). **Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setCancelMessage Set a message to be sent when the dialog is canceled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setCancelable Sets whether this dialog is cancelable with the `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setCanceledOnTouchOutside Sets whether this dialog is canceled when touched outside the window's bounds. If setting to true, the dialog is set to be cancelable if not already set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setContentView Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setContentView Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setContentView Set the screen content from a layout resource. The resource will be inflated, adding all top-level views to the screen. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDismissMessage Set a message to be sent when the dialog is dismissed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFeatureDrawable Convenience for calling setFeatureDrawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFeatureDrawableAlpha Convenience for calling setFeatureDrawableAlpha. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFeatureDrawableResource Convenience for calling setFeatureDrawableResource. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFeatureDrawableUri Convenience for calling setFeatureDrawableUri. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOnCancelListener Set a listener to be invoked when the dialog is canceled. This will only be invoked when the dialog is canceled. Cancel events alone will not capture all ways that the dialog might be dismissed. If the creator needs to know when a dialog is dismissed in general, use setOnDismissListener. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOnDismissListener Set a listener to be invoked when the dialog is dismissed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOnKeyListener Sets the callback that will be called if a key is dispatched to the dialog. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOnShowListener Sets a listener to be invoked when the dialog is shown. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOwnerActivity Sets the Activity that owns this dialog. An example use: This Dialog will use the suggested volume control stream of the Activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTitle Set the title text for this dialog's window. The text is retrieved from the resources with the supplied identifier. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTitle Set the title text for this dialog's window. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setVolumeControlStream By default, this will use the owner Activity's suggested stream type. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | takeKeyEvents Request that key events come to this dialog. Use this if your dialog has no views with focus, but the dialog still wants a chance to process key events. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unregisterForContextMenu <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onPointerCaptureChanged Called when pointer capture is enabled or disabled for the current window. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onProvideKeyboardShortcuts Called when Keyboard Shortcuts are requested for the current window. <br /> | ||

## Public constructors

### Presentation

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Presentation(
    outerContext: Context!, 
    display: Display!)
```

Creates a new presentation that is attached to the specified display using the default theme.

| Parameters ||
|---|---|
| `outerContext` | [Context](../android.content/Context.md)!: The context of the application that is showing the presentation. The presentation will create its own context (see getContext) based on this context and information about the associated display. The presentation is associated with the UID of this context for policy enforcement. |
| `display` | [Display](../android.view/Display.md)!: The display to which the presentation should be attached. |

### Presentation

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Presentation(
    outerContext: Context!, 
    display: Display!, 
    theme: Int)
```

Creates a new presentation that is attached to the specified display using the optionally specified theme.

| Parameters ||
|---|---|
| `outerContext` | [Context](../android.content/Context.md)!: The context of the application that is showing the presentation. The presentation will create its own context (see getContext) based on this context and information about the associated display. The presentation is associated with the UID of this context for policy enforcement. From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, the presentation will create its own window context based on this context, information about the associated display. Customizing window type by setType causes the mismatch of the window and the created window context, which leads to `https://developer.android.com/reference/kotlin/android/view/WindowManager.InvalidDisplayException.html#` when invoking show. |
| `display` | [Display](../android.view/Display.md)!: The display to which the presentation should be attached. |
| `theme` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A style resource describing the theme to use for the window. See [Style and Theme Resources](https://developer.android.com/guide/topics/resources/available-resources.html#stylesandthemes) for more information about defining and using styles. This theme is applied on top of the current theme in outerContext. If 0, the default presentation theme will be used. |
| --- | --- |

## Public methods

### getDisplay

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplay(): Display!
```

Gets the `https://developer.android.com/reference/kotlin/android/view/Display.html#` that this presentation appears on.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Display.html#!` | The display. |

### getResources

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResources(): Resources!
```

Gets the `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` that should be used to inflate the layout of this presentation. This resources object has been configured according to the metrics of the display that the presentation appears on.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!` | The presentation resources object. |

### onDisplayChanged

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDisplayChanged(): Unit
```

Called by the system when the properties of the `https://developer.android.com/reference/kotlin/android/view/Display.html#` to which the presentation is attached have changed.
**See Also**

- getDisplay

### onDisplayRemoved

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDisplayRemoved(): Unit
```

Called by the system when the `https://developer.android.com/reference/kotlin/android/view/Display.html#` to which the presentation is attached has been removed. The system automatically calls cancel to dismiss the presentation after sending this event.
**See Also**

- getDisplay

### show

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun show(): Unit
```

Inherited from show. Will throw `https://developer.android.com/reference/kotlin/android/view/WindowManager.InvalidDisplayException.html#` if the specified `https://developer.android.com/reference/kotlin/android/view/Display.html#` can't be found, if it does not have `https://developer.android.com/reference/kotlin/android/view/Display.html#FLAG_PRESENTATION:kotlin.Int` set, or if it is currently not allowed to show a presentation on the display (e.g. it would obscure the application's own task).

## Protected methods

### onStart

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onStart(): Unit
```

Called when the dialog is starting.

### onStop

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onStop(): Unit
```

Called to tell you that you're stopping.
