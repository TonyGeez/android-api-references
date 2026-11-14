# android.widget

# android.widget

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [MultiChoiceModeListener](../android/widget/AbsListView.MultiChoiceModeListener.md) | A MultiChoiceModeListener receives events for [AbsListView.CHOICE_MODE_MULTIPLE_MODAL](AbsListView.md). |
| --- | --- |
| [OnScrollListener](../android/widget/AbsListView.OnScrollListener.md) | Interface definition for a callback to be invoked when the list or grid has been scrolled. |
| [RecyclerListener](../android/widget/AbsListView.RecyclerListener.md) | A RecyclerListener is used to receive a notification whenever a View is placed inside the RecycleBin's scrap heap. |
| [SelectionBoundsAdjuster](../android/widget/AbsListView.SelectionBoundsAdjuster.md) | The top-level view of a list item can implement this interface to allow itself to modify the bounds of the selection shown for that item. |
| --- | --- |
| [OnMenuItemClickListener](../android/widget/ActionMenuView.OnMenuItemClickListener.md) | Interface responsible for receiving menu item click events if the items themselves do not have individual item click listeners. |
| [Adapter](Adapter.md) | An Adapter object acts as a bridge between an [AdapterView](AdapterView.md) and the underlying data for that view. |
| [OnItemClickListener](../android/widget/AdapterView.OnItemClickListener.md) | Interface definition for a callback to be invoked when an item in this AdapterView has been clicked. |
| --- | --- |
| [OnItemLongClickListener](../android/widget/AdapterView.OnItemLongClickListener.md) | Interface definition for a callback to be invoked when an item in this view has been clicked and held. |
| [OnItemSelectedListener](../android/widget/AdapterView.OnItemSelectedListener.md) | Interface definition for a callback to be invoked when an item in this view has been selected. |
| [Advanceable](Advanceable.md) | This interface can be implemented by any collection-type view which has a notion of progressing through its set of children. |
| --- | --- |
| [OnDismissListener](../android/widget/AutoCompleteTextView.OnDismissListener.md) | Listener to respond to the AutoCompleteTextView's completion list being dismissed. |
| [Validator](../android/widget/AutoCompleteTextView.Validator.md) | This interface is used to make sure that the text entered in this TextView complies to a certain format. |
| [OnDateChangeListener](../android/widget/CalendarView.OnDateChangeListener.md) | The callback used to indicate the user changes the date. |
| --- | --- |
| [Checkable](Checkable.md) | Defines an extension for views that make them checkable. |
| [OnChronometerTickListener](../android/widget/Chronometer.OnChronometerTickListener.md) | A callback that notifies when the chronometer has incremented on its own. |
| [OnCheckedChangeListener](../android/widget/CompoundButton.OnCheckedChangeListener.md) | Interface definition for a callback to be invoked when the checked state of a compound button changed. |
| --- | --- |
| [OnDateChangedListener](../android/widget/DatePicker.OnDateChangedListener.md) | The callback used to indicate the user changed the date. |
| [ExpandableListAdapter](ExpandableListAdapter.md) | An adapter that links a [ExpandableListView](ExpandableListView.md) with the underlying data. |
| [OnChildClickListener](../android/widget/ExpandableListView.OnChildClickListener.md) | Interface definition for a callback to be invoked when a child in this expandable list has been clicked. |
| --- | --- |
| [OnGroupClickListener](../android/widget/ExpandableListView.OnGroupClickListener.md) | Interface definition for a callback to be invoked when a group in this expandable list has been clicked. |
| [OnGroupCollapseListener](../android/widget/ExpandableListView.OnGroupCollapseListener.md) | Used for being notified when a group is collapsed |
| [OnGroupExpandListener](../android/widget/ExpandableListView.OnGroupExpandListener.md) | Used for being notified when a group is expanded |
| --- | --- |
| [FilterListener](../android/widget/Filter.FilterListener.md) | Listener used to receive a notification upon completion of a filtering operation. |
| [Filterable](Filterable.md) | Defines a filterable behavior. |
| [FilterQueryProvider](FilterQueryProvider.md) | This class can be used by external clients of CursorAdapter and CursorTreeAdapter to define how the content of the adapter should be filtered. |
| --- | --- |
| [HeterogeneousExpandableList](HeterogeneousExpandableList.md) | Additional methods that when implemented make an [ExpandableListAdapter](ExpandableListAdapter.md) take advantage of the [Adapter](Adapter.md) view type mechanism. |
| [ListAdapter](ListAdapter.md) | Extended [Adapter](Adapter.md) that is the bridge between a [ListView](ListView.md) and the data that backs the list. |
| [MediaPlayerControl](../android/widget/MediaController.MediaPlayerControl.md) | <br /> |
| --- | --- |
| [Tokenizer](../android/widget/MultiAutoCompleteTextView.Tokenizer.md) | <br /> |
| [Formatter](../android/widget/NumberPicker.Formatter.md) | Interface used to format current value into a string for presentation. |
| [OnScrollListener](../android/widget/NumberPicker.OnScrollListener.md) | Interface to listen for the picker scroll state. |
| --- | --- |
| [OnValueChangeListener](../android/widget/NumberPicker.OnValueChangeListener.md) | Interface to listen for changes of the current value. |
| [OnDismissListener](../android/widget/PopupMenu.OnDismissListener.md) | Callback interface used to notify the application that the menu has closed. |
| [OnMenuItemClickListener](../android/widget/PopupMenu.OnMenuItemClickListener.md) | Interface responsible for receiving menu item click events if the items themselves do not have individual item click listeners. |
| --- | --- |
| [OnDismissListener](../android/widget/PopupWindow.OnDismissListener.md) | Listener that is called when this popup window is dismissed. |
| [OnCheckedChangeListener](../android/widget/RadioGroup.OnCheckedChangeListener.md) | Interface definition for a callback to be invoked when the checked radio button changed in this group. |
| [OnRatingBarChangeListener](../android/widget/RatingBar.OnRatingBarChangeListener.md) | A callback that notifies clients when the rating has been changed. |
| --- | --- |
| [RemoteViewsFactory](../android/widget/RemoteViewsService.RemoteViewsFactory.md) | An interface for an adapter between a remote collection view (ListView, GridView, etc) and the underlying data for that view. |
| [OnCloseListener](../android/widget/SearchView.OnCloseListener.md) | <br /> |
| [OnQueryTextListener](../android/widget/SearchView.OnQueryTextListener.md) | Callbacks for changes to the query text. |
| --- | --- |
| [OnSuggestionListener](../android/widget/SearchView.OnSuggestionListener.md) | Callback interface for selection events on suggestions. |
| [SectionIndexer](SectionIndexer.md) | Interface that may implemented on [Adapter](Adapter.md) s to enable fast scrolling between sections of an [AbsListView](AbsListView.md). |
| [OnSeekBarChangeListener](../android/widget/SeekBar.OnSeekBarChangeListener.md) | A callback that notifies clients when the progress level has been changed. |
| --- | --- |
| [OnShareTargetSelectedListener](../android/widget/ShareActionProvider.OnShareTargetSelectedListener.md) | Listener for the event of selecting a share target. |
| [ViewBinder](../android/widget/SimpleAdapter.ViewBinder.md) | This class can be used by external clients of SimpleAdapter to bind values to views. |
| [CursorToStringConverter](../android/widget/SimpleCursorAdapter.CursorToStringConverter.md) | This class can be used by external clients of SimpleCursorAdapter to define how the Cursor should be converted to a String. |
| --- | --- |
| [ViewBinder](../android/widget/SimpleCursorAdapter.ViewBinder.md) | This class can be used by external clients of SimpleCursorAdapter to bind values fom the Cursor to views. |
| [ViewBinder](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md) | This class can be used by external clients of SimpleCursorTreeAdapter to bind values from the Cursor to views. |
| [OnDrawerCloseListener](../android/widget/SlidingDrawer.OnDrawerCloseListener.md) | Callback invoked when the drawer is closed. |
| --- | --- |
| [OnDrawerOpenListener](../android/widget/SlidingDrawer.OnDrawerOpenListener.md) | Callback invoked when the drawer is opened. |
| [OnDrawerScrollListener](../android/widget/SlidingDrawer.OnDrawerScrollListener.md) | Callback invoked when the drawer is scrolled. |
| [SpinnerAdapter](SpinnerAdapter.md) | Extended [Adapter](Adapter.md) that is the bridge between a [android.widget.Spinner](Spinner.md) and its data. |
| --- | --- |
| [OnTabChangeListener](../android/widget/TabHost.OnTabChangeListener.md) | Interface definition for a callback to be invoked when tab changed |
| [TabContentFactory](../android/widget/TabHost.TabContentFactory.md) | Makes the content of a tab when it is selected. |
| [OnEditorActionListener](../android/widget/TextView.OnEditorActionListener.md) | Interface definition for a callback to be invoked when an action is performed on the editor. |
| --- | --- |
| [ThemedSpinnerAdapter](ThemedSpinnerAdapter.md) | An extension of SpinnerAdapter that is capable of inflating drop-down views against a different theme than normal views. |
| [OnTimeChangedListener](../android/widget/TimePicker.OnTimeChangedListener.md) | The callback interface used to indicate the time has been adjusted. |
| [OnMenuItemClickListener](../android/widget/Toolbar.OnMenuItemClickListener.md) | Interface responsible for receiving menu item click events if the items themselves do not have individual item click listeners. |
| --- | --- |
| [ViewFactory](../android/widget/ViewSwitcher.ViewFactory.md) | Creates views in a ViewSwitcher. |
| [WrapperListAdapter](WrapperListAdapter.md) | List adapter that wraps another list adapter. |
| [OnZoomListener](../android/widget/ZoomButtonsController.OnZoomListener.md) | Interface that will be called when the user performs an interaction that triggers some action, for example zooming. |
| --- | --- |

## Classes

| [AbsListView](AbsListView.md) | Base class that can be used to implement virtualized lists of items. |
| --- | --- |
| [AbsoluteLayout](AbsoluteLayout.md) | A layout that lets you specify exact locations (x/y coordinates) of its children. |
| [AbsSeekBar](AbsSeekBar.md) | AbsSeekBar extends the capabilities of ProgressBar by adding a draggable thumb. |
| [AbsSpinner](AbsSpinner.md) | An abstract base class for spinner widgets. |
| --- | --- |
| [ActionMenuView](ActionMenuView.md) | ActionMenuView is a presentation of a series of menu options as a View. |
| [AdapterView](AdapterView.md) | An AdapterView is a view whose children are determined by an [Adapter](Adapter.md). |
| [AdapterViewAnimator](AdapterViewAnimator.md) | Base class for a [AdapterView](AdapterView.md) that will perform animations when switching between its views. |
| --- | --- |
| [AdapterViewFlipper](AdapterViewFlipper.md) | Simple [ViewAnimator](ViewAnimator.md) that will animate between two or more views that have been added to it. |
| [AlphabetIndexer](AlphabetIndexer.md) | A helper class for adapters that implement the SectionIndexer interface. |
| [AnalogClock](AnalogClock.md) | This widget displays an analogic clock with two hands for hours and minutes. |
| --- | --- |
| [ArrayAdapter](ArrayAdapter.md) | You can use this adapter to provide views for an [AdapterView](AdapterView.md), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](ListView.md) or [Spinner](Spinner.md). |
| [AutoCompleteTextView](AutoCompleteTextView.md) | An editable text view that shows completion suggestions automatically while the user is typing. |
| [BaseAdapter](BaseAdapter.md) | Common base class of common implementation for an [Adapter](Adapter.md) that can be used in both [ListView](ListView.md)(by implementing the specialized [ListAdapter](ListAdapter.md) interface) and [Spinner](Spinner.md)(by implementing the specialized [SpinnerAdapter](SpinnerAdapter.md) interface). |
| --- | --- |
| [BaseExpandableListAdapter](BaseExpandableListAdapter.md) | Base class for a [ExpandableListAdapter](ExpandableListAdapter.md) used to provide data and Views from some data to an expandable list view. |
| [Button](Button.md) | A user interface element the user can tap or click to perform an action. |
| [CalendarView](CalendarView.md) | This class is a calendar widget for displaying and selecting dates. |
| --- | --- |
| [CheckBox](CheckBox.md) | A checkbox is a specific type of two-states button that can be either checked or unchecked. |
| [CheckedTextView](CheckedTextView.md) | An extension to [TextView](TextView.md) that supports the [Checkable](Checkable.md) interface and displays. |
| [Chronometer](Chronometer.md) | Class that implements a simple timer. |
| --- | --- |
| [CompoundButton](CompoundButton.md) | A button with two states, checked and unchecked. |
| [CursorAdapter](CursorAdapter.md) | Adapter that exposes data from a [Cursor](../android.database/Cursor.md) to a [ListView](ListView.md) widget. |
| [CursorTreeAdapter](CursorTreeAdapter.md) | An adapter that exposes data from a series of [Cursor](../android.database/Cursor.md) s to an [ExpandableListView](ExpandableListView.md) widget. |
| --- | --- |
| [DatePicker](DatePicker.md) | Provides a widget for selecting a date. |
| [DialerFilter](DialerFilter.md) | This widget is a layout that contains several specifically-named child views that handle keyboard entry interpreted as standard phone dialpad digits. |
| [DigitalClock](DigitalClock.md) | Like AnalogClock, but digital. |
| --- | --- |
| [EdgeEffect](EdgeEffect.md) | This class performs the graphical effect used at the edges of scrollable widgets when the user scrolls beyond the content bounds in 2D space. |
| [EditText](EditText.md) | A user interface element for entering and modifying text. |
| [ExpandableListView](ExpandableListView.md) | A view that shows items in a vertically scrolling two-level list. |
| --- | --- |
| [Filter](Filter.md) | A filter constrains data with a filtering pattern. |
| [FrameLayout](FrameLayout.md) | FrameLayout is designed to block out an area on the screen to display a single item. |
| [Gallery](Gallery.md) | A view that shows items in a center-locked, horizontally scrolling list. |
| --- | --- |
| [GridLayout](GridLayout.md) | A layout that places its children in a rectangular*grid*. |
| [GridView](GridView.md) | A view that shows items in two-dimensional scrolling grid. |
| [HeaderViewListAdapter](HeaderViewListAdapter.md) | ListAdapter used when a ListView has header views. |
| --- | --- |
| [HorizontalScrollView](HorizontalScrollView.md) | Layout container for a view hierarchy that can be scrolled by the user, allowing it to be larger than the physical display. |
| [ImageButton](ImageButton.md) | Displays a button with an image (instead of text) that can be pressed or clicked by the user. |
| [ImageSwitcher](ImageSwitcher.md) | [ViewSwitcher](ViewSwitcher.md) that switches between two ImageViews when a new image is set on it. |
| --- | --- |
| [ImageView](ImageView.md) | Displays image resources, for example [android.graphics.Bitmap](../android.graphics/Bitmap.md) or [android.graphics.drawable.Drawable](../android.graphics.drawable/Drawable.md) resources. |
| [LinearLayout](LinearLayout.md) | A layout that arranges other views either horizontally in a single column or vertically in a single row. |
| [ListPopupWindow](ListPopupWindow.md) | A ListPopupWindow anchors itself to a host view and displays a list of choices. |
| --- | --- |
| [ListView](ListView.md) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. |
| [Magnifier](Magnifier.md) | Android magnifier widget. |
| [MediaController](MediaController.md) | A view containing controls for a MediaPlayer. |
| --- | --- |
| [MultiAutoCompleteTextView](MultiAutoCompleteTextView.md) | An editable text view, extending [AutoCompleteTextView](AutoCompleteTextView.md), that can show completion suggestions for the substring of the text where the user is typing instead of necessarily for the entire thing. |
| [NumberPicker](NumberPicker.md) | A widget that enables the user to select a number from a predefined range. |
| [OverScroller](OverScroller.md) | This class encapsulates scrolling with the ability to overshoot the bounds of a scrolling operation. |
| --- | --- |
| [PopupMenu](PopupMenu.md) | A PopupMenu displays a [Menu](../android.view/Menu.md) in a modal popup window anchored to a [View](../android.view/View.md). |
| [PopupWindow](PopupWindow.md) | This class represents a popup window that can be used to display an arbitrary view. |
| [ProgressBar](ProgressBar.md) | A user interface element that indicates the progress of an operation. |
| --- | --- |
| [QuickContactBadge](QuickContactBadge.md) | Widget used to show an image with the standard QuickContact badge and on-click behavior. |
| [RadioButton](RadioButton.md) | A radio button is a two-states button that can be either checked or unchecked. |
| [RadioGroup](RadioGroup.md) | This class is used to create a multiple-exclusion scope for a set of radio buttons. |
| --- | --- |
| [RatingBar](RatingBar.md) | A RatingBar is an extension of SeekBar and ProgressBar that shows a rating in stars. |
| [RelativeLayout](RelativeLayout.md) | A Layout where the positions of the children can be described in relation to each other or to the parent. |
| [RemoteViews](RemoteViews.md) | A class that describes a view hierarchy that can be displayed in another process. |
| --- | --- |
| [RemoteViewsService](RemoteViewsService.md) | The service to be connected to for a remote adapter to request RemoteViews. |
| [ResourceCursorAdapter](ResourceCursorAdapter.md) | An easy adapter that creates views defined in an XML file. |
| [ResourceCursorTreeAdapter](ResourceCursorTreeAdapter.md) | A fairly simple ExpandableListAdapter that creates views defined in an XML file. |
| --- | --- |
| [Scroller](Scroller.md) | This class encapsulates scrolling. |
| [ScrollView](ScrollView.md) | A view group that allows the view hierarchy placed within it to be scrolled. |
| [SearchView](SearchView.md) | A widget that provides a user interface for the user to enter a search query and submit a request to a search provider. |
| --- | --- |
| [SeekBar](SeekBar.md) | A SeekBar is an extension of ProgressBar that adds a draggable thumb. |
| [ShareActionProvider](ShareActionProvider.md) | This is a provider for a share action. |
| [SimpleAdapter](SimpleAdapter.md) | An easy adapter to map static data to views defined in an XML file. |
| --- | --- |
| [SimpleCursorAdapter](SimpleCursorAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. |
| [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. |
| [SimpleExpandableListAdapter](SimpleExpandableListAdapter.md) | An easy adapter to map static data to group and child views defined in an XML file. |
| --- | --- |
| [SlidingDrawer](SlidingDrawer.md) | SlidingDrawer hides content out of the screen and allows the user to drag a handle to bring the content on screen. |
| [Space](Space.md) | Space is a lightweight View subclass that may be used to create gaps between components in general purpose layouts. |
| [Spinner](Spinner.md) | A view that displays one child at a time and lets the user pick among them. |
| --- | --- |
| [StackView](StackView.md) | <br /> |
| [Switch](Switch.md) | A Switch is a two-state toggle widget. |
| [TabHost](TabHost.md) | Container for a tabbed window view. |
| --- | --- |
| [TableLayout](TableLayout.md) | A layout that arranges its children into rows and columns. |
| [TableRow](TableRow.md) | A layout that arranges its children horizontally. |
| [TabWidget](TabWidget.md) | Displays a list of tab labels representing each page in the parent's tab collection. |
| --- | --- |
| [TextClock](TextClock.md) | `TextClock`can display the current date and/or time as a formatted string. |
| [TextSwitcher](TextSwitcher.md) | Specialized [android.widget.ViewSwitcher](ViewSwitcher.md) that contains only children of type [android.widget.TextView](TextView.md). |
| [TextView](TextView.md) | A user interface element that displays text to the user. |
| --- | --- |
| [TimePicker](TimePicker.md) | A widget for selecting the time of day, in either 24-hour or AM/PM mode. |
| [Toast](Toast.md) | A toast is a view containing a quick little message for the user. |
| [ToggleButton](ToggleButton.md) | Displays checked/unchecked states as a button with a "light" indicator and by default accompanied with the text "ON" or "OFF". |
| --- | --- |
| [Toolbar](Toolbar.md) | A standard toolbar for use within application content. |
| [TwoLineListItem](TwoLineListItem.md) | A view group with two children, intended for use in ListViews. |
| [VideoView](VideoView.md) | Displays a video file. |
| --- | --- |
| [ViewAnimator](ViewAnimator.md) | Base class for a [FrameLayout](FrameLayout.md) container that will perform animations when switching between its views. |
| [ViewFlipper](ViewFlipper.md) | Simple [ViewAnimator](ViewAnimator.md) that will animate between two or more views that have been added to it. |
| [ViewSwitcher](ViewSwitcher.md) | [ViewAnimator](ViewAnimator.md) that switches between two views, and has a factory from which these views are created. |
| --- | --- |
| [ZoomButton](ZoomButton.md) | This widget provides a simple utility for turning a continued long-press event into a series of clicks at some set frequency. |
| [ZoomButtonsController](ZoomButtonsController.md) | The [ZoomButtonsController](ZoomButtonsController.md) handles showing and hiding the zoom controls and positioning it relative to an owner view. |
| [ZoomControls](ZoomControls.md) | The`ZoomControls`class displays a simple set of controls used for zooming and provides callbacks to register for events. |
| --- | --- |
