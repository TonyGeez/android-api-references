# android.widget

# android.widget

Kotlin| [Java](https://developer.android.com/reference/android/widget/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [MultiChoiceModeListener](https://developer.android.com/reference/kotlin/android/widget/AbsListView.MultiChoiceModeListener) | A MultiChoiceModeListener receives events for [AbsListView.CHOICE_MODE_MULTIPLE_MODAL](https://developer.android.com/reference/kotlin/android/widget/AbsListView#CHOICE_MODE_MULTIPLE_MODAL:kotlin.Int). |
| --- | --- |
| [OnScrollListener](https://developer.android.com/reference/kotlin/android/widget/AbsListView.OnScrollListener) | Interface definition for a callback to be invoked when the list or grid has been scrolled. |
| [RecyclerListener](https://developer.android.com/reference/kotlin/android/widget/AbsListView.RecyclerListener) | A RecyclerListener is used to receive a notification whenever a View is placed inside the RecycleBin's scrap heap. |
| [SelectionBoundsAdjuster](https://developer.android.com/reference/kotlin/android/widget/AbsListView.SelectionBoundsAdjuster) | The top-level view of a list item can implement this interface to allow itself to modify the bounds of the selection shown for that item. |
| --- | --- |
| [OnMenuItemClickListener](https://developer.android.com/reference/kotlin/android/widget/ActionMenuView.OnMenuItemClickListener) | Interface responsible for receiving menu item click events if the items themselves do not have individual item click listeners. |
| [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter) | An Adapter object acts as a bridge between an [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView) and the underlying data for that view. |
| [OnItemClickListener](https://developer.android.com/reference/kotlin/android/widget/AdapterView.OnItemClickListener) | Interface definition for a callback to be invoked when an item in this AdapterView has been clicked. |
| --- | --- |
| [OnItemLongClickListener](https://developer.android.com/reference/kotlin/android/widget/AdapterView.OnItemLongClickListener) | Interface definition for a callback to be invoked when an item in this view has been clicked and held. |
| [OnItemSelectedListener](https://developer.android.com/reference/kotlin/android/widget/AdapterView.OnItemSelectedListener) | Interface definition for a callback to be invoked when an item in this view has been selected. |
| [Advanceable](https://developer.android.com/reference/kotlin/android/widget/Advanceable) | This interface can be implemented by any collection-type view which has a notion of progressing through its set of children. |
| --- | --- |
| [OnDismissListener](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.OnDismissListener) | Listener to respond to the AutoCompleteTextView's completion list being dismissed. |
| [Validator](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.Validator) | This interface is used to make sure that the text entered in this TextView complies to a certain format. |
| [OnDateChangeListener](https://developer.android.com/reference/kotlin/android/widget/CalendarView.OnDateChangeListener) | The callback used to indicate the user changes the date. |
| --- | --- |
| [Checkable](https://developer.android.com/reference/kotlin/android/widget/Checkable) | Defines an extension for views that make them checkable. |
| [OnChronometerTickListener](https://developer.android.com/reference/kotlin/android/widget/Chronometer.OnChronometerTickListener) | A callback that notifies when the chronometer has incremented on its own. |
| [OnCheckedChangeListener](https://developer.android.com/reference/kotlin/android/widget/CompoundButton.OnCheckedChangeListener) | Interface definition for a callback to be invoked when the checked state of a compound button changed. |
| --- | --- |
| [OnDateChangedListener](https://developer.android.com/reference/kotlin/android/widget/DatePicker.OnDateChangedListener) | The callback used to indicate the user changed the date. |
| [ExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter) | An adapter that links a [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView) with the underlying data. |
| [OnChildClickListener](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.OnChildClickListener) | Interface definition for a callback to be invoked when a child in this expandable list has been clicked. |
| --- | --- |
| [OnGroupClickListener](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.OnGroupClickListener) | Interface definition for a callback to be invoked when a group in this expandable list has been clicked. |
| [OnGroupCollapseListener](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.OnGroupCollapseListener) | Used for being notified when a group is collapsed |
| [OnGroupExpandListener](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.OnGroupExpandListener) | Used for being notified when a group is expanded |
| --- | --- |
| [FilterListener](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterListener) | Listener used to receive a notification upon completion of a filtering operation. |
| [Filterable](https://developer.android.com/reference/kotlin/android/widget/Filterable) | Defines a filterable behavior. |
| [FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider) | This class can be used by external clients of CursorAdapter and CursorTreeAdapter to define how the content of the adapter should be filtered. |
| --- | --- |
| [HeterogeneousExpandableList](https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList) | Additional methods that when implemented make an [ExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter) take advantage of the [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter) view type mechanism. |
| [ListAdapter](https://developer.android.com/reference/kotlin/android/widget/ListAdapter) | Extended [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter) that is the bridge between a [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) and the data that backs the list. |
| [MediaPlayerControl](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl) | <br /> |
| --- | --- |
| [Tokenizer](https://developer.android.com/reference/kotlin/android/widget/MultiAutoCompleteTextView.Tokenizer) | <br /> |
| [Formatter](https://developer.android.com/reference/kotlin/android/widget/NumberPicker.Formatter) | Interface used to format current value into a string for presentation. |
| [OnScrollListener](https://developer.android.com/reference/kotlin/android/widget/NumberPicker.OnScrollListener) | Interface to listen for the picker scroll state. |
| --- | --- |
| [OnValueChangeListener](https://developer.android.com/reference/kotlin/android/widget/NumberPicker.OnValueChangeListener) | Interface to listen for changes of the current value. |
| [OnDismissListener](https://developer.android.com/reference/kotlin/android/widget/PopupMenu.OnDismissListener) | Callback interface used to notify the application that the menu has closed. |
| [OnMenuItemClickListener](https://developer.android.com/reference/kotlin/android/widget/PopupMenu.OnMenuItemClickListener) | Interface responsible for receiving menu item click events if the items themselves do not have individual item click listeners. |
| --- | --- |
| [OnDismissListener](https://developer.android.com/reference/kotlin/android/widget/PopupWindow.OnDismissListener) | Listener that is called when this popup window is dismissed. |
| [OnCheckedChangeListener](https://developer.android.com/reference/kotlin/android/widget/RadioGroup.OnCheckedChangeListener) | Interface definition for a callback to be invoked when the checked radio button changed in this group. |
| [OnRatingBarChangeListener](https://developer.android.com/reference/kotlin/android/widget/RatingBar.OnRatingBarChangeListener) | A callback that notifies clients when the rating has been changed. |
| --- | --- |
| [RemoteViewsFactory](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory) | An interface for an adapter between a remote collection view (ListView, GridView, etc) and the underlying data for that view. |
| [OnCloseListener](https://developer.android.com/reference/kotlin/android/widget/SearchView.OnCloseListener) | <br /> |
| [OnQueryTextListener](https://developer.android.com/reference/kotlin/android/widget/SearchView.OnQueryTextListener) | Callbacks for changes to the query text. |
| --- | --- |
| [OnSuggestionListener](https://developer.android.com/reference/kotlin/android/widget/SearchView.OnSuggestionListener) | Callback interface for selection events on suggestions. |
| [SectionIndexer](https://developer.android.com/reference/kotlin/android/widget/SectionIndexer) | Interface that may implemented on [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter) s to enable fast scrolling between sections of an [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView). |
| [OnSeekBarChangeListener](https://developer.android.com/reference/kotlin/android/widget/SeekBar.OnSeekBarChangeListener) | A callback that notifies clients when the progress level has been changed. |
| --- | --- |
| [OnShareTargetSelectedListener](https://developer.android.com/reference/kotlin/android/widget/ShareActionProvider.OnShareTargetSelectedListener) | Listener for the event of selecting a share target. |
| [ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter.ViewBinder) | This class can be used by external clients of SimpleAdapter to bind values to views. |
| [CursorToStringConverter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.CursorToStringConverter) | This class can be used by external clients of SimpleCursorAdapter to define how the Cursor should be converted to a String. |
| --- | --- |
| [ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.ViewBinder) | This class can be used by external clients of SimpleCursorAdapter to bind values fom the Cursor to views. |
| [ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorTreeAdapter.ViewBinder) | This class can be used by external clients of SimpleCursorTreeAdapter to bind values from the Cursor to views. |
| [OnDrawerCloseListener](https://developer.android.com/reference/kotlin/android/widget/SlidingDrawer.OnDrawerCloseListener) | Callback invoked when the drawer is closed. |
| --- | --- |
| [OnDrawerOpenListener](https://developer.android.com/reference/kotlin/android/widget/SlidingDrawer.OnDrawerOpenListener) | Callback invoked when the drawer is opened. |
| [OnDrawerScrollListener](https://developer.android.com/reference/kotlin/android/widget/SlidingDrawer.OnDrawerScrollListener) | Callback invoked when the drawer is scrolled. |
| [SpinnerAdapter](https://developer.android.com/reference/kotlin/android/widget/SpinnerAdapter) | Extended [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter) that is the bridge between a [android.widget.Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner) and its data. |
| --- | --- |
| [OnTabChangeListener](https://developer.android.com/reference/kotlin/android/widget/TabHost.OnTabChangeListener) | Interface definition for a callback to be invoked when tab changed |
| [TabContentFactory](https://developer.android.com/reference/kotlin/android/widget/TabHost.TabContentFactory) | Makes the content of a tab when it is selected. |
| [OnEditorActionListener](https://developer.android.com/reference/kotlin/android/widget/TextView.OnEditorActionListener) | Interface definition for a callback to be invoked when an action is performed on the editor. |
| --- | --- |
| [ThemedSpinnerAdapter](https://developer.android.com/reference/kotlin/android/widget/ThemedSpinnerAdapter) | An extension of SpinnerAdapter that is capable of inflating drop-down views against a different theme than normal views. |
| [OnTimeChangedListener](https://developer.android.com/reference/kotlin/android/widget/TimePicker.OnTimeChangedListener) | The callback interface used to indicate the time has been adjusted. |
| [OnMenuItemClickListener](https://developer.android.com/reference/kotlin/android/widget/Toolbar.OnMenuItemClickListener) | Interface responsible for receiving menu item click events if the items themselves do not have individual item click listeners. |
| --- | --- |
| [ViewFactory](https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher.ViewFactory) | Creates views in a ViewSwitcher. |
| [WrapperListAdapter](https://developer.android.com/reference/kotlin/android/widget/WrapperListAdapter) | List adapter that wraps another list adapter. |
| [OnZoomListener](https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController.OnZoomListener) | Interface that will be called when the user performs an interaction that triggers some action, for example zooming. |
| --- | --- |

## Classes

| [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView) | Base class that can be used to implement virtualized lists of items. |
| --- | --- |
| [AbsoluteLayout](https://developer.android.com/reference/kotlin/android/widget/AbsoluteLayout) | A layout that lets you specify exact locations (x/y coordinates) of its children. |
| [AbsSeekBar](https://developer.android.com/reference/kotlin/android/widget/AbsSeekBar) | AbsSeekBar extends the capabilities of ProgressBar by adding a draggable thumb. |
| [AbsSpinner](https://developer.android.com/reference/kotlin/android/widget/AbsSpinner) | An abstract base class for spinner widgets. |
| --- | --- |
| [ActionMenuView](https://developer.android.com/reference/kotlin/android/widget/ActionMenuView) | ActionMenuView is a presentation of a series of menu options as a View. |
| [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView) | An AdapterView is a view whose children are determined by an [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter). |
| [AdapterViewAnimator](https://developer.android.com/reference/kotlin/android/widget/AdapterViewAnimator) | Base class for a [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView) that will perform animations when switching between its views. |
| --- | --- |
| [AdapterViewFlipper](https://developer.android.com/reference/kotlin/android/widget/AdapterViewFlipper) | Simple [ViewAnimator](https://developer.android.com/reference/kotlin/android/widget/ViewAnimator) that will animate between two or more views that have been added to it. |
| [AlphabetIndexer](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer) | A helper class for adapters that implement the SectionIndexer interface. |
| [AnalogClock](https://developer.android.com/reference/kotlin/android/widget/AnalogClock) | This widget displays an analogic clock with two hands for hours and minutes. |
| --- | --- |
| [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter) | You can use this adapter to provide views for an [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) or [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner). |
| [AutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView) | An editable text view that shows completion suggestions automatically while the user is typing. |
| [BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) | Common base class of common implementation for an [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter) that can be used in both [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView)(by implementing the specialized [ListAdapter](https://developer.android.com/reference/kotlin/android/widget/ListAdapter) interface) and [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner)(by implementing the specialized [SpinnerAdapter](https://developer.android.com/reference/kotlin/android/widget/SpinnerAdapter) interface). |
| --- | --- |
| [BaseExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter) | Base class for a [ExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter) used to provide data and Views from some data to an expandable list view. |
| [Button](https://developer.android.com/reference/kotlin/android/widget/Button) | A user interface element the user can tap or click to perform an action. |
| [CalendarView](https://developer.android.com/reference/kotlin/android/widget/CalendarView) | This class is a calendar widget for displaying and selecting dates. |
| --- | --- |
| [CheckBox](https://developer.android.com/reference/kotlin/android/widget/CheckBox) | A checkbox is a specific type of two-states button that can be either checked or unchecked. |
| [CheckedTextView](https://developer.android.com/reference/kotlin/android/widget/CheckedTextView) | An extension to [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView) that supports the [Checkable](https://developer.android.com/reference/kotlin/android/widget/Checkable) interface and displays. |
| [Chronometer](https://developer.android.com/reference/kotlin/android/widget/Chronometer) | Class that implements a simple timer. |
| --- | --- |
| [CompoundButton](https://developer.android.com/reference/kotlin/android/widget/CompoundButton) | A button with two states, checked and unchecked. |
| [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter) | Adapter that exposes data from a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) to a [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) widget. |
| [CursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter) | An adapter that exposes data from a series of [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) s to an [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView) widget. |
| --- | --- |
| [DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker) | Provides a widget for selecting a date. |
| [DialerFilter](https://developer.android.com/reference/kotlin/android/widget/DialerFilter) | This widget is a layout that contains several specifically-named child views that handle keyboard entry interpreted as standard phone dialpad digits. |
| [DigitalClock](https://developer.android.com/reference/kotlin/android/widget/DigitalClock) | Like AnalogClock, but digital. |
| --- | --- |
| [EdgeEffect](https://developer.android.com/reference/kotlin/android/widget/EdgeEffect) | This class performs the graphical effect used at the edges of scrollable widgets when the user scrolls beyond the content bounds in 2D space. |
| [EditText](https://developer.android.com/reference/kotlin/android/widget/EditText) | A user interface element for entering and modifying text. |
| [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView) | A view that shows items in a vertically scrolling two-level list. |
| --- | --- |
| [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter) | A filter constrains data with a filtering pattern. |
| [FrameLayout](https://developer.android.com/reference/kotlin/android/widget/FrameLayout) | FrameLayout is designed to block out an area on the screen to display a single item. |
| [Gallery](https://developer.android.com/reference/kotlin/android/widget/Gallery) | A view that shows items in a center-locked, horizontally scrolling list. |
| --- | --- |
| [GridLayout](https://developer.android.com/reference/kotlin/android/widget/GridLayout) | A layout that places its children in a rectangular*grid*. |
| [GridView](https://developer.android.com/reference/kotlin/android/widget/GridView) | A view that shows items in two-dimensional scrolling grid. |
| [HeaderViewListAdapter](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter) | ListAdapter used when a ListView has header views. |
| --- | --- |
| [HorizontalScrollView](https://developer.android.com/reference/kotlin/android/widget/HorizontalScrollView) | Layout container for a view hierarchy that can be scrolled by the user, allowing it to be larger than the physical display. |
| [ImageButton](https://developer.android.com/reference/kotlin/android/widget/ImageButton) | Displays a button with an image (instead of text) that can be pressed or clicked by the user. |
| [ImageSwitcher](https://developer.android.com/reference/kotlin/android/widget/ImageSwitcher) | [ViewSwitcher](https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher) that switches between two ImageViews when a new image is set on it. |
| --- | --- |
| [ImageView](https://developer.android.com/reference/kotlin/android/widget/ImageView) | Displays image resources, for example [android.graphics.Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) or [android.graphics.drawable.Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) resources. |
| [LinearLayout](https://developer.android.com/reference/kotlin/android/widget/LinearLayout) | A layout that arranges other views either horizontally in a single column or vertically in a single row. |
| [ListPopupWindow](https://developer.android.com/reference/kotlin/android/widget/ListPopupWindow) | A ListPopupWindow anchors itself to a host view and displays a list of choices. |
| --- | --- |
| [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. |
| [Magnifier](https://developer.android.com/reference/kotlin/android/widget/Magnifier) | Android magnifier widget. |
| [MediaController](https://developer.android.com/reference/kotlin/android/widget/MediaController) | A view containing controls for a MediaPlayer. |
| --- | --- |
| [MultiAutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/MultiAutoCompleteTextView) | An editable text view, extending [AutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView), that can show completion suggestions for the substring of the text where the user is typing instead of necessarily for the entire thing. |
| [NumberPicker](https://developer.android.com/reference/kotlin/android/widget/NumberPicker) | A widget that enables the user to select a number from a predefined range. |
| [OverScroller](https://developer.android.com/reference/kotlin/android/widget/OverScroller) | This class encapsulates scrolling with the ability to overshoot the bounds of a scrolling operation. |
| --- | --- |
| [PopupMenu](https://developer.android.com/reference/kotlin/android/widget/PopupMenu) | A PopupMenu displays a [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#) in a modal popup window anchored to a [View](https://developer.android.com/reference/kotlin/android/view/View.html#). |
| [PopupWindow](https://developer.android.com/reference/kotlin/android/widget/PopupWindow) | This class represents a popup window that can be used to display an arbitrary view. |
| [ProgressBar](https://developer.android.com/reference/kotlin/android/widget/ProgressBar) | A user interface element that indicates the progress of an operation. |
| --- | --- |
| [QuickContactBadge](https://developer.android.com/reference/kotlin/android/widget/QuickContactBadge) | Widget used to show an image with the standard QuickContact badge and on-click behavior. |
| [RadioButton](https://developer.android.com/reference/kotlin/android/widget/RadioButton) | A radio button is a two-states button that can be either checked or unchecked. |
| [RadioGroup](https://developer.android.com/reference/kotlin/android/widget/RadioGroup) | This class is used to create a multiple-exclusion scope for a set of radio buttons. |
| --- | --- |
| [RatingBar](https://developer.android.com/reference/kotlin/android/widget/RatingBar) | A RatingBar is an extension of SeekBar and ProgressBar that shows a rating in stars. |
| [RelativeLayout](https://developer.android.com/reference/kotlin/android/widget/RelativeLayout) | A Layout where the positions of the children can be described in relation to each other or to the parent. |
| [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews) | A class that describes a view hierarchy that can be displayed in another process. |
| --- | --- |
| [RemoteViewsService](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService) | The service to be connected to for a remote adapter to request RemoteViews. |
| [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter) | An easy adapter that creates views defined in an XML file. |
| [ResourceCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorTreeAdapter) | A fairly simple ExpandableListAdapter that creates views defined in an XML file. |
| --- | --- |
| [Scroller](https://developer.android.com/reference/kotlin/android/widget/Scroller) | This class encapsulates scrolling. |
| [ScrollView](https://developer.android.com/reference/kotlin/android/widget/ScrollView) | A view group that allows the view hierarchy placed within it to be scrolled. |
| [SearchView](https://developer.android.com/reference/kotlin/android/widget/SearchView) | A widget that provides a user interface for the user to enter a search query and submit a request to a search provider. |
| --- | --- |
| [SeekBar](https://developer.android.com/reference/kotlin/android/widget/SeekBar) | A SeekBar is an extension of ProgressBar that adds a draggable thumb. |
| [ShareActionProvider](https://developer.android.com/reference/kotlin/android/widget/ShareActionProvider) | This is a provider for a share action. |
| [SimpleAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter) | An easy adapter to map static data to views defined in an XML file. |
| --- | --- |
| [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. |
| [SimpleCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorTreeAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. |
| [SimpleExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter) | An easy adapter to map static data to group and child views defined in an XML file. |
| --- | --- |
| [SlidingDrawer](https://developer.android.com/reference/kotlin/android/widget/SlidingDrawer) | SlidingDrawer hides content out of the screen and allows the user to drag a handle to bring the content on screen. |
| [Space](https://developer.android.com/reference/kotlin/android/widget/Space) | Space is a lightweight View subclass that may be used to create gaps between components in general purpose layouts. |
| [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner) | A view that displays one child at a time and lets the user pick among them. |
| --- | --- |
| [StackView](https://developer.android.com/reference/kotlin/android/widget/StackView) | <br /> |
| [Switch](https://developer.android.com/reference/kotlin/android/widget/Switch) | A Switch is a two-state toggle widget. |
| [TabHost](https://developer.android.com/reference/kotlin/android/widget/TabHost) | Container for a tabbed window view. |
| --- | --- |
| [TableLayout](https://developer.android.com/reference/kotlin/android/widget/TableLayout) | A layout that arranges its children into rows and columns. |
| [TableRow](https://developer.android.com/reference/kotlin/android/widget/TableRow) | A layout that arranges its children horizontally. |
| [TabWidget](https://developer.android.com/reference/kotlin/android/widget/TabWidget) | Displays a list of tab labels representing each page in the parent's tab collection. |
| --- | --- |
| [TextClock](https://developer.android.com/reference/kotlin/android/widget/TextClock) | `TextClock`can display the current date and/or time as a formatted string. |
| [TextSwitcher](https://developer.android.com/reference/kotlin/android/widget/TextSwitcher) | Specialized [android.widget.ViewSwitcher](https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher) that contains only children of type [android.widget.TextView](https://developer.android.com/reference/kotlin/android/widget/TextView). |
| [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView) | A user interface element that displays text to the user. |
| --- | --- |
| [TimePicker](https://developer.android.com/reference/kotlin/android/widget/TimePicker) | A widget for selecting the time of day, in either 24-hour or AM/PM mode. |
| [Toast](https://developer.android.com/reference/kotlin/android/widget/Toast) | A toast is a view containing a quick little message for the user. |
| [ToggleButton](https://developer.android.com/reference/kotlin/android/widget/ToggleButton) | Displays checked/unchecked states as a button with a "light" indicator and by default accompanied with the text "ON" or "OFF". |
| --- | --- |
| [Toolbar](https://developer.android.com/reference/kotlin/android/widget/Toolbar) | A standard toolbar for use within application content. |
| [TwoLineListItem](https://developer.android.com/reference/kotlin/android/widget/TwoLineListItem) | A view group with two children, intended for use in ListViews. |
| [VideoView](https://developer.android.com/reference/kotlin/android/widget/VideoView) | Displays a video file. |
| --- | --- |
| [ViewAnimator](https://developer.android.com/reference/kotlin/android/widget/ViewAnimator) | Base class for a [FrameLayout](https://developer.android.com/reference/kotlin/android/widget/FrameLayout) container that will perform animations when switching between its views. |
| [ViewFlipper](https://developer.android.com/reference/kotlin/android/widget/ViewFlipper) | Simple [ViewAnimator](https://developer.android.com/reference/kotlin/android/widget/ViewAnimator) that will animate between two or more views that have been added to it. |
| [ViewSwitcher](https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher) | [ViewAnimator](https://developer.android.com/reference/kotlin/android/widget/ViewAnimator) that switches between two views, and has a factory from which these views are created. |
| --- | --- |
| [ZoomButton](https://developer.android.com/reference/kotlin/android/widget/ZoomButton) | This widget provides a simple utility for turning a continued long-press event into a series of clicks at some set frequency. |
| [ZoomButtonsController](https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController) | The [ZoomButtonsController](https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController) handles showing and hiding the zoom controls and positioning it relative to an owner view. |
| [ZoomControls](https://developer.android.com/reference/kotlin/android/widget/ZoomControls) | The`ZoomControls`class displays a simple set of controls used for zooming and provides callbacks to register for events. |
| --- | --- |
