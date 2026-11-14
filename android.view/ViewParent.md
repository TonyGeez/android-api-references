# ViewParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewParent

Kotlin| [Java](../android/view/ViewParent.md) 
| --- | --- |

```
interface ViewParent
```

| [android.view.ViewParent](../android/view/ViewParent.md) |

| Known Direct Subclasses [ViewGroup](../android/view/ViewGroup.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------| | [ViewGroup](../android/view/ViewGroup.md) | A`ViewGroup`is a special view that can contain other views (called children.) The view group is the base class for layouts and views containers. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbsListView](../android/widget/AbsListView.md), [AbsSpinner](../android/widget/AbsSpinner.md), [AbsoluteLayout](../android/widget/AbsoluteLayout.md), [ActionMenuView](../android/widget/ActionMenuView.md), [AdapterView](../android/widget/AdapterView.md), [AdapterViewAnimator](../android/widget/AdapterViewAnimator.md), [AdapterViewFlipper](../android/widget/AdapterViewFlipper.md), [AppWidgetHostView](../android/appwidget/AppWidgetHostView.md), [CalendarView](../android/widget/CalendarView.md), [DatePicker](../android/widget/DatePicker.md), [DialerFilter](../android/widget/DialerFilter.md), [ExpandableListView](../android/widget/ExpandableListView.md), and 37 others. |--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsListView](../android/widget/AbsListView.md) | Base class that can be used to implement virtualized lists of items. | | [AbsSpinner](../android/widget/AbsSpinner.md) | An abstract base class for spinner widgets. | | [AbsoluteLayout](../android/widget/AbsoluteLayout.md) | A layout that lets you specify exact locations (x/y coordinates) of its children. | | [ActionMenuView](../android/widget/ActionMenuView.md) | ActionMenuView is a presentation of a series of menu options as a View. | | [AdapterView](../android/widget/AdapterView.md) | An AdapterView is a view whose children are determined by an [Adapter](../android/widget/Adapter.md). | | [AdapterViewAnimator](../android/widget/AdapterViewAnimator.md) | Base class for a [AdapterView](../android/widget/AdapterView.md) that will perform animations when switching between its views. | | [AdapterViewFlipper](../android/widget/AdapterViewFlipper.md) | Simple [ViewAnimator](../android/widget/ViewAnimator.md) that will animate between two or more views that have been added to it. | | [AppWidgetHostView](../android/appwidget/AppWidgetHostView.md) | Provides the glue to show AppWidget views. | | [CalendarView](../android/widget/CalendarView.md) | This class is a calendar widget for displaying and selecting dates. | | [DatePicker](../android/widget/DatePicker.md) | Provides a widget for selecting a date. | | [DialerFilter](../android/widget/DialerFilter.md) | This widget is a layout that contains several specifically-named child views that handle keyboard entry interpreted as standard phone dialpad digits. | | [ExpandableListView](../android/widget/ExpandableListView.md) | A view that shows items in a vertically scrolling two-level list. | | [FragmentBreadCrumbs](../android/app/FragmentBreadCrumbs.md) | Helper class for showing "bread crumbs" representing the fragment stack in an activity. | | [FrameLayout](../android/widget/FrameLayout.md) | FrameLayout is designed to block out an area on the screen to display a single item. | | [Gallery](../android/widget/Gallery.md) | A view that shows items in a center-locked, horizontally scrolling list. | | [GestureOverlayView](../android/gesture/GestureOverlayView.md) | A transparent overlay for gesture input that can be placed on top of other widgets or contain other widgets. | | [GridLayout](../android/widget/GridLayout.md) | A layout that places its children in a rectangular*grid*. | | [GridView](../android/widget/GridView.md) | A view that shows items in two-dimensional scrolling grid. | | [HorizontalScrollView](../android/widget/HorizontalScrollView.md) | Layout container for a view hierarchy that can be scrolled by the user, allowing it to be larger than the physical display. | | [ImageSwitcher](../android/widget/ImageSwitcher.md) | [ViewSwitcher](../android/widget/ViewSwitcher.md) that switches between two ImageViews when a new image is set on it. | | [InlineContentView](../android/widget/inline/InlineContentView.md) | This class represents a view that holds opaque content from another app that you can inline in your UI. | | [LinearLayout](../android/widget/LinearLayout.md) | A layout that arranges other views either horizontally in a single column or vertically in a single row. | | [ListView](../android/widget/ListView.md) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | | [MediaController](../android/widget/MediaController.md) | A view containing controls for a MediaPlayer. | | [NumberPicker](../android/widget/NumberPicker.md) | A widget that enables the user to select a number from a predefined range. | | [RadioGroup](../android/widget/RadioGroup.md) | This class is used to create a multiple-exclusion scope for a set of radio buttons. | | [RelativeLayout](../android/widget/RelativeLayout.md) | A Layout where the positions of the children can be described in relation to each other or to the parent. | | [ScrollView](../android/widget/ScrollView.md) | A view group that allows the view hierarchy placed within it to be scrolled. | | [SearchView](../android/widget/SearchView.md) | A widget that provides a user interface for the user to enter a search query and submit a request to a search provider. | | [SlidingDrawer](../android/widget/SlidingDrawer.md) | SlidingDrawer hides content out of the screen and allows the user to drag a handle to bring the content on screen. | | [Spinner](../android/widget/Spinner.md) | A view that displays one child at a time and lets the user pick among them. | | [SplashScreenView](../android/window/SplashScreenView.md) | The view which allows an activity to customize its splash screen exit animation. | | [StackView](../android/widget/StackView.md) | <br /> | | [TabHost](../android/widget/TabHost.md) | Container for a tabbed window view. | | [TabWidget](../android/widget/TabWidget.md) | Displays a list of tab labels representing each page in the parent's tab collection. | | [TableLayout](../android/widget/TableLayout.md) | A layout that arranges its children into rows and columns. | | [TableRow](../android/widget/TableRow.md) | A layout that arranges its children horizontally. | | [TextSwitcher](../android/widget/TextSwitcher.md) | Specialized [android.widget.ViewSwitcher](../android/widget/ViewSwitcher.md) that contains only children of type [android.widget.TextView](../android/widget/TextView.md). | | [TimePicker](../android/widget/TimePicker.md) | A widget for selecting the time of day, in either 24-hour or AM/PM mode. | | [Toolbar](../android/widget/Toolbar.md) | A standard toolbar for use within application content. | | [TvAdView](../android/media/tv/ad/TvAdView.md) | Displays contents of TV advertisement services. | | [TvInteractiveAppView](../android/media/tv/interactive/TvInteractiveAppView.md) | Displays contents of interactive TV applications. | | [TvView](../android/media/tv/TvView.md) | Displays TV contents. | | [TwoLineListItem](../android/widget/TwoLineListItem.md) | A view group with two children, intended for use in ListViews. | | [ViewAnimator](../android/widget/ViewAnimator.md) | Base class for a [FrameLayout](../android/widget/FrameLayout.md) container that will perform animations when switching between its views. | | [ViewFlipper](../android/widget/ViewFlipper.md) | Simple [ViewAnimator](../android/widget/ViewAnimator.md) that will animate between two or more views that have been added to it. | | [ViewSwitcher](../android/widget/ViewSwitcher.md) | [ViewAnimator](../android/widget/ViewAnimator.md) that switches between two views, and has a factory from which these views are created. | | [WebView](../android/webkit/WebView.md) | A View that displays web pages. | | [ZoomControls](../android/widget/ZoomControls.md) | The`ZoomControls`class displays a simple set of controls used for zooming and provides callbacks to register for events. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines the responsibilities for a class that will be a parent of a View. This is the API that a view sees when it wants to interact with its parent.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bringChildToFront](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)!`)` Change the z order of the child so it's on top of all other children. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canResolveLayoutDirection](../android/view/ViewParent.md))`()` Tells if this view parent can resolve the layout direction. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canResolveTextAlignment](../android/view/ViewParent.md))`()` Tells if this view parent can resolve the text alignment. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canResolveTextDirection](../android/view/ViewParent.md))`()` Tells if this view parent can resolve the text direction. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [childDrawableStateChanged](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)`)` This method is called on the parent when a child's drawable state has changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [childHasTransientStateChanged](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)`, `hasTransientState:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when a child view now has or no longer is tracking transient state. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearChildFocus](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)!`)` Called when a child of this parent is giving up focus |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createContextMenu](../android/view/ViewParent.md))`(`menu:` ` [ContextMenu](../android/view/ContextMenu.md)!`)` Have the parent populate the specified context menu if it has anything to add (and then recurse on its parent). |
| open [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md)? | [findOnBackInvokedDispatcherForChild](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)`, `requester:` ` [View](../android/view/View.md)`)` Walk up the View hierarchy to find the nearest [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md). |
| --- | --- |
| abstract [View](../android/view/View.md)! | [focusSearch](../android/view/ViewParent.md))`(`v:` ` [View](../android/view/View.md)!`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Find the nearest view in the specified direction that wants to take focus |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [focusableViewAvailable](../android/view/ViewParent.md))`(`v:` ` [View](../android/view/View.md)!`)` Tells the parent that a new focusable view has become available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getChildVisibleRect](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)!`, `r:` ` [Rect](../android/graphics/Rect.md)!`, `offset:` ` [Point](../android/graphics/Point.md)!`)` Compute the visible part of a rectangular region defined in terms of a child view's coordinates. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](../android/view/ViewParent.md))`()` Return this view parent layout direction. |
| abstract [ViewParent](../android/view/ViewParent.md)! | [getParent](../android/view/ViewParent.md))`()` Returns the parent if it exists, or null. |
| abstract [ViewParent](../android/view/ViewParent.md)! | [getParentForAccessibility](../android/view/ViewParent.md))`()` Gets the parent of a given View for accessibility. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextAlignment](../android/view/ViewParent.md))`()` Return this view parent text alignment. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextDirection](../android/view/ViewParent.md))`()` Return this view parent text direction. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateChild](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)!`, `r:` ` [Rect](../android/graphics/Rect.md)!`)` All or part of a child is dirty and needs to be redrawn. |
| --- | --- |
| abstract [ViewParent](../android/view/ViewParent.md)! | [invalidateChildInParent](../android/view/ViewParent.md))`(`location:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `r:` ` [Rect](../android/graphics/Rect.md)!`)` All or part of a child is dirty and needs to be redrawn. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLayoutDirectionResolved](../android/view/ViewParent.md))`()` Tells if this view parent layout direction is resolved. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLayoutRequested](../android/view/ViewParent.md))`()` Indicates whether layout was requested on this view parent. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTextAlignmentResolved](../android/view/ViewParent.md))`()` Tells if this view parent text alignment is resolved. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTextDirectionResolved](../android/view/ViewParent.md))`()` Tells if this view parent text direction is resolved. |
| abstract [View](../android/view/View.md)! | [keyboardNavigationClusterSearch](../android/view/ViewParent.md))`(`currentCluster:` ` [View](../android/view/View.md)!`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Find the nearest keyboard navigation cluster in the specified direction. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifySubtreeAccessibilityStateChanged](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)`, `source:` ` [View](../android/view/View.md)`, `changeType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notifies a view parent that the accessibility state of one of its descendants has changed and that the structure of the subtree is different. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDescendantInvalidated](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)`, `target:` ` [View](../android/view/View.md)`)` The target View has been invalidated, or has had a drawing property changed that requires the hierarchy to re-render. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onNestedFling](../android/view/ViewParent.md))`(`target:` ` [View](../android/view/View.md)`, `velocityX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `velocityY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `consumed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Request a fling from a nested scroll. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onNestedPreFling](../android/view/ViewParent.md))`(`target:` ` [View](../android/view/View.md)`, `velocityX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `velocityY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` React to a nested fling before the target view consumes it. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onNestedPrePerformAccessibilityAction](../android/view/ViewParent.md))`(`target:` ` [View](../android/view/View.md)`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arguments:` ` [Bundle](../android/os/Bundle.md)?`)` React to an accessibility action delegated by a target descendant view before the target processes it. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNestedPreScroll](../android/view/ViewParent.md))`(`target:` ` [View](../android/view/View.md)`, `dx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `consumed:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` React to a nested scroll in progress before the target view consumes a portion of the scroll. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNestedScroll](../android/view/ViewParent.md))`(`target:` ` [View](../android/view/View.md)`, `dxConsumed:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dyConsumed:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dxUnconsumed:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dyUnconsumed:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` React to a nested scroll in progress. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNestedScrollAccepted](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)`, `target:` ` [View](../android/view/View.md)`, `nestedScrollAxes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` React to the successful claiming of a nested scroll operation. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStartNestedScroll](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)`, `target:` ` [View](../android/view/View.md)`, `nestedScrollAxes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` React to a descendant view initiating a nestable scroll operation, claiming the nested scroll operation if appropriate. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopNestedScroll](../android/view/ViewParent.md))`(`target:` ` [View](../android/view/View.md)`)` React to a nested scroll operation ending. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recomputeViewAttributes](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)!`)` Tell view hierarchy that the global view attributes need to be re-evaluated. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestChildFocus](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)!`, `focused:` ` [View](../android/view/View.md)!`)` Called when a child of this parent wants focus |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requestChildRectangleOnScreen](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)`, `rectangle:` ` [Rect](../android/graphics/Rect.md)!`, `immediate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when a child of this group wants a particular rectangle to be positioned onto the screen. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requestChildRectangleOnScreen](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)`, `rectangle:` ` [Rect](../android/graphics/Rect.md)`, `immediate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a child of this group wants a particular rectangle to be positioned onto the screen. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestDisallowInterceptTouchEvent](../android/view/ViewParent.md))`(`disallowIntercept:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when a child does not want this parent and its ancestors to intercept touch events with [ViewGroup.onInterceptTouchEvent(MotionEvent)](../android/view/ViewGroup.md)). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestFitSystemWindows](../android/view/ViewParent.md))`()` Ask that a new dispatch of [View.fitSystemWindows(Rect)](../android/view/View.md))be performed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLayout](../android/view/ViewParent.md))`()` Called when something has changed which has invalidated the layout of a child of this view parent. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requestSendAccessibilityEvent](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)`, `event:` ` [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)!`)` Called by a child to request from its parent to send an [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestTransparentRegion](../android/view/ViewParent.md))`(`child:` ` [View](../android/view/View.md)!`)` Called when a child wants the view hierarchy to gather and report transparent regions to the window compositor. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [showContextMenuForChild](../android/view/ViewParent.md))`(`originalView:` ` [View](../android/view/View.md)!`)` Shows the context menu for the specified view or its ancestors. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [showContextMenuForChild](../android/view/ViewParent.md))`(`originalView:` ` [View](../android/view/View.md)!`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Shows the context menu for the specified view or its ancestors anchored to the specified view-relative coordinate. |
| --- | --- |
| abstract [ActionMode](../android/view/ActionMode.md)! | [startActionModeForChild](../android/view/ViewParent.md))`(`originalView:` ` [View](../android/view/View.md)!`, `callback:` ` [ActionMode.Callback](../android/view/ActionMode.Callback.md)!`)` Start an action mode for the specified view with the default type [ActionMode.TYPE_PRIMARY](../android/view/ActionMode.md). |
| abstract [ActionMode](../android/view/ActionMode.md)! | [startActionModeForChild](../android/view/ViewParent.md))`(`originalView:` ` [View](../android/view/View.md)!`, `callback:` ` [ActionMode.Callback](../android/view/ActionMode.Callback.md)!`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start an action mode of a specific type for the specified view. |

## Public methods

### bringChildToFront

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun bringChildToFront(child: View!): Unit
```

Change the z order of the child so it's on top of all other children. This ordering change may affect layout, if this container uses an order-dependent layout scheme (e.g., LinearLayout). Prior to [android.os.Build.VERSION_CODES#KITKAT](../android/os/Build.VERSION_CODES.md) this method should be followed by calls to [requestLayout()](../android/view/ViewParent.md))and [View.invalidate()](../android/view/View.md))on this parent to force the parent to redraw with the new child ordering.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md)!:The child to bring to the top of the z order |

### canResolveLayoutDirection

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun canResolveLayoutDirection(): Boolean
```

Tells if this view parent can resolve the layout direction. See [View.setLayoutDirection(int)](../android/view/View.md))

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this view parent can resolve the layout direction. |

### canResolveTextAlignment

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun canResolveTextAlignment(): Boolean
```

Tells if this view parent can resolve the text alignment. See [View.setTextAlignment(int)](../android/view/View.md))

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this view parent can resolve the text alignment. |

### canResolveTextDirection

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun canResolveTextDirection(): Boolean
```

Tells if this view parent can resolve the text direction. See [View.setTextDirection(int)](../android/view/View.md))

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this view parent can resolve the text direction. |

### childDrawableStateChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun childDrawableStateChanged(child: View): Unit
```

This method is called on the parent when a child's drawable state has changed.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md):The child whose drawable state has changed. This value cannot be`null`. |

### childHasTransientStateChanged

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun childHasTransientStateChanged(
    child: View, 
    hasTransientState: Boolean
): Unit
```

Called when a child view now has or no longer is tracking transient state.

"Transient state" is any state that a View might hold that is not expected to be reflected in the data model that the View currently presents. This state only affects the presentation to the user within the View itself, such as the current state of animations in progress or the state of a text selection operation.

Transient state is useful for hinting to other components of the View system that a particular view is tracking something complex but encapsulated. A`ListView`for example may acknowledge that list item Views with transient state should be preserved within their position or stable item ID instead of treating that view as trivially replaceable by the backing adapter. This allows adapter implementations to be simpler instead of needing to track the state of item view animations in progress such that they could be restored in the event of an unexpected recycling and rebinding of attached item views.

This method is called on a parent view when a child view or a view within its subtree begins or ends tracking of internal transient state.

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md):Child view whose state has changed This value cannot be`null`. |
| `hasTransientState` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if this child has transient state |

### clearChildFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearChildFocus(child: View!): Unit
```

Called when a child of this parent is giving up focus

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md)!:The view that is giving up focus |

### createContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createContextMenu(menu: ContextMenu!): Unit
```

Have the parent populate the specified context menu if it has anything to add (and then recurse on its parent).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `menu` | [ContextMenu](../android/view/ContextMenu.md)!:The menu to populate |

### findOnBackInvokedDispatcherForChild

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findOnBackInvokedDispatcherForChild(
    child: View, 
    requester: View
): OnBackInvokedDispatcher?
```

Walk up the View hierarchy to find the nearest [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md):The direct child of this view for which to find a dispatcher. This value cannot be`null`. |
| `requester` | [View](../android/view/View.md):The requester that will use the dispatcher. Can be the same as child. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md)? | The [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md) from this or the nearest ancestor, or null if the view is both not attached and have no ancestor providing an [OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md). |

### focusSearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun focusSearch(
    v: View!, 
    direction: Int
): View!
```

Find the nearest view in the specified direction that wants to take focus

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](../android/view/View.md)!:The view that currently has focus |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of FOCUS_UP, FOCUS_DOWN, FOCUS_LEFT, and FOCUS_RIGHT |

### focusableViewAvailable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun focusableViewAvailable(v: View!): Unit
```

Tells the parent that a new focusable view has become available. This is to handle transitions from the case where there are no focusable views to the case where the first focusable view appears.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------|
| `v` | [View](../android/view/View.md)!:The view that has become newly focusable |

### getChildVisibleRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getChildVisibleRect(
    child: View!, 
    r: Rect!, 
    offset: Point!
): Boolean
```

Compute the visible part of a rectangular region defined in terms of a child view's coordinates.

Returns the clipped visible part of the rectangle`r`, defined in the`child`'s local coordinate system.`r`is modified by this method to contain the result, expressed in the global (root) coordinate system.

The resulting rectangle is always axis aligned. If a rotation is applied to a node in the View hierarchy, the result is the axis-aligned bounding box of the visible rectangle.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md)!:A child View, whose rectangular visible region we want to compute |
| `r` | [Rect](../android/graphics/Rect.md)!:The input rectangle, defined in the child coordinate system. Will be overwritten to contain the resulting visible rectangle, expressed in global (root) coordinates |
| `offset` | [Point](../android/graphics/Point.md)!:The input coordinates of a point, defined in the child coordinate system. As with the`r`parameter, this will be overwritten to contain the global (root) coordinates of that point. A`null`value is valid (in case you are not interested in this result) |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting rectangle is not empty, false otherwise |

### getLayoutDirection

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLayoutDirection(): Int
```

Return this view parent layout direction. See [View.getLayoutDirection()](../android/view/View.md))

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [View.LAYOUT_DIRECTION_RTL](../android/view/View.md) if the layout direction is RTL or returns [View.LAYOUT_DIRECTION_LTR](../android/view/View.md) if the layout direction is not RTL. |

### getParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParent(): ViewParent!
```

Returns the parent if it exists, or null.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [ViewParent](../android/view/ViewParent.md)! | a ViewParent or null if this ViewParent does not have a parent |

### getParentForAccessibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParentForAccessibility(): ViewParent!
```

Gets the parent of a given View for accessibility. Since some Views are not exposed to the accessibility layer the parent for accessibility is not necessarily the direct parent of the View, rather it is a predecessor.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------|
| [ViewParent](../android/view/ViewParent.md)! | The parent or`null`if no such is found. |

### getTextAlignment

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTextAlignment(): Int
```

Return this view parent text alignment. See [android.view.View#getTextAlignment()](../android/view/View.md))

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the resolved text alignment. Returns one of: [View.TEXT_ALIGNMENT_GRAVITY](../android/view/View.md), [View.TEXT_ALIGNMENT_CENTER](../android/view/View.md), [View.TEXT_ALIGNMENT_TEXT_START](../android/view/View.md), [View.TEXT_ALIGNMENT_TEXT_END](../android/view/View.md), [View.TEXT_ALIGNMENT_VIEW_START](../android/view/View.md), [View.TEXT_ALIGNMENT_VIEW_END](../android/view/View.md) |

### getTextDirection

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTextDirection(): Int
```

Return this view parent text direction. See [View.getTextDirection()](../android/view/View.md))

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the resolved text direction. Returns one of: [View.TEXT_DIRECTION_FIRST_STRONG](../android/view/View.md) [View.TEXT_DIRECTION_ANY_RTL](../android/view/View.md), [View.TEXT_DIRECTION_LTR](../android/view/View.md), [View.TEXT_DIRECTION_RTL](../android/view/View.md), [View.TEXT_DIRECTION_LOCALE](../android/view/View.md) |

### invalidateChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun invalidateChild(
    child: View!, 
    r: Rect!
): Unit
```

**Deprecated:** *Use [onDescendantInvalidated(android.view.View,android.view.View)](../android/view/ViewParent.md))instead.*

All or part of a child is dirty and needs to be redrawn.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md)!:The child which is dirty |
| `r` | [Rect](../android/graphics/Rect.md)!:The area within the child that is invalid |

### invalidateChildInParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun invalidateChildInParent(
    location: IntArray!, 
    r: Rect!
): ViewParent!
```

**Deprecated:** *Use [onDescendantInvalidated(android.view.View,android.view.View)](../android/view/ViewParent.md))instead.*

All or part of a child is dirty and needs to be redrawn.

The location array is an array of two int values which respectively define the left and the top position of the dirty child.

This method must return the parent of this ViewParent if the specified rectangle must be invalidated in the parent. If the specified rectangle does not require invalidation in the parent or if the parent does not exist, this method must return null.

When this method returns a non-null value, the location array must have been updated with the left and top coordinates of this ViewParent.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `location` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:An array of 2 ints containing the left and top coordinates of the child to invalidate |
| `r` | [Rect](../android/graphics/Rect.md)!:The area within the child that is invalid |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------|
| [ViewParent](../android/view/ViewParent.md)! | the parent of this ViewParent or null |

### isLayoutDirectionResolved

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isLayoutDirectionResolved(): Boolean
```

Tells if this view parent layout direction is resolved. See [View.setLayoutDirection(int)](../android/view/View.md))

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this view parent layout direction is resolved. |

### isLayoutRequested

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isLayoutRequested(): Boolean
```

Indicates whether layout was requested on this view parent.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if layout was requested, false otherwise |

### isTextAlignmentResolved

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isTextAlignmentResolved(): Boolean
```

Tells if this view parent text alignment is resolved. See [View.setTextAlignment(int)](../android/view/View.md))

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this view parent text alignment is resolved. |

### isTextDirectionResolved

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isTextDirectionResolved(): Boolean
```

Tells if this view parent text direction is resolved. See [View.setTextDirection(int)](../android/view/View.md))

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this view parent text direction is resolved. |

### keyboardNavigationClusterSearch

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun keyboardNavigationClusterSearch(
    currentCluster: View!, 
    direction: Int
): View!
```

Find the nearest keyboard navigation cluster in the specified direction. This does not actually give focus to that cluster.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `currentCluster` | [View](../android/view/View.md)!:The starting point of the search. Null means the current cluster is not found yet |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Direction to look |

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [View](../android/view/View.md)! | The nearest keyboard navigation cluster in the specified direction, or null if none can be found |

### notifySubtreeAccessibilityStateChanged

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun notifySubtreeAccessibilityStateChanged(
    child: View, 
    source: View, 
    changeType: Int
): Unit
```

Notifies a view parent that the accessibility state of one of its descendants has changed and that the structure of the subtree is different.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md):The direct child whose subtree has changed. This value cannot be`null`. |
| `source` | [View](../android/view/View.md):The descendant view that changed. May not be`null`. |
| `changeType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bit mask of the types of changes that occurred. One or more of: - [AccessibilityEvent.CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_STATE_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_SUBTREE](../android/view/accessibility/AccessibilityEvent.md) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_TEXT](../android/view/accessibility/AccessibilityEvent.md) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_UNDEFINED](../android/view/accessibility/AccessibilityEvent.md) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_DRAG_STARTED](../android/view/accessibility/AccessibilityEvent.md) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_DRAG_CANCELLED](../android/view/accessibility/AccessibilityEvent.md) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_DRAG_DROPPED](../android/view/accessibility/AccessibilityEvent.md) |
| --- | --- |

### onDescendantInvalidated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDescendantInvalidated(
    child: View, 
    target: View
): Unit
```

The target View has been invalidated, or has had a drawing property changed that requires the hierarchy to re-render. This method is called by the View hierarchy to signal ancestors that a View either needs to re-record its drawing commands, or drawing properties have changed. This is how Views schedule a drawing traversal. This signal is generally only dispatched for attached Views, since only they need to draw.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md):Direct child of this ViewParent containing target This value cannot be`null`. |
| `target` | [View](../android/view/View.md):The view that needs to redraw This value cannot be`null`. |

### onNestedFling

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNestedFling(
    target: View, 
    velocityX: Float, 
    velocityY: Float, 
    consumed: Boolean
): Boolean
```

Request a fling from a nested scroll.

This method signifies that a nested scrolling child has detected suitable conditions for a fling. Generally this means that a touch scroll has ended with a [velocity](../android/view/VelocityTracker.md) in the direction of scrolling that meets or exceeds the [minimum fling velocity](../android/view/ViewConfiguration.md))along a scrollable axis.

If a nested scrolling child view would normally fling but it is at the edge of its own content, it can use this method to delegate the fling to its nested scrolling parent instead. The parent may optionally consume the fling or observe a child fling.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [View](../android/view/View.md):View that initiated the nested scroll This value cannot be`null`. |
| `velocityX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Horizontal velocity in pixels per second |
| `velocityY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Vertical velocity in pixels per second |
| --- | --- |
| `consumed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the child consumed the fling, false otherwise |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this parent consumed or otherwise reacted to the fling |

### onNestedPreFling

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNestedPreFling(
    target: View, 
    velocityX: Float, 
    velocityY: Float
): Boolean
```

React to a nested fling before the target view consumes it.

This method siginfies that a nested scrolling child has detected a fling with the given velocity along each axis. Generally this means that a touch scroll has ended with a [velocity](../android/view/VelocityTracker.md) in the direction of scrolling that meets or exceeds the [minimum fling velocity](../android/view/ViewConfiguration.md))along a scrollable axis.

If a nested scrolling parent is consuming motion as part of a [pre-scroll](../android/view/ViewParent.md)), it may be appropriate for it to also consume the pre-fling to complete that same motion. By returning`true`from this method, the parent indicates that the child should not fling its own internal content as well.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [View](../android/view/View.md):View that initiated the nested scroll This value cannot be`null`. |
| `velocityX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Horizontal velocity in pixels per second |
| `velocityY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Vertical velocity in pixels per second |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this parent consumed the fling ahead of the target view |

### onNestedPrePerformAccessibilityAction

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNestedPrePerformAccessibilityAction(
    target: View, 
    action: Int, 
    arguments: Bundle?
): Boolean
```

React to an accessibility action delegated by a target descendant view before the target processes it.

This method may be called by a target descendant view if the target wishes to give a view in its parent chain a chance to react to the event before normal processing occurs. Most commonly this will be a scroll event such as [android.view.accessibility.AccessibilityNodeInfo#ACTION_SCROLL_FORWARD](../android/view/accessibility/AccessibilityNodeInfo.md). A ViewParent that supports acting as a nested scrolling parent should override this method and act accordingly to implement scrolling via accesibility systems.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [View](../android/view/View.md):The target view dispatching this action This value cannot be`null`. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Action being performed; see [android.view.accessibility.AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md) |
| `arguments` | [Bundle](../android/os/Bundle.md)?:Optional action arguments This value may be`null`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the action was consumed by this ViewParent |

### onNestedPreScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNestedPreScroll(
    target: View, 
    dx: Int, 
    dy: Int, 
    consumed: IntArray
): Unit
```

React to a nested scroll in progress before the target view consumes a portion of the scroll.

When working with nested scrolling often the parent view may want an opportunity to consume the scroll before the nested scrolling child does. An example of this is a drawer that contains a scrollable list. The user will want to be able to scroll the list fully into view before the list itself begins scrolling.

`onNestedPreScroll`is called when a nested scrolling child invokes[View.dispatchNestedPreScroll(int, int, int[], int[])](https://developer.android.com/reference/kotlin/android/view/View#dispatchNestedPreScroll(kotlin.Int,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.IntArray)). The implementation should report how any pixels of the scroll reported by dx, dy were consumed in the`consumed`array. Index 0 corresponds to dx and index 1 corresponds to dy. This parameter will never be null. Initial values for consumed\[0\] and consumed\[1\] will always be 0.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [View](../android/view/View.md):View that initiated the nested scroll This value cannot be`null`. |
| `dx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Horizontal scroll distance in pixels |
| `dy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Vertical scroll distance in pixels |
| --- | --- |
| `consumed` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):Output. The horizontal and vertical scroll distance consumed by this parent This value cannot be`null`. |

### onNestedScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNestedScroll(
    target: View, 
    dxConsumed: Int, 
    dyConsumed: Int, 
    dxUnconsumed: Int, 
    dyUnconsumed: Int
): Unit
```

React to a nested scroll in progress.

This method will be called when the ViewParent's current nested scrolling child view dispatches a nested scroll event. To receive calls to this method the ViewParent must have previously returned`true`for a call to [onStartNestedScroll(android.view.View,android.view.View,int)](../android/view/ViewParent.md)).

Both the consumed and unconsumed portions of the scroll distance are reported to the ViewParent. An implementation may choose to use the consumed portion to match or chase scroll position of multiple child elements, for example. The unconsumed portion may be used to allow continuous dragging of multiple scrolling or draggable elements, such as scrolling a list within a vertical drawer where the drawer begins dragging once the edge of inner scrolling content is reached.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [View](../android/view/View.md):The descendent view controlling the nested scroll This value cannot be`null`. |
| `dxConsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Horizontal scroll distance in pixels already consumed by target |
| `dyConsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Vertical scroll distance in pixels already consumed by target |
| --- | --- |
| `dxUnconsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Horizontal scroll distance in pixels not consumed by target |
| `dyUnconsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Vertical scroll distance in pixels not consumed by target |

### onNestedScrollAccepted

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNestedScrollAccepted(
    child: View, 
    target: View, 
    nestedScrollAxes: Int
): Unit
```

React to the successful claiming of a nested scroll operation.

This method will be called after [onStartNestedScroll](../android/view/ViewParent.md))returns true. It offers an opportunity for the view and its superclasses to perform initial configuration for the nested scroll. Implementations of this method should always call their superclass's implementation of this method if one is present.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md):Direct child of this ViewParent containing target This value cannot be`null`. |
| `target` | [View](../android/view/View.md):View that initiated the nested scroll This value cannot be`null`. |
| `nestedScrollAxes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags consisting of [View.SCROLL_AXIS_HORIZONTAL](../android/view/View.md), [View.SCROLL_AXIS_VERTICAL](../android/view/View.md) or both |
| --- | --- |

**See Also**

- [#onStartNestedScroll(View, View, int)](../android/view/ViewParent.md))
- [#onStopNestedScroll(View)](../android/view/ViewParent.md)) 

### onStartNestedScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStartNestedScroll(
    child: View, 
    target: View, 
    nestedScrollAxes: Int
): Boolean
```

React to a descendant view initiating a nestable scroll operation, claiming the nested scroll operation if appropriate.

This method will be called in response to a descendant view invoking [View.startNestedScroll(int)](../android/view/View.md)). Each parent up the view hierarchy will be given an opportunity to respond and claim the nested scrolling operation by returning`true`.

This method may be overridden by ViewParent implementations to indicate when the view is willing to support a nested scrolling operation that is about to begin. If it returns true, this ViewParent will become the target view's nested scrolling parent for the duration of the scroll operation in progress. When the nested scroll is finished this ViewParent will receive a call to [onStopNestedScroll(android.view.View)](../android/view/ViewParent.md)).

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md):Direct child of this ViewParent containing target This value cannot be`null`. |
| `target` | [View](../android/view/View.md):View that initiated the nested scroll This value cannot be`null`. |
| `nestedScrollAxes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags consisting of [View.SCROLL_AXIS_HORIZONTAL](../android/view/View.md), [View.SCROLL_AXIS_VERTICAL](../android/view/View.md) or both |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this ViewParent accepts the nested scroll operation |

### onStopNestedScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStopNestedScroll(target: View): Unit
```

React to a nested scroll operation ending.

Perform cleanup after a nested scrolling operation. This method will be called when a nested scroll stops, for example when a nested touch scroll ends with a [MotionEvent.ACTION_UP](../android/view/MotionEvent.md) or [MotionEvent.ACTION_CANCEL](../android/view/MotionEvent.md) event. Implementations of this method should always call their superclass's implementation of this method if one is present.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [View](../android/view/View.md):View that initiated the nested scroll This value cannot be`null`. |

### recomputeViewAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun recomputeViewAttributes(child: View!): Unit
```

Tell view hierarchy that the global view attributes need to be re-evaluated.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md)!:View whose attributes have changed. |

### requestChildFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requestChildFocus(
    child: View!, 
    focused: View!
): Unit
```

Called when a child of this parent wants focus

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md)!:The child of this ViewParent that wants focus. This view will contain the focused view. It is not necessarily the view that actually has focus. |
| `focused` | [View](../android/view/View.md)!:The view that is a descendant of child that actually has focus |

### requestChildRectangleOnScreen

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requestChildRectangleOnScreen(
    child: View, 
    rectangle: Rect!, 
    immediate: Boolean
): Boolean
```

Called when a child of this group wants a particular rectangle to be positioned onto the screen. [ViewGroup](../android/view/ViewGroup.md) s overriding this can trust that:

- `child`will be a direct child of this group
- `rectangle`will be in the child's content coordinates

<br />

[ViewGroup](../android/view/ViewGroup.md) s overriding this should uphold the contract:

- nothing will change if the rectangle is already visible
- the view port will be scrolled only just enough to make the rectangle visible

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md):The direct child making the request. This value cannot be`null`. |
| `rectangle` | [Rect](../android/graphics/Rect.md)!:The rectangle in the child's coordinates the child wishes to be on the screen. |
| `immediate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True to forbid animated or delayed scrolling, false otherwise |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the group scrolled to handle the operation |

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

Called when a child of this group wants a particular rectangle to be positioned onto the screen. [ViewGroup](../android/view/ViewGroup.md) s overriding this can trust that:

- `child`will be a direct child of this group
- `rectangle`will be in the child's content coordinates

<br />

[ViewGroup](../android/view/ViewGroup.md) s overriding this should uphold the contract:

- nothing will change if the rectangle is already visible
- the view port will be scrolled only just enough to make the rectangle visible

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md):The direct child making the request. This value cannot be`null`. |
| `rectangle` | [Rect](../android/graphics/Rect.md):The rectangle in the child's coordinates the child wishes to be on the screen. This value cannot be`null`. |
| `immediate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True to forbid animated or delayed scrolling, false otherwise |
| --- | --- |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The parameter for the source of this request. Value is [android.view.View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED](../android/view/View.md), [android.view.View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY](../android/view/View.md), [android.view.View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR](../android/view/View.md), or [android.view.View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS](../android/view/View.md) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the group scrolled to handle the operation |

### requestDisallowInterceptTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requestDisallowInterceptTouchEvent(disallowIntercept: Boolean): Unit
```

Called when a child does not want this parent and its ancestors to intercept touch events with [ViewGroup.onInterceptTouchEvent(MotionEvent)](../android/view/ViewGroup.md)).

This parent should pass this call onto its parents. This parent must obey this request for the duration of the touch (that is, only clear the flag after this parent has received an up or a cancel.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `disallowIntercept` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the child does not want the parent to intercept touch events. |

### requestFitSystemWindows

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requestFitSystemWindows(): Unit
```

Ask that a new dispatch of [View.fitSystemWindows(Rect)](../android/view/View.md))be performed. 

### requestLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requestLayout(): Unit
```

Called when something has changed which has invalidated the layout of a child of this view parent. This will schedule a layout pass of the view tree. 

### requestSendAccessibilityEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requestSendAccessibilityEvent(
    child: View, 
    event: AccessibilityEvent!
): Boolean
```

Called by a child to request from its parent to send an [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md). The child has already populated a record for itself in the event and is delegating to its parent to send the event. The parent can optionally add a record for itself.

Note: An accessibility event is fired by an individual view which populates the event with a record for its state and requests from its parent to perform the sending. The parent can optionally add a record for itself before dispatching the request to its parent. A parent can also choose not to respect the request for sending the event. The accessibility event is sent by the topmost view in the view tree.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md):The child which requests sending the event. This value cannot be`null`. |
| `event` | [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)!:The event to be sent. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was sent. |

### requestTransparentRegion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requestTransparentRegion(child: View!): Unit
```

Called when a child wants the view hierarchy to gather and report transparent regions to the window compositor. Views that "punch" holes in the view hierarchy, such as SurfaceView can use this API to improve performance of the system. When no such a view is present in the hierarchy, this optimization in unnecessary and might slightly reduce the view hierarchy performance.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](../android/view/View.md)!:the view requesting the transparent region computation |

### showContextMenuForChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun showContextMenuForChild(originalView: View!): Boolean
```

Shows the context menu for the specified view or its ancestors.

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, [ViewManager.addView(View, android.view.ViewGroup.LayoutParams)](../android/view/ViewManager.md))) then it should override this and show the context menu.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| `originalView` | [View](../android/view/View.md)!:the source view where the context menu was first invoked |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the context menu was shown,`false`otherwise |

**See Also**

- [#showContextMenuForChild(View, float, float)](../android/view/ViewParent.md)) 

### showContextMenuForChild

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun showContextMenuForChild(
    originalView: View!, 
    x: Float, 
    y: Float
): Boolean
```

Shows the context menu for the specified view or its ancestors anchored to the specified view-relative coordinate.

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, [ViewManager.addView(View, android.view.ViewGroup.LayoutParams)](../android/view/ViewManager.md))) then it should override this and show the context menu.

If a subclass overrides this method it should also override [showContextMenuForChild(android.view.View)](../android/view/ViewParent.md)).

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `originalView` | [View](../android/view/View.md)!:the source view where the context menu was first invoked |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the X coordinate in pixels relative to the original view to which the menu should be anchored, or [Float.NaN](../java/lang/Float.md) to disable anchoring |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the Y coordinate in pixels relative to the original view to which the menu should be anchored, or [Float.NaN](../java/lang/Float.md) to disable anchoring |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the context menu was shown,`false`otherwise |

### startActionModeForChild

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startActionModeForChild(
    originalView: View!, 
    callback: ActionMode.Callback!
): ActionMode!
```

Start an action mode for the specified view with the default type [ActionMode.TYPE_PRIMARY](../android/view/ActionMode.md).

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, [ViewManager.addView(View, android.view.ViewGroup.LayoutParams)](../android/view/ViewManager.md))) then it should override this and start the action mode.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `originalView` | [View](../android/view/View.md)!:The source view where the action mode was first invoked |
| `callback` | [ActionMode.Callback](../android/view/ActionMode.Callback.md)!:The callback that will handle lifecycle events for the action mode |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------|
| [ActionMode](../android/view/ActionMode.md)! | The new action mode if it was started, null otherwise |

**See Also**

- [#startActionModeForChild(View, android.view.ActionMode.Callback, int)](../android/view/ViewParent.md)) 

### startActionModeForChild

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startActionModeForChild(
    originalView: View!, 
    callback: ActionMode.Callback!, 
    type: Int
): ActionMode!
```

Start an action mode of a specific type for the specified view.

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, [ViewManager.addView(View, android.view.ViewGroup.LayoutParams)](../android/view/ViewManager.md))) then it should override this and start the action mode.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `originalView` | [View](../android/view/View.md)!:The source view where the action mode was first invoked |
| `callback` | [ActionMode.Callback](../android/view/ActionMode.Callback.md)!:The callback that will handle lifecycle events for the action mode |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [ActionMode.TYPE_PRIMARY](../android/view/ActionMode.md) or [ActionMode.TYPE_FLOATING](../android/view/ActionMode.md). |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------|
| [ActionMode](../android/view/ActionMode.md)! | The new action mode if it was started, null otherwise |
