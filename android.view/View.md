Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# View

```
open class View : AccessibilityEventSource, Drawable.Callback, KeyEvent.Callback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.View](View.md) |

Known Direct Subclasses [AnalogClock](../android.widget/AnalogClock.md), [ImageView](../android.widget/ImageView.md), [KeyboardView](../android.inputmethodservice/KeyboardView.md), [MediaRouteButton](../android.app/MediaRouteButton.md), [ProgressBar](../android.widget/ProgressBar.md), [Space](../android.widget/Space.md), [SurfaceView](SurfaceView.md), [TextView](../android.widget/TextView.md), [TextureView](TextureView.md), [ViewGroup](ViewGroup.md), [ViewStub](ViewStub.md) [AnalogClock](../android.widget/AnalogClock.md) This widget displays an analogic clock with two hands for hours and minutes.
[ImageView](../android.widget/ImageView.md) Displays image resources, for example `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` resources.
[KeyboardView](../android.inputmethodservice/KeyboardView.md) A view that renders a virtual `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard.html#`.
[MediaRouteButton](../android.app/MediaRouteButton.md) <br />

[ProgressBar](../android.widget/ProgressBar.md) A user interface element that indicates the progress of an operation.
[Space](../android.widget/Space.md) Space is a lightweight View subclass that may be used to create gaps between components in general purpose layouts.
[SurfaceView](SurfaceView.md) Provides a dedicated drawing surface embedded inside of a view hierarchy.
[TextView](../android.widget/TextView.md) A user interface element that displays text to the user.
[TextureView](TextureView.md) A TextureView can be used to display a content stream, such as that coming from a camera preview, a video, or an OpenGL scene.
[ViewGroup](ViewGroup.md) A `ViewGroup` is a special view that can contain other views (called children.) The view group is the base class for layouts and views containers.
[ViewStub](ViewStub.md) A ViewStub is an invisible, zero-sized View that can be used to lazily inflate layout resources at runtime.
Known Indirect Subclasses [AbsListView](../android.widget/AbsListView.md), [AbsSeekBar](../android.widget/AbsSeekBar.md), [AbsSpinner](../android.widget/AbsSpinner.md), [AbsoluteLayout](../android.widget/AbsoluteLayout.md), [ActionMenuView](../android.widget/ActionMenuView.md), [AdapterView](../android.widget/AdapterView.md), [AdapterViewAnimator](../android.widget/AdapterViewAnimator.md), [AdapterViewFlipper](../android.widget/AdapterViewFlipper.md), [AppWidgetHostView](../android.appwidget/AppWidgetHostView.md), [AutoCompleteTextView](../android.widget/AutoCompleteTextView.md), [Button](../android.widget/Button.md), [CalendarView](../android.widget/CalendarView.md), and 59 others. [AbsListView](../android.widget/AbsListView.md) Base class that can be used to implement virtualized lists of items.
[AbsSeekBar](../android.widget/AbsSeekBar.md) AbsSeekBar extends the capabilities of ProgressBar by adding a draggable thumb.
[AbsSpinner](../android.widget/AbsSpinner.md) An abstract base class for spinner widgets.
[AbsoluteLayout](../android.widget/AbsoluteLayout.md) A layout that lets you specify exact locations (x/y coordinates) of its children.
[ActionMenuView](../android.widget/ActionMenuView.md) ActionMenuView is a presentation of a series of menu options as a View.
[AdapterView](../android.widget/AdapterView.md) An AdapterView is a view whose children are determined by an `https://developer.android.com/reference/kotlin/android/widget/Adapter.html#`.
[AdapterViewAnimator](../android.widget/AdapterViewAnimator.md) Base class for a `https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#` that will perform animations when switching between its views.
[AdapterViewFlipper](../android.widget/AdapterViewFlipper.md) Simple `https://developer.android.com/reference/kotlin/android/widget/ViewAnimator.html#` that will animate between two or more views that have been added to it.
[AppWidgetHostView](../android.appwidget/AppWidgetHostView.md) Provides the glue to show AppWidget views.
[AutoCompleteTextView](../android.widget/AutoCompleteTextView.md) An editable text view that shows completion suggestions automatically while the user is typing.
[Button](../android.widget/Button.md) A user interface element the user can tap or click to perform an action.
[CalendarView](../android.widget/CalendarView.md) This class is a calendar widget for displaying and selecting dates.
[CheckBox](../android.widget/CheckBox.md) A checkbox is a specific type of two-states button that can be either checked or unchecked.
[CheckedTextView](../android.widget/CheckedTextView.md) An extension to `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` that supports the `https://developer.android.com/reference/kotlin/android/widget/Checkable.html#` interface and displays.
[Chronometer](../android.widget/Chronometer.md) Class that implements a simple timer.
[CompoundButton](../android.widget/CompoundButton.md) A button with two states, checked and unchecked.
[DatePicker](../android.widget/DatePicker.md) Provides a widget for selecting a date.
[DialerFilter](../android.widget/DialerFilter.md) This widget is a layout that contains several specifically-named child views that handle keyboard entry interpreted as standard phone dialpad digits.
[DigitalClock](../android.widget/DigitalClock.md) Like AnalogClock, but digital.
[EditText](../android.widget/EditText.md) A user interface element for entering and modifying text.
[ExpandableListView](../android.widget/ExpandableListView.md) A view that shows items in a vertically scrolling two-level list.
[ExtractEditText](../android.inputmethodservice/ExtractEditText.md) \* Specialization of `https://developer.android.com/reference/kotlin/android/widget/EditText.html#` for showing and interacting with the extracted text in a full-screen input method.
[FragmentBreadCrumbs](../android.app/FragmentBreadCrumbs.md) Helper class for showing "bread crumbs" representing the fragment stack in an activity.
[FrameLayout](../android.widget/FrameLayout.md) FrameLayout is designed to block out an area on the screen to display a single item.
[GLSurfaceView](../android.opengl/GLSurfaceView.md) An implementation of SurfaceView that uses the dedicated surface for displaying OpenGL rendering.
[Gallery](../android.widget/Gallery.md) A view that shows items in a center-locked, horizontally scrolling list.
[GestureOverlayView](../android.gesture/GestureOverlayView.md) A transparent overlay for gesture input that can be placed on top of other widgets or contain other widgets.
[GridLayout](../android.widget/GridLayout.md) A layout that places its children in a rectangular *grid*.
[GridView](../android.widget/GridView.md) A view that shows items in two-dimensional scrolling grid.
[HorizontalScrollView](../android.widget/HorizontalScrollView.md) Layout container for a view hierarchy that can be scrolled by the user, allowing it to be larger than the physical display.
[ImageButton](../android.widget/ImageButton.md) Displays a button with an image (instead of text) that can be pressed or clicked by the user.
[ImageSwitcher](../android.widget/ImageSwitcher.md) `https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher.html#` that switches between two ImageViews when a new image is set on it.
[InlineContentView](../android.widget.inline/InlineContentView.md) This class represents a view that holds opaque content from another app that you can inline in your UI.
[LinearLayout](../android.widget/LinearLayout.md) A layout that arranges other views either horizontally in a single column or vertically in a single row.
[ListView](../android.widget/ListView.md) Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list.
[MediaController](../android.widget/MediaController.md) A view containing controls for a MediaPlayer.
[MultiAutoCompleteTextView](../android.widget/MultiAutoCompleteTextView.md) An editable text view, extending `https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.html#`, that can show completion suggestions for the substring of the text where the user is typing instead of necessarily for the entire thing.
[NumberPicker](../android.widget/NumberPicker.md) A widget that enables the user to select a number from a predefined range.
[QuickContactBadge](../android.widget/QuickContactBadge.md) Widget used to show an image with the standard QuickContact badge and on-click behavior.
[RadioButton](../android.widget/RadioButton.md) A radio button is a two-states button that can be either checked or unchecked.
[RadioGroup](../android.widget/RadioGroup.md) This class is used to create a multiple-exclusion scope for a set of radio buttons.
[RatingBar](../android.widget/RatingBar.md) A RatingBar is an extension of SeekBar and ProgressBar that shows a rating in stars.
[RelativeLayout](../android.widget/RelativeLayout.md) A Layout where the positions of the children can be described in relation to each other or to the parent.
[ScrollView](../android.widget/ScrollView.md) A view group that allows the view hierarchy placed within it to be scrolled.
[SearchView](../android.widget/SearchView.md) A widget that provides a user interface for the user to enter a search query and submit a request to a search provider.
[SeekBar](../android.widget/SeekBar.md) A SeekBar is an extension of ProgressBar that adds a draggable thumb.
[SlidingDrawer](../android.widget/SlidingDrawer.md) SlidingDrawer hides content out of the screen and allows the user to drag a handle to bring the content on screen.
[Spinner](../android.widget/Spinner.md) A view that displays one child at a time and lets the user pick among them.
[SplashScreenView](../android.window/SplashScreenView.md) The view which allows an activity to customize its splash screen exit animation.
[StackView](../android.widget/StackView.md) A view that displays its children in a stack and allows users to discretely swipe through the children.
[Switch](../android.widget/Switch.md) A Switch is a two-state toggle widget.
[TabHost](../android.widget/TabHost.md) Container for a tabbed window view.
[TabWidget](../android.widget/TabWidget.md) Displays a list of tab labels representing each page in the parent's tab collection.
[TableLayout](../android.widget/TableLayout.md) A layout that arranges its children into rows and columns.
[TableRow](../android.widget/TableRow.md) A layout that arranges its children horizontally.
[TextClock](../android.widget/TextClock.md) `TextClock` can display the current date and/or time as a formatted string.
[TextSwitcher](../android.widget/TextSwitcher.md) Specialized `https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher.html#` that contains only children of type `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`.
[TimePicker](../android.widget/TimePicker.md) A widget for selecting the time of day, in either 24-hour or AM/PM mode.
[ToggleButton](../android.widget/ToggleButton.md) Displays checked/unchecked states as a button with a "light" indicator and by default accompanied with the text "ON" or "OFF".
[Toolbar](../android.widget/Toolbar.md) A standard toolbar for use within application content.
[TvAdView](../android.media.tv.ad/TvAdView.md) Displays contents of TV advertisement services.
[TvInteractiveAppView](../android.media.tv.interactive/TvInteractiveAppView.md) Displays contents of interactive TV applications.
[TvView](../android.media.tv/TvView.md) Displays TV contents.
[TwoLineListItem](../android.widget/TwoLineListItem.md) A view group with two children, intended for use in ListViews.
[VideoView](../android.widget/VideoView.md) Displays a video file.
[ViewAnimator](../android.widget/ViewAnimator.md) Base class for a `https://developer.android.com/reference/kotlin/android/widget/FrameLayout.html#` container that will perform animations when switching between its views.
[ViewFlipper](../android.widget/ViewFlipper.md) Simple `https://developer.android.com/reference/kotlin/android/widget/ViewAnimator.html#` that will animate between two or more views that have been added to it.
[ViewSwitcher](../android.widget/ViewSwitcher.md) `https://developer.android.com/reference/kotlin/android/widget/ViewAnimator.html#` that switches between two views, and has a factory from which these views are created.
[WebView](../android.webkit/WebView.md) A View that displays web pages.
[ZoomButton](../android.widget/ZoomButton.md) This widget provides a simple utility for turning a continued long-press event into a series of clicks at some set frequency.
[ZoomControls](../android.widget/ZoomControls.md) The `ZoomControls` class displays a simple set of controls used for zooming and provides callbacks to register for events.

This class represents the basic building block for user interface components. A View occupies a rectangular area on the screen and is responsible for drawing and event handling. View is the base class for *widgets* , which are used to create interactive UI components (buttons, text fields, etc.). The ViewGroup subclass is the base class for *layouts*, which are invisible containers that hold other Views (or other ViewGroups) and define their layout properties.

> [!NOTE]
>
> ### Developer Guides
>
> For information about using this class to develop your application's user interface, read the [User Interface](https://developer.android.com/guide/topics/ui/index.html) developer guide.

### Using Views

All of the views in a window are arranged in a single tree. You can add views either from code or by specifying a tree of views in one or more XML layout files. There are many specialized subclasses of views that act as controls or are capable of displaying text, images, or other content.

Once you have created a tree of views, there are typically a few types of common operations you may wish to perform:

- **Set properties:** for example setting the text of a `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`. The available properties and the methods that set them will vary among the different subclasses of views. Note that properties that are known at build time can be set in the XML layout files.
- **Set focus:** The framework will handle moving focus in response to user input. To force focus to a specific view, call #requestFocus.
- **Set up listeners:** Views allow clients to set listeners that will be notified when something interesting happens to the view. For example, all views will let you set a listener to be notified when the view gains or loses focus. You can register such a listener using setOnFocusChangeListener. Other view subclasses offer more specialized listeners. For example, a Button exposes a listener to notify clients when the button is clicked.
- **Set visibility:** You can hide or show views using setVisibility.

<br />

*Note: The Android framework is responsible for measuring, laying out and drawing views. You should not call methods that perform these actions on views yourself unless you are actually implementing a ViewGroup.*

### Implementing a Custom View

To implement a custom view, you will usually begin by providing overrides for some of the standard methods that the framework calls on all views. You do not need to override all of these methods. In fact, you can start by just overriding onDraw.

| Category | Methods | Description |
|---|---|---|
| Creation | Constructors | There is a form of the constructor that are called when the view is created from code and a form that is called when the view is inflated from a layout file. The second form should parse and apply any attributes defined in the layout file. |
| Creation | `` onFinishInflate `` | Called after a view and all of its children has been inflated from XML. |
| Layout | `` onMeasure `` | Called to determine the size requirements for this view and all of its children. |
| --- | --- | --- |
| Layout | `` onLayout `` | Called when this view should assign a size and position to all of its children. |
| Layout | `` onSizeChanged `` | Called when the size of this view has changed. |
| Drawing | `` onDraw `` | Called when the view should render its content. |
| --- | --- | --- |
| Event processing | `` onKeyDown `` | Called when a new hardware key event occurs. |
| Event processing | `` onKeyUp `` | Called when a hardware key up event occurs. |
| Event processing | `` onTrackballEvent `` | Called when a trackball motion event occurs. |
| --- | --- | --- |
| Event processing | `` onTouchEvent `` | Called when a motion event occurs with pointers down on the view. |
| Event processing | `` onGenericMotionEvent `` | Called when a generic motion event occurs. |
| Event processing | `` onHoverEvent `` | Called when a hover motion event occurs. |
| --- | --- | --- |
| Focus | `` onFocusChanged `` | Called when the view gains or loses focus. |
| Focus | `` onWindowFocusChanged `` | Called when the window containing the view gains or loses focus. |
| Attaching | `` onAttachedToWindow `` | Called when the view is attached to a window. |
| --- | --- | --- |
| Attaching | `` onDetachedFromWindow `` | Called when the view is detached from its window. |
| Attaching | `` onWindowVisibilityChanged `` | Called when the visibility of the window containing the view has changed. |

<br />

### IDs

Views may have an integer id associated with them. These ids are typically assigned in the layout XML files, and are used to find specific views within the view tree. A common pattern is to:

- Define a Button in the layout file and assign it a unique ID.

  ```kotlin
  <Button
        android:id="@+id/my_button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/my_button_text"/>
    
  ```
- From the onCreate method of an Activity, find the Button

  ```kotlin
  Button myButton = findViewById(R.id.my_button);
    
  ```

View IDs need not be unique throughout the tree, but it is good practice to ensure that they are at least unique within the part of the tree you are searching.

### Position

The geometry of a view is that of a rectangle. A view has a location, expressed as a pair of *left* and *top* coordinates, and two dimensions, expressed as a width and a height. The unit for location and dimensions is the pixel.

It is possible to retrieve the location of a view by invoking the methods getLeft and getTop. The former returns the left, or X, coordinate of the rectangle representing the view. The latter returns the top, or Y, coordinate of the rectangle representing the view. These methods both return the location of the view relative to its parent. For instance, when getLeft() returns 20, that means the view is located 20 pixels to the right of the left edge of its direct parent.

In addition, several convenience methods are offered to avoid unnecessary computations, namely getRight and getBottom. These methods return the coordinates of the right and bottom edges of the rectangle representing the view. For instance, calling getRight is similar to the following computation: `getLeft() + getWidth()` (see [Size](View.md) for more information about the width.)

### Size, padding and margins

The size of a view is expressed with a width and a height. A view actually possess two pairs of width and height values.

The first pair is known as *measured width* and *measured height* . These dimensions define how big a view wants to be within its parent (see [Layout](View.md) for more details.) The measured dimensions can be obtained by calling getMeasuredWidth and getMeasuredHeight.

The second pair is simply known as *width* and *height* , or sometimes *drawing width* and *drawing height* . These dimensions define the actual size of the view on screen, at drawing time and after layout. These values may, but do not have to, be different from the measured width and height. The width and height can be obtained by calling getWidth and getHeight.

To measure its dimensions, a view takes into account its padding. The padding is expressed in pixels for the left, top, right and bottom parts of the view. Padding can be used to offset the content of the view by a specific amount of pixels. For instance, a left padding of 2 will push the view's content by 2 pixels to the right of the left edge. Padding can be set using the setPadding or setPaddingRelative method and queried by calling getPaddingLeft, getPaddingTop, getPaddingRight, getPaddingBottom, getPaddingStart, getPaddingEnd.

Even though a view can define a padding, it does not provide any support for margins. However, view groups provide such a support. Refer to ViewGroup and `https://developer.android.com/reference/kotlin/android/view/ViewGroup.MarginLayoutParams` for further information.

### Layout

Layout is a two pass process: a measure pass and a layout pass. The measuring pass is implemented in measure and is a top-down traversal of the view tree. Each view pushes dimension specifications down the tree during the recursion. At the end of the measure pass, every view has stored its measurements. The second pass happens in layout and is also top-down. During this pass each parent is responsible for positioning all of its children using the sizes computed in the measure pass.

When a view's measure() method returns, its getMeasuredWidth and getMeasuredHeight values must be set, along with those for all of that view's descendants. A view's measured width and measured height values must respect the constraints imposed by the view's parents. This guarantees that at the end of the measure pass, all parents accept all of their children's measurements. A parent view may call measure() more than once on its children. For example, the parent may measure each child once with unspecified dimensions to find out how big they want to be, then call measure() on them again with actual numbers if the sum of all the children's unconstrained sizes is too big or too small.

The measure pass uses two classes to communicate dimensions. The `https://developer.android.com/reference/kotlin/android/view/View.MeasureSpec` class is used by views to tell their parents how they want to be measured and positioned. The base LayoutParams class just describes how big the view wants to be for both width and height. For each dimension, it can specify one of:

- an exact number
- MATCH_PARENT, which means the view wants to be as big as its parent (minus padding)
- WRAP_CONTENT, which means that the view wants to be just big enough to enclose its content (plus padding).

There are subclasses of LayoutParams for different subclasses of ViewGroup. For example, AbsoluteLayout has its own subclass of LayoutParams which adds an X and Y value.

<br />

MeasureSpecs are used to push requirements down the tree from parent to child. A MeasureSpec can be in one of three modes:

- UNSPECIFIED: This is used by a parent to determine the desired dimension of a child view. For example, a LinearLayout may call measure() on its child with the height set to UNSPECIFIED and a width of EXACTLY 240 to find out how tall the child view wants to be given a width of 240 pixels.
- EXACTLY: This is used by the parent to impose an exact size on the child. The child must use this size, and guarantee that all of its descendants will fit within this size.
- AT_MOST: This is used by the parent to impose a maximum size on the child. The child must guarantee that it and all of its descendants will fit within this size.

<br />

To initiate a layout, call requestLayout. This method is typically called by a view on itself when it believes that it can no longer fit within its current bounds.

### Drawing

Drawing is handled by walking the tree and recording the drawing commands of any View that needs to update. After this, the drawing commands of the entire tree are issued to screen, clipped to the newly damaged area.

The tree is largely recorded and drawn in order, with parents drawn before (i.e., behind) their children, with siblings drawn in the order they appear in the tree. If you set a background drawable for a View, then the View will draw it before calling back to its `onDraw()` method. The child drawing order can be overridden with setChildrenDrawingOrderEnabled in a ViewGroup, and with setZ custom Z values} set on Views.

To force a view to draw, call invalidate.

### Event Handling and Threading

The basic cycle of a view is as follows:

1. An event comes in and is dispatched to the appropriate view. The view handles the event and notifies any listeners.
2. If in the course of processing the event, the view's bounds may need to be changed, the view will call requestLayout.
3. Similarly, if in the course of processing the event the view's appearance may need to be changed, the view will call invalidate.
4. If either requestLayout or invalidate were called, the framework will take care of measuring, laying out, and drawing the tree as appropriate.

<br />

*Note: The entire view tree is single threaded. You must always be on the UI thread when calling any method on any view.* If you are doing work on other threads and want to update the state of a view from that thread, you should use a `https://developer.android.com/reference/kotlin/android/os/Handler.html#`.

### Focus Handling

The framework will handle routine focus movement in response to user input. This includes changing the focus as views are removed or hidden, or as new views become available. Views indicate their willingness to take focus through the isFocusable method. To change whether a view can take focus, call setFocusable. When in touch mode (see notes below) views indicate whether they still would like focus via isFocusableInTouchMode and can change this via setFocusableInTouchMode.

Focus movement is based on an algorithm which finds the nearest neighbor in a given direction. In rare cases, the default algorithm may not match the intended behavior of the developer. In these situations, you can provide explicit overrides by using these XML attributes in the layout file:

```kotlin
nextFocusDown
  nextFocusLeft
  nextFocusRight
  nextFocusUp
  
```

<br />

To get a particular view to take focus, call requestFocus.

### Touch Mode

When a user is navigating a user interface via directional keys such as a D-pad, it is necessary to give focus to actionable items such as buttons so the user can see what will take input. If the device has touch capabilities, however, and the user begins interacting with the interface by touching it, it is no longer necessary to always highlight, or give focus to, a particular view. This motivates a mode for interaction named 'touch mode'.

For a touch capable device, once the user touches the screen, the device will enter touch mode. From this point onward, only views for which isFocusableInTouchMode is true will be focusable, such as text editing widgets. Other views that are touchable, like buttons, will not take focus when touched; they will only fire the on click listeners.

Any time a user hits a directional key, such as a D-pad direction, the view device will exit touch mode, and find a view to take focus, so that the user may resume interacting with the user interface without touching the screen again.

The touch mode state is maintained across `https://developer.android.com/reference/kotlin/android/app/Activity.html#`s. Call isInTouchMode to see whether the device is currently in touch mode.

### Scrolling

The framework provides basic support for views that wish to internally scroll their content. This includes keeping track of the X and Y scroll offset as well as mechanisms for drawing scrollbars. See scrollBy, scrollTo, and awakenScrollBars for more details.

### Tags

Unlike IDs, tags are not used to identify views. Tags are essentially an extra piece of information that can be associated with a view. They are most often used as a convenience to store data related to views in the views themselves rather than by putting them in a separate structure.

Tags may be specified with character sequence values in layout XML as either a single tag using the `https://developer.android.com/reference/kotlin/android/R.styleable.html#View_tag:kotlin.Int` attribute or multiple tags using the `<tag>` child element:

```kotlin
<View ...
            android:tag="@string/mytag_value" />
      <View ...>
          <tag android:id="@+id/mytag"
               android:value="@string/mytag_value" />
      </View>
  
```

<br />

Tags may also be specified with arbitrary objects from code using setTag or setTag.

### Themes

By default, Views are created using the theme of the Context object supplied to their constructor; however, a different theme may be specified by using the `https://developer.android.com/reference/kotlin/android/R.styleable.html#View_theme:kotlin.Int` attribute in layout XML or by passing a ContextThemeWrapper to the constructor from code.

When the `https://developer.android.com/reference/kotlin/android/R.styleable.html#View_theme:kotlin.Int` attribute is used in XML, the specified theme is applied on top of the inflation context's theme (see LayoutInflater) and used for the view itself as well as any child elements.

In the following example, both views will be created using the Material dark color scheme; however, because an overlay theme is used which only defines a subset of attributes, the value of `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_colorAccent:kotlin.Int` defined on the inflation context's theme (e.g. the Activity theme) will be preserved.

```kotlin
<LinearLayout
              ...
              android:theme="@android:theme/ThemeOverlay.Material.Dark">
          <View ...>
      </LinearLayout>
  
```

<br />

### Properties

The View class exposes an `https://developer.android.com/reference/kotlin/android/view/View#ALPHA:android.util.Property` property, as well as several transform-related properties, such as `https://developer.android.com/reference/kotlin/android/view/View#TRANSLATION_X:android.util.Property` and `https://developer.android.com/reference/kotlin/android/view/View#TRANSLATION_Y:android.util.Property`. These properties are available both in the `https://developer.android.com/reference/kotlin/android/util/Property.html#` form as well as in similarly-named setter/getter methods (such as setAlpha for `https://developer.android.com/reference/kotlin/android/view/View#ALPHA:android.util.Property`). These properties can be used to set persistent state associated with these rendering-related properties on the view. The properties and methods can also be used in conjunction with `https://developer.android.com/reference/kotlin/android/animation/Animator.html#`-based animations, described more in the [Animation](View.md) section.

### Animation

Starting with Android 3.0, the preferred way of animating views is to use the `https://developer.android.com/reference/kotlin/android/animation/package-summary.html` package APIs. These `https://developer.android.com/reference/kotlin/android/animation/Animator.html#`-based classes change actual properties of the View object, such as setAlpha and setTranslationX. This behavior is contrasted to that of the pre-3.0 Animation-based classes, which instead animate only how the view is drawn on the display. In particular, the ViewPropertyAnimator class makes animating these View properties particularly easy and efficient.

Alternatively, you can use the pre-3.0 animation classes to animate how Views are rendered. You can attach an Animation object to a view using setAnimation or startAnimation. The animation can alter the scale, rotation, translation and alpha of a view over time. If the animation is attached to a view that has children, the animation will affect the entire subtree rooted by that node. When an animation is started, the framework will take care of redrawing the appropriate views until the animation completes.

### Security

Sometimes it is essential that an application be able to verify that an action is being performed with the full knowledge and consent of the user, such as granting a permission request, making a purchase or clicking on an advertisement. Unfortunately, a malicious application could try to spoof the user into performing these actions, unaware, by concealing the intended purpose of the view. As a remedy, the framework offers a touch filtering mechanism that can be used to improve the security of views that provide access to sensitive functionality.

To enable touch filtering, call setFilterTouchesWhenObscured or set the android:filterTouchesWhenObscured layout attribute to true. When enabled, the framework will discard touches that are received whenever the view's window is obscured by another visible window at the touched location. As a result, the view will not receive touches whenever the touch passed through a toast, dialog or other window that appears above the view's window.

For more fine-grained control over security, consider overriding the onFilterTouchEventForSecurity method to implement your own security policy. See also `https://developer.android.com/reference/kotlin/android/view/MotionEvent#FLAG_WINDOW_IS_OBSCURED:kotlin.Int`.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` This class represents a delegate that can be registered in a View to enhance accessibility support via composition rather via inheritance. |
| open | `https://developer.android.com/reference/kotlin/android/view/View.BaseSavedState` Base class for derived classes that want to save and restore their own state in onSaveInstanceState. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.CalledFromWrongThreadListener` A listener that is notified when certain View APIs are called from the wrong thread. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder` Creates an image that the system displays during the drag and drop operation. |
| open | `https://developer.android.com/reference/kotlin/android/view/View.MeasureSpec` A MeasureSpec encapsulates the layout requirements passed from parent to child. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener` Listener for applying window insets on a view in a custom way. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnAttachStateChangeListener` Interface definition for a callback to be invoked when this view is attached or detached from its window. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnCapturedPointerListener` Interface definition for a callback to be invoked when a captured pointer event is being dispatched this view. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnClickListener` Interface definition for a callback to be invoked when a view is clicked. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnContextClickListener` Interface definition for a callback to be invoked when a view is context clicked. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener` Interface definition for a callback to be invoked when the context menu for this view is being built. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnDragListener` Interface definition for a listener that's invoked when a drag event is dispatched to this view. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnFocusChangeListener` Interface definition for a callback to be invoked when the focus state of a view changed. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnGenericMotionListener` Interface definition for a callback to be invoked when a generic motion event is dispatched to this view. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnHoverListener` Interface definition for a callback to be invoked when a hover event is dispatched to this view. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnKeyListener` Interface definition for a callback to be invoked when a hardware key event is dispatched to this view. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnLayoutChangeListener` Interface definition for a callback to be invoked when the layout bounds of a view changes due to layout processing. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnLongClickListener` Interface definition for a callback to be invoked when a view has been clicked and held. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnScrollChangeListener` Interface definition for a callback to be invoked when the scroll X or Y positions of a view change. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnSystemUiVisibilityChangeListener` Interface definition for a callback to be invoked when the status bar changes visibility. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener` Interface definition for a callback to be invoked when a touch event is dispatched to this view. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/view/View.OnUnhandledKeyEventListener` Interface definition for a callback to be invoked when a hardware key event hasn't been handled by the view hierarchy. |

| XML attributes ||
|---|---|
| [`android:accessibilityHeading`](View.md) | Whether or not this view is a heading for accessibility purposes. |
| [`android:allowClickWhenDisabled`](View.md) | Whether or not allow clicks on disabled view. |
| [`android:alpha`](View.md) | alpha property of the view, as a value between 0 (completely transparent) and 1 (completely opaque). |
| --- | --- |
| [`android:background`](View.md) | A drawable to use as the background. |
| [`android:clickable`](View.md) | Defines whether this view reacts to click events. |
| [`android:clipToOutline`](View.md) | Whether the View's Outline should be used to clip the contents of the View. |
| --- | --- |
| [`android:contentDescription`](View.md) | Defines text that briefly describes content of the view. |
| [`android:drawingCacheQuality`](View.md) | Defines the quality of translucent drawing caches. |
| [`android:duplicateParentState`](View.md) | When this attribute is set to true, the view gets its drawable state (focused, pressed, etc.) from its direct parent rather than from itself. |
| --- | --- |
| [`android:fadeScrollbars`](View.md) | Defines whether to fade out scrollbars when they are not in use. |
| [`android:fadingEdgeLength`](View.md) | Defines the length of the fading edges. |
| [`android:filterTouchesWhenObscured`](View.md) | Specifies whether to filter touches when the view's window is obscured by another visible window. |
| --- | --- |
| [`android:fitsSystemWindows`](View.md) | Boolean internal attribute to adjust view layout based on system windows such as the status bar. |
| [`android:focusable`](View.md) | Controls whether a view can take focus. |
| [`android:focusableInTouchMode`](View.md) | Boolean that controls whether a view can take focus while in touch mode. |
| --- | --- |
| [`android:focusedByDefault`](View.md) | Whether this view is a default-focus view. |
| [`android:hapticFeedbackEnabled`](View.md) | Boolean that controls whether a view should have haptic feedback enabled for events such as long presses. |
| [`android:id`](View.md) | Supply an identifier name for this view, to later retrieve it with View. |
| --- | --- |
| [`android:isScrollContainer`](View.md) | Set this if the view will serve as a scrolling container, meaning that it can be resized to shrink its overall window so that there will be space for an input method. |
| [`android:keepScreenOn`](View.md) | Controls whether the view's window should keep the screen on while visible. |
| [`android:keyboardNavigationCluster`](View.md) | Whether this view is a root of a keyboard navigation cluster. |
| --- | --- |
| [`android:layerType`](View.md) | Specifies the type of layer backing this view. |
| [`android:layoutDirection`](View.md) | Defines the direction of layout drawing. |
| [`android:longClickable`](View.md) | Defines whether this view reacts to long click events. |
| --- | --- |
| [`android:minHeight`](View.md) | Defines the minimum height of the view. |
| [`android:minWidth`](View.md) | Defines the minimum width of the view. |
| [`android:nextClusterForward`](View.md) | Defines the next keyboard navigation cluster. |
| --- | --- |
| [`android:nextFocusDown`](View.md) | Defines the next view to give focus to when the next focus is android. |
| [`android:nextFocusLeft`](View.md) | Defines the next view to give focus to when the next focus is android. |
| [`android:nextFocusRight`](View.md) | Defines the next view to give focus to when the next focus is android. |
| --- | --- |
| [`android:nextFocusUp`](View.md) | Defines the next view to give focus to when the next focus is android. |
| [`android:onClick`](View.md) | Name of the method in this View's context to invoke when the view is clicked. |
| [`android:outlineAmbientShadowColor`](View.md) | Sets the color of the ambient shadow that is drawn when the view has a positive Z or elevation value. |
| --- | --- |
| [`android:outlineSpotShadowColor`](View.md) | Sets the color of the spot shadow that is drawn when the view has a positive Z or elevation value. |
| [`android:padding`](View.md) | Sets the padding, in pixels, of all four edges. |
| [`android:paddingBottom`](View.md) | Sets the padding, in pixels, of the bottom edge; see android. |
| --- | --- |
| [`android:paddingEnd`](View.md) | Sets the padding, in pixels, of the end edge; see android. |
| [`android:paddingHorizontal`](View.md) | Sets the padding, in pixels, of the left and right edges; see android. |
| [`android:paddingLeft`](View.md) | Sets the padding, in pixels, of the left edge; see android. |
| --- | --- |
| [`android:paddingRight`](View.md) | Sets the padding, in pixels, of the right edge; see android. |
| [`android:paddingStart`](View.md) | Sets the padding, in pixels, of the start edge; see android. |
| [`android:paddingTop`](View.md) | Sets the padding, in pixels, of the top edge; see android. |
| --- | --- |
| [`android:paddingVertical`](View.md) | Sets the padding, in pixels, of the top and bottom edges; see android. |
| [`android:requiresFadingEdge`](View.md) | Defines which edges should be faded on scrolling. |
| [`android:rotation`](View.md) | rotation of the view, in degrees. |
| --- | --- |
| [`android:rotationX`](View.md) | rotation of the view around the x axis, in degrees. |
| [`android:rotationY`](View.md) | rotation of the view around the y axis, in degrees. |
| [`android:saveEnabled`](View.md) | If false, no state will be saved for this view when it is being frozen. |
| --- | --- |
| [`android:scaleX`](View.md) | scale of the view in the x direction. |
| [`android:scaleY`](View.md) | scale of the view in the y direction. |
| [`android:scrollX`](View.md) | The initial horizontal scroll offset, in pixels. |
| --- | --- |
| [`android:scrollY`](View.md) | The initial vertical scroll offset, in pixels. |
| [`android:scrollbarAlwaysDrawHorizontalTrack`](View.md) | Defines whether the horizontal scrollbar track should always be drawn. |
| [`android:scrollbarAlwaysDrawVerticalTrack`](View.md) | Defines whether the vertical scrollbar track should always be drawn. |
| --- | --- |
| [`android:scrollbarDefaultDelayBeforeFade`](View.md) | Defines the delay in milliseconds that a scrollbar waits before fade out. |
| [`android:scrollbarFadeDuration`](View.md) | Defines the delay in milliseconds that a scrollbar takes to fade out. |
| [`android:scrollbarSize`](View.md) | Sets the width of vertical scrollbars and height of horizontal scrollbars. |
| --- | --- |
| [`android:scrollbarStyle`](View.md) | Controls the scrollbar style and position. |
| [`android:scrollbarThumbHorizontal`](View.md) | Defines the horizontal scrollbar thumb drawable. |
| [`android:scrollbarThumbVertical`](View.md) | Defines the vertical scrollbar thumb drawable. |
| --- | --- |
| [`android:scrollbarTrackHorizontal`](View.md) | Defines the horizontal scrollbar track drawable. |
| [`android:scrollbarTrackVertical`](View.md) | Defines the vertical scrollbar track drawable. |
| [`android:scrollbars`](View.md) | Defines which scrollbars should be displayed on scrolling or not. |
| --- | --- |
| [`android:soundEffectsEnabled`](View.md) | Boolean that controls whether a view should have sound effects enabled for events such as clicking and touching. |
| [`android:stateListAnimator`](View.md) | Sets the state-based animator for the View. |
| [`android:tag`](View.md) | Supply a tag for this view containing a String, to be retrieved later with android. |
| --- | --- |
| [`android:textAlignment`](View.md) | Defines the alignment of the text. |
| [`android:textDirection`](View.md) | Defines the direction of the text. |
| [`android:theme`](View.md) | Specifies a theme override for a view. |
| --- | --- |
| [`android:transformPivotX`](View.md) | x location of the pivot point around which the view will rotate and scale. |
| [`android:transformPivotY`](View.md) | y location of the pivot point around which the view will rotate and scale. |
| [`android:transitionName`](View.md) | Names a View such that it can be identified for Transitions. |
| --- | --- |
| [`android:translationX`](View.md) | translation in x of the view. |
| [`android:translationY`](View.md) | translation in y of the view. |
| [`android:translationZ`](View.md) | translation in z of the view. |
| --- | --- |
| [`android:visibility`](View.md) | Controls the initial visibility of the view. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_AUTO:kotlin.Int` Automatically determine whether the view should only allow interactions from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s with the isAccessibilityTool property set to true. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_NO:kotlin.Int` Allow interactions from all `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s, regardless of their isAccessibilityTool property. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_YES:kotlin.Int` Only allow interactions from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s with the isAccessibilityTool property set to true. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_ASSERTIVE:kotlin.Int` Live region mode specifying that accessibility services should immediately notify users of changes to this view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_NONE:kotlin.Int` Live region mode specifying that accessibility services should not automatically announce changes to this view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_POLITE:kotlin.Int` Live region mode specifying that accessibility services should notify users of changes to this view. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int` Flag requesting you to add views that are marked as not important for autofill (see setImportantForAutofill) to a ViewStructure. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE:kotlin.String` Hint indicating that this view can be autofilled with a credit card expiration date. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY:kotlin.String` Hint indicating that this view can be autofilled with a credit card expiration day. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH:kotlin.String` Hint indicating that this view can be autofilled with a credit card expiration month. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR:kotlin.String` Hint indicating that this view can be autofilled with a credit card expiration year. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_NUMBER:kotlin.String` Hint indicating that this view can be autofilled with a credit card number. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE:kotlin.String` Hint indicating that this view can be autofilled with a credit card security code. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_EMAIL_ADDRESS:kotlin.String` Hint indicating that this view can be autofilled with an email address. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_NAME:kotlin.String` Hint indicating that this view can be autofilled with a user's real name. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_PASSWORD:kotlin.String` Hint indicating that this view can be autofilled with a password. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_PHONE:kotlin.String` Hint indicating that this view can be autofilled with a phone number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_POSTAL_ADDRESS:kotlin.String` Hint indicating that this view can be autofilled with a postal address. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_POSTAL_CODE:kotlin.String` Hint indicating that this view can be autofilled with a postal code. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_USERNAME:kotlin.String` Hint indicating that this view can be autofilled with a username. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_DATE:kotlin.Int` Autofill type for a field that contains a date, which is represented by a long representing the number of milliseconds since the standard base time known as "the epoch", namely January 1, 1970, 00:00:00 GMT (see getTime. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_LIST:kotlin.Int` Autofill type for a selection list field, which is filled by an `int` representing the element index inside the list (starting at `0`). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_NONE:kotlin.Int` Autofill type for views that cannot be autofilled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_TEXT:kotlin.Int` Autofill type for a text field, which is filled by a `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_TOGGLE:kotlin.Int` Autofill type for a togglable field, which is filled by a `boolean`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_AUTO:kotlin.Int` Content sensitivity is determined by the framework. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_NOT_SENSITIVE:kotlin.Int` The view doesn't display sensitive content. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_SENSITIVE:kotlin.Int` The view displays sensitive content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_ACCESSIBILITY_ACTION:kotlin.Int` Flag indicating that the drag was initiated with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_DRAG_START:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL:kotlin.Int` Flag indicating that a drag can cross window boundaries. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_PERSISTABLE_URI_PERMISSION:kotlin.Int` When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_READ:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_WRITE:kotlin.Int`, the URI permission grant can be persisted across device reboots until explicitly revoked with revokeUriPermission Context. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_PREFIX_URI_PERMISSION:kotlin.Int` When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_READ:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_WRITE:kotlin.Int`, the URI permission grant applies to any URI that is a prefix match against the original granted URI. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_SAME_APPLICATION:kotlin.Int` Flag indicating that a drag can cross window boundaries (within the same application). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_READ:kotlin.Int` When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL:kotlin.Int`, the drag recipient will be able to request read access to the content URI(s) contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_WRITE:kotlin.Int` When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL:kotlin.Int`, the drag recipient will be able to request write access to the content URI(s) contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_HIDE_CALLING_TASK_ON_DRAG_START:kotlin.Int` Flag indicating that this drag will result in the caller activity's task to be hidden for the duration of the drag, which means that the source activity will not receive drag events for the current drag gesture. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_OPAQUE:kotlin.Int` Flag indicating that the drag shadow will be opaque. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_START_INTENT_SENDER_ON_UNHANDLED_DRAG:kotlin.Int` Flag indicating that an unhandled drag should be delegated to the system to be started if no visible window wishes to handle the drop. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_AUTO:kotlin.Int` Enables automatic quality mode for the drawing cache. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_HIGH:kotlin.Int` Enables high quality mode for the drawing cache. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_LOW:kotlin.Int` Enables low quality mode for the drawing cache. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_CONTENT_DESCRIPTION:kotlin.Int` Find find views that contain the specified content description. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_TEXT:kotlin.Int` Find views that render the specified text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE:kotlin.Int` This view wants keystrokes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLES_ALL:kotlin.Int` View flag indicating whether addFocusables should add all focusable Views regardless if they are focusable in touch mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLES_TOUCH_MODE:kotlin.Int` View flag indicating whether addFocusables should add only Views focusable in touch mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE_AUTO:kotlin.Int` This view determines focusability automatically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int` Use with focusSearch. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` Use with focusSearch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int` Use with focusSearch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int` Use with focusSearch. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int` Use with focusSearch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int` Use with focusSearch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` This view is invisible, and it doesn't take any space for layout purposes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#HAPTIC_FEEDBACK_ENABLED:kotlin.Int` View flag indicating whether this view should have haptic feedback enabled for events such as long presses. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_AUTO:kotlin.Int` Automatically determine whether a view is important for accessibility. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO:kotlin.Int` The view is not important for accessibility. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int` The view is not important for accessibility, nor are any of its descendant views. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_YES:kotlin.Int` The view is important for accessibility. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int` Automatically determine whether a view is important for autofill. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int` The view is not important for autofill, but its children (if any) will be traversed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int` The view is not important for autofill, and its children (if any) will not be traversed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int` The view is important for autofill, and its children (if any) will be traversed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int` The view is important for autofill, but its children (if any) will not be traversed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_AUTO:kotlin.Int` Automatically determine whether a view is important for content capture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO:kotlin.Int` The view is not important for content capture, but its children (if any) will be traversed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO_EXCLUDE_DESCENDANTS:kotlin.Int` The view is not important for content capture, and its children (if any) will not be traversed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES:kotlin.Int` The view is important for content capture, and its children (if any) will be traversed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES_EXCLUDE_DESCENDANTS:kotlin.Int` The view is important for content capture, but its children (if any) will not be traversed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` This view is invisible, but it still takes up space for layout purposes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#KEEP_SCREEN_ON:kotlin.Int` View flag indicating that the screen should remain on while the window containing this view is visible to the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int` Indicates that the view has a hardware layer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int` Indicates that the view does not have a layer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int` Indicates that the view has a software layer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_INHERIT:kotlin.Int` Horizontal layout direction of this view is inherited from its parent. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LOCALE:kotlin.Int` Horizontal layout direction of this view is from deduced from the default language script for the locale. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LTR:kotlin.Int` Horizontal layout direction of this view is from Left to Right. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_RTL:kotlin.Int` Horizontal layout direction of this view is from Right to Left. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_HEIGHT_STATE_SHIFT:kotlin.Int` Bit shift of `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_MASK:kotlin.Int` to get to the height bits for functions that combine both width and height into a single int, such as getMeasuredState and the childState argument of resolveSizeAndState. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` Bits of getMeasuredWidthAndState and getMeasuredWidthAndState that provide the actual measured size. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_MASK:kotlin.Int` Bits of getMeasuredWidthAndState and getMeasuredWidthAndState that provide the additional state bits. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_TOO_SMALL:kotlin.Int` Bit of getMeasuredWidthAndState and getMeasuredWidthAndState that indicates the measured size is smaller that the space the view would like to have. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#NOT_FOCUSABLE:kotlin.Int` This view does not want keystrokes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` Used to mark a View that has no ID. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_ALWAYS:kotlin.Int` Always allow a user to over-scroll this view, provided it is a view that can scroll. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_IF_CONTENT_SCROLLS:kotlin.Int` Allow a user to over-scroll this view only if the content is large enough to meaningfully scroll, provided it is a view that can scroll. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_NEVER:kotlin.Int` Never allow a user to over-scroll this view. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_ABSOLUTE:kotlin.Int` A pointer capture mode in which touchpads report absolute finger locations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_RELATIVE:kotlin.Int` A pointer capture mode in which touchpad gestures are recognized and reported like mouse movements. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_UNCAPTURED:kotlin.Int` A "pointer capture mode" in which the pointer is not captured. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS:kotlin.Int` Represents that the user interaction that is requesting a rectangle on screen is doing so because the View has input/keyboard focus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY:kotlin.Int` Represents that the user interaction that is requesting a rectangle on screen is doing so only to scroll the View on screen, and the rectangle is not associated with a text cursor or keyboard focus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR:kotlin.Int` Represents that the user interaction that is requesting a rectangle on screen is doing so because the View contains a text cursor (caret). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED:kotlin.Int` Represents that the user interaction that is requesting a rectangle on screen is doing so via the original requestRectangleOnScreen or requestRectangleOnScreen APIs that do not define the source. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#REQUESTED_FRAME_RATE_CATEGORY_DEFAULT:kotlin.Float` <br /> |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#REQUESTED_FRAME_RATE_CATEGORY_HIGH:kotlin.Float` <br /> |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#REQUESTED_FRAME_RATE_CATEGORY_LOW:kotlin.Float` <br /> |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#REQUESTED_FRAME_RATE_CATEGORY_NORMAL:kotlin.Float` <br /> |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE:kotlin.Float` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCREEN_STATE_OFF:kotlin.Int` Indicates that the screen has changed state and is now off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCREEN_STATE_ON:kotlin.Int` Indicates that the screen has changed state and is now on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_INSIDE_INSET:kotlin.Int` The scrollbar style to display the scrollbars inside the padded area, increasing the padding of the view. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_INSIDE_OVERLAY:kotlin.Int` The scrollbar style to display the scrollbars inside the content area, without increasing the padding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_OUTSIDE_INSET:kotlin.Int` The scrollbar style to display the scrollbars at the edge of the view, increasing the padding of the view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_OUTSIDE_OVERLAY:kotlin.Int` The scrollbar style to display the scrollbars at the edge of the view, without increasing the padding. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBAR_POSITION_DEFAULT:kotlin.Int` Position the scroll bar at the default position as determined by the system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBAR_POSITION_LEFT:kotlin.Int` Position the scroll bar along the left edge. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBAR_POSITION_RIGHT:kotlin.Int` Position the scroll bar along the right edge. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_HORIZONTAL:kotlin.Int` Indicates scrolling along the horizontal axis. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_NONE:kotlin.Int` Indicates no axis of view scrolling. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_VERTICAL:kotlin.Int` Indicates scrolling along the vertical axis. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_AUTO:kotlin.Int` The content of this view will be considered for scroll capture if scrolling is possible. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE:kotlin.Int` Explicitly exclude this view as a potential scroll capture target. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE_DESCENDANTS:kotlin.Int` Explicitly exclude all children of this view as potential scroll capture targets. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int` Explicitly include this view as a potential scroll capture target. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_BOTTOM:kotlin.Int` Scroll indicator direction for the bottom edge of the view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_END:kotlin.Int` Scroll indicator direction for the ending edge of the view. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_LEFT:kotlin.Int` Scroll indicator direction for the left edge of the view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_RIGHT:kotlin.Int` Scroll indicator direction for the right edge of the view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_START:kotlin.Int` Scroll indicator direction for the starting edge of the view. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_TOP:kotlin.Int` Scroll indicator direction for the top edge of the view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SOUND_EFFECTS_ENABLED:kotlin.Int` View flag indicating whether this view should have sound effects enabled for events such as clicking and touching. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#STATUS_BAR_HIDDEN:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#STATUS_BAR_VISIBLE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` Flag for setSystemUiVisibility: View has requested to go into the normal fullscreen mode so that its content can take over the screen while still allowing the user to interact with the application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int` Flag for setSystemUiVisibility: View has requested that the system navigation be temporarily hidden. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_IMMERSIVE:kotlin.Int` Flag for setSystemUiVisibility: View would like to remain interactive when hiding the navigation bar with `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_IMMERSIVE_STICKY:kotlin.Int` Flag for setSystemUiVisibility: View would like to remain interactive when hiding the status bar with `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` and/or hiding the navigation bar with `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int` Flag for setSystemUiVisibility: View would like its window to be laid out as if it has requested `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`, even if it currently hasn't. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int` Flag for setSystemUiVisibility: View would like its window to be laid out as if it has requested `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`, even if it currently hasn't. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_STABLE:kotlin.Int` Flag for setSystemUiVisibility: When using other layout flags, we would like a stable view of the content insets given to fitSystemWindows. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LIGHT_NAVIGATION_BAR:kotlin.Int` Flag for setSystemUiVisibility: Requests the navigation bar to draw in a mode that is compatible with light navigation bar backgrounds. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LIGHT_STATUS_BAR:kotlin.Int` Flag for setSystemUiVisibility: Requests the status bar to draw in a mode that is compatible with light status bar backgrounds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LOW_PROFILE:kotlin.Int` Flag for setSystemUiVisibility: View has requested the system UI to enter an unobtrusive "low profile" mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_VISIBLE:kotlin.Int` Special constant for setSystemUiVisibility: View has requested the system UI (status bar) to be visible (the default). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_LAYOUT_FLAGS:kotlin.Int` Flags that can impact the layout in relation to system UI. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_CENTER:kotlin.Int` Center the paragraph, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_GRAVITY:kotlin.Int` Default for the root view. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_INHERIT:kotlin.Int` Default text alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_END:kotlin.Int` Align to the end of the paragraph, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_START:kotlin.Int` Align to the start of the paragraph, e. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_END:kotlin.Int` Align to the end of the view, which is ALIGN_RIGHT if the view's resolved layoutDirection is LTR, and ALIGN_LEFT otherwise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_START:kotlin.Int` Align to the start of the view, which is ALIGN_LEFT if the view's resolved layoutDirection is LTR, and ALIGN_RIGHT otherwise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_ANY_RTL:kotlin.Int` Text direction is using "any-RTL" algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG:kotlin.Int` Text direction is using "first strong algorithm". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG_LTR:kotlin.Int` Text direction is using "first strong algorithm". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG_RTL:kotlin.Int` Text direction is using "first strong algorithm". |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_INHERIT:kotlin.Int` Text direction is inherited through ViewGroup |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_LOCALE:kotlin.Int` Text direction is coming from the system Locale. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_LTR:kotlin.Int` Text direction is forced to LTR. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_RTL:kotlin.Int` Text direction is forced to RTL. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#VIEW_LOG_TAG:kotlin.String` The logging tag used by this class with android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` This view is visible. |
| --- | --- |

| Public constructors ||
|---|---|
| View Simple constructor to use when creating a view from code. |
| View Constructor that is called when inflating a view from XML. |
| View Perform inflation from XML and apply a class-specific base style from a theme attribute. |
| View Perform inflation from XML and apply a class-specific base style from a theme attribute or style resource. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addChildrenForAccessibility Adds the children of this View relevant for accessibility to the given list as output. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addExtraDataToAccessibilityNodeInfo Adds extra data to an AccessibilityNodeInfo based on an explicit request for the additional data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addFocusables Add any focusable views that are descendants of this view (possibly including this view if it is focusable itself) to views. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addFocusables Adds any focusable views that are descendants of this view (possibly including this view if it is focusable itself) to views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addKeyboardNavigationClusters Adds any keyboard navigation cluster roots that are descendants of this view (possibly including this view if it is a cluster root itself) to views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnAttachStateChangeListener Add a listener for attach state changes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnLayoutChangeListener Add a listener that will be called when the bounds of the view change due to layout processing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnUnhandledKeyEventListener Adds a listener which will receive unhandled KeyEvents. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addTouchables Add any touchable views that are descendants of this view (possibly including this view if it is touchable itself) to views. |
| --- | --- |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md)! | animate This method returns a ViewPropertyAnimator object, which can be used to animate specific properties on this View. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | announceForAccessibility Convenience method for sending a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_ANNOUNCEMENT:kotlin.Int` AccessibilityEvent to suggest that an accessibility service announce the specified text to its users. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | autofill Automatically fills the content of the virtual children within this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | autofill Automatically fills the content of this view with the `value`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | bringToFront Change the view's z order in the tree, so it's on top of other sibling views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | buildDrawingCache Calling this method is equivalent to calling `buildDrawingCache(false)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | buildDrawingCache Forces the drawing cache to be built if the drawing cache is invalid. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | buildLayer Forces this view's layer to be created and this view to be rendered into its layer. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | callOnClick Directly call any attached OnClickListener. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canResolveLayoutDirection Check if layout direction resolution can be done. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canResolveTextAlignment Check if text alignment resolution can be done. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canResolveTextDirection Check if text direction resolution can be done. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canScrollHorizontally Check if this view can be scrolled horizontally in a certain direction. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canScrollVertically Check if this view can be scrolled vertically in a certain direction. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancelDragAndDrop Cancels an ongoing drag and drop operation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancelLongPress Cancels a pending long press. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancelPendingInputEvents Cancel any deferred high-level input events that were previously posted to the event queue. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | checkInputConnectionProxy Called by the InputMethodManager when a view who is not the current input connection target is trying to make a call on the manager. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearAnimation Cancels any animations for this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearFocus Called when this view wants to give up focus. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearPendingCredentialRequest Clears the request and callback previously set through setPendingCredentialRequest. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearViewTranslationCallback Clear the ViewTranslationCallback from this view. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | combineMeasuredStates Merge two states as returned by getMeasuredState. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | computeScroll Called by a parent to request that a child update its values for mScrollX and mScrollY if necessary. |
| --- | --- |
| open [WindowInsets](WindowInsets.md)! | computeSystemWindowInsets Compute insets that should be consumed by this view and the ones that should propagate to those under it. |
| open [AccessibilityNodeInfo](../android.view.accessibility/AccessibilityNodeInfo.md)! | createAccessibilityNodeInfo Returns an AccessibilityNodeInfo representing this view from the point of view of an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | createContextMenu Show the context menu for this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | destroyDrawingCache Frees the resources used by the drawing cache. |
| open [WindowInsets](WindowInsets.md)! | dispatchApplyWindowInsets Request to apply the given window insets to this view or another view in its subtree. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchCapturedPointerEvent Pass a captured pointer event down to the focused view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchConfigurationChanged Dispatch a notification about a resource configuration change down the view hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchCreateViewTranslationRequest Dispatch to collect the ViewTranslationRequests for translation purpose by traversing the hierarchy when the app requests ui translation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchDisplayHint Dispatch a hint about whether this view is displayed. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchDragEvent Detects if this View is enabled and has a drag event listener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchDrawableHotspotChanged Dispatches drawableHotspotChanged to all of this View's children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchFinishTemporaryDetach Dispatch onFinishTemporaryDetach to this View and its direct children if this is a container View. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchGenericMotionEvent Dispatch a generic motion event. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchKeyEvent Dispatch a key event to the next view on the focus path. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchKeyEventPreIme Dispatch a key event before it is processed by any input method associated with the view hierarchy. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchKeyShortcutEvent Dispatches a key shortcut event. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchNestedFling Dispatch a fling to a nested scrolling parent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchNestedPreFling Dispatch a fling to a nested scrolling parent before it is processed by this view. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchNestedPrePerformAccessibilityAction Report an accessibility action to this view's parents for delegated processing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchNestedPreScroll Dispatch one step of a nested scroll in progress before this view consumes any portion of it. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchNestedScroll Dispatch one step of a nested scroll in progress. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchPointerCaptureChanged <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchPopulateAccessibilityEvent Dispatches an AccessibilityEvent to the View to add the text content of the view and its children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchProvideAutofillStructure Dispatches creation of a ViewStructures for autofill purposes down the hierarchy, when an Assist structure is being created as part of an autofill request. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchProvideStructure Dispatch creation of ViewStructure down the hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchScrollCaptureSearch Dispatch a scroll capture search request down the view hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchStartTemporaryDetach Dispatch onStartTemporaryDetach to this View and its direct children if this is a container View. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchSystemUiVisibilityChanged Dispatch callbacks to setOnSystemUiVisibilityChangeListener down the view hierarchy. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchTouchEvent Pass the touch screen motion event down to the target view, or this view if it is the target. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchTrackballEvent Pass a trackball motion event down to the focused view. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchUnhandledMove This method is the last chance for the focused view and its ancestors to respond to an arrow key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchWindowFocusChanged Called when the window containing this view gains or loses window focus. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchWindowInsetsAnimationEnd Dispatches onEnd when Window Insets animation ends. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchWindowInsetsAnimationPrepare Dispatches onPrepare when Window Insets animation is being prepared. |
| open [WindowInsets](WindowInsets.md) | dispatchWindowInsetsAnimationProgress Dispatches onProgress when Window Insets animation makes progress. |
| open [WindowInsetsAnimation.Bounds](../android/view/WindowInsetsAnimation.Bounds.md) | dispatchWindowInsetsAnimationStart Dispatches onStart when Window Insets animation is started. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchWindowSystemUiVisiblityChanged Dispatch callbacks to onWindowSystemUiVisibilityChanged down the view hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchWindowVisibilityChanged Dispatch a window visibility change down the view hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | draw Manually render this view (and all of its children) to the given Canvas. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawableHotspotChanged This function is called whenever the view hotspot changes and needs to be propagated to drawables or child views managed by the view. |
| open [View](View.md)! | findFocus Find the view in the hierarchy rooted at this view that currently has focus. |
| [OnBackInvokedDispatcher](../android.window/OnBackInvokedDispatcher.md)? | findOnBackInvokedDispatcher Walk up the View hierarchy to find the nearest `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#`. |
| --- | --- |
| T | findViewById Finds the first descendant view with the given ID, the view itself if the ID matches getId, or `null` if the ID is invalid (\< 0) or there is no matching view in the hierarchy. |
| T | findViewWithTag Look for a child view with the given tag. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | findViewsWithText Finds the Views that contain given text. |
| --- | --- |
| open [View](View.md)! | focusSearch Find the nearest view in the specified direction that can take focus. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | forceHasOverlappingRendering Sets the behavior for overlapping rendering for this view (see hasOverlappingRendering for more details on this behavior). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | forceLayout Forces this view to be laid out during the next layout pass. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | gatherTransparentRegion This is used by the ViewRoot to perform an optimization when the view hierarchy contains one or several SurfaceView. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | generateDisplayHash Called to generate a DisplayHash for this view. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | generateViewId Generate a value suitable for use in setId. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | getAccessibilityClassName Return the class name of this object to be used for accessibility purposes. |
| open [View.AccessibilityDelegate](../android/view/View.AccessibilityDelegate.md)! | getAccessibilityDelegate Returns the delegate for implementing accessibility support via composition. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAccessibilityLiveRegion Gets the live region mode for this View. |
| --- | --- |
| open [AccessibilityNodeProvider](../android.view.accessibility/AccessibilityNodeProvider.md)! | getAccessibilityNodeProvider Gets the provider for managing a virtual view hierarchy rooted at this View and reported to `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s that explore the window content. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getAccessibilityPaneTitle Get the title of the pane for purposes of accessibility. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAccessibilityTraversalAfter Gets the id of a view after which this one is visited in accessibility traversal. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAccessibilityTraversalBefore Gets the id of a view before which this one is visited in accessibility traversal. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getAllowedHandwritingDelegatePackageName Returns the allowed package for delegate editor views for which this view may act as a handwriting delegator, as set by setAllowedHandwritingDelegatePackage. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getAllowedHandwritingDelegatorPackageName Returns the allowed package for views which may act as a handwriting delegator for this delegate editor view, as set by setAllowedHandwritingDelegatorPackage. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getAlpha The opacity of the view. |
| open [Animation](../android.view.animation/Animation.md)! | getAnimation Get the animation currently associated with this view. |
| open [Matrix](../android.graphics/Matrix.md)? | getAnimationMatrix Return the current transformation matrix of the view. |
| --- | --- |
| open [IBinder](../android.os/IBinder.md)! | getApplicationWindowToken Retrieve a unique token identifying the top-level "real" window of the window that this view is attached to. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | getAttributeResolutionStack Returns the ordered list of resource ID that are considered when resolving attribute values for this View. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | getAttributeSourceResourceMap Returns the mapping of attribute resource ID to source resource ID where the attribute value was set. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | getAutofillHints Gets the hints that help an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` determine how to autofill the view with the user's data. |
| [AutofillId](../android.view.autofill/AutofillId.md)! | getAutofillId Gets the unique, logical identifier of this view in the activity, for autofill purposes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAutofillType Describes the autofill type of this view, so an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` can create the proper AutofillValue when autofilling the view. |
| --- | --- |
| open [AutofillValue](../android.view.autofill/AutofillValue.md)? | getAutofillValue Gets the View's current autofill value. |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | getBackground Gets the background drawable |
| open [BlendMode](../android.graphics/BlendMode.md)? | getBackgroundTintBlendMode Return the blending mode used to apply the tint to the background drawable, if specified. |
| --- | --- |
| open [ColorStateList](../android.content.res/ColorStateList.md)? | getBackgroundTintList Return the tint applied to the background drawable, if specified. |
| open [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)? | getBackgroundTintMode Return the blending mode used to apply the tint to the background drawable, if specified. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getBaseline Return the offset of the widget's text baseline from the widget's top boundary. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getBottom Bottom position of this view relative to its parent. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getCameraDistance Gets the distance along the Z axis from the camera to this view. |
| open [Rect](../android.graphics/Rect.md)! | getClipBounds Returns a copy of the current setClipBounds. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getClipBounds Populates an output rectangle with the clip bounds of the view, returning `true` if successful or `false` if the view's clip bounds are `null`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getClipToOutline Returns whether the Outline should be used to clip the contents of the View. |
| [ContentCaptureSession](../android.view.contentcapture/ContentCaptureSession.md)? | getContentCaptureSession Gets the session used to notify content capture events. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | getContentDescription Returns the View's content description. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getContentSensitivity Gets content sensitivity mode to determine whether this view displays sensitive content. |
| [Context](../android.content/Context.md)! | getContext Returns the context the view is running in, through which it can access the current theme, resources, etc. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getDefaultFocusHighlightEnabled Returns whether this View should use a default focus highlight when it gets focused but doesn't have `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` defined in its background. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDefaultSize Utility to return a default size. |
| open [Display](Display.md)! | getDisplay Gets the logical display to which the view's window has been attached. |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | getDrawableState Return an array of resource IDs of the drawable states representing the current state of the view. |
| open [Bitmap](../android.graphics/Bitmap.md)! | getDrawingCache Calling this method is equivalent to calling `getDrawingCache(false)`. |
| open [Bitmap](../android.graphics/Bitmap.md)! | getDrawingCache Returns the bitmap in which this view drawing is cached. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDrawingCacheBackgroundColor <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDrawingCacheQuality Returns the quality of the drawing cache. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getDrawingRect Return the visible drawing bounds of your view. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getDrawingTime Return the time at which the drawing of the view hierarchy started. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getElevation The base elevation of this view relative to its parent, in pixels. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getExplicitStyle Returns the resource ID for the style specified using `style="..."` in the `https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#`'s backing XML element or `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int` otherwise if not specified or otherwise not applicable. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getFilterTouchesWhenObscured Gets whether the framework should discard touches when the view's window is obscured by another visible window at the touched location. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getFitsSystemWindows Check for state of setFitsSystemWindows. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getFocusable Returns the focusable setting for this view. |
| --- | --- |
| open [ArrayList](../java.util/ArrayList.md)\< [View](View.md)!\>! | getFocusables Find and return all focusable views that are descendants of this view, possibly including this view if it is focusable itself. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getFocusedRect When a view has focus and the user navigates away from it, the next view is searched for starting from the rectangle filled in by this method. |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | getForeground Returns the drawable used as the foreground of this View. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getForegroundGravity Describes how the foreground is positioned. |
| open [BlendMode](../android.graphics/BlendMode.md)? | getForegroundTintBlendMode Return the blending mode used to apply the tint to the foreground drawable, if specified. |
| open [ColorStateList](../android.content.res/ColorStateList.md)? | getForegroundTintList Return the tint applied to the foreground drawable, if specified. |
| --- | --- |
| open [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)? | getForegroundTintMode Return the blending mode used to apply the tint to the foreground drawable, if specified. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getFrameContentVelocity Get the current velocity of the View. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getGlobalVisibleRect Sets `r` to the coordinates of the non-clipped area of this view in the coordinate space of the view's root view. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getGlobalVisibleRect Sets `r` to the coordinates of the non-clipped area of this view in the coordinate space of the view's root view. |
| open [Handler](../android.os/Handler.md)! | getHandler <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getHandwritingBoundsOffsetBottom Return the amount of offset applied to the bottom edge of this view's handwriting bounds, in the unit of pixel. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getHandwritingBoundsOffsetLeft Return the amount of offset applied to the left edge of this view's handwriting bounds, in the unit of pixel. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getHandwritingBoundsOffsetRight Return the amount of offset applied to the right edge of this view's handwriting bounds, in the unit of pixel. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getHandwritingBoundsOffsetTop Return the amount of offset applied to the top edge of this view's handwriting bounds, in the unit of pixel. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHandwritingDelegateFlags Returns flags configuring the handwriting delegation behavior for this delegate editor view, as set by setHandwritingDelegateFlags. |
| open [Runnable](../java.lang/Runnable.md)? | getHandwritingDelegatorCallback Returns the callback set by setHandwritingDelegatorCallback which should be called when a stylus MotionEvent occurs within this view's bounds. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getHasOverlappingRendering Returns the value for overlapping rendering that is used internally. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHeight Return the height of your view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getHitRect Hit rectangle in parent's coordinates |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHorizontalFadingEdgeLength Returns the size of the horizontal faded edges used to indicate that more content in this view is visible. |
| --- | --- |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | getHorizontalScrollbarThumbDrawable Returns the currently configured Drawable for the thumb of the horizontal scroll bar if it exists, null otherwise. |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | getHorizontalScrollbarTrackDrawable Returns the currently configured Drawable for the track of the horizontal scroll bar if it exists, null otherwise. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getId Returns this view's identifier. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getImportantForAccessibility Gets the mode for determining whether this View is important for accessibility. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getImportantForAutofill Gets the mode for determining whether this view is important for autofill. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getImportantForContentCapture Gets the mode for determining whether this view is important for content capture. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getKeepScreenOn Returns whether the screen should remain on, corresponding to the current value of `https://developer.android.com/reference/kotlin/android/view/View#KEEP_SCREEN_ON:kotlin.Int`. |
| open [KeyEvent.DispatcherState](../android/view/KeyEvent.DispatcherState.md)! | getKeyDispatcherState Return the global `https://developer.android.com/reference/kotlin/android/view/KeyEvent.DispatcherState` for this view's window. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLabelFor Gets the id of a view for which this view serves as a label for accessibility purposes. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLayerType Indicates what type of layer is currently associated with this view. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLayoutDirection Returns the resolved layout direction for this view. |
| open [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)! | getLayoutParams Get the LayoutParams associated with this view. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLeft Left position of this view relative to its parent. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getLocalVisibleRect Sets `r` to the coordinates of the non-clipped area of this view relative to the top left corner of the view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getLocationInSurface Gets the coordinates of this view in the coordinate space of the Surface that contains the view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getLocationInWindow Gets the coordinates of this view in the coordinate space of the window that contains the view, irrespective of system decorations. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getLocationOnScreen Gets the coordinates of this view in the coordinate space of the device screen, irrespective of system decorations and whether the system is in multi-window mode. |
| open [Matrix](../android.graphics/Matrix.md)! | getMatrix The transform matrix of this view, which is calculated based on the current rotation, scale, and pivot properties. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMeasuredHeight Like getMeasuredHeightAndState, but only returns the raw height component (that is the result is masked by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int`). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMeasuredHeightAndState Return the full height measurement information for this view as computed by the most recent call to measure. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMeasuredState Return only the state bits of getMeasuredWidthAndState and getMeasuredHeightAndState, combined into one integer. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMeasuredWidth Like getMeasuredWidthAndState, but only returns the raw width component (that is the result is masked by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int`). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMeasuredWidthAndState Return the full width measurement information for this view as computed by the most recent call to measure. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMinimumHeight Returns the minimum height of the view. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMinimumWidth Returns the minimum width of the view. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNextClusterForwardId Gets the id of the root of the next keyboard navigation cluster. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNextFocusDownId Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNextFocusForwardId Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNextFocusLeftId Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNextFocusRightId Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNextFocusUpId Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int`. |
| open [View.OnFocusChangeListener](../android/view/View.OnFocusChangeListener.md)! | getOnFocusChangeListener Returns the focus-change callback registered for this view. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getOutlineAmbientShadowColor <br /> |
| --- | --- |
| open [ViewOutlineProvider](ViewOutlineProvider.md)! | getOutlineProvider Returns the current ViewOutlineProvider of the view, which generates the Outline that defines the shape of the shadow it casts, and enables outline clipping. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getOutlineSpotShadowColor <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getOverScrollMode Returns the over-scroll mode for this view. |
| --- | --- |
| open [ViewOverlay](ViewOverlay.md)! | getOverlay Returns the overlay for this view, creating it if it does not yet exist. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPaddingBottom Returns the bottom padding of this view. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPaddingEnd Returns the end padding of this view depending on its resolved layout direction. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPaddingLeft Returns the left padding of this view. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPaddingRight Returns the right padding of this view. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPaddingStart Returns the start padding of this view depending on its resolved layout direction. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPaddingTop Returns the top padding of this view. |
| [ViewParent](ViewParent.md)! | getParent Gets the parent of this view. |
| open [ViewParent](ViewParent.md)! | getParentForAccessibility Gets the parent for accessibility purposes. |
| --- | --- |
| [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [GetCredentialResponse](../android.credentials/GetCredentialResponse.md)!, [GetCredentialException](../android.credentials/GetCredentialException.md)!\>? | getPendingCredentialCallback Returns the callback that has previously been set up on this view through the setPendingCredentialRequest API. |
| [GetCredentialRequest](../android.credentials/GetCredentialRequest.md)? | getPendingCredentialRequest Returns the `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#` associated with the view. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getPivotX The x location of the point around which the view is setRotation and setScaleX. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getPivotY The y location of the point around which the view is setRotation and setScaleY. |
| open [PointerIcon](PointerIcon.md)! | getPointerIcon Gets the mouse pointer icon for the current view. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](../android.graphics/Rect.md)!\> | getPreferKeepClearRects <br /> |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | getReceiveContentMimeTypes Returns the MIME types accepted by performReceiveContent for this view, as configured via setOnReceiveContentListener. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getRequestedFrameRate Get the current preferred frame rate of the View. |
| open [Resources](../android.content.res/Resources.md)! | getResources Returns the resources associated with this view. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getRevealOnFocusHint Returns this view's preference for reveal behavior when it gains focus. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRight Right position of this view relative to its parent. |
| open [AttachedSurfaceControl](AttachedSurfaceControl.md)? | getRootSurfaceControl The AttachedSurfaceControl itself is not a View, it is just the interface to the windowing-system object that contains the entire view hierarchy. |
| --- | --- |
| open [View](View.md)! | getRootView Finds the topmost view in the current view hierarchy. |
| open [WindowInsets](WindowInsets.md)! | getRootWindowInsets Provide original WindowInsets that are dispatched to the view hierarchy. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getRotation The degrees that the view is rotated around the pivot point. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getRotationX The degrees that the view is rotated around the horizontal axis through the pivot point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getRotationY The degrees that the view is rotated around the vertical axis through the pivot point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getScaleX The amount that the view is scaled in x around the pivot point, as a proportion of the view's unscaled width. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getScaleY The amount that the view is scaled in y around the pivot point, as a proportion of the view's unscaled height. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScrollBarDefaultDelayBeforeFade Returns the delay before scrollbars fade. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScrollBarFadeDuration Returns the scrollbar fade duration. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScrollBarSize Returns the scrollbar size. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScrollBarStyle Returns the current scrollbar style. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScrollCaptureHint Returns the current scroll capture hint for this view. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScrollIndicators Returns a bitmask representing the enabled scroll indicators. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScrollX Return the scrolled left position of this view. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScrollY Return the scrolled top position of this view. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSolidColor Override this if your view is known to always be drawn on top of a solid color background, and needs to draw fading edges. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSourceLayoutResId A View can be inflated from an XML layout. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getStateDescription Returns the View's state description. |
| --- | --- |
| open [StateListAnimator](../android.animation/StateListAnimator.md)! | getStateListAnimator Returns the current StateListAnimator if exists. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getSupplementalDescription Returns the View's supplemental description. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](../android.graphics/Rect.md)!\> | getSystemGestureExclusionRects Retrieve the list of areas within this view's post-layout coordinate space where the system should not intercept touch or other pointing device gestures. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSystemUiVisibility Returns the last setSystemUiVisibility that this view has requested. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | getTag Returns this view's tag. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | getTag Returns the tag associated with this view and the specified key. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getTextAlignment Return the resolved text alignment. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getTextDirection Return the resolved text direction. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getTooltipText Returns the view's tooltip text. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getTop Top position of this view relative to its parent. |
| open [TouchDelegate](TouchDelegate.md)! | getTouchDelegate Gets the TouchDelegate for this View. |
| open [ArrayList](../java.util/ArrayList.md)\< [View](View.md)!\>! | getTouchables Find and return all touchable views that are descendants of this view, possibly including this view if it is touchable itself. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getTransitionAlpha This property is intended only for use by the Fade transition, which animates it to produce a visual translucency that does not side-effect (or get affected by) the real alpha property. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getTransitionName Returns the name of the View to be used to identify Views in Transitions. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getTranslationX The horizontal location of this view relative to its getLeft position. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getTranslationY The vertical location of this view relative to its getTop position. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getTranslationZ The depth location of this view relative to its getElevation. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getUniqueDrawingId Get the identifier used for this view by the drawing system. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getVerticalFadingEdgeLength Returns the size of the vertical faded edges used to indicate that more content in this view is visible. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getVerticalScrollbarPosition <br /> |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | getVerticalScrollbarThumbDrawable Returns the currently configured Drawable for the thumb of the vertical scroll bar if it exists, null otherwise. |
| --- | --- |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | getVerticalScrollbarTrackDrawable Returns the currently configured Drawable for the track of the vertical scroll bar if it exists, null otherwise. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getVerticalScrollbarWidth Returns the width of the vertical scrollbar. |
| open [ViewTranslationResponse](../android.view.translation/ViewTranslationResponse.md)? | getViewTranslationResponse Returns the ViewTranslationResponse associated with this view. |
| --- | --- |
| open [ViewTreeObserver](ViewTreeObserver.md)! | getViewTreeObserver Returns the ViewTreeObserver for this view's hierarchy. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getVisibility Returns the visibility status for this view. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getWidth Return the width of your view. |
| --- | --- |
| open [WindowId](WindowId.md)! | getWindowId Retrieve the WindowId for the window this view is currently attached to. |
| open [WindowInsetsController](WindowInsetsController.md)? | getWindowInsetsController Retrieves the single WindowInsetsController of the window this view is attached to. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getWindowSystemUiVisibility Returns the current system UI visibility that is currently set for the entire window. |
| --- | --- |
| open [IBinder](../android.os/IBinder.md)! | getWindowToken Retrieve a unique token identifying the window this view is attached to. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getWindowVisibility Returns the current visibility of the window this view is attached to (either `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getWindowVisibleDisplayFrame Retrieve the overall visible display size in which the window this view is attached to has been positioned in. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getX The visual x position of this view, in pixels. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getY The visual y position of this view, in pixels. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getZ The visual z position of this view, in pixels. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasExplicitFocusable Returns true if this view is focusable or if it contains a reachable View for which hasExplicitFocusable returns `true`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasFocus Returns true if this view has focus itself, or is the ancestor of the view that has focus. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasFocusable Returns true if this view is focusable or if it contains a reachable View for which hasFocusable returns `true`. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNestedScrollingParent Returns true if this view has a nested scrolling parent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasOnClickListeners Return whether this view has an attached OnClickListener. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasOnLongClickListeners Return whether this view has an attached OnLongClickListener. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasOverlappingRendering Returns whether this View has content which overlaps. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasPointerCapture Checks pointer capture status. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasTransientState Indicates whether the view is currently tracking transient state that the app should not need to concern itself with saving and restoring, but that the framework should take special note to preserve when possible. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasWindowFocus Returns true if this view is in a window that currently has window focus. |
| open static [View](View.md)! | inflate Inflate a view from an XML resource. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | invalidate Invalidate the whole view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | invalidate Mark the area defined by dirty as needing to be drawn. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | invalidate Mark the area defined by the rect (l,t,r,b) as needing to be drawn. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | invalidateDrawable Invalidates the specified Drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | invalidateOutline Called to rebuild this View's Outline from its ViewOutlineProvider |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAccessibilityDataSensitive Whether this view should restrict accessibility service access only to services that have the isAccessibilityTool property set to true. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAccessibilityFocused Returns whether this View is accessibility focused. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAccessibilityHeading Gets whether this view is a heading for accessibility purposes. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isActivated Indicates the activation state of this view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAttachedToWindow Returns true if this view is currently attached to a window. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAutoHandwritingEnabled Return whether the View allows automatic handwriting initiation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isClickable Indicates whether this view reacts to click events or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isContentCaptureSelfReportingEnabled Returns whether this View automatically reports its lifecycle events and layout bounds to the Content Capture Version 2. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isContentSensitive Returns whether this view displays sensitive content, based on the value explicitly set by setContentSensitivity. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isContextClickable Indicates whether this view reacts to context clicks or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isCredential Gets the mode for determining whether this view is a credential. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDirty True if this view has changed since the last time being drawn. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDrawingCacheEnabled Indicates whether the drawing cache is enabled for this view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDuplicateParentStateEnabled Indicates whether this duplicates its drawable state from its parent. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isEnabled Returns the enabled status for this view. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isFocusable Returns whether this View is currently able to take focus. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isFocusableInTouchMode When a view is focusable, it may not want to take focus when in touch mode. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isFocused Returns true if this view has focus |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isFocusedByDefault Returns whether this View should receive focus when the focus is restored for the view hierarchy containing this view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isForceDarkAllowed See setForceDarkAllowed |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isHandwritingDelegate Returns whether this view has been set as a handwriting delegate by setIsHandwritingDelegate. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isHapticFeedbackEnabled <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isHardwareAccelerated Indicates whether this view is attached to a hardware accelerated window or not. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isHorizontalFadingEdgeEnabled Indicate whether the horizontal edges are faded when the view is scrolled horizontally. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isHorizontalScrollBarEnabled Indicate whether the horizontal scrollbar should be drawn or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isHovered Returns true if the view is currently hovered. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isImportantForAccessibility Computes whether this view should be exposed for accessibility. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isImportantForAutofill Hints the Android System whether the `https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.ViewNode.html#` associated with this view is considered important for autofill purposes. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isImportantForContentCapture Hints the Android System whether this view is considered important for content capture, based on the value explicitly set by setImportantForContentCapture and heuristics when it's `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_AUTO:kotlin.Int`. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isInEditMode Indicates whether this View is currently in edit mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isInLayout Returns whether the view hierarchy is currently undergoing a layout pass. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isInTouchMode Returns the touch mode state associated with this view. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isKeyboardNavigationCluster Returns whether this View is a root of a keyboard navigation cluster. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isLaidOut Returns true if this view has been through at least one layout since it was last attached to or detached from a window. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isLayoutDirectionResolved <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isLayoutRequested Indicates whether or not this view's layout will be requested during the next hierarchy layout pass. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isLongClickable Indicates whether this view reacts to long click events or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isNestedScrollingEnabled Returns true if nested scrolling is enabled for this view. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isOpaque Indicates whether this View is opaque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPaddingRelative Return if the padding has been set through relative values setPaddingRelative or through |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPivotSet Returns whether or not a pivot has been set by a call to setPivotX or setPivotY. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPreferKeepClear Retrieve the preference for this view to be kept clear. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPressed Indicates whether the view is currently in pressed state. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSaveEnabled Indicates whether this view will save its state (that is, whether its onSaveInstanceState method will be called). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSaveFromParentEnabled Indicates whether the entire hierarchy under this view will save its state when a state saving traversal occurs from its parent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isScreenReaderFocusable Returns whether the view should be treated as a focusable unit by screen reader accessibility tools. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isScrollContainer Indicates whether this view is one of the set of scrollable containers in its window. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isScrollbarFadingEnabled Returns true if scrollbars will fade when this view is not scrolling |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSelected Indicates the selection state of this view. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isShowingLayoutBounds Returns `true` when the View is attached and the system developer setting to show the layout bounds is enabled or `false` otherwise. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isShown Returns the visibility of this view and all of its ancestors |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSoundEffectsEnabled <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isTemporarilyDetached Tells whether the View is in the state between onStartTemporaryDetach and onFinishTemporaryDetach. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isTextAlignmentResolved <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isTextDirectionResolved <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isVerticalFadingEdgeEnabled Indicate whether the vertical edges are faded when the view is scrolled horizontally. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isVerticalScrollBarEnabled Indicate whether the vertical scrollbar should be drawn or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isVisibleToUserForAutofill Computes whether this virtual autofill view is visible to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | jumpDrawablesToCurrentState Call jumpToCurrentState on all Drawable objects associated with this view. |
| --- | --- |
| open [View](View.md)! | keyboardNavigationClusterSearch Find the nearest keyboard navigation cluster in the specified direction. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | layout Assign a size and position to a view and all of its descendants |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | measure This is called to find out how big a view should be. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | offsetLeftAndRight Offset this view's horizontal location by the specified amount of pixels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | offsetTopAndBottom Offset this view's vertical location by the specified number of pixels. |
| open [WindowInsets](WindowInsets.md)! | onApplyWindowInsets Called when the view should apply WindowInsets according to its internal policy. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onCancelPendingInputEvents Called as the result of a call to cancelPendingInputEvents on this view or a parent view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onCapturedPointerEvent Implement this method to handle captured pointer events |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onCheckIsTextEditor Check whether the called view is a text editor, in which case it would make sense to automatically display a soft input window for it. |
| --- | --- |
| open [InputConnection](../android.view.inputmethod/InputConnection.md)! | onCreateInputConnection Create a new InputConnection for an InputMethod to interact with the view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onCreateViewTranslationRequest Collects a ViewTranslationRequest which represents the content to be translated in the view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onCreateVirtualViewTranslationRequests Collects ViewTranslationRequests which represents the content to be translated for the virtual views in the host view. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onDragEvent Handles drag events sent by the system following a call to startDragAndDrop. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDrawForeground Draw any foreground content for this view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onFilterTouchEventForSecurity Filter the touch event to apply security policies. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onFinishTemporaryDetach Called after onStartTemporaryDetach when the container is done changing the view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onGenericMotionEvent Implement this method to handle generic motion events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onHoverChanged Implement this method to handle hover state changes. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onHoverEvent Implement this method to handle hover events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onInitializeAccessibilityEvent Initializes an AccessibilityEvent with information about this View which is the event source. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onInitializeAccessibilityNodeInfo Initializes an AccessibilityNodeInfo with information about this view. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onKeyDown Default implementation of onKeyDown: perform press of the view when `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_CENTER:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ENTER:kotlin.Int` is released, if the view is enabled and clickable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onKeyLongPress Default implementation of onKeyLongPress: always returns false (doesn't handle the event). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onKeyMultiple Default implementation of onKeyMultiple: always returns false (doesn't handle the event). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onKeyPreIme Handle a key event before it is processed by any input method associated with the view hierarchy. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onKeyShortcut Called on the focused view when a key shortcut event is not handled. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onKeyUp Default implementation of onKeyUp: perform clicking of the view when `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_CENTER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ENTER:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SPACE:kotlin.Int` is released. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPointerCaptureChange Called when the window has just acquired or lost pointer capture. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPopulateAccessibilityEvent Called from dispatchPopulateAccessibilityEvent giving a chance to this View to populate the accessibility event with its text content. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onProvideAutofillStructure Populates a ViewStructure to fullfil an autofill request. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onProvideAutofillVirtualStructure Populates a ViewStructure containing virtual children to fullfil an autofill request. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onProvideContentCaptureNodeProperties Populates the properties of this View for Content Capture version 2. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onProvideContentCaptureStructure Populates a ViewStructure for content capture. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onProvideStructure Called when assist structure is being retrieved from a view as part of onProvideAssistData. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onProvideVirtualStructure Called when assist structure is being retrieved from a view as part of onProvideAssistData to generate additional virtual structure under this view. |
| open [ContentInfo](ContentInfo.md)? | onReceiveContent Implements the default behavior for receiving content for this type of view. |
| --- | --- |
| open [PointerIcon](PointerIcon.md)! | onResolvePointerIcon Resolve the pointer icon that should be used for specified pointer in the motion event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRtlPropertiesChanged Called when any RTL property (layout direction or text direction or text alignment) has been changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onScreenStateChanged This method is called whenever the state of the screen this view is attached to changes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onScrollCaptureSearch Called when scroll capture is requested, to search for appropriate content to scroll. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onStartTemporaryDetach This is called when a container is going to temporarily detach a child, with detachViewFromParent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onTouchEvent Implement this method to handle pointer events. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onTrackballEvent Implement this method to handle trackball motion events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onViewTranslationResponse Called when the content from onCreateViewTranslationRequest had been translated by the TranslationService. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onVirtualViewTranslationResponses Called when the content from onCreateVirtualViewTranslationRequests had been translated by the TranslationService. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onVisibilityAggregated Called when the user-visibility of this View is potentially affected by a change to this view itself, an ancestor view or the window this view is attached to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onWindowFocusChanged Called when the window containing this view gains or loses focus. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onWindowSystemUiVisibilityChanged Override to find out when the window's requested system UI visibility has changed, that is the value returned by getWindowSystemUiVisibility. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performAccessibilityAction Performs the specified accessibility action on the view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performClick Call this view's OnClickListener, if it is defined. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performContextClick Call this view's OnContextClickListener, if it is defined. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performContextClick Call this view's OnContextClickListener, if it is defined. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performHapticFeedback Like performHapticFeedback, but takes a `https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.html#`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performHapticFeedback BZZZTT!!1! |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performHapticFeedback BZZZTT!!1! |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performLongClick Calls this view's OnLongClickListener, if it is defined. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performLongClick Calls this view's OnLongClickListener, if it is defined. |
| --- | --- |
| open [ContentInfo](ContentInfo.md)? | performReceiveContent Receives the given content. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | playSoundEffect Play a sound effect for this view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | post Causes the Runnable to be added to the message queue. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | postDelayed Causes the Runnable to be added to the message queue, to be run after the specified amount of time elapses. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | postInvalidate Cause an invalidate to happen on a subsequent cycle through the event loop. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | postInvalidate Cause an invalidate of the specified area to happen on a subsequent cycle through the event loop. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | postInvalidateDelayed Cause an invalidate to happen on a subsequent cycle through the event loop. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | postInvalidateDelayed Cause an invalidate of the specified area to happen on a subsequent cycle through the event loop. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | postInvalidateOnAnimation Cause an invalidate to happen on the next animation time step, typically the next display frame. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | postInvalidateOnAnimation Cause an invalidate of the specified area to happen on the next animation time step, typically the next display frame. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | postOnAnimation Causes the Runnable to execute on the next animation time step. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | postOnAnimationDelayed Causes the Runnable to execute on the next animation time step, after the specified amount of time elapses. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | refreshDrawableState Call this to force a view to update its drawable state. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerCalledFromWrongThreadListener Registers a listener that is notified when a View API is called from the wrong thread. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | releasePointerCapture Releases the pointer capture. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | removeCallbacks Removes the specified Runnable from the message queue. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnAttachStateChangeListener Remove a listener for attach state changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnLayoutChangeListener Remove a listener for layout changes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnUnhandledKeyEventListener Removes a listener which will receive unhandled KeyEvents. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | reportAppJankStats Called from apps when they want to report jank stats to the system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestApplyInsets Ask that a new dispatch of onApplyWindowInsets be performed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestFitSystemWindows Ask that a new dispatch of fitSystemWindows be performed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | requestFocus Call this to try to give focus to a specific view or to one of its descendants. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | requestFocus Call this to try to give focus to a specific view or to one of its descendants and give it a hint about what direction focus is heading. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | requestFocus Call this to try to give focus to a specific view or to one of its descendants and give it hints about the direction and a specific rectangle that the focus is coming from. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | requestFocusFromTouch Call this to try to give focus to a specific view or to one of its descendants. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestLayout Call this when something has changed which has invalidated the layout of this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestPointerCapture Requests pointer capture in relative mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestPointerCapture Requests pointer capture in the specified mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | requestRectangleOnScreen Request that a rectangle of this view be visible on the screen, scrolling if necessary just enough. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | requestRectangleOnScreen Request that a rectangle of this view be visible on the screen, scrolling if necessary just enough. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | requestRectangleOnScreen Request that a rectangle of this view be visible on the screen, scrolling if necessary just enough. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestUnbufferedDispatch Request unbuffered dispatch of the given stream of MotionEvents to this View. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestUnbufferedDispatch Request unbuffered dispatch of the given event source class to this view. |
| T | requireViewById Finds the first descendant view with the given ID, the view itself if the ID matches getId, or throws an IllegalArgumentException if the ID is invalid or there is no matching view in the hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | resetPivot Clears any pivot previously set by a call to setPivotX or setPivotY. |
| --- | --- |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | resolveSize Version of resolveSizeAndState returning only the `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` bits of the result. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | resolveSizeAndState Utility to reconcile a desired size and state, with constraints imposed by a MeasureSpec. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | restoreDefaultFocus Gives focus to the default-focus view in the view hierarchy that has this view as a root. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | restoreHierarchyState Restore this view hierarchy's frozen state from the given container. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | saveAttributeDataForStyleable Stores debugging information about attributes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | saveHierarchyState Store this view hierarchy's frozen state into the given container. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | scheduleDrawable Schedules an action on a drawable to occur at a specified time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | scrollBy Move the scrolled position of your view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | scrollTo Set the scrolled position of your view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendAccessibilityEvent Sends an accessibility event of the given type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendAccessibilityEventUnchecked This method behaves exactly as sendAccessibilityEvent but takes as an argument an empty AccessibilityEvent and does not perform a check whether accessibility is enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAccessibilityDataSensitive Specifies whether this view should only allow interactions from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s with the isAccessibilityTool property set to true. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAccessibilityDelegate Sets a delegate for implementing accessibility support via composition (as opposed to inheritance). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAccessibilityHeading Set if view is a heading for a section of content for accessibility purposes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAccessibilityLiveRegion Sets the live region mode for this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAccessibilityPaneTitle Visually distinct portion of a window with window-like semantics are considered panes for accessibility purposes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAccessibilityTraversalAfter Sets the id of a view that screen readers are requested to visit before this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAccessibilityTraversalBefore Sets the id of a view that screen readers are requested to visit after this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setActivated Changes the activated state of this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAllowClickWhenDisabled Enables or disables click events for this view when disabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAllowedHandwritingDelegatePackage Specifies that this view may act as a handwriting initiation delegator for a delegate editor view from the specified package. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAllowedHandwritingDelegatorPackage Specifies that a view from the specified package may act as a handwriting delegator for this delegate editor view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAlpha Sets the opacity of the view to a value from 0 to 1, where 0 means the view is completely transparent and 1 means the view is completely opaque. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAnimation Sets the next animation to play for this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAnimationMatrix Changes the transformation matrix on the view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAutoHandwritingEnabled Set whether this view enables automatic handwriting initiation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAutofillHints Sets the hints that help an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` determine how to autofill the view with the user's data. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAutofillId Sets the unique, logical identifier of this view in the activity, for autofill purposes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBackdropRenderEffect Configure the `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#` to apply to the backdrop contents of this View. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBackground Set the background to a given Drawable, or remove the background. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBackgroundColor Sets the background color for this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBackgroundDrawable <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBackgroundResource Set the background to a given resource. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBackgroundTintBlendMode Specifies the blending mode used to apply the tint specified by setBackgroundTintList} to the background drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBackgroundTintList Applies a tint to the background drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBackgroundTintMode Specifies the blending mode used to apply the tint specified by setBackgroundTintList} to the background drawable. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBottom Sets the bottom position of this view relative to its parent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCameraDistance Sets the distance along the Z axis (orthogonal to the X/Y plane on which views are drawn) from the camera to this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setClickable Enables or disables click events for this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setClipBounds Sets a rectangular area on this view to which the view will be clipped when it is drawn. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setClipToOutline Sets whether the View's Outline should be used to clip the contents of the View. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setContentCaptureSession Sets the (optional) ContentCaptureSession associated with this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setContentDescription Sets the View's content description. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setContentSensitivity Sets content sensitivity mode to determine whether this view displays sensitive content (e.g. username, password etc.). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setContextClickable Enables or disables context clicking for this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDefaultFocusHighlightEnabled Sets whether this View should use a default focus highlight when it gets focused but doesn't have `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` defined in its background. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDrawingCacheBackgroundColor Setting a solid background color for the drawing cache's bitmaps will improve performance and memory usage. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDrawingCacheEnabled Enables or disables the drawing cache. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDrawingCacheQuality Set the drawing cache quality of this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDuplicateParentStateEnabled Enables or disables the duplication of the parent's state into this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setElevation Sets the base elevation of this view, in pixels. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setEnabled Set the enabled state of this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFadingEdgeLength Set the size of the faded edge used to indicate that more content in this view is available. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFilterTouchesWhenObscured Sets whether the framework should discard touches when the view's window is obscured by another visible window at the touched location. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFitsSystemWindows Sets whether or not this view should account for system screen decorations such as the status bar and inset its content; that is, controlling whether the default implementation of fitSystemWindows will be executed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFocusable Set whether this view can receive the focus. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFocusable Sets whether this view can receive focus. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFocusableInTouchMode Set whether this view can receive focus while in touch mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFocusedByDefault Sets whether this View should receive focus when the focus is restored for the view hierarchy containing this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setForceDarkAllowed Sets whether or not to allow force dark to apply to this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setForeground Supply a Drawable that is to be rendered on top of all of the content in the view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setForegroundGravity Describes how the foreground is positioned. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setForegroundTintBlendMode Specifies the blending mode used to apply the tint specified by setForegroundTintList} to the background drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setForegroundTintList Applies a tint to the foreground drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setForegroundTintMode Specifies the blending mode used to apply the tint specified by setForegroundTintList} to the background drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFrameContentVelocity Set the current velocity of the View, we only track positive value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHandwritingBoundsOffsets Set the amount of offset applied to this view's stylus handwriting bounds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHandwritingDelegateFlags Sets flags configuring the handwriting delegation behavior for this delegate editor view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHandwritingDelegatorCallback Sets a callback which should be called when a stylus MotionEvent occurs within this view's bounds. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHapticFeedbackEnabled Set whether this view should have haptic feedback for events such as long presses. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHasTransientState Set whether this view is currently tracking transient state that the framework should attempt to preserve when possible. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHorizontalFadingEdgeEnabled Define whether the horizontal edges should be faded when this view is scrolled horizontally. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHorizontalScrollBarEnabled Define whether the horizontal scrollbar should be drawn or not. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHorizontalScrollbarThumbDrawable Defines the horizontal thumb drawable |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHorizontalScrollbarTrackDrawable Defines the horizontal track drawable |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHovered Sets whether the view is currently hovered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setId Sets the identifier for this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setImportantForAccessibility Sets how to determine whether this view is important for accessibility which is if it fires accessibility events and if it is reported to accessibility services that query the screen. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setImportantForAutofill Sets the mode for determining whether this view is considered important for autofill. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setImportantForContentCapture Sets the mode for determining whether this view is considered important for content capture. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setIsCredential Sets whether this view is a credential for Credential Manager purposes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setIsHandwritingDelegate Sets this view to be a handwriting delegate. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setKeepScreenOn Controls whether the screen should remain on, modifying the value of `https://developer.android.com/reference/kotlin/android/view/View#KEEP_SCREEN_ON:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setKeyboardNavigationCluster Set whether this view is a root of a keyboard navigation cluster. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLabelFor Sets the id of a view for which this view serves as a label for accessibility purposes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLayerPaint Updates the `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` object used with the current layer (used only if the current layer type is not set to `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLayerType Specifies the type of layer backing this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLayoutDirection Set the layout direction for this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLayoutParams Set the layout parameters associated with this view. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLeft Sets the left position of this view relative to its parent. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLeftTopRightBottom Assign a size and position to this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLongClickable Enables or disables long click events for this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMinimumHeight Sets the minimum height of the view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMinimumWidth Sets the minimum width of the view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNestedScrollingEnabled Enable or disable nested scrolling for this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNextClusterForwardId Sets the id of the view to use as the root of the next keyboard navigation cluster. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNextFocusDownId Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNextFocusForwardId Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNextFocusLeftId Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNextFocusRightId Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNextFocusUpId Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnApplyWindowInsetsListener Set an `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener` to take over the policy for applying window insets to this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnCapturedPointerListener Set a listener to receive callbacks when the pointer capture state of a view changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnClickListener Register a callback to be invoked when this view is clicked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnContextClickListener Register a callback to be invoked when this view is context clicked. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnCreateContextMenuListener Register a callback to be invoked when the context menu for this view is being built. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnDragListener Register a drag event listener callback object for this View. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnFocusChangeListener Register a callback to be invoked when focus of this view changed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnGenericMotionListener Register a callback to be invoked when a generic motion event is sent to this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnHoverListener Register a callback to be invoked when a hover event is sent to this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnKeyListener Register a callback to be invoked when a hardware key is pressed in this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnLongClickListener Register a callback to be invoked when this view is clicked and held. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnReceiveContentListener Sets the listener to be performReceiveContent to handle insertion of content into this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnScrollChangeListener Register a callback to be invoked when the scroll X or Y positions of this view change. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnSystemUiVisibilityChangeListener Set a listener to receive callbacks when the visibility of the system bar changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnTouchListener Register a callback to be invoked when a touch event is sent to this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOutlineAmbientShadowColor Sets the color of the ambient shadow that is drawn when the view has a positive Z or elevation value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOutlineProvider Sets the ViewOutlineProvider of the view, which generates the Outline that defines the shape of the shadow it casts, and enables outline clipping. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOutlineSpotShadowColor Sets the color of the spot shadow that is drawn when the view has a positive Z or elevation value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOverScrollMode Set the over-scroll mode for this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPadding Sets the padding. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPaddingRelative Sets the relative padding. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPendingCredentialRequest Sets a `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` request to retrieve credentials, when the user focuses on this given view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPivotX Sets the x location of the point around which the view is setRotation and setScaleX. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPivotY Sets the y location of the point around which the view is setRotation and setScaleY. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPointerIcon Set the pointer icon to be used for a mouse pointer in the current view. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPreferKeepClear Set a preference to keep the bounds of this view clear from floating windows above this view's window. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPreferKeepClearRects Set a preference to keep the provided rects clear from floating windows above this view's window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPressed Sets the pressed state for this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRenderEffect Configure the `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#` to apply to this View. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRequestedFrameRate You can set the preferred frame rate for a View using a positive number or by specifying the preferred frame rate category using constants, including REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE, REQUESTED_FRAME_RATE_CATEGORY_LOW, REQUESTED_FRAME_RATE_CATEGORY_NORMAL, REQUESTED_FRAME_RATE_CATEGORY_HIGH. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRevealOnFocusHint Sets this view's preference for reveal behavior when it gains focus. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRight Sets the right position of this view relative to its parent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRotation Sets the degrees that the view is rotated around the pivot point. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRotationX Sets the degrees that the view is rotated around the horizontal axis through the pivot point. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRotationY Sets the degrees that the view is rotated around the vertical axis through the pivot point. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSaveEnabled Controls whether the saving of this view's state is enabled (that is, whether its onSaveInstanceState method will be called). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSaveFromParentEnabled Controls whether the entire hierarchy under this view will save its state when a state saving traversal occurs from its parent. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScaleX Sets the amount that the view is scaled in x around the pivot point, as a proportion of the view's unscaled width. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScaleY Sets the amount that the view is scaled in Y around the pivot point, as a proportion of the view's unscaled width. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScreenReaderFocusable Sets whether this View should be a focusable element for screen readers and include non-focusable Views from its subtree when providing feedback. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollBarDefaultDelayBeforeFade Define the delay before scrollbars fade. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollBarFadeDuration Define the scrollbar fade duration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollBarSize Define the scrollbar size. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollBarStyle Specify the style of the scrollbars. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollCaptureCallback Sets the callback to receive scroll capture requests. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollCaptureHint Sets the scroll capture hint for this View. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollContainer Change whether this view is one of the set of scrollable containers in its window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollIndicators Sets the state of all scroll indicators. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollIndicators Sets the state of the scroll indicators specified by the mask. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollX Set the horizontal scrolled position of your view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollY Set the vertical scrolled position of your view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollbarFadingEnabled Define whether scrollbars will fade when the view is not scrolling. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSelected Changes the selection state of this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSoundEffectsEnabled Set whether this view should have sound effects enabled for events such as clicking and touching. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setStateDescription Sets the View's state description. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setStateListAnimator Attaches the provided StateListAnimator to this View. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSupplementalDescription Sets the View's supplemental description. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSystemGestureExclusionRects Sets a list of areas within this view's post-layout coordinate space where the system should not intercept touch or other pointing device gestures. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSystemUiVisibility Request that the visibility of the status bar or other screen/window decorations be changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTag Sets a tag associated with this view and a key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTag Sets the tag associated with this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTextAlignment Set the text alignment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTextDirection Set the text direction. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTooltipText Sets the tooltip text which will be displayed in a small popup next to the view. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTop Sets the top position of this view relative to its parent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTouchDelegate Sets the TouchDelegate for this View. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTransitionAlpha This property is intended only for use by the Fade transition, which animates it to produce a visual translucency that does not side-effect (or get affected by) the real alpha property. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTransitionName Sets the name of the View to be used to identify Views in Transitions. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTransitionVisibility Changes the visibility of this View without triggering any other changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTranslationX Sets the horizontal location of this view relative to its getLeft position. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTranslationY Sets the vertical location of this view relative to its getTop position. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTranslationZ Sets the depth location of this view relative to its getElevation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setVerticalFadingEdgeEnabled Define whether the vertical edges should be faded when this view is scrolled vertically. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setVerticalScrollBarEnabled Define whether the vertical scrollbar should be drawn or not. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setVerticalScrollbarPosition Set the position of the vertical scroll bar. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setVerticalScrollbarThumbDrawable Defines the vertical scrollbar thumb drawable |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setVerticalScrollbarTrackDrawable Defines the vertical scrollbar track drawable |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewTranslationCallback Sets a ViewTranslationCallback that is used to display/hide the translated information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setVisibility Set the visibility state of this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setWillNotCacheDrawing When a View's drawing cache is enabled, drawing is redirected to an offscreen bitmap. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setWillNotDraw If this view doesn't do any drawing on its own, set this flag to allow further optimizations. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setWindowInsetsAnimationCallback Sets a `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback` to be notified about animations of windows that cause insets. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setX Sets the visual x position of this view, in pixels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setY Sets the visual y position of this view, in pixels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setZ Sets the visual z position of this view, in pixels. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | showContextMenu Shows the context menu for this view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | showContextMenu Shows the context menu for this view anchored to the specified view-relative coordinate. |
| open [ActionMode](ActionMode.md)! | startActionMode Start an action mode with the default type `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int`. |
| --- | --- |
| open [ActionMode](ActionMode.md)! | startActionMode Start an action mode with the given type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | startAnimation Start the specified animation now. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | startDrag <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | startDragAndDrop Starts a drag and drop operation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | startNestedScroll Begin a nestable scroll operation along the given axes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | stopNestedScroll Stop a nested scroll in progress. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | transformMatrixToGlobal Modifies the input matrix such that it maps view-local coordinates to on-screen coordinates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | transformMatrixToLocal Modifies the input matrix such that it maps on-screen coordinates to view-local coordinates. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterCalledFromWrongThreadListener Unregisters a listener that was previously registered with registerCalledFromWrongThreadListener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unscheduleDrawable Unschedule any events associated with the given Drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unscheduleDrawable Cancels a scheduled action on a drawable. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | updateDragShadow Updates the drag shadow for the ongoing drag and drop operation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | willNotCacheDrawing Returns whether or not this View can cache its drawing or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | willNotDraw Returns whether or not this View draws on its own. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | awakenScrollBars Trigger the scrollbars to draw. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | awakenScrollBars Trigger the scrollbars to draw. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | awakenScrollBars Trigger the scrollbars to draw. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | computeHorizontalScrollExtent Compute the horizontal extent of the horizontal scrollbar's thumb within the horizontal range. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | computeHorizontalScrollOffset Compute the horizontal offset of the horizontal scrollbar's thumb within the horizontal range. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | computeHorizontalScrollRange Compute the horizontal range that the horizontal scrollbar represents. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | computeVerticalScrollExtent Compute the vertical extent of the vertical scrollbar's thumb within the vertical range. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | computeVerticalScrollOffset Compute the vertical offset of the vertical scrollbar's thumb within the horizontal range. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | computeVerticalScrollRange Compute the vertical range that the vertical scrollbar represents. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchDraw Called by draw to draw the child views. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchGenericFocusedEvent Dispatch a generic motion event to the currently focused view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchGenericPointerEvent Dispatch a generic motion event to the view under the first pointer. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchHoverEvent Dispatch a hover event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchRestoreInstanceState Called by restoreHierarchyState to retrieve the state for this view and its children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchSaveInstanceState Called by saveHierarchyState to store the state for this view and its children. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchSetActivated Dispatch setActivated to all of this View's children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchSetPressed Dispatch setPressed to all of this View's children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchSetSelected Dispatch setSelected to all of this View's children. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchVisibilityChanged Dispatch a view visibility change down the view hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawableStateChanged This function is called whenever the state of the view changes in such a way that it impacts the state of drawables being shown. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | fitSystemWindows Called by the view hierarchy when the content insets for a window have changed, to allow it to adjust its content to fit within those windows. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getBottomFadingEdgeStrength Returns the strength, or intensity, of the bottom faded edge. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getBottomPaddingOffset Amount by which to extend the bottom fading region. |
| open [ContextMenu.ContextMenuInfo](../android/view/ContextMenu.ContextMenuInfo.md)! | getContextMenuInfo Views should implement this if they have extra information to associate with the context menu. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHorizontalScrollbarHeight Returns the height of the horizontal scrollbar. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getLeftFadingEdgeStrength Returns the strength, or intensity, of the left faded edge. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLeftPaddingOffset Amount by which to extend the left fading region. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getRightFadingEdgeStrength Returns the strength, or intensity, of the right faded edge. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRightPaddingOffset Amount by which to extend the right fading region. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSuggestedMinimumHeight Returns the suggested minimum height that the view should use. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSuggestedMinimumWidth Returns the suggested minimum width that the view should use. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getTopFadingEdgeStrength Returns the strength, or intensity, of the top faded edge. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getTopPaddingOffset Amount by which to extend the top fading region. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getWindowAttachCount <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPaddingOffsetRequired If the View draws content inside its padding and enables fading edges, it needs to support padding offsets. |
| open static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | mergeDrawableStates Merge your own state values in additionalState into the base state values baseState that were returned by onCreateDrawableState. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAnimationEnd Invoked by a parent ViewGroup to notify the end of the animation currently associated with this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAnimationStart Invoked by a parent ViewGroup to notify the start of the animation currently associated with this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAttachedToWindow This is called when the view is attached to a window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onConfigurationChanged Called when the current configuration of the resources being used by the application have changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onCreateContextMenu Views should implement this if the view itself is going to add items to the context menu. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | onCreateDrawableState Generate the new `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` state for this view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDetachedFromWindow This is called when the view is detached from a window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDisplayHint Gives this view a hint about whether is displayed or not. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDraw Implement this to do your drawing. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDrawScrollBars Request the drawing of the horizontal and the vertical scrollbar. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onFinishInflate Finalize inflating a view from XML. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onFocusChanged Called by the view system when the focus state of this view changes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onLayout Called from layout when this view should assign a size and position to each of its children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onMeasure Measure the view and its content to determine the measured width and the measured height. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onOverScrolled Called by overScrollBy to respond to the results of an over-scroll operation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRestoreInstanceState Hook allowing a view to re-apply a representation of its internal state that had previously been generated by onSaveInstanceState. |
| open [Parcelable](../android.os/Parcelable.md)? | onSaveInstanceState Hook allowing a view to generate a representation of its internal state that can later be used to create a new instance with that same state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onScrollChanged This is called in response to an internal scroll in this view (i.e., the view scrolled its own contents). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onSetAlpha Invoked if there is a Transform that involves alpha. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onSizeChanged This is called during layout when the size of this view has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onVisibilityChanged Called when the visibility of the view or an ancestor of the view has changed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onWindowVisibilityChanged Called when the window containing has change its visibility (between `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | overScrollBy Scroll the view with standard behavior for scrolling beyond the normal content boundaries. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMeasuredDimension This method must be called by onMeasure to store the measured width and measured height. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | verifyDrawable If your view subclass is displaying its own Drawable objects, it should override this function and return true for any Drawable it is displaying. |

| Properties ||
|---|---|
| static [Property](../android.util/Property.md)\< [View](View.md)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/View#ALPHA:android.util.Property` A Property wrapper around the `alpha` functionality handled by the setAlpha and getAlpha methods. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#EMPTY_STATE_SET:kotlin.IntArray` Indicates the view has no states set. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_FOCUSED_SELECTED_STATE_SET:kotlin.IntArray` Indicates the view is enabled, focused and selected. |
| --- | --- |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is enabled, focused, selected and its window has the focus. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is enabled and has the focus. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_FOCUSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is enabled, focused and its window has the focus. |
| --- | --- |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_SELECTED_STATE_SET:kotlin.IntArray` Indicates the view is enabled and selected. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is enabled, selected and its window has the focus. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray` Indicates the view is enabled. |
| --- | --- |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is enabled and that its window has focus. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_SELECTED_STATE_SET:kotlin.IntArray` Indicates the view is focused and selected. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is focused, selected and its window has the focus. |
| --- | --- |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is focused. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view has the focus and that its window has the focus. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_FOCUSED_SELECTED_STATE_SET:kotlin.IntArray` Indicates the view is pressed, enabled, focused and selected. |
| --- | --- |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is pressed, enabled, focused, selected and its window has the focus. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is pressed, enabled and focused. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_FOCUSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is pressed, enabled, focused and its window has the focus. |
| --- | --- |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_SELECTED_STATE_SET:kotlin.IntArray` Indicates the view is pressed, enabled and selected. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is pressed, enabled, selected and its window has the focus. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_STATE_SET:kotlin.IntArray` Indicates the view is pressed and enabled. |
| --- | --- |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is pressed, enabled and its window has the focus. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_FOCUSED_SELECTED_STATE_SET:kotlin.IntArray` Indicates the view is pressed, focused and selected. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is pressed, focused, selected and its window has the focus. |
| --- | --- |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is pressed and focused. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_FOCUSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is pressed, focused and its window has the focus. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_SELECTED_STATE_SET:kotlin.IntArray` Indicates the view is pressed and selected. |
| --- | --- |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is pressed, selected and its window has the focus. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray` Indicates the view is pressed. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is pressed and its window has the focus. |
| --- | --- |
| static [Property](../android.util/Property.md)\< [View](View.md)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/View#ROTATION:android.util.Property` A Property wrapper around the `rotation` functionality handled by the setRotation and getRotation methods. |
| static [Property](../android.util/Property.md)\< [View](View.md)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/View#ROTATION_X:android.util.Property` A Property wrapper around the `rotationX` functionality handled by the setRotationX and getRotationX methods. |
| static [Property](../android.util/Property.md)\< [View](View.md)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/View#ROTATION_Y:android.util.Property` A Property wrapper around the `rotationY` functionality handled by the setRotationY and getRotationY methods. |
| --- | --- |
| static [Property](../android.util/Property.md)\< [View](View.md)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/View#SCALE_X:android.util.Property` A Property wrapper around the `scaleX` functionality handled by the setScaleX and getScaleX methods. |
| static [Property](../android.util/Property.md)\< [View](View.md)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/View#SCALE_Y:android.util.Property` A Property wrapper around the `scaleY` functionality handled by the setScaleY and getScaleY methods. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray` Indicates the view is selected. |
| --- | --- |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view is selected and that its window has the focus. |
| static [Property](../android.util/Property.md)\< [View](View.md)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/View#TRANSLATION_X:android.util.Property` A Property wrapper around the `translationX` functionality handled by the setTranslationX and getTranslationX methods. |
| static [Property](../android.util/Property.md)\< [View](View.md)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/View#TRANSLATION_Y:android.util.Property` A Property wrapper around the `translationY` functionality handled by the setTranslationY and getTranslationY methods. |
| --- | --- |
| static [Property](../android.util/Property.md)\< [View](View.md)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/View#TRANSLATION_Z:android.util.Property` A Property wrapper around the `translationZ` functionality handled by the setTranslationZ and getTranslationZ methods. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray` Indicates the view's window has focus. |
| static [Property](../android.util/Property.md)\< [View](View.md)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/View#X:android.util.Property` A Property wrapper around the `x` functionality handled by the setX and getX methods. |
| --- | --- |
| static [Property](../android.util/Property.md)\< [View](View.md)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/View#Y:android.util.Property` A Property wrapper around the `y` functionality handled by the setY and getY methods. |
| static [Property](../android.util/Property.md)\< [View](View.md)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/View#Z:android.util.Property` A Property wrapper around the `z` functionality handled by the setZ and getZ methods. |

## XML attributes

### android:accessibilityHeading

```
android:accessibilityHeading
```
Whether or not this view is a heading for accessibility purposes.

May be a boolean value, such as "`true`" or "`false`".

### android:allowClickWhenDisabled

```
android:allowClickWhenDisabled
```
Whether or not allow clicks on disabled view.

May be a boolean value, such as "`true`" or "`false`".

### android:alpha

```
android:alpha
```
alpha property of the view, as a value between 0 (completely transparent) and 1 (completely opaque).

May be a floating point value, such as "`1.2`".

### android:background

```
android:background
```
A drawable to use as the background. This can be either a reference to a full drawable resource (such as a PNG image, 9-patch, XML state list description, etc), or a solid color such as "#ff000000" (black).

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

May be a color value, in the form of "`rgb`", "`argb`", "`rrggbb`", or "`aarrggbb`".

### android:clickable

```
android:clickable
```
Defines whether this view reacts to click events.

May be a boolean value, such as "`true`" or "`false`".

### android:clipToOutline

```
android:clipToOutline
```

Whether the View's Outline should be used to clip the contents of the View.

Only a single non-rectangular clip can be applied on a View at any time. Circular clips from a android.view.ViewAnimationUtils#createCircularReveal(View,int,int,float,float) circular reveal animation take priority over Outline clipping, and child Outline clipping takes priority over Outline clipping done by a parent.

Note that this flag will only be respected if the View's Outline returns true from canClip.

May be a boolean value, such as "`true`" or "`false`".

### android:contentDescription

```
android:contentDescription
```
Defines text that briefly describes content of the view. This property is used primarily for accessibility. Since some views do not have textual representation this attribute can be used for providing such.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

### android:drawingCacheQuality

```
android:drawingCacheQuality
```
Defines the quality of translucent drawing caches. This property is used only when the drawing cache is enabled and translucent. The default value is auto. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11.

Must be one of the following constant values.

| Constant | Value | Description |
|---|---|---|
| auto | 0 | Lets the framework decide what quality level should be used for the drawing cache. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. |
| high | 2 | High quality. When set to high quality, the drawing cache uses a higher color depth but uses more memory. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. |
| low | 1 | Low quality. When set to low quality, the drawing cache uses a lower color depth, thus losing precision in rendering gradients, but uses less memory. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. |
| --- | --- | --- |

### android:duplicateParentState

```
android:duplicateParentState
```
When this attribute is set to true, the view gets its drawable state (focused, pressed, etc.) from its direct parent rather than from itself.

May be a boolean value, such as "`true`" or "`false`".

### android:fadeScrollbars

```
android:fadeScrollbars
```
Defines whether to fade out scrollbars when they are not in use.

May be a boolean value, such as "`true`" or "`false`".

### android:fadingEdgeLength

```
android:fadingEdgeLength
```
Defines the length of the fading edges.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:filterTouchesWhenObscured

```
android:filterTouchesWhenObscured
```
Specifies whether to filter touches when the view's window is obscured by another visible window. When set to true, the view will not receive touches whenever a toast, dialog or other window appears above the view's window. Refer to the View security documentation for more details.

May be a boolean value, such as "`true`" or "`false`".

### android:fitsSystemWindows

```
android:fitsSystemWindows
```
Boolean internal attribute to adjust view layout based on system windows such as the status bar. If true, adjusts the padding of this view to leave space for the system windows. Will only take effect if this view is in a non-embedded activity.

May be a boolean value, such as "`true`" or "`false`".

### android:focusable

```
android:focusable
```
Controls whether a view can take focus. By default, this is "auto" which lets the framework determine whether a user can move focus to a view. By setting this attribute to true the view is allowed to take focus. By setting it to "false" the view will not take focus. This value does not impact the behavior of directly calling android.view.View#requestFocus, which will always request focus regardless of this view. It only impacts where focus navigation will try to move focus.

May be a boolean value, such as "`true`" or "`false`".

Must be one of the following constant values.

| Constant | Value | Description |
|---|---|---|
| auto | 10 | |

### android:focusableInTouchMode

```
android:focusableInTouchMode
```
Boolean that controls whether a view can take focus while in touch mode. If this is true for a view, that view can gain focus when clicked on, and can keep focus if another view is clicked on that doesn't have this attribute set to true.

May be a boolean value, such as "`true`" or "`false`".

### android:focusedByDefault

```
android:focusedByDefault
```
Whether this view is a default-focus view. Only one view per keyboard navigation cluster can have this attribute set to true. See setFocusedByDefault.

May be a boolean value, such as "`true`" or "`false`".

### android:hapticFeedbackEnabled

```
android:hapticFeedbackEnabled
```
Boolean that controls whether a view should have haptic feedback enabled for events such as long presses.

May be a boolean value, such as "`true`" or "`false`".

### android:id

```
android:id
```
Supply an identifier name for this view, to later retrieve it with findViewById or findViewById. This must be a resource reference; typically you set this using the `@+` syntax to create a new ID resources. For example: `android:id="@+id/my_id"` which allows you to later retrieve the view with `findViewById(R.id.my_id)`.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:isScrollContainer

```
android:isScrollContainer
```
Set this if the view will serve as a scrolling container, meaning that it can be resized to shrink its overall window so that there will be space for an input method. If not set, the default value will be true if "scrollbars" has the vertical scrollbar set, else it will be false.

May be a boolean value, such as "`true`" or "`false`".

### android:keepScreenOn

```
android:keepScreenOn
```
Controls whether the view's window should keep the screen on while visible.

May be a boolean value, such as "`true`" or "`false`".

### android:keyboardNavigationCluster

```
android:keyboardNavigationCluster
```
Whether this view is a root of a keyboard navigation cluster. See setKeyboardNavigationCluster.

May be a boolean value, such as "`true`" or "`false`".

### android:layerType

```
android:layerType
```
Specifies the type of layer backing this view. The default value is none. Refer to setLayerType for more information.

Must be one of the following constant values.

| Constant | Value | Description |
|---|---|---|
| hardware | 2 | Use a hardware layer. Refer to setLayerType for more information. |
| none | 0 | Don't use a layer. |
| software | 1 | Use a software layer. Refer to setLayerType for more information. |
| --- | --- | --- |

### android:layoutDirection

```
android:layoutDirection
```
Defines the direction of layout drawing. This typically is associated with writing direction of the language script used. The possible values are "ltr" for Left-to-Right, "rtl" for Right-to-Left, "locale", and "inherit" from parent view. If there is nothing to inherit, "locale" is used. "locale" falls back to "en-US". "ltr" is the direction used in "en-US". The default for this attribute is "inherit".

Must be one of the following constant values.

| Constant | Value | Description |
|---|---|---|
| inherit | 2 | Inherit from parent. |
| locale | 3 | Locale. |
| ltr | 0 | Left-to-Right. |
| --- | --- | --- |
| rtl | 1 | Right-to-Left. |

### android:longClickable

```
android:longClickable
```
Defines whether this view reacts to long click events.

May be a boolean value, such as "`true`" or "`false`".

### android:minHeight

```
android:minHeight
```
Defines the minimum height of the view. It is not guaranteed the view will be able to achieve this minimum height (for example, if its parent layout constrains it with less available height).

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:minWidth

```
android:minWidth
```
Defines the minimum width of the view. It is not guaranteed the view will be able to achieve this minimum width (for example, if its parent layout constrains it with less available width).

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:nextClusterForward

```
android:nextClusterForward
```
Defines the next keyboard navigation cluster. If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:nextFocusDown

```
android:nextFocusDown
```
Defines the next view to give focus to when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:nextFocusLeft

```
android:nextFocusLeft
```
Defines the next view to give focus to when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int`. If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:nextFocusRight

```
android:nextFocusRight
```
Defines the next view to give focus to when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int` If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:nextFocusUp

```
android:nextFocusUp
```
Defines the next view to give focus to when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int` If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:onClick

```
android:onClick
```
Name of the method in this View's context to invoke when the view is clicked. This name must correspond to a public method that takes exactly one parameter of type View. For instance, if you specify `android:onClick="sayHello"`, you must declare a `public void sayHello(View v)` method of your context (typically, your Activity).

### android:outlineAmbientShadowColor

```
android:outlineAmbientShadowColor
```
Sets the color of the ambient shadow that is drawn when the view has a positive Z or elevation value.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different views with different colors.

The opacity of the final ambient shadow is a function of the shadow caster height, the alpha channel of the outlineAmbientShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#ambientShadowAlpha:kotlin.Int` theme attribute.

May be a color value, in the form of "`rgb`", "`argb`", "`rrggbb`", or "`aarrggbb`".

### android:outlineSpotShadowColor

```
android:outlineSpotShadowColor
```
Sets the color of the spot shadow that is drawn when the view has a positive Z or elevation value.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different views with different colors.

The opacity of the final spot shadow is a function of the shadow caster height, the alpha channel of the outlineSpotShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#spotShadowAlpha:kotlin.Int` theme attribute.

May be a color value, in the form of "`rgb`", "`argb`", "`rrggbb`", or "`aarrggbb`".

### android:padding

```
android:padding
```
Sets the padding, in pixels, of all four edges. Padding is defined as space between the edges of the view and the view's content. This value will take precedence over any of the edge-specific values (paddingLeft, paddingTop, paddingRight, paddingBottom, paddingHorizontal and paddingVertical), but will not override paddingStart or paddingEnd, if set. A view's size will include its padding. If a `https://developer.android.com/reference/kotlin/android/R.attr.html#background:kotlin.Int` is provided, the padding will initially be set to that (0 if the drawable does not have padding). Explicitly setting a padding value will override the corresponding padding found in the background.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:paddingBottom

```
android:paddingBottom
```
Sets the padding, in pixels, of the bottom edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:paddingEnd

```
android:paddingEnd
```
Sets the padding, in pixels, of the end edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:paddingHorizontal

```
android:paddingHorizontal
```
Sets the padding, in pixels, of the left and right edges; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`. This value will take precedence over paddingLeft and paddingRight, but not paddingStart or paddingEnd (if set).

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:paddingLeft

```
android:paddingLeft
```
Sets the padding, in pixels, of the left edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:paddingRight

```
android:paddingRight
```
Sets the padding, in pixels, of the right edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:paddingStart

```
android:paddingStart
```
Sets the padding, in pixels, of the start edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:paddingTop

```
android:paddingTop
```
Sets the padding, in pixels, of the top edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:paddingVertical

```
android:paddingVertical
```
Sets the padding, in pixels, of the top and bottom edges; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`. This value will take precedence over paddingTop and paddingBottom, if set.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:requiresFadingEdge

```
android:requiresFadingEdge
```
Defines which edges should be faded on scrolling.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |

| Constant | Value | Description |
|---|---|---|
| horizontal | 1000 | Fades horizontal edges only. |
| none | 0 | No edge is faded. |
| vertical | 2000 | Fades vertical edges only. |
| --- | --- | --- |

### android:rotation

```
android:rotation
```
rotation of the view, in degrees.

May be a floating point value, such as "`1.2`".

### android:rotationX

```
android:rotationX
```
rotation of the view around the x axis, in degrees.

May be a floating point value, such as "`1.2`".

### android:rotationY

```
android:rotationY
```
rotation of the view around the y axis, in degrees.

May be a floating point value, such as "`1.2`".

### android:saveEnabled

```
android:saveEnabled
```
If false, no state will be saved for this view when it is being frozen. The default is true, allowing the view to be saved (however it also must have an ID assigned to it for its state to be saved). Setting this to false only disables the state for this view, not for its children which may still be saved.

May be a boolean value, such as "`true`" or "`false`".

### android:scaleX

```
android:scaleX
```
scale of the view in the x direction.

May be a floating point value, such as "`1.2`".

### android:scaleY

```
android:scaleY
```
scale of the view in the y direction.

May be a floating point value, such as "`1.2`".

### android:scrollX

```
android:scrollX
```
The initial horizontal scroll offset, in pixels.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:scrollY

```
android:scrollY
```
The initial vertical scroll offset, in pixels.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:scrollbarAlwaysDrawHorizontalTrack

```
android:scrollbarAlwaysDrawHorizontalTrack
```
Defines whether the horizontal scrollbar track should always be drawn.

May be a boolean value, such as "`true`" or "`false`".

### android:scrollbarAlwaysDrawVerticalTrack

```
android:scrollbarAlwaysDrawVerticalTrack
```
Defines whether the vertical scrollbar track should always be drawn.

May be a boolean value, such as "`true`" or "`false`".

### android:scrollbarDefaultDelayBeforeFade

```
android:scrollbarDefaultDelayBeforeFade
```
Defines the delay in milliseconds that a scrollbar waits before fade out.

May be an integer value, such as "`100`".

### android:scrollbarFadeDuration

```
android:scrollbarFadeDuration
```
Defines the delay in milliseconds that a scrollbar takes to fade out.

May be an integer value, such as "`100`".

### android:scrollbarSize

```
android:scrollbarSize
```
Sets the width of vertical scrollbars and height of horizontal scrollbars.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:scrollbarStyle

```
android:scrollbarStyle
```
Controls the scrollbar style and position. The scrollbars can be overlaid or inset. When inset, they add to the padding of the view. And the scrollbars can be drawn inside the padding area or on the edge of the view. For example, if a view has a background drawable and you want to draw the scrollbars inside the padding specified by the drawable, you can use insideOverlay or insideInset. If you want them to appear at the edge of the view, ignoring the padding, then you can use outsideOverlay or outsideInset.

Must be one of the following constant values.

| Constant | Value | Description |
|---|---|---|
| insideInset | 1000000 | Inside the padding and inset. |
| insideOverlay | 0 | Inside the padding and overlaid. |
| outsideInset | 3000000 | Edge of the view and inset. |
| --- | --- | --- |
| outsideOverlay | 2000000 | Edge of the view and overlaid. |

### android:scrollbarThumbHorizontal

```
android:scrollbarThumbHorizontal
```
Defines the horizontal scrollbar thumb drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:scrollbarThumbVertical

```
android:scrollbarThumbVertical
```
Defines the vertical scrollbar thumb drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:scrollbarTrackHorizontal

```
android:scrollbarTrackHorizontal
```
Defines the horizontal scrollbar track drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:scrollbarTrackVertical

```
android:scrollbarTrackVertical
```
Defines the vertical scrollbar track drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:scrollbars

```
android:scrollbars
```
Defines which scrollbars should be displayed on scrolling or not.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |

| Constant | Value | Description |
|---|---|---|
| horizontal | 100 | Displays horizontal scrollbar only. |
| none | 0 | No scrollbar is displayed. |
| vertical | 200 | Displays vertical scrollbar only. |
| --- | --- | --- |

### android:soundEffectsEnabled

```
android:soundEffectsEnabled
```
Boolean that controls whether a view should have sound effects enabled for events such as clicking and touching.

May be a boolean value, such as "`true`" or "`false`".

### android:stateListAnimator

```
android:stateListAnimator
```
Sets the state-based animator for the View.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:tag

```
android:tag
```
Supply a tag for this view containing a String, to be retrieved later with android.view.View#getTag or searched for with findViewWithTag. It is generally preferable to use IDs (through the android:id attribute) instead of tags because they are faster and allow for compile-time type checking.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

### android:textAlignment

```
android:textAlignment
```
Defines the alignment of the text.

May be an integer value, such as "`100`".

Must be one of the following constant values.

| Constant | Value | Description |
|---|---|---|
| center | 4 | Center the paragraph, for example: ALIGN_CENTER. |
| gravity | 1 | Default for the root view. The gravity determines the alignment, ALIGN_NORMAL, ALIGN_CENTER, or ALIGN_OPPOSITE, which are relative to each paragraph's text direction. |
| inherit | 0 | Default. |
| --- | --- | --- |
| textEnd | 3 | Align to the end of the paragraph, for example: ALIGN_OPPOSITE. |
| textStart | 2 | Align to the start of the paragraph, for example: ALIGN_NORMAL. |
| viewEnd | 6 | Align to the end of the view, which is ALIGN_RIGHT if the view's resolved layoutDirection is LTR, and ALIGN_LEFT otherwise. |
| --- | --- | --- |
| viewStart | 5 | Align to the start of the view, which is ALIGN_LEFT if the view's resolved layoutDirection is LTR, and ALIGN_RIGHT otherwise. |

### android:textDirection

```
android:textDirection
```
Defines the direction of the text.

May be an integer value, such as "`100`".

Must be one of the following constant values.

| Constant | Value | Description |
|---|---|---|
| anyRtl | 2 | The paragraph direction is RTL if it contains any strong RTL character, otherwise it is LTR if it contains any strong LTR characters. If there are neither, the paragraph direction is the view's resolved layout direction. |
| firstStrong | 1 | Default for the root view. The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is the view's resolved layout direction. |
| firstStrongLtr | 6 | The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is LTR. |
| --- | --- | --- |
| firstStrongRtl | 7 | The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is RTL. |
| inherit | 0 | Default. |
| locale | 5 | The paragraph direction is coming from the system Locale. |
| --- | --- | --- |
| ltr | 3 | The paragraph direction is left to right. |
| rtl | 4 | The paragraph direction is right to left. |

### android:theme

```
android:theme
```
Specifies a theme override for a view. When a theme override is set, the view will be inflated using a `https://developer.android.com/reference/kotlin/android/content/Context.html#` themed with the specified resource. During XML inflation, any child views under the view with a theme override will inherit the themed context.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:transformPivotX

```
android:transformPivotX
```
x location of the pivot point around which the view will rotate and scale. This xml attribute sets the pivotX property of the View.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:transformPivotY

```
android:transformPivotY
```
y location of the pivot point around which the view will rotate and scale. This xml attribute sets the pivotY property of the View.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:transitionName

```
android:transitionName
```
Names a View such that it can be identified for Transitions. Names should be unique in the View hierarchy.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

### android:translationX

```
android:translationX
```
translation in x of the view. This value is added post-layout to the left property of the view, which is set by its layout.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:translationY

```
android:translationY
```
translation in y of the view. This value is added post-layout to the top property of the view, which is set by its layout.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:translationZ

```
android:translationZ
```
translation in z of the view. This value is added to its elevation.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:visibility

```
android:visibility
```
Controls the initial visibility of the view.

Must be one of the following constant values.

| Constant | Value | Description |
|---|---|---|
| gone | 2 | Completely hidden, as if the view had not been added. |
| invisible | 1 | Not displayed, but taken into account during layout (space is left for it). |
| visible | 0 | Visible on screen; the default value. |
| --- | --- | --- |

## Constants

### ACCESSIBILITY_DATA_SENSITIVE_AUTO

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESSIBILITY_DATA_SENSITIVE_AUTO: Int
```

Automatically determine whether the view should only allow interactions from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s with the isAccessibilityTool property set to true.

Accessibility interactions from services without `isAccessibilityTool` set to true are disallowed for any of the following conditions:
- this view sets getFilterTouchesWhenObscured.
- any parent of this view returns true from isAccessibilityDataSensitive.

 Value: 0

### ACCESSIBILITY_DATA_SENSITIVE_NO

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESSIBILITY_DATA_SENSITIVE_NO: Int
```

Allow interactions from all `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s, regardless of their isAccessibilityTool property.

 Value: 2

### ACCESSIBILITY_DATA_SENSITIVE_YES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESSIBILITY_DATA_SENSITIVE_YES: Int
```

Only allow interactions from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s with the isAccessibilityTool property set to true.

 Value: 1

### ACCESSIBILITY_LIVE_REGION_ASSERTIVE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESSIBILITY_LIVE_REGION_ASSERTIVE: Int
```

Live region mode specifying that accessibility services should immediately notify users of changes to this view. For example, a screen reader may interrupt ongoing speech to immediately announce these changes.

Use with setAccessibilityLiveRegion.

 Value: 2

### ACCESSIBILITY_LIVE_REGION_NONE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESSIBILITY_LIVE_REGION_NONE: Int
```

Live region mode specifying that accessibility services should not automatically announce changes to this view. This is the default live region mode for most views.

Use with setAccessibilityLiveRegion.

 Value: 0

### ACCESSIBILITY_LIVE_REGION_POLITE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESSIBILITY_LIVE_REGION_POLITE: Int
```

Live region mode specifying that accessibility services should notify users of changes to this view.

Use with setAccessibilityLiveRegion.

 Value: 1

### AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS: Int
```

Flag requesting you to add views that are marked as not important for autofill (see setImportantForAutofill) to a ViewStructure.

 Value: 1

### AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE: String
```

Hint indicating that this view can be autofilled with a credit card expiration date.

It should be used when the credit card expiration date is represented by just one view; if it is represented by more than one (for example, one view for the month and another view for the year), then each of these views should use the hint specific for the unit (`https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH:kotlin.String`, or `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR:kotlin.String`).

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE}`).

When annotating a view with this hint, it's recommended to use a date autofill value to avoid ambiguity when the autofill service provides a value for it. To understand why a value can be ambiguous, consider "April of 2020", which could be represented as either of the following options:

- `"04/2020"`
- `"4/2020"`
- `"2020/04"`
- `"2020/4"`
- `"April/2020"`
- `"Apr/2020"`

You define a date autofill value for the view by overriding the following methods:

1. getAutofillType to return `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_DATE:kotlin.Int`.
2. getAutofillValue to return a forDate.
3. autofill to expect a data autofillvalue.

See setAutofillHints for more info about autofill hints.

 Value: "creditCardExpirationDate"

### AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY: String
```

Hint indicating that this view can be autofilled with a credit card expiration day.

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY}`).

See setAutofillHints for more info about autofill hints.

 Value: "creditCardExpirationDay"

### AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH: String
```

Hint indicating that this view can be autofilled with a credit card expiration month.

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH}`).

When annotating a view with this hint, it's recommended to use a text autofill value whose value is the numerical representation of the month, starting on `1` to avoid ambiguity when the autofill service provides a value for it. To understand why a value can be ambiguous, consider "January", which could be represented as either of

- `"1"`: recommended way.
- `"0"`: if following the `https://developer.android.com/reference/kotlin/java/util/Calendar.html#MONTH:kotlin.Int` convention.
- `"January"`: full name, in English.
- `"jan"`: abbreviated name, in English.
- `"Janeiro"`: full name, in another language.

Another recommended approach is to use a date autofill value - see `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE:kotlin.String` for more details.

See setAutofillHints for more info about autofill hints.

 Value: "creditCardExpirationMonth"

### AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR: String
```

Hint indicating that this view can be autofilled with a credit card expiration year.

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR}`).

See setAutofillHints for more info about autofill hints.

 Value: "creditCardExpirationYear"

### AUTOFILL_HINT_CREDIT_CARD_NUMBER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_CREDIT_CARD_NUMBER: String
```

Hint indicating that this view can be autofilled with a credit card number.

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_NUMBER}`).

See setAutofillHints for more info about autofill hints.

 Value: "creditCardNumber"

### AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE: String
```

Hint indicating that this view can be autofilled with a credit card security code.

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE}`).

See setAutofillHints for more info about autofill hints.

 Value: "creditCardSecurityCode"

### AUTOFILL_HINT_EMAIL_ADDRESS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_EMAIL_ADDRESS: String
```

Hint indicating that this view can be autofilled with an email address.

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_EMAIL_ADDRESS}`).

See setAutofillHints for more info about autofill hints.

 Value: "emailAddress"

### AUTOFILL_HINT_NAME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_NAME: String
```

Hint indicating that this view can be autofilled with a user's real name.

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_NAME}`).

See setAutofillHints for more info about autofill hints.

 Value: "name"

### AUTOFILL_HINT_PASSWORD

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_PASSWORD: String
```

Hint indicating that this view can be autofilled with a password.

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_PASSWORD}`).

See setAutofillHints for more info about autofill hints.

 Value: "password"

### AUTOFILL_HINT_PHONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_PHONE: String
```

Hint indicating that this view can be autofilled with a phone number.

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_PHONE}`).

See setAutofillHints for more info about autofill hints.

 Value: "phone"

### AUTOFILL_HINT_POSTAL_ADDRESS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_POSTAL_ADDRESS: String
```

Hint indicating that this view can be autofilled with a postal address.

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_POSTAL_ADDRESS}`).

See setAutofillHints for more info about autofill hints.

 Value: "postalAddress"

### AUTOFILL_HINT_POSTAL_CODE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_POSTAL_CODE: String
```

Hint indicating that this view can be autofilled with a postal code.

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_POSTAL_CODE}`).

See setAutofillHints for more info about autofill hints.

 Value: "postalCode"

### AUTOFILL_HINT_USERNAME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_HINT_USERNAME: String
```

Hint indicating that this view can be autofilled with a username.

Can be used with either setAutofillHints or [`android:autofillHint`](View.md) (in which case the value should be `{@value #AUTOFILL_HINT_USERNAME}`).

See setAutofillHints for more info about autofill hints.

 Value: "username"

### AUTOFILL_TYPE_DATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_TYPE_DATE: Int
```

Autofill type for a field that contains a date, which is represented by a long representing the number of milliseconds since the standard base time known as "the epoch", namely January 1, 1970, 00:00:00 GMT (see getTime.

AutofillValue instances for autofilling a View can be obtained through forDate, and the values passed to autofill a View can be fetched through getDateValue.

 Value: 4

**See Also**

- getAutofillType

### AUTOFILL_TYPE_LIST

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_TYPE_LIST: Int
```

Autofill type for a selection list field, which is filled by an `int` representing the element index inside the list (starting at `0`).

AutofillValue instances for autofilling a View can be obtained through forList, and the value passed to autofill a View can be fetched through getListValue.

The available options in the selection list are typically provided by getAutofillOptions.

 Value: 3

**See Also**

- getAutofillType

### AUTOFILL_TYPE_NONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_TYPE_NONE: Int
```

Autofill type for views that cannot be autofilled.

Typically used when the view is read-only; for example, a text label.

 Value: 0

**See Also**

- getAutofillType

### AUTOFILL_TYPE_TEXT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_TYPE_TEXT: Int
```

Autofill type for a text field, which is filled by a `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#`.

AutofillValue instances for autofilling a View can be obtained through forText, and the value passed to autofill a View can be fetched through getTextValue.

 Value: 1

**See Also**

- getAutofillType

### AUTOFILL_TYPE_TOGGLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOFILL_TYPE_TOGGLE: Int
```

Autofill type for a togglable field, which is filled by a `boolean`.

AutofillValue instances for autofilling a View can be obtained through forToggle, and the value passed to autofill a View can be fetched through getToggleValue.

 Value: 2

**See Also**

- getAutofillType

### CONTENT_SENSITIVITY_AUTO

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTENT_SENSITIVITY_AUTO: Int
```

Content sensitivity is determined by the framework. The framework uses a heuristic to determine if this view displays sensitive content. Autofill hints i.e. getAutofillHints are used in the heuristic to determine if this view should be considered as a sensitive view.

`https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_USERNAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_PASSWORD:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_NUMBER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR:kotlin.String` are considered sensitive hints by the framework, and the list may include more hints in the future.

The window hosting a sensitive view will be marked as secure during an active media projection session. This would be equivalent to applying `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_SECURE:kotlin.Int` to the window.

 Value: 0

**See Also**

- getContentSensitivity

### CONTENT_SENSITIVITY_NOT_SENSITIVE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTENT_SENSITIVITY_NOT_SENSITIVE: Int
```

The view doesn't display sensitive content.

 Value: 2

**See Also**

- getContentSensitivity

### CONTENT_SENSITIVITY_SENSITIVE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTENT_SENSITIVITY_SENSITIVE: Int
```

The view displays sensitive content.

The window hosting a sensitive view will be marked as secure during an active media projection session. This would be equivalent to applying `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_SECURE:kotlin.Int` to the window.

 Value: 1

**See Also**

- getContentSensitivity

### DRAG_FLAG_ACCESSIBILITY_ACTION

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAG_FLAG_ACCESSIBILITY_ACTION: Int
```

Flag indicating that the drag was initiated with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_DRAG_START:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`. When startDragAndDrop is called, this is used by the system to perform a drag without animations.

 Value: 1024

### DRAG_FLAG_GLOBAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAG_FLAG_GLOBAL: Int
```

Flag indicating that a drag can cross window boundaries. When startDragAndDrop is called with this flag set, all visible applications with targetSdkVersion \>= `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` will be able to participate in the drag operation and receive the dragged content.

Global drags require a valid non-null `https://developer.android.com/reference/kotlin/android/content/ClipData.html#`.

If this is the only flag set, then the drag recipient will only have access to text data and intents contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object. Access to URIs contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` is determined by other DRAG_FLAG_GLOBAL_\* flags

 Value: 256

### DRAG_FLAG_GLOBAL_PERSISTABLE_URI_PERMISSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAG_FLAG_GLOBAL_PERSISTABLE_URI_PERMISSION: Int
```

When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_READ:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_WRITE:kotlin.Int`, the URI permission grant can be persisted across device reboots until explicitly revoked with revokeUriPermission Context.revokeUriPermission}.

 Value: 64

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PERSISTABLE_URI_PERMISSION:kotlin.Int`

### DRAG_FLAG_GLOBAL_PREFIX_URI_PERMISSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAG_FLAG_GLOBAL_PREFIX_URI_PERMISSION: Int
```

When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_READ:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_WRITE:kotlin.Int`, the URI permission grant applies to any URI that is a prefix match against the original granted URI.

 Value: 128

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PREFIX_URI_PERMISSION:kotlin.Int`

### DRAG_FLAG_GLOBAL_SAME_APPLICATION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAG_FLAG_GLOBAL_SAME_APPLICATION: Int
```

Flag indicating that a drag can cross window boundaries (within the same application). When startDragAndDrop is called with this flag set, only visible windows belonging to the same application (ie. share the same UID) with targetSdkVersion \>= `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` will be able to participate in the drag operation and receive the dragged content. If both DRAG_FLAG_GLOBAL_SAME_APPLICATION and DRAG_FLAG_GLOBAL are set, then DRAG_FLAG_GLOBAL_SAME_APPLICATION takes precedence and the drag will only go to visible windows from the same application.

 Value: 4096

### DRAG_FLAG_GLOBAL_URI_READ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAG_FLAG_GLOBAL_URI_READ: Int
```

When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL:kotlin.Int`, the drag recipient will be able to request read access to the content URI(s) contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int`

### DRAG_FLAG_GLOBAL_URI_WRITE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAG_FLAG_GLOBAL_URI_WRITE: Int
```

When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL:kotlin.Int`, the drag recipient will be able to request write access to the content URI(s) contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`

### DRAG_FLAG_HIDE_CALLING_TASK_ON_DRAG_START

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAG_FLAG_HIDE_CALLING_TASK_ON_DRAG_START: Int
```

Flag indicating that this drag will result in the caller activity's task to be hidden for the duration of the drag, which means that the source activity will not receive drag events for the current drag gesture. Only the current `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService.html#` may use this flag.

 Value: 16384

### DRAG_FLAG_OPAQUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAG_FLAG_OPAQUE: Int
```

Flag indicating that the drag shadow will be opaque. When startDragAndDrop is called with this flag set, the drag shadow will be opaque, otherwise, it will be semitransparent.

 Value: 512

### DRAG_FLAG_START_INTENT_SENDER_ON_UNHANDLED_DRAG

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAG_FLAG_START_INTENT_SENDER_ON_UNHANDLED_DRAG: Int
```

Flag indicating that an unhandled drag should be delegated to the system to be started if no visible window wishes to handle the drop. When using this flag, the caller must provide ClipData with an Item that contains an immutable IntentSender to an activity to be launched (not a broadcast, service, etc). See setIntentSender. The system can decide to launch the intent or not based on factors like the current screen size or windowing mode. If the system does not launch the intent, it will be canceled via the normal drag and drop flow.

 Value: 8192

### DRAWING_CACHE_QUALITY_AUTO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAWING_CACHE_QUALITY_AUTO: Int
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Enables automatic quality mode for the drawing cache.

 Value: 0

### DRAWING_CACHE_QUALITY_HIGH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAWING_CACHE_QUALITY_HIGH: Int
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Enables high quality mode for the drawing cache.

 Value: 1048576

### DRAWING_CACHE_QUALITY_LOW

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DRAWING_CACHE_QUALITY_LOW: Int
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Enables low quality mode for the drawing cache.

 Value: 524288

### FIND_VIEWS_WITH_CONTENT_DESCRIPTION

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FIND_VIEWS_WITH_CONTENT_DESCRIPTION: Int
```

Find find views that contain the specified content description.

 Value: 2

**See Also**

- findViewsWithText

### FIND_VIEWS_WITH_TEXT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FIND_VIEWS_WITH_TEXT: Int
```

Find views that render the specified text.

 Value: 1

**See Also**

- findViewsWithText

### FOCUSABLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUSABLE: Int
```

This view wants keystrokes.

Use with setFocusable and [`android:focusable`.](View.md)

 Value: 1

### FOCUSABLES_ALL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUSABLES_ALL: Int
```

View flag indicating whether addFocusables should add all focusable Views regardless if they are focusable in touch mode.

 Value: 0

### FOCUSABLES_TOUCH_MODE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUSABLES_TOUCH_MODE: Int
```

View flag indicating whether addFocusables should add only Views focusable in touch mode.

 Value: 1

### FOCUSABLE_AUTO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUSABLE_AUTO: Int
```

This view determines focusability automatically. This is the default.

Use with setFocusable and [`android:focusable`.](View.md)

 Value: 16

### FOCUS_BACKWARD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUS_BACKWARD: Int
```

Use with focusSearch. Move focus to the previous selectable item.

 Value: 1

### FOCUS_DOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUS_DOWN: Int
```

Use with focusSearch. Move focus down.

 Value: 130

### FOCUS_FORWARD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUS_FORWARD: Int
```

Use with focusSearch. Move focus to the next selectable item.

 Value: 2

### FOCUS_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUS_LEFT: Int
```

Use with focusSearch. Move focus to the left.

 Value: 17

### FOCUS_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUS_RIGHT: Int
```

Use with focusSearch. Move focus to the right.

 Value: 66

### FOCUS_UP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUS_UP: Int
```

Use with focusSearch. Move focus up.

 Value: 33

### GONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GONE: Int
```

This view is invisible, and it doesn't take any space for layout purposes. Use with setVisibility and [`android:visibility`.](View.md)

 Value: 8

### HAPTIC_FEEDBACK_ENABLED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HAPTIC_FEEDBACK_ENABLED: Int
```

View flag indicating whether this view should have haptic feedback enabled for events such as long presses.

 Value: 268435456

### IMPORTANT_FOR_ACCESSIBILITY_AUTO

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_ACCESSIBILITY_AUTO: Int
```

Automatically determine whether a view is important for accessibility.

 Value: 0

### IMPORTANT_FOR_ACCESSIBILITY_NO

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_ACCESSIBILITY_NO: Int
```

The view is not important for accessibility.

 Value: 2

### IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS: Int
```

The view is not important for accessibility, nor are any of its descendant views.

 Value: 4

### IMPORTANT_FOR_ACCESSIBILITY_YES

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_ACCESSIBILITY_YES: Int
```

The view is important for accessibility.

 Value: 1

### IMPORTANT_FOR_AUTOFILL_AUTO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_AUTOFILL_AUTO: Int
```

Automatically determine whether a view is important for autofill.

 Value: 0

**See Also**

- isImportantForAutofill
- setImportantForAutofill

### IMPORTANT_FOR_AUTOFILL_NO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_AUTOFILL_NO: Int
```

The view is not important for autofill, but its children (if any) will be traversed.

 Value: 2

**See Also**

- isImportantForAutofill
- setImportantForAutofill

### IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS: Int
```

The view is not important for autofill, and its children (if any) will not be traversed.

 Value: 8

**See Also**

- isImportantForAutofill
- setImportantForAutofill

### IMPORTANT_FOR_AUTOFILL_YES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_AUTOFILL_YES: Int
```

The view is important for autofill, and its children (if any) will be traversed.

 Value: 1

**See Also**

- isImportantForAutofill
- setImportantForAutofill

### IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS: Int
```

The view is important for autofill, but its children (if any) will not be traversed.

 Value: 4

**See Also**

- isImportantForAutofill
- setImportantForAutofill

### IMPORTANT_FOR_CONTENT_CAPTURE_AUTO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_CONTENT_CAPTURE_AUTO: Int
```

Automatically determine whether a view is important for content capture.

 Value: 0

**See Also**

- isImportantForContentCapture
- setImportantForContentCapture

### IMPORTANT_FOR_CONTENT_CAPTURE_NO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_CONTENT_CAPTURE_NO: Int
```

The view is not important for content capture, but its children (if any) will be traversed.

 Value: 2

**See Also**

- isImportantForContentCapture
- setImportantForContentCapture

### IMPORTANT_FOR_CONTENT_CAPTURE_NO_EXCLUDE_DESCENDANTS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_CONTENT_CAPTURE_NO_EXCLUDE_DESCENDANTS: Int
```

The view is not important for content capture, and its children (if any) will not be traversed.

 Value: 8

**See Also**

- isImportantForContentCapture
- setImportantForContentCapture

### IMPORTANT_FOR_CONTENT_CAPTURE_YES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_CONTENT_CAPTURE_YES: Int
```

The view is important for content capture, and its children (if any) will be traversed.

 Value: 1

**See Also**

- isImportantForContentCapture
- setImportantForContentCapture

### IMPORTANT_FOR_CONTENT_CAPTURE_YES_EXCLUDE_DESCENDANTS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANT_FOR_CONTENT_CAPTURE_YES_EXCLUDE_DESCENDANTS: Int
```

The view is important for content capture, but its children (if any) will not be traversed.

 Value: 4

**See Also**

- isImportantForContentCapture
- setImportantForContentCapture

### INVISIBLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVISIBLE: Int
```

This view is invisible, but it still takes up space for layout purposes. Use with setVisibility and [`android:visibility`.](View.md)

 Value: 4

### KEEP_SCREEN_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEEP_SCREEN_ON: Int
```

View flag indicating that the screen should remain on while the window containing this view is visible to the user. This effectively takes care of automatically setting the WindowManager's `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_KEEP_SCREEN_ON:kotlin.Int`.

 Value: 67108864

### LAYER_TYPE_HARDWARE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAYER_TYPE_HARDWARE: Int
```

Indicates that the view has a hardware layer. A hardware layer is backed by a hardware specific texture (generally Frame Buffer Objects or FBO on OpenGL hardware) and causes the view to be rendered using Android's hardware rendering pipeline, but only if hardware acceleration is turned on for the view hierarchy. When hardware acceleration is turned off, hardware layers behave exactly as `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int`.

A hardware layer is useful to apply a specific color filter and/or blending mode and/or translucency to a view and all its children.

A hardware layer can be used to cache a complex view tree into a texture and reduce the complexity of drawing operations. For instance, when animating a complex view tree with a translation, a hardware layer can be used to render the view tree only once.

A hardware layer can also be used to increase the rendering quality when rotation transformations are applied on a view. It can also be used to prevent potential clipping issues when applying 3D transforms on a view.

 Value: 2

**See Also**

- getLayerType
- setLayerType
- `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int`

### LAYER_TYPE_NONE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAYER_TYPE_NONE: Int
```

Indicates that the view does not have a layer.

 Value: 0

**See Also**

- getLayerType
- setLayerType
- `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int`

### LAYER_TYPE_SOFTWARE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAYER_TYPE_SOFTWARE: Int
```

Indicates that the view has a software layer. A software layer is backed by a bitmap and causes the view to be rendered using Android's software rendering pipeline, even if hardware acceleration is enabled.

Software layers have various usages:

When the application is not using hardware acceleration, a software layer is useful to apply a specific color filter and/or blending mode and/or translucency to a view and all its children.

When the application is using hardware acceleration, a software layer is useful to render drawing primitives not supported by the hardware accelerated pipeline. It can also be used to cache a complex view tree into a texture and reduce the complexity of drawing operations. For instance, when animating a complex view tree with a translation, a software layer can be used to render the view tree only once.

Software layers should be avoided when the affected view tree updates often. Every update will require to re-render the software layer, which can potentially be slow (particularly when hardware acceleration is turned on since the layer will have to be uploaded into a hardware texture after every update.)

 Value: 1

**See Also**

- getLayerType
- setLayerType
- `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int`

### LAYOUT_DIRECTION_INHERIT

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAYOUT_DIRECTION_INHERIT: Int
```

Horizontal layout direction of this view is inherited from its parent. Use with setLayoutDirection.

 Value: 2

### LAYOUT_DIRECTION_LOCALE

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAYOUT_DIRECTION_LOCALE: Int
```

Horizontal layout direction of this view is from deduced from the default language script for the locale. Use with setLayoutDirection.

 Value: 3

### LAYOUT_DIRECTION_LTR

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAYOUT_DIRECTION_LTR: Int
```

Horizontal layout direction of this view is from Left to Right. Use with setLayoutDirection.

 Value: 0

### LAYOUT_DIRECTION_RTL

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAYOUT_DIRECTION_RTL: Int
```

Horizontal layout direction of this view is from Right to Left. Use with setLayoutDirection.

 Value: 1

### MEASURED_HEIGHT_STATE_SHIFT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEASURED_HEIGHT_STATE_SHIFT: Int
```

Bit shift of `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_MASK:kotlin.Int` to get to the height bits for functions that combine both width and height into a single int, such as getMeasuredState and the childState argument of resolveSizeAndState.

 Value: 16

### MEASURED_SIZE_MASK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEASURED_SIZE_MASK: Int
```

Bits of getMeasuredWidthAndState and getMeasuredWidthAndState that provide the actual measured size.

 Value: 16777215

### MEASURED_STATE_MASK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEASURED_STATE_MASK: Int
```

Bits of getMeasuredWidthAndState and getMeasuredWidthAndState that provide the additional state bits.

 Value: -16777216

### MEASURED_STATE_TOO_SMALL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEASURED_STATE_TOO_SMALL: Int
```

Bit of getMeasuredWidthAndState and getMeasuredWidthAndState that indicates the measured size is smaller that the space the view would like to have.

 Value: 16777216

### NOT_FOCUSABLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOT_FOCUSABLE: Int
```

This view does not want keystrokes.

Use with setFocusable and [`android:focusable`.](View.md)

 Value: 0

### NO_ID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_ID: Int
```

Used to mark a View that has no ID.

 Value: -1

### OVER_SCROLL_ALWAYS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OVER_SCROLL_ALWAYS: Int
```

Always allow a user to over-scroll this view, provided it is a view that can scroll.

 Value: 0

**See Also**

- getOverScrollMode
- setOverScrollMode

### OVER_SCROLL_IF_CONTENT_SCROLLS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OVER_SCROLL_IF_CONTENT_SCROLLS: Int
```

Allow a user to over-scroll this view only if the content is large enough to meaningfully scroll, provided it is a view that can scroll.

 Value: 1

**See Also**

- getOverScrollMode
- setOverScrollMode

### OVER_SCROLL_NEVER

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OVER_SCROLL_NEVER: Int
```

Never allow a user to over-scroll this view.

 Value: 2

**See Also**

- getOverScrollMode
- setOverScrollMode

### POINTER_CAPTURE_MODE_ABSOLUTE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POINTER_CAPTURE_MODE_ABSOLUTE: Int
```

A pointer capture mode in which touchpads report absolute finger locations.

In this capture mode, no attempt is made to recognize gestures from touchpad input. Instead, the absolute location of each touch on the pad is reported directly to the View, in the same way that other touches on devices with `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_POINTER:kotlin.Int` are reported.

Events will be delivered with the source `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_TOUCHPAD:kotlin.Int`. The absolute position of each touch will be available through getX and getY, and their relative movements through `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RELATIVE_X:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RELATIVE_Y:kotlin.Int`. If the touchpad supports them, touch dimension information may be available through the `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_PRESSURE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MAJOR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MINOR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MAJOR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MINOR:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_ORIENTATION:kotlin.Int` axes.

Events from mice are always reported in the same way regardless of capture mode.

 Value: 1

**See Also**

- requestPointerCapture

### POINTER_CAPTURE_MODE_RELATIVE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POINTER_CAPTURE_MODE_RELATIVE: Int
```

A pointer capture mode in which touchpad gestures are recognized and reported like mouse movements.

In this capture mode, the following gestures made on a captured touchpad will be recognized and reported:

- Pointer movement gestures (such as moving a single finger on the pad) will be reported like mouse movements, with the `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_MOVE:kotlin.Int` action and their relative position changes available through android.view.MotionEvent#getX and android.view.MotionEvent#getY.
- Scrolling gestures (such as two-finger swipes) will be reported like scroll wheel movements on a mouse, with the `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_SCROLL:kotlin.Int` action and the scroll amounts available through the `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_VSCROLL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_HSCROLL:kotlin.Int` axes.

Motion values are proportional to the physical motion of the gesturing finger(s), and the physical movement in mm can be found using the resolution reported by getResolution for the relevant axis.

These events will be reported with `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_MOUSE_RELATIVE:kotlin.Int`.

Events from mice are always reported in the same way regardless of capture mode.

 Value: 2

**See Also**

- requestPointerCapture

### POINTER_CAPTURE_MODE_UNCAPTURED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POINTER_CAPTURE_MODE_UNCAPTURED: Int
```

A "pointer capture mode" in which the pointer is not captured.

Passing this to requestPointerCapture is equivalent to calling releasePointerCapture.

 Value: 0

**See Also**

- requestPointerCapture

### RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS: Int
```

Represents that the user interaction that is requesting a rectangle on screen is doing so because the View has input/keyboard focus.

 Value: 3

### RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY: Int
```

Represents that the user interaction that is requesting a rectangle on screen is doing so only to scroll the View on screen, and the rectangle is not associated with a text cursor or keyboard focus.

 Value: 1

### RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR: Int
```

Represents that the user interaction that is requesting a rectangle on screen is doing so because the View contains a text cursor (caret).

 Value: 2

### RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED: Int
```

Represents that the user interaction that is requesting a rectangle on screen is doing so via the original requestRectangleOnScreen or requestRectangleOnScreen APIs that do not define the source. RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED should be reserved for backward compatibility and should only be provided from calls to the original API.

 Value: 0

### REQUESTED_FRAME_RATE_CATEGORY_DEFAULT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUESTED_FRAME_RATE_CATEGORY_DEFAULT: Float
```

 Value: (0.0f/0.0f)

### REQUESTED_FRAME_RATE_CATEGORY_HIGH

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUESTED_FRAME_RATE_CATEGORY_HIGH: Float
```

 Value: -4.0f

### REQUESTED_FRAME_RATE_CATEGORY_LOW

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUESTED_FRAME_RATE_CATEGORY_LOW: Float
```

 Value: -2.0f

### REQUESTED_FRAME_RATE_CATEGORY_NORMAL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUESTED_FRAME_RATE_CATEGORY_NORMAL: Float
```

 Value: -3.0f

### REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE: Float
```

 Value: -1.0f

### SCREEN_STATE_OFF

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_STATE_OFF: Int
```

Indicates that the screen has changed state and is now off.

 Value: 0

**See Also**

- onScreenStateChanged

### SCREEN_STATE_ON

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_STATE_ON: Int
```

Indicates that the screen has changed state and is now on.

 Value: 1

**See Also**

- onScreenStateChanged

### SCROLLBARS_INSIDE_INSET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLLBARS_INSIDE_INSET: Int
```

The scrollbar style to display the scrollbars inside the padded area, increasing the padding of the view. The scrollbars will not overlap the content area of the view.

 Value: 16777216

### SCROLLBARS_INSIDE_OVERLAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLLBARS_INSIDE_OVERLAY: Int
```

The scrollbar style to display the scrollbars inside the content area, without increasing the padding. The scrollbars will be overlaid with translucency on the view's content.

 Value: 0

### SCROLLBARS_OUTSIDE_INSET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLLBARS_OUTSIDE_INSET: Int
```

The scrollbar style to display the scrollbars at the edge of the view, increasing the padding of the view. The scrollbars will only overlap the background, if any.

 Value: 50331648

### SCROLLBARS_OUTSIDE_OVERLAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLLBARS_OUTSIDE_OVERLAY: Int
```

The scrollbar style to display the scrollbars at the edge of the view, without increasing the padding. The scrollbars will be overlaid with translucency.

 Value: 33554432

### SCROLLBAR_POSITION_DEFAULT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLLBAR_POSITION_DEFAULT: Int
```

Position the scroll bar at the default position as determined by the system.

 Value: 0

### SCROLLBAR_POSITION_LEFT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLLBAR_POSITION_LEFT: Int
```

Position the scroll bar along the left edge.

 Value: 1

### SCROLLBAR_POSITION_RIGHT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLLBAR_POSITION_RIGHT: Int
```

Position the scroll bar along the right edge.

 Value: 2

### SCROLL_AXIS_HORIZONTAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_AXIS_HORIZONTAL: Int
```

Indicates scrolling along the horizontal axis.

 Value: 1

### SCROLL_AXIS_NONE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_AXIS_NONE: Int
```

Indicates no axis of view scrolling.

 Value: 0

### SCROLL_AXIS_VERTICAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_AXIS_VERTICAL: Int
```

Indicates scrolling along the vertical axis.

 Value: 2

### SCROLL_CAPTURE_HINT_AUTO

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_CAPTURE_HINT_AUTO: Int
```

The content of this view will be considered for scroll capture if scrolling is possible.

 Value: 0

**See Also**

- getScrollCaptureHint
- setScrollCaptureHint

### SCROLL_CAPTURE_HINT_EXCLUDE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_CAPTURE_HINT_EXCLUDE: Int
```

Explicitly exclude this view as a potential scroll capture target. The system will not consider it. Mutually exclusive with `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int`, which this flag takes precedence over.

 Value: 1

**See Also**

- getScrollCaptureHint
- setScrollCaptureHint

### SCROLL_CAPTURE_HINT_EXCLUDE_DESCENDANTS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_CAPTURE_HINT_EXCLUDE_DESCENDANTS: Int
```

Explicitly exclude all children of this view as potential scroll capture targets. This view is unaffected. Note: Excluded children are not considered, regardless of `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int`.

 Value: 4

**See Also**

- getScrollCaptureHint
- setScrollCaptureHint

### SCROLL_CAPTURE_HINT_INCLUDE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_CAPTURE_HINT_INCLUDE: Int
```

Explicitly include this view as a potential scroll capture target. When locating a scroll capture target, this view will be prioritized before others without this flag. Mutually exclusive with `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE:kotlin.Int`, which takes precedence.

 Value: 2

**See Also**

- getScrollCaptureHint
- setScrollCaptureHint

### SCROLL_INDICATOR_BOTTOM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_INDICATOR_BOTTOM: Int
```

Scroll indicator direction for the bottom edge of the view.

 Value: 2

**See Also**

- setScrollIndicators
- setScrollIndicators
- getScrollIndicators

### SCROLL_INDICATOR_END

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_INDICATOR_END: Int
```

Scroll indicator direction for the ending edge of the view.

Resolved according to the view's layout direction, see getLayoutDirection for more information.

 Value: 32

**See Also**

- setScrollIndicators
- setScrollIndicators
- getScrollIndicators

### SCROLL_INDICATOR_LEFT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_INDICATOR_LEFT: Int
```

Scroll indicator direction for the left edge of the view.

 Value: 4

**See Also**

- setScrollIndicators
- setScrollIndicators
- getScrollIndicators

### SCROLL_INDICATOR_RIGHT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_INDICATOR_RIGHT: Int
```

Scroll indicator direction for the right edge of the view.

 Value: 8

**See Also**

- setScrollIndicators
- setScrollIndicators
- getScrollIndicators

### SCROLL_INDICATOR_START

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_INDICATOR_START: Int
```

Scroll indicator direction for the starting edge of the view.

Resolved according to the view's layout direction, see getLayoutDirection for more information.

 Value: 16

**See Also**

- setScrollIndicators
- setScrollIndicators
- getScrollIndicators

### SCROLL_INDICATOR_TOP

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCROLL_INDICATOR_TOP: Int
```

Scroll indicator direction for the top edge of the view.

 Value: 1

**See Also**

- setScrollIndicators
- setScrollIndicators
- getScrollIndicators

### SOUND_EFFECTS_ENABLED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOUND_EFFECTS_ENABLED: Int
```

View flag indicating whether this view should have sound effects enabled for events such as clicking and touching.

 Value: 134217728

### STATUS_BAR_HIDDEN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_BAR_HIDDEN: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LOW_PROFILE:kotlin.Int` instead.*

 Value: 1

### STATUS_BAR_VISIBLE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_BAR_VISIBLE: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_VISIBLE:kotlin.Int` instead.*

 Value: 0

### SYSTEM_UI_FLAG_FULLSCREEN

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UI_FLAG_FULLSCREEN: Int
```

**Deprecated:** *Use hide with statusBars instead.*

Flag for setSystemUiVisibility: View has requested to go into the normal fullscreen mode so that its content can take over the screen while still allowing the user to interact with the application.

This has the same visual effect as `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_FULLSCREEN:kotlin.Int`, meaning that non-critical screen decorations (such as the status bar) will be hidden while the user is in the View's window, focusing the experience on that content. Unlike the window flag, if you are using ActionBar in overlay mode with `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int`, then enabling this flag will also hide the action bar.

This approach to going fullscreen is best used over the window flag when it is a transient state -- that is, the application does this at certain points in its user interaction where it wants to allow the user to focus on content, but not as a continuous state. For situations where the application would like to simply stay full screen the entire time (such as a game that wants to take over the screen), the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_FULLSCREEN:kotlin.Int` is usually a better approach. The state set here will be removed by the system in various situations (such as the user moving to another application) like the other system UI states.

When using this flag, the application should provide some easy facility for the user to go out of it. A common example would be in an e-book reader, where tapping on the screen brings back whatever screen and UI decorations that had been hidden while the user was immersed in reading the book.

 Value: 4

**See Also**

- setSystemUiVisibility

### SYSTEM_UI_FLAG_HIDE_NAVIGATION

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UI_FLAG_HIDE_NAVIGATION: Int
```

**Deprecated:** *Use hide with navigationBars instead.*

Flag for setSystemUiVisibility: View has requested that the system navigation be temporarily hidden.

This is an even less obtrusive state than that called for by `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LOW_PROFILE:kotlin.Int`; on devices that draw essential navigation controls (Home, Back, and the like) on screen, `SYSTEM_UI_FLAG_HIDE_NAVIGATION` will cause those to disappear. This is useful (in conjunction with the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_FULLSCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_LAYOUT_IN_SCREEN:kotlin.Int` window flags) for displaying content using every last pixel on the display.

There is a limitation: because navigation controls are so important, the least user interaction will cause them to reappear immediately. When this happens, both this flag and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` will be cleared automatically, so that both elements reappear at the same time.

 Value: 2

**See Also**

- setSystemUiVisibility

### SYSTEM_UI_FLAG_IMMERSIVE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UI_FLAG_IMMERSIVE: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_DEFAULT:kotlin.Int` instead.*

Flag for setSystemUiVisibility: View would like to remain interactive when hiding the navigation bar with `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`. If this flag is not set, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int` will be force cleared by the system on any user interaction.

Since this flag is a modifier for `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`, it only has an effect when used in combination with that flag.

 Value: 2048

### SYSTEM_UI_FLAG_IMMERSIVE_STICKY

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UI_FLAG_IMMERSIVE_STICKY: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE:kotlin.Int` instead.*

Flag for setSystemUiVisibility: View would like to remain interactive when hiding the status bar with `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` and/or hiding the navigation bar with `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`. Use this flag to create an immersive experience while also hiding the system bars. If this flag is not set, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int` will be force cleared by the system on any user interaction, and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` will be force-cleared by the system if the user swipes from the top of the screen.

When system bars are hidden in immersive mode, they can be revealed temporarily with system gestures, such as swiping from the top of the screen. These transient system bars will overlay app's content, may have some degree of transparency, and will automatically hide after a short timeout.

Since this flag is a modifier for `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`, it only has an effect when used in combination with one or both of those flags.

 Value: 4096

### SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN: Int
```

**Deprecated:** *For floating windows, use setFitInsetsTypes with statusBars ()}. For non-floating windows that fill the screen, call setDecorFitsSystemWindows with `false`.*

Flag for setSystemUiVisibility: View would like its window to be laid out as if it has requested `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`, even if it currently hasn't. This allows it to avoid artifacts when switching in and out of that mode, at the expense that some of its user interface may be covered by screen decorations when they are shown. You can perform layout of your inner UI elements to account for non-fullscreen system UI through the fitSystemWindows method.

Note: on displays that have a DisplayCutout, the window may still be placed differently than if `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` was set, if the window's `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#layoutInDisplayCutoutMode:kotlin.Int` is `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#LAYOUT_IN_DISPLAY_CUTOUT_MODE_DEFAULT:kotlin.Int`. To avoid this, use either of the other modes.

 Value: 1024

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#layoutInDisplayCutoutMode:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#LAYOUT_IN_DISPLAY_CUTOUT_MODE_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#LAYOUT_IN_DISPLAY_CUTOUT_MODE_SHORT_EDGES:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#LAYOUT_IN_DISPLAY_CUTOUT_MODE_NEVER:kotlin.Int`

### SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION: Int
```

**Deprecated:** *For floating windows, use setFitInsetsTypes with navigationBars. For non-floating windows that fill the screen, call setDecorFitsSystemWindows with `false`.*

Flag for setSystemUiVisibility: View would like its window to be laid out as if it has requested `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`, even if it currently hasn't. This allows it to avoid artifacts when switching in and out of that mode, at the expense that some of its user interface may be covered by screen decorations when they are shown. You can perform layout of your inner UI elements to account for the navigation system UI through the fitSystemWindows method.

 Value: 512

### SYSTEM_UI_FLAG_LAYOUT_STABLE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UI_FLAG_LAYOUT_STABLE: Int
```

**Deprecated:** *Use getInsetsIgnoringVisibility instead to retrieve insets that don't change when system bars change visibility state.*

Flag for setSystemUiVisibility: When using other layout flags, we would like a stable view of the content insets given to fitSystemWindows. This means that the insets seen there will always represent the worst case that the application can expect as a continuous state. In the stock Android UI this is the space for the system bar, nav bar, and status bar, but not more transient elements such as an input method. The stable layout your UI sees is based on the system UI modes you can switch to. That is, if you specify `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int` then you will get a stable layout for changes of the `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` mode; if you specify `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int`, then you can transition to `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int` with a stable layout. (Note that you should avoid using `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int` by itself.) If you have set the window flag `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_FULLSCREEN:kotlin.Int` to hide the status bar (instead of using `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`), then a hidden status bar will be considered a "stable" state for purposes here. This allows your UI to continually hide the status bar, while still using the system UI flags to hide the action bar while still retaining a stable layout. Note that changing the window fullscreen flag will never provide a stable layout for a clean transition.

If you are using ActionBar in overlay mode with `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int`, this flag will also impact the insets it adds to those given to the application.

 Value: 256

### SYSTEM_UI_FLAG_LIGHT_NAVIGATION_BAR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UI_FLAG_LIGHT_NAVIGATION_BAR: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_NAVIGATION_BARS:kotlin.Int` instead.*

Flag for setSystemUiVisibility: Requests the navigation bar to draw in a mode that is compatible with light navigation bar backgrounds.

For this to take effect, the window must request `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS:kotlin.Int` but not `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_TRANSLUCENT_NAVIGATION:kotlin.Int`.

 Value: 16

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.attr.html#windowLightNavigationBar:kotlin.Int`

### SYSTEM_UI_FLAG_LIGHT_STATUS_BAR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UI_FLAG_LIGHT_STATUS_BAR: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_STATUS_BARS:kotlin.Int` instead.*

Flag for setSystemUiVisibility: Requests the status bar to draw in a mode that is compatible with light status bar backgrounds.

For this to take effect, the window must request `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS:kotlin.Int` but not `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_TRANSLUCENT_STATUS:kotlin.Int`.

 Value: 8192

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.attr.html#windowLightStatusBar:kotlin.Int`

### SYSTEM_UI_FLAG_LOW_PROFILE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UI_FLAG_LOW_PROFILE: Int
```

**Deprecated:** *Low profile mode is deprecated. Hide the system bars instead if the application needs to be in a unobtrusive mode. Use hide with systemBars.*

Flag for setSystemUiVisibility: View has requested the system UI to enter an unobtrusive "low profile" mode.

This is for use in games, book readers, video players, or any other "immersive" application where the usual system chrome is deemed too distracting.

In low profile mode, the status bar and/or navigation icons may dim.

 Value: 1

**See Also**

- setSystemUiVisibility

### SYSTEM_UI_FLAG_VISIBLE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UI_FLAG_VISIBLE: Int
```

**Deprecated:** *SystemUiVisibility flags are deprecated. Use WindowInsetsController instead.*

Special constant for setSystemUiVisibility: View has requested the system UI (status bar) to be visible (the default).

 Value: 0

**See Also**

- setSystemUiVisibility

### SYSTEM_UI_LAYOUT_FLAGS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UI_LAYOUT_FLAGS: Int
```

**Deprecated:** *System UI layout flags are deprecated.*

Flags that can impact the layout in relation to system UI.

 Value: 1536

### TEXT_ALIGNMENT_CENTER

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_ALIGNMENT_CENTER: Int
```

Center the paragraph, e.g. ALIGN_CENTER. Use with setTextAlignment

 Value: 4

### TEXT_ALIGNMENT_GRAVITY

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_ALIGNMENT_GRAVITY: Int
```

Default for the root view. The gravity determines the text alignment, ALIGN_NORMAL, ALIGN_CENTER, or ALIGN_OPPOSITE, which are relative to each paragraph's text direction. Use with setTextAlignment

 Value: 1

### TEXT_ALIGNMENT_INHERIT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_ALIGNMENT_INHERIT: Int
```

Default text alignment. The text alignment of this View is inherited from its parent. Use with setTextAlignment

 Value: 0

### TEXT_ALIGNMENT_TEXT_END

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_ALIGNMENT_TEXT_END: Int
```

Align to the end of the paragraph, e.g. ALIGN_OPPOSITE. Use with setTextAlignment

 Value: 3

### TEXT_ALIGNMENT_TEXT_START

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_ALIGNMENT_TEXT_START: Int
```

Align to the start of the paragraph, e.g. ALIGN_NORMAL. Use with setTextAlignment

 Value: 2

### TEXT_ALIGNMENT_VIEW_END

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_ALIGNMENT_VIEW_END: Int
```

Align to the end of the view, which is ALIGN_RIGHT if the view's resolved layoutDirection is LTR, and ALIGN_LEFT otherwise. Use with setTextAlignment

 Value: 6

### TEXT_ALIGNMENT_VIEW_START

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_ALIGNMENT_VIEW_START: Int
```

Align to the start of the view, which is ALIGN_LEFT if the view's resolved layoutDirection is LTR, and ALIGN_RIGHT otherwise. Use with setTextAlignment

 Value: 5

### TEXT_DIRECTION_ANY_RTL

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_DIRECTION_ANY_RTL: Int
```

Text direction is using "any-RTL" algorithm. The paragraph direction is RTL if it contains any strong RTL character, otherwise it is LTR if it contains any strong LTR characters. If there are neither, the paragraph direction is the view's resolved layout direction.

 Value: 2

### TEXT_DIRECTION_FIRST_STRONG

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_DIRECTION_FIRST_STRONG: Int
```

Text direction is using "first strong algorithm". The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is the view's resolved layout direction.

 Value: 1

### TEXT_DIRECTION_FIRST_STRONG_LTR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_DIRECTION_FIRST_STRONG_LTR: Int
```

Text direction is using "first strong algorithm". The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is LTR.

 Value: 6

### TEXT_DIRECTION_FIRST_STRONG_RTL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_DIRECTION_FIRST_STRONG_RTL: Int
```

Text direction is using "first strong algorithm". The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is RTL.

 Value: 7

### TEXT_DIRECTION_INHERIT

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_DIRECTION_INHERIT: Int
```

Text direction is inherited through ViewGroup

 Value: 0

### TEXT_DIRECTION_LOCALE

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_DIRECTION_LOCALE: Int
```

Text direction is coming from the system Locale.

 Value: 5

### TEXT_DIRECTION_LTR

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_DIRECTION_LTR: Int
```

Text direction is forced to LTR.

 Value: 3

### TEXT_DIRECTION_RTL

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_DIRECTION_RTL: Int
```

Text direction is forced to RTL.

 Value: 4

### VIEW_LOG_TAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val VIEW_LOG_TAG: String
```

The logging tag used by this class with android.util.Log.

 Value: "View"

### VISIBLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VISIBLE: Int
```

This view is visible. Use with setVisibility and [`android:visibility`.](View.md)

 Value: 0

## Public constructors

### View

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
View(context: Context!)
```

Simple constructor to use when creating a view from code.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: The Context the view is running in, through which it can access the current theme, resources, etc. |

### View

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
View(
    context: Context!, 
    attrs: AttributeSet?)
```

Constructor that is called when inflating a view from XML. This is called when a view is being constructed from an XML file, supplying attributes that were specified in the XML file. This version uses a default style of 0, so the only attribute values applied are those in the Context's Theme and the given AttributeSet.

The method onFinishInflate() will be called after all children have been added.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: The Context the view is running in, through which it can access the current theme, resources, etc. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)?: The attributes of the XML tag that is inflating the view. This value may be `null`. |

**See Also**

- View

### View

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
View(
    context: Context!, 
    attrs: AttributeSet?, 
    defStyleAttr: Int)
```

Perform inflation from XML and apply a class-specific base style from a theme attribute. This constructor of View allows subclasses to use their own base style when they are inflating. For example, a Button class's constructor would call this version of the super class constructor and supply `R.attr.buttonStyle` for defStyleAttr; this allows the theme's button style to modify all of the base view attributes (in particular its background) as well as the Button class's attributes.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: The Context the view is running in, through which it can access the current theme, resources, etc. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)?: The attributes of the XML tag that is inflating the view. This value may be `null`. |
| `defStyleAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An attribute in the current theme that contains a reference to a style resource that supplies default values for the view. Can be 0 to not look for defaults. |
| --- | --- |

**See Also**

- View

### View

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
View(
    context: Context!, 
    attrs: AttributeSet?, 
    defStyleAttr: Int, 
    defStyleRes: Int)
```

Perform inflation from XML and apply a class-specific base style from a theme attribute or style resource. This constructor of View allows subclasses to use their own base style when they are inflating.

When determining the final value of a particular attribute, there are four inputs that come into play:

1. Any attribute values in the given AttributeSet.
2. The style resource specified in the AttributeSet (named "style").
3. The default style specified by defStyleAttr.
4. The default style specified by defStyleRes.
5. The base values in this theme.

Each of these inputs is considered in-order, with the first listed taking precedence over the following ones. In other words, if in the AttributeSet you have supplied `<Button * textColor="#ff000000">` , then the button's text will *always* be black, regardless of what is specified in any of the styles.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: The Context the view is running in, through which it can access the current theme, resources, etc. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)?: The attributes of the XML tag that is inflating the view. This value may be `null`. |
| `defStyleAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An attribute in the current theme that contains a reference to a style resource that supplies default values for the view. Can be 0 to not look for defaults. |
| --- | --- |
| `defStyleRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A resource identifier of a style resource that supplies default values for the view, used only if defStyleAttr is 0 or can not be found in the theme. Can be 0 to not look for defaults. |

**See Also**

- View

## Public methods

### addChildrenForAccessibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addChildrenForAccessibility(outChildren: ArrayList<View!>!): Unit
```

Adds the children of this View relevant for accessibility to the given list as output. Since some Views are not important for accessibility the added child views are not necessarily direct children of this view, rather they are the first level of descendants important for accessibility.

| Parameters ||
|---|---|
| `outChildren` | [ArrayList](../java.util/ArrayList.md)\< [View](View.md)!\>!: The output list that will receive children for accessibility. |

### addExtraDataToAccessibilityNodeInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addExtraDataToAccessibilityNodeInfo(
    info: AccessibilityNodeInfo, 
    extraDataKey: String, 
    arguments: Bundle?
): Unit
```

Adds extra data to an AccessibilityNodeInfo based on an explicit request for the additional data.

This method only needs overloading if the node is marked as having extra data available.
. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `info` | [AccessibilityNodeInfo](../android.view.accessibility/AccessibilityNodeInfo.md): The info to which to add the extra data. Never `null`. |
| `extraDataKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A key specifying the type of extra data to add to the info. The extra data should be added to the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` returned by the info's getExtras method. Never `null`. |
| `arguments` | [Bundle](../android.os/Bundle.md)?: A `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` holding any arguments relevant for this request. May be `null` if the service provided no arguments. |
| --- | --- |

**See Also**

- setAvailableExtraData

### addFocusables

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addFocusables(
    views: ArrayList<View!>!, 
    direction: Int
): Unit
```

Add any focusable views that are descendants of this view (possibly including this view if it is focusable itself) to views. If we are in touch mode, only add views that are also focusable in touch mode.

| Parameters ||
|---|---|
| `views` | [ArrayList](../java.util/ArrayList.md)\< [View](View.md)!\>!: Focusable views found so far |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction of the focus. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` |

### addFocusables

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addFocusables(
    views: ArrayList<View!>!, 
    direction: Int, 
    focusableMode: Int
): Unit
```

Adds any focusable views that are descendants of this view (possibly including this view if it is focusable itself) to views. This method adds all focusable views regardless if we are in touch mode or only views focusable in touch mode if we are in touch mode or only views that can take accessibility focus if accessibility is enabled depending on the focusable mode parameter.

| Parameters ||
|---|---|
| `views` | [ArrayList](../java.util/ArrayList.md)\< [View](View.md)!\>!: Focusable views found so far or null if all we are interested is the number of focusables. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction of the focus. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` |
| `focusableMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of focusables to be added. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLES_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLES_TOUCH_MODE:kotlin.Int` |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLES_ALL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLES_TOUCH_MODE:kotlin.Int`

### addKeyboardNavigationClusters

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addKeyboardNavigationClusters(
    views: MutableCollection<View!>, 
    direction: Int
): Unit
```

Adds any keyboard navigation cluster roots that are descendants of this view (possibly including this view if it is a cluster root itself) to views.

| Parameters ||
|---|---|
| `views` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [View](View.md)!\>: Keyboard navigation cluster roots found so far. This value cannot be `null`. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Direction to look |

### addOnAttachStateChangeListener

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnAttachStateChangeListener(listener: View.OnAttachStateChangeListener!): Unit
```

Add a listener for attach state changes. This listener will be called whenever this view is attached or detached from a window. Remove the listener using removeOnAttachStateChangeListener.

| Parameters ||
|---|---|
| `listener` | [View.OnAttachStateChangeListener](../android/view/View.OnAttachStateChangeListener.md)!: Listener to attach |

**See Also**

- removeOnAttachStateChangeListener

### addOnLayoutChangeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnLayoutChangeListener(listener: View.OnLayoutChangeListener!): Unit
```

Add a listener that will be called when the bounds of the view change due to layout processing.

| Parameters ||
|---|---|
| `listener` | [View.OnLayoutChangeListener](../android/view/View.OnLayoutChangeListener.md)!: The listener that will be called when layout bounds change. |

### addOnUnhandledKeyEventListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnUnhandledKeyEventListener(listener: View.OnUnhandledKeyEventListener!): Unit
```

Adds a listener which will receive unhandled KeyEvents. This must be called on the UI thread.

| Parameters ||
|---|---|
| `listener` | [View.OnUnhandledKeyEventListener](../android/view/View.OnUnhandledKeyEventListener.md)!: a receiver of unhandled KeyEvents. |

**See Also**

- removeOnUnhandledKeyEventListener

### addTouchables

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addTouchables(views: ArrayList<View!>!): Unit
```

Add any touchable views that are descendants of this view (possibly including this view if it is touchable itself) to views.

| Parameters ||
|---|---|
| `views` | [ArrayList](../java.util/ArrayList.md)\< [View](View.md)!\>!: Touchable views found so far |

### animate

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun animate(): ViewPropertyAnimator!
```

This method returns a ViewPropertyAnimator object, which can be used to animate specific properties on this View.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator!` | ViewPropertyAnimator The ViewPropertyAnimator associated with this View. |

### announceForAccessibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun announceForAccessibility(text: CharSequence!): Unit
```

**Deprecated:** *Use one of the methods described in the documentation above to semantically describe UI instead of using an announcement, as accessibility services may choose to ignore events dispatched with this method.*

Convenience method for sending a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_ANNOUNCEMENT:kotlin.Int` AccessibilityEvent to suggest that an accessibility service announce the specified text to its users.

Note: The event generated with this API carries no semantic meaning, and accessibility services may choose to ignore it. Apps that accurately supply accessibility with the semantics of their UI should not need to specify what exactly is announced.

In general, do not attempt to generate announcements as confirmation message for simple actions like a button press. Label your controls concisely and precisely instead.

To convey significant UI changes like window changes, use setTitle and setAccessibilityPaneTitle.

Use setAccessibilityLiveRegion to inform the user of changes to critical views within the user interface. These should still be used sparingly as they may generate announcements every time a View is updated.

Use setStateDescription to convey state changes to views within the user interface. While a live region may send different types of events generated by the view, state description will send `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` events of type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION:kotlin.Int`.

For notifying users about errors, such as in a login screen with text that displays an "incorrect password" notification, set setError and dispatch an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` event with a change type of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_ERROR:kotlin.Int`, instead. Some widgets may expose methods that convey error states to accessibility automatically, such as setError, which manages these accessibility semantics and event dispatch for callers.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The announcement text. |

### autofill

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun autofill(values: SparseArray<AutofillValue!>): Unit
```

Automatically fills the content of the virtual children within this view.

Views with virtual children support the Autofill Framework mainly by:

- Providing the metadata defining what the virtual children mean and how they can be autofilled.
- Implementing the methods that autofill the virtual children.

onProvideAutofillVirtualStructure is responsible for the former, this method is responsible for the latter - see autofill and onProvideAutofillVirtualStructure for more info about autofill.

If a child value is updated asynchronously, the next call to notifyValueChanged must happen **after** the value was changed to the autofilled value. If not, the child will not be considered autofilled.

**Note:** To indicate that a virtual view was autofilled, `?android:attr/autofilledHighlight` should be drawn over it until the data changes.

| Parameters ||
|---|---|
| `values` | [SparseArray](../android.util/SparseArray.md)\< [AutofillValue](../android.view.autofill/AutofillValue.md)!\>: map of values to be autofilled, keyed by virtual child id. This value cannot be `null`. |

### autofill

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun autofill(value: AutofillValue!): Unit
```

Automatically fills the content of this view with the `value`.

Views support the Autofill Framework mainly by:

- Providing the metadata defining what the view means and how it can be autofilled.
- Implementing the methods that autofill the view.

onProvideAutofillStructure is responsible for the former, this method is responsible for latter.

This method does nothing by default, but when overridden it typically:

1. Checks if the provided value matches the expected type (which is defined by getAutofillType).
2. Checks if the view is editable - if it isn't, it should return right away.
3. Call the proper getter method on AutofillValue to fetch the actual value.
4. Pass the actual value to the equivalent setter in the view.

For example, a text-field view could implement the method this way:

```kotlin
@Override
  public void autofill(AutofillValue value) {
    if (!value.isText() || !this.isEditable()) {
       return;
    }
    CharSequence text = value.getTextValue();
    if (text != null) {
      this.setText(text);
    }
  }
  
```

If the value is updated asynchronously, the next call to notifyValueChanged must happen **after** the value was changed to the autofilled value. If not, the view will not be considered autofilled.

**Note:** After this method is called, the value returned by getAutofillValue must be equal to the `value` passed to it, otherwise the view will not be highlighted as autofilled.

| Parameters ||
|---|---|
| `value` | [AutofillValue](../android.view.autofill/AutofillValue.md)!: value to be autofilled. |

### bringToFront

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bringToFront(): Unit
```

Change the view's z order in the tree, so it's on top of other sibling views. This ordering change may affect layout, if the parent container uses an order-dependent layout scheme (e.g., LinearLayout). Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int` this method should be followed by calls to requestLayout and invalidate on the view's parent to force the parent to redraw with the new child ordering.
**See Also**

- bringChildToFront

### buildDrawingCache

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun buildDrawingCache(): Unit
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Calling this method is equivalent to calling `buildDrawingCache(false)`.
**See Also**

- buildDrawingCache

### buildDrawingCache

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun buildDrawingCache(autoScale: Boolean): Unit
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Forces the drawing cache to be built if the drawing cache is invalid.

If you call buildDrawingCache manually without calling setDrawingCacheEnabled, you should cleanup the cache by calling destroyDrawingCache afterwards.

Note about auto scaling in compatibility mode: When auto scaling is not enabled, this method will create a bitmap of the same size as this view. Because this bitmap will be drawn scaled by the parent ViewGroup, the result on screen might show scaling artifacts. To avoid such artifacts, you should call this method by setting the auto scaling to true. Doing so, however, will generate a bitmap of a different size than the view. This implies that your application must be able to handle this size.

You should avoid calling this method when hardware acceleration is enabled. If you do not need the drawing cache bitmap, calling this method will increase memory usage and cause the view to be rendered in software once, thus negatively impacting performance.
**See Also**

- getDrawingCache
- destroyDrawingCache

### buildLayer

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun buildLayer(): Unit
```

Forces this view's layer to be created and this view to be rendered into its layer. If this view's layer type is set to `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`, invoking this method will have no effect. This method can for instance be used to render a view into its layer before starting an animation. If this view is complex, rendering into the layer before starting the animation will avoid skipping frames.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If this view is not attached to a window |

**See Also**

- setLayerType

### callOnClick

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callOnClick(): Boolean
```

Directly call any attached OnClickListener. Unlike performClick, this only calls the listener, and does not do any associated clicking actions like reporting an accessibility event.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True there was an assigned OnClickListener that was called, false otherwise is returned. |

### canResolveLayoutDirection

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canResolveLayoutDirection(): Boolean
```

Check if layout direction resolution can be done.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if layout direction resolution can be done otherwise return false. |

### canResolveTextAlignment

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canResolveTextAlignment(): Boolean
```

Check if text alignment resolution can be done.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if text alignment resolution can be done otherwise return false. |

### canResolveTextDirection

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canResolveTextDirection(): Boolean
```

Check if text direction resolution can be done.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if text direction resolution can be done otherwise return false. |

### canScrollHorizontally

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canScrollHorizontally(direction: Int): Boolean
```

Check if this view can be scrolled horizontally in a certain direction.

This is without regard to whether the view is enabled or not, or if it will scroll in response to user input or not.

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Negative to check scrolling left, positive to check scrolling right. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this view can be scrolled in the specified direction, false otherwise. |

### canScrollVertically

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canScrollVertically(direction: Int): Boolean
```

Check if this view can be scrolled vertically in a certain direction.

This is without regard to whether the view is enabled or not, or if it will scroll in response to user input or not.

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Negative to check scrolling up, positive to check scrolling down. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this view can be scrolled in the specified direction, false otherwise. |

### cancelDragAndDrop

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun cancelDragAndDrop(): Unit
```

Cancels an ongoing drag and drop operation.

A DragEvent object with getAction value of `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENDED:kotlin.Int` and getResult value of `false` will be sent to every View that received `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_STARTED:kotlin.Int` even if they are not currently visible.

This method can be called on any View in the same window as the View on which startDragAndDrop was called.

### cancelLongPress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancelLongPress(): Unit
```

Cancels a pending long press. Your subclass can use this if you want the context menu to come up if the user presses and holds at the same place, but you don't want it to come up if they press and then move around enough to cause scrolling.

### cancelPendingInputEvents

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun cancelPendingInputEvents(): Unit
```

Cancel any deferred high-level input events that were previously posted to the event queue.

Many views post high-level events such as click handlers to the event queue to run deferred in order to preserve a desired user experience - clearing visible pressed states before executing, etc. This method will abort any events of this nature that are currently in flight.

Custom views that generate their own high-level deferred input events should override onCancelPendingInputEvents and remove those pending events from the queue.

This will also cancel pending input events for any child views.

Note that this may not be sufficient as a debouncing strategy for clicks in all cases. This will not impact newer events posted after this call that may occur as a result of lower-level input events still waiting in the queue. If you are trying to prevent double-submitted events for the duration of some sort of asynchronous transaction you should also take other steps to protect against unexpected double inputs e.g. calling setEnabled and re-enabling the view when the transaction completes, tracking already submitted transaction IDs, etc.

### checkInputConnectionProxy

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkInputConnectionProxy(view: View!): Boolean
```

Called by the InputMethodManager when a view who is not the current input connection target is trying to make a call on the manager. The default implementation returns false; you can override this to return true for certain views if you are performing InputConnection proxying to them.

| Parameters ||
|---|---|
| `view` | [View](View.md)!: The View that is making the InputMethodManager call. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Return true to allow the call, false to reject. |

### clearAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearAnimation(): Unit
```

Cancels any animations for this view.

### clearFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearFocus(): Unit
```

Called when this view wants to give up focus. If focus is cleared onFocusChanged is called.

**Note:** When not in touch-mode, the framework will try to give focus to the first focusable View from the top after focus is cleared. Hence, if this View is the first from the top that can take focus, then all callbacks related to clearing focus will be invoked after which the framework will give focus to this view.

### clearPendingCredentialRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearPendingCredentialRequest(): Unit
```

Clears the request and callback previously set through setPendingCredentialRequest. Once this API is invoked, there will be no request fired to `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` on future view focus events.
**See Also**

- setPendingCredentialRequest

### clearViewTranslationCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearViewTranslationCallback(): Unit
```

Clear the ViewTranslationCallback from this view.

### combineMeasuredStates

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun combineMeasuredStates(
    curState: Int, 
    newState: Int
): Int
```

Merge two states as returned by getMeasuredState.

| Parameters ||
|---|---|
| `curState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The current state as returned from a view or the result of combining multiple views. |
| `newState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new view state to combine. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns a new integer reflecting the combination of the two states. |

### computeScroll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeScroll(): Unit
```

Called by a parent to request that a child update its values for mScrollX and mScrollY if necessary. This will typically be done if the child is animating a scroll using a `https://developer.android.com/reference/kotlin/android/widget/Scroller.html#` object.

### computeSystemWindowInsets

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeSystemWindowInsets(
    in: WindowInsets!, 
    outLocalInsets: Rect!
): WindowInsets!
```

Compute insets that should be consumed by this view and the ones that should propagate to those under it.

| Parameters ||
|---|---|
| `in` | [WindowInsets](WindowInsets.md)!: Insets currently being processed by this View, likely received as a parameter to onApplyWindowInsets. |
| `outLocalInsets` | [Rect](../android.graphics/Rect.md)!: A Rect that will receive the insets that should be consumed by this view |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/WindowInsets!` | Insets that should be passed along to views under this one |

### createAccessibilityNodeInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createAccessibilityNodeInfo(): AccessibilityNodeInfo!
```

Returns an AccessibilityNodeInfo representing this view from the point of view of an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This method is responsible for obtaining an accessibility node info from a pool of reusable instances and calling onInitializeAccessibilityNodeInfo on this view to initialize the former.

Note: The client is responsible for recycling the obtained instance by calling recycle to minimize object creation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo!` | A populated AccessibilityNodeInfo. |

**See Also**

- AccessibilityNodeInfo

### createContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createContextMenu(menu: ContextMenu!): Unit
```

Show the context menu for this view. It is not safe to hold on to the menu after returning from this method. You should normally not overload this method. Overload onCreateContextMenu or define an `https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener` to add items to the context menu.

| Parameters ||
|---|---|
| `menu` | [ContextMenu](ContextMenu.md)!: The context menu to populate |

### destroyDrawingCache

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun destroyDrawingCache(): Unit
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Frees the resources used by the drawing cache. If you call buildDrawingCache manually without calling setDrawingCacheEnabled, you should cleanup the cache with this method afterwards.
**See Also**

- setDrawingCacheEnabled
- buildDrawingCache
- getDrawingCache

### dispatchApplyWindowInsets

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchApplyWindowInsets(insets: WindowInsets!): WindowInsets!
```

Request to apply the given window insets to this view or another view in its subtree.

This method should be called by clients wishing to apply insets corresponding to areas obscured by window decorations or overlays. This can include the status and navigation bars, action bars, input methods and more. New inset categories may be added in the future. The method returns the insets provided minus any that were applied by this view or its children.

Clients wishing to provide custom behavior should override the onApplyWindowInsets method or alternatively provide a `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener` via the setOnApplyWindowInsetsListener method.

This method replaces the older fitSystemWindows method.

| Parameters ||
|---|---|
| `insets` | [WindowInsets](WindowInsets.md)!: Insets to apply |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/WindowInsets!` | The provided insets minus the insets that were consumed |

### dispatchCapturedPointerEvent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchCapturedPointerEvent(event: MotionEvent!): Boolean
```

Pass a captured pointer event down to the focused view.

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The motion event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

### dispatchConfigurationChanged

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchConfigurationChanged(newConfig: Configuration!): Unit
```

Dispatch a notification about a resource configuration change down the view hierarchy. ViewGroups should override to route to their children.

| Parameters ||
|---|---|
| `newConfig` | [Configuration](../android.content.res/Configuration.md)!: The new resource configuration. |

**See Also**

- onConfigurationChanged

### dispatchCreateViewTranslationRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchCreateViewTranslationRequest(
    viewIds: MutableMap<AutofillId!, LongArray!>, 
    supportedFormats: IntArray, 
    capability: TranslationCapability, 
    requests: MutableList<ViewTranslationRequest!>
): Unit
```

Dispatch to collect the ViewTranslationRequests for translation purpose by traversing the hierarchy when the app requests ui translation. Typically, this method should only be overridden by subclasses that provide a view hierarchy (such as ViewGroup). Other classes should override onCreateViewTranslationRequest for normal view or override onVirtualViewTranslationResponses for view contains virtual children. When requested to start the ui translation, the system will call this method to traverse the view hierarchy to collect ViewTranslationRequests and create a Translator to translate the requests. All the ViewTranslationRequests must be added when the traversal is done.

The default implementation calls onCreateViewTranslationRequest for normal view or calls onVirtualViewTranslationResponses for view contains virtual children to build ViewTranslationRequest if the view should be translated. The view is marked as having setHasTransientState so that recycling of views doesn't prevent the system from attaching the response to it. Therefore, if overriding this method, you should set or reset the transient state.

| Parameters ||
|---|---|
| `viewIds` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [AutofillId](../android.view.autofill/AutofillId.md)!, [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!\>: a map for the view's AutofillId and its virtual child ids or `null` if the view doesn't have virtual child that should be translated. The virtual child ids are the same virtual ids provided by ContentCapture. |
| `supportedFormats` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the supported translation formats. For now, the only possible value is the `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec#DATA_FORMAT_TEXT:kotlin.Int`. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec#DATA_FORMAT_TEXT:kotlin.Int` |
| `capability` | [TranslationCapability](../android.view.translation/TranslationCapability.md): a TranslationCapability that holds translation capability. information, e.g. source spec, target spec. This value cannot be `null`. |
| --- | --- |
| `requests` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ViewTranslationRequest](../android.view.translation/ViewTranslationRequest.md)!\>: fill in with ViewTranslationRequests for translation purpose. This value cannot be `null`. |

### dispatchDisplayHint

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchDisplayHint(hint: Int): Unit
```

Dispatch a hint about whether this view is displayed. For instance, when a View moves out of the screen, it might receives a display hint indicating the view is not displayed. Applications should not *rely* on this hint as there is no guarantee that they will receive one.

| Parameters ||
|---|---|
| `hint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A hint about whether or not this view is displayed: `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` |

### dispatchDragEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchDragEvent(event: DragEvent!): Boolean
```

Detects if this View is enabled and has a drag event listener. If both are true, then it calls the drag event listener with the DragEvent it received. If the drag event listener returns `true`, then dispatchDragEvent() returns `true`.

For all other cases, the method calls the onDragEvent drag event handler method and returns its result.

This ensures that a drag event is always consumed, even if the View does not have a drag event listener. However, if the View has a listener and the listener returns true, then onDragEvent() is not called.

### dispatchDrawableHotspotChanged

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchDrawableHotspotChanged(
    x: Float, 
    y: Float
): Unit
```

Dispatches drawableHotspotChanged to all of this View's children.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): hotspot x coordinate |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): hotspot y coordinate |

**See Also**

- drawableHotspotChanged

### dispatchFinishTemporaryDetach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchFinishTemporaryDetach(): Unit
```

Dispatch onFinishTemporaryDetach to this View and its direct children if this is a container View. 
If you override this method you *must* call through to the superclass implementation.

### dispatchGenericMotionEvent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchGenericMotionEvent(event: MotionEvent!): Boolean
```

Dispatch a generic motion event.

Generic motion events with source class `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_POINTER:kotlin.Int` are delivered to the view under the pointer. All other generic motion events are delivered to the focused view. Hover events are handled specially and are delivered to onHoverEvent first.

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The motion event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

**See Also**

- onHoverEvent
- onGenericMotionEvent

### dispatchKeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchKeyEvent(event: KeyEvent!): Boolean
```

Dispatch a key event to the next view on the focus path. This path runs from the top of the view tree down to the currently focused view. If this view has focus, it will dispatch to itself. Otherwise it will dispatch the next node down the focus path. This method also fires any key listeners.

| Parameters ||
|---|---|
| `event` | [KeyEvent](KeyEvent.md)!: The key event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled, false otherwise. |

### dispatchKeyEventPreIme

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchKeyEventPreIme(event: KeyEvent!): Boolean
```

Dispatch a key event before it is processed by any input method associated with the view hierarchy. This can be used to intercept key events in special situations before the IME consumes them; a typical example would be handling the BACK key to update the application's UI instead of allowing the IME to see it and close itself.

| Parameters ||
|---|---|
| `event` | [KeyEvent](KeyEvent.md)!: The key event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled, false otherwise. |

### dispatchKeyShortcutEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchKeyShortcutEvent(event: KeyEvent!): Boolean
```

Dispatches a key shortcut event.

| Parameters ||
|---|---|
| `event` | [KeyEvent](KeyEvent.md)!: The key event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

### dispatchNestedFling

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchNestedFling(
    velocityX: Float, 
    velocityY: Float, 
    consumed: Boolean
): Boolean
```

Dispatch a fling to a nested scrolling parent.

This method should be used to indicate that a nested scrolling child has detected suitable conditions for a fling. Generally this means that a touch scroll has ended with a VelocityTracker in the direction of scrolling that meets or exceeds the getScaledMinimumFlingVelocity along a scrollable axis.

If a nested scrolling child view would normally fling but it is at the edge of its own content, it can use this method to delegate the fling to its nested scrolling parent instead. The parent may optionally consume the fling or observe a child fling.

| Parameters ||
|---|---|
| `velocityX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Horizontal fling velocity in pixels per second |
| `velocityY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Vertical fling velocity in pixels per second |
| `consumed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the child consumed the fling, false otherwise |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the nested scrolling parent consumed or otherwise reacted to the fling |

### dispatchNestedPreFling

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchNestedPreFling(
    velocityX: Float, 
    velocityY: Float
): Boolean
```

Dispatch a fling to a nested scrolling parent before it is processed by this view.

Nested pre-fling events are to nested fling events what touch intercept is to touch and what nested pre-scroll is to nested scroll. `dispatchNestedPreFling` offsets an opportunity for the parent view in a nested fling to fully consume the fling before the child view consumes it. If this method returns `true`, a nested parent view consumed the fling and this view should not scroll as a result.

For a better user experience, only one view in a nested scrolling chain should consume the fling at a time. If a parent view consumed the fling this method will return false. Custom view implementations should account for this in two ways:

- If a custom view is paged and needs to settle to a fixed page-point, do not call `dispatchNestedPreFling`; consume the fling and settle to a valid position regardless.
- If a nested parent does consume the fling, this view should not scroll at all, even to settle back to a valid idle position.

Views should also not offer fling velocities to nested parent views along an axis where scrolling is not currently supported; a `https://developer.android.com/reference/kotlin/android/widget/ScrollView.html#` should not offer a horizontal fling velocity to its parents since scrolling along that axis is not permitted and carrying velocity along that motion does not make sense.

| Parameters ||
|---|---|
| `velocityX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Horizontal fling velocity in pixels per second |
| `velocityY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Vertical fling velocity in pixels per second |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a nested scrolling parent consumed the fling |

### dispatchNestedPrePerformAccessibilityAction

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchNestedPrePerformAccessibilityAction(
    action: Int, 
    arguments: Bundle?
): Boolean
```

Report an accessibility action to this view's parents for delegated processing.

Implementations of performAccessibilityAction may internally call this method to delegate an accessibility action to a supporting parent. If the parent returns true from its onNestedPrePerformAccessibilityAction method this method will return true to signify that the action was consumed.

This method is useful for implementing nested scrolling child views. If isNestedScrollingEnabled returns true and the action is a scrolling action a custom view implementation may invoke this method to allow a parent to consume the scroll first. If this method returns true the custom view should skip its own scrolling behavior.

| Parameters ||
|---|---|
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Accessibility action to delegate |
| `arguments` | [Bundle](../android.os/Bundle.md)?: Optional action arguments. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the action was consumed by a parent |

### dispatchNestedPreScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchNestedPreScroll(
    dx: Int, 
    dy: Int, 
    consumed: IntArray?, 
    offsetInWindow: IntArray?
): Boolean
```

Dispatch one step of a nested scroll in progress before this view consumes any portion of it.

Nested pre-scroll events are to nested scroll events what touch intercept is to touch. `dispatchNestedPreScroll` offers an opportunity for the parent view in a nested scrolling operation to consume some or all of the scroll operation before the child view consumes it.

| Parameters ||
|---|---|
| `dx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Horizontal scroll distance in pixels |
| `dy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Vertical scroll distance in pixels |
| `consumed` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: Output. If not null, consumed\[0\] will contain the consumed component of dx and consumed\[1\] the consumed dy. |
| --- | --- |
| `offsetInWindow` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: Optional. If not null, on return this will contain the offset in local view coordinates of this view from before this operation to after it completes. View implementations may use this to adjust expected input coordinate tracking. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the parent consumed some or all of the scroll delta |

**See Also**

- dispatchNestedScroll

### dispatchNestedScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchNestedScroll(
    dxConsumed: Int, 
    dyConsumed: Int, 
    dxUnconsumed: Int, 
    dyUnconsumed: Int, 
    offsetInWindow: IntArray?
): Boolean
```

Dispatch one step of a nested scroll in progress.

Implementations of views that support nested scrolling should call this to report info about a scroll in progress to the current nested scrolling parent. If a nested scroll is not currently in progress or nested scrolling is not isNestedScrollingEnabled for this view this method does nothing.

Compatible View implementations should also call dispatchNestedPreScroll before consuming a component of the scroll event themselves.

| Parameters ||
|---|---|
| `dxConsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Horizontal distance in pixels consumed by this view during this scroll step |
| `dyConsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Vertical distance in pixels consumed by this view during this scroll step |
| `dxUnconsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Horizontal scroll distance in pixels not consumed by this view |
| --- | --- |
| `dyUnconsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Horizontal scroll distance in pixels not consumed by this view |
| `offsetInWindow` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: Optional. If not null, on return this will contain the offset in local view coordinates of this view from before this operation to after it completes. View implementations may use this to adjust expected input coordinate tracking. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the event was dispatched, false if it could not be dispatched. |

**See Also**

- dispatchNestedPreScroll

### dispatchPointerCaptureChanged

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchPointerCaptureChanged(hasCapture: Boolean): Unit
```
**See Also**

- onPointerCaptureChange

### dispatchPopulateAccessibilityEvent

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchPopulateAccessibilityEvent(event: AccessibilityEvent!): Boolean
```

Dispatches an AccessibilityEvent to the View to add the text content of the view and its children.

**Note:** This method should only be used with event.setText(). Avoid mutating other event state in this method. In general, put UI metadata in the node for services to easily query.

- If you are modifying other event properties, you may be eliminating semantics accessibility services may want. Instead, send a separate event using sendAccessibilityEvent and override onInitializeAccessibilityEvent.
- If you are checking for type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int` to generate window/title announcements, you may be causing disruptive announcements (or making no announcements at all). Instead, follow the practices described in announceForAccessibility. **Note:** this does not suggest calling announceForAccessibility(), but using the suggestions listed in its documentation.
- If you are making changes based on the state of accessibility, such as checking for an event type to trigger a UI update, while well-intentioned, you are creating brittle, less well-maintained code that works for some users but not others. Instead, leverage existing code for equitable experiences and less technical debt. See isEnabled for an example.

Note that the event text is populated in a separate dispatch path (onPopulateAccessibilityEvent) since we add to the event not only the text of the source but also the text of all its descendants.

A typical implementation will call onPopulateAccessibilityEvent on this view and then call the dispatchPopulateAccessibilityEvent on each child or the first child that is visible. Override this method if custom population of the event text content is required.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling setAccessibilityDelegate its dispatchPopulateAccessibilityEvent is responsible for handling this call.

If this view sets isAccessibilityDataSensitive then this view should only append sensitive information to an event that also sets isAccessibilityDataSensitive.

*Note:* Accessibility events of certain types are not dispatched for populating the event text via this method. For details refer to AccessibilityEvent.

| Parameters ||
|---|---|
| `event` | [AccessibilityEvent](../android.view.accessibility/AccessibilityEvent.md)!: The event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event population was completed. |

### dispatchProvideAutofillStructure

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchProvideAutofillStructure(
    structure: ViewStructure, 
    flags: Int
): Unit
```

Dispatches creation of a ViewStructures for autofill purposes down the hierarchy, when an Assist structure is being created as part of an autofill request.

The default implementation does the following:

- Sets the AutofillId in the structure.
- Calls onProvideAutofillStructure.
- Calls onProvideAutofillVirtualStructure.

Typically, this method should only be overridden by subclasses that provide a view hierarchy (such as ViewGroup) - other classes should override onProvideAutofillStructure or onProvideAutofillVirtualStructure instead.

When overridden, it must:

- Either call `super.dispatchProvideAutofillStructure(structure, flags)` or explicitly set the AutofillId in the structure (for example, by calling `structure.setAutofillId(getAutofillId())`).
- Decide how to handle the `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int` flag - when set, all views in the structure should be considered important for autofill, regardless of what isImportantForAutofill returns. We encourage you to respect this flag to provide a better user experience - this flag is typically used when an user explicitly requested autofill. If the flag is not set, then only views marked as important for autofill should be included in the structure - skipping non-important views optimizes the overall autofill performance.

| Parameters ||
|---|---|
| `structure` | [ViewStructure](ViewStructure.md): fill in with structured view data for autofill purposes. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): optional flags. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int`

### dispatchProvideStructure

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchProvideStructure(structure: ViewStructure!): Unit
```

Dispatch creation of ViewStructure down the hierarchy. The default implementation calls onProvideStructure and onProvideVirtualStructure.

### dispatchScrollCaptureSearch

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchScrollCaptureSearch(
    localVisibleRect: Rect, 
    windowOffset: Point, 
    targets: Consumer<ScrollCaptureTarget!>
): Unit
```

Dispatch a scroll capture search request down the view hierarchy.

| Parameters ||
|---|---|
| `localVisibleRect` | [Rect](../android.graphics/Rect.md): the visible area of this ViewGroup in local coordinates, according to the parent. This value cannot be `null`. |
| `windowOffset` | [Point](../android.graphics/Point.md): the offset of this view within the window. This value cannot be `null`. |
| `targets` | [Consumer](../java.util.function/Consumer.md)\< [ScrollCaptureTarget](ScrollCaptureTarget.md)!\>: accepts potential scroll capture targets; accept may be called zero or more times on the calling thread before onScrollCaptureSearch returns. This value cannot be `null`. |
| --- | --- |

### dispatchStartTemporaryDetach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchStartTemporaryDetach(): Unit
```

Dispatch onStartTemporaryDetach to this View and its direct children if this is a container View. 
If you override this method you *must* call through to the superclass implementation.

### dispatchSystemUiVisibilityChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchSystemUiVisibilityChanged(visibility: Int): Unit
```

**Deprecated:** *Use isVisible to find out about system bar visibilities by setting a `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener` on this view.*

Dispatch callbacks to setOnSystemUiVisibilityChangeListener down the view hierarchy.

### dispatchTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchTouchEvent(event: MotionEvent!): Boolean
```

Pass the touch screen motion event down to the target view, or this view if it is the target.

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The motion event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

**See Also**

- onTouchEvent

### dispatchTrackballEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchTrackballEvent(event: MotionEvent!): Boolean
```

Pass a trackball motion event down to the focused view.

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The motion event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

**See Also**

- onTrackballEvent

### dispatchUnhandledMove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchUnhandledMove(
    focused: View!, 
    direction: Int
): Boolean
```

This method is the last chance for the focused view and its ancestors to respond to an arrow key. This is called when the focused view did not consume the key internally, nor could the view system find a new view in the requested direction to give focus to.

| Parameters ||
|---|---|
| `focused` | [View](View.md)!: The currently focused view. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction focus wants to move. One of FOCUS_UP, FOCUS_DOWN, FOCUS_LEFT, and FOCUS_RIGHT. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the this view consumed this unhandled move. |

### dispatchWindowFocusChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchWindowFocusChanged(hasFocus: Boolean): Unit
```

Called when the window containing this view gains or loses window focus. ViewGroups should override to route to their children.

| Parameters ||
|---|---|
| `hasFocus` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the window containing this view now has focus, false otherwise. |

### dispatchWindowInsetsAnimationEnd

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchWindowInsetsAnimationEnd(animation: WindowInsetsAnimation): Unit
```

Dispatches onEnd when Window Insets animation ends.

| Parameters ||
|---|---|
| `animation` | [WindowInsetsAnimation](WindowInsetsAnimation.md): The current ongoing WindowInsetsAnimation. This value cannot be `null`. |

### dispatchWindowInsetsAnimationPrepare

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchWindowInsetsAnimationPrepare(animation: WindowInsetsAnimation): Unit
```

Dispatches onPrepare when Window Insets animation is being prepared.

| Parameters ||
|---|---|
| `animation` | [WindowInsetsAnimation](WindowInsetsAnimation.md): current animation. This value cannot be `null`. |

**See Also**

- onPrepare

### dispatchWindowInsetsAnimationProgress

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchWindowInsetsAnimationProgress(
    insets: WindowInsets, 
    runningAnimations: MutableList<WindowInsetsAnimation!>
): WindowInsets
```

Dispatches onProgress when Window Insets animation makes progress.

| Parameters ||
|---|---|
| `insets` | [WindowInsets](WindowInsets.md): The current WindowInsets. This value cannot be `null`. |
| `runningAnimations` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WindowInsetsAnimation](WindowInsetsAnimation.md)!\>: The currently running WindowInsetsAnimations. This value cannot be `null`. |

| Return ||
|---|---|
| WindowInsets | current WindowInsets. This value cannot be `null`. |

### dispatchWindowInsetsAnimationStart

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchWindowInsetsAnimationStart(
    animation: WindowInsetsAnimation, 
    bounds: WindowInsetsAnimation.Bounds
): WindowInsetsAnimation.Bounds
```

Dispatches onStart when Window Insets animation is started.

| Parameters ||
|---|---|
| `animation` | [WindowInsetsAnimation](WindowInsetsAnimation.md): current animation. This value cannot be `null`. |
| `bounds` | [WindowInsetsAnimation.Bounds](../android/view/WindowInsetsAnimation.Bounds.md): the upper and lower `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Bounds` that provides range of WindowInsetsAnimation. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Bounds` | the upper and lower `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Bounds`. This value cannot be `null`. |

### dispatchWindowSystemUiVisiblityChanged

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchWindowSystemUiVisiblityChanged(visible: Int): Unit
```

**Deprecated:** *SystemUiVisibility flags are deprecated. Use WindowInsetsController instead.*

Dispatch callbacks to onWindowSystemUiVisibilityChanged down the view hierarchy.

### dispatchWindowVisibilityChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchWindowVisibilityChanged(visibility: Int): Unit
```

Dispatch a window visibility change down the view hierarchy. ViewGroups should override to route to their children.

| Parameters ||
|---|---|
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new visibility of the window. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` |

**See Also**

- onWindowVisibilityChanged

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun draw(canvas: Canvas): Unit
```

Manually render this view (and all of its children) to the given Canvas. The view must have already done a full layout before this function is called. When implementing a view, implement onDraw instead of overriding this method. If you do need to override this method, call the superclass version. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `canvas` | [Canvas](../android.graphics/Canvas.md): The Canvas to which the View is rendered. This value cannot be `null`. |

### drawableHotspotChanged

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun drawableHotspotChanged(
    x: Float, 
    y: Float
): Unit
```

This function is called whenever the view hotspot changes and needs to be propagated to drawables or child views managed by the view.

Dispatching to child views is handled by dispatchDrawableHotspotChanged.

Be sure to call through to the superclass when overriding this function. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): hotspot x coordinate |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): hotspot y coordinate |

### findFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findFocus(): View!
```

Find the view in the hierarchy rooted at this view that currently has focus.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View#!` | The view that currently has focus, or null if no focused view can be found. |

### findOnBackInvokedDispatcher

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun findOnBackInvokedDispatcher(): OnBackInvokedDispatcher?
```

Walk up the View hierarchy to find the nearest `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#?` | The `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` from this or the nearest ancestor, or null if this view is both not attached and have no ancestor providing an `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#`. |

### findViewById

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : View!> findViewById(id: Int): T
```

Finds the first descendant view with the given ID, the view itself if the ID matches getId, or `null` if the ID is invalid (\< 0) or there is no matching view in the hierarchy.

**Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID to search for |

| Return ||
|---|---|
| `T` | a view with given ID if found, or `null` otherwise |

**See Also**

- requireViewById

### findViewWithTag

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : View!> findViewWithTag(tag: Any!): T
```

Look for a child view with the given tag. If this view has the given tag, return this view.

| Parameters ||
|---|---|
| `tag` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The tag to search for, using "tag.equals(getTag())". |

| Return ||
|---|---|
| `T` | The View that has the given tag in the hierarchy or null |

### findViewsWithText

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findViewsWithText(
    outViews: ArrayList<View!>!, 
    searched: CharSequence!, 
    flags: Int
): Unit
```

Finds the Views that contain given text. The containment is case insensitive. The search is performed by either the text that the View renders or the content description that describes the view for accessibility purposes and the view does not render or both. Clients can specify how the search is to be performed via passing the `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_TEXT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_CONTENT_DESCRIPTION:kotlin.Int` flags.

| Parameters ||
|---|---|
| `outViews` | [ArrayList](../java.util/ArrayList.md)\< [View](View.md)!\>!: The output list of matching Views. |
| `searched` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to match against. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_TEXT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_CONTENT_DESCRIPTION:kotlin.Int` |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_TEXT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_CONTENT_DESCRIPTION:kotlin.Int`
- setContentDescription

### focusSearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun focusSearch(direction: Int): View!
```

Find the nearest view in the specified direction that can take focus. This does not actually give focus to that view.

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of FOCUS_UP, FOCUS_DOWN, FOCUS_LEFT, and FOCUS_RIGHT. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View#!` | The nearest focusable in the specified direction, or null if none can be found. |

### forceHasOverlappingRendering

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun forceHasOverlappingRendering(hasOverlappingRendering: Boolean): Unit
```

Sets the behavior for overlapping rendering for this view (see hasOverlappingRendering for more details on this behavior). Calling this method is an alternative to overriding hasOverlappingRendering in a subclass, providing the value which is then used internally. That is, when forceHasOverlappingRendering is called, the value of hasOverlappingRendering is ignored and the value passed into this method is used instead.

| Parameters ||
|---|---|
| `hasOverlappingRendering` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The value for overlapping rendering to be used internally instead of that returned by hasOverlappingRendering. |

### forceLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun forceLayout(): Unit
```

Forces this view to be laid out during the next layout pass. This method does not call requestLayout() or forceLayout() on the parent.

### gatherTransparentRegion

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun gatherTransparentRegion(region: Region?): Boolean
```

This is used by the ViewRoot to perform an optimization when the view hierarchy contains one or several SurfaceView. SurfaceView is always considered transparent, but its children are not, therefore all View objects remove themselves from the global transparent region (passed as a parameter to this function).

| Parameters ||
|---|---|
| `region` | [Region](../android.graphics/Region.md)?: The transparent region for this ViewAncestor (window). This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the effective visibility of the view at this point is opaque, regardless of the transparent region; returns false if it is possible for underlying windows to be seen behind the view. |

### generateDisplayHash

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun generateDisplayHash(
    hashAlgorithm: String, 
    bounds: Rect?, 
    executor: Executor, 
    callback: DisplayHashResultCallback
): Unit
```

Called to generate a DisplayHash for this view.

| Parameters ||
|---|---|
| `hashAlgorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The hash algorithm to use when hashing the display. Must be one of the values returned from getSupportedHashAlgorithms This value cannot be `null`. |
| `bounds` | [Rect](../android.graphics/Rect.md)?: The bounds for the content within the View to generate the hash for. If bounds are null, the entire View's bounds will be used. If empty, it will invoke the callback onDisplayHashError with error `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashResultCallback#DISPLAY_HASH_ERROR_INVALID_BOUNDS:kotlin.Int` |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor that the callback should be invoked on. This value cannot be `null`. |
| --- | --- |
| `callback` | [DisplayHashResultCallback](../android.view.displayhash/DisplayHashResultCallback.md): The callback to handle the results of generating the display hash. This value cannot be `null`. |

### generateViewId

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun generateViewId(): Int
```

Generate a value suitable for use in setId. This value will not collide with ID values generated at build time by aapt for R.id.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a generated ID value |

### getAccessibilityClassName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccessibilityClassName(): CharSequence!
```

Return the class name of this object to be used for accessibility purposes. Subclasses should only override this if they are implementing something that should be seen as a completely new class of view when used by accessibility, unrelated to the class it is deriving from. This is used to fill in setClassName.

### getAccessibilityDelegate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccessibilityDelegate(): View.AccessibilityDelegate!
```

Returns the delegate for implementing accessibility support via composition. For more details see `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate!` | The delegate, or null if none set. |

### getAccessibilityLiveRegion

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccessibilityLiveRegion(): Int
```

Gets the live region mode for this View.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The live region mode for the view. |

**See Also**

- setAccessibilityLiveRegion

### getAccessibilityNodeProvider

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccessibilityNodeProvider(): AccessibilityNodeProvider!
```

Gets the provider for managing a virtual view hierarchy rooted at this View and reported to `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s that explore the window content.

If this method returns an instance, this instance is responsible for managing AccessibilityNodeInfos describing the virtual sub-tree rooted at this View including the one representing the View itself. Similarly the returned instance is responsible for performing accessibility actions on any virtual view or the root view itself.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling setAccessibilityDelegate its getAccessibilityNodeProvider is responsible for handling this call.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider!` | The provider. |

**See Also**

- AccessibilityNodeProvider

### getAccessibilityPaneTitle

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccessibilityPaneTitle(): CharSequence?
```

Get the title of the pane for purposes of accessibility.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The current pane title. This value may be `null`. |

**See Also**

- setAccessibilityPaneTitle

### getAccessibilityTraversalAfter

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccessibilityTraversalAfter(): Int
```

Gets the id of a view after which this one is visited in accessibility traversal.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The id of a view this one succeedes in accessibility traversal if specified, otherwise `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int`. |

**See Also**

- setAccessibilityTraversalAfter

### getAccessibilityTraversalBefore

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccessibilityTraversalBefore(): Int
```

Gets the id of a view before which this one is visited in accessibility traversal.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The id of a view this one precedes in accessibility traversal if specified, otherwise `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int`. |

**See Also**

- setAccessibilityTraversalBefore

### getAllowedHandwritingDelegatePackageName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllowedHandwritingDelegatePackageName(): String?
```

Returns the allowed package for delegate editor views for which this view may act as a handwriting delegator, as set by setAllowedHandwritingDelegatePackage. If setAllowedHandwritingDelegatePackage has not been called, or called with `null` argument, this will return `null`, meaning that this delegator view may only be used to initiate handwriting mode for a delegate editor view from the same package as this delegator view.

### getAllowedHandwritingDelegatorPackageName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllowedHandwritingDelegatorPackageName(): String?
```

Returns the allowed package for views which may act as a handwriting delegator for this delegate editor view, as set by setAllowedHandwritingDelegatorPackage. If setAllowedHandwritingDelegatorPackage has not been called, or called with `null` argument, this will return `null`, meaning that only views from the same package as this delegator editor view may act as a handwriting delegator.

### getAlpha

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAlpha(): Float
```

The opacity of the view. This is a value from 0 to 1, where 0 means the view is completely transparent and 1 means the view is completely opaque.

By default this is 1.0f.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The opacity of the view. |

### getAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAnimation(): Animation!
```

Get the animation currently associated with this view.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/Animation!` | The animation that is currently playing or scheduled to play for this view. |

### getAnimationMatrix

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAnimationMatrix(): Matrix?
```

Return the current transformation matrix of the view. This is used in animation frameworks, such as `https://developer.android.com/reference/kotlin/android/transition/Transition.html#`. Returns `null` when there is no transformation provided by setAnimationMatrix. Application developers should use transformation methods like setRotation, setScaleX, setScaleX, setTranslationX} and setTranslationY (float)}} instead.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#?` | the Matrix, null indicates there is no transformation |

**See Also**

- setAnimationMatrix

### getApplicationWindowToken

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationWindowToken(): IBinder!
```

Retrieve a unique token identifying the top-level "real" window of the window that this view is attached to. That is, this is like getWindowToken, except if the window this view in is a panel window (attached to another containing window), then the token of the containing window is returned instead.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/IBinder.html#!` | Returns the associated window token, either getWindowToken or the containing window's token. |

### getAttributeResolutionStack

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAttributeResolutionStack(attribute: Int): IntArray
```

Returns the ordered list of resource ID that are considered when resolving attribute values for this View. The list will include layout resource ID if the View is inflated from XML. It will also include a set of explicit styles if specified in XML using `style="..."`. Finally, it will include the default styles resolved from the theme.

**Note:** this method will only return actual values if the view attribute debugging is enabled in Android developer options.

| Parameters ||
|---|---|
| `attribute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Attribute resource ID for which the resolution stack should be returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | ordered list of resource ID that are considered when resolving attribute values for this View. This value cannot be `null`. |

### getAttributeSourceResourceMap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAttributeSourceResourceMap(): MutableMap<Int!, Int!>
```

Returns the mapping of attribute resource ID to source resource ID where the attribute value was set. Source resource ID can either be a layout resource ID, if the value was set in XML within the View tag, or a style resource ID, if the attribute was set in a style. The source resource value will be one of the resource IDs from getAttributeSourceResourceMap.

**Note:** this method will only return actual values if the view attribute debugging is enabled in Android developer options.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | mapping of attribute resource ID to source resource ID where the attribute value was set. This value cannot be `null`. |

### getAutofillHints

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAutofillHints(): Array<String!>?
```

Gets the hints that help an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` determine how to autofill the view with the user's data.

See setAutofillHints for more info about these hints.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | The hints set via the attribute or setAutofillHints, or `null` if no hints were set. |

### getAutofillId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAutofillId(): AutofillId!
```

Gets the unique, logical identifier of this view in the activity, for autofill purposes.

The autofill id is created on demand, unless it is explicitly set by setAutofillId.

See setAutofillId for more info.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId!` | The View's autofill id. |

### getAutofillType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAutofillType(): Int
```

Describes the autofill type of this view, so an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` can create the proper AutofillValue when autofilling the view.

By default returns `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_NONE:kotlin.Int`, but views should override it to properly support the Autofill Framework.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | either `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_TEXT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_LIST:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_DATE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_TOGGLE:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_TEXT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_TOGGLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_LIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_DATE:kotlin.Int` |

**See Also**

- onProvideAutofillStructure
- autofill

### getAutofillValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAutofillValue(): AutofillValue?
```

Gets the View's current autofill value.

By default returns `null`, but subclasses should override it and return an appropriate value to properly support the Autofill Framework.
**See Also**

- onProvideAutofillStructure
- autofill

### getBackground

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBackground(): Drawable!
```

Gets the background drawable

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | The drawable used as the background for this view, if any. |

**See Also**

- setBackground

### getBackgroundTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBackgroundTintBlendMode(): BlendMode?
```

Return the blending mode used to apply the tint to the background drawable, if specified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#?` | the blending mode used to apply the tint to the background drawable, null if no blend has previously been configured |

**See Also**

- setBackgroundTintBlendMode

### getBackgroundTintList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBackgroundTintList(): ColorStateList?
```

Return the tint applied to the background drawable, if specified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?` | the tint applied to the background drawable. This value may be `null`. |

**See Also**

- setBackgroundTintList

### getBackgroundTintMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBackgroundTintMode(): PorterDuff.Mode?
```

Return the blending mode used to apply the tint to the background drawable, if specified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#?` | the blending mode used to apply the tint to the background drawable. This value may be `null`. |

**See Also**

- setBackgroundTintBlendMode

### getBaseline

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBaseline(): Int
```

Return the offset of the widget's text baseline from the widget's top boundary. If this widget does not support baseline alignment, this method returns -1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the offset of the baseline within the widget's bounds or -1 if baseline alignment is not supported |

### getBottom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBottom(): Int
```

Bottom position of this view relative to its parent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The bottom of this view, in pixels. |

### getCameraDistance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCameraDistance(): Float
```

Gets the distance along the Z axis from the camera to this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The distance along the Z axis. |

**See Also**

- setCameraDistance

### getClipBounds

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClipBounds(): Rect!
```

Returns a copy of the current setClipBounds.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!` | A copy of the current clip bounds if clip bounds are set, otherwise null. |

### getClipBounds

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClipBounds(outRect: Rect!): Boolean
```

Populates an output rectangle with the clip bounds of the view, returning `true` if successful or `false` if the view's clip bounds are `null`.

| Parameters ||
|---|---|
| `outRect` | [Rect](../android.graphics/Rect.md)!: rectangle in which to place the clip bounds of the view |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful or `false` if the view's clip bounds are `null` |

### getClipToOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getClipToOutline(): Boolean
```

Returns whether the Outline should be used to clip the contents of the View.

Note that this flag will only be respected if the View's Outline returns true from canClip.
**See Also**

- setOutlineProvider
- setClipToOutline

### getContentCaptureSession

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContentCaptureSession(): ContentCaptureSession?
```

Gets the session used to notify content capture events.

| Return ||
|---|---|
| ContentCaptureSession | session explicitly set by setContentCaptureSession, inherited by ancestors, default session or `null` if content capture is disabled for this view. |

### getContentDescription

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContentDescription(): CharSequence!
```

Returns the View's content description.

**Note:** Do not override this method, as it will have no effect on the content description presented to accessibility services. You must call setContentDescription to modify the content description.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | the content description |

**See Also**

- setContentDescription

### getContentSensitivity

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContentSensitivity(): Int
```

Gets content sensitivity mode to determine whether this view displays sensitive content.

See setContentSensitivity and isContentSensitive for more info about this mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_AUTO:kotlin.Int` by default, or value passed to setContentSensitivity. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_SENSITIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_NOT_SENSITIVE:kotlin.Int` |

### getContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContext(): Context!
```

Returns the context the view is running in, through which it can access the current theme, resources, etc.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | The view's Context. |

### getDefaultFocusHighlightEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDefaultFocusHighlightEnabled(): Boolean
```

Returns whether this View should use a default focus highlight when it gets focused but doesn't have `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` defined in its background.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this View should use a default focus highlight. |

### getDefaultSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDefaultSize(
    size: Int, 
    measureSpec: Int
): Int
```

Utility to return a default size. Uses the supplied size if the MeasureSpec imposed no constraints. Will get larger if allowed by the MeasureSpec.

| Parameters ||
|---|---|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Default size for this view |
| `measureSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Constraints imposed by the parent |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The size this view should be. |

### getDisplay

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplay(): Display!
```

Gets the logical display to which the view's window has been attached.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Display!` | The logical display, or null if the view is not currently attached to a window. |

### getDrawableState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDrawableState(): IntArray!
```

Return an array of resource IDs of the drawable states representing the current state of the view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | The current drawable state |

**See Also**

- setState
- drawableStateChanged
- onCreateDrawableState

### getDrawingCache

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawingCache(): Bitmap!
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Calling this method is equivalent to calling `getDrawingCache(false)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!` | A non-scaled bitmap representing this view or null if cache is disabled. |

**See Also**

- getDrawingCache

### getDrawingCache

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawingCache(autoScale: Boolean): Bitmap!
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Returns the bitmap in which this view drawing is cached. The returned bitmap is null when caching is disabled. If caching is enabled and the cache is not ready, this method will create it. Calling draw will not draw from the cache when the cache is enabled. To benefit from the cache, you must request the drawing cache by calling this method and draw it on screen if the returned bitmap is not null.

Note about auto scaling in compatibility mode: When auto scaling is not enabled, this method will create a bitmap of the same size as this view. Because this bitmap will be drawn scaled by the parent ViewGroup, the result on screen might show scaling artifacts. To avoid such artifacts, you should call this method by setting the auto scaling to true. Doing so, however, will generate a bitmap of a different size than the view. This implies that your application must be able to handle this size.

| Parameters ||
|---|---|
| `autoScale` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Indicates whether the generated bitmap should be scaled based on the current density of the screen when the application is in compatibility mode. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!` | A bitmap representing this view or null if cache is disabled. |

**See Also**

- setDrawingCacheEnabled
- isDrawingCacheEnabled
- buildDrawingCache
- destroyDrawingCache

### getDrawingCacheBackgroundColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawingCacheBackgroundColor(): Int
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The background color to used for the drawing cache's bitmap |

**See Also**

- setDrawingCacheBackgroundColor

### getDrawingCacheQuality

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawingCacheQuality(): Int
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Returns the quality of the drawing cache.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | One of `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_LOW:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_HIGH:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_HIGH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_AUTO:kotlin.Int` |

**See Also**

- setDrawingCacheQuality
- setDrawingCacheEnabled
- isDrawingCacheEnabled

### getDrawingRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawingRect(outRect: Rect!): Unit
```

Return the visible drawing bounds of your view. Fills in the output rectangle with the values from getScrollX(), getScrollY(), getWidth(), and getHeight(). These bounds do not account for any transformation properties currently set on the view, such as setScaleX or setRotation.

| Parameters ||
|---|---|
| `outRect` | [Rect](../android.graphics/Rect.md)!: The (scrolled) drawing bounds of the view. |

### getDrawingTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawingTime(): Long
```

Return the time at which the drawing of the view hierarchy started.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the drawing start time in milliseconds |

### getElevation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getElevation(): Float
```

The base elevation of this view relative to its parent, in pixels.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The base depth position of the view, in pixels. |

### getExplicitStyle

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExplicitStyle(): Int
```

Returns the resource ID for the style specified using `style="..."` in the `https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#`'s backing XML element or `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int` otherwise if not specified or otherwise not applicable.

Each View can have an explicit style specified in the layout file. This style is used first during the View attribute resolution, then if an attribute is not defined there the resource system looks at default style and theme as fallbacks.

**Note:** this method will only return actual values if the view attribute debugging is enabled in Android developer options.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The resource ID for the style specified using `style="..."` in the `https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#`'s backing XML element or `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int` otherwise if not specified or otherwise not applicable. |

### getFilterTouchesWhenObscured

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFilterTouchesWhenObscured(): Boolean
```

Gets whether the framework should discard touches when the view's window is obscured by another visible window at the touched location. Refer to the View security documentation for more details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if touch filtering is enabled. |

**See Also**

- setFilterTouchesWhenObscured

### getFitsSystemWindows

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFitsSystemWindows(): Boolean
```

Check for state of setFitsSystemWindows. If this method returns `true`, the default implementation of fitSystemWindows will be executed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the default implementation of fitSystemWindows will be executed. |

**See Also**

- setFitsSystemWindows
- fitSystemWindows
- setSystemUiVisibility

### getFocusable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFocusable(): Int
```

Returns the focusable setting for this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | One of `https://developer.android.com/reference/kotlin/android/view/View#NOT_FOCUSABLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE_AUTO:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#NOT_FOCUSABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE_AUTO:kotlin.Int` |

### getFocusables

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFocusables(direction: Int): ArrayList<View!>!
```

Find and return all focusable views that are descendants of this view, possibly including this view if it is focusable itself.

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction of the focus. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/view/View#!>!` | A list of focusable views |

### getFocusedRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFocusedRect(r: Rect!): Unit
```

When a view has focus and the user navigates away from it, the next view is searched for starting from the rectangle filled in by this method. By default, the rectangle is the getDrawingRect) of the view. However, if your view maintains some idea of internal selection, such as a cursor, or a selected row or column, you should override this method and fill in a more specific rectangle.

| Parameters ||
|---|---|
| `r` | [Rect](../android.graphics/Rect.md)!: The rectangle to fill in, in this view's coordinates. |

### getForeground

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getForeground(): Drawable!
```

Returns the drawable used as the foreground of this View. The foreground drawable, if non-null, is always drawn on top of the view's content.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | a Drawable or null if no foreground was set |

**See Also**

- onDrawForeground

### getForegroundGravity

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getForegroundGravity(): Int
```

Describes how the foreground is positioned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | foreground gravity. |

**See Also**

- setForegroundGravity

### getForegroundTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getForegroundTintBlendMode(): BlendMode?
```

Return the blending mode used to apply the tint to the foreground drawable, if specified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#?` | the blending mode used to apply the tint to the foreground drawable. This value may be `null`. |

**See Also**

- setForegroundTintBlendMode

### getForegroundTintList

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getForegroundTintList(): ColorStateList?
```

Return the tint applied to the foreground drawable, if specified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?` | the tint applied to the foreground drawable. This value may be `null`. |

**See Also**

- setForegroundTintList

### getForegroundTintMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getForegroundTintMode(): PorterDuff.Mode?
```

Return the blending mode used to apply the tint to the foreground drawable, if specified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#?` | the blending mode used to apply the tint to the foreground drawable. This value may be `null`. |

**See Also**

- setForegroundTintMode

### getFrameContentVelocity

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFrameContentVelocity(): Float
```

Get the current velocity of the View. The value should always be greater than or equal to 0. Note that this is only valid till the next drawn frame.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | 0 by default, or value passed to setFrameContentVelocity. |

### getGlobalVisibleRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGlobalVisibleRect(r: Rect!): Boolean
```

Sets `r` to the coordinates of the non-clipped area of this view in the coordinate space of the view's root view.

See getGlobalVisibleRect for more information.

| Parameters ||
|---|---|
| `r` | [Rect](../android.graphics/Rect.md)!: If the method returns true, contains the coordinates of the visible portion of this view in the coordinate space of the view's root view. If the method returns false, the contents of `r` are undefined. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if at least part of the view is visible within the root view; otherwise false. |

### getGlobalVisibleRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGlobalVisibleRect(
    r: Rect!, 
    globalOffset: Point!
): Boolean
```

Sets `r` to the coordinates of the non-clipped area of this view in the coordinate space of the view's root view. Sets `globalOffset` to the offset of the view's x and y coordinates from the coordinate space origin, which is the top left corner of the root view irrespective of screen decorations and system UI elements.

To convert `r` to coordinates relative to the top left corner of this view (without taking view rotations into account), offset `r` by the inverse values of `globalOffset`---`r.offset(-globalOffset.x, -globalOffset.y)`---which is equivalent to calling getLocalVisibleRect.

**Note:** Do not use this method to determine the size of a window in multi-window mode; use getCurrentWindowMetrics.

| Parameters ||
|---|---|
| `r` | [Rect](../android.graphics/Rect.md)!: If the method returns true, contains the coordinates of the visible portion of this view in the coordinate space of the view's root view. If the method returns false, the contents of `r` are undefined. |
| `globalOffset` | [Point](../android.graphics/Point.md)!: If the method returns true, contains the offset of the x and y coordinates of this view from the top left corner of the view's root view. If the method returns false, the contents of `globalOffset` are undefined. The argument can be null (see getGlobalVisibleRect. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if at least part of the view is visible within the root view; false if the view is completely clipped or translated out of the visible area of the root view. |

**See Also**

- getLocalVisibleRect

### getHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHandler(): Handler!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Handler.html#!` | A handler associated with the thread running the View. This handler can be used to pump events in the UI events queue. |

### getHandwritingBoundsOffsetBottom

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHandwritingBoundsOffsetBottom(): Float
```

Return the amount of offset applied to the bottom edge of this view's handwriting bounds, in the unit of pixel.
**See Also**

- setAutoHandwritingEnabled
- setHandwritingBoundsOffsets

### getHandwritingBoundsOffsetLeft

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHandwritingBoundsOffsetLeft(): Float
```

Return the amount of offset applied to the left edge of this view's handwriting bounds, in the unit of pixel.
**See Also**

- setAutoHandwritingEnabled
- setHandwritingBoundsOffsets

### getHandwritingBoundsOffsetRight

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHandwritingBoundsOffsetRight(): Float
```

Return the amount of offset applied to the right edge of this view's handwriting bounds, in the unit of pixel.
**See Also**

- setAutoHandwritingEnabled
- setHandwritingBoundsOffsets

### getHandwritingBoundsOffsetTop

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHandwritingBoundsOffsetTop(): Float
```

Return the amount of offset applied to the top edge of this view's handwriting bounds, in the unit of pixel.
**See Also**

- setAutoHandwritingEnabled
- setHandwritingBoundsOffsets

### getHandwritingDelegateFlags

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHandwritingDelegateFlags(): Int
```

Returns flags configuring the handwriting delegation behavior for this delegate editor view, as set by setHandwritingDelegateFlags.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HANDWRITING_DELEGATE_FLAG_HOME_DELEGATOR_ALLOWED:kotlin.Int` |

### getHandwritingDelegatorCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHandwritingDelegatorCallback(): Runnable?
```

Returns the callback set by setHandwritingDelegatorCallback which should be called when a stylus MotionEvent occurs within this view's bounds. The callback should only be called from the UI thread.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Runnable.html#?` | This value may be `null`. |

### getHasOverlappingRendering

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHasOverlappingRendering(): Boolean
```

Returns the value for overlapping rendering that is used internally. This is either the value passed into forceHasOverlappingRendering, if called, or the return value of hasOverlappingRendering, otherwise.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The value for overlapping rendering being used internally. |

### getHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHeight(): Int
```

Return the height of your view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The height of your view, in pixels. |

### getHitRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHitRect(outRect: Rect!): Unit
```

Hit rectangle in parent's coordinates

| Parameters ||
|---|---|
| `outRect` | [Rect](../android.graphics/Rect.md)!: The hit rectangle of the view. |

### getHorizontalFadingEdgeLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHorizontalFadingEdgeLength(): Int
```

Returns the size of the horizontal faded edges used to indicate that more content in this view is visible.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The size in pixels of the horizontal faded edge or 0 if horizontal faded edges are not enabled for this view. |

### getHorizontalScrollbarThumbDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHorizontalScrollbarThumbDrawable(): Drawable?
```

Returns the currently configured Drawable for the thumb of the horizontal scroll bar if it exists, null otherwise.
**See Also**

- awakenScrollBars
- isHorizontalScrollBarEnabled
- setHorizontalScrollBarEnabled

### getHorizontalScrollbarTrackDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHorizontalScrollbarTrackDrawable(): Drawable?
```

Returns the currently configured Drawable for the track of the horizontal scroll bar if it exists, null otherwise.
**See Also**

- awakenScrollBars
- isHorizontalScrollBarEnabled
- setHorizontalScrollBarEnabled

### getId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getId(): Int
```

Returns this view's identifier.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a positive integer used to identify the view or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the view has no ID |

**See Also**

- setId
- findViewById

### getImportantForAccessibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getImportantForAccessibility(): Int
```

Gets the mode for determining whether this View is important for accessibility. A view is important for accessibility if it fires accessibility events and if it is reported to accessibility services that query the screen.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The mode for determining whether a view is important for accessibility, one of `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_YES:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_YES:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_AUTO:kotlin.Int`

### getImportantForAutofill

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getImportantForAutofill(): Int
```

Gets the mode for determining whether this view is important for autofill.

See setImportantForAutofill and isImportantForAutofill for more info about this mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int` by default, or value passed to setImportantForAutofill. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int` |

### getImportantForContentCapture

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getImportantForContentCapture(): Int
```

Gets the mode for determining whether this view is important for content capture.

See setImportantForContentCapture and isImportantForContentCapture for more info about this mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_AUTO:kotlin.Int` by default, or value passed to setImportantForContentCapture. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES_EXCLUDE_DESCENDANTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO_EXCLUDE_DESCENDANTS:kotlin.Int` |

### getKeepScreenOn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getKeepScreenOn(): Boolean
```

Returns whether the screen should remain on, corresponding to the current value of `https://developer.android.com/reference/kotlin/android/view/View#KEEP_SCREEN_ON:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if `https://developer.android.com/reference/kotlin/android/view/View#KEEP_SCREEN_ON:kotlin.Int` is set. |

**See Also**

- setKeepScreenOn

### getKeyDispatcherState

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getKeyDispatcherState(): KeyEvent.DispatcherState!
```

Return the global `https://developer.android.com/reference/kotlin/android/view/KeyEvent.DispatcherState` for this view's window. Returns null if the view is not currently attached to the window. Normally you will not need to use this directly, but just use the standard high-level event callbacks like onKeyDown.

### getLabelFor

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLabelFor(): Int
```

Gets the id of a view for which this view serves as a label for accessibility purposes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The labeled view id. |

### getLayerType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayerType(): Int
```

Indicates what type of layer is currently associated with this view. By default a view does not have a layer, and the layer type is `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`. Refer to the documentation of setLayerType for more information on the different types of layers.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int` |

**See Also**

- setLayerType
- buildLayer
- `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int`

### getLayoutDirection

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayoutDirection(): Int
```

Returns the resolved layout direction for this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_RTL:kotlin.Int` if the layout direction is RTL or returns `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LTR:kotlin.Int` if the layout direction is not RTL. For compatibility, this will return `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LTR:kotlin.Int` if API version is lower than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LTR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_RTL:kotlin.Int` |

### getLayoutParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayoutParams(): ViewGroup.LayoutParams!
```

Get the LayoutParams associated with this view. All views should have layout parameters. These supply parameters to the *parent* of this view specifying how it should be arranged. There are many subclasses of ViewGroup.LayoutParams, and these correspond to the different subclasses of ViewGroup that are responsible for arranging their children. This method may return null if this View is not attached to a parent ViewGroup or setLayoutParams was not invoked successfully. When a View is attached to a parent ViewGroup, this method must not return null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!` | The LayoutParams associated with this view, or null if no parameters have been set yet |

### getLeft

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLeft(): Int
```

Left position of this view relative to its parent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The left edge of this view, in pixels. |

### getLocalVisibleRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLocalVisibleRect(r: Rect!): Boolean
```

Sets `r` to the coordinates of the non-clipped area of this view relative to the top left corner of the view.

If the view is clipped on the left or top, the left and top coordinates are offset from 0 by the clipped amount. For example, if the view is off screen 50px on the left and 30px at the top, the left and top coordinates are 50 and 30 respectively.

If the view is clipped on the right or bottom, the right and bottom coordinates are reduced by the clipped amount. For example, if the view is off screen 40px on the right and 20px at the bottom, the right coordinate is the view width - 40, and the bottom coordinate is the view height - 20.

| Parameters ||
|---|---|
| `r` | [Rect](../android.graphics/Rect.md)!: If the method returns true, contains the coordinates of the visible portion of this view relative to the top left corner of the view. If the method returns false, the contents of `r` are undefined. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if at least part of the view is visible; false if the view is completely clipped or translated out of the visible area. |

**See Also**

- getGlobalVisibleRect

### getLocationInSurface

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocationInSurface(location: IntArray): Unit
```

Gets the coordinates of this view in the coordinate space of the Surface that contains the view.

In multiple-screen scenarios, if the surface spans multiple screens, the coordinate space of the surface also spans multiple screens.

After the method returns, the argument array contains the x and y coordinates of the view relative to the view's left and top edges, respectively.

| Parameters ||
|---|---|
| `location` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): A two-element integer array in which the view coordinates are stored. The x-coordinate is at index 0; the y-coordinate, at index 1. This value cannot be `null`. |

### getLocationInWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocationInWindow(outLocation: IntArray!): Unit
```

Gets the coordinates of this view in the coordinate space of the window that contains the view, irrespective of system decorations.

In multi-window mode, the origin of the coordinate space is the top left corner of the window that contains the view. In full screen mode, the origin is the top left corner of the device screen.

In multiple-screen scenarios, if the app spans multiple screens, the coordinate space also spans multiple screens. But if the app is restricted to a single screen, the coordinate space includes only the screen on which the app is running.

After the method returns, the argument array contains the x and y coordinates of the view relative to the view's left and top edges, respectively.

| Parameters ||
|---|---|
| `outLocation` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: A two-element integer array in which the view coordinates are stored. The x-coordinate is at index 0; the y-coordinate, at index 1. |

### getLocationOnScreen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocationOnScreen(outLocation: IntArray!): Unit
```

Gets the coordinates of this view in the coordinate space of the device screen, irrespective of system decorations and whether the system is in multi-window mode.

In multi-window mode, the coordinate space encompasses the entire device screen, ignoring the bounds of the app window. For example, if the view is in the bottom portion of a horizontal split screen, the top edge of the screen---not the top edge of the window---is the origin from which the y-coordinate is calculated.

In multiple-screen scenarios, the coordinate space can span screens. For example, if the app is spanning both screens of a dual-screen device and the view is located on the right-hand screen, the x-coordinate is calculated from the left edge of the left-hand screen to the left edge of the view. When the app is restricted to a single screen in a multiple-screen environment, the coordinate space includes only the screen on which the app is running.

After the method returns, the argument array contains the x and y coordinates of the view relative to the view's left and top edges, respectively.

| Parameters ||
|---|---|
| `outLocation` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: A two-element integer array in which the view coordinates are stored. The x-coordinate is at index 0; the y-coordinate, at index 1. |

### getMatrix

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMatrix(): Matrix!
```

The transform matrix of this view, which is calculated based on the current rotation, scale, and pivot properties.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#!` | The current transform matrix for the view |

**See Also**

- getRotation
- getScaleX
- getScaleY
- getPivotX
- getPivotY

### getMeasuredHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMeasuredHeight(): Int
```

Like getMeasuredHeightAndState, but only returns the raw height component (that is the result is masked by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int`).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The raw measured height of this view. |

### getMeasuredHeightAndState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMeasuredHeightAndState(): Int
```

Return the full height measurement information for this view as computed by the most recent call to measure. This result is a bit mask as defined by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_TOO_SMALL:kotlin.Int`. This should be used during measurement and layout calculations only. Use getHeight to see how high a view is after layout.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The measured height of this view as a bit mask. |

### getMeasuredState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMeasuredState(): Int
```

Return only the state bits of getMeasuredWidthAndState and getMeasuredHeightAndState, combined into one integer. The width component is in the regular bits `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_MASK:kotlin.Int` and the height component is at the shifted bits `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_HEIGHT_STATE_SHIFT:kotlin.Int`\>\>`https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_MASK:kotlin.Int`.

### getMeasuredWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMeasuredWidth(): Int
```

Like getMeasuredWidthAndState, but only returns the raw width component (that is the result is masked by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int`).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The raw measured width of this view. |

### getMeasuredWidthAndState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMeasuredWidthAndState(): Int
```

Return the full width measurement information for this view as computed by the most recent call to measure. This result is a bit mask as defined by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_TOO_SMALL:kotlin.Int`. This should be used during measurement and layout calculations only. Use getWidth to see how wide a view is after layout.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The measured width of this view as a bit mask. |

### getMinimumHeight

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinimumHeight(): Int
```

Returns the minimum height of the view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minimum height the view will try to be, in pixels |

**See Also**

- setMinimumHeight

### getMinimumWidth

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinimumWidth(): Int
```

Returns the minimum width of the view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minimum width the view will try to be, in pixels |

**See Also**

- setMinimumWidth

### getNextClusterForwardId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNextClusterForwardId(): Int
```

Gets the id of the root of the next keyboard navigation cluster.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The next keyboard navigation cluster ID, or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the framework should decide automatically. |

### getNextFocusDownId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNextFocusDownId(): Int
```

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The next focus ID, or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the framework should decide automatically. |

### getNextFocusForwardId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNextFocusForwardId(): Int
```

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The next focus ID, or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the framework should decide automatically. |

### getNextFocusLeftId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNextFocusLeftId(): Int
```

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The next focus ID, or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the framework should decide automatically. |

### getNextFocusRightId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNextFocusRightId(): Int
```

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The next focus ID, or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the framework should decide automatically. |

### getNextFocusUpId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNextFocusUpId(): Int
```

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The next focus ID, or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the framework should decide automatically. |

### getOnFocusChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOnFocusChangeListener(): View.OnFocusChangeListener!
```

Returns the focus-change callback registered for this view.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.OnFocusChangeListener!` | The callback, or null if one is not registered. |

### getOutlineAmbientShadowColor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOutlineAmbientShadowColor(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The shadow color set by setOutlineAmbientShadowColor, or black if nothing was set |

### getOutlineProvider

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOutlineProvider(): ViewOutlineProvider!
```

Returns the current ViewOutlineProvider of the view, which generates the Outline that defines the shape of the shadow it casts, and enables outline clipping.
**See Also**

- setOutlineProvider

### getOutlineSpotShadowColor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOutlineSpotShadowColor(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The shadow color set by setOutlineSpotShadowColor, or black if nothing was set |

### getOverScrollMode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOverScrollMode(): Int
```

Returns the over-scroll mode for this view. The result will be one of `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_ALWAYS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_IF_CONTENT_SCROLLS:kotlin.Int` (allow over-scrolling only if the view content is larger than the container), or `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_NEVER:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | This view's over-scroll mode. |

### getOverlay

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOverlay(): ViewOverlay!
```

Returns the overlay for this view, creating it if it does not yet exist. Adding drawables to the overlay will cause them to be displayed whenever the view itself is redrawn. Objects in the overlay should be actively managed: remove them when they should not be displayed anymore. The overlay will always have the same size as its host view.

Note: Overlays do not currently work correctly with SurfaceView or TextureView; contents in overlays for these types of views may not display correctly.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewOverlay!` | The ViewOverlay object for this view. |

**See Also**

- ViewOverlay

### getPaddingBottom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPaddingBottom(): Int
```

Returns the bottom padding of this view. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the bottom padding in pixels |

### getPaddingEnd

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPaddingEnd(): Int
```

Returns the end padding of this view depending on its resolved layout direction. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the end padding in pixels |

### getPaddingLeft

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPaddingLeft(): Int
```

Returns the left padding of this view. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the left padding in pixels |

### getPaddingRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPaddingRight(): Int
```

Returns the right padding of this view. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the right padding in pixels |

### getPaddingStart

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPaddingStart(): Int
```

Returns the start padding of this view depending on its resolved layout direction. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the start padding in pixels |

### getPaddingTop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPaddingTop(): Int
```

Returns the top padding of this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the top padding in pixels |

### getParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParent(): ViewParent!
```

Gets the parent of this view. Note that the parent is a ViewParent and not necessarily a View.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewParent!` | Parent of this view. |

### getParentForAccessibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParentForAccessibility(): ViewParent!
```

Gets the parent for accessibility purposes. Note that the parent for accessibility is not necessary the immediate parent. It is the first predecessor that is important for accessibility.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewParent!` | The parent for accessibility purposes. |

### getPendingCredentialCallback

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPendingCredentialCallback(): OutcomeReceiver<GetCredentialResponse!, GetCredentialException!>?
```

Returns the callback that has previously been set up on this view through the setPendingCredentialRequest API. If the return value is null, that means no callback, or request, has been set on the view and no `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` flow will be invoked when this view is focused. Traditioanl autofill flows will still work, and autofillable content will still be returned through the autofill )} API.

See setPendingCredentialRequest for more info.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse.html#!, https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException.html#!>?` | The callback associated with this view that will be invoked on a response from `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` . |

### getPendingCredentialRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPendingCredentialRequest(): GetCredentialRequest?
```

Returns the `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#` associated with the view. If the return value is null, that means no request has been set on the view and no `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` flow will be invoked when this view is focused. Traditioanl autofill flows will still work, autofilling content if applicable, from the active `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` on the device.

See setPendingCredentialRequest for more info.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#?` | The credential request associated with this View. |

### getPivotX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPivotX(): Float
```

The x location of the point around which the view is setRotation and setScaleX.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The x location of the pivot point. |

**See Also**

- getRotation
- getScaleX
- getScaleY
- getPivotY

### getPivotY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPivotY(): Float
```

The y location of the point around which the view is setRotation and setScaleY.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The y location of the pivot point. |

**See Also**

- getRotation
- getScaleX
- getScaleY
- getPivotY

### getPointerIcon

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPointerIcon(): PointerIcon!
```

Gets the mouse pointer icon for the current view.
**See Also**

- setPointerIcon

### getPreferKeepClearRects

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPreferKeepClearRects(): MutableList<Rect!>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!>` | the list of rects, set by setPreferKeepClearRects. This value cannot be `null`. |

**See Also**

- setPreferKeepClearRects

### getReceiveContentMimeTypes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReceiveContentMimeTypes(): Array<String!>?
```

Returns the MIME types accepted by performReceiveContent for this view, as configured via setOnReceiveContentListener. By default returns null.

Different features (e.g. pasting from the clipboard, inserting stickers from the soft keyboard, etc) may optionally use this metadata to conditionally alter their behavior. For example, a soft keyboard may choose to hide its UI for inserting GIFs for a particular input field if the MIME types returned here for that field don't include "image/gif" or "image/\*".

Note: Comparisons of MIME types should be performed using utilities such as compareMimeTypes rather than simple string equality, in order to correctly handle patterns such as "text/\*", "image/\*", etc. Note that MIME type matching in the Android framework is case-sensitive, unlike formal RFC MIME types. As a result, you should always write your MIME types with lowercase letters, or use normalizeMimeType to ensure that it is converted to lowercase.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | The MIME types accepted by performReceiveContent for this view (may include patterns such as "image/\*"). |

### getRequestedFrameRate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRequestedFrameRate(): Float
```

Get the current preferred frame rate of the View. The value could be negative when preferred frame rate category is set instead of perferred frame rate. The frame rate category includes REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE, REQUESTED_FRAME_RATE_CATEGORY_LOW, REQUESTED_FRAME_RATE_CATEGORY_NORMAL, and REQUESTED_FRAME_RATE_CATEGORY_HIGH. Note that the frame rate value is valid as long as the View is invalidated. Please also be aware that the requested frame rate will not propagate to child views when this API is used on a ViewGroup.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | REQUESTED_FRAME_RATE_CATEGORY_DEFAULT by default, or value passed to setRequestedFrameRate. |

### getResources

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResources(): Resources!
```

Returns the resources associated with this view.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!` | Resources object. |

### getRevealOnFocusHint

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRevealOnFocusHint(): Boolean
```

Returns this view's preference for reveal behavior when it gains focus.

When this method returns true for a child view requesting focus, ancestor views responding to a focus change in requestChildFocus should make a best effort to make the newly focused child fully visible to the user. When it returns false, ancestor views should preferably not disrupt scroll positioning or other properties affecting visibility to the user as part of the focus change.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this view would prefer to become fully visible when it gains focus, false if it would prefer not to disrupt scroll positioning |

**See Also**

- setRevealOnFocusHint

### getRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRight(): Int
```

Right position of this view relative to its parent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The right edge of this view, in pixels. |

### getRootSurfaceControl

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRootSurfaceControl(): AttachedSurfaceControl?
```

The AttachedSurfaceControl itself is not a View, it is just the interface to the windowing-system object that contains the entire view hierarchy. For the root View of a given hierarchy see getRootView.

| Return ||
|---|---|
| AttachedSurfaceControl | The AttachedSurfaceControl interface for this View. This will only return a non-null value when called between onAttachedToWindow and onDetachedFromWindow. |

### getRootView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRootView(): View!
```

Finds the topmost view in the current view hierarchy.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View#!` | the topmost view containing this view |

### getRootWindowInsets

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRootWindowInsets(): WindowInsets!
```

Provide original WindowInsets that are dispatched to the view hierarchy. The insets are only available if the view is attached.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/WindowInsets!` | WindowInsets from the top of the view hierarchy or null if View is detached |

### getRotation

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRotation(): Float
```

The degrees that the view is rotated around the pivot point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The degrees of rotation. |

**See Also**

- setRotation
- getPivotX
- getPivotY

### getRotationX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRotationX(): Float
```

The degrees that the view is rotated around the horizontal axis through the pivot point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The degrees of X rotation. |

**See Also**

- getPivotX
- getPivotY
- setRotationX

### getRotationY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRotationY(): Float
```

The degrees that the view is rotated around the vertical axis through the pivot point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The degrees of Y rotation. |

**See Also**

- getPivotX
- getPivotY
- setRotationY

### getScaleX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getScaleX(): Float
```

The amount that the view is scaled in x around the pivot point, as a proportion of the view's unscaled width. A value of 1, the default, means that no scaling is applied.

By default, this is 1.0f.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The scaling factor. |

**See Also**

- getPivotX
- getPivotY

### getScaleY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getScaleY(): Float
```

The amount that the view is scaled in y around the pivot point, as a proportion of the view's unscaled height. A value of 1, the default, means that no scaling is applied.

By default, this is 1.0f.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The scaling factor. |

**See Also**

- getPivotX
- getPivotY

### getScrollBarDefaultDelayBeforeFade

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getScrollBarDefaultDelayBeforeFade(): Int
```

Returns the delay before scrollbars fade.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the delay before scrollbars fade |

### getScrollBarFadeDuration

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getScrollBarFadeDuration(): Int
```

Returns the scrollbar fade duration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the scrollbar fade duration, in milliseconds |

### getScrollBarSize

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getScrollBarSize(): Int
```

Returns the scrollbar size.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the scrollbar size |

### getScrollBarStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getScrollBarStyle(): Int
```

Returns the current scrollbar style.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current scrollbar style. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_INSIDE_OVERLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_INSIDE_INSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_OUTSIDE_OVERLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_OUTSIDE_INSET:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_INSIDE_OVERLAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_INSIDE_INSET:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_OUTSIDE_OVERLAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_OUTSIDE_INSET:kotlin.Int`

### getScrollCaptureHint

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getScrollCaptureHint(): Int
```

Returns the current scroll capture hint for this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current scroll capture hint. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE_DESCENDANTS:kotlin.Int` |

### getScrollIndicators

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getScrollIndicators(): Int
```

Returns a bitmask representing the enabled scroll indicators.

For example, if the top and left scroll indicators are enabled and all other indicators are disabled, the return value will be `View.SCROLL_INDICATOR_TOP | View.SCROLL_INDICATOR_LEFT`.
| --- | --- |

To check whether the bottom scroll indicator is enabled, use the value of `(getScrollIndicators() & View.SCROLL_INDICATOR_BOTTOM) != 0`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask representing the enabled scroll indicators. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_BOTTOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_END:kotlin.Int` |

### getScrollX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScrollX(): Int
```

Return the scrolled left position of this view. This is the left edge of the displayed part of your view. You do not need to draw any pixels farther left, since those are outside of the frame of your view on screen.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The left edge of the displayed part of your view, in pixels. |

### getScrollY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScrollY(): Int
```

Return the scrolled top position of this view. This is the top edge of the displayed part of your view. You do not need to draw any pixels above it, since those are outside of the frame of your view on screen.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The top edge of the displayed part of your view, in pixels. |

### getSolidColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSolidColor(): Int
```

Override this if your view is known to always be drawn on top of a solid color background, and needs to draw fading edges. Returning a non-zero color enables the view system to optimize the drawing of the fading edges. If you do return a non-zero color, the alpha should be set to 0xFF.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The known solid color background for this view, or 0 if the color may vary |

**See Also**

- setVerticalFadingEdgeEnabled
- setHorizontalFadingEdgeEnabled

### getSourceLayoutResId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSourceLayoutResId(): Int
```

A View can be inflated from an XML layout. For such Views this method returns the resource ID of the source layout.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The layout resource id if this view was inflated from XML, otherwise `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int`. |

### getStateDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStateDescription(): CharSequence?
```

Returns the View's state description.

**Note:** Do not override this method, as it will have no effect on the state description presented to accessibility services. You must call setStateDescription to modify the state description.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the state description. This value may be `null`. |

**See Also**

- setStateDescription

### getStateListAnimator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStateListAnimator(): StateListAnimator!
```

Returns the current StateListAnimator if exists.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/animation/StateListAnimator.html#!` | StateListAnimator or null if it does not exists |

**See Also**

- setStateListAnimator

### getSupplementalDescription

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSupplementalDescription(): CharSequence?
```

Returns the View's supplemental description.

A supplemental description provides brief supplemental information for this node, such as the purpose of the node when that purpose is not conveyed within its textual representation. For example, if a dropdown select has a purpose of setting font family, the supplemental description could be "font family". If this node has children, its supplemental description serves as additional information and is not intended to replace any existing information in the subtree. This is different from the getContentDescription in that this description is purely supplemental while a content description may be used to replace a description for a node or its subtree that an assistive technology would otherwise compute based on other properties of the node and its descendants.

**Note:** Do not override this method, as it will have no effect on the supplemental description presented to accessibility services. You must call setSupplementalDescription to modify the supplemental description.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the supplemental description. This value may be `null`. |

**See Also**

- setSupplementalDescription
- getContentDescription

### getSystemGestureExclusionRects

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemGestureExclusionRects(): MutableList<Rect!>
```

Retrieve the list of areas within this view's post-layout coordinate space where the system should not intercept touch or other pointing device gestures.

Do not modify the returned list.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!>` | the list set by setSystemGestureExclusionRects This value cannot be `null`. |

### getSystemUiVisibility

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemUiVisibility(): Int
```

**Deprecated:** *SystemUiVisibility flags are deprecated. Use WindowInsetsController instead.*

Returns the last setSystemUiVisibility that this view has requested.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Bitwise-or of flags `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LOW_PROFILE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_STABLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_IMMERSIVE:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_IMMERSIVE_STICKY:kotlin.Int`. |

### getTag

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTag(): Any!
```

Returns this view's tag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the Object stored in this view as a tag, or `null` if not set |

**See Also**

- setTag
- getTag

### getTag

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTag(key: Int): Any!
```

Returns the tag associated with this view and the specified key.

| Parameters ||
|---|---|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key identifying the tag |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the Object stored in this view as a tag, or `null` if not set |

**See Also**

- setTag
- getTag

### getTextAlignment

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextAlignment(): Int
```

Return the resolved text alignment.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the resolved text alignment. Returns one of: `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_GRAVITY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_CENTER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_START:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_END:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_START:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_END:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_INHERIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_GRAVITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_CENTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_END:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_END:kotlin.Int` |

### getTextDirection

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextDirection(): Int
```

Return the resolved text direction.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the resolved text direction. Returns one of: `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_ANY_RTL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_LTR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_RTL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_LOCALE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG_LTR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG_RTL:kotlin.Int` |

### getTooltipText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTooltipText(): CharSequence?
```

Returns the view's tooltip text. **Note:** Do not override this method, as it will have no effect on the text displayed in the tooltip. You must call setTooltipText to modify the tooltip text.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the tooltip text. This value may be `null`. |

**See Also**

- setTooltipText

### getTop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTop(): Int
```

Top position of this view relative to its parent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The top of this view, in pixels. |

### getTouchDelegate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTouchDelegate(): TouchDelegate!
```

Gets the TouchDelegate for this View.

### getTouchables

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTouchables(): ArrayList<View!>!
```

Find and return all touchable views that are descendants of this view, possibly including this view if it is touchable itself.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/view/View#!>!` | A list of touchable views |

### getTransitionAlpha

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTransitionAlpha(): Float
```

This property is intended only for use by the Fade transition, which animates it to produce a visual translucency that does not side-effect (or get affected by) the real alpha property. This value is composited with the other alpha value (and the AlphaAnimation value, when that is present) to produce a final visual translucency result, which is what is passed into the DisplayList.

### getTransitionName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTransitionName(): String!
```

Returns the name of the View to be used to identify Views in Transitions. Names should be unique in the View hierarchy.

This returns null if the View has not been given a name.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The name used of the View to be used to identify Views in Transitions or null if no name has been given. |

### getTranslationX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTranslationX(): Float
```

The horizontal location of this view relative to its getLeft position. This position is post-layout, in addition to wherever the object's layout placed it.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The horizontal position of this view relative to its left position, in pixels. |

### getTranslationY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTranslationY(): Float
```

The vertical location of this view relative to its getTop position. This position is post-layout, in addition to wherever the object's layout placed it.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The vertical position of this view relative to its top position, in pixels. |

### getTranslationZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTranslationZ(): Float
```

The depth location of this view relative to its getElevation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The depth of this view relative to its elevation. |

### getUniqueDrawingId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUniqueDrawingId(): Long
```

Get the identifier used for this view by the drawing system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | A long that uniquely identifies this view's drawing component |

**See Also**

- getUniqueId

### getVerticalFadingEdgeLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVerticalFadingEdgeLength(): Int
```

Returns the size of the vertical faded edges used to indicate that more content in this view is visible.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The size in pixels of the vertical faded edge or 0 if vertical faded edges are not enabled for this view. |

### getVerticalScrollbarPosition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVerticalScrollbarPosition(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The position where the vertical scroll bar will show, if applicable. |

**See Also**

- setVerticalScrollbarPosition

### getVerticalScrollbarThumbDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVerticalScrollbarThumbDrawable(): Drawable?
```

Returns the currently configured Drawable for the thumb of the vertical scroll bar if it exists, null otherwise.
**See Also**

- awakenScrollBars
- isVerticalScrollBarEnabled
- setVerticalScrollBarEnabled

### getVerticalScrollbarTrackDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVerticalScrollbarTrackDrawable(): Drawable?
```

Returns the currently configured Drawable for the track of the vertical scroll bar if it exists, null otherwise.
**See Also**

- awakenScrollBars
- isVerticalScrollBarEnabled
- setVerticalScrollBarEnabled

### getVerticalScrollbarWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVerticalScrollbarWidth(): Int
```

Returns the width of the vertical scrollbar.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The width in pixels of the vertical scrollbar or 0 if there is no vertical scrollbar. |

### getViewTranslationResponse

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getViewTranslationResponse(): ViewTranslationResponse?
```

Returns the ViewTranslationResponse associated with this view. The response will be set when the translation is done then onViewTranslationResponse is called. The ViewTranslationCallback can use to get ViewTranslationResponse to display the translated information.

| Return ||
|---|---|
| ViewTranslationResponse | a ViewTranslationResponse that contains the translated information associated with this view or `null` if this View doesn't have the translation. |

### getViewTreeObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getViewTreeObserver(): ViewTreeObserver!
```

Returns the ViewTreeObserver for this view's hierarchy. The view tree observer can be used to get notifications when global events, like layout, happen. The returned ViewTreeObserver observer is not guaranteed to remain valid for the lifetime of this View. If the caller of this method keeps a long-lived reference to ViewTreeObserver, it should always check for the return value of isAlive.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver!` | The ViewTreeObserver for this view's hierarchy. |

### getVisibility

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVisibility(): Int
```

Returns the visibility status for this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | One of `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` |

### getWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWidth(): Int
```

Return the width of your view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The width of your view, in pixels. |

### getWindowId

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWindowId(): WindowId!
```

Retrieve the WindowId for the window this view is currently attached to.

### getWindowInsetsController

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWindowInsetsController(): WindowInsetsController?
```

Retrieves the single WindowInsetsController of the window this view is attached to.

| Return ||
|---|---|
| WindowInsetsController | The WindowInsetsController or `null` if the view is neither attached to a window nor a view tree with a decor. |

**See Also**

- getInsetsController

### getWindowSystemUiVisibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWindowSystemUiVisibility(): Int
```

**Deprecated:** *SystemUiVisibility flags are deprecated. Use WindowInsetsController instead.*

Returns the current system UI visibility that is currently set for the entire window. This is the combination of the setSystemUiVisibility values supplied by all of the views in the window.

### getWindowToken

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWindowToken(): IBinder!
```

Retrieve a unique token identifying the window this view is attached to.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/IBinder.html#!` | Return the window's token for use in `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#token:android.os.IBinder`. This token maybe null if this view is not attached to a window. |

**See Also**

- isAttachedToWindow
- `https://developer.android.com/reference/kotlin/android/view/View.OnAttachStateChangeListener`

### getWindowVisibility

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWindowVisibility(): Int
```

Returns the current visibility of the window this view is attached to (either `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the current visibility of the view's window. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` |

### getWindowVisibleDisplayFrame

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWindowVisibleDisplayFrame(outRect: Rect!): Unit
```

Retrieve the overall visible display size in which the window this view is attached to has been positioned in. This takes into account screen decorations above the window, for both cases where the window itself is being position inside of them or the window is being placed under then and covered insets are used for the window to position its content inside. In effect, this tells you the available area where content can be placed and remain visible to users.

| Parameters ||
|---|---|
| `outRect` | [Rect](../android.graphics/Rect.md)!: Filled in with the visible display frame. If the view is not attached to a window, this is simply the raw display size. |

### getX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getX(): Float
```

The visual x position of this view, in pixels. This is equivalent to the setTranslationX property plus the current getLeft property.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The visual x position of this view, in pixels. |

### getY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getY(): Float
```

The visual y position of this view, in pixels. This is equivalent to the setTranslationY property plus the current getTop property.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The visual y position of this view, in pixels. |

### getZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getZ(): Float
```

The visual z position of this view, in pixels. This is equivalent to the setTranslationZ property plus the current getElevation property.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The visual z position of this view, in pixels. |

### hasExplicitFocusable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasExplicitFocusable(): Boolean
```

Returns true if this view is focusable or if it contains a reachable View for which hasExplicitFocusable returns `true`. A "reachable hasExplicitFocusable()" is a view whose parents do not block descendants focus. Only `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` views for which getFocusable would return `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE:kotlin.Int` are considered focusable.

This method preserves the pre-`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` behavior of hasFocusable in that only views explicitly set focusable will cause this method to return true. A view set to `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE_AUTO:kotlin.Int` that resolves to focusable will not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the view is focusable or if the view contains a focusable view, `false` otherwise |

**See Also**

- hasFocusable

### hasFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasFocus(): Boolean
```

Returns true if this view has focus itself, or is the ancestor of the view that has focus.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this view has or contains focus, false otherwise. |

### hasFocusable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasFocusable(): Boolean
```

Returns true if this view is focusable or if it contains a reachable View for which hasFocusable returns `true`. A "reachable hasFocusable()" is a view whose parents do not block descendants focus. Only `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` views are considered focusable.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` views that are determined to be focusable through `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE_AUTO:kotlin.Int` will also cause this method to return `true`. Apps that declare a `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#targetSdkVersion:kotlin.Int` of earlier than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` will continue to see this method return `false` for views not explicitly marked as focusable. Use hasExplicitFocusable if you require the pre-`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` behavior.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the view is focusable or if the view contains a focusable view, `false` otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_BLOCK_DESCENDANTS:kotlin.Int`
- getTouchscreenBlocksFocus
- hasExplicitFocusable

### hasNestedScrollingParent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasNestedScrollingParent(): Boolean
```

Returns true if this view has a nested scrolling parent.

The presence of a nested scrolling parent indicates that this view has initiated a nested scroll and it was accepted by an ancestor view further up the view hierarchy.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether this view has a nested scrolling parent |

### hasOnClickListeners

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasOnClickListeners(): Boolean
```

Return whether this view has an attached OnClickListener. Returns true if there is a listener, false if there is none.

### hasOnLongClickListeners

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasOnLongClickListeners(): Boolean
```

Return whether this view has an attached OnLongClickListener. Returns true if there is a listener, false if there is none.

### hasOverlappingRendering

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasOverlappingRendering(): Boolean
```

Returns whether this View has content which overlaps.

This function, intended to be overridden by specific View types, is an optimization when alpha is set on a view. If rendering overlaps in a view with alpha \< 1, that view is drawn to an offscreen buffer and then composited into place, which can be expensive. If the view has no overlapping rendering, the view can draw each primitive with the appropriate alpha value directly. An example of overlapping rendering is a TextView with a background image, such as a Button. An example of non-overlapping rendering is a TextView with no background, or an ImageView with only the foreground image. The default implementation returns true; subclasses should override if they have cases which can be optimized.

**Note:** The return value of this method is ignored if forceHasOverlappingRendering has been called on this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the content in this view might overlap, false otherwise. |

### hasPointerCapture

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasPointerCapture(): Boolean
```

Checks pointer capture status.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the view has pointer capture. |

**See Also**

- requestPointerCapture
- hasPointerCapture

### hasTransientState

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasTransientState(): Boolean
```

Indicates whether the view is currently tracking transient state that the app should not need to concern itself with saving and restoring, but that the framework should take special note to preserve when possible.

A view with transient state cannot be trivially rebound from an external data source, such as an adapter binding item views in a list. This may be because the view is performing an animation, tracking user selection of content, or similar.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the view has transient state |

### hasWindowFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasWindowFocus(): Boolean
```

Returns true if this view is in a window that currently has window focus. Note that this is not the same as the view itself having focus.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this view is in a window that currently has window focus. |

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun inflate(
    context: Context!, 
    resource: Int, 
    root: ViewGroup!
): View!
```

Inflate a view from an XML resource. This convenience method wraps the LayoutInflater class, which provides a full range of options for view inflation.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: The Context object for your activity or application. |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource ID to inflate |
| `root` | [ViewGroup](ViewGroup.md)!: A view group that will be the parent. Used to properly inflate the layout_\* parameters. |
| --- | --- |

**See Also**

- LayoutInflater

### invalidate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invalidate(): Unit
```

Invalidate the whole view. If the view is visible, onDraw will be called at some point in the future.

This must be called from a UI thread. To call from a non-UI thread, call postInvalidate.

### invalidate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invalidate(dirty: Rect!): Unit
```

**Deprecated:** *The switch to hardware accelerated rendering in API 14 reduced the importance of the dirty rectangle. In API 21 the given rectangle is ignored entirely in favor of an internally-calculated area instead. Because of this, clients are encouraged to just call invalidate.*

Mark the area defined by dirty as needing to be drawn. If the view is visible, onDraw will be called at some point in the future.

This must be called from a UI thread. To call from a non-UI thread, call postInvalidate.

**WARNING:** In API 19 and below, this method may be destructive to `dirty`.

| Parameters ||
|---|---|
| `dirty` | [Rect](../android.graphics/Rect.md)!: the rectangle representing the bounds of the dirty region |

### invalidate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invalidate(
    l: Int, 
    t: Int, 
    r: Int, 
    b: Int
): Unit
```

**Deprecated:** *The switch to hardware accelerated rendering in API 14 reduced the importance of the dirty rectangle. In API 21 the given rectangle is ignored entirely in favor of an internally-calculated area instead. Because of this, clients are encouraged to just call invalidate.*

Mark the area defined by the rect (l,t,r,b) as needing to be drawn. The coordinates of the dirty rect are relative to the view. If the view is visible, onDraw will be called at some point in the future.

This must be called from a UI thread. To call from a non-UI thread, call postInvalidate.

| Parameters ||
|---|---|
| `l` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the left position of the dirty region |
| `t` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the top position of the dirty region |
| `r` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the right position of the dirty region |
| --- | --- |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the bottom position of the dirty region |

### invalidateDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invalidateDrawable(drawable: Drawable): Unit
```

Invalidates the specified Drawable.

| Parameters ||
|---|---|
| `who` | The drawable that is requesting the update. This value cannot be `null`. |
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md): the drawable to invalidate. This value cannot be `null`. |

### invalidateOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invalidateOutline(): Unit
```

Called to rebuild this View's Outline from its ViewOutlineProvider
**See Also**

- setOutlineProvider

### isAccessibilityDataSensitive

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAccessibilityDataSensitive(): Boolean
```

Whether this view should restrict accessibility service access only to services that have the isAccessibilityTool property set to true.

See default behavior provided by `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_AUTO:kotlin.Int`. Otherwise, returns true for `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_YES:kotlin.Int` or false for `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_NO:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this view should restrict accessibility service access to services that have the isAccessibilityTool property. |

### isAccessibilityFocused

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAccessibilityFocused(): Boolean
```

Returns whether this View is accessibility focused.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this View is accessibility focused. |

### isAccessibilityHeading

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAccessibilityHeading(): Boolean
```

Gets whether this view is a heading for accessibility purposes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the view is a heading, `false` otherwise. |

### isActivated

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isActivated(): Boolean
```

Indicates the activation state of this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the view is activated, false otherwise |

### isAttachedToWindow

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAttachedToWindow(): Boolean
```

Returns true if this view is currently attached to a window.

### isAutoHandwritingEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAutoHandwritingEnabled(): Boolean
```

Return whether the View allows automatic handwriting initiation. Returns true if automatic handwriting initiation is enabled, and vice versa.
**See Also**

- setAutoHandwritingEnabled

### isClickable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isClickable(): Boolean
```

Indicates whether this view reacts to click events or not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the view is clickable, false otherwise |

**See Also**

- setClickable

### isContentCaptureSelfReportingEnabled

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isContentCaptureSelfReportingEnabled(): Boolean
```

Returns whether this View automatically reports its lifecycle events and layout bounds to the Content Capture Version 2.

By default, this method returns `true`, which instructs the Android View system to automatically track this view's visibility, position, layout bounds, and structural changes and report them directly to the active ContentCaptureSession.

Views can override this method to return `false` to disable this automatic monitoring and take full manual control over when and how their properties are reported. This is particularly useful for Views that participate in hybrid hierarchies that can nest Views and Virtual Views bidirectionally. By disabling this behavior, the View itself can choose its own parent id and report the relative bounds to that parent in the Content Capture hierarchy.

#### Important for Content Capture Status and Self Reporting

setImportantForContentCapture can influence whether this View is reported to the Content Capture entirely, e.g. `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO:kotlin.Int` also disables self reporting. However, not being important for Content Capture influences how descendant nodes are reported. If this View were to be set as **NOT** important for Content Capture, its children will skip this View while finding their parent id and relative bounds to that parent. Therefore, if this View needs to still act as a parent to its children in Content Capture hierarchy, but needs to control how itself is reported, overriding this method and returning `false` is recommended.

**Note:** If this method returns `false`, the view is fully responsible for notifying the system about its lifecycle and property updates by calling methods such as notifyNodeAppearedOrChanged and notifyNodeDisappeared on the main thread.
This methods belongs to Content Capture Version 2.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if automatic self-reporting is enabled (default), `false` otherwise. |

**See Also**

- getContentCaptureVersion
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_2:kotlin.Int`

### isContentSensitive

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isContentSensitive(): Boolean
```

Returns whether this view displays sensitive content, based on the value explicitly set by setContentSensitivity.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the view displays sensitive content. |

**See Also**

- setContentSensitivity
- `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_AUTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_SENSITIVE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_NOT_SENSITIVE:kotlin.Int`

### isContextClickable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isContextClickable(): Boolean
```

Indicates whether this view reacts to context clicks or not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the view is context clickable, false otherwise |

**See Also**

- setContextClickable

### isCredential

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCredential(): Boolean
```

**Deprecated:** *The isCredential is no longer used by the system and is not recommended for use by apps. The purpose and usage expectations of this property were never clearly defined.*

Gets the mode for determining whether this view is a credential.

See setIsCredential.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | false by default, or value passed to setIsCredential. |

### isDirty

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDirty(): Boolean
```

True if this view has changed since the last time being drawn.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The dirty state of this view. |

### isDrawingCacheEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDrawingCacheEnabled(): Boolean
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Indicates whether the drawing cache is enabled for this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the drawing cache is enabled |

**See Also**

- setDrawingCacheEnabled
- getDrawingCache

### isDuplicateParentStateEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDuplicateParentStateEnabled(): Boolean
```

Indicates whether this duplicates its drawable state from its parent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this view's drawable state is duplicated from the parent, false otherwise |

**See Also**

- getDrawableState
- setDuplicateParentStateEnabled

### isEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEnabled(): Boolean
```

Returns the enabled status for this view. The interpretation of the enabled state varies by subclass.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this view is enabled, false otherwise. |

### isFocusable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFocusable(): Boolean
```

Returns whether this View is currently able to take focus.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this view can take focus, or false otherwise. |

### isFocusableInTouchMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFocusableInTouchMode(): Boolean
```

When a view is focusable, it may not want to take focus when in touch mode. For example, a button would like focus when the user is navigating via a D-pad so that the user can click on it, but once the user starts touching the screen, the button shouldn't take focus

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the view is focusable in touch mode. |

### isFocused

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFocused(): Boolean
```

Returns true if this view has focus

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this view has focus, false otherwise. |

### isFocusedByDefault

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFocusedByDefault(): Boolean
```

Returns whether this View should receive focus when the focus is restored for the view hierarchy containing this view.

Focus gets restored for a view hierarchy when the root of the hierarchy gets added to a window or serves as a target of cluster navigation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this view is the default-focus view, `false` otherwise |

**See Also**

- restoreDefaultFocus

### isForceDarkAllowed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isForceDarkAllowed(): Boolean
```

See setForceDarkAllowed

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if force dark is allowed (default), false if it is disabled |

### isHandwritingDelegate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isHandwritingDelegate(): Boolean
```

Returns whether this view has been set as a handwriting delegate by setIsHandwritingDelegate.

### isHapticFeedbackEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isHapticFeedbackEnabled(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether this view should have haptic feedback enabled for events such as long presses. |

**See Also**

- setHapticFeedbackEnabled
- performHapticFeedback

### isHardwareAccelerated

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isHardwareAccelerated(): Boolean
```

Indicates whether this view is attached to a hardware accelerated window or not.

Even if this method returns true, it does not mean that every call to draw will be made with an hardware accelerated `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#`. For instance, if this view is drawn onto an offscreen `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` and its window is hardware accelerated, isHardwareAccelerated will likely return false, and this method will return true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the view is attached to a window and the window is hardware accelerated; false in any other case. |

### isHorizontalFadingEdgeEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isHorizontalFadingEdgeEnabled(): Boolean
```

Indicate whether the horizontal edges are faded when the view is scrolled horizontally.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the horizontal edges should are faded on scroll, false otherwise |

**See Also**

- setHorizontalFadingEdgeEnabled

### isHorizontalScrollBarEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isHorizontalScrollBarEnabled(): Boolean
```

Indicate whether the horizontal scrollbar should be drawn or not. The scrollbar is not drawn by default.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the horizontal scrollbar should be painted, false otherwise |

**See Also**

- setHorizontalScrollBarEnabled

### isHovered

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isHovered(): Boolean
```

Returns true if the view is currently hovered.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the view is currently hovered. |

**See Also**

- setHovered
- onHoverChanged

### isImportantForAccessibility

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isImportantForAccessibility(): Boolean
```

Computes whether this view should be exposed for accessibility. In general, views that are interactive or provide information are exposed while views that serve only as containers are hidden.

If an ancestor of this view has importance `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int`, this method returns `false`.

Otherwise, the value is computed according to the view's getImportantForAccessibility value:

1. `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int`, return `false `
2. `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_YES:kotlin.Int`, return `true`
3. `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_AUTO:kotlin.Int`, return `true` if view satisfies any of the following:
 - Is actionable, e.g. isClickable, isLongClickable, isContextClickable, isScreenReaderFocusable, or isFocusable
 - Has an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate`
 - Has an AccessibilityNodeProvider
 - Has an interaction listener, e.g. `https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener`, `https://developer.android.com/reference/kotlin/android/view/View.OnKeyListener`, etc.
 - Is an accessibility live region, e.g. getAccessibilityLiveRegion is not `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_NONE:kotlin.Int`.
4. Has an accessibility pane title, see setAccessibilityPaneTitle
5. Is an accessibility heading, see setAccessibilityHeading.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the view is exposed for accessibility. |

**See Also**

- setImportantForAccessibility
- getImportantForAccessibility

### isImportantForAutofill

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isImportantForAutofill(): Boolean
```

Hints the Android System whether the `https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.ViewNode.html#` associated with this view is considered important for autofill purposes.

Generally speaking, a view is important for autofill if:

1. The view can be autofilled by an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#`.
2. The view contents can help an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` determine how other views can be autofilled.
 1. For example, view containers should typically return `false` for performance reasons (since the important info is provided by their children), but if its properties have relevant information (for example, a resource id called `credentials`, it should return `true`. On the other hand, views representing labels or editable fields should typically return `true`, but in some cases they could return `false` (for example, if they're part of a "Captcha" mechanism).
 2. The value returned by this method depends on the value returned by getImportantForAutofill:
 1. if it returns `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`, then it returns `true`
 2. if it returns `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int`, then it returns `false`
 3. if it returns `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int`, then it uses some simple heuristics that can return `true` in some cases (like a container with a resource id), but `false` in most.
 4. otherwise, it returns `false`.
 3. The behavior of importances depends on Android version:
 1. For `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` and below:
 1. When a view is considered important for autofill:
 1. The view might automatically trigger an autofill request when focused on.
 2. The contents of the view are included in the ViewStructure used in an autofill request.
 2. On the other hand, when a view is considered not important for autofill:
 1. The view never automatically triggers autofill requests, but it can trigger a manual request through requestAutofill.
 2. The contents of the view are not included in the ViewStructure used in an autofill request, unless the request has the `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int` flag.
 2. For `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and above:
 1. The system uses importance, along with other view properties and other optimization factors, to determine if a view should trigger autofill on focus.
 2. The contents of `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int` views will be included in the ViewStructure used in an autofill request.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the view is considered important for autofill. |

**See Also**

- setImportantForAutofill
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int`
- requestAutofill

### isImportantForContentCapture

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isImportantForContentCapture(): Boolean
```

Hints the Android System whether this view is considered important for content capture, based on the value explicitly set by setImportantForContentCapture and heuristics when it's `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_AUTO:kotlin.Int`.

See ContentCaptureManager for more info about content capture.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the view is considered important for content capture. |

**See Also**

- setImportantForContentCapture
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_AUTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES_EXCLUDE_DESCENDANTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO_EXCLUDE_DESCENDANTS:kotlin.Int`

### isInEditMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInEditMode(): Boolean
```

Indicates whether this View is currently in edit mode. A View is usually in edit mode when displayed within a developer tool. For instance, if this View is being drawn by a visual user interface builder, this method should return true. Subclasses should check the return value of this method to provide different behaviors if their normal behavior might interfere with the host environment. For instance: the class spawns a thread in its constructor, the drawing code relies on device-specific features, etc. This method is usually checked in the drawing code of custom widgets.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this View is in edit mode, false otherwise. |

### isInLayout

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInLayout(): Boolean
```

Returns whether the view hierarchy is currently undergoing a layout pass. This information is useful to avoid situations such as calling requestLayout during a layout pass.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the view hierarchy is currently undergoing a layout pass |

### isInTouchMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInTouchMode(): Boolean
```

Returns the touch mode state associated with this view. Attached views return the touch mode state from the associated window's display. Detached views just return the default touch mode value defined in `com.android.internal.R.bool.config_defaultInTouchMode`. Touch mode is entered once the user begins interacting with the device by touch, and affects various things like whether focus highlight is always visible to the user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the touch mode state associated with this view |

### isKeyboardNavigationCluster

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isKeyboardNavigationCluster(): Boolean
```

Returns whether this View is a root of a keyboard navigation cluster.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this view is a root of a cluster, or false otherwise. |

### isLaidOut

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isLaidOut(): Boolean
```

Returns true if this view has been through at least one layout since it was last attached to or detached from a window.

### isLayoutDirectionResolved

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isLayoutDirectionResolved(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if layout direction has been resolved. |

### isLayoutRequested

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isLayoutRequested(): Boolean
```

Indicates whether or not this view's layout will be requested during the next hierarchy layout pass.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the layout will be forced during next layout pass |

### isLongClickable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isLongClickable(): Boolean
```

Indicates whether this view reacts to long click events or not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the view is long clickable, false otherwise |

**See Also**

- setLongClickable

### isNestedScrollingEnabled

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isNestedScrollingEnabled(): Boolean
```

Returns true if nested scrolling is enabled for this view.

If nested scrolling is enabled and this View class implementation supports it, this view will act as a nested scrolling child view when applicable, forwarding data about the scroll operation in progress to a compatible and cooperating nested scrolling parent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if nested scrolling is enabled |

**See Also**

- setNestedScrollingEnabled

### isOpaque

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isOpaque(): Boolean
```

Indicates whether this View is opaque. An opaque View guarantees that it will draw all the pixels overlapping its bounds using a fully opaque color. Subclasses of View should override this method whenever possible to indicate whether an instance is opaque. Opaque Views are treated in a special way by the View hierarchy, possibly allowing it to perform optimizations during invalidate/draw passes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this View is guaranteed to be fully opaque, false otherwise. |

### isPaddingRelative

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPaddingRelative(): Boolean
```

Return if the padding has been set through relative values setPaddingRelative or through

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the padding is relative or false if it is not. |

### isPivotSet

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPivotSet(): Boolean
```

Returns whether or not a pivot has been set by a call to setPivotX or setPivotY. If no pivot has been set then the pivot will be the center of the view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if a pivot has been set, false if the default pivot is being used |

### isPreferKeepClear

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isPreferKeepClear(): Boolean
```

Retrieve the preference for this view to be kept clear. This is set either by setPreferKeepClear or via the attribute android.R.styleable#View_preferKeepClear.

If this is `true`, the system will ignore the Rects set by setPreferKeepClearRects and try to keep the whole view clear.

<br />

**See Also**

- setPreferKeepClear

### isPressed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPressed(): Boolean
```

Indicates whether the view is currently in pressed state. Unless setPressed is explicitly called, only clickable views can enter the pressed state.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the view is currently pressed, false otherwise |

**See Also**

- setPressed
- isClickable
- setClickable

### isSaveEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSaveEnabled(): Boolean
```

Indicates whether this view will save its state (that is, whether its onSaveInstanceState method will be called).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the view state saving is enabled, else false. |

**See Also**

- setSaveEnabled

### isSaveFromParentEnabled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSaveFromParentEnabled(): Boolean
```

Indicates whether the entire hierarchy under this view will save its state when a state saving traversal occurs from its parent. The default is true; if false, these views will not be saved unless saveHierarchyState is called directly on this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the view state saving from parent is enabled, else false. |

**See Also**

- setSaveFromParentEnabled

### isScreenReaderFocusable

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isScreenReaderFocusable(): Boolean
```

Returns whether the view should be treated as a focusable unit by screen reader accessibility tools.

**Note:** Use androidx.core.view.ViewCompat#setScreenReaderFocusable(android.view.View,boolean) for backwards-compatibility.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the view should be treated as a focusable unit by screen reader. |

**See Also**

- setScreenReaderFocusable

### isScrollContainer

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isScrollContainer(): Boolean
```

Indicates whether this view is one of the set of scrollable containers in its window.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether this view is one of the set of scrollable containers in its window |

### isScrollbarFadingEnabled

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isScrollbarFadingEnabled(): Boolean
```

Returns true if scrollbars will fade when this view is not scrolling

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if scrollbar fading is enabled |

### isSelected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSelected(): Boolean
```

Indicates the selection state of this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the view is selected, false otherwise |

### isShowingLayoutBounds

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isShowingLayoutBounds(): Boolean
```

Returns `true` when the View is attached and the system developer setting to show the layout bounds is enabled or `false` otherwise.

### isShown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isShown(): Boolean
```

Returns the visibility of this view and all of its ancestors

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this view and all of its ancestors are `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` |

### isSoundEffectsEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSoundEffectsEnabled(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether this view should have sound effects enabled for events such as clicking and touching. |

**See Also**

- setSoundEffectsEnabled
- playSoundEffect

### isTemporarilyDetached

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isTemporarilyDetached(): Boolean
```

Tells whether the View is in the state between onStartTemporaryDetach and onFinishTemporaryDetach.

This method always returns `true` when called directly or indirectly from onStartTemporaryDetach. The return value when called directly or indirectly from onFinishTemporaryDetach, however, depends on the OS version.

- `true` on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`
- `false` on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N_MR1:kotlin.Int`} and later

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` when the View is in the state between onStartTemporaryDetach and onFinishTemporaryDetach. |

### isTextAlignmentResolved

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTextAlignmentResolved(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if text alignment is resolved. |

### isTextDirectionResolved

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTextDirectionResolved(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if text direction is resolved. |

### isVerticalFadingEdgeEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVerticalFadingEdgeEnabled(): Boolean
```

Indicate whether the vertical edges are faded when the view is scrolled horizontally.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the vertical edges should are faded on scroll, false otherwise |

**See Also**

- setVerticalFadingEdgeEnabled

### isVerticalScrollBarEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVerticalScrollBarEnabled(): Boolean
```

Indicate whether the vertical scrollbar should be drawn or not. The scrollbar is not drawn by default.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the vertical scrollbar should be painted, false otherwise |

**See Also**

- setVerticalScrollBarEnabled

### isVisibleToUserForAutofill

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVisibleToUserForAutofill(virtualId: Int): Boolean
```

Computes whether this virtual autofill view is visible to the user.

**Note:** By default it returns `true`, but views providing a virtual hierarchy view must override it.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the view is visible on the screen. |

### jumpDrawablesToCurrentState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun jumpDrawablesToCurrentState(): Unit
```

Call jumpToCurrentState on all Drawable objects associated with this view.

Also calls jumpToCurrentState if there is a StateListAnimator attached to this view. 
If you override this method you *must* call through to the superclass implementation.

### keyboardNavigationClusterSearch

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun keyboardNavigationClusterSearch(
    currentCluster: View!, 
    direction: Int
): View!
```

Find the nearest keyboard navigation cluster in the specified direction. This does not actually give focus to that cluster.

| Parameters ||
|---|---|
| `currentCluster` | [View](View.md)!: The starting point of the search. Null means the current cluster is not found yet |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Direction to look. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View#!` | The nearest keyboard navigation cluster in the specified direction, or null if none can be found |

### layout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun layout(
    l: Int, 
    t: Int, 
    r: Int, 
    b: Int
): Unit
```

Assign a size and position to a view and all of its descendants

This is the second phase of the layout mechanism. (The first is measuring). In this phase, each parent calls layout on all of its children to position them. This is typically done using the child measurements that were stored in the measure pass().

Derived classes should not override this method. Derived classes with children should override onLayout. In that method, they should call layout on each of their children.

| Parameters ||
|---|---|
| `l` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Left position, relative to parent |
| `t` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Top position, relative to parent |
| `r` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Right position, relative to parent |
| --- | --- |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bottom position, relative to parent |

### measure

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun measure(
    widthMeasureSpec: Int, 
    heightMeasureSpec: Int
): Unit
```

This is called to find out how big a view should be. The parent supplies constraint information in the width and height parameters.

The actual measurement work of a view is performed in onMeasure, called by this method. Therefore, only onMeasure can and must be overridden by subclasses.

| Parameters ||
|---|---|
| `widthMeasureSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Horizontal space requirements as imposed by the parent |
| `heightMeasureSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Vertical space requirements as imposed by the parent |

**See Also**

- onMeasure

### offsetLeftAndRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun offsetLeftAndRight(offset: Int): Unit
```

Offset this view's horizontal location by the specified amount of pixels.

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of pixels to offset the view by |

### offsetTopAndBottom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun offsetTopAndBottom(offset: Int): Unit
```

Offset this view's vertical location by the specified number of pixels.

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of pixels to offset the view by |

### onApplyWindowInsets

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onApplyWindowInsets(insets: WindowInsets!): WindowInsets!
```

Called when the view should apply WindowInsets according to its internal policy.

This method should be overridden by views that wish to apply a policy different from or in addition to the default behavior. Clients that wish to force a view subtree to apply insets should call dispatchApplyWindowInsets.

Clients may supply an `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener` to a view. If one is set it will be called during dispatch instead of this method. The listener may optionally call this method from its own implementation if it wishes to apply the view's default insets policy in addition to its own.

Implementations of this method should either return the insets parameter unchanged or a new WindowInsets cloned from the supplied insets with any insets consumed that this view applied itself. This allows new inset types added in future platform versions to pass through existing implementations unchanged without being erroneously consumed.

By default if a view's setFitsSystemWindows property is set then the view will consume the system window insets and apply them as padding for the view.

| Parameters ||
|---|---|
| `insets` | [WindowInsets](WindowInsets.md)!: Insets to apply |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/WindowInsets!` | The supplied insets with any applied insets consumed |

### onCancelPendingInputEvents

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCancelPendingInputEvents(): Unit
```

Called as the result of a call to cancelPendingInputEvents on this view or a parent view.

This method is responsible for removing any pending high-level input events that were posted to the event queue to run later. Custom view classes that post their own deferred high-level events via post, postDelayed or `https://developer.android.com/reference/kotlin/android/os/Handler.html#` should override this method, call `super.onCancelPendingInputEvents()` and remove those callbacks as appropriate.

### onCapturedPointerEvent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCapturedPointerEvent(event: MotionEvent!): Boolean
```

Implement this method to handle captured pointer events

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The captured pointer event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled, false otherwise. |

**See Also**

- requestPointerCapture

### onCheckIsTextEditor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCheckIsTextEditor(): Boolean
```

Check whether the called view is a text editor, in which case it would make sense to automatically display a soft input window for it. Subclasses should override this if they implement onCreateInputConnection to return true if a call on that method would return a non-null InputConnection, and they are really a first-class editor that the user would normally start typing on when the go into a window containing your view.

The default implementation always returns false. This does *not* mean that its onCreateInputConnection will not be called or the user can not otherwise perform edits on your view; it is just a hint to the system that this is not the primary purpose of this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if this view is a text editor, else false. |

### onCreateInputConnection

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateInputConnection(outAttrs: EditorInfo!): InputConnection!
```

Create a new InputConnection for an InputMethod to interact with the view. The default implementation returns null, since it doesn't support input methods. You can override this to implement such support. This is only needed for views that take focus and text input.

When implementing this, you probably also want to implement onCheckIsTextEditor to indicate you will return a non-null InputConnection.

Also, take good care to fill in the EditorInfo object correctly and in its entirety, so that the connected IME can rely on its values. For example, `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#initialSelStart:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#initialSelEnd:kotlin.Int` members must be filled in with the correct cursor position for IMEs to work correctly with your application.

| Parameters ||
|---|---|
| `outAttrs` | [EditorInfo](../android.view.inputmethod/EditorInfo.md)!: Fill in with attribute information about the connection. |

### onCreateViewTranslationRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateViewTranslationRequest(
    supportedFormats: IntArray, 
    requestsCollector: Consumer<ViewTranslationRequest!>
): Unit
```

Collects a ViewTranslationRequest which represents the content to be translated in the view.

The default implementation does nothing.

| Parameters ||
|---|---|
| `supportedFormats` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the supported translation formats. For now, the only possible value is the `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec#DATA_FORMAT_TEXT:kotlin.Int`. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec#DATA_FORMAT_TEXT:kotlin.Int` |
| `requestsCollector` | [Consumer](../java.util.function/Consumer.md)\< [ViewTranslationRequest](../android.view.translation/ViewTranslationRequest.md)!\>: a ViewTranslationRequest collector that can be used to collect the information to be translated in the view. The `requestsCollector` only accepts one request; an IllegalStateException is thrown if more than one ViewTranslationRequest is submitted to it. The AutofillId must be set on the ViewTranslationRequest. This value cannot be `null`. |

### onCreateVirtualViewTranslationRequests

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateVirtualViewTranslationRequests(
    virtualIds: LongArray, 
    supportedFormats: IntArray, 
    requestsCollector: Consumer<ViewTranslationRequest!>
): Unit
```

Collects ViewTranslationRequests which represents the content to be translated for the virtual views in the host view. This is called if this view returned a virtual view structure from onProvideContentCaptureStructure and the system determined that those virtual views were relevant for translation.

The default implementation does nothing.

| Parameters ||
|---|---|
| `virtualIds` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the virtual view ids which represents the virtual views in the host view. This value cannot be `null`. |
| `supportedFormats` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the supported translation formats. For now, the only possible value is the `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec#DATA_FORMAT_TEXT:kotlin.Int`. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec#DATA_FORMAT_TEXT:kotlin.Int` |
| `requestsCollector` | [Consumer](../java.util.function/Consumer.md)\< [ViewTranslationRequest](../android.view.translation/ViewTranslationRequest.md)!\>: a ViewTranslationRequest collector that can be called multiple times to collect the information to be translated in the host view. One ViewTranslationRequest per virtual child. The ViewTranslationRequest must contains the AutofillId corresponding to the virtualChildIds. Do not keep this Consumer after the method returns. This value cannot be `null`. |
| --- | --- |

### onDragEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDragEvent(event: DragEvent!): Boolean
```

Handles drag events sent by the system following a call to startDragAndDrop.

The system calls this method and passes a DragEvent object in response to drag and drop events. This method can then call getAction to determine the state of the drag and drop operation.

The default implementation returns `false` unless an OnReceiveContentListener has been set for this view (see setOnReceiveContentListener), in which case the default implementation does the following:

- Returns `true` for an `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_STARTED:kotlin.Int` event
- Calls performReceiveContent for an `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int` event
- Returns `true` for an `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int` event if the `OnReceiveContentListener` consumed some or all of the content

| Parameters ||
|---|---|
| `event` | [DragEvent](DragEvent.md)!: The DragEvent object sent by the system. The getAction method returns an action type constant that indicates the type of drag event represented by this object. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the method successfully handled the drag event, otherwise `false`. The method must return `true` in response to an `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_STARTED:kotlin.Int` action type to continue to receive drag events for the current drag and drop operation. The method should return `true` in response to an `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int` action type if the dropped data was consumed (at least partially); `false`, if none of the data was consumed. For all other events, the return value is `false`. |

### onDrawForeground

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDrawForeground(canvas: Canvas): Unit
```

Draw any foreground content for this view.

Foreground content may consist of scroll bars, a setForeground drawable or other view-specific decorations. The foreground is drawn on top of the primary view content.

| Parameters ||
|---|---|
| `canvas` | [Canvas](../android.graphics/Canvas.md): canvas to draw into. This value cannot be `null`. |

### onFilterTouchEventForSecurity

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onFilterTouchEventForSecurity(event: MotionEvent!): Boolean
```

Filter the touch event to apply security policies.

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The motion event to be filtered. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event should be dispatched, false if the event should be dropped. |

**See Also**

- getFilterTouchesWhenObscured

### onFinishTemporaryDetach

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onFinishTemporaryDetach(): Unit
```

Called after onStartTemporaryDetach when the container is done changing the view.

### onGenericMotionEvent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onGenericMotionEvent(event: MotionEvent!): Boolean
```

Implement this method to handle generic motion events.

Generic motion events describe joystick movements, hover events from mouse or stylus devices, trackpad touches, scroll wheel movements and other motion events not handled by onTouchEvent or onTrackballEvent. The getSource of the motion event specifies the class of input that was received. Implementations of this method must examine the bits in the source before processing the event. The following code example shows how this is done.

Generic motion events with source class `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_POINTER:kotlin.Int` are delivered to the view under the pointer. All other generic motion events are delivered to the focused view.

```kotlin
public boolean onGenericMotionEvent(MotionEvent event) {
      if (event.isFromSource(InputDevice.SOURCE_CLASS_JOYSTICK)) {
          if (event.getAction() == MotionEvent.ACTION_MOVE) {
              // process the joystick movement...
              return true;
          }
      }
      if (event.isFromSource(InputDevice.SOURCE_CLASS_POINTER)) {
          switch (event.getAction()) {
              case MotionEvent.ACTION_HOVER_MOVE:
                  // process the hover movement...
                  return true;
              case MotionEvent.ACTION_SCROLL:
                  // process the scroll wheel movement...
                  return true;
          }
      }
      return super.onGenericMotionEvent(event);
  }
```

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The generic motion event being processed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled, false otherwise. |

### onHoverChanged

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onHoverChanged(hovered: Boolean): Unit
```

Implement this method to handle hover state changes.

This method is called whenever the hover state changes as a result of a call to setHovered.

| Parameters ||
|---|---|
| `hovered` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The current hover state, as returned by isHovered. |

**See Also**

- isHovered
- setHovered

### onHoverEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onHoverEvent(event: MotionEvent!): Boolean
```

Implement this method to handle hover events.

This method is called whenever a pointer is hovering into, over, or out of the bounds of a view and the view is not currently being touched. Hover events are represented as pointer events with action `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_ENTER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_MOVE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_EXIT:kotlin.Int`.

- The view receives a hover event with action `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_ENTER:kotlin.Int` when the pointer enters the bounds of the view.
- The view receives a hover event with action `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_MOVE:kotlin.Int` when the pointer has already entered the bounds of the view and has moved.
- The view receives a hover event with action `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_EXIT:kotlin.Int` when the pointer has exited the bounds of the view or when the pointer is about to go down due to a button click, tap, or similar user action that causes the view to be touched.

The view should implement this method to return true to indicate that it is handling the hover event, such as by changing its drawable state.

The default implementation calls setHovered to update the hovered state of the view when a hover enter or hover exit event is received, if the view is enabled and is clickable. The default implementation also sends hover accessibility events.

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The motion event that describes the hover. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the view handled the hover event. |

**See Also**

- isHovered
- setHovered
- onHoverChanged

### onInitializeAccessibilityEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onInitializeAccessibilityEvent(event: AccessibilityEvent!): Unit
```

Initializes an AccessibilityEvent with information about this View which is the event source. In other words, the source of an accessibility event is the view whose state change triggered firing the event.

Example: Setting the password property of an event in addition to properties set by the super implementation:

```kotlin
public void onInitializeAccessibilityEvent(AccessibilityEvent event) {
      super.onInitializeAccessibilityEvent(event);
      event.setPassword(true);
  }
```

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling setAccessibilityDelegate its onInitializeAccessibilityEvent is responsible for handling this call.

**Note:** Always call the super implementation before adding information to the event, in case the default implementation has basic information to add.
. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `event` | [AccessibilityEvent](../android.view.accessibility/AccessibilityEvent.md)!: The event to initialize. |

**See Also**

- sendAccessibilityEvent
- dispatchPopulateAccessibilityEvent

### onInitializeAccessibilityNodeInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onInitializeAccessibilityNodeInfo(info: AccessibilityNodeInfo!): Unit
```

Initializes an AccessibilityNodeInfo with information about this view. The base implementation sets:

- setParent,
- setBoundsInParent,
- setBoundsInScreen,
- setPackageName,
- setClassName,
- setContentDescription,
- setEnabled,
- setClickable,
- setFocusable,
- setFocused,
- setLongClickable,
- setSelected,
- setContextClickable

<br />

Subclasses should override this method, call the super implementation, and set additional attributes.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling setAccessibilityDelegate its onInitializeAccessibilityNodeInfo is responsible for handling this call.
. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `info` | [AccessibilityNodeInfo](../android.view.accessibility/AccessibilityNodeInfo.md)!: The instance to initialize. |

### onKeyDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyDown(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

Default implementation of onKeyDown: perform press of the view when `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_CENTER:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ENTER:kotlin.Int` is released, if the view is enabled and clickable.

Key presses in software keyboards will generally NOT trigger this listener, although some may elect to do so in some situations. Do not rely on this to catch software key presses.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a key code that represents the button pressed, from KeyEvent |
| `event` | [KeyEvent](KeyEvent.md)!: the KeyEvent object that defines the button action |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyLongPress

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyLongPress(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

Default implementation of onKeyLongPress: always returns false (doesn't handle the event).

Key presses in software keyboards will generally NOT trigger this listener, although some may elect to do so in some situations. Do not rely on this to catch software key presses.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value in event.getKeyCode(). |
| `event` | [KeyEvent](KeyEvent.md)!: Description of the key event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyMultiple

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyMultiple(
    keyCode: Int, 
    repeatCount: Int, 
    event: KeyEvent!
): Boolean
```

Default implementation of onKeyMultiple: always returns false (doesn't handle the event).

Key presses in software keyboards will generally NOT trigger this listener, although some may elect to do so in some situations. Do not rely on this to catch software key presses.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A key code that represents the button pressed, from KeyEvent. |
| `count` | Number of pairs as returned by event.getRepeatCount(). |
| `event` | [KeyEvent](KeyEvent.md)!: The KeyEvent object that defines the button action. |
| --- | --- |
| `repeatCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of times the action was made. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyPreIme

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyPreIme(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

Handle a key event before it is processed by any input method associated with the view hierarchy. This can be used to intercept key events in special situations before the IME consumes them; a typical example would be handling the BACK key to update the application's UI instead of allowing the IME to see it and close itself. Due to a bug, this function is not called for BACK key events on Android T and U, when the IME is shown.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value in event.getKeyCode(). |
| `event` | [KeyEvent](KeyEvent.md)!: Description of the key event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyShortcut(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

Called on the focused view when a key shortcut event is not handled. Override this method to implement local key shortcuts for the View. Key shortcuts can also be implemented by setting the setShortcut property of menu items.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value in event.getKeyCode(). |
| `event` | [KeyEvent](KeyEvent.md)!: Description of the key event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onKeyUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyUp(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

Default implementation of onKeyUp: perform clicking of the view when `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_CENTER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ENTER:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SPACE:kotlin.Int` is released.

Key presses in software keyboards will generally NOT trigger this listener, although some may elect to do so in some situations. Do not rely on this to catch software key presses.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A key code that represents the button pressed, from KeyEvent. |
| `event` | [KeyEvent](KeyEvent.md)!: The KeyEvent object that defines the button action. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If you handled the event, return true. If you want to allow the event to be handled by the next receiver, return false. |

### onPointerCaptureChange

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPointerCaptureChange(hasCapture: Boolean): Unit
```

Called when the window has just acquired or lost pointer capture. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `hasCapture` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the view now has pointerCapture, false otherwise. |

### onPopulateAccessibilityEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPopulateAccessibilityEvent(event: AccessibilityEvent!): Unit
```

Called from dispatchPopulateAccessibilityEvent giving a chance to this View to populate the accessibility event with its text content.

**Note:** This method should only be used with event.setText(). Avoid mutating other event state in this method. Instead, follow the practices described in dispatchPopulateAccessibilityEvent. In general, put UI metadata in the node for services to easily query, than in transient events.

Example: Adding formatted date string to an accessibility event in addition to the text added by the super implementation:

```kotlin
public void onPopulateAccessibilityEvent(AccessibilityEvent event) {
      super.onPopulateAccessibilityEvent(event);
      final int flags = DateUtils.FORMAT_SHOW_DATE | DateUtils.FORMAT_SHOW_WEEKDAY;
      String selectedDateUtterance = DateUtils.formatDateTime(mContext,
          mCurrentDate.getTimeInMillis(), flags);
      event.getText().add(selectedDateUtterance);
  }
```

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling setAccessibilityDelegate its onPopulateAccessibilityEvent is responsible for handling this call.

**Note:** Always call the super implementation before adding information to the event, in case the default implementation has basic information to add.
. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `event` | [AccessibilityEvent](../android.view.accessibility/AccessibilityEvent.md)!: The accessibility event which to populate. |

**See Also**

- sendAccessibilityEvent
- dispatchPopulateAccessibilityEvent

### onProvideAutofillStructure

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onProvideAutofillStructure(
    structure: ViewStructure!, 
    flags: Int
): Unit
```

Populates a ViewStructure to fullfil an autofill request.

The structure should contain at least the following properties:

- Autofill id (setAutofillId).
- Autofill type (setAutofillType).
- Autofill value (setAutofillValue).
- Whether the data is sensitive (setDataIsSensitive).

It's also recommended to set the following properties - the more properties the structure has, the higher the chances of an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` properly using the structure:

- Autofill hints (setAutofillHints).
- Autofill options (setAutofillOptions) when the view can only be filled with predefined values (typically used when the autofill type is `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_LIST:kotlin.Int`).
- Resource id (setId).
- Class name (setClassName).
- Content description (setContentDescription).
- Visual properties such as visibility (setVisibility), dimensions (setDimens), and opacity (setOpaque).
- For views representing text fields, text properties such as the text itself (setText), text hints (setHint, input type (setInputType),
- For views representing HTML nodes, its web domain (setWebDomain) and HTML properties ((setHtmlInfo).

The default implementation of this method already sets most of these properties based on related View methods (for example, the autofill id is set using getAutofillId, the autofill type set using getAutofillType, etc.), and views in the standard Android widgets library also override it to set their relevant properties (for example, `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` already sets the text properties), so it's recommended to only override this method (and call `super.onProvideAutofillStructure()`) when:

- The view contents does not include PII (Personally Identifiable Information), so it can call setDataIsSensitive passing `false`.
- The view can only be autofilled with predefined options, so it can call setAutofillOptions.

**Note:** The `left` and `top` values set in setDimens must be relative to the next isImportantForAutofill predecessor view included in the structure.

Views support the Autofill Framework mainly by:

- Providing the metadata defining what the view means and how it can be autofilled.
- Notifying the Android System when the view value changed by calling notifyValueChanged.
- Implementing the methods that autofill the view.

This method is responsible for the former; autofill is responsible for the latter.

| Parameters ||
|---|---|
| `structure` | [ViewStructure](ViewStructure.md)!: fill in with structured view data for autofill purposes. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): optional flags. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int`

### onProvideAutofillVirtualStructure

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onProvideAutofillVirtualStructure(
    structure: ViewStructure!, 
    flags: Int
): Unit
```

Populates a ViewStructure containing virtual children to fullfil an autofill request.

This method should be used when the view manages a virtual structure under this view. For example, a view that draws input fields using draw.

When implementing this method, subclasses must follow the rules below:

- Add virtual children by calling the newChild or asyncNewChild methods, where the `id` is an unique id identifying the children in the virtual structure.
- The children hierarchy can have multiple levels if necessary, but ideally it should exclude intermediate levels that are irrelevant for autofill; that would improve the autofill performance.
- Also implement autofill to autofill the virtual children.
- Set the autofill properties of the child structure as defined by onProvideAutofillStructure, using setAutofillId to set its autofill id.
- Call notifyViewEntered and/or notifyViewExited when the focused virtual child changed.
- Override isVisibleToUserForAutofill to allow the platform to query whether a given virtual view is visible to the user in order to support triggering save when all views of interest go away.
- Call notifyValueChanged when the value of a virtual child changed.
- Call notifyViewVisibilityChanged when the visibility of a virtual child changed.
- Call notifyViewClicked when a virtual child is clicked.
- Call commit when the autofill context of the view structure changed and the current context should be committed (for example, when the user tapped a `SUBMIT` button in an HTML page).
- Call cancel when the autofill context of the view structure changed and the current context should be canceled (for example, when the user tapped a `CANCEL` button in an HTML page).
- Provide ways for users to manually request autofill by calling requestAutofill.
- The `left` and `top` values set in setDimens must be relative to the next isImportantForAutofill predecessor view included in the structure.

Views with virtual children support the Autofill Framework mainly by:

- Providing the metadata defining what the virtual children mean and how they can be autofilled.
- Implementing the methods that autofill the virtual children.

This method is responsible for the former; autofill is responsible for the latter.

| Parameters ||
|---|---|
| `structure` | [ViewStructure](ViewStructure.md)!: fill in with virtual children data for autofill purposes. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): optional flags. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int`

### onProvideContentCaptureNodeProperties

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onProvideContentCaptureNodeProperties(properties: ContentCaptureNodeProperties): Unit
```

Populates the properties of this View for Content Capture version 2.

This method is called when a view that is eligible for content capture is initially registered and appeared on the screen, or when its properties are explicitly requested to be repopulated. The populated ContentCaptureNodeProperties is subsequently sent to the intelligence service through notifyNodeAppearedOrChanged.

The default implementation of this method computes and sets the most relevant properties, such as the layout bounds relative to the nearest content-capture-important parent, the parent's AutofillId, and the view's content description. Subclasses overriding this method should call the super implementation (`super.onProvideContentCaptureNodeProperties(properties)`) to populate these default properties, and then modify them as appropriate.

**Note for Virtual Views:**Views that host a virtual view structure (such as web pages) must only populate the node properties representing the host view itself and return immediately. They must subsequently report virtual child node events on the main (UI) thread by calling:

- notifyNodeAppearedOrChanged when virtual nodes appear or their properties change
- notifyNodeDisappeared when virtual nodes disappear

<br />

| Parameters ||
|---|---|
| `properties` | [ContentCaptureNodeProperties](../android.view.contentcapture/ContentCaptureNodeProperties.md): This value cannot be `null`. |

**See Also**

- getContentCaptureVersion
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_2:kotlin.Int`

### onProvideContentCaptureStructure

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onProvideContentCaptureStructure(
    structure: ViewStructure, 
    flags: Int
): Unit
```

Populates a ViewStructure for content capture.

This method is called after a view that is eligible for content capture (for example, if it isImportantForContentCapture, an intelligence service is enabled for the user, and the activity rendering the view is enabled for content capture) is laid out and is visible. The populated structure is then passed to the service through notifyViewAppeared.

The default implementation of this method sets the most relevant properties based on related View methods, and views in the standard Android widgets library also override it to set their relevant properties. Therefore, if overriding this method, it is recommended to call `super.onProvideContentCaptureStructure()`.

**Note:** views that manage a virtual structure under this view must populate just the node representing this view and return right away, then asynchronously report (not necessarily in the UI thread) when the children nodes appear, disappear or have their text changed by calling notifyViewAppeared, notifyViewDisappeared, and notifyViewTextChanged respectively. The structure for a child must be created using newVirtualViewStructure, and the `autofillId` for a child can be obtained either through `childStructure.getAutofillId()` or newAutofillId.

When the virtual view hierarchy represents a web page, you should also:

- Call getContentCaptureConditions to infer content capture events should be generate for that URL.
- Create a new ContentCaptureSession child for every HTML element that renders a new URL (like an `IFRAME`) and use that session to notify events from that subtree.

**Note:** the following methods of the `structure` will be ignored:

- setChildCount
- addChildCount
- getChildCount
- newChild
- asyncNewChild
- asyncCommit
- setWebDomain
- newHtmlInfoBuilder
- setHtmlInfo
- setDataIsSensitive
- setAlpha
- setElevation
- setTransformation

| Parameters ||
|---|---|
| `structure` | [ViewStructure](ViewStructure.md): This value cannot be `null`. |

### onProvideStructure

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onProvideStructure(structure: ViewStructure!): Unit
```

Called when assist structure is being retrieved from a view as part of onProvideAssistData.

| Parameters ||
|---|---|
| `structure` | [ViewStructure](ViewStructure.md)!: Fill in with structured view data. The default implementation fills in all data that can be inferred from the view itself. |

### onProvideVirtualStructure

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onProvideVirtualStructure(structure: ViewStructure!): Unit
```

Called when assist structure is being retrieved from a view as part of onProvideAssistData to generate additional virtual structure under this view. The default implementation uses getAccessibilityNodeProvider to try to generate this from the view's virtual accessibility nodes, if any. You can override this for a more optimal implementation providing this data.

### onReceiveContent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onReceiveContent(payload: ContentInfo): ContentInfo?
```

Implements the default behavior for receiving content for this type of view. The default view implementation is a no-op (returns the passed-in content without acting on it).

Widgets should override this method to define their default behavior for receiving content. Apps should setOnReceiveContentListener to provide app-specific handling for receiving content.

See setOnReceiveContentListener and performReceiveContent for more info.

| Parameters ||
|---|---|
| `payload` | [ContentInfo](ContentInfo.md): The content to insert and related metadata. This value cannot be `null`. |

| Return ||
|---|---|
| ContentInfo | The portion of the passed-in content that was not handled (may be all, some, or none of the passed-in content). This value may be `null`. |

### onResolvePointerIcon

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onResolvePointerIcon(
    event: MotionEvent!, 
    pointerIndex: Int
): PointerIcon!
```

Resolve the pointer icon that should be used for specified pointer in the motion event. The default implementation will resolve the pointer icon to one set using setPointerIcon for mouse devices. Subclasses may override this to customize the icon for the given pointer. For example, to always show the PointerIcon.TYPE_HANDWRITING icon for a stylus pointer, the event can be resolved in the following way: `
`

 @Override
 public PointerIcon onResolvePointerIcon(MotionEvent event, int pointerIndex) {
 final int toolType = event.getToolType(pointerIndex);
 if (!event.isFromSource(InputDevice.SOURCE_MOUSE)
 && event.isFromSource(InputDevice.SOURCE_STYLUS)
 && (toolType == MotionEvent.TOOL_TYPE_STYLUS
 || toolType == MotionEvent.TOOL_TYPE_ERASER)) {
| --- | --- |
 // Show this pointer icon only if this pointer is a stylus.
 return PointerIcon.getSystemIcon(mContext, PointerIcon.TYPE_HANDWRITING);
 }
 // Use the default logic for determining the pointer icon for other non-stylus pointers,
 // like for the mouse cursor.
 return super.onResolvePointerIcon(event, pointerIndex);
 }
 
`
`

<br />

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The MotionEvent that requires a pointer icon to be resolved for one of pointers. |
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the pointer in `event` for which to retrieve the PointerIcon. This will be between 0 and getPointerCount. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/PointerIcon!` | the pointer icon to use for specified pointer, or `null` if a pointer icon is not specified and the default icon should be used. |

**See Also**

- PointerIcon
- isStylusPointerIconEnabled

### onRtlPropertiesChanged

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onRtlPropertiesChanged(layoutDirection: Int): Unit
```

Called when any RTL property (layout direction or text direction or text alignment) has been changed. Subclasses need to override this method to take care of cached information that depends on the resolved layout direction, or to inform child views that inherit their layout direction. The default implementation does nothing.

| Parameters ||
|---|---|
| `layoutDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the direction of the layout. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LTR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_RTL:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LTR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_RTL:kotlin.Int`

### onScreenStateChanged

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onScreenStateChanged(screenState: Int): Unit
```

This method is called whenever the state of the screen this view is attached to changes. A state change will usually occurs when the screen turns on or off (whether it happens automatically or the user does it manually.)

| Parameters ||
|---|---|
| `screenState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new state of the screen. Can be either `https://developer.android.com/reference/kotlin/android/view/View#SCREEN_STATE_ON:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#SCREEN_STATE_OFF:kotlin.Int` |

### onScrollCaptureSearch

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onScrollCaptureSearch(
    localVisibleRect: Rect, 
    windowOffset: Point, 
    targets: Consumer<ScrollCaptureTarget!>
): Unit
```

Called when scroll capture is requested, to search for appropriate content to scroll. If applicable, this view adds itself to the provided list for consideration, subject to the flags set by setScrollCaptureHint.

| Parameters ||
|---|---|
| `localVisibleRect` | [Rect](../android.graphics/Rect.md): the local visible rect of this view. This value cannot be `null`. |
| `windowOffset` | [Point](../android.graphics/Point.md): the offset of localVisibleRect within the window. This value cannot be `null`. |
| `targets` | [Consumer](../java.util.function/Consumer.md)\< [ScrollCaptureTarget](ScrollCaptureTarget.md)!\>: accepts potential scroll capture targets; accept may be called zero or more times on the calling thread before onScrollCaptureSearch returns. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this view is not attached to a window |

### onStartTemporaryDetach

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStartTemporaryDetach(): Unit
```

This is called when a container is going to temporarily detach a child, with detachViewFromParent. It will either be followed by onFinishTemporaryDetach or onDetachedFromWindow when the container is done.

### onTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTouchEvent(event: MotionEvent!): Boolean
```

Implement this method to handle pointer events.

This method is called to handle motion events where pointers are down on the view. For example, this could include touchscreen touches, stylus touches, or click-and-drag events from a mouse. However, it is not called for motion events that do not involve pointers being down, such as hover events or mouse scroll wheel movements.

If this method is used to detect click actions, it is recommended that the actions be performed by implementing and calling performClick. This will ensure consistent system behavior, including:

- obeying click sound preferences
- dispatching OnClickListener calls
- handling `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLICK:kotlin.Int` when accessibility features are enabled

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The motion event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled, false otherwise. |

### onTrackballEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTrackballEvent(event: MotionEvent!): Boolean
```

Implement this method to handle trackball motion events.

The *relative* movement of the trackball since the last event can be retrieve with android.view.MotionEvent#getX and android.view.MotionEvent#getY. These are normalized so that a movement of 1 corresponds to the user pressing one DPAD key (so they will often be fractional values, representing the more fine-grained movement information available from a trackball).

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The motion event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled, false otherwise. |

### onViewTranslationResponse

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onViewTranslationResponse(response: ViewTranslationResponse): Unit
```

Called when the content from onCreateViewTranslationRequest had been translated by the TranslationService. The ViewTranslationResponse should be saved here so that the ViewTranslationResponse can be used to display the translation when the system calls onShowTranslation.

The default implementation will set the ViewTranslationResponse that can be get from getViewTranslationResponse.

| Parameters ||
|---|---|
| `response` | [ViewTranslationResponse](../android.view.translation/ViewTranslationResponse.md): a ViewTranslationResponse that contains the translated information which can be shown in the view. This value cannot be `null`. |

### onVirtualViewTranslationResponses

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onVirtualViewTranslationResponses(response: LongSparseArray<ViewTranslationResponse!>): Unit
```

Called when the content from onCreateVirtualViewTranslationRequests had been translated by the TranslationService.

The default implementation does nothing.

| Parameters ||
|---|---|
| `response` | [LongSparseArray](../android.util/LongSparseArray.md)\< [ViewTranslationResponse](../android.view.translation/ViewTranslationResponse.md)!\>: a ViewTranslationResponse SparseArray for the request that send by onCreateVirtualViewTranslationRequests that contains the translated information which can be shown in the view. The key of SparseArray is the virtual child ids. This value cannot be `null`. |

### onVisibilityAggregated

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onVisibilityAggregated(isVisible: Boolean): Unit
```

Called when the user-visibility of this View is potentially affected by a change to this view itself, an ancestor view or the window this view is attached to. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `isVisible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if this view and all of its ancestors are `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` and this view's window is also visible |

### onWindowFocusChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onWindowFocusChanged(hasWindowFocus: Boolean): Unit
```

Called when the window containing this view gains or loses focus. Note that this is separate from view focus: to receive key events, both your view and its window must have focus. If a window is displayed on top of yours that takes input focus, then your own window will lose focus but the view focus will remain unchanged.

| Parameters ||
|---|---|
| `hasWindowFocus` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the window containing this view now has focus, false otherwise. |

### onWindowSystemUiVisibilityChanged

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onWindowSystemUiVisibilityChanged(visible: Int): Unit
```

**Deprecated:** *SystemUiVisibility flags are deprecated. Use WindowInsetsController instead.*

Override to find out when the window's requested system UI visibility has changed, that is the value returned by getWindowSystemUiVisibility. This is different from the callbacks received through setOnSystemUiVisibilityChangeListener in that this is only telling you about the local request of the window, not the actual values applied by the system.

### performAccessibilityAction

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performAccessibilityAction(
    action: Int, 
    arguments: Bundle?
): Boolean
```

Performs the specified accessibility action on the view. For possible accessibility actions look at AccessibilityNodeInfo.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling setAccessibilityDelegate its performAccessibilityAction is responsible for handling this call.

The default implementation will delegate `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SCROLL_BACKWARD:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SCROLL_FORWARD:kotlin.Int` to nested scrolling parents if isNestedScrollingEnabled on this view.

**Note:** Avoid setting accessibility focus with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ACCESSIBILITY_FOCUS:kotlin.Int`. This is intended to be controlled by screen readers. Apps changing focus can confuse screen readers, so the resulting behavior can vary by device and screen reader version.

| Parameters ||
|---|---|
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The action to perform. |
| `arguments` | [Bundle](../android.os/Bundle.md)?: Optional action arguments. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the action was performed. |

### performClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performClick(): Boolean
```

Call this view's OnClickListener, if it is defined. Performs all normal actions associated with clicking: reporting accessibility event, playing a sound, etc.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True there was an assigned OnClickListener that was called, false otherwise is returned. |

### performContextClick

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performContextClick(): Boolean
```

Call this view's OnContextClickListener, if it is defined.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if there was an assigned OnContextClickListener that consumed the event, false otherwise. |

### performContextClick

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performContextClick(
    x: Float, 
    y: Float
): Boolean
```

Call this view's OnContextClickListener, if it is defined.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the x coordinate of the context click |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the y coordinate of the context click |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if there was an assigned OnContextClickListener that consumed the event, false otherwise. |

### performHapticFeedback

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performHapticFeedback(request: HapticFeedbackRequest): Boolean
```

Like performHapticFeedback, but takes a `https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.html#`.

Using a `https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.html#` allows you to make more elaborate haptic feedback requests, including setting the usage type for the requested feedback.

Specifying the usage type for your feedback allows the system to understand the context of the feedback better, and tune the haptic accordingly. When not specifying the usage type for the feedback request, or when using the other performHapticFeedback APIs, the system will do a best guess of the vibration usage based on the constant.

See `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#` to learn more about vibration usages. The usage provided for this API must be of `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_CLASS_FEEDBACK:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_UNKNOWN:kotlin.Int`. Otherwise, the haptic feedback will not be played. If `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_UNKNOWN:kotlin.Int` is used, the system will do a best guess of the vibration usage based on the constant.

Note that, if you will be calling this API repeatedly and your `https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.html#` does not change across these repeated calls, it is recommended that you create, cache, and reuse the request object to avoid the costs of repeated object creation and garbage collection.

| Parameters ||
|---|---|
| `request` | [HapticFeedbackRequest](../android.os.vibrator/HapticFeedbackRequest.md): the `https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.html#` encapsulating the request for haptic. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `false` if isHapticFeedbackEnabled is `false`, or this View is not attached to a visible window, or the vibration usage in the provided request is not valid (i.e. neither has `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_CLASS_FEEDBACK:kotlin.Int` nor is `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_UNKNOWN:kotlin.Int`); otherwise, `true`, indicating that the haptic feedback request has been sent to the system. Note that `true` could be returned but no vibration may be produced if the service decides that the device's states do not allow for this haptic feedback (for example, the user disabled vibrations for this usage). |

**See Also**

- getUsage
- getUsageClass

### performHapticFeedback

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performHapticFeedback(feedbackConstant: Int): Boolean
```

BZZZTT!!1!

Provide haptic feedback to the user for this view.

The framework will provide haptic feedback for some built in actions, such as long presses, but you may wish to provide feedback for your own widget.

The feedback will only be performed if isHapticFeedbackEnabled is true.

| Parameters ||
|---|---|
| `feedbackConstant` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of the constants defined in HapticFeedbackConstants |

### performHapticFeedback

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performHapticFeedback(
    feedbackConstant: Int, 
    flags: Int
): Boolean
```

BZZZTT!!1!

Like performHapticFeedback, with additional options.

| Parameters ||
|---|---|
| `feedbackConstant` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of the constants defined in HapticFeedbackConstants |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags as per HapticFeedbackConstants. |

### performLongClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performLongClick(): Boolean
```

Calls this view's OnLongClickListener, if it is defined. Invokes the context menu if the OnLongClickListener did not consume the event.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if one of the above receivers consumed the event, `false` otherwise |

### performLongClick

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performLongClick(
    x: Float, 
    y: Float
): Boolean
```

Calls this view's OnLongClickListener, if it is defined. Invokes the context menu if the OnLongClickListener did not consume the event, anchoring it to an (x,y) coordinate.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): x coordinate of the anchoring touch event, or `https://developer.android.com/reference/kotlin/java/lang/Float.html#NaN:kotlin.Float` to disable anchoring |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): y coordinate of the anchoring touch event, or `https://developer.android.com/reference/kotlin/java/lang/Float.html#NaN:kotlin.Float` to disable anchoring |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if one of the above receivers consumed the event, `false` otherwise |

### performReceiveContent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performReceiveContent(payload: ContentInfo): ContentInfo?
```

Receives the given content. If no listener is set, invokes onReceiveContent. If a listener is setOnReceiveContentListener, invokes the listener instead; if the listener returns a non-null result, invokes onReceiveContent to handle it.

| Parameters ||
|---|---|
| `payload` | [ContentInfo](ContentInfo.md): The content to insert and related metadata. This value cannot be `null`. |

| Return ||
|---|---|
| ContentInfo | The portion of the passed-in content that was not accepted (may be all, some, or none of the passed-in content). |

### playSoundEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun playSoundEffect(soundConstant: Int): Unit
```

Play a sound effect for this view.

The framework will play sound effects for some built in actions, such as clicking, but you may wish to play these effects in your widget, for instance, for internal navigation.

The sound effect will only be played if sound effects are enabled by the user, and isSoundEffectsEnabled is true.

| Parameters ||
|---|---|
| `soundConstant` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of the constants defined in SoundEffectConstants. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_REPEAT_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_REPEAT_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_REPEAT_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_REPEAT_DOWN:kotlin.Int` |

### post

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun post(action: Runnable!): Boolean
```

Causes the Runnable to be added to the message queue. The runnable will be run on the user interface thread.

| Parameters ||
|---|---|
| `action` | [Runnable](../java.lang/Runnable.md)!: The Runnable that will be executed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the Runnable was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. |

**See Also**

- postDelayed
- removeCallbacks

### postDelayed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun postDelayed(
    action: Runnable!, 
    delayMillis: Long
): Boolean
```

Causes the Runnable to be added to the message queue, to be run after the specified amount of time elapses. The runnable will be run on the user interface thread.

| Parameters ||
|---|---|
| `action` | [Runnable](../java.lang/Runnable.md)!: The Runnable that will be executed. |
| `delayMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The delay (in milliseconds) until the Runnable will be executed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the Runnable was successfully placed in to the message queue. Returns false on failure, usually because the looper processing the message queue is exiting. Note that a result of true does not mean the Runnable will be processed -- if the looper is quit before the delivery time of the message occurs then the message will be dropped. |

**See Also**

- post
- removeCallbacks

### postInvalidate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun postInvalidate(): Unit
```

Cause an invalidate to happen on a subsequent cycle through the event loop. Use this to invalidate the View from a non-UI thread.

This method can be invoked from outside of the UI thread only when this View is attached to a window.
**See Also**

- invalidate
- postInvalidateDelayed

### postInvalidate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun postInvalidate(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Cause an invalidate of the specified area to happen on a subsequent cycle through the event loop. Use this to invalidate the View from a non-UI thread.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

| Parameters ||
|---|---|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The left coordinate of the rectangle to invalidate. |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The top coordinate of the rectangle to invalidate. |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The right coordinate of the rectangle to invalidate. |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The bottom coordinate of the rectangle to invalidate. |

**See Also**

- invalidate
- invalidate
- postInvalidateDelayed

### postInvalidateDelayed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun postInvalidateDelayed(delayMilliseconds: Long): Unit
```

Cause an invalidate to happen on a subsequent cycle through the event loop. Waits for the specified amount of time.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

| Parameters ||
|---|---|
| `delayMilliseconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the duration in milliseconds to delay the invalidation by |

**See Also**

- invalidate
- postInvalidate

### postInvalidateDelayed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun postInvalidateDelayed(
    delayMilliseconds: Long, 
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Cause an invalidate of the specified area to happen on a subsequent cycle through the event loop. Waits for the specified amount of time.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

| Parameters ||
|---|---|
| `delayMilliseconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the duration in milliseconds to delay the invalidation by |
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The left coordinate of the rectangle to invalidate. |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The top coordinate of the rectangle to invalidate. |
| --- | --- |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The right coordinate of the rectangle to invalidate. |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The bottom coordinate of the rectangle to invalidate. |

**See Also**

- invalidate
- invalidate
- postInvalidate

### postInvalidateOnAnimation

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun postInvalidateOnAnimation(): Unit
```

Cause an invalidate to happen on the next animation time step, typically the next display frame.

This method can be invoked from outside of the UI thread only when this View is attached to a window.
**See Also**

- invalidate

### postInvalidateOnAnimation

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun postInvalidateOnAnimation(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Cause an invalidate of the specified area to happen on the next animation time step, typically the next display frame.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

| Parameters ||
|---|---|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The left coordinate of the rectangle to invalidate. |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The top coordinate of the rectangle to invalidate. |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The right coordinate of the rectangle to invalidate. |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The bottom coordinate of the rectangle to invalidate. |

**See Also**

- invalidate
- invalidate

### postOnAnimation

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun postOnAnimation(action: Runnable!): Unit
```

Causes the Runnable to execute on the next animation time step. The runnable will be run on the user interface thread.

| Parameters ||
|---|---|
| `action` | [Runnable](../java.lang/Runnable.md)!: The Runnable that will be executed. |

**See Also**

- postOnAnimationDelayed
- removeCallbacks

### postOnAnimationDelayed

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun postOnAnimationDelayed(
    action: Runnable!, 
    delayMillis: Long
): Unit
```

Causes the Runnable to execute on the next animation time step, after the specified amount of time elapses. The runnable will be run on the user interface thread.

| Parameters ||
|---|---|
| `action` | [Runnable](../java.lang/Runnable.md)!: The Runnable that will be executed. |
| `delayMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The delay (in milliseconds) until the Runnable will be executed. |

**See Also**

- postOnAnimation
- removeCallbacks

### refreshDrawableState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun refreshDrawableState(): Unit
```

Call this to force a view to update its drawable state. This will cause drawableStateChanged to be called on this view. Views that are interested in the new state should call getDrawableState.
**See Also**

- drawableStateChanged
- getDrawableState

### registerCalledFromWrongThreadListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun registerCalledFromWrongThreadListener(listener: View.CalledFromWrongThreadListener): Unit
```

Registers a listener that is notified when a View API is called from the wrong thread.

Most View APIs should only be called on the UI thread, and will throw a `CalledFromWrongThreadException` if they are called from the wrong thread. View APIs that throw `CalledFromWrongThreadException` will not notify registered listeners.

For certain APIs, if they are called on the wrong thread then an exception may not be thrown, subject to App Compatibility settings. Instead, applications may be notified when a call to such an API is made from the wrong thread by registering a `https://developer.android.com/reference/kotlin/android/view/View.CalledFromWrongThreadListener` using this method.

| Parameters ||
|---|---|
| `listener` | [View.CalledFromWrongThreadListener](../android/view/View.CalledFromWrongThreadListener.md): The listener to register. This value cannot be `null`. |

**See Also**

- unregisterCalledFromWrongThreadListener

### releasePointerCapture

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun releasePointerCapture(): Unit
```

Releases the pointer capture.

If the window does not have pointer capture, this call will do nothing.
**See Also**

- requestPointerCapture
- hasPointerCapture
- onPointerCaptureChange

### removeCallbacks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeCallbacks(action: Runnable!): Boolean
```

Removes the specified Runnable from the message queue.

| Parameters ||
|---|---|
| `action` | [Runnable](../java.lang/Runnable.md)!: The Runnable to remove from the message handling queue |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this view could ask the Handler to remove the Runnable, false otherwise. When the returned value is true, the Runnable may or may not have been actually removed from the message queue (for instance, if the Runnable was not in the queue already.) |

**See Also**

- post
- postDelayed
- postOnAnimation
- postOnAnimationDelayed

### removeOnAttachStateChangeListener

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnAttachStateChangeListener(listener: View.OnAttachStateChangeListener!): Unit
```

Remove a listener for attach state changes. The listener will receive no further notification of window attach/detach events.

| Parameters ||
|---|---|
| `listener` | [View.OnAttachStateChangeListener](../android/view/View.OnAttachStateChangeListener.md)!: Listener to remove |

**See Also**

- addOnAttachStateChangeListener

### removeOnLayoutChangeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnLayoutChangeListener(listener: View.OnLayoutChangeListener!): Unit
```

Remove a listener for layout changes.

| Parameters ||
|---|---|
| `listener` | [View.OnLayoutChangeListener](../android/view/View.OnLayoutChangeListener.md)!: The listener for layout bounds change. |

### removeOnUnhandledKeyEventListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnUnhandledKeyEventListener(listener: View.OnUnhandledKeyEventListener!): Unit
```

Removes a listener which will receive unhandled KeyEvents. This must be called on the UI thread.

| Parameters ||
|---|---|
| `listener` | [View.OnUnhandledKeyEventListener](../android/view/View.OnUnhandledKeyEventListener.md)!: a receiver of unhandled KeyEvents. |

**See Also**

- addOnUnhandledKeyEventListener

### reportAppJankStats

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reportAppJankStats(appJankStats: AppJankStats): Unit
```

Called from apps when they want to report jank stats to the system.

| Parameters ||
|---|---|
| `appJankStats` | [AppJankStats](../android.app.jank/AppJankStats.md): the stats that will be merged with the stats collected by the system. This value cannot be `null`. |

### requestApplyInsets

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestApplyInsets(): Unit
```

Ask that a new dispatch of onApplyWindowInsets be performed.

### requestFitSystemWindows

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestFitSystemWindows(): Unit
```

**Deprecated:** *Use requestApplyInsets for newer platform versions.*

Ask that a new dispatch of fitSystemWindows be performed.

### requestFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestFocus(): Boolean
```

Call this to try to give focus to a specific view or to one of its descendants. A view will not actually take focus if it is not focusable (isFocusable returns false), or if it can't be focused due to other conditions (not focusable in touch mode (isFocusableInTouchMode) while the device is in touch mode, not visible, not enabled, or has no size). See also focusSearch, which is what you call to say that you have focus, and you want your parent to look for the next one. This is equivalent to calling requestFocus with arguments `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` and `null`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether this view or one of its descendants actually took focus. |

### requestFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestFocus(direction: Int): Boolean
```

Call this to try to give focus to a specific view or to one of its descendants and give it a hint about what direction focus is heading. A view will not actually take focus if it is not focusable (isFocusable returns false), or if it is focusable and it is not focusable in touch mode (isFocusableInTouchMode) while the device is in touch mode. See also focusSearch, which is what you call to say that you have focus, and you want your parent to look for the next one. This is equivalent to calling requestFocus with `null` set for the previously focused rectangle.

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of FOCUS_UP, FOCUS_DOWN, FOCUS_LEFT, and FOCUS_RIGHT |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether this view or one of its descendants actually took focus. |

### requestFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestFocus(
    direction: Int, 
    previouslyFocusedRect: Rect!
): Boolean
```

Call this to try to give focus to a specific view or to one of its descendants and give it hints about the direction and a specific rectangle that the focus is coming from. The rectangle can help give larger views a finer grained hint about where focus is coming from, and therefore, where to show selection, or forward focus change internally. A view will not actually take focus if it is not focusable (isFocusable returns false), or if it is focusable and it is not focusable in touch mode (isFocusableInTouchMode) while the device is in touch mode. A View will not take focus if it is not visible. A View will not take focus if one of its parents has getDescendantFocusability equal to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_BLOCK_DESCENDANTS:kotlin.Int`. See also focusSearch, which is what you call to say that you have focus, and you want your parent to look for the next one. You may wish to override this method if your custom View has an internal View that it wishes to forward the request to.

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of FOCUS_UP, FOCUS_DOWN, FOCUS_LEFT, and FOCUS_RIGHT |
| `previouslyFocusedRect` | [Rect](../android.graphics/Rect.md)!: The rectangle (in this View's coordinate system) to give a finer grained hint about where focus is coming from. May be null if there is no hint. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether this view or one of its descendants actually took focus. |

### requestFocusFromTouch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestFocusFromTouch(): Boolean
```

Call this to try to give focus to a specific view or to one of its descendants. This is a special variant of requestFocus that will allow views that are not focusable in touch mode to request focus when they are touched.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether this view or one of its descendants actually took focus. |

**See Also**

- isInTouchMode

### requestLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestLayout(): Unit
```

Call this when something has changed which has invalidated the layout of this view. This will schedule a layout pass of the view tree. This should not be called while the view hierarchy is currently in a layout pass (isInLayout. If layout is happening, the request may be honored at the end of the current layout pass (and then layout will run again) or after the current frame is drawn and the next layout occurs.

Subclasses which override this method should call the superclass method to handle possible request-during-layout errors correctly.
. 
If you override this method you *must* call through to the superclass implementation.

### requestPointerCapture

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestPointerCapture(): Unit
```

Requests pointer capture in relative mode.

Equivalent to calling requestPointerCapture with `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_RELATIVE:kotlin.Int`.
**See Also**

- releasePointerCapture
- hasPointerCapture
- onPointerCaptureChange

### requestPointerCapture

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestPointerCapture(mode: Int): Unit
```

Requests pointer capture in the specified mode.

When the window has pointer capture, the mouse pointer icon will disappear and will not change its position. Enabling pointer capture will change the behavior of input devices in the following ways:

- Events from a mouse will be delivered with the source `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_MOUSE_RELATIVE:kotlin.Int`, and relative position changes will be available through android.view.MotionEvent#getX and android.view.MotionEvent#getY.
- Events from a touchpad (also known as a trackpad) will be delivered according to the chosen pointer capture mode. See `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_RELATIVE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_ABSOLUTE:kotlin.Int` for details.
- Events from other types of devices, such as touchscreens, will not be affected.

Pointer ballistics curves and the user's pointer speed settings will not be applied in this mode.

When pointer capture changes, connected mouse and touchpad devices may be reconfigured, and their properties (such as their sources or motion ranges) may change. Use an `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.InputDeviceListener.html#` to be notified when a device changes (which may happen after enabling or disabling pointer capture), and use getDevice to get the updated InputDevice.

Events captured through pointer capture will be dispatched to onCapturedPointer if an `https://developer.android.com/reference/kotlin/android/view/View.OnCapturedPointerListener` is set, and otherwise to onCapturedPointerEvent.

If the window already has pointer capture in the same mode, this call does nothing. If it already has pointer capture in a different mode, it will transition to the new mode.

The capture may be released through releasePointerCapture, or will be lost automatically when the window loses focus.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The mode in which to capture the pointer, which determines how events from touchpads are delivered. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_UNCAPTURED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_ABSOLUTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_RELATIVE:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_RELATIVE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_ABSOLUTE:kotlin.Int`
- releasePointerCapture
- hasPointerCapture
- onPointerCaptureChange

### requestRectangleOnScreen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestRectangleOnScreen(rectangle: Rect!): Boolean
```

Request that a rectangle of this view be visible on the screen, scrolling if necessary just enough.

A View should call this if it maintains some notion of which part of its content is interesting. For example, a text editing view should call this when its cursor moves.

The Rectangle passed into this method should be in the View's content coordinate space. It should not be affected by which part of the View is currently visible or its scroll position.

| Parameters ||
|---|---|
| `rectangle` | [Rect](../android.graphics/Rect.md)!: The rectangle in the View's content coordinate space |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether any parent scrolled. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SHOW_ON_SCREEN:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- requestRectangleOnScreen

### requestRectangleOnScreen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestRectangleOnScreen(
    rectangle: Rect!, 
    immediate: Boolean
): Boolean
```

Request that a rectangle of this view be visible on the screen, scrolling if necessary just enough.

A View should call this if it maintains some notion of which part of its content is interesting. For example, a text editing view should call this when its cursor moves.

The Rectangle passed into this method should be in the View's content coordinate space. It should not be affected by which part of the View is currently visible or its scroll position.

When `immediate` is set to true, scrolling will not be animated.

| Parameters ||
|---|---|
| `rectangle` | [Rect](../android.graphics/Rect.md)!: The rectangle in the View's content coordinate space |
| `immediate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True to forbid animated scrolling, false otherwise |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether any parent scrolled. |

**See Also**

- requestRectangleOnScreen

### requestRectangleOnScreen

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestRectangleOnScreen(
    rectangle: Rect, 
    immediate: Boolean, 
    source: Int
): Boolean
```

Request that a rectangle of this view be visible on the screen, scrolling if necessary just enough.

A View should call this if it maintains some notion of which part of its content is interesting. For example, a text editing view should call this when its cursor moves.

The Rectangle passed into this method should be in the View's content coordinate space. It should not be affected by which part of the View is currently visible or its scroll position.

When `immediate` is set to true, scrolling will not be animated.

The `source` parameter is used to differentiate behaviors of certain system features, like focus-following with display magnification, based on user preferences and the source of requests to show content on-screen. Callers are encouraged to provide one of the following request sources, when applicable, instead of using requestRectangleOnScreen or requestRectangleOnScreen:

1. `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY:kotlin.Int`
2. `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR:kotlin.Int`
3. `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS:kotlin.Int`

| Parameters ||
|---|---|
| `rectangle` | [Rect](../android.graphics/Rect.md): The rectangle in the View's content coordinate space. This value cannot be `null`. |
| `immediate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True to forbid animated scrolling, false otherwise |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of user interaction that requested this rectangle. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether any parent scrolled. |

### requestUnbufferedDispatch

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestUnbufferedDispatch(event: MotionEvent!): Unit
```

Request unbuffered dispatch of the given stream of MotionEvents to this View. Until this View receives a corresponding `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_UP:kotlin.Int`, ask that the input system not batch MotionEvents but instead deliver them as soon as they're available. This method should only be called for touch events.

This API is not intended for most applications. Buffered dispatch provides many of benefits, and just requesting unbuffered dispatch on most MotionEvent streams will not improve your input latency. Side effects include: increased latency, jittery scrolls and inability to take advantage of system resampling. Talk to your input professional to see if requestUnbufferedDispatch is right for you.
To receive unbuffered events for arbitrary input device source classes, use requestUnbufferedDispatch, **See Also**

- requestUnbufferedDispatch

### requestUnbufferedDispatch

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestUnbufferedDispatch(source: Int): Unit
```

Request unbuffered dispatch of the given event source class to this view. This is similar to requestUnbufferedDispatch, but does not automatically terminate, and allows the specification of arbitrary input source classes.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, calling this method will not result in any behavioral changes when this View is not attached to a window.

| Parameters ||
|---|---|
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The combined input source class to request unbuffered dispatch for. All events coming from these source classes will not be buffered. Set to `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_NONE:kotlin.Int` in order to return to default behaviour. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_BUTTON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_POINTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_TRACKBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_POSITION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_JOYSTICK:kotlin.Int` |

**See Also**

- requestUnbufferedDispatch

### requireViewById

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : View!> requireViewById(id: Int): T
```

Finds the first descendant view with the given ID, the view itself if the ID matches getId, or throws an IllegalArgumentException if the ID is invalid or there is no matching view in the hierarchy.

**Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID to search for |

| Return ||
|---|---|
| `T` | a view with given ID. This value cannot be `null`. |

**See Also**

- findViewById

### resetPivot

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resetPivot(): Unit
```

Clears any pivot previously set by a call to setPivotX or setPivotY. After calling this isPivotSet will be false and the pivot used for rotation will return to default of being centered on the view.

### resolveSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun resolveSize(
    size: Int, 
    measureSpec: Int
): Int
```

Version of resolveSizeAndState returning only the `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` bits of the result.

### resolveSizeAndState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun resolveSizeAndState(
    size: Int, 
    measureSpec: Int, 
    childMeasuredState: Int
): Int
```

Utility to reconcile a desired size and state, with constraints imposed by a MeasureSpec. Will take the desired size, unless a different size is imposed by the constraints. The returned value is a compound integer, with the resolved size in the `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` bits and optionally the bit `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_TOO_SMALL:kotlin.Int` set if the resulting size is smaller than the size the view wants to be.

| Parameters ||
|---|---|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): How big the view wants to be. |
| `measureSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Constraints imposed by the parent. |
| `childMeasuredState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Size information bit mask for the view's children. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Size information bit mask as defined by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_TOO_SMALL:kotlin.Int`. |

### restoreDefaultFocus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun restoreDefaultFocus(): Boolean
```

Gives focus to the default-focus view in the view hierarchy that has this view as a root. If the default-focus view cannot be found, falls back to calling requestFocus.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether this view or one of its descendants actually took focus |

### restoreHierarchyState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun restoreHierarchyState(container: SparseArray<Parcelable!>!): Unit
```

Restore this view hierarchy's frozen state from the given container.

| Parameters ||
|---|---|
| `container` | [SparseArray](../android.util/SparseArray.md)\< [Parcelable](../android.os/Parcelable.md)!\>!: The SparseArray which holds previously frozen states. |

**See Also**

- saveHierarchyState
- dispatchRestoreInstanceState
- onRestoreInstanceState

### saveAttributeDataForStyleable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun saveAttributeDataForStyleable(
    context: Context, 
    styleable: IntArray, 
    attrs: AttributeSet?, 
    t: TypedArray, 
    defStyleAttr: Int, 
    defStyleRes: Int
): Unit
```

Stores debugging information about attributes. This should be called in a constructor by every custom View that uses a custom styleable. If the custom view does not call it, then the custom attributes used by this view will not be visible in layout inspection tools.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): Context under which this view is created. This value cannot be `null`. |
| `styleable` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): A reference to styleable array R.styleable.Foo. This value cannot be `null`. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)?: AttributeSet used to construct this view. This value may be `null`. |
| --- | --- |
| `t` | [TypedArray](../android.content.res/TypedArray.md): Resolved `https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` returned by a call to obtainAttributes. This value cannot be `null`. |
| `defStyleAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Default style attribute passed into the view constructor. |
| `defStyleRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Default style resource passed into the view constructor. |
| --- | --- |

### saveHierarchyState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun saveHierarchyState(container: SparseArray<Parcelable!>!): Unit
```

Store this view hierarchy's frozen state into the given container.

| Parameters ||
|---|---|
| `container` | [SparseArray](../android.util/SparseArray.md)\< [Parcelable](../android.os/Parcelable.md)!\>!: The SparseArray in which to save the view's state. |

**See Also**

- restoreHierarchyState
- dispatchSaveInstanceState
- onSaveInstanceState

### scheduleDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun scheduleDrawable(
    who: Drawable, 
    what: Runnable, 
    when: Long
): Unit
```

Schedules an action on a drawable to occur at a specified time.

| Parameters ||
|---|---|
| `who` | [Drawable](../android.graphics.drawable/Drawable.md): the recipient of the action. This value cannot be `null`. |
| `what` | [Runnable](../java.lang/Runnable.md): the action to run on the drawable. This value cannot be `null`. |
| `when` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the time at which the action must occur. Uses the uptimeMillis timebase. |
| --- | --- |

### scrollBy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun scrollBy(
    x: Int, 
    y: Int
): Unit
```

Move the scrolled position of your view. This will cause a call to onScrollChanged and the view will be invalidated.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the amount of pixels to scroll by horizontally |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the amount of pixels to scroll by vertically |

### scrollTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun scrollTo(
    x: Int, 
    y: Int
): Unit
```

Set the scrolled position of your view. This will cause a call to onScrollChanged and the view will be invalidated.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the x position to scroll to |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the y position to scroll to |

### sendAccessibilityEvent

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendAccessibilityEvent(eventType: Int): Unit
```

Sends an accessibility event of the given type. If accessibility is not enabled this method has no effect. The default implementation calls onInitializeAccessibilityEvent first to populate information about the event source (this View), then calls dispatchPopulateAccessibilityEvent to populate the text content of the event source including its descendants, then for events type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_SCROLLED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` with subtype `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION:kotlin.Int`, throttle the events, and last calls requestSendAccessibilityEvent on its parent to request sending of the event to interested parties.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling setAccessibilityDelegate its sendAccessibilityEvent is responsible for handling this call.

If this view uses AccessibilityNodeProvider to provide virtual view hierarchy rooted at this view, this method should not be called to send events from virtual children because it will populate the events with wrong information and the events should be throttled per child instead at the virtual root level. To send events from virtual children, call requestSendAccessibilityEvent on the view's parent to request sending of the event to interested parties.

| Parameters ||
|---|---|
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of the event to send, as defined by several types from AccessibilityEvent, such as `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_CLICKED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_ENTER:kotlin.Int`. |

**See Also**

- onInitializeAccessibilityEvent
- dispatchPopulateAccessibilityEvent
- requestSendAccessibilityEvent
- `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate`

### sendAccessibilityEventUnchecked

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendAccessibilityEventUnchecked(event: AccessibilityEvent!): Unit
```

This method behaves exactly as sendAccessibilityEvent but takes as an argument an empty AccessibilityEvent and does not perform a check whether accessibility is enabled.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling setAccessibilityDelegate its sendAccessibilityEventUnchecked is responsible for handling this call.

| Parameters ||
|---|---|
| `event` | [AccessibilityEvent](../android.view.accessibility/AccessibilityEvent.md)!: The event to send. |

**See Also**

- sendAccessibilityEvent

### setAccessibilityDataSensitive

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccessibilityDataSensitive(accessibilityDataSensitive: Int): Unit
```

Specifies whether this view should only allow interactions from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s with the isAccessibilityTool property set to true.

| Parameters ||
|---|---|
| `accessibilityDataSensitive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_YES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_NO:kotlin.Int` |

### setAccessibilityDelegate

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccessibilityDelegate(delegate: View.AccessibilityDelegate?): Unit
```

Sets a delegate for implementing accessibility support via composition (as opposed to inheritance). For more details, see `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate`.

**Note:** On platform versions prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, delegate methods on views in the `android.widget.*` package are called *before* host methods. This prevents certain properties such as class name from being modified by overriding onInitializeAccessibilityNodeInfo, as any changes will be overwritten by the host class.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, delegate methods are called *after* host methods, which all properties to be modified without being overwritten by the host class.

| Parameters ||
|---|---|
| `delegate` | [View.AccessibilityDelegate](../android/view/View.AccessibilityDelegate.md)?: the object to which accessibility method calls should be delegated. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate`

### setAccessibilityHeading

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccessibilityHeading(isHeading: Boolean): Unit
```

Set if view is a heading for a section of content for accessibility purposes.

Users of some accessibility services can choose to navigate between headings instead of between paragraphs, words, etc. Apps that provide headings on sections of text can help the text navigation experience.

**Note:** Use androidx.core.view.ViewCompat#setAccessibilityHeading(android.view.View,boolean) for backwards-compatibility.

| Parameters ||
|---|---|
| `isHeading` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the view is a heading, `false` otherwise. |

### setAccessibilityLiveRegion

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccessibilityLiveRegion(mode: Int): Unit
```

Sets the live region mode for this view. This indicates to accessibility services whether they should automatically notify the user about changes to the view's content description or text, or to the content descriptions or text of the view's children (where applicable).

Different priority levels are available:

- `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_POLITE:kotlin.Int`: Indicates that updates to the region should be presented to the user. Suitable in most cases for prominent updates within app content that don't require the user's immediate attention.
- `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_ASSERTIVE:kotlin.Int`: Indicates that updates to the region have the highest priority and should be presented to the user immediately. This may result in disruptive notifications from an accessibility service, which may potentially interrupt other feedback or user actions, so it should generally be used only for critical, time-sensitive information.
- `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_NONE:kotlin.Int`: Disables change announcements (the default for most views).

Examples:

- Selecting an option in a dropdown menu updates a panel below with the updated content. This panel may be marked as a live region with `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_POLITE:kotlin.Int` to notify users of the change. A screen reader may queue changes as announcements that don't disrupt ongoing speech.
- An emergency alert may be marked with `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_ASSERTIVE:kotlin.Int` to immediately inform users of the emergency.

For error notifications, like an "incorrect password" warning in a login screen, views should send a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` `AccessibilityEvent` with a content change type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_ERROR:kotlin.Int` and set setError. Custom widgets should provide error-setting methods that support accessibility. For example, use setError instead of explicitly sending events.

Don't use live regions for frequently-updating UI elements (e.g., progress bars), as this can overwhelm the user with feedback from accessibility services. If necessary, use setMinDurationBetweenContentChanges to throttle feedback and reduce disruptions.

**Note:** Use androidx.core.view.ViewCompat#setAccessibilityLiveRegion(android.view.View,int) for backwards-compatibility.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The live region mode for this view, one of: - `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_POLITE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_ASSERTIVE:kotlin.Int` |

### setAccessibilityPaneTitle

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccessibilityPaneTitle(accessibilityPaneTitle: CharSequence?): Unit
```

Visually distinct portion of a window with window-like semantics are considered panes for accessibility purposes. One example is the content view of a large fragment that is replaced. In order for accessibility services to understand a pane's window-like behavior, panes should have descriptive titles. Views with pane titles produce `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int`s when they appear, disappear, or change title.

When transitioning from one Activity to another, instead of using `setAccessibilityPaneTitle()`, set a descriptive title for its window by using `android:label` for the matching Activity entry in your application's manifest or updating the title at runtime with setTitle.

**Note:** Use androidx.core.view.ViewCompat#setAccessibilityPaneTitle(android.view.View,java.lang.CharSequence) for backwards-compatibility.

| Parameters ||
|---|---|
| `accessibilityPaneTitle` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The pane's title. Setting to `null` indicates that this View is not a pane. |

**See Also**

- setPaneTitle

### setAccessibilityTraversalAfter

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccessibilityTraversalAfter(afterId: Int): Unit
```

Sets the id of a view that screen readers are requested to visit before this view.

For example, if view B should be visited after A, with B.setAccessibilityTraversalAfter(A), then this requests that screen readers visit and traverse view A before visiting view B.

**Note:** Views are visited in the order determined by the screen reader. Avoid explicitly manipulating focus order, as this may result in inconsistent user experiences between apps. Instead, use other semantics, such as restructuring the view hierarchy layout, to communicate order.

Setting this view to be after a view that is not important for accessibility, or if this view is not important for accessibility, means this method will have no effect if the service is not aware of unimportant views.

To avoid a risk of loops, set clear relationships between views. For example, if focus order should be B -\> A, and B.setAccessibilityTraversalBefore(A), then also call A.setAccessibilityTraversalAfter(B).

| Parameters ||
|---|---|
| `afterId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a view this one succeeds in accessibility traversal. |

**See Also**

- setImportantForAccessibility
- setAccessibilityTraversalBefore

### setAccessibilityTraversalBefore

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccessibilityTraversalBefore(beforeId: Int): Unit
```

Sets the id of a view that screen readers are requested to visit after this view.

For example, if view B should be visited before view A, with B.setAccessibilityTraversalBefore(A), this requests that screen readers visit and traverse view B before visiting view A.

**Note:** Views are visited in the order determined by the screen reader. Avoid explicitly manipulating focus order, as this may result in inconsistent user experiences between apps. Instead, use other semantics, such as restructuring the view hierarchy layout, to communicate order.

Setting this view to be after a view that is not important for accessibility, or if this view is not important for accessibility, means this method will have no effect if the service is not aware of unimportant views.

To avoid a risk of loops, set clear relationships between views. For example, if focus order should be B -\> A, and B.setAccessibilityTraversalBefore(A), then also call A.setAccessibilityTraversalAfter(B).

| Parameters ||
|---|---|
| `beforeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a view this one precedes in accessibility traversal. |

**See Also**

- setImportantForAccessibility
- setAccessibilityTraversalAfter

### setActivated

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setActivated(activated: Boolean): Unit
```

Changes the activated state of this view. A view can be activated or not. Note that activation is not the same as selection. Selection is a transient property, representing the view (hierarchy) the user is currently interacting with. Activation is a longer-term state that the user can move views in and out of. For example, in a list view with single or multiple selection enabled, the views in the current selection set are activated. (Um, yeah, we are deeply sorry about the terminology here.) The activated state is propagated down to children of the view it is set on.

| Parameters ||
|---|---|
| `activated` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the view must be activated, false otherwise |

### setAllowClickWhenDisabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAllowClickWhenDisabled(clickableWhenDisabled: Boolean): Unit
```

Enables or disables click events for this view when disabled.

| Parameters ||
|---|---|
| `clickableWhenDisabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to make the view clickable, false otherwise |

### setAllowedHandwritingDelegatePackage

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAllowedHandwritingDelegatePackage(allowedPackageName: String?): Unit
```

Specifies that this view may act as a handwriting initiation delegator for a delegate editor view from the specified package. If this method is not called, delegators may only be used to initiate handwriting mode for a delegate editor view from the same package as the delegator view. This method allows specifying a different trusted package which may contain a delegate editor view linked to this delegator view.

This method has no effect unless setHandwritingDelegatorCallback is also called to configure this view to act as a handwriting delegator.

If this method is called on the delegator view, then setAllowedHandwritingDelegatorPackage should also be called on the delegate editor view.

For example, to configure a delegator view in package 1:

```kotlin
delegatorView.setHandwritingDelegatorCallback(callback);
  delegatorView.setAllowedHandwritingDelegatePackage(package2);
```
Then to configure the corresponding delegate editor view in package 2:

```kotlin
delegateEditorView.setIsHandwritingDelegate(true);
  delegateEditorView.setAllowedHandwritingDelegatorPackage(package1);
```

| Parameters ||
|---|---|
| `allowedPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the package name of a delegate editor view linked to this delegator view, or `null` to restore the default behavior of only allowing delegate editor views from the same package as this delegator view |

### setAllowedHandwritingDelegatorPackage

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAllowedHandwritingDelegatorPackage(allowedPackageName: String?): Unit
```

Specifies that a view from the specified package may act as a handwriting delegator for this delegate editor view. If this method is not called, only views from the same package as this delegate editor view may act as a handwriting delegator. This method allows specifying a different trusted package which may contain a delegator view linked to this delegate editor view.

This method has no effect unless setIsHandwritingDelegate is also called to configure this view to act as a handwriting delegate.

If this method is called on the delegate editor view, then setAllowedHandwritingDelegatePackage should also be called on the delegator view.

| Parameters ||
|---|---|
| `allowedPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the package name of a delegator view linked to this delegate editor view, or `null` to restore the default behavior of only allowing delegator views from the same package as this delegate editor view |

### setAlpha

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAlpha(alpha: Float): Unit
```

Sets the opacity of the view to a value from 0 to 1, where 0 means the view is completely transparent and 1 means the view is completely opaque.

**Note:** setting alpha to a translucent value (0 \< alpha \< 1) can have significant performance implications, especially for large views. It is best to use the alpha property sparingly and transiently, as in the case of fading animations.

For a view with a frequently changing alpha, such as during a fading animation, it is strongly recommended for performance reasons to either override hasOverlappingRendering to return `false` if appropriate, or setting a setLayerType on the view for the duration of the animation. On versions `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int` and below, the default path for rendering an unlayered View with alpha could add multiple milliseconds of rendering cost, even for simple or small views. Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int` is automatically applied to the view at the rendering level.

If this view overrides onSetAlpha to return true, then this view is responsible for applying the opacity itself.

On versions `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int` and below, note that if the view is backed by a setLayerType and is associated with a setLayerPaint, setting an alpha value less than 1.0 will supersede the alpha of the layer paint.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, setting a translucent alpha value will clip a View to its bounds, unless the View returns `false` from hasOverlappingRendering.

| Parameters ||
|---|---|
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The opacity of the view. Value is between 0.0f and 1.0f inclusive |

**See Also**

- hasOverlappingRendering
- setLayerType

### setAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAnimation(animation: Animation!): Unit
```

Sets the next animation to play for this view. If you want the animation to play immediately, use startAnimation instead. This method provides allows fine-grained control over the start time and invalidation, but you must make sure that 1) the animation has a start time set, and 2) the view's parent (which controls animations on its children) will be invalidated when the animation is supposed to start.

| Parameters ||
|---|---|
| `animation` | [Animation](../android.view.animation/Animation.md)!: The next animation, or null. |

### setAnimationMatrix

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAnimationMatrix(matrix: Matrix?): Unit
```

Changes the transformation matrix on the view. This is used in animation frameworks, such as `https://developer.android.com/reference/kotlin/android/transition/Transition.html#`. When the animation finishes, the matrix should be cleared by calling this method with `null` as the matrix parameter. Application developers should use transformation methods like setRotation, setScaleX, setScaleX, setTranslationX} and setTranslationY (float)}} instead.

| Parameters ||
|---|---|
| `matrix` | [Matrix](../android.graphics/Matrix.md)?: The matrix, null indicates that the matrix should be cleared. |

**See Also**

- getAnimationMatrix

### setAutoHandwritingEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAutoHandwritingEnabled(enabled: Boolean): Unit
```

Set whether this view enables automatic handwriting initiation. For a view with an active InputConnection, if auto handwriting is enabled then stylus movement within its view boundary will automatically trigger the handwriting mode. Check startStylusHandwriting for more details about handwriting mode. If the View wants to initiate handwriting mode by itself, it can set this field to `false` and call startStylusHandwriting when there is stylus movement detected. Note that this attribute has no effect on the View's children. For example, if a ViewGroup disables auto handwriting but its children set auto handwriting to true, auto handwriting will still work for the children, and vice versa.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether auto handwriting initiation is enabled for this view. |

**See Also**

- onCreateInputConnection
- startStylusHandwriting

### setAutofillHints

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAutofillHints(vararg autofillHints: String!): Unit
```

Sets the hints that help an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` determine how to autofill the view with the user's data.

Typically, there is only one way to autofill a view, but there could be more than one. For example, if the application accepts either an username or email address to identify an user.

These hints are not validated by the Android System, but passed "as is" to the service. Hence, they can have any value, but it's recommended to use the `AUTOFILL_HINT_` constants such as: `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_USERNAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_PASSWORD:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_EMAIL_ADDRESS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_NAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_PHONE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_POSTAL_ADDRESS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_POSTAL_CODE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_NUMBER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH:kotlin.String` or `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR:kotlin.String`.

| Parameters ||
|---|---|
| `autofillHints` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The autofill hints to set. If the array is emtpy, `null` is set. |

### setAutofillId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAutofillId(id: AutofillId?): Unit
```

Sets the unique, logical identifier of this view in the activity, for autofill purposes.

The autofill id is created on demand, and this method should only be called when a view is reused after dispatchProvideAutofillStructure is called, as that method creates a snapshot of the view that is passed along to the autofill service.

This method is typically used when view subtrees are recycled to represent different content\* ---in this case, the autofill id can be saved before the view content is swapped out, and restored later when it's swapped back in. For example:

```kotlin
EditText reusableView = ...;
  ViewGroup parentView = ...;
  AutofillManager afm = ...;
 
  // Swap out the view and change its contents
  AutofillId oldId = reusableView.getAutofillId();
  CharSequence oldText = reusableView.getText();
  parentView.removeView(reusableView);
  AutofillId newId = afm.getNextAutofillId();
  reusableView.setText("New I am");
  reusableView.setAutofillId(newId);
  parentView.addView(reusableView);
 
  // Later, swap the old content back in
  parentView.removeView(reusableView);
  reusableView.setAutofillId(oldId);
  reusableView.setText(oldText);
  parentView.addView(reusableView);
  
```

NOTE: If this view is a descendant of an `https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#`, the system may reset its autofill id when this view is recycled. If the autofill ids need to be stable, they should be set again in getView.

| Parameters ||
|---|---|
| `id` | [AutofillId](../android.view.autofill/AutofillId.md)?: an autofill ID that is unique in the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` hosting the view, or `null` to reset it. Usually it's an id previously allocated to another view (and obtained through getAutofillId), or a new value obtained through getNextAutofillId. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the id is an autofill id associated with a virtual view. |
| `java.lang.IllegalStateException` | if the view is already isAttachedToWindow. |

### setBackdropRenderEffect

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackdropRenderEffect(renderEffect: RenderEffect?): Unit
```

Configure the `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#` to apply to the backdrop contents of this View. This will apply a visual effect to the result of the backdrop contents of this View before it is drawn. For example if createBlurEffect is provided, the previous content behind this View will be blurred before this View is drawn.

| Parameters ||
|---|---|
| `renderEffect` | [RenderEffect](../android.graphics/RenderEffect.md)?: to be applied to the View. Passing null clears the previously configured `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#` |

### setBackground

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackground(background: Drawable!): Unit
```

Set the background to a given Drawable, or remove the background. If the background has padding, this View's padding is set to the background's padding. However, when a background is removed, this View's padding isn't touched. If setting the padding is desired, please use setPadding.

| Parameters ||
|---|---|
| `background` | [Drawable](../android.graphics.drawable/Drawable.md)!: The Drawable to use as the background, or null to remove the background |

### setBackgroundColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackgroundColor(color: Int): Unit
```

Sets the background color for this view.

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the color of the background |

### setBackgroundDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackgroundDrawable(background: Drawable!): Unit
```

**Deprecated:** *use setBackground instead*

### setBackgroundResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackgroundResource(resid: Int): Unit
```

Set the background to a given resource. The resource should refer to a Drawable object or 0 to remove the background.

| Parameters ||
|---|---|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The identifier of the resource. |

### setBackgroundTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackgroundTintBlendMode(blendMode: BlendMode?): Unit
```

Specifies the blending mode used to apply the tint specified by setBackgroundTintList} to the background drawable. The default mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`.

| Parameters ||
|---|---|
| `blendMode` | [BlendMode](../android.graphics/BlendMode.md)?: the blending mode used to apply the tint, may be `null` to clear tint |

**See Also**

- getBackgroundTintMode
- setTintBlendMode

### setBackgroundTintList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackgroundTintList(tint: ColorStateList?): Unit
```

Applies a tint to the background drawable. Does not modify the current tint mode, which is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#` by default.

Subsequent calls to setBackground will automatically mutate the drawable and apply the specified tint and tint mode using setTintList.

| Parameters ||
|---|---|
| `tint` | [ColorStateList](../android.content.res/ColorStateList.md)?: the tint to apply, may be `null` to clear tint |

**See Also**

- getBackgroundTintList
- setTintList

### setBackgroundTintMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackgroundTintMode(tintMode: PorterDuff.Mode?): Unit
```

Specifies the blending mode used to apply the tint specified by setBackgroundTintList} to the background drawable. The default mode is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#`.

| Parameters ||
|---|---|
| `tintMode` | [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?: the blending mode used to apply the tint, may be `null` to clear tint |

**See Also**

- getBackgroundTintMode
- setTintMode

### setBottom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setBottom(bottom: Int): Unit
```

Sets the bottom position of this view relative to its parent. This method is meant to be called by the layout system and should not generally be called otherwise, because the property may be changed at any time by the layout.

| Parameters ||
|---|---|
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The bottom of this view, in pixels. |

### setCameraDistance

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCameraDistance(distance: Float): Unit
```

Sets the distance along the Z axis (orthogonal to the X/Y plane on which views are drawn) from the camera to this view. The camera's distance affects 3D transformations, for instance rotations around the X and Y axis. If the rotationX or rotationY properties are changed and this view is large (more than half the size of the screen), it is recommended to always use a camera distance that's greater than the height (X axis rotation) or the width (Y axis rotation) of this view.

The distance of the camera from the view plane can have an affect on the perspective distortion of the view when it is rotated around the x or y axis. For example, a large distance will result in a large viewing angle, and there will not be much perspective distortion of the view as it rotates. A short distance may cause much more perspective distortion upon rotation, and can also result in some drawing artifacts if the rotated view ends up partially behind the camera (which is why the recommendation is to use a distance at least as far as the size of the view, if the view is to be rotated.)

The distance is expressed in "depth pixels." The default distance depends on the screen density. For instance, on a medium density display, the default distance is 1280. On a high density display, the default distance is 1920.

If you want to specify a distance that leads to visually consistent results across various densities, use the following formula:

```kotlin
float scale = context.getResources().getDisplayMetrics().density;
  view.setCameraDistance(distance * scale);
  
```

The density scale factor of a high density display is 1.5, and 1920 = 1280 \* 1.5.

| Parameters ||
|---|---|
| `distance` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The distance in "depth pixels", if negative the opposite value is used |

**See Also**

- setRotationX
- setRotationY

### setClickable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setClickable(clickable: Boolean): Unit
```

Enables or disables click events for this view. When a view is clickable it will change its state to "pressed" on every click. Subclasses should set the view clickable to visually react to user's clicks.

| Parameters ||
|---|---|
| `clickable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to make the view clickable, false otherwise |

**See Also**

- isClickable

### setClipBounds

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setClipBounds(clipBounds: Rect!): Unit
```

Sets a rectangular area on this view to which the view will be clipped when it is drawn. Setting the value to null will remove the clip bounds and the view will draw normally, using its full bounds.

| Parameters ||
|---|---|
| `clipBounds` | [Rect](../android.graphics/Rect.md)!: The rectangular area, in the local coordinates of this view, to which future drawing operations will be clipped. |

### setClipToOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setClipToOutline(clipToOutline: Boolean): Unit
```

Sets whether the View's Outline should be used to clip the contents of the View.

Only a single non-rectangular clip can be applied on a View at any time. Circular clips from a createCircularReveal animation take priority over Outline clipping, and child Outline clipping takes priority over Outline clipping done by a parent.

Note that this flag will only be respected if the View's Outline returns true from canClip.
**See Also**

- setOutlineProvider
- getClipToOutline

### setContentCaptureSession

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContentCaptureSession(contentCaptureSession: ContentCaptureSession?): Unit
```

Sets the (optional) ContentCaptureSession associated with this view.

This method should be called when you need to associate a ContentCaptureContext to the content capture events associated with this view or its view hierarchy (if it's a ViewGroup).

For example, if your activity is associated with a web domain, first you would need to set the context for the main DOM:

```kotlin
ContentCaptureSession mainSession = rootView.getContentCaptureSession();
    mainSession.setContentCaptureContext(ContentCaptureContext.forLocusId(Uri.parse(myUrl));
  
```

Then if the page had an `IFRAME`, you would create a new session for it:

```kotlin
ContentCaptureSession iframeSession = mainSession.createContentCaptureSession(
        ContentCaptureContext.forLocusId(Uri.parse(iframeUrl)));
    iframeView.setContentCaptureSession(iframeSession);
  
```

| Parameters ||
|---|---|
| `contentCaptureSession` | [ContentCaptureSession](../android.view.contentcapture/ContentCaptureSession.md)?: a session created by createContentCaptureSession. This value may be `null`. |

### setContentDescription

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContentDescription(contentDescription: CharSequence!): Unit
```

Sets the View's content description.

A content description briefly describes the view and is primarily used for accessibility support to determine how a view should be presented to the user. In the case of a view with no textual representation, such as `https://developer.android.com/reference/kotlin/android/widget/ImageButton.html#`, a useful content description explains what the view does. For example, an image button with a phone icon that is used to place a call may use "Call" as its content description. An image of a floppy disk that is used to save a file may use "Save".

This should omit role or state. Role refers to the kind of user-interface element the View is, such as a Button or Checkbox. State refers to a frequently changing property of the View, such as an On/Off state of a button or the audio level of a volume slider.

Content description updates are not frequent, and are used when the semantic content - not the state - of the element changes. For example, a Play button might change to a Pause button during music playback.

| Parameters ||
|---|---|
| `contentDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The content description. |

**See Also**

- getContentDescription
- setStateDescription

### setContentSensitivity

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setContentSensitivity(mode: Int): Unit
```

Sets content sensitivity mode to determine whether this view displays sensitive content (e.g. username, password etc.). The system will improve user privacy i.e. hide content drawn by a sensitive view from screen sharing and recording.

The window hosting a sensitive view will be marked as secure during an active media projection session. This would be equivalent to applying `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_SECURE:kotlin.Int` to the window.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_NOT_SENSITIVE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_SENSITIVE:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_SENSITIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_NOT_SENSITIVE:kotlin.Int` |

### setContextClickable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContextClickable(contextClickable: Boolean): Unit
```

Enables or disables context clicking for this view. This event can launch the listener.

| Parameters ||
|---|---|
| `contextClickable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to make the view react to a context click, false otherwise |

**See Also**

- isContextClickable

### setDefaultFocusHighlightEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDefaultFocusHighlightEnabled(defaultFocusHighlightEnabled: Boolean): Unit
```

Sets whether this View should use a default focus highlight when it gets focused but doesn't have `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` defined in its background.

| Parameters ||
|---|---|
| `defaultFocusHighlightEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` to set this view to use a default focus highlight, `false` otherwise. |

### setDrawingCacheBackgroundColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDrawingCacheBackgroundColor(color: Int): Unit
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Setting a solid background color for the drawing cache's bitmaps will improve performance and memory usage. Note, though that this should only be used if this view will always be drawn on top of a solid color.

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The background color to use for the drawing cache's bitmap |

**See Also**

- setDrawingCacheEnabled
- buildDrawingCache
- getDrawingCache

### setDrawingCacheEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDrawingCacheEnabled(enabled: Boolean): Unit
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Enables or disables the drawing cache. When the drawing cache is enabled, the next call to getDrawingCache or buildDrawingCache will draw the view in a bitmap. Calling draw will not draw from the cache when the cache is enabled. To benefit from the cache, you must request the drawing cache by calling getDrawingCache and draw it on screen if the returned bitmap is not null.

Enabling the drawing cache is similar to setLayerType when hardware acceleration is turned off. When hardware acceleration is turned on, enabling the drawing cache has no effect on rendering because the system uses a different mechanism for acceleration which ignores the flag. If you want to use a Bitmap for the view, even when hardware acceleration is enabled, see setLayerType for information on how to enable software and hardware layers.

This API can be used to manually generate a bitmap copy of this view, by setting the flag to `true` and calling getDrawingCache.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable the drawing cache, false otherwise |

**See Also**

- isDrawingCacheEnabled
- getDrawingCache
- buildDrawingCache
- setLayerType

### setDrawingCacheQuality

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDrawingCacheQuality(quality: Int): Unit
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Set the drawing cache quality of this view. This value is used only when the drawing cache is enabled

| Parameters ||
|---|---|
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_LOW:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_HIGH:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_HIGH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_AUTO:kotlin.Int` |

**See Also**

- getDrawingCacheQuality
- setDrawingCacheEnabled
- isDrawingCacheEnabled

### setDuplicateParentStateEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDuplicateParentStateEnabled(enabled: Boolean): Unit
```

Enables or disables the duplication of the parent's state into this view. When duplication is enabled, this view gets its drawable state from its parent rather than from its own internal properties.

Note: in the current implementation, setting this property to true after the view was added to a ViewGroup might have no effect at all. This property should always be used from XML or set to true before adding this view to a ViewGroup.

Note: if this view's parent addStateFromChildren property is enabled and this property is enabled, an exception will be thrown.

Note: if the child view uses and updates additional states which are unknown to the parent, these states should not be affected by this method.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True to enable duplication of the parent's drawable state, false to disable it. |

**See Also**

- getDrawableState
- isDuplicateParentStateEnabled

### setElevation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setElevation(elevation: Float): Unit
```

Sets the base elevation of this view, in pixels.

### setEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setEnabled(enabled: Boolean): Unit
```

Set the enabled state of this view. The interpretation of the enabled state varies by subclass.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if this view is enabled, false otherwise. |

### setFadingEdgeLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFadingEdgeLength(length: Int): Unit
```

Set the size of the faded edge used to indicate that more content in this view is available. Will not change whether the fading edge is enabled; use setVerticalFadingEdgeEnabled or setHorizontalFadingEdgeEnabled to enable the fading edge for the vertical or horizontal fading edges.

| Parameters ||
|---|---|
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The size in pixels of the faded edge used to indicate that more content in this view is visible. |

### setFilterTouchesWhenObscured

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFilterTouchesWhenObscured(enabled: Boolean): Unit
```

Sets whether the framework should discard touches when the view's window is obscured by another visible window at the touched location. Refer to the View security documentation for more details.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if touch filtering should be enabled. |

**See Also**

- getFilterTouchesWhenObscured

### setFitsSystemWindows

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFitsSystemWindows(fitSystemWindows: Boolean): Unit
```

Sets whether or not this view should account for system screen decorations such as the status bar and inset its content; that is, controlling whether the default implementation of fitSystemWindows will be executed. See that method for more details.

Note that if you are providing your own implementation of fitSystemWindows, then there is no need to set this flag to true -- your implementation will be overriding the default implementation that checks this flag.

| Parameters ||
|---|---|
| `fitSystemWindows` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, then the default implementation of fitSystemWindows will be executed. |

**See Also**

- getFitsSystemWindows
- fitSystemWindows
- setSystemUiVisibility

### setFocusable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFocusable(focusable: Boolean): Unit
```

Set whether this view can receive the focus.

Setting this to false will also ensure that this view is not focusable in touch mode.

| Parameters ||
|---|---|
| `focusable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, this view can receive the focus. |

**See Also**

- setFocusableInTouchMode
- setFocusable

### setFocusable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFocusable(focusable: Int): Unit
```

Sets whether this view can receive focus.

Setting this to `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE_AUTO:kotlin.Int` tells the framework to determine focusability automatically based on the view's interactivity. This is the default.

Setting this to NOT_FOCUSABLE will ensure that this view is also not focusable in touch mode.

| Parameters ||
|---|---|
| `focusable` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of `https://developer.android.com/reference/kotlin/android/view/View#NOT_FOCUSABLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE_AUTO:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#NOT_FOCUSABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE_AUTO:kotlin.Int` |

**See Also**

- setFocusableInTouchMode

### setFocusableInTouchMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFocusableInTouchMode(focusableInTouchMode: Boolean): Unit
```

Set whether this view can receive focus while in touch mode. Setting this to true will also ensure that this view is focusable.

| Parameters ||
|---|---|
| `focusableInTouchMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, this view can receive the focus while in touch mode. |

**See Also**

- setFocusable

### setFocusedByDefault

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFocusedByDefault(isFocusedByDefault: Boolean): Unit
```

Sets whether this View should receive focus when the focus is restored for the view hierarchy containing this view.

Focus gets restored for a view hierarchy when the root of the hierarchy gets added to a window or serves as a target of cluster navigation.

| Parameters ||
|---|---|
| `isFocusedByDefault` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` to set this view as the default-focus view, `false` otherwise. |

**See Also**

- restoreDefaultFocus

### setForceDarkAllowed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setForceDarkAllowed(allow: Boolean): Unit
```

Sets whether or not to allow force dark to apply to this view. Setting this to false will disable the auto-dark feature on everything this view draws, including any descendants. Setting this to true will allow this view to be automatically made dark, however a value of 'true' will not override any 'false' value in its parent chain nor will it prevent any 'false' in any of its children. The default behavior of force dark is also influenced by the Theme's `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_isLightTheme:kotlin.Int` attribute. If a theme is isLightTheme="false", then force dark is globally disabled for that theme.

| Parameters ||
|---|---|
| `allow` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether or not to allow force dark. |

### setForeground

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setForeground(foreground: Drawable!): Unit
```

Supply a Drawable that is to be rendered on top of all of the content in the view.

| Parameters ||
|---|---|
| `foreground` | [Drawable](../android.graphics.drawable/Drawable.md)!: the Drawable to be drawn on top of the children |

### setForegroundGravity

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setForegroundGravity(gravity: Int): Unit
```

Describes how the foreground is positioned. Defaults to START and TOP.

| Parameters ||
|---|---|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): see Gravity |

**See Also**

- getForegroundGravity

### setForegroundTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setForegroundTintBlendMode(blendMode: BlendMode?): Unit
```

Specifies the blending mode used to apply the tint specified by setForegroundTintList} to the background drawable. The default mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`.

| Parameters ||
|---|---|
| `blendMode` | [BlendMode](../android.graphics/BlendMode.md)?: the blending mode used to apply the tint, may be `null` to clear tint |

**See Also**

- getForegroundTintMode
- setTintBlendMode

### setForegroundTintList

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setForegroundTintList(tint: ColorStateList?): Unit
```

Applies a tint to the foreground drawable. Does not modify the current tint mode, which is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#` by default.

Subsequent calls to setForeground will automatically mutate the drawable and apply the specified tint and tint mode using setTintList.

| Parameters ||
|---|---|
| `tint` | [ColorStateList](../android.content.res/ColorStateList.md)?: the tint to apply, may be `null` to clear tint |

**See Also**

- getForegroundTintList
- setTintList

### setForegroundTintMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setForegroundTintMode(tintMode: PorterDuff.Mode?): Unit
```

Specifies the blending mode used to apply the tint specified by setForegroundTintList} to the background drawable. The default mode is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#`.

| Parameters ||
|---|---|
| `tintMode` | [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?: the blending mode used to apply the tint, may be `null` to clear tint |

**See Also**

- getForegroundTintMode
- setTintMode

### setFrameContentVelocity

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFrameContentVelocity(pixelsPerSecond: Float): Unit
```

Set the current velocity of the View, we only track positive value. We will use the velocity information to adjust the frame rate when applicable. For example, we could potentially lower the frame rate when the velocity of a fling gesture becomes slower. Note that this is only valid till the next drawn frame.

| Parameters ||
|---|---|
| `pixelsPerSecond` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): how many pixels move per second. |

### setHandwritingBoundsOffsets

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHandwritingBoundsOffsets(
    offsetLeft: Float, 
    offsetTop: Float, 
    offsetRight: Float, 
    offsetBottom: Float
): Unit
```

Set the amount of offset applied to this view's stylus handwriting bounds. A positive offset will offset the edge outwards.The base handwriting bounds of a view is its visible bounds. The handwriting bounds offsets are applied to the base handwriting bounds to determine the final handwriting bounds.

This method is mainly used to enlarge the view's handwriting bounds for a better user experience.

Note that when the view is clipped (e.g. the view is in a `https://developer.android.com/reference/kotlin/android/widget/ScrollView.html#`), the offsets are applied after the view's handwriting bounds is clipped.

| Parameters ||
|---|---|
| `offsetLeft` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the amount of pixel offset applied to the left edge outwards of the view's handwriting bounds. |
| `offsetTop` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the amount of pixel offset applied to the top edge outwards of the view's handwriting bounds. |
| `offsetRight` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the amount of pixel offset applied to the right edge outwards of the view's handwriting bounds. |
| --- | --- |
| `offsetBottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the amount of pixel offset applied to the bottom edge outwards of the view's handwriting bounds. |

**See Also**

- setAutoHandwritingEnabled
- getHandwritingBoundsOffsetLeft
- getHandwritingBoundsOffsetTop
- getHandwritingBoundsOffsetRight
- getHandwritingBoundsOffsetBottom

### setHandwritingDelegateFlags

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHandwritingDelegateFlags(flags: Int): Unit
```

Sets flags configuring the handwriting delegation behavior for this delegate editor view.

This method has no effect unless setIsHandwritingDelegate is also called to configure this view to act as a handwriting delegate.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HANDWRITING_DELEGATE_FLAG_HOME_DELEGATOR_ALLOWED:kotlin.Int` or `0` Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HANDWRITING_DELEGATE_FLAG_HOME_DELEGATOR_ALLOWED:kotlin.Int` |

### setHandwritingDelegatorCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHandwritingDelegatorCallback(callback: Runnable?): Unit
```

Sets a callback which should be called when a stylus MotionEvent occurs within this view's bounds. The callback will be called from the UI thread.

Setting a callback allows this view to act as a handwriting delegator, so that handwriting mode for a delegate editor view can be initiated by stylus movement on this delegator view. The callback implementation is expected to show and focus the delegate editor view. If a view which returns `true` for isHandwritingDelegate creates an input connection while the same stylus MotionEvent sequence is ongoing, handwriting mode will be initiated for that view.

A common use case is a custom view which looks like a text editor but does not actually support text editing itself, and clicking on the custom view causes an EditText to be shown. To support handwriting initiation in this case, this method can be called on the custom view to configure it as a delegator. The EditText should call setIsHandwritingDelegate to set it as a delegate. The `callback` implementation is typically the same as the click listener implementation which shows the EditText.

If `null` is passed, this view will no longer act as a handwriting initiation delegator.

| Parameters ||
|---|---|
| `callback` | [Runnable](../java.lang/Runnable.md)?: a callback which should be called when a stylus MotionEvent occurs within this view's bounds. This value may be `null`. |

### setHapticFeedbackEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHapticFeedbackEnabled(hapticFeedbackEnabled: Boolean): Unit
```

Set whether this view should have haptic feedback for events such as long presses.

You may wish to disable haptic feedback if your view already controls its own haptic feedback.

| Parameters ||
|---|---|
| `hapticFeedbackEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether haptic feedback enabled for this view. |

**See Also**

- isHapticFeedbackEnabled
- performHapticFeedback

### setHasTransientState

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHasTransientState(hasTransientState: Boolean): Unit
```

Set whether this view is currently tracking transient state that the framework should attempt to preserve when possible. This flag is reference counted, so every call to setHasTransientState(true) should be paired with a later call to setHasTransientState(false).

A view with transient state cannot be trivially rebound from an external data source, such as an adapter binding item views in a list. This may be because the view is performing an animation, tracking user selection of content, or similar.

| Parameters ||
|---|---|
| `hasTransientState` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if this view has transient state |

### setHorizontalFadingEdgeEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHorizontalFadingEdgeEnabled(horizontalFadingEdgeEnabled: Boolean): Unit
```

Define whether the horizontal edges should be faded when this view is scrolled horizontally.

| Parameters ||
|---|---|
| `horizontalFadingEdgeEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the horizontal edges should be faded when the view is scrolled horizontally |

**See Also**

- isHorizontalFadingEdgeEnabled

### setHorizontalScrollBarEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHorizontalScrollBarEnabled(horizontalScrollBarEnabled: Boolean): Unit
```

Define whether the horizontal scrollbar should be drawn or not. The scrollbar is not drawn by default.

| Parameters ||
|---|---|
| `horizontalScrollBarEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the horizontal scrollbar should be painted |

**See Also**

- isHorizontalScrollBarEnabled

### setHorizontalScrollbarThumbDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHorizontalScrollbarThumbDrawable(drawable: Drawable?): Unit
```

Defines the horizontal thumb drawable

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md)?: This value may be `null`. |

**See Also**

- awakenScrollBars
- isHorizontalScrollBarEnabled
- setHorizontalScrollBarEnabled

### setHorizontalScrollbarTrackDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHorizontalScrollbarTrackDrawable(drawable: Drawable?): Unit
```

Defines the horizontal track drawable

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md)?: This value may be `null`. |

**See Also**

- awakenScrollBars
- isHorizontalScrollBarEnabled
- setHorizontalScrollBarEnabled

### setHovered

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHovered(hovered: Boolean): Unit
```

Sets whether the view is currently hovered.

Calling this method also changes the drawable state of the view. This enables the view to react to hover by using different drawable resources to change its appearance.

The onHoverChanged method is called when the hovered state changes.

| Parameters ||
|---|---|
| `hovered` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the view is hovered. |

**See Also**

- isHovered
- onHoverChanged

### setId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setId(id: Int): Unit
```

Sets the identifier for this view. The identifier does not have to be unique in this view's hierarchy. The identifier should be a positive number.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a number used to identify the view |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int`
- getId
- findViewById

### setImportantForAccessibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setImportantForAccessibility(mode: Int): Unit
```

Sets how to determine whether this view is important for accessibility which is if it fires accessibility events and if it is reported to accessibility services that query the screen.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): How to determine whether this view is important for accessibility. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_YES:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_AUTO:kotlin.Int`

### setImportantForAutofill

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setImportantForAutofill(mode: Int): Unit
```

Sets the mode for determining whether this view is considered important for autofill.

The platform determines the importance for autofill automatically but you can use this method to customize the behavior. For example:

1. When the view contents is irrelevant for autofill (for example, a text field used in a "Captcha" challenge), it should be `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int`.
2. When both the view and its children are irrelevant for autofill (for example, the root view of an activity containing a spreadhseet editor), it should be `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int`.
3. When the view content is relevant for autofill but its children aren't (for example, a credit card expiration date represented by a custom view that overrides the proper autofill methods and has 2 children representing the month and year), it should be `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`.

**Note:** Setting the mode as `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int` does not guarantee the view (and its children) will not be used for autofill purpose; for example, when the user explicitly makes an autofill request, all views are included in the ViewStructure, and starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` the system uses other factors along with importance to determine the autofill behavior. See isImportantForAutofill for more details about how the View's importance for autofill is used.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int` |

### setImportantForContentCapture

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setImportantForContentCapture(mode: Int): Unit
```

Sets the mode for determining whether this view is considered important for content capture.

The platform determines the importance for autofill automatically but you can use this method to customize the behavior. Typically, a view that provides text should be marked as `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES:kotlin.Int`.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES_EXCLUDE_DESCENDANTS:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO_EXCLUDE_DESCENDANTS:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES_EXCLUDE_DESCENDANTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO_EXCLUDE_DESCENDANTS:kotlin.Int` |

### setIsCredential

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIsCredential(isCredential: Boolean): Unit
```

**Deprecated:** *The isCredential is no longer used by the system and is not recommended for use by apps. The purpose and usage expectations of this property were never clearly defined.*

Sets whether this view is a credential for Credential Manager purposes.

See isCredential.

| Parameters ||
|---|---|
| `isCredential` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the view is a credential. |

### setIsHandwritingDelegate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIsHandwritingDelegate(isHandwritingDelegate: Boolean): Unit
```

Sets this view to be a handwriting delegate. If a delegate view creates an input connection while a stylus MotionEvent sequence from a delegator view is ongoing, handwriting mode will be initiated for the delegate view.

| Parameters ||
|---|---|
| `isHandwritingDelegate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether this view is a handwriting initiation delegate |

**See Also**

- setHandwritingDelegatorCallback

### setKeepScreenOn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setKeepScreenOn(keepScreenOn: Boolean): Unit
```

Controls whether the screen should remain on, modifying the value of `https://developer.android.com/reference/kotlin/android/view/View#KEEP_SCREEN_ON:kotlin.Int`.

| Parameters ||
|---|---|
| `keepScreenOn` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Supply true to set `https://developer.android.com/reference/kotlin/android/view/View#KEEP_SCREEN_ON:kotlin.Int`. |

**See Also**

- getKeepScreenOn

### setKeyboardNavigationCluster

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setKeyboardNavigationCluster(isCluster: Boolean): Unit
```

Set whether this view is a root of a keyboard navigation cluster.

| Parameters ||
|---|---|
| `isCluster` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, this view is a root of a cluster. |

### setLabelFor

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLabelFor(id: Int): Unit
```

Sets the id of a view for which this view serves as a label for accessibility purposes.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The labeled view id. |

### setLayerPaint

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerPaint(paint: Paint?): Unit
```

Updates the `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` object used with the current layer (used only if the current layer type is not set to `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`). Changed properties of the Paint provided to setLayerType will be used the next time the View is redrawn, but setLayerPaint must be called to ensure that the view gets redrawn immediately.

A layer is associated with an optional `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` instance that controls how the layer is composed on screen. The following properties of the paint are taken into account when composing the layer:

- getAlpha
- getXfermode
- getColorFilter

If this view has an alpha value set to \< 1.0 by calling setAlpha, the alpha value of the layer's paint is superseded by this view's alpha value.

| Parameters ||
|---|---|
| `paint` | [Paint](../android.graphics/Paint.md)?: The paint used to compose the layer. This argument is optional and can be null. It is ignored when the layer type is `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int` |

**See Also**

- setLayerType

### setLayerType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerType(
    layerType: Int, 
    paint: Paint?
): Unit
```

Specifies the type of layer backing this view. The layer can be `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int`.

A layer is associated with an optional `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` instance that controls how the layer is composed on screen. The following properties of the paint are taken into account when composing the layer:

- getAlpha
- getXfermode
- getColorFilter

If this view has an alpha value set to \< 1.0 by calling setAlpha, the alpha value of the layer's paint is superseded by this view's alpha value.

Refer to the documentation of `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int` for more information on when and how to use layers.

| Parameters ||
|---|---|
| `layerType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of layer to use with this view, must be one of `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int` |
| `paint` | [Paint](../android.graphics/Paint.md)?: The paint used to compose the layer. This argument is optional and can be null. It is ignored when the layer type is `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int` |

**See Also**

- getLayerType
- `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int`
- setAlpha

### setLayoutDirection

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayoutDirection(layoutDirection: Int): Unit
```

Set the layout direction for this view. This will propagate a reset of layout direction resolution to the view's children and resolve layout direction for this view.

| Parameters ||
|---|---|
| `layoutDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the layout direction to set. Should be one of: `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LTR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_RTL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_INHERIT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LOCALE:kotlin.Int`. Resolution will be done if the value is set to LAYOUT_DIRECTION_INHERIT. The resolution proceeds up the parent chain of the view to get the value. If there is no parent, then it will return the default `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LTR:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LTR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_RTL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_INHERIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LOCALE:kotlin.Int` |

### setLayoutParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayoutParams(params: ViewGroup.LayoutParams!): Unit
```

Set the layout parameters associated with this view. These supply parameters to the *parent* of this view specifying how it should be arranged. There are many subclasses of ViewGroup.LayoutParams, and these correspond to the different subclasses of ViewGroup that are responsible for arranging their children.

| Parameters ||
|---|---|
| `params` | [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)!: The layout parameters for this view, cannot be null |

### setLeft

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setLeft(left: Int): Unit
```

Sets the left position of this view relative to its parent. This method is meant to be called by the layout system and should not generally be called otherwise, because the property may be changed at any time by the layout.

| Parameters ||
|---|---|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The left of this view, in pixels. |

### setLeftTopRightBottom

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setLeftTopRightBottom(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Assign a size and position to this view. This method is meant to be used in animations only as it applies this position and size for the view only temporary and it can be changed back at any time by the layout.

| Parameters ||
|---|---|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Left position, relative to parent |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Top position, relative to parent |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Right position, relative to parent |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bottom position, relative to parent |

**See Also**

- setLeft
- setRight
- setTop
- setBottom

### setLongClickable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLongClickable(longClickable: Boolean): Unit
```

Enables or disables long click events for this view. When a view is long clickable it reacts to the user holding down the button for a longer duration than a tap. This event can either launch the listener or a context menu.

| Parameters ||
|---|---|
| `longClickable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to make the view long clickable, false otherwise |

**See Also**

- isLongClickable

### setMinimumHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMinimumHeight(minHeight: Int): Unit
```

Sets the minimum height of the view. It is not guaranteed the view will be able to achieve this minimum height (for example, if its parent layout constrains it with less available height).

| Parameters ||
|---|---|
| `minHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The minimum height the view will try to be, in pixels |

**See Also**

- getMinimumHeight

### setMinimumWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMinimumWidth(minWidth: Int): Unit
```

Sets the minimum width of the view. It is not guaranteed the view will be able to achieve this minimum width (for example, if its parent layout constrains it with less available width).

| Parameters ||
|---|---|
| `minWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The minimum width the view will try to be, in pixels |

**See Also**

- getMinimumWidth

### setNestedScrollingEnabled

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNestedScrollingEnabled(enabled: Boolean): Unit
```

Enable or disable nested scrolling for this view.

If this property is set to true the view will be permitted to initiate nested scrolling operations with a compatible parent view in the current hierarchy. If this view does not implement nested scrolling this will have no effect. Disabling nested scrolling while a nested scroll is in progress has the effect of stopNestedScroll the nested scroll.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable nested scrolling, false to disable |

**See Also**

- isNestedScrollingEnabled

### setNextClusterForwardId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNextClusterForwardId(nextClusterForwardId: Int): Unit
```

Sets the id of the view to use as the root of the next keyboard navigation cluster.

| Parameters ||
|---|---|
| `nextClusterForwardId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The next cluster ID, or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the framework should decide automatically. |

### setNextFocusDownId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNextFocusDownId(nextFocusDownId: Int): Unit
```

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int`.

| Parameters ||
|---|---|
| `nextFocusDownId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The next focus ID, or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the framework should decide automatically. |

### setNextFocusForwardId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNextFocusForwardId(nextFocusForwardId: Int): Unit
```

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int`.

| Parameters ||
|---|---|
| `nextFocusForwardId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The next focus ID, or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the framework should decide automatically. |

### setNextFocusLeftId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNextFocusLeftId(nextFocusLeftId: Int): Unit
```

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int`.

| Parameters ||
|---|---|
| `nextFocusLeftId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The next focus ID, or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the framework should decide automatically. |

### setNextFocusRightId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNextFocusRightId(nextFocusRightId: Int): Unit
```

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int`.

| Parameters ||
|---|---|
| `nextFocusRightId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The next focus ID, or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the framework should decide automatically. |

### setNextFocusUpId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNextFocusUpId(nextFocusUpId: Int): Unit
```

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int`.

| Parameters ||
|---|---|
| `nextFocusUpId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The next focus ID, or `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int` if the framework should decide automatically. |

### setOnApplyWindowInsetsListener

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnApplyWindowInsetsListener(listener: View.OnApplyWindowInsetsListener!): Unit
```

Set an `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener` to take over the policy for applying window insets to this view. The listener's onApplyWindowInsets method will be called instead of the view's onApplyWindowInsets method.

| Parameters ||
|---|---|
| `listener` | [View.OnApplyWindowInsetsListener](../android/view/View.OnApplyWindowInsetsListener.md)!: Listener to set |

**See Also**

- onApplyWindowInsets

### setOnCapturedPointerListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnCapturedPointerListener(l: View.OnCapturedPointerListener!): Unit
```

Set a listener to receive callbacks when the pointer capture state of a view changes.

| Parameters ||
|---|---|
| `l` | [View.OnCapturedPointerListener](../android/view/View.OnCapturedPointerListener.md)!: The `https://developer.android.com/reference/kotlin/android/view/View.OnCapturedPointerListener` to receive callbacks. |

### setOnClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnClickListener(l: View.OnClickListener?): Unit
```

Register a callback to be invoked when this view is clicked. If this view is not clickable, it becomes clickable.

| Parameters ||
|---|---|
| `l` | [View.OnClickListener](../android/view/View.OnClickListener.md)?: The callback that will run. This value may be `null`. |

**See Also**

- setClickable

### setOnContextClickListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnContextClickListener(l: View.OnContextClickListener?): Unit
```

Register a callback to be invoked when this view is context clicked. If the view is not context clickable, it becomes context clickable.

| Parameters ||
|---|---|
| `l` | [View.OnContextClickListener](../android/view/View.OnContextClickListener.md)?: The callback that will run. This value may be `null`. |

**See Also**

- setContextClickable

### setOnCreateContextMenuListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnCreateContextMenuListener(l: View.OnCreateContextMenuListener!): Unit
```

Register a callback to be invoked when the context menu for this view is being built. If this view is not long clickable, it becomes long clickable.

| Parameters ||
|---|---|
| `l` | [View.OnCreateContextMenuListener](../android/view/View.OnCreateContextMenuListener.md)!: The callback that will run |

### setOnDragListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnDragListener(l: View.OnDragListener!): Unit
```

Register a drag event listener callback object for this View. The parameter is an implementation of `https://developer.android.com/reference/kotlin/android/view/View.OnDragListener`. To send a drag event to a View, the system calls the onDrag method.

| Parameters ||
|---|---|
| `l` | [View.OnDragListener](../android/view/View.OnDragListener.md)!: An implementation of `https://developer.android.com/reference/kotlin/android/view/View.OnDragListener`. |

### setOnFocusChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnFocusChangeListener(l: View.OnFocusChangeListener!): Unit
```

Register a callback to be invoked when focus of this view changed.

| Parameters ||
|---|---|
| `l` | [View.OnFocusChangeListener](../android/view/View.OnFocusChangeListener.md)!: The callback that will run. |

### setOnGenericMotionListener

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnGenericMotionListener(l: View.OnGenericMotionListener!): Unit
```

Register a callback to be invoked when a generic motion event is sent to this view.

| Parameters ||
|---|---|
| `l` | [View.OnGenericMotionListener](../android/view/View.OnGenericMotionListener.md)!: the generic motion listener to attach to this view |

### setOnHoverListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnHoverListener(l: View.OnHoverListener!): Unit
```

Register a callback to be invoked when a hover event is sent to this view.

| Parameters ||
|---|---|
| `l` | [View.OnHoverListener](../android/view/View.OnHoverListener.md)!: the hover listener to attach to this view |

### setOnKeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnKeyListener(l: View.OnKeyListener!): Unit
```

Register a callback to be invoked when a hardware key is pressed in this view. Key presses in software input methods will generally not trigger the methods of this listener.

| Parameters ||
|---|---|
| `l` | [View.OnKeyListener](../android/view/View.OnKeyListener.md)!: the key listener to attach to this view |

### setOnLongClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnLongClickListener(l: View.OnLongClickListener?): Unit
```

Register a callback to be invoked when this view is clicked and held. If this view is not long clickable, it becomes long clickable.

| Parameters ||
|---|---|
| `l` | [View.OnLongClickListener](../android/view/View.OnLongClickListener.md)?: The callback that will run. This value may be `null`. |

**See Also**

- setLongClickable

### setOnReceiveContentListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnReceiveContentListener(
    mimeTypes: Array<String!>?, 
    listener: OnReceiveContentListener?
): Unit
```

Sets the listener to be performReceiveContent to handle insertion of content into this view.

Depending on the type of view, this listener may be invoked for different scenarios. For example, for an editable `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`, this listener will be invoked for the following scenarios:

1. Paste from the clipboard (e.g. "Paste" or "Paste as plain text" action in the insertion/selection menu)
2. Content insertion from the keyboard (from commitContent)
3. Drag and drop (drop events from onDragEvent)
4. Autofill
5. Selection replacement via `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROCESS_TEXT:kotlin.String`

When setting a listener, clients must also declare the accepted MIME types. The listener will still be invoked even if the MIME type of the content is not one of the declared MIME types (e.g. if the user pastes content whose type is not one of the declared MIME types). In that case, the listener may reject the content (defer to the default platform behavior) or execute some other fallback logic (e.g. show an appropriate message to the user). The declared MIME types serve as a hint to allow different features to optionally alter their behavior. For example, a soft keyboard may optionally choose to hide its UI for inserting GIFs for a particular input field if the MIME types set here for that field don't include "image/gif" or "image/\*".

Note: MIME type matching in the Android framework is case-sensitive, unlike formal RFC MIME types. As a result, you should always write your MIME types with lowercase letters, or use normalizeMimeType to ensure that it is converted to lowercase.

| Parameters ||
|---|---|
| `mimeTypes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: The MIME types accepted by the given listener. These may use patterns such as "image/\*", but may not start with a wildcard. This argument must not be null or empty if a non-null listener is passed in. |
| `listener` | [OnReceiveContentListener](OnReceiveContentListener.md)?: The listener to use. This can be null to reset to the default behavior. |

### setOnScrollChangeListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnScrollChangeListener(l: View.OnScrollChangeListener!): Unit
```

Register a callback to be invoked when the scroll X or Y positions of this view change.

**Note:** Some views handle scrolling independently from View and may have their own separate listeners for scroll-type events. For example, `https://developer.android.com/reference/kotlin/android/widget/ListView.html#` allows clients to register an setOnScrollListener to listen for changes in list scroll position.

| Parameters ||
|---|---|
| `l` | [View.OnScrollChangeListener](../android/view/View.OnScrollChangeListener.md)!: The listener to notify when the scroll X or Y position changes. |

**See Also**

- getScrollX
- getScrollY

### setOnSystemUiVisibilityChangeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnSystemUiVisibilityChangeListener(l: View.OnSystemUiVisibilityChangeListener!): Unit
```

**Deprecated:** *Use isVisible to find out about system bar visibilities by setting a `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener` on this view.*

Set a listener to receive callbacks when the visibility of the system bar changes.

| Parameters ||
|---|---|
| `l` | [View.OnSystemUiVisibilityChangeListener](../android/view/View.OnSystemUiVisibilityChangeListener.md)!: The `https://developer.android.com/reference/kotlin/android/view/View.OnSystemUiVisibilityChangeListener` to receive callbacks. |

### setOnTouchListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnTouchListener(l: View.OnTouchListener!): Unit
```

Register a callback to be invoked when a touch event is sent to this view.

| Parameters ||
|---|---|
| `l` | [View.OnTouchListener](../android/view/View.OnTouchListener.md)!: the touch listener to attach to this view |

### setOutlineAmbientShadowColor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOutlineAmbientShadowColor(color: Int): Unit
```

Sets the color of the ambient shadow that is drawn when the view has a positive Z or elevation value.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different views with different colors.

The opacity of the final ambient shadow is a function of the shadow caster height, the alpha channel of the outlineAmbientShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#ambientShadowAlpha:kotlin.Int` theme attribute.

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The color this View will cast for its elevation shadow. |

### setOutlineProvider

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOutlineProvider(provider: ViewOutlineProvider!): Unit
```

Sets the ViewOutlineProvider of the view, which generates the Outline that defines the shape of the shadow it casts, and enables outline clipping.

The default ViewOutlineProvider, `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider#BACKGROUND:android.view.ViewOutlineProvider`, queries the Outline from the View's background drawable, via getOutline. Changing the outline provider with this method allows this behavior to be overridden.

If the ViewOutlineProvider is null, if querying it for an outline returns false, or if the produced Outline is isEmpty, shadows will not be cast.

Only outlines that return true from canClip may be used for clipping.
**See Also**

- setClipToOutline
- getClipToOutline
- getOutlineProvider

### setOutlineSpotShadowColor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOutlineSpotShadowColor(color: Int): Unit
```

Sets the color of the spot shadow that is drawn when the view has a positive Z or elevation value.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different views with different colors.

The opacity of the final spot shadow is a function of the shadow caster height, the alpha channel of the outlineSpotShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#spotShadowAlpha:kotlin.Int` theme attribute.

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The color this View will cast for its elevation spot shadow. |

### setOverScrollMode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOverScrollMode(overScrollMode: Int): Unit
```

Set the over-scroll mode for this view. Valid over-scroll modes are `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_ALWAYS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_IF_CONTENT_SCROLLS:kotlin.Int` (allow over-scrolling only if the view content is larger than the container), or `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_NEVER:kotlin.Int`. Setting the over-scroll mode of a view will have an effect only if the view is capable of scrolling.

| Parameters ||
|---|---|
| `overScrollMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new over-scroll mode for this view. |

### setPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPadding(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Sets the padding. The view may add on the space required to display the scrollbars, depending on the style and visibility of the scrollbars. So the values returned from getPaddingLeft, getPaddingTop, getPaddingRight and getPaddingBottom may be different from the values set in this call.

| Parameters ||
|---|---|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the left padding in pixels |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the top padding in pixels |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the right padding in pixels |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the bottom padding in pixels |

### setPaddingRelative

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPaddingRelative(
    start: Int, 
    top: Int, 
    end: Int, 
    bottom: Int
): Unit
```

Sets the relative padding. The view may add on the space required to display the scrollbars, depending on the style and visibility of the scrollbars. So the values returned from getPaddingStart, getPaddingTop, getPaddingEnd and getPaddingBottom may be different from the values set in this call.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start padding in pixels |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the top padding in pixels |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end padding in pixels |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the bottom padding in pixels |

### setPendingCredentialRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPendingCredentialRequest(
    request: GetCredentialRequest, 
    callback: OutcomeReceiver<GetCredentialResponse!, GetCredentialException!>
): Unit
```

Sets a `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` request to retrieve credentials, when the user focuses on this given view. When this view is focused, the given `request` will be fired to `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#`, which will fetch content from all `https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService.html#` services on the device, and then display credential options to the user on a relevant UI (dropdown, keyboard suggestions etc.). When the user selects a credential, the final `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse.html#` will be propagated to the given `callback`. Developers are expected to handle the response programmatically and perform a relevant action, e.g. signing in the user.

For details on how to build a Credential Manager request, please see `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#`.

This API should be called at any point before the user focuses on the view, e.g. during `onCreate` of an Activity.

| Parameters ||
|---|---|
| `request` | [GetCredentialRequest](../android.credentials/GetCredentialRequest.md): the request to be fired when this view is entered. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [GetCredentialResponse](../android.credentials/GetCredentialResponse.md)!, [GetCredentialException](../android.credentials/GetCredentialException.md)!\>: to be invoked when either a response or an exception needs to be propagated for the given view. This value cannot be `null`. |

### setPivotX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPivotX(pivotX: Float): Unit
```

Sets the x location of the point around which the view is setRotation and setScaleX. By default, the pivot point is centered on the object. Setting this property disables this behavior and causes the view to use only the explicitly set pivotX and pivotY values.

| Parameters ||
|---|---|
| `pivotX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x location of the pivot point. |

**See Also**

- getRotation
- getScaleX
- getScaleY
- getPivotY

### setPivotY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPivotY(pivotY: Float): Unit
```

Sets the y location of the point around which the view is setRotation and setScaleY. By default, the pivot point is centered on the object. Setting this property disables this behavior and causes the view to use only the explicitly set pivotX and pivotY values.

| Parameters ||
|---|---|
| `pivotY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y location of the pivot point. |

**See Also**

- getRotation
- getScaleX
- getScaleY
- getPivotY

### setPointerIcon

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPointerIcon(pointerIcon: PointerIcon!): Unit
```

Set the pointer icon to be used for a mouse pointer in the current view. Passing `null` will restore the pointer icon to its default value. Note that setting the pointer icon using this method will only set it for events coming from a mouse device (i.e. with source `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_MOUSE:kotlin.Int`). To resolve the pointer icon for other device types like styluses, override onResolvePointerIcon.

| Parameters ||
|---|---|
| `pointerIcon` | [PointerIcon](PointerIcon.md)!: A PointerIcon instance which will be shown when the mouse hovers. |

**See Also**

- onResolvePointerIcon
- PointerIcon

### setPreferKeepClear

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPreferKeepClear(preferKeepClear: Boolean): Unit
```

Set a preference to keep the bounds of this view clear from floating windows above this view's window. This informs the system that the view is considered a vital area for the user and that ideally it should not be covered. Setting this is only appropriate for UI where the user would likely take action to uncover it.

The system will try to respect this preference, but when not possible will ignore it.

Note: This is independent from setPreferKeepClearRects. If both are set, both will be taken into account.

<br />

**See Also**

- setPreferKeepClearRects
- isPreferKeepClear

### setPreferKeepClearRects

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPreferKeepClearRects(rects: MutableList<Rect!>): Unit
```

Set a preference to keep the provided rects clear from floating windows above this view's window. This informs the system that these rects are considered vital areas for the user and that ideally they should not be covered. Setting this is only appropriate for UI where the user would likely take action to uncover it.

The system will try to respect this preference, but when not possible will ignore it.

Note: This is independent from setPreferKeepClear. If both are set, both will be taken into account.

<br />

| Parameters ||
|---|---|
| `rects` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](../android.graphics/Rect.md)!\>: A list of rects in this view's local coordinate system. This value cannot be `null`. |

**See Also**

- setPreferKeepClear
- getPreferKeepClearRects

### setPressed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPressed(pressed: Boolean): Unit
```

Sets the pressed state for this view.

| Parameters ||
|---|---|
| `pressed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Pass true to set the View's internal state to "pressed", or false to reverts the View's internal state from a previously set "pressed" state. |

**See Also**

- isClickable
- setClickable

### setRenderEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRenderEffect(renderEffect: RenderEffect?): Unit
```

Configure the `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#` to apply to this View. This will apply a visual effect to the results of the View before it is drawn. For example if createBlurEffect is provided, the contents will be drawn in a separate layer, then this layer will be blurred when this View is drawn.

| Parameters ||
|---|---|
| `renderEffect` | [RenderEffect](../android.graphics/RenderEffect.md)?: to be applied to the View. Passing null clears the previously configured `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#` |

### setRequestedFrameRate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRequestedFrameRate(frameRate: Float): Unit
```

You can set the preferred frame rate for a View using a positive number or by specifying the preferred frame rate category using constants, including REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE, REQUESTED_FRAME_RATE_CATEGORY_LOW, REQUESTED_FRAME_RATE_CATEGORY_NORMAL, REQUESTED_FRAME_RATE_CATEGORY_HIGH. Keep in mind that the preferred frame rate affects the frame rate for the next frame, so use this method carefully. It's important to note that the preference is valid as long as the View is invalidated. Please also be aware that the requested frame rate will not propagate to child views when this API is used on a ViewGroup.

| Parameters ||
|---|---|
| `frameRate` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the preferred frame rate of the view. |

### setRevealOnFocusHint

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRevealOnFocusHint(revealOnFocus: Boolean): Unit
```

Sets this view's preference for reveal behavior when it gains focus.

When set to true, this is a signal to ancestor views in the hierarchy that this view would prefer to be brought fully into view when it gains focus. For example, a text field that a user is meant to type into. Other views such as scrolling containers may prefer to opt-out of this behavior.

The default value for views is true, though subclasses may change this based on their preferred behavior.

| Parameters ||
|---|---|
| `revealOnFocus` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to request reveal on focus in ancestors, false otherwise |

**See Also**

- getRevealOnFocusHint

### setRight

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRight(right: Int): Unit
```

Sets the right position of this view relative to its parent. This method is meant to be called by the layout system and should not generally be called otherwise, because the property may be changed at any time by the layout.

| Parameters ||
|---|---|
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The right of this view, in pixels. |

### setRotation

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRotation(rotation: Float): Unit
```

Sets the degrees that the view is rotated around the pivot point. Increasing values result in clockwise rotation.

| Parameters ||
|---|---|
| `rotation` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The degrees of rotation. |

**See Also**

- getRotation
- getPivotX
- getPivotY
- setRotationX
- setRotationY

### setRotationX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRotationX(rotationX: Float): Unit
```

Sets the degrees that the view is rotated around the horizontal axis through the pivot point. Increasing values result in clockwise rotation from the viewpoint of looking down the x axis. When rotating large views, it is recommended to adjust the camera distance accordingly. Refer to setCameraDistance for more information.

| Parameters ||
|---|---|
| `rotationX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The degrees of X rotation. |

**See Also**

- getRotationX
- getPivotX
- getPivotY
- setRotation
- setRotationY
- setCameraDistance

### setRotationY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRotationY(rotationY: Float): Unit
```

Sets the degrees that the view is rotated around the vertical axis through the pivot point. Increasing values result in counter-clockwise rotation from the viewpoint of looking down the y axis. When rotating large views, it is recommended to adjust the camera distance accordingly. Refer to setCameraDistance for more information.

| Parameters ||
|---|---|
| `rotationY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The degrees of Y rotation. |

**See Also**

- getRotationY
- getPivotX
- getPivotY
- setRotation
- setRotationX
- setCameraDistance

### setSaveEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSaveEnabled(enabled: Boolean): Unit
```

Controls whether the saving of this view's state is enabled (that is, whether its onSaveInstanceState method will be called). Note that even if freezing is enabled, the view still must have an id assigned to it (via setId) for its state to be saved. This flag can only disable the saving of this view; any child views may still have their state saved.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to false to *disable* state saving, or true (the default) to allow it. |

**See Also**

- isSaveEnabled
- setId
- onSaveInstanceState

### setSaveFromParentEnabled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSaveFromParentEnabled(enabled: Boolean): Unit
```

Controls whether the entire hierarchy under this view will save its state when a state saving traversal occurs from its parent. The default is true; if false, these views will not be saved unless saveHierarchyState is called directly on this view.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to false to *disable* state saving, or true (the default) to allow it. |

**See Also**

- isSaveFromParentEnabled
- setId
- onSaveInstanceState

### setScaleX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScaleX(scaleX: Float): Unit
```

Sets the amount that the view is scaled in x around the pivot point, as a proportion of the view's unscaled width. A value of 1 means that no scaling is applied.

| Parameters ||
|---|---|
| `scaleX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scaling factor. |

**See Also**

- getPivotX
- getPivotY

### setScaleY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScaleY(scaleY: Float): Unit
```

Sets the amount that the view is scaled in Y around the pivot point, as a proportion of the view's unscaled width. A value of 1 means that no scaling is applied.

| Parameters ||
|---|---|
| `scaleY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scaling factor. |

**See Also**

- getPivotX
- getPivotY

### setScreenReaderFocusable

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScreenReaderFocusable(screenReaderFocusable: Boolean): Unit
```

Sets whether this View should be a focusable element for screen readers and include non-focusable Views from its subtree when providing feedback.

Note: this is similar to using [`android:focusable`, but does not impact input focus behavior.](View.md)

| Parameters ||
|---|---|
| `screenReaderFocusable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the view should be treated as a unit by screen reader accessibility tools. |

### setScrollBarDefaultDelayBeforeFade

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollBarDefaultDelayBeforeFade(scrollBarDefaultDelayBeforeFade: Int): Unit
```

Define the delay before scrollbars fade.

| Parameters ||
|---|---|
| `scrollBarDefaultDelayBeforeFade` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): - the delay before scrollbars fade |

### setScrollBarFadeDuration

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollBarFadeDuration(scrollBarFadeDuration: Int): Unit
```

Define the scrollbar fade duration.

| Parameters ||
|---|---|
| `scrollBarFadeDuration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): - the scrollbar fade duration, in milliseconds |

### setScrollBarSize

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollBarSize(scrollBarSize: Int): Unit
```

Define the scrollbar size.

| Parameters ||
|---|---|
| `scrollBarSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): - the scrollbar size |

### setScrollBarStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollBarStyle(style: Int): Unit
```

Specify the style of the scrollbars. The scrollbars can be overlaid or inset. When inset, they add to the padding of the view. And the scrollbars can be drawn inside the padding area or on the edge of the view. For example, if a view has a background drawable and you want to draw the scrollbars inside the padding specified by the drawable, you can use SCROLLBARS_INSIDE_OVERLAY or SCROLLBARS_INSIDE_INSET. If you want them to appear at the edge of the view, ignoring the padding, then you can use SCROLLBARS_OUTSIDE_OVERLAY or SCROLLBARS_OUTSIDE_INSET.

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the style of the scrollbars. Should be one of SCROLLBARS_INSIDE_OVERLAY, SCROLLBARS_INSIDE_INSET, SCROLLBARS_OUTSIDE_OVERLAY or SCROLLBARS_OUTSIDE_INSET. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_INSIDE_OVERLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_INSIDE_INSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_OUTSIDE_OVERLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_OUTSIDE_INSET:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_INSIDE_OVERLAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_INSIDE_INSET:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_OUTSIDE_OVERLAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_OUTSIDE_INSET:kotlin.Int`

### setScrollCaptureCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setScrollCaptureCallback(callback: ScrollCaptureCallback?): Unit
```

Sets the callback to receive scroll capture requests. This component is the adapter between the scroll capture API and application UI code. If no callback is set, the system may provide an implementation. Any value provided here will take precedence over a system version.

This view will be ignored when `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE:kotlin.Int` is set in its setScrollCaptureHint, regardless whether a callback has been set.

It is recommended to set the scroll capture hint `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int` when setting a custom callback to help ensure it is selected as the target.

| Parameters ||
|---|---|
| `callback` | [ScrollCaptureCallback](ScrollCaptureCallback.md)?: the new callback to assign. This value may be `null`. |

### setScrollCaptureHint

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollCaptureHint(hint: Int): Unit
```

Sets the scroll capture hint for this View. These flags affect the search for a potential scroll capture targets.

| Parameters ||
|---|---|
| `hint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the scrollCaptureHint flags value to set. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE_DESCENDANTS:kotlin.Int` |

### setScrollContainer

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollContainer(isScrollContainer: Boolean): Unit
```

Change whether this view is one of the set of scrollable containers in its window. This will be used to determine whether the window can resize or must pan when a soft input area is open -- scrollable containers allow the window to use resize mode since the container will appropriately shrink.

### setScrollIndicators

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollIndicators(indicators: Int): Unit
```

Sets the state of all scroll indicators.

See setScrollIndicators for usage information.

| Parameters ||
|---|---|
| `indicators` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a bitmask of indicators that should be enabled, or `0` to disable all indicators. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_BOTTOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_END:kotlin.Int` |

**See Also**

- setScrollIndicators
- getScrollIndicators

### setScrollIndicators

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollIndicators(
    indicators: Int, 
    mask: Int
): Unit
```

Sets the state of the scroll indicators specified by the mask. To change all scroll indicators at once, see setScrollIndicators.

When a scroll indicator is enabled, it will be displayed if the view can scroll in the direction of the indicator.

Multiple indicator types may be enabled or disabled by passing the logical OR of the desired types. If multiple types are specified, they will all be set to the same enabled state.

For example, to enable the top scroll indicatorExample: `setScrollIndicators`

| Parameters ||
|---|---|
| `indicators` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the indicator direction, or the logical OR of multiple indicator directions. One or more of: - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_BOTTOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_END:kotlin.Int` . Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_BOTTOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_END:kotlin.Int` |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_BOTTOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_END:kotlin.Int` |

**See Also**

- setScrollIndicators
- getScrollIndicators

### setScrollX

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollX(value: Int): Unit
```

Set the horizontal scrolled position of your view. This will cause a call to onScrollChanged and the view will be invalidated.

| Parameters ||
|---|---|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the x position to scroll to |

### setScrollY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollY(value: Int): Unit
```

Set the vertical scrolled position of your view. This will cause a call to onScrollChanged and the view will be invalidated.

| Parameters ||
|---|---|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the y position to scroll to |

### setScrollbarFadingEnabled

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollbarFadingEnabled(fadeScrollbars: Boolean): Unit
```

Define whether scrollbars will fade when the view is not scrolling.

| Parameters ||
|---|---|
| `fadeScrollbars` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether to enable fading |

### setSelected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSelected(selected: Boolean): Unit
```

Changes the selection state of this view. A view can be selected or not. Note that selection is not the same as focus. Views are typically selected in the context of an AdapterView like ListView or GridView; the selected view is the view that is highlighted.

| Parameters ||
|---|---|
| `selected` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the view must be selected, false otherwise |

### setSoundEffectsEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSoundEffectsEnabled(soundEffectsEnabled: Boolean): Unit
```

Set whether this view should have sound effects enabled for events such as clicking and touching.

You may wish to disable sound effects for a view if you already play sounds, for instance, a dial key that plays dtmf tones.

| Parameters ||
|---|---|
| `soundEffectsEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether sound effects are enabled for this view. |

**See Also**

- isSoundEffectsEnabled
- playSoundEffect

### setStateDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStateDescription(stateDescription: CharSequence?): Unit
```

Sets the View's state description.

A state description briefly describes the states of the view and is primarily used for accessibility support to determine how the states of a view should be presented to the user. It is a supplement to the boolean states (for example, checked/unchecked) and it is used for customized state description (for example, "wifi, connected, three bars"). State description changes frequently while content description should change less often. State description should be localized. For android widgets which have default state descriptions, app developers can call this method to override the state descriptions. Setting state description to null restores the default behavior.

| Parameters ||
|---|---|
| `stateDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The state description. This value may be `null`. |

**See Also**

- getStateDescription
- setContentDescription

### setStateListAnimator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStateListAnimator(stateListAnimator: StateListAnimator!): Unit
```

Attaches the provided StateListAnimator to this View.

Any previously attached StateListAnimator will be detached.

| Parameters ||
|---|---|
| `stateListAnimator` | [StateListAnimator](../android.animation/StateListAnimator.md)!: The StateListAnimator to update the view |

**See Also**

- `https://developer.android.com/reference/kotlin/android/animation/StateListAnimator.html#`

### setSupplementalDescription

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSupplementalDescription(supplementalDescription: CharSequence?): Unit
```

Sets the View's supplemental description.

A supplemental description provides brief supplemental information for this node, such as the purpose of the node when that purpose is not conveyed within its textual representation. For example, if a dropdown select has a purpose of setting font family, the supplemental description could be "font family". If this node has children, its supplemental description serves as additional information and is not intended to replace any existing information in the subtree. This is different from the setContentDescription in that this description is purely supplemental while a content description may be used to replace a description for a node or its subtree that an assistive technology would otherwise compute based on other properties of the node and its descendants.

This should omit role or state. Role refers to the kind of user-interface element the View is, such as a Button or Checkbox. State refers to a frequently changing property of the View, such as an On/Off state of a button or the audio level of a volume slider.

| Parameters ||
|---|---|
| `supplementalDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The supplemental description. This value may be `null`. |

**See Also**

- getSupplementalDescription
- setContentDescription
- setStateDescription

### setSystemGestureExclusionRects

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSystemGestureExclusionRects(rects: MutableList<Rect!>): Unit
```

Sets a list of areas within this view's post-layout coordinate space where the system should not intercept touch or other pointing device gestures. *This method should be called by onLayout or onDraw.*

Use this to tell the system which specific sub-areas of a view need to receive gesture input in order to function correctly in the presence of global system gestures that may conflict. For example, if the system wishes to capture swipe-in-from-screen-edge gestures to provide system-level navigation functionality, a view such as a navigation drawer container can mark the left (or starting) edge of itself as requiring gesture capture priority using this API. The system may then choose to relax its own gesture recognition to allow the app to consume the user's gesture. It is not necessary for an app to register exclusion rects for broadly spanning regions such as the entirety of a `ScrollView` or for simple press and release click targets such as `Button`. Mark an exclusion rect when interacting with a view requires a precision touch gesture in a small area in either the X or Y dimension, such as an edge swipe or dragging a `SeekBar` thumb.

Note: the system will put a limit of `200dp` on the vertical extent of the exclusions it takes into account. The limit does not apply while the navigation bar is `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_IMMERSIVE_STICKY:kotlin.Int` hidden, nor to the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HOME:kotlin.String`.

| Parameters ||
|---|---|
| `rects` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](../android.graphics/Rect.md)!\>: A list of precision gesture regions that this view needs to function correctly. This value cannot be `null`. |

### setSystemUiVisibility

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSystemUiVisibility(visibility: Int): Unit
```

**Deprecated:** *SystemUiVisibility flags are deprecated. Use WindowInsetsController instead.*

Request that the visibility of the status bar or other screen/window decorations be changed.

This method is used to put the over device UI into temporary modes where the user's attention is focused more on the application content, by dimming or hiding surrounding system affordances. This is typically used in conjunction with `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int`, allowing the applications content to be placed behind the action bar (and with these flags other system affordances) so that smooth transitions between hiding and showing them can be done.

Two representative examples of the use of system UI visibility is implementing a content browsing application (like a magazine reader) and a video playing application.

The first code shows a typical implementation of a View in a content browsing application. In this implementation, the application goes into a content-oriented mode by hiding the status bar and action bar, and putting the navigation elements into lights out mode. The user can then interact with content while in this mode. Such an application should provide an easy way for the user to toggle out of the mode (such as to check information in the status bar or access notifications). In the implementation here, this is done simply by tapping on the content.

This second code sample shows a typical implementation of a View in a video playing application. In this situation, while the video is playing the application would like to go into a complete full-screen mode, to use as much of the display as possible for the video. When in this state the user can not interact with the application; the system intercepts touching on the screen to pop the UI out of full screen mode. See fitSystemWindows for a sample layout that goes with this code.

| Parameters ||
|---|---|
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bitwise-or of flags `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LOW_PROFILE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_STABLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_IMMERSIVE:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_IMMERSIVE_STICKY:kotlin.Int`. |

### setTag

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTag(
    key: Int, 
    tag: Any!
): Unit
```

Sets a tag associated with this view and a key. A tag can be used to mark a view in its hierarchy and does not have to be unique within the hierarchy. Tags can also be used to store data within a view without resorting to another data structure. The specified key should be an id declared in the resources of the application to ensure it is unique (see the [ID resource type](https://developer.android.com/guide/topics/resources/more-resources.html#Id)). Keys identified as belonging to the Android framework or not associated with any package will cause an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` to be thrown.

| Parameters ||
|---|---|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key identifying the tag |
| `tag` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: An Object to tag the view with |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If they specified key is not valid |

**See Also**

- setTag
- getTag

### setTag

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTag(tag: Any!): Unit
```

Sets the tag associated with this view. A tag can be used to mark a view in its hierarchy and does not have to be unique within the hierarchy. Tags can also be used to store data within a view without resorting to another data structure.

| Parameters ||
|---|---|
| `tag` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: an Object to tag the view with |

**See Also**

- getTag
- setTag

### setTextAlignment

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextAlignment(textAlignment: Int): Unit
```

Set the text alignment.

| Parameters ||
|---|---|
| `textAlignment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The text alignment to set. Should be one of `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_INHERIT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_GRAVITY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_CENTER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_START:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_END:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_START:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_END:kotlin.Int` Resolution will be done if the value is set to TEXT_ALIGNMENT_INHERIT. The resolution proceeds up the parent chain of the view to get the value. If there is no parent, then it will return the default `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_GRAVITY:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_INHERIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_GRAVITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_CENTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_END:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_END:kotlin.Int` |

### setTextDirection

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextDirection(textDirection: Int): Unit
```

Set the text direction.

| Parameters ||
|---|---|
| `textDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the direction to set. Should be one of: `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_INHERIT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_ANY_RTL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_LTR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_RTL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_LOCALE:kotlin.Int` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG_LTR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG_RTL:kotlin.Int`, Resolution will be done if the value is set to TEXT_DIRECTION_INHERIT. The resolution proceeds up the parent chain of the view to get the value. If there is no parent, then it will return the default `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG:kotlin.Int`. |

### setTooltipText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTooltipText(tooltipText: CharSequence?): Unit
```

Sets the tooltip text which will be displayed in a small popup next to the view.

The tooltip will be displayed:

- On long click, unless it is handled otherwise (by OnLongClickListener or a context menu).
- On hover, after a brief delay since the pointer has stopped moving

**Note:** Do not override this method, as it will have no effect on the text displayed in the tooltip.

| Parameters ||
|---|---|
| `tooltipText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: the tooltip text, or null if no tooltip is required |

**See Also**

- getTooltipText

### setTop

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTop(top: Int): Unit
```

Sets the top position of this view relative to its parent. This method is meant to be called by the layout system and should not generally be called otherwise, because the property may be changed at any time by the layout.

| Parameters ||
|---|---|
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The top of this view, in pixels. |

### setTouchDelegate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTouchDelegate(delegate: TouchDelegate!): Unit
```

Sets the TouchDelegate for this View.

### setTransitionAlpha

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTransitionAlpha(alpha: Float): Unit
```

This property is intended only for use by the Fade transition, which animates it to produce a visual translucency that does not side-effect (or get affected by) the real alpha property. This value is composited with the other alpha value (and the AlphaAnimation value, when that is present) to produce a final visual translucency result, which is what is passed into the DisplayList.

### setTransitionName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTransitionName(transitionName: String!): Unit
```

Sets the name of the View to be used to identify Views in Transitions. Names should be unique in the View hierarchy.

| Parameters ||
|---|---|
| `transitionName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the View to uniquely identify it for Transitions. |

### setTransitionVisibility

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTransitionVisibility(visibility: Int): Unit
```

Changes the visibility of this View without triggering any other changes. This should only be used by animation frameworks, such as `https://developer.android.com/reference/kotlin/android/transition/Transition.html#`, where visibility changes should not adjust focus or trigger a new layout. Application developers should use setVisibility instead to ensure that the hierarchy is correctly updated.

Only call this method when a temporary visibility must be applied during an animation and the original visibility value is guaranteed to be reset after the animation completes. Use setVisibility in all other cases.

| Parameters ||
|---|---|
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` |

**See Also**

- setVisibility

### setTranslationX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTranslationX(translationX: Float): Unit
```

Sets the horizontal location of this view relative to its getLeft position. This effectively positions the object post-layout, in addition to wherever the object's layout placed it.

| Parameters ||
|---|---|
| `translationX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The horizontal position of this view relative to its left position, in pixels. |

### setTranslationY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTranslationY(translationY: Float): Unit
```

Sets the vertical location of this view relative to its getTop position. This effectively positions the object post-layout, in addition to wherever the object's layout placed it.

| Parameters ||
|---|---|
| `translationY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The vertical position of this view relative to its top position, in pixels. |

### setTranslationZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTranslationZ(translationZ: Float): Unit
```

Sets the depth location of this view relative to its getElevation.

### setVerticalFadingEdgeEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVerticalFadingEdgeEnabled(verticalFadingEdgeEnabled: Boolean): Unit
```

Define whether the vertical edges should be faded when this view is scrolled vertically.

| Parameters ||
|---|---|
| `verticalFadingEdgeEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the vertical edges should be faded when the view is scrolled vertically |

**See Also**

- isVerticalFadingEdgeEnabled

### setVerticalScrollBarEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVerticalScrollBarEnabled(verticalScrollBarEnabled: Boolean): Unit
```

Define whether the vertical scrollbar should be drawn or not. The scrollbar is not drawn by default.

| Parameters ||
|---|---|
| `verticalScrollBarEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the vertical scrollbar should be painted |

**See Also**

- isVerticalScrollBarEnabled

### setVerticalScrollbarPosition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVerticalScrollbarPosition(position: Int): Unit
```

Set the position of the vertical scroll bar. Should be one of `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBAR_POSITION_DEFAULT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBAR_POSITION_LEFT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBAR_POSITION_RIGHT:kotlin.Int`.

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Where the vertical scroll bar should be positioned. |

### setVerticalScrollbarThumbDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVerticalScrollbarThumbDrawable(drawable: Drawable?): Unit
```

Defines the vertical scrollbar thumb drawable

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md)?: This value may be `null`. |

**See Also**

- awakenScrollBars
- isVerticalScrollBarEnabled
- setVerticalScrollBarEnabled

### setVerticalScrollbarTrackDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVerticalScrollbarTrackDrawable(drawable: Drawable?): Unit
```

Defines the vertical scrollbar track drawable

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md)?: This value may be `null`. |

**See Also**

- awakenScrollBars
- isVerticalScrollBarEnabled
- setVerticalScrollBarEnabled

### setViewTranslationCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewTranslationCallback(callback: ViewTranslationCallback): Unit
```

Sets a ViewTranslationCallback that is used to display/hide the translated information. Developers can provide the customized implementation for show/hide translated information.

| Parameters ||
|---|---|
| `callback` | [ViewTranslationCallback](../android.view.translation/ViewTranslationCallback.md): a ViewTranslationCallback that is used to control how to display the translated information. This value cannot be `null`. |

### setVisibility

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVisibility(visibility: Int): Unit
```

Set the visibility state of this view.

| Parameters ||
|---|---|
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` |

### setWillNotCacheDrawing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWillNotCacheDrawing(willNotCacheDrawing: Boolean): Unit
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

When a View's drawing cache is enabled, drawing is redirected to an offscreen bitmap. Some views, like an ImageView, must be able to bypass this mechanism if they already draw a single bitmap, to avoid unnecessary usage of the memory.

| Parameters ||
|---|---|
| `willNotCacheDrawing` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if this view does not cache its drawing, false otherwise |

### setWillNotDraw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWillNotDraw(willNotDraw: Boolean): Unit
```

If this view doesn't do any drawing on its own, set this flag to allow further optimizations. By default, this flag is not set on View, but could be set on some View subclasses such as ViewGroup. Typically, if you override onDraw you should clear this flag.

| Parameters ||
|---|---|
| `willNotDraw` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether or not this View draw on its own |

### setWindowInsetsAnimationCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWindowInsetsAnimationCallback(callback: WindowInsetsAnimation.Callback?): Unit
```

Sets a `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback` to be notified about animations of windows that cause insets.

The callback's getDispatchMode will affect whether animation callbacks are dispatched to the children of this view.

| Parameters ||
|---|---|
| `callback` | [WindowInsetsAnimation.Callback](../android/view/WindowInsetsAnimation.Callback.md)?: The callback to set. This value may be `null`. |

### setX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setX(x: Float): Unit
```

Sets the visual x position of this view, in pixels. This is equivalent to setting the setTranslationX property to be the difference between the x value passed in and the current getLeft property.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The visual x position of this view, in pixels. |

### setY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setY(y: Float): Unit
```

Sets the visual y position of this view, in pixels. This is equivalent to setting the setTranslationY property to be the difference between the y value passed in and the current getTop property.

| Parameters ||
|---|---|
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The visual y position of this view, in pixels. |

### setZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setZ(z: Float): Unit
```

Sets the visual z position of this view, in pixels. This is equivalent to setting the setTranslationZ property to be the difference between the z value passed in and the current getElevation property.

| Parameters ||
|---|---|
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The visual z position of this view, in pixels. |

### showContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun showContextMenu(): Boolean
```

Shows the context menu for this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the context menu was shown, `false` otherwise |

**See Also**

- showContextMenu

### showContextMenu

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun showContextMenu(
    x: Float, 
    y: Float
): Boolean
```

Shows the context menu for this view anchored to the specified view-relative coordinate.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the X coordinate in pixels relative to the view to which the menu should be anchored, or `https://developer.android.com/reference/kotlin/java/lang/Float.html#NaN:kotlin.Float` to disable anchoring |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the Y coordinate in pixels relative to the view to which the menu should be anchored, or `https://developer.android.com/reference/kotlin/java/lang/Float.html#NaN:kotlin.Float` to disable anchoring |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the context menu was shown, `false` otherwise |

### startActionMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startActionMode(callback: ActionMode.Callback!): ActionMode!
```

Start an action mode with the default type `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int`.

| Parameters ||
|---|---|
| `callback` | [ActionMode.Callback](../android/view/ActionMode.Callback.md)!: Callback that will control the lifecycle of the action mode |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ActionMode!` | The new action mode if it is started, null otherwise |

**See Also**

- ActionMode
- startActionMode

### startActionMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startActionMode(
    callback: ActionMode.Callback!, 
    type: Int
): ActionMode!
```

Start an action mode with the given type.

| Parameters ||
|---|---|
| `callback` | [ActionMode.Callback](../android/view/ActionMode.Callback.md)!: Callback that will control the lifecycle of the action mode |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_FLOATING:kotlin.Int`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ActionMode!` | The new action mode if it is started, null otherwise |

**See Also**

- ActionMode

### startAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startAnimation(animation: Animation!): Unit
```

Start the specified animation now.

| Parameters ||
|---|---|
| `animation` | [Animation](../android.view.animation/Animation.md)!: the animation to start now |

### startDrag

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startDrag(
    data: ClipData!, 
    shadowBuilder: View.DragShadowBuilder!, 
    myLocalState: Any!, 
    flags: Int
): Boolean
```

**Deprecated:** *Use startDragAndDrop for newer platform versions.*

### startDragAndDrop

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startDragAndDrop(
    data: ClipData!, 
    shadowBuilder: View.DragShadowBuilder!, 
    myLocalState: Any!, 
    flags: Int
): Boolean
```

Starts a drag and drop operation. When your application calls this method, it passes a `https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder` object to the system. The system calls this object's onProvideShadowMetrics to get metrics for the drag shadow, and then calls the object's onDrawShadow to draw the drag shadow itself.

Once the system has the drag shadow, it begins the drag and drop operation by sending drag events to all the View objects in your application that are currently visible. It does this either by calling the View object's drag listener (an implementation of onDrag or by calling the View object's onDragEvent method. Both are passed a DragEvent object that has a getAction value of `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_STARTED:kotlin.Int`.

Your application can invoke startDragAndDrop on any attached View object. The View object does not need to be the one used in `https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder`, nor does it need to be related to the View the user selected for dragging.

| Parameters ||
|---|---|
| `data` | [ClipData](../android.content/ClipData.md)!: A `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object pointing to the data to be transferred by the drag and drop operation. |
| `shadowBuilder` | [View.DragShadowBuilder](../android/view/View.DragShadowBuilder.md)!: A `https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder` object for building the drag shadow. |
| `myLocalState` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: An `https://developer.android.com/reference/kotlin/java/lang/Object.html#` containing local data about the drag and drop operation. When dispatching drag events to views in the same activity this object will be available through getLocalState. Views in other activities will not have access to this data (getLocalState will return null). myLocalState is a lightweight mechanism for the sending information from the dragged View to the target Views. For example, it can contain flags that differentiate between a a copy operation and a move operation. |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags that control the drag and drop operation. This can be set to 0 for no flags, or any combination of the following: - `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_PERSISTABLE_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_PREFIX_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_READ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_WRITE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_OPAQUE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_ACCESSIBILITY_ACTION:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the method completes successfully, or `false` if it fails anywhere. Returning `false` means the system was unable to do a drag because of another ongoing operation or some other reasons. |

### startNestedScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startNestedScroll(axes: Int): Boolean
```

Begin a nestable scroll operation along the given axes.

A view starting a nested scroll promises to abide by the following contract:

The view will call startNestedScroll upon initiating a scroll operation. In the case of a touch scroll this corresponds to the initial `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int`. In the case of touch scrolling the nested scroll will be terminated automatically in the same manner as requestDisallowInterceptTouchEvent. In the event of programmatic scrolling the caller must explicitly call stopNestedScroll to indicate the end of the nested scroll.

If `startNestedScroll` returns true, a cooperative parent was found. If it returns false the caller may ignore the rest of this contract until the next scroll. Calling startNestedScroll while a nested scroll is already in progress will return true.

At each incremental step of the scroll the caller should invoke dispatchNestedPreScroll once it has calculated the requested scrolling delta. If it returns true the nested scrolling parent at least partially consumed the scroll and the caller should adjust the amount it scrolls by.

After applying the remainder of the scroll delta the caller should invoke dispatchNestedScroll, passing both the delta consumed and the delta unconsumed. A nested scrolling parent may treat these values differently. See onNestedScroll.

| Parameters ||
|---|---|
| `axes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags consisting of a combination of `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_HORIZONTAL:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_VERTICAL:kotlin.Int`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a cooperative parent was found and nested scrolling has been enabled for the current gesture. |

**See Also**

- stopNestedScroll
- dispatchNestedPreScroll
- dispatchNestedScroll

### stopNestedScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stopNestedScroll(): Unit
```

Stop a nested scroll in progress.

Calling this method when a nested scroll is not currently in progress is harmless.
**See Also**

- startNestedScroll

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### transformMatrixToGlobal

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun transformMatrixToGlobal(matrix: Matrix): Unit
```

Modifies the input matrix such that it maps view-local coordinates to on-screen coordinates.

| Parameters ||
|---|---|
| `matrix` | [Matrix](../android.graphics/Matrix.md): input matrix to modify. This value cannot be `null`. |

### transformMatrixToLocal

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun transformMatrixToLocal(matrix: Matrix): Unit
```

Modifies the input matrix such that it maps on-screen coordinates to view-local coordinates.

| Parameters ||
|---|---|
| `matrix` | [Matrix](../android.graphics/Matrix.md): input matrix to modify. This value cannot be `null`. |

### unregisterCalledFromWrongThreadListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun unregisterCalledFromWrongThreadListener(listener: View.CalledFromWrongThreadListener): Unit
```

Unregisters a listener that was previously registered with registerCalledFromWrongThreadListener.

| Parameters ||
|---|---|
| `listener` | [View.CalledFromWrongThreadListener](../android/view/View.CalledFromWrongThreadListener.md): The listener to unregister. This value cannot be `null`. |

**See Also**

### unscheduleDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unscheduleDrawable(who: Drawable!): Unit
```

Unschedule any events associated with the given Drawable. This can be used when selecting a new Drawable into a view, so that the previous one is completely unscheduled.

| Parameters ||
|---|---|
| `who` | [Drawable](../android.graphics.drawable/Drawable.md)!: The Drawable to unschedule. |

**See Also**

- drawableStateChanged

### unscheduleDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unscheduleDrawable(
    who: Drawable, 
    what: Runnable
): Unit
```

Cancels a scheduled action on a drawable.

| Parameters ||
|---|---|
| `who` | [Drawable](../android.graphics.drawable/Drawable.md): the recipient of the action. This value cannot be `null`. |
| `what` | [Runnable](../java.lang/Runnable.md): the action to cancel. This value cannot be `null`. |

### updateDragShadow

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun updateDragShadow(shadowBuilder: View.DragShadowBuilder!): Unit
```

Updates the drag shadow for the ongoing drag and drop operation.

| Parameters ||
|---|---|
| `shadowBuilder` | [View.DragShadowBuilder](../android/view/View.DragShadowBuilder.md)!: A `https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder` object for building the new drag shadow. |

### willNotCacheDrawing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun willNotCacheDrawing(): Boolean
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, setLayerType handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call draw on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the PixelCopy API is recommended.*

Returns whether or not this View can cache its drawing or not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this view does not cache its drawing, false otherwise |

### willNotDraw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun willNotDraw(): Boolean
```

Returns whether or not this View draws on its own.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this view has nothing to draw, false otherwise |

## Protected methods

### awakenScrollBars

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun awakenScrollBars(): Boolean
```

Trigger the scrollbars to draw. When invoked this method starts an animation to fade the scrollbars out after a default delay. If a subclass provides animated scrolling, the start delay should equal the duration of the scrolling animation.

The animation starts only if at least one of the scrollbars is enabled, as specified by isHorizontalScrollBarEnabled and isVerticalScrollBarEnabled. When the animation is started, this method returns true, and false otherwise. If the animation is started, this method calls invalidate; in that case the caller should not call invalidate.

This method should be invoked every time a subclass directly updates the scroll parameters.

This method is automatically invoked by scrollBy and scrollTo.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the animation is played, false otherwise |

**See Also**

- awakenScrollBars
- scrollBy
- scrollTo
- isHorizontalScrollBarEnabled
- isVerticalScrollBarEnabled
- setHorizontalScrollBarEnabled
- setVerticalScrollBarEnabled

### awakenScrollBars

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun awakenScrollBars(startDelay: Int): Boolean
```

Trigger the scrollbars to draw. When invoked this method starts an animation to fade the scrollbars out after a fixed delay. If a subclass provides animated scrolling, the start delay should equal the duration of the scrolling animation.

The animation starts only if at least one of the scrollbars is enabled, as specified by isHorizontalScrollBarEnabled and isVerticalScrollBarEnabled. When the animation is started, this method returns true, and false otherwise. If the animation is started, this method calls invalidate; in that case the caller should not call invalidate.

This method should be invoked every time a subclass directly updates the scroll parameters.

| Parameters ||
|---|---|
| `startDelay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the delay, in milliseconds, after which the animation should start; when the delay is 0, the animation starts immediately |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the animation is played, false otherwise |

**See Also**

- scrollBy
- scrollTo
- isHorizontalScrollBarEnabled
- isVerticalScrollBarEnabled
- setHorizontalScrollBarEnabled
- setVerticalScrollBarEnabled

### awakenScrollBars

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun awakenScrollBars(
    startDelay: Int, 
    invalidate: Boolean
): Boolean
```

Trigger the scrollbars to draw. When invoked this method starts an animation to fade the scrollbars out after a fixed delay. If a subclass provides animated scrolling, the start delay should equal the duration of the scrolling animation.

The animation starts only if at least one of the scrollbars is enabled, as specified by isHorizontalScrollBarEnabled and isVerticalScrollBarEnabled. When the animation is started, this method returns true, and false otherwise. If the animation is started, this method calls invalidate if the invalidate parameter is set to true; in that case the caller should not call invalidate.

This method should be invoked every time a subclass directly updates the scroll parameters.

| Parameters ||
|---|---|
| `startDelay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the delay, in milliseconds, after which the animation should start; when the delay is 0, the animation starts immediately |
| `invalidate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether this method should call invalidate if an animation is scheduled |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the animation is played, false otherwise |

**See Also**

- scrollBy
- scrollTo
- isHorizontalScrollBarEnabled
- isVerticalScrollBarEnabled
- setHorizontalScrollBarEnabled
- setVerticalScrollBarEnabled

### computeHorizontalScrollExtent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun computeHorizontalScrollExtent(): Int
```

Compute the horizontal extent of the horizontal scrollbar's thumb within the horizontal range. This value is used to compute the length of the thumb within the scrollbar's track.

The range is expressed in arbitrary units that must be the same as the units used by computeHorizontalScrollRange and computeHorizontalScrollOffset.

The default extent is the drawing width of this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the horizontal extent of the scrollbar's thumb |

**See Also**

- computeHorizontalScrollRange
- computeHorizontalScrollOffset

### computeHorizontalScrollOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun computeHorizontalScrollOffset(): Int
```

Compute the horizontal offset of the horizontal scrollbar's thumb within the horizontal range. This value is used to compute the position of the thumb within the scrollbar's track.

The range is expressed in arbitrary units that must be the same as the units used by computeHorizontalScrollRange and computeHorizontalScrollExtent.

The default offset is the scroll offset of this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the horizontal offset of the scrollbar's thumb |

**See Also**

- computeHorizontalScrollRange
- computeHorizontalScrollExtent

### computeHorizontalScrollRange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun computeHorizontalScrollRange(): Int
```

Compute the horizontal range that the horizontal scrollbar represents.

The range is expressed in arbitrary units that must be the same as the units used by computeHorizontalScrollExtent and computeHorizontalScrollOffset.

The default range is the drawing width of this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the total horizontal range represented by the horizontal scrollbar |

**See Also**

- computeHorizontalScrollExtent
- computeHorizontalScrollOffset

### computeVerticalScrollExtent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun computeVerticalScrollExtent(): Int
```

Compute the vertical extent of the vertical scrollbar's thumb within the vertical range. This value is used to compute the length of the thumb within the scrollbar's track.

The range is expressed in arbitrary units that must be the same as the units used by computeVerticalScrollRange and computeVerticalScrollOffset.

The default extent is the drawing height of this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the vertical extent of the scrollbar's thumb |

**See Also**

- computeVerticalScrollRange
- computeVerticalScrollOffset

### computeVerticalScrollOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun computeVerticalScrollOffset(): Int
```

Compute the vertical offset of the vertical scrollbar's thumb within the horizontal range. This value is used to compute the position of the thumb within the scrollbar's track.

The range is expressed in arbitrary units that must be the same as the units used by computeVerticalScrollRange and computeVerticalScrollExtent.

The default offset is the scroll offset of this view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the vertical offset of the scrollbar's thumb |

**See Also**

- computeVerticalScrollRange
- computeVerticalScrollExtent

### computeVerticalScrollRange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun computeVerticalScrollRange(): Int
```

Compute the vertical range that the vertical scrollbar represents.

The range is expressed in arbitrary units that must be the same as the units used by computeVerticalScrollExtent and computeVerticalScrollOffset.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the total vertical range represented by the vertical scrollbar The default range is the drawing height of this view. |

**See Also**

- computeVerticalScrollExtent
- computeVerticalScrollOffset

### dispatchDraw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchDraw(canvas: Canvas): Unit
```

Called by draw to draw the child views. This may be overridden by derived classes to gain control just before its children are drawn (but after its own view has been drawn).

| Parameters ||
|---|---|
| `canvas` | [Canvas](../android.graphics/Canvas.md): the canvas on which to draw the view. This value cannot be `null`. |

### dispatchGenericFocusedEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchGenericFocusedEvent(event: MotionEvent!): Boolean
```

Dispatch a generic motion event to the currently focused view.

Do not call this method directly. Call dispatchGenericMotionEvent instead.

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The motion event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

### dispatchGenericPointerEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchGenericPointerEvent(event: MotionEvent!): Boolean
```

Dispatch a generic motion event to the view under the first pointer.

Do not call this method directly. Call dispatchGenericMotionEvent instead.

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The motion event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

### dispatchHoverEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchHoverEvent(event: MotionEvent!): Boolean
```

Dispatch a hover event.

Do not call this method directly. Call dispatchGenericMotionEvent instead.

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md)!: The motion event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

### dispatchRestoreInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchRestoreInstanceState(container: SparseArray<Parcelable!>!): Unit
```

Called by restoreHierarchyState to retrieve the state for this view and its children. May be overridden to modify how restoring happens to a view's children; for example, some views may want to not store state for their children.

| Parameters ||
|---|---|
| `container` | [SparseArray](../android.util/SparseArray.md)\< [Parcelable](../android.os/Parcelable.md)!\>!: The SparseArray which holds previously saved state. |

**See Also**

- dispatchSaveInstanceState
- restoreHierarchyState
- onRestoreInstanceState

### dispatchSaveInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchSaveInstanceState(container: SparseArray<Parcelable!>!): Unit
```

Called by saveHierarchyState to store the state for this view and its children. May be overridden to modify how freezing happens to a view's children; for example, some views may want to not store state for their children.

| Parameters ||
|---|---|
| `container` | [SparseArray](../android.util/SparseArray.md)\< [Parcelable](../android.os/Parcelable.md)!\>!: The SparseArray in which to save the view's state. |

**See Also**

- dispatchRestoreInstanceState
- saveHierarchyState
- onSaveInstanceState

### dispatchSetActivated

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchSetActivated(activated: Boolean): Unit
```

Dispatch setActivated to all of this View's children.

| Parameters ||
|---|---|
| `activated` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The new activated state |

**See Also**

- setActivated

### dispatchSetPressed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchSetPressed(pressed: Boolean): Unit
```

Dispatch setPressed to all of this View's children.

| Parameters ||
|---|---|
| `pressed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The new pressed state |

**See Also**

- setPressed

### dispatchSetSelected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchSetSelected(selected: Boolean): Unit
```

Dispatch setSelected to all of this View's children.

| Parameters ||
|---|---|
| `selected` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The new selected state |

**See Also**

- setSelected

### dispatchVisibilityChanged

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchVisibilityChanged(
    changedView: View, 
    visibility: Int
): Unit
```

Dispatch a view visibility change down the view hierarchy. ViewGroups should override to route to their children.

| Parameters ||
|---|---|
| `changedView` | [View](View.md): The view whose visibility changed. Could be 'this' or an ancestor view. This value cannot be `null`. |
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new visibility of changedView: `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` |

### drawableStateChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun drawableStateChanged(): Unit
```

This function is called whenever the state of the view changes in such a way that it impacts the state of drawables being shown.

If the View has a StateListAnimator, it will also be called to run necessary state change animations.

Be sure to call through to the superclass when overriding this function. 
If you override this method you *must* call through to the superclass implementation.
**See Also**

- setState

### fitSystemWindows

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun fitSystemWindows(insets: Rect!): Boolean
```

**Deprecated:** *As of API 20 use dispatchApplyWindowInsets to apply insets to views. Views should override onApplyWindowInsets or use setOnApplyWindowInsetsListener to implement handling their own insets.*

Called by the view hierarchy when the content insets for a window have changed, to allow it to adjust its content to fit within those windows. The content insets tell you the space that the status bar, input method, and other system windows infringe on the application's window.

You do not normally need to deal with this function, since the default window decoration given to applications takes care of applying it to the content of the window. If you use `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int` this will not be the case, and your content can be placed under those system elements. You can then use this method within your view hierarchy if you have parts of your UI which you would like to ensure are not being covered.

The default implementation of this method simply applies the content insets to the view's padding, consuming that content (modifying the insets to be 0), and returning true. This behavior is off by default, but can be enabled through setFitsSystemWindows.

This function's traversal down the hierarchy is depth-first. The same content insets object is propagated down the hierarchy, so any changes made to it will be seen by all following views (including potentially ones above in the hierarchy since this is a depth-first traversal). The first view that returns true will abort the entire traversal.

The default implementation works well for a situation where it is used with a container that covers the entire window, allowing it to apply the appropriate insets to its content on all edges. If you need a more complicated layout (such as two different views fitting system windows, one on the top of the window, and one on the bottom), you can override the method and handle the insets however you would like. Note that the insets provided by the framework are always relative to the far edges of the window, not accounting for the location of the called view within that window. (In fact when this method is called you do not yet know where the layout will place the view, as it is done before layout happens.)

Note: unlike many View methods, there is no dispatch phase to this call. If you are overriding it in a ViewGroup and want to allow the call to continue to your children, you must be sure to call the super implementation.

Here is a sample layout that makes use of fitting system windows to have controls for a video view placed inside of the window decorations that it hides and shows. This can be used with code like the second sample (video player) shown in setSystemUiVisibility.

| Parameters ||
|---|---|
| `insets` | [Rect](../android.graphics/Rect.md)!: Current content insets of the window. Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN:kotlin.Int` you must not modify the insets or else you and Android will be unhappy. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this view applied the insets and it should not continue propagating further down the hierarchy, `false` otherwise. |

**See Also**

- getFitsSystemWindows
- setFitsSystemWindows
- setSystemUiVisibility

### getBottomFadingEdgeStrength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getBottomFadingEdgeStrength(): Float
```

Returns the strength, or intensity, of the bottom faded edge. The strength is a value between 0.0 (no fade) and 1.0 (full fade). The default implementation returns 0.0 or 1.0 but no value in between. Subclasses should override this method to provide a smoother fade transition when scrolling occurs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the intensity of the bottom fade as a float between 0.0f and 1.0f |

### getBottomPaddingOffset

Added in [API level 2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getBottomPaddingOffset(): Int
```

Amount by which to extend the bottom fading region. Called only when isPaddingOffsetRequired returns true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The bottom padding offset in pixels. |

**See Also**

- isPaddingOffsetRequired

### getContextMenuInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getContextMenuInfo(): ContextMenu.ContextMenuInfo!
```

Views should implement this if they have extra information to associate with the context menu. The return result is supplied as a parameter to the onCreateContextMenu callback.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo!` | Extra information about the item for which the context menu should be shown. This information will vary across different subclasses of View. |

### getHorizontalScrollbarHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getHorizontalScrollbarHeight(): Int
```

Returns the height of the horizontal scrollbar.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The height in pixels of the horizontal scrollbar or 0 if there is no horizontal scrollbar. |

### getLeftFadingEdgeStrength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getLeftFadingEdgeStrength(): Float
```

Returns the strength, or intensity, of the left faded edge. The strength is a value between 0.0 (no fade) and 1.0 (full fade). The default implementation returns 0.0 or 1.0 but no value in between. Subclasses should override this method to provide a smoother fade transition when scrolling occurs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the intensity of the left fade as a float between 0.0f and 1.0f |

### getLeftPaddingOffset

Added in [API level 2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getLeftPaddingOffset(): Int
```

Amount by which to extend the left fading region. Called only when isPaddingOffsetRequired returns true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The left padding offset in pixels. |

**See Also**

- isPaddingOffsetRequired

### getRightFadingEdgeStrength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getRightFadingEdgeStrength(): Float
```

Returns the strength, or intensity, of the right faded edge. The strength is a value between 0.0 (no fade) and 1.0 (full fade). The default implementation returns 0.0 or 1.0 but no value in between. Subclasses should override this method to provide a smoother fade transition when scrolling occurs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the intensity of the right fade as a float between 0.0f and 1.0f |

### getRightPaddingOffset

Added in [API level 2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getRightPaddingOffset(): Int
```

Amount by which to extend the right fading region. Called only when isPaddingOffsetRequired returns true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The right padding offset in pixels. |

**See Also**

- isPaddingOffsetRequired

### getSuggestedMinimumHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getSuggestedMinimumHeight(): Int
```

Returns the suggested minimum height that the view should use. This returns the maximum of the view's minimum height and the background's minimum height (getMinimumHeight).

When being used in onMeasure, the caller should still ensure the returned height is within the requirements of the parent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The suggested minimum height of the view. |

### getSuggestedMinimumWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getSuggestedMinimumWidth(): Int
```

Returns the suggested minimum width that the view should use. This returns the maximum of the view's minimum width and the background's minimum width (getMinimumWidth).

When being used in onMeasure, the caller should still ensure the returned width is within the requirements of the parent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The suggested minimum width of the view. |

### getTopFadingEdgeStrength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getTopFadingEdgeStrength(): Float
```

Returns the strength, or intensity, of the top faded edge. The strength is a value between 0.0 (no fade) and 1.0 (full fade). The default implementation returns 0.0 or 1.0 but no value in between. Subclasses should override this method to provide a smoother fade transition when scrolling occurs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the intensity of the top fade as a float between 0.0f and 1.0f |

### getTopPaddingOffset

Added in [API level 2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getTopPaddingOffset(): Int
```

Amount by which to extend the top fading region. Called only when isPaddingOffsetRequired returns true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The top padding offset in pixels. |

**See Also**

- isPaddingOffsetRequired

### getWindowAttachCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getWindowAttachCount(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of times this view has been attached to a window |

### isPaddingOffsetRequired

Added in [API level 2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun isPaddingOffsetRequired(): Boolean
```

If the View draws content inside its padding and enables fading edges, it needs to support padding offsets. Padding offsets are added to the fading edges to extend the length of the fade so that it covers pixels drawn inside the padding. Subclasses of this class should override this method if they need to draw content inside the padding.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if padding offset must be applied, false otherwise. |

**See Also**

- getLeftPaddingOffset
- getRightPaddingOffset
- getTopPaddingOffset
- getBottomPaddingOffset

### mergeDrawableStates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open static fun mergeDrawableStates(
    baseState: IntArray!, 
    additionalState: IntArray!
): IntArray!
```

Merge your own state values in additionalState into the base state values baseState that were returned by onCreateDrawableState.

| Parameters ||
|---|---|
| `baseState` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The base state values returned by onCreateDrawableState, which will be modified to also hold your own additional state values. |
| `additionalState` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The additional state values you would like added to baseState; this array is not modified. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | As a convenience, the baseState array you originally passed into the function is returned. |

**See Also**

- onCreateDrawableState

### onAnimationEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onAnimationEnd(): Unit
```

Invoked by a parent ViewGroup to notify the end of the animation currently associated with this view. If you override this method, always call super.onAnimationEnd();. 
If you override this method you *must* call through to the superclass implementation.
**See Also**

- setAnimation
- getAnimation

### onAnimationStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onAnimationStart(): Unit
```

Invoked by a parent ViewGroup to notify the start of the animation currently associated with this view. If you override this method, always call super.onAnimationStart();. 
If you override this method you *must* call through to the superclass implementation.
**See Also**

- setAnimation
- getAnimation

### onAttachedToWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onAttachedToWindow(): Unit
```

This is called when the view is attached to a window. At this point it has a Surface and will start drawing. Note that this function is guaranteed to be called before onDraw, however it may be called any time before the first onDraw -- including before or after onMeasure. 
If you override this method you *must* call through to the superclass implementation.
**See Also**

- onDetachedFromWindow

### onConfigurationChanged

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onConfigurationChanged(newConfig: Configuration!): Unit
```

Called when the current configuration of the resources being used by the application have changed. You can use this to decide when to reload resources that can changed based on orientation and other configuration characteristics. You only need to use this if you are not relying on the normal `https://developer.android.com/reference/kotlin/android/app/Activity.html#` mechanism of recreating the activity instance upon a configuration change.

| Parameters ||
|---|---|
| `newConfig` | [Configuration](../android.content.res/Configuration.md)!: The new resource configuration. |

### onCreateContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onCreateContextMenu(menu: ContextMenu!): Unit
```

Views should implement this if the view itself is going to add items to the context menu.

| Parameters ||
|---|---|
| `menu` | [ContextMenu](ContextMenu.md)!: the context menu to populate |

### onCreateDrawableState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onCreateDrawableState(extraSpace: Int): IntArray!
```

Generate the new `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` state for this view. This is called by the view system when the cached Drawable state is determined to be invalid. To retrieve the current state, you should use getDrawableState.

| Parameters ||
|---|---|
| `extraSpace` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): if non-zero, this is the number of extra entries you would like in the returned array in which you can place your own states. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | Returns an array holding the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` state of the view. |

**See Also**

- mergeDrawableStates

### onDetachedFromWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onDetachedFromWindow(): Unit
```

This is called when the view is detached from a window. At this point it no longer has a surface for drawing. 
If you override this method you *must* call through to the superclass implementation.
**See Also**

- onAttachedToWindow

### onDisplayHint

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onDisplayHint(hint: Int): Unit
```

Gives this view a hint about whether is displayed or not. For instance, when a View moves out of the screen, it might receives a display hint indicating the view is not displayed. Applications should not *rely* on this hint as there is no guarantee that they will receive one.

| Parameters ||
|---|---|
| `hint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A hint about whether or not this view is displayed: `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` |

### onDraw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onDraw(canvas: Canvas): Unit
```

Implement this to do your drawing.

| Parameters ||
|---|---|
| `canvas` | [Canvas](../android.graphics/Canvas.md): the canvas on which the background will be drawn. This value cannot be `null`. |

### onDrawScrollBars

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun onDrawScrollBars(canvas: Canvas): Unit
```

Request the drawing of the horizontal and the vertical scrollbar. The scrollbars are painted only if they have been awakened first.

| Parameters ||
|---|---|
| `canvas` | [Canvas](../android.graphics/Canvas.md): the canvas on which to draw the scrollbars. This value cannot be `null`. |

**See Also**

- awakenScrollBars

### onFinishInflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onFinishInflate(): Unit
```

Finalize inflating a view from XML. This is called as the last phase of inflation, after all child views have been added.

Even if the subclass overrides onFinishInflate, they should always be sure to call the super method, so that we get called. 
If you override this method you *must* call through to the superclass implementation.

### onFocusChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onFocusChanged(
    gainFocus: Boolean, 
    direction: Int, 
    previouslyFocusedRect: Rect?
): Unit
```

Called by the view system when the focus state of this view changes. When the focus change event is caused by directional navigation, direction and previouslyFocusedRect provide insight into where the focus is coming from. When overriding, be sure to call up through to the super class so that the standard focus handling will occur. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `gainFocus` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the View has focus; false otherwise. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction focus has moved when requestFocus() is called to give this view focus. Values are `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int`. It may not always apply, in which case use the default. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` |
| `previouslyFocusedRect` | [Rect](../android.graphics/Rect.md)?: The rectangle, in this view's coordinate system, of the previously focused view. If applicable, this will be passed in as finer grained information about where the focus is coming from (in addition to direction). Will be `null` otherwise. |
| --- | --- |

### onLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onLayout(
    changed: Boolean, 
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Called from layout when this view should assign a size and position to each of its children. Derived classes with children should override this method and call layout on each of their children.

| Parameters ||
|---|---|
| `changed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): This is a new size or position for this view |
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Left position, relative to parent |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Top position, relative to parent |
| --- | --- |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Right position, relative to parent |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bottom position, relative to parent |

### onMeasure

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onMeasure(
    widthMeasureSpec: Int, 
    heightMeasureSpec: Int
): Unit
```

Measure the view and its content to determine the measured width and the measured height. This method is invoked by measure and should be overridden by subclasses to provide accurate and efficient measurement of their contents.

**CONTRACT:** When overriding this method, you *must* call setMeasuredDimension to store the measured width and height of this view. Failure to do so will trigger an `IllegalStateException`, thrown by measure. Calling the superclass' onMeasure is a valid use.

The base class implementation of measure defaults to the background size, unless a larger size is allowed by the MeasureSpec. Subclasses should override onMeasure to provide better measurements of their content.

If this method is overridden, it is the subclass's responsibility to make sure the measured height and width are at least the view's minimum height and width (getSuggestedMinimumHeight and getSuggestedMinimumWidth).

| Parameters ||
|---|---|
| `widthMeasureSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): horizontal space requirements as imposed by the parent. The requirements are encoded with `https://developer.android.com/reference/kotlin/android/view/View.MeasureSpec`. |
| `heightMeasureSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): vertical space requirements as imposed by the parent. The requirements are encoded with `https://developer.android.com/reference/kotlin/android/view/View.MeasureSpec`. |

**See Also**

- getMeasuredWidth
- getMeasuredHeight
- setMeasuredDimension
- getSuggestedMinimumHeight
- getSuggestedMinimumWidth
- getMode
- getSize

### onOverScrolled

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onOverScrolled(
    scrollX: Int, 
    scrollY: Int, 
    clampedX: Boolean, 
    clampedY: Boolean
): Unit
```

Called by overScrollBy to respond to the results of an over-scroll operation.

| Parameters ||
|---|---|
| `scrollX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): New X scroll value in pixels |
| `scrollY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): New Y scroll value in pixels |
| `clampedX` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if scrollX was clamped to an over-scroll boundary |
| --- | --- |
| `clampedY` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if scrollY was clamped to an over-scroll boundary |

### onRestoreInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onRestoreInstanceState(state: Parcelable!): Unit
```

Hook allowing a view to re-apply a representation of its internal state that had previously been generated by onSaveInstanceState. This function will never be called with a null state. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `state` | [Parcelable](../android.os/Parcelable.md)!: The frozen state that had previously been returned by onSaveInstanceState. |

**See Also**

- onSaveInstanceState
- restoreHierarchyState
- dispatchRestoreInstanceState

### onSaveInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onSaveInstanceState(): Parcelable?
```

Hook allowing a view to generate a representation of its internal state that can later be used to create a new instance with that same state. This state should only contain information that is not persistent or can not be reconstructed later. For example, you will never store your current position on screen because that will be computed again when a new instance of the view is placed in its view hierarchy.

Some examples of things you may store here: the current cursor position in a text view (but usually not the text itself since that is stored in a content provider or other persistent storage), the currently selected item in a list view. 
If you override this method you *must* call through to the superclass implementation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#?` | Returns a Parcelable object containing the view's current dynamic state, or null if there is nothing interesting to save. |

**See Also**

- onRestoreInstanceState
- saveHierarchyState
- dispatchSaveInstanceState
- setSaveEnabled

### onScrollChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onScrollChanged(
    l: Int, 
    t: Int, 
    oldl: Int, 
    oldt: Int
): Unit
```

This is called in response to an internal scroll in this view (i.e., the view scrolled its own contents). This is typically as a result of scrollBy or scrollTo having been called.

| Parameters ||
|---|---|
| `l` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Current horizontal scroll origin. |
| `t` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Current vertical scroll origin. |
| `oldl` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Previous horizontal scroll origin. |
| --- | --- |
| `oldt` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Previous vertical scroll origin. |

### onSetAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onSetAlpha(alpha: Int): Boolean
```

Invoked if there is a Transform that involves alpha. Subclass that can draw themselves with the specified alpha should return true, and then respect that alpha when their onDraw() is called. If this returns false then the view may be redirected to draw into an offscreen buffer to fulfill the request, which will look fine, but may be slower than if the subclass handles it internally. The default implementation returns false.

| Parameters ||
|---|---|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The alpha (0..255) to apply to the view's drawing |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the view can draw with the specified alpha. |

### onSizeChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onSizeChanged(
    w: Int, 
    h: Int, 
    oldw: Int, 
    oldh: Int
): Unit
```

This is called during layout when the size of this view has changed. If you were just added to the view hierarchy, you're called with the old values of 0.

| Parameters ||
|---|---|
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Current width of this view. |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Current height of this view. |
| `oldw` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Old width of this view. |
| --- | --- |
| `oldh` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Old height of this view. |

### onVisibilityChanged

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onVisibilityChanged(
    changedView: View, 
    visibility: Int
): Unit
```

Called when the visibility of the view or an ancestor of the view has changed.

| Parameters ||
|---|---|
| `changedView` | [View](View.md): The view whose visibility changed. May be `this` or an ancestor view. This value cannot be `null`. |
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new visibility, one of `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` |

### onWindowVisibilityChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onWindowVisibilityChanged(visibility: Int): Unit
```

Called when the window containing has change its visibility (between `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`). Note that this tells you whether or not your window is being made visible to the window manager; this does *not* tell you whether or not your window is obscured by other windows on the screen, even if it is itself visible.

| Parameters ||
|---|---|
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new visibility of the window. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` |

### overScrollBy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun overScrollBy(
    deltaX: Int, 
    deltaY: Int, 
    scrollX: Int, 
    scrollY: Int, 
    scrollRangeX: Int, 
    scrollRangeY: Int, 
    maxOverScrollX: Int, 
    maxOverScrollY: Int, 
    isTouchEvent: Boolean
): Boolean
```

Scroll the view with standard behavior for scrolling beyond the normal content boundaries. Views that call this method should override onOverScrolled to respond to the results of an over-scroll operation. Views can use this method to handle any touch or fling-based scrolling.

| Parameters ||
|---|---|
| `deltaX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Change in X in pixels |
| `deltaY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Change in Y in pixels |
| `scrollX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Current X scroll value in pixels before applying deltaX |
| --- | --- |
| `scrollY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Current Y scroll value in pixels before applying deltaY |
| `scrollRangeX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Maximum content scroll range along the X axis |
| `scrollRangeY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Maximum content scroll range along the Y axis |
| --- | --- |
| `maxOverScrollX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of pixels to overscroll by in either direction along the X axis. |
| `maxOverScrollY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of pixels to overscroll by in either direction along the Y axis. |
| `isTouchEvent` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if this scroll operation is the result of a touch event. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if scrolling was clamped to an over-scroll boundary along either axis, false otherwise. |

### setMeasuredDimension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun setMeasuredDimension(
    measuredWidth: Int, 
    measuredHeight: Int
): Unit
```

This method must be called by onMeasure to store the measured width and measured height. Failing to do so will trigger an exception at measurement time.

| Parameters ||
|---|---|
| `measuredWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The measured width of this view. May be a complex bit mask as defined by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_TOO_SMALL:kotlin.Int`. |
| `measuredHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The measured height of this view. May be a complex bit mask as defined by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_TOO_SMALL:kotlin.Int`. |

### verifyDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun verifyDrawable(who: Drawable): Boolean
```

If your view subclass is displaying its own Drawable objects, it should override this function and return true for any Drawable it is displaying. This allows animations for those drawables to be scheduled.

Be sure to call through to the super class when overriding this function. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `who` | [Drawable](../android.graphics.drawable/Drawable.md): The Drawable to verify. Return true if it is one you are displaying, else return the result of calling through to the super class. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean If true then the Drawable is being displayed in the view; else false and it is not allowed to animate. |

**See Also**

- unscheduleDrawable
- drawableStateChanged

## Properties

### ALPHA

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALPHA: Property<View!, Float!>!
```

A Property wrapper around the `alpha` functionality handled by the setAlpha and getAlpha methods.

### EMPTY_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val EMPTY_STATE_SET: IntArray!
```

Indicates the view has no states set. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`
- getDrawableState

### ENABLED_FOCUSED_SELECTED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ENABLED_FOCUSED_SELECTED_STATE_SET: IntArray!
```

Indicates the view is enabled, focused and selected.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`

### ENABLED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ENABLED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is enabled, focused, selected and its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### ENABLED_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ENABLED_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is enabled and has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`

### ENABLED_FOCUSED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ENABLED_FOCUSED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is enabled, focused and its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### ENABLED_SELECTED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ENABLED_SELECTED_STATE_SET: IntArray!
```

Indicates the view is enabled and selected.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`

### ENABLED_SELECTED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ENABLED_SELECTED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is enabled, selected and its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### ENABLED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ENABLED_STATE_SET: IntArray!
```

Indicates the view is enabled. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`
- getDrawableState

### ENABLED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ENABLED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is enabled and that its window has focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### FOCUSED_SELECTED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val FOCUSED_SELECTED_STATE_SET: IntArray!
```

Indicates the view is focused and selected.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`

### FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is focused, selected and its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val FOCUSED_STATE_SET: IntArray!
```

Indicates the view is focused. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`
- getDrawableState

### FOCUSED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val FOCUSED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view has the focus and that its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### PRESSED_ENABLED_FOCUSED_SELECTED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_ENABLED_FOCUSED_SELECTED_STATE_SET: IntArray!
```

Indicates the view is pressed, enabled, focused and selected.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`

### PRESSED_ENABLED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_ENABLED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is pressed, enabled, focused, selected and its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### PRESSED_ENABLED_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_ENABLED_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is pressed, enabled and focused.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`

### PRESSED_ENABLED_FOCUSED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_ENABLED_FOCUSED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is pressed, enabled, focused and its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### PRESSED_ENABLED_SELECTED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_ENABLED_SELECTED_STATE_SET: IntArray!
```

Indicates the view is pressed, enabled and selected.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`

### PRESSED_ENABLED_SELECTED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_ENABLED_SELECTED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is pressed, enabled, selected and its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### PRESSED_ENABLED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_ENABLED_STATE_SET: IntArray!
```

Indicates the view is pressed and enabled.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`

### PRESSED_ENABLED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_ENABLED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is pressed, enabled and its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### PRESSED_FOCUSED_SELECTED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_FOCUSED_SELECTED_STATE_SET: IntArray!
```

Indicates the view is pressed, focused and selected.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`

### PRESSED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is pressed, focused, selected and its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### PRESSED_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is pressed and focused.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`

### PRESSED_FOCUSED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_FOCUSED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is pressed, focused and its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### PRESSED_SELECTED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_SELECTED_STATE_SET: IntArray!
```

Indicates the view is pressed and selected.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`

### PRESSED_SELECTED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_SELECTED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is pressed, selected and its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### PRESSED_STATE_SET

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_STATE_SET: IntArray!
```

Indicates the view is pressed. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`
- getDrawableState

### PRESSED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val PRESSED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is pressed and its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### ROTATION

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROTATION: Property<View!, Float!>!
```

A Property wrapper around the `rotation` functionality handled by the setRotation and getRotation methods.

### ROTATION_X

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROTATION_X: Property<View!, Float!>!
```

A Property wrapper around the `rotationX` functionality handled by the setRotationX and getRotationX methods.

### ROTATION_Y

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROTATION_Y: Property<View!, Float!>!
```

A Property wrapper around the `rotationY` functionality handled by the setRotationY and getRotationY methods.

### SCALE_X

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALE_X: Property<View!, Float!>!
```

A Property wrapper around the `scaleX` functionality handled by the setScaleX and getScaleX methods.

### SCALE_Y

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALE_Y: Property<View!, Float!>!
```

A Property wrapper around the `scaleY` functionality handled by the setScaleY and getScaleY methods.

### SELECTED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val SELECTED_STATE_SET: IntArray!
```

Indicates the view is selected. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`
- getDrawableState

### SELECTED_WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val SELECTED_WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view is selected and that its window has the focus.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`
- `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

### TRANSLATION_X

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSLATION_X: Property<View!, Float!>!
```

A Property wrapper around the `translationX` functionality handled by the setTranslationX and getTranslationX methods.

### TRANSLATION_Y

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSLATION_Y: Property<View!, Float!>!
```

A Property wrapper around the `translationY` functionality handled by the setTranslationY and getTranslationY methods.

### TRANSLATION_Z

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSLATION_Z: Property<View!, Float!>!
```

A Property wrapper around the `translationZ` functionality handled by the setTranslationZ and getTranslationZ methods.

### WINDOW_FOCUSED_STATE_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val WINDOW_FOCUSED_STATE_SET: IntArray!
```

Indicates the view's window has focus. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`
- getDrawableState

### X

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val X: Property<View!, Float!>!
```

A Property wrapper around the `x` functionality handled by the setX and getX methods.

### Y

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val Y: Property<View!, Float!>!
```

A Property wrapper around the `y` functionality handled by the setY and getY methods.

### Z

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val Z: Property<View!, Float!>!
```

A Property wrapper around the `z` functionality handled by the setZ and getZ methods.
