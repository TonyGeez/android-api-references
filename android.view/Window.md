Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Window

```
abstract class Window
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.Window](../android/view/Window.md) |

Abstract base class for a top-level window look and behavior policy. An instance of this class should be used as the top-level view added to the window manager. It provides standard UI policies such as a background, title area, default key processing, etc.

The framework will instantiate an implementation of this class on behalf of the application.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/view/Window.Callback` API from a Window back to its caller. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/Window.OnFrameMetricsAvailableListener` Callback for clients that want frame timing information for each frame rendered by the Window. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/Window.OnRestrictedCaptionAreaChangedListener` Callback for clients that want to be aware of where caption draws content. |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#DECOR_CAPTION_SHADE_AUTO:kotlin.Int` Flag for letting the theme drive the color of the window caption controls. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#DECOR_CAPTION_SHADE_DARK:kotlin.Int` Flag for setting dark-color controls on the window caption. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#DECOR_CAPTION_SHADE_LIGHT:kotlin.Int` Flag for setting light-color controls on the window caption. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#DEFAULT_FEATURES:kotlin.Int` The default features enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTION_BAR:kotlin.Int` Flag for enabling the Action Bar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int` Flag for requesting an Action Bar that overlays window content. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTION_MODE_OVERLAY:kotlin.Int` Flag for specifying the behavior of action modes when an Action Bar is not present. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int` Enables Activities to run Activity Transitions either through sending or receiving ActivityOptions bundle created with `https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#makeSceneTransitionAnimation(android.app.Activity,%20android.util.Pair)` or `https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#makeSceneTransitionAnimation(android.app.Activity,%20android.view.View,%20kotlin.String)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_CONTENT_TRANSITIONS:kotlin.Int` Flag for requesting that window content changes should be animated using a TransitionManager. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_CONTEXT_MENU:kotlin.Int` Flag for the context menu. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_CUSTOM_TITLE:kotlin.Int` Flag for custom title. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_INDETERMINATE_PROGRESS:kotlin.Int` Flag for indeterminate progress. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_LEFT_ICON:kotlin.Int` Flag for having an icon on the left side of the title bar |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_NO_TITLE:kotlin.Int` Flag for the "no title" feature, turning off the title at the top of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_OPTIONS_PANEL:kotlin.Int` Flag for the "options panel" feature. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_PROGRESS:kotlin.Int` Flag for the progress indicator feature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_RIGHT_ICON:kotlin.Int` Flag for having an icon on the right side of the title bar |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_SWIPE_TO_DISMISS:kotlin.Int` Flag for requesting a decoration-free window that is dismissed by swiping from the left. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#ID_ANDROID_CONTENT:kotlin.Int` The ID that the main layout in the XML layout file should have. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#NAVIGATION_BAR_BACKGROUND_TRANSITION_NAME:kotlin.String` The transitionName for the navigation bar background View when a custom background is used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#PROGRESS_END:kotlin.Int` Ending value for the (primary) progress. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#PROGRESS_INDETERMINATE_OFF:kotlin.Int` Flag for setting the progress bar's indeterminate mode off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#PROGRESS_INDETERMINATE_ON:kotlin.Int` Flag for setting the progress bar's indeterminate mode on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#PROGRESS_SECONDARY_END:kotlin.Int` Highest possible value for the secondary progress. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#PROGRESS_SECONDARY_START:kotlin.Int` Lowest possible value for the secondary progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#PROGRESS_START:kotlin.Int` Starting value for the (primary) progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#PROGRESS_VISIBILITY_OFF:kotlin.Int` Flag for setting the progress bar's visibility to GONE. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#PROGRESS_VISIBILITY_ON:kotlin.Int` Flag for setting the progress bar's visibility to VISIBLE. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#STATUS_BAR_BACKGROUND_TRANSITION_NAME:kotlin.String` The transitionName for the status bar background View when a custom background is used. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Window#Window(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#addContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)(view: https://developer.android.com/reference/kotlin/android/view/View!, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!)` Variation on `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)` to add an additional content view to the screen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#addFlags(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Convenience function to set the flag bits as specified in flags, as per `https://developer.android.com/reference/kotlin/android/view/Window#setFlags(kotlin.Int,%20kotlin.Int)`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#addOnFrameMetricsAvailableListener(android.view.Window.OnFrameMetricsAvailableListener,%20android.os.Handler)(listener: https://developer.android.com/reference/kotlin/android/view/Window.OnFrameMetricsAvailableListener, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Set an observer to collect frame stats for each frame rendered in this window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#clearFlags(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Convenience function to clear the flag bits as specified in flags, as per `https://developer.android.com/reference/kotlin/android/view/Window#setFlags(kotlin.Int,%20kotlin.Int)`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#closeAllPanels()()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#closePanel(kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| open T | `https://developer.android.com/reference/kotlin/android/view/Window#findViewById(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Finds a view that was identified by the `android:id` XML attribute that was processed in android. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getAllowEnterTransitionOverlap()()` Returns how the transition set in `https://developer.android.com/reference/kotlin/android/view/Window#setEnterTransition(android.transition.Transition)` overlaps with the exit transition of the calling Activity. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getAllowReturnTransitionOverlap()()` Returns how the transition set in `https://developer.android.com/reference/kotlin/android/view/Window#setExitTransition(android.transition.Transition)` overlaps with the exit transition of the called Activity when reentering after if finishes. |
| --- | --- |
| [WindowManager.LayoutParams](../android/view/WindowManager.LayoutParams.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getAttributes()()` Retrieve the current window attributes associated with this panel. |
| [Window.Callback](../android/view/Window.Callback.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getCallback()()` Return the current Callback interface for this window. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getColorMode()()` Returns the requested color mode of the window, one of `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_DEFAULT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_WIDE_COLOR_GAMUT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_HDR:kotlin.Int`. |
| --- | --- |
| [Window](../android/view/Window.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getContainer()()` Return the container for this Window. |
| open [Scene](../android/transition/Scene.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getContentScene()()` Retrieve the `https://developer.android.com/reference/kotlin/android/transition/Scene.html#` representing this window's current content. |
| [Context](../android/content/Context.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getContext()()` Return the Context this window policy is running in, for retrieving resources and other information. |
| --- | --- |
| abstract [View](../android/view/View.md)? | `https://developer.android.com/reference/kotlin/android/view/Window#getCurrentFocus()()` Return the view in this Window that currently has focus, or null if there are none. |
| abstract [View](../android/view/View.md) | `https://developer.android.com/reference/kotlin/android/view/Window#getDecorView()()` Retrieve the top-level window decor view (containing the standard window frame/decorations and the client's content inside of that), which can be added as a window to the window manager. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getDefaultFeatures(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Return the feature bits set by default on a window. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getDesiredHdrHeadroom()()` Get the desired amount of HDR headroom as set by `https://developer.android.com/reference/kotlin/android/view/Window#setDesiredHdrHeadroom(kotlin.Float)` |
| open [Transition](../android/transition/Transition.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getEnterTransition()()` Returns the transition used to move Views into the initial scene. |
| open [Transition](../android/transition/Transition.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getExitTransition()()` Returns the Transition that will be used to move Views out of the scene when starting a new Activity. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getFrameRateBoostOnTouchEnabled()()` Get whether frame rate touch boost is enabled `https://developer.android.com/reference/kotlin/android/view/Window#setFrameRateBoostOnTouchEnabled(kotlin.Boolean)` |
| open [WindowInsetsController](../android/view/WindowInsetsController.md)? | `https://developer.android.com/reference/kotlin/android/view/Window#getInsetsController()()` <br /> |
| abstract [LayoutInflater](../android/view/LayoutInflater.md) | `https://developer.android.com/reference/kotlin/android/view/Window#getLayoutInflater()()` Quick access to the `https://developer.android.com/reference/kotlin/android/view/LayoutInflater` instance that this Window retrieved from its Context. |
| --- | --- |
| open [MediaController](../android/media/session/MediaController.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getMediaController()()` Gets the `https://developer.android.com/reference/kotlin/android/media/session/MediaController.html#` that was previously set. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getNavigationBarColor()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getNavigationBarDividerColor()()` Retrieves the color of the navigation bar divider. |
| --- | --- |
| open [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md) | `https://developer.android.com/reference/kotlin/android/view/Window#getOnBackInvokedDispatcher()()` Returns the `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` instance associated with this window. |
| open [Transition](../android/transition/Transition.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getReenterTransition()()` Returns the Transition that will be used to move Views in to the scene when returning from a previously-started Activity. |
| open [Transition](../android/transition/Transition.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getReturnTransition()()` Returns the Transition that will be used to move Views out of the scene when the Window is preparing to close, for example after a call to `https://developer.android.com/reference/kotlin/android/app/Activity.html#finishAfterTransition()`. |
| --- | --- |
| open [AttachedSurfaceControl](../android/view/AttachedSurfaceControl.md)? | `https://developer.android.com/reference/kotlin/android/view/Window#getRootSurfaceControl()()` This will be null before a content view is added, e. |
| open [Transition](../android/transition/Transition.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getSharedElementEnterTransition()()` Returns the Transition that will be used for shared elements transferred into the content Scene. |
| open [Transition](../android/transition/Transition.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getSharedElementExitTransition()()` Returns the Transition to use for shared elements in the launching Window prior to transferring to the launched Activity's Window. |
| --- | --- |
| open [Transition](../android/transition/Transition.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getSharedElementReenterTransition()()` Returns the Transition that will be used for shared elements reentering from a started Activity after it has returned the shared element to it start location. |
| open [Transition](../android/transition/Transition.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getSharedElementReturnTransition()()` Returns the Transition that will be used for shared elements transferred back to a calling Activity. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getSharedElementsUseOverlay()()` Returns `true` when shared elements should use an Overlay during shared element transitions or `false` when they should animate as part of the normal View hierarchy. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getStatusBarColor()()` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](../android/graphics/Rect.md)!\> | `https://developer.android.com/reference/kotlin/android/view/Window#getSystemGestureExclusionRects()()` Retrieve the list of areas within this window's coordinate space where the system should not intercept touch or other pointing device gestures. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getTransitionBackgroundFadeDuration()()` Returns the duration, in milliseconds, of the window background fade when transitioning into or away from an Activity when called with an Activity Transition. |
| --- | --- |
| open [TransitionManager](../android/transition/TransitionManager.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getTransitionManager()()` Retrieve the `https://developer.android.com/reference/kotlin/android/transition/TransitionManager.html#` responsible for for default transitions in this window. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getVolumeControlStream()()` <br /> |
| open [WindowManager](../android/view/WindowManager.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getWindowManager()()` Return the window manager allowing this Window to display its own windows. |
| --- | --- |
| [TypedArray](../android/content/res/TypedArray.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#getWindowStyle()()` Return the `https://developer.android.com/reference/kotlin/android/R.styleable.html#Window:kotlin.IntArray` attributes from this window's theme. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#hasChildren()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#hasFeature(kotlin.Int)(feature: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Query for the availability of a certain feature. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#injectInputEvent(android.view.InputEvent)(event: https://developer.android.com/reference/kotlin/android/view/InputEvent!)` Inject an event to window locally. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#invalidatePanelMenu(kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#isActive()()` <br /> |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#isFloating()()` Return whether this window is being displayed with a floating style (based on the `https://developer.android.com/reference/kotlin/android/R.attr.html#windowIsFloating:kotlin.Int` attribute in the style/theme). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#isFrameRatePowerSavingsBalanced()()` Get whether frameratepowersavingsbalance is enabled for this Window. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#isNavigationBarContrastEnforced()()` Returns whether the system is ensuring that the navigation bar has enough contrast when a fully transparent background is requested. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#isShortcutKey(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)` Is a keypress one of the defined shortcut keys for this window. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#isStatusBarContrastEnforced()()` Returns whether the system is ensuring that the status bar has enough contrast when a fully transparent background is requested. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#isWideColorGamut()()` Returns true if this window's color mode is `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_WIDE_COLOR_GAMUT:kotlin.Int`, the display has a wide color gamut and this device supports wide color gamut rendering. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#makeActive()()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#!)` Should be called when the configuration is changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#openPanel(kotlin.Int,%20android.view.KeyEvent)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)` <br /> |
| --- | --- |
| abstract [View](../android/view/View.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#peekDecorView()()` Retrieve the current decor view, but only if it has already been created; otherwise returns null. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#performContextMenuIdentifierAction(kotlin.Int,%20kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#performPanelIdentifierAction(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#performPanelShortcut(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent,%20kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#registerScrollCaptureCallback(android.view.ScrollCaptureCallback)(callback: https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback)` Used to provide scroll capture support for an arbitrary window. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#removeOnFrameMetricsAvailableListener(android.view.Window.OnFrameMetricsAvailableListener)(listener: https://developer.android.com/reference/kotlin/android/view/Window.OnFrameMetricsAvailableListener!)` Remove observer and stop listening to frame stats for this window. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#requestFeature(kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Enable extended screen features. |
| T | `https://developer.android.com/reference/kotlin/android/view/Window#requireViewById(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Finds a view that was identified by the `android:id` XML attribute that was processed in android. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#restoreHierarchyState(android.os.Bundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` <br /> |
| --- | --- |
| abstract [Bundle](../android/os/Bundle.md)! | `https://developer.android.com/reference/kotlin/android/view/Window#saveHierarchyState()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setAllowEnterTransitionOverlap(kotlin.Boolean)(allow: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Controls how the transition set in `https://developer.android.com/reference/kotlin/android/view/Window#setEnterTransition(android.transition.Transition)` overlaps with the exit transition of the calling Activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setAllowReturnTransitionOverlap(kotlin.Boolean)(allow: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Controls how the transition set in `https://developer.android.com/reference/kotlin/android/view/Window#setExitTransition(android.transition.Transition)` overlaps with the exit transition of the called Activity when reentering after if finishes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setAttributes(android.view.WindowManager.LayoutParams)(a: https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams!)` Specify custom window attributes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setBackgroundBlurRadius(kotlin.Int)(blurRadius: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Blurs the screen behind the window within the bounds of the window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setBackgroundDrawable(android.graphics.drawable.Drawable)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)` Change the background of this window to a custom Drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setBackgroundDrawableResource(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Change the background of this window to a Drawable resource. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setCallback(android.view.Window.Callback)(callback: https://developer.android.com/reference/kotlin/android/view/Window.Callback!)` Set the Callback interface for this window, used to intercept key events and other dynamic operations in the window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setChildDrawable(kotlin.Int,%20android.graphics.drawable.Drawable)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setChildInt(kotlin.Int,%20kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setClipToOutline(kotlin.Boolean)(clipToOutline: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether window content should be clipped to the outline of the window background. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setColorMode(kotlin.Int)(colorMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the requested color mode of the window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setContainer(android.view.Window)(container: https://developer.android.com/reference/kotlin/android/view/Window#!)` Set the container for this window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View!)` Convenience for `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)` set the screen content to an explicit view. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)(view: https://developer.android.com/reference/kotlin/android/view/View!, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!)` Set the screen content to an explicit view. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(kotlin.Int)(layoutResID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Convenience for `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)` to set the screen content from a layout resource. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setDecorCaptionShade(kotlin.Int)(decorCaptionShade: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set what color should the caption controls be. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setDecorFitsSystemWindows(kotlin.Boolean)(decorFitsSystemWindows: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the decor view should fit root-level content views for `https://developer.android.com/reference/kotlin/android/view/WindowInsets`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setDesiredHdrHeadroom(kotlin.Float)(desiredHeadroom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the desired amount of HDR headroom to be used when rendering as a ratio of targetHdrPeakBrightnessInNits / targetSdrWhitePointInNits. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setDimAmount(kotlin.Float)(amount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set the amount of dim behind the window when using `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_DIM_BEHIND:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setDimColor(kotlin.Long)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Set the color of the dim behind the window when using `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_DIM_BEHIND:kotlin.Int`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setElevation(kotlin.Float)(elevation: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the window elevation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setEnterTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)` Sets the Transition that will be used to move Views into the initial scene. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setExitTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)` Sets the Transition that will be used to move Views out of the scene when starting a new Activity. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setFeatureDrawable(kotlin.Int,%20android.graphics.drawable.Drawable)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)` Set an explicit Drawable value for feature of this window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setFeatureDrawableAlpha(kotlin.Int,%20kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, alpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set a custom alpha value for the given drawable feature, controlling how much the background is visible through it. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setFeatureDrawableResource(kotlin.Int,%20kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the value for a drawable feature of this window, from a resource identifier. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setFeatureDrawableUri(kotlin.Int,%20android.net.Uri)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Set the value for a drawable feature of this window, from a URI. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setFeatureInt(kotlin.Int,%20kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the integer value for a feature. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setFlags(kotlin.Int,%20kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the flags of the window, as per the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams` flags. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setFormat(kotlin.Int)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the format of window, as per the PixelFormat types. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setFrameRateBoostOnTouchEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the frame rate touch boost is enabled for this Window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setFrameRatePowerSavingsBalanced(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether frameratepowersavingsbalance is enabled for this Window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setGravity(kotlin.Int)(gravity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the gravity of the window, as per the Gravity constants. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setHideOverlayWindows(kotlin.Boolean)(hide: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Prevent non-system overlay windows from being drawn on top of this window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setIcon(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the primary icon for this window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setLayout(kotlin.Int,%20kotlin.Int)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the width and height layout parameters of the window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setLocalFocus(kotlin.Boolean,%20kotlin.Boolean)(hasFocus: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, inTouchMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set focus locally. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setLogo(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the logo for this window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setMediaController(android.media.session.MediaController)(controller: https://developer.android.com/reference/kotlin/android/media/session/MediaController.html#!)` Sets a `https://developer.android.com/reference/kotlin/android/media/session/MediaController.html#` to send media keys and volume changes to. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setNavigationBarColor(kotlin.Int)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the color of the navigation bar to `color`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setNavigationBarContrastEnforced(kotlin.Boolean)(enforceContrast: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the system should ensure that the navigation bar has enough contrast when a fully transparent background is requested. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setNavigationBarDividerColor(kotlin.Int)(dividerColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Shows a thin line of the specified color between the navigation bar and the app content. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setPreferMinimalPostProcessing(kotlin.Boolean)(isPreferred: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` If `isPreferred` is true, this method requests that the connected display does minimal post processing when this window is visible on the screen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setReenterTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)` Sets the Transition that will be used to move Views in to the scene when returning from a previously-started Activity. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setResizingCaptionDrawable(android.graphics.drawable.Drawable)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)` Set the drawable that is drawn underneath the caption during the resizing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setRestrictedCaptionAreaListener(android.view.Window.OnRestrictedCaptionAreaChangedListener)(listener: https://developer.android.com/reference/kotlin/android/view/Window.OnRestrictedCaptionAreaChangedListener!)` Set a callback for changes of area where caption will draw its content. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setReturnTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)` Sets the Transition that will be used to move Views out of the scene when the Window is preparing to close, for example after a call to `https://developer.android.com/reference/kotlin/android/app/Activity.html#finishAfterTransition()`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setSharedElementEnterTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)` Sets the Transition that will be used for shared elements transferred into the content Scene. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setSharedElementExitTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)` Sets the Transition that will be used for shared elements after starting a new Activity before the shared elements are transferred to the called Activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setSharedElementReenterTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)` Sets the Transition that will be used for shared elements reentering from a started Activity after it has returned the shared element to it start location. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setSharedElementReturnTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)` Sets the Transition that will be used for shared elements transferred back to a calling Activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setSharedElementsUseOverlay(kotlin.Boolean)(sharedElementsUseOverlay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether or not shared elements should use an Overlay during shared element transitions. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setSoftInputMode(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify an explicit soft input mode to use for the window, as per `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#softInputMode:kotlin.Int`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setStatusBarColor(kotlin.Int)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the color of the status bar to `color`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setStatusBarContrastEnforced(kotlin.Boolean)(ensureContrast: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the system should ensure that the status bar has enough contrast when a fully transparent background is requested. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setSustainedPerformanceMode(kotlin.Boolean)(enable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the Sustained Performance requirement for the calling window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setSystemGestureExclusionRects(kotlin.collections.MutableList)(rects: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!>)` Sets a list of areas within this window's coordinate space where the system should not intercept touch or other pointing device gestures. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setTitle(kotlin.CharSequence)(title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Sets a user-facing title for the window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setTitleColor(kotlin.Int)(textColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setTransitionBackgroundFadeDuration(kotlin.Long)(fadeDurationMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the duration, in milliseconds, of the window background fade when transitioning into or away from an Activity when called with an Activity Transition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setTransitionManager(android.transition.TransitionManager)(tm: https://developer.android.com/reference/kotlin/android/transition/TransitionManager.html#!)` Set the `https://developer.android.com/reference/kotlin/android/transition/TransitionManager.html#` to use for default transitions in this window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setType(kotlin.Int)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the type of the window, as per the WindowManager. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setUiOptions(kotlin.Int)(uiOptions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set extra options that will influence the UI for this window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setUiOptions(kotlin.Int,%20kotlin.Int)(uiOptions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set extra options that will influence the UI for this window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setVolumeControlStream(kotlin.Int)(streamType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setWindowAnimations(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify custom animations to use for the window, as per `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#windowAnimations:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setWindowManager(android.view.WindowManager,%20android.os.IBinder,%20kotlin.String)(wm: https://developer.android.com/reference/kotlin/android/view/WindowManager!, appToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!, appName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates and sets the window manager for use by this Window to, for example, display panels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setWindowManager(android.view.WindowManager,%20android.os.IBinder,%20kotlin.String,%20kotlin.Boolean)(wm: https://developer.android.com/reference/kotlin/android/view/WindowManager!, appToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!, appName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, hardwareAccelerated: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Creates and sets the window manager for use by this Window to, for example, display panels. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#superDispatchGenericMotionEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)` Used by custom windows, such as Dialog, to pass the generic motion event further down the view hierarchy. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#superDispatchKeyEvent(android.view.KeyEvent)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)` Used by custom windows, such as Dialog, to pass the key press event further down the view hierarchy. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#superDispatchKeyShortcutEvent(android.view.KeyEvent)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)` Used by custom windows, such as Dialog, to pass the key shortcut press event further down the view hierarchy. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#superDispatchTouchEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)` Used by custom windows, such as Dialog, to pass the touch screen event further down the view hierarchy. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#superDispatchTrackballEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)` Used by custom windows, such as Dialog, to pass the trackball event further down the view hierarchy. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#takeInputQueue(android.view.InputQueue.Callback)(callback: https://developer.android.com/reference/kotlin/android/view/InputQueue.Callback!)` Take ownership of this window's InputQueue. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#takeKeyEvents(kotlin.Boolean)(get: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Request that key events come to this activity. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#takeSurface(android.view.SurfaceHolder.Callback2)(callback: https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback2!)` Take ownership of this window's surface. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#togglePanel(kotlin.Int,%20android.view.KeyEvent)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#unregisterScrollCaptureCallback(android.view.ScrollCaptureCallback)(callback: https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback)` Unregisters a `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback` previously registered with this window. |

| Protected methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getFeatures()()` Return the feature bits that are enabled. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getForcedWindowFlags()()` Return the window flags that have been explicitly set by the client, so will not be modified by `https://developer.android.com/reference/kotlin/android/view/Window#getDecorView()`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#getLocalFeatures()()` Return the feature bits that are being implemented by this Window. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#hasSoftInputMode()()` Has the app specified their own soft input mode? |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#onActive()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Window#setDefaultWindowFormat(kotlin.Int)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the default format of window, as per the PixelFormat types. |
| --- | --- |

## Constants

### DECOR_CAPTION_SHADE_AUTO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DECOR_CAPTION_SHADE_AUTO: Int
```

Flag for letting the theme drive the color of the window caption controls. Use with `https://developer.android.com/reference/kotlin/android/view/Window#setDecorCaptionShade(kotlin.Int)`. This is the default value.

 Value: 0

### DECOR_CAPTION_SHADE_DARK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DECOR_CAPTION_SHADE_DARK: Int
```

Flag for setting dark-color controls on the window caption. Use with `https://developer.android.com/reference/kotlin/android/view/Window#setDecorCaptionShade(kotlin.Int)`.

 Value: 2

### DECOR_CAPTION_SHADE_LIGHT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DECOR_CAPTION_SHADE_LIGHT: Int
```

Flag for setting light-color controls on the window caption. Use with `https://developer.android.com/reference/kotlin/android/view/Window#setDecorCaptionShade(kotlin.Int)`.

 Value: 1

### DEFAULT_FEATURES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val DEFAULT_FEATURES: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/view/Window#getDefaultFeatures(android.content.Context)` instead.*

The default features enabled.

 Value: 65

### FEATURE_ACTION_BAR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_ACTION_BAR: Int
```

Flag for enabling the Action Bar. This is enabled by default for some devices. The Action Bar replaces the title bar and provides an alternate location for an on-screen menu button on some devices.

 Value: 8

### FEATURE_ACTION_BAR_OVERLAY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_ACTION_BAR_OVERLAY: Int
```

Flag for requesting an Action Bar that overlays window content. Normally an Action Bar will sit in the space above window content, but if this feature is requested along with `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTION_BAR:kotlin.Int` it will be layered over the window content itself. This is useful if you would like your app to have more control over how the Action Bar is displayed, such as letting application content scroll beneath an Action Bar with a transparent background or otherwise displaying a transparent/translucent Action Bar over application content.

This mode is especially useful with `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`, which allows you to seamlessly hide the action bar in conjunction with other screen decorations.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN:kotlin.Int`, when an ActionBar is in this mode it will adjust the insets provided to `https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect)` to include the content covered by the action bar, so you can do layout within that space.

 Value: 9

### FEATURE_ACTION_MODE_OVERLAY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_ACTION_MODE_OVERLAY: Int
```

Flag for specifying the behavior of action modes when an Action Bar is not present. If overlay is enabled, the action mode UI will be allowed to cover existing window content.

 Value: 10

### FEATURE_ACTIVITY_TRANSITIONS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_ACTIVITY_TRANSITIONS: Int
```

Enables Activities to run Activity Transitions either through sending or receiving ActivityOptions bundle created with `https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#makeSceneTransitionAnimation(android.app.Activity,%20android.util.Pair)` or `https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#makeSceneTransitionAnimation(android.app.Activity,%20android.view.View,%20kotlin.String)`.

 Value: 13

### FEATURE_CONTENT_TRANSITIONS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CONTENT_TRANSITIONS: Int
```

Flag for requesting that window content changes should be animated using a TransitionManager.

The TransitionManager is set using `https://developer.android.com/reference/kotlin/android/view/Window#setTransitionManager(android.transition.TransitionManager)`. If none is set, a default TransitionManager will be used.

 Value: 12

**See Also**

### FEATURE_CONTEXT_MENU

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CONTEXT_MENU: Int
```

Flag for the context menu. This is enabled by default.

 Value: 6

### FEATURE_CUSTOM_TITLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CUSTOM_TITLE: Int
```

Flag for custom title. You cannot combine this feature with other title features.

 Value: 7

### FEATURE_INDETERMINATE_PROGRESS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_INDETERMINATE_PROGRESS: Int
```

**Deprecated:** *No longer supported starting in API 21.*

Flag for indeterminate progress.

 Value: 5

### FEATURE_LEFT_ICON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_LEFT_ICON: Int
```

Flag for having an icon on the left side of the title bar

 Value: 3

### FEATURE_NO_TITLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_NO_TITLE: Int
```

Flag for the "no title" feature, turning off the title at the top of the screen.

 Value: 1

### FEATURE_OPTIONS_PANEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_OPTIONS_PANEL: Int
```

Flag for the "options panel" feature. This is enabled by default.

 Value: 0

### FEATURE_PROGRESS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_PROGRESS: Int
```

**Deprecated:** *No longer supported starting in API 21.*

Flag for the progress indicator feature.

 Value: 2

### FEATURE_RIGHT_ICON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_RIGHT_ICON: Int
```

Flag for having an icon on the right side of the title bar

 Value: 4

### FEATURE_SWIPE_TO_DISMISS

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SWIPE_TO_DISMISS: Int
```

**Deprecated:** *Swipe-to-dismiss isn't functional anymore.*

Flag for requesting a decoration-free window that is dismissed by swiping from the left.

 Value: 11

### ID_ANDROID_CONTENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ID_ANDROID_CONTENT: Int
```

The ID that the main layout in the XML layout file should have.

 Value: 16908290

### NAVIGATION_BAR_BACKGROUND_TRANSITION_NAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NAVIGATION_BAR_BACKGROUND_TRANSITION_NAME: String
```

The transitionName for the navigation bar background View when a custom background is used.

 Value: "android:navigation:background"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setNavigationBarColor(kotlin.Int)`

### PROGRESS_END

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROGRESS_END: Int
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_PROGRESS:kotlin.Int` and related methods are no longer supported starting in API 21.*

Ending value for the (primary) progress.

 Value: 10000

### PROGRESS_INDETERMINATE_OFF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROGRESS_INDETERMINATE_OFF: Int
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_INDETERMINATE_PROGRESS:kotlin.Int` and related methods are no longer supported starting in API 21.*

Flag for setting the progress bar's indeterminate mode off.

 Value: -4

### PROGRESS_INDETERMINATE_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROGRESS_INDETERMINATE_ON: Int
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_INDETERMINATE_PROGRESS:kotlin.Int` and related methods are no longer supported starting in API 21.*

Flag for setting the progress bar's indeterminate mode on.

 Value: -3

### PROGRESS_SECONDARY_END

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROGRESS_SECONDARY_END: Int
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_PROGRESS:kotlin.Int` and related methods are no longer supported starting in API 21.*

Highest possible value for the secondary progress.

 Value: 30000

### PROGRESS_SECONDARY_START

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROGRESS_SECONDARY_START: Int
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_PROGRESS:kotlin.Int` and related methods are no longer supported starting in API 21.*

Lowest possible value for the secondary progress.

 Value: 20000

### PROGRESS_START

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROGRESS_START: Int
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_PROGRESS:kotlin.Int` and related methods are no longer supported starting in API 21.*

Starting value for the (primary) progress.

 Value: 0

### PROGRESS_VISIBILITY_OFF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROGRESS_VISIBILITY_OFF: Int
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_PROGRESS:kotlin.Int` and related methods are no longer supported starting in API 21.*

Flag for setting the progress bar's visibility to GONE.

 Value: -2

### PROGRESS_VISIBILITY_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROGRESS_VISIBILITY_ON: Int
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_PROGRESS:kotlin.Int` and related methods are no longer supported starting in API 21.*

Flag for setting the progress bar's visibility to VISIBLE.

 Value: -1

### STATUS_BAR_BACKGROUND_TRANSITION_NAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_BAR_BACKGROUND_TRANSITION_NAME: String
```

The transitionName for the status bar background View when a custom background is used.

 Value: "android:status:background"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setStatusBarColor(kotlin.Int)`

## Public constructors

### Window

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Window(context: Context!)
```

## Public methods

### addContentView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addContentView(
    view: View!, 
    params: ViewGroup.LayoutParams!
): Unit
```

Variation on `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)` to add an additional content view to the screen. Added after any existing ones in the screen -- existing views are NOT removed.

| Parameters ||
|---|---|
| `view` | [View](../android/view/View.md)!: The desired content to display. |
| `params` | [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)!: Layout parameters for the view. |

### addFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addFlags(flags: Int): Unit
```

Convenience function to set the flag bits as specified in flags, as per `https://developer.android.com/reference/kotlin/android/view/Window#setFlags(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flag bits to be set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setFlags(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/Window#clearFlags(kotlin.Int)`

### addOnFrameMetricsAvailableListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnFrameMetricsAvailableListener(
    listener: Window.OnFrameMetricsAvailableListener, 
    handler: Handler!
): Unit
```

Set an observer to collect frame stats for each frame rendered in this window. Must be in hardware rendering mode.

| Parameters ||
|---|---|
| `listener` | [Window.OnFrameMetricsAvailableListener](../android/view/Window.OnFrameMetricsAvailableListener.md): This value cannot be `null`. |

### clearFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearFlags(flags: Int): Unit
```

Convenience function to clear the flag bits as specified in flags, as per `https://developer.android.com/reference/kotlin/android/view/Window#setFlags(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flag bits to be cleared. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setFlags(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/Window#addFlags(kotlin.Int)`

### closeAllPanels

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun closeAllPanels(): Unit
```

### closePanel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun closePanel(featureId: Int): Unit
```

### findViewById

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : View!> findViewById(id: Int): T
```

Finds a view that was identified by the `android:id` XML attribute that was processed in android.app.Activity#onCreate.

This will implicitly call `https://developer.android.com/reference/kotlin/android/view/Window#getDecorView()` with all of the associated side-effects.

**Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID to search for |

| Return ||
|---|---|
| `T` | a view with given ID if found, or `null` otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#findViewById(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/Window#requireViewById(kotlin.Int)`

### getAllowEnterTransitionOverlap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllowEnterTransitionOverlap(): Boolean
```

Returns how the transition set in `https://developer.android.com/reference/kotlin/android/view/Window#setEnterTransition(android.transition.Transition)` overlaps with the exit transition of the calling Activity. When true, the transition will start as soon as possible. When false, the transition will wait until the remote exiting transition completes before starting. The default value is true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true when the enter transition should start as soon as possible or false to when it should wait until the exiting transition completes. |

### getAllowReturnTransitionOverlap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllowReturnTransitionOverlap(): Boolean
```

Returns how the transition set in `https://developer.android.com/reference/kotlin/android/view/Window#setExitTransition(android.transition.Transition)` overlaps with the exit transition of the called Activity when reentering after if finishes. When true, the transition will start as soon as possible. When false, the transition will wait until the called Activity's exiting transition completes before starting. The default value is true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true when the transition should start when possible or false when it should wait until the called Activity's exiting transition completes. |

### getAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAttributes(): WindowManager.LayoutParams!
```

Retrieve the current window attributes associated with this panel.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams!` | WindowManager.LayoutParams Either the existing window attributes object, or a freshly created one if there is none. |

### getCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCallback(): Window.Callback!
```

Return the current Callback interface for this window.

### getColorMode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColorMode(): Int
```

Returns the requested color mode of the window, one of `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_DEFAULT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_WIDE_COLOR_GAMUT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_HDR:kotlin.Int`. If `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_WIDE_COLOR_GAMUT:kotlin.Int` was requested it is possible the window will not be put in wide color gamut mode depending on device and display support for that mode. Use `https://developer.android.com/reference/kotlin/android/view/Window#isWideColorGamut()` to determine if the window is currently in wide color gamut mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_WIDE_COLOR_GAMUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_HDR:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setColorMode(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/Display#isWideColorGamut()`
- `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#isScreenWideColorGamut()`

### getContainer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContainer(): Window!
```

Return the container for this Window.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Window#!` | Window The containing window, or null if this is a top-level window. |

### getContentScene

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContentScene(): Scene!
```

Retrieve the `https://developer.android.com/reference/kotlin/android/transition/Scene.html#` representing this window's current content. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_CONTENT_TRANSITIONS:kotlin.Int`.

This method will return null if the current content is not represented by a Scene.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Scene.html#!` | Current Scene being shown or null |

### getContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContext(): Context!
```

Return the Context this window policy is running in, for retrieving resources and other information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | Context The Context that was supplied to the constructor. |

### getCurrentFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCurrentFocus(): View?
```

Return the view in this Window that currently has focus, or null if there are none. Note that this does not look in any containing Window.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View?` | View The current View with focus or null. |

### getDecorView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDecorView(): View
```

Retrieve the top-level window decor view (containing the standard window frame/decorations and the client's content inside of that), which can be added as a window to the window manager.

*Note that calling this function for the first time "locks in" various window characteristics as described in `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)`.*

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View` | Returns the top-level window decor view. This value cannot be `null`. |

### getDefaultFeatures

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDefaultFeatures(context: Context!): Int
```

Return the feature bits set by default on a window.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md)!: The context used to access resources |

### getDesiredHdrHeadroom

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDesiredHdrHeadroom(): Float
```

Get the desired amount of HDR headroom as set by `https://developer.android.com/reference/kotlin/android/view/Window#setDesiredHdrHeadroom(kotlin.Float)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The amount of HDR headroom set, or 0 for automatic/default behavior. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setDesiredHdrHeadroom(kotlin.Float)`

### getEnterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEnterTransition(): Transition!
```

Returns the transition used to move Views into the initial scene. The entering Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as entering is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`. If `transition` is null, entering Views will remain unaffected. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | the Transition to use to move Views into the initial Scene. |

### getExitTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExitTransition(): Transition!
```

Returns the Transition that will be used to move Views out of the scene when starting a new Activity. The exiting Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as exiting is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`. If transition is null, the views will remain unaffected. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | the Transition to use to move Views out of the scene when calling a new Activity. |

### getFrameRateBoostOnTouchEnabled

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFrameRateBoostOnTouchEnabled(): Boolean
```

Get whether frame rate touch boost is enabled `https://developer.android.com/reference/kotlin/android/view/Window#setFrameRateBoostOnTouchEnabled(kotlin.Boolean)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the frame rate touch boost is enabled. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setFrameRateBoostOnTouchEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#getFrameRateBoostOnTouchEnabled()`

### getInsetsController

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInsetsController(): WindowInsetsController?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController?` | The `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController` associated with this window. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#getWindowInsetsController()`

### getLayoutInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLayoutInflater(): LayoutInflater
```

Quick access to the `https://developer.android.com/reference/kotlin/android/view/LayoutInflater` instance that this Window retrieved from its Context.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/LayoutInflater` | LayoutInflater The shared LayoutInflater. This value cannot be `null`. |

### getMediaController

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMediaController(): MediaController!
```

Gets the `https://developer.android.com/reference/kotlin/android/media/session/MediaController.html#` that was previously set.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/session/MediaController.html#!` | The controller which should receive events. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setMediaController(android.media.session.MediaController)`
- `https://developer.android.com/reference/kotlin/android/app/Activity.html#getMediaController()`

### getNavigationBarColor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getNavigationBarColor(): Int
```

**Deprecated:** *This is no longer needed since the setter is deprecated.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the color of the navigation bar. |

### getNavigationBarDividerColor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNavigationBarDividerColor(): Int
```

**Deprecated:** *This is no longer needed since the setter is deprecated.*

Retrieves the color of the navigation bar divider.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The color of the navigation bar divider color. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setNavigationBarColor(kotlin.Int)`

### getOnBackInvokedDispatcher

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOnBackInvokedDispatcher(): OnBackInvokedDispatcher
```

Returns the `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` instance associated with this window.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` | This value cannot be `null`. |

### getReenterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReenterTransition(): Transition!
```

Returns the Transition that will be used to move Views in to the scene when returning from a previously-started Activity. The entering Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as exiting is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | The Transition to use to move Views into the scene when reentering from a previously-started Activity. |

### getReturnTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReturnTransition(): Transition!
```

Returns the Transition that will be used to move Views out of the scene when the Window is preparing to close, for example after a call to `https://developer.android.com/reference/kotlin/android/app/Activity.html#finishAfterTransition()`. The exiting Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as entering is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | The Transition to use to move Views out of the Scene when the Window is preparing to close. |

### getRootSurfaceControl

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRootSurfaceControl(): AttachedSurfaceControl?
```

This will be null before a content view is added, e.g. via #setContentView or `https://developer.android.com/reference/kotlin/android/view/Window#addContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)`. See `https://developer.android.com/reference/kotlin/android/view/View#getRootSurfaceControl()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl?` | The `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl` interface for this Window |

### getSharedElementEnterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSharedElementEnterTransition(): Transition!
```

Returns the Transition that will be used for shared elements transferred into the content Scene. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | Transition to use for sharend elements transferred into the content Scene. |

### getSharedElementExitTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSharedElementExitTransition(): Transition!
```

Returns the Transition to use for shared elements in the launching Window prior to transferring to the launched Activity's Window. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | the Transition to use for shared elements in the launching Window prior to transferring to the launched Activity's Window. |

### getSharedElementReenterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSharedElementReenterTransition(): Transition!
```

Returns the Transition that will be used for shared elements reentering from a started Activity after it has returned the shared element to it start location. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | the Transition that will be used for shared elements reentering from a started Activity after it has returned the shared element to it start location. |

### getSharedElementReturnTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSharedElementReturnTransition(): Transition!
```

Returns the Transition that will be used for shared elements transferred back to a calling Activity. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | Transition to use for sharend elements transferred into the content Scene. |

### getSharedElementsUseOverlay

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSharedElementsUseOverlay(): Boolean
```

Returns `true` when shared elements should use an Overlay during shared element transitions or `false` when they should animate as part of the normal View hierarchy. The default value is true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` when shared elements should use an Overlay during shared element transitions or `false` when they should animate as part of the normal View hierarchy. |

### getStatusBarColor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getStatusBarColor(): Int
```

**Deprecated:** *This is no longer needed since the setter is deprecated.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the color of the status bar. |

### getSystemGestureExclusionRects

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemGestureExclusionRects(): MutableList<Rect!>
```

Retrieve the list of areas within this window's coordinate space where the system should not intercept touch or other pointing device gestures. This is the list as set by `https://developer.android.com/reference/kotlin/android/view/Window#setSystemGestureExclusionRects(kotlin.collections.MutableList)` or an empty list if `https://developer.android.com/reference/kotlin/android/view/Window#setSystemGestureExclusionRects(kotlin.collections.MutableList)` has not been called. It does not include exclusion rects set by this window's view hierarchy.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!>` | a list of system gesture exclusion rects specific to this window. This value cannot be `null`. |

### getTransitionBackgroundFadeDuration

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTransitionBackgroundFadeDuration(): Long
```

Returns the duration, in milliseconds, of the window background fade when transitioning into or away from an Activity when called with an Activity Transition.

When executing the enter transition, the background starts transparent and fades in. This requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`. The default is 300 milliseconds.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The duration of the window background fade to opaque during enter transition. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#getEnterTransition()`

### getTransitionManager

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTransitionManager(): TransitionManager!
```

Retrieve the `https://developer.android.com/reference/kotlin/android/transition/TransitionManager.html#` responsible for for default transitions in this window. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_CONTENT_TRANSITIONS:kotlin.Int`.

This method will return non-null after content has been initialized (e.g. by using #setContentView) if `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_CONTENT_TRANSITIONS:kotlin.Int` has been granted.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/TransitionManager.html#!` | This window's content TransitionManager or null if none is set. |

### getVolumeControlStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getVolumeControlStream(): Int
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Activity.html#getVolumeControlStream()`

### getWindowManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWindowManager(): WindowManager!
```

Return the window manager allowing this Window to display its own windows.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/WindowManager!` | WindowManager The ViewManager. |

### getWindowStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWindowStyle(): TypedArray!
```

Return the `https://developer.android.com/reference/kotlin/android/R.styleable.html#Window:kotlin.IntArray` attributes from this window's theme.

### hasChildren

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasChildren(): Boolean
```

### hasFeature

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasFeature(feature: Int): Boolean
```

Query for the availability of a certain feature.

| Parameters ||
|---|---|
| `feature` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The feature ID to check |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the feature is enabled, false otherwise. |

### injectInputEvent

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun injectInputEvent(event: InputEvent!): Unit
```

Inject an event to window locally.

| Parameters ||
|---|---|
| `event` | [InputEvent](../android/view/InputEvent.md)!: A key or touch event to inject to this window. |

### invalidatePanelMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun invalidatePanelMenu(featureId: Int): Unit
```

### isActive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isActive(): Boolean
```

### isFloating

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isFloating(): Boolean
```

Return whether this window is being displayed with a floating style (based on the `https://developer.android.com/reference/kotlin/android/R.attr.html#windowIsFloating:kotlin.Int` attribute in the style/theme).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the window is configured to be displayed floating on top of whatever is behind it. |

### isFrameRatePowerSavingsBalanced

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFrameRatePowerSavingsBalanced(): Boolean
```

Get whether frameratepowersavingsbalance is enabled for this Window. This allows device to adjust refresh rate as needed and can be useful for power saving. `https://developer.android.com/reference/kotlin/android/view/Window#setFrameRateBoostOnTouchEnabled(kotlin.Boolean)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the frameratepowersavingsbalance is enabled. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setFrameRatePowerSavingsBalanced(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#isFrameRatePowerSavingsBalanced()`

### isNavigationBarContrastEnforced

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isNavigationBarContrastEnforced(): Boolean
```

Returns whether the system is ensuring that the navigation bar has enough contrast when a fully transparent background is requested.

When the navigation bar color has a non-zero alpha value, the value of this property has no effect.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the system is ensuring contrast, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.attr.html#enforceNavigationBarContrast:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/Window#setNavigationBarContrastEnforced(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/Window#setNavigationBarColor(kotlin.Int)`

### isShortcutKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isShortcutKey(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

Is a keypress one of the defined shortcut keys for this window.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the key code from `https://developer.android.com/reference/kotlin/android/view/KeyEvent` to check. |
| `event` | [KeyEvent](../android/view/KeyEvent.md)!: the `https://developer.android.com/reference/kotlin/android/view/KeyEvent` to use to help check. |

### isStatusBarContrastEnforced

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStatusBarContrastEnforced(): Boolean
```

**Deprecated:** *This is not needed since the setter is deprecated.*

Returns whether the system is ensuring that the status bar has enough contrast when a fully transparent background is requested.

When the status bar color has a non-zero alpha value, the value of this property has no effect.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the system is ensuring contrast, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.attr.html#enforceStatusBarContrast:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/Window#setStatusBarContrastEnforced(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/Window#setStatusBarColor(kotlin.Int)`

### isWideColorGamut

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWideColorGamut(): Boolean
```

Returns true if this window's color mode is `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_WIDE_COLOR_GAMUT:kotlin.Int`, the display has a wide color gamut and this device supports wide color gamut rendering.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Display#isWideColorGamut()`
- `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#isScreenWideColorGamut()`

### makeActive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun makeActive(): Unit
```

### onConfigurationChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onConfigurationChanged(newConfig: Configuration!): Unit
```

Should be called when the configuration is changed.

| Parameters ||
|---|---|
| `newConfig` | [Configuration](../android/content/res/Configuration.md)!: The new configuration. |

### openPanel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun openPanel(
    featureId: Int, 
    event: KeyEvent!
): Unit
```

### peekDecorView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun peekDecorView(): View!
```

Retrieve the current decor view, but only if it has already been created; otherwise returns null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View!` | Returns the top-level window decor or null. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#getDecorView()`

### performContextMenuIdentifierAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun performContextMenuIdentifierAction(
    id: Int, 
    flags: Int
): Boolean
```

### performPanelIdentifierAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun performPanelIdentifierAction(
    featureId: Int, 
    id: Int, 
    flags: Int
): Boolean
```

### performPanelShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun performPanelShortcut(
    featureId: Int, 
    keyCode: Int, 
    event: KeyEvent!, 
    flags: Int
): Boolean
```

### registerScrollCaptureCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerScrollCaptureCallback(callback: ScrollCaptureCallback): Unit
```

Used to provide scroll capture support for an arbitrary window. This registeres the given callback with the root view of the window.

| Parameters ||
|---|---|
| `callback` | [ScrollCaptureCallback](../android/view/ScrollCaptureCallback.md): the callback to add. This value cannot be `null`. |

### removeOnFrameMetricsAvailableListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnFrameMetricsAvailableListener(listener: Window.OnFrameMetricsAvailableListener!): Unit
```

Remove observer and stop listening to frame stats for this window.

### requestFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestFeature(featureId: Int): Boolean
```

Enable extended screen features. This must be called before setContentView(). May be called as many times as desired as long as it is before setContentView(). If not called, no extended features will be available. You can not turn off a feature once it is requested. You canot use other title features with `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_CUSTOM_TITLE:kotlin.Int`.

| Parameters ||
|---|---|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired features, defined as constants by Window. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The features that are now set. |

### requireViewById

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : View!> requireViewById(id: Int): T
```

Finds a view that was identified by the `android:id` XML attribute that was processed in android.app.Activity#onCreate, or throws an IllegalArgumentException if the ID is invalid, or there is no matching view in the hierarchy.

**Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID to search for |

| Return ||
|---|---|
| `T` | a view with given ID. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#requireViewById(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/Window#findViewById(kotlin.Int)`

### restoreHierarchyState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun restoreHierarchyState(savedInstanceState: Bundle!): Unit
```

### saveHierarchyState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun saveHierarchyState(): Bundle!
```

### setAllowEnterTransitionOverlap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAllowEnterTransitionOverlap(allow: Boolean): Unit
```

Controls how the transition set in `https://developer.android.com/reference/kotlin/android/view/Window#setEnterTransition(android.transition.Transition)` overlaps with the exit transition of the calling Activity. When true, the transition will start as soon as possible. When false, the transition will wait until the remote exiting transition completes before starting. The default value is true.

| Parameters ||
|---|---|
| `allow` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to start the enter transition when possible or false to wait until the exiting transition completes. |

### setAllowReturnTransitionOverlap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAllowReturnTransitionOverlap(allow: Boolean): Unit
```

Controls how the transition set in `https://developer.android.com/reference/kotlin/android/view/Window#setExitTransition(android.transition.Transition)` overlaps with the exit transition of the called Activity when reentering after if finishes. When true, the transition will start as soon as possible. When false, the transition will wait until the called Activity's exiting transition completes before starting. The default value is true.

| Parameters ||
|---|---|
| `allow` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to start the transition when possible or false to wait until the called Activity's exiting transition completes. |

### setAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAttributes(a: WindowManager.LayoutParams!): Unit
```

Specify custom window attributes. **PLEASE NOTE:** the layout params you give here should generally be from values previously retrieved with `https://developer.android.com/reference/kotlin/android/view/Window#getAttributes()`; you probably do not want to blindly create and apply your own, since this will blow away any values set by the framework that you are not interested in.

| Parameters ||
|---|---|
| `a` | [WindowManager.LayoutParams](../android/view/WindowManager.LayoutParams.md)!: The new window attributes, which will completely override any current values. |

### setBackgroundBlurRadius

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackgroundBlurRadius(blurRadius: Int): Unit
```

Blurs the screen behind the window within the bounds of the window.

The density of the blur is set by the blur radius. The radius defines the size of the neighbouring area, from which pixels will be averaged to form the final color for each pixel. The operation approximates a Gaussian blur. A radius of 0 means no blur. The higher the radius, the denser the blur.

The window background drawable is drawn on top of the blurred region. The blur region bounds and rounded corners will mimic those of the background drawable.

For the blur region to be visible, the window has to be translucent (see `https://developer.android.com/reference/kotlin/android/R.attr.html#windowIsTranslucent:kotlin.Int`) and floating (see `https://developer.android.com/reference/kotlin/android/R.attr.html#windowIsFloating:kotlin.Int`).

Note the difference with `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#setBlurBehindRadius(kotlin.Int)`, which blurs the whole screen behind the window. Background blur blurs the screen behind only within the bounds of the window.

Some devices might not support cross-window blur due to GPU limitations. It can also be disabled at runtime, e.g. during battery saving mode, when multimedia tunneling is used or when minimal post processing is requested. In such situations, no blur will be computed or drawn, resulting in a transparent window background. To avoid this, the app might want to change its theme to one that does not use blurs. To listen for cross-window blur enabled/disabled events, use android.view.WindowManager#addCrossWindowBlurEnabledListener.

| Parameters ||
|---|---|
| `blurRadius` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The blur radius to use for window background blur in pixels |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Window_windowBackgroundBlurRadius:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#setBlurBehindRadius(kotlin.Int)`

### setBackgroundDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setBackgroundDrawable(drawable: Drawable!): Unit
```

Change the background of this window to a custom Drawable. Setting the background to null will make the window be opaque. To make the window transparent, you can use an empty drawable (for instance a ColorDrawable with the color 0 or the system drawable android:drawable/empty.)

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android/graphics/drawable/Drawable.md)!: The new Drawable to use for this window's background. |

### setBackgroundDrawableResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackgroundDrawableResource(resId: Int): Unit
```

Change the background of this window to a Drawable resource. Setting the background to null will make the window be opaque. To make the window transparent, you can use an empty drawable (for instance a ColorDrawable with the color 0 or the system drawable android:drawable/empty.)

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier of a drawable resource which will be installed as the new background. |

### setCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCallback(callback: Window.Callback!): Unit
```

Set the Callback interface for this window, used to intercept key events and other dynamic operations in the window.

| Parameters ||
|---|---|
| `callback` | [Window.Callback](../android/view/Window.Callback.md)!: The desired Callback interface. |

### setChildDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setChildDrawable(
    featureId: Int, 
    drawable: Drawable!
): Unit
```

### setChildInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setChildInt(
    featureId: Int, 
    value: Int
): Unit
```

### setClipToOutline

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setClipToOutline(clipToOutline: Boolean): Unit
```

Sets whether window content should be clipped to the outline of the window background.

| Parameters ||
|---|---|
| `clipToOutline` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether window content should be clipped to the outline of the window background. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#setClipToOutline(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Window_windowClipToOutline:kotlin.Int`

### setColorMode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorMode(colorMode: Int): Unit
```

Sets the requested color mode of the window. The requested the color mode might override the window's pixel `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#format:kotlin.Int`.

The requested color mode must be one of `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_DEFAULT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_WIDE_COLOR_GAMUT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_HDR:kotlin.Int`.

The requested color mode is not guaranteed to be honored. Please refer to `https://developer.android.com/reference/kotlin/android/view/Window#getColorMode()` for more information.

Note: This does not impact SurfaceViews or SurfaceControls, as those have their own independent color mode and HDR parameters.

| Parameters ||
|---|---|
| `colorMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_WIDE_COLOR_GAMUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_HDR:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#getColorMode()`
- `https://developer.android.com/reference/kotlin/android/view/Display#isWideColorGamut()`
- `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#isScreenWideColorGamut()`

### setContainer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContainer(container: Window!): Unit
```

Set the container for this window. If not set, the DecorWindow operates as a top-level window; otherwise, it negotiates with the container to display itself appropriately.

| Parameters ||
|---|---|
| `container` | [Window](../android/view/Window.md)!: The desired containing Window. |

### setContentView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setContentView(view: View!): Unit
```

Convenience for `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)` set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarhcy.

| Parameters ||
|---|---|
| `view` | [View](../android/view/View.md)!: The desired content to display. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)`

### setContentView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setContentView(
    view: View!, 
    params: ViewGroup.LayoutParams!
): Unit
```

Set the screen content to an explicit view. This view is placed directly into the screen's view hierarchy. It can itself be a complex view hierarchy.

Note that calling this function "locks in" various characteristics of the window that can not, from this point forward, be changed: the features that have been requested with `https://developer.android.com/reference/kotlin/android/view/Window#requestFeature(kotlin.Int)`, and certain window flags as described in `https://developer.android.com/reference/kotlin/android/view/Window#setFlags(kotlin.Int,%20kotlin.Int)`.

If `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_CONTENT_TRANSITIONS:kotlin.Int` is set, the window's TransitionManager will be used to animate content from the current content View to view.

| Parameters ||
|---|---|
| `view` | [View](../android/view/View.md)!: The desired content to display. |
| `params` | [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)!: Layout parameters for the view. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#getTransitionManager()`
- `https://developer.android.com/reference/kotlin/android/view/Window#setTransitionManager(android.transition.TransitionManager)`

### setContentView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setContentView(layoutResID: Int): Unit
```

Convenience for `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)` to set the screen content from a layout resource. The resource will be inflated, adding all top-level views to the screen.

| Parameters ||
|---|---|
| `layoutResID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource ID to be inflated. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)`

### setDecorCaptionShade

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setDecorCaptionShade(decorCaptionShade: Int): Unit
```

Set what color should the caption controls be. By default the system will try to determine the color from the theme. You can overwrite this by using `https://developer.android.com/reference/kotlin/android/view/Window#DECOR_CAPTION_SHADE_DARK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/Window#DECOR_CAPTION_SHADE_LIGHT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/Window#DECOR_CAPTION_SHADE_AUTO:kotlin.Int`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#DECOR_CAPTION_SHADE_DARK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/Window#DECOR_CAPTION_SHADE_LIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/Window#DECOR_CAPTION_SHADE_AUTO:kotlin.Int`

### setDecorFitsSystemWindows

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDecorFitsSystemWindows(decorFitsSystemWindows: Boolean): Unit
```

**Deprecated:** *Make space in the container views to prevent the critical elements from getting obscured by `https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars()` or `https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#displayCutout()` instead.*

Sets whether the decor view should fit root-level content views for `https://developer.android.com/reference/kotlin/android/view/WindowInsets`.

If set to `true`, the framework will inspect the now deprecated `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_LAYOUT_FLAGS:kotlin.Int` as well the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#SOFT_INPUT_ADJUST_RESIZE:kotlin.Int` flag and fits content according to these flags.

If set to `false`, the framework will not fit the content view to the insets and will just pass through the `https://developer.android.com/reference/kotlin/android/view/WindowInsets` to the content view.

If the app targets `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` or above, the behavior will be like setting this to `false`, and cannot be changed.

| Parameters ||
|---|---|
| `decorFitsSystemWindows` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the decor view should fit root-level content views for insets. |

### setDesiredHdrHeadroom

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDesiredHdrHeadroom(desiredHeadroom: Float): Unit
```

Sets the desired amount of HDR headroom to be used when rendering as a ratio of targetHdrPeakBrightnessInNits / targetSdrWhitePointInNits. Only applies when `https://developer.android.com/reference/kotlin/android/view/Window#setColorMode(kotlin.Int)` is `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_HDR:kotlin.Int`

By default the system will choose an amount of HDR headroom that is appropriate for the underlying device capabilities \& bit-depth of the panel. However, for some types of content this can end up being more headroom than necessary or desired. An example would be a messaging app or gallery thumbnail view where some amount of HDR pop is desired without overly influencing the perceived brightness of the majority SDR content. This can also be used to animate in/out of an HDR range for smoother transitions.

Note: The actual amount of HDR headroom that will be given is subject to a variety of factors such as ambient conditions, display capabilities, or bit-depth limitations. See `https://developer.android.com/reference/kotlin/android/view/Display#getHdrSdrRatio()` for more information as well as how to query the current value.

Note: This does not impact SurfaceViews or SurfaceControls, as those have their own independent desired HDR headroom and HDR capabilities.

| Parameters ||
|---|---|
| `desiredHeadroom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount of HDR headroom that is desired. Must be \>= 1.0 (no HDR) and \<= 10,000.0. Passing 0.0 will reset to the default, automatically chosen value. Value is between 0.0f and 10000.0f inclusive |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#getDesiredHdrHeadroom()`
- `https://developer.android.com/reference/kotlin/android/view/Display#getHdrSdrRatio()`

### setDimAmount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDimAmount(amount: Float): Unit
```

Set the amount of dim behind the window when using `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_DIM_BEHIND:kotlin.Int`. This overrides the default dim amount of that is selected by the Window based on its theme.

| Parameters ||
|---|---|
| `amount` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The new dim amount, from 0 for no dim to 1 for full dim. |

### setDimColor

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDimColor(color: Long): Unit
```

Set the color of the dim behind the window when using `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_DIM_BEHIND:kotlin.Int`. This overrides the default dim color that is selected by the Window based on its theme.

| Parameters ||
|---|---|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The new dim color. |

### setElevation

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setElevation(elevation: Float): Unit
```

Sets the window elevation.

Changes to this property take effect immediately and will cause the window surface to be recreated. This is an expensive operation and as a result, this property should not be animated.

| Parameters ||
|---|---|
| `elevation` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The window elevation. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#setElevation(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Window_windowElevation:kotlin.Int`

### setEnterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setEnterTransition(transition: Transition!): Unit
```

Sets the Transition that will be used to move Views into the initial scene. The entering Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as entering is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`. If `transition` is null, entering Views will remain unaffected.

| Parameters ||
|---|---|
| `transition` | [Transition](../android/transition/Transition.md)!: The Transition to use to move Views into the initial Scene. |

### setExitTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExitTransition(transition: Transition!): Unit
```

Sets the Transition that will be used to move Views out of the scene when starting a new Activity. The exiting Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as exiting is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`. If transition is null, the views will remain unaffected. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Parameters ||
|---|---|
| `transition` | [Transition](../android/transition/Transition.md)!: The Transition to use to move Views out of the scene when calling a new Activity. |

### setFeatureDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setFeatureDrawable(
    featureId: Int, 
    drawable: Drawable!
): Unit
```

Set an explicit Drawable value for feature of this window. You must have called requestFeature(featureId) before calling this function.

| Parameters ||
|---|---|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired drawable feature to change. Features are constants defined by Window. |
| `drawable` | [Drawable](../android/graphics/drawable/Drawable.md)!: A Drawable object to display. |

### setFeatureDrawableAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setFeatureDrawableAlpha(
    featureId: Int, 
    alpha: Int
): Unit
```

Set a custom alpha value for the given drawable feature, controlling how much the background is visible through it.

| Parameters ||
|---|---|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired drawable feature to change. Features are constants defined by Window. |
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The alpha amount, 0 is completely transparent and 255 is completely opaque. |

### setFeatureDrawableResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setFeatureDrawableResource(
    featureId: Int, 
    resId: Int
): Unit
```

Set the value for a drawable feature of this window, from a resource identifier. You must have called requestFeature(featureId) before calling this function.

| Parameters ||
|---|---|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired drawable feature to change, defined as a constant by Window. |
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource identifier of the desired image. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getDrawable(kotlin.Int)`

### setFeatureDrawableUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setFeatureDrawableUri(
    featureId: Int, 
    uri: Uri!
): Unit
```

Set the value for a drawable feature of this window, from a URI. You must have called requestFeature(featureId) before calling this function.

The only URI currently supported is "content:", specifying an image in a content provider.

| Parameters ||
|---|---|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired drawable feature to change. Features are constants defined by Window. |
| `uri` | [Uri](../android/net/Uri.md)!: The desired URI. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/ImageView.html#setImageURI(android.net.Uri)`

### setFeatureInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setFeatureInt(
    featureId: Int, 
    value: Int
): Unit
```

Set the integer value for a feature. The range of the value depends on the feature being set. For `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_PROGRESS:kotlin.Int`, it should go from 0 to 10000. At 10000 the progress is complete and the indicator hidden.

| Parameters ||
|---|---|
| `featureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired feature to change. Features are constants defined by Window. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value for the feature. The interpretation of this value is feature-specific. |

### setFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFlags(
    flags: Int, 
    mask: Int
): Unit
```

Set the flags of the window, as per the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams` flags.

Note that some flags must be set before the window decoration is created (by the first call to `https://developer.android.com/reference/kotlin/android/view/Window#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)` or `https://developer.android.com/reference/kotlin/android/view/Window#getDecorView()`: `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_LAYOUT_IN_SCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_LAYOUT_INSET_DECOR:kotlin.Int`. These will be set for you based on the `https://developer.android.com/reference/kotlin/android/R.attr.html#windowIsFloating:kotlin.Int` attribute.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new window flags (see WindowManager.LayoutParams). |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which of the window flag bits to modify. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#addFlags(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/Window#clearFlags(kotlin.Int)`

### setFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFormat(format: Int): Unit
```

Set the format of window, as per the PixelFormat types. This overrides the default format that is selected by the Window based on its window decorations.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new window format (see PixelFormat). Use PixelFormat.UNKNOWN to allow the Window to select the format. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`

### setFrameRateBoostOnTouchEnabled

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFrameRateBoostOnTouchEnabled(enabled: Boolean): Unit
```

Sets whether the frame rate touch boost is enabled for this Window. When enabled, the frame rate will be boosted when a user touches the Window.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the frame rate touch boost is enabled. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#getFrameRateBoostOnTouchEnabled()`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#setFrameRateBoostOnTouchEnabled(kotlin.Boolean)`

### setFrameRatePowerSavingsBalanced

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFrameRatePowerSavingsBalanced(enabled: Boolean): Unit
```

Set whether frameratepowersavingsbalance is enabled for this Window. This allows device to adjust refresh rate as needed and can be useful for power saving.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the frameratepowersavingsbalance is enabled. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#isFrameRatePowerSavingsBalanced()`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#setFrameRatePowerSavingsBalanced(kotlin.Boolean)`

### setGravity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setGravity(gravity: Int): Unit
```

Set the gravity of the window, as per the Gravity constants. This controls how the window manager is positioned in the overall window; it is only useful when using WRAP_CONTENT for the layout width or height.

| Parameters ||
|---|---|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired gravity constant. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Gravity`
- `https://developer.android.com/reference/kotlin/android/view/Window#setLayout(kotlin.Int,%20kotlin.Int)`

### setHideOverlayWindows

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setHideOverlayWindows(hide: Boolean): Unit
```

Prevent non-system overlay windows from being drawn on top of this window. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#HIDE_OVERLAY_WINDOWS:kotlin.String`

| Parameters ||
|---|---|
| `hide` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether non-system overlay windows should be hidden. |

### setIcon

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIcon(resId: Int): Unit
```

Set the primary icon for this window.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): resource ID of a drawable to set |

### setLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayout(
    width: Int, 
    height: Int
): Unit
```

Set the width and height layout parameters of the window. The default for both of these is MATCH_PARENT; you can change them to WRAP_CONTENT or an absolute value to make a window that is not full-screen.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired layout width of the window. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired layout height of the window. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams#height:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams#width:kotlin.Int`

### setLocalFocus

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLocalFocus(
    hasFocus: Boolean, 
    inTouchMode: Boolean
): Unit
```

Set focus locally. The window should have the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_LOCAL_FOCUS_MODE:kotlin.Int` flag set already.

| Parameters ||
|---|---|
| `hasFocus` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether this window has focus or not. |
| `inTouchMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether this window is in touch mode or not. |

### setLogo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLogo(resId: Int): Unit
```

Set the logo for this window. A logo is often shown in place of an `https://developer.android.com/reference/kotlin/android/view/Window#setIcon(kotlin.Int)` but is generally wider and communicates window title information as well.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): resource ID of a drawable to set |

### setMediaController

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMediaController(controller: MediaController!): Unit
```

Sets a `https://developer.android.com/reference/kotlin/android/media/session/MediaController.html#` to send media keys and volume changes to. If set, this should be preferred for all media keys and volume requests sent to this window.

| Parameters ||
|---|---|
| `controller` | [MediaController](../android/media/session/MediaController.md)!: The controller for the session which should receive media keys and volume changes. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Activity.html#setMediaController(android.media.session.MediaController)`

### setNavigationBarColor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setNavigationBarColor(color: Int): Unit
```

**Deprecated:** *Draw proper background behind `https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#navigationBars()` or `https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#tappableElement()` instead.*

Sets the color of the navigation bar to `color`. For this to take effect, the window must be drawing the system bar backgrounds with `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_TRANSLUCENT_NAVIGATION:kotlin.Int` must not be set. If `color` is not opaque, consider setting `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_STABLE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int`.

The transitionName for the view background will be "android:navigation:background".

If the color is transparent and the window enforces the navigation bar contrast, the system will determine whether a scrim is necessary and draw one on behalf of the app to ensure that the navigation bar has enough contrast with the contents of this app, and set an appropriate effective bar background accordingly.

If the app targets `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` or above, the color will be transparent and cannot be changed.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setNavigationBarContrastEnforced(kotlin.Boolean)`

### setNavigationBarContrastEnforced

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNavigationBarContrastEnforced(enforceContrast: Boolean): Unit
```

Sets whether the system should ensure that the navigation bar has enough contrast when a fully transparent background is requested.

If set to this value, the system will determine whether a scrim is necessary to ensure that the navigation bar has enough contrast with the contents of this app, and set an appropriate effective bar background color accordingly.

When the navigation bar color has a non-zero alpha value, the value of this property has no effect.
**See Also**

- `https://developer.android.com/reference/kotlin/android/R.attr.html#enforceNavigationBarContrast:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/Window#isNavigationBarContrastEnforced()`
- `https://developer.android.com/reference/kotlin/android/view/Window#setNavigationBarColor(kotlin.Int)`

### setNavigationBarDividerColor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNavigationBarDividerColor(dividerColor: Int): Unit
```

**Deprecated:** *Draw proper background behind `https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#navigationBars()` or `https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#tappableElement()` instead.*

Shows a thin line of the specified color between the navigation bar and the app content.

For this to take effect, the window must be drawing the system bar backgrounds with `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_TRANSLUCENT_NAVIGATION:kotlin.Int` must not be set.

If the app targets `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` or above, the color will be transparent and cannot be changed.

| Parameters ||
|---|---|
| `dividerColor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The color of the thin line. |

### setPreferMinimalPostProcessing

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPreferMinimalPostProcessing(isPreferred: Boolean): Unit
```

If `isPreferred` is true, this method requests that the connected display does minimal post processing when this window is visible on the screen. Otherwise, it requests that the display switches back to standard image processing.

By default, the display does not do minimal post processing and if this is desired, this method should not be used. It should be used with `isPreferred=true` when low latency has a higher priority than image enhancement processing (e.g. for games or video conferencing). The display will automatically go back into standard image processing mode when no window requesting minimal posst processing is visible on screen anymore. `setPreferMinimalPostProcessing(false)` can be used if `setPreferMinimalPostProcessing(true)` was previously called for this window and minimal post processing is no longer required.

If the Display sink is connected via HDMI, the device will begin to send infoframes with Auto Low Latency Mode enabled and Game Content Type. This will switch the connected display to a minimal image processing mode (if available), which reduces latency, improving the user experience for gaming or video conferencing applications. For more information, see HDMI 2.1 specification.

If the Display sink has an internal connection or uses some other protocol than HDMI, effects may be similar but implementation-defined.

The ability to switch to a mode with minimal post proessing may be disabled by a user setting in the system settings menu. In that case, this method does nothing.

| Parameters ||
|---|---|
| `isPreferred` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Indicates whether minimal post processing is preferred for this window (`isPreferred=true`) or not (`isPreferred=false`). |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#FLAG_PREFER_MINIMAL_POST_PROCESSING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/Display#isMinimalPostProcessingSupported()`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#preferMinimalPostProcessing:kotlin.Boolean`

### setReenterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setReenterTransition(transition: Transition!): Unit
```

Sets the Transition that will be used to move Views in to the scene when returning from a previously-started Activity. The entering Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as exiting is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`. If transition is null, the views will remain unaffected. If nothing is set, the default will be to use the same transition as `https://developer.android.com/reference/kotlin/android/view/Window#setExitTransition(android.transition.Transition)`. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Parameters ||
|---|---|
| `transition` | [Transition](../android/transition/Transition.md)!: The Transition to use to move Views into the scene when reentering from a previously-started Activity. |

### setResizingCaptionDrawable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setResizingCaptionDrawable(drawable: Drawable!): Unit
```

Set the drawable that is drawn underneath the caption during the resizing. During the resizing the caption might not be drawn fast enough to match the new dimensions. There is a second caption drawn underneath it that will be fast enough. By default the caption is constructed from the theme. You can provide a drawable, that will be drawn instead to better match your application. Starting in Android 15, this API is a no-op. New window decorations introduced in Android 14 are drawn in SystemUI process, and OEMs are responsible to make them responsive to resizing. There is no need to set a background drawable to improve UX anymore since then. Additionally, the foremost activity can draw in caption areas starting in Android 15. Check `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_CAPTION_BARS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsAppearance(kotlin.Int,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/view/WindowInsets#getBoundingRects(kotlin.Int)`.

### setRestrictedCaptionAreaListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRestrictedCaptionAreaListener(listener: Window.OnRestrictedCaptionAreaChangedListener!): Unit
```

Set a callback for changes of area where caption will draw its content.

| Parameters ||
|---|---|
| `listener` | [Window.OnRestrictedCaptionAreaChangedListener](../android/view/Window.OnRestrictedCaptionAreaChangedListener.md)!: Callback that will be called when the area changes. |

### setReturnTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setReturnTransition(transition: Transition!): Unit
```

Sets the Transition that will be used to move Views out of the scene when the Window is preparing to close, for example after a call to `https://developer.android.com/reference/kotlin/android/app/Activity.html#finishAfterTransition()`. The exiting Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as entering is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`. If `transition` is null, entering Views will remain unaffected. If nothing is set, the default will be to use the same value as set in `https://developer.android.com/reference/kotlin/android/view/Window#setEnterTransition(android.transition.Transition)`.

| Parameters ||
|---|---|
| `transition` | [Transition](../android/transition/Transition.md)!: The Transition to use to move Views out of the Scene when the Window is preparing to close. |

### setSharedElementEnterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSharedElementEnterTransition(transition: Transition!): Unit
```

Sets the Transition that will be used for shared elements transferred into the content Scene. Typical Transitions will affect size and location, such as `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#`. A null value will cause transferred shared elements to blink to the final position. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Parameters ||
|---|---|
| `transition` | [Transition](../android/transition/Transition.md)!: The Transition to use for shared elements transferred into the content Scene. |

### setSharedElementExitTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSharedElementExitTransition(transition: Transition!): Unit
```

Sets the Transition that will be used for shared elements after starting a new Activity before the shared elements are transferred to the called Activity. If the shared elements must animate during the exit transition, this Transition should be used. Upon completion, the shared elements may be transferred to the started Activity. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Parameters ||
|---|---|
| `transition` | [Transition](../android/transition/Transition.md)!: The Transition to use for shared elements in the launching Window prior to transferring to the launched Activity's Window. |

### setSharedElementReenterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSharedElementReenterTransition(transition: Transition!): Unit
```

Sets the Transition that will be used for shared elements reentering from a started Activity after it has returned the shared element to it start location. If no value is set, this will default to `https://developer.android.com/reference/kotlin/android/view/Window#setSharedElementExitTransition(android.transition.Transition)`. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Parameters ||
|---|---|
| `transition` | [Transition](../android/transition/Transition.md)!: The Transition to use for shared elements in the launching Window after the shared element has returned to the Window. |

### setSharedElementReturnTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSharedElementReturnTransition(transition: Transition!): Unit
```

Sets the Transition that will be used for shared elements transferred back to a calling Activity. Typical Transitions will affect size and location, such as `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#`. A null value will cause transferred shared elements to blink to the final position. If no value is set, the default will be to use the same value as `https://developer.android.com/reference/kotlin/android/view/Window#setSharedElementEnterTransition(android.transition.Transition)`. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

| Parameters ||
|---|---|
| `transition` | [Transition](../android/transition/Transition.md)!: The Transition to use for shared elements transferred out of the content Scene. |

### setSharedElementsUseOverlay

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSharedElementsUseOverlay(sharedElementsUseOverlay: Boolean): Unit
```

Sets whether or not shared elements should use an Overlay during shared element transitions. The default value is true.

| Parameters ||
|---|---|
| `sharedElementsUseOverlay` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` indicates that shared elements should be transitioned with an Overlay or `false` to transition within the normal View hierarchy. |

### setSoftInputMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSoftInputMode(mode: Int): Unit
```

Specify an explicit soft input mode to use for the window, as per `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#softInputMode:kotlin.Int`. Providing anything besides "unspecified" here will override the input mode the window would normally retrieve from its theme.

### setStatusBarColor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setStatusBarColor(color: Int): Unit
```

**Deprecated:** *Draw proper background behind `https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#statusBars()`} instead.*

Sets the color of the status bar to `color`. For this to take effect, the window must be drawing the system bar backgrounds with `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_TRANSLUCENT_STATUS:kotlin.Int` must not be set. If `color` is not opaque, consider setting `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_STABLE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int`.

The transitionName for the view background will be "android:status:background".

If the color is transparent and the window enforces the status bar contrast, the system will determine whether a scrim is necessary and draw one on behalf of the app to ensure that the status bar has enough contrast with the contents of this app, and set an appropriate effective bar background accordingly.

If the app targets `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` or above, the color will be transparent and cannot be changed.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setNavigationBarContrastEnforced(kotlin.Boolean)`

### setStatusBarContrastEnforced

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStatusBarContrastEnforced(ensureContrast: Boolean): Unit
```

**Deprecated:** *Draw proper background behind `https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#statusBars()`} instead.*

Sets whether the system should ensure that the status bar has enough contrast when a fully transparent background is requested.

If set to this value, the system will determine whether a scrim is necessary to ensure that the status bar has enough contrast with the contents of this app, and set an appropriate effective bar background color accordingly.

When the status bar color has a non-zero alpha value, the value of this property has no effect.
**See Also**

- `https://developer.android.com/reference/kotlin/android/R.attr.html#enforceStatusBarContrast:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/Window#isStatusBarContrastEnforced()`
- `https://developer.android.com/reference/kotlin/android/view/Window#setStatusBarColor(kotlin.Int)`

### setSustainedPerformanceMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSustainedPerformanceMode(enable: Boolean): Unit
```

Sets the Sustained Performance requirement for the calling window.

| Parameters ||
|---|---|
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): disables or enables the mode. |

### setSystemGestureExclusionRects

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSystemGestureExclusionRects(rects: MutableList<Rect!>): Unit
```

Sets a list of areas within this window's coordinate space where the system should not intercept touch or other pointing device gestures.

This method should be used by apps that make use of `https://developer.android.com/reference/kotlin/android/view/Window#takeSurface(android.view.SurfaceHolder.Callback2)` and do not have a view hierarchy available. Apps that do have a view hierarchy should use `https://developer.android.com/reference/kotlin/android/view/View#setSystemGestureExclusionRects(kotlin.collections.MutableList)` instead. This method does not modify or replace the gesture exclusion rects populated by individual views in this window's view hierarchy using `https://developer.android.com/reference/kotlin/android/view/View#setSystemGestureExclusionRects(kotlin.collections.MutableList)`.

Use this to tell the system which specific sub-areas of a view need to receive gesture input in order to function correctly in the presence of global system gestures that may conflict. For example, if the system wishes to capture swipe-in-from-screen-edge gestures to provide system-level navigation functionality, a view such as a navigation drawer container can mark the left (or starting) edge of itself as requiring gesture capture priority using this API. The system may then choose to relax its own gesture recognition to allow the app to consume the user's gesture. It is not necessary for an app to register exclusion rects for broadly spanning regions such as the entirety of a `ScrollView` or for simple press and release click targets such as `Button`. Mark an exclusion rect when interacting with a view requires a precision touch gesture in a small area in either the X or Y dimension, such as an edge swipe or dragging a `SeekBar` thumb.

Do not modify the provided list after this method is called.

| Parameters ||
|---|---|
| `rects` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](../android/graphics/Rect.md)!\>: A list of precision gesture regions that this window needs to function correctly. This value cannot be `null`. |

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setTitle(title: CharSequence!): Unit
```

Sets a user-facing title for the window.

This title may be shown to the user in the window's title or action bar if the `https://developer.android.com/reference/kotlin/android/view/Window#requestFeature(kotlin.Int)` provide such a bar. It is also exposed through `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getTitle()`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#setTitle(kotlin.CharSequence)`

### setTitleColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setTitleColor(textColor: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

### setTransitionBackgroundFadeDuration

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTransitionBackgroundFadeDuration(fadeDurationMillis: Long): Unit
```

Sets the duration, in milliseconds, of the window background fade when transitioning into or away from an Activity when called with an Activity Transition.

When executing the enter transition, the background starts transparent and fades in. This requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`. The default is 300 milliseconds.

| Parameters ||
|---|---|
| `fadeDurationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The duration of the window background fade to or from opaque during enter transition. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setEnterTransition(android.transition.Transition)`

### setTransitionManager

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTransitionManager(tm: TransitionManager!): Unit
```

Set the `https://developer.android.com/reference/kotlin/android/transition/TransitionManager.html#` to use for default transitions in this window. Requires `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_CONTENT_TRANSITIONS:kotlin.Int`.

| Parameters ||
|---|---|
| `tm` | [TransitionManager](../android/transition/TransitionManager.md)!: The TransitionManager to use for scene changes. |

### setType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setType(type: Int): Unit
```

Set the type of the window, as per the WindowManager.LayoutParams types.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new window type (see WindowManager.LayoutParams). |

### setUiOptions

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUiOptions(uiOptions: Int): Unit
```

Set extra options that will influence the UI for this window.

| Parameters ||
|---|---|
| `uiOptions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags specifying extra options for this window. |

### setUiOptions

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUiOptions(
    uiOptions: Int, 
    mask: Int
): Unit
```

Set extra options that will influence the UI for this window. Only the bits filtered by mask will be modified.

| Parameters ||
|---|---|
| `uiOptions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags specifying extra options for this window. |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags specifying which options should be modified. Others will remain unchanged. |

### setVolumeControlStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setVolumeControlStream(streamType: Int): Unit
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Activity.html#setVolumeControlStream(kotlin.Int)`

### setWindowAnimations

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWindowAnimations(resId: Int): Unit
```

Specify custom animations to use for the window, as per `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#windowAnimations:kotlin.Int`. Providing anything besides 0 here will override the animations the window would normally retrieve from its theme.

### setWindowManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWindowManager(
    wm: WindowManager!, 
    appToken: IBinder!, 
    appName: String!
): Unit
```

Creates and sets the window manager for use by this Window to, for example, display panels. This is *not* used for displaying the Window itself -- that must be done by the client.

If `wm` is not `null`, this method will creates a new instance of `https://developer.android.com/reference/kotlin/android/view/WindowManager` with this window attached based on `wm`, or, otherwise, based on `https://developer.android.com/reference/kotlin/android/view/WindowManager` obtained from `https://developer.android.com/reference/kotlin/android/view/Window#getContext()`.

| Parameters ||
|---|---|
| `wm` | [WindowManager](../android/view/WindowManager.md)!: the window manager for adding new windows. |
| `appToken` | [IBinder](../android/os/IBinder.md)!: the token of the window, which applies to the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#token:android.os.IBinder` of `https://developer.android.com/reference/kotlin/android/view/Window#getAttributes()` if specified. |
| `appName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the window, which applies to the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#getTitle()` of `https://developer.android.com/reference/kotlin/android/view/Window#getAttributes()` if specified. |
| --- | --- |

### setWindowManager

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWindowManager(
    wm: WindowManager!, 
    appToken: IBinder!, 
    appName: String!, 
    hardwareAccelerated: Boolean
): Unit
```

Creates and sets the window manager for use by this Window to, for example, display panels. This is *not* used for displaying the Window itself -- that must be done by the client.

If `wm` is not `null`, this method will creates a new instance of `https://developer.android.com/reference/kotlin/android/view/WindowManager` with this window attached based on `wm`, or, otherwise, based on `https://developer.android.com/reference/kotlin/android/view/WindowManager` obtained from `https://developer.android.com/reference/kotlin/android/view/Window#getContext()`.

| Parameters ||
|---|---|
| `wm` | [WindowManager](../android/view/WindowManager.md)!: the window manager for adding new windows. |
| `appToken` | [IBinder](../android/os/IBinder.md)!: the token of the window, which applies to the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#token:android.os.IBinder` of `https://developer.android.com/reference/kotlin/android/view/Window#getAttributes()` if specified. |
| `appName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the window, which applies to the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#getTitle()` of `https://developer.android.com/reference/kotlin/android/view/Window#getAttributes()` if specified. |
| --- | --- |
| `hardwareAccelerated` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): indicate whether this window or its sub-windows should be hardware accelerated, which is default to `false`. |

### superDispatchGenericMotionEvent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun superDispatchGenericMotionEvent(event: MotionEvent!): Boolean
```

Used by custom windows, such as Dialog, to pass the generic motion event further down the view hierarchy. Application developers should not need to implement or call this.

### superDispatchKeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun superDispatchKeyEvent(event: KeyEvent!): Boolean
```

Used by custom windows, such as Dialog, to pass the key press event further down the view hierarchy. Application developers should not need to implement or call this.

### superDispatchKeyShortcutEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun superDispatchKeyShortcutEvent(event: KeyEvent!): Boolean
```

Used by custom windows, such as Dialog, to pass the key shortcut press event further down the view hierarchy. Application developers should not need to implement or call this.

### superDispatchTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun superDispatchTouchEvent(event: MotionEvent!): Boolean
```

Used by custom windows, such as Dialog, to pass the touch screen event further down the view hierarchy. Application developers should not need to implement or call this.

### superDispatchTrackballEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun superDispatchTrackballEvent(event: MotionEvent!): Boolean
```

Used by custom windows, such as Dialog, to pass the trackball event further down the view hierarchy. Application developers should not need to implement or call this.

### takeInputQueue

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun takeInputQueue(callback: InputQueue.Callback!): Unit
```

Take ownership of this window's InputQueue. The window will no longer read and dispatch input events from the queue; it is your responsibility to do so.

### takeKeyEvents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun takeKeyEvents(get: Boolean): Unit
```

Request that key events come to this activity. Use this if your activity has no views with focus, but the activity still wants a chance to process key events.

### takeSurface

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun takeSurface(callback: SurfaceHolder.Callback2!): Unit
```

Take ownership of this window's surface. The window's view hierarchy will no longer draw into the surface, though it will otherwise continue to operate (such as for receiving input events). The given SurfaceHolder callback will be used to tell you about state changes to the surface.

### togglePanel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun togglePanel(
    featureId: Int, 
    event: KeyEvent!
): Unit
```

### unregisterScrollCaptureCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterScrollCaptureCallback(callback: ScrollCaptureCallback): Unit
```

Unregisters a `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback` previously registered with this window.

| Parameters ||
|---|---|
| `callback` | [ScrollCaptureCallback](../android/view/ScrollCaptureCallback.md): the callback to remove. This value cannot be `null`. |

## Protected methods

### getFeatures

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun getFeatures(): Int
```

Return the feature bits that are enabled. This is the set of features that were given to requestFeature(), and are being handled by this Window itself or its container. That is, it is the set of requested features that you can actually use.

To do: add a public version of this API that allows you to check for features by their feature ID.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int The feature bits. |

### getForcedWindowFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun getForcedWindowFlags(): Int
```

Return the window flags that have been explicitly set by the client, so will not be modified by `https://developer.android.com/reference/kotlin/android/view/Window#getDecorView()`.

### getLocalFeatures

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun getLocalFeatures(): Int
```

Return the feature bits that are being implemented by this Window. This is the set of features that were given to requestFeature(), and are being handled by only this Window itself, not by its containers.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int The feature bits. |

### hasSoftInputMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun hasSoftInputMode(): Boolean
```

Has the app specified their own soft input mode?

### onActive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun onActive(): Unit
```

### setDefaultWindowFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setDefaultWindowFormat(format: Int): Unit
```

Set the default format of window, as per the PixelFormat types. This is the format that will be used unless the client specifies in explicit format with setFormat();

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new window format (see PixelFormat). |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window#setFormat(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`
