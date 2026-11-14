# ViewManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewManager

Kotlin| [Java](../android/view/ViewManager.md) 
| --- | --- |

```
interface ViewManager
```

| [android.view.ViewManager](../android/view/ViewManager.md) |

| Known Direct Subclasses [ViewGroup](../android/view/ViewGroup.md), [WindowManager](../android/view/WindowManager.md) |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------| | [ViewGroup](../android/view/ViewGroup.md) | A`ViewGroup`is a special view that can contain other views (called children.) The view group is the base class for layouts and views containers. | | [WindowManager](../android/view/WindowManager.md) | The interface that apps use to talk to the window manager. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbsListView](../android/widget/AbsListView.md), [AbsSpinner](../android/widget/AbsSpinner.md), [AbsoluteLayout](../android/widget/AbsoluteLayout.md), [ActionMenuView](../android/widget/ActionMenuView.md), [AdapterView](../android/widget/AdapterView.md), [AdapterViewAnimator](../android/widget/AdapterViewAnimator.md), [AdapterViewFlipper](../android/widget/AdapterViewFlipper.md), [AppWidgetHostView](../android/appwidget/AppWidgetHostView.md), [CalendarView](../android/widget/CalendarView.md), [DatePicker](../android/widget/DatePicker.md), [DialerFilter](../android/widget/DialerFilter.md), [ExpandableListView](../android/widget/ExpandableListView.md), and 37 others. |--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsListView](../android/widget/AbsListView.md) | Base class that can be used to implement virtualized lists of items. | | [AbsSpinner](../android/widget/AbsSpinner.md) | An abstract base class for spinner widgets. | | [AbsoluteLayout](../android/widget/AbsoluteLayout.md) | A layout that lets you specify exact locations (x/y coordinates) of its children. | | [ActionMenuView](../android/widget/ActionMenuView.md) | ActionMenuView is a presentation of a series of menu options as a View. | | [AdapterView](../android/widget/AdapterView.md) | An AdapterView is a view whose children are determined by an [Adapter](../android/widget/Adapter.md). | | [AdapterViewAnimator](../android/widget/AdapterViewAnimator.md) | Base class for a [AdapterView](../android/widget/AdapterView.md) that will perform animations when switching between its views. | | [AdapterViewFlipper](../android/widget/AdapterViewFlipper.md) | Simple [ViewAnimator](../android/widget/ViewAnimator.md) that will animate between two or more views that have been added to it. | | [AppWidgetHostView](../android/appwidget/AppWidgetHostView.md) | Provides the glue to show AppWidget views. | | [CalendarView](../android/widget/CalendarView.md) | This class is a calendar widget for displaying and selecting dates. | | [DatePicker](../android/widget/DatePicker.md) | Provides a widget for selecting a date. | | [DialerFilter](../android/widget/DialerFilter.md) | This widget is a layout that contains several specifically-named child views that handle keyboard entry interpreted as standard phone dialpad digits. | | [ExpandableListView](../android/widget/ExpandableListView.md) | A view that shows items in a vertically scrolling two-level list. | | [FragmentBreadCrumbs](../android/app/FragmentBreadCrumbs.md) | Helper class for showing "bread crumbs" representing the fragment stack in an activity. | | [FrameLayout](../android/widget/FrameLayout.md) | FrameLayout is designed to block out an area on the screen to display a single item. | | [Gallery](../android/widget/Gallery.md) | A view that shows items in a center-locked, horizontally scrolling list. | | [GestureOverlayView](../android/gesture/GestureOverlayView.md) | A transparent overlay for gesture input that can be placed on top of other widgets or contain other widgets. | | [GridLayout](../android/widget/GridLayout.md) | A layout that places its children in a rectangular*grid*. | | [GridView](../android/widget/GridView.md) | A view that shows items in two-dimensional scrolling grid. | | [HorizontalScrollView](../android/widget/HorizontalScrollView.md) | Layout container for a view hierarchy that can be scrolled by the user, allowing it to be larger than the physical display. | | [ImageSwitcher](../android/widget/ImageSwitcher.md) | [ViewSwitcher](../android/widget/ViewSwitcher.md) that switches between two ImageViews when a new image is set on it. | | [InlineContentView](../android/widget/inline/InlineContentView.md) | This class represents a view that holds opaque content from another app that you can inline in your UI. | | [LinearLayout](../android/widget/LinearLayout.md) | A layout that arranges other views either horizontally in a single column or vertically in a single row. | | [ListView](../android/widget/ListView.md) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | | [MediaController](../android/widget/MediaController.md) | A view containing controls for a MediaPlayer. | | [NumberPicker](../android/widget/NumberPicker.md) | A widget that enables the user to select a number from a predefined range. | | [RadioGroup](../android/widget/RadioGroup.md) | This class is used to create a multiple-exclusion scope for a set of radio buttons. | | [RelativeLayout](../android/widget/RelativeLayout.md) | A Layout where the positions of the children can be described in relation to each other or to the parent. | | [ScrollView](../android/widget/ScrollView.md) | A view group that allows the view hierarchy placed within it to be scrolled. | | [SearchView](../android/widget/SearchView.md) | A widget that provides a user interface for the user to enter a search query and submit a request to a search provider. | | [SlidingDrawer](../android/widget/SlidingDrawer.md) | SlidingDrawer hides content out of the screen and allows the user to drag a handle to bring the content on screen. | | [Spinner](../android/widget/Spinner.md) | A view that displays one child at a time and lets the user pick among them. | | [SplashScreenView](../android/window/SplashScreenView.md) | The view which allows an activity to customize its splash screen exit animation. | | [StackView](../android/widget/StackView.md) | <br /> | | [TabHost](../android/widget/TabHost.md) | Container for a tabbed window view. | | [TabWidget](../android/widget/TabWidget.md) | Displays a list of tab labels representing each page in the parent's tab collection. | | [TableLayout](../android/widget/TableLayout.md) | A layout that arranges its children into rows and columns. | | [TableRow](../android/widget/TableRow.md) | A layout that arranges its children horizontally. | | [TextSwitcher](../android/widget/TextSwitcher.md) | Specialized [android.widget.ViewSwitcher](../android/widget/ViewSwitcher.md) that contains only children of type [android.widget.TextView](../android/widget/TextView.md). | | [TimePicker](../android/widget/TimePicker.md) | A widget for selecting the time of day, in either 24-hour or AM/PM mode. | | [Toolbar](../android/widget/Toolbar.md) | A standard toolbar for use within application content. | | [TvAdView](../android/media/tv/ad/TvAdView.md) | Displays contents of TV advertisement services. | | [TvInteractiveAppView](../android/media/tv/interactive/TvInteractiveAppView.md) | Displays contents of interactive TV applications. | | [TvView](../android/media/tv/TvView.md) | Displays TV contents. | | [TwoLineListItem](../android/widget/TwoLineListItem.md) | A view group with two children, intended for use in ListViews. | | [ViewAnimator](../android/widget/ViewAnimator.md) | Base class for a [FrameLayout](../android/widget/FrameLayout.md) container that will perform animations when switching between its views. | | [ViewFlipper](../android/widget/ViewFlipper.md) | Simple [ViewAnimator](../android/widget/ViewAnimator.md) that will animate between two or more views that have been added to it. | | [ViewSwitcher](../android/widget/ViewSwitcher.md) | [ViewAnimator](../android/widget/ViewAnimator.md) that switches between two views, and has a factory from which these views are created. | | [WebView](../android/webkit/WebView.md) | A View that displays web pages. | | [ZoomControls](../android/widget/ZoomControls.md) | The`ZoomControls`class displays a simple set of controls used for zooming and provides callbacks to register for events. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface to let you add and remove child views to an Activity. To get an instance of this class, call [Context.getSystemService()](../android/content/Context.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addView](../android/view/ViewManager.md))`(`view:` ` [View](../android/view/View.md)!`, `params:` ` [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)!`)` Assign the passed LayoutParams to the passed View and add the view to the window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeView](../android/view/ViewManager.md))`(`view:` ` [View](../android/view/View.md)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateViewLayout](../android/view/ViewManager.md))`(`view:` ` [View](../android/view/View.md)!`, `params:` ` [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)!`)` <br /> |
| --- | --- |

## Public methods

### addView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addView(
    view: View!, 
    params: ViewGroup.LayoutParams!
): Unit
```

Assign the passed LayoutParams to the passed View and add the view to the window.

Throws [android.view.WindowManager.BadTokenException](../android/view/WindowManager.BadTokenException.md) for certain programming errors, such as adding a second view to a window without removing the first view.

Throws [android.view.WindowManager.InvalidDisplayException](../android/view/WindowManager.InvalidDisplayException.md) if the window is on a secondary [Display](../android/view/Display.md) and the specified display can't be found (see [android.app.Presentation](../android/app/Presentation.md)).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md)!:The view to be added to this window. |
| `params` | [ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md)!:The LayoutParams to assign to view. |

### removeView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeView(view: View!): Unit
```  

### updateViewLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updateViewLayout(
    view: View!, 
    params: ViewGroup.LayoutParams!
): Unit
```
