# android.view

## Interfaces

| [Callback](../android/view/ActionMode.Callback.md) | Callback interface for action modes. |
| --- | --- |
| [VisibilityListener](../android/view/ActionProvider.VisibilityListener.md) | Listens to changes in visibility as reported by `https://developer.android.com/reference/kotlin/android/view/ActionProvider#refreshVisibility()`. |
| [AttachedSurfaceControl](../android/view/AttachedSurfaceControl.md) | Provides an interface to the root-Surface of a View Hierarchy or Window. |
| [FrameCallback](../android/view/Choreographer.FrameCallback.md) | Implement this interface to receive a callback when a new display frame is being rendered. |
| --- | --- |
| [VsyncCallback](../android/view/Choreographer.VsyncCallback.md) | Implement this interface to receive a callback to start the next frame. |
| [CollapsibleActionView](../android/view/CollapsibleActionView.md) | When a `https://developer.android.com/reference/kotlin/android/view/View` implements this interface it will receive callbacks when expanded or collapsed as an action view alongside the optional, app-specified callbacks to `https://developer.android.com/reference/kotlin/android/view/MenuItem.OnActionExpandListener`. |
| [ContextMenu](../android/view/ContextMenu.md) | Extension of `https://developer.android.com/reference/kotlin/android/view/Menu` for context menus providing functionality to modify the header of the context menu. |
| --- | --- |
| [OnContextClickListener](../android/view/GestureDetector.OnContextClickListener.md) | The listener that is used to notify when a context click occurs. |
| [OnDoubleTapListener](../android/view/GestureDetector.OnDoubleTapListener.md) | The listener that is used to notify when a double-tap or a confirmed single-tap occur. |
| [OnGestureListener](../android/view/GestureDetector.OnGestureListener.md) | The listener that is used to notify when gestures occur. |
| --- | --- |
| [Callback](../android/view/InputQueue.Callback.md) | Interface to receive notification of when an InputQueue is associated and dissociated with a thread. |
| [Callback](../android/view/KeyEvent.Callback.md) | <br /> |
| [Factory](../android/view/LayoutInflater.Factory.md) | <br /> |
| --- | --- |
| [Factory2](../android/view/LayoutInflater.Factory2.md) | <br /> |
| [Filter](../android/view/LayoutInflater.Filter.md) | Hook to allow clients of the LayoutInflater to restrict the set of Views that are allowed to be inflated. |
| [Menu](../android/view/Menu.md) | Interface for managing the items in a menu. |
| --- | --- |
| [MenuItem](../android/view/MenuItem.md) | Interface for direct access to a previously created menu item. |
| [OnReceiveContentListener](../android/view/OnReceiveContentListener.md) | Listener for apps to implement handling for insertion of content. |
| [OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md) | Listener for observing the completion of a PixelCopy request. |
| --- | --- |
| [OnScaleGestureListener](../android/view/ScaleGestureDetector.OnScaleGestureListener.md) | The listener for receiving notifications when gestures occur. |
| [ScrollCaptureCallback](../android/view/ScrollCaptureCallback.md) | A ScrollCaptureCallback is responsible for providing rendered snapshots of scrolling content for the scroll capture system. |
| [ScrollFeedbackProvider](../android/view/ScrollFeedbackProvider.md) | Provides feedback to the user for scroll events on a `https://developer.android.com/reference/kotlin/android/view/View`. |
| --- | --- |
| [SubMenu](../android/view/SubMenu.md) | Subclass of `https://developer.android.com/reference/kotlin/android/view/Menu` for sub menus. |
| [OnJankDataListener](../android/view/SurfaceControl.OnJankDataListener.md) | Listener interface to be informed about SurfaceFlinger's jank classification for a specific surface. |
| [TransactionCommittedListener](../android/view/SurfaceControl.TransactionCommittedListener.md) | Interface to handle request to `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction#addTransactionCommittedListener(java.util.concurrent.Executor,%20android.view.SurfaceControl.TransactionCommittedListener)` |
| --- | --- |
| [SurfaceControlInputReceiver](../android/view/SurfaceControlInputReceiver.md) | Provides a mechanism for a SurfaceControl to receive input events. |
| [SurfaceHolder](../android/view/SurfaceHolder.md) | Abstract interface to someone holding a display surface. |
| [SurfaceTextureListener](../android/view/TextureView.SurfaceTextureListener.md) | This listener can be used to be notified when the surface texture associated with this texture view is available. |
| --- | --- |
| [CalledFromWrongThreadListener](../android/view/View.CalledFromWrongThreadListener.md) | A listener that is notified when certain View APIs are called from the wrong thread. |
| [OnApplyWindowInsetsListener](../android/view/View.OnApplyWindowInsetsListener.md) | Listener for applying window insets on a view in a custom way. |
| [OnAttachStateChangeListener](../android/view/View.OnAttachStateChangeListener.md) | Interface definition for a callback to be invoked when this view is attached or detached from its window. |
| --- | --- |
| [OnCapturedPointerListener](../android/view/View.OnCapturedPointerListener.md) | Interface definition for a callback to be invoked when a captured pointer event is being dispatched this view. |
| [OnClickListener](../android/view/View.OnClickListener.md) | Interface definition for a callback to be invoked when a view is clicked. |
| [OnContextClickListener](../android/view/View.OnContextClickListener.md) | Interface definition for a callback to be invoked when a view is context clicked. |
| --- | --- |
| [OnCreateContextMenuListener](../android/view/View.OnCreateContextMenuListener.md) | Interface definition for a callback to be invoked when the context menu for this view is being built. |
| [OnDragListener](../android/view/View.OnDragListener.md) | Interface definition for a listener that's invoked when a drag event is dispatched to this view. |
| [OnFocusChangeListener](../android/view/View.OnFocusChangeListener.md) | Interface definition for a callback to be invoked when the focus state of a view changed. |
| --- | --- |
| [OnGenericMotionListener](../android/view/View.OnGenericMotionListener.md) | Interface definition for a callback to be invoked when a generic motion event is dispatched to this view. |
| [OnHoverListener](../android/view/View.OnHoverListener.md) | Interface definition for a callback to be invoked when a hover event is dispatched to this view. |
| [OnKeyListener](../android/view/View.OnKeyListener.md) | Interface definition for a callback to be invoked when a hardware key event is dispatched to this view. |
| --- | --- |
| [OnLayoutChangeListener](../android/view/View.OnLayoutChangeListener.md) | Interface definition for a callback to be invoked when the layout bounds of a view changes due to layout processing. |
| [OnLongClickListener](../android/view/View.OnLongClickListener.md) | Interface definition for a callback to be invoked when a view has been clicked and held. |
| [OnScrollChangeListener](../android/view/View.OnScrollChangeListener.md) | Interface definition for a callback to be invoked when the scroll X or Y positions of a view change. |
| --- | --- |
| [OnSystemUiVisibilityChangeListener](../android/view/View.OnSystemUiVisibilityChangeListener.md) | Interface definition for a callback to be invoked when the status bar changes visibility. |
| [OnTouchListener](../android/view/View.OnTouchListener.md) | Interface definition for a callback to be invoked when a touch event is dispatched to this view. |
| [OnUnhandledKeyEventListener](../android/view/View.OnUnhandledKeyEventListener.md) | Interface definition for a callback to be invoked when a hardware key event hasn't been handled by the view hierarchy. |
| --- | --- |
| [OnHierarchyChangeListener](../android/view/ViewGroup.OnHierarchyChangeListener.md) | Interface definition for a callback to be invoked when the hierarchy within this view changed. |
| [ViewManager](../android/view/ViewManager.md) | Interface to let you add and remove child views to an Activity. |
| [ViewParent](../android/view/ViewParent.md) | Defines the responsibilities for a class that will be a parent of a View. |
| --- | --- |
| [OnInflateListener](../android/view/ViewStub.OnInflateListener.md) | Listener used to receive a notification after a ViewStub has successfully inflated its layout resource. |
| [OnDrawListener](../android/view/ViewTreeObserver.OnDrawListener.md) | Interface definition for a callback to be invoked when the view tree is about to be drawn. |
| [OnGlobalFocusChangeListener](../android/view/ViewTreeObserver.OnGlobalFocusChangeListener.md) | Interface definition for a callback to be invoked when the focus state within the view tree changes. |
| --- | --- |
| [OnGlobalLayoutListener](../android/view/ViewTreeObserver.OnGlobalLayoutListener.md) | Interface definition for a callback to be invoked when the global layout state or the visibility of views within the view tree changes. |
| [OnPreDrawListener](../android/view/ViewTreeObserver.OnPreDrawListener.md) | Interface definition for a callback to be invoked when the view tree is about to be drawn. |
| [OnScrollChangedListener](../android/view/ViewTreeObserver.OnScrollChangedListener.md) | Interface definition for a callback to be invoked when something in the view tree has been scrolled. |
| --- | --- |
| [OnTouchModeChangeListener](../android/view/ViewTreeObserver.OnTouchModeChangeListener.md) | Interface definition for a callback to be invoked when the touch mode changes. |
| [OnWindowAttachListener](../android/view/ViewTreeObserver.OnWindowAttachListener.md) | Interface definition for a callback to be invoked when the view hierarchy is attached to and detached from its window. |
| [OnWindowFocusChangeListener](../android/view/ViewTreeObserver.OnWindowFocusChangeListener.md) | Interface definition for a callback to be invoked when the view hierarchy's window focus state changes. |
| --- | --- |
| [OnWindowVisibilityChangeListener](../android/view/ViewTreeObserver.OnWindowVisibilityChangeListener.md) | Interface definition for a callback to be invoked when the view hierarchy's window visibility changes. |
| [WindowInsetsAnimationListener](../android/view/ViewTreeObserver.WindowInsetsAnimationListener.md) | Interface definition for a callback to be invoked when window insets animations prepare or end. |
| [Callback](../android/view/Window.Callback.md) | API from a Window back to its caller. |
| --- | --- |
| [OnFrameMetricsAvailableListener](../android/view/Window.OnFrameMetricsAvailableListener.md) | Callback for clients that want frame timing information for each frame rendered by the Window. |
| [OnRestrictedCaptionAreaChangedListener](../android/view/Window.OnRestrictedCaptionAreaChangedListener.md) | Callback for clients that want to be aware of where caption draws content. |
| [WindowInsetsAnimationController](../android/view/WindowInsetsAnimationController.md) | Controller for app-driven animation of system windows. |
| --- | --- |
| [WindowInsetsAnimationControlListener](../android/view/WindowInsetsAnimationControlListener.md) | Listener that encapsulates a request to `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener)`. |
| [WindowInsetsController](../android/view/WindowInsetsController.md) | Interface to control windows that generate insets. |
| [WindowManager](../android/view/WindowManager.md) | The interface that apps use to talk to the window manager. |
| --- | --- |

## Classes

| [AbsSavedState](../android/view/AbsSavedState.md) | A `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` implementation that should be used by inheritance hierarchies to ensure the state of all classes along the chain is saved. |
| --- | --- |
| [ActionMode](../android/view/ActionMode.md) | Represents a contextual mode of the user interface. |
| [ActionProvider](../android/view/ActionProvider.md) | An ActionProvider defines rich menu interaction in a single component. |
| [BlurRegion](../android/view/BlurRegion.md) | The abstract base class defining a region on the SurfaceView that should have a blur applied. |
| --- | --- |
| [Choreographer](../android/view/Choreographer.md) | Coordinates the timing of animations, input and drawing. |
| [ContentInfo](../android/view/ContentInfo.md) | Holds all the relevant data for a request to `https://developer.android.com/reference/kotlin/android/view/View#performReceiveContent(android.view.ContentInfo)`. |
| [ContextThemeWrapper](../android/view/ContextThemeWrapper.md) | A context wrapper that allows you to modify or replace the theme of the wrapped context. |
| --- | --- |
| [Display](../android/view/Display.md) | Provides information about the size and density of a logical display. |
| [DisplayCutout](../android/view/DisplayCutout.md) | Represents the area of the display that is not functional for displaying content. |
| [DisplayShape](../android/view/DisplayShape.md) | A class representing the shape of a display. |
| --- | --- |
| [DragAndDropPermissions](../android/view/DragAndDropPermissions.md) | `https://developer.android.com/reference/kotlin/android/view/DragAndDropPermissions` controls the access permissions for the content URIs associated with a `https://developer.android.com/reference/kotlin/android/view/DragEvent`. |
| [DragEvent](../android/view/DragEvent.md) | Represents an event that is sent out by the system at various times during a drag and drop operation. |
| [FocusFinder](../android/view/FocusFinder.md) | The algorithm used for finding the next focusable view in a given direction from a view that currently has focus. |
| --- | --- |
| [FrameMetrics](../android/view/FrameMetrics.md) | Class containing timing data for various milestones in a frame lifecycle reported by the rendering subsystem. |
| [FrameRateVelocityPoint](../android/view/FrameRateVelocityPoint.md) | Contains the frame rate / velocity values. |
| [FrameStats](../android/view/FrameStats.md) | This is the base class for frame statistics. |
| --- | --- |
| [GestureDetector](../android/view/GestureDetector.md) | Detects various gestures and events using the supplied `https://developer.android.com/reference/kotlin/android/view/MotionEvent`s. |
| [Gravity](../android/view/Gravity.md) | Standard constants and tools for placing an object within a potentially larger container. |
| [HapticFeedbackConstants](../android/view/HapticFeedbackConstants.md) | Constants to be used to perform haptic feedback effects via `https://developer.android.com/reference/kotlin/android/view/View#performHapticFeedback(kotlin.Int)` |
| --- | --- |
| [InputDevice](../android/view/InputDevice.md) | Describes the capabilities of a particular input device. |
| [InputEvent](../android/view/InputEvent.md) | Common base class for input events. |
| [InputQueue](../android/view/InputQueue.md) | An input queue provides a mechanism for an application to receive incoming input events. |
| --- | --- |
| [KeyboardShortcutGroup](../android/view/KeyboardShortcutGroup.md) | A group of `https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo`. |
| [KeyboardShortcutInfo](../android/view/KeyboardShortcutInfo.md) | Information about a Keyboard Shortcut. |
| [KeyCharacterMap](../android/view/KeyCharacterMap.md) | Describes the keys provided by a keyboard device and their associated labels. |
| --- | --- |
| [KeyEvent](../android/view/KeyEvent.md) | Object used to report key and button events. |
| [LayoutInflater](../android/view/LayoutInflater.md) | Instantiates a layout XML file into its corresponding `https://developer.android.com/reference/kotlin/android/view/View` objects. |
| [MenuInflater](../android/view/MenuInflater.md) | This class is used to instantiate menu XML files into Menu objects. |
| --- | --- |
| [MotionEvent](../android/view/MotionEvent.md) | Object used to report movement (mouse, pen, finger, trackball) events. |
| [MotionPredictor](../android/view/MotionPredictor.md) | Calculate motion predictions. |
| [OrientationEventListener](../android/view/OrientationEventListener.md) | Helper class for receiving notifications from the SensorManager when the orientation of the device has changed. |
| --- | --- |
| [OrientationListener](../android/view/OrientationListener.md) | Helper class for receiving notifications from the SensorManager when the orientation of the device has changed. |
| [PixelCopy](../android/view/PixelCopy.md) | Provides a mechanisms to issue pixel copy requests to allow for copy operations from `https://developer.android.com/reference/kotlin/android/view/Surface` to `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` |
| [PointerIcon](../android/view/PointerIcon.md) | Represents an icon that can be used as a mouse pointer. |
| --- | --- |
| [RoundedCorner](../android/view/RoundedCorner.md) | Represents a rounded corner of the display. |
| [RoundedRectBlurRegion](../android/view/RoundedRectBlurRegion.md) | Defines a rounded rectangular blur region on the SurfaceView. |
| [ScaleGestureDetector](../android/view/ScaleGestureDetector.md) | Detects scaling transformation gestures using the supplied `https://developer.android.com/reference/kotlin/android/view/MotionEvent`s. |
| --- | --- |
| [ScrollCaptureSession](../android/view/ScrollCaptureSession.md) | A session represents the scope of interaction between a `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback` and the system during an active scroll capture operation. |
| [ScrollCaptureTarget](../android/view/ScrollCaptureTarget.md) | A target collects the set of contextual information for a ScrollCaptureHandler discovered during a `https://developer.android.com/reference/kotlin/android/view/View#dispatchScrollCaptureSearch(android.graphics.Rect,%20android.graphics.Point,%20java.util.function.Consumer)`. |
| [SearchEvent](../android/view/SearchEvent.md) | Class that contains information about an event that triggers a search. |
| --- | --- |
| [SoundEffectConstants](../android/view/SoundEffectConstants.md) | Constants to be used to play sound effects via `https://developer.android.com/reference/kotlin/android/view/View#playSoundEffect(kotlin.Int)` |
| [Surface](../android/view/Surface.md) | Handle onto a raw buffer that is being managed by the screen compositor. |
| [SurfaceControl](../android/view/SurfaceControl.md) | Handle to an on-screen Surface managed by the system compositor. |
| --- | --- |
| [SurfaceControlViewHost](../android/view/SurfaceControlViewHost.md) | Utility class for adding a View hierarchy to a `https://developer.android.com/reference/kotlin/android/view/SurfaceControl`. |
| [SurfaceView](../android/view/SurfaceView.md) | Provides a dedicated drawing surface embedded inside of a view hierarchy. |
| [TextureView](../android/view/TextureView.md) | A TextureView can be used to display a content stream, such as that coming from a camera preview, a video, or an OpenGL scene. |
| --- | --- |
| [TouchDelegate](../android/view/TouchDelegate.md) | Helper class to handle situations where you want a view to have a larger touch area than its actual view bounds. |
| [VelocityTracker](../android/view/VelocityTracker.md) | Helper for tracking the velocity of motion events, for implementing flinging and other such gestures. |
| [VerifiedInputEvent](../android/view/VerifiedInputEvent.md) | Base class for verified events. |
| --- | --- |
| [VerifiedKeyEvent](../android/view/VerifiedKeyEvent.md) | KeyEvent that has been verified by the system. |
| [VerifiedMotionEvent](../android/view/VerifiedMotionEvent.md) | MotionEvent that has been verified by the system. |
| [VibrationEffectInflater](../android/view/VibrationEffectInflater.md) | Instantiates `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#` objects from Android XML resources. |
| --- | --- |
| [View](../android/view/View.md) | This class represents the basic building block for user interface components. |
| [ViewAnimationUtils](../android/view/ViewAnimationUtils.md) | Defines common utilities for working with View's animations. |
| [ViewConfiguration](../android/view/ViewConfiguration.md) | Contains methods to standard constants used in the UI for timeouts, sizes, and distances. |
| --- | --- |
| [ViewDebug](../android/view/ViewDebug.md) | Various debugging/tracing tools related to `https://developer.android.com/reference/kotlin/android/view/View` and the view hierarchy. |
| [ViewGroup](../android/view/ViewGroup.md) | A `ViewGroup` is a special view that can contain other views (called children.) The view group is the base class for layouts and views containers. |
| [ViewGroupOverlay](../android/view/ViewGroupOverlay.md) | A group overlay is an extra layer that sits on top of a ViewGroup (the "host view") which is drawn after all other content in that view (including the view group's children). |
| --- | --- |
| [ViewOutlineProvider](../android/view/ViewOutlineProvider.md) | Interface by which a View builds its `https://developer.android.com/reference/kotlin/android/graphics/Outline.html#`, used for shadow casting and clipping. |
| [ViewOverlay](../android/view/ViewOverlay.md) | An overlay is an extra layer that sits on top of a View (the "host view") which is drawn after all other content in that view (including children, if the view is a ViewGroup). |
| [ViewPropertyAnimator](../android/view/ViewPropertyAnimator.md) | This class enables automatic and optimized animation of select properties on View objects. |
| --- | --- |
| [ViewStructure](../android/view/ViewStructure.md) | `ViewStructure` is a container for storing additional per-view data generated by `https://developer.android.com/reference/kotlin/android/view/View#onProvideStructure(android.view.ViewStructure)` and `https://developer.android.com/reference/kotlin/android/view/View#onProvideAutofillStructure(android.view.ViewStructure,%20kotlin.Int)`. |
| [ViewStub](../android/view/ViewStub.md) | A ViewStub is an invisible, zero-sized View that can be used to lazily inflate layout resources at runtime. |
| [ViewTreeObserver](../android/view/ViewTreeObserver.md) | A view tree observer is used to register listeners that can be notified of global changes in the view tree. |
| --- | --- |
| [Window](../android/view/Window.md) | Abstract base class for a top-level window look and behavior policy. |
| [WindowAnimationFrameStats](../android/view/WindowAnimationFrameStats.md) | This class contains window animation frame statistics. |
| [WindowContentFrameStats](../android/view/WindowContentFrameStats.md) | This class contains window content frame statistics. |
| --- | --- |
| [WindowId](../android/view/WindowId.md) | Safe identifier for a window. |
| [WindowInsets](../android/view/WindowInsets.md) | Describes a set of insets for window content. |
| [WindowInsetsAnimation](../android/view/WindowInsetsAnimation.md) | Class representing an animation of a set of windows that cause insets. |
| --- | --- |
| [WindowMetrics](../android/view/WindowMetrics.md) | Metrics about a Window, consisting of the bounds and `https://developer.android.com/reference/kotlin/android/view/WindowInsets`. |

## Exceptions

| [InflateException](../android/view/InflateException.md) | This exception is thrown by an inflater on error conditions. |
| --- | --- |
