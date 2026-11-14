# ViewParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewParent

Kotlin| [Java](https://developer.android.com/reference/android/view/ViewParent "View this page in Java") 

```
interface ViewParent
```

| [android.view.ViewParent](https://developer.android.com/reference/kotlin/android/view/ViewParent#) |

| Known Direct Subclasses [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------| | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup) | A`ViewGroup`is a special view that can contain other views (called children.) The view group is the base class for layouts and views containers. | |

| Known Indirect Subclasses [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#), [AbsSpinner](https://developer.android.com/reference/kotlin/android/widget/AbsSpinner.html#), [AbsoluteLayout](https://developer.android.com/reference/kotlin/android/widget/AbsoluteLayout.html#), [ActionMenuView](https://developer.android.com/reference/kotlin/android/widget/ActionMenuView.html#), [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#), [AdapterViewAnimator](https://developer.android.com/reference/kotlin/android/widget/AdapterViewAnimator.html#), [AdapterViewFlipper](https://developer.android.com/reference/kotlin/android/widget/AdapterViewFlipper.html#), [AppWidgetHostView](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHostView.html#), [CalendarView](https://developer.android.com/reference/kotlin/android/widget/CalendarView.html#), [DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#), [DialerFilter](https://developer.android.com/reference/kotlin/android/widget/DialerFilter.html#), [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.html#), and 37 others. |--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#) | Base class that can be used to implement virtualized lists of items. | | [AbsSpinner](https://developer.android.com/reference/kotlin/android/widget/AbsSpinner.html#) | An abstract base class for spinner widgets. | | [AbsoluteLayout](https://developer.android.com/reference/kotlin/android/widget/AbsoluteLayout.html#) | A layout that lets you specify exact locations (x/y coordinates) of its children. | | [ActionMenuView](https://developer.android.com/reference/kotlin/android/widget/ActionMenuView.html#) | ActionMenuView is a presentation of a series of menu options as a View. | | [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#) | An AdapterView is a view whose children are determined by an [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter.html#). | | [AdapterViewAnimator](https://developer.android.com/reference/kotlin/android/widget/AdapterViewAnimator.html#) | Base class for a [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#) that will perform animations when switching between its views. | | [AdapterViewFlipper](https://developer.android.com/reference/kotlin/android/widget/AdapterViewFlipper.html#) | Simple [ViewAnimator](https://developer.android.com/reference/kotlin/android/widget/ViewAnimator.html#) that will animate between two or more views that have been added to it. | | [AppWidgetHostView](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHostView.html#) | Provides the glue to show AppWidget views. | | [CalendarView](https://developer.android.com/reference/kotlin/android/widget/CalendarView.html#) | This class is a calendar widget for displaying and selecting dates. | | [DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#) | Provides a widget for selecting a date. | | [DialerFilter](https://developer.android.com/reference/kotlin/android/widget/DialerFilter.html#) | This widget is a layout that contains several specifically-named child views that handle keyboard entry interpreted as standard phone dialpad digits. | | [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.html#) | A view that shows items in a vertically scrolling two-level list. | | [FragmentBreadCrumbs](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs.html#) | Helper class for showing "bread crumbs" representing the fragment stack in an activity. | | [FrameLayout](https://developer.android.com/reference/kotlin/android/widget/FrameLayout.html#) | FrameLayout is designed to block out an area on the screen to display a single item. | | [Gallery](https://developer.android.com/reference/kotlin/android/widget/Gallery.html#) | A view that shows items in a center-locked, horizontally scrolling list. | | [GestureOverlayView](https://developer.android.com/reference/kotlin/android/gesture/GestureOverlayView.html#) | A transparent overlay for gesture input that can be placed on top of other widgets or contain other widgets. | | [GridLayout](https://developer.android.com/reference/kotlin/android/widget/GridLayout.html#) | A layout that places its children in a rectangular*grid*. | | [GridView](https://developer.android.com/reference/kotlin/android/widget/GridView.html#) | A view that shows items in two-dimensional scrolling grid. | | [HorizontalScrollView](https://developer.android.com/reference/kotlin/android/widget/HorizontalScrollView.html#) | Layout container for a view hierarchy that can be scrolled by the user, allowing it to be larger than the physical display. | | [ImageSwitcher](https://developer.android.com/reference/kotlin/android/widget/ImageSwitcher.html#) | [ViewSwitcher](https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher.html#) that switches between two ImageViews when a new image is set on it. | | [InlineContentView](https://developer.android.com/reference/kotlin/android/widget/inline/InlineContentView.html#) | This class represents a view that holds opaque content from another app that you can inline in your UI. | | [LinearLayout](https://developer.android.com/reference/kotlin/android/widget/LinearLayout.html#) | A layout that arranges other views either horizontally in a single column or vertically in a single row. | | [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | | [MediaController](https://developer.android.com/reference/kotlin/android/widget/MediaController.html#) | A view containing controls for a MediaPlayer. | | [NumberPicker](https://developer.android.com/reference/kotlin/android/widget/NumberPicker.html#) | A widget that enables the user to select a number from a predefined range. | | [RadioGroup](https://developer.android.com/reference/kotlin/android/widget/RadioGroup.html#) | This class is used to create a multiple-exclusion scope for a set of radio buttons. | | [RelativeLayout](https://developer.android.com/reference/kotlin/android/widget/RelativeLayout.html#) | A Layout where the positions of the children can be described in relation to each other or to the parent. | | [ScrollView](https://developer.android.com/reference/kotlin/android/widget/ScrollView.html#) | A view group that allows the view hierarchy placed within it to be scrolled. | | [SearchView](https://developer.android.com/reference/kotlin/android/widget/SearchView.html#) | A widget that provides a user interface for the user to enter a search query and submit a request to a search provider. | | [SlidingDrawer](https://developer.android.com/reference/kotlin/android/widget/SlidingDrawer.html#) | SlidingDrawer hides content out of the screen and allows the user to drag a handle to bring the content on screen. | | [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner.html#) | A view that displays one child at a time and lets the user pick among them. | | [SplashScreenView](https://developer.android.com/reference/kotlin/android/window/SplashScreenView.html#) | The view which allows an activity to customize its splash screen exit animation. | | [StackView](https://developer.android.com/reference/kotlin/android/widget/StackView.html#) | <br /> | | [TabHost](https://developer.android.com/reference/kotlin/android/widget/TabHost.html#) | Container for a tabbed window view. | | [TabWidget](https://developer.android.com/reference/kotlin/android/widget/TabWidget.html#) | Displays a list of tab labels representing each page in the parent's tab collection. | | [TableLayout](https://developer.android.com/reference/kotlin/android/widget/TableLayout.html#) | A layout that arranges its children into rows and columns. | | [TableRow](https://developer.android.com/reference/kotlin/android/widget/TableRow.html#) | A layout that arranges its children horizontally. | | [TextSwitcher](https://developer.android.com/reference/kotlin/android/widget/TextSwitcher.html#) | Specialized [android.widget.ViewSwitcher](https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher.html#) that contains only children of type [android.widget.TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#). | | [TimePicker](https://developer.android.com/reference/kotlin/android/widget/TimePicker.html#) | A widget for selecting the time of day, in either 24-hour or AM/PM mode. | | [Toolbar](https://developer.android.com/reference/kotlin/android/widget/Toolbar.html#) | A standard toolbar for use within application content. | | [TvAdView](https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdView.html#) | Displays contents of TV advertisement services. | | [TvInteractiveAppView](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView.html#) | Displays contents of interactive TV applications. | | [TvView](https://developer.android.com/reference/kotlin/android/media/tv/TvView.html#) | Displays TV contents. | | [TwoLineListItem](https://developer.android.com/reference/kotlin/android/widget/TwoLineListItem.html#) | A view group with two children, intended for use in ListViews. | | [ViewAnimator](https://developer.android.com/reference/kotlin/android/widget/ViewAnimator.html#) | Base class for a [FrameLayout](https://developer.android.com/reference/kotlin/android/widget/FrameLayout.html#) container that will perform animations when switching between its views. | | [ViewFlipper](https://developer.android.com/reference/kotlin/android/widget/ViewFlipper.html#) | Simple [ViewAnimator](https://developer.android.com/reference/kotlin/android/widget/ViewAnimator.html#) that will animate between two or more views that have been added to it. | | [ViewSwitcher](https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher.html#) | [ViewAnimator](https://developer.android.com/reference/kotlin/android/widget/ViewAnimator.html#) that switches between two views, and has a factory from which these views are created. | | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView.html#) | A View that displays web pages. | | [ZoomControls](https://developer.android.com/reference/kotlin/android/widget/ZoomControls.html#) | The`ZoomControls`class displays a simple set of controls used for zooming and provides callbacks to register for events. | |

Defines the responsibilities for a class that will be a parent of a View. This is the API that a view sees when it wants to interact with its parent.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bringChildToFront](https://developer.android.com/reference/kotlin/android/view/ViewParent#bringChildToFront(android.view.View))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Change the z order of the child so it's on top of all other children. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canResolveLayoutDirection](https://developer.android.com/reference/kotlin/android/view/ViewParent#canResolveLayoutDirection())`()` Tells if this view parent can resolve the layout direction. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canResolveTextAlignment](https://developer.android.com/reference/kotlin/android/view/ViewParent#canResolveTextAlignment())`()` Tells if this view parent can resolve the text alignment. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canResolveTextDirection](https://developer.android.com/reference/kotlin/android/view/ViewParent#canResolveTextDirection())`()` Tells if this view parent can resolve the text direction. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [childDrawableStateChanged](https://developer.android.com/reference/kotlin/android/view/ViewParent#childDrawableStateChanged(android.view.View))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`)` This method is called on the parent when a child's drawable state has changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [childHasTransientStateChanged](https://developer.android.com/reference/kotlin/android/view/ViewParent#childHasTransientStateChanged(android.view.View,%20kotlin.Boolean))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `hasTransientState:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when a child view now has or no longer is tracking transient state. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearChildFocus](https://developer.android.com/reference/kotlin/android/view/ViewParent#clearChildFocus(android.view.View))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Called when a child of this parent is giving up focus |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createContextMenu](https://developer.android.com/reference/kotlin/android/view/ViewParent#createContextMenu(android.view.ContextMenu))`(`menu:` ` [ContextMenu](https://developer.android.com/reference/kotlin/android/view/ContextMenu)!`)` Have the parent populate the specified context menu if it has anything to add (and then recurse on its parent). |
| open [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#)? | [findOnBackInvokedDispatcherForChild](https://developer.android.com/reference/kotlin/android/view/ViewParent#findOnBackInvokedDispatcherForChild(android.view.View,%20android.view.View))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `requester:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`)` Walk up the View hierarchy to find the nearest [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#). |
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View)! | [focusSearch](https://developer.android.com/reference/kotlin/android/view/ViewParent#focusSearch(android.view.View,%20kotlin.Int))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Find the nearest view in the specified direction that wants to take focus |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [focusableViewAvailable](https://developer.android.com/reference/kotlin/android/view/ViewParent#focusableViewAvailable(android.view.View))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Tells the parent that a new focusable view has become available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getChildVisibleRect](https://developer.android.com/reference/kotlin/android/view/ViewParent#getChildVisibleRect(android.view.View,%20android.graphics.Rect,%20android.graphics.Point))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `r:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`, `offset:` ` [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)!`)` Compute the visible part of a rectangular region defined in terms of a child view's coordinates. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](https://developer.android.com/reference/kotlin/android/view/ViewParent#getLayoutDirection())`()` Return this view parent layout direction. |
| abstract [ViewParent](https://developer.android.com/reference/kotlin/android/view/ViewParent#)! | [getParent](https://developer.android.com/reference/kotlin/android/view/ViewParent#getParent())`()` Returns the parent if it exists, or null. |
| abstract [ViewParent](https://developer.android.com/reference/kotlin/android/view/ViewParent#)! | [getParentForAccessibility](https://developer.android.com/reference/kotlin/android/view/ViewParent#getParentForAccessibility())`()` Gets the parent of a given View for accessibility. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextAlignment](https://developer.android.com/reference/kotlin/android/view/ViewParent#getTextAlignment())`()` Return this view parent text alignment. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextDirection](https://developer.android.com/reference/kotlin/android/view/ViewParent#getTextDirection())`()` Return this view parent text direction. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateChild](https://developer.android.com/reference/kotlin/android/view/ViewParent#invalidateChild(android.view.View,%20android.graphics.Rect))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `r:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` All or part of a child is dirty and needs to be redrawn. |
| abstract [ViewParent](https://developer.android.com/reference/kotlin/android/view/ViewParent#)! | [invalidateChildInParent](https://developer.android.com/reference/kotlin/android/view/ViewParent#invalidateChildInParent(kotlin.IntArray,%20android.graphics.Rect))`(`location:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `r:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` All or part of a child is dirty and needs to be redrawn. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLayoutDirectionResolved](https://developer.android.com/reference/kotlin/android/view/ViewParent#isLayoutDirectionResolved())`()` Tells if this view parent layout direction is resolved. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLayoutRequested](https://developer.android.com/reference/kotlin/android/view/ViewParent#isLayoutRequested())`()` Indicates whether layout was requested on this view parent. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTextAlignmentResolved](https://developer.android.com/reference/kotlin/android/view/ViewParent#isTextAlignmentResolved())`()` Tells if this view parent text alignment is resolved. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTextDirectionResolved](https://developer.android.com/reference/kotlin/android/view/ViewParent#isTextDirectionResolved())`()` Tells if this view parent text direction is resolved. |
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View)! | [keyboardNavigationClusterSearch](https://developer.android.com/reference/kotlin/android/view/ViewParent#keyboardNavigationClusterSearch(android.view.View,%20kotlin.Int))`(`currentCluster:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Find the nearest keyboard navigation cluster in the specified direction. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifySubtreeAccessibilityStateChanged](https://developer.android.com/reference/kotlin/android/view/ViewParent#notifySubtreeAccessibilityStateChanged(android.view.View,%20android.view.View,%20kotlin.Int))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `source:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `changeType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notifies a view parent that the accessibility state of one of its descendants has changed and that the structure of the subtree is different. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDescendantInvalidated](https://developer.android.com/reference/kotlin/android/view/ViewParent#onDescendantInvalidated(android.view.View,%20android.view.View))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `target:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`)` The target View has been invalidated, or has had a drawing property changed that requires the hierarchy to re-render. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onNestedFling](https://developer.android.com/reference/kotlin/android/view/ViewParent#onNestedFling(android.view.View,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean))`(`target:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `velocityX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `velocityY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `consumed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Request a fling from a nested scroll. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onNestedPreFling](https://developer.android.com/reference/kotlin/android/view/ViewParent#onNestedPreFling(android.view.View,%20kotlin.Float,%20kotlin.Float))`(`target:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `velocityX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `velocityY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` React to a nested fling before the target view consumes it. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onNestedPrePerformAccessibilityAction](https://developer.android.com/reference/kotlin/android/view/ViewParent#onNestedPrePerformAccessibilityAction(android.view.View,%20kotlin.Int,%20android.os.Bundle))`(`target:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arguments:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` React to an accessibility action delegated by a target descendant view before the target processes it. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNestedPreScroll](https://developer.android.com/reference/kotlin/android/view/ViewParent#onNestedPreScroll(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.IntArray))`(`target:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `dx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `consumed:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` React to a nested scroll in progress before the target view consumes a portion of the scroll. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNestedScroll](https://developer.android.com/reference/kotlin/android/view/ViewParent#onNestedScroll(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`target:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `dxConsumed:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dyConsumed:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dxUnconsumed:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dyUnconsumed:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` React to a nested scroll in progress. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNestedScrollAccepted](https://developer.android.com/reference/kotlin/android/view/ViewParent#onNestedScrollAccepted(android.view.View,%20android.view.View,%20kotlin.Int))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `target:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `nestedScrollAxes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` React to the successful claiming of a nested scroll operation. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStartNestedScroll](https://developer.android.com/reference/kotlin/android/view/ViewParent#onStartNestedScroll(android.view.View,%20android.view.View,%20kotlin.Int))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `target:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `nestedScrollAxes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` React to a descendant view initiating a nestable scroll operation, claiming the nested scroll operation if appropriate. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopNestedScroll](https://developer.android.com/reference/kotlin/android/view/ViewParent#onStopNestedScroll(android.view.View))`(`target:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`)` React to a nested scroll operation ending. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recomputeViewAttributes](https://developer.android.com/reference/kotlin/android/view/ViewParent#recomputeViewAttributes(android.view.View))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Tell view hierarchy that the global view attributes need to be re-evaluated. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestChildFocus](https://developer.android.com/reference/kotlin/android/view/ViewParent#requestChildFocus(android.view.View,%20android.view.View))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `focused:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Called when a child of this parent wants focus |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requestChildRectangleOnScreen](https://developer.android.com/reference/kotlin/android/view/ViewParent#requestChildRectangleOnScreen(android.view.View,%20android.graphics.Rect,%20kotlin.Boolean))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `rectangle:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`, `immediate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when a child of this group wants a particular rectangle to be positioned onto the screen. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requestChildRectangleOnScreen](https://developer.android.com/reference/kotlin/android/view/ViewParent#requestChildRectangleOnScreen(android.view.View,%20android.graphics.Rect,%20kotlin.Boolean,%20kotlin.Int))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `rectangle:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`, `immediate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a child of this group wants a particular rectangle to be positioned onto the screen. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestDisallowInterceptTouchEvent](https://developer.android.com/reference/kotlin/android/view/ViewParent#requestDisallowInterceptTouchEvent(kotlin.Boolean))`(`disallowIntercept:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when a child does not want this parent and its ancestors to intercept touch events with [ViewGroup.onInterceptTouchEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/ViewGroup#onInterceptTouchEvent(android.view.MotionEvent)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestFitSystemWindows](https://developer.android.com/reference/kotlin/android/view/ViewParent#requestFitSystemWindows())`()` Ask that a new dispatch of [View.fitSystemWindows(Rect)](https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect))be performed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLayout](https://developer.android.com/reference/kotlin/android/view/ViewParent#requestLayout())`()` Called when something has changed which has invalidated the layout of a child of this view parent. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requestSendAccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/ViewParent#requestSendAccessibilityEvent(android.view.View,%20android.view.accessibility.AccessibilityEvent))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `event:` ` [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent)!`)` Called by a child to request from its parent to send an [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestTransparentRegion](https://developer.android.com/reference/kotlin/android/view/ViewParent#requestTransparentRegion(android.view.View))`(`child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Called when a child wants the view hierarchy to gather and report transparent regions to the window compositor. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [showContextMenuForChild](https://developer.android.com/reference/kotlin/android/view/ViewParent#showContextMenuForChild(android.view.View))`(`originalView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Shows the context menu for the specified view or its ancestors. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [showContextMenuForChild](https://developer.android.com/reference/kotlin/android/view/ViewParent#showContextMenuForChild(android.view.View,%20kotlin.Float,%20kotlin.Float))`(`originalView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Shows the context menu for the specified view or its ancestors anchored to the specified view-relative coordinate. |
| abstract [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)! | [startActionModeForChild](https://developer.android.com/reference/kotlin/android/view/ViewParent#startActionModeForChild(android.view.View,%20android.view.ActionMode.Callback))`(`originalView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `callback:` ` [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback)!`)` Start an action mode for the specified view with the default type [ActionMode.TYPE_PRIMARY](https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int). |
| abstract [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)! | [startActionModeForChild](https://developer.android.com/reference/kotlin/android/view/ViewParent#startActionModeForChild(android.view.View,%20android.view.ActionMode.Callback,%20kotlin.Int))`(`originalView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `callback:` ` [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback)!`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start an action mode of a specific type for the specified view. |

## Public methods

### bringChildToFront

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun bringChildToFront(child: View!): Unit
```

Change the z order of the child so it's on top of all other children. This ordering change may affect layout, if this container uses an order-dependent layout scheme (e.g., LinearLayout). Prior to [android.os.Build.VERSION_CODES#KITKAT](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int) this method should be followed by calls to [requestLayout()](https://developer.android.com/reference/kotlin/android/view/ViewParent#requestLayout())and [View.invalidate()](https://developer.android.com/reference/kotlin/android/view/View#invalidate())on this parent to force the parent to redraw with the new child ordering.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The child to bring to the top of the z order |

### canResolveLayoutDirection

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun canResolveLayoutDirection(): Boolean
```

Tells if this view parent can resolve the layout direction. See [View.setLayoutDirection(int)](https://developer.android.com/reference/kotlin/android/view/View#setLayoutDirection(kotlin.Int))

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this view parent can resolve the layout direction. |

### canResolveTextAlignment

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun canResolveTextAlignment(): Boolean
```

Tells if this view parent can resolve the text alignment. See [View.setTextAlignment(int)](https://developer.android.com/reference/kotlin/android/view/View#setTextAlignment(kotlin.Int))

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this view parent can resolve the text alignment. |

### canResolveTextDirection

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun canResolveTextDirection(): Boolean
```

Tells if this view parent can resolve the text direction. See [View.setTextDirection(int)](https://developer.android.com/reference/kotlin/android/view/View#setTextDirection(kotlin.Int))

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
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View):The child whose drawable state has changed. This value cannot be`null`. |

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
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View):Child view whose state has changed This value cannot be`null`. |
| `hasTransientState` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if this child has transient state |

### clearChildFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearChildFocus(child: View!): Unit
```

Called when a child of this parent is giving up focus

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view that is giving up focus |

### createContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createContextMenu(menu: ContextMenu!): Unit
```

Have the parent populate the specified context menu if it has anything to add (and then recurse on its parent).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `menu` | [ContextMenu](https://developer.android.com/reference/kotlin/android/view/ContextMenu)!:The menu to populate |

### findOnBackInvokedDispatcherForChild

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findOnBackInvokedDispatcherForChild(
    child: View, 
    requester: View
): OnBackInvokedDispatcher?
```

Walk up the View hierarchy to find the nearest [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View):The direct child of this view for which to find a dispatcher. This value cannot be`null`. |
| `requester` | [View](https://developer.android.com/reference/kotlin/android/view/View):The requester that will use the dispatcher. Can be the same as child. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#)? | The [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#) from this or the nearest ancestor, or null if the view is both not attached and have no ancestor providing an [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#). |

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
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view that currently has focus |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of FOCUS_UP, FOCUS_DOWN, FOCUS_LEFT, and FOCUS_RIGHT |

### focusableViewAvailable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun focusableViewAvailable(v: View!): Unit
```

Tells the parent that a new focusable view has become available. This is to handle transitions from the case where there are no focusable views to the case where the first focusable view appears.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view that has become newly focusable |

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
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:A child View, whose rectangular visible region we want to compute |
| `r` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:The input rectangle, defined in the child coordinate system. Will be overwritten to contain the resulting visible rectangle, expressed in global (root) coordinates |
| `offset` | [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)!:The input coordinates of a point, defined in the child coordinate system. As with the`r`parameter, this will be overwritten to contain the global (root) coordinates of that point. A`null`value is valid (in case you are not interested in this result) |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting rectangle is not empty, false otherwise |

### getLayoutDirection

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLayoutDirection(): Int
```

Return this view parent layout direction. See [View.getLayoutDirection()](https://developer.android.com/reference/kotlin/android/view/View#getLayoutDirection())

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [View.LAYOUT_DIRECTION_RTL](https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_RTL:kotlin.Int) if the layout direction is RTL or returns [View.LAYOUT_DIRECTION_LTR](https://developer.android.com/reference/kotlin/android/view/View#LAYOUT_DIRECTION_LTR:kotlin.Int) if the layout direction is not RTL. |

### getParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParent(): ViewParent!
```

Returns the parent if it exists, or null.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [ViewParent](https://developer.android.com/reference/kotlin/android/view/ViewParent#)! | a ViewParent or null if this ViewParent does not have a parent |

### getParentForAccessibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParentForAccessibility(): ViewParent!
```

Gets the parent of a given View for accessibility. Since some Views are not exposed to the accessibility layer the parent for accessibility is not necessarily the direct parent of the View, rather it is a predecessor.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------|
| [ViewParent](https://developer.android.com/reference/kotlin/android/view/ViewParent#)! | The parent or`null`if no such is found. |

### getTextAlignment

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTextAlignment(): Int
```

Return this view parent text alignment. See [android.view.View#getTextAlignment()](https://developer.android.com/reference/kotlin/android/view/View#getTextAlignment())

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the resolved text alignment. Returns one of: [View.TEXT_ALIGNMENT_GRAVITY](https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_GRAVITY:kotlin.Int), [View.TEXT_ALIGNMENT_CENTER](https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_CENTER:kotlin.Int), [View.TEXT_ALIGNMENT_TEXT_START](https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_START:kotlin.Int), [View.TEXT_ALIGNMENT_TEXT_END](https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_TEXT_END:kotlin.Int), [View.TEXT_ALIGNMENT_VIEW_START](https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_START:kotlin.Int), [View.TEXT_ALIGNMENT_VIEW_END](https://developer.android.com/reference/kotlin/android/view/View#TEXT_ALIGNMENT_VIEW_END:kotlin.Int) |

### getTextDirection

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTextDirection(): Int
```

Return this view parent text direction. See [View.getTextDirection()](https://developer.android.com/reference/kotlin/android/view/View#getTextDirection())

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the resolved text direction. Returns one of: [View.TEXT_DIRECTION_FIRST_STRONG](https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_FIRST_STRONG:kotlin.Int) [View.TEXT_DIRECTION_ANY_RTL](https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_ANY_RTL:kotlin.Int), [View.TEXT_DIRECTION_LTR](https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_LTR:kotlin.Int), [View.TEXT_DIRECTION_RTL](https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_RTL:kotlin.Int), [View.TEXT_DIRECTION_LOCALE](https://developer.android.com/reference/kotlin/android/view/View#TEXT_DIRECTION_LOCALE:kotlin.Int) |

### invalidateChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun invalidateChild(
    child: View!, 
    r: Rect!
): Unit
```

**Deprecated:** *Use [onDescendantInvalidated(android.view.View,android.view.View)](https://developer.android.com/reference/kotlin/android/view/ViewParent#onDescendantInvalidated(android.view.View,%20android.view.View))instead.*

All or part of a child is dirty and needs to be redrawn.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The child which is dirty |
| `r` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:The area within the child that is invalid |

### invalidateChildInParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun invalidateChildInParent(
    location: IntArray!, 
    r: Rect!
): ViewParent!
```

**Deprecated:** *Use [onDescendantInvalidated(android.view.View,android.view.View)](https://developer.android.com/reference/kotlin/android/view/ViewParent#onDescendantInvalidated(android.view.View,%20android.view.View))instead.*

All or part of a child is dirty and needs to be redrawn.

The location array is an array of two int values which respectively define the left and the top position of the dirty child.

This method must return the parent of this ViewParent if the specified rectangle must be invalidated in the parent. If the specified rectangle does not require invalidation in the parent or if the parent does not exist, this method must return null.

When this method returns a non-null value, the location array must have been updated with the left and top coordinates of this ViewParent.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `location` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:An array of 2 ints containing the left and top coordinates of the child to invalidate |
| `r` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:The area within the child that is invalid |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------|
| [ViewParent](https://developer.android.com/reference/kotlin/android/view/ViewParent#)! | the parent of this ViewParent or null |

### isLayoutDirectionResolved

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isLayoutDirectionResolved(): Boolean
```

Tells if this view parent layout direction is resolved. See [View.setLayoutDirection(int)](https://developer.android.com/reference/kotlin/android/view/View#setLayoutDirection(kotlin.Int))

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

Tells if this view parent text alignment is resolved. See [View.setTextAlignment(int)](https://developer.android.com/reference/kotlin/android/view/View#setTextAlignment(kotlin.Int))

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this view parent text alignment is resolved. |

### isTextDirectionResolved

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isTextDirectionResolved(): Boolean
```

Tells if this view parent text direction is resolved. See [View.setTextDirection(int)](https://developer.android.com/reference/kotlin/android/view/View#setTextDirection(kotlin.Int))

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
| `currentCluster` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The starting point of the search. Null means the current cluster is not found yet |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Direction to look |

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View)! | The nearest keyboard navigation cluster in the specified direction, or null if none can be found |

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
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View):The direct child whose subtree has changed. This value cannot be`null`. |
| `source` | [View](https://developer.android.com/reference/kotlin/android/view/View):The descendant view that changed. May not be`null`. |
| `changeType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bit mask of the types of changes that occurred. One or more of: - [AccessibilityEvent.CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION:kotlin.Int) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_STATE_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION:kotlin.Int) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_SUBTREE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_SUBTREE:kotlin.Int) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_TEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_TEXT:kotlin.Int) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_UNDEFINED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_UNDEFINED:kotlin.Int) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_DRAG_STARTED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_STARTED:kotlin.Int) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_DRAG_CANCELLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_CANCELLED:kotlin.Int) - [AccessibilityEvent.CONTENT_CHANGE_TYPE_DRAG_DROPPED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_DROPPED:kotlin.Int) |

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
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View):Direct child of this ViewParent containing target This value cannot be`null`. |
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View):The view that needs to redraw This value cannot be`null`. |

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

This method signifies that a nested scrolling child has detected suitable conditions for a fling. Generally this means that a touch scroll has ended with a [velocity](https://developer.android.com/reference/kotlin/android/view/VelocityTracker) in the direction of scrolling that meets or exceeds the [minimum fling velocity](https://developer.android.com/reference/kotlin/android/view/ViewConfiguration#getScaledMinimumFlingVelocity())along a scrollable axis.

If a nested scrolling child view would normally fling but it is at the edge of its own content, it can use this method to delegate the fling to its nested scrolling parent instead. The parent may optionally consume the fling or observe a child fling.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View):View that initiated the nested scroll This value cannot be`null`. |
| `velocityX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Horizontal velocity in pixels per second |
| `velocityY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Vertical velocity in pixels per second |
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

This method siginfies that a nested scrolling child has detected a fling with the given velocity along each axis. Generally this means that a touch scroll has ended with a [velocity](https://developer.android.com/reference/kotlin/android/view/VelocityTracker) in the direction of scrolling that meets or exceeds the [minimum fling velocity](https://developer.android.com/reference/kotlin/android/view/ViewConfiguration#getScaledMinimumFlingVelocity())along a scrollable axis.

If a nested scrolling parent is consuming motion as part of a [pre-scroll](https://developer.android.com/reference/kotlin/android/view/ViewParent#onNestedPreScroll(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.IntArray)), it may be appropriate for it to also consume the pre-fling to complete that same motion. By returning`true`from this method, the parent indicates that the child should not fling its own internal content as well.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View):View that initiated the nested scroll This value cannot be`null`. |
| `velocityX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Horizontal velocity in pixels per second |
| `velocityY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Vertical velocity in pixels per second |

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

This method may be called by a target descendant view if the target wishes to give a view in its parent chain a chance to react to the event before normal processing occurs. Most commonly this will be a scroll event such as [android.view.accessibility.AccessibilityNodeInfo#ACTION_SCROLL_FORWARD](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SCROLL_FORWARD:kotlin.Int). A ViewParent that supports acting as a nested scrolling parent should override this method and act accordingly to implement scrolling via accesibility systems.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View):The target view dispatching this action This value cannot be`null`. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Action being performed; see [android.view.accessibility.AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) |
| `arguments` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Optional action arguments This value may be`null`. |

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
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View):View that initiated the nested scroll This value cannot be`null`. |
| `dx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Horizontal scroll distance in pixels |
| `dy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Vertical scroll distance in pixels |
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

This method will be called when the ViewParent's current nested scrolling child view dispatches a nested scroll event. To receive calls to this method the ViewParent must have previously returned`true`for a call to [onStartNestedScroll(android.view.View,android.view.View,int)](https://developer.android.com/reference/kotlin/android/view/ViewParent#onStartNestedScroll(android.view.View,%20android.view.View,%20kotlin.Int)).

Both the consumed and unconsumed portions of the scroll distance are reported to the ViewParent. An implementation may choose to use the consumed portion to match or chase scroll position of multiple child elements, for example. The unconsumed portion may be used to allow continuous dragging of multiple scrolling or draggable elements, such as scrolling a list within a vertical drawer where the drawer begins dragging once the edge of inner scrolling content is reached.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View):The descendent view controlling the nested scroll This value cannot be`null`. |
| `dxConsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Horizontal scroll distance in pixels already consumed by target |
| `dyConsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Vertical scroll distance in pixels already consumed by target |
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

This method will be called after [onStartNestedScroll](https://developer.android.com/reference/kotlin/android/view/ViewParent#onStartNestedScroll(android.view.View,%20android.view.View,%20kotlin.Int))returns true. It offers an opportunity for the view and its superclasses to perform initial configuration for the nested scroll. Implementations of this method should always call their superclass's implementation of this method if one is present.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View):Direct child of this ViewParent containing target This value cannot be`null`. |
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View):View that initiated the nested scroll This value cannot be`null`. |
| `nestedScrollAxes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags consisting of [View.SCROLL_AXIS_HORIZONTAL](https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_HORIZONTAL:kotlin.Int), [View.SCROLL_AXIS_VERTICAL](https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_VERTICAL:kotlin.Int) or both |

**See Also**

- [#onStartNestedScroll(View, View, int)](https://developer.android.com/reference/kotlin/android/view/ViewParent#onStartNestedScroll(android.view.View,%20android.view.View,%20kotlin.Int))
- [#onStopNestedScroll(View)](https://developer.android.com/reference/kotlin/android/view/ViewParent#onStopNestedScroll(android.view.View)) 

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

This method will be called in response to a descendant view invoking [View.startNestedScroll(int)](https://developer.android.com/reference/kotlin/android/view/View#startNestedScroll(kotlin.Int)). Each parent up the view hierarchy will be given an opportunity to respond and claim the nested scrolling operation by returning`true`.

This method may be overridden by ViewParent implementations to indicate when the view is willing to support a nested scrolling operation that is about to begin. If it returns true, this ViewParent will become the target view's nested scrolling parent for the duration of the scroll operation in progress. When the nested scroll is finished this ViewParent will receive a call to [onStopNestedScroll(android.view.View)](https://developer.android.com/reference/kotlin/android/view/ViewParent#onStopNestedScroll(android.view.View)).

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View):Direct child of this ViewParent containing target This value cannot be`null`. |
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View):View that initiated the nested scroll This value cannot be`null`. |
| `nestedScrollAxes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags consisting of [View.SCROLL_AXIS_HORIZONTAL](https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_HORIZONTAL:kotlin.Int), [View.SCROLL_AXIS_VERTICAL](https://developer.android.com/reference/kotlin/android/view/View#SCROLL_AXIS_VERTICAL:kotlin.Int) or both |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this ViewParent accepts the nested scroll operation |

### onStopNestedScroll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStopNestedScroll(target: View): Unit
```

React to a nested scroll operation ending.

Perform cleanup after a nested scrolling operation. This method will be called when a nested scroll stops, for example when a nested touch scroll ends with a [MotionEvent.ACTION_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_UP:kotlin.Int) or [MotionEvent.ACTION_CANCEL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_CANCEL:kotlin.Int) event. Implementations of this method should always call their superclass's implementation of this method if one is present.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View):View that initiated the nested scroll This value cannot be`null`. |

### recomputeViewAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun recomputeViewAttributes(child: View!): Unit
```

Tell view hierarchy that the global view attributes need to be re-evaluated.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:View whose attributes have changed. |

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
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The child of this ViewParent that wants focus. This view will contain the focused view. It is not necessarily the view that actually has focus. |
| `focused` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view that is a descendant of child that actually has focus |

### requestChildRectangleOnScreen

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requestChildRectangleOnScreen(
    child: View, 
    rectangle: Rect!, 
    immediate: Boolean
): Boolean
```

Called when a child of this group wants a particular rectangle to be positioned onto the screen. [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup) s overriding this can trust that:

- `child`will be a direct child of this group
- `rectangle`will be in the child's content coordinates

<br />

[ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup) s overriding this should uphold the contract:

- nothing will change if the rectangle is already visible
- the view port will be scrolled only just enough to make the rectangle visible

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View):The direct child making the request. This value cannot be`null`. |
| `rectangle` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:The rectangle in the child's coordinates the child wishes to be on the screen. |
| `immediate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True to forbid animated or delayed scrolling, false otherwise |

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

Called when a child of this group wants a particular rectangle to be positioned onto the screen. [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup) s overriding this can trust that:

- `child`will be a direct child of this group
- `rectangle`will be in the child's content coordinates

<br />

[ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup) s overriding this should uphold the contract:

- nothing will change if the rectangle is already visible
- the view port will be scrolled only just enough to make the rectangle visible

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View):The direct child making the request. This value cannot be`null`. |
| `rectangle` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#):The rectangle in the child's coordinates the child wishes to be on the screen. This value cannot be`null`. |
| `immediate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True to forbid animated or delayed scrolling, false otherwise |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The parameter for the source of this request. Value is [android.view.View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED](https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED:kotlin.Int), [android.view.View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY](https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY:kotlin.Int), [android.view.View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR](https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR:kotlin.Int), or [android.view.View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS](https://developer.android.com/reference/kotlin/android/view/View#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the group scrolled to handle the operation |

### requestDisallowInterceptTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requestDisallowInterceptTouchEvent(disallowIntercept: Boolean): Unit
```

Called when a child does not want this parent and its ancestors to intercept touch events with [ViewGroup.onInterceptTouchEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/ViewGroup#onInterceptTouchEvent(android.view.MotionEvent)).

This parent should pass this call onto its parents. This parent must obey this request for the duration of the touch (that is, only clear the flag after this parent has received an up or a cancel.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `disallowIntercept` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the child does not want the parent to intercept touch events. |

### requestFitSystemWindows

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requestFitSystemWindows(): Unit
```

Ask that a new dispatch of [View.fitSystemWindows(Rect)](https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect))be performed. 

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

Called by a child to request from its parent to send an [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent). The child has already populated a record for itself in the event and is delegating to its parent to send the event. The parent can optionally add a record for itself.

Note: An accessibility event is fired by an individual view which populates the event with a record for its state and requests from its parent to perform the sending. The parent can optionally add a record for itself before dispatching the request to its parent. A parent can also choose not to respect the request for sending the event. The accessibility event is sent by the topmost view in the view tree.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View):The child which requests sending the event. This value cannot be`null`. |
| `event` | [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent)!:The event to be sent. |

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
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:the view requesting the transparent region computation |

### showContextMenuForChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun showContextMenuForChild(originalView: View!): Boolean
```

Shows the context menu for the specified view or its ancestors.

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, [ViewManager.addView(View, android.view.ViewGroup.LayoutParams)](https://developer.android.com/reference/kotlin/android/view/ViewManager#addView(android.view.View,%20android.view.ViewGroup.LayoutParams))) then it should override this and show the context menu.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| `originalView` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:the source view where the context menu was first invoked |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the context menu was shown,`false`otherwise |

**See Also**

- [#showContextMenuForChild(View, float, float)](https://developer.android.com/reference/kotlin/android/view/ViewParent#showContextMenuForChild(android.view.View,%20kotlin.Float,%20kotlin.Float)) 

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

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, [ViewManager.addView(View, android.view.ViewGroup.LayoutParams)](https://developer.android.com/reference/kotlin/android/view/ViewManager#addView(android.view.View,%20android.view.ViewGroup.LayoutParams))) then it should override this and show the context menu.

If a subclass overrides this method it should also override [showContextMenuForChild(android.view.View)](https://developer.android.com/reference/kotlin/android/view/ViewParent#showContextMenuForChild(android.view.View)).

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `originalView` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:the source view where the context menu was first invoked |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the X coordinate in pixels relative to the original view to which the menu should be anchored, or [Float.NaN](https://developer.android.com/reference/kotlin/java/lang/Float.html#NaN:kotlin.Float) to disable anchoring |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the Y coordinate in pixels relative to the original view to which the menu should be anchored, or [Float.NaN](https://developer.android.com/reference/kotlin/java/lang/Float.html#NaN:kotlin.Float) to disable anchoring |

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

Start an action mode for the specified view with the default type [ActionMode.TYPE_PRIMARY](https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int).

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, [ViewManager.addView(View, android.view.ViewGroup.LayoutParams)](https://developer.android.com/reference/kotlin/android/view/ViewManager#addView(android.view.View,%20android.view.ViewGroup.LayoutParams))) then it should override this and start the action mode.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `originalView` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The source view where the action mode was first invoked |
| `callback` | [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback)!:The callback that will handle lifecycle events for the action mode |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------|
| [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)! | The new action mode if it was started, null otherwise |

**See Also**

- [#startActionModeForChild(View, android.view.ActionMode.Callback, int)](https://developer.android.com/reference/kotlin/android/view/ViewParent#startActionModeForChild(android.view.View,%20android.view.ActionMode.Callback,%20kotlin.Int)) 

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

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, [ViewManager.addView(View, android.view.ViewGroup.LayoutParams)](https://developer.android.com/reference/kotlin/android/view/ViewManager#addView(android.view.View,%20android.view.ViewGroup.LayoutParams))) then it should override this and start the action mode.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `originalView` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The source view where the action mode was first invoked |
| `callback` | [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback)!:The callback that will handle lifecycle events for the action mode |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [ActionMode.TYPE_PRIMARY](https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int) or [ActionMode.TYPE_FLOATING](https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_FLOATING:kotlin.Int). |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------|
| [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)! | The new action mode if it was started, null otherwise |
