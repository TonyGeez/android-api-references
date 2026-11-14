Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewGroup

```
abstract class ViewGroup : View, ViewManager, ViewParent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.view.View](https://developer.android.com/reference/kotlin/android/view/View) ||
| | ↳ | [android.view.ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup#) |

Known Direct Subclasses [AbsoluteLayout](https://developer.android.com/reference/kotlin/android/widget/AbsoluteLayout.html#), [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#), [FragmentBreadCrumbs](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs.html#), [FrameLayout](https://developer.android.com/reference/kotlin/android/widget/FrameLayout.html#), [GridLayout](https://developer.android.com/reference/kotlin/android/widget/GridLayout.html#), [InlineContentView](https://developer.android.com/reference/kotlin/android/widget/inline/InlineContentView.html#), [LinearLayout](https://developer.android.com/reference/kotlin/android/widget/LinearLayout.html#), [RelativeLayout](https://developer.android.com/reference/kotlin/android/widget/RelativeLayout.html#), [SlidingDrawer](https://developer.android.com/reference/kotlin/android/widget/SlidingDrawer.html#), [Toolbar](https://developer.android.com/reference/kotlin/android/widget/Toolbar.html#), [TvAdView](https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdView.html#), [TvInteractiveAppView](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView.html#), and 1 others. [AbsoluteLayout](https://developer.android.com/reference/kotlin/android/widget/AbsoluteLayout.html#) A layout that lets you specify exact locations (x/y coordinates) of its children.
[AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#) An AdapterView is a view whose children are determined by an `https://developer.android.com/reference/kotlin/android/widget/Adapter.html#`.
[FragmentBreadCrumbs](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs.html#) Helper class for showing "bread crumbs" representing the fragment stack in an activity.
[FrameLayout](https://developer.android.com/reference/kotlin/android/widget/FrameLayout.html#) FrameLayout is designed to block out an area on the screen to display a single item.
[GridLayout](https://developer.android.com/reference/kotlin/android/widget/GridLayout.html#) A layout that places its children in a rectangular *grid*.
[InlineContentView](https://developer.android.com/reference/kotlin/android/widget/inline/InlineContentView.html#) This class represents a view that holds opaque content from another app that you can inline in your UI.
[LinearLayout](https://developer.android.com/reference/kotlin/android/widget/LinearLayout.html#) A layout that arranges other views either horizontally in a single column or vertically in a single row.
[RelativeLayout](https://developer.android.com/reference/kotlin/android/widget/RelativeLayout.html#) A Layout where the positions of the children can be described in relation to each other or to the parent.
[SlidingDrawer](https://developer.android.com/reference/kotlin/android/widget/SlidingDrawer.html#) SlidingDrawer hides content out of the screen and allows the user to drag a handle to bring the content on screen.
[Toolbar](https://developer.android.com/reference/kotlin/android/widget/Toolbar.html#) A standard toolbar for use within application content.
[TvAdView](https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdView.html#) Displays contents of TV advertisement services.
[TvInteractiveAppView](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView.html#) Displays contents of interactive TV applications.
[TvView](https://developer.android.com/reference/kotlin/android/media/tv/TvView.html#) Displays TV contents.
Known Indirect Subclasses [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#), [AbsSpinner](https://developer.android.com/reference/kotlin/android/widget/AbsSpinner.html#), [ActionMenuView](https://developer.android.com/reference/kotlin/android/widget/ActionMenuView.html#), [AdapterViewAnimator](https://developer.android.com/reference/kotlin/android/widget/AdapterViewAnimator.html#), [AdapterViewFlipper](https://developer.android.com/reference/kotlin/android/widget/AdapterViewFlipper.html#), [AppWidgetHostView](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHostView.html#), [CalendarView](https://developer.android.com/reference/kotlin/android/widget/CalendarView.html#), [DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#), [DialerFilter](https://developer.android.com/reference/kotlin/android/widget/DialerFilter.html#), [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.html#), [Gallery](https://developer.android.com/reference/kotlin/android/widget/Gallery.html#), [GestureOverlayView](https://developer.android.com/reference/kotlin/android/gesture/GestureOverlayView.html#), and 24 others. [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#) Base class that can be used to implement virtualized lists of items.
[AbsSpinner](https://developer.android.com/reference/kotlin/android/widget/AbsSpinner.html#) An abstract base class for spinner widgets.
[ActionMenuView](https://developer.android.com/reference/kotlin/android/widget/ActionMenuView.html#) ActionMenuView is a presentation of a series of menu options as a View.
[AdapterViewAnimator](https://developer.android.com/reference/kotlin/android/widget/AdapterViewAnimator.html#) Base class for a `https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#` that will perform animations when switching between its views.
[AdapterViewFlipper](https://developer.android.com/reference/kotlin/android/widget/AdapterViewFlipper.html#) Simple `https://developer.android.com/reference/kotlin/android/widget/ViewAnimator.html#` that will animate between two or more views that have been added to it.
[AppWidgetHostView](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHostView.html#) Provides the glue to show AppWidget views.
[CalendarView](https://developer.android.com/reference/kotlin/android/widget/CalendarView.html#) This class is a calendar widget for displaying and selecting dates.
[DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#) Provides a widget for selecting a date.
[DialerFilter](https://developer.android.com/reference/kotlin/android/widget/DialerFilter.html#) This widget is a layout that contains several specifically-named child views that handle keyboard entry interpreted as standard phone dialpad digits.
[ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.html#) A view that shows items in a vertically scrolling two-level list.
[Gallery](https://developer.android.com/reference/kotlin/android/widget/Gallery.html#) A view that shows items in a center-locked, horizontally scrolling list.
[GestureOverlayView](https://developer.android.com/reference/kotlin/android/gesture/GestureOverlayView.html#) A transparent overlay for gesture input that can be placed on top of other widgets or contain other widgets.
[GridView](https://developer.android.com/reference/kotlin/android/widget/GridView.html#) A view that shows items in two-dimensional scrolling grid.
[HorizontalScrollView](https://developer.android.com/reference/kotlin/android/widget/HorizontalScrollView.html#) Layout container for a view hierarchy that can be scrolled by the user, allowing it to be larger than the physical display.
[ImageSwitcher](https://developer.android.com/reference/kotlin/android/widget/ImageSwitcher.html#) `https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher.html#` that switches between two ImageViews when a new image is set on it.
[ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#) Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list.
[MediaController](https://developer.android.com/reference/kotlin/android/widget/MediaController.html#) A view containing controls for a MediaPlayer.
[NumberPicker](https://developer.android.com/reference/kotlin/android/widget/NumberPicker.html#) A widget that enables the user to select a number from a predefined range.
[RadioGroup](https://developer.android.com/reference/kotlin/android/widget/RadioGroup.html#) This class is used to create a multiple-exclusion scope for a set of radio buttons.
[ScrollView](https://developer.android.com/reference/kotlin/android/widget/ScrollView.html#) A view group that allows the view hierarchy placed within it to be scrolled.
[SearchView](https://developer.android.com/reference/kotlin/android/widget/SearchView.html#) A widget that provides a user interface for the user to enter a search query and submit a request to a search provider.
[Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner.html#) A view that displays one child at a time and lets the user pick among them.
[SplashScreenView](https://developer.android.com/reference/kotlin/android/window/SplashScreenView.html#) The view which allows an activity to customize its splash screen exit animation.
[StackView](https://developer.android.com/reference/kotlin/android/widget/StackView.html#) A view that displays its children in a stack and allows users to discretely swipe through the children.
[TabHost](https://developer.android.com/reference/kotlin/android/widget/TabHost.html#) Container for a tabbed window view.
[TabWidget](https://developer.android.com/reference/kotlin/android/widget/TabWidget.html#) Displays a list of tab labels representing each page in the parent's tab collection.
[TableLayout](https://developer.android.com/reference/kotlin/android/widget/TableLayout.html#) A layout that arranges its children into rows and columns.
[TableRow](https://developer.android.com/reference/kotlin/android/widget/TableRow.html#) A layout that arranges its children horizontally.
[TextSwitcher](https://developer.android.com/reference/kotlin/android/widget/TextSwitcher.html#) Specialized `https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher.html#` that contains only children of type `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`.
[TimePicker](https://developer.android.com/reference/kotlin/android/widget/TimePicker.html#) A widget for selecting the time of day, in either 24-hour or AM/PM mode.
[TwoLineListItem](https://developer.android.com/reference/kotlin/android/widget/TwoLineListItem.html#) A view group with two children, intended for use in ListViews.
[ViewAnimator](https://developer.android.com/reference/kotlin/android/widget/ViewAnimator.html#) Base class for a `https://developer.android.com/reference/kotlin/android/widget/FrameLayout.html#` container that will perform animations when switching between its views.
[ViewFlipper](https://developer.android.com/reference/kotlin/android/widget/ViewFlipper.html#) Simple `https://developer.android.com/reference/kotlin/android/widget/ViewAnimator.html#` that will animate between two or more views that have been added to it.
[ViewSwitcher](https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher.html#) `https://developer.android.com/reference/kotlin/android/widget/ViewAnimator.html#` that switches between two views, and has a factory from which these views are created.
[WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView.html#) A View that displays web pages.
[ZoomControls](https://developer.android.com/reference/kotlin/android/widget/ZoomControls.html#) The `ZoomControls` class displays a simple set of controls used for zooming and provides callbacks to register for events.

A `ViewGroup` is a special view that can contain other views (called children.) The view group is the base class for layouts and views containers. This class also defines the `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams` class which serves as the base class for layouts parameters.

Also see `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams` for layout attributes.

> [!NOTE]
>
> ### Developer Guides
>
> For more information about creating user interface layouts, read the [XML Layouts](https://developer.android.com/guide/topics/ui/declaring-layout.html) developer guide.

Here is a complete implementation of a custom ViewGroup that implements a simple `https://developer.android.com/reference/kotlin/android/widget/FrameLayout.html#` along with the ability to stack children in left and right gutters.

If you are implementing XML layout attributes as shown in the example, this is the corresponding definition for them that would go in `res/values/attrs.xml`:

Finally the layout manager can be used in an XML layout like so:

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams` LayoutParams are used by views to tell their parents how they want to be laid out. |
| open | `https://developer.android.com/reference/kotlin/android/view/ViewGroup.MarginLayoutParams` Per-child layout information for layouts that support margins. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/ViewGroup.OnHierarchyChangeListener` Interface definition for a callback to be invoked when the hierarchy within this view changed. |

| XML attributes ||
|---|---|
| [`android:addStatesFromChildren`](https://developer.android.com/reference/kotlin/android/view/ViewGroup#attr_ViewGroup) | Sets whether this ViewGroup's drawable states also include its children's drawable states. |
| [`android:alwaysDrawnWithCache`](https://developer.android.com/reference/kotlin/android/view/ViewGroup#attr_ViewGroup) | Defines whether the ViewGroup should always draw its children using their drawing cache or not. |
| [`android:animateLayoutChanges`](https://developer.android.com/reference/kotlin/android/view/ViewGroup#attr_ViewGroup) | Defines whether changes in layout (caused by adding and removing items) should cause a LayoutTransition to run. |
| [`android:animationCache`](https://developer.android.com/reference/kotlin/android/view/ViewGroup#attr_ViewGroup) | Defines whether layout animations should create a drawing cache for their children. |
| [`android:clipChildren`](https://developer.android.com/reference/kotlin/android/view/ViewGroup#attr_ViewGroup) | Defines whether a child is limited to draw inside of its bounds or not. |
| [`android:clipToPadding`](https://developer.android.com/reference/kotlin/android/view/ViewGroup#attr_ViewGroup) | Defines whether the ViewGroup will clip its children and resize (but not clip) any EdgeEffect to its padding, if padding is not zero. |
| [`android:descendantFocusability`](https://developer.android.com/reference/kotlin/android/view/ViewGroup#attr_ViewGroup) | Defines the relationship between the ViewGroup and its descendants when looking for a View to take focus. |
| [`android:layoutAnimation`](https://developer.android.com/reference/kotlin/android/view/ViewGroup#attr_ViewGroup) | Defines the layout animation to use the first time the ViewGroup is laid out. |
| [`android:layoutMode`](https://developer.android.com/reference/kotlin/android/view/ViewGroup#attr_ViewGroup) | Defines the layout mode of this ViewGroup. |
| [`android:persistentDrawingCache`](https://developer.android.com/reference/kotlin/android/view/ViewGroup#attr_ViewGroup) | Defines the persistence of the drawing cache. |
| [`android:splitMotionEvents`](https://developer.android.com/reference/kotlin/android/view/ViewGroup#attr_ViewGroup) | Sets whether this ViewGroup should split MotionEvents to separate child views during touch event dispatch. |

Inherited XML attributes From class `https://developer.android.com/reference/kotlin/android/view/View` `https://developer.android.com/reference/kotlin/android/view/View#attr_View` Whether or not this view is a heading for accessibility purposes.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Whether or not allow clicks on disabled view.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` alpha property of the view, as a value between 0 (completely transparent) and 1 (completely opaque).

May be a floating point value, such as "`1.2`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` A drawable to use as the background. This can be either a reference to a full drawable resource (such as a PNG image, 9-patch, XML state list description, etc), or a solid color such as "#ff000000" (black).

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

May be a color value, in the form of "`rgb`", "`argb`", "`rrggbb`", or "`aarrggbb`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines whether this view reacts to click events.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View`

Whether the View's Outline should be used to clip the contents of the View.

Only a single non-rectangular clip can be applied on a View at any time. Circular clips from a android.view.ViewAnimationUtils#createCircularReveal(View,int,int,float,float) circular reveal animation take priority over Outline clipping, and child Outline clipping takes priority over Outline clipping done by a parent.

Note that this flag will only be respected if the View's Outline returns true from `https://developer.android.com/reference/kotlin/android/graphics/Outline.html#canClip()`.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines text that briefly describes content of the view. This property is used primarily for accessibility. Since some views do not have textual representation this attribute can be used for providing such.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the quality of translucent drawing caches. This property is used only when the drawing cache is enabled and translucent. The default value is auto. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11.

Must be one of the following constant values.
Constant Value Description auto 0 Lets the framework decide what quality level should be used for the drawing cache. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. high 2 High quality. When set to high quality, the drawing cache uses a higher color depth but uses more memory. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. low 1 Low quality. When set to low quality, the drawing cache uses a lower color depth, thus losing precision in rendering gradients, but uses less memory. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11.

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` When this attribute is set to true, the view gets its drawable state (focused, pressed, etc.) from its direct parent rather than from itself.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines whether to fade out scrollbars when they are not in use.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the length of the fading edges.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Specifies whether to filter touches when the view's window is obscured by another visible window. When set to true, the view will not receive touches whenever a toast, dialog or other window appears above the view's window. Refer to the `https://developer.android.com/reference/kotlin/android/view/View` security documentation for more details.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Boolean internal attribute to adjust view layout based on system windows such as the status bar. If true, adjusts the padding of this view to leave space for the system windows. Will only take effect if this view is in a non-embedded activity.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Controls whether a view can take focus. By default, this is "auto" which lets the framework determine whether a user can move focus to a view. By setting this attribute to true the view is allowed to take focus. By setting it to "false" the view will not take focus. This value does not impact the behavior of directly calling android.view.View#requestFocus, which will always request focus regardless of this view. It only impacts where focus navigation will try to move focus.

May be a boolean value, such as "`true`" or "`false`".

Must be one of the following constant values.
Constant Value Description auto 10

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Boolean that controls whether a view can take focus while in touch mode. If this is true for a view, that view can gain focus when clicked on, and can keep focus if another view is clicked on that doesn't have this attribute set to true.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Whether this view is a default-focus view. Only one view per keyboard navigation cluster can have this attribute set to true. See `https://developer.android.com/reference/kotlin/android/view/View#setFocusedByDefault(kotlin.Boolean)`.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Boolean that controls whether a view should have haptic feedback enabled for events such as long presses.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Supply an identifier name for this view, to later retrieve it with `https://developer.android.com/reference/kotlin/android/view/View#findViewById(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/app/Activity.html#findViewById(kotlin.Int)`. This must be a resource reference; typically you set this using the `@+` syntax to create a new ID resources. For example: `android:id="@+id/my_id"` which allows you to later retrieve the view with `findViewById(R.id.my_id)`.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Set this if the view will serve as a scrolling container, meaning that it can be resized to shrink its overall window so that there will be space for an input method. If not set, the default value will be true if "scrollbars" has the vertical scrollbar set, else it will be false.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Controls whether the view's window should keep the screen on while visible.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Whether this view is a root of a keyboard navigation cluster. See `https://developer.android.com/reference/kotlin/android/view/View#setKeyboardNavigationCluster(kotlin.Boolean)`.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Specifies the type of layer backing this view. The default value is none. Refer to `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` for more information.

Must be one of the following constant values.
Constant Value Description hardware 2 Use a hardware layer. Refer to `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` for more information. none 0 Don't use a layer. software 1 Use a software layer. Refer to `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the direction of layout drawing. This typically is associated with writing direction of the language script used. The possible values are "ltr" for Left-to-Right, "rtl" for Right-to-Left, "locale", and "inherit" from parent view. If there is nothing to inherit, "locale" is used. "locale" falls back to "en-US". "ltr" is the direction used in "en-US". The default for this attribute is "inherit".

Must be one of the following constant values.
Constant Value Description inherit 2 Inherit from parent. locale 3 Locale. ltr 0 Left-to-Right. rtl 1 Right-to-Left.

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines whether this view reacts to long click events.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the minimum height of the view. It is not guaranteed the view will be able to achieve this minimum height (for example, if its parent layout constrains it with less available height).

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the minimum width of the view. It is not guaranteed the view will be able to achieve this minimum width (for example, if its parent layout constrains it with less available width).

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the next keyboard navigation cluster. If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the next view to give focus to when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the next view to give focus to when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int`. If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the next view to give focus to when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int` If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the next view to give focus to when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int` If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Name of the method in this View's context to invoke when the view is clicked. This name must correspond to a public method that takes exactly one parameter of type View. For instance, if you specify `android:onClick="sayHello"`, you must declare a `public void sayHello(View v)` method of your context (typically, your Activity).
`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the color of the ambient shadow that is drawn when the view has a positive Z or elevation value.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different views with different colors.

The opacity of the final ambient shadow is a function of the shadow caster height, the alpha channel of the outlineAmbientShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#ambientShadowAlpha:kotlin.Int` theme attribute.

May be a color value, in the form of "`rgb`", "`argb`", "`rrggbb`", or "`aarrggbb`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the color of the spot shadow that is drawn when the view has a positive Z or elevation value.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different views with different colors.

The opacity of the final spot shadow is a function of the shadow caster height, the alpha channel of the outlineSpotShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#spotShadowAlpha:kotlin.Int` theme attribute.

May be a color value, in the form of "`rgb`", "`argb`", "`rrggbb`", or "`aarrggbb`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the padding, in pixels, of all four edges. Padding is defined as space between the edges of the view and the view's content. This value will take precedence over any of the edge-specific values (paddingLeft, paddingTop, paddingRight, paddingBottom, paddingHorizontal and paddingVertical), but will not override paddingStart or paddingEnd, if set. A view's size will include its padding. If a `https://developer.android.com/reference/kotlin/android/R.attr.html#background:kotlin.Int` is provided, the padding will initially be set to that (0 if the drawable does not have padding). Explicitly setting a padding value will override the corresponding padding found in the background.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the padding, in pixels, of the bottom edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the padding, in pixels, of the end edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the padding, in pixels, of the left and right edges; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`. This value will take precedence over paddingLeft and paddingRight, but not paddingStart or paddingEnd (if set).

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the padding, in pixels, of the left edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the padding, in pixels, of the right edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the padding, in pixels, of the start edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the padding, in pixels, of the top edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the padding, in pixels, of the top and bottom edges; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`. This value will take precedence over paddingTop and paddingBottom, if set.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines which edges should be faded on scrolling.

Must be one or more (separated by '|') of the following constant values.
Constant Value Description horizontal 1000 Fades horizontal edges only. none 0 No edge is faded. vertical 2000 Fades vertical edges only.

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` rotation of the view, in degrees.

May be a floating point value, such as "`1.2`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` rotation of the view around the x axis, in degrees.

May be a floating point value, such as "`1.2`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` rotation of the view around the y axis, in degrees.

May be a floating point value, such as "`1.2`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` If false, no state will be saved for this view when it is being frozen. The default is true, allowing the view to be saved (however it also must have an ID assigned to it for its state to be saved). Setting this to false only disables the state for this view, not for its children which may still be saved.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` scale of the view in the x direction.

May be a floating point value, such as "`1.2`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` scale of the view in the y direction.

May be a floating point value, such as "`1.2`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` The initial horizontal scroll offset, in pixels.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` The initial vertical scroll offset, in pixels.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines whether the horizontal scrollbar track should always be drawn.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines whether the vertical scrollbar track should always be drawn.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the delay in milliseconds that a scrollbar waits before fade out.

May be an integer value, such as "`100`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the delay in milliseconds that a scrollbar takes to fade out.

May be an integer value, such as "`100`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the width of vertical scrollbars and height of horizontal scrollbars.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Controls the scrollbar style and position. The scrollbars can be overlaid or inset. When inset, they add to the padding of the view. And the scrollbars can be drawn inside the padding area or on the edge of the view. For example, if a view has a background drawable and you want to draw the scrollbars inside the padding specified by the drawable, you can use insideOverlay or insideInset. If you want them to appear at the edge of the view, ignoring the padding, then you can use outsideOverlay or outsideInset.

Must be one of the following constant values.
Constant Value Description insideInset 1000000 Inside the padding and inset. insideOverlay 0 Inside the padding and overlaid. outsideInset 3000000 Edge of the view and inset. outsideOverlay 2000000 Edge of the view and overlaid.

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the horizontal scrollbar thumb drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the vertical scrollbar thumb drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the horizontal scrollbar track drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the vertical scrollbar track drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines which scrollbars should be displayed on scrolling or not.

Must be one or more (separated by '|') of the following constant values.
Constant Value Description horizontal 100 Displays horizontal scrollbar only. none 0 No scrollbar is displayed. vertical 200 Displays vertical scrollbar only.

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Boolean that controls whether a view should have sound effects enabled for events such as clicking and touching.

May be a boolean value, such as "`true`" or "`false`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Sets the state-based animator for the View.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Supply a tag for this view containing a String, to be retrieved later with android.view.View#getTag or searched for with `https://developer.android.com/reference/kotlin/android/view/View#findViewWithTag(kotlin.Any)`. It is generally preferable to use IDs (through the android:id attribute) instead of tags because they are faster and allow for compile-time type checking.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the alignment of the text.

May be an integer value, such as "`100`".

Must be one of the following constant values.
Constant Value Description center 4 Center the paragraph, for example: ALIGN_CENTER. gravity 1 Default for the root view. The gravity determines the alignment, ALIGN_NORMAL, ALIGN_CENTER, or ALIGN_OPPOSITE, which are relative to each paragraph's text direction. inherit 0 Default. textEnd 3 Align to the end of the paragraph, for example: ALIGN_OPPOSITE. textStart 2 Align to the start of the paragraph, for example: ALIGN_NORMAL. viewEnd 6 Align to the end of the view, which is ALIGN_RIGHT if the view's resolved layoutDirection is LTR, and ALIGN_LEFT otherwise. viewStart 5 Align to the start of the view, which is ALIGN_LEFT if the view's resolved layoutDirection is LTR, and ALIGN_RIGHT otherwise.

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Defines the direction of the text.

May be an integer value, such as "`100`".

Must be one of the following constant values.
Constant Value Description anyRtl 2 The paragraph direction is RTL if it contains any strong RTL character, otherwise it is LTR if it contains any strong LTR characters. If there are neither, the paragraph direction is the view's resolved layout direction. firstStrong 1 Default for the root view. The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is the view's resolved layout direction. firstStrongLtr 6 The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is LTR. firstStrongRtl 7 The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is RTL. inherit 0 Default. locale 5 The paragraph direction is coming from the system Locale. ltr 3 The paragraph direction is left to right. rtl 4 The paragraph direction is right to left.

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Specifies a theme override for a view. When a theme override is set, the view will be inflated using a `https://developer.android.com/reference/kotlin/android/content/Context.html#` themed with the specified resource. During XML inflation, any child views under the view with a theme override will inherit the themed context.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` x location of the pivot point around which the view will rotate and scale. This xml attribute sets the pivotX property of the View.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` y location of the pivot point around which the view will rotate and scale. This xml attribute sets the pivotY property of the View.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Names a View such that it can be identified for Transitions. Names should be unique in the View hierarchy.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` translation in x of the view. This value is added post-layout to the left property of the view, which is set by its layout.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` translation in y of the view. This value is added post-layout to the top property of the view, which is set by its layout.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` translation in z of the view. This value is added to its elevation.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/view/View#attr_View` Controls the initial visibility of the view.

Must be one of the following constant values.
Constant Value Description gone 2 Completely hidden, as if the view had not been added. invisible 1 Not displayed, but taken into account during layout (space is left for it). visible 0 Visible on screen; the default value.

<br />

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#CLIP_TO_PADDING_MASK:kotlin.Int` We clip to padding when FLAG_CLIP_TO_PADDING and FLAG_PADDING_NOT_NULL are set at the same time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_AFTER_DESCENDANTS:kotlin.Int` This view will get focus only if none of its descendants want it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_BEFORE_DESCENDANTS:kotlin.Int` This view will get focus before any of its descendants. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_BLOCK_DESCENDANTS:kotlin.Int` This view will block any of its descendants from getting focus, even if they are focusable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#LAYOUT_MODE_CLIP_BOUNDS:kotlin.Int` This constant is a `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setLayoutMode(kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#LAYOUT_MODE_OPTICAL_BOUNDS:kotlin.Int` This constant is a `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setLayoutMode(kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#PERSISTENT_ALL_CACHES:kotlin.Int` Used to indicate that all drawing caches should be kept in memory. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#PERSISTENT_ANIMATION_CACHE:kotlin.Int` Used to indicate that the animation drawing cache should be kept in memory. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#PERSISTENT_NO_CACHE:kotlin.Int` Used to indicate that no drawing cache should be kept in memory. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#PERSISTENT_SCROLLING_CACHE:kotlin.Int` Used to indicate that the scrolling drawing cache should be kept in memory. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/view/View` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_AUTO:kotlin.Int`

Automatically determine whether the view should only allow interactions from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s with the `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#isAccessibilityTool()` property set to true.

Accessibility interactions from services without `isAccessibilityTool` set to true are disallowed for any of the following conditions:
- this view sets `https://developer.android.com/reference/kotlin/android/view/View#getFilterTouchesWhenObscured()`.
- any parent of this view returns true from `https://developer.android.com/reference/kotlin/android/view/View#isAccessibilityDataSensitive()`.

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_NO:kotlin.Int`

Allow interactions from all `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s, regardless of their `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#isAccessibilityTool()` property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_YES:kotlin.Int`

Only allow interactions from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s with the `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#isAccessibilityTool()` property set to true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_ASSERTIVE:kotlin.Int`

Live region mode specifying that accessibility services should immediately notify users of changes to this view. For example, a screen reader may interrupt ongoing speech to immediately announce these changes.

Use with `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityLiveRegion(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_NONE:kotlin.Int`

Live region mode specifying that accessibility services should not automatically announce changes to this view. This is the default live region mode for most views.

Use with `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityLiveRegion(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_POLITE:kotlin.Int`

Live region mode specifying that accessibility services should notify users of changes to this view.

Use with `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityLiveRegion(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int`

Flag requesting you to add views that are marked as not important for autofill (see `https://developer.android.com/reference/kotlin/android/view/View#setImportantForAutofill(kotlin.Int)`) to a `https://developer.android.com/reference/kotlin/android/view/ViewStructure`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE:kotlin.String`

Hint indicating that this view can be autofilled with a credit card expiration date.

It should be used when the credit card expiration date is represented by just one view; if it is represented by more than one (for example, one view for the month and another view for the year), then each of these views should use the hint specific for the unit (`https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH:kotlin.String`, or `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR:kotlin.String`).

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE}`).

When annotating a view with this hint, it's recommended to use a date autofill value to avoid ambiguity when the autofill service provides a value for it. To understand why a value can be ambiguous, consider "April of 2020", which could be represented as either of the following options:

- `"04/2020"`
- `"4/2020"`
- `"2020/04"`
- `"2020/4"`
- `"April/2020"`
- `"Apr/2020"`

You define a date autofill value for the view by overriding the following methods:

1. `https://developer.android.com/reference/kotlin/android/view/View#getAutofillType()` to return `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_DATE:kotlin.Int`.
2. `https://developer.android.com/reference/kotlin/android/view/View#getAutofillValue()` to return a `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#forDate(kotlin.Long)`.
3. `https://developer.android.com/reference/kotlin/android/view/View#autofill(android.view.autofill.AutofillValue)` to expect a data autofillvalue.

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY:kotlin.String`

Hint indicating that this view can be autofilled with a credit card expiration day.

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY}`).

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH:kotlin.String`

Hint indicating that this view can be autofilled with a credit card expiration month.

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH}`).

When annotating a view with this hint, it's recommended to use a text autofill value whose value is the numerical representation of the month, starting on `1` to avoid ambiguity when the autofill service provides a value for it. To understand why a value can be ambiguous, consider "January", which could be represented as either of

- `"1"`: recommended way.
- `"0"`: if following the `https://developer.android.com/reference/kotlin/java/util/Calendar.html#MONTH:kotlin.Int` convention.
- `"January"`: full name, in English.
- `"jan"`: abbreviated name, in English.
- `"Janeiro"`: full name, in another language.

Another recommended approach is to use a date autofill value - see `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE:kotlin.String` for more details.

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR:kotlin.String`

Hint indicating that this view can be autofilled with a credit card expiration year.

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR}`).

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_NUMBER:kotlin.String`

Hint indicating that this view can be autofilled with a credit card number.

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_NUMBER}`).

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE:kotlin.String`

Hint indicating that this view can be autofilled with a credit card security code.

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE}`).

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_EMAIL_ADDRESS:kotlin.String`

Hint indicating that this view can be autofilled with an email address.

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_EMAIL_ADDRESS}`).

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_NAME:kotlin.String`

Hint indicating that this view can be autofilled with a user's real name.

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_NAME}`).

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_PASSWORD:kotlin.String`

Hint indicating that this view can be autofilled with a password.

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_PASSWORD}`).

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_PHONE:kotlin.String`

Hint indicating that this view can be autofilled with a phone number.

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_PHONE}`).

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_POSTAL_ADDRESS:kotlin.String`

Hint indicating that this view can be autofilled with a postal address.

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_POSTAL_ADDRESS}`).

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_POSTAL_CODE:kotlin.String`

Hint indicating that this view can be autofilled with a postal code.

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_POSTAL_CODE}`).

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_USERNAME:kotlin.String`

Hint indicating that this view can be autofilled with a username.

Can be used with either `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` or [`android:autofillHint`](https://developer.android.com/reference/kotlin/android/view/View#attr_android:autofillHint) (in which case the value should be `{@value #AUTOFILL_HINT_USERNAME}`).

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_DATE:kotlin.Int`

Autofill type for a field that contains a date, which is represented by a long representing the number of milliseconds since the standard base time known as "the epoch", namely January 1, 1970, 00:00:00 GMT (see `https://developer.android.com/reference/kotlin/java/util/Date.html#getTime()`.

`https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue` instances for autofilling a `https://developer.android.com/reference/kotlin/android/view/View` can be obtained through `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#forDate(kotlin.Long)`, and the values passed to autofill a `https://developer.android.com/reference/kotlin/android/view/View` can be fetched through `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#getDateValue()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_LIST:kotlin.Int`

Autofill type for a selection list field, which is filled by an `int` representing the element index inside the list (starting at `0`).

`https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue` instances for autofilling a `https://developer.android.com/reference/kotlin/android/view/View` can be obtained through `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#forList(kotlin.Int)`, and the value passed to autofill a `https://developer.android.com/reference/kotlin/android/view/View` can be fetched through `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#getListValue()`.

The available options in the selection list are typically provided by `https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.ViewNode.html#getAutofillOptions()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_NONE:kotlin.Int`

Autofill type for views that cannot be autofilled.

Typically used when the view is read-only; for example, a text label.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_TEXT:kotlin.Int`

Autofill type for a text field, which is filled by a `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#`.

`https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue` instances for autofilling a `https://developer.android.com/reference/kotlin/android/view/View` can be obtained through `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#forText(kotlin.CharSequence)`, and the value passed to autofill a `https://developer.android.com/reference/kotlin/android/view/View` can be fetched through `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#getTextValue()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_TOGGLE:kotlin.Int`

Autofill type for a togglable field, which is filled by a `boolean`.

`https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue` instances for autofilling a `https://developer.android.com/reference/kotlin/android/view/View` can be obtained through `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#forToggle(kotlin.Boolean)`, and the value passed to autofill a `https://developer.android.com/reference/kotlin/android/view/View` can be fetched through `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#getToggleValue()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_AUTO:kotlin.Int`

Content sensitivity is determined by the framework. The framework uses a heuristic to determine if this view displays sensitive content. Autofill hints i.e. `https://developer.android.com/reference/kotlin/android/view/View#getAutofillHints()` are used in the heuristic to determine if this view should be considered as a sensitive view.

`https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_USERNAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_PASSWORD:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_NUMBER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR:kotlin.String` are considered sensitive hints by the framework, and the list may include more hints in the future.

The window hosting a sensitive view will be marked as secure during an active media projection session. This would be equivalent to applying `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_SECURE:kotlin.Int` to the window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_NOT_SENSITIVE:kotlin.Int`

The view doesn't display sensitive content.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#CONTENT_SENSITIVITY_SENSITIVE:kotlin.Int`

The view displays sensitive content.

The window hosting a sensitive view will be marked as secure during an active media projection session. This would be equivalent to applying `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_SECURE:kotlin.Int` to the window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_ACCESSIBILITY_ACTION:kotlin.Int`

Flag indicating that the drag was initiated with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_DRAG_START:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`. When `https://developer.android.com/reference/kotlin/android/view/View#startDragAndDrop(android.content.ClipData,%20android.view.View.DragShadowBuilder,%20kotlin.Any,%20kotlin.Int)` is called, this is used by the system to perform a drag without animations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL:kotlin.Int`

Flag indicating that a drag can cross window boundaries. When `https://developer.android.com/reference/kotlin/android/view/View#startDragAndDrop(android.content.ClipData,%20android.view.View.DragShadowBuilder,%20kotlin.Any,%20kotlin.Int)` is called with this flag set, all visible applications with targetSdkVersion \>= `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` will be able to participate in the drag operation and receive the dragged content.

Global drags require a valid non-null `https://developer.android.com/reference/kotlin/android/content/ClipData.html#`.

If this is the only flag set, then the drag recipient will only have access to text data and intents contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object. Access to URIs contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` is determined by other DRAG_FLAG_GLOBAL_\* flags

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_PERSISTABLE_URI_PERMISSION:kotlin.Int`

When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_READ:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_WRITE:kotlin.Int`, the URI permission grant can be persisted across device reboots until explicitly revoked with `https://developer.android.com/reference/kotlin/android/content/Context.html#revokeUriPermission(android.net.Uri,%20kotlin.Int)` Context.revokeUriPermission}.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_PREFIX_URI_PERMISSION:kotlin.Int`

When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_READ:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_WRITE:kotlin.Int`, the URI permission grant applies to any URI that is a prefix match against the original granted URI.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_SAME_APPLICATION:kotlin.Int`

Flag indicating that a drag can cross window boundaries (within the same application). When `https://developer.android.com/reference/kotlin/android/view/View#startDragAndDrop(android.content.ClipData,%20android.view.View.DragShadowBuilder,%20kotlin.Any,%20kotlin.Int)` is called with this flag set, only visible windows belonging to the same application (ie. share the same UID) with targetSdkVersion \>= `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` will be able to participate in the drag operation and receive the dragged content. If both DRAG_FLAG_GLOBAL_SAME_APPLICATION and DRAG_FLAG_GLOBAL are set, then DRAG_FLAG_GLOBAL_SAME_APPLICATION takes precedence and the drag will only go to visible windows from the same application.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_READ:kotlin.Int`

When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL:kotlin.Int`, the drag recipient will be able to request read access to the content URI(s) contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL_URI_WRITE:kotlin.Int`

When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_GLOBAL:kotlin.Int`, the drag recipient will be able to request write access to the content URI(s) contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_HIDE_CALLING_TASK_ON_DRAG_START:kotlin.Int`

Flag indicating that this drag will result in the caller activity's task to be hidden for the duration of the drag, which means that the source activity will not receive drag events for the current drag gesture. Only the current `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService.html#` may use this flag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_OPAQUE:kotlin.Int`

Flag indicating that the drag shadow will be opaque. When `https://developer.android.com/reference/kotlin/android/view/View#startDragAndDrop(android.content.ClipData,%20android.view.View.DragShadowBuilder,%20kotlin.Any,%20kotlin.Int)` is called with this flag set, the drag shadow will be opaque, otherwise, it will be semitransparent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAG_FLAG_START_INTENT_SENDER_ON_UNHANDLED_DRAG:kotlin.Int`

Flag indicating that an unhandled drag should be delegated to the system to be started if no visible window wishes to handle the drop. When using this flag, the caller must provide ClipData with an Item that contains an immutable IntentSender to an activity to be launched (not a broadcast, service, etc). See `https://developer.android.com/reference/kotlin/android/content/ClipData.Item.Builder.html#setIntentSender(android.content.IntentSender)`. The system can decide to launch the intent or not based on factors like the current screen size or windowing mode. If the system does not launch the intent, it will be canceled via the normal drag and drop flow.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_AUTO:kotlin.Int`

Enables automatic quality mode for the drawing cache.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_HIGH:kotlin.Int`

Enables high quality mode for the drawing cache.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#DRAWING_CACHE_QUALITY_LOW:kotlin.Int`

Enables low quality mode for the drawing cache.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_CONTENT_DESCRIPTION:kotlin.Int`

Find find views that contain the specified content description.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_TEXT:kotlin.Int`

Find views that render the specified text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE:kotlin.Int`

This view wants keystrokes.

Use with `https://developer.android.com/reference/kotlin/android/view/View#setFocusable(kotlin.Int)` and [`android:focusable`.](https://developer.android.com/reference/kotlin/android/view/View#attr_android:focusable)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLES_ALL:kotlin.Int`

View flag indicating whether `https://developer.android.com/reference/kotlin/android/view/View#addFocusables(java.util.ArrayList,%20kotlin.Int,%20kotlin.Int)` should add all focusable Views regardless if they are focusable in touch mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLES_TOUCH_MODE:kotlin.Int`

View flag indicating whether `https://developer.android.com/reference/kotlin/android/view/View#addFocusables(java.util.ArrayList,%20kotlin.Int,%20kotlin.Int)` should add only Views focusable in touch mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE_AUTO:kotlin.Int`

This view determines focusability automatically. This is the default.

Use with `https://developer.android.com/reference/kotlin/android/view/View#setFocusable(kotlin.Int)` and [`android:focusable`.](https://developer.android.com/reference/kotlin/android/view/View#attr_android:focusable)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/view/View#focusSearch(kotlin.Int)`. Move focus to the previous selectable item.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/view/View#focusSearch(kotlin.Int)`. Move focus down.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/view/View#focusSearch(kotlin.Int)`. Move focus to the next selectable item.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/view/View#focusSearch(kotlin.Int)`. Move focus to the left.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/view/View#focusSearch(kotlin.Int)`. Move focus to the right.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/view/View#focusSearch(kotlin.Int)`. Move focus up.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`

This view is invisible, and it doesn't take any space for layout purposes. Use with `https://developer.android.com/reference/kotlin/android/view/View#setVisibility(kotlin.Int)` and [`android:visibility`.](https://developer.android.com/reference/kotlin/android/view/View#attr_android:visibility)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#HAPTIC_FEEDBACK_ENABLED:kotlin.Int`

View flag indicating whether this view should have haptic feedback enabled for events such as long presses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_AUTO:kotlin.Int`

Automatically determine whether a view is important for accessibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO:kotlin.Int`

The view is not important for accessibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int`

The view is not important for accessibility, nor are any of its descendant views.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_YES:kotlin.Int`

The view is important for accessibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int`

Automatically determine whether a view is important for autofill.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int`

The view is not important for autofill, but its children (if any) will be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int`

The view is not important for autofill, and its children (if any) will not be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int`

The view is important for autofill, and its children (if any) will be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`

The view is important for autofill, but its children (if any) will not be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_AUTO:kotlin.Int`

Automatically determine whether a view is important for content capture.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO:kotlin.Int`

The view is not important for content capture, but its children (if any) will be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO_EXCLUDE_DESCENDANTS:kotlin.Int`

The view is not important for content capture, and its children (if any) will not be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES:kotlin.Int`

The view is important for content capture, and its children (if any) will be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES_EXCLUDE_DESCENDANTS:kotlin.Int`

The view is important for content capture, but its children (if any) will not be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`

This view is invisible, but it still takes up space for layout purposes. Use with `https://developer.android.com/reference/kotlin/android/view/View#setVisibility(kotlin.Int)` and [`android:visibility`.](https://developer.android.com/reference/kotlin/android/view/View#attr_android:visibility)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#KEEP_SCREEN_ON:kotlin.Int`

View flag indicating that the screen should remain on while the window containing this view is visible to the user. This effectively takes care of automatically setting the WindowManager's `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_KEEP_SCREEN_ON:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int`

Indicates that the view has a hardware layer. A hardware layer is backed by a hardware specific texture (generally Frame Buffer Objects or FBO on OpenGL hardware) and causes the view to be rendered using Android's hardware rendering pipeline, but only if hardware acceleration is turned on for the view hierarchy. When hardware acceleration is turned off, hardware layers behave exactly as `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int`.

A hardware layer is useful to apply a specific color filter and/or blending mode and/or translucency to a view and all its children.

A hardware layer can be used to cache a complex view tree into a texture and reduce the complexity of drawing operations. For instance, when animating a complex view tree with a translation, a hardware layer can be used to render the view tree only once.

A hardware layer can also be used to increase the rendering quality when rotation transformations are applied on a view. It can also be used to prevent potential clipping issues when applying 3D transforms on a view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`

Indicates that the view does not have a layer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int`

Indicates that the view has a software layer. A software layer is backed by a bitmap and causes the view to be rendered using Android's software rendering pipeline, even if hardware acceleration is enabled.

Software layers have various usages:

When the application is not using hardware acceleration, a software layer is useful to apply a specific color filter and/or blending mode and/or translucency to a view and all its children.

When the application is using hardware acceleration, a software layer is useful to render drawing primitives not supported by the hardware accelerated pipeline. It can also be used to cache a complex view tree into a texture and reduce the complexity of drawing operations. For instance, when animating a complex view tree with a translation, a software layer can be used to render the view tree only once.

Software layers should be avoided when the affected view tree updates often. Every update will require to re-render the software layer, which can potentially be slow (particularly when hardware acceleration is turned on since the layer will have to be uploaded into a hardware texture after every update.)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_INHERIT:kotlin.Int`

Horizontal layout direction of this view is inherited from its parent. Use with `https://developer.android.com/reference/kotlin/android/view/View#setLayoutDirection(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LOCALE:kotlin.Int`

Horizontal layout direction of this view is from deduced from the default language script for the locale. Use with `https://developer.android.com/reference/kotlin/android/view/View#setLayoutDirection(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LTR:kotlin.Int`

Horizontal layout direction of this view is from Left to Right. Use with `https://developer.android.com/reference/kotlin/android/view/View#setLayoutDirection(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_RTL:kotlin.Int`

Horizontal layout direction of this view is from Right to Left. Use with `https://developer.android.com/reference/kotlin/android/view/View#setLayoutDirection(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_HEIGHT_STATE_SHIFT:kotlin.Int`

Bit shift of `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_MASK:kotlin.Int` to get to the height bits for functions that combine both width and height into a single int, such as `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredState()` and the childState argument of `https://developer.android.com/reference/kotlin/android/view/View#resolveSizeAndState(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int`

Bits of `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredWidthAndState()` and `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredWidthAndState()` that provide the actual measured size.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_MASK:kotlin.Int`

Bits of `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredWidthAndState()` and `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredWidthAndState()` that provide the additional state bits.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_TOO_SMALL:kotlin.Int`

Bit of `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredWidthAndState()` and `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredWidthAndState()` that indicates the measured size is smaller that the space the view would like to have.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#NOT_FOCUSABLE:kotlin.Int`

This view does not want keystrokes.

Use with `https://developer.android.com/reference/kotlin/android/view/View#setFocusable(kotlin.Int)` and [`android:focusable`.](https://developer.android.com/reference/kotlin/android/view/View#attr_android:focusable)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#NO_ID:kotlin.Int`

Used to mark a View that has no ID.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_ALWAYS:kotlin.Int`

Always allow a user to over-scroll this view, provided it is a view that can scroll.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_IF_CONTENT_SCROLLS:kotlin.Int`

Allow a user to over-scroll this view only if the content is large enough to meaningfully scroll, provided it is a view that can scroll.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_NEVER:kotlin.Int`

Never allow a user to over-scroll this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_ABSOLUTE:kotlin.Int`

A pointer capture mode in which touchpads report absolute finger locations.

In this capture mode, no attempt is made to recognize gestures from touchpad input. Instead, the absolute location of each touch on the pad is reported directly to the View, in the same way that other touches on devices with `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_POINTER:kotlin.Int` are reported.

Events will be delivered with the source `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_TOUCHPAD:kotlin.Int`. The absolute position of each touch will be available through `https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY(kotlin.Int)`, and their relative movements through `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RELATIVE_X:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RELATIVE_Y:kotlin.Int`. If the touchpad supports them, touch dimension information may be available through the `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_PRESSURE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MAJOR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MINOR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MAJOR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MINOR:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_ORIENTATION:kotlin.Int` axes.

Events from mice are always reported in the same way regardless of capture mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_RELATIVE:kotlin.Int`

A pointer capture mode in which touchpad gestures are recognized and reported like mouse movements.

In this capture mode, the following gestures made on a captured touchpad will be recognized and reported:

- Pointer movement gestures (such as moving a single finger on the pad) will be reported like mouse movements, with the `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_MOVE:kotlin.Int` action and their relative position changes available through android.view.MotionEvent#getX and android.view.MotionEvent#getY.
- Scrolling gestures (such as two-finger swipes) will be reported like scroll wheel movements on a mouse, with the `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_SCROLL:kotlin.Int` action and the scroll amounts available through the `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_VSCROLL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_HSCROLL:kotlin.Int` axes.

Motion values are proportional to the physical motion of the gesturing finger(s), and the physical movement in mm can be found using the resolution reported by `https://developer.android.com/reference/kotlin/android/view/InputDevice.MotionRange#getResolution()` for the relevant axis.

These events will be reported with `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_MOUSE_RELATIVE:kotlin.Int`.

Events from mice are always reported in the same way regardless of capture mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_UNCAPTURED:kotlin.Int`

A "pointer capture mode" in which the pointer is not captured.

Passing this to `https://developer.android.com/reference/kotlin/android/view/View#requestPointerCapture(kotlin.Int)` is equivalent to calling `https://developer.android.com/reference/kotlin/android/view/View#releasePointerCapture()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS:kotlin.Int`

Represents that the user interaction that is requesting a rectangle on screen is doing so because the View has input/keyboard focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY:kotlin.Int`

Represents that the user interaction that is requesting a rectangle on screen is doing so only to scroll the View on screen, and the rectangle is not associated with a text cursor or keyboard focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR:kotlin.Int`

Represents that the user interaction that is requesting a rectangle on screen is doing so because the View contains a text cursor (caret).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED:kotlin.Int`

Represents that the user interaction that is requesting a rectangle on screen is doing so via the original `https://developer.android.com/reference/kotlin/android/view/View#requestRectangleOnScreen(android.graphics.Rect)` or `https://developer.android.com/reference/kotlin/android/view/View#requestRectangleOnScreen(android.graphics.Rect,%20kotlin.Boolean)` APIs that do not define the source. RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED should be reserved for backward compatibility and should only be provided from calls to the original API.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#REQUESTED_FRAME_RATE_CATEGORY_DEFAULT:kotlin.Float`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#REQUESTED_FRAME_RATE_CATEGORY_HIGH:kotlin.Float`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#REQUESTED_FRAME_RATE_CATEGORY_LOW:kotlin.Float`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#REQUESTED_FRAME_RATE_CATEGORY_NORMAL:kotlin.Float`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE:kotlin.Float`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCREEN_STATE_OFF:kotlin.Int`

Indicates that the screen has changed state and is now off.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCREEN_STATE_ON:kotlin.Int`

Indicates that the screen has changed state and is now on.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_INSIDE_INSET:kotlin.Int`

The scrollbar style to display the scrollbars inside the padded area, increasing the padding of the view. The scrollbars will not overlap the content area of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_INSIDE_OVERLAY:kotlin.Int`

The scrollbar style to display the scrollbars inside the content area, without increasing the padding. The scrollbars will be overlaid with translucency on the view's content.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_OUTSIDE_INSET:kotlin.Int`

The scrollbar style to display the scrollbars at the edge of the view, increasing the padding of the view. The scrollbars will only overlap the background, if any.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBARS_OUTSIDE_OVERLAY:kotlin.Int`

The scrollbar style to display the scrollbars at the edge of the view, without increasing the padding. The scrollbars will be overlaid with translucency.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBAR_POSITION_DEFAULT:kotlin.Int`

Position the scroll bar at the default position as determined by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBAR_POSITION_LEFT:kotlin.Int`

Position the scroll bar along the left edge.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBAR_POSITION_RIGHT:kotlin.Int`

Position the scroll bar along the right edge.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_HORIZONTAL:kotlin.Int`

Indicates scrolling along the horizontal axis.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_NONE:kotlin.Int`

Indicates no axis of view scrolling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_VERTICAL:kotlin.Int`

Indicates scrolling along the vertical axis.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_AUTO:kotlin.Int`

The content of this view will be considered for scroll capture if scrolling is possible.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE:kotlin.Int`

Explicitly exclude this view as a potential scroll capture target. The system will not consider it. Mutually exclusive with `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int`, which this flag takes precedence over.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE_DESCENDANTS:kotlin.Int`

Explicitly exclude all children of this view as potential scroll capture targets. This view is unaffected. Note: Excluded children are not considered, regardless of `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int`

Explicitly include this view as a potential scroll capture target. When locating a scroll capture target, this view will be prioritized before others without this flag. Mutually exclusive with `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE:kotlin.Int`, which takes precedence.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_BOTTOM:kotlin.Int`

Scroll indicator direction for the bottom edge of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_END:kotlin.Int`

Scroll indicator direction for the ending edge of the view.

Resolved according to the view's layout direction, see `https://developer.android.com/reference/kotlin/android/view/View#getLayoutDirection()` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_LEFT:kotlin.Int`

Scroll indicator direction for the left edge of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_RIGHT:kotlin.Int`

Scroll indicator direction for the right edge of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_START:kotlin.Int`

Scroll indicator direction for the starting edge of the view.

Resolved according to the view's layout direction, see `https://developer.android.com/reference/kotlin/android/view/View#getLayoutDirection()` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_INDICATOR_TOP:kotlin.Int`

Scroll indicator direction for the top edge of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SOUND_EFFECTS_ENABLED:kotlin.Int`

View flag indicating whether this view should have sound effects enabled for events such as clicking and touching.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#STATUS_BAR_HIDDEN:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#STATUS_BAR_VISIBLE:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)`: View has requested to go into the normal fullscreen mode so that its content can take over the screen while still allowing the user to interact with the application.

This has the same visual effect as `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_FULLSCREEN:kotlin.Int`, meaning that non-critical screen decorations (such as the status bar) will be hidden while the user is in the View's window, focusing the experience on that content. Unlike the window flag, if you are using ActionBar in overlay mode with `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int`, then enabling this flag will also hide the action bar.

This approach to going fullscreen is best used over the window flag when it is a transient state -- that is, the application does this at certain points in its user interaction where it wants to allow the user to focus on content, but not as a continuous state. For situations where the application would like to simply stay full screen the entire time (such as a game that wants to take over the screen), the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_FULLSCREEN:kotlin.Int` is usually a better approach. The state set here will be removed by the system in various situations (such as the user moving to another application) like the other system UI states.

When using this flag, the application should provide some easy facility for the user to go out of it. A common example would be in an e-book reader, where tapping on the screen brings back whatever screen and UI decorations that had been hidden while the user was immersed in reading the book.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)`: View has requested that the system navigation be temporarily hidden.

This is an even less obtrusive state than that called for by `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LOW_PROFILE:kotlin.Int`; on devices that draw essential navigation controls (Home, Back, and the like) on screen, `SYSTEM_UI_FLAG_HIDE_NAVIGATION` will cause those to disappear. This is useful (in conjunction with the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_FULLSCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_LAYOUT_IN_SCREEN:kotlin.Int` window flags) for displaying content using every last pixel on the display.

There is a limitation: because navigation controls are so important, the least user interaction will cause them to reappear immediately. When this happens, both this flag and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` will be cleared automatically, so that both elements reappear at the same time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_IMMERSIVE:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)`: View would like to remain interactive when hiding the navigation bar with `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`. If this flag is not set, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int` will be force cleared by the system on any user interaction.

Since this flag is a modifier for `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`, it only has an effect when used in combination with that flag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_IMMERSIVE_STICKY:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)`: View would like to remain interactive when hiding the status bar with `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` and/or hiding the navigation bar with `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`. Use this flag to create an immersive experience while also hiding the system bars. If this flag is not set, `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int` will be force cleared by the system on any user interaction, and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` will be force-cleared by the system if the user swipes from the top of the screen.

When system bars are hidden in immersive mode, they can be revealed temporarily with system gestures, such as swiping from the top of the screen. These transient system bars will overlay app's content, may have some degree of transparency, and will automatically hide after a short timeout.

Since this flag is a modifier for `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`, it only has an effect when used in combination with one or both of those flags.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)`: View would like its window to be laid out as if it has requested `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`, even if it currently hasn't. This allows it to avoid artifacts when switching in and out of that mode, at the expense that some of its user interface may be covered by screen decorations when they are shown. You can perform layout of your inner UI elements to account for non-fullscreen system UI through the `https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect)` method.

Note: on displays that have a `https://developer.android.com/reference/kotlin/android/view/DisplayCutout`, the window may still be placed differently than if `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` was set, if the window's `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#layoutInDisplayCutoutMode:kotlin.Int` is `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#LAYOUT_IN_DISPLAY_CUTOUT_MODE_DEFAULT:kotlin.Int`. To avoid this, use either of the other modes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)`: View would like its window to be laid out as if it has requested `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`, even if it currently hasn't. This allows it to avoid artifacts when switching in and out of that mode, at the expense that some of its user interface may be covered by screen decorations when they are shown. You can perform layout of your inner UI elements to account for the navigation system UI through the `https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect)` method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_STABLE:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)`: When using other layout flags, we would like a stable view of the content insets given to `https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect)`. This means that the insets seen there will always represent the worst case that the application can expect as a continuous state. In the stock Android UI this is the space for the system bar, nav bar, and status bar, but not more transient elements such as an input method. The stable layout your UI sees is based on the system UI modes you can switch to. That is, if you specify `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int` then you will get a stable layout for changes of the `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` mode; if you specify `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int`, then you can transition to `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int` with a stable layout. (Note that you should avoid using `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int` by itself.) If you have set the window flag `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_FULLSCREEN:kotlin.Int` to hide the status bar (instead of using `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`), then a hidden status bar will be considered a "stable" state for purposes here. This allows your UI to continually hide the status bar, while still using the system UI flags to hide the action bar while still retaining a stable layout. Note that changing the window fullscreen flag will never provide a stable layout for a clean transition.

If you are using ActionBar in overlay mode with `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int`, this flag will also impact the insets it adds to those given to the application.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LIGHT_NAVIGATION_BAR:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)`: Requests the navigation bar to draw in a mode that is compatible with light navigation bar backgrounds.

For this to take effect, the window must request `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS:kotlin.Int` but not `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_TRANSLUCENT_NAVIGATION:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LIGHT_STATUS_BAR:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)`: Requests the status bar to draw in a mode that is compatible with light status bar backgrounds.

For this to take effect, the window must request `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS:kotlin.Int` but not `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_TRANSLUCENT_STATUS:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LOW_PROFILE:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)`: View has requested the system UI to enter an unobtrusive "low profile" mode.

This is for use in games, book readers, video players, or any other "immersive" application where the usual system chrome is deemed too distracting.

In low profile mode, the status bar and/or navigation icons may dim.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_VISIBLE:kotlin.Int`

Special constant for `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)`: View has requested the system UI (status bar) to be visible (the default).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_LAYOUT_FLAGS:kotlin.Int`

Flags that can impact the layout in relation to system UI.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_CENTER:kotlin.Int`

Center the paragraph, e.g. ALIGN_CENTER. Use with `https://developer.android.com/reference/kotlin/android/view/View#setTextAlignment(kotlin.Int)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_GRAVITY:kotlin.Int`

Default for the root view. The gravity determines the text alignment, ALIGN_NORMAL, ALIGN_CENTER, or ALIGN_OPPOSITE, which are relative to each paragraph's text direction. Use with `https://developer.android.com/reference/kotlin/android/view/View#setTextAlignment(kotlin.Int)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_INHERIT:kotlin.Int`

Default text alignment. The text alignment of this View is inherited from its parent. Use with `https://developer.android.com/reference/kotlin/android/view/View#setTextAlignment(kotlin.Int)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_END:kotlin.Int`

Align to the end of the paragraph, e.g. ALIGN_OPPOSITE. Use with `https://developer.android.com/reference/kotlin/android/view/View#setTextAlignment(kotlin.Int)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_START:kotlin.Int`

Align to the start of the paragraph, e.g. ALIGN_NORMAL. Use with `https://developer.android.com/reference/kotlin/android/view/View#setTextAlignment(kotlin.Int)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_END:kotlin.Int`

Align to the end of the view, which is ALIGN_RIGHT if the view's resolved layoutDirection is LTR, and ALIGN_LEFT otherwise. Use with `https://developer.android.com/reference/kotlin/android/view/View#setTextAlignment(kotlin.Int)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_START:kotlin.Int`

Align to the start of the view, which is ALIGN_LEFT if the view's resolved layoutDirection is LTR, and ALIGN_RIGHT otherwise. Use with `https://developer.android.com/reference/kotlin/android/view/View#setTextAlignment(kotlin.Int)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_ANY_RTL:kotlin.Int`

Text direction is using "any-RTL" algorithm. The paragraph direction is RTL if it contains any strong RTL character, otherwise it is LTR if it contains any strong LTR characters. If there are neither, the paragraph direction is the view's resolved layout direction.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG:kotlin.Int`

Text direction is using "first strong algorithm". The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is the view's resolved layout direction.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG_LTR:kotlin.Int`

Text direction is using "first strong algorithm". The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is LTR.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG_RTL:kotlin.Int`

Text direction is using "first strong algorithm". The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is RTL.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_INHERIT:kotlin.Int`

Text direction is inherited through `https://developer.android.com/reference/kotlin/android/view/ViewGroup#`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_LOCALE:kotlin.Int`

Text direction is coming from the system Locale.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_LTR:kotlin.Int`

Text direction is forced to LTR.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_RTL:kotlin.Int`

Text direction is forced to RTL.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#VIEW_LOG_TAG:kotlin.String`

The logging tag used by this class with android.util.Log.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`

This view is visible. Use with `https://developer.android.com/reference/kotlin/android/view/View#setVisibility(kotlin.Int)` and [`android:visibility`.](https://developer.android.com/reference/kotlin/android/view/View#attr_android:visibility)

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewGroup#ViewGroup(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` <br /> |
| `https://developer.android.com/reference/kotlin/android/view/ViewGroup#ViewGroup(android.content.Context,%20android.util.AttributeSet)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!)` <br /> |
| `https://developer.android.com/reference/kotlin/android/view/ViewGroup#ViewGroup(android.content.Context,%20android.util.AttributeSet,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!, defStyleAttr: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| `https://developer.android.com/reference/kotlin/android/view/ViewGroup#ViewGroup(android.content.Context,%20android.util.AttributeSet,%20kotlin.Int,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!, defStyleAttr: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, defStyleRes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addChildrenForAccessibility(java.util.ArrayList)(outChildren: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/view/View!>!)` Adds the children of this View relevant for accessibility to the given list as output. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addExtraDataToAccessibilityNodeInfo(android.view.accessibility.AccessibilityNodeInfo,%20kotlin.String,%20android.os.Bundle)(info: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo, extraDataKey: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, arguments: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Adds extra data to an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo` based on an explicit request for the additional data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addFocusables(java.util.ArrayList,%20kotlin.Int,%20kotlin.Int)(views: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/view/View!>!, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, focusableMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adds any focusable views that are descendants of this view (possibly including this view if it is focusable itself) to views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addKeyboardNavigationClusters(kotlin.collections.MutableCollection,%20kotlin.Int)(views: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/view/View!>, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adds any keyboard navigation cluster roots that are descendants of this view (possibly including this view if it is a cluster root itself) to views. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addStatesFromChildren()()` Returns whether this ViewGroup's drawable states also include its children's drawable states. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addTouchables(java.util.ArrayList)(views: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/view/View!>!)` Add any touchable views that are descendants of this view (possibly including this view if it is touchable itself) to views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addView(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View!)` Adds a child view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)(child: https://developer.android.com/reference/kotlin/android/view/View!, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!)` Adds a child view with the specified layout parameters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addView(android.view.View,%20kotlin.Int)(child: https://developer.android.com/reference/kotlin/android/view/View!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adds a child view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addView(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams)(child: https://developer.android.com/reference/kotlin/android/view/View!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!)` Adds a child view with the specified layout parameters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addView(android.view.View,%20kotlin.Int,%20kotlin.Int)(child: https://developer.android.com/reference/kotlin/android/view/View!, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adds a child view with this ViewGroup's default layout parameters and the specified width and height. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#bringChildToFront(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View!)` Change the z order of the child so it's on top of all other children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#childDrawableStateChanged(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View)` If `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addStatesFromChildren()` is true, refreshes this group's drawable state (to include the states from its children). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#childHasTransientStateChanged(android.view.View,%20kotlin.Boolean)(child: https://developer.android.com/reference/kotlin/android/view/View, childHasTransientState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when a child view has changed whether or not it is tracking transient state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#clearChildFocus(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View!)` Called when a child of this parent is giving up focus |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#clearDisappearingChildren()()` Removes any pending animations for views that have been removed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#clearFocus()()` Called when this view wants to give up focus. |
| open [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchApplyWindowInsets(android.view.WindowInsets)(insets: https://developer.android.com/reference/kotlin/android/view/WindowInsets!)` Request to apply the given window insets to this view or another view in its subtree. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchCapturedPointerEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)` Pass a captured pointer event down to the focused view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#!)` Dispatch a notification about a resource configuration change down the view hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchCreateViewTranslationRequest(kotlin.collections.MutableMap,%20kotlin.IntArray,%20android.view.translation.TranslationCapability,%20kotlin.collections.MutableList)(viewIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html!>, supportedFormats: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, capability: https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability!, requests: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest!>)` Dispatch to collect the `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest`s for translation purpose by traversing the hierarchy when the app requests ui translation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDisplayHint(kotlin.Int)(hint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Dispatch a hint about whether this view is displayed. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDragEvent(android.view.DragEvent)(event: https://developer.android.com/reference/kotlin/android/view/DragEvent!)` Detects if this View is enabled and has a drag event listener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDrawableHotspotChanged(kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Dispatches drawable hotspot changes to child views that meet at least one of the following criteria: - Returns `false` from both `https://developer.android.com/reference/kotlin/android/view/View#isClickable()` and `https://developer.android.com/reference/kotlin/android/view/View#isLongClickable()` - Requests duplication of parent state via `https://developer.android.com/reference/kotlin/android/view/View#setDuplicateParentStateEnabled(kotlin.Boolean)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchFinishTemporaryDetach()()` Dispatch `https://developer.android.com/reference/kotlin/android/view/View#onFinishTemporaryDetach()` to this View and its direct children if this is a container View. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchKeyEvent(android.view.KeyEvent)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)` Dispatch a key event to the next view on the focus path. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchKeyEventPreIme(android.view.KeyEvent)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)` Dispatch a key event before it is processed by any input method associated with the view hierarchy. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchKeyShortcutEvent(android.view.KeyEvent)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)` Dispatches a key shortcut event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchPointerCaptureChanged(kotlin.Boolean)(hasCapture: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchProvideAutofillStructure(android.view.ViewStructure,%20kotlin.Int)(structure: https://developer.android.com/reference/kotlin/android/view/ViewStructure, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Dispatches creation of a `https://developer.android.com/reference/kotlin/android/view/ViewStructure`s for autofill purposes down the hierarchy, when an Assist structure is being created as part of an autofill request. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchProvideStructure(android.view.ViewStructure)(structure: https://developer.android.com/reference/kotlin/android/view/ViewStructure!)` Dispatch creation of `https://developer.android.com/reference/kotlin/android/view/ViewStructure` down the hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchScrollCaptureSearch(android.graphics.Rect,%20android.graphics.Point,%20java.util.function.Consumer)(localVisibleRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#, windowOffset: https://developer.android.com/reference/kotlin/android/graphics/Point.html#, targets: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget!>)` Handle the scroll capture search request by checking this view if applicable, then to each child view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchSetActivated(kotlin.Boolean)(activated: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Dispatch setActivated to all of this View's children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchSetSelected(kotlin.Boolean)(selected: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Dispatch setSelected to all of this View's children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchStartTemporaryDetach()()` Dispatch `https://developer.android.com/reference/kotlin/android/view/View#onStartTemporaryDetach()` to this View and its direct children if this is a container View. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchSystemUiVisibilityChanged(kotlin.Int)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Dispatch callbacks to `https://developer.android.com/reference/kotlin/android/view/View#setOnSystemUiVisibilityChangeListener(android.view.View.OnSystemUiVisibilityChangeListener)` down the view hierarchy. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchTouchEvent(android.view.MotionEvent)(ev: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)` Pass the touch screen motion event down to the target view, or this view if it is the target. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchTrackballEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)` Pass a trackball motion event down to the focused view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchUnhandledMove(android.view.View,%20kotlin.Int)(focused: https://developer.android.com/reference/kotlin/android/view/View!, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This method is the last chance for the focused view and its ancestors to respond to an arrow key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchWindowFocusChanged(kotlin.Boolean)(hasFocus: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when the window containing this view gains or loses window focus. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchWindowInsetsAnimationEnd(android.view.WindowInsetsAnimation)(animation: https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation)` Dispatches `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback#onEnd(android.view.WindowInsetsAnimation)` when Window Insets animation ends. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchWindowInsetsAnimationPrepare(android.view.WindowInsetsAnimation)(animation: https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation)` Dispatches `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback#onPrepare(android.view.WindowInsetsAnimation)` when Window Insets animation is being prepared. |
| open [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchWindowInsetsAnimationProgress(android.view.WindowInsets,%20kotlin.collections.MutableList)(insets: https://developer.android.com/reference/kotlin/android/view/WindowInsets, runningAnimations: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation!>)` Dispatches `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback#onProgress(android.view.WindowInsets,%20kotlin.collections.MutableList)` when Window Insets animation makes progress. |
| open [WindowInsetsAnimation.Bounds](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Bounds) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchWindowInsetsAnimationStart(android.view.WindowInsetsAnimation,%20android.view.WindowInsetsAnimation.Bounds)(animation: https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation, bounds: https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Bounds)` Dispatches `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback#onStart(android.view.WindowInsetsAnimation,%20android.view.WindowInsetsAnimation.Bounds)` when Window Insets animation is started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchWindowSystemUiVisiblityChanged(kotlin.Int)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Dispatch callbacks to `https://developer.android.com/reference/kotlin/android/view/View#onWindowSystemUiVisibilityChanged(kotlin.Int)` down the view hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchWindowVisibilityChanged(kotlin.Int)(visibility: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Dispatch a window visibility change down the view hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#endViewTransition(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View!)` This method should always be called following an earlier call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#startViewTransition(android.view.View)`. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#findFocus()()` Find the view in the hierarchy rooted at this view that currently has focus. |
| open [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#)? | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#findOnBackInvokedDispatcherForChild(android.view.View,%20android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View, requester: https://developer.android.com/reference/kotlin/android/view/View)` Walk up the View hierarchy to find the nearest `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#findViewsWithText(java.util.ArrayList,%20kotlin.CharSequence,%20kotlin.Int)(outViews: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/view/View!>!, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Finds the Views that contain given text. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#focusSearch(android.view.View,%20kotlin.Int)(focused: https://developer.android.com/reference/kotlin/android/view/View!, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Find the nearest view in the specified direction that wants to take focus. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#focusableViewAvailable(android.view.View)(v: https://developer.android.com/reference/kotlin/android/view/View!)` Tells the parent that a new focusable view has become available. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#gatherTransparentRegion(android.graphics.Region)(region: https://developer.android.com/reference/kotlin/android/graphics/Region.html#?)` This is used by the ViewRoot to perform an optimization when the view hierarchy contains one or several SurfaceView. |
| open [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#generateLayoutParams(android.util.AttributeSet)(attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!)` Returns a new set of layout parameters based on the supplied attributes set. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getAccessibilityClassName()()` Return the class name of this object to be used for accessibility purposes. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the view at the specified position in the group. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildCount()()` Returns the number of children in the group. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildDrawingOrder(kotlin.Int)(drawingPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Converts drawing order position to container position. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildMeasureSpec(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(spec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, padding: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, childDimension: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Does the hard part of measureChildren: figuring out the MeasureSpec to pass to a particular child. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildVisibleRect(android.view.View,%20android.graphics.Rect,%20android.graphics.Point)(child: https://developer.android.com/reference/kotlin/android/view/View!, r: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!, offset: https://developer.android.com/reference/kotlin/android/graphics/Point.html#!)` Compute the visible part of a rectangular region defined in terms of a child view's coordinates. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getClipChildren()()` Returns whether this group's children are clipped to their bounds before drawing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getClipToPadding()()` Returns whether this ViewGroup will clip its children to its padding, and resize (but not clip) any EdgeEffect to the padded region, if padding is present. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getDescendantFocusability()()` Gets the descendant focusability of this view group. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getFocusedChild()()` Returns the focused child of this view, if any. |
| open [LayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getLayoutAnimation()()` Returns the layout animation controller used to animate the group's children. |
| open [Animation.AnimationListener](https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getLayoutAnimationListener()()` Returns the animation listener to which layout animation events are sent. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getLayoutMode()()` Returns the basis of alignment during layout operations on this ViewGroup: either `https://developer.android.com/reference/kotlin/android/view/ViewGroup#LAYOUT_MODE_CLIP_BOUNDS:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/ViewGroup#LAYOUT_MODE_OPTICAL_BOUNDS:kotlin.Int`. |
| open [LayoutTransition](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.html#)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getLayoutTransition()()` Gets the LayoutTransition object for this ViewGroup. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getNestedScrollAxes()()` Return the current axes of nested scrolling for this ViewGroup. |
| open [ViewGroupOverlay](https://developer.android.com/reference/kotlin/android/view/ViewGroupOverlay)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getOverlay()()` Returns the ViewGroupOverlay for this view group, creating it if it does not yet exist. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getPersistentDrawingCache()()` Returns an integer indicating what types of drawing caches are kept in memory. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getTouchscreenBlocksFocus()()` Check whether this ViewGroup should ignore focus requests for itself and its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#hasFocus()()` Returns true if this view has or contains focus |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#hasTransientState()()` Indicates whether the view is currently tracking transient state that the app should not need to concern itself with saving and restoring, but that the framework should take special note to preserve when possible. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#indexOfChild(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View!)` Returns the position in the group of the specified child view. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#invalidateChild(android.view.View,%20android.graphics.Rect)(child: https://developer.android.com/reference/kotlin/android/view/View!, dirty: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Don't call or override this method. |
| open [ViewParent](https://developer.android.com/reference/kotlin/android/view/ViewParent)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#invalidateChildInParent(kotlin.IntArray,%20android.graphics.Rect)(location: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!, dirty: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Don't call or override this method. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isAlwaysDrawnWithCacheEnabled()()` Indicates whether this ViewGroup will always try to draw its children using their drawing cache. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isAnimationCacheEnabled()()` Indicates whether the children's drawing cache is used during a layout animation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isLayoutSuppressed()()` Returns whether layout calls on this container are currently being suppressed, due to an earlier call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#suppressLayout(kotlin.Boolean)`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isMotionEventSplittingEnabled()()` Returns true if MotionEvents dispatched to this ViewGroup can be split to multiple children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isTransitionGroup()()` Returns true if this ViewGroup should be considered as a single entity for removal when executing an Activity transition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#jumpDrawablesToCurrentState()()` Call `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#jumpToCurrentState()` on all Drawable objects associated with this view. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#layout(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(l: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, t: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Assign a size and position to a view and all of its descendants |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#notifySubtreeAccessibilityStateChanged(android.view.View,%20android.view.View,%20kotlin.Int)(child: https://developer.android.com/reference/kotlin/android/view/View, source: https://developer.android.com/reference/kotlin/android/view/View, changeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Notifies a view parent that the accessibility state of one of its descendants has changed and that the structure of the subtree is different. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#offsetDescendantRectToMyCoords(android.view.View,%20android.graphics.Rect)(descendant: https://developer.android.com/reference/kotlin/android/view/View!, rect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Offset a rectangle that is in a descendant's coordinate space into our coordinate space. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#offsetRectIntoDescendantCoords(android.view.View,%20android.graphics.Rect)(descendant: https://developer.android.com/reference/kotlin/android/view/View!, rect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Offset a rectangle that is in our coordinate space into an ancestor's coordinate space. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onDescendantInvalidated(android.view.View,%20android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View, target: https://developer.android.com/reference/kotlin/android/view/View)` The target View has been invalidated, or has had a drawing property changed that requires the hierarchy to re-render. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onInterceptHoverEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)` Implement this method to intercept hover events before they are handled by child views. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onInterceptTouchEvent(android.view.MotionEvent)(ev: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)` Implement this method to intercept all touch screen motion events. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onNestedFling(android.view.View,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean)(target: https://developer.android.com/reference/kotlin/android/view/View, velocityX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, velocityY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, consumed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Request a fling from a nested scroll. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onNestedPreFling(android.view.View,%20kotlin.Float,%20kotlin.Float)(target: https://developer.android.com/reference/kotlin/android/view/View, velocityX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, velocityY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` React to a nested fling before the target view consumes it. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onNestedPrePerformAccessibilityAction(android.view.View,%20kotlin.Int,%20android.os.Bundle)(target: https://developer.android.com/reference/kotlin/android/view/View, action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, args: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` React to an accessibility action delegated by a target descendant view before the target processes it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onNestedPreScroll(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.IntArray)(target: https://developer.android.com/reference/kotlin/android/view/View, dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, consumed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` React to a nested scroll in progress before the target view consumes a portion of the scroll. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onNestedScroll(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(target: https://developer.android.com/reference/kotlin/android/view/View, dxConsumed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dyConsumed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dxUnconsumed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dyUnconsumed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` React to a nested scroll in progress. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onNestedScrollAccepted(android.view.View,%20android.view.View,%20kotlin.Int)(child: https://developer.android.com/reference/kotlin/android/view/View, target: https://developer.android.com/reference/kotlin/android/view/View, axes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` React to the successful claiming of a nested scroll operation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onRequestSendAccessibilityEvent(android.view.View,%20android.view.accessibility.AccessibilityEvent)(child: https://developer.android.com/reference/kotlin/android/view/View!, event: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent!)` Called when a child has requested sending an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent` and gives an opportunity to its parent to augment the event. |
| open [PointerIcon](https://developer.android.com/reference/kotlin/android/view/PointerIcon)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onResolvePointerIcon(android.view.MotionEvent,%20kotlin.Int)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!, pointerIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Resolve the pointer icon that should be used for specified pointer in the motion event. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onStartNestedScroll(android.view.View,%20android.view.View,%20kotlin.Int)(child: https://developer.android.com/reference/kotlin/android/view/View, target: https://developer.android.com/reference/kotlin/android/view/View, nestedScrollAxes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` React to a descendant view initiating a nestable scroll operation, claiming the nested scroll operation if appropriate. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onStopNestedScroll(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View)` React to a nested scroll operation ending. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onViewAdded(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View!)` Called when a new child is added to this ViewGroup. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onViewRemoved(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View!)` Called when a child view is removed from this ViewGroup. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#propagateRequestedFrameRate(kotlin.Float,%20kotlin.Boolean)(frameRate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, forceOverride: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` You can set the preferred frame rate for a ViewGroup and its children using a positive number or by specifying the preferred frame rate category using constants, including REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE, REQUESTED_FRAME_RATE_CATEGORY_LOW, REQUESTED_FRAME_RATE_CATEGORY_NORMAL, REQUESTED_FRAME_RATE_CATEGORY_HIGH. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#recomputeViewAttributes(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View!)` Tell view hierarchy that the global view attributes need to be re-evaluated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeAllViews()()` Call this method to remove all child views from the ViewGroup. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeAllViewsInLayout()()` Called by a ViewGroup subclass to remove child views from itself, when it must first know its size on screen before it can calculate how many child views it will render. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeView(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View!)` **Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeViewAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes the view at the specified position in the group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeViewInLayout(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View!)` Removes a view during layout. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeViews(kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes the specified range of views from the group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeViewsInLayout(kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes a range of views during layout. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#requestChildFocus(android.view.View,%20android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View!, focused: https://developer.android.com/reference/kotlin/android/view/View!)` Called when a child of this parent wants focus |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#requestChildRectangleOnScreen(android.view.View,%20android.graphics.Rect,%20kotlin.Boolean)(child: https://developer.android.com/reference/kotlin/android/view/View, rectangle: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!, immediate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when a child of this group wants a particular rectangle to be positioned onto the screen. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#requestChildRectangleOnScreen(android.view.View,%20android.graphics.Rect,%20kotlin.Boolean,%20kotlin.Int)(child: https://developer.android.com/reference/kotlin/android/view/View, rectangle: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#, immediate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when a child of this group wants a particular rectangle to be positioned onto the screen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#requestDisallowInterceptTouchEvent(kotlin.Boolean)(disallowIntercept: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when a child does not want this parent and its ancestors to intercept touch events with `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onInterceptTouchEvent(android.view.MotionEvent)`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#requestFocus(kotlin.Int,%20android.graphics.Rect)(direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, previouslyFocusedRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Call this to try to give focus to a specific view or to one of its descendants and give it hints about the direction and a specific rectangle that the focus is coming from. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#requestSendAccessibilityEvent(android.view.View,%20android.view.accessibility.AccessibilityEvent)(child: https://developer.android.com/reference/kotlin/android/view/View, event: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent!)` Called by a child to request from its parent to send an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#requestTransparentRegion(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View!)` Called when a child wants the view hierarchy to gather and report transparent regions to the window compositor. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#restoreDefaultFocus()()` Gives focus to the default-focus view in the view hierarchy that has this view as a root. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#scheduleLayoutAnimation()()` Schedules the layout animation to be played after the next layout pass of this view group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setAddStatesFromChildren(kotlin.Boolean)(addsStates: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this ViewGroup's drawable states also include its children's drawable states. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setAlwaysDrawnWithCacheEnabled(kotlin.Boolean)(always: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Indicates whether this ViewGroup will always try to draw its children using their drawing cache. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setAnimationCacheEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enables or disables the children's drawing cache during a layout animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setClipChildren(kotlin.Boolean)(clipChildren: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` By default, children are clipped to their bounds before drawing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setClipToPadding(kotlin.Boolean)(clipToPadding: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this ViewGroup will clip its children to its padding and resize (but not clip) any EdgeEffect to the padded region, if padding is present. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setDescendantFocusability(kotlin.Int)(focusability: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the descendant focusability of this view group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setLayoutAnimation(android.view.animation.LayoutAnimationController)(controller: https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController!)` Sets the layout animation controller used to animate the group's children after the first layout. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setLayoutAnimationListener(android.view.animation.Animation.AnimationListener)(animationListener: https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener!)` Specifies the animation listener to which layout animation events must be sent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setLayoutMode(kotlin.Int)(layoutMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the basis of alignment during the layout of this ViewGroup. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setLayoutTransition(android.animation.LayoutTransition)(transition: https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.html#!)` Sets the LayoutTransition object for this ViewGroup. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setMotionEventSplittingEnabled(kotlin.Boolean)(split: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enable or disable the splitting of MotionEvents to multiple children during touch event dispatch. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setOnHierarchyChangeListener(android.view.ViewGroup.OnHierarchyChangeListener)(listener: https://developer.android.com/reference/kotlin/android/view/ViewGroup.OnHierarchyChangeListener!)` Register a callback to be invoked when a child is added to or removed from this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setPersistentDrawingCache(kotlin.Int)(drawingCacheToKeep: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Indicates what types of drawing caches should be kept in memory after they have been created. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setRequestedFrameRate(kotlin.Float)(frameRate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` You can set the preferred frame rate for a ViewGroup using a positive number or by specifying the preferred frame rate category using constants, including REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE, REQUESTED_FRAME_RATE_CATEGORY_LOW, REQUESTED_FRAME_RATE_CATEGORY_NORMAL, REQUESTED_FRAME_RATE_CATEGORY_HIGH. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setTouchscreenBlocksFocus(kotlin.Boolean)(touchscreenBlocksFocus: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether this ViewGroup should ignore focus requests for itself and its children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setTransitionGroup(kotlin.Boolean)(isTransitionGroup: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Changes whether or not this ViewGroup should be treated as a single entity during Activity Transitions. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setWindowInsetsAnimationCallback(android.view.WindowInsetsAnimation.Callback)(callback: https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback?)` Sets a `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback` to be notified about animations of windows that cause insets. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#shouldDelayChildPressedState()()` Return true if the pressed state should be delayed for children or descendants of this ViewGroup. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#showContextMenuForChild(android.view.View)(originalView: https://developer.android.com/reference/kotlin/android/view/View!)` Shows the context menu for the specified view or its ancestors. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#showContextMenuForChild(android.view.View,%20kotlin.Float,%20kotlin.Float)(originalView: https://developer.android.com/reference/kotlin/android/view/View!, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Shows the context menu for the specified view or its ancestors anchored to the specified view-relative coordinate. |
| open [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#startActionModeForChild(android.view.View,%20android.view.ActionMode.Callback)(originalView: https://developer.android.com/reference/kotlin/android/view/View!, callback: https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback!)` Start an action mode for the specified view with the default type `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int`. |
| open [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#startActionModeForChild(android.view.View,%20android.view.ActionMode.Callback,%20kotlin.Int)(originalView: https://developer.android.com/reference/kotlin/android/view/View!, callback: https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback!, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Start an action mode of a specific type for the specified view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#startLayoutAnimation()()` Runs the layout animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#startViewTransition(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View!)` This method tells the ViewGroup that the given View object, which should have this ViewGroup as its parent, should be kept around (re-displayed when the ViewGroup draws its children) even if it is removed from its parent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#suppressLayout(kotlin.Boolean)(suppress: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Tells this ViewGroup to suppress all layout() calls until layout suppression is disabled with a later call to suppressLayout(false). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#updateViewLayout(android.view.View,%20android.view.ViewGroup.LayoutParams)(view: https://developer.android.com/reference/kotlin/android/view/View!, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!)` <br /> |

| Protected methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addViewInLayout(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams)(child: https://developer.android.com/reference/kotlin/android/view/View!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!)` Adds a view during layout. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addViewInLayout(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams,%20kotlin.Boolean)(child: https://developer.android.com/reference/kotlin/android/view/View!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!, preventRequestLayout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Adds a view during layout. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#attachLayoutAnimationParameters(android.view.View,%20android.view.ViewGroup.LayoutParams,%20kotlin.Int,%20kotlin.Int)(child: https://developer.android.com/reference/kotlin/android/view/View!, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Subclasses should override this method to set layout animation parameters on the supplied child. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#attachViewToParent(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams)(child: https://developer.android.com/reference/kotlin/android/view/View!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!)` Attaches a view to this view group. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#canAnimate()()` Indicates whether the view group has the ability to animate its children after the first layout. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#checkLayoutParams(android.view.ViewGroup.LayoutParams)(p: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#cleanupLayoutState(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View!)` Prevents the specified child to be laid out during the next layout pass. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#debug(kotlin.Int)(depth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachAllViewsFromParent()()` Detaches all views from the parent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View!)` Detaches a view from its parent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Detaches a view from its parent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewsFromParent(kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Detaches a range of views from their parents. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)` Called by draw to draw the child views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchFreezeSelfOnly(android.util.SparseArray)(container: https://developer.android.com/reference/kotlin/android/util/SparseArray.html#<https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!>!)` Perform dispatching of a `https://developer.android.com/reference/kotlin/android/view/View#saveHierarchyState(android.util.SparseArray)` freeze()} to only this view, not to its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchGenericFocusedEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)` Dispatch a generic motion event to the currently focused view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchGenericPointerEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)` Dispatch a generic motion event to the view under the first pointer. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchHoverEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)` Dispatch a hover event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchRestoreInstanceState(android.util.SparseArray)(container: https://developer.android.com/reference/kotlin/android/util/SparseArray.html#<https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!>!)` Called by `https://developer.android.com/reference/kotlin/android/view/View#restoreHierarchyState(android.util.SparseArray)` to retrieve the state for this view and its children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchSaveInstanceState(android.util.SparseArray)(container: https://developer.android.com/reference/kotlin/android/util/SparseArray.html#<https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!>!)` Called by `https://developer.android.com/reference/kotlin/android/view/View#saveHierarchyState(android.util.SparseArray)` to store the state for this view and its children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchSetPressed(kotlin.Boolean)(pressed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Dispatch setPressed to all of this View's children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchThawSelfOnly(android.util.SparseArray)(container: https://developer.android.com/reference/kotlin/android/util/SparseArray.html#<https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!>!)` Perform dispatching of a `https://developer.android.com/reference/kotlin/android/view/View#restoreHierarchyState(android.util.SparseArray)` to only this view, not to its children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchVisibilityChanged(android.view.View,%20kotlin.Int)(changedView: https://developer.android.com/reference/kotlin/android/view/View, visibility: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Dispatch a view visibility change down the view hierarchy. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#drawChild(android.graphics.Canvas,%20android.view.View,%20kotlin.Long)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#, child: https://developer.android.com/reference/kotlin/android/view/View!, drawingTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Draw one child of this View Group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#drawableStateChanged()()` This function is called whenever the state of the view changes in such a way that it impacts the state of drawables being shown. |
| open [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#generateDefaultLayoutParams()()` Returns a set of default layout parameters. |
| open [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#generateLayoutParams(android.view.ViewGroup.LayoutParams)(p: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!)` Returns a safe set of layout parameters based on the supplied layout params. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildDrawingOrder(kotlin.Int,%20kotlin.Int)(childCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, drawingPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Converts drawing order position to container position. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildStaticTransformation(android.view.View,%20android.view.animation.Transformation)(child: https://developer.android.com/reference/kotlin/android/view/View!, t: https://developer.android.com/reference/kotlin/android/view/animation/Transformation!)` Sets `t` to be the static transformation of the child, if set, returning a boolean to indicate whether a static transform was set. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isChildrenDrawingOrderEnabled()()` Indicates whether the ViewGroup is drawing its children in the order defined by `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildDrawingOrder(kotlin.Int,%20kotlin.Int)`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isChildrenDrawnWithCacheEnabled()()` Indicates whether the ViewGroup is currently drawing its children using their drawing cache. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#measureChild(android.view.View,%20kotlin.Int,%20kotlin.Int)(child: https://developer.android.com/reference/kotlin/android/view/View!, parentWidthMeasureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, parentHeightMeasureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Ask one of the children of this view to measure itself, taking into account both the MeasureSpec requirements for this view and its padding. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#measureChildWithMargins(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(child: https://developer.android.com/reference/kotlin/android/view/View!, parentWidthMeasureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, widthUsed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, parentHeightMeasureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, heightUsed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Ask one of the children of this view to measure itself, taking into account both the MeasureSpec requirements for this view and its padding and margins. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#measureChildren(kotlin.Int,%20kotlin.Int)(widthMeasureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, heightMeasureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Ask all of the children of this view to measure themselves, taking into account both the MeasureSpec requirements for this view and its padding. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onAttachedToWindow()()` This is called when the view is attached to a window. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onCreateDrawableState(kotlin.Int)(extraSpace: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Generate the new `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` state for this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onDetachedFromWindow()()` This is called when the view is detached from a window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onLayout(kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(changed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, l: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, t: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called from layout when this view should assign a size and position to each of its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onRequestFocusInDescendants(kotlin.Int,%20android.graphics.Rect)(direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, previouslyFocusedRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Look for a descendant to call android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeDetachedView(android.view.View,%20kotlin.Boolean)(child: https://developer.android.com/reference/kotlin/android/view/View!, animate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Finishes the removal of a detached view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setChildrenDrawingCacheEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enables or disables the drawing cache for each child of this view group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setChildrenDrawingOrderEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Tells the ViewGroup whether to draw its children in the order defined by the method `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildDrawingOrder(kotlin.Int,%20kotlin.Int)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setChildrenDrawnWithCacheEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Tells the ViewGroup to draw its children using their drawing cache. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setStaticTransformationsEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` When this property is set to true, this ViewGroup supports static transformations on children; this causes `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildStaticTransformation(android.view.View,%20android.view.animation.Transformation)` to be invoked when a child is drawn. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/view/View` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#addFocusables(java.util.ArrayList,%20kotlin.Int)(views: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/view/View!>!, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Add any focusable views that are descendants of this view (possibly including this view if it is focusable itself) to views. If we are in touch mode, only add views that are also focusable in touch mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#addOnAttachStateChangeListener(android.view.View.OnAttachStateChangeListener)(listener: https://developer.android.com/reference/kotlin/android/view/View.OnAttachStateChangeListener!)`

Add a listener for attach state changes. This listener will be called whenever this view is attached or detached from a window. Remove the listener using `https://developer.android.com/reference/kotlin/android/view/View#removeOnAttachStateChangeListener(android.view.View.OnAttachStateChangeListener)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#addOnLayoutChangeListener(android.view.View.OnLayoutChangeListener)(listener: https://developer.android.com/reference/kotlin/android/view/View.OnLayoutChangeListener!)`

Add a listener that will be called when the bounds of the view change due to layout processing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#addOnUnhandledKeyEventListener(android.view.View.OnUnhandledKeyEventListener)(listener: https://developer.android.com/reference/kotlin/android/view/View.OnUnhandledKeyEventListener!)`

Adds a listener which will receive unhandled `https://developer.android.com/reference/kotlin/android/view/KeyEvent`s. This must be called on the UI thread.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator!` `https://developer.android.com/reference/kotlin/android/view/View#animate()()`

This method returns a ViewPropertyAnimator object, which can be used to animate specific properties on this View.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#announceForAccessibility(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)`

Convenience method for sending a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_ANNOUNCEMENT:kotlin.Int` `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent` to suggest that an accessibility service announce the specified text to its users.

Note: The event generated with this API carries no semantic meaning, and accessibility services may choose to ignore it. Apps that accurately supply accessibility with the semantics of their UI should not need to specify what exactly is announced.

In general, do not attempt to generate announcements as confirmation message for simple actions like a button press. Label your controls concisely and precisely instead.

To convey significant UI changes like window changes, use `https://developer.android.com/reference/kotlin/android/app/Activity.html#setTitle(kotlin.CharSequence)` and `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityPaneTitle(kotlin.CharSequence)`.

Use `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityLiveRegion(kotlin.Int)` to inform the user of changes to critical views within the user interface. These should still be used sparingly as they may generate announcements every time a View is updated.

Use `https://developer.android.com/reference/kotlin/android/view/View#setStateDescription(kotlin.CharSequence)` to convey state changes to views within the user interface. While a live region may send different types of events generated by the view, state description will send `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` events of type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION:kotlin.Int`.

For notifying users about errors, such as in a login screen with text that displays an "incorrect password" notification, set `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setError(kotlin.CharSequence)` and dispatch an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` event with a change type of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_ERROR:kotlin.Int`, instead. Some widgets may expose methods that convey error states to accessibility automatically, such as `https://developer.android.com/reference/kotlin/android/widget/TextView.html#setError(kotlin.CharSequence)`, which manages these accessibility semantics and event dispatch for callers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#autofill(android.util.SparseArray)(values: https://developer.android.com/reference/kotlin/android/util/SparseArray.html#<https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue!>)`

Automatically fills the content of the virtual children within this view.

Views with virtual children support the Autofill Framework mainly by:

- Providing the metadata defining what the virtual children mean and how they can be autofilled.
- Implementing the methods that autofill the virtual children.

`https://developer.android.com/reference/kotlin/android/view/View#onProvideAutofillVirtualStructure(android.view.ViewStructure,%20kotlin.Int)` is responsible for the former, this method is responsible for the latter - see `https://developer.android.com/reference/kotlin/android/view/View#autofill(android.view.autofill.AutofillValue)` and `https://developer.android.com/reference/kotlin/android/view/View#onProvideAutofillVirtualStructure(android.view.ViewStructure,%20kotlin.Int)` for more info about autofill.

If a child value is updated asynchronously, the next call to `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyValueChanged(android.view.View,%20kotlin.Int,%20android.view.autofill.AutofillValue)` must happen **after** the value was changed to the autofilled value. If not, the child will not be considered autofilled.

**Note:** To indicate that a virtual view was autofilled, `?android:attr/autofilledHighlight` should be drawn over it until the data changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#autofill(android.view.autofill.AutofillValue)(value: https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue!)`

Automatically fills the content of this view with the `value`.

Views support the Autofill Framework mainly by:

- Providing the metadata defining what the view means and how it can be autofilled.
- Implementing the methods that autofill the view.

`https://developer.android.com/reference/kotlin/android/view/View#onProvideAutofillStructure(android.view.ViewStructure,%20kotlin.Int)` is responsible for the former, this method is responsible for latter.

This method does nothing by default, but when overridden it typically:

1. Checks if the provided value matches the expected type (which is defined by `https://developer.android.com/reference/kotlin/android/view/View#getAutofillType()`).
2. Checks if the view is editable - if it isn't, it should return right away.
3. Call the proper getter method on `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue` to fetch the actual value.
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

If the value is updated asynchronously, the next call to `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyValueChanged(android.view.View)` must happen **after** the value was changed to the autofilled value. If not, the view will not be considered autofilled.

**Note:** After this method is called, the value returned by `https://developer.android.com/reference/kotlin/android/view/View#getAutofillValue()` must be equal to the `value` passed to it, otherwise the view will not be highlighted as autofilled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#awakenScrollBars()()`

Trigger the scrollbars to draw. When invoked this method starts an animation to fade the scrollbars out after a default delay. If a subclass provides animated scrolling, the start delay should equal the duration of the scrolling animation.

The animation starts only if at least one of the scrollbars is enabled, as specified by `https://developer.android.com/reference/kotlin/android/view/View#isHorizontalScrollBarEnabled()` and `https://developer.android.com/reference/kotlin/android/view/View#isVerticalScrollBarEnabled()`. When the animation is started, this method returns true, and false otherwise. If the animation is started, this method calls `https://developer.android.com/reference/kotlin/android/view/View#invalidate()`; in that case the caller should not call `https://developer.android.com/reference/kotlin/android/view/View#invalidate()`.

This method should be invoked every time a subclass directly updates the scroll parameters.

This method is automatically invoked by `https://developer.android.com/reference/kotlin/android/view/View#scrollBy(kotlin.Int,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/view/View#scrollTo(kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#awakenScrollBars(kotlin.Int)(startDelay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Trigger the scrollbars to draw. When invoked this method starts an animation to fade the scrollbars out after a fixed delay. If a subclass provides animated scrolling, the start delay should equal the duration of the scrolling animation.

The animation starts only if at least one of the scrollbars is enabled, as specified by `https://developer.android.com/reference/kotlin/android/view/View#isHorizontalScrollBarEnabled()` and `https://developer.android.com/reference/kotlin/android/view/View#isVerticalScrollBarEnabled()`. When the animation is started, this method returns true, and false otherwise. If the animation is started, this method calls `https://developer.android.com/reference/kotlin/android/view/View#invalidate()`; in that case the caller should not call `https://developer.android.com/reference/kotlin/android/view/View#invalidate()`.

This method should be invoked every time a subclass directly updates the scroll parameters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#awakenScrollBars(kotlin.Int,%20kotlin.Boolean)(startDelay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, invalidate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Trigger the scrollbars to draw. When invoked this method starts an animation to fade the scrollbars out after a fixed delay. If a subclass provides animated scrolling, the start delay should equal the duration of the scrolling animation.

The animation starts only if at least one of the scrollbars is enabled, as specified by `https://developer.android.com/reference/kotlin/android/view/View#isHorizontalScrollBarEnabled()` and `https://developer.android.com/reference/kotlin/android/view/View#isVerticalScrollBarEnabled()`. When the animation is started, this method returns true, and false otherwise. If the animation is started, this method calls `https://developer.android.com/reference/kotlin/android/view/View#invalidate()` if the invalidate parameter is set to true; in that case the caller should not call `https://developer.android.com/reference/kotlin/android/view/View#invalidate()`.

This method should be invoked every time a subclass directly updates the scroll parameters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#bringToFront()()`

Change the view's z order in the tree, so it's on top of other sibling views. This ordering change may affect layout, if the parent container uses an order-dependent layout scheme (e.g., LinearLayout). Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int` this method should be followed by calls to `https://developer.android.com/reference/kotlin/android/view/View#requestLayout()` and `https://developer.android.com/reference/kotlin/android/view/View#invalidate()` on the view's parent to force the parent to redraw with the new child ordering.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#buildDrawingCache()()`

Calling this method is equivalent to calling `buildDrawingCache(false)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#buildDrawingCache(kotlin.Boolean)(autoScale: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Forces the drawing cache to be built if the drawing cache is invalid.

If you call `https://developer.android.com/reference/kotlin/android/view/View#buildDrawingCache()` manually without calling `https://developer.android.com/reference/kotlin/android/view/View#setDrawingCacheEnabled(kotlin.Boolean)`, you should cleanup the cache by calling `https://developer.android.com/reference/kotlin/android/view/View#destroyDrawingCache()` afterwards.

Note about auto scaling in compatibility mode: When auto scaling is not enabled, this method will create a bitmap of the same size as this view. Because this bitmap will be drawn scaled by the parent ViewGroup, the result on screen might show scaling artifacts. To avoid such artifacts, you should call this method by setting the auto scaling to true. Doing so, however, will generate a bitmap of a different size than the view. This implies that your application must be able to handle this size.

You should avoid calling this method when hardware acceleration is enabled. If you do not need the drawing cache bitmap, calling this method will increase memory usage and cause the view to be rendered in software once, thus negatively impacting performance.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#buildLayer()()`

Forces this view's layer to be created and this view to be rendered into its layer. If this view's layer type is set to `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`, invoking this method will have no effect. This method can for instance be used to render a view into its layer before starting an animation. If this view is complex, rendering into the layer before starting the animation will avoid skipping frames.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#callOnClick()()`

Directly call any attached OnClickListener. Unlike `https://developer.android.com/reference/kotlin/android/view/View#performClick()`, this only calls the listener, and does not do any associated clicking actions like reporting an accessibility event.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#canResolveLayoutDirection()()`

Check if layout direction resolution can be done.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#canResolveTextAlignment()()`

Check if text alignment resolution can be done.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#canResolveTextDirection()()`

Check if text direction resolution can be done.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#canScrollHorizontally(kotlin.Int)(direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Check if this view can be scrolled horizontally in a certain direction.

This is without regard to whether the view is enabled or not, or if it will scroll in response to user input or not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#canScrollVertically(kotlin.Int)(direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Check if this view can be scrolled vertically in a certain direction.

This is without regard to whether the view is enabled or not, or if it will scroll in response to user input or not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#cancelDragAndDrop()()`

Cancels an ongoing drag and drop operation.

A `https://developer.android.com/reference/kotlin/android/view/DragEvent` object with `https://developer.android.com/reference/kotlin/android/view/DragEvent#getAction()` value of `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENDED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/DragEvent#getResult()` value of `false` will be sent to every View that received `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_STARTED:kotlin.Int` even if they are not currently visible.

This method can be called on any View in the same window as the View on which `https://developer.android.com/reference/kotlin/android/view/View#startDragAndDrop(android.content.ClipData,%20android.view.View.DragShadowBuilder,%20kotlin.Any,%20kotlin.Int)` was called.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#cancelLongPress()()`

Cancels a pending long press. Your subclass can use this if you want the context menu to come up if the user presses and holds at the same place, but you don't want it to come up if they press and then move around enough to cause scrolling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#cancelPendingInputEvents()()`

Cancel any deferred high-level input events that were previously posted to the event queue.

Many views post high-level events such as click handlers to the event queue to run deferred in order to preserve a desired user experience - clearing visible pressed states before executing, etc. This method will abort any events of this nature that are currently in flight.

Custom views that generate their own high-level deferred input events should override `https://developer.android.com/reference/kotlin/android/view/View#onCancelPendingInputEvents()` and remove those pending events from the queue.

This will also cancel pending input events for any child views.

Note that this may not be sufficient as a debouncing strategy for clicks in all cases. This will not impact newer events posted after this call that may occur as a result of lower-level input events still waiting in the queue. If you are trying to prevent double-submitted events for the duration of some sort of asynchronous transaction you should also take other steps to protect against unexpected double inputs e.g. calling `https://developer.android.com/reference/kotlin/android/view/View#setEnabled(kotlin.Boolean)` and re-enabling the view when the transaction completes, tracking already submitted transaction IDs, etc.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#checkInputConnectionProxy(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View!)`

Called by the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager` when a view who is not the current input connection target is trying to make a call on the manager. The default implementation returns false; you can override this to return true for certain views if you are performing InputConnection proxying to them.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#clearAnimation()()`

Cancels any animations for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#clearPendingCredentialRequest()()`

Clears the request and callback previously set through `https://developer.android.com/reference/kotlin/android/view/View#setPendingCredentialRequest(android.credentials.GetCredentialRequest,%20android.os.OutcomeReceiver)`. Once this API is invoked, there will be no request fired to `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` on future view focus events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#clearViewTranslationCallback()()`

Clear the `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback` from this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#combineMeasuredStates(kotlin.Int,%20kotlin.Int)(curState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Merge two states as returned by `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredState()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#computeHorizontalScrollExtent()()`

Compute the horizontal extent of the horizontal scrollbar's thumb within the horizontal range. This value is used to compute the length of the thumb within the scrollbar's track.

The range is expressed in arbitrary units that must be the same as the units used by `https://developer.android.com/reference/kotlin/android/view/View#computeHorizontalScrollRange()` and `https://developer.android.com/reference/kotlin/android/view/View#computeHorizontalScrollOffset()`.

The default extent is the drawing width of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#computeHorizontalScrollOffset()()`

Compute the horizontal offset of the horizontal scrollbar's thumb within the horizontal range. This value is used to compute the position of the thumb within the scrollbar's track.

The range is expressed in arbitrary units that must be the same as the units used by `https://developer.android.com/reference/kotlin/android/view/View#computeHorizontalScrollRange()` and `https://developer.android.com/reference/kotlin/android/view/View#computeHorizontalScrollExtent()`.

The default offset is the scroll offset of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#computeHorizontalScrollRange()()`

Compute the horizontal range that the horizontal scrollbar represents.

The range is expressed in arbitrary units that must be the same as the units used by `https://developer.android.com/reference/kotlin/android/view/View#computeHorizontalScrollExtent()` and `https://developer.android.com/reference/kotlin/android/view/View#computeHorizontalScrollOffset()`.

The default range is the drawing width of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#computeScroll()()`

Called by a parent to request that a child update its values for mScrollX and mScrollY if necessary. This will typically be done if the child is animating a scroll using a `https://developer.android.com/reference/kotlin/android/widget/Scroller.html#` object.

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowInsets!` `https://developer.android.com/reference/kotlin/android/view/View#computeSystemWindowInsets(android.view.WindowInsets,%20android.graphics.Rect)(in: https://developer.android.com/reference/kotlin/android/view/WindowInsets!, outLocalInsets: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Compute insets that should be consumed by this view and the ones that should propagate to those under it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#computeVerticalScrollExtent()()`

Compute the vertical extent of the vertical scrollbar's thumb within the vertical range. This value is used to compute the length of the thumb within the scrollbar's track.

The range is expressed in arbitrary units that must be the same as the units used by `https://developer.android.com/reference/kotlin/android/view/View#computeVerticalScrollRange()` and `https://developer.android.com/reference/kotlin/android/view/View#computeVerticalScrollOffset()`.

The default extent is the drawing height of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#computeVerticalScrollOffset()()`

Compute the vertical offset of the vertical scrollbar's thumb within the horizontal range. This value is used to compute the position of the thumb within the scrollbar's track.

The range is expressed in arbitrary units that must be the same as the units used by `https://developer.android.com/reference/kotlin/android/view/View#computeVerticalScrollRange()` and `https://developer.android.com/reference/kotlin/android/view/View#computeVerticalScrollExtent()`.

The default offset is the scroll offset of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#computeVerticalScrollRange()()`

Compute the vertical range that the vertical scrollbar represents.

The range is expressed in arbitrary units that must be the same as the units used by `https://developer.android.com/reference/kotlin/android/view/View#computeVerticalScrollExtent()` and `https://developer.android.com/reference/kotlin/android/view/View#computeVerticalScrollOffset()`.

<br />

`https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo!` `https://developer.android.com/reference/kotlin/android/view/View#createAccessibilityNodeInfo()()`

Returns an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo` representing this view from the point of view of an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This method is responsible for obtaining an accessibility node info from a pool of reusable instances and calling `https://developer.android.com/reference/kotlin/android/view/View#onInitializeAccessibilityNodeInfo(android.view.accessibility.AccessibilityNodeInfo)` on this view to initialize the former.

Note: The client is responsible for recycling the obtained instance by calling `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#recycle()` to minimize object creation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#createContextMenu(android.view.ContextMenu)(menu: https://developer.android.com/reference/kotlin/android/view/ContextMenu!)`

Show the context menu for this view. It is not safe to hold on to the menu after returning from this method. You should normally not overload this method. Overload `https://developer.android.com/reference/kotlin/android/view/View#onCreateContextMenu(android.view.ContextMenu)` or define an `https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener` to add items to the context menu.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#destroyDrawingCache()()`

Frees the resources used by the drawing cache. If you call `https://developer.android.com/reference/kotlin/android/view/View#buildDrawingCache()` manually without calling `https://developer.android.com/reference/kotlin/android/view/View#setDrawingCacheEnabled(kotlin.Boolean)`, you should cleanup the cache with this method afterwards.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#dispatchGenericMotionEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)`

Dispatch a generic motion event.

Generic motion events with source class `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_POINTER:kotlin.Int` are delivered to the view under the pointer. All other generic motion events are delivered to the focused view. Hover events are handled specially and are delivered to `https://developer.android.com/reference/kotlin/android/view/View#onHoverEvent(android.view.MotionEvent)` first.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#dispatchNestedFling(kotlin.Float,%20kotlin.Float,%20kotlin.Boolean)(velocityX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, velocityY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, consumed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Dispatch a fling to a nested scrolling parent.

This method should be used to indicate that a nested scrolling child has detected suitable conditions for a fling. Generally this means that a touch scroll has ended with a `https://developer.android.com/reference/kotlin/android/view/VelocityTracker` in the direction of scrolling that meets or exceeds the `https://developer.android.com/reference/kotlin/android/view/ViewConfiguration#getScaledMinimumFlingVelocity()` along a scrollable axis.

If a nested scrolling child view would normally fling but it is at the edge of its own content, it can use this method to delegate the fling to its nested scrolling parent instead. The parent may optionally consume the fling or observe a child fling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#dispatchNestedPreFling(kotlin.Float,%20kotlin.Float)(velocityX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, velocityY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Dispatch a fling to a nested scrolling parent before it is processed by this view.

Nested pre-fling events are to nested fling events what touch intercept is to touch and what nested pre-scroll is to nested scroll. `dispatchNestedPreFling` offsets an opportunity for the parent view in a nested fling to fully consume the fling before the child view consumes it. If this method returns `true`, a nested parent view consumed the fling and this view should not scroll as a result.

For a better user experience, only one view in a nested scrolling chain should consume the fling at a time. If a parent view consumed the fling this method will return false. Custom view implementations should account for this in two ways:

- If a custom view is paged and needs to settle to a fixed page-point, do not call `dispatchNestedPreFling`; consume the fling and settle to a valid position regardless.
- If a nested parent does consume the fling, this view should not scroll at all, even to settle back to a valid idle position.

Views should also not offer fling velocities to nested parent views along an axis where scrolling is not currently supported; a `https://developer.android.com/reference/kotlin/android/widget/ScrollView.html#` should not offer a horizontal fling velocity to its parents since scrolling along that axis is not permitted and carrying velocity along that motion does not make sense.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#dispatchNestedPrePerformAccessibilityAction(kotlin.Int,%20android.os.Bundle)(action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, arguments: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Report an accessibility action to this view's parents for delegated processing.

Implementations of `https://developer.android.com/reference/kotlin/android/view/View#performAccessibilityAction(kotlin.Int,%20android.os.Bundle)` may internally call this method to delegate an accessibility action to a supporting parent. If the parent returns true from its `https://developer.android.com/reference/kotlin/android/view/ViewParent#onNestedPrePerformAccessibilityAction(android.view.View,%20kotlin.Int,%20android.os.Bundle)` method this method will return true to signify that the action was consumed.

This method is useful for implementing nested scrolling child views. If `https://developer.android.com/reference/kotlin/android/view/View#isNestedScrollingEnabled()` returns true and the action is a scrolling action a custom view implementation may invoke this method to allow a parent to consume the scroll first. If this method returns true the custom view should skip its own scrolling behavior.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#dispatchNestedPreScroll(kotlin.Int,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.IntArray)(dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, consumed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?, offsetInWindow: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?)`

Dispatch one step of a nested scroll in progress before this view consumes any portion of it.

Nested pre-scroll events are to nested scroll events what touch intercept is to touch. `dispatchNestedPreScroll` offers an opportunity for the parent view in a nested scrolling operation to consume some or all of the scroll operation before the child view consumes it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#dispatchNestedScroll(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.IntArray)(dxConsumed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dyConsumed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dxUnconsumed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dyUnconsumed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, offsetInWindow: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?)`

Dispatch one step of a nested scroll in progress.

Implementations of views that support nested scrolling should call this to report info about a scroll in progress to the current nested scrolling parent. If a nested scroll is not currently in progress or nested scrolling is not `https://developer.android.com/reference/kotlin/android/view/View#isNestedScrollingEnabled()` for this view this method does nothing.

Compatible View implementations should also call `https://developer.android.com/reference/kotlin/android/view/View#dispatchNestedPreScroll(kotlin.Int,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.IntArray)` before consuming a component of the scroll event themselves.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#dispatchPopulateAccessibilityEvent(android.view.accessibility.AccessibilityEvent)(event: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent!)`

Dispatches an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent` to the `https://developer.android.com/reference/kotlin/android/view/View` to add the text content of the view and its children.

**Note:** This method should only be used with event.setText(). Avoid mutating other event state in this method. In general, put UI metadata in the node for services to easily query.

- If you are modifying other event properties, you may be eliminating semantics accessibility services may want. Instead, send a separate event using `https://developer.android.com/reference/kotlin/android/view/View#sendAccessibilityEvent(kotlin.Int)` and override `https://developer.android.com/reference/kotlin/android/view/View#onInitializeAccessibilityEvent(android.view.accessibility.AccessibilityEvent)`.
- If you are checking for type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int` to generate window/title announcements, you may be causing disruptive announcements (or making no announcements at all). Instead, follow the practices described in `https://developer.android.com/reference/kotlin/android/view/View#announceForAccessibility(kotlin.CharSequence)`. **Note:** this does not suggest calling announceForAccessibility(), but using the suggestions listed in its documentation.
- If you are making changes based on the state of accessibility, such as checking for an event type to trigger a UI update, while well-intentioned, you are creating brittle, less well-maintained code that works for some users but not others. Instead, leverage existing code for equitable experiences and less technical debt. See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#isEnabled()` for an example.

Note that the event text is populated in a separate dispatch path (`https://developer.android.com/reference/kotlin/android/view/View#onPopulateAccessibilityEvent(android.view.accessibility.AccessibilityEvent)`) since we add to the event not only the text of the source but also the text of all its descendants.

A typical implementation will call `https://developer.android.com/reference/kotlin/android/view/View#onPopulateAccessibilityEvent(android.view.accessibility.AccessibilityEvent)` on this view and then call the `https://developer.android.com/reference/kotlin/android/view/View#dispatchPopulateAccessibilityEvent(android.view.accessibility.AccessibilityEvent)` on each child or the first child that is visible. Override this method if custom population of the event text content is required.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityDelegate(android.view.View.AccessibilityDelegate)` its `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate#dispatchPopulateAccessibilityEvent(android.view.View,%20android.view.accessibility.AccessibilityEvent)` is responsible for handling this call.

If this view sets `https://developer.android.com/reference/kotlin/android/view/View#isAccessibilityDataSensitive()` then this view should only append sensitive information to an event that also sets `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#isAccessibilityDataSensitive()`.

*Note:* Accessibility events of certain types are not dispatched for populating the event text via this method. For details refer to `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`

Manually render this view (and all of its children) to the given Canvas. The view must have already done a full layout before this function is called. When implementing a view, implement `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)` instead of overriding this method. If you do need to override this method, call the superclass version. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#drawableHotspotChanged(kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

This function is called whenever the view hotspot changes and needs to be propagated to drawables or child views managed by the view.

Dispatching to child views is handled by `https://developer.android.com/reference/kotlin/android/view/View#dispatchDrawableHotspotChanged(kotlin.Float,%20kotlin.Float)`.

Be sure to call through to the superclass when overriding this function. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#?` `https://developer.android.com/reference/kotlin/android/view/View#findOnBackInvokedDispatcher()()`

Walk up the View hierarchy to find the nearest `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#`.

<br />

`T` `https://developer.android.com/reference/kotlin/android/view/View#findViewById(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Finds the first descendant view with the given ID, the view itself if the ID matches `https://developer.android.com/reference/kotlin/android/view/View#getId()`, or `null` if the ID is invalid (\< 0) or there is no matching view in the hierarchy.

**Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

<br />

`T` `https://developer.android.com/reference/kotlin/android/view/View#findViewWithTag(kotlin.Any)(tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)`

Look for a child view with the given tag. If this view has the given tag, return this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect)(insets: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Called by the view hierarchy when the content insets for a window have changed, to allow it to adjust its content to fit within those windows. The content insets tell you the space that the status bar, input method, and other system windows infringe on the application's window.

You do not normally need to deal with this function, since the default window decoration given to applications takes care of applying it to the content of the window. If you use `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int` this will not be the case, and your content can be placed under those system elements. You can then use this method within your view hierarchy if you have parts of your UI which you would like to ensure are not being covered.

The default implementation of this method simply applies the content insets to the view's padding, consuming that content (modifying the insets to be 0), and returning true. This behavior is off by default, but can be enabled through `https://developer.android.com/reference/kotlin/android/view/View#setFitsSystemWindows(kotlin.Boolean)`.

This function's traversal down the hierarchy is depth-first. The same content insets object is propagated down the hierarchy, so any changes made to it will be seen by all following views (including potentially ones above in the hierarchy since this is a depth-first traversal). The first view that returns true will abort the entire traversal.

The default implementation works well for a situation where it is used with a container that covers the entire window, allowing it to apply the appropriate insets to its content on all edges. If you need a more complicated layout (such as two different views fitting system windows, one on the top of the window, and one on the bottom), you can override the method and handle the insets however you would like. Note that the insets provided by the framework are always relative to the far edges of the window, not accounting for the location of the called view within that window. (In fact when this method is called you do not yet know where the layout will place the view, as it is done before layout happens.)

Note: unlike many View methods, there is no dispatch phase to this call. If you are overriding it in a ViewGroup and want to allow the call to continue to your children, you must be sure to call the super implementation.

Here is a sample layout that makes use of fitting system windows to have controls for a video view placed inside of the window decorations that it hides and shows. This can be used with code like the second sample (video player) shown in `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)`.

<br />

`https://developer.android.com/reference/kotlin/android/view/View!` `https://developer.android.com/reference/kotlin/android/view/View#focusSearch(kotlin.Int)(direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Find the nearest view in the specified direction that can take focus. This does not actually give focus to that view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#forceHasOverlappingRendering(kotlin.Boolean)(hasOverlappingRendering: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets the behavior for overlapping rendering for this view (see `https://developer.android.com/reference/kotlin/android/view/View#hasOverlappingRendering()` for more details on this behavior). Calling this method is an alternative to overriding `https://developer.android.com/reference/kotlin/android/view/View#hasOverlappingRendering()` in a subclass, providing the value which is then used internally. That is, when `https://developer.android.com/reference/kotlin/android/view/View#forceHasOverlappingRendering(kotlin.Boolean)` is called, the value of `https://developer.android.com/reference/kotlin/android/view/View#hasOverlappingRendering()` is ignored and the value passed into this method is used instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#forceLayout()()`

Forces this view to be laid out during the next layout pass. This method does not call requestLayout() or forceLayout() on the parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#generateDisplayHash(kotlin.String,%20android.graphics.Rect,%20java.util.concurrent.Executor,%20android.view.displayhash.DisplayHashResultCallback)(hashAlgorithm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashResultCallback)`

Called to generate a `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHash` for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#generateViewId()()`

Generate a value suitable for use in `https://developer.android.com/reference/kotlin/android/view/View#setId(kotlin.Int)`. This value will not collide with ID values generated at build time by aapt for R.id.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate!` `https://developer.android.com/reference/kotlin/android/view/View#getAccessibilityDelegate()()`

Returns the delegate for implementing accessibility support via composition. For more details see `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getAccessibilityLiveRegion()()`

Gets the live region mode for this View.

<br />

`https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider!` `https://developer.android.com/reference/kotlin/android/view/View#getAccessibilityNodeProvider()()`

Gets the provider for managing a virtual view hierarchy rooted at this View and reported to `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s that explore the window content.

If this method returns an instance, this instance is responsible for managing `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo`s describing the virtual sub-tree rooted at this View including the one representing the View itself. Similarly the returned instance is responsible for performing accessibility actions on any virtual view or the root view itself.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityDelegate(android.view.View.AccessibilityDelegate)` its `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate#getAccessibilityNodeProvider(android.view.View)` is responsible for handling this call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` `https://developer.android.com/reference/kotlin/android/view/View#getAccessibilityPaneTitle()()`

Get the title of the pane for purposes of accessibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getAccessibilityTraversalAfter()()`

Gets the id of a view after which this one is visited in accessibility traversal.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getAccessibilityTraversalBefore()()`

Gets the id of a view before which this one is visited in accessibility traversal.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/view/View#getAllowedHandwritingDelegatePackageName()()`

Returns the allowed package for delegate editor views for which this view may act as a handwriting delegator, as set by `https://developer.android.com/reference/kotlin/android/view/View#setAllowedHandwritingDelegatePackage(kotlin.String)`. If `https://developer.android.com/reference/kotlin/android/view/View#setAllowedHandwritingDelegatePackage(kotlin.String)` has not been called, or called with `null` argument, this will return `null`, meaning that this delegator view may only be used to initiate handwriting mode for a delegate editor view from the same package as this delegator view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/view/View#getAllowedHandwritingDelegatorPackageName()()`

Returns the allowed package for views which may act as a handwriting delegator for this delegate editor view, as set by `https://developer.android.com/reference/kotlin/android/view/View#setAllowedHandwritingDelegatorPackage(kotlin.String)`. If `https://developer.android.com/reference/kotlin/android/view/View#setAllowedHandwritingDelegatorPackage(kotlin.String)` has not been called, or called with `null` argument, this will return `null`, meaning that only views from the same package as this delegator editor view may act as a handwriting delegator.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getAlpha()()`

The opacity of the view. This is a value from 0 to 1, where 0 means the view is completely transparent and 1 means the view is completely opaque.

By default this is 1.0f.

<br />

`https://developer.android.com/reference/kotlin/android/view/animation/Animation!` `https://developer.android.com/reference/kotlin/android/view/View#getAnimation()()`

Get the animation currently associated with this view.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getAnimationMatrix()()`

Return the current transformation matrix of the view. This is used in animation frameworks, such as `https://developer.android.com/reference/kotlin/android/transition/Transition.html#`. Returns `null` when there is no transformation provided by `https://developer.android.com/reference/kotlin/android/view/View#setAnimationMatrix(android.graphics.Matrix)`. Application developers should use transformation methods like `https://developer.android.com/reference/kotlin/android/view/View#setRotation(kotlin.Float)`, `https://developer.android.com/reference/kotlin/android/view/View#setScaleX(kotlin.Float)`, `https://developer.android.com/reference/kotlin/android/view/View#setScaleX(kotlin.Float)`, `https://developer.android.com/reference/kotlin/android/view/View#setTranslationX(kotlin.Float)`} and `https://developer.android.com/reference/kotlin/android/view/View#setTranslationY(kotlin.Float)` (float)}} instead.

<br />

`https://developer.android.com/reference/kotlin/android/os/IBinder.html#!` `https://developer.android.com/reference/kotlin/android/view/View#getApplicationWindowToken()()`

Retrieve a unique token identifying the top-level "real" window of the window that this view is attached to. That is, this is like `https://developer.android.com/reference/kotlin/android/view/View#getWindowToken()`, except if the window this view in is a panel window (attached to another containing window), then the token of the containing window is returned instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getAttributeResolutionStack(kotlin.Int)(attribute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns the ordered list of resource ID that are considered when resolving attribute values for this `https://developer.android.com/reference/kotlin/android/view/View`. The list will include layout resource ID if the View is inflated from XML. It will also include a set of explicit styles if specified in XML using `style="..."`. Finally, it will include the default styles resolved from the theme.

**Note:** this method will only return actual values if the view attribute debugging is enabled in Android developer options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` `https://developer.android.com/reference/kotlin/android/view/View#getAttributeSourceResourceMap()()`

Returns the mapping of attribute resource ID to source resource ID where the attribute value was set. Source resource ID can either be a layout resource ID, if the value was set in XML within the View tag, or a style resource ID, if the attribute was set in a style. The source resource value will be one of the resource IDs from `https://developer.android.com/reference/kotlin/android/view/View#getAttributeSourceResourceMap()`.

**Note:** this method will only return actual values if the view attribute debugging is enabled in Android developer options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` `https://developer.android.com/reference/kotlin/android/view/View#getAutofillHints()()`

Gets the hints that help an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` determine how to autofill the view with the user's data.

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)` for more info about these hints.

<br />

`https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId!` `https://developer.android.com/reference/kotlin/android/view/View#getAutofillId()()`

Gets the unique, logical identifier of this view in the activity, for autofill purposes.

The autofill id is created on demand, unless it is explicitly set by `https://developer.android.com/reference/kotlin/android/view/View#setAutofillId(android.view.autofill.AutofillId)`.

See `https://developer.android.com/reference/kotlin/android/view/View#setAutofillId(android.view.autofill.AutofillId)` for more info.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getAutofillType()()`

Describes the autofill type of this view, so an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` can create the proper `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue` when autofilling the view.

By default returns `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_NONE:kotlin.Int`, but views should override it to properly support the Autofill Framework.

<br />

`https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue?` `https://developer.android.com/reference/kotlin/android/view/View#getAutofillValue()()`

Gets the `https://developer.android.com/reference/kotlin/android/view/View`'s current autofill value.

By default returns `null`, but subclasses should override it and return an appropriate value to properly support the Autofill Framework.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/view/View#getBackground()()`

Gets the background drawable

<br />

`https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getBackgroundTintBlendMode()()`

Return the blending mode used to apply the tint to the background drawable, if specified.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getBackgroundTintList()()`

Return the tint applied to the background drawable, if specified.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getBackgroundTintMode()()`

Return the blending mode used to apply the tint to the background drawable, if specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getBaseline()()`

Return the offset of the widget's text baseline from the widget's top boundary. If this widget does not support baseline alignment, this method returns -1.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getBottom()()`

Bottom position of this view relative to its parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getBottomFadingEdgeStrength()()`

Returns the strength, or intensity, of the bottom faded edge. The strength is a value between 0.0 (no fade) and 1.0 (full fade). The default implementation returns 0.0 or 1.0 but no value in between. Subclasses should override this method to provide a smoother fade transition when scrolling occurs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getBottomPaddingOffset()()`

Amount by which to extend the bottom fading region. Called only when `https://developer.android.com/reference/kotlin/android/view/View#isPaddingOffsetRequired()` returns true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getCameraDistance()()`

Gets the distance along the Z axis from the camera to this view.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!` `https://developer.android.com/reference/kotlin/android/view/View#getClipBounds()()`

Returns a copy of the current `https://developer.android.com/reference/kotlin/android/view/View#setClipBounds(android.graphics.Rect)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getClipBounds(android.graphics.Rect)(outRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Populates an output rectangle with the clip bounds of the view, returning `true` if successful or `false` if the view's clip bounds are `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getClipToOutline()()`

Returns whether the Outline should be used to clip the contents of the View.

Note that this flag will only be respected if the View's Outline returns true from `https://developer.android.com/reference/kotlin/android/graphics/Outline.html#canClip()`.

<br />

`https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession?` `https://developer.android.com/reference/kotlin/android/view/View#getContentCaptureSession()()`

Gets the session used to notify content capture events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#getContentDescription()()`

Returns the `https://developer.android.com/reference/kotlin/android/view/View`'s content description.

**Note:** Do not override this method, as it will have no effect on the content description presented to accessibility services. You must call `https://developer.android.com/reference/kotlin/android/view/View#setContentDescription(kotlin.CharSequence)` to modify the content description.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getContentSensitivity()()`

Gets content sensitivity mode to determine whether this view displays sensitive content.

See `https://developer.android.com/reference/kotlin/android/view/View#setContentSensitivity(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/view/View#isContentSensitive()` for more info about this mode.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/view/View#getContext()()`

Returns the context the view is running in, through which it can access the current theme, resources, etc.

<br />

`https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo!` `https://developer.android.com/reference/kotlin/android/view/View#getContextMenuInfo()()`

Views should implement this if they have extra information to associate with the context menu. The return result is supplied as a parameter to the `https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo)` callback.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getDefaultFocusHighlightEnabled()()`

Returns whether this View should use a default focus highlight when it gets focused but doesn't have `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` defined in its background.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getDefaultSize(kotlin.Int,%20kotlin.Int)(size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, measureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Utility to return a default size. Uses the supplied size if the MeasureSpec imposed no constraints. Will get larger if allowed by the MeasureSpec.

<br />

`https://developer.android.com/reference/kotlin/android/view/Display!` `https://developer.android.com/reference/kotlin/android/view/View#getDisplay()()`

Gets the logical display to which the view's window has been attached.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#getDrawableState()()`

Return an array of resource IDs of the drawable states representing the current state of the view.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!` `https://developer.android.com/reference/kotlin/android/view/View#getDrawingCache()()`

Calling this method is equivalent to calling `getDrawingCache(false)`.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!` `https://developer.android.com/reference/kotlin/android/view/View#getDrawingCache(kotlin.Boolean)(autoScale: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Returns the bitmap in which this view drawing is cached. The returned bitmap is null when caching is disabled. If caching is enabled and the cache is not ready, this method will create it. Calling `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)` will not draw from the cache when the cache is enabled. To benefit from the cache, you must request the drawing cache by calling this method and draw it on screen if the returned bitmap is not null.

Note about auto scaling in compatibility mode: When auto scaling is not enabled, this method will create a bitmap of the same size as this view. Because this bitmap will be drawn scaled by the parent ViewGroup, the result on screen might show scaling artifacts. To avoid such artifacts, you should call this method by setting the auto scaling to true. Doing so, however, will generate a bitmap of a different size than the view. This implies that your application must be able to handle this size.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getDrawingCacheBackgroundColor()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getDrawingCacheQuality()()`

Returns the quality of the drawing cache.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getDrawingRect(android.graphics.Rect)(outRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Return the visible drawing bounds of your view. Fills in the output rectangle with the values from getScrollX(), getScrollY(), getWidth(), and getHeight(). These bounds do not account for any transformation properties currently set on the view, such as `https://developer.android.com/reference/kotlin/android/view/View#setScaleX(kotlin.Float)` or `https://developer.android.com/reference/kotlin/android/view/View#setRotation(kotlin.Float)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getDrawingTime()()`

Return the time at which the drawing of the view hierarchy started.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getElevation()()`

The base elevation of this view relative to its parent, in pixels.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getExplicitStyle()()`

Returns the resource ID for the style specified using `style="..."` in the `https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#`'s backing XML element or `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int` otherwise if not specified or otherwise not applicable.

Each `https://developer.android.com/reference/kotlin/android/view/View` can have an explicit style specified in the layout file. This style is used first during the `https://developer.android.com/reference/kotlin/android/view/View` attribute resolution, then if an attribute is not defined there the resource system looks at default style and theme as fallbacks.

**Note:** this method will only return actual values if the view attribute debugging is enabled in Android developer options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getFilterTouchesWhenObscured()()`

Gets whether the framework should discard touches when the view's window is obscured by another visible window at the touched location. Refer to the `https://developer.android.com/reference/kotlin/android/view/View` security documentation for more details.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getFitsSystemWindows()()`

Check for state of `https://developer.android.com/reference/kotlin/android/view/View#setFitsSystemWindows(kotlin.Boolean)`. If this method returns `true`, the default implementation of `https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect)` will be executed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getFocusable()()`

Returns the focusable setting for this view.

<br />

`https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/view/View!>!` `https://developer.android.com/reference/kotlin/android/view/View#getFocusables(kotlin.Int)(direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Find and return all focusable views that are descendants of this view, possibly including this view if it is focusable itself.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getFocusedRect(android.graphics.Rect)(r: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

When a view has focus and the user navigates away from it, the next view is searched for starting from the rectangle filled in by this method. By default, the rectangle is the `https://developer.android.com/reference/kotlin/android/view/View#getDrawingRect(android.graphics.Rect)`) of the view. However, if your view maintains some idea of internal selection, such as a cursor, or a selected row or column, you should override this method and fill in a more specific rectangle.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/view/View#getForeground()()`

Returns the drawable used as the foreground of this View. The foreground drawable, if non-null, is always drawn on top of the view's content.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getForegroundGravity()()`

Describes how the foreground is positioned.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getForegroundTintBlendMode()()`

Return the blending mode used to apply the tint to the foreground drawable, if specified.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getForegroundTintList()()`

Return the tint applied to the foreground drawable, if specified.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getForegroundTintMode()()`

Return the blending mode used to apply the tint to the foreground drawable, if specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getFrameContentVelocity()()`

Get the current velocity of the View. The value should always be greater than or equal to 0. Note that this is only valid till the next drawn frame.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getGlobalVisibleRect(android.graphics.Rect)(r: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Sets `r` to the coordinates of the non-clipped area of this view in the coordinate space of the view's root view.

See `https://developer.android.com/reference/kotlin/android/view/View#getGlobalVisibleRect(android.graphics.Rect,%20android.graphics.Point)` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getGlobalVisibleRect(android.graphics.Rect,%20android.graphics.Point)(r: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!, globalOffset: https://developer.android.com/reference/kotlin/android/graphics/Point.html#!)`

Sets `r` to the coordinates of the non-clipped area of this view in the coordinate space of the view's root view. Sets `globalOffset` to the offset of the view's x and y coordinates from the coordinate space origin, which is the top left corner of the root view irrespective of screen decorations and system UI elements.

To convert `r` to coordinates relative to the top left corner of this view (without taking view rotations into account), offset `r` by the inverse values of `globalOffset`---`r.offset(-globalOffset.x, -globalOffset.y)`---which is equivalent to calling `https://developer.android.com/reference/kotlin/android/view/View#getLocalVisibleRect(android.graphics.Rect)`.

**Note:** Do not use this method to determine the size of a window in multi-window mode; use `https://developer.android.com/reference/kotlin/android/view/WindowManager#getCurrentWindowMetrics()`.

<br />

`https://developer.android.com/reference/kotlin/android/os/Handler.html#!` `https://developer.android.com/reference/kotlin/android/view/View#getHandler()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getHandwritingBoundsOffsetBottom()()`

Return the amount of offset applied to the bottom edge of this view's handwriting bounds, in the unit of pixel.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getHandwritingBoundsOffsetLeft()()`

Return the amount of offset applied to the left edge of this view's handwriting bounds, in the unit of pixel.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getHandwritingBoundsOffsetRight()()`

Return the amount of offset applied to the right edge of this view's handwriting bounds, in the unit of pixel.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getHandwritingBoundsOffsetTop()()`

Return the amount of offset applied to the top edge of this view's handwriting bounds, in the unit of pixel.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getHandwritingDelegateFlags()()`

Returns flags configuring the handwriting delegation behavior for this delegate editor view, as set by `https://developer.android.com/reference/kotlin/android/view/View#setHandwritingDelegateFlags(kotlin.Int)`.

<br />

`https://developer.android.com/reference/kotlin/java/lang/Runnable.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getHandwritingDelegatorCallback()()`

Returns the callback set by `https://developer.android.com/reference/kotlin/android/view/View#setHandwritingDelegatorCallback(java.lang.Runnable)` which should be called when a stylus `https://developer.android.com/reference/kotlin/android/view/MotionEvent` occurs within this view's bounds. The callback should only be called from the UI thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getHasOverlappingRendering()()`

Returns the value for overlapping rendering that is used internally. This is either the value passed into `https://developer.android.com/reference/kotlin/android/view/View#forceHasOverlappingRendering(kotlin.Boolean)`, if called, or the return value of `https://developer.android.com/reference/kotlin/android/view/View#hasOverlappingRendering()`, otherwise.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getHeight()()`

Return the height of your view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getHitRect(android.graphics.Rect)(outRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Hit rectangle in parent's coordinates

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getHorizontalFadingEdgeLength()()`

Returns the size of the horizontal faded edges used to indicate that more content in this view is visible.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getHorizontalScrollbarHeight()()`

Returns the height of the horizontal scrollbar.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getHorizontalScrollbarThumbDrawable()()`

Returns the currently configured Drawable for the thumb of the horizontal scroll bar if it exists, null otherwise.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getHorizontalScrollbarTrackDrawable()()`

Returns the currently configured Drawable for the track of the horizontal scroll bar if it exists, null otherwise.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getId()()`

Returns this view's identifier.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getImportantForAccessibility()()`

Gets the mode for determining whether this View is important for accessibility. A view is important for accessibility if it fires accessibility events and if it is reported to accessibility services that query the screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getImportantForAutofill()()`

Gets the mode for determining whether this view is important for autofill.

See `https://developer.android.com/reference/kotlin/android/view/View#setImportantForAutofill(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/view/View#isImportantForAutofill()` for more info about this mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getImportantForContentCapture()()`

Gets the mode for determining whether this view is important for content capture.

See `https://developer.android.com/reference/kotlin/android/view/View#setImportantForContentCapture(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/view/View#isImportantForContentCapture()` for more info about this mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getKeepScreenOn()()`

Returns whether the screen should remain on, corresponding to the current value of `https://developer.android.com/reference/kotlin/android/view/View#KEEP_SCREEN_ON:kotlin.Int`.

<br />

`https://developer.android.com/reference/kotlin/android/view/KeyEvent.DispatcherState!` `https://developer.android.com/reference/kotlin/android/view/View#getKeyDispatcherState()()`

Return the global `https://developer.android.com/reference/kotlin/android/view/KeyEvent.DispatcherState` for this view's window. Returns null if the view is not currently attached to the window. Normally you will not need to use this directly, but just use the standard high-level event callbacks like `https://developer.android.com/reference/kotlin/android/view/View#onKeyDown(kotlin.Int,%20android.view.KeyEvent)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getLabelFor()()`

Gets the id of a view for which this view serves as a label for accessibility purposes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getLayerType()()`

Indicates what type of layer is currently associated with this view. By default a view does not have a layer, and the layer type is `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`. Refer to the documentation of `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` for more information on the different types of layers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getLayoutDirection()()`

Returns the resolved layout direction for this view.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!` `https://developer.android.com/reference/kotlin/android/view/View#getLayoutParams()()`

Get the LayoutParams associated with this view. All views should have layout parameters. These supply parameters to the *parent* of this view specifying how it should be arranged. There are many subclasses of ViewGroup.LayoutParams, and these correspond to the different subclasses of ViewGroup that are responsible for arranging their children. This method may return null if this View is not attached to a parent ViewGroup or `https://developer.android.com/reference/kotlin/android/view/View#setLayoutParams(android.view.ViewGroup.LayoutParams)` was not invoked successfully. When a View is attached to a parent ViewGroup, this method must not return null.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getLeft()()`

Left position of this view relative to its parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getLeftFadingEdgeStrength()()`

Returns the strength, or intensity, of the left faded edge. The strength is a value between 0.0 (no fade) and 1.0 (full fade). The default implementation returns 0.0 or 1.0 but no value in between. Subclasses should override this method to provide a smoother fade transition when scrolling occurs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getLeftPaddingOffset()()`

Amount by which to extend the left fading region. Called only when `https://developer.android.com/reference/kotlin/android/view/View#isPaddingOffsetRequired()` returns true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getLocalVisibleRect(android.graphics.Rect)(r: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Sets `r` to the coordinates of the non-clipped area of this view relative to the top left corner of the view.

If the view is clipped on the left or top, the left and top coordinates are offset from 0 by the clipped amount. For example, if the view is off screen 50px on the left and 30px at the top, the left and top coordinates are 50 and 30 respectively.

If the view is clipped on the right or bottom, the right and bottom coordinates are reduced by the clipped amount. For example, if the view is off screen 40px on the right and 20px at the bottom, the right coordinate is the view width - 40, and the bottom coordinate is the view height - 20.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getLocationInSurface(kotlin.IntArray)(location: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Gets the coordinates of this view in the coordinate space of the `https://developer.android.com/reference/kotlin/android/view/Surface` that contains the view.

In multiple-screen scenarios, if the surface spans multiple screens, the coordinate space of the surface also spans multiple screens.

After the method returns, the argument array contains the x and y coordinates of the view relative to the view's left and top edges, respectively.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getLocationInWindow(kotlin.IntArray)(outLocation: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)`

Gets the coordinates of this view in the coordinate space of the window that contains the view, irrespective of system decorations.

In multi-window mode, the origin of the coordinate space is the top left corner of the window that contains the view. In full screen mode, the origin is the top left corner of the device screen.

In multiple-screen scenarios, if the app spans multiple screens, the coordinate space also spans multiple screens. But if the app is restricted to a single screen, the coordinate space includes only the screen on which the app is running.

After the method returns, the argument array contains the x and y coordinates of the view relative to the view's left and top edges, respectively.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getLocationOnScreen(kotlin.IntArray)(outLocation: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)`

Gets the coordinates of this view in the coordinate space of the device screen, irrespective of system decorations and whether the system is in multi-window mode.

In multi-window mode, the coordinate space encompasses the entire device screen, ignoring the bounds of the app window. For example, if the view is in the bottom portion of a horizontal split screen, the top edge of the screen---not the top edge of the window---is the origin from which the y-coordinate is calculated.

In multiple-screen scenarios, the coordinate space can span screens. For example, if the app is spanning both screens of a dual-screen device and the view is located on the right-hand screen, the x-coordinate is calculated from the left edge of the left-hand screen to the left edge of the view. When the app is restricted to a single screen in a multiple-screen environment, the coordinate space includes only the screen on which the app is running.

After the method returns, the argument array contains the x and y coordinates of the view relative to the view's left and top edges, respectively.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#!` `https://developer.android.com/reference/kotlin/android/view/View#getMatrix()()`

The transform matrix of this view, which is calculated based on the current rotation, scale, and pivot properties.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredHeight()()`

Like `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredHeightAndState()`, but only returns the raw height component (that is the result is masked by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int`).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredHeightAndState()()`

Return the full height measurement information for this view as computed by the most recent call to `https://developer.android.com/reference/kotlin/android/view/View#measure(kotlin.Int,%20kotlin.Int)`. This result is a bit mask as defined by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_TOO_SMALL:kotlin.Int`. This should be used during measurement and layout calculations only. Use `https://developer.android.com/reference/kotlin/android/view/View#getHeight()` to see how high a view is after layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredState()()`

Return only the state bits of `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredWidthAndState()` and `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredHeightAndState()`, combined into one integer. The width component is in the regular bits `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_MASK:kotlin.Int` and the height component is at the shifted bits `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_HEIGHT_STATE_SHIFT:kotlin.Int`\>\>`https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_MASK:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredWidth()()`

Like `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredWidthAndState()`, but only returns the raw width component (that is the result is masked by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int`).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getMeasuredWidthAndState()()`

Return the full width measurement information for this view as computed by the most recent call to `https://developer.android.com/reference/kotlin/android/view/View#measure(kotlin.Int,%20kotlin.Int)`. This result is a bit mask as defined by `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_TOO_SMALL:kotlin.Int`. This should be used during measurement and layout calculations only. Use `https://developer.android.com/reference/kotlin/android/view/View#getWidth()` to see how wide a view is after layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getMinimumHeight()()`

Returns the minimum height of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getMinimumWidth()()`

Returns the minimum width of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getNextClusterForwardId()()`

Gets the id of the root of the next keyboard navigation cluster.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getNextFocusDownId()()`

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getNextFocusForwardId()()`

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getNextFocusLeftId()()`

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getNextFocusRightId()()`

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getNextFocusUpId()()`

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int`.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.OnFocusChangeListener!` `https://developer.android.com/reference/kotlin/android/view/View#getOnFocusChangeListener()()`

Returns the focus-change callback registered for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getOutlineAmbientShadowColor()()`

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider!` `https://developer.android.com/reference/kotlin/android/view/View#getOutlineProvider()()`

Returns the current `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider` of the view, which generates the Outline that defines the shape of the shadow it casts, and enables outline clipping.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getOutlineSpotShadowColor()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getOverScrollMode()()`

Returns the over-scroll mode for this view. The result will be one of `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_ALWAYS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_IF_CONTENT_SCROLLS:kotlin.Int` (allow over-scrolling only if the view content is larger than the container), or `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_NEVER:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getPaddingBottom()()`

Returns the bottom padding of this view. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getPaddingEnd()()`

Returns the end padding of this view depending on its resolved layout direction. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getPaddingLeft()()`

Returns the left padding of this view. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getPaddingRight()()`

Returns the right padding of this view. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getPaddingStart()()`

Returns the start padding of this view depending on its resolved layout direction. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getPaddingTop()()`

Returns the top padding of this view.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewParent!` `https://developer.android.com/reference/kotlin/android/view/View#getParent()()`

Gets the parent of this view. Note that the parent is a ViewParent and not necessarily a View.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewParent!` `https://developer.android.com/reference/kotlin/android/view/View#getParentForAccessibility()()`

Gets the parent for accessibility purposes. Note that the parent for accessibility is not necessary the immediate parent. It is the first predecessor that is important for accessibility.

<br />

`https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse.html#!, https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException.html#!>?` `https://developer.android.com/reference/kotlin/android/view/View#getPendingCredentialCallback()()`

Returns the callback that has previously been set up on this view through the `https://developer.android.com/reference/kotlin/android/view/View#setPendingCredentialRequest(android.credentials.GetCredentialRequest,%20android.os.OutcomeReceiver)` API. If the return value is null, that means no callback, or request, has been set on the view and no `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` flow will be invoked when this view is focused. Traditioanl autofill flows will still work, and autofillable content will still be returned through the `https://developer.android.com/reference/kotlin/android/view/View#autofill(android.view.autofill.AutofillValue)` )} API.

See `https://developer.android.com/reference/kotlin/android/view/View#setPendingCredentialRequest(android.credentials.GetCredentialRequest,%20android.os.OutcomeReceiver)` for more info.

<br />

`https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getPendingCredentialRequest()()`

Returns the `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#` associated with the view. If the return value is null, that means no request has been set on the view and no `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` flow will be invoked when this view is focused. Traditioanl autofill flows will still work, autofilling content if applicable, from the active `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` on the device.

See `https://developer.android.com/reference/kotlin/android/view/View#setPendingCredentialRequest(android.credentials.GetCredentialRequest,%20android.os.OutcomeReceiver)` for more info.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getPivotX()()`

The x location of the point around which the view is `https://developer.android.com/reference/kotlin/android/view/View#setRotation(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#setScaleX(kotlin.Float)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getPivotY()()`

The y location of the point around which the view is `https://developer.android.com/reference/kotlin/android/view/View#setRotation(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#setScaleY(kotlin.Float)`.

<br />

`https://developer.android.com/reference/kotlin/android/view/PointerIcon!` `https://developer.android.com/reference/kotlin/android/view/View#getPointerIcon()()`

Gets the mouse pointer icon for the current view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!>` `https://developer.android.com/reference/kotlin/android/view/View#getPreferKeepClearRects()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` `https://developer.android.com/reference/kotlin/android/view/View#getReceiveContentMimeTypes()()`

Returns the MIME types accepted by `https://developer.android.com/reference/kotlin/android/view/View#performReceiveContent(android.view.ContentInfo)` for this view, as configured via `https://developer.android.com/reference/kotlin/android/view/View#setOnReceiveContentListener(kotlin.Array,%20android.view.OnReceiveContentListener)`. By default returns null.

Different features (e.g. pasting from the clipboard, inserting stickers from the soft keyboard, etc) may optionally use this metadata to conditionally alter their behavior. For example, a soft keyboard may choose to hide its UI for inserting GIFs for a particular input field if the MIME types returned here for that field don't include "image/gif" or "image/\*".

Note: Comparisons of MIME types should be performed using utilities such as `https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#compareMimeTypes(kotlin.String,%20kotlin.String)` rather than simple string equality, in order to correctly handle patterns such as "text/\*", "image/\*", etc. Note that MIME type matching in the Android framework is case-sensitive, unlike formal RFC MIME types. As a result, you should always write your MIME types with lowercase letters, or use `https://developer.android.com/reference/kotlin/android/content/Intent.html#normalizeMimeType(kotlin.String)` to ensure that it is converted to lowercase.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getRequestedFrameRate()()`

Get the current preferred frame rate of the View. The value could be negative when preferred frame rate category is set instead of perferred frame rate. The frame rate category includes REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE, REQUESTED_FRAME_RATE_CATEGORY_LOW, REQUESTED_FRAME_RATE_CATEGORY_NORMAL, and REQUESTED_FRAME_RATE_CATEGORY_HIGH. Note that the frame rate value is valid as long as the View is invalidated. Please also be aware that the requested frame rate will not propagate to child views when this API is used on a ViewGroup.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!` `https://developer.android.com/reference/kotlin/android/view/View#getResources()()`

Returns the resources associated with this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getRevealOnFocusHint()()`

Returns this view's preference for reveal behavior when it gains focus.

When this method returns true for a child view requesting focus, ancestor views responding to a focus change in `https://developer.android.com/reference/kotlin/android/view/ViewParent#requestChildFocus(android.view.View,%20android.view.View)` should make a best effort to make the newly focused child fully visible to the user. When it returns false, ancestor views should preferably not disrupt scroll positioning or other properties affecting visibility to the user as part of the focus change.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getRight()()`

Right position of this view relative to its parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getRightFadingEdgeStrength()()`

Returns the strength, or intensity, of the right faded edge. The strength is a value between 0.0 (no fade) and 1.0 (full fade). The default implementation returns 0.0 or 1.0 but no value in between. Subclasses should override this method to provide a smoother fade transition when scrolling occurs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getRightPaddingOffset()()`

Amount by which to extend the right fading region. Called only when `https://developer.android.com/reference/kotlin/android/view/View#isPaddingOffsetRequired()` returns true.

<br />

`https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl?` `https://developer.android.com/reference/kotlin/android/view/View#getRootSurfaceControl()()`

The AttachedSurfaceControl itself is not a View, it is just the interface to the windowing-system object that contains the entire view hierarchy. For the root View of a given hierarchy see `https://developer.android.com/reference/kotlin/android/view/View#getRootView()`.

<br />

`https://developer.android.com/reference/kotlin/android/view/View!` `https://developer.android.com/reference/kotlin/android/view/View#getRootView()()`

Finds the topmost view in the current view hierarchy.

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowInsets!` `https://developer.android.com/reference/kotlin/android/view/View#getRootWindowInsets()()`

Provide original WindowInsets that are dispatched to the view hierarchy. The insets are only available if the view is attached.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getRotation()()`

The degrees that the view is rotated around the pivot point.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getRotationX()()`

The degrees that the view is rotated around the horizontal axis through the pivot point.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getRotationY()()`

The degrees that the view is rotated around the vertical axis through the pivot point.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getScaleX()()`

The amount that the view is scaled in x around the pivot point, as a proportion of the view's unscaled width. A value of 1, the default, means that no scaling is applied.

By default, this is 1.0f.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getScaleY()()`

The amount that the view is scaled in y around the pivot point, as a proportion of the view's unscaled height. A value of 1, the default, means that no scaling is applied.

By default, this is 1.0f.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getScrollBarDefaultDelayBeforeFade()()`

Returns the delay before scrollbars fade.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getScrollBarFadeDuration()()`

Returns the scrollbar fade duration.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getScrollBarSize()()`

Returns the scrollbar size.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getScrollBarStyle()()`

Returns the current scrollbar style.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getScrollCaptureHint()()`

Returns the current scroll capture hint for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getScrollIndicators()()`

Returns a bitmask representing the enabled scroll indicators.

For example, if the top and left scroll indicators are enabled and all other indicators are disabled, the return value will be `View.SCROLL_INDICATOR_TOP | View.SCROLL_INDICATOR_LEFT`.

To check whether the bottom scroll indicator is enabled, use the value of `(getScrollIndicators() & View.SCROLL_INDICATOR_BOTTOM) != 0`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getScrollX()()`

Return the scrolled left position of this view. This is the left edge of the displayed part of your view. You do not need to draw any pixels farther left, since those are outside of the frame of your view on screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getScrollY()()`

Return the scrolled top position of this view. This is the top edge of the displayed part of your view. You do not need to draw any pixels above it, since those are outside of the frame of your view on screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getSolidColor()()`

Override this if your view is known to always be drawn on top of a solid color background, and needs to draw fading edges. Returning a non-zero color enables the view system to optimize the drawing of the fading edges. If you do return a non-zero color, the alpha should be set to 0xFF.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getSourceLayoutResId()()`

A `https://developer.android.com/reference/kotlin/android/view/View` can be inflated from an XML layout. For such Views this method returns the resource ID of the source layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` `https://developer.android.com/reference/kotlin/android/view/View#getStateDescription()()`

Returns the `https://developer.android.com/reference/kotlin/android/view/View`'s state description.

**Note:** Do not override this method, as it will have no effect on the state description presented to accessibility services. You must call `https://developer.android.com/reference/kotlin/android/view/View#setStateDescription(kotlin.CharSequence)` to modify the state description.

<br />

`https://developer.android.com/reference/kotlin/android/animation/StateListAnimator.html#!` `https://developer.android.com/reference/kotlin/android/view/View#getStateListAnimator()()`

Returns the current StateListAnimator if exists.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getSuggestedMinimumHeight()()`

Returns the suggested minimum height that the view should use. This returns the maximum of the view's minimum height and the background's minimum height (`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#getMinimumHeight()`).

When being used in `https://developer.android.com/reference/kotlin/android/view/View#onMeasure(kotlin.Int,%20kotlin.Int)`, the caller should still ensure the returned height is within the requirements of the parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getSuggestedMinimumWidth()()`

Returns the suggested minimum width that the view should use. This returns the maximum of the view's minimum width and the background's minimum width (`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#getMinimumWidth()`).

When being used in `https://developer.android.com/reference/kotlin/android/view/View#onMeasure(kotlin.Int,%20kotlin.Int)`, the caller should still ensure the returned width is within the requirements of the parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` `https://developer.android.com/reference/kotlin/android/view/View#getSupplementalDescription()()`

Returns the `https://developer.android.com/reference/kotlin/android/view/View`'s supplemental description.

A supplemental description provides brief supplemental information for this node, such as the purpose of the node when that purpose is not conveyed within its textual representation. For example, if a dropdown select has a purpose of setting font family, the supplemental description could be "font family". If this node has children, its supplemental description serves as additional information and is not intended to replace any existing information in the subtree. This is different from the `https://developer.android.com/reference/kotlin/android/view/View#getContentDescription()` in that this description is purely supplemental while a content description may be used to replace a description for a node or its subtree that an assistive technology would otherwise compute based on other properties of the node and its descendants.

**Note:** Do not override this method, as it will have no effect on the supplemental description presented to accessibility services. You must call `https://developer.android.com/reference/kotlin/android/view/View#setSupplementalDescription(kotlin.CharSequence)` to modify the supplemental description.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!>` `https://developer.android.com/reference/kotlin/android/view/View#getSystemGestureExclusionRects()()`

Retrieve the list of areas within this view's post-layout coordinate space where the system should not intercept touch or other pointing device gestures.

Do not modify the returned list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getSystemUiVisibility()()`

Returns the last `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)` that this view has requested.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#getTag()()`

Returns this view's tag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#getTag(kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns the tag associated with this view and the specified key.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getTextAlignment()()`

Return the resolved text alignment.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getTextDirection()()`

Return the resolved text direction.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` `https://developer.android.com/reference/kotlin/android/view/View#getTooltipText()()`

Returns the view's tooltip text. **Note:** Do not override this method, as it will have no effect on the text displayed in the tooltip. You must call `https://developer.android.com/reference/kotlin/android/view/View#setTooltipText(kotlin.CharSequence)` to modify the tooltip text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getTop()()`

Top position of this view relative to its parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getTopFadingEdgeStrength()()`

Returns the strength, or intensity, of the top faded edge. The strength is a value between 0.0 (no fade) and 1.0 (full fade). The default implementation returns 0.0 or 1.0 but no value in between. Subclasses should override this method to provide a smoother fade transition when scrolling occurs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getTopPaddingOffset()()`

Amount by which to extend the top fading region. Called only when `https://developer.android.com/reference/kotlin/android/view/View#isPaddingOffsetRequired()` returns true.

<br />

`https://developer.android.com/reference/kotlin/android/view/TouchDelegate!` `https://developer.android.com/reference/kotlin/android/view/View#getTouchDelegate()()`

Gets the TouchDelegate for this View.

<br />

`https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/view/View!>!` `https://developer.android.com/reference/kotlin/android/view/View#getTouchables()()`

Find and return all touchable views that are descendants of this view, possibly including this view if it is touchable itself.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getTransitionAlpha()()`

This property is intended only for use by the Fade transition, which animates it to produce a visual translucency that does not side-effect (or get affected by) the real alpha property. This value is composited with the other alpha value (and the AlphaAnimation value, when that is present) to produce a final visual translucency result, which is what is passed into the DisplayList.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#getTransitionName()()`

Returns the name of the View to be used to identify Views in Transitions. Names should be unique in the View hierarchy.

This returns null if the View has not been given a name.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getTranslationX()()`

The horizontal location of this view relative to its `https://developer.android.com/reference/kotlin/android/view/View#getLeft()` position. This position is post-layout, in addition to wherever the object's layout placed it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getTranslationY()()`

The vertical location of this view relative to its `https://developer.android.com/reference/kotlin/android/view/View#getTop()` position. This position is post-layout, in addition to wherever the object's layout placed it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getTranslationZ()()`

The depth location of this view relative to its `https://developer.android.com/reference/kotlin/android/view/View#getElevation()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getUniqueDrawingId()()`

Get the identifier used for this view by the drawing system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getVerticalFadingEdgeLength()()`

Returns the size of the vertical faded edges used to indicate that more content in this view is visible.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getVerticalScrollbarPosition()()`

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getVerticalScrollbarThumbDrawable()()`

Returns the currently configured Drawable for the thumb of the vertical scroll bar if it exists, null otherwise.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` `https://developer.android.com/reference/kotlin/android/view/View#getVerticalScrollbarTrackDrawable()()`

Returns the currently configured Drawable for the track of the vertical scroll bar if it exists, null otherwise.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getVerticalScrollbarWidth()()`

Returns the width of the vertical scrollbar.

<br />

`https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse?` `https://developer.android.com/reference/kotlin/android/view/View#getViewTranslationResponse()()`

Returns the `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse` associated with this view. The response will be set when the translation is done then `https://developer.android.com/reference/kotlin/android/view/View#onViewTranslationResponse(android.view.translation.ViewTranslationResponse)` is called. The `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback` can use to get `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse` to display the translated information.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver!` `https://developer.android.com/reference/kotlin/android/view/View#getViewTreeObserver()()`

Returns the ViewTreeObserver for this view's hierarchy. The view tree observer can be used to get notifications when global events, like layout, happen. The returned ViewTreeObserver observer is not guaranteed to remain valid for the lifetime of this View. If the caller of this method keeps a long-lived reference to ViewTreeObserver, it should always check for the return value of `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver#isAlive()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getVisibility()()`

Returns the visibility status for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getWidth()()`

Return the width of your view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getWindowAttachCount()()`

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowId!` `https://developer.android.com/reference/kotlin/android/view/View#getWindowId()()`

Retrieve the `https://developer.android.com/reference/kotlin/android/view/WindowId` for the window this view is currently attached to.

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowInsetsController?` `https://developer.android.com/reference/kotlin/android/view/View#getWindowInsetsController()()`

Retrieves the single `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController` of the window this view is attached to.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getWindowSystemUiVisibility()()`

Returns the current system UI visibility that is currently set for the entire window. This is the combination of the `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)` values supplied by all of the views in the window.

<br />

`https://developer.android.com/reference/kotlin/android/os/IBinder.html#!` `https://developer.android.com/reference/kotlin/android/view/View#getWindowToken()()`

Retrieve a unique token identifying the window this view is attached to.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getWindowVisibility()()`

Returns the current visibility of the window this view is attached to (either `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getWindowVisibleDisplayFrame(android.graphics.Rect)(outRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Retrieve the overall visible display size in which the window this view is attached to has been positioned in. This takes into account screen decorations above the window, for both cases where the window itself is being position inside of them or the window is being placed under then and covered insets are used for the window to position its content inside. In effect, this tells you the available area where content can be placed and remain visible to users.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getX()()`

The visual x position of this view, in pixels. This is equivalent to the `https://developer.android.com/reference/kotlin/android/view/View#setTranslationX(kotlin.Float)` property plus the current `https://developer.android.com/reference/kotlin/android/view/View#getLeft()` property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getY()()`

The visual y position of this view, in pixels. This is equivalent to the `https://developer.android.com/reference/kotlin/android/view/View#setTranslationY(kotlin.Float)` property plus the current `https://developer.android.com/reference/kotlin/android/view/View#getTop()` property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View#getZ()()`

The visual z position of this view, in pixels. This is equivalent to the `https://developer.android.com/reference/kotlin/android/view/View#setTranslationZ(kotlin.Float)` property plus the current `https://developer.android.com/reference/kotlin/android/view/View#getElevation()` property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#hasExplicitFocusable()()`

Returns true if this view is focusable or if it contains a reachable View for which `https://developer.android.com/reference/kotlin/android/view/View#hasExplicitFocusable()` returns `true`. A "reachable hasExplicitFocusable()" is a view whose parents do not block descendants focus. Only `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` views for which `https://developer.android.com/reference/kotlin/android/view/View#getFocusable()` would return `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE:kotlin.Int` are considered focusable.

This method preserves the pre-`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` behavior of `https://developer.android.com/reference/kotlin/android/view/View#hasFocusable()` in that only views explicitly set focusable will cause this method to return true. A view set to `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE_AUTO:kotlin.Int` that resolves to focusable will not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#hasFocusable()()`

Returns true if this view is focusable or if it contains a reachable View for which `https://developer.android.com/reference/kotlin/android/view/View#hasFocusable()` returns `true`. A "reachable hasFocusable()" is a view whose parents do not block descendants focus. Only `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` views are considered focusable.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` views that are determined to be focusable through `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE_AUTO:kotlin.Int` will also cause this method to return `true`. Apps that declare a `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#targetSdkVersion:kotlin.Int` of earlier than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` will continue to see this method return `false` for views not explicitly marked as focusable. Use `https://developer.android.com/reference/kotlin/android/view/View#hasExplicitFocusable()` if you require the pre-`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` behavior.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#hasNestedScrollingParent()()`

Returns true if this view has a nested scrolling parent.

The presence of a nested scrolling parent indicates that this view has initiated a nested scroll and it was accepted by an ancestor view further up the view hierarchy.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#hasOnClickListeners()()`

Return whether this view has an attached OnClickListener. Returns true if there is a listener, false if there is none.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#hasOnLongClickListeners()()`

Return whether this view has an attached OnLongClickListener. Returns true if there is a listener, false if there is none.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#hasOverlappingRendering()()`

Returns whether this View has content which overlaps.

This function, intended to be overridden by specific View types, is an optimization when alpha is set on a view. If rendering overlaps in a view with alpha \< 1, that view is drawn to an offscreen buffer and then composited into place, which can be expensive. If the view has no overlapping rendering, the view can draw each primitive with the appropriate alpha value directly. An example of overlapping rendering is a TextView with a background image, such as a Button. An example of non-overlapping rendering is a TextView with no background, or an ImageView with only the foreground image. The default implementation returns true; subclasses should override if they have cases which can be optimized.

**Note:** The return value of this method is ignored if `https://developer.android.com/reference/kotlin/android/view/View#forceHasOverlappingRendering(kotlin.Boolean)` has been called on this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#hasPointerCapture()()`

Checks pointer capture status.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#hasWindowFocus()()`

Returns true if this view is in a window that currently has window focus. Note that this is not the same as the view itself having focus.

<br />

`https://developer.android.com/reference/kotlin/android/view/View!` `https://developer.android.com/reference/kotlin/android/view/View#inflate(android.content.Context,%20kotlin.Int,%20android.view.ViewGroup)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, resource: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, root: https://developer.android.com/reference/kotlin/android/view/ViewGroup#!)`

Inflate a view from an XML resource. This convenience method wraps the `https://developer.android.com/reference/kotlin/android/view/LayoutInflater` class, which provides a full range of options for view inflation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#invalidate()()`

Invalidate the whole view. If the view is visible, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)` will be called at some point in the future.

This must be called from a UI thread. To call from a non-UI thread, call `https://developer.android.com/reference/kotlin/android/view/View#postInvalidate()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#invalidate(android.graphics.Rect)(dirty: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Mark the area defined by dirty as needing to be drawn. If the view is visible, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)` will be called at some point in the future.

This must be called from a UI thread. To call from a non-UI thread, call `https://developer.android.com/reference/kotlin/android/view/View#postInvalidate()`.

**WARNING:** In API 19 and below, this method may be destructive to `dirty`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#invalidate(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(l: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, t: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Mark the area defined by the rect (l,t,r,b) as needing to be drawn. The coordinates of the dirty rect are relative to the view. If the view is visible, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)` will be called at some point in the future.

This must be called from a UI thread. To call from a non-UI thread, call `https://developer.android.com/reference/kotlin/android/view/View#postInvalidate()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#invalidateDrawable(android.graphics.drawable.Drawable)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)`

Invalidates the specified Drawable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#invalidateOutline()()`

Called to rebuild this View's Outline from its `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isAccessibilityDataSensitive()()`

Whether this view should restrict accessibility service access only to services that have the `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#isAccessibilityTool()` property set to true.

See default behavior provided by `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_AUTO:kotlin.Int`. Otherwise, returns true for `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_YES:kotlin.Int` or false for `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_DATA_SENSITIVE_NO:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isAccessibilityFocused()()`

Returns whether this View is accessibility focused.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isAccessibilityHeading()()`

Gets whether this view is a heading for accessibility purposes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isActivated()()`

Indicates the activation state of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isAttachedToWindow()()`

Returns true if this view is currently attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isAutoHandwritingEnabled()()`

Return whether the View allows automatic handwriting initiation. Returns true if automatic handwriting initiation is enabled, and vice versa.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isClickable()()`

Indicates whether this view reacts to click events or not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isContentCaptureSelfReportingEnabled()()`

Returns whether this View automatically reports its lifecycle events and layout bounds to the Content Capture Version 2.

By default, this method returns `true`, which instructs the Android View system to automatically track this view's visibility, position, layout bounds, and structural changes and report them directly to the active `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession`.

Views can override this method to return `false` to disable this automatic monitoring and take full manual control over when and how their properties are reported. This is particularly useful for Views that participate in hybrid hierarchies that can nest Views and Virtual Views bidirectionally. By disabling this behavior, the View itself can choose its own parent id and report the relative bounds to that parent in the Content Capture hierarchy.

#### Important for Content Capture Status and Self Reporting

`https://developer.android.com/reference/kotlin/android/view/View#setImportantForContentCapture(kotlin.Int)` can influence whether this View is reported to the Content Capture entirely, e.g. `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_NO:kotlin.Int` also disables self reporting. However, not being important for Content Capture influences how descendant nodes are reported. If this View were to be set as **NOT** important for Content Capture, its children will skip this View while finding their parent id and relative bounds to that parent. Therefore, if this View needs to still act as a parent to its children in Content Capture hierarchy, but needs to control how itself is reported, overriding this method and returning `false` is recommended.

**Note:** If this method returns `false`, the view is fully responsible for notifying the system about its lifecycle and property updates by calling methods such as `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyNodeAppearedOrChanged(android.view.autofill.AutofillId,%20android.view.contentcapture.ContentCaptureNodeProperties)` and `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyNodeDisappeared(android.view.autofill.AutofillId)` on the main thread.
This methods belongs to Content Capture Version 2.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isContentSensitive()()`

Returns whether this view displays sensitive content, based on the value explicitly set by `https://developer.android.com/reference/kotlin/android/view/View#setContentSensitivity(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isContextClickable()()`

Indicates whether this view reacts to context clicks or not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isCredential()()`

Gets the mode for determining whether this view is a credential.

See `https://developer.android.com/reference/kotlin/android/view/View#setIsCredential(kotlin.Boolean)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isDirty()()`

True if this view has changed since the last time being drawn.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isDrawingCacheEnabled()()`

Indicates whether the drawing cache is enabled for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isDuplicateParentStateEnabled()()`

Indicates whether this duplicates its drawable state from its parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isEnabled()()`

Returns the enabled status for this view. The interpretation of the enabled state varies by subclass.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isFocusable()()`

Returns whether this View is currently able to take focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isFocusableInTouchMode()()`

When a view is focusable, it may not want to take focus when in touch mode. For example, a button would like focus when the user is navigating via a D-pad so that the user can click on it, but once the user starts touching the screen, the button shouldn't take focus

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isFocused()()`

Returns true if this view has focus

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isFocusedByDefault()()`

Returns whether this View should receive focus when the focus is restored for the view hierarchy containing this view.

Focus gets restored for a view hierarchy when the root of the hierarchy gets added to a window or serves as a target of cluster navigation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isForceDarkAllowed()()`

See `https://developer.android.com/reference/kotlin/android/view/View#setForceDarkAllowed(kotlin.Boolean)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isHandwritingDelegate()()`

Returns whether this view has been set as a handwriting delegate by `https://developer.android.com/reference/kotlin/android/view/View#setIsHandwritingDelegate(kotlin.Boolean)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isHapticFeedbackEnabled()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isHardwareAccelerated()()`

Indicates whether this view is attached to a hardware accelerated window or not.

Even if this method returns true, it does not mean that every call to `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)` will be made with an hardware accelerated `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#`. For instance, if this view is drawn onto an offscreen `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` and its window is hardware accelerated, `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#isHardwareAccelerated()` will likely return false, and this method will return true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isHorizontalFadingEdgeEnabled()()`

Indicate whether the horizontal edges are faded when the view is scrolled horizontally.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isHorizontalScrollBarEnabled()()`

Indicate whether the horizontal scrollbar should be drawn or not. The scrollbar is not drawn by default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isHovered()()`

Returns true if the view is currently hovered.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isImportantForAccessibility()()`

Computes whether this view should be exposed for accessibility. In general, views that are interactive or provide information are exposed while views that serve only as containers are hidden.

If an ancestor of this view has importance `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int`, this method returns `false`.

Otherwise, the value is computed according to the view's `https://developer.android.com/reference/kotlin/android/view/View#getImportantForAccessibility()` value:

1. `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int`, return `false `
2. `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_YES:kotlin.Int`, return `true`
3. `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_ACCESSIBILITY_AUTO:kotlin.Int`, return `true` if view satisfies any of the following:
 - Is actionable, e.g. `https://developer.android.com/reference/kotlin/android/view/View#isClickable()`, `https://developer.android.com/reference/kotlin/android/view/View#isLongClickable()`, `https://developer.android.com/reference/kotlin/android/view/View#isContextClickable()`, `https://developer.android.com/reference/kotlin/android/view/View#isScreenReaderFocusable()`, or `https://developer.android.com/reference/kotlin/android/view/View#isFocusable()`
 - Has an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate`
 - Has an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider`
 - Has an interaction listener, e.g. `https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener`, `https://developer.android.com/reference/kotlin/android/view/View.OnKeyListener`, etc.
 - Is an accessibility live region, e.g. `https://developer.android.com/reference/kotlin/android/view/View#getAccessibilityLiveRegion()` is not `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_NONE:kotlin.Int`.
4. Has an accessibility pane title, see `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityPaneTitle(kotlin.CharSequence)`
5. Is an accessibility heading, see `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityHeading(kotlin.Boolean)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isImportantForAutofill()()`

Hints the Android System whether the `https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.ViewNode.html#` associated with this view is considered important for autofill purposes.

Generally speaking, a view is important for autofill if:

1. The view can be autofilled by an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#`.
2. The view contents can help an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` determine how other views can be autofilled.
 1. For example, view containers should typically return `false` for performance reasons (since the important info is provided by their children), but if its properties have relevant information (for example, a resource id called `credentials`, it should return `true`. On the other hand, views representing labels or editable fields should typically return `true`, but in some cases they could return `false` (for example, if they're part of a "Captcha" mechanism).
 2. The value returned by this method depends on the value returned by `https://developer.android.com/reference/kotlin/android/view/View#getImportantForAutofill()`:
 1. if it returns `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`, then it returns `true`
 2. if it returns `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int`, then it returns `false`
 3. if it returns `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int`, then it uses some simple heuristics that can return `true` in some cases (like a container with a resource id), but `false` in most.
 4. otherwise, it returns `false`.
 3. The behavior of importances depends on Android version:
 1. For `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` and below:
 1. When a view is considered important for autofill:
 1. The view might automatically trigger an autofill request when focused on.
 2. The contents of the view are included in the `https://developer.android.com/reference/kotlin/android/view/ViewStructure` used in an autofill request.
 2. On the other hand, when a view is considered not important for autofill:
 1. The view never automatically triggers autofill requests, but it can trigger a manual request through `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#requestAutofill(android.view.View)`.
 2. The contents of the view are not included in the `https://developer.android.com/reference/kotlin/android/view/ViewStructure` used in an autofill request, unless the request has the `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int` flag.
 2. For `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and above:
 1. The system uses importance, along with other view properties and other optimization factors, to determine if a view should trigger autofill on focus.
 2. The contents of `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int` views will be included in the `https://developer.android.com/reference/kotlin/android/view/ViewStructure` used in an autofill request.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isImportantForContentCapture()()`

Hints the Android System whether this view is considered important for content capture, based on the value explicitly set by `https://developer.android.com/reference/kotlin/android/view/View#setImportantForContentCapture(kotlin.Int)` and heuristics when it's `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_AUTO:kotlin.Int`.

See `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager` for more info about content capture.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isInEditMode()()`

Indicates whether this View is currently in edit mode. A View is usually in edit mode when displayed within a developer tool. For instance, if this View is being drawn by a visual user interface builder, this method should return true. Subclasses should check the return value of this method to provide different behaviors if their normal behavior might interfere with the host environment. For instance: the class spawns a thread in its constructor, the drawing code relies on device-specific features, etc. This method is usually checked in the drawing code of custom widgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isInLayout()()`

Returns whether the view hierarchy is currently undergoing a layout pass. This information is useful to avoid situations such as calling `https://developer.android.com/reference/kotlin/android/view/View#requestLayout()` during a layout pass.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isInTouchMode()()`

Returns the touch mode state associated with this view. Attached views return the touch mode state from the associated window's display. Detached views just return the default touch mode value defined in `com.android.internal.R.bool.config_defaultInTouchMode`. Touch mode is entered once the user begins interacting with the device by touch, and affects various things like whether focus highlight is always visible to the user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isKeyboardNavigationCluster()()`

Returns whether this View is a root of a keyboard navigation cluster.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isLaidOut()()`

Returns true if this view has been through at least one layout since it was last attached to or detached from a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isLayoutDirectionResolved()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isLayoutRequested()()`

Indicates whether or not this view's layout will be requested during the next hierarchy layout pass.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isLongClickable()()`

Indicates whether this view reacts to long click events or not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isNestedScrollingEnabled()()`

Returns true if nested scrolling is enabled for this view.

If nested scrolling is enabled and this View class implementation supports it, this view will act as a nested scrolling child view when applicable, forwarding data about the scroll operation in progress to a compatible and cooperating nested scrolling parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isOpaque()()`

Indicates whether this View is opaque. An opaque View guarantees that it will draw all the pixels overlapping its bounds using a fully opaque color. Subclasses of View should override this method whenever possible to indicate whether an instance is opaque. Opaque Views are treated in a special way by the View hierarchy, possibly allowing it to perform optimizations during invalidate/draw passes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isPaddingOffsetRequired()()`

If the View draws content inside its padding and enables fading edges, it needs to support padding offsets. Padding offsets are added to the fading edges to extend the length of the fade so that it covers pixels drawn inside the padding. Subclasses of this class should override this method if they need to draw content inside the padding.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isPaddingRelative()()`

Return if the padding has been set through relative values `https://developer.android.com/reference/kotlin/android/view/View#setPaddingRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` or through

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isPivotSet()()`

Returns whether or not a pivot has been set by a call to `https://developer.android.com/reference/kotlin/android/view/View#setPivotX(kotlin.Float)` or `https://developer.android.com/reference/kotlin/android/view/View#setPivotY(kotlin.Float)`. If no pivot has been set then the pivot will be the center of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isPreferKeepClear()()`

Retrieve the preference for this view to be kept clear. This is set either by `https://developer.android.com/reference/kotlin/android/view/View#setPreferKeepClear(kotlin.Boolean)` or via the attribute android.R.styleable#View_preferKeepClear.

If this is `true`, the system will ignore the Rects set by `https://developer.android.com/reference/kotlin/android/view/View#setPreferKeepClearRects(kotlin.collections.MutableList)` and try to keep the whole view clear.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isPressed()()`

Indicates whether the view is currently in pressed state. Unless `https://developer.android.com/reference/kotlin/android/view/View#setPressed(kotlin.Boolean)` is explicitly called, only clickable views can enter the pressed state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isSaveEnabled()()`

Indicates whether this view will save its state (that is, whether its `https://developer.android.com/reference/kotlin/android/view/View#onSaveInstanceState()` method will be called).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isSaveFromParentEnabled()()`

Indicates whether the entire hierarchy under this view will save its state when a state saving traversal occurs from its parent. The default is true; if false, these views will not be saved unless `https://developer.android.com/reference/kotlin/android/view/View#saveHierarchyState(android.util.SparseArray)` is called directly on this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isScreenReaderFocusable()()`

Returns whether the view should be treated as a focusable unit by screen reader accessibility tools.

**Note:** Use androidx.core.view.ViewCompat#setScreenReaderFocusable(android.view.View,boolean) for backwards-compatibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isScrollContainer()()`

Indicates whether this view is one of the set of scrollable containers in its window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isScrollbarFadingEnabled()()`

Returns true if scrollbars will fade when this view is not scrolling

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isSelected()()`

Indicates the selection state of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isShowingLayoutBounds()()`

Returns `true` when the View is attached and the system developer setting to show the layout bounds is enabled or `false` otherwise.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isShown()()`

Returns the visibility of this view and all of its ancestors

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isSoundEffectsEnabled()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isTemporarilyDetached()()`

Tells whether the `https://developer.android.com/reference/kotlin/android/view/View` is in the state between `https://developer.android.com/reference/kotlin/android/view/View#onStartTemporaryDetach()` and `https://developer.android.com/reference/kotlin/android/view/View#onFinishTemporaryDetach()`.

This method always returns `true` when called directly or indirectly from `https://developer.android.com/reference/kotlin/android/view/View#onStartTemporaryDetach()`. The return value when called directly or indirectly from `https://developer.android.com/reference/kotlin/android/view/View#onFinishTemporaryDetach()`, however, depends on the OS version.

- `true` on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`
- `false` on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N_MR1:kotlin.Int`} and later

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isTextAlignmentResolved()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isTextDirectionResolved()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isVerticalFadingEdgeEnabled()()`

Indicate whether the vertical edges are faded when the view is scrolled horizontally.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isVerticalScrollBarEnabled()()`

Indicate whether the vertical scrollbar should be drawn or not. The scrollbar is not drawn by default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#isVisibleToUserForAutofill(kotlin.Int)(virtualId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Computes whether this virtual autofill view is visible to the user.

**Note:** By default it returns `true`, but views providing a virtual hierarchy view must override it.

<br />

`https://developer.android.com/reference/kotlin/android/view/View!` `https://developer.android.com/reference/kotlin/android/view/View#keyboardNavigationClusterSearch(android.view.View,%20kotlin.Int)(currentCluster: https://developer.android.com/reference/kotlin/android/view/View!, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Find the nearest keyboard navigation cluster in the specified direction. This does not actually give focus to that cluster.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#measure(kotlin.Int,%20kotlin.Int)(widthMeasureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, heightMeasureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

This is called to find out how big a view should be. The parent supplies constraint information in the width and height parameters.

The actual measurement work of a view is performed in `https://developer.android.com/reference/kotlin/android/view/View#onMeasure(kotlin.Int,%20kotlin.Int)`, called by this method. Therefore, only `https://developer.android.com/reference/kotlin/android/view/View#onMeasure(kotlin.Int,%20kotlin.Int)` can and must be overridden by subclasses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#mergeDrawableStates(kotlin.IntArray,%20kotlin.IntArray)(baseState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!, additionalState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)`

Merge your own state values in additionalState into the base state values baseState that were returned by `https://developer.android.com/reference/kotlin/android/view/View#onCreateDrawableState(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#offsetLeftAndRight(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Offset this view's horizontal location by the specified amount of pixels.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#offsetTopAndBottom(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Offset this view's vertical location by the specified number of pixels.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onAnimationEnd()()`

Invoked by a parent ViewGroup to notify the end of the animation currently associated with this view. If you override this method, always call super.onAnimationEnd();. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onAnimationStart()()`

Invoked by a parent ViewGroup to notify the start of the animation currently associated with this view. If you override this method, always call super.onAnimationStart();. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowInsets!` `https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets)(insets: https://developer.android.com/reference/kotlin/android/view/WindowInsets!)`

Called when the view should apply `https://developer.android.com/reference/kotlin/android/view/WindowInsets` according to its internal policy.

This method should be overridden by views that wish to apply a policy different from or in addition to the default behavior. Clients that wish to force a view subtree to apply insets should call `https://developer.android.com/reference/kotlin/android/view/View#dispatchApplyWindowInsets(android.view.WindowInsets)`.

Clients may supply an `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener` to a view. If one is set it will be called during dispatch instead of this method. The listener may optionally call this method from its own implementation if it wishes to apply the view's default insets policy in addition to its own.

Implementations of this method should either return the insets parameter unchanged or a new `https://developer.android.com/reference/kotlin/android/view/WindowInsets` cloned from the supplied insets with any insets consumed that this view applied itself. This allows new inset types added in future platform versions to pass through existing implementations unchanged without being erroneously consumed.

By default if a view's `https://developer.android.com/reference/kotlin/android/view/View#setFitsSystemWindows(kotlin.Boolean)` property is set then the view will consume the system window insets and apply them as padding for the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onCancelPendingInputEvents()()`

Called as the result of a call to `https://developer.android.com/reference/kotlin/android/view/View#cancelPendingInputEvents()` on this view or a parent view.

This method is responsible for removing any pending high-level input events that were posted to the event queue to run later. Custom view classes that post their own deferred high-level events via `https://developer.android.com/reference/kotlin/android/view/View#post(java.lang.Runnable)`, `https://developer.android.com/reference/kotlin/android/view/View#postDelayed(java.lang.Runnable,%20kotlin.Long)` or `https://developer.android.com/reference/kotlin/android/os/Handler.html#` should override this method, call `super.onCancelPendingInputEvents()` and remove those callbacks as appropriate.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onCapturedPointerEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)`

Implement this method to handle captured pointer events

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onCheckIsTextEditor()()`

Check whether the called view is a text editor, in which case it would make sense to automatically display a soft input window for it. Subclasses should override this if they implement `https://developer.android.com/reference/kotlin/android/view/View#onCreateInputConnection(android.view.inputmethod.EditorInfo)` to return true if a call on that method would return a non-null InputConnection, and they are really a first-class editor that the user would normally start typing on when the go into a window containing your view.

The default implementation always returns false. This does *not* mean that its `https://developer.android.com/reference/kotlin/android/view/View#onCreateInputConnection(android.view.inputmethod.EditorInfo)` will not be called or the user can not otherwise perform edits on your view; it is just a hint to the system that this is not the primary purpose of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#!)`

Called when the current configuration of the resources being used by the application have changed. You can use this to decide when to reload resources that can changed based on orientation and other configuration characteristics. You only need to use this if you are not relying on the normal `https://developer.android.com/reference/kotlin/android/app/Activity.html#` mechanism of recreating the activity instance upon a configuration change.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onCreateContextMenu(android.view.ContextMenu)(menu: https://developer.android.com/reference/kotlin/android/view/ContextMenu!)`

Views should implement this if the view itself is going to add items to the context menu.

<br />

`https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection!` `https://developer.android.com/reference/kotlin/android/view/View#onCreateInputConnection(android.view.inputmethod.EditorInfo)(outAttrs: https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo!)`

Create a new InputConnection for an InputMethod to interact with the view. The default implementation returns null, since it doesn't support input methods. You can override this to implement such support. This is only needed for views that take focus and text input.

When implementing this, you probably also want to implement `https://developer.android.com/reference/kotlin/android/view/View#onCheckIsTextEditor()` to indicate you will return a non-null InputConnection.

Also, take good care to fill in the `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo` object correctly and in its entirety, so that the connected IME can rely on its values. For example, `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#initialSelStart:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#initialSelEnd:kotlin.Int` members must be filled in with the correct cursor position for IMEs to work correctly with your application.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onCreateViewTranslationRequest(kotlin.IntArray,%20java.util.function.Consumer)(supportedFormats: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, requestsCollector: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest!>)`

Collects a `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest` which represents the content to be translated in the view.

The default implementation does nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onCreateVirtualViewTranslationRequests(kotlin.LongArray,%20kotlin.IntArray,%20java.util.function.Consumer)(virtualIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html, supportedFormats: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, requestsCollector: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest!>)`

Collects `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest`s which represents the content to be translated for the virtual views in the host view. This is called if this view returned a virtual view structure from `https://developer.android.com/reference/kotlin/android/view/View#onProvideContentCaptureStructure(android.view.ViewStructure,%20kotlin.Int)` and the system determined that those virtual views were relevant for translation.

The default implementation does nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onDisplayHint(kotlin.Int)(hint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Gives this view a hint about whether is displayed or not. For instance, when a View moves out of the screen, it might receives a display hint indicating the view is not displayed. Applications should not *rely* on this hint as there is no guarantee that they will receive one.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onDragEvent(android.view.DragEvent)(event: https://developer.android.com/reference/kotlin/android/view/DragEvent!)`

Handles drag events sent by the system following a call to `https://developer.android.com/reference/kotlin/android/view/View#startDragAndDrop(android.content.ClipData,%20android.view.View.DragShadowBuilder,%20kotlin.Any,%20kotlin.Int)`.

The system calls this method and passes a `https://developer.android.com/reference/kotlin/android/view/DragEvent` object in response to drag and drop events. This method can then call `https://developer.android.com/reference/kotlin/android/view/DragEvent#getAction()` to determine the state of the drag and drop operation.

The default implementation returns `false` unless an `https://developer.android.com/reference/kotlin/android/view/OnReceiveContentListener` has been set for this view (see `https://developer.android.com/reference/kotlin/android/view/View#setOnReceiveContentListener(kotlin.Array,%20android.view.OnReceiveContentListener)`), in which case the default implementation does the following:

- Returns `true` for an `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_STARTED:kotlin.Int` event
- Calls `https://developer.android.com/reference/kotlin/android/view/View#performReceiveContent(android.view.ContentInfo)` for an `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int` event
- Returns `true` for an `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int` event if the `OnReceiveContentListener` consumed some or all of the content

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`

Implement this to do your drawing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onDrawForeground(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`

Draw any foreground content for this view.

Foreground content may consist of scroll bars, a `https://developer.android.com/reference/kotlin/android/view/View#setForeground(android.graphics.drawable.Drawable)` drawable or other view-specific decorations. The foreground is drawn on top of the primary view content.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onDrawScrollBars(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`

Request the drawing of the horizontal and the vertical scrollbar. The scrollbars are painted only if they have been awakened first.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onFilterTouchEventForSecurity(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)`

Filter the touch event to apply security policies.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onFinishInflate()()`

Finalize inflating a view from XML. This is called as the last phase of inflation, after all child views have been added.

Even if the subclass overrides onFinishInflate, they should always be sure to call the super method, so that we get called. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onFinishTemporaryDetach()()`

Called after `https://developer.android.com/reference/kotlin/android/view/View#onStartTemporaryDetach()` when the container is done changing the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onFocusChanged(kotlin.Boolean,%20kotlin.Int,%20android.graphics.Rect)(gainFocus: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, previouslyFocusedRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?)`

Called by the view system when the focus state of this view changes. When the focus change event is caused by directional navigation, direction and previouslyFocusedRect provide insight into where the focus is coming from. When overriding, be sure to call up through to the super class so that the standard focus handling will occur. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onGenericMotionEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)`

Implement this method to handle generic motion events.

Generic motion events describe joystick movements, hover events from mouse or stylus devices, trackpad touches, scroll wheel movements and other motion events not handled by `https://developer.android.com/reference/kotlin/android/view/View#onTouchEvent(android.view.MotionEvent)` or `https://developer.android.com/reference/kotlin/android/view/View#onTrackballEvent(android.view.MotionEvent)`. The `https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSource()` of the motion event specifies the class of input that was received. Implementations of this method must examine the bits in the source before processing the event. The following code example shows how this is done.

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

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onHoverChanged(kotlin.Boolean)(hovered: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Implement this method to handle hover state changes.

This method is called whenever the hover state changes as a result of a call to `https://developer.android.com/reference/kotlin/android/view/View#setHovered(kotlin.Boolean)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onHoverEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)`

Implement this method to handle hover events.

This method is called whenever a pointer is hovering into, over, or out of the bounds of a view and the view is not currently being touched. Hover events are represented as pointer events with action `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_ENTER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_MOVE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_EXIT:kotlin.Int`.

- The view receives a hover event with action `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_ENTER:kotlin.Int` when the pointer enters the bounds of the view.
- The view receives a hover event with action `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_MOVE:kotlin.Int` when the pointer has already entered the bounds of the view and has moved.
- The view receives a hover event with action `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_EXIT:kotlin.Int` when the pointer has exited the bounds of the view or when the pointer is about to go down due to a button click, tap, or similar user action that causes the view to be touched.

The view should implement this method to return true to indicate that it is handling the hover event, such as by changing its drawable state.

The default implementation calls `https://developer.android.com/reference/kotlin/android/view/View#setHovered(kotlin.Boolean)` to update the hovered state of the view when a hover enter or hover exit event is received, if the view is enabled and is clickable. The default implementation also sends hover accessibility events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onInitializeAccessibilityEvent(android.view.accessibility.AccessibilityEvent)(event: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent!)`

Initializes an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent` with information about this View which is the event source. In other words, the source of an accessibility event is the view whose state change triggered firing the event.

Example: Setting the password property of an event in addition to properties set by the super implementation:

```kotlin
public void onInitializeAccessibilityEvent(AccessibilityEvent event) {
      super.onInitializeAccessibilityEvent(event);
      event.setPassword(true);
  }
```

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityDelegate(android.view.View.AccessibilityDelegate)` its `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate#onInitializeAccessibilityEvent(android.view.View,%20android.view.accessibility.AccessibilityEvent)` is responsible for handling this call.

**Note:** Always call the super implementation before adding information to the event, in case the default implementation has basic information to add.
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onInitializeAccessibilityNodeInfo(android.view.accessibility.AccessibilityNodeInfo)(info: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo!)`

Initializes an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo` with information about this view. The base implementation sets:

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setParent(android.view.View)`,
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setBoundsInParent(android.graphics.Rect)`,
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setBoundsInScreen(android.graphics.Rect)`,
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setPackageName(kotlin.CharSequence)`,
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setClassName(kotlin.CharSequence)`,
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setContentDescription(kotlin.CharSequence)`,
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setEnabled(kotlin.Boolean)`,
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setClickable(kotlin.Boolean)`,
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setFocusable(kotlin.Boolean)`,
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setFocused(kotlin.Boolean)`,
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setLongClickable(kotlin.Boolean)`,
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setSelected(kotlin.Boolean)`,
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setContextClickable(kotlin.Boolean)`

<br />

Subclasses should override this method, call the super implementation, and set additional attributes.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityDelegate(android.view.View.AccessibilityDelegate)` its `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate#onInitializeAccessibilityNodeInfo(android.view.View,%20android.view.accessibility.AccessibilityNodeInfo)` is responsible for handling this call.
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onKeyDown(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)`

Default implementation of `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback#onKeyDown(kotlin.Int,%20android.view.KeyEvent)`: perform press of the view when `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_CENTER:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ENTER:kotlin.Int` is released, if the view is enabled and clickable.

Key presses in software keyboards will generally NOT trigger this listener, although some may elect to do so in some situations. Do not rely on this to catch software key presses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)`

Default implementation of `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)`: always returns false (doesn't handle the event).

Key presses in software keyboards will generally NOT trigger this listener, although some may elect to do so in some situations. Do not rely on this to catch software key presses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, repeatCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)`

Default implementation of `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent)`: always returns false (doesn't handle the event).

Key presses in software keyboards will generally NOT trigger this listener, although some may elect to do so in some situations. Do not rely on this to catch software key presses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onKeyPreIme(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)`

Handle a key event before it is processed by any input method associated with the view hierarchy. This can be used to intercept key events in special situations before the IME consumes them; a typical example would be handling the BACK key to update the application's UI instead of allowing the IME to see it and close itself. Due to a bug, this function is not called for BACK key events on Android T and U, when the IME is shown.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onKeyShortcut(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)`

Called on the focused view when a key shortcut event is not handled. Override this method to implement local key shortcuts for the View. Key shortcuts can also be implemented by setting the `https://developer.android.com/reference/kotlin/android/view/MenuItem#setShortcut(kotlin.Char,%20kotlin.Char)` property of menu items.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onKeyUp(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent!)`

Default implementation of `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback#onKeyUp(kotlin.Int,%20android.view.KeyEvent)`: perform clicking of the view when `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_CENTER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ENTER:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SPACE:kotlin.Int` is released.

Key presses in software keyboards will generally NOT trigger this listener, although some may elect to do so in some situations. Do not rely on this to catch software key presses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onMeasure(kotlin.Int,%20kotlin.Int)(widthMeasureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, heightMeasureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Measure the view and its content to determine the measured width and the measured height. This method is invoked by `https://developer.android.com/reference/kotlin/android/view/View#measure(kotlin.Int,%20kotlin.Int)` and should be overridden by subclasses to provide accurate and efficient measurement of their contents.

**CONTRACT:** When overriding this method, you *must* call `https://developer.android.com/reference/kotlin/android/view/View#setMeasuredDimension(kotlin.Int,%20kotlin.Int)` to store the measured width and height of this view. Failure to do so will trigger an `IllegalStateException`, thrown by `https://developer.android.com/reference/kotlin/android/view/View#measure(kotlin.Int,%20kotlin.Int)`. Calling the superclass' `https://developer.android.com/reference/kotlin/android/view/View#onMeasure(kotlin.Int,%20kotlin.Int)` is a valid use.

The base class implementation of measure defaults to the background size, unless a larger size is allowed by the MeasureSpec. Subclasses should override `https://developer.android.com/reference/kotlin/android/view/View#onMeasure(kotlin.Int,%20kotlin.Int)` to provide better measurements of their content.

If this method is overridden, it is the subclass's responsibility to make sure the measured height and width are at least the view's minimum height and width (`https://developer.android.com/reference/kotlin/android/view/View#getSuggestedMinimumHeight()` and `https://developer.android.com/reference/kotlin/android/view/View#getSuggestedMinimumWidth()`).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onOverScrolled(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean)(scrollX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, scrollY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, clampedX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, clampedY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called by `https://developer.android.com/reference/kotlin/android/view/View#overScrollBy(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)` to respond to the results of an over-scroll operation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onPointerCaptureChange(kotlin.Boolean)(hasCapture: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called when the window has just acquired or lost pointer capture. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onPopulateAccessibilityEvent(android.view.accessibility.AccessibilityEvent)(event: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent!)`

Called from `https://developer.android.com/reference/kotlin/android/view/View#dispatchPopulateAccessibilityEvent(android.view.accessibility.AccessibilityEvent)` giving a chance to this View to populate the accessibility event with its text content.

**Note:** This method should only be used with event.setText(). Avoid mutating other event state in this method. Instead, follow the practices described in `https://developer.android.com/reference/kotlin/android/view/View#dispatchPopulateAccessibilityEvent(android.view.accessibility.AccessibilityEvent)`. In general, put UI metadata in the node for services to easily query, than in transient events.

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

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityDelegate(android.view.View.AccessibilityDelegate)` its `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate#onPopulateAccessibilityEvent(android.view.View,%20android.view.accessibility.AccessibilityEvent)` is responsible for handling this call.

**Note:** Always call the super implementation before adding information to the event, in case the default implementation has basic information to add.
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onProvideAutofillStructure(android.view.ViewStructure,%20kotlin.Int)(structure: https://developer.android.com/reference/kotlin/android/view/ViewStructure!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Populates a `https://developer.android.com/reference/kotlin/android/view/ViewStructure` to fullfil an autofill request.

The structure should contain at least the following properties:

- Autofill id (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setAutofillId(android.view.autofill.AutofillId,%20kotlin.Int)`).
- Autofill type (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setAutofillType(kotlin.Int)`).
- Autofill value (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setAutofillValue(android.view.autofill.AutofillValue)`).
- Whether the data is sensitive (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setDataIsSensitive(kotlin.Boolean)`).

It's also recommended to set the following properties - the more properties the structure has, the higher the chances of an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` properly using the structure:

- Autofill hints (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setAutofillHints(kotlin.Array)`).
- Autofill options (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setAutofillOptions(kotlin.Array)`) when the view can only be filled with predefined values (typically used when the autofill type is `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_TYPE_LIST:kotlin.Int`).
- Resource id (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setId(kotlin.Int,%20kotlin.String,%20kotlin.String,%20kotlin.String)`).
- Class name (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setClassName(kotlin.String)`).
- Content description (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setContentDescription(kotlin.CharSequence)`).
- Visual properties such as visibility (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setVisibility(kotlin.Int)`), dimensions (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setDimens(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`), and opacity (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setOpaque(kotlin.Boolean)`).
- For views representing text fields, text properties such as the text itself (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setText(kotlin.CharSequence)`), text hints (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setHint(kotlin.CharSequence)`, input type (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setInputType(kotlin.Int)`),
- For views representing HTML nodes, its web domain (`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setWebDomain(kotlin.String)`) and HTML properties ((`https://developer.android.com/reference/kotlin/android/view/ViewStructure#setHtmlInfo(android.view.ViewStructure.HtmlInfo)`).

The default implementation of this method already sets most of these properties based on related `https://developer.android.com/reference/kotlin/android/view/View` methods (for example, the autofill id is set using `https://developer.android.com/reference/kotlin/android/view/View#getAutofillId()`, the autofill type set using `https://developer.android.com/reference/kotlin/android/view/View#getAutofillType()`, etc.), and views in the standard Android widgets library also override it to set their relevant properties (for example, `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` already sets the text properties), so it's recommended to only override this method (and call `super.onProvideAutofillStructure()`) when:

- The view contents does not include PII (Personally Identifiable Information), so it can call `https://developer.android.com/reference/kotlin/android/view/ViewStructure#setDataIsSensitive(kotlin.Boolean)` passing `false`.
- The view can only be autofilled with predefined options, so it can call `https://developer.android.com/reference/kotlin/android/view/ViewStructure#setAutofillOptions(kotlin.Array)`.

**Note:** The `left` and `top` values set in `https://developer.android.com/reference/kotlin/android/view/ViewStructure#setDimens(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` must be relative to the next `https://developer.android.com/reference/kotlin/android/view/View#isImportantForAutofill()` predecessor view included in the structure.

Views support the Autofill Framework mainly by:

- Providing the metadata defining what the view means and how it can be autofilled.
- Notifying the Android System when the view value changed by calling `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyValueChanged(android.view.View)`.
- Implementing the methods that autofill the view.

This method is responsible for the former; `https://developer.android.com/reference/kotlin/android/view/View#autofill(android.view.autofill.AutofillValue)` is responsible for the latter.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onProvideAutofillVirtualStructure(android.view.ViewStructure,%20kotlin.Int)(structure: https://developer.android.com/reference/kotlin/android/view/ViewStructure!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Populates a `https://developer.android.com/reference/kotlin/android/view/ViewStructure` containing virtual children to fullfil an autofill request.

This method should be used when the view manages a virtual structure under this view. For example, a view that draws input fields using `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`.

When implementing this method, subclasses must follow the rules below:

- Add virtual children by calling the `https://developer.android.com/reference/kotlin/android/view/ViewStructure#newChild(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/view/ViewStructure#asyncNewChild(kotlin.Int)` methods, where the `id` is an unique id identifying the children in the virtual structure.
- The children hierarchy can have multiple levels if necessary, but ideally it should exclude intermediate levels that are irrelevant for autofill; that would improve the autofill performance.
- Also implement `https://developer.android.com/reference/kotlin/android/view/View#autofill(android.util.SparseArray)` to autofill the virtual children.
- Set the autofill properties of the child structure as defined by `https://developer.android.com/reference/kotlin/android/view/View#onProvideAutofillStructure(android.view.ViewStructure,%20kotlin.Int)`, using `https://developer.android.com/reference/kotlin/android/view/ViewStructure#setAutofillId(android.view.autofill.AutofillId,%20kotlin.Int)` to set its autofill id.
- Call `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewEntered(android.view.View,%20kotlin.Int,%20android.graphics.Rect)` and/or `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewExited(android.view.View,%20kotlin.Int)` when the focused virtual child changed.
- Override `https://developer.android.com/reference/kotlin/android/view/View#isVisibleToUserForAutofill(kotlin.Int)` to allow the platform to query whether a given virtual view is visible to the user in order to support triggering save when all views of interest go away.
- Call `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyValueChanged(android.view.View,%20kotlin.Int,%20android.view.autofill.AutofillValue)` when the value of a virtual child changed.
- Call `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewVisibilityChanged(android.view.View,%20kotlin.Int,%20kotlin.Boolean)` when the visibility of a virtual child changed.
- Call `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewClicked(android.view.View,%20kotlin.Int)` when a virtual child is clicked.
- Call `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#commit()` when the autofill context of the view structure changed and the current context should be committed (for example, when the user tapped a `SUBMIT` button in an HTML page).
- Call `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#cancel()` when the autofill context of the view structure changed and the current context should be canceled (for example, when the user tapped a `CANCEL` button in an HTML page).
- Provide ways for users to manually request autofill by calling `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#requestAutofill(android.view.View,%20kotlin.Int,%20android.graphics.Rect)`.
- The `left` and `top` values set in `https://developer.android.com/reference/kotlin/android/view/ViewStructure#setDimens(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` must be relative to the next `https://developer.android.com/reference/kotlin/android/view/View#isImportantForAutofill()` predecessor view included in the structure.

Views with virtual children support the Autofill Framework mainly by:

- Providing the metadata defining what the virtual children mean and how they can be autofilled.
- Implementing the methods that autofill the virtual children.

This method is responsible for the former; `https://developer.android.com/reference/kotlin/android/view/View#autofill(android.util.SparseArray)` is responsible for the latter.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onProvideContentCaptureNodeProperties(android.view.contentcapture.ContentCaptureNodeProperties)(properties: https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties)`

Populates the properties of this `https://developer.android.com/reference/kotlin/android/view/View` for Content Capture version 2.

This method is called when a view that is eligible for content capture is initially registered and appeared on the screen, or when its properties are explicitly requested to be repopulated. The populated `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties` is subsequently sent to the intelligence service through `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyNodeAppearedOrChanged(android.view.autofill.AutofillId,%20android.view.contentcapture.ContentCaptureNodeProperties)`.

The default implementation of this method computes and sets the most relevant properties, such as the layout bounds relative to the nearest content-capture-important parent, the parent's AutofillId, and the view's content description. Subclasses overriding this method should call the super implementation (`super.onProvideContentCaptureNodeProperties(properties)`) to populate these default properties, and then modify them as appropriate.

**Note for Virtual Views:**Views that host a virtual view structure (such as web pages) must only populate the node properties representing the host view itself and return immediately. They must subsequently report virtual child node events on the main (UI) thread by calling:

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyNodeAppearedOrChanged(android.view.autofill.AutofillId,%20android.view.contentcapture.ContentCaptureNodeProperties)` when virtual nodes appear or their properties change
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyNodeDisappeared(android.view.autofill.AutofillId)` when virtual nodes disappear

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onProvideContentCaptureStructure(android.view.ViewStructure,%20kotlin.Int)(structure: https://developer.android.com/reference/kotlin/android/view/ViewStructure, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Populates a `https://developer.android.com/reference/kotlin/android/view/ViewStructure` for content capture.

This method is called after a view that is eligible for content capture (for example, if it `https://developer.android.com/reference/kotlin/android/view/View#isImportantForContentCapture()`, an intelligence service is enabled for the user, and the activity rendering the view is enabled for content capture) is laid out and is visible. The populated structure is then passed to the service through `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewAppeared(android.view.ViewStructure)`.

The default implementation of this method sets the most relevant properties based on related `https://developer.android.com/reference/kotlin/android/view/View` methods, and views in the standard Android widgets library also override it to set their relevant properties. Therefore, if overriding this method, it is recommended to call `super.onProvideContentCaptureStructure()`.

**Note:** views that manage a virtual structure under this view must populate just the node representing this view and return right away, then asynchronously report (not necessarily in the UI thread) when the children nodes appear, disappear or have their text changed by calling `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewAppeared(android.view.ViewStructure)`, `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewDisappeared(android.view.autofill.AutofillId)`, and `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewTextChanged(android.view.autofill.AutofillId,%20kotlin.CharSequence)` respectively. The structure for a child must be created using `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#newVirtualViewStructure(android.view.autofill.AutofillId,%20kotlin.Long)`, and the `autofillId` for a child can be obtained either through `childStructure.getAutofillId()` or `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#newAutofillId(android.view.autofill.AutofillId,%20kotlin.Long)`.

When the virtual view hierarchy represents a web page, you should also:

- Call `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#getContentCaptureConditions()` to infer content capture events should be generate for that URL.
- Create a new `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession` child for every HTML element that renders a new URL (like an `IFRAME`) and use that session to notify events from that subtree.

**Note:** the following methods of the `structure` will be ignored:

- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#setChildCount(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#addChildCount(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#getChildCount()`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#newChild(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#asyncNewChild(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#asyncCommit()`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#setWebDomain(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#newHtmlInfoBuilder(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#setHtmlInfo(android.view.ViewStructure.HtmlInfo)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#setDataIsSensitive(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#setAlpha(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#setElevation(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure#setTransformation(android.graphics.Matrix)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onProvideStructure(android.view.ViewStructure)(structure: https://developer.android.com/reference/kotlin/android/view/ViewStructure!)`

Called when assist structure is being retrieved from a view as part of `https://developer.android.com/reference/kotlin/android/app/Activity.html#onProvideAssistData(android.os.Bundle)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onProvideVirtualStructure(android.view.ViewStructure)(structure: https://developer.android.com/reference/kotlin/android/view/ViewStructure!)`

Called when assist structure is being retrieved from a view as part of `https://developer.android.com/reference/kotlin/android/app/Activity.html#onProvideAssistData(android.os.Bundle)` to generate additional virtual structure under this view. The default implementation uses `https://developer.android.com/reference/kotlin/android/view/View#getAccessibilityNodeProvider()` to try to generate this from the view's virtual accessibility nodes, if any. You can override this for a more optimal implementation providing this data.

<br />

`https://developer.android.com/reference/kotlin/android/view/ContentInfo?` `https://developer.android.com/reference/kotlin/android/view/View#onReceiveContent(android.view.ContentInfo)(payload: https://developer.android.com/reference/kotlin/android/view/ContentInfo)`

Implements the default behavior for receiving content for this type of view. The default view implementation is a no-op (returns the passed-in content without acting on it).

Widgets should override this method to define their default behavior for receiving content. Apps should `https://developer.android.com/reference/kotlin/android/view/View#setOnReceiveContentListener(kotlin.Array,%20android.view.OnReceiveContentListener)` to provide app-specific handling for receiving content.

See `https://developer.android.com/reference/kotlin/android/view/View#setOnReceiveContentListener(kotlin.Array,%20android.view.OnReceiveContentListener)` and `https://developer.android.com/reference/kotlin/android/view/View#performReceiveContent(android.view.ContentInfo)` for more info.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onRestoreInstanceState(android.os.Parcelable)(state: https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!)`

Hook allowing a view to re-apply a representation of its internal state that had previously been generated by `https://developer.android.com/reference/kotlin/android/view/View#onSaveInstanceState()`. This function will never be called with a null state. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onRtlPropertiesChanged(kotlin.Int)(layoutDirection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called when any RTL property (layout direction or text direction or text alignment) has been changed. Subclasses need to override this method to take care of cached information that depends on the resolved layout direction, or to inform child views that inherit their layout direction. The default implementation does nothing.

<br />

`https://developer.android.com/reference/kotlin/android/os/Parcelable.html#?` `https://developer.android.com/reference/kotlin/android/view/View#onSaveInstanceState()()`

Hook allowing a view to generate a representation of its internal state that can later be used to create a new instance with that same state. This state should only contain information that is not persistent or can not be reconstructed later. For example, you will never store your current position on screen because that will be computed again when a new instance of the view is placed in its view hierarchy.

Some examples of things you may store here: the current cursor position in a text view (but usually not the text itself since that is stored in a content provider or other persistent storage), the currently selected item in a list view. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onScreenStateChanged(kotlin.Int)(screenState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

This method is called whenever the state of the screen this view is attached to changes. A state change will usually occurs when the screen turns on or off (whether it happens automatically or the user does it manually.)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onScrollCaptureSearch(android.graphics.Rect,%20android.graphics.Point,%20java.util.function.Consumer)(localVisibleRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#, windowOffset: https://developer.android.com/reference/kotlin/android/graphics/Point.html#, targets: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget!>)`

Called when scroll capture is requested, to search for appropriate content to scroll. If applicable, this view adds itself to the provided list for consideration, subject to the flags set by `https://developer.android.com/reference/kotlin/android/view/View#setScrollCaptureHint(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onScrollChanged(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(l: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, t: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, oldl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, oldt: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

This is called in response to an internal scroll in this view (i.e., the view scrolled its own contents). This is typically as a result of `https://developer.android.com/reference/kotlin/android/view/View#scrollBy(kotlin.Int,%20kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/view/View#scrollTo(kotlin.Int,%20kotlin.Int)` having been called.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onSetAlpha(kotlin.Int)(alpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Invoked if there is a Transform that involves alpha. Subclass that can draw themselves with the specified alpha should return true, and then respect that alpha when their onDraw() is called. If this returns false then the view may be redirected to draw into an offscreen buffer to fulfill the request, which will look fine, but may be slower than if the subclass handles it internally. The default implementation returns false.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onSizeChanged(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(w: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, oldw: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, oldh: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

This is called during layout when the size of this view has changed. If you were just added to the view hierarchy, you're called with the old values of 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onStartTemporaryDetach()()`

This is called when a container is going to temporarily detach a child, with `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(android.view.View)`. It will either be followed by `https://developer.android.com/reference/kotlin/android/view/View#onFinishTemporaryDetach()` or `https://developer.android.com/reference/kotlin/android/view/View#onDetachedFromWindow()` when the container is done.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onTouchEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)`

Implement this method to handle pointer events.

This method is called to handle motion events where pointers are down on the view. For example, this could include touchscreen touches, stylus touches, or click-and-drag events from a mouse. However, it is not called for motion events that do not involve pointers being down, such as hover events or mouse scroll wheel movements.

If this method is used to detect click actions, it is recommended that the actions be performed by implementing and calling `https://developer.android.com/reference/kotlin/android/view/View#performClick()`. This will ensure consistent system behavior, including:

- obeying click sound preferences
- dispatching OnClickListener calls
- handling `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLICK:kotlin.Int` when accessibility features are enabled

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onTrackballEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)`

Implement this method to handle trackball motion events.

The *relative* movement of the trackball since the last event can be retrieve with android.view.MotionEvent#getX and android.view.MotionEvent#getY. These are normalized so that a movement of 1 corresponds to the user pressing one DPAD key (so they will often be fractional values, representing the more fine-grained movement information available from a trackball).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onViewTranslationResponse(android.view.translation.ViewTranslationResponse)(response: https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse)`

Called when the content from `https://developer.android.com/reference/kotlin/android/view/View#onCreateViewTranslationRequest(kotlin.IntArray,%20java.util.function.Consumer)` had been translated by the TranslationService. The `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse` should be saved here so that the `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse` can be used to display the translation when the system calls `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback#onShowTranslation(android.view.View)`.

The default implementation will set the ViewTranslationResponse that can be get from `https://developer.android.com/reference/kotlin/android/view/View#getViewTranslationResponse()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onVirtualViewTranslationResponses(android.util.LongSparseArray)(response: https://developer.android.com/reference/kotlin/android/util/LongSparseArray.html#<https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse!>)`

Called when the content from `https://developer.android.com/reference/kotlin/android/view/View#onCreateVirtualViewTranslationRequests(kotlin.LongArray,%20kotlin.IntArray,%20java.util.function.Consumer)` had been translated by the TranslationService.

The default implementation does nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onVisibilityAggregated(kotlin.Boolean)(isVisible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called when the user-visibility of this View is potentially affected by a change to this view itself, an ancestor view or the window this view is attached to. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onVisibilityChanged(android.view.View,%20kotlin.Int)(changedView: https://developer.android.com/reference/kotlin/android/view/View, visibility: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called when the visibility of the view or an ancestor of the view has changed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onWindowFocusChanged(kotlin.Boolean)(hasWindowFocus: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called when the window containing this view gains or loses focus. Note that this is separate from view focus: to receive key events, both your view and its window must have focus. If a window is displayed on top of yours that takes input focus, then your own window will lose focus but the view focus will remain unchanged.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onWindowSystemUiVisibilityChanged(kotlin.Int)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Override to find out when the window's requested system UI visibility has changed, that is the value returned by `https://developer.android.com/reference/kotlin/android/view/View#getWindowSystemUiVisibility()`. This is different from the callbacks received through `https://developer.android.com/reference/kotlin/android/view/View#setOnSystemUiVisibilityChangeListener(android.view.View.OnSystemUiVisibilityChangeListener)` in that this is only telling you about the local request of the window, not the actual values applied by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#onWindowVisibilityChanged(kotlin.Int)(visibility: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called when the window containing has change its visibility (between `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`). Note that this tells you whether or not your window is being made visible to the window manager; this does *not* tell you whether or not your window is obscured by other windows on the screen, even if it is itself visible.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#overScrollBy(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)(deltaX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, deltaY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, scrollX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, scrollY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, scrollRangeX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, scrollRangeY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxOverScrollX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxOverScrollY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isTouchEvent: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Scroll the view with standard behavior for scrolling beyond the normal content boundaries. Views that call this method should override `https://developer.android.com/reference/kotlin/android/view/View#onOverScrolled(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean)` to respond to the results of an over-scroll operation. Views can use this method to handle any touch or fling-based scrolling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#performAccessibilityAction(kotlin.Int,%20android.os.Bundle)(action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, arguments: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Performs the specified accessibility action on the view. For possible accessibility actions look at `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo`.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityDelegate(android.view.View.AccessibilityDelegate)` its `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate#performAccessibilityAction(android.view.View,%20kotlin.Int,%20android.os.Bundle)` is responsible for handling this call.

The default implementation will delegate `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SCROLL_BACKWARD:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SCROLL_FORWARD:kotlin.Int` to nested scrolling parents if `https://developer.android.com/reference/kotlin/android/view/View#isNestedScrollingEnabled()` on this view.

**Note:** Avoid setting accessibility focus with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ACCESSIBILITY_FOCUS:kotlin.Int`. This is intended to be controlled by screen readers. Apps changing focus can confuse screen readers, so the resulting behavior can vary by device and screen reader version.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#performClick()()`

Call this view's OnClickListener, if it is defined. Performs all normal actions associated with clicking: reporting accessibility event, playing a sound, etc.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#performContextClick()()`

Call this view's OnContextClickListener, if it is defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#performContextClick(kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Call this view's OnContextClickListener, if it is defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#performHapticFeedback(android.os.vibrator.HapticFeedbackRequest)(request: https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.html#)`

Like `https://developer.android.com/reference/kotlin/android/view/View#performHapticFeedback(kotlin.Int,%20kotlin.Int)`, but takes a `https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.html#`.

Using a `https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.html#` allows you to make more elaborate haptic feedback requests, including setting the usage type for the requested feedback.

Specifying the usage type for your feedback allows the system to understand the context of the feedback better, and tune the haptic accordingly. When not specifying the usage type for the feedback request, or when using the other performHapticFeedback APIs, the system will do a best guess of the vibration usage based on the constant.

See `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#` to learn more about vibration usages. The usage provided for this API must be of `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_CLASS_FEEDBACK:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_UNKNOWN:kotlin.Int`. Otherwise, the haptic feedback will not be played. If `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_UNKNOWN:kotlin.Int` is used, the system will do a best guess of the vibration usage based on the constant.

Note that, if you will be calling this API repeatedly and your `https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.html#` does not change across these repeated calls, it is recommended that you create, cache, and reuse the request object to avoid the costs of repeated object creation and garbage collection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#performHapticFeedback(kotlin.Int)(feedbackConstant: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

BZZZTT!!1!

Provide haptic feedback to the user for this view.

The framework will provide haptic feedback for some built in actions, such as long presses, but you may wish to provide feedback for your own widget.

The feedback will only be performed if `https://developer.android.com/reference/kotlin/android/view/View#isHapticFeedbackEnabled()` is true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#performHapticFeedback(kotlin.Int,%20kotlin.Int)(feedbackConstant: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

BZZZTT!!1!

Like `https://developer.android.com/reference/kotlin/android/view/View#performHapticFeedback(kotlin.Int)`, with additional options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#performLongClick()()`

Calls this view's OnLongClickListener, if it is defined. Invokes the context menu if the OnLongClickListener did not consume the event.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#performLongClick(kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Calls this view's OnLongClickListener, if it is defined. Invokes the context menu if the OnLongClickListener did not consume the event, anchoring it to an (x,y) coordinate.

<br />

`https://developer.android.com/reference/kotlin/android/view/ContentInfo?` `https://developer.android.com/reference/kotlin/android/view/View#performReceiveContent(android.view.ContentInfo)(payload: https://developer.android.com/reference/kotlin/android/view/ContentInfo)`

Receives the given content. If no listener is set, invokes `https://developer.android.com/reference/kotlin/android/view/View#onReceiveContent(android.view.ContentInfo)`. If a listener is `https://developer.android.com/reference/kotlin/android/view/View#setOnReceiveContentListener(kotlin.Array,%20android.view.OnReceiveContentListener)`, invokes the listener instead; if the listener returns a non-null result, invokes `https://developer.android.com/reference/kotlin/android/view/View#onReceiveContent(android.view.ContentInfo)` to handle it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#playSoundEffect(kotlin.Int)(soundConstant: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Play a sound effect for this view.

The framework will play sound effects for some built in actions, such as clicking, but you may wish to play these effects in your widget, for instance, for internal navigation.

The sound effect will only be played if sound effects are enabled by the user, and `https://developer.android.com/reference/kotlin/android/view/View#isSoundEffectsEnabled()` is true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#post(java.lang.Runnable)(action: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!)`

Causes the Runnable to be added to the message queue. The runnable will be run on the user interface thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#postDelayed(java.lang.Runnable,%20kotlin.Long)(action: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!, delayMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

Causes the Runnable to be added to the message queue, to be run after the specified amount of time elapses. The runnable will be run on the user interface thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#postInvalidate()()`

Cause an invalidate to happen on a subsequent cycle through the event loop. Use this to invalidate the View from a non-UI thread.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#postInvalidate(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Cause an invalidate of the specified area to happen on a subsequent cycle through the event loop. Use this to invalidate the View from a non-UI thread.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#postInvalidateDelayed(kotlin.Long)(delayMilliseconds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

Cause an invalidate to happen on a subsequent cycle through the event loop. Waits for the specified amount of time.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#postInvalidateDelayed(kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(delayMilliseconds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Cause an invalidate of the specified area to happen on a subsequent cycle through the event loop. Waits for the specified amount of time.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#postInvalidateOnAnimation()()`

Cause an invalidate to happen on the next animation time step, typically the next display frame.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#postInvalidateOnAnimation(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Cause an invalidate of the specified area to happen on the next animation time step, typically the next display frame.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#postOnAnimation(java.lang.Runnable)(action: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!)`

Causes the Runnable to execute on the next animation time step. The runnable will be run on the user interface thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#postOnAnimationDelayed(java.lang.Runnable,%20kotlin.Long)(action: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!, delayMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

Causes the Runnable to execute on the next animation time step, after the specified amount of time elapses. The runnable will be run on the user interface thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#refreshDrawableState()()`

Call this to force a view to update its drawable state. This will cause drawableStateChanged to be called on this view. Views that are interested in the new state should call getDrawableState.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#registerCalledFromWrongThreadListener(android.view.View.CalledFromWrongThreadListener)(listener: https://developer.android.com/reference/kotlin/android/view/View.CalledFromWrongThreadListener)`

Registers a listener that is notified when a View API is called from the wrong thread.

Most View APIs should only be called on the UI thread, and will throw a `CalledFromWrongThreadException` if they are called from the wrong thread. View APIs that throw `CalledFromWrongThreadException` will not notify registered listeners.

For certain APIs, if they are called on the wrong thread then an exception may not be thrown, subject to App Compatibility settings. Instead, applications may be notified when a call to such an API is made from the wrong thread by registering a `https://developer.android.com/reference/kotlin/android/view/View.CalledFromWrongThreadListener` using this method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#releasePointerCapture()()`

Releases the pointer capture.

If the window does not have pointer capture, this call will do nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#removeCallbacks(java.lang.Runnable)(action: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!)`

Removes the specified Runnable from the message queue.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#removeOnAttachStateChangeListener(android.view.View.OnAttachStateChangeListener)(listener: https://developer.android.com/reference/kotlin/android/view/View.OnAttachStateChangeListener!)`

Remove a listener for attach state changes. The listener will receive no further notification of window attach/detach events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#removeOnLayoutChangeListener(android.view.View.OnLayoutChangeListener)(listener: https://developer.android.com/reference/kotlin/android/view/View.OnLayoutChangeListener!)`

Remove a listener for layout changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#removeOnUnhandledKeyEventListener(android.view.View.OnUnhandledKeyEventListener)(listener: https://developer.android.com/reference/kotlin/android/view/View.OnUnhandledKeyEventListener!)`

Removes a listener which will receive unhandled `https://developer.android.com/reference/kotlin/android/view/KeyEvent`s. This must be called on the UI thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#reportAppJankStats(android.app.jank.AppJankStats)(appJankStats: https://developer.android.com/reference/kotlin/android/app/jank/AppJankStats.html#)`

Called from apps when they want to report jank stats to the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestApplyInsets()()`

Ask that a new dispatch of `https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets)` be performed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestFitSystemWindows()()`

Ask that a new dispatch of `https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect)` be performed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestFocus()()`

Call this to try to give focus to a specific view or to one of its descendants. A view will not actually take focus if it is not focusable (`https://developer.android.com/reference/kotlin/android/view/View#isFocusable()` returns false), or if it can't be focused due to other conditions (not focusable in touch mode (`https://developer.android.com/reference/kotlin/android/view/View#isFocusableInTouchMode()`) while the device is in touch mode, not visible, not enabled, or has no size). See also `https://developer.android.com/reference/kotlin/android/view/View#focusSearch(kotlin.Int)`, which is what you call to say that you have focus, and you want your parent to look for the next one. This is equivalent to calling `https://developer.android.com/reference/kotlin/android/view/View#requestFocus(kotlin.Int,%20android.graphics.Rect)` with arguments `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` and `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestFocus(kotlin.Int)(direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Call this to try to give focus to a specific view or to one of its descendants and give it a hint about what direction focus is heading. A view will not actually take focus if it is not focusable (`https://developer.android.com/reference/kotlin/android/view/View#isFocusable()` returns false), or if it is focusable and it is not focusable in touch mode (`https://developer.android.com/reference/kotlin/android/view/View#isFocusableInTouchMode()`) while the device is in touch mode. See also `https://developer.android.com/reference/kotlin/android/view/View#focusSearch(kotlin.Int)`, which is what you call to say that you have focus, and you want your parent to look for the next one. This is equivalent to calling `https://developer.android.com/reference/kotlin/android/view/View#requestFocus(kotlin.Int,%20android.graphics.Rect)` with `null` set for the previously focused rectangle.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestFocusFromTouch()()`

Call this to try to give focus to a specific view or to one of its descendants. This is a special variant of `https://developer.android.com/reference/kotlin/android/view/View#requestFocus()` that will allow views that are not focusable in touch mode to request focus when they are touched.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestLayout()()`

Call this when something has changed which has invalidated the layout of this view. This will schedule a layout pass of the view tree. This should not be called while the view hierarchy is currently in a layout pass (`https://developer.android.com/reference/kotlin/android/view/View#isInLayout()`. If layout is happening, the request may be honored at the end of the current layout pass (and then layout will run again) or after the current frame is drawn and the next layout occurs.

Subclasses which override this method should call the superclass method to handle possible request-during-layout errors correctly.
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestPointerCapture()()`

Requests pointer capture in relative mode.

Equivalent to calling `https://developer.android.com/reference/kotlin/android/view/View#requestPointerCapture(kotlin.Int)` with `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_RELATIVE:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestPointerCapture(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Requests pointer capture in the specified mode.

When the window has pointer capture, the mouse pointer icon will disappear and will not change its position. Enabling pointer capture will change the behavior of input devices in the following ways:

- Events from a mouse will be delivered with the source `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_MOUSE_RELATIVE:kotlin.Int`, and relative position changes will be available through android.view.MotionEvent#getX and android.view.MotionEvent#getY.
- Events from a touchpad (also known as a trackpad) will be delivered according to the chosen pointer capture mode. See `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_RELATIVE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#POINTER_CAPTURE_MODE_ABSOLUTE:kotlin.Int` for details.
- Events from other types of devices, such as touchscreens, will not be affected.

Pointer ballistics curves and the user's pointer speed settings will not be applied in this mode.

When pointer capture changes, connected mouse and touchpad devices may be reconfigured, and their properties (such as their sources or motion ranges) may change. Use an `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.InputDeviceListener.html#` to be notified when a device changes (which may happen after enabling or disabling pointer capture), and use `https://developer.android.com/reference/kotlin/android/view/InputDevice#getDevice(kotlin.Int)` to get the updated `https://developer.android.com/reference/kotlin/android/view/InputDevice`.

Events captured through pointer capture will be dispatched to `https://developer.android.com/reference/kotlin/android/view/View.OnCapturedPointerListener#onCapturedPointer(android.view.View,%20android.view.MotionEvent)` if an `https://developer.android.com/reference/kotlin/android/view/View.OnCapturedPointerListener` is set, and otherwise to `https://developer.android.com/reference/kotlin/android/view/View#onCapturedPointerEvent(android.view.MotionEvent)`.

If the window already has pointer capture in the same mode, this call does nothing. If it already has pointer capture in a different mode, it will transition to the new mode.

The capture may be released through `https://developer.android.com/reference/kotlin/android/view/View#releasePointerCapture()`, or will be lost automatically when the window loses focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestRectangleOnScreen(android.graphics.Rect)(rectangle: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Request that a rectangle of this view be visible on the screen, scrolling if necessary just enough.

A View should call this if it maintains some notion of which part of its content is interesting. For example, a text editing view should call this when its cursor moves.

The Rectangle passed into this method should be in the View's content coordinate space. It should not be affected by which part of the View is currently visible or its scroll position.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestRectangleOnScreen(android.graphics.Rect,%20kotlin.Boolean)(rectangle: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!, immediate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Request that a rectangle of this view be visible on the screen, scrolling if necessary just enough.

A View should call this if it maintains some notion of which part of its content is interesting. For example, a text editing view should call this when its cursor moves.

The Rectangle passed into this method should be in the View's content coordinate space. It should not be affected by which part of the View is currently visible or its scroll position.

When `immediate` is set to true, scrolling will not be animated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestRectangleOnScreen(android.graphics.Rect,%20kotlin.Boolean,%20kotlin.Int)(rectangle: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#, immediate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Request that a rectangle of this view be visible on the screen, scrolling if necessary just enough.

A View should call this if it maintains some notion of which part of its content is interesting. For example, a text editing view should call this when its cursor moves.

The Rectangle passed into this method should be in the View's content coordinate space. It should not be affected by which part of the View is currently visible or its scroll position.

When `immediate` is set to true, scrolling will not be animated.

The `source` parameter is used to differentiate behaviors of certain system features, like focus-following with display magnification, based on user preferences and the source of requests to show content on-screen. Callers are encouraged to provide one of the following request sources, when applicable, instead of using `https://developer.android.com/reference/kotlin/android/view/View#requestRectangleOnScreen(android.graphics.Rect)` or `https://developer.android.com/reference/kotlin/android/view/View#requestRectangleOnScreen(android.graphics.Rect,%20kotlin.Boolean)`:

1. `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY:kotlin.Int`
2. `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR:kotlin.Int`
3. `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestUnbufferedDispatch(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent!)`

Request unbuffered dispatch of the given stream of MotionEvents to this View. Until this View receives a corresponding `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_UP:kotlin.Int`, ask that the input system not batch `https://developer.android.com/reference/kotlin/android/view/MotionEvent`s but instead deliver them as soon as they're available. This method should only be called for touch events.

This API is not intended for most applications. Buffered dispatch provides many of benefits, and just requesting unbuffered dispatch on most MotionEvent streams will not improve your input latency. Side effects include: increased latency, jittery scrolls and inability to take advantage of system resampling. Talk to your input professional to see if `https://developer.android.com/reference/kotlin/android/view/View#requestUnbufferedDispatch(android.view.MotionEvent)` is right for you.
To receive unbuffered events for arbitrary input device source classes, use `https://developer.android.com/reference/kotlin/android/view/View#requestUnbufferedDispatch(kotlin.Int)`,

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#requestUnbufferedDispatch(kotlin.Int)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Request unbuffered dispatch of the given event source class to this view. This is similar to `https://developer.android.com/reference/kotlin/android/view/View#requestUnbufferedDispatch(android.view.MotionEvent)`, but does not automatically terminate, and allows the specification of arbitrary input source classes.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, calling this method will not result in any behavioral changes when this View is not attached to a window.

<br />

`T` `https://developer.android.com/reference/kotlin/android/view/View#requireViewById(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Finds the first descendant view with the given ID, the view itself if the ID matches `https://developer.android.com/reference/kotlin/android/view/View#getId()`, or throws an IllegalArgumentException if the ID is invalid or there is no matching view in the hierarchy.

**Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#resetPivot()()`

Clears any pivot previously set by a call to `https://developer.android.com/reference/kotlin/android/view/View#setPivotX(kotlin.Float)` or `https://developer.android.com/reference/kotlin/android/view/View#setPivotY(kotlin.Float)`. After calling this `https://developer.android.com/reference/kotlin/android/view/View#isPivotSet()` will be false and the pivot used for rotation will return to default of being centered on the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#resolveSize(kotlin.Int,%20kotlin.Int)(size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, measureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Version of `https://developer.android.com/reference/kotlin/android/view/View#resolveSizeAndState(kotlin.Int,%20kotlin.Int,%20kotlin.Int)` returning only the `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` bits of the result.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View#resolveSizeAndState(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, measureSpec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, childMeasuredState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Utility to reconcile a desired size and state, with constraints imposed by a MeasureSpec. Will take the desired size, unless a different size is imposed by the constraints. The returned value is a compound integer, with the resolved size in the `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_SIZE_MASK:kotlin.Int` bits and optionally the bit `https://developer.android.com/reference/kotlin/android/view/View#MEASURED_STATE_TOO_SMALL:kotlin.Int` set if the resulting size is smaller than the size the view wants to be.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#restoreHierarchyState(android.util.SparseArray)(container: https://developer.android.com/reference/kotlin/android/util/SparseArray.html#<https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!>!)`

Restore this view hierarchy's frozen state from the given container.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#saveAttributeDataForStyleable(android.content.Context,%20kotlin.IntArray,%20android.util.AttributeSet,%20android.content.res.TypedArray,%20kotlin.Int,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, styleable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#?, t: https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#, defStyleAttr: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, defStyleRes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Stores debugging information about attributes. This should be called in a constructor by every custom `https://developer.android.com/reference/kotlin/android/view/View` that uses a custom styleable. If the custom view does not call it, then the custom attributes used by this view will not be visible in layout inspection tools.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#saveHierarchyState(android.util.SparseArray)(container: https://developer.android.com/reference/kotlin/android/util/SparseArray.html#<https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!>!)`

Store this view hierarchy's frozen state into the given container.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#, what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, when: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

Schedules an action on a drawable to occur at a specified time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#scrollBy(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Move the scrolled position of your view. This will cause a call to `https://developer.android.com/reference/kotlin/android/view/View#onScrollChanged(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` and the view will be invalidated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#scrollTo(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the scrolled position of your view. This will cause a call to `https://developer.android.com/reference/kotlin/android/view/View#onScrollChanged(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` and the view will be invalidated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#sendAccessibilityEvent(kotlin.Int)(eventType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sends an accessibility event of the given type. If accessibility is not enabled this method has no effect. The default implementation calls `https://developer.android.com/reference/kotlin/android/view/View#onInitializeAccessibilityEvent(android.view.accessibility.AccessibilityEvent)` first to populate information about the event source (this View), then calls `https://developer.android.com/reference/kotlin/android/view/View#dispatchPopulateAccessibilityEvent(android.view.accessibility.AccessibilityEvent)` to populate the text content of the event source including its descendants, then for events type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_SCROLLED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` with subtype `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION:kotlin.Int`, throttle the events, and last calls `https://developer.android.com/reference/kotlin/android/view/ViewParent#requestSendAccessibilityEvent(android.view.View,%20android.view.accessibility.AccessibilityEvent)` on its parent to request sending of the event to interested parties.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityDelegate(android.view.View.AccessibilityDelegate)` its `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate#sendAccessibilityEvent(android.view.View,%20kotlin.Int)` is responsible for handling this call.

If this view uses `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider` to provide virtual view hierarchy rooted at this view, this method should not be called to send events from virtual children because it will populate the events with wrong information and the events should be throttled per child instead at the virtual root level. To send events from virtual children, call `https://developer.android.com/reference/kotlin/android/view/ViewParent#requestSendAccessibilityEvent(android.view.View,%20android.view.accessibility.AccessibilityEvent)` on the view's parent to request sending of the event to interested parties.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#sendAccessibilityEventUnchecked(android.view.accessibility.AccessibilityEvent)(event: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent!)`

This method behaves exactly as `https://developer.android.com/reference/kotlin/android/view/View#sendAccessibilityEvent(kotlin.Int)` but takes as an argument an empty `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent` and does not perform a check whether accessibility is enabled.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityDelegate(android.view.View.AccessibilityDelegate)` its `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate#sendAccessibilityEventUnchecked(android.view.View,%20android.view.accessibility.AccessibilityEvent)` is responsible for handling this call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityDataSensitive(kotlin.Int)(accessibilityDataSensitive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Specifies whether this view should only allow interactions from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s with the `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#isAccessibilityTool()` property set to true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityDelegate(android.view.View.AccessibilityDelegate)(delegate: https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate?)`

Sets a delegate for implementing accessibility support via composition (as opposed to inheritance). For more details, see `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate`.

**Note:** On platform versions prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, delegate methods on views in the `android.widget.*` package are called *before* host methods. This prevents certain properties such as class name from being modified by overriding `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate#onInitializeAccessibilityNodeInfo(android.view.View,%20android.view.accessibility.AccessibilityNodeInfo)`, as any changes will be overwritten by the host class.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, delegate methods are called *after* host methods, which all properties to be modified without being overwritten by the host class.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityHeading(kotlin.Boolean)(isHeading: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set if view is a heading for a section of content for accessibility purposes.

Users of some accessibility services can choose to navigate between headings instead of between paragraphs, words, etc. Apps that provide headings on sections of text can help the text navigation experience.

**Note:** Use androidx.core.view.ViewCompat#setAccessibilityHeading(android.view.View,boolean) for backwards-compatibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityLiveRegion(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the live region mode for this view. This indicates to accessibility services whether they should automatically notify the user about changes to the view's content description or text, or to the content descriptions or text of the view's children (where applicable).

Different priority levels are available:

- `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_POLITE:kotlin.Int`: Indicates that updates to the region should be presented to the user. Suitable in most cases for prominent updates within app content that don't require the user's immediate attention.
- `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_ASSERTIVE:kotlin.Int`: Indicates that updates to the region have the highest priority and should be presented to the user immediately. This may result in disruptive notifications from an accessibility service, which may potentially interrupt other feedback or user actions, so it should generally be used only for critical, time-sensitive information.
- `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_NONE:kotlin.Int`: Disables change announcements (the default for most views).

Examples:

- Selecting an option in a dropdown menu updates a panel below with the updated content. This panel may be marked as a live region with `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_POLITE:kotlin.Int` to notify users of the change. A screen reader may queue changes as announcements that don't disrupt ongoing speech.
- An emergency alert may be marked with `https://developer.android.com/reference/kotlin/android/view/View#ACCESSIBILITY_LIVE_REGION_ASSERTIVE:kotlin.Int` to immediately inform users of the emergency.

For error notifications, like an "incorrect password" warning in a login screen, views should send a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` `AccessibilityEvent` with a content change type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_ERROR:kotlin.Int` and set `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setError(kotlin.CharSequence)`. Custom widgets should provide error-setting methods that support accessibility. For example, use `https://developer.android.com/reference/kotlin/android/widget/TextView.html#setError(kotlin.CharSequence)` instead of explicitly sending events.

Don't use live regions for frequently-updating UI elements (e.g., progress bars), as this can overwhelm the user with feedback from accessibility services. If necessary, use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setMinDurationBetweenContentChanges(java.time.Duration)` to throttle feedback and reduce disruptions.

**Note:** Use androidx.core.view.ViewCompat#setAccessibilityLiveRegion(android.view.View,int) for backwards-compatibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityPaneTitle(kotlin.CharSequence)(accessibilityPaneTitle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)`

Visually distinct portion of a window with window-like semantics are considered panes for accessibility purposes. One example is the content view of a large fragment that is replaced. In order for accessibility services to understand a pane's window-like behavior, panes should have descriptive titles. Views with pane titles produce `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int`s when they appear, disappear, or change title.

When transitioning from one Activity to another, instead of using `setAccessibilityPaneTitle()`, set a descriptive title for its window by using `android:label` for the matching Activity entry in your application's manifest or updating the title at runtime with `https://developer.android.com/reference/kotlin/android/app/Activity.html#setTitle(kotlin.CharSequence)`.

**Note:** Use androidx.core.view.ViewCompat#setAccessibilityPaneTitle(android.view.View,java.lang.CharSequence) for backwards-compatibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityTraversalAfter(kotlin.Int)(afterId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the id of a view that screen readers are requested to visit before this view.

For example, if view B should be visited after A, with B.setAccessibilityTraversalAfter(A), then this requests that screen readers visit and traverse view A before visiting view B.

**Note:** Views are visited in the order determined by the screen reader. Avoid explicitly manipulating focus order, as this may result in inconsistent user experiences between apps. Instead, use other semantics, such as restructuring the view hierarchy layout, to communicate order.

Setting this view to be after a view that is not important for accessibility, or if this view is not important for accessibility, means this method will have no effect if the service is not aware of unimportant views.

To avoid a risk of loops, set clear relationships between views. For example, if focus order should be B -\> A, and B.setAccessibilityTraversalBefore(A), then also call A.setAccessibilityTraversalAfter(B).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityTraversalBefore(kotlin.Int)(beforeId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the id of a view that screen readers are requested to visit after this view.

For example, if view B should be visited before view A, with B.setAccessibilityTraversalBefore(A), this requests that screen readers visit and traverse view B before visiting view A.

**Note:** Views are visited in the order determined by the screen reader. Avoid explicitly manipulating focus order, as this may result in inconsistent user experiences between apps. Instead, use other semantics, such as restructuring the view hierarchy layout, to communicate order.

Setting this view to be after a view that is not important for accessibility, or if this view is not important for accessibility, means this method will have no effect if the service is not aware of unimportant views.

To avoid a risk of loops, set clear relationships between views. For example, if focus order should be B -\> A, and B.setAccessibilityTraversalBefore(A), then also call A.setAccessibilityTraversalAfter(B).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setActivated(kotlin.Boolean)(activated: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Changes the activated state of this view. A view can be activated or not. Note that activation is not the same as selection. Selection is a transient property, representing the view (hierarchy) the user is currently interacting with. Activation is a longer-term state that the user can move views in and out of. For example, in a list view with single or multiple selection enabled, the views in the current selection set are activated. (Um, yeah, we are deeply sorry about the terminology here.) The activated state is propagated down to children of the view it is set on.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAllowClickWhenDisabled(kotlin.Boolean)(clickableWhenDisabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Enables or disables click events for this view when disabled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAllowedHandwritingDelegatePackage(kotlin.String)(allowedPackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Specifies that this view may act as a handwriting initiation delegator for a delegate editor view from the specified package. If this method is not called, delegators may only be used to initiate handwriting mode for a delegate editor view from the same package as the delegator view. This method allows specifying a different trusted package which may contain a delegate editor view linked to this delegator view.

This method has no effect unless `https://developer.android.com/reference/kotlin/android/view/View#setHandwritingDelegatorCallback(java.lang.Runnable)` is also called to configure this view to act as a handwriting delegator.

If this method is called on the delegator view, then `https://developer.android.com/reference/kotlin/android/view/View#setAllowedHandwritingDelegatorPackage(kotlin.String)` should also be called on the delegate editor view.

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

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAllowedHandwritingDelegatorPackage(kotlin.String)(allowedPackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Specifies that a view from the specified package may act as a handwriting delegator for this delegate editor view. If this method is not called, only views from the same package as this delegate editor view may act as a handwriting delegator. This method allows specifying a different trusted package which may contain a delegator view linked to this delegate editor view.

This method has no effect unless `https://developer.android.com/reference/kotlin/android/view/View#setIsHandwritingDelegate(kotlin.Boolean)` is also called to configure this view to act as a handwriting delegate.

If this method is called on the delegate editor view, then `https://developer.android.com/reference/kotlin/android/view/View#setAllowedHandwritingDelegatePackage(kotlin.String)` should also be called on the delegator view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAlpha(kotlin.Float)(alpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the opacity of the view to a value from 0 to 1, where 0 means the view is completely transparent and 1 means the view is completely opaque.

**Note:** setting alpha to a translucent value (0 \< alpha \< 1) can have significant performance implications, especially for large views. It is best to use the alpha property sparingly and transiently, as in the case of fading animations.

For a view with a frequently changing alpha, such as during a fading animation, it is strongly recommended for performance reasons to either override `https://developer.android.com/reference/kotlin/android/view/View#hasOverlappingRendering()` to return `false` if appropriate, or setting a `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` on the view for the duration of the animation. On versions `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int` and below, the default path for rendering an unlayered View with alpha could add multiple milliseconds of rendering cost, even for simple or small views. Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int` is automatically applied to the view at the rendering level.

If this view overrides `https://developer.android.com/reference/kotlin/android/view/View#onSetAlpha(kotlin.Int)` to return true, then this view is responsible for applying the opacity itself.

On versions `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int` and below, note that if the view is backed by a `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` and is associated with a `https://developer.android.com/reference/kotlin/android/view/View#setLayerPaint(android.graphics.Paint)`, setting an alpha value less than 1.0 will supersede the alpha of the layer paint.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, setting a translucent alpha value will clip a View to its bounds, unless the View returns `false` from `https://developer.android.com/reference/kotlin/android/view/View#hasOverlappingRendering()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAnimation(android.view.animation.Animation)(animation: https://developer.android.com/reference/kotlin/android/view/animation/Animation!)`

Sets the next animation to play for this view. If you want the animation to play immediately, use `https://developer.android.com/reference/kotlin/android/view/View#startAnimation(android.view.animation.Animation)` instead. This method provides allows fine-grained control over the start time and invalidation, but you must make sure that 1) the animation has a start time set, and 2) the view's parent (which controls animations on its children) will be invalidated when the animation is supposed to start.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAnimationMatrix(android.graphics.Matrix)(matrix: https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#?)`

Changes the transformation matrix on the view. This is used in animation frameworks, such as `https://developer.android.com/reference/kotlin/android/transition/Transition.html#`. When the animation finishes, the matrix should be cleared by calling this method with `null` as the matrix parameter. Application developers should use transformation methods like `https://developer.android.com/reference/kotlin/android/view/View#setRotation(kotlin.Float)`, `https://developer.android.com/reference/kotlin/android/view/View#setScaleX(kotlin.Float)`, `https://developer.android.com/reference/kotlin/android/view/View#setScaleX(kotlin.Float)`, `https://developer.android.com/reference/kotlin/android/view/View#setTranslationX(kotlin.Float)`} and `https://developer.android.com/reference/kotlin/android/view/View#setTranslationY(kotlin.Float)` (float)}} instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAutoHandwritingEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set whether this view enables automatic handwriting initiation. For a view with an active `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection`, if auto handwriting is enabled then stylus movement within its view boundary will automatically trigger the handwriting mode. Check `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)` for more details about handwriting mode. If the View wants to initiate handwriting mode by itself, it can set this field to `false` and call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)` when there is stylus movement detected. Note that this attribute has no effect on the View's children. For example, if a `https://developer.android.com/reference/kotlin/android/view/ViewGroup#` disables auto handwriting but its children set auto handwriting to true, auto handwriting will still work for the children, and vice versa.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAutofillHints(kotlin.String)(vararg autofillHints: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Sets the hints that help an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` determine how to autofill the view with the user's data.

Typically, there is only one way to autofill a view, but there could be more than one. For example, if the application accepts either an username or email address to identify an user.

These hints are not validated by the Android System, but passed "as is" to the service. Hence, they can have any value, but it's recommended to use the `AUTOFILL_HINT_` constants such as: `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_USERNAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_PASSWORD:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_EMAIL_ADDRESS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_NAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_PHONE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_POSTAL_ADDRESS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_POSTAL_CODE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_NUMBER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH:kotlin.String` or `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setAutofillId(android.view.autofill.AutofillId)(id: https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId?)`

Sets the unique, logical identifier of this view in the activity, for autofill purposes.

The autofill id is created on demand, and this method should only be called when a view is reused after `https://developer.android.com/reference/kotlin/android/view/View#dispatchProvideAutofillStructure(android.view.ViewStructure,%20kotlin.Int)` is called, as that method creates a snapshot of the view that is passed along to the autofill service.

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

NOTE: If this view is a descendant of an `https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#`, the system may reset its autofill id when this view is recycled. If the autofill ids need to be stable, they should be set again in `https://developer.android.com/reference/kotlin/android/widget/Adapter.html#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setBackdropRenderEffect(android.graphics.RenderEffect)(renderEffect: https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#?)`

Configure the `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#` to apply to the backdrop contents of this View. This will apply a visual effect to the result of the backdrop contents of this View before it is drawn. For example if `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#createBlurEffect(kotlin.Float,%20kotlin.Float,%20android.graphics.RenderEffect,%20android.graphics.Shader.TileMode)` is provided, the previous content behind this View will be blurred before this View is drawn.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setBackground(android.graphics.drawable.Drawable)(background: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)`

Set the background to a given Drawable, or remove the background. If the background has padding, this View's padding is set to the background's padding. However, when a background is removed, this View's padding isn't touched. If setting the padding is desired, please use `https://developer.android.com/reference/kotlin/android/view/View#setPadding(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setBackgroundColor(kotlin.Int)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the background color for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setBackgroundDrawable(android.graphics.drawable.Drawable)(background: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setBackgroundResource(kotlin.Int)(resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the background to a given resource. The resource should refer to a Drawable object or 0 to remove the background.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setBackgroundTintBlendMode(android.graphics.BlendMode)(blendMode: https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#?)`

Specifies the blending mode used to apply the tint specified by `https://developer.android.com/reference/kotlin/android/view/View#setBackgroundTintList(android.content.res.ColorStateList)`} to the background drawable. The default mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setBackgroundTintList(android.content.res.ColorStateList)(tint: https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?)`

Applies a tint to the background drawable. Does not modify the current tint mode, which is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#` by default.

Subsequent calls to `https://developer.android.com/reference/kotlin/android/view/View#setBackground(android.graphics.drawable.Drawable)` will automatically mutate the drawable and apply the specified tint and tint mode using `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#setTintList(android.content.res.ColorStateList)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setBackgroundTintMode(android.graphics.PorterDuff.Mode)(tintMode: https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#?)`

Specifies the blending mode used to apply the tint specified by `https://developer.android.com/reference/kotlin/android/view/View#setBackgroundTintList(android.content.res.ColorStateList)`} to the background drawable. The default mode is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setBottom(kotlin.Int)(bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the bottom position of this view relative to its parent. This method is meant to be called by the layout system and should not generally be called otherwise, because the property may be changed at any time by the layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setCameraDistance(kotlin.Float)(distance: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the distance along the Z axis (orthogonal to the X/Y plane on which views are drawn) from the camera to this view. The camera's distance affects 3D transformations, for instance rotations around the X and Y axis. If the rotationX or rotationY properties are changed and this view is large (more than half the size of the screen), it is recommended to always use a camera distance that's greater than the height (X axis rotation) or the width (Y axis rotation) of this view.

The distance of the camera from the view plane can have an affect on the perspective distortion of the view when it is rotated around the x or y axis. For example, a large distance will result in a large viewing angle, and there will not be much perspective distortion of the view as it rotates. A short distance may cause much more perspective distortion upon rotation, and can also result in some drawing artifacts if the rotated view ends up partially behind the camera (which is why the recommendation is to use a distance at least as far as the size of the view, if the view is to be rotated.)

The distance is expressed in "depth pixels." The default distance depends on the screen density. For instance, on a medium density display, the default distance is 1280. On a high density display, the default distance is 1920.

If you want to specify a distance that leads to visually consistent results across various densities, use the following formula:

```kotlin
float scale = context.getResources().getDisplayMetrics().density;
  view.setCameraDistance(distance * scale);
  
```

The density scale factor of a high density display is 1.5, and 1920 = 1280 \* 1.5.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setClickable(kotlin.Boolean)(clickable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Enables or disables click events for this view. When a view is clickable it will change its state to "pressed" on every click. Subclasses should set the view clickable to visually react to user's clicks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setClipBounds(android.graphics.Rect)(clipBounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Sets a rectangular area on this view to which the view will be clipped when it is drawn. Setting the value to null will remove the clip bounds and the view will draw normally, using its full bounds.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setClipToOutline(kotlin.Boolean)(clipToOutline: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether the View's Outline should be used to clip the contents of the View.

Only a single non-rectangular clip can be applied on a View at any time. Circular clips from a `https://developer.android.com/reference/kotlin/android/view/ViewAnimationUtils#createCircularReveal(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float)` animation take priority over Outline clipping, and child Outline clipping takes priority over Outline clipping done by a parent.

Note that this flag will only be respected if the View's Outline returns true from `https://developer.android.com/reference/kotlin/android/graphics/Outline.html#canClip()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setContentCaptureSession(android.view.contentcapture.ContentCaptureSession)(contentCaptureSession: https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession?)`

Sets the (optional) `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession` associated with this view.

This method should be called when you need to associate a `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext` to the content capture events associated with this view or its view hierarchy (if it's a `https://developer.android.com/reference/kotlin/android/view/ViewGroup#`).

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

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setContentDescription(kotlin.CharSequence)(contentDescription: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)`

Sets the `https://developer.android.com/reference/kotlin/android/view/View`'s content description.

A content description briefly describes the view and is primarily used for accessibility support to determine how a view should be presented to the user. In the case of a view with no textual representation, such as `https://developer.android.com/reference/kotlin/android/widget/ImageButton.html#`, a useful content description explains what the view does. For example, an image button with a phone icon that is used to place a call may use "Call" as its content description. An image of a floppy disk that is used to save a file may use "Save".

This should omit role or state. Role refers to the kind of user-interface element the View is, such as a Button or Checkbox. State refers to a frequently changing property of the View, such as an On/Off state of a button or the audio level of a volume slider.

Content description updates are not frequent, and are used when the semantic content - not the state - of the element changes. For example, a Play button might change to a Pause button during music playback.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setContentSensitivity(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets content sensitivity mode to determine whether this view displays sensitive content (e.g. username, password etc.). The system will improve user privacy i.e. hide content drawn by a sensitive view from screen sharing and recording.

The window hosting a sensitive view will be marked as secure during an active media projection session. This would be equivalent to applying `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#FLAG_SECURE:kotlin.Int` to the window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setContextClickable(kotlin.Boolean)(contextClickable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Enables or disables context clicking for this view. This event can launch the listener.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setDefaultFocusHighlightEnabled(kotlin.Boolean)(defaultFocusHighlightEnabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether this View should use a default focus highlight when it gets focused but doesn't have `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` defined in its background.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setDrawingCacheBackgroundColor(kotlin.Int)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Setting a solid background color for the drawing cache's bitmaps will improve performance and memory usage. Note, though that this should only be used if this view will always be drawn on top of a solid color.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setDrawingCacheEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Enables or disables the drawing cache. When the drawing cache is enabled, the next call to `https://developer.android.com/reference/kotlin/android/view/View#getDrawingCache()` or `https://developer.android.com/reference/kotlin/android/view/View#buildDrawingCache()` will draw the view in a bitmap. Calling `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)` will not draw from the cache when the cache is enabled. To benefit from the cache, you must request the drawing cache by calling `https://developer.android.com/reference/kotlin/android/view/View#getDrawingCache()` and draw it on screen if the returned bitmap is not null.

Enabling the drawing cache is similar to `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` when hardware acceleration is turned off. When hardware acceleration is turned on, enabling the drawing cache has no effect on rendering because the system uses a different mechanism for acceleration which ignores the flag. If you want to use a Bitmap for the view, even when hardware acceleration is enabled, see `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` for information on how to enable software and hardware layers.

This API can be used to manually generate a bitmap copy of this view, by setting the flag to `true` and calling `https://developer.android.com/reference/kotlin/android/view/View#getDrawingCache()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setDrawingCacheQuality(kotlin.Int)(quality: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the drawing cache quality of this view. This value is used only when the drawing cache is enabled

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setDuplicateParentStateEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Enables or disables the duplication of the parent's state into this view. When duplication is enabled, this view gets its drawable state from its parent rather than from its own internal properties.

Note: in the current implementation, setting this property to true after the view was added to a ViewGroup might have no effect at all. This property should always be used from XML or set to true before adding this view to a ViewGroup.

Note: if this view's parent addStateFromChildren property is enabled and this property is enabled, an exception will be thrown.

Note: if the child view uses and updates additional states which are unknown to the parent, these states should not be affected by this method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setElevation(kotlin.Float)(elevation: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the base elevation of this view, in pixels.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set the enabled state of this view. The interpretation of the enabled state varies by subclass.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setFadingEdgeLength(kotlin.Int)(length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the size of the faded edge used to indicate that more content in this view is available. Will not change whether the fading edge is enabled; use `https://developer.android.com/reference/kotlin/android/view/View#setVerticalFadingEdgeEnabled(kotlin.Boolean)` or `https://developer.android.com/reference/kotlin/android/view/View#setHorizontalFadingEdgeEnabled(kotlin.Boolean)` to enable the fading edge for the vertical or horizontal fading edges.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setFilterTouchesWhenObscured(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether the framework should discard touches when the view's window is obscured by another visible window at the touched location. Refer to the `https://developer.android.com/reference/kotlin/android/view/View` security documentation for more details.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setFitsSystemWindows(kotlin.Boolean)(fitSystemWindows: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether or not this view should account for system screen decorations such as the status bar and inset its content; that is, controlling whether the default implementation of `https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect)` will be executed. See that method for more details.

Note that if you are providing your own implementation of `https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect)`, then there is no need to set this flag to true -- your implementation will be overriding the default implementation that checks this flag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setFocusable(kotlin.Boolean)(focusable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set whether this view can receive the focus.

Setting this to false will also ensure that this view is not focusable in touch mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setFocusable(kotlin.Int)(focusable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets whether this view can receive focus.

Setting this to `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLE_AUTO:kotlin.Int` tells the framework to determine focusability automatically based on the view's interactivity. This is the default.

Setting this to NOT_FOCUSABLE will ensure that this view is also not focusable in touch mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setFocusableInTouchMode(kotlin.Boolean)(focusableInTouchMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set whether this view can receive focus while in touch mode. Setting this to true will also ensure that this view is focusable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setFocusedByDefault(kotlin.Boolean)(isFocusedByDefault: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether this View should receive focus when the focus is restored for the view hierarchy containing this view.

Focus gets restored for a view hierarchy when the root of the hierarchy gets added to a window or serves as a target of cluster navigation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setForceDarkAllowed(kotlin.Boolean)(allow: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether or not to allow force dark to apply to this view. Setting this to false will disable the auto-dark feature on everything this view draws, including any descendants. Setting this to true will allow this view to be automatically made dark, however a value of 'true' will not override any 'false' value in its parent chain nor will it prevent any 'false' in any of its children. The default behavior of force dark is also influenced by the Theme's `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_isLightTheme:kotlin.Int` attribute. If a theme is isLightTheme="false", then force dark is globally disabled for that theme.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setForeground(android.graphics.drawable.Drawable)(foreground: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)`

Supply a Drawable that is to be rendered on top of all of the content in the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setForegroundGravity(kotlin.Int)(gravity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Describes how the foreground is positioned. Defaults to START and TOP.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setForegroundTintBlendMode(android.graphics.BlendMode)(blendMode: https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#?)`

Specifies the blending mode used to apply the tint specified by `https://developer.android.com/reference/kotlin/android/view/View#setForegroundTintList(android.content.res.ColorStateList)`} to the background drawable. The default mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setForegroundTintList(android.content.res.ColorStateList)(tint: https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?)`

Applies a tint to the foreground drawable. Does not modify the current tint mode, which is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#` by default.

Subsequent calls to `https://developer.android.com/reference/kotlin/android/view/View#setForeground(android.graphics.drawable.Drawable)` will automatically mutate the drawable and apply the specified tint and tint mode using `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#setTintList(android.content.res.ColorStateList)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setForegroundTintMode(android.graphics.PorterDuff.Mode)(tintMode: https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#?)`

Specifies the blending mode used to apply the tint specified by `https://developer.android.com/reference/kotlin/android/view/View#setForegroundTintList(android.content.res.ColorStateList)`} to the background drawable. The default mode is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setFrameContentVelocity(kotlin.Float)(pixelsPerSecond: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Set the current velocity of the View, we only track positive value. We will use the velocity information to adjust the frame rate when applicable. For example, we could potentially lower the frame rate when the velocity of a fling gesture becomes slower. Note that this is only valid till the next drawn frame.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setHandwritingBoundsOffsets(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)(offsetLeft: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, offsetTop: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, offsetRight: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, offsetBottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Set the amount of offset applied to this view's stylus handwriting bounds. A positive offset will offset the edge outwards.The base handwriting bounds of a view is its visible bounds. The handwriting bounds offsets are applied to the base handwriting bounds to determine the final handwriting bounds.

This method is mainly used to enlarge the view's handwriting bounds for a better user experience.

Note that when the view is clipped (e.g. the view is in a `https://developer.android.com/reference/kotlin/android/widget/ScrollView.html#`), the offsets are applied after the view's handwriting bounds is clipped.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setHandwritingDelegateFlags(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets flags configuring the handwriting delegation behavior for this delegate editor view.

This method has no effect unless `https://developer.android.com/reference/kotlin/android/view/View#setIsHandwritingDelegate(kotlin.Boolean)` is also called to configure this view to act as a handwriting delegate.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setHandwritingDelegatorCallback(java.lang.Runnable)(callback: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#?)`

Sets a callback which should be called when a stylus `https://developer.android.com/reference/kotlin/android/view/MotionEvent` occurs within this view's bounds. The callback will be called from the UI thread.

Setting a callback allows this view to act as a handwriting delegator, so that handwriting mode for a delegate editor view can be initiated by stylus movement on this delegator view. The callback implementation is expected to show and focus the delegate editor view. If a view which returns `true` for `https://developer.android.com/reference/kotlin/android/view/View#isHandwritingDelegate()` creates an input connection while the same stylus `https://developer.android.com/reference/kotlin/android/view/MotionEvent` sequence is ongoing, handwriting mode will be initiated for that view.

A common use case is a custom view which looks like a text editor but does not actually support text editing itself, and clicking on the custom view causes an EditText to be shown. To support handwriting initiation in this case, this method can be called on the custom view to configure it as a delegator. The EditText should call `https://developer.android.com/reference/kotlin/android/view/View#setIsHandwritingDelegate(kotlin.Boolean)` to set it as a delegate. The `callback` implementation is typically the same as the click listener implementation which shows the EditText.

If `null` is passed, this view will no longer act as a handwriting initiation delegator.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setHapticFeedbackEnabled(kotlin.Boolean)(hapticFeedbackEnabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set whether this view should have haptic feedback for events such as long presses.

You may wish to disable haptic feedback if your view already controls its own haptic feedback.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setHasTransientState(kotlin.Boolean)(hasTransientState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set whether this view is currently tracking transient state that the framework should attempt to preserve when possible. This flag is reference counted, so every call to setHasTransientState(true) should be paired with a later call to setHasTransientState(false).

A view with transient state cannot be trivially rebound from an external data source, such as an adapter binding item views in a list. This may be because the view is performing an animation, tracking user selection of content, or similar.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setHorizontalFadingEdgeEnabled(kotlin.Boolean)(horizontalFadingEdgeEnabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Define whether the horizontal edges should be faded when this view is scrolled horizontally.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setHorizontalScrollBarEnabled(kotlin.Boolean)(horizontalScrollBarEnabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Define whether the horizontal scrollbar should be drawn or not. The scrollbar is not drawn by default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setHorizontalScrollbarThumbDrawable(android.graphics.drawable.Drawable)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?)`

Defines the horizontal thumb drawable

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setHorizontalScrollbarTrackDrawable(android.graphics.drawable.Drawable)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?)`

Defines the horizontal track drawable

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setHovered(kotlin.Boolean)(hovered: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether the view is currently hovered.

Calling this method also changes the drawable state of the view. This enables the view to react to hover by using different drawable resources to change its appearance.

The `https://developer.android.com/reference/kotlin/android/view/View#onHoverChanged(kotlin.Boolean)` method is called when the hovered state changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setId(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the identifier for this view. The identifier does not have to be unique in this view's hierarchy. The identifier should be a positive number.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setImportantForAccessibility(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets how to determine whether this view is important for accessibility which is if it fires accessibility events and if it is reported to accessibility services that query the screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setImportantForAutofill(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the mode for determining whether this view is considered important for autofill.

The platform determines the importance for autofill automatically but you can use this method to customize the behavior. For example:

1. When the view contents is irrelevant for autofill (for example, a text field used in a "Captcha" challenge), it should be `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int`.
2. When both the view and its children are irrelevant for autofill (for example, the root view of an activity containing a spreadhseet editor), it should be `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int`.
3. When the view content is relevant for autofill but its children aren't (for example, a credit card expiration date represented by a custom view that overrides the proper autofill methods and has 2 children representing the month and year), it should be `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`.

**Note:** Setting the mode as `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int` does not guarantee the view (and its children) will not be used for autofill purpose; for example, when the user explicitly makes an autofill request, all views are included in the ViewStructure, and starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` the system uses other factors along with importance to determine the autofill behavior. See `https://developer.android.com/reference/kotlin/android/view/View#isImportantForAutofill()` for more details about how the View's importance for autofill is used.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setImportantForContentCapture(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the mode for determining whether this view is considered important for content capture.

The platform determines the importance for autofill automatically but you can use this method to customize the behavior. Typically, a view that provides text should be marked as `https://developer.android.com/reference/kotlin/android/view/View#IMPORTANT_FOR_CONTENT_CAPTURE_YES:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setIsCredential(kotlin.Boolean)(isCredential: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether this view is a credential for Credential Manager purposes.

See `https://developer.android.com/reference/kotlin/android/view/View#isCredential()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setIsHandwritingDelegate(kotlin.Boolean)(isHandwritingDelegate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets this view to be a handwriting delegate. If a delegate view creates an input connection while a stylus `https://developer.android.com/reference/kotlin/android/view/MotionEvent` sequence from a delegator view is ongoing, handwriting mode will be initiated for the delegate view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setKeepScreenOn(kotlin.Boolean)(keepScreenOn: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Controls whether the screen should remain on, modifying the value of `https://developer.android.com/reference/kotlin/android/view/View#KEEP_SCREEN_ON:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setKeyboardNavigationCluster(kotlin.Boolean)(isCluster: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set whether this view is a root of a keyboard navigation cluster.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setLabelFor(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the id of a view for which this view serves as a label for accessibility purposes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setLayerPaint(android.graphics.Paint)(paint: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#?)`

Updates the `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` object used with the current layer (used only if the current layer type is not set to `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`). Changed properties of the Paint provided to `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` will be used the next time the View is redrawn, but `https://developer.android.com/reference/kotlin/android/view/View#setLayerPaint(android.graphics.Paint)` must be called to ensure that the view gets redrawn immediately.

A layer is associated with an optional `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` instance that controls how the layer is composed on screen. The following properties of the paint are taken into account when composing the layer:

- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getAlpha()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getXfermode()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getColorFilter()`

If this view has an alpha value set to \< 1.0 by calling `https://developer.android.com/reference/kotlin/android/view/View#setAlpha(kotlin.Float)`, the alpha value of the layer's paint is superseded by this view's alpha value.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)(layerType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, paint: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#?)`

Specifies the type of layer backing this view. The layer can be `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int`.

A layer is associated with an optional `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` instance that controls how the layer is composed on screen. The following properties of the paint are taken into account when composing the layer:

- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getAlpha()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getXfermode()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getColorFilter()`

If this view has an alpha value set to \< 1.0 by calling `https://developer.android.com/reference/kotlin/android/view/View#setAlpha(kotlin.Float)`, the alpha value of the layer's paint is superseded by this view's alpha value.

Refer to the documentation of `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int` for more information on when and how to use layers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setLayoutDirection(kotlin.Int)(layoutDirection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the layout direction for this view. This will propagate a reset of layout direction resolution to the view's children and resolve layout direction for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setLayoutParams(android.view.ViewGroup.LayoutParams)(params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!)`

Set the layout parameters associated with this view. These supply parameters to the *parent* of this view specifying how it should be arranged. There are many subclasses of ViewGroup.LayoutParams, and these correspond to the different subclasses of ViewGroup that are responsible for arranging their children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setLeft(kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the left position of this view relative to its parent. This method is meant to be called by the layout system and should not generally be called otherwise, because the property may be changed at any time by the layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setLeftTopRightBottom(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Assign a size and position to this view. This method is meant to be used in animations only as it applies this position and size for the view only temporary and it can be changed back at any time by the layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setLongClickable(kotlin.Boolean)(longClickable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Enables or disables long click events for this view. When a view is long clickable it reacts to the user holding down the button for a longer duration than a tap. This event can either launch the listener or a context menu.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setMeasuredDimension(kotlin.Int,%20kotlin.Int)(measuredWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, measuredHeight: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

This method must be called by `https://developer.android.com/reference/kotlin/android/view/View#onMeasure(kotlin.Int,%20kotlin.Int)` to store the measured width and measured height. Failing to do so will trigger an exception at measurement time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setMinimumHeight(kotlin.Int)(minHeight: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the minimum height of the view. It is not guaranteed the view will be able to achieve this minimum height (for example, if its parent layout constrains it with less available height).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setMinimumWidth(kotlin.Int)(minWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the minimum width of the view. It is not guaranteed the view will be able to achieve this minimum width (for example, if its parent layout constrains it with less available width).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setNestedScrollingEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Enable or disable nested scrolling for this view.

If this property is set to true the view will be permitted to initiate nested scrolling operations with a compatible parent view in the current hierarchy. If this view does not implement nested scrolling this will have no effect. Disabling nested scrolling while a nested scroll is in progress has the effect of `https://developer.android.com/reference/kotlin/android/view/View#stopNestedScroll()` the nested scroll.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setNextClusterForwardId(kotlin.Int)(nextClusterForwardId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the id of the view to use as the root of the next keyboard navigation cluster.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setNextFocusDownId(kotlin.Int)(nextFocusDownId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setNextFocusForwardId(kotlin.Int)(nextFocusForwardId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setNextFocusLeftId(kotlin.Int)(nextFocusLeftId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setNextFocusRightId(kotlin.Int)(nextFocusRightId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setNextFocusUpId(kotlin.Int)(nextFocusUpId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnApplyWindowInsetsListener(android.view.View.OnApplyWindowInsetsListener)(listener: https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener!)`

Set an `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener` to take over the policy for applying window insets to this view. The listener's `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener#onApplyWindowInsets(android.view.View,%20android.view.WindowInsets)` method will be called instead of the view's `https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets)` method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnCapturedPointerListener(android.view.View.OnCapturedPointerListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnCapturedPointerListener!)`

Set a listener to receive callbacks when the pointer capture state of a view changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnClickListener(android.view.View.OnClickListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnClickListener?)`

Register a callback to be invoked when this view is clicked. If this view is not clickable, it becomes clickable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnContextClickListener(android.view.View.OnContextClickListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnContextClickListener?)`

Register a callback to be invoked when this view is context clicked. If the view is not context clickable, it becomes context clickable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnCreateContextMenuListener(android.view.View.OnCreateContextMenuListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener!)`

Register a callback to be invoked when the context menu for this view is being built. If this view is not long clickable, it becomes long clickable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnDragListener(android.view.View.OnDragListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnDragListener!)`

Register a drag event listener callback object for this View. The parameter is an implementation of `https://developer.android.com/reference/kotlin/android/view/View.OnDragListener`. To send a drag event to a View, the system calls the `https://developer.android.com/reference/kotlin/android/view/View.OnDragListener#onDrag(android.view.View,%20android.view.DragEvent)` method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnFocusChangeListener(android.view.View.OnFocusChangeListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnFocusChangeListener!)`

Register a callback to be invoked when focus of this view changed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnGenericMotionListener(android.view.View.OnGenericMotionListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnGenericMotionListener!)`

Register a callback to be invoked when a generic motion event is sent to this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnHoverListener(android.view.View.OnHoverListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnHoverListener!)`

Register a callback to be invoked when a hover event is sent to this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnKeyListener(android.view.View.OnKeyListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnKeyListener!)`

Register a callback to be invoked when a hardware key is pressed in this view. Key presses in software input methods will generally not trigger the methods of this listener.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnLongClickListener(android.view.View.OnLongClickListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnLongClickListener?)`

Register a callback to be invoked when this view is clicked and held. If this view is not long clickable, it becomes long clickable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnReceiveContentListener(kotlin.Array,%20android.view.OnReceiveContentListener)(mimeTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, listener: https://developer.android.com/reference/kotlin/android/view/OnReceiveContentListener?)`

Sets the listener to be `https://developer.android.com/reference/kotlin/android/view/View#performReceiveContent(android.view.ContentInfo)` to handle insertion of content into this view.

Depending on the type of view, this listener may be invoked for different scenarios. For example, for an editable `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`, this listener will be invoked for the following scenarios:

1. Paste from the clipboard (e.g. "Paste" or "Paste as plain text" action in the insertion/selection menu)
2. Content insertion from the keyboard (from `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#commitContent(android.view.inputmethod.InputContentInfo,%20kotlin.Int,%20android.os.Bundle)`)
3. Drag and drop (drop events from `https://developer.android.com/reference/kotlin/android/view/View#onDragEvent(android.view.DragEvent)`)
4. Autofill
5. Selection replacement via `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROCESS_TEXT:kotlin.String`

When setting a listener, clients must also declare the accepted MIME types. The listener will still be invoked even if the MIME type of the content is not one of the declared MIME types (e.g. if the user pastes content whose type is not one of the declared MIME types). In that case, the listener may reject the content (defer to the default platform behavior) or execute some other fallback logic (e.g. show an appropriate message to the user). The declared MIME types serve as a hint to allow different features to optionally alter their behavior. For example, a soft keyboard may optionally choose to hide its UI for inserting GIFs for a particular input field if the MIME types set here for that field don't include "image/gif" or "image/\*".

Note: MIME type matching in the Android framework is case-sensitive, unlike formal RFC MIME types. As a result, you should always write your MIME types with lowercase letters, or use `https://developer.android.com/reference/kotlin/android/content/Intent.html#normalizeMimeType(kotlin.String)` to ensure that it is converted to lowercase.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnScrollChangeListener(android.view.View.OnScrollChangeListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnScrollChangeListener!)`

Register a callback to be invoked when the scroll X or Y positions of this view change.

**Note:** Some views handle scrolling independently from View and may have their own separate listeners for scroll-type events. For example, `https://developer.android.com/reference/kotlin/android/widget/ListView.html#` allows clients to register an `https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#setOnScrollListener(android.widget.AbsListView.OnScrollListener)` to listen for changes in list scroll position.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnSystemUiVisibilityChangeListener(android.view.View.OnSystemUiVisibilityChangeListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnSystemUiVisibilityChangeListener!)`

Set a listener to receive callbacks when the visibility of the system bar changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOnTouchListener(android.view.View.OnTouchListener)(l: https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener!)`

Register a callback to be invoked when a touch event is sent to this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOutlineAmbientShadowColor(kotlin.Int)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the color of the ambient shadow that is drawn when the view has a positive Z or elevation value.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different views with different colors.

The opacity of the final ambient shadow is a function of the shadow caster height, the alpha channel of the outlineAmbientShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#ambientShadowAlpha:kotlin.Int` theme attribute.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOutlineProvider(android.view.ViewOutlineProvider)(provider: https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider!)`

Sets the `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider` of the view, which generates the Outline that defines the shape of the shadow it casts, and enables outline clipping.

The default ViewOutlineProvider, `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider#BACKGROUND:android.view.ViewOutlineProvider`, queries the Outline from the View's background drawable, via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#getOutline(android.graphics.Outline)`. Changing the outline provider with this method allows this behavior to be overridden.

If the ViewOutlineProvider is null, if querying it for an outline returns false, or if the produced Outline is `https://developer.android.com/reference/kotlin/android/graphics/Outline.html#isEmpty()`, shadows will not be cast.

Only outlines that return true from `https://developer.android.com/reference/kotlin/android/graphics/Outline.html#canClip()` may be used for clipping.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOutlineSpotShadowColor(kotlin.Int)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the color of the spot shadow that is drawn when the view has a positive Z or elevation value.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different views with different colors.

The opacity of the final spot shadow is a function of the shadow caster height, the alpha channel of the outlineSpotShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#spotShadowAlpha:kotlin.Int` theme attribute.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setOverScrollMode(kotlin.Int)(overScrollMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the over-scroll mode for this view. Valid over-scroll modes are `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_ALWAYS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_IF_CONTENT_SCROLLS:kotlin.Int` (allow over-scrolling only if the view content is larger than the container), or `https://developer.android.com/reference/kotlin/android/view/View#OVER_SCROLL_NEVER:kotlin.Int`. Setting the over-scroll mode of a view will have an effect only if the view is capable of scrolling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setPadding(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the padding. The view may add on the space required to display the scrollbars, depending on the style and visibility of the scrollbars. So the values returned from `https://developer.android.com/reference/kotlin/android/view/View#getPaddingLeft()`, `https://developer.android.com/reference/kotlin/android/view/View#getPaddingTop()`, `https://developer.android.com/reference/kotlin/android/view/View#getPaddingRight()` and `https://developer.android.com/reference/kotlin/android/view/View#getPaddingBottom()` may be different from the values set in this call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setPaddingRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the relative padding. The view may add on the space required to display the scrollbars, depending on the style and visibility of the scrollbars. So the values returned from `https://developer.android.com/reference/kotlin/android/view/View#getPaddingStart()`, `https://developer.android.com/reference/kotlin/android/view/View#getPaddingTop()`, `https://developer.android.com/reference/kotlin/android/view/View#getPaddingEnd()` and `https://developer.android.com/reference/kotlin/android/view/View#getPaddingBottom()` may be different from the values set in this call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setPendingCredentialRequest(android.credentials.GetCredentialRequest,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse.html#!, https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException.html#!>)`

Sets a `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` request to retrieve credentials, when the user focuses on this given view. When this view is focused, the given `request` will be fired to `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#`, which will fetch content from all `https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService.html#` services on the device, and then display credential options to the user on a relevant UI (dropdown, keyboard suggestions etc.). When the user selects a credential, the final `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse.html#` will be propagated to the given `callback`. Developers are expected to handle the response programmatically and perform a relevant action, e.g. signing in the user.

For details on how to build a Credential Manager request, please see `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#`.

This API should be called at any point before the user focuses on the view, e.g. during `onCreate` of an Activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setPivotX(kotlin.Float)(pivotX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the x location of the point around which the view is `https://developer.android.com/reference/kotlin/android/view/View#setRotation(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#setScaleX(kotlin.Float)`. By default, the pivot point is centered on the object. Setting this property disables this behavior and causes the view to use only the explicitly set pivotX and pivotY values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setPivotY(kotlin.Float)(pivotY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the y location of the point around which the view is `https://developer.android.com/reference/kotlin/android/view/View#setRotation(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#setScaleY(kotlin.Float)`. By default, the pivot point is centered on the object. Setting this property disables this behavior and causes the view to use only the explicitly set pivotX and pivotY values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setPointerIcon(android.view.PointerIcon)(pointerIcon: https://developer.android.com/reference/kotlin/android/view/PointerIcon!)`

Set the pointer icon to be used for a mouse pointer in the current view. Passing `null` will restore the pointer icon to its default value. Note that setting the pointer icon using this method will only set it for events coming from a mouse device (i.e. with source `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_MOUSE:kotlin.Int`). To resolve the pointer icon for other device types like styluses, override `https://developer.android.com/reference/kotlin/android/view/View#onResolvePointerIcon(android.view.MotionEvent,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setPreferKeepClear(kotlin.Boolean)(preferKeepClear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set a preference to keep the bounds of this view clear from floating windows above this view's window. This informs the system that the view is considered a vital area for the user and that ideally it should not be covered. Setting this is only appropriate for UI where the user would likely take action to uncover it.

The system will try to respect this preference, but when not possible will ignore it.

Note: This is independent from `https://developer.android.com/reference/kotlin/android/view/View#setPreferKeepClearRects(kotlin.collections.MutableList)`. If both are set, both will be taken into account.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setPreferKeepClearRects(kotlin.collections.MutableList)(rects: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!>)`

Set a preference to keep the provided rects clear from floating windows above this view's window. This informs the system that these rects are considered vital areas for the user and that ideally they should not be covered. Setting this is only appropriate for UI where the user would likely take action to uncover it.

The system will try to respect this preference, but when not possible will ignore it.

Note: This is independent from `https://developer.android.com/reference/kotlin/android/view/View#setPreferKeepClear(kotlin.Boolean)`. If both are set, both will be taken into account.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setPressed(kotlin.Boolean)(pressed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets the pressed state for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setRenderEffect(android.graphics.RenderEffect)(renderEffect: https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#?)`

Configure the `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#` to apply to this View. This will apply a visual effect to the results of the View before it is drawn. For example if `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#createBlurEffect(kotlin.Float,%20kotlin.Float,%20android.graphics.RenderEffect,%20android.graphics.Shader.TileMode)` is provided, the contents will be drawn in a separate layer, then this layer will be blurred when this View is drawn.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setRevealOnFocusHint(kotlin.Boolean)(revealOnFocus: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets this view's preference for reveal behavior when it gains focus.

When set to true, this is a signal to ancestor views in the hierarchy that this view would prefer to be brought fully into view when it gains focus. For example, a text field that a user is meant to type into. Other views such as scrolling containers may prefer to opt-out of this behavior.

The default value for views is true, though subclasses may change this based on their preferred behavior.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setRight(kotlin.Int)(right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the right position of this view relative to its parent. This method is meant to be called by the layout system and should not generally be called otherwise, because the property may be changed at any time by the layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setRotation(kotlin.Float)(rotation: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the degrees that the view is rotated around the pivot point. Increasing values result in clockwise rotation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setRotationX(kotlin.Float)(rotationX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the degrees that the view is rotated around the horizontal axis through the pivot point. Increasing values result in clockwise rotation from the viewpoint of looking down the x axis. When rotating large views, it is recommended to adjust the camera distance accordingly. Refer to `https://developer.android.com/reference/kotlin/android/view/View#setCameraDistance(kotlin.Float)` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setRotationY(kotlin.Float)(rotationY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the degrees that the view is rotated around the vertical axis through the pivot point. Increasing values result in counter-clockwise rotation from the viewpoint of looking down the y axis. When rotating large views, it is recommended to adjust the camera distance accordingly. Refer to `https://developer.android.com/reference/kotlin/android/view/View#setCameraDistance(kotlin.Float)` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setSaveEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Controls whether the saving of this view's state is enabled (that is, whether its `https://developer.android.com/reference/kotlin/android/view/View#onSaveInstanceState()` method will be called). Note that even if freezing is enabled, the view still must have an id assigned to it (via `https://developer.android.com/reference/kotlin/android/view/View#setId(kotlin.Int)`) for its state to be saved. This flag can only disable the saving of this view; any child views may still have their state saved.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setSaveFromParentEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Controls whether the entire hierarchy under this view will save its state when a state saving traversal occurs from its parent. The default is true; if false, these views will not be saved unless `https://developer.android.com/reference/kotlin/android/view/View#saveHierarchyState(android.util.SparseArray)` is called directly on this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScaleX(kotlin.Float)(scaleX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the amount that the view is scaled in x around the pivot point, as a proportion of the view's unscaled width. A value of 1 means that no scaling is applied.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScaleY(kotlin.Float)(scaleY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the amount that the view is scaled in Y around the pivot point, as a proportion of the view's unscaled width. A value of 1 means that no scaling is applied.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScreenReaderFocusable(kotlin.Boolean)(screenReaderFocusable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether this View should be a focusable element for screen readers and include non-focusable Views from its subtree when providing feedback.

Note: this is similar to using [`android:focusable`, but does not impact input focus behavior.](https://developer.android.com/reference/kotlin/android/view/View#attr_android:focusable)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScrollBarDefaultDelayBeforeFade(kotlin.Int)(scrollBarDefaultDelayBeforeFade: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Define the delay before scrollbars fade.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScrollBarFadeDuration(kotlin.Int)(scrollBarFadeDuration: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Define the scrollbar fade duration.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScrollBarSize(kotlin.Int)(scrollBarSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Define the scrollbar size.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScrollBarStyle(kotlin.Int)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Specify the style of the scrollbars. The scrollbars can be overlaid or inset. When inset, they add to the padding of the view. And the scrollbars can be drawn inside the padding area or on the edge of the view. For example, if a view has a background drawable and you want to draw the scrollbars inside the padding specified by the drawable, you can use SCROLLBARS_INSIDE_OVERLAY or SCROLLBARS_INSIDE_INSET. If you want them to appear at the edge of the view, ignoring the padding, then you can use SCROLLBARS_OUTSIDE_OVERLAY or SCROLLBARS_OUTSIDE_INSET.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScrollCaptureCallback(android.view.ScrollCaptureCallback)(callback: https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback?)`

Sets the callback to receive scroll capture requests. This component is the adapter between the scroll capture API and application UI code. If no callback is set, the system may provide an implementation. Any value provided here will take precedence over a system version.

This view will be ignored when `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE:kotlin.Int` is set in its `https://developer.android.com/reference/kotlin/android/view/View#setScrollCaptureHint(kotlin.Int)`, regardless whether a callback has been set.

It is recommended to set the scroll capture hint `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int` when setting a custom callback to help ensure it is selected as the target.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScrollCaptureHint(kotlin.Int)(hint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the scroll capture hint for this View. These flags affect the search for a potential scroll capture targets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScrollContainer(kotlin.Boolean)(isScrollContainer: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Change whether this view is one of the set of scrollable containers in its window. This will be used to determine whether the window can resize or must pan when a soft input area is open -- scrollable containers allow the window to use resize mode since the container will appropriately shrink.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScrollIndicators(kotlin.Int)(indicators: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the state of all scroll indicators.

See `https://developer.android.com/reference/kotlin/android/view/View#setScrollIndicators(kotlin.Int,%20kotlin.Int)` for usage information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScrollIndicators(kotlin.Int,%20kotlin.Int)(indicators: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the state of the scroll indicators specified by the mask. To change all scroll indicators at once, see `https://developer.android.com/reference/kotlin/android/view/View#setScrollIndicators(kotlin.Int)`.

When a scroll indicator is enabled, it will be displayed if the view can scroll in the direction of the indicator.

Multiple indicator types may be enabled or disabled by passing the logical OR of the desired types. If multiple types are specified, they will all be set to the same enabled state.

For example, to enable the top scroll indicatorExample: `setScrollIndicators`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScrollX(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the horizontal scrolled position of your view. This will cause a call to `https://developer.android.com/reference/kotlin/android/view/View#onScrollChanged(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` and the view will be invalidated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScrollY(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the vertical scrolled position of your view. This will cause a call to `https://developer.android.com/reference/kotlin/android/view/View#onScrollChanged(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` and the view will be invalidated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setScrollbarFadingEnabled(kotlin.Boolean)(fadeScrollbars: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Define whether scrollbars will fade when the view is not scrolling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setSelected(kotlin.Boolean)(selected: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Changes the selection state of this view. A view can be selected or not. Note that selection is not the same as focus. Views are typically selected in the context of an AdapterView like ListView or GridView; the selected view is the view that is highlighted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setSoundEffectsEnabled(kotlin.Boolean)(soundEffectsEnabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set whether this view should have sound effects enabled for events such as clicking and touching.

You may wish to disable sound effects for a view if you already play sounds, for instance, a dial key that plays dtmf tones.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setStateDescription(kotlin.CharSequence)(stateDescription: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)`

Sets the `https://developer.android.com/reference/kotlin/android/view/View`'s state description.

A state description briefly describes the states of the view and is primarily used for accessibility support to determine how the states of a view should be presented to the user. It is a supplement to the boolean states (for example, checked/unchecked) and it is used for customized state description (for example, "wifi, connected, three bars"). State description changes frequently while content description should change less often. State description should be localized. For android widgets which have default state descriptions, app developers can call this method to override the state descriptions. Setting state description to null restores the default behavior.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setStateListAnimator(android.animation.StateListAnimator)(stateListAnimator: https://developer.android.com/reference/kotlin/android/animation/StateListAnimator.html#!)`

Attaches the provided StateListAnimator to this View.

Any previously attached StateListAnimator will be detached.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setSupplementalDescription(kotlin.CharSequence)(supplementalDescription: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)`

Sets the `https://developer.android.com/reference/kotlin/android/view/View`'s supplemental description.

A supplemental description provides brief supplemental information for this node, such as the purpose of the node when that purpose is not conveyed within its textual representation. For example, if a dropdown select has a purpose of setting font family, the supplemental description could be "font family". If this node has children, its supplemental description serves as additional information and is not intended to replace any existing information in the subtree. This is different from the `https://developer.android.com/reference/kotlin/android/view/View#setContentDescription(kotlin.CharSequence)` in that this description is purely supplemental while a content description may be used to replace a description for a node or its subtree that an assistive technology would otherwise compute based on other properties of the node and its descendants.

This should omit role or state. Role refers to the kind of user-interface element the View is, such as a Button or Checkbox. State refers to a frequently changing property of the View, such as an On/Off state of a button or the audio level of a volume slider.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setSystemGestureExclusionRects(kotlin.collections.MutableList)(rects: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!>)`

Sets a list of areas within this view's post-layout coordinate space where the system should not intercept touch or other pointing device gestures. *This method should be called by `https://developer.android.com/reference/kotlin/android/view/View#onLayout(kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`.*

Use this to tell the system which specific sub-areas of a view need to receive gesture input in order to function correctly in the presence of global system gestures that may conflict. For example, if the system wishes to capture swipe-in-from-screen-edge gestures to provide system-level navigation functionality, a view such as a navigation drawer container can mark the left (or starting) edge of itself as requiring gesture capture priority using this API. The system may then choose to relax its own gesture recognition to allow the app to consume the user's gesture. It is not necessary for an app to register exclusion rects for broadly spanning regions such as the entirety of a `ScrollView` or for simple press and release click targets such as `Button`. Mark an exclusion rect when interacting with a view requires a precision touch gesture in a small area in either the X or Y dimension, such as an edge swipe or dragging a `SeekBar` thumb.

Note: the system will put a limit of `200dp` on the vertical extent of the exclusions it takes into account. The limit does not apply while the navigation bar is `https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_IMMERSIVE_STICKY:kotlin.Int` hidden, nor to the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HOME:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)(visibility: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Request that the visibility of the status bar or other screen/window decorations be changed.

This method is used to put the over device UI into temporary modes where the user's attention is focused more on the application content, by dimming or hiding surrounding system affordances. This is typically used in conjunction with `https://developer.android.com/reference/kotlin/android/view/Window#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int`, allowing the applications content to be placed behind the action bar (and with these flags other system affordances) so that smooth transitions between hiding and showing them can be done.

Two representative examples of the use of system UI visibility is implementing a content browsing application (like a magazine reader) and a video playing application.

The first code shows a typical implementation of a View in a content browsing application. In this implementation, the application goes into a content-oriented mode by hiding the status bar and action bar, and putting the navigation elements into lights out mode. The user can then interact with content while in this mode. Such an application should provide an easy way for the user to toggle out of the mode (such as to check information in the status bar or access notifications). In the implementation here, this is done simply by tapping on the content.

This second code sample shows a typical implementation of a View in a video playing application. In this situation, while the video is playing the application would like to go into a complete full-screen mode, to use as much of the display as possible for the video. When in this state the user can not interact with the application; the system intercepts touching on the screen to pop the UI out of full screen mode. See `https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect)` for a sample layout that goes with this code.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTag(kotlin.Int,%20kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)`

Sets a tag associated with this view and a key. A tag can be used to mark a view in its hierarchy and does not have to be unique within the hierarchy. Tags can also be used to store data within a view without resorting to another data structure. The specified key should be an id declared in the resources of the application to ensure it is unique (see the [ID resource type](https://developer.android.com/guide/topics/resources/more-resources.html#Id)). Keys identified as belonging to the Android framework or not associated with any package will cause an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` to be thrown.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTag(kotlin.Any)(tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)`

Sets the tag associated with this view. A tag can be used to mark a view in its hierarchy and does not have to be unique within the hierarchy. Tags can also be used to store data within a view without resorting to another data structure.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTextAlignment(kotlin.Int)(textAlignment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the text alignment.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTextDirection(kotlin.Int)(textDirection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the text direction.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTooltipText(kotlin.CharSequence)(tooltipText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)`

Sets the tooltip text which will be displayed in a small popup next to the view.

The tooltip will be displayed:

- On long click, unless it is handled otherwise (by OnLongClickListener or a context menu).
- On hover, after a brief delay since the pointer has stopped moving

**Note:** Do not override this method, as it will have no effect on the text displayed in the tooltip.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTop(kotlin.Int)(top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the top position of this view relative to its parent. This method is meant to be called by the layout system and should not generally be called otherwise, because the property may be changed at any time by the layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTouchDelegate(android.view.TouchDelegate)(delegate: https://developer.android.com/reference/kotlin/android/view/TouchDelegate!)`

Sets the TouchDelegate for this View.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTransitionAlpha(kotlin.Float)(alpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

This property is intended only for use by the Fade transition, which animates it to produce a visual translucency that does not side-effect (or get affected by) the real alpha property. This value is composited with the other alpha value (and the AlphaAnimation value, when that is present) to produce a final visual translucency result, which is what is passed into the DisplayList.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTransitionName(kotlin.String)(transitionName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Sets the name of the View to be used to identify Views in Transitions. Names should be unique in the View hierarchy.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTransitionVisibility(kotlin.Int)(visibility: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Changes the visibility of this View without triggering any other changes. This should only be used by animation frameworks, such as `https://developer.android.com/reference/kotlin/android/transition/Transition.html#`, where visibility changes should not adjust focus or trigger a new layout. Application developers should use `https://developer.android.com/reference/kotlin/android/view/View#setVisibility(kotlin.Int)` instead to ensure that the hierarchy is correctly updated.

Only call this method when a temporary visibility must be applied during an animation and the original visibility value is guaranteed to be reset after the animation completes. Use `https://developer.android.com/reference/kotlin/android/view/View#setVisibility(kotlin.Int)` in all other cases.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTranslationX(kotlin.Float)(translationX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the horizontal location of this view relative to its `https://developer.android.com/reference/kotlin/android/view/View#getLeft()` position. This effectively positions the object post-layout, in addition to wherever the object's layout placed it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTranslationY(kotlin.Float)(translationY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the vertical location of this view relative to its `https://developer.android.com/reference/kotlin/android/view/View#getTop()` position. This effectively positions the object post-layout, in addition to wherever the object's layout placed it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setTranslationZ(kotlin.Float)(translationZ: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the depth location of this view relative to its `https://developer.android.com/reference/kotlin/android/view/View#getElevation()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setVerticalFadingEdgeEnabled(kotlin.Boolean)(verticalFadingEdgeEnabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Define whether the vertical edges should be faded when this view is scrolled vertically.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setVerticalScrollBarEnabled(kotlin.Boolean)(verticalScrollBarEnabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Define whether the vertical scrollbar should be drawn or not. The scrollbar is not drawn by default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setVerticalScrollbarPosition(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the position of the vertical scroll bar. Should be one of `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBAR_POSITION_DEFAULT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBAR_POSITION_LEFT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#SCROLLBAR_POSITION_RIGHT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setVerticalScrollbarThumbDrawable(android.graphics.drawable.Drawable)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?)`

Defines the vertical scrollbar thumb drawable

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setVerticalScrollbarTrackDrawable(android.graphics.drawable.Drawable)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?)`

Defines the vertical scrollbar track drawable

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setViewTranslationCallback(android.view.translation.ViewTranslationCallback)(callback: https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback)`

Sets a `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback` that is used to display/hide the translated information. Developers can provide the customized implementation for show/hide translated information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setVisibility(kotlin.Int)(visibility: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the visibility state of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setWillNotCacheDrawing(kotlin.Boolean)(willNotCacheDrawing: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

When a View's drawing cache is enabled, drawing is redirected to an offscreen bitmap. Some views, like an ImageView, must be able to bypass this mechanism if they already draw a single bitmap, to avoid unnecessary usage of the memory.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setWillNotDraw(kotlin.Boolean)(willNotDraw: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

If this view doesn't do any drawing on its own, set this flag to allow further optimizations. By default, this flag is not set on View, but could be set on some View subclasses such as ViewGroup. Typically, if you override `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)` you should clear this flag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setX(kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the visual x position of this view, in pixels. This is equivalent to setting the `https://developer.android.com/reference/kotlin/android/view/View#setTranslationX(kotlin.Float)` property to be the difference between the x value passed in and the current `https://developer.android.com/reference/kotlin/android/view/View#getLeft()` property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setY(kotlin.Float)(y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the visual y position of this view, in pixels. This is equivalent to setting the `https://developer.android.com/reference/kotlin/android/view/View#setTranslationY(kotlin.Float)` property to be the difference between the y value passed in and the current `https://developer.android.com/reference/kotlin/android/view/View#getTop()` property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#setZ(kotlin.Float)(z: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Sets the visual z position of this view, in pixels. This is equivalent to setting the `https://developer.android.com/reference/kotlin/android/view/View#setTranslationZ(kotlin.Float)` property to be the difference between the z value passed in and the current `https://developer.android.com/reference/kotlin/android/view/View#getElevation()` property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#showContextMenu()()`

Shows the context menu for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#showContextMenu(kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Shows the context menu for this view anchored to the specified view-relative coordinate.

<br />

`https://developer.android.com/reference/kotlin/android/view/ActionMode!` `https://developer.android.com/reference/kotlin/android/view/View#startActionMode(android.view.ActionMode.Callback)(callback: https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback!)`

Start an action mode with the default type `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int`.

<br />

`https://developer.android.com/reference/kotlin/android/view/ActionMode!` `https://developer.android.com/reference/kotlin/android/view/View#startActionMode(android.view.ActionMode.Callback,%20kotlin.Int)(callback: https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback!, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Start an action mode with the given type.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#startAnimation(android.view.animation.Animation)(animation: https://developer.android.com/reference/kotlin/android/view/animation/Animation!)`

Start the specified animation now.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#startDrag(android.content.ClipData,%20android.view.View.DragShadowBuilder,%20kotlin.Any,%20kotlin.Int)(data: https://developer.android.com/reference/kotlin/android/content/ClipData.html#!, shadowBuilder: https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder!, myLocalState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#startDragAndDrop(android.content.ClipData,%20android.view.View.DragShadowBuilder,%20kotlin.Any,%20kotlin.Int)(data: https://developer.android.com/reference/kotlin/android/content/ClipData.html#!, shadowBuilder: https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder!, myLocalState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Starts a drag and drop operation. When your application calls this method, it passes a `https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder` object to the system. The system calls this object's `https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder#onProvideShadowMetrics(android.graphics.Point,%20android.graphics.Point)` to get metrics for the drag shadow, and then calls the object's `https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder#onDrawShadow(android.graphics.Canvas)` to draw the drag shadow itself.

Once the system has the drag shadow, it begins the drag and drop operation by sending drag events to all the View objects in your application that are currently visible. It does this either by calling the View object's drag listener (an implementation of `https://developer.android.com/reference/kotlin/android/view/View.OnDragListener#onDrag(android.view.View,%20android.view.DragEvent)` or by calling the View object's `https://developer.android.com/reference/kotlin/android/view/View#onDragEvent(android.view.DragEvent)` method. Both are passed a `https://developer.android.com/reference/kotlin/android/view/DragEvent` object that has a `https://developer.android.com/reference/kotlin/android/view/DragEvent#getAction()` value of `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_STARTED:kotlin.Int`.

Your application can invoke `https://developer.android.com/reference/kotlin/android/view/View#startDragAndDrop(android.content.ClipData,%20android.view.View.DragShadowBuilder,%20kotlin.Any,%20kotlin.Int)` on any attached View object. The View object does not need to be the one used in `https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder`, nor does it need to be related to the View the user selected for dragging.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#startNestedScroll(kotlin.Int)(axes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Begin a nestable scroll operation along the given axes.

A view starting a nested scroll promises to abide by the following contract:

The view will call startNestedScroll upon initiating a scroll operation. In the case of a touch scroll this corresponds to the initial `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int`. In the case of touch scrolling the nested scroll will be terminated automatically in the same manner as `https://developer.android.com/reference/kotlin/android/view/ViewParent#requestDisallowInterceptTouchEvent(kotlin.Boolean)`. In the event of programmatic scrolling the caller must explicitly call `https://developer.android.com/reference/kotlin/android/view/View#stopNestedScroll()` to indicate the end of the nested scroll.

If `startNestedScroll` returns true, a cooperative parent was found. If it returns false the caller may ignore the rest of this contract until the next scroll. Calling startNestedScroll while a nested scroll is already in progress will return true.

At each incremental step of the scroll the caller should invoke `https://developer.android.com/reference/kotlin/android/view/View#dispatchNestedPreScroll(kotlin.Int,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.IntArray)` once it has calculated the requested scrolling delta. If it returns true the nested scrolling parent at least partially consumed the scroll and the caller should adjust the amount it scrolls by.

After applying the remainder of the scroll delta the caller should invoke `https://developer.android.com/reference/kotlin/android/view/View#dispatchNestedScroll(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.IntArray)`, passing both the delta consumed and the delta unconsumed. A nested scrolling parent may treat these values differently. See `https://developer.android.com/reference/kotlin/android/view/ViewParent#onNestedScroll(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#stopNestedScroll()()`

Stop a nested scroll in progress.

Calling this method when a nested scroll is not currently in progress is harmless.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View#toString()()`

Returns a string representation of the object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#transformMatrixToGlobal(android.graphics.Matrix)(matrix: https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#)`

Modifies the input matrix such that it maps view-local coordinates to on-screen coordinates.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#transformMatrixToLocal(android.graphics.Matrix)(matrix: https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#)`

Modifies the input matrix such that it maps on-screen coordinates to view-local coordinates.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#unregisterCalledFromWrongThreadListener(android.view.View.CalledFromWrongThreadListener)(listener: https://developer.android.com/reference/kotlin/android/view/View.CalledFromWrongThreadListener)`

Unregisters a listener that was previously registered with `https://developer.android.com/reference/kotlin/android/view/View#registerCalledFromWrongThreadListener(android.view.View.CalledFromWrongThreadListener)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#unscheduleDrawable(android.graphics.drawable.Drawable)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)`

Unschedule any events associated with the given Drawable. This can be used when selecting a new Drawable into a view, so that the previous one is completely unscheduled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#unscheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#, what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`

Cancels a scheduled action on a drawable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/View#updateDragShadow(android.view.View.DragShadowBuilder)(shadowBuilder: https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder!)`

Updates the drag shadow for the ongoing drag and drop operation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#verifyDrawable(android.graphics.drawable.Drawable)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)`

If your view subclass is displaying its own Drawable objects, it should override this function and return true for any Drawable it is displaying. This allows animations for those drawables to be scheduled.

Be sure to call through to the super class when overriding this function. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#willNotCacheDrawing()()`

Returns whether or not this View can cache its drawing or not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/View#willNotDraw()()`

Returns whether or not this View draws on its own.

<br />

Inherited properties From class `https://developer.android.com/reference/kotlin/android/view/View` `https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View#ALPHA:android.util.Property`

A Property wrapper around the `alpha` functionality handled by the `https://developer.android.com/reference/kotlin/android/view/View#setAlpha(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#getAlpha()` methods.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#EMPTY_STATE_SET:kotlin.IntArray`

Indicates the view has no states set. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_FOCUSED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled, focused and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled, focused, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled and has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_FOCUSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled, focused and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#ENABLED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled and that its window has focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is focused and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is focused, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is focused. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#FOCUSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view has the focus and that its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_FOCUSED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled, focused and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled, focused, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled and focused.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_FOCUSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled, focused and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed and enabled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_ENABLED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_FOCUSED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, focused and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, focused, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed and focused.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_FOCUSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, focused and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#PRESSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed and its window has the focus.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View#ROTATION:android.util.Property`

A Property wrapper around the `rotation` functionality handled by the `https://developer.android.com/reference/kotlin/android/view/View#setRotation(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#getRotation()` methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View#ROTATION_X:android.util.Property`

A Property wrapper around the `rotationX` functionality handled by the `https://developer.android.com/reference/kotlin/android/view/View#setRotationX(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#getRotationX()` methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View#ROTATION_Y:android.util.Property`

A Property wrapper around the `rotationY` functionality handled by the `https://developer.android.com/reference/kotlin/android/view/View#setRotationY(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#getRotationY()` methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View#SCALE_X:android.util.Property`

A Property wrapper around the `scaleX` functionality handled by the `https://developer.android.com/reference/kotlin/android/view/View#setScaleX(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#getScaleX()` methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View#SCALE_Y:android.util.Property`

A Property wrapper around the `scaleY` functionality handled by the `https://developer.android.com/reference/kotlin/android/view/View#setScaleY(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#getScaleY()` methods.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is selected. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is selected and that its window has the focus.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View#TRANSLATION_X:android.util.Property`

A Property wrapper around the `translationX` functionality handled by the `https://developer.android.com/reference/kotlin/android/view/View#setTranslationX(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#getTranslationX()` methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View#TRANSLATION_Y:android.util.Property`

A Property wrapper around the `translationY` functionality handled by the `https://developer.android.com/reference/kotlin/android/view/View#setTranslationY(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#getTranslationY()` methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View#TRANSLATION_Z:android.util.Property`

A Property wrapper around the `translationZ` functionality handled by the `https://developer.android.com/reference/kotlin/android/view/View#setTranslationZ(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#getTranslationZ()` methods.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view's window has focus. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View#X:android.util.Property`

A Property wrapper around the `x` functionality handled by the `https://developer.android.com/reference/kotlin/android/view/View#setX(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#getX()` methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View#Y:android.util.Property`

A Property wrapper around the `y` functionality handled by the `https://developer.android.com/reference/kotlin/android/view/View#setY(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#getY()` methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View#Z:android.util.Property`

A Property wrapper around the `z` functionality handled by the `https://developer.android.com/reference/kotlin/android/view/View#setZ(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/view/View#getZ()` methods.

<br />

## XML attributes

### android:addStatesFromChildren

```
android:addStatesFromChildren
```
Sets whether this ViewGroup's drawable states also include its children's drawable states. This is used, for example, to make a group appear to be focused when its child EditText or button is focused.

May be a boolean value, such as "`true`" or "`false`".

### android:alwaysDrawnWithCache

```
android:alwaysDrawnWithCache
```
Defines whether the ViewGroup should always draw its children using their drawing cache or not. The default value is true. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11.

May be a boolean value, such as "`true`" or "`false`".

### android:animateLayoutChanges

```
android:animateLayoutChanges
```
Defines whether changes in layout (caused by adding and removing items) should cause a LayoutTransition to run. When this flag is set to true, a default LayoutTransition object will be set on the ViewGroup container and default animations will run when these layout changes occur.

May be a boolean value, such as "`true`" or "`false`".

### android:animationCache

```
android:animationCache
```
Defines whether layout animations should create a drawing cache for their children. Enabling the animation cache consumes more memory and requires a longer initialization but provides better performance. The animation cache is enabled by default.

May be a boolean value, such as "`true`" or "`false`".

### android:clipChildren

```
android:clipChildren
```
Defines whether a child is limited to draw inside of its bounds or not. This is useful with animations that scale the size of the children to more than 100% for instance. In such a case, this property should be set to false to allow the children to draw outside of their bounds. The default value of this property is true.

May be a boolean value, such as "`true`" or "`false`".

### android:clipToPadding

```
android:clipToPadding
```
Defines whether the ViewGroup will clip its children and resize (but not clip) any EdgeEffect to its padding, if padding is not zero. This property is set to true by default.

May be a boolean value, such as "`true`" or "`false`".

### android:descendantFocusability

```
android:descendantFocusability
```
Defines the relationship between the ViewGroup and its descendants when looking for a View to take focus.

Must be one of the following constant values.

| Constant | Value | Description |
|---|---|---|
| afterDescendants | 1 | The ViewGroup will get focus only if none of its descendants want it. |
| beforeDescendants | 0 | The ViewGroup will get focus before any of its descendants. |
| blocksDescendants | 2 | The ViewGroup will block its descendants from receiving focus. |

### android:layoutAnimation

```
android:layoutAnimation
```
Defines the layout animation to use the first time the ViewGroup is laid out. Layout animations can also be started manually after the first layout.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:layoutMode

```
android:layoutMode
```
Defines the layout mode of this ViewGroup.

Must be one of the following constant values.

| Constant | Value | Description |
|---|---|---|
| clipBounds | 0 | Use the children's clip bounds when laying out this container. |
| opticalBounds | 1 | Use the children's optical bounds when laying out this container. |

### android:persistentDrawingCache

```
android:persistentDrawingCache
```
Defines the persistence of the drawing cache. The drawing cache might be enabled by a ViewGroup for all its children in specific situations (for instance during a scrolling.) This property lets you persist the cache in memory after its initial usage. Persisting the cache consumes more memory but may prevent frequent garbage collection if the cache is created over and over again. By default the persistence is set to scrolling. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11.

Must be one or more (separated by '|') of the following constant values.

| Constant | Value | Description |
|---|---|---|
| all | 3 | The drawing cache is always persisted. |
| animation | 1 | The drawing cache is persisted after a layout animation. |
| none | 0 | The drawing cache is not persisted after use. |
| scrolling | 2 | The drawing cache is persisted after a scroll. |

### android:splitMotionEvents

```
android:splitMotionEvents
```
Sets whether this ViewGroup should split MotionEvents to separate child views during touch event dispatch. If false (default prior to HONEYCOMB), touch events will be dispatched to the child view where the first pointer went down until the last pointer goes up. If true (default for HONEYCOMB and later), touch events may be dispatched to multiple children. MotionEvents for each pointer will be dispatched to the child view where the initial ACTION_DOWN event happened. See `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setMotionEventSplittingEnabled(kotlin.Boolean)` for more information.

May be a boolean value, such as "`true`" or "`false`".

## Constants

### CLIP_TO_PADDING_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val CLIP_TO_PADDING_MASK: Int
```

We clip to padding when FLAG_CLIP_TO_PADDING and FLAG_PADDING_NOT_NULL are set at the same time.

 Value: 34

### FOCUS_AFTER_DESCENDANTS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUS_AFTER_DESCENDANTS: Int
```

This view will get focus only if none of its descendants want it.

 Value: 262144

### FOCUS_BEFORE_DESCENDANTS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUS_BEFORE_DESCENDANTS: Int
```

This view will get focus before any of its descendants.

 Value: 131072

### FOCUS_BLOCK_DESCENDANTS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUS_BLOCK_DESCENDANTS: Int
```

This view will block any of its descendants from getting focus, even if they are focusable.

 Value: 393216

### LAYOUT_MODE_CLIP_BOUNDS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAYOUT_MODE_CLIP_BOUNDS: Int
```

This constant is a `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setLayoutMode(kotlin.Int)`. Clip bounds are the raw values of `https://developer.android.com/reference/kotlin/android/view/View#getLeft()`, `https://developer.android.com/reference/kotlin/android/view/View#getTop()`, `https://developer.android.com/reference/kotlin/android/view/View#getRight()` and `https://developer.android.com/reference/kotlin/android/view/View#getBottom()`.

 Value: 0

### LAYOUT_MODE_OPTICAL_BOUNDS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAYOUT_MODE_OPTICAL_BOUNDS: Int
```

This constant is a `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setLayoutMode(kotlin.Int)`. Optical bounds describe where a widget appears to be. They sit inside the clip bounds which need to cover a larger area to allow other effects, such as shadows and glows, to be drawn.

 Value: 1

### PERSISTENT_ALL_CACHES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERSISTENT_ALL_CACHES: Int
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)` on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the `https://developer.android.com/reference/kotlin/android/view/PixelCopy` API is recommended.*

Used to indicate that all drawing caches should be kept in memory.

 Value: 3

### PERSISTENT_ANIMATION_CACHE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERSISTENT_ANIMATION_CACHE: Int
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)` on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the `https://developer.android.com/reference/kotlin/android/view/PixelCopy` API is recommended.*

Used to indicate that the animation drawing cache should be kept in memory.

 Value: 1

### PERSISTENT_NO_CACHE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERSISTENT_NO_CACHE: Int
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)` on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the `https://developer.android.com/reference/kotlin/android/view/PixelCopy` API is recommended.*

Used to indicate that no drawing cache should be kept in memory.

 Value: 0

### PERSISTENT_SCROLLING_CACHE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERSISTENT_SCROLLING_CACHE: Int
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)` on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the `https://developer.android.com/reference/kotlin/android/view/PixelCopy` API is recommended.*

Used to indicate that the scrolling drawing cache should be kept in memory.

 Value: 2

## Public constructors

### ViewGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ViewGroup(context: Context!)
```

### ViewGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ViewGroup(
    context: Context!, 
    attrs: AttributeSet!)
```

### ViewGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ViewGroup(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int)
```

### ViewGroup

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ViewGroup(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int, 
    defStyleRes: Int)
```

## Public methods

### addChildrenForAccessibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addChildrenForAccessibility(outChildren: ArrayList<View!>!): Unit
```

Adds the children of this View relevant for accessibility to the given list as output. Since some Views are not important for accessibility the added child views are not necessarily direct children of this view, rather they are the first level of descendants important for accessibility.

| Parameters ||
|---|---|
| `outChildren` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [View](https://developer.android.com/reference/kotlin/android/view/View)!\>!: The output list that will receive children for accessibility. |

### addExtraDataToAccessibilityNodeInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addExtraDataToAccessibilityNodeInfo(
    info: AccessibilityNodeInfo, 
    extraDataKey: String, 
    arguments: Bundle?
): Unit
```

Adds extra data to an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo` based on an explicit request for the additional data.

This method only needs overloading if the node is marked as having extra data available.
. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `info` | [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo): The info to which to add the extra data. Never `null`. |
| `extraDataKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A key specifying the type of extra data to add to the info. The extra data should be added to the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` returned by the info's `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExtras()` method. Never `null`. |
| `arguments` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: A `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` holding any arguments relevant for this request. May be `null` if the service provided no arguments. |

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
| `views` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [View](https://developer.android.com/reference/kotlin/android/view/View)!\>!: Focusable views found so far or null if all we are interested is the number of focusables. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction of the focus. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` |
| `focusableMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of focusables to be added. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLES_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUSABLES_TOUCH_MODE:kotlin.Int` |

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
| `views` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [View](https://developer.android.com/reference/kotlin/android/view/View)!\>: Keyboard navigation cluster roots found so far. This value cannot be `null`. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Direction to look |

### addStatesFromChildren

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addStatesFromChildren(): Boolean
```

Returns whether this ViewGroup's drawable states also include its children's drawable states. This is used, for example, to make a group appear to be focused when its child EditText or button is focused.

### addTouchables

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addTouchables(views: ArrayList<View!>!): Unit
```

Add any touchable views that are descendants of this view (possibly including this view if it is touchable itself) to views.

| Parameters ||
|---|---|
| `views` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [View](https://developer.android.com/reference/kotlin/android/view/View)!\>!: Touchable views found so far |

### addView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addView(child: View!): Unit
```

Adds a child view. If no layout parameters are already set on the child, the default parameters for this ViewGroup are set on the child.

**Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the child view to add |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#generateDefaultLayoutParams()`

### addView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addView(
    child: View!, 
    params: ViewGroup.LayoutParams!
): Unit
```

Adds a child view with the specified layout parameters.

**Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method.

| Parameters ||
|---|---|
| `view` | The view to be added to this window. |
| `params` | [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams)!: the layout parameters to set on the child |
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the child view to add |

### addView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addView(
    child: View!, 
    index: Int
): Unit
```

Adds a child view. If no layout parameters are already set on the child, the default parameters for this ViewGroup are set on the child.

**Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the child view to add |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position at which to add the child |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#generateDefaultLayoutParams()`

### addView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addView(
    child: View!, 
    index: Int, 
    params: ViewGroup.LayoutParams!
): Unit
```

Adds a child view with the specified layout parameters.

**Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the child view to add |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position at which to add the child or -1 to add last |
| `params` | [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams)!: the layout parameters to set on the child |

### addView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addView(
    child: View!, 
    width: Int, 
    height: Int
): Unit
```

Adds a child view with this ViewGroup's default layout parameters and the specified width and height.

**Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the child view to add |

### bringChildToFront

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bringChildToFront(child: View!): Unit
```

Change the z order of the child so it's on top of all other children. This ordering change may affect layout, if this container uses an order-dependent layout scheme (e.g., LinearLayout). Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int` this method should be followed by calls to `https://developer.android.com/reference/kotlin/android/view/ViewParent#requestLayout()` and `https://developer.android.com/reference/kotlin/android/view/View#invalidate()` on this parent to force the parent to redraw with the new child ordering.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The child to bring to the top of the z order |

### childDrawableStateChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun childDrawableStateChanged(child: View): Unit
```

If `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addStatesFromChildren()` is true, refreshes this group's drawable state (to include the states from its children).

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View): The child whose drawable state has changed. This value cannot be `null`. |

### childHasTransientStateChanged

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun childHasTransientStateChanged(
    child: View, 
    childHasTransientState: Boolean
): Unit
```

Called when a child view has changed whether or not it is tracking transient state.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View): Child view whose state has changed. This value cannot be `null`. |
| `hasTransientState` | true if this child has transient state |

### clearChildFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearChildFocus(child: View!): Unit
```

Called when a child of this parent is giving up focus

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The view that is giving up focus |

### clearDisappearingChildren

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearDisappearingChildren(): Unit
```

Removes any pending animations for views that have been removed. Call this if you don't want animations for exiting views to stack up.

### clearFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearFocus(): Unit
```

Called when this view wants to give up focus. If focus is cleared `https://developer.android.com/reference/kotlin/android/view/View#onFocusChanged(kotlin.Boolean,%20kotlin.Int,%20android.graphics.Rect)` is called.

**Note:** When not in touch-mode, the framework will try to give focus to the first focusable View from the top after focus is cleared. Hence, if this View is the first from the top that can take focus, then all callbacks related to clearing focus will be invoked after which the framework will give focus to this view.

### dispatchApplyWindowInsets

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchApplyWindowInsets(insets: WindowInsets!): WindowInsets!
```

Request to apply the given window insets to this view or another view in its subtree.

This method should be called by clients wishing to apply insets corresponding to areas obscured by window decorations or overlays. This can include the status and navigation bars, action bars, input methods and more. New inset categories may be added in the future. The method returns the insets provided minus any that were applied by this view or its children.

Clients wishing to provide custom behavior should override the `https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets)` method or alternatively provide a `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener` via the `https://developer.android.com/reference/kotlin/android/view/View#setOnApplyWindowInsetsListener(android.view.View.OnApplyWindowInsetsListener)` method.

This method replaces the older `https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect)` method.

| Parameters ||
|---|---|
| `insets` | [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets)!: Insets to apply |

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
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!: The motion event to be dispatched. |

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
| `newConfig` | [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)!: The new resource configuration. |

### dispatchCreateViewTranslationRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchCreateViewTranslationRequest(
    viewIds: MutableMap<AutofillId!, LongArray!>, 
    supportedFormats: IntArray, 
    capability: TranslationCapability!, 
    requests: MutableList<ViewTranslationRequest!>
): Unit
```

Dispatch to collect the `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest`s for translation purpose by traversing the hierarchy when the app requests ui translation. Typically, this method should only be overridden by subclasses that provide a view hierarchy (such as `https://developer.android.com/reference/kotlin/android/view/ViewGroup#`). Other classes should override `https://developer.android.com/reference/kotlin/android/view/View#onCreateViewTranslationRequest(kotlin.IntArray,%20java.util.function.Consumer)` for normal view or override `https://developer.android.com/reference/kotlin/android/view/View#onVirtualViewTranslationResponses(android.util.LongSparseArray)` for view contains virtual children. When requested to start the ui translation, the system will call this method to traverse the view hierarchy to collect `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest`s and create a `https://developer.android.com/reference/kotlin/android/view/translation/Translator` to translate the requests. All the `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest`s must be added when the traversal is done.

The default implementation calls `https://developer.android.com/reference/kotlin/android/view/View#onCreateViewTranslationRequest(kotlin.IntArray,%20java.util.function.Consumer)` for normal view or calls `https://developer.android.com/reference/kotlin/android/view/View#onVirtualViewTranslationResponses(android.util.LongSparseArray)` for view contains virtual children to build `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest` if the view should be translated. The view is marked as having `https://developer.android.com/reference/kotlin/android/view/View#setHasTransientState(kotlin.Boolean)` so that recycling of views doesn't prevent the system from attaching the response to it. Therefore, if overriding this method, you should set or reset the transient state.
The implementation calls `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchCreateViewTranslationRequest(kotlin.collections.MutableMap,%20kotlin.IntArray,%20android.view.translation.TranslationCapability,%20kotlin.collections.MutableList)` for all the child views.

| Parameters ||
|---|---|
| `viewIds` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [AutofillId](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId)!, [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!\>: This value cannot be `null`. |
| `supportedFormats` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec#DATA_FORMAT_TEXT:kotlin.Int` |
| `capability` | [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability)!: This value may be `null`. |
| `requests` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ViewTranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest)!\>: This value cannot be `null`. |

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

Detects if this View is enabled and has a drag event listener. If both are true, then it calls the drag event listener with the `https://developer.android.com/reference/kotlin/android/view/DragEvent` it received. If the drag event listener returns `true`, then dispatchDragEvent() returns `true`.

For all other cases, the method calls the `https://developer.android.com/reference/kotlin/android/view/View#onDragEvent(android.view.DragEvent)` drag event handler method and returns its result.

This ensures that a drag event is always consumed, even if the View does not have a drag event listener. However, if the View has a listener and the listener returns true, then onDragEvent() is not called.

### dispatchDrawableHotspotChanged

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchDrawableHotspotChanged(
    x: Float, 
    y: Float
): Unit
```

Dispatches drawable hotspot changes to child views that meet at least one of the following criteria:

- Returns `false` from both `https://developer.android.com/reference/kotlin/android/view/View#isClickable()` and `https://developer.android.com/reference/kotlin/android/view/View#isLongClickable()`
- Requests duplication of parent state via `https://developer.android.com/reference/kotlin/android/view/View#setDuplicateParentStateEnabled(kotlin.Boolean)`

<br />

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): hotspot x coordinate |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): hotspot y coordinate |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#drawableHotspotChanged(kotlin.Float,%20kotlin.Float)`

### dispatchFinishTemporaryDetach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchFinishTemporaryDetach(): Unit
```

Dispatch `https://developer.android.com/reference/kotlin/android/view/View#onFinishTemporaryDetach()` to this View and its direct children if this is a container View. 
If you override this method you *must* call through to the superclass implementation.

### dispatchKeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchKeyEvent(event: KeyEvent!): Boolean
```

Dispatch a key event to the next view on the focus path. This path runs from the top of the view tree down to the currently focused view. If this view has focus, it will dispatch to itself. Otherwise it will dispatch the next node down the focus path. This method also fires any key listeners.

| Parameters ||
|---|---|
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent)!: The key event to be dispatched. |

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
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent)!: The key event to be dispatched. |

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
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent)!: The key event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

### dispatchPointerCaptureChanged

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchPointerCaptureChanged(hasCapture: Boolean): Unit
```

### dispatchProvideAutofillStructure

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchProvideAutofillStructure(
    structure: ViewStructure, 
    flags: Int
): Unit
```

Dispatches creation of a `https://developer.android.com/reference/kotlin/android/view/ViewStructure`s for autofill purposes down the hierarchy, when an Assist structure is being created as part of an autofill request.

The default implementation does the following:

- Sets the `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId` in the structure.
- Calls `https://developer.android.com/reference/kotlin/android/view/View#onProvideAutofillStructure(android.view.ViewStructure,%20kotlin.Int)`.
- Calls `https://developer.android.com/reference/kotlin/android/view/View#onProvideAutofillVirtualStructure(android.view.ViewStructure,%20kotlin.Int)`.

Typically, this method should only be overridden by subclasses that provide a view hierarchy (such as `https://developer.android.com/reference/kotlin/android/view/ViewGroup#`) - other classes should override `https://developer.android.com/reference/kotlin/android/view/View#onProvideAutofillStructure(android.view.ViewStructure,%20kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/view/View#onProvideAutofillVirtualStructure(android.view.ViewStructure,%20kotlin.Int)` instead.

When overridden, it must:

- Either call `super.dispatchProvideAutofillStructure(structure, flags)` or explicitly set the `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId` in the structure (for example, by calling `structure.setAutofillId(getAutofillId())`).
- Decide how to handle the `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int` flag - when set, all views in the structure should be considered important for autofill, regardless of what `https://developer.android.com/reference/kotlin/android/view/View#isImportantForAutofill()` returns. We encourage you to respect this flag to provide a better user experience - this flag is typically used when an user explicitly requested autofill. If the flag is not set, then only views marked as important for autofill should be included in the structure - skipping non-important views optimizes the overall autofill performance.

This implementation adds in all child views of the view group, in addition to calling the default `https://developer.android.com/reference/kotlin/android/view/View` implementation.

| Parameters ||
|---|---|
| `structure` | [ViewStructure](https://developer.android.com/reference/kotlin/android/view/ViewStructure): fill in with structured view data for autofill purposes. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/View#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int` |

### dispatchProvideStructure

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchProvideStructure(structure: ViewStructure!): Unit
```

Dispatch creation of `https://developer.android.com/reference/kotlin/android/view/ViewStructure` down the hierarchy. This implementation adds in all child views of the view group, in addition to calling the default View implementation.

### dispatchScrollCaptureSearch

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchScrollCaptureSearch(
    localVisibleRect: Rect, 
    windowOffset: Point, 
    targets: Consumer<ScrollCaptureTarget!>
): Unit
```

Handle the scroll capture search request by checking this view if applicable, then to each child view.

| Parameters ||
|---|---|
| `localVisibleRect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): the visible area of this ViewGroup in local coordinates, according to the parent. This value cannot be `null`. |
| `windowOffset` | [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#): the offset of this view within the window. This value cannot be `null`. |
| `targets` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [ScrollCaptureTarget](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget)!\>: accepts potential scroll capture targets; `https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#accept(java.util.function.Consumer.T)` may be called zero or more times on the calling thread before onScrollCaptureSearch returns. This value cannot be `null`. |

### dispatchSetActivated

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchSetActivated(activated: Boolean): Unit
```

Dispatch setActivated to all of this View's children.

| Parameters ||
|---|---|
| `activated` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The new activated state |

### dispatchSetSelected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchSetSelected(selected: Boolean): Unit
```

Dispatch setSelected to all of this View's children.

| Parameters ||
|---|---|
| `selected` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The new selected state |

### dispatchStartTemporaryDetach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchStartTemporaryDetach(): Unit
```

Dispatch `https://developer.android.com/reference/kotlin/android/view/View#onStartTemporaryDetach()` to this View and its direct children if this is a container View. 
If you override this method you *must* call through to the superclass implementation.

### dispatchSystemUiVisibilityChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchSystemUiVisibilityChanged(visible: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Dispatch callbacks to `https://developer.android.com/reference/kotlin/android/view/View#setOnSystemUiVisibilityChangeListener(android.view.View.OnSystemUiVisibilityChangeListener)` down the view hierarchy.

### dispatchTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchTouchEvent(ev: MotionEvent!): Boolean
```

Pass the touch screen motion event down to the target view, or this view if it is the target.

| Parameters ||
|---|---|
| `event` | The motion event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

### dispatchTrackballEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchTrackballEvent(event: MotionEvent!): Boolean
```

Pass a trackball motion event down to the focused view.

| Parameters ||
|---|---|
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!: The motion event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

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
| `focused` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The currently focused view. |
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

Dispatches `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback#onEnd(android.view.WindowInsetsAnimation)` when Window Insets animation ends.

| Parameters ||
|---|---|
| `animation` | [WindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation): This value cannot be `null`. |

### dispatchWindowInsetsAnimationPrepare

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchWindowInsetsAnimationPrepare(animation: WindowInsetsAnimation): Unit
```

Dispatches `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback#onPrepare(android.view.WindowInsetsAnimation)` when Window Insets animation is being prepared.

| Parameters ||
|---|---|
| `animation` | [WindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation): This value cannot be `null`. |

### dispatchWindowInsetsAnimationProgress

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchWindowInsetsAnimationProgress(
    insets: WindowInsets, 
    runningAnimations: MutableList<WindowInsetsAnimation!>
): WindowInsets
```

Dispatches `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback#onProgress(android.view.WindowInsets,%20kotlin.collections.MutableList)` when Window Insets animation makes progress.

| Parameters ||
|---|---|
| `insets` | [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets): This value cannot be `null`. |
| `runningAnimations` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation)!\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/WindowInsets` | This value cannot be `null`. |

### dispatchWindowInsetsAnimationStart

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchWindowInsetsAnimationStart(
    animation: WindowInsetsAnimation, 
    bounds: WindowInsetsAnimation.Bounds
): WindowInsetsAnimation.Bounds
```

Dispatches `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback#onStart(android.view.WindowInsetsAnimation,%20android.view.WindowInsetsAnimation.Bounds)` when Window Insets animation is started.

| Parameters ||
|---|---|
| `animation` | [WindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation): This value cannot be `null`. |
| `bounds` | [WindowInsetsAnimation.Bounds](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Bounds): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Bounds` | This value cannot be `null`. |

### dispatchWindowSystemUiVisiblityChanged

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchWindowSystemUiVisiblityChanged(visible: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Dispatch callbacks to `https://developer.android.com/reference/kotlin/android/view/View#onWindowSystemUiVisibilityChanged(kotlin.Int)` down the view hierarchy.

### dispatchWindowVisibilityChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchWindowVisibilityChanged(visibility: Int): Unit
```

Dispatch a window visibility change down the view hierarchy. ViewGroups should override to route to their children.

| Parameters ||
|---|---|
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new visibility of the window. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` |

### endViewTransition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun endViewTransition(view: View!): Unit
```

This method should always be called following an earlier call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#startViewTransition(android.view.View)`. The given View is finally removed from its parent and will no longer be displayed. Note that this method does not perform the functionality of removing a view from its parent; it just discontinues the display of a View that has previously been removed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | view The View object that has been removed but is being kept around in the visible hierarchy by an earlier call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#startViewTransition(android.view.View)`. |

### findFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findFocus(): View!
```

Find the view in the hierarchy rooted at this view that currently has focus.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View!` | The view that currently has focus, or null if no focused view can be found. |

### findOnBackInvokedDispatcherForChild

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findOnBackInvokedDispatcherForChild(
    child: View, 
    requester: View
): OnBackInvokedDispatcher?
```

Walk up the View hierarchy to find the nearest `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#`.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View): The direct child of this view for which to find a dispatcher. This value cannot be `null`. |
| `requester` | [View](https://developer.android.com/reference/kotlin/android/view/View): The requester that will use the dispatcher. Can be the same as child. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#?` | The `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` from this or the nearest ancestor, or null if the view is both not attached and have no ancestor providing an `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#`. |

### findViewsWithText

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findViewsWithText(
    outViews: ArrayList<View!>!, 
    text: CharSequence!, 
    flags: Int
): Unit
```

Finds the Views that contain given text. The containment is case insensitive. The search is performed by either the text that the View renders or the content description that describes the view for accessibility purposes and the view does not render or both. Clients can specify how the search is to be performed via passing the `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_TEXT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_CONTENT_DESCRIPTION:kotlin.Int` flags.

| Parameters ||
|---|---|
| `outViews` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [View](https://developer.android.com/reference/kotlin/android/view/View)!\>!: The output list of matching Views. |
| `searched` | The text to match against. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_TEXT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FIND_VIEWS_WITH_CONTENT_DESCRIPTION:kotlin.Int` |

### focusSearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun focusSearch(
    focused: View!, 
    direction: Int
): View!
```

Find the nearest view in the specified direction that wants to take focus.

| Parameters ||
|---|---|
| `v` | The view that currently has focus |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of FOCUS_UP, FOCUS_DOWN, FOCUS_LEFT, and FOCUS_RIGHT, or 0 for not applicable. |
| `focused` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The view that currently has focus |

### focusableViewAvailable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun focusableViewAvailable(v: View!): Unit
```

Tells the parent that a new focusable view has become available. This is to handle transitions from the case where there are no focusable views to the case where the first focusable view appears.

| Parameters ||
|---|---|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The view that has become newly focusable |

### gatherTransparentRegion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun gatherTransparentRegion(region: Region?): Boolean
```

This is used by the ViewRoot to perform an optimization when the view hierarchy contains one or several SurfaceView. SurfaceView is always considered transparent, but its children are not, therefore all View objects remove themselves from the global transparent region (passed as a parameter to this function).

| Parameters ||
|---|---|
| `region` | [Region](https://developer.android.com/reference/kotlin/android/graphics/Region.html#)?: The transparent region for this ViewAncestor (window). This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the effective visibility of the view at this point is opaque, regardless of the transparent region; returns false if it is possible for underlying windows to be seen behind the view. |

### generateLayoutParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun generateLayoutParams(attrs: AttributeSet!): ViewGroup.LayoutParams!
```

Returns a new set of layout parameters based on the supplied attributes set.

| Parameters ||
|---|---|
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!: the attributes to build the layout parameters from |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!` | an instance of `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams` or one of its descendants |

### getAccessibilityClassName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccessibilityClassName(): CharSequence!
```

Return the class name of this object to be used for accessibility purposes. Subclasses should only override this if they are implementing something that should be seen as a completely new class of view when used by accessibility, unrelated to the class it is deriving from. This is used to fill in `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setClassName(kotlin.CharSequence)`.

### getChildAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChildAt(index: Int): View!
```

Returns the view at the specified position in the group.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position at which to get the view from |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View!` | the view at the specified position or null if the position does not exist within the group |

### getChildCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChildCount(): Int
```

Returns the number of children in the group.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a positive integer representing the number of children in the group |

### getChildDrawingOrder

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChildDrawingOrder(drawingPosition: Int): Int
```

Converts drawing order position to container position.

Children are not necessarily drawn in the order in which they appear in the container. ViewGroups can enable a custom ordering via `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setChildrenDrawingOrderEnabled(kotlin.Boolean)`. This method returns the container position of a child that appears in the given position in the current drawing order.

| Parameters ||
|---|---|
| `drawingPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the drawing order position. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the container position of a child for this drawing order position. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildDrawingOrder(kotlin.Int,%20kotlin.Int)`

### getChildMeasureSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getChildMeasureSpec(
    spec: Int, 
    padding: Int, 
    childDimension: Int
): Int
```

Does the hard part of measureChildren: figuring out the MeasureSpec to pass to a particular child. This method figures out the right MeasureSpec for one dimension (height or width) of one child view. The goal is to combine information from our MeasureSpec with the LayoutParams of the child to get the best possible results. For example, if the this view knows its size (because its MeasureSpec has a mode of EXACTLY), and the child has indicated in its LayoutParams that it wants to be the same size as the parent, the parent should ask the child to layout given an exact size.

| Parameters ||
|---|---|
| `spec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The requirements for this view |
| `padding` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The padding of this view for the current dimension and margins, if applicable |
| `childDimension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): How big the child wants to be in the current dimension |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a MeasureSpec integer for the child |

### getChildVisibleRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChildVisibleRect(
    child: View!, 
    r: Rect!, 
    offset: Point!
): Boolean
```

Compute the visible part of a rectangular region defined in terms of a child view's coordinates.

Returns the clipped visible part of the rectangle `r`, defined in the `child`'s local coordinate system. `r` is modified by this method to contain the result, expressed in the global (root) coordinate system.

The resulting rectangle is always axis aligned. If a rotation is applied to a node in the View hierarchy, the result is the axis-aligned bounding box of the visible rectangle.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: A child View, whose rectangular visible region we want to compute |
| `r` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!: The input rectangle, defined in the child coordinate system. Will be overwritten to contain the resulting visible rectangle, expressed in global (root) coordinates |
| `offset` | [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)!: The input coordinates of a point, defined in the child coordinate system. As with the `r` parameter, this will be overwritten to contain the global (root) coordinates of that point. A `null` value is valid (in case you are not interested in this result) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the resulting rectangle is not empty, false otherwise |

### getClipChildren

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClipChildren(): Boolean
```

Returns whether this group's children are clipped to their bounds before drawing. The default value is true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the group's children will be clipped to their bounds, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setClipChildren(kotlin.Boolean)`

### getClipToPadding

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClipToPadding(): Boolean
```

Returns whether this ViewGroup will clip its children to its padding, and resize (but not clip) any EdgeEffect to the padded region, if padding is present.

By default, children are clipped to the padding of their parent Viewgroup. This clipping behavior is only enabled if padding is non-zero.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this ViewGroup clips children to its padding and resizes (but doesn't clip) any EdgeEffect to the padded region, false otherwise. |

### getDescendantFocusability

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDescendantFocusability(): Int
```

Gets the descendant focusability of this view group. The descendant focusability defines the relationship between this view group and its descendants when looking for a view to take focus in `https://developer.android.com/reference/kotlin/android/view/ViewGroup#requestFocus(kotlin.Int,%20android.graphics.Rect)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | one of `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_BEFORE_DESCENDANTS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_AFTER_DESCENDANTS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_BLOCK_DESCENDANTS:kotlin.Int`. |

### getFocusedChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFocusedChild(): View!
```

Returns the focused child of this view, if any. The child may have focus or contain focus.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View!` | the focused child or null. |

### getLayoutAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayoutAnimation(): LayoutAnimationController!
```

Returns the layout animation controller used to animate the group's children.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController!` | the current animation controller |

### getLayoutAnimationListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayoutAnimationListener(): Animation.AnimationListener!
```

Returns the animation listener to which layout animation events are sent.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener!` | an `https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener` |

### getLayoutMode

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayoutMode(): Int
```

Returns the basis of alignment during layout operations on this ViewGroup: either `https://developer.android.com/reference/kotlin/android/view/ViewGroup#LAYOUT_MODE_CLIP_BOUNDS:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/ViewGroup#LAYOUT_MODE_OPTICAL_BOUNDS:kotlin.Int`.

If no layoutMode was explicitly set, either programmatically or in an XML resource, the method returns the layoutMode of the view's parent ViewGroup if such a parent exists, otherwise the method returns a default value of `https://developer.android.com/reference/kotlin/android/view/ViewGroup#LAYOUT_MODE_CLIP_BOUNDS:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the layout mode to use during layout operations |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setLayoutMode(kotlin.Int)`

### getLayoutTransition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayoutTransition(): LayoutTransition!
```

Gets the LayoutTransition object for this ViewGroup. If the LayoutTransition object is not null, changes in layout which occur because of children being added to or removed from the ViewGroup will be animated according to the animations defined in that LayoutTransition object. By default, the transition object is null (so layout changes are not animated).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.html#!` | LayoutTranstion The LayoutTransition object that will animated changes in layout. A value of `null` means no transition will run on layout changes. |

### getNestedScrollAxes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNestedScrollAxes(): Int
```

Return the current axes of nested scrolling for this ViewGroup.

A ViewGroup returning something other than `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_NONE:kotlin.Int` is currently acting as a nested scrolling parent for one or more descendant views in the hierarchy.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Flags indicating the current axes of nested scrolling |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_HORIZONTAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_VERTICAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_NONE:kotlin.Int`

### getOverlay

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOverlay(): ViewGroupOverlay!
```

Returns the ViewGroupOverlay for this view group, creating it if it does not yet exist. In addition to `https://developer.android.com/reference/kotlin/android/view/ViewOverlay`'s support for drawables, `https://developer.android.com/reference/kotlin/android/view/ViewGroupOverlay` allows views to be added to the overlay. These views, like overlay drawables, are visual-only; they do not receive input events and should not be used as anything other than a temporary representation of a view in a parent container, such as might be used by an animation effect.

Note: Overlays do not currently work correctly with `https://developer.android.com/reference/kotlin/android/view/SurfaceView` or `https://developer.android.com/reference/kotlin/android/view/TextureView`; contents in overlays for these types of views may not display correctly.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewGroupOverlay!` | The ViewGroupOverlay object for this view. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroupOverlay`

### getPersistentDrawingCache

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPersistentDrawingCache(): Int
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)` on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the `https://developer.android.com/reference/kotlin/android/view/PixelCopy` API is recommended.*

Returns an integer indicating what types of drawing caches are kept in memory.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | one or a combination of `https://developer.android.com/reference/kotlin/android/view/ViewGroup#PERSISTENT_NO_CACHE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#PERSISTENT_ANIMATION_CACHE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#PERSISTENT_SCROLLING_CACHE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/ViewGroup#PERSISTENT_ALL_CACHES:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setPersistentDrawingCache(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setAnimationCacheEnabled(kotlin.Boolean)`

### getTouchscreenBlocksFocus

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTouchscreenBlocksFocus(): Boolean
```

Check whether this ViewGroup should ignore focus requests for itself and its children.

### hasFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasFocus(): Boolean
```

Returns true if this view has or contains focus

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this view has or contains focus |

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

### indexOfChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOfChild(child: View!): Int
```

Returns the position in the group of the specified child view.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the view for which to get the position |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a positive integer representing the position of the view in the group, or -1 if the view does not exist in the group |

### invalidateChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun invalidateChild(
    child: View!, 
    dirty: Rect!
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onDescendantInvalidated(android.view.View,%20android.view.View)` instead to observe updates to draw state in descendants.*

Don't call or override this method. It is used for the implementation of the view hierarchy.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The child which is dirty |
| `r` | The area within the child that is invalid |

### invalidateChildInParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invalidateChildInParent(
    location: IntArray!, 
    dirty: Rect!
): ViewParent!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onDescendantInvalidated(android.view.View,%20android.view.View)` instead to observe updates to draw state in descendants.*

Don't call or override this method. It is used for the implementation of the view hierarchy. This implementation returns null if this ViewGroup does not have a parent, if this ViewGroup is already fully invalidated or if the dirty rectangle does not intersect with this ViewGroup's bounds.

| Parameters ||
|---|---|
| `location` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: An array of 2 ints containing the left and top coordinates of the child to invalidate |
| `r` | The area within the child that is invalid |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewParent!` | the parent of this ViewParent or null |

### isAlwaysDrawnWithCacheEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAlwaysDrawnWithCacheEnabled(): Boolean
```

**Deprecated:** *As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, this property is ignored. Child views may no longer have their caching behavior disabled by parents.*

Indicates whether this ViewGroup will always try to draw its children using their drawing cache. By default this property is enabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the animation cache is enabled, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setAlwaysDrawnWithCacheEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setChildrenDrawnWithCacheEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/View#setDrawingCacheEnabled(kotlin.Boolean)`

### isAnimationCacheEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAnimationCacheEnabled(): Boolean
```

**Deprecated:** *As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, this property is ignored. Caching behavior of children may be controlled through `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)`.*

Indicates whether the children's drawing cache is used during a layout animation. By default, the drawing cache is enabled but this will prevent nested layout animations from working. To nest animations, you must disable the cache.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the animation cache is enabled, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setAnimationCacheEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/View#setDrawingCacheEnabled(kotlin.Boolean)`

### isLayoutSuppressed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isLayoutSuppressed(): Boolean
```

Returns whether layout calls on this container are currently being suppressed, due to an earlier call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#suppressLayout(kotlin.Boolean)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if layout calls are currently suppressed, false otherwise. |

### isMotionEventSplittingEnabled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isMotionEventSplittingEnabled(): Boolean
```

Returns true if MotionEvents dispatched to this ViewGroup can be split to multiple children.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if MotionEvents dispatched to this ViewGroup can be split to multiple children. |

### isTransitionGroup

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTransitionGroup(): Boolean
```

Returns true if this ViewGroup should be considered as a single entity for removal when executing an Activity transition. If this is false, child elements will move individually during the transition.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the ViewGroup should be acted on together during an Activity transition. The default value is true when there is a non-null background or if `https://developer.android.com/reference/kotlin/android/view/View#getTransitionName()` is not null or if a non-null `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider` other than `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider#BACKGROUND:android.view.ViewOutlineProvider` was given to `https://developer.android.com/reference/kotlin/android/view/View#setOutlineProvider(android.view.ViewOutlineProvider)` and false otherwise. |

### jumpDrawablesToCurrentState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun jumpDrawablesToCurrentState(): Unit
```

Call `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#jumpToCurrentState()` on all Drawable objects associated with this view.

Also calls `https://developer.android.com/reference/kotlin/android/animation/StateListAnimator.html#jumpToCurrentState()` if there is a StateListAnimator attached to this view. 
If you override this method you *must* call through to the superclass implementation.

### layout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun layout(
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
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bottom position, relative to parent |

### notifySubtreeAccessibilityStateChanged

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifySubtreeAccessibilityStateChanged(
    child: View, 
    source: View, 
    changeType: Int
): Unit
```

Notifies a view parent that the accessibility state of one of its descendants has changed and that the structure of the subtree is different.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View): The direct child whose subtree has changed. This value cannot be `null`. |
| `source` | [View](https://developer.android.com/reference/kotlin/android/view/View): The descendant view that changed. May not be `null`. |
| `changeType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A bit mask of the types of changes that occurred. One or more of: - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_SUBTREE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_TEXT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_STARTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_CANCELLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_DROPPED:kotlin.Int` |

### offsetDescendantRectToMyCoords

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun offsetDescendantRectToMyCoords(
    descendant: View!, 
    rect: Rect!
): Unit
```

Offset a rectangle that is in a descendant's coordinate space into our coordinate space.

| Parameters ||
|---|---|
| `descendant` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: A descendant of this view |
| `rect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!: A rectangle defined in descendant's coordinate space. |

### offsetRectIntoDescendantCoords

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun offsetRectIntoDescendantCoords(
    descendant: View!, 
    rect: Rect!
): Unit
```

Offset a rectangle that is in our coordinate space into an ancestor's coordinate space.

| Parameters ||
|---|---|
| `descendant` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: A descendant of this view |
| `rect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!: A rectangle defined in descendant's coordinate space. |

### onDescendantInvalidated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDescendantInvalidated(
    child: View, 
    target: View
): Unit
```

The target View has been invalidated, or has had a drawing property changed that requires the hierarchy to re-render. This method is called by the View hierarchy to signal ancestors that a View either needs to re-record its drawing commands, or drawing properties have changed. This is how Views schedule a drawing traversal. This signal is generally only dispatched for attached Views, since only they need to draw. If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View): This value cannot be `null`. |
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View): This value cannot be `null`. |

### onInterceptHoverEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onInterceptHoverEvent(event: MotionEvent!): Boolean
```

Implement this method to intercept hover events before they are handled by child views.

This method is called before dispatching a hover event to a child of the view group or to the view group's own `https://developer.android.com/reference/kotlin/android/view/View#onHoverEvent(android.view.MotionEvent)` to allow the view group a chance to intercept the hover event. This method can also be used to watch all pointer motions that occur within the bounds of the view group even when the pointer is hovering over a child of the view group rather than over the view group itself.

The view group can prevent its children from receiving hover events by implementing this method and returning `true` to indicate that it would like to intercept hover events. The view group must continuously return `true` from `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onInterceptHoverEvent(android.view.MotionEvent)` for as long as it wishes to continue intercepting hover events from its children.

Interception preserves the invariant that at most one view can be hovered at a time by transferring hover focus from the currently hovered child to the view group or vice-versa as needed.

If this method returns `true` and a child is already hovered, then the child view will first receive a hover exit event and then the view group itself will receive a hover enter event in `https://developer.android.com/reference/kotlin/android/view/View#onHoverEvent(android.view.MotionEvent)`. Likewise, if this method had previously returned `true` to intercept hover events and instead returns `false` while the pointer is hovering within the bounds of one of a child, then the view group will first receive a hover exit event in `https://developer.android.com/reference/kotlin/android/view/View#onHoverEvent(android.view.MotionEvent)` and then the hovered child will receive a hover enter event.

The default implementation handles mouse hover on the scroll bars.

| Parameters ||
|---|---|
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!: The motion event that describes the hover. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the view group would like to intercept the hover event and prevent its children from receiving it. |

### onInterceptTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onInterceptTouchEvent(ev: MotionEvent!): Boolean
```

Implement this method to intercept all touch screen motion events. This allows you to watch events as they are dispatched to your children, and take ownership of the current gesture at any point.

Using this function takes some care, as it has a fairly complicated interaction with `https://developer.android.com/reference/kotlin/android/view/View#onTouchEvent(android.view.MotionEvent)`, and using it requires implementing that method as well as this one in the correct way. Events will be received in the following order:

1. You will receive the down event here.
2. The down event will be handled either by a child of this view group, or given to your own onTouchEvent() method to handle; this means you should implement onTouchEvent() to return true, so you will continue to see the rest of the gesture (instead of looking for a parent view to handle it). Also, by returning true from onTouchEvent(), you will not receive any following events in onInterceptTouchEvent() and all touch processing must happen in onTouchEvent() like normal.
3. For as long as you return false from this function, each following event (up to and including the final up) will be delivered first here and then to the target's onTouchEvent().
4. If you return true from here, you will not receive any following events: the target view will receive the same event but with the action `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_CANCEL:kotlin.Int`, and all further events will be delivered to your onTouchEvent() method and no longer appear here.

| Parameters ||
|---|---|
| `ev` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!: The motion event being dispatched down the hierarchy. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Return true to steal motion events from the children and have them dispatched to this ViewGroup through onTouchEvent(). The current target will receive an ACTION_CANCEL event, and no further messages will be delivered here. |

### onNestedFling

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onNestedFling(
    target: View, 
    velocityX: Float, 
    velocityY: Float, 
    consumed: Boolean
): Boolean
```

Request a fling from a nested scroll.

This method signifies that a nested scrolling child has detected suitable conditions for a fling. Generally this means that a touch scroll has ended with a `https://developer.android.com/reference/kotlin/android/view/VelocityTracker` in the direction of scrolling that meets or exceeds the `https://developer.android.com/reference/kotlin/android/view/ViewConfiguration#getScaledMinimumFlingVelocity()` along a scrollable axis.

If a nested scrolling child view would normally fling but it is at the edge of its own content, it can use this method to delegate the fling to its nested scrolling parent instead. The parent may optionally consume the fling or observe a child fling.

| Parameters ||
|---|---|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View): View that initiated the nested scroll. This value cannot be `null`. |
| `velocityX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Horizontal velocity in pixels per second |
| `velocityY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Vertical velocity in pixels per second |
| `consumed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the child consumed the fling, false otherwise |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this parent consumed or otherwise reacted to the fling |

### onNestedPreFling

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onNestedPreFling(
    target: View, 
    velocityX: Float, 
    velocityY: Float
): Boolean
```

React to a nested fling before the target view consumes it.

This method siginfies that a nested scrolling child has detected a fling with the given velocity along each axis. Generally this means that a touch scroll has ended with a `https://developer.android.com/reference/kotlin/android/view/VelocityTracker` in the direction of scrolling that meets or exceeds the `https://developer.android.com/reference/kotlin/android/view/ViewConfiguration#getScaledMinimumFlingVelocity()` along a scrollable axis.

If a nested scrolling parent is consuming motion as part of a `https://developer.android.com/reference/kotlin/android/view/ViewParent#onNestedPreScroll(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.IntArray)`, it may be appropriate for it to also consume the pre-fling to complete that same motion. By returning `true` from this method, the parent indicates that the child should not fling its own internal content as well.

| Parameters ||
|---|---|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View): View that initiated the nested scroll. This value cannot be `null`. |
| `velocityX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Horizontal velocity in pixels per second |
| `velocityY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Vertical velocity in pixels per second |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this parent consumed the fling ahead of the target view |

### onNestedPrePerformAccessibilityAction

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onNestedPrePerformAccessibilityAction(
    target: View, 
    action: Int, 
    args: Bundle?
): Boolean
```

React to an accessibility action delegated by a target descendant view before the target processes it.

This method may be called by a target descendant view if the target wishes to give a view in its parent chain a chance to react to the event before normal processing occurs. Most commonly this will be a scroll event such as `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SCROLL_FORWARD:kotlin.Int`. A ViewParent that supports acting as a nested scrolling parent should override this method and act accordingly to implement scrolling via accesibility systems.

Subclasses should always call `super.onNestedPrePerformAccessibilityAction`

| Parameters ||
|---|---|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View): The target view dispatching this action |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Action being performed; see `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo` |
| `arguments` | Optional action arguments. This value may be `null`. |
| `args` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: Optional action arguments |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | false by default. Subclasses should return true if they handle the event. |

### onNestedPreScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onNestedPreScroll(
    target: View, 
    dx: Int, 
    dy: Int, 
    consumed: IntArray
): Unit
```

React to a nested scroll in progress before the target view consumes a portion of the scroll.

When working with nested scrolling often the parent view may want an opportunity to consume the scroll before the nested scrolling child does. An example of this is a drawer that contains a scrollable list. The user will want to be able to scroll the list fully into view before the list itself begins scrolling.

`onNestedPreScroll` is called when a nested scrolling child invokes `https://developer.android.com/reference/kotlin/android/view/View#dispatchNestedPreScroll(kotlin.Int,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.IntArray)`. The implementation should report how any pixels of the scroll reported by dx, dy were consumed in the `consumed` array. Index 0 corresponds to dx and index 1 corresponds to dy. This parameter will never be null. Initial values for consumed\[0\] and consumed\[1\] will always be 0.

| Parameters ||
|---|---|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View): View that initiated the nested scroll. This value cannot be `null`. |
| `dx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Horizontal scroll distance in pixels |
| `dy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Vertical scroll distance in pixels |
| `consumed` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): Output. The horizontal and vertical scroll distance consumed by this parent. This value cannot be `null`. |

### onNestedScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onNestedScroll(
    target: View, 
    dxConsumed: Int, 
    dyConsumed: Int, 
    dxUnconsumed: Int, 
    dyUnconsumed: Int
): Unit
```

React to a nested scroll in progress.

This method will be called when the ViewParent's current nested scrolling child view dispatches a nested scroll event. To receive calls to this method the ViewParent must have previously returned `true` for a call to `https://developer.android.com/reference/kotlin/android/view/ViewParent#onStartNestedScroll(android.view.View,%20android.view.View,%20kotlin.Int)`.

Both the consumed and unconsumed portions of the scroll distance are reported to the ViewParent. An implementation may choose to use the consumed portion to match or chase scroll position of multiple child elements, for example. The unconsumed portion may be used to allow continuous dragging of multiple scrolling or draggable elements, such as scrolling a list within a vertical drawer where the drawer begins dragging once the edge of inner scrolling content is reached.

| Parameters ||
|---|---|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View): The descendent view controlling the nested scroll. This value cannot be `null`. |
| `dxConsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Horizontal scroll distance in pixels already consumed by target |
| `dyConsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Vertical scroll distance in pixels already consumed by target |
| `dxUnconsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Horizontal scroll distance in pixels not consumed by target |
| `dyUnconsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Vertical scroll distance in pixels not consumed by target |

### onNestedScrollAccepted

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onNestedScrollAccepted(
    child: View, 
    target: View, 
    axes: Int
): Unit
```

React to the successful claiming of a nested scroll operation.

This method will be called after `https://developer.android.com/reference/kotlin/android/view/ViewParent#onStartNestedScroll(android.view.View,%20android.view.View,%20kotlin.Int)` returns true. It offers an opportunity for the view and its superclasses to perform initial configuration for the nested scroll. Implementations of this method should always call their superclass's implementation of this method if one is present.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View): Direct child of this ViewParent containing target. This value cannot be `null`. |
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View): View that initiated the nested scroll. This value cannot be `null`. |
| `nestedScrollAxes` | Flags consisting of `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_HORIZONTAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_VERTICAL:kotlin.Int` or both |

### onRequestSendAccessibilityEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onRequestSendAccessibilityEvent(
    child: View!, 
    event: AccessibilityEvent!
): Boolean
```

Called when a child has requested sending an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent` and gives an opportunity to its parent to augment the event.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate` has been specified via calling `https://developer.android.com/reference/kotlin/android/view/View#setAccessibilityDelegate(android.view.View.AccessibilityDelegate)` its `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate#onRequestSendAccessibilityEvent(android.view.ViewGroup,%20android.view.View,%20android.view.accessibility.AccessibilityEvent)` is responsible for handling this call.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The child which requests sending the event. |
| `event` | [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent)!: The event to be sent. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event should be sent. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#requestSendAccessibilityEvent(android.view.View,%20android.view.accessibility.AccessibilityEvent)`

### onResolvePointerIcon

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onResolvePointerIcon(
    event: MotionEvent!, 
    pointerIndex: Int
): PointerIcon!
```

Resolve the pointer icon that should be used for specified pointer in the motion event. The default implementation will resolve the pointer icon to one set using `https://developer.android.com/reference/kotlin/android/view/View#setPointerIcon(android.view.PointerIcon)` for mouse devices. Subclasses may override this to customize the icon for the given pointer. For example, to always show the PointerIcon.TYPE_HANDWRITING icon for a stylus pointer, the event can be resolved in the following way: `
`

 @Override
 public PointerIcon onResolvePointerIcon(MotionEvent event, int pointerIndex) {
 final int toolType = event.getToolType(pointerIndex);
 if (!event.isFromSource(InputDevice.SOURCE_MOUSE)
 && event.isFromSource(InputDevice.SOURCE_STYLUS)
 && (toolType == MotionEvent.TOOL_TYPE_STYLUS
 || toolType == MotionEvent.TOOL_TYPE_ERASER)) {
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
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!: The `https://developer.android.com/reference/kotlin/android/view/MotionEvent` that requires a pointer icon to be resolved for one of pointers. |
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the pointer in `event` for which to retrieve the `https://developer.android.com/reference/kotlin/android/view/PointerIcon`. This will be between 0 and `https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount()`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/PointerIcon!` | the pointer icon to use for specified pointer, or `null` if a pointer icon is not specified and the default icon should be used. |

### onStartNestedScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStartNestedScroll(
    child: View, 
    target: View, 
    nestedScrollAxes: Int
): Boolean
```

React to a descendant view initiating a nestable scroll operation, claiming the nested scroll operation if appropriate.

This method will be called in response to a descendant view invoking `https://developer.android.com/reference/kotlin/android/view/View#startNestedScroll(kotlin.Int)`. Each parent up the view hierarchy will be given an opportunity to respond and claim the nested scrolling operation by returning `true`.

This method may be overridden by ViewParent implementations to indicate when the view is willing to support a nested scrolling operation that is about to begin. If it returns true, this ViewParent will become the target view's nested scrolling parent for the duration of the scroll operation in progress. When the nested scroll is finished this ViewParent will receive a call to `https://developer.android.com/reference/kotlin/android/view/ViewParent#onStopNestedScroll(android.view.View)`.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View): Direct child of this ViewParent containing target. This value cannot be `null`. |
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View): View that initiated the nested scroll. This value cannot be `null`. |
| `nestedScrollAxes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags consisting of `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_HORIZONTAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_VERTICAL:kotlin.Int` or both |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this ViewParent accepts the nested scroll operation |

### onStopNestedScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStopNestedScroll(child: View): Unit
```

React to a nested scroll operation ending.

Perform cleanup after a nested scrolling operation. This method will be called when a nested scroll stops, for example when a nested touch scroll ends with a `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_UP:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_CANCEL:kotlin.Int` event. Implementations of this method should always call their superclass's implementation of this method if one is present.

The default implementation of onStopNestedScroll calls `https://developer.android.com/reference/kotlin/android/view/View#stopNestedScroll()` to halt any recursive nested scrolling in progress.

| Parameters ||
|---|---|
| `target` | View that initiated the nested scroll. This value cannot be `null`. |

### onViewAdded

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onViewAdded(child: View!): Unit
```

Called when a new child is added to this ViewGroup. Overrides should always call super.onViewAdded.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the added child view |

### onViewRemoved

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onViewRemoved(child: View!): Unit
```

Called when a child view is removed from this ViewGroup. Overrides should always call super.onViewRemoved.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the removed child view |

### propagateRequestedFrameRate

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun propagateRequestedFrameRate(
    frameRate: Float, 
    forceOverride: Boolean
): Unit
```

You can set the preferred frame rate for a ViewGroup and its children using a positive number or by specifying the preferred frame rate category using constants, including REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE, REQUESTED_FRAME_RATE_CATEGORY_LOW, REQUESTED_FRAME_RATE_CATEGORY_NORMAL, REQUESTED_FRAME_RATE_CATEGORY_HIGH. Keep in mind that the preferred frame rate affects the frame rate for the next frame, so use this method carefully. It's important to note that the preference is valid as long as the ViewGroup or any of its children is invalidated. To undo the frame rate propagation, call the API with REQUESTED_FRAME_RATE_CATEGORY_DEFAULT.

| Parameters ||
|---|---|
| `frameRate` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the preferred frame rate of the ViewGroup. |
| `forceOverride` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): indicate whether it should override the frame rate of all the children with the given frame rate. |

### recomputeViewAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun recomputeViewAttributes(child: View!): Unit
```

Tell view hierarchy that the global view attributes need to be re-evaluated.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: View whose attributes have changed. |

### removeAllViews

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAllViews(): Unit
```

Call this method to remove all child views from the ViewGroup.

**Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method.

### removeAllViewsInLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAllViewsInLayout(): Unit
```

Called by a ViewGroup subclass to remove child views from itself, when it must first know its size on screen before it can calculate how many child views it will render. An example is a Gallery or a ListView, which may "have" 50 children, but actually only render the number of children that can currently fit inside the object on screen. Do not call this method unless you are extending ViewGroup and understand the view measuring and layout pipeline.

**Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method.

### removeView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeView(view: View!): Unit
```

**Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method.

### removeViewAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeViewAt(index: Int): Unit
```

Removes the view at the specified position in the group.

**Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position in the group of the view to remove |

### removeViewInLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeViewInLayout(view: View!): Unit
```

Removes a view during layout. This is useful if in your onLayout() method, you need to remove more views.

**Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the view to remove from the group |

### removeViews

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeViews(
    start: Int, 
    count: Int
): Unit
```

Removes the specified range of views from the group.

**Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first position in the group of the range of views to remove |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of views to remove |

### removeViewsInLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeViewsInLayout(
    start: Int, 
    count: Int
): Unit
```

Removes a range of views during layout. This is useful if in your onLayout() method, you need to remove more views.

**Note:** do not invoke this method from `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)` or any related method.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first view to remove from the group |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of views to remove from the group |

### requestChildFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestChildFocus(
    child: View!, 
    focused: View!
): Unit
```

Called when a child of this parent wants focus

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The child of this ViewParent that wants focus. This view will contain the focused view. It is not necessarily the view that actually has focus. |
| `focused` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The view that is a descendant of child that actually has focus |

### requestChildRectangleOnScreen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestChildRectangleOnScreen(
    child: View, 
    rectangle: Rect!, 
    immediate: Boolean
): Boolean
```

Called when a child of this group wants a particular rectangle to be positioned onto the screen. `https://developer.android.com/reference/kotlin/android/view/ViewGroup#`s overriding this can trust that:

- `child` will be a direct child of this group
- `rectangle` will be in the child's content coordinates

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewGroup#`s overriding this should uphold the contract:

- nothing will change if the rectangle is already visible
- the view port will be scrolled only just enough to make the rectangle visible

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View): The direct child making the request. This value cannot be `null`. |
| `rectangle` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!: The rectangle in the child's coordinates the child wishes to be on the screen. |
| `immediate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True to forbid animated or delayed scrolling, false otherwise |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the group scrolled to handle the operation |

### requestChildRectangleOnScreen

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestChildRectangleOnScreen(
    child: View, 
    rectangle: Rect, 
    immediate: Boolean, 
    source: Int
): Boolean
```

Called when a child of this group wants a particular rectangle to be positioned onto the screen. `https://developer.android.com/reference/kotlin/android/view/ViewGroup#`s overriding this can trust that:

- `child` will be a direct child of this group
- `rectangle` will be in the child's content coordinates

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewGroup#`s overriding this should uphold the contract:

- nothing will change if the rectangle is already visible
- the view port will be scrolled only just enough to make the rectangle visible

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View): This value cannot be `null`. |
| `rectangle` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): This value cannot be `null`. |
| `immediate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True to forbid animated or delayed scrolling, false otherwise |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the group scrolled to handle the operation |

### requestDisallowInterceptTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestDisallowInterceptTouchEvent(disallowIntercept: Boolean): Unit
```

Called when a child does not want this parent and its ancestors to intercept touch events with `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onInterceptTouchEvent(android.view.MotionEvent)`.

This parent should pass this call onto its parents. This parent must obey this request for the duration of the touch (that is, only clear the flag after this parent has received an up or a cancel.

| Parameters ||
|---|---|
| `disallowIntercept` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the child does not want the parent to intercept touch events. |

### requestFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestFocus(
    direction: Int, 
    previouslyFocusedRect: Rect!
): Boolean
```

Call this to try to give focus to a specific view or to one of its descendants and give it hints about the direction and a specific rectangle that the focus is coming from. The rectangle can help give larger views a finer grained hint about where focus is coming from, and therefore, where to show selection, or forward focus change internally. A view will not actually take focus if it is not focusable (`https://developer.android.com/reference/kotlin/android/view/View#isFocusable()` returns false), or if it is focusable and it is not focusable in touch mode (`https://developer.android.com/reference/kotlin/android/view/View#isFocusableInTouchMode()`) while the device is in touch mode. A View will not take focus if it is not visible. A View will not take focus if one of its parents has `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getDescendantFocusability()` equal to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_BLOCK_DESCENDANTS:kotlin.Int`. See also `https://developer.android.com/reference/kotlin/android/view/View#focusSearch(kotlin.Int)`, which is what you call to say that you have focus, and you want your parent to look for the next one. You may wish to override this method if your custom `https://developer.android.com/reference/kotlin/android/view/View` has an internal `https://developer.android.com/reference/kotlin/android/view/View` that it wishes to forward the request to. Looks for a view to give focus to respecting the setting specified by `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getDescendantFocusability()`. Uses `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onRequestFocusInDescendants(kotlin.Int,%20android.graphics.Rect)` to find focus within the children of this group when appropriate.

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of FOCUS_UP, FOCUS_DOWN, FOCUS_LEFT, and FOCUS_RIGHT |
| `previouslyFocusedRect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!: The rectangle (in this View's coordinate system) to give a finer grained hint about where focus is coming from. May be null if there is no hint. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether this view or one of its descendants actually took focus. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_BEFORE_DESCENDANTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_AFTER_DESCENDANTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_BLOCK_DESCENDANTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#onRequestFocusInDescendants(kotlin.Int,%20android.graphics.Rect)`

### requestSendAccessibilityEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestSendAccessibilityEvent(
    child: View, 
    event: AccessibilityEvent!
): Boolean
```

Called by a child to request from its parent to send an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent`. The child has already populated a record for itself in the event and is delegating to its parent to send the event. The parent can optionally add a record for itself.

Note: An accessibility event is fired by an individual view which populates the event with a record for its state and requests from its parent to perform the sending. The parent can optionally add a record for itself before dispatching the request to its parent. A parent can also choose not to respect the request for sending the event. The accessibility event is sent by the topmost view in the view tree.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View): The child which requests sending the event. This value cannot be `null`. |
| `event` | [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent)!: The event to be sent. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was sent. |

### requestTransparentRegion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestTransparentRegion(child: View!): Unit
```

Called when a child wants the view hierarchy to gather and report transparent regions to the window compositor. Views that "punch" holes in the view hierarchy, such as SurfaceView can use this API to improve performance of the system. When no such a view is present in the hierarchy, this optimization in unnecessary and might slightly reduce the view hierarchy performance.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the view requesting the transparent region computation |

### restoreDefaultFocus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun restoreDefaultFocus(): Boolean
```

Gives focus to the default-focus view in the view hierarchy that has this view as a root. If the default-focus view cannot be found, falls back to calling `https://developer.android.com/reference/kotlin/android/view/View#requestFocus(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether this view or one of its descendants actually took focus |

### scheduleLayoutAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun scheduleLayoutAnimation(): Unit
```

Schedules the layout animation to be played after the next layout pass of this view group. This can be used to restart the layout animation when the content of the view group changes or when the activity is paused and resumed.

### setAddStatesFromChildren

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAddStatesFromChildren(addsStates: Boolean): Unit
```

Sets whether this ViewGroup's drawable states also include its children's drawable states. This is used, for example, to make a group appear to be focused when its child EditText or button is focused.

### setAlwaysDrawnWithCacheEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAlwaysDrawnWithCacheEnabled(always: Boolean): Unit
```

**Deprecated:** *As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, this property is ignored. Child views may no longer have their caching behavior disabled by parents.*

Indicates whether this ViewGroup will always try to draw its children using their drawing cache. This property can be set to true when the cache rendering is slightly different from the children's normal rendering. Renderings can be different, for instance, when the cache's quality is set to low. When this property is disabled, the ViewGroup will use the drawing cache of its children only when asked to. It's usually the task of subclasses to tell ViewGroup when to start using the drawing cache and when to stop using it.

| Parameters ||
|---|---|
| `always` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to always draw with the drawing cache, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isAlwaysDrawnWithCacheEnabled()`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setChildrenDrawnWithCacheEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/View#setDrawingCacheEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/View#setDrawingCacheQuality(kotlin.Int)`

### setAnimationCacheEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAnimationCacheEnabled(enabled: Boolean): Unit
```

**Deprecated:** *As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, this property is ignored. Caching behavior of children may be controlled through `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)`.*

Enables or disables the children's drawing cache during a layout animation. By default, the drawing cache is enabled but this will prevent nested layout animations from working. To nest animations, you must disable the cache.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable the animation cache, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isAnimationCacheEnabled()`
- `https://developer.android.com/reference/kotlin/android/view/View#setDrawingCacheEnabled(kotlin.Boolean)`

### setClipChildren

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setClipChildren(clipChildren: Boolean): Unit
```

By default, children are clipped to their bounds before drawing. This allows view groups to override this behavior for animations, etc.

| Parameters ||
|---|---|
| `clipChildren` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to clip children to their bounds, false otherwise |

### setClipToPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setClipToPadding(clipToPadding: Boolean): Unit
```

Sets whether this ViewGroup will clip its children to its padding and resize (but not clip) any EdgeEffect to the padded region, if padding is present.

By default, children are clipped to the padding of their parent ViewGroup. This clipping behavior is only enabled if padding is non-zero.

| Parameters ||
|---|---|
| `clipToPadding` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to clip children to the padding of the group, and resize (but not clip) any EdgeEffect to the padded region. False otherwise. |

### setDescendantFocusability

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDescendantFocusability(focusability: Int): Unit
```

Set the descendant focusability of this view group. This defines the relationship between this view group and its descendants when looking for a view to take focus in `https://developer.android.com/reference/kotlin/android/view/ViewGroup#requestFocus(kotlin.Int,%20android.graphics.Rect)`.

| Parameters ||
|---|---|
| `focusability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_BEFORE_DESCENDANTS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_AFTER_DESCENDANTS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#FOCUS_BLOCK_DESCENDANTS:kotlin.Int`. |

### setLayoutAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayoutAnimation(controller: LayoutAnimationController!): Unit
```

Sets the layout animation controller used to animate the group's children after the first layout.

| Parameters ||
|---|---|
| `controller` | [LayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController)!: the animation controller |

### setLayoutAnimationListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayoutAnimationListener(animationListener: Animation.AnimationListener!): Unit
```

Specifies the animation listener to which layout animation events must be sent. Only `https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener#onAnimationStart(android.view.animation.Animation)` and `https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener#onAnimationEnd(android.view.animation.Animation)` are invoked.

| Parameters ||
|---|---|
| `animationListener` | [Animation.AnimationListener](https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener)!: the layout animation listener |

### setLayoutMode

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayoutMode(layoutMode: Int): Unit
```

Sets the basis of alignment during the layout of this ViewGroup. Valid values are either `https://developer.android.com/reference/kotlin/android/view/ViewGroup#LAYOUT_MODE_CLIP_BOUNDS:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/ViewGroup#LAYOUT_MODE_OPTICAL_BOUNDS:kotlin.Int`.

| Parameters ||
|---|---|
| `layoutMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the layout mode to use during layout operations |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getLayoutMode()`

### setLayoutTransition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayoutTransition(transition: LayoutTransition!): Unit
```

Sets the LayoutTransition object for this ViewGroup. If the LayoutTransition object is not null, changes in layout which occur because of children being added to or removed from the ViewGroup will be animated according to the animations defined in that LayoutTransition object. By default, the transition object is null (so layout changes are not animated).

Replacing a non-null transition will cause that previous transition to be canceled, if it is currently running, to restore this container to its correct post-transition state.

| Parameters ||
|---|---|
| `transition` | [LayoutTransition](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.html#)!: The LayoutTransition object that will animated changes in layout. A value of `null` means no transition will run on layout changes. |

### setMotionEventSplittingEnabled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMotionEventSplittingEnabled(split: Boolean): Unit
```

Enable or disable the splitting of MotionEvents to multiple children during touch event dispatch. This behavior is enabled by default for applications that target an SDK version of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` or newer.

When this option is enabled MotionEvents may be split and dispatched to different child views depending on where each pointer initially went down. This allows for user interactions such as scrolling two panes of content independently, chording of buttons, and performing independent gestures on different pieces of content.

| Parameters ||
|---|---|
| `split` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` to allow MotionEvents to be split and dispatched to multiple child views. `false` to only allow one child view to be the target of any MotionEvent received by this ViewGroup. |

### setOnHierarchyChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnHierarchyChangeListener(listener: ViewGroup.OnHierarchyChangeListener!): Unit
```

Register a callback to be invoked when a child is added to or removed from this view.

| Parameters ||
|---|---|
| `listener` | [ViewGroup.OnHierarchyChangeListener](https://developer.android.com/reference/kotlin/android/view/ViewGroup.OnHierarchyChangeListener)!: the callback to invoke on hierarchy change |

### setPersistentDrawingCache

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPersistentDrawingCache(drawingCacheToKeep: Int): Unit
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)` on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the `https://developer.android.com/reference/kotlin/android/view/PixelCopy` API is recommended.*

Indicates what types of drawing caches should be kept in memory after they have been created.

| Parameters ||
|---|---|
| `drawingCacheToKeep` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one or a combination of `https://developer.android.com/reference/kotlin/android/view/ViewGroup#PERSISTENT_NO_CACHE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#PERSISTENT_ANIMATION_CACHE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/ViewGroup#PERSISTENT_SCROLLING_CACHE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/ViewGroup#PERSISTENT_ALL_CACHES:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getPersistentDrawingCache()`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setAnimationCacheEnabled(kotlin.Boolean)`

### setRequestedFrameRate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRequestedFrameRate(frameRate: Float): Unit
```

You can set the preferred frame rate for a ViewGroup using a positive number or by specifying the preferred frame rate category using constants, including REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE, REQUESTED_FRAME_RATE_CATEGORY_LOW, REQUESTED_FRAME_RATE_CATEGORY_NORMAL, REQUESTED_FRAME_RATE_CATEGORY_HIGH. Keep in mind that the preferred frame rate affects the frame rate for the next frame, so use this method carefully. It's important to note that the preference is valid as long as the ViewGroup is invalidated. Please also be aware that the requested frame rate will not propagate to child views.

| Parameters ||
|---|---|
| `frameRate` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the preferred frame rate of the ViewGroup. |

### setTouchscreenBlocksFocus

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTouchscreenBlocksFocus(touchscreenBlocksFocus: Boolean): Unit
```

Set whether this ViewGroup should ignore focus requests for itself and its children. If this option is enabled and the ViewGroup or a descendant currently has focus, focus will proceed forward.

| Parameters ||
|---|---|
| `touchscreenBlocksFocus` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable blocking focus in the presence of a touchscreen |

### setTransitionGroup

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTransitionGroup(isTransitionGroup: Boolean): Unit
```

Changes whether or not this ViewGroup should be treated as a single entity during Activity Transitions.

| Parameters ||
|---|---|
| `isTransitionGroup` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether or not the ViewGroup should be treated as a unit in Activity transitions. If false, the ViewGroup won't transition, only its children. If true, the entire ViewGroup will transition together. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#makeSceneTransitionAnimation(android.app.Activity,%20android.util.Pair)`

### setWindowInsetsAnimationCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWindowInsetsAnimationCallback(callback: WindowInsetsAnimation.Callback?): Unit
```

Sets a `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback` to be notified about animations of windows that cause insets.

The callback's `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback#getDispatchMode()` will affect whether animation callbacks are dispatched to the children of this view.

| Parameters ||
|---|---|
| `callback` | [WindowInsetsAnimation.Callback](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback)?: This value may be `null`. |

### shouldDelayChildPressedState

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun shouldDelayChildPressedState(): Boolean
```

Return true if the pressed state should be delayed for children or descendants of this ViewGroup. Generally, this should be done for containers that can scroll, such as a List. This prevents the pressed state from appearing when the user is actually trying to scroll the content. The default implementation returns true for compatibility reasons. Subclasses that do not scroll should generally override this method and return false.

### showContextMenuForChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun showContextMenuForChild(originalView: View!): Boolean
```

Shows the context menu for the specified view or its ancestors.

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, `https://developer.android.com/reference/kotlin/android/view/ViewManager#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)`) then it should override this and show the context menu.

| Parameters ||
|---|---|
| `originalView` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the source view where the context menu was first invoked |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the context menu was shown, `false` otherwise |

### showContextMenuForChild

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun showContextMenuForChild(
    originalView: View!, 
    x: Float, 
    y: Float
): Boolean
```

Shows the context menu for the specified view or its ancestors anchored to the specified view-relative coordinate.

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, `https://developer.android.com/reference/kotlin/android/view/ViewManager#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)`) then it should override this and show the context menu.

If a subclass overrides this method it should also override `https://developer.android.com/reference/kotlin/android/view/ViewParent#showContextMenuForChild(android.view.View)`.

| Parameters ||
|---|---|
| `originalView` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the source view where the context menu was first invoked |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the X coordinate in pixels relative to the original view to which the menu should be anchored, or `https://developer.android.com/reference/kotlin/java/lang/Float.html#NaN:kotlin.Float` to disable anchoring |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the Y coordinate in pixels relative to the original view to which the menu should be anchored, or `https://developer.android.com/reference/kotlin/java/lang/Float.html#NaN:kotlin.Float` to disable anchoring |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the context menu was shown, `false` otherwise |

### startActionModeForChild

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startActionModeForChild(
    originalView: View!, 
    callback: ActionMode.Callback!
): ActionMode!
```

Start an action mode for the specified view with the default type `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int`.

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, `https://developer.android.com/reference/kotlin/android/view/ViewManager#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)`) then it should override this and start the action mode.

| Parameters ||
|---|---|
| `originalView` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The source view where the action mode was first invoked |
| `callback` | [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback)!: The callback that will handle lifecycle events for the action mode |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ActionMode!` | The new action mode if it was started, null otherwise |

### startActionModeForChild

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startActionModeForChild(
    originalView: View!, 
    callback: ActionMode.Callback!, 
    type: Int
): ActionMode!
```

Start an action mode of a specific type for the specified view.

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, `https://developer.android.com/reference/kotlin/android/view/ViewManager#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)`) then it should override this and start the action mode.

| Parameters ||
|---|---|
| `originalView` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The source view where the action mode was first invoked |
| `callback` | [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback)!: The callback that will handle lifecycle events for the action mode |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_FLOATING:kotlin.Int`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ActionMode!` | The new action mode if it was started, null otherwise |

### startLayoutAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startLayoutAnimation(): Unit
```

Runs the layout animation. Calling this method triggers a relayout of this view group.

### startViewTransition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startViewTransition(view: View!): Unit
```

This method tells the ViewGroup that the given View object, which should have this ViewGroup as its parent, should be kept around (re-displayed when the ViewGroup draws its children) even if it is removed from its parent. This allows animations, such as those used by `https://developer.android.com/reference/kotlin/android/app/Fragment.html#` and `https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.html#` to animate the removal of views. A call to this method should always be accompanied by a later call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#endViewTransition(android.view.View)`, such as after an animation on the View has finished, so that the View finally gets removed.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The View object to be kept visible even if it gets removed from its parent. |

### suppressLayout

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun suppressLayout(suppress: Boolean): Unit
```

Tells this ViewGroup to suppress all layout() calls until layout suppression is disabled with a later call to suppressLayout(false). When layout suppression is disabled, a requestLayout() call is sent if layout() was attempted while layout was being suppressed.

### updateViewLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateViewLayout(
    view: View!, 
    params: ViewGroup.LayoutParams!
): Unit
```

## Protected methods

### addViewInLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun addViewInLayout(
    child: View!, 
    index: Int, 
    params: ViewGroup.LayoutParams!
): Boolean
```

Adds a view during layout. This is useful if in your onLayout() method, you need to add more views (as does the list view for example). If index is negative, it means put it at the end of the list.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the view to add to the group |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index at which the child must be added or -1 to add last |
| `params` | [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams)!: the layout parameters to associate with the child |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the child was added, false otherwise |

### addViewInLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun addViewInLayout(
    child: View!, 
    index: Int, 
    params: ViewGroup.LayoutParams!, 
    preventRequestLayout: Boolean
): Boolean
```

Adds a view during layout. This is useful if in your onLayout() method, you need to add more views (as does the list view for example). If index is negative, it means put it at the end of the list.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the view to add to the group |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index at which the child must be added or -1 to add last |
| `params` | [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams)!: the layout parameters to associate with the child |
| `preventRequestLayout` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, calling this method will not trigger a layout request on child |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the child was added, false otherwise |

### attachLayoutAnimationParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun attachLayoutAnimationParameters(
    child: View!, 
    params: ViewGroup.LayoutParams!, 
    index: Int, 
    count: Int
): Unit
```

Subclasses should override this method to set layout animation parameters on the supplied child.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the child to associate with animation parameters |
| `params` | [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams)!: the child's layout parameters which hold the animation parameters |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the child in the view group |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of children in the view group |

### attachViewToParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun attachViewToParent(
    child: View!, 
    index: Int, 
    params: ViewGroup.LayoutParams!
): Unit
```

Attaches a view to this view group. Attaching a view assigns this group as the parent, sets the layout parameters and puts the view in the list of children so that it can be retrieved by calling `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildAt(kotlin.Int)`.

This method is intended to be lightweight and makes no assumptions about whether the parent or child should be redrawn. Proper use of this method will include also making any appropriate #requestLayout() or `https://developer.android.com/reference/kotlin/android/view/View#invalidate()` calls. For example, callers can `https://developer.android.com/reference/kotlin/android/view/View#post(java.lang.Runnable)` a `https://developer.android.com/reference/kotlin/java/lang/Runnable.html#` which performs a #requestLayout() on the next frame, after all detach/attach calls are finished, causing layout to be run prior to redrawing the view hierarchy.

This method should be called only for views which were detached from their parent.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the child to attach |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index at which the child should be attached |
| `params` | [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams)!: the layout parameters of the child |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeDetachedView(android.view.View,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachAllViewsFromParent()`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(kotlin.Int)`

### canAnimate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun canAnimate(): Boolean
```

Indicates whether the view group has the ability to animate its children after the first layout.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the children can be animated, false otherwise |

### checkLayoutParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun checkLayoutParams(p: ViewGroup.LayoutParams!): Boolean
```

### cleanupLayoutState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun cleanupLayoutState(child: View!): Unit
```

Prevents the specified child to be laid out during the next layout pass.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the child on which to perform the cleanup |

### debug

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun debug(depth: Int): Unit
```

### detachAllViewsFromParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun detachAllViewsFromParent(): Unit
```

Detaches all views from the parent. Detaching a view should be followed either by a call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#attachViewToParent(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams)` or a call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeDetachedView(android.view.View,%20kotlin.Boolean)`. Detachment should only be temporary; reattachment or removal should happen within the same drawing cycle as detachment. When a view is detached, its parent is null and cannot be retrieved by a call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildAt(kotlin.Int)`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewsFromParent(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#attachViewToParent(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeDetachedView(android.view.View,%20kotlin.Boolean)`

### detachViewFromParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun detachViewFromParent(child: View!): Unit
```

Detaches a view from its parent. Detaching a view should be followed either by a call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#attachViewToParent(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams)` or a call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeDetachedView(android.view.View,%20kotlin.Boolean)`. Detachment should only be temporary; reattachment or removal should happen within the same drawing cycle as detachment. When a view is detached, its parent is null and cannot be retrieved by a call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildAt(kotlin.Int)`.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the child to detach |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewsFromParent(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachAllViewsFromParent()`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#attachViewToParent(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeDetachedView(android.view.View,%20kotlin.Boolean)`

### detachViewFromParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun detachViewFromParent(index: Int): Unit
```

Detaches a view from its parent. Detaching a view should be followed either by a call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#attachViewToParent(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams)` or a call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeDetachedView(android.view.View,%20kotlin.Boolean)`. Detachment should only be temporary; reattachment or removal should happen within the same drawing cycle as detachment. When a view is detached, its parent is null and cannot be retrieved by a call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildAt(kotlin.Int)`.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the child to detach |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachAllViewsFromParent()`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewsFromParent(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#attachViewToParent(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeDetachedView(android.view.View,%20kotlin.Boolean)`

### detachViewsFromParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun detachViewsFromParent(
    start: Int, 
    count: Int
): Unit
```

Detaches a range of views from their parents. Detaching a view should be followed either by a call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#attachViewToParent(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams)` or a call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeDetachedView(android.view.View,%20kotlin.Boolean)`. Detachment should only be temporary; reattachment or removal should happen within the same drawing cycle as detachment. When a view is detached, its parent is null and cannot be retrieved by a call to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildAt(kotlin.Int)`.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first index of the childrend range to detach |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of children to detach |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachAllViewsFromParent()`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#attachViewToParent(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#removeDetachedView(android.view.View,%20kotlin.Boolean)`

### dispatchDraw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchDraw(canvas: Canvas): Unit
```

Called by draw to draw the child views. This may be overridden by derived classes to gain control just before its children are drawn (but after its own view has been drawn).

| Parameters ||
|---|---|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#): This value cannot be `null`. |

### dispatchFreezeSelfOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchFreezeSelfOnly(container: SparseArray<Parcelable!>!): Unit
```

Perform dispatching of a `https://developer.android.com/reference/kotlin/android/view/View#saveHierarchyState(android.util.SparseArray)` freeze()} to only this view, not to its children. For use when overriding `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchSaveInstanceState(android.util.SparseArray)` dispatchFreeze()} to allow subclasses to freeze their own state but not the state of their children.

| Parameters ||
|---|---|
| `container` | [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)\< [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)!\>!: the container |

### dispatchGenericFocusedEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchGenericFocusedEvent(event: MotionEvent!): Boolean
```

Dispatch a generic motion event to the currently focused view.

Do not call this method directly. Call `https://developer.android.com/reference/kotlin/android/view/View#dispatchGenericMotionEvent(android.view.MotionEvent)` instead.

| Parameters ||
|---|---|
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!: The motion event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

### dispatchGenericPointerEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchGenericPointerEvent(event: MotionEvent!): Boolean
```

Dispatch a generic motion event to the view under the first pointer.

Do not call this method directly. Call `https://developer.android.com/reference/kotlin/android/view/View#dispatchGenericMotionEvent(android.view.MotionEvent)` instead.

| Parameters ||
|---|---|
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!: The motion event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

### dispatchHoverEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchHoverEvent(event: MotionEvent!): Boolean
```

Dispatch a hover event.

Do not call this method directly. Call `https://developer.android.com/reference/kotlin/android/view/View#dispatchGenericMotionEvent(android.view.MotionEvent)` instead.

| Parameters ||
|---|---|
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!: The motion event to be dispatched. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled by the view, false otherwise. |

### dispatchRestoreInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchRestoreInstanceState(container: SparseArray<Parcelable!>!): Unit
```

Called by `https://developer.android.com/reference/kotlin/android/view/View#restoreHierarchyState(android.util.SparseArray)` to retrieve the state for this view and its children. May be overridden to modify how restoring happens to a view's children; for example, some views may want to not store state for their children.

| Parameters ||
|---|---|
| `container` | [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)\< [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)!\>!: The SparseArray which holds previously saved state. |

### dispatchSaveInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchSaveInstanceState(container: SparseArray<Parcelable!>!): Unit
```

Called by `https://developer.android.com/reference/kotlin/android/view/View#saveHierarchyState(android.util.SparseArray)` to store the state for this view and its children. May be overridden to modify how freezing happens to a view's children; for example, some views may want to not store state for their children.

| Parameters ||
|---|---|
| `container` | [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)\< [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)!\>!: The SparseArray in which to save the view's state. |

### dispatchSetPressed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchSetPressed(pressed: Boolean): Unit
```

Dispatch setPressed to all of this View's children.

| Parameters ||
|---|---|
| `pressed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The new pressed state |

### dispatchThawSelfOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dispatchThawSelfOnly(container: SparseArray<Parcelable!>!): Unit
```

Perform dispatching of a `https://developer.android.com/reference/kotlin/android/view/View#restoreHierarchyState(android.util.SparseArray)` to only this view, not to its children. For use when overriding `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchRestoreInstanceState(android.util.SparseArray)` to allow subclasses to thaw their own state but not the state of their children.

| Parameters ||
|---|---|
| `container` | [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)\< [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)!\>!: the container |

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
| `changedView` | [View](https://developer.android.com/reference/kotlin/android/view/View): The view whose visibility changed. Could be 'this' or an ancestor view. This value cannot be `null`. |
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new visibility of changedView: `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#GONE:kotlin.Int` |

### drawChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun drawChild(
    canvas: Canvas, 
    child: View!, 
    drawingTime: Long
): Boolean
```

Draw one child of this View Group. This method is responsible for getting the canvas in the right state. This includes clipping, translating so that the child's scrolled origin is at 0, 0, and applying any animation transformations.

| Parameters ||
|---|---|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#): The canvas on which to draw the child. This value cannot be `null`. |
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: Who to draw |
| `drawingTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time at which draw is occurring |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if an invalidate() was issued |

### drawableStateChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun drawableStateChanged(): Unit
```

This function is called whenever the state of the view changes in such a way that it impacts the state of drawables being shown.

If the View has a StateListAnimator, it will also be called to run necessary state change animations.

Be sure to call through to the superclass when overriding this function. 
If you override this method you *must* call through to the superclass implementation.

### generateDefaultLayoutParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun generateDefaultLayoutParams(): ViewGroup.LayoutParams!
```

Returns a set of default layout parameters. These parameters are requested when the View passed to `https://developer.android.com/reference/kotlin/android/view/ViewGroup#addView(android.view.View)` has no layout parameters already set. If null is returned, an exception is thrown from addView.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!` | a set of default layout parameters or null |

### generateLayoutParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun generateLayoutParams(p: ViewGroup.LayoutParams!): ViewGroup.LayoutParams!
```

Returns a safe set of layout parameters based on the supplied layout params. When a ViewGroup is passed a View whose layout params do not pass the test of `https://developer.android.com/reference/kotlin/android/view/ViewGroup#checkLayoutParams(android.view.ViewGroup.LayoutParams)`, this method is invoked. This method should return a new set of layout params suitable for this ViewGroup, possibly by copying the appropriate attributes from the specified set of layout params.

| Parameters ||
|---|---|
| `p` | [ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams)!: The layout parameters to convert into a suitable set of layout parameters for this ViewGroup. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams!` | an instance of `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams` or one of its descendants |

### getChildDrawingOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getChildDrawingOrder(
    childCount: Int, 
    drawingPosition: Int
): Int
```

Converts drawing order position to container position. Override this if you want to change the drawing order of children. By default, it returns drawingPosition.

NOTE: In order for this method to be called, you must enable child ordering first by calling `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setChildrenDrawingOrderEnabled(kotlin.Boolean)`.

| Parameters ||
|---|---|
| `drawingPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the drawing order position. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the container position of a child for this drawing order position. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setChildrenDrawingOrderEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isChildrenDrawingOrderEnabled()`

### getChildStaticTransformation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getChildStaticTransformation(
    child: View!, 
    t: Transformation!
): Boolean
```

Sets `t` to be the static transformation of the child, if set, returning a boolean to indicate whether a static transform was set. The default implementation simply returns `false`; subclasses may override this method for different behavior. `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setStaticTransformationsEnabled(kotlin.Boolean)` must be set to true for this method to be called.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The child view whose static transform is being requested |
| `t` | [Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation)!: The Transformation which will hold the result |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the transformation was set, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setStaticTransformationsEnabled(kotlin.Boolean)`

### isChildrenDrawingOrderEnabled

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun isChildrenDrawingOrderEnabled(): Boolean
```

Indicates whether the ViewGroup is drawing its children in the order defined by `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildDrawingOrder(kotlin.Int,%20kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if children drawing order is defined by `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildDrawingOrder(kotlin.Int,%20kotlin.Int)`, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setChildrenDrawingOrderEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildDrawingOrder(kotlin.Int,%20kotlin.Int)`

### isChildrenDrawnWithCacheEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun isChildrenDrawnWithCacheEnabled(): Boolean
```

**Deprecated:** *As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, this property is ignored. Child views may no longer be forced to cache their rendering state by their parents. Use `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` on individual Views instead.*

Indicates whether the ViewGroup is currently drawing its children using their drawing cache.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if children should be drawn with their cache, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setAlwaysDrawnWithCacheEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setChildrenDrawnWithCacheEnabled(kotlin.Boolean)`

### measureChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun measureChild(
    child: View!, 
    parentWidthMeasureSpec: Int, 
    parentHeightMeasureSpec: Int
): Unit
```

Ask one of the children of this view to measure itself, taking into account both the MeasureSpec requirements for this view and its padding. The heavy lifting is done in getChildMeasureSpec.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The child to measure |
| `parentWidthMeasureSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width requirements for this view |
| `parentHeightMeasureSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height requirements for this view |

### measureChildWithMargins

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun measureChildWithMargins(
    child: View!, 
    parentWidthMeasureSpec: Int, 
    widthUsed: Int, 
    parentHeightMeasureSpec: Int, 
    heightUsed: Int
): Unit
```

Ask one of the children of this view to measure itself, taking into account both the MeasureSpec requirements for this view and its padding and margins. The child must have MarginLayoutParams The heavy lifting is done in getChildMeasureSpec.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The child to measure |
| `parentWidthMeasureSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width requirements for this view |
| `widthUsed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Extra space that has been used up by the parent horizontally (possibly by other children of the parent) |
| `parentHeightMeasureSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height requirements for this view |
| `heightUsed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Extra space that has been used up by the parent vertically (possibly by other children of the parent) |

### measureChildren

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun measureChildren(
    widthMeasureSpec: Int, 
    heightMeasureSpec: Int
): Unit
```

Ask all of the children of this view to measure themselves, taking into account both the MeasureSpec requirements for this view and its padding. We skip children that are in the GONE state The heavy lifting is done in getChildMeasureSpec.

| Parameters ||
|---|---|
| `widthMeasureSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width requirements for this view |
| `heightMeasureSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height requirements for this view |

### onAttachedToWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onAttachedToWindow(): Unit
```

This is called when the view is attached to a window. At this point it has a Surface and will start drawing. Note that this function is guaranteed to be called before `https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas)`, however it may be called any time before the first onDraw -- including before or after `https://developer.android.com/reference/kotlin/android/view/View#onMeasure(kotlin.Int,%20kotlin.Int)`. 
If you override this method you *must* call through to the superclass implementation.

### onCreateDrawableState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onCreateDrawableState(extraSpace: Int): IntArray!
```

Generate the new `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` state for this view. This is called by the view system when the cached Drawable state is determined to be invalid. To retrieve the current state, you should use `https://developer.android.com/reference/kotlin/android/view/View#getDrawableState()`.

| Parameters ||
|---|---|
| `extraSpace` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): if non-zero, this is the number of extra entries you would like in the returned array in which you can place your own states. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | Returns an array holding the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` state of the view. |

### onDetachedFromWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onDetachedFromWindow(): Unit
```

This is called when the view is detached from a window. At this point it no longer has a surface for drawing. 
If you override this method you *must* call through to the superclass implementation.

### onLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun onLayout(
    changed: Boolean, 
    l: Int, 
    t: Int, 
    r: Int, 
    b: Int
): Unit
```

Called from layout when this view should assign a size and position to each of its children. Derived classes with children should override this method and call layout on each of their children.

| Parameters ||
|---|---|
| `changed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): This is a new size or position for this view |
| `left` | Left position, relative to parent |
| `top` | Top position, relative to parent |
| `right` | Right position, relative to parent |
| `bottom` | Bottom position, relative to parent |

### onRequestFocusInDescendants

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onRequestFocusInDescendants(
    direction: Int, 
    previouslyFocusedRect: Rect!
): Boolean
```

Look for a descendant to call android.view.View#requestFocus on. Called by `https://developer.android.com/reference/kotlin/android/view/ViewGroup#requestFocus(kotlin.Int,%20android.graphics.Rect)` when it wants to request focus within its children. Override this to customize how your `https://developer.android.com/reference/kotlin/android/view/ViewGroup#` requests focus within its children.

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of FOCUS_UP, FOCUS_DOWN, FOCUS_LEFT, and FOCUS_RIGHT |
| `previouslyFocusedRect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!: The rectangle (in this View's coordinate system) to give a finer grained hint about where focus is coming from. May be null if there is no hint. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether focus was taken. |

### removeDetachedView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun removeDetachedView(
    child: View!, 
    animate: Boolean
): Unit
```

Finishes the removal of a detached view. This method will dispatch the detached from window event and notify the hierarchy change listener.

This method is intended to be lightweight and makes no assumptions about whether the parent or child should be redrawn. Proper use of this method will include also making any appropriate #requestLayout() or `https://developer.android.com/reference/kotlin/android/view/View#invalidate()` calls. For example, callers can `https://developer.android.com/reference/kotlin/android/view/View#post(java.lang.Runnable)` a `https://developer.android.com/reference/kotlin/java/lang/Runnable.html#` which performs a #requestLayout() on the next frame, after all detach/remove calls are finished, causing layout to be run prior to redrawing the view hierarchy.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: the child to be definitely removed from the view hierarchy |
| `animate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true and the view has an animation, the view is placed in the disappearing views list, otherwise, it is detached from the window |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#attachViewToParent(android.view.View,%20kotlin.Int,%20android.view.ViewGroup.LayoutParams)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachAllViewsFromParent()`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#detachViewFromParent(kotlin.Int)`

### setChildrenDrawingCacheEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setChildrenDrawingCacheEnabled(enabled: Boolean): Unit
```

**Deprecated:** *The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. With hardware-acceleration, intermediate cache layers are largely unnecessary and can easily result in a net loss in performance due to the cost of creating and updating the layer. In the rare cases where caching layers are useful, such as for alpha animations, `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` handles this with hardware rendering. For software-rendered snapshots of a small part of the View hierarchy or individual Views it is recommended to create a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` from either a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or `https://developer.android.com/reference/kotlin/android/graphics/Picture.html#` and call `https://developer.android.com/reference/kotlin/android/view/View#draw(android.graphics.Canvas)` on the View. However these software-rendered usages are discouraged and have compatibility issues with hardware-only rendering features such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#` bitmaps, real-time shadows, and outline clipping. For screenshots of the UI for feedback reports or unit testing the `https://developer.android.com/reference/kotlin/android/view/PixelCopy` API is recommended.*

Enables or disables the drawing cache for each child of this view group.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable the cache, false to dispose of it |

### setChildrenDrawingOrderEnabled

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setChildrenDrawingOrderEnabled(enabled: Boolean): Unit
```

Tells the ViewGroup whether to draw its children in the order defined by the method `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildDrawingOrder(kotlin.Int,%20kotlin.Int)`.

Note that `https://developer.android.com/reference/kotlin/android/view/View#getZ()` reordering, done by `https://developer.android.com/reference/kotlin/android/view/ViewGroup#dispatchDraw(android.graphics.Canvas)`, will override custom child ordering done via this method.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the order of the children when drawing is determined by `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildDrawingOrder(kotlin.Int,%20kotlin.Int)`, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isChildrenDrawingOrderEnabled()`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildDrawingOrder(kotlin.Int,%20kotlin.Int)`

### setChildrenDrawnWithCacheEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setChildrenDrawnWithCacheEnabled(enabled: Boolean): Unit
```

**Deprecated:** *As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, this property is ignored. Child views may no longer be forced to cache their rendering state by their parents. Use `https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)` on individual Views instead.*

Tells the ViewGroup to draw its children using their drawing cache. This property is ignored when `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isAlwaysDrawnWithCacheEnabled()` is true. A child's drawing cache will be used only if it has been enabled. Subclasses should call this method to start and stop using the drawing cache when they perform performance sensitive operations, like scrolling or animating.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if children should be drawn with their cache, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#setAlwaysDrawnWithCacheEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#isChildrenDrawnWithCacheEnabled()`

### setStaticTransformationsEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setStaticTransformationsEnabled(enabled: Boolean): Unit
```

When this property is set to true, this ViewGroup supports static transformations on children; this causes `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildStaticTransformation(android.view.View,%20android.view.animation.Transformation)` to be invoked when a child is drawn. Any subclass overriding `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildStaticTransformation(android.view.View,%20android.view.animation.Transformation)` should set this property to true.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True to enable static transformations on children, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewGroup#getChildStaticTransformation(android.view.View,%20android.view.animation.Transformation)`
