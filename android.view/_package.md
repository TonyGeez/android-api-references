# android.view

## Interfaces

| [Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback) | Callback interface for action modes. |
| [VisibilityListener](https://developer.android.com/reference/kotlin/android/view/ActionProvider.VisibilityListener) | Listens to changes in visibility as reported by `https://developer.android.com/reference/kotlin/android/view/ActionProvider#refreshVisibility()`. |
| [AttachedSurfaceControl](https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl) | Provides an interface to the root-Surface of a View Hierarchy or Window. |
| [FrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameCallback) | Implement this interface to receive a callback when a new display frame is being rendered. |
| [VsyncCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.VsyncCallback) | Implement this interface to receive a callback to start the next frame. |
| [CollapsibleActionView](https://developer.android.com/reference/kotlin/android/view/CollapsibleActionView) | When a `https://developer.android.com/reference/kotlin/android/view/View` implements this interface it will receive callbacks when expanded or collapsed as an action view alongside the optional, app-specified callbacks to `https://developer.android.com/reference/kotlin/android/view/MenuItem.OnActionExpandListener`. |
| [ContextMenu](https://developer.android.com/reference/kotlin/android/view/ContextMenu) | Extension of `https://developer.android.com/reference/kotlin/android/view/Menu` for context menus providing functionality to modify the header of the context menu. |
| [OnContextClickListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnContextClickListener) | The listener that is used to notify when a context click occurs. |
| [OnDoubleTapListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnDoubleTapListener) | The listener that is used to notify when a double-tap or a confirmed single-tap occur. |
| [OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener) | The listener that is used to notify when gestures occur. |
| [Callback](https://developer.android.com/reference/kotlin/android/view/InputQueue.Callback) | Interface to receive notification of when an InputQueue is associated and dissociated with a thread. |
| [Callback](https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback) | <br /> |
| [Factory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory) | <br /> |
| [Factory2](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory2) | <br /> |
| [Filter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Filter) | Hook to allow clients of the LayoutInflater to restrict the set of Views that are allowed to be inflated. |
| [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) | Interface for managing the items in a menu. |
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem) | Interface for direct access to a previously created menu item. |
| [OnReceiveContentListener](https://developer.android.com/reference/kotlin/android/view/OnReceiveContentListener) | Listener for apps to implement handling for insertion of content. |
| [OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener) | Listener for observing the completion of a PixelCopy request. |
| [OnScaleGestureListener](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener) | The listener for receiving notifications when gestures occur. |
| [ScrollCaptureCallback](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback) | A ScrollCaptureCallback is responsible for providing rendered snapshots of scrolling content for the scroll capture system. |
| [ScrollFeedbackProvider](https://developer.android.com/reference/kotlin/android/view/ScrollFeedbackProvider) | Provides feedback to the user for scroll events on a `https://developer.android.com/reference/kotlin/android/view/View`. |
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu) | Subclass of `https://developer.android.com/reference/kotlin/android/view/Menu` for sub menus. |
| [OnJankDataListener](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListener) | Listener interface to be informed about SurfaceFlinger's jank classification for a specific surface. |
| [TransactionCommittedListener](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.TransactionCommittedListener) | Interface to handle request to `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction#addTransactionCommittedListener(java.util.concurrent.Executor,%20android.view.SurfaceControl.TransactionCommittedListener)` |
| [SurfaceControlInputReceiver](https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver) | Provides a mechanism for a SurfaceControl to receive input events. |
| [SurfaceHolder](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder) | Abstract interface to someone holding a display surface. |
| [SurfaceTextureListener](https://developer.android.com/reference/kotlin/android/view/TextureView.SurfaceTextureListener) | This listener can be used to be notified when the surface texture associated with this texture view is available. |
| [CalledFromWrongThreadListener](https://developer.android.com/reference/kotlin/android/view/View.CalledFromWrongThreadListener) | A listener that is notified when certain View APIs are called from the wrong thread. |
| [OnApplyWindowInsetsListener](https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener) | Listener for applying window insets on a view in a custom way. |
| [OnAttachStateChangeListener](https://developer.android.com/reference/kotlin/android/view/View.OnAttachStateChangeListener) | Interface definition for a callback to be invoked when this view is attached or detached from its window. |
| [OnCapturedPointerListener](https://developer.android.com/reference/kotlin/android/view/View.OnCapturedPointerListener) | Interface definition for a callback to be invoked when a captured pointer event is being dispatched this view. |
| [OnClickListener](https://developer.android.com/reference/kotlin/android/view/View.OnClickListener) | Interface definition for a callback to be invoked when a view is clicked. |
| [OnContextClickListener](https://developer.android.com/reference/kotlin/android/view/View.OnContextClickListener) | Interface definition for a callback to be invoked when a view is context clicked. |
| [OnCreateContextMenuListener](https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener) | Interface definition for a callback to be invoked when the context menu for this view is being built. |
| [OnDragListener](https://developer.android.com/reference/kotlin/android/view/View.OnDragListener) | Interface definition for a listener that's invoked when a drag event is dispatched to this view. |
| [OnFocusChangeListener](https://developer.android.com/reference/kotlin/android/view/View.OnFocusChangeListener) | Interface definition for a callback to be invoked when the focus state of a view changed. |
| [OnGenericMotionListener](https://developer.android.com/reference/kotlin/android/view/View.OnGenericMotionListener) | Interface definition for a callback to be invoked when a generic motion event is dispatched to this view. |
| [OnHoverListener](https://developer.android.com/reference/kotlin/android/view/View.OnHoverListener) | Interface definition for a callback to be invoked when a hover event is dispatched to this view. |
| [OnKeyListener](https://developer.android.com/reference/kotlin/android/view/View.OnKeyListener) | Interface definition for a callback to be invoked when a hardware key event is dispatched to this view. |
| [OnLayoutChangeListener](https://developer.android.com/reference/kotlin/android/view/View.OnLayoutChangeListener) | Interface definition for a callback to be invoked when the layout bounds of a view changes due to layout processing. |
| [OnLongClickListener](https://developer.android.com/reference/kotlin/android/view/View.OnLongClickListener) | Interface definition for a callback to be invoked when a view has been clicked and held. |
| [OnScrollChangeListener](https://developer.android.com/reference/kotlin/android/view/View.OnScrollChangeListener) | Interface definition for a callback to be invoked when the scroll X or Y positions of a view change. |
| [OnSystemUiVisibilityChangeListener](https://developer.android.com/reference/kotlin/android/view/View.OnSystemUiVisibilityChangeListener) | Interface definition for a callback to be invoked when the status bar changes visibility. |
| [OnTouchListener](https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener) | Interface definition for a callback to be invoked when a touch event is dispatched to this view. |
| [OnUnhandledKeyEventListener](https://developer.android.com/reference/kotlin/android/view/View.OnUnhandledKeyEventListener) | Interface definition for a callback to be invoked when a hardware key event hasn't been handled by the view hierarchy. |
| [OnHierarchyChangeListener](https://developer.android.com/reference/kotlin/android/view/ViewGroup.OnHierarchyChangeListener) | Interface definition for a callback to be invoked when the hierarchy within this view changed. |
| [ViewManager](https://developer.android.com/reference/kotlin/android/view/ViewManager) | Interface to let you add and remove child views to an Activity. |
| [ViewParent](https://developer.android.com/reference/kotlin/android/view/ViewParent) | Defines the responsibilities for a class that will be a parent of a View. |
| [OnInflateListener](https://developer.android.com/reference/kotlin/android/view/ViewStub.OnInflateListener) | Listener used to receive a notification after a ViewStub has successfully inflated its layout resource. |
| [OnDrawListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnDrawListener) | Interface definition for a callback to be invoked when the view tree is about to be drawn. |
| [OnGlobalFocusChangeListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnGlobalFocusChangeListener) | Interface definition for a callback to be invoked when the focus state within the view tree changes. |
| [OnGlobalLayoutListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnGlobalLayoutListener) | Interface definition for a callback to be invoked when the global layout state or the visibility of views within the view tree changes. |
| [OnPreDrawListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnPreDrawListener) | Interface definition for a callback to be invoked when the view tree is about to be drawn. |
| [OnScrollChangedListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnScrollChangedListener) | Interface definition for a callback to be invoked when something in the view tree has been scrolled. |
| [OnTouchModeChangeListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnTouchModeChangeListener) | Interface definition for a callback to be invoked when the touch mode changes. |
| [OnWindowAttachListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnWindowAttachListener) | Interface definition for a callback to be invoked when the view hierarchy is attached to and detached from its window. |
| [OnWindowFocusChangeListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnWindowFocusChangeListener) | Interface definition for a callback to be invoked when the view hierarchy's window focus state changes. |
| [OnWindowVisibilityChangeListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnWindowVisibilityChangeListener) | Interface definition for a callback to be invoked when the view hierarchy's window visibility changes. |
| [WindowInsetsAnimationListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.WindowInsetsAnimationListener) | Interface definition for a callback to be invoked when window insets animations prepare or end. |
| [Callback](https://developer.android.com/reference/kotlin/android/view/Window.Callback) | API from a Window back to its caller. |
| [OnFrameMetricsAvailableListener](https://developer.android.com/reference/kotlin/android/view/Window.OnFrameMetricsAvailableListener) | Callback for clients that want frame timing information for each frame rendered by the Window. |
| [OnRestrictedCaptionAreaChangedListener](https://developer.android.com/reference/kotlin/android/view/Window.OnRestrictedCaptionAreaChangedListener) | Callback for clients that want to be aware of where caption draws content. |
| [WindowInsetsAnimationController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController) | Controller for app-driven animation of system windows. |
| [WindowInsetsAnimationControlListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener) | Listener that encapsulates a request to `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener)`. |
| [WindowInsetsController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController) | Interface to control windows that generate insets. |
| [WindowManager](https://developer.android.com/reference/kotlin/android/view/WindowManager) | The interface that apps use to talk to the window manager. |

## Classes

| [AbsSavedState](https://developer.android.com/reference/kotlin/android/view/AbsSavedState) | A `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` implementation that should be used by inheritance hierarchies to ensure the state of all classes along the chain is saved. |
| [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode) | Represents a contextual mode of the user interface. |
| [ActionProvider](https://developer.android.com/reference/kotlin/android/view/ActionProvider) | An ActionProvider defines rich menu interaction in a single component. |
| [BlurRegion](https://developer.android.com/reference/kotlin/android/view/BlurRegion) | The abstract base class defining a region on the SurfaceView that should have a blur applied. |
| [Choreographer](https://developer.android.com/reference/kotlin/android/view/Choreographer) | Coordinates the timing of animations, input and drawing. |
| [ContentInfo](https://developer.android.com/reference/kotlin/android/view/ContentInfo) | Holds all the relevant data for a request to `https://developer.android.com/reference/kotlin/android/view/View#performReceiveContent(android.view.ContentInfo)`. |
| [ContextThemeWrapper](https://developer.android.com/reference/kotlin/android/view/ContextThemeWrapper) | A context wrapper that allows you to modify or replace the theme of the wrapped context. |
| [Display](https://developer.android.com/reference/kotlin/android/view/Display) | Provides information about the size and density of a logical display. |
| [DisplayCutout](https://developer.android.com/reference/kotlin/android/view/DisplayCutout) | Represents the area of the display that is not functional for displaying content. |
| [DisplayShape](https://developer.android.com/reference/kotlin/android/view/DisplayShape) | A class representing the shape of a display. |
| [DragAndDropPermissions](https://developer.android.com/reference/kotlin/android/view/DragAndDropPermissions) | `https://developer.android.com/reference/kotlin/android/view/DragAndDropPermissions` controls the access permissions for the content URIs associated with a `https://developer.android.com/reference/kotlin/android/view/DragEvent`. |
| [DragEvent](https://developer.android.com/reference/kotlin/android/view/DragEvent) | Represents an event that is sent out by the system at various times during a drag and drop operation. |
| [FocusFinder](https://developer.android.com/reference/kotlin/android/view/FocusFinder) | The algorithm used for finding the next focusable view in a given direction from a view that currently has focus. |
| [FrameMetrics](https://developer.android.com/reference/kotlin/android/view/FrameMetrics) | Class containing timing data for various milestones in a frame lifecycle reported by the rendering subsystem. |
| [FrameRateVelocityPoint](https://developer.android.com/reference/kotlin/android/view/FrameRateVelocityPoint) | Contains the frame rate / velocity values. |
| [FrameStats](https://developer.android.com/reference/kotlin/android/view/FrameStats) | This is the base class for frame statistics. |
| [GestureDetector](https://developer.android.com/reference/kotlin/android/view/GestureDetector) | Detects various gestures and events using the supplied `https://developer.android.com/reference/kotlin/android/view/MotionEvent`s. |
| [Gravity](https://developer.android.com/reference/kotlin/android/view/Gravity) | Standard constants and tools for placing an object within a potentially larger container. |
| [HapticFeedbackConstants](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants) | Constants to be used to perform haptic feedback effects via `https://developer.android.com/reference/kotlin/android/view/View#performHapticFeedback(kotlin.Int)` |
| [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice) | Describes the capabilities of a particular input device. |
| [InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent) | Common base class for input events. |
| [InputQueue](https://developer.android.com/reference/kotlin/android/view/InputQueue) | An input queue provides a mechanism for an application to receive incoming input events. |
| [KeyboardShortcutGroup](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutGroup) | A group of `https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo`. |
| [KeyboardShortcutInfo](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo) | Information about a Keyboard Shortcut. |
| [KeyCharacterMap](https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap) | Describes the keys provided by a keyboard device and their associated labels. |
| [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent) | Object used to report key and button events. |
| [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater) | Instantiates a layout XML file into its corresponding `https://developer.android.com/reference/kotlin/android/view/View` objects. |
| [MenuInflater](https://developer.android.com/reference/kotlin/android/view/MenuInflater) | This class is used to instantiate menu XML files into Menu objects. |
| [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) | Object used to report movement (mouse, pen, finger, trackball) events. |
| [MotionPredictor](https://developer.android.com/reference/kotlin/android/view/MotionPredictor) | Calculate motion predictions. |
| [OrientationEventListener](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener) | Helper class for receiving notifications from the SensorManager when the orientation of the device has changed. |
| [OrientationListener](https://developer.android.com/reference/kotlin/android/view/OrientationListener) | Helper class for receiving notifications from the SensorManager when the orientation of the device has changed. |
| [PixelCopy](https://developer.android.com/reference/kotlin/android/view/PixelCopy) | Provides a mechanisms to issue pixel copy requests to allow for copy operations from `https://developer.android.com/reference/kotlin/android/view/Surface` to `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` |
| [PointerIcon](https://developer.android.com/reference/kotlin/android/view/PointerIcon) | Represents an icon that can be used as a mouse pointer. |
| [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner) | Represents a rounded corner of the display. |
| [RoundedRectBlurRegion](https://developer.android.com/reference/kotlin/android/view/RoundedRectBlurRegion) | Defines a rounded rectangular blur region on the SurfaceView. |
| [ScaleGestureDetector](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector) | Detects scaling transformation gestures using the supplied `https://developer.android.com/reference/kotlin/android/view/MotionEvent`s. |
| [ScrollCaptureSession](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureSession) | A session represents the scope of interaction between a `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback` and the system during an active scroll capture operation. |
| [ScrollCaptureTarget](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget) | A target collects the set of contextual information for a ScrollCaptureHandler discovered during a `https://developer.android.com/reference/kotlin/android/view/View#dispatchScrollCaptureSearch(android.graphics.Rect,%20android.graphics.Point,%20java.util.function.Consumer)`. |
| [SearchEvent](https://developer.android.com/reference/kotlin/android/view/SearchEvent) | Class that contains information about an event that triggers a search. |
| [SoundEffectConstants](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants) | Constants to be used to play sound effects via `https://developer.android.com/reference/kotlin/android/view/View#playSoundEffect(kotlin.Int)` |
| [Surface](https://developer.android.com/reference/kotlin/android/view/Surface) | Handle onto a raw buffer that is being managed by the screen compositor. |
| [SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl) | Handle to an on-screen Surface managed by the system compositor. |
| [SurfaceControlViewHost](https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost) | Utility class for adding a View hierarchy to a `https://developer.android.com/reference/kotlin/android/view/SurfaceControl`. |
| [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView) | Provides a dedicated drawing surface embedded inside of a view hierarchy. |
| [TextureView](https://developer.android.com/reference/kotlin/android/view/TextureView) | A TextureView can be used to display a content stream, such as that coming from a camera preview, a video, or an OpenGL scene. |
| [TouchDelegate](https://developer.android.com/reference/kotlin/android/view/TouchDelegate) | Helper class to handle situations where you want a view to have a larger touch area than its actual view bounds. |
| [VelocityTracker](https://developer.android.com/reference/kotlin/android/view/VelocityTracker) | Helper for tracking the velocity of motion events, for implementing flinging and other such gestures. |
| [VerifiedInputEvent](https://developer.android.com/reference/kotlin/android/view/VerifiedInputEvent) | Base class for verified events. |
| [VerifiedKeyEvent](https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent) | KeyEvent that has been verified by the system. |
| [VerifiedMotionEvent](https://developer.android.com/reference/kotlin/android/view/VerifiedMotionEvent) | MotionEvent that has been verified by the system. |
| [VibrationEffectInflater](https://developer.android.com/reference/kotlin/android/view/VibrationEffectInflater) | Instantiates `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#` objects from Android XML resources. |
| [View](https://developer.android.com/reference/kotlin/android/view/View) | This class represents the basic building block for user interface components. |
| [ViewAnimationUtils](https://developer.android.com/reference/kotlin/android/view/ViewAnimationUtils) | Defines common utilities for working with View's animations. |
| [ViewConfiguration](https://developer.android.com/reference/kotlin/android/view/ViewConfiguration) | Contains methods to standard constants used in the UI for timeouts, sizes, and distances. |
| [ViewDebug](https://developer.android.com/reference/kotlin/android/view/ViewDebug) | Various debugging/tracing tools related to `https://developer.android.com/reference/kotlin/android/view/View` and the view hierarchy. |
| [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup) | A `ViewGroup` is a special view that can contain other views (called children.) The view group is the base class for layouts and views containers. |
| [ViewGroupOverlay](https://developer.android.com/reference/kotlin/android/view/ViewGroupOverlay) | A group overlay is an extra layer that sits on top of a ViewGroup (the "host view") which is drawn after all other content in that view (including the view group's children). |
| [ViewOutlineProvider](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider) | Interface by which a View builds its `https://developer.android.com/reference/kotlin/android/graphics/Outline.html#`, used for shadow casting and clipping. |
| [ViewOverlay](https://developer.android.com/reference/kotlin/android/view/ViewOverlay) | An overlay is an extra layer that sits on top of a View (the "host view") which is drawn after all other content in that view (including children, if the view is a ViewGroup). |
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator) | This class enables automatic and optimized animation of select properties on View objects. |
| [ViewStructure](https://developer.android.com/reference/kotlin/android/view/ViewStructure) | `ViewStructure` is a container for storing additional per-view data generated by `https://developer.android.com/reference/kotlin/android/view/View#onProvideStructure(android.view.ViewStructure)` and `https://developer.android.com/reference/kotlin/android/view/View#onProvideAutofillStructure(android.view.ViewStructure,%20kotlin.Int)`. |
| [ViewStub](https://developer.android.com/reference/kotlin/android/view/ViewStub) | A ViewStub is an invisible, zero-sized View that can be used to lazily inflate layout resources at runtime. |
| [ViewTreeObserver](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver) | A view tree observer is used to register listeners that can be notified of global changes in the view tree. |
| [Window](https://developer.android.com/reference/kotlin/android/view/Window) | Abstract base class for a top-level window look and behavior policy. |
| [WindowAnimationFrameStats](https://developer.android.com/reference/kotlin/android/view/WindowAnimationFrameStats) | This class contains window animation frame statistics. |
| [WindowContentFrameStats](https://developer.android.com/reference/kotlin/android/view/WindowContentFrameStats) | This class contains window content frame statistics. |
| [WindowId](https://developer.android.com/reference/kotlin/android/view/WindowId) | Safe identifier for a window. |
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets) | Describes a set of insets for window content. |
| [WindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation) | Class representing an animation of a set of windows that cause insets. |
| [WindowMetrics](https://developer.android.com/reference/kotlin/android/view/WindowMetrics) | Metrics about a Window, consisting of the bounds and `https://developer.android.com/reference/kotlin/android/view/WindowInsets`. |

## Exceptions

| [InflateException](https://developer.android.com/reference/kotlin/android/view/InflateException) | This exception is thrown by an inflater on error conditions. |
